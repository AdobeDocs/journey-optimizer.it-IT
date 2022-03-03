---
title: Introduzione ai percorsi
description: Introduzione ai percorsi
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
source-git-commit: dee8dbac067dac851af02d87a3dece1ba2b29376
workflow-type: tm+mt
source-wordcount: '1721'
ht-degree: 7%

---

# Introduzione ai percorsi{#jo-quick-start}

## Prerequisiti

In order to send messages with journeys, the following configuration is required:

1. **** You define the expected information and how to process it. e viene eseguita da un **utente tecnico**. [Ulteriori informazioni](../event/about-events.md).

   ![](assets/jo-event7bis.png)

1. **** For this, you need to create segments. [Ulteriori informazioni](../segment/about-segments.md).

   ![](assets/segment2.png)

1. **** Al momento del provisioning, viene configurata anche un’origine dati integrata in Adobe Experience Platform. Se sfrutti solo i dati degli eventi del tuo percorso, questo passaggio non è necessario e viene eseguita da un **utente tecnico**. [Ulteriori informazioni](../datasource/about-data-sources.md)

   ![](assets/jo-datasource.png)

1. **** Vedi [questa sezione](../messages/get-started-content.md). If you&#39;re using a third-party system to send your messages, you can create a custom action. [](../action/action.md) e viene eseguita da un **utente tecnico**.

   ![](assets/create-content-push.png)

## Building your journey{#jo-build}

**** This is where you create your journeys. Combina le diverse attività relative a un evento, un percorso e un’azione in modo da creare scenari tra canali con più passaggi.

Here are the main steps to send messages through journeys:

1. **[!UICONTROL Journeys]** The list of journeys is displayed.

   ![](assets/interface-journeys.png)

1. **[!UICONTROL Create Journey]**

1. Modifica le proprietà del percorso nel riquadro di configurazione visualizzato sul lato destro. [](journey-gs.md#change-properties)

   ![](assets/jo-properties.png)

1. **** [](using-the-journey-designer.md)

   ![](assets/read-segment.png)

1. Drag and drop the next steps that the individual will follow. For example, you can add a condition followed by a message. [](using-the-journey-designer.md)

1. Test your journey using test profiles. [](testing-the-journey.md)

1. Publish your journey to activate it. [](publishing-the-journey.md)

   ![](assets/jo-journeyuc2_32bis.png)

1. Monitor your journey using the dedicated reporting tools to measure your journey&#39;s effectiveness. [](../reports/live-report.md)

   ![](assets/jo-dynamic_report_journey_12.png)

## Modifica delle proprietà {#change-properties}

Click on the pencil icon, in the top right to access the journey&#39;s properties.

**[!UICONTROL Timeout and error]**

For live journeys, this screen displays the publication date and the name of the user who published the journey.

**** The following information is copied: JourneyVersion UID, OrgID, orgName, sandboxName, lastDeployedBy, lastDeployedAt.

![](assets/journey32.png)

### Entrance{#entrance}

By default, new journeys allow re-entrance. You can uncheck the option for “one shot” journeys, for example if you want to offer a one-time gift when a person enters a shop. In that case, you don&#39;t want the customer to be able to re-enter the journey and receive the offer again.

**[!UICONTROL Closed]** The journey will stop letting new individuals enter the journey. Persons already in the journey will finish the journey normally.

**** [](../building-journeys/journey-gs.md#global_timeout)

### Timeout and error in journey activities {#timeout_and_error}

When editing an action or condition activity, you can define an alternative path in case of error or timeout. **[!UICONTROL Timeout and  error]**

Authorized values are between 1 and 30 seconds.

**[!UICONTROL Timeout and error]** If your journey is less time sensitive, you can use a longer value to give more time to the system called to send a valid response.

Journeys also uses a global timeout. [](#global_timeout)

### Global journey timeout {#global_timeout}

[](#timeout_and_error) This timeout will stop the progress of individuals in the journey 30 days after they enter. This means that an individual&#39;s journey cannot last longer than 30 days. After the 30 day timeout period, the individual&#39;s data is deleted. Individuals still flowing in the journey at the end of the timeout period will be stopped and they will be taken into account as errors in reporting.

>[!NOTE]
>
>Journeys do not directly react to privacy opt-out, access or delete requests. However, the global timeout ensures that individuals never stay more than 30 days in any journey.

Due to the 30-day journey timeout, when journey re-entrance is not allowed, we cannot make sure the re-entrance blocking will work more than 30 days. Indeed, as we remove all information about persons who entered the journey 30 days after they enter, we cannot know the person entered previously, more than 30 days ago.

### Timezone and profile timezone {#timezone}

Timezone are defined at journey level.

You can enter a fixed time zone or use Adobe Experience Platform profiles to define the journey time zone.

[](../building-journeys/timezone-management.md)

### Burst mode {#burst}

Burst mode is a paid add-on that allows very fast push message sending in large volumes. It is used for simple journeys that include a read segment and a simple push message. Burst is used when delay in message delivery is business-critical, when you want to send an urgent push alert on mobile phones, for example a breaking news to users who have installed your news channel app.

Limitazioni:

* The journey must start with a read segment. Events are not allowed.
* The next step must be a push message. No other activity or step is allowed (except the optional end activity):
   * Push channel only
   * No personalization is allowed in the message
   * The message must be small (&lt;2KB)

Important note:

If any of the requirements is not fulfilled, burst mode will not be available in the journey.

To activate Burst mode, open your journey and click the pencil icon, in the top right to access the journey&#39;s properties. ****

![](assets/burst.png)

Burst mode will be deactivated if you modify a burst journey and add an activity that is not compliant with burst (message, any other action, an event etc.). A message will be displayed.

![](assets/burst2.png)

Then test and publish your journey normally. Test mode messages are not sent via the burst mode.

## Ending a journey

A journey can end for an individual because of two reasons:

* The person arrives at the last activity of a path. This last activity can be an end activity or another activity. There is no obligation to end a path with an end activity. Consulta [questa pagina](../building-journeys/end-activity.md).
* The person arrives at a condition activity (or a wait activity with a condition) and does not match any of the conditions.

The person can then re-enter the journey if re-entrance is allowed. Consulta [questa pagina](../building-journeys/journey-gs.md#change-properties)

A journey can close because of the following reasons:

* **[!UICONTROL Close to new entrances]**
* A one-shot segment based journey that has finished executing.
* After the last occurrence of a recurring segment based journey.

**[!UICONTROL Closed]** The journey will stop letting new individuals enter the journey. Persons already in the journey will finish the journey normally. **** [](../building-journeys/journey-gs.md#global_timeout)

In case you need to stop the progress of all individuals in the journey, you can stop it. Stopping the journey will timeout all individuals in the journey.

Here is how you close or stop a journey manually:

**[!UICONTROL Stop]****[!UICONTROL Close to new entrances]****** **** This is the most recommended way to put an end to a journey as it offers the best experience for customers. Stopping a journey involves that people who already entered a journey are all stopped in their progress. The journey is basically switched off.

>[!NOTE]
>
>Note that you cannot resume a closed or stopped journey.

### Closing a journey

You can close a journey manually to ensure that customers who already entered the journey can finish their path but new users are not able to enter the journey.

**[!UICONTROL Closed]** **** [](../building-journeys/journey-gs.md#global_timeout)

A closed journey version cannot be restarted or deleted. You can create a new version of it or duplicate it. Only finished journeys can be deleted.

**[!UICONTROL Ellipsis]****[!UICONTROL Close to new entrances]**

![](assets/journey-finish-quick-action.png)

È inoltre possibile:

1. **[!UICONTROL Journeys]**
1. On the top-right, click the down arrow.

   ![](assets/finish_drop_down_list.png)

1. Fai clic su **[!UICONTROL Close to new entrances]**. Viene visualizzata una finestra di dialogo.
1. **[!UICONTROL Close to new entrances]**

### Stopping a journey

You can stop a journey when an emergency occurred and all processing needs to be ended immediately on a journey.

A stopped journey version cannot be restarted.

**[!UICONTROL Stopped]**

You can stop a journey, for example, if a marketer realizes that the journey targets the wrong audience or a custom action supposed to deliver messages is not working correctly. **[!UICONTROL Ellipsis]****[!UICONTROL Stop]**

![](assets/journey-finish-quick-action.png)

È inoltre possibile:

1. **[!UICONTROL Journeys]**
1. On the top-right, click on the down arrow.

![](assets/finish_drop_down_list.png)

1. Fai clic su **[!UICONTROL Stop]**. Viene visualizzata una finestra di dialogo.
1. **[!UICONTROL Stop]**
