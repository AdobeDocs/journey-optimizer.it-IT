---
solution: Journey Optimizer
product: journey optimizer
title: Configurare il canale WhatsApp
description: Scopri come configurare il tuo ambiente per inviare messaggi WhatsApp con Journey Optimizer
feature: Whatsapp, Channel Configuration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: d1f40cd8-f311-4df6-b401-8858095cef3e
source-git-commit: 9af09d694f58d169dcf4448562129ed0b37f35df
workflow-type: tm+mt
source-wordcount: '773'
ht-degree: 4%

---

# Introduzione alla configurazione di WhatsApp {#whatsapp-config}

>[!BEGINSHADEBOX]

**Sommario**

* [Introduzione ai messaggi WhatsApp](get-started-whatsapp.md)
* **[Introduzione alla configurazione di WhatsApp](whatsapp-configuration.md)**
* [Creare un messaggio WhatsApp](create-whatsapp.md)
* [Verificare e inviare i messaggi WhatsApp](send-whatsapp.md)

>[!ENDSHADEBOX]

Prima di inviare il messaggio WhatsApp, devi configurare l’ambiente Adobe Journey Optimizer e associarti all’account WhatsApp. Per eseguire questa operazione:

1. [Creare le credenziali API WhatsApp](#WhatsApp-credentials)
1. [Creare i webhook WhatsApp](#WhatsApp-webhook)
1. [Creare la configurazione WhatsApp](#WhatsApp-configuration)

Questi passaggi devono essere eseguiti da un [amministratore di sistema](../start/path/administrator.md) di Adobe Journey Optimizer.

## Creare le credenziali API WhatsApp {#whatsapp-credentials}

1. Nella barra a sinistra, passa a **[!UICONTROL Amministrazione]** `>` **[!UICONTROL Canali]** e seleziona il menu **[!UICONTROL Credenziali API]**. Fare clic sul pulsante **[!UICONTROL Crea nuove credenziali API]**.

1. Configura le credenziali API come descritto di seguito:

   * **Token API**: immetti il token API. Ulteriori informazioni nella [documentazione Meta](https://developers.facebook.com/docs/facebook-login/guides/access-tokens/)
   * **ID account aziendale**: immetti il numero univoco relativo al tuo portfolio aziendale. Ulteriori informazioni nella [documentazione Meta](https://www.facebook.com/business/help/1181250022022158?id=180505742745347).

   ![](assets/whatsapp-api.png)

1. Fai clic su **[!UICONTROL Continua]**.

1. Scegli l&#39;**account aziendale** che desideri connettere alle credenziali API WhatsApp.

   ![](assets/whatsapp-api-2.png)

1. Seleziona il **Nome mittente** utilizzato per inviare i messaggi Whatsapp.

1. Le impostazioni del numero di telefono vengono compilate automaticamente:

   * **Valutazione qualità**: riflette il feedback del cliente sui messaggi inviati nelle ultime 24 ore.
      * Verde: alta qualità
      * Giallo: qualità Medium
      * Rosso: bassa qualità

     Ulteriori informazioni sulla [valutazione qualità](https://www.facebook.com/business/help/766346674749731#)

   * **Velocità effettiva**: indica la velocità con cui il numero di telefono può inviare messaggi.

1. Fai clic su **[!UICONTROL Invia]** al termine della configurazione delle credenziali API.

Dopo aver creato e configurato le credenziali API, ora è necessario creare una configurazione del canale per i messaggi WhatsApp. [Ulteriori informazioni](#whatsapp-configuration)

## Crea webhook {#WhatsApp-webhook}

>[!CONTEXTUALHELP]
>id="ajo_admin_whatsapp_webhook_inbound_keyword_category"
>title="Categoria parole chiave in entrata"
>abstract="<b>Opt-in</b>: invia la risposta automatica definita quando un utente si abbona. <br/><b>Rinuncia</b>: invia la risposta automatica definita quando un utente annulla l&#39;iscrizione. <br/><b>Guida</b>: invia la risposta automatica definita quando un utente richiede assistenza o supporto. <br/><b>Predefinito</b>: invia la risposta automatica di fallback quando nessuna parola chiave corrisponde."

>[!CONTEXTUALHELP]
>id="ajo_admin_whatsapp_webhook_inbound_keyword"
>title="Immetti le parole chiave"
>abstract="Puoi definire parole chiave per attivare risposte automatiche specifiche in base al testo digitato dagli utenti. Le parole chiave non fanno distinzione tra maiuscole e minuscole, ad esempio, stop e STOP vengono trattate allo stesso modo."

>[!CONTEXTUALHELP]
>id="ajo_admin_whatsapp_webhook_webhook_url"
>title="URL callback"
>abstract="La richiesta di convalida e le notifiche webhook per questo oggetto vengono inviate all&#39;URL specificato."

>[!CONTEXTUALHELP]
>id="ajo_admin_whatsapp_webhook_verify_token"
>title="Verifica token"
>abstract="Token restituito da Meta per confermare e verificare l&#39;URL di callback durante il processo di verifica."

>[!NOTE]
>
>Senza le parole chiave di consenso o rinuncia specificate, i messaggi di consenso standard non sono abilitati.

Dopo aver creato correttamente le credenziali API WhatsApp e i [Meta Webhook](https://developers.facebook.com/docs/whatsapp/webhooks/), il passaggio successivo consiste nel creare un webhook e configurare le impostazioni in entrata.

1. Nella barra a sinistra, passa a **[!UICONTROL Amministrazione]** `>` **[!UICONTROL Canali]**, seleziona il menu **[!UICONTROL Webhook WhatsApp]** in **[!UICONTROL Impostazioni WhatsApp]** e fai clic sul pulsante **[!UICONTROL Crea webhook]**.

1. Immetti un [!UICONTROL Nome] per il tuo webhook.

1. Dall&#39;elenco a discesa, seleziona le [credenziali API](#whatsapp-credentials) create in precedenza.

1. Fai clic su ![aggiungi](assets/do-not-localize/Smock_AddCircle_18_N.svg) per iniziare a configurare una **[!UICONTROL categoria di parole chiave in entrata]**, ad esempio:

   * **[!UICONTROL Parole chiave di consenso]**
   * **[!UICONTROL Parole chiave per la rinuncia]**
   * **[!UICONTROL Parole chiave della Guida]**

1. Immetti la **[!UICONTROL parola chiave]**.

   Per aggiungere più parole chiave, fare clic su ![aggiungi](assets/do-not-localize/Smock_AddCircle_18_N.svg).

1. Specifica il **[!UICONTROL Messaggio di risposta]** da inviare quando viene ricevuta una parola chiave configurata.

<!--
1. Click **[!UICONTROL View payload editor]** to validate and customize your request payloads. 
    
    You can dynamically personalize your payload using profile attributes, and ensure accurate data is sent for processing and response generation with the help of built-in helper functions.
-->

1. Fai clic su **[!UICONTROL Invia]** al termine della configurazione del webhook WhatsApp.

1. Nel menu **[!UICONTROL Webhook]**, fai clic sull&#39;icona ![raccoglitore](assets/do-not-localize/Smock_Delete_18_N.svg) per eliminare il tuo webhook WhatsApp.

1. Per modificare la configurazione esistente, individuare il webhook desiderato e fare clic sull&#39;opzione **[!UICONTROL Modifica]** per apportare le modifiche necessarie.

1. Accedi e copia il nuovo **[!UICONTROL URL webhook]** dal **[!UICONTROL webhook WhatsApp]** inviato in precedenza.

Una volta configurato il webhook, puoi creare la configurazione WhatsApp.

## Crea configurazione WhatsApp {#whatsapp-configuration}

1. Nella barra a sinistra, passa a **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** e seleziona **[!UICONTROL Impostazioni generali]** > **[!UICONTROL Configurazioni canale]**. Fare clic sul pulsante **[!UICONTROL Crea configurazione canale]**.

   ![](assets/whatsapp-config-1.png)

1. Inserisci un nome e una descrizione (facoltativa) per la configurazione, quindi seleziona il canale WhatsApp.

   >[!NOTE]
   >
   > I nomi devono iniziare con una lettera (A-Z). Può contenere solo caratteri alfanumerici. È inoltre possibile utilizzare i caratteri trattino basso `_`, punto `.` e trattino `-`.

1. Seleziona **[!DNL WhatsApp]** come tuo canale.

   ![](assets/whatsapp-config-2.png)

1. Seleziona **[!UICONTROL Azioni di marketing]** per associare i criteri di consenso ai messaggi utilizzando questa configurazione. Tutti i criteri di consenso associati all’azione di marketing vengono utilizzati per rispettare le preferenze dei clienti. Ulteriori informazioni

1. Seleziona la **[!UICONTROL configurazione API WhatsApp]** creata in precedenza.

   ![](assets/whatsapp-config-3.png)

1. Immettere il **[!UICONTROL numero mittente]** &#x200B;che si desidera utilizzare per le comunicazioni.

1. Una volta configurati tutti i parametri, fai clic su **[!UICONTROL Invia]** per confermare. Puoi anche salvare la configurazione del canale come bozza e riprenderla in un secondo momento.

1. Una volta creata, la configurazione del canale viene visualizzata nell&#39;elenco con lo stato **[!UICONTROL Elaborazione]**.

   >[!NOTE]
   >
   >Se i controlli non hanno esito positivo, ulteriori informazioni sui possibili motivi di errore in [questa sezione](../configuration/channel-surfaces.md).

1. Una volta completati i controlli, la configurazione del canale ottiene lo stato **[!UICONTROL Attivo]**. È pronto per essere utilizzato per inviare messaggi.

Una volta configurata, puoi sfruttare tutte le funzionalità di canale predefinite, come l’authoring dei messaggi, la personalizzazione, il tracciamento dei collegamenti e il reporting.

Ora puoi inviare messaggi WhatsApp con Journey Optimizer.