---
title: Configurare il supporto per la casella in entrata in Web SDK
description: Scopri come creare una casella in entrata di messaggi persistenti in Adobe Journey Optimizer utilizzando le campagne Content Card (Scheda contenuto) e Inbox (Casella in entrata) con Adobe Experience Platform Web SDK.
feature: Content Cards
topic: Content Management
role: Developer
level: Experienced
source-git-commit: 4eb7013c2c3178caf7863ff36cb4c194c829e37c
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 0%

---

# Configurare il supporto per la casella in entrata in Web SDK {#inbox-configuration-sdk}

>[!BEGINSHADEBOX]

**In questa pagina:** Configura ed esegui un esempio che combina una campagna Scheda contenuto e una campagna Casella in entrata con Adobe Experience Platform Web SDK, in modo da poter inviare una casella in entrata di notifica persistente sul sito Web.

>[!ENDSHADEBOX]

Una casella in entrata dei messaggi è una casella in entrata di notifica persistente guidata da due campagne Adobe Journey Optimizer che hanno come target la stessa superficie:

* Una **campagna per schede di contenuto**, che consegna singoli elementi di notifica alla casella in entrata.
* Una **campagna Posta in arrivo**, che fornisce configurazioni quali titolo, copia in stato vuoto e layout.


## Configurare Adobe Journey Optimizer {#ajo-setup}

Prima di implementare il Web SDK, imposta lo stream di dati, i canali e le campagne in Journey Optimizer che distribuiscono il contenuto alla casella in entrata.

1. Configura un **datastream** configurato con **Adobe Experience Platform** come servizio, con **Journey Optimizer** abilitato e un **set di dati evento** selezionato.

1. Crea due configurazioni di canale che condividono la stessa superficie: un canale **Schede di contenuto** e un canale **Posta in arrivo**. [Scopri come configurare un canale per schede di contenuto](../content-card/content-card-configuration.md) e [come configurare un canale Posta in arrivo](inbox-configuration.md).

   Imposta l&#39;**URL pagina** e la **posizione a pagina** di entrambi i canali sulla superficie definita nei prerequisiti. Questa posizione deve corrispondere alla superficie per la quale si esegue la query nel codice Web SDK.

1. [Crea una campagna per schede di contenuto](../content-card/create-content-card.md) che utilizza il canale Schede di contenuto per la configurazione della scheda di contenuto.

   Per i messaggi che devono essere consegnati in base alle azioni dell&#39;utente nella pagina Web, abilitare **Regole di consegna aggiuntive** per l&#39;azione pertinente e impostare le condizioni di evento e valore che determinano quando verrà visualizzato il messaggio. Ripeti questa operazione per ogni tipo di notifica che la casella in entrata dovrebbe ricevere.

1. [Crea una campagna Posta in arrivo](inbox-create.md) che utilizza il canale Posta in arrivo. Questa campagna fornisce i metadati che configurano la shell della casella in entrata stessa.

   Fai corrispondere le impostazioni di audience e pianificazione della campagna Casella in entrata con la campagna Scheda contenuto, in modo che entrambe siano attive per gli stessi utenti allo stesso tempo.

1. Attiva entrambe le campagne.

## Implementare il Web SDK {#web-sdk-implementation}

La casella in entrata si basa su due comandi di Web SDK:

* `subscribeRulesetItems` registra un callback che viene eseguito ogni volta che le proposte idonee per la visualizzazione cambiano.

* `sendEvent` recupera tali proposte. In seguito puoi inviare eventi aggiuntivi per aggiornare quali messaggi sono idonei per la visualizzazione.

1. Definisci gli schemi della scheda di contenuto e della casella in entrata e la superficie che corrisponde alla configurazione del canale AJO:

   ```javascript
   const CONTENT_CARD_SCHEMA = "https://ns.adobe.com/personalization/message/content-card";
   const INBOX_SCHEMA        = "https://ns.adobe.com/personalization/message/inbox";
   const SURFACE             = "web://your-site.example/#message-inbox";
   ```

1. Configura il Web SDK con lo stream di dati:

   ```javascript
   alloy("configure", {
     datastreamId: "YOUR_DATASTREAM_ID",
     orgId: "YOUR_ORG_ID@AdobeOrg",
     defaultConsent: "in", // May not be usable in your implementation, but should be used for testing
     personalizationStorageEnabled: true,
   })
   ```

1. Iscriviti agli elementi del set di regole per la superficie e gli schemi e fornisci un callback che gestisca le proposte di schede di contenuto mentre cambiano:

   ```javascript
   alloy("subscribeRulesetItems", {
     surfaces: [SURFACE],
     schemas: [CONTENT_CARD_SCHEMA, INBOX_SCHEMA],
     callback: (result, collectEvent) => {
       const { propositions = [] } = result;
       const notifications = propositions
         .filter((p) => p.items?.[0]?.schema === CONTENT_CARD_SCHEMA)
         .map((proposition) => {
           const content = proposition.items[0]?.data?.content ?? {};
           return {
             id: proposition.scopeDetails.activity.id,
             title: content.title?.content ?? content.title ?? "",
             description: content.body?.content ?? content.body ?? "",
             proposition,
           };
         });
       renderNotifications(notifications, collectEvent);
     },
   });
   ```

1. Quando gli utenti interagiscono con l’applicazione, invia eventi per aggiornare quali proposte di schede di contenuto devono essere visualizzate:

   ```javascript
   alloy("sendEvent", {
     renderDecisions: true,
     personalization: { surfaces: [SURFACE] },
   });
   ```

1. Utilizza la funzione `collectEvent` fornita dal callback `subscribeRulesetItems` per segnalare le interazioni ad AJO. In questo modo i rapporti della campagna sono sempre accurati:

   ```javascript
   // When a notification is displayed in the detail view:
   collectEvent("display", [notification.proposition]);
   
   // When a user clicks or interacts with a notification:
   collectEvent("interact", [notification.proposition]);
   
   // When a user dismisses a notification without reading it:
   collectEvent("dismiss", [notification.proposition]);
   
   // When a user deletes a notification:
   collectEvent("interact", [notification.proposition]);
   collectEvent("delete",   [notification.proposition]);
   ```

1. Per le schede con regole di consegna aggiuntive, ad esempio `action = deposit-funds`, chiama `evaluateRulesets` con il corrispondente `decisionContext` per attivarle, poiché non vengono visualizzate solo su `sendEvent`:

   ```javascript
   alloy("evaluateRulesets", {
     renderDecisions: true,
     personalization: {
       decisionContext: { action: "deposit-funds" },
     },
   });
   ```

   Il callback `subscribeRulesetItems` viene eseguito nuovamente con tutte le nuove schede qualificate incluse insieme a quelle esistenti.

1. Installare le dipendenze e avviare il server di esempio:

   ```bash
   npm install
   npm start
   ```

1. Apri `https://localhost` nel browser.

1. Aggiorna le costanti `datastreamId`, `orgId` e `SURFACE` in `src/app/page.js` in modo che puntino al tuo ambiente AJO prima di eseguire il test.

