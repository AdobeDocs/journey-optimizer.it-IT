---
title: Introduzione per gli sviluppatori
description: In qualità di sviluppatore, scopri di più su come utilizzare Journey Optimizer
feature: Get Started
role: Developer
level: Experienced
exl-id: 5053dd4f-d050-415f-bc74-d6d061bdcbe1
source-git-commit: 5ff7987c00afda3263cb97654967c5b698f726c2
workflow-type: tm+mt
source-wordcount: '1891'
ht-degree: 2%

---

# Introduzione per gli sviluppatori {#get-started-developers}

In qualità di **sviluppatore**, sei responsabile dell&#39;implementazione e dell&#39;integrazione di [!DNL Adobe Journey Optimizer] nelle applicazioni e nei sistemi. Puoi iniziare a lavorare con [!DNL Adobe Journey Optimizer] una volta che l&#39;[Amministratore di sistema](administrator.md) e il [Data Engineer](data-engineer.md) ti avranno concesso l&#39;accesso e avranno preparato il tuo ambiente.

## Il tuo ruolo nell’ecosistema Journey Optimizer

Mentre altri membri del gruppo configurano Journey Optimizer tramite l’interfaccia utente, ti concentrerai su:

* **Implementazione degli SDK** nelle applicazioni mobili e web
* **Invio di eventi** dalle applicazioni per l&#39;attivazione di percorsi
* **Creazione di endpoint API** che Journey Optimizer può richiamare tramite azioni personalizzate
* **Integrazione** di Journey Optimizer con i sistemi e l&#39;infrastruttura esistenti
* **Verifica e debug** delle implementazioni

Il [Data Engineer](data-engineer.md) gestirà schemi di dati, configurazioni di eventi e origini dati. L&#39;[Amministratore](administrator.md) configurerà le autorizzazioni e le configurazioni dei canali. [Gli addetti al marketing](marketer.md) progetteranno percorsi e contenuti che utilizzano le tue implementazioni.

Questa guida descrive i passaggi tecnici essenziali per iniziare a utilizzare Journey Optimizer. Per la creazione di app mobili, esperienze web o integrazioni API, segui le sezioni seguenti per configurare la tua implementazione.

## Prerequisiti {#prerequisites}

Prima di iniziare l’implementazione, assicurati di disporre di:

**Competenze tecniche:**

* Esperienza con JavaScript (per Web SDK) o Swift/Kotlin (per Mobile SDK)
* Informazioni sulle API RESTful e su JSON
* Familiarità con la programmazione asincrona e le architetture basate su eventi
* Conoscenza dell&#39;architettura dell&#39;applicazione aziendale

**Accesso e strumenti:**

* Accesso a [Adobe Developer Console](https://developer.adobe.com){target="_blank"} per le credenziali API
* Ambiente di sviluppo con accesso alla base di codice dell&#39;applicazione
* Strumenti di test come Postman per i test API
* Strumenti per sviluppatori di browser o strumenti di debug per dispositivi mobili

**Da altri membri del team:**

* Accesso all&#39;ambiente concesso dall&#39;[Amministratore](administrator.md)
* Schemi XDM e definizioni di eventi da [Data Engineer](data-engineer.md)
* Requisiti e casi d&#39;uso di [addetti al marketing](marketer.md)

## Comprendere la base tecnica {#technical-foundation}

Prima di iniziare a implementare, acquisisci familiarità con i concetti tecnici di base:

1. **Integrazione Adobe Experience Platform**: Journey Optimizer è stato creato in modalità nativa in Adobe Experience Platform. Comprendere l’architettura di base ti aiuterà a creare implementazioni più efficaci. Ulteriori informazioni su [come funziona Journey Optimizer](../understanding-ajo.md).

1. **Modelli dati XDM**: Journey Optimizer utilizza Experience Data Model (XDM) per strutturare i dati di eventi e profili. In qualità di sviluppatore, devi capire come inviare dati conformi agli schemi configurati dal tuo [Data Engineer](data-engineer.md). Informazioni sugli [schemi XDM](../../data/get-started-schemas.md).

1. **Autenticazione e sicurezza**: tutte le implementazioni richiedono l&#39;autenticazione corretta. Scopri come impostare l’autenticazione per SDK e API. Informazioni sull&#39;[autenticazione API](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}.

## Configurare le integrazioni di app mobili {#mobile-integration}

### Configurare Adobe Experience Platform Mobile SDK

Per abilitare le notifiche push, i messaggi in-app e altre funzionalità mobili, integra il SDK mobile di Adobe Experience Platform nelle tue applicazioni mobili.

1. **Installa e configura il SDK mobile**: segui la [documentazione di Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation/getting-started/){target="_blank"} per iniziare a utilizzare l&#39;integrazione con SDK.

1. **Creare una proprietà mobile**: configurare una proprietà mobile in [!DNL Adobe Experience Platform Data Collection]. Scopri come [creare e configurare una proprietà mobile](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property/){target="_blank"}.

1. **Configurare le notifiche push**:
   * Per **app iOS**: registra l&#39;app con APN (Apple Push Notification Service). Ulteriori informazioni sono disponibili nella [documentazione di Apple](https://developer.apple.com/documentation/usernotifications/registering_your_app_with_apns){target="_blank"}.
   * Per **app Android**: configura Firebase Cloud Messaging per la tua app Android. Ulteriori informazioni sono disponibili nella [documentazione di Google](https://firebase.google.com/docs/cloud-messaging/android/client){target="_blank"}.

1. **Verifica la tua integrazione mobile**: utilizza il [flusso di lavoro di avvio rapido per l&#39;onboarding di dispositivi mobili](../../push/mobile-onboarding-wf.md) per configurare e testare rapidamente la configurazione di dispositivi mobili.

I passaggi dettagliati per la configurazione delle notifiche push sono disponibili in [questa pagina](../../push/push-configuration.md).

### Implementare esperienze basate su codice (Mobile SDK)

Per la personalizzazione nativa delle app mobili tramite esperienze basate su codice:

* Segui [questa esercitazione](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/code-based/tutorial/){target="_blank"} per l&#39;implementazione di Mobile SDK
* Esamina implementazioni di esempio per [iOS](https://github.com/adobe/aepsdk-messaging-ios/tree/main/TestApps/MessagingDemoAppSwiftUI){target="_blank"} e [Android](https://github.com/adobe/aepsdk-messaging-android/tree/main/code/testapp){target="_blank"}

## Implementare esperienze web {#web-implementation}

### Configurare Adobe Experience Platform Web SDK

Per le implementazioni basate su web, il Web SDK è il punto di integrazione principale:

1. **Installa il Web SDK**: segui la [guida all&#39;implementazione del Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=it){target="_blank"} per configurare il SDK sul tuo sito Web.

1. **Configura flussi di dati**: crea e configura uno stream di dati in [!DNL Adobe Experience Platform Data Collection] con Journey Optimizer abilitato. Ulteriori informazioni sono disponibili nella [documentazione sugli stream di dati](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=it){target="_blank"}.

1. **Abilita notifiche push Web** (facoltativo): configura la proprietà [pushNotifications](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/pushnotifications){target="_blank"} nella configurazione del Web SDK e utilizza il comando [sendPushSubscription](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/sendpushsubscription){target="_blank"} per registrare le sottoscrizioni push.

### Implementare esperienze basate su codice (Web SDK)

Le esperienze basate su codice ti consentono di personalizzare qualsiasi punto di contatto digitale:

1. **Scegliere il metodo di implementazione**: lato client, lato server o ibrido. Rivedi [esempi di implementazione](../../code-based/code-based-implementation-samples.md) per ogni approccio.

1. **Definisci superfici**: identifica le posizioni nell&#39;applicazione in cui desideri distribuire contenuti personalizzati. Scopri la [configurazione superficiale](../../code-based/code-based-surface.md).

1. **Implementa rendering del contenuto**: utilizza il Web SDK per recuperare e applicare contenuti di personalizzazione. Consulta [esercitazioni sull&#39;implementazione basate su codice](../../code-based/code-based-decisioning-implementations.md).

1. **Invio di eventi di visualizzazione e interazione**: tenere traccia di quando il contenuto viene visualizzato e quando gli utenti interagiscono con esso per l&#39;analisi e l&#39;ottimizzazione.

Esplora [implementazioni di esempio su GitHub](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"} per visualizzare in azione le esperienze basate su codice.

Ulteriori informazioni su [introduzione alle esperienze basate su codice](../../code-based/get-started-code-based.md).

## Implementare lo streaming degli eventi {#event-streaming}

### Inviare eventi ai percorsi di attivazione

In qualità di sviluppatore, implementerai il codice per inviare eventi che attivano i percorsi. Il [Data Engineer](data-engineer.md) configurerà gli schemi e le definizioni degli eventi in Journey Optimizer.

1. **Comprendere il payload dell&#39;evento**: rivolgiti al tuo Data Engineer per ottenere lo schema dell&#39;evento e la struttura del payload richiesti. Il payload deve essere conforme allo schema XDM configurato. Scopri i [requisiti dello schema eventi](../../event/experience-event-schema.md).

1. **Implementa streaming eventi**: invia eventi a Adobe Experience Platform utilizzando le [API Streaming Ingestion](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=it){target="_blank"}. Scopri i [passaggi per inviare eventi](../../event/additional-steps-to-send-events-to-journey.md).

1. **Gestisci tipi di evento**:
   * **Eventi unitari**: implementa l&#39;invio di eventi per azioni specifiche della persona (ad esempio, clic sul pulsante, completamento dell&#39;acquisto)
   * **Eventi di business**: invia eventi correlati all&#39;azienda (ad esempio, aggiornamenti di inventario, modifiche di prezzo)

1. **Consegna evento di test**: verificare che gli eventi siano ricevuti correttamente e attivare i percorsi come previsto. Informazioni sulla [risoluzione dei problemi dell&#39;evento](../../building-journeys/troubleshooting-inbound.md).

**Implementazione di esempio** per l&#39;invio di un evento tramite API:

```javascript
POST https://{DATACOLLECTION_ENDPOINT}/collection/{DATASTREAM_ID}
Content-Type: application/json

{
  "header": {
    "datasetId": "{DATASET_ID}",
    "imsOrgId": "{ORG_ID}",
    "source": {
      "name": "Web SDK"
    }
  },
  "body": {
    "xdmMeta": {
      "schemaRef": {
        "id": "{SCHEMA_ID}"
      }
    },
    "xdmEntity": {
      "_id": "unique-event-id",
      "eventType": "purchase",
      "timestamp": "2024-01-01T12:00:00Z",
      // ... your event data
    }
  }
}
```

Ulteriori informazioni sull&#39;utilizzo di [eventi di percorso](../../event/about-events.md).

## Sviluppare endpoint di azione personalizzati {#custom-actions}

Le azioni personalizzate consentono ai percorsi di richiamare le API. In qualità di sviluppatore, creerai gli endpoint API richiamati dalle azioni personalizzate:

1. **Genera l&#39;endpoint API**: crea endpoint API RESTful che Journey Optimizer chiamerà durante l&#39;esecuzione del percorso. L’endpoint deve:
   * Accetta payload JSON
   * Autentica richieste (OAuth, chiave API o JWT)
   * Elabora le richieste entro i limiti di timeout appropriati
   * Risposte restituite nel formato previsto

1. **Comprendere le funzionalità delle azioni personalizzate**: le azioni personalizzate possono connettersi a sistemi di terze parti come Epsilon, Slack, Firebase o ai tuoi servizi. Ulteriori informazioni sulle [azioni personalizzate](../../action/action.md).

1. **Utilizzare le configurazioni delle azioni**: l&#39;[amministratore](administrator.md) o il [data engineer](data-engineer.md) configurerà l&#39;azione personalizzata in Journey Optimizer, definendo l&#39;URL dell&#39;endpoint API, il metodo di autenticazione e i parametri. Fornirai loro le tue specifiche API. Scopri la [configurazione azione personalizzata](../../action/about-custom-action-configuration.md).

1. **Restituisci dati actionable**: progetta l&#39;API per restituire dati che possono essere utilizzati nei passaggi di percorso successivi. Scopri le [risposte alle azioni](../../action/action-response.md).

1. **Implementa limitazione di velocità**: assicurati che gli endpoint possano gestire il volume previsto. Journey Optimizer applica un limite di 5000 chiamate/secondo, ma il sistema deve essere resiliente. Scopri le [limitazioni e limitazioni](../../configuration/external-systems.md).

**Caso d&#39;uso di esempio**: [Scrittura di eventi di percorso in Experience Platform](../../building-journeys/custom-action-aep.md) mediante azioni personalizzate.

## Utilizzare le API di Journey Optimizer {#apis}

Journey Optimizer fornisce API REST complete per l’accesso programmatico:

1. **Comprendere le funzionalità API**: le API di Journey Optimizer consentono di creare, leggere, aggiornare ed eliminare varie risorse a livello di programmazione. Informazioni sulle [API Journey Optimizer](../../configuration/ajo-apis.md).

1. **Autenticazione**: segui [questa esercitazione](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"} per configurare l&#39;autenticazione API tramite Adobe Developer Console.

1. **Esplora i riferimenti API**: sfoglia la documentazione API completa e prova le API direttamente nel [riferimento API di Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}.

1. **Campagne attivate da API**: crea messaggi transazionali con campagne attivate da API. Per scenari con volumi elevati (fino a 5000 TPS), esplora la [modalità High Throughput](../../campaigns/api-triggered-high-throughput.md) (richiede una licenza aggiuntiva).

1. **API per la gestione delle decisioni**: utilizza API specializzate per la gestione delle offerte e per il decisioning. Ulteriori informazioni sono disponibili nella [Guida API per la gestione delle decisioni](../../offers/api-reference/getting-started.md).

## Test e debug {#testing}

1. **Implementazione debug di SDK**: utilizza Adobe Experience Platform Assurance per controllare gli eventi di SDK, convalidare la raccolta dati e risolvere in tempo reale i problemi di integrazione. [Ulteriori informazioni su Assurance](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html){target="_blank"}.

1. **Consegna evento di test**: verifica che gli eventi dell&#39;applicazione siano ricevuti correttamente da Adobe Experience Platform e attiva i percorsi come previsto. Monitora l’acquisizione degli eventi e convalida la struttura del payload.

1. **Convalida integrazioni API**: verifica gli endpoint di azione personalizzati per garantire che gestiscano correttamente le richieste di Journey Optimizer, rispondano entro i limiti di timeout e restituiscano i formati di dati previsti.

1. **Utilizza la modalità di test con i profili di test**: rivolgiti al tuo [Data Engineer](data-engineer.md) per accedere ai profili di test, quindi convalida l&#39;implementazione utilizzando la modalità di test percorso. Scopri come [verificare i percorsi](../../building-journeys/testing-the-journey.md).

1. **Monitoraggio dei registri di SDK**: abilita la registrazione di debug nell&#39;implementazione di SDK per risolvere i problemi durante lo sviluppo:
   * **Mobile SDK**: abilita la registrazione per visualizzare eventi SDK e chiamate API
   * **Web SDK**: usa la console del browser per monitorare l&#39;attività di SDK

1. **Verifica la configurazione dello stream di dati**: verificare che lo stream di dati sia configurato correttamente per l&#39;invio di dati a Journey Optimizer. Verifica che gli eventi fluiscano attraverso lo stream di dati verso le destinazioni corrette.

1. **Query dei dati del percorso per l&#39;analisi**: utilizzare le query SQL nel Data Lake per analizzare gli eventi dei passaggi del percorso, eseguire il debug dei problemi e monitorare le prestazioni delle azioni personalizzate. Esplora [esempi di query per l&#39;analisi del percorso](../../reports/query-examples.md), tra cui:
   * Tracciamento di entrata/uscita profilo e motivi di eliminazione
   * Metriche delle prestazioni delle azioni personalizzate (latenza, velocità effettiva, errori)
   * Modelli di consegna degli eventi e di errore
   * Stati dell’istanza del percorso

## Argomenti per sviluppatori avanzati {#advanced-topics}

### Utilizzo dei dati contestuali e dell’arricchimento

* **Iterazione su array**: utilizza la sintassi Handlebars per visualizzare elenchi dinamici da eventi, risposte di azioni personalizzate e ricerche di set di dati nei messaggi. Scopri come [iterare dati contestuali](../../personalization/iterate-contextual-data.md).
* **Ricerca set di dati**: implementa le ricerche dei set di dati per arricchire i dati di percorso dai set di dati di Adobe Experience Platform. Lavora con il tuo Data Engineer sulla configurazione. Scopri [ricerca set di dati](../../building-journeys/dataset-lookup.md).

### Lavorare con il consenso e la governance

Implementa la governance dei dati e i criteri di consenso nelle integrazioni:

* **Governance dei dati**: applica i criteri di utilizzo dei dati alle azioni personalizzate. Ulteriori informazioni sulla [governance dei dati](../../action/action-privacy.md).
* **Gestione del consenso**: gestisci le preferenze di consenso del cliente nelle tue implementazioni. Scopri di più sul [consenso](../../action/consent.md).

### Ottimizzazione e best practice

* **Limitazione e limitazione**: comprendi i limiti di velocità e implementa la limitazione appropriata. Informazioni su [sistemi esterni](../../configuration/external-systems.md).
* **Ottimizzazione Percorso**: seguire le best practice per [Ottimizzazione percorso](../../building-journeys/optimize.md).
* **Gestione degli errori**: implementare una gestione affidabile degli errori. Rivedi [codici di errore](../../building-journeys/error-codes-reference.md) e [guide alla risoluzione dei problemi](../../building-journeys/troubleshooting.md).

## Risorse aggiuntive {#additional-resources}

* **Developer Console**: accedere a [Adobe Developer Console](https://developer.adobe.com){target="_blank"} per creare integrazioni e gestire le credenziali API.
* **Codice di esempio**: esplora [implementazioni di esempio su GitHub](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"}.
* **Video tutorial**: scopri le esercitazioni pratiche in [Experience League](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=it){target="_blank"}.
* **Community sviluppatori**: contatta altri sviluppatori e ottieni supporto nei forum della community Adobe.

## Collaborazione tra ruoli {#next-steps}

Il tuo lavoro di implementazione si interseca con altri membri del gruppo:

**Lavora con [Ingegneri dati](data-engineer.md):**

* Ottenere gli schemi XDM e le strutture di eventi necessari per implementare
* Scopri quali eventi devi inviare e il formato del payload richiesto
* Allineamento ai requisiti di raccolta dei dati e agli standard di qualità dei dati
* Testare insieme la consegna degli eventi e l’acquisizione dei dati

**Lavora con [Amministratori](administrator.md):**

* Specifica le API per le azioni personalizzate che configureranno
* Richiedi le autorizzazioni e le credenziali API necessarie
* Coordinate sui requisiti di configurazione del canale (ad esempio, certificati push)
* Allineamento su ambienti di test e strategia sandbox

**Lavora con [Addetti al marketing](marketer.md):**

* Scopri quali interazioni utente devono attivare gli eventi
* Implementare il tracciamento per migliorare le prestazioni dei contenuti e il coinvolgimento degli utenti
* Test di supporto dei percorsi con le funzioni implementate
* Risolvere i problemi relativi alla consegna o alla personalizzazione dei messaggi

## Rimani aggiornato

Tenere il passo con le funzionalità e le modifiche tecniche più recenti di Journey Optimizer:

* **[Note sulla versione](../../rn/release-notes.md)**: rivedi nuove funzioni, modifiche API, aggiornamenti SDK e correzioni di bug rilasciati ogni mese
* **[Aggiornamenti alla documentazione](../../rn/documentation-updates.md)**: tieni traccia delle recenti modifiche alla documentazione tecnica, incluse nuove guide all&#39;implementazione ed esempi di codice
* **Notifiche prodotto**: abilita le notifiche nel tuo [profilo Adobe Experience Cloud](https://experience.adobe.com/preferences){target="_blank"} per ricevere avvisi su:
   * Nuove versioni di SDK e aggiornamenti API
   * Interruzione di modifiche ed elementi obsoleti
   * Finestre di manutenzione che influiscono sulle integrazioni
   * Aggiornamenti di sicurezza critici

  Per abilitare le notifiche, fai clic sull&#39;icona del tuo profilo in alto a destra di Adobe Experience Cloud, vai a **Preferenze > Notifiche** e configura le preferenze per le notifiche Journey Optimizer.

## Avvia implementazione

Pronto per iniziare a creare? Scegli la tua prima area di implementazione dalle sezioni precedenti:

1. **App mobile?** Inizia con [Integrazione con Mobile SDK](#mobile-integration)
2. **Sito Web?** Inizia con [Installazione di Web SDK](#web-implementation)
3. Integrazione con **API?** Passa a [Utilizzo delle API](#apis)
4. **Sistema personalizzato?** Estrai [Azioni personalizzate](#custom-actions)

Ogni sezione include collegamenti alla documentazione tecnica dettagliata, esempi di codice e tutorial per guidare l’implementazione.
