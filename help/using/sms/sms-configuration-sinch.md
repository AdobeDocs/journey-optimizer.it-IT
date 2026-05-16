---
solution: Journey Optimizer
product: journey optimizer
title: Configurare il provider Sinch
description: Scopri come configurare l’ambiente per l’invio di messaggi di testo con Journey Optimizer con Sinch
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 85412a85-edf0-4069-8bc7-b80371375f1f
TQID: https://experienceleague.adobe.com/24n9GhVTfQ9y4hlvY6g67dyL0FHqNOJW0aP-WIpzRqs
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: bb359667-ec7d-4d4b-8663-5850fc219d32id: d556b755-390a-43f0-be32-a08cf6236126
subfeature_v2: id: d2e8a157-b3b0-4143-9ff3-809bf400be56id: fdac7813-bd56-47ae-9f6d-fa94ad1c5dee
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 9e5edbefb19b7cf30da3a7164300e966a42e8711
workflow-type: tm+mt
source-wordcount: 946
ht-degree: 1%

---

# Configurare il provider Sinch {#sms-configuration-sinch}

Quando utilizzi il provider Sinch con Journey Optimizer, puoi trovare tre opzioni distinte:

* **Configurazione SMS**: configura le credenziali API Sinch per inviare messaggi SMS senza problemi.

* **Configurazione MMS**: per i messaggi multimediali (MMS), configura le credenziali API Sinch MMS. Tieni presente che il tracciamento e la risposta ai messaggi in entrata sono gestiti dalla configurazione SMS. La configurazione MMS è valida solo per il recapito in uscita del messaggio MMS.

* **Configurazione RCS**: configura le credenziali API Sinch per inviare messaggi RCS senza problemi.

Per configurare il provider Sinch, effettua le seguenti operazioni:

1. [Crea credenziali API](#create-api)
1. [Creare webhook](sms-webhook.md)
1. [Crea configurazione canale](sms-configuration-surface.md)
1. [Creare un Percorso o una campagna con un’azione del canale SMS](create-sms.md)

## Configurare le credenziali API per SMS{#create-api}

Per configurare il provider Sinch per l’invio di messaggi SMS e MMS con Journey Optimizer, effettua le seguenti operazioni:

1. Nella barra a sinistra, passa a **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** `>` **[!UICONTROL Impostazioni SMS]** e seleziona il menu **[!UICONTROL Credenziali API]**. Fare clic sul pulsante **[!UICONTROL Crea nuove credenziali API]**.

1. Configura le credenziali API SMS, come descritto di seguito:

   +++ Elenco delle credenziali SMS per la configurazione

   | Campi di configurazione | Descrizione |
   |---|---|
   | Fornitore SMS | Sinch |
   | Nome | Scegli un nome per le credenziali API. |
   | ID servizio e token API | Accedi alla pagina API e individua le tue credenziali nella scheda SMS. Ulteriori informazioni sono disponibili nella [documentazione di Sinch](https://developers.sinch.com/docs/sms/getting-started/){target="_blank"}. |
   | Numero in entrata | Aggiungi un numero in entrata univoco o un codice breve. Questo consente di utilizzare le stesse credenziali API in sandbox diverse, ciascuna con il proprio numero in entrata o codice breve. |
   | Sovrascrivi URL | Immetti l’URL personalizzato per sostituire gli endpoint predefiniti per rapporti di consegna SMS, dati di feedback, messaggi in entrata o notifiche di eventi. Sinch invierà tutti gli aggiornamenti rilevanti a questo URL invece di quelli predefiniti. |

   +++

<!--
1. Choose how user consent should be tracked for messaging:

    * **[!UICONTROL Sender short code]**: Inbound keyword consent is keyed to your **sender short code** only. Use when one inbound number is enough to represent consent.

    * **[!UICONTROL Sender short code + profile number]**: Consent is keyed to the **sender short code** and the profile **mobile number**. Use when profiles can have several numbers, or when opt-in/out must apply per sender and recipient pair.
-->

1. Seleziona **[!UICONTROL Usa set di dati personalizzato per in entrata]** per instradare gli SMS in entrata di questa credenziale a un set di dati precreato scelto dal menu a discesa. [Ulteriori informazioni sull&#39;utilizzo di un set di dati personalizzato per le parole chiave in entrata](custom-dataset-inbound-keywords.md)

   >[!NOTE]
   >
   >Lo schema del set di dati deve essere **[!UICONTROL XDM ExperienceEvent]** e includere almeno questi gruppi di campi:
   >* Adobe CJM ExperienceEvent - Dettagli sull’interazione del messaggio
   >* Adobe CJM ExperienceEvent - Dettagli sull’esecuzione dei messaggi
   >* Adobe CJM ExperienceEvent - Dettagli profilo messaggio
   >
   >Lo schema e il set di dati devono essere abilitati per il profilo.


1. Fai clic su **[!UICONTROL Invia]** al termine della configurazione delle credenziali API.

1. Nel menu **[!UICONTROL Credenziali API]**, fai clic sull&#39;icona bin per eliminare le credenziali API.

1. Per modificare le credenziali esistenti, individuare le credenziali API desiderate e fare clic sull&#39;opzione **[!UICONTROL Modifica]** per apportare le modifiche necessarie.

1. Fai clic su **[!UICONTROL Verifica connessione SMS]**, dalle credenziali API esistenti, per verificare le credenziali API SMS inviando un messaggio di esempio a un dispositivo designato.

1. Compila i campi **Numero** e **Messaggio** e fai clic su **[!UICONTROL Verifica connessione]**.

   >[!IMPORTANT]
   >
   >Il messaggio deve essere strutturato in modo da essere allineato al formato di payload del provider.

   ![](assets/verify-connection.png)

Dopo aver creato e configurato le credenziali API, devi creare [il tuo webhook](sms-webhook.md) e una configurazione del canale per i messaggi RCS. [Ulteriori informazioni](sms-configuration-surface.md)

## Configurare le credenziali API per MMS{#sinch-mms}

>[!IMPORTANT]
>
> Oltre alla configurazione di MMS, devi anche creare credenziali API Sinch specifiche per il tracciamento dei messaggi in entrata e la gestione delle richieste di consenso.

Per configurare Sinch MMS per l’invio di MMS con Journey Optimizer, effettua le seguenti operazioni:

1. Nella barra a sinistra, passa a **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** `>` **[!UICONTROL Impostazioni SMS]** e seleziona il menu **[!UICONTROL Credenziali API]**. Fare clic sul pulsante **[!UICONTROL Crea nuove credenziali API]**.

1. Configura le credenziali API MMS, come descritto di seguito:

   * **[!UICONTROL Fornitore SMS]**: Sinch MMS.

   * **[!UICONTROL Nome]**: scegli un nome per le credenziali API.

   * **[!UICONTROL ID progetto]**, **[!UICONTROL ID app]** e **[!UICONTROL Token API]**: segui i passaggi seguenti per raccogliere le credenziali API MMS.

      * Per **[!UICONTROL ID progetto]** e **[!UICONTROL ID app]**: accedi alla pagina [Panoramica API di conversazione](https://dashboard.sinch.com/convapi/overview) del progetto Sinch nel tuo dashboard di Sinch.
      * Per **[!UICONTROL token API]**: ottieni le [chiavi di accesso](https://community.sinch.com/t5/Customer-Dashboard/Sinch-Access-Keys/ta-p/12638) per il tuo progetto Sinch e genera un **token API Base64** dal tuo progetto Sinch **chiavi di accesso**.

1. Fai clic su **[!UICONTROL Invia]** al termine della configurazione delle credenziali API.

1. Nel menu **[!UICONTROL Credenziali API]**, fai clic sull&#39;icona bin per eliminare le credenziali API.

1. Per modificare le credenziali esistenti, individuare le credenziali API desiderate e fare clic sull&#39;opzione **[!UICONTROL Modifica]** per apportare le modifiche necessarie.

Dopo aver creato e configurato le credenziali API, devi creare [il tuo webhook](sms-webhook.md) e una configurazione del canale per i messaggi RCS. [Ulteriori informazioni](sms-configuration-surface.md)

## Configurare le credenziali API per RCS

<!--![](assets/do-not-localize/rcs-sms.png)-->

La messaggistica RCS (Rich Communication Services) è supportata in Journey Optimizer tramite Sinch, consentendo l’invio di messaggi di base tramite profili aziendali verificati con elementi di branding come loghi e nomi di mittenti.

Tieni presente che i messaggi tornano automaticamente a SMS quando il dispositivo del profilo non supporta RCS o è temporaneamente non raggiungibile tramite RCS.

<!--
### Basic RCS Messages

>[!AVAILABILITY]
>
> Basic RCS messages is only available upon Adobe RCS add-on offering.

1. **Set up your branded RCS agent**

    Create a branded RCS agent in the Sinch Dashboard. [Learn more on branded RCS agent](https://community.sinch.com/t5/RCS/Getting-Started-with-RCS-using-Conversation-API/ta-p/17844)

1. **Set up your [Custom API credentials](sms-configuration-custom.md)**
    
    Once your RCS agent is approved, you need to set up your Sinch API credentials, which include your access key, secret, and service plan ID. These credentials will be used by Journey Optimizer to authenticate and send messages through Sinch's platform.

1. **Create a [channel configuration](sms-configuration-surface.md) for your RCS messages**

    Configure a channel surface in Journey Optimizer by linking your Sinch credentials and defining the messaging parameters. This setup enables you to compose and send RCS messages from Journey Optimizer.

1. **Create and personalize your [SMS message](../sms/create-sms.md)**

    Your messages automatically falls back to SMS when the profile's device does not support RCS or is temporarily unreachable via RCS.
-->

### Messaggi multimediali RCS

>[!AVAILABILITY]
>
> I messaggi RCS avanzati sono disponibili solo con un account diretto gestito da Sinch.

1. **Configura l&#39;agente RCS con marchio**

   Crea un agente RCS con marchio nel dashboard di Sinch. [Ulteriori informazioni sull&#39;agente RCS con marchio](https://community.sinch.com/t5/RCS/Getting-Started-with-RCS-using-Conversation-API/ta-p/17844)

1. **Configura le [credenziali API personalizzate](sms-configuration-custom.md)**

   Una volta approvato l’agente RCS, devi impostare le credenziali API personalizzate, che includono AppId, Nome, URL e Tipo di autenticazione.

1. **Configura il tuo RCS con il payload del provider.**

   Nelle [credenziali API personalizzate](sms-configuration-custom.md), aggiungi il payload del provider per convalidare e personalizzare i messaggi RCS.

1. **Crea una [configurazione canale](sms-configuration-surface.md) per i messaggi RCS**

   Configura una superficie di canale in Journey Optimizer collegando le credenziali Sinch e definendo i parametri di messaggistica. Questa configurazione consente di comporre e inviare messaggi RCS da Journey Optimizer.

1. **Crea e personalizza il [messaggio SMS](../sms/create-sms.md)**

   Incolla il payload direttamente nel contenuto SMS per incorporare e distribuire i messaggi RCS (Rich Communication Services).

   ➡️ [Scopri come Sinch supporta RCS nella documentazione di Sinch](https://sinch.com/blog/rcs-api-guide/)


