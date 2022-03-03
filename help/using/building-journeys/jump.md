---
title: Passaggio da un percorso a un altro
description: Passaggio da un percorso a un altro
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 46d8950b-8b02-4160-89b4-1c492533c0e2
source-git-commit: dee8dbac067dac851af02d87a3dece1ba2b29376
workflow-type: tm+mt
source-wordcount: '801'
ht-degree: 3%

---

# Jump from one journey to another {#jump}

**[!UICONTROL Jump]** This feature allows you to:

* simplify the design of very complex journeys by splitting them into several ones
* build journeys based on common and reusable journey patterns

**[!UICONTROL Jump]** **[!UICONTROL Jump]** **[!UICONTROL Jump]** The behavior is similar to other actions.

**[!UICONTROL Jump]**

>[!NOTE]
>
>[](https://experienceleague.adobe.com/docs/journey-orchestration-learn/tutorials/building-a-journey/jumping-to-another-journey.html?lang=it)

## Ciclo di vita

**[!UICONTROL Jump]**********
Here are the different steps of the execution process:

****

1. Journey A receives an external event related to an individual.
1. **[!UICONTROL Jump]**
1. **[!UICONTROL Jump]**

**[!UICONTROL Jump]**

1. Journey B received an internal event from Journey A.
1. The individual starts flowing in Journey B.

>[!NOTE]
>
>Journey B can also be triggered via an external event.

## Best practice e limitazioni

### Authoring

* **[!UICONTROL Jump]**
* You can only jump to a journey that uses the same namespace as the origin journey.
* ********
* **[!UICONTROL Jump]**********
* **[!UICONTROL Jump]** **[!UICONTROL Jump]**
* You can have as many jump levels as needed. For example, Journey A jumps to journey B, which jumps to journey C, and so on.
* **[!UICONTROL Jump]**
* Loop patterns are not supported. There is no way to link two or more journeys together which would create an infinite loop. **[!UICONTROL Jump]**

### Esecuzione

* **[!UICONTROL Jump]**
* As usual, a unique individual can only be present once in a same journey. As a result, if the individual pushed from the origin journey is already in the target journey, then the individual will not enter the target journey. **[!UICONTROL Jump]**

## Configuring the Jump activity

1. ****

   ![](assets/jump1.png)

1. **[!UICONTROL Jump]****[!UICONTROL ACTIONS]** Add a label and description.

   ![](assets/jump2.png)

1. ****
The list displays all journey versions that are draft, live or in test mode. **** Target journeys that would create a loop pattern are also filtered out.

   ![](assets/jump3.png)

   >[!NOTE]
   >
   >****

1. Select the target journey that you want to jump to.
**** **[!UICONTROL Jump]**

   ![](assets/jump4.png)

1. **** In the same way as for other types of actions, map each field with fields from the origin event or data source. This information will be passed to the target journey at runtime.
1. Add the next activities to finish your origin journey.

   ![](assets/jump5.png)


   >[!NOTE]
   >
   >The individual&#39;s identity is automatically mapped. This information is not visible in the interface.

**[!UICONTROL Jump]** **[!UICONTROL Jump]**

**[!UICONTROL Jump]****[!UICONTROL Jump]** **[!UICONTROL Jump]**

![](assets/jump7.png)

## Risoluzione dei problemi

When the journey is published or in test mode, errors will happen if:
* the target journey no longer exists
* the target journey is draft, closed or stopped
* if the first event of the target journey has changed and the mapping is broken

![](assets/jump6.png)
