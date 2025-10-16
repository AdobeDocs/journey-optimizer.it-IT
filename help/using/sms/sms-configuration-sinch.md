---
solution: Journey Optimizer
product: journey optimizer
title: Configurare il provider Sinch
description: Scopri come configurare l’ambiente per l’invio di messaggi di testo con Journey Optimizer con Sinch
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 85412a85-edf0-4069-8bc7-b80371375f1f
source-git-commit: 7b1be144776fd11cd4aa90aa315eee60b1acc40f
workflow-type: tm+mt
source-wordcount: '1146'
ht-degree: 2%

---

# Configurare il provider Sinch {#sms-configuration-sinch}

Quando utilizzi il provider Sinch con Journey Optimizer, puoi trovare tre opzioni distinte:

* **Configurazione SMS**: configura le credenziali API Sinch per inviare messaggi SMS senza problemi.

* **Configurazione MMS**: per i messaggi multimediali (MMS), configura le credenziali API Sinch MMS. Tieni presente che il tracciamento e la risposta ai messaggi in entrata sono gestiti dalla configurazione SMS. La configurazione MMS è valida solo per il recapito in uscita del messaggio MMS.

* **Configurazione RCS**: configura le credenziali API Sinch per inviare messaggi RCS senza problemi.

## Configurare le credenziali API per SMS{#create-api}

>[!BEGINSHADEBOX]

Se non vengono fornite parole chiave di consenso o rinuncia, vengono utilizzati messaggi di consenso standard per rispettare la privacy dell’utente. L&#39;aggiunta di parole chiave personalizzate sostituisce automaticamente le impostazioni predefinite.

**Parole chiave predefinite:**

* **Consenso**: SOTTOSCRIVI, SÌ, RIPRENDI, AVVIA, CONTINUA, RIPRENDI, INIZIA
* **Rinuncia**: INTERROMPI, ESCI, ANNULLA, TERMINA, ANNULLA ISCRIZIONE, NO
* **Guida**: GUIDA

>[!ENDSHADEBOX]

Per configurare il provider Sinch per l’invio di messaggi SMS e MMS con Journey Optimizer, effettua le seguenti operazioni:

1. Nella barra a sinistra, passa a **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** `>` **[!UICONTROL Impostazioni SMS]** e seleziona il menu **[!UICONTROL Credenziali API]**. Fare clic sul pulsante **[!UICONTROL Crea nuove credenziali API]**.

1. Configura le credenziali API SMS, come descritto di seguito:

   +++ Elenco delle credenziali SMS per la configurazione

   | Campi di configurazione | Descrizione |
   |---|---|    
   | Fornitore SMS | Sinch |
   | Nome | Scegli un nome per le credenziali API. |
   | ID servizio e token API | Accedi alla pagina API e individua le tue credenziali nella scheda SMS. Ulteriori informazioni sono disponibili nella [documentazione di Sinch](https://developers.sinch.com/docs/sms/getting-started/){target="_blank"}. |
   | Parole chiave di Opt-in | Immetti le parole chiave predefinite o personalizzate che attiveranno automaticamente il messaggio di consenso. Per più parole chiave, utilizza valori separati da virgola. |
   | Messaggio di Opt-in | Immetti la risposta personalizzata inviata automaticamente come messaggio di consenso. |
   | Parole chiave di rinuncia | Immetti le parole chiave predefinite o personalizzate che attiveranno automaticamente il messaggio di rinuncia. Per più parole chiave, utilizza valori separati da virgola. |
   | Messaggio di rinuncia | Immetti la risposta personalizzata inviata automaticamente come messaggio di rinuncia. |
   | Parole chiave della Guida | Immetti le parole chiave predefinite o personalizzate che attiveranno automaticamente il **Messaggio di aiuto**. Per più parole chiave, utilizza valori separati da virgola. |
   | Messaggio di aiuto | Immetti la risposta personalizzata inviata automaticamente come **Messaggio di aiuto**. |
   | Parole chiave per doppio consenso | Immetti le parole chiave che attivano il doppio processo di consenso. Se un profilo utente non esiste, viene creato a conferma avvenuta correttamente. Per più parole chiave, utilizza valori separati da virgola. [Ulteriori informazioni sul doppio consenso SMS](https://video.tv.adobe.com/v/3427129/?learn=on). |
   | Doppio messaggio di consenso | Immetti la risposta personalizzata inviata automaticamente in risposta alla conferma del doppio consenso. |
   | Numero in entrata | Aggiungi un numero in entrata univoco o un codice breve. Questo consente di utilizzare le stesse credenziali API in sandbox diverse, ciascuna con il proprio numero in entrata o codice breve. |
   | Parole chiave in entrata personalizzate | Definisci parole chiave univoche per azioni specifiche, ad esempio SCONTO, OFFERTE, ISCRIZIONE. Queste parole chiave vengono acquisite e memorizzate come attributi nel profilo, consentendoti di attivare una qualificazione del segmento di streaming all’interno del percorso e di fornire una risposta o un’azione personalizzata. |
   | Messaggio di risposta in entrata predefinito | Immetti la risposta predefinita inviata quando un utente finale invia un SMS in entrata che non corrisponde a nessuna delle parole chiave definite. |
   | Sovrascrivi URL | Immetti l’URL personalizzato per sostituire gli endpoint predefiniti per rapporti di consegna SMS, dati di feedback, messaggi in entrata o notifiche di eventi. Sinch invierà tutti gli aggiornamenti rilevanti a questo URL invece di quelli predefiniti. |

   +++

1. Abilita l&#39;opzione **[!UICONTROL Rinuncia fuzzy]** per rilevare messaggi simili alle parole chiave di rinuncia (ad esempio, &#39;CANCIL&#39;) e personalizzare la risposta di conferma nel campo **[!UICONTROL Risposta automatica fuzzy]**.

   **[!UICONTROL La rinuncia fuzzy]** identifica i messaggi SMS che indicano che un utente desidera annullare l&#39;abbonamento, anche se il messaggio non corrisponde esattamente a una parola chiave di rinuncia definita. È in grado di rilevare frasi di rinuncia comuni e alcuni termini offensivi, garantendo il rispetto delle preferenze utente e la conformità delle campagne.

1. Fai clic su **[!UICONTROL Invia]** al termine della configurazione delle credenziali API.

1. Nel menu **[!UICONTROL Credenziali API]**, fai clic sull&#39;icona bin per eliminare le credenziali API.

1. Per modificare le credenziali esistenti, individuare le credenziali API desiderate e fare clic sull&#39;opzione **[!UICONTROL Modifica]** per apportare le modifiche necessarie.

1. Fai clic su **[!UICONTROL Verifica connessione SMS]**, dalle credenziali API esistenti, per verificare le credenziali API SMS inviando un messaggio di esempio a un dispositivo designato.

1. Compila i campi **Numero** e **Messaggio** e fai clic su **[!UICONTROL Verifica connessione]**.

   >[!IMPORTANT]
   >
   >Il messaggio deve essere strutturato in modo da essere allineato al formato di payload del provider.

   ![](assets/verify-connection.png)

Dopo aver creato e configurato le credenziali API, ora è necessario creare una configurazione del canale per i messaggi SMS. [Ulteriori informazioni](sms-configuration-surface.md)

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

Dopo aver creato e configurato le credenziali API, ora è necessario creare una configurazione del canale per i messaggi MMS. [Ulteriori informazioni](sms-configuration-surface.md)


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


