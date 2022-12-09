---
solution: Journey Optimizer
product: journey optimizer
title: Avviare l’esecuzione del percorso
description: Scopri come avviare il percorso e inviare messaggi
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---


# Esecuzione del percorso {#message-execution}

## Testare il percorso

Puoi testare il percorso utilizzando i profili di test. Questo passaggio è consigliato per convalidare le impostazioni e i messaggi.

Ulteriori informazioni [sezione](testing-the-journey.md).

## Attiva il percorso

Devi pubblicare il percorso per attivarlo.

![](assets/jo-journeyuc2_32bis.png)

Ulteriori informazioni [sezione](publishing-the-journey.md).


Una volta pubblicato, puoi monitorare il percorso utilizzando gli strumenti di reporting dedicati per misurare l’efficacia del percorso.

![](assets/jo-dynamic_report_journey_12.png)

[Ulteriori informazioni sui report](../reports/live-report.md)

## Inviare messaggi {#send-messages}

Quando il messaggio ha un contenuto definito, è pronto per essere inviato tramite un [viaggio](journey.md).

Una volta inviato un messaggio, puoi monitorarne l’esecuzione tramite più indicatori. [Ulteriori informazioni sul reporting](../global-report.md).

## Pianificare messaggi {#schedule-messages}

I messaggi possono essere pianificati tramite **[!UICONTROL Read Segment]** attività in un [viaggio](journey.md). Puoi specificare quando il segmento entrerà nel percorso. [Ulteriori informazioni sull’attività Leggi segmento](read-segment.md).

A questo scopo, segui i passaggi seguenti:

1. Modificare un percorso, trascinarlo e rilasciarlo **[!UICONTROL Read Segment]** e inizia a configurarlo. [Ulteriori informazioni sulla configurazione dell’attività Leggi segmento](read-segment.md#configuring-segment-trigger-activity).

1. Fai clic sul pulsante **[!UICONTROL Edit journey schedule]** per accedere alle proprietà del percorso.

   ![](assets/message-read-segment-schedule.png)

1. Configura le **[!UICONTROL Scheduler type]** campo: seleziona il valore desiderato dall’elenco per far sì che il segmento entri nel percorso in una data/ora specifica o su base ricorrente.

   >[!NOTE]
   >
   >La **[!UICONTROL Schedule]** è disponibile solo quando una **[!UICONTROL Read Segment]** l’attività è stata rilasciata nell’area di lavoro.

   ![](assets/message-read-segment-scheduler.png)

1. Se si seleziona **[!UICONTROL Once]**, definisci una data e un’ora specifiche in cui il segmento entrerà nel percorso.

   ![](assets/message-read-segment-scheduler-once.png)

1. Se selezioni un metodo ricorrente, modifica la data e l&#39;ora di inizio. Puoi anche definire una data e un’ora di fine facoltative.

   ![](assets/message-read-segment-scheduler-daily.png)

   >[!NOTE]
   >
   >Per impostazione predefinita, i segmenti entrano nel percorso **[!UICONTROL As soon as possible]**, ovvero 1 ora dopo la pubblicazione del percorso.

1. Fai clic su **[!UICONTROL OK]** per salvare le modifiche.

<!--Unitary messages that are triggered by an event within a journey cannot be scheduled.-->
