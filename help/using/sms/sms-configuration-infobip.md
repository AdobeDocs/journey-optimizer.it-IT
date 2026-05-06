---
solution: Journey Optimizer
product: journey optimizer
title: Configurare il provider Infobip
description: Scopri come configurare l’ambiente per l’invio di messaggi di testo e MMS con Journey Optimizer con Infobip
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 7b6dc89a-1a81-49c2-b2a7-bf24b9d215e3
source-git-commit: ea2753bd9ce7372e53fefc7816d19a7a3c73b87d
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 1%

---

# Configurare il provider Infobip {#sms-configuration-infobip}

Integrando Infobip con Adobe Journey Optimizer, puoi inviare messaggi di testo ai profili come parte dei tuoi percorsi e delle tue campagne.

Per configurare Infobip come provider SMS, segui i passaggi seguenti:

1. [Crea credenziali API](#api-credential)
1. [Creare webhook](sms-webhook.md)
1. [Crea configurazione canale](sms-configuration-surface.md)
1. [Creare un Percorso o una campagna con un’azione del canale SMS](create-sms.md)

## Configurare le credenziali API per SMS {#api-credential}

Per configurare Infobip con Journey Optimizer, eseguire la procedura seguente:

1. Nella barra a sinistra, passa a **[!UICONTROL Amministrazione]** `>` **[!UICONTROL Canali]** e seleziona il menu **[!UICONTROL Credenziali API]**. Fare clic sul pulsante **[!UICONTROL Crea nuove credenziali API]**.

1. Configura le credenziali API SMS, come descritto di seguito:

   +++ Elenco delle credenziali SMS per la configurazione

   | Campi di configurazione | Descrizione |
   |---|---|
   | Fornitore SMS | Infobip |
   | Nome | Scegli un nome per le credenziali API. |
   | URL di base API e chiave API | Per trovare le credenziali, accedi alla home page dell’interfaccia web o alla pagina di gestione delle chiavi API. Per gli endpoint di dominio regionali o alternativi, ad esempio `api-ny2.infobip.com`, specificare l&#39;URL di base completo e verificare il token di autorizzazione con il supporto di Infobip. </br>Ulteriori informazioni nella [documentazione Infobip](https://www.infobip.com/docs/api){target="_blank"} |
   | ID entità principale | Immettere l&#39;ID entità entità principale DLT assegnato. |
   | ID modello contenuto | Immetti l&#39;ID del modello di contenuto DLT registrato. |
   | Periodo di validità | Immetti il periodo di validità del messaggio in ore. Nel caso in cui i messaggi non possano essere consegnati entro questo intervallo di tempo, il sistema effettuerà ulteriori tentativi per inviarli nuovamente. Il periodo di validità predefinito è impostato su 48 ore. |
   | Dati callback | Immetti i dati client aggiuntivi che verranno inviati sull’URL di notifica. |
   | Numero in entrata | Aggiungi il tuo numero univoco in entrata. Questo consente di utilizzare le stesse credenziali API in sandbox diverse, ciascuna con il proprio numero in entrata. |

   +++

1. Abilita l&#39;opzione **[!UICONTROL Rinuncia fuzzy]** per rilevare messaggi simili alle parole chiave di rinuncia (ad esempio, &#39;CANCIL&#39;) e personalizzare la risposta di conferma nel campo **[!UICONTROL Risposta automatica fuzzy]**.

   **[!UICONTROL La rinuncia fuzzy]** identifica i messaggi SMS che indicano che un utente desidera annullare l&#39;abbonamento, anche se il messaggio non corrisponde esattamente a una parola chiave di rinuncia definita. È in grado di rilevare frasi di rinuncia comuni e alcuni termini offensivi, garantendo il rispetto delle preferenze utente e la conformità delle campagne.

1. Seleziona **[!UICONTROL Usa set di dati personalizzato per in entrata]** per instradare gli SMS in entrata di questa credenziale a un set di dati precreato scelto dal menu a discesa. [Ulteriori informazioni sulla creazione di set di dati](../experience-decisioning/data-collection/create-dataset.md)

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

Dopo aver creato e configurato le credenziali API, ora è necessario creare una configurazione del canale per i messaggi SMS e MMS. [Ulteriori informazioni](sms-configuration-surface.md)

## Configurare le credenziali API per RCS

La messaggistica RCS è supportata in Adobe Journey Optimizer tramite Infobip utilizzando la funzionalità [Provider SMS personalizzato](sms-configuration-custom.md). Ciò consente la distribuzione di messaggi avanzati e interattivi tramite profili aziendali verificati, incorporando elementi quali caroselli, pulsanti e contenuti multimediali.

➡️ [Scopri come Infobip supporta RCS nella documentazione di Infobip](https://www.infobip.com/docs/api/channels/rcs)

Per abilitare la messaggistica RCS con Infobip, è necessario configurare le nuove credenziali API tramite un provider SMS personalizzato. Le credenziali SMS di Infobip esistenti non sono compatibili, in quanto RCS richiede un formato di payload distinto.

Per configurare RCS con Infobip:

1. **Registra la tua attività per RCS tramite Infobip**

   Inizia completando il processo di onboarding e registrazione RCS all’interno della piattaforma Infobip. Ciò comporta la configurazione del profilo del mittente RCS e la verifica che l’account sia abilitato per RCS. Ulteriori informazioni sono disponibili nella [documentazione di Infobip](https://www.infobip.com/docs/rcs/get-started)

1. **Creare un webhook SMS**

   [Configura un webhook SMS personalizzato](sms-configuration-custom.md#webhook) in Journey Optimizer. Questo webhook sarà responsabile della gestione delle conferme di recapito, dei messaggi RCS in entrata e degli aggiornamenti dello stato dalla piattaforma Infobip.

1. **Crea credenziali API utilizzando Personalizzato come fornitore SMS**

   [Creare una nuova credenziale API](sms-configuration-custom.md#api-credential) in Journey Optimizer, selezionando &quot;Personalizzato&quot; come provider SMS. Utilizza il metodo di autenticazione dell’endpoint RCS appropriato, l’URL di base e le intestazioni.

Dopo aver creato e configurato le credenziali API, devi creare [il tuo webhook](sms-webhook.md) e una configurazione del canale per i messaggi RCS. [Ulteriori informazioni](sms-configuration-surface.md)
