---
solution: Journey Optimizer
product: journey optimizer
title: Configurare il provider Sinch
description: Scopri come configurare l’ambiente per l’invio di messaggi di testo con Journey Optimizer con Sinch
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 85412a85-edf0-4069-8bc7-b80371375f1f
source-git-commit: c9a35c2950c061318f673cdd53d0a5fd08063c27
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 3%

---

# Configurare il provider Sinch {#sms-configuration-sinch}

Quando utilizzi il provider Sinch con Journey Optimizer, puoi trovare due opzioni distinte:

* **Configurazione SMS**: configura le credenziali API Sinch per inviare messaggi SMS senza problemi.

* **Configurazione MMS**: per i messaggi multimediali (MMS), configura le credenziali API Sinch MMS. Tieni presente che il tracciamento e la risposta ai messaggi in entrata sono gestiti dalla configurazione SMS. La configurazione MMS è valida solo per il recapito in uscita del messaggio MMS.

## Credenziali API Sinch{#create-api}

Per configurare il provider Sinch per l’invio di messaggi SMS e MMS con Journey Optimizer, effettua le seguenti operazioni:

1. Nella barra a sinistra, passa a **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** `>` **[!UICONTROL Impostazioni SMS]** e seleziona il menu **[!UICONTROL Credenziali API]**. Fare clic sul pulsante **[!UICONTROL Crea nuove credenziali API]**.

1. Configura le credenziali API SMS, come descritto di seguito:

   * **[!UICONTROL Fornitore SMS]**: Sinch.

   * **[!UICONTROL Nome]**: scegli un nome per le credenziali API.

   * **[!UICONTROL ID servizio]** e **[!UICONTROL Token API]**: accedi alla pagina API e trova le credenziali nella scheda SMS. Ulteriori informazioni nella [documentazione di Sinch](https://developers.sinch.com/docs/sms/getting-started/){target="_blank"}.

   * **[!UICONTROL Parole chiave di consenso]**: immetti le parole chiave predefinite o personalizzate che attiveranno automaticamente il **[!UICONTROL Messaggio di consenso]**. Per più parole chiave, utilizza valori separati da virgola.

   * **[!UICONTROL Messaggio di consenso]**: immetti la risposta personalizzata inviata automaticamente come **[!UICONTROL Messaggio di consenso]**.

   * **[!UICONTROL Parole chiave di rinuncia]**: immetti le parole chiave predefinite o personalizzate che attiveranno automaticamente il **[!UICONTROL Messaggio di rinuncia]**. Per più parole chiave, utilizza valori separati da virgola.

   * **[!UICONTROL Messaggio di rinuncia]**: immetti la risposta personalizzata inviata automaticamente come **[!UICONTROL Messaggio di rinuncia]**.

   * **[!UICONTROL Parole chiave della Guida]**: immetti le parole chiave predefinite o personalizzate che attiveranno automaticamente il **Messaggio della Guida**. Per più parole chiave, utilizza valori separati da virgola.

   * **[!UICONTROL Messaggio di aiuto]**: immetti la risposta personalizzata inviata automaticamente come **Messaggio di aiuto**.

   * **[!UICONTROL Parole chiave per doppio consenso]**: inserisci le parole chiave che attivano il processo di doppio consenso. Se un profilo utente non esiste, viene creato a conferma avvenuta correttamente. Per più parole chiave, utilizza valori separati da virgola. [Ulteriori informazioni sul consenso SMS Double](https://video.tv.adobe.com/v/3427129/?learn=on).

   * **[!UICONTROL Doppio messaggio di consenso]**: inserisci la risposta personalizzata inviata automaticamente in risposta alla conferma del doppio consenso.

   * **[!UICONTROL Numero in entrata]**: aggiungi il tuo numero in entrata univoco o il tuo codice breve. Questo consente di utilizzare le stesse credenziali API in sandbox diverse, ciascuna con il proprio numero in entrata o codice breve.

   * **[!UICONTROL Parole chiave in entrata personalizzate]**: definisci parole chiave univoche per azioni specifiche, ad esempio SCONTO, OFFERTE, ISCRIZIONE. Queste parole chiave vengono acquisite e memorizzate come attributi nel profilo, consentendoti di attivare una qualificazione del segmento di streaming all’interno del percorso e di fornire una risposta o un’azione personalizzata.

   * **[!UICONTROL Messaggio di risposta in entrata predefinito]**: immettere la risposta predefinita inviata quando un utente finale invia un SMS in entrata che non corrisponde a nessuna delle parole chiave definite.

1. Fai clic su **[!UICONTROL Invia]** al termine della configurazione delle credenziali API.

1. Nel menu **[!UICONTROL Credenziali API]**, fai clic sull&#39;icona bin per eliminare le credenziali API.

1. Per modificare le credenziali esistenti, individuare le credenziali API desiderate e fare clic sull&#39;opzione **[!UICONTROL Modifica]** per apportare le modifiche necessarie.

Dopo aver creato e configurato le credenziali API, ora è necessario creare una configurazione del canale per i messaggi SMS. [Ulteriori informazioni](sms-configuration-surface.md)

## Credenziali API Sinch MMS {#sinch-mms}

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

   * **[!UICONTROL ID piano di servizio]** e **[!UICONTROL Token API SMS]**: il **[!UICONTROL ID piano di servizio]** e il **[!UICONTROL Token API SMS]** si trovano nella scheda SMS della pagina API.

1. Fai clic su **[!UICONTROL Invia]** al termine della configurazione delle credenziali API.

1. Nel menu **[!UICONTROL Credenziali API]**, fai clic sull&#39;icona bin per eliminare le credenziali API.

1. Per modificare le credenziali esistenti, individuare le credenziali API desiderate e fare clic sull&#39;opzione **[!UICONTROL Modifica]** per apportare le modifiche necessarie.

Dopo aver creato e configurato le credenziali API, ora è necessario creare una configurazione del canale per i messaggi MMS. [Ulteriori informazioni](sms-configuration-surface.md)
