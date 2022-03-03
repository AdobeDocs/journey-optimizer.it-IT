---
title: Utilizzare un segmento in un percorso
description: Learn how to use a segment in a journey
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 7b27d42e-3bfe-45ab-8a37-c55b231052ee
source-git-commit: dee8dbac067dac851af02d87a3dece1ba2b29376
workflow-type: tm+mt
source-wordcount: '1036'
ht-degree: 5%

---

# Utilizzare un segmento in un percorso {#segment-trigger-activity}

## About the Read Segment activity {#about-segment-trigger-actvitiy}

The Read Segment activity allows you to make all individuals belonging to an Adobe Experience Platform segment enter a journey. L’entrata in un percorso può essere eseguita una volta o su base regolare.

[](../segment/about-segments.md) With the Read Segment activity, you can make all individuals belonging to this segment enter a journey and make them flow into individualized journeys that will leverage all journey functionalities: conditions, timers, events, actions.

>[!NOTE]
>
>The Burst paid add-on allows very fast push message sending in large volumes for simple journeys that include a read segment and a simple push message. Per ulteriori informazioni, consulta [questa sezione](../building-journeys/journey-gs.md#burst)

### Configure the activity {#configuring-segment-trigger-activity}

The steps to configure the Read Segment activity are as follows:

1. **[!UICONTROL Orchestration]****[!UICONTROL Read Segment]**

   The activity must be positioned as the first step of a journey.

1. **[!UICONTROL Label]**

1. **[!UICONTROL Segment]****[!UICONTROL Save]**

   Note that you can customize the columns displayed in the list and sort them.

   >[!NOTE]
   >
   >******** [](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results)

   ![](assets/read-segment-selection.png)

   **[!UICONTROL Copy]**

   `{"name":"Luma app opening and checkout",”id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](assets/read-segment-copy.png)

1. **[!UICONTROL Namespace]** [](../event/about-creating.md#select-the-namespace)

   >[!NOTE]
   >
   >Individuals belonging to a segment that does not have the selected identity (namespace) among their different identities cannot enter the journey.

1. **[!UICONTROL Throttling rate]**

   This value is stored in the journey version payload. The default value is 20,000 messages per second. You can modify this value from 500 to 20,000 messages per second.

   >[!NOTE]
   >
   >The overall throttling rate per sandbox is set to 20,000 messages per second. Therefore, the throttling rate of all the read segments that run simultaneously in the same sandbox add up to at most 20,000 messages per second. You cannot modify this cap.

1. **[!UICONTROL Read Segment]** **[!UICONTROL Edit journey schedule]****[!UICONTROL Scheduler type]**

   ![](assets/read-segment-schedule.png)

   **[!UICONTROL As soon as possible]** If you want to make the segment enter the journey on a specific date/time or on a recurring basis, select the desired value from the list.

   >[!NOTE]
   >
   >**[!UICONTROL Schedule]****[!UICONTROL Read Segment]**

   ![](assets/read-segment-schedule-list.png)

   **** La prima esecuzione indirizza sempre tutti i membri del segmento. ****

<!--

### Segment filters {#segment-filters}

[!CONTEXTUALHELP]
>id="jo_segment_filters"
>title="About segment filters"
>abstract="You can choose to target only the individuals who entered or exited a specific segment during a specific time window. For example, you can decide to only retrieve all the customers who entered the VIP segment since last week."

You can choose to target only the individuals who entered or exited a specific segment during a specific time window. For example, you can decide to only retrieve all the customers who entered the VIP segment since last week. Only the new VIP customers will be targeted. All the customers who were already part of the VIP segment before will be excluded.

To activate this mode, click the **Segment Filters** toggle. Two fields are displayed:

**Segment membership**: choose whether you want to listen to segment entrances or exits. 

**Lookback window**: define when you want to start to listen to entrances or exits. This lookback window is expressed in hours, starting from the moment the journey is triggered.  If you set this duration to 0, the journey will target all members of the segment. For recurring journeys, it will take into account all entrances/exits since the last time the journey was triggered.

-->

### Test e pubblicazione del percorso {#testing-publishing}

**[!UICONTROL Read Segment]**

To do this, activate the test mode, then select the desired option from the left pane.

![](assets/read-segment-test-mode.png)

You can then configure and run the test mode as usual. [](testing-the-journey.md)

**[!UICONTROL Show logs]**

* **[!UICONTROL Single profile at a time]** Per ulteriori informazioni al riguardo, consulta [questa sezione](testing-the-journey.md#viewing_logs)

* **[!UICONTROL Up to 100 profiles at once]**

   Note that testing the journey using up to 100 profiles at once does not allow you to track the progress of the individuals in the journey using the visual flow.

   ![](assets/read-segment-log.png)

[](publishing-the-journey.md) **[!UICONTROL Scheduler]**

>[!NOTE]
>
>For recurring segment-based journeys, the journey will automatically close once its last occurrence is executed. If no end date/time has been specified, you will have to close the journey to new entrances manually to end it.

## Audience targeting in segment-based journeys

****

The audience belonging to the segment is retrieved once or on a regular basis.

After entering the journey, you can create audience orchestration use cases, making individuals from the initial segment flow into different branches of the journey.

**Segmentazione**

**** For example, you can make VIP persons take a particular path and non-VIP flow in another path.

The segmentation can be based on:

* data source data
* the context of events part of the journey data, for example: did a person click on the message received an hour ago?
* a date, for example: are we in June when a person go through the journey?
* a time, for example: is it morning in the person’s timezone?
* an algorithm splitting the audience flowing in the journey based on a percentage, for example: 90% - 10% to exclude a control group

![](assets/read-segment-audience1.png)

**Exclusion**

**** For example, you can exclude VIP persons by making them flow into a branch with an end step right after.

This exclusion could happen right after segment retrieval, for population counting purposes or along a multistep journey.

![](assets/read-segment-audience2.png)

**Unione**

Journeys allow you to create N branches and join them together after a segmentation.

As a result, you can make two audiences return to a common experience.

For example, after following a different experience during ten days in a journey, VIP and non-VIP customers can return to the same path.

After a union, you can split the audience again by performing a segmentation or an exclusion.

![](assets/read-segment-audience3.png)
