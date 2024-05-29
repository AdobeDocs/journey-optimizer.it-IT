---
solution: Journey Optimizer
product: journey optimizer
title: Configurare il provider Infobip
description: Scopri come configurare l’ambiente per l’invio di messaggi di testo e MMS con Journey Optimizer con Infobip
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 7b6dc89a-1a81-49c2-b2a7-bf24b9d215e3
source-git-commit: 8f045e1b709c0059ce21cda68c21e8732f58e51e
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 5%

---

# Configurare il provider Infobip {#sms-configuration-infobip}

Per configurare Infobip con Journey Optimizer, eseguire la procedura seguente:

1. Nella barra a sinistra, passa a **[!UICONTROL Amministrazione]** `>` **[!UICONTROL Canali]** e seleziona la **[!UICONTROL Credenziali API]** menu. Fai clic su **[!UICONTROL Crea nuove credenziali API]** pulsante.

1. Configura le credenziali API come descritto di seguito.

   * **[!UICONTROL Fornitore SMS]**: Infobip.

   * **[!UICONTROL Nome]**: scegli un nome per le credenziali API.

   * **[!UICONTROL URL di base API]** e **[!UICONTROL Chiave API]**: accedi alla pagina home dell’interfaccia web o alla pagina gestione delle chiavi API per trovare le tue credenziali. Ulteriori informazioni in [Documentazione di Infobip](https://www.infobip.com/docs/api){target="_blank"}.

   * **[!UICONTROL Parole chiave di Opt-in]**: immetti le parole chiave predefinite o personalizzate che attiveranno automaticamente il **[!UICONTROL Messaggio di Opt-in]**. Per più parole chiave, utilizza valori separati da virgola.

   * **[!UICONTROL Messaggio di Opt-in]**: inserisci la risposta personalizzata inviata automaticamente come **[!UICONTROL Messaggio di Opt-in]**.

   * **[!UICONTROL Parole chiave di rinuncia]**: immetti il valore predefinito o le parole chiave che attiveranno automaticamente il **[!UICONTROL Messaggio di rinuncia]**. Per più parole chiave, utilizza valori separati da virgola.

   * **[!UICONTROL Messaggio di rinuncia]**: inserisci la risposta personalizzata inviata automaticamente come **[!UICONTROL Messaggio di rinuncia]**.

   * **[!UICONTROL Parole chiave della Guida]**: immetti le parole chiave predefinite o personalizzate che attiveranno automaticamente il **Messaggio di aiuto**. Per più parole chiave, utilizza valori separati da virgola.

   * **[!UICONTROL Messaggio di aiuto]**: inserisci la risposta personalizzata inviata automaticamente come **Messaggio di aiuto**.

   * **[!UICONTROL Parole chiave per doppio consenso]**: immetti le parole chiave che attivano il processo di doppio consenso. Se un profilo utente non esiste, viene creato a conferma avvenuta correttamente. Per più parole chiave, utilizza valori separati da virgola.

   * **[!UICONTROL Doppio messaggio di consenso]**: inserisci la risposta personalizzata che viene inviata automaticamente in risposta alla conferma del doppio consenso.

   * **[!UICONTROL ID entità principale]**: inserisci l&#39;ID entità principale DLT assegnato.

   * **[!UICONTROL ID modello contenuto]**: immetti l&#39;ID del modello di contenuto DLT registrato.

   * **[!UICONTROL Periodo di validità]**: inserisci il periodo di validità del messaggio in ore. Nel caso in cui i messaggi non possano essere consegnati entro questo intervallo di tempo, il sistema effettuerà ulteriori tentativi per inviarli nuovamente. Il periodo di validità predefinito è impostato su 48 ore.

   * **[!UICONTROL Dati callback]**: inserisci i dati client aggiuntivi che verranno inviati sull’URL di notifica.

1. Clic **[!UICONTROL Invia]** al termine della configurazione delle credenziali API.

Dopo aver creato e configurato le credenziali API, ora è necessario creare una superficie di canale per i messaggi SMS e MMS. [Ulteriori informazioni](sms-configuration-surface.md)
