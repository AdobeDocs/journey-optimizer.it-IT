---
solution: Journey Optimizer
product: journey optimizer
title: Configurare il provider Sinch
description: Scopri come configurare l’ambiente per l’invio di messaggi di testo con Journey Optimizer con Sinch
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 85412a85-edf0-4069-8bc7-b80371375f1f
source-git-commit: 794ac45177e467be4bd5b8f7288e07c85e4d806a
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 3%

---

# Configurare il provider Sinch {#sms-configuration-sinch}

Quando utilizzi il provider Sinch con Journey Optimizer, puoi trovare due opzioni distinte:

* **Configurazione SMS**: configura le credenziali API di Sinch per inviare messaggi SMS senza problemi.

* **Configurazione MMS**: per i messaggi multimediali (MMS), configura le credenziali API di Sinch MMS. Tieni presente che il tracciamento e la risposta ai messaggi in entrata sono gestiti dalla configurazione SMS. La configurazione MMS è valida solo per il recapito in uscita del messaggio MMS.

## Credenziali API Sinch{#create-api}

Per configurare il provider Sinch per l’invio di messaggi SMS e MMS con Journey Optimizer, effettua le seguenti operazioni:

1. Nella barra a sinistra, passa a **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** e seleziona la **[!UICONTROL Credenziali API]** menu. Fai clic su **[!UICONTROL Crea nuove credenziali API]** pulsante.

1. Configura le credenziali API SMS, come descritto di seguito:

   * **[!UICONTROL Fornitore SMS]**: Sinch

   * **[!UICONTROL Nome]**: scegli un nome per le credenziali API.

   * **[!UICONTROL ID servizio]** e **[!UICONTROL Token API]**: accedi alla pagina API, e trovi le tue credenziali nella scheda SMS. Ulteriori informazioni in [Documentazione di Sinch](https://developers.sinch.com/docs/sms/getting-started/){target="_blank"}.

   * **[!UICONTROL Parole chiave di Opt-in]**: immetti le parole chiave predefinite o personalizzate che attiveranno automaticamente il **[!UICONTROL Messaggio di Opt-in]**. Per più parole chiave, utilizza valori separati da virgola.

   * **[!UICONTROL Messaggio di Opt-in]**: inserisci la risposta personalizzata inviata automaticamente come **[!UICONTROL Messaggio di Opt-in]**.

   * **[!UICONTROL Parole chiave di rinuncia]**: immetti le parole chiave predefinite o personalizzate che attiveranno automaticamente il **[!UICONTROL Messaggio di rinuncia]**. Per più parole chiave, utilizza valori separati da virgola.

   * **[!UICONTROL Messaggio di rinuncia]**: inserisci la risposta personalizzata inviata automaticamente come **[!UICONTROL Messaggio di rinuncia]**.

   * **[!UICONTROL Parole chiave della Guida]**: immetti le parole chiave predefinite o personalizzate che attiveranno automaticamente il **Messaggio di aiuto**. Per più parole chiave, utilizza valori separati da virgola.

   * **[!UICONTROL Messaggio di aiuto]**: inserisci la risposta personalizzata inviata automaticamente come **Messaggio di aiuto**.

   * **[!UICONTROL Parole chiave per doppio consenso]**: immetti le parole chiave che attivano il processo di doppio consenso. Se un profilo utente non esiste, viene creato a conferma avvenuta correttamente. Per più parole chiave, utilizza valori separati da virgola. [Ulteriori informazioni sul doppio consenso SMS](https://video.tv.adobe.com/v/3427129/?learn=on).

   * **[!UICONTROL Doppio messaggio di consenso]**: inserisci la risposta personalizzata inviata automaticamente in risposta alla conferma del doppio consenso.

   * **[!UICONTROL Numero in entrata]**: aggiungi il tuo numero univoco in entrata. Questo consente di utilizzare le stesse credenziali API in sandbox diverse, ciascuna con il proprio numero in entrata.

1. Clic **[!UICONTROL Invia]** al termine della configurazione delle credenziali API.

Dopo aver creato e configurato le credenziali API, ora è necessario creare una superficie di canale per i messaggi SMS. [Ulteriori informazioni](sms-configuration-surface.md)

## Credenziali API Sinch MMS {#sinch-mms}

>[!IMPORTANT]
>
> Oltre alla configurazione di MMS, devi anche creare credenziali API Sinch specifiche per il tracciamento dei messaggi in entrata e la gestione delle richieste di consenso.

Per configurare Sinch MMS per l’invio di MMS con Journey Optimizer, effettua le seguenti operazioni:

1. Nella barra a sinistra, passa a **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** e seleziona la **[!UICONTROL Credenziali API]** menu. Fai clic su **[!UICONTROL Crea nuove credenziali API]** pulsante.

1. Configura le credenziali API MMS, come descritto di seguito:

   * **[!UICONTROL Fornitore SMS]**: Sinch MMS.

   * **[!UICONTROL Nome]**: scegli un nome per le credenziali API.

   * **[!UICONTROL ID Progetto]**, **[!UICONTROL ID app]** e **[!UICONTROL Token API]**: segui i passaggi seguenti per raccogliere le credenziali API MMS.

      * Per **[!UICONTROL ID Progetto]** e **[!UICONTROL ID app]**: Accedi a [Panoramica dell’API di conversazione](https://dashboard.sinch.com/convapi/overview) del progetto Sinch sul dashboard di Sinch.
      * Per **[!UICONTROL Token API]**: ottieni [Chiavi di accesso](https://community.sinch.com/t5/Customer-Dashboard/Sinch-Access-Keys/ta-p/12638) per il progetto Sinch e generare un **Token API Base64** del progetto Sinch **Chiavi di accesso**.

   * **[!UICONTROL ID piano di servizio]** e **[!UICONTROL Token API SMS]**: il tuo **[!UICONTROL ID piano di servizio]** e **[!UICONTROL Token API SMS]** si trovano nella scheda SMS della pagina API.

1. Clic **[!UICONTROL Invia]** al termine della configurazione delle credenziali API.

Dopo aver creato e configurato le credenziali API, ora è necessario creare una superficie di canale per i messaggi MMS. [Ulteriori informazioni](sms-configuration-surface.md)
