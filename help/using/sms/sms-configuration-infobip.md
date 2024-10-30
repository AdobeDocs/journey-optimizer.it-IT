---
solution: Journey Optimizer
product: journey optimizer
title: Configurare il provider Infobip
description: Scopri come configurare l’ambiente per l’invio di messaggi di testo e MMS con Journey Optimizer con Infobip
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 7b6dc89a-1a81-49c2-b2a7-bf24b9d215e3
source-git-commit: c9a35c2950c061318f673cdd53d0a5fd08063c27
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 4%

---

# Configurare il provider Infobip {#sms-configuration-infobip}

Per configurare Infobip con Journey Optimizer, eseguire la procedura seguente:

1. Nella barra a sinistra, passa a **[!UICONTROL Amministrazione]** `>` **[!UICONTROL Canali]** e seleziona il menu **[!UICONTROL Credenziali API]**. Fare clic sul pulsante **[!UICONTROL Crea nuove credenziali API]**.

1. Configura le credenziali API come descritto di seguito.

   * **[!UICONTROL Fornitore SMS]**: Infobip.

   * **[!UICONTROL Nome]**: scegli un nome per le credenziali API.

   * **[!UICONTROL URL di base API]** e **[!UICONTROL chiave API]**: accedi alla home page dell&#39;interfaccia Web o alla pagina di gestione della chiave API per trovare le tue credenziali. Ulteriori informazioni sono disponibili nella [documentazione Infobip](https://www.infobip.com/docs/api){target="_blank"}.

   * **[!UICONTROL Parole chiave di consenso]**: immetti le parole chiave predefinite o personalizzate che attiveranno automaticamente il **[!UICONTROL Messaggio di consenso]**. Per più parole chiave, utilizza valori separati da virgola.

   * **[!UICONTROL Messaggio di consenso]**: immetti la risposta personalizzata inviata automaticamente come **[!UICONTROL Messaggio di consenso]**.

   * **[!UICONTROL Parole chiave di rinuncia]**: immetti le parole chiave predefinite o che attiveranno automaticamente il **[!UICONTROL Messaggio di rinuncia]**. Per più parole chiave, utilizza valori separati da virgola.

   * **[!UICONTROL Messaggio di rinuncia]**: immetti la risposta personalizzata inviata automaticamente come **[!UICONTROL Messaggio di rinuncia]**.

   * **[!UICONTROL Parole chiave della Guida]**: immetti le parole chiave predefinite o personalizzate che attiveranno automaticamente il **Messaggio della Guida**. Per più parole chiave, utilizza valori separati da virgola.

   * **[!UICONTROL Messaggio di aiuto]**: immetti la risposta personalizzata inviata automaticamente come **Messaggio di aiuto**.

   * **[!UICONTROL Parole chiave per doppio consenso]**: inserisci le parole chiave che attivano il processo di doppio consenso. Se un profilo utente non esiste, viene creato a conferma avvenuta correttamente. Per più parole chiave, utilizza valori separati da virgola.

   * **[!UICONTROL Doppio messaggio di consenso]**: inserisci la risposta personalizzata inviata automaticamente in risposta alla conferma del doppio consenso.

   * **[!UICONTROL ID entità principale]**: immettere l&#39;ID entità principale DLT assegnato.

   * **[!UICONTROL ID modello di contenuto]**: immetti l&#39;ID del modello di contenuto DLT registrato.

   * **[!UICONTROL Periodo di validità]**: inserisci il periodo di validità del messaggio in ore. Nel caso in cui i messaggi non possano essere consegnati entro questo intervallo di tempo, il sistema effettuerà ulteriori tentativi per inviarli nuovamente. Il periodo di validità predefinito è impostato su 48 ore.

   * **[!UICONTROL Dati callback]**: immettere i dati client aggiuntivi che verranno inviati nell&#39;URL di notifica.

   * **[!UICONTROL Numero in entrata]**: aggiungi il tuo numero univoco in entrata. Questo consente di utilizzare le stesse credenziali API in sandbox diverse, ciascuna con il proprio numero in entrata.

   * **[!UICONTROL Parole chiave in entrata personalizzate]**: definisci parole chiave univoche per azioni specifiche, ad esempio SCONTO, OFFERTE, ISCRIZIONE. Queste parole chiave vengono acquisite e memorizzate come attributi nel profilo, consentendoti di attivare una qualificazione del segmento di streaming all’interno del percorso e di fornire una risposta o un’azione personalizzata.

   * **[!UICONTROL Messaggio di risposta in entrata predefinito]**: immettere la risposta predefinita inviata quando un utente finale invia un SMS in entrata che non corrisponde a nessuna delle parole chiave definite.

1. Fai clic su **[!UICONTROL Invia]** al termine della configurazione delle credenziali API.

1. Nel menu **[!UICONTROL Credenziali API]**, fai clic sull&#39;icona bin per eliminare le credenziali API.

1. Per modificare le credenziali esistenti, individuare le credenziali API desiderate e fare clic sull&#39;opzione **[!UICONTROL Modifica]** per apportare le modifiche necessarie.

Dopo aver creato e configurato le credenziali API, ora è necessario creare una configurazione del canale per i messaggi SMS e MMS. [Ulteriori informazioni](sms-configuration-surface.md)
