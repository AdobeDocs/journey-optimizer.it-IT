---
title: Start journey execution
description: Learn how to start your journey and send messages
source-git-commit: dee8dbac067dac851af02d87a3dece1ba2b29376
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 3%

---


# Journey execution {#message-execution}

## Test del percorso

You can test your journey using test profiles. This step is recommended to validate your settings and messages.

[](testing-the-journey.md)

## Activate your journey

You must publish your journey to activate it.

![](assets/jo-journeyuc2_32bis.png)

[](publishing-the-journey.md)


Once published, you can monitor your journey using the dedicated reporting tools to measure your journey&#39;s effectiveness.

![](assets/jo-dynamic_report_journey_12.png)

[](../reports/live-report.md)

## Inviare messaggi {#send-messages}

[](journey.md)

>[!NOTE]
>
>You can add a message that is still in draft mode to a journey, but make sure the message is published before publishing the journey.

Once a message is sent, you can monitor its execution through multiple indicators. [](../message-monitoring.md)

## Schedule messages {#schedule-messages}

**[!UICONTROL Read Segment]**[](journey.md) You can specify when the segment will enter the journey. [](read-segment.md)

Per farlo, segui la procedura indicata di seguito:

1. **[!UICONTROL Read Segment]** [](read-segment.md#configuring-segment-trigger-activity)

1. **[!UICONTROL Edit journey schedule]**

   ![](assets/message-read-segment-schedule.png)

1. **[!UICONTROL Scheduler type]**

   >[!NOTE]
   >
   >**[!UICONTROL Schedule]****[!UICONTROL Read Segment]**

   ![](assets/message-read-segment-scheduler.png)

1. **[!UICONTROL Once]**

   ![](assets/message-read-segment-scheduler-once.png)

1. If you select a recurring method, edit the start date and time. You can also define an optional end date and time.

   ![](assets/message-read-segment-scheduler-daily.png)

   >[!NOTE]
   >
   >**[!UICONTROL As soon as possible]**

1. **[!UICONTROL OK]**

<!--Unitary messages that are triggered by an event within a journey cannot be scheduled.-->
