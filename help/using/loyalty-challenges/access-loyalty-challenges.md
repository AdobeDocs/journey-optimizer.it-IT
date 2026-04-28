---
solution: Journey Optimizer
product: journey optimizer
title: Accesso e gestione di sfide e attività
description: Learn how to access, manage, and organize loyalty challenges and tasks in Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
badge: label="Beta privata" type="Informative"
mini-toc-levels: 1
exl-id: 8907c18e-4623-4743-a76b-333f34e13baf
source-git-commit: 1ee6f9d74b83ca2b9c2cc0336af0f23a42f4da4f
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 2%

---

# Accesso e gestione di sfide e attività {#access-loyalty-challenges}

>[!BEGINSHADEBOX]

**Documentazione sulle sfide di fedeltà:**

* [Introduzione alle sfide di fedeltà](get-started.md)
* **Access &amp; manage challenges and tasks** ◀︎ **You are here**
* [Creare le sfide](create-challenges.md)
* [Creare le attività](create-tasks.md)
* [Riferimento API per le sfide di fedeltà](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Questa funzionalità è attualmente in **versione beta privata**. Per informazioni dettagliate sul ciclo di rilascio e sulle fasi di disponibilità, consulta [Ciclo di rilascio di Journey Optimizer](../rn/releases.md).

## Accesso e gestione di sfide e attività

To access Loyalty Challenges, navigate to Journey Optimizer and select **[!UICONTROL Loyalty Challenge (Beta)]** under the **[!UICONTROL Journey management]** section. The Loyalty Challenges interface provides a centralized location to view, manage, and organize all your challenges and tasks.

The interface provides access to two main inventories:

* **Challenges**: View and manage all loyalty challenges, monitor their status, and perform quick actions such as viewing, editing, duplicating, or deleting challenges
* **Tasks**: Browse reusable tasks that can be used across multiple challenges, and manage task definitions independently

## Challenges inventory {#challenges-tab}

The **[!UICONTROL Challenges]** tab displays all challenges sorted by last modified date, with the most recently modified challenges appearing first.

![](assets/challenges-inventory.png)

Key information displayed:

* **[!UICONTROL State]**: Current state of the challenge (Draft or Published)
* **[!UICONTROL Tasks]**: Number of tasks configured in the challenge
* **[!UICONTROL Journey]**: Link to the auto-generated journey associated with the challenge
* **[!UICONTROL Status]**: Current status of the auto-generated journey that delivers the challenge.
* **[!UICONTROL Start/End Date (UTC)]**: When the challenge becomes active and expires

From the Challenges tab, you can perform actions on challenges:

* **View challenge**: Select the challenge name to open its details page
* **Duplicate a challenge**: Select the ![](assets/do-not-localize/Smock_More_18_N.svg) icon and choose **[!UICONTROL Duplicate]**. A copy is created with all tasks, content, and messaging intact.
* **Delete a challenge**: Select the ![](assets/do-not-localize/Smock_More_18_N.svg) icon and choose **[!UICONTROL Delete]**.

  >[!IMPORTANT]
  >
  >You can delete a challenge even when it is published. Consider the impact before deleting.

* **Edit a challenge**: Select the challenge name to open its details page and make the desired changes.

  When you open a published challenge for editing, you first need to revert it to Draft state. Any customizations made directly to the auto-generated journey will be lost. After making your changes, save and publish the challenge again, then publish the associated journey. [Learn how to launch a challenge](create-challenges.md#launch)

  >[!IMPORTANT]
  >
  >Reverting a published challenge to draft cannot be undone. Consider the impact on your active journey before proceeding.

## Tasks inventory {#tasks-tab}

The **[!UICONTROL Tasks]** tab displays all reusable tasks that can be used across multiple challenges. Tasks created here become available for selection when creating or editing any challenge.

![](assets/tasks-inventory.png)

Key information displayed:

* **[!UICONTROL Description]**: Brief description of what the task requires
* **[!UICONTROL Task Activity]**: Type of activity (Purchase, Spend)
* **[!UICONTROL SKU]**: Eligible and/or excluded items
* **[!UICONTROL Used in challenges]**: Number of challenges currently using this task

From the Tasks tab, you can perform actions on tasks:

* **View/Edit a task**: Select the task name to view the full configuration and edit the task
* **Duplica attività**: seleziona l&#39;icona ![](assets/do-not-localize/Smock_More_18_N.svg) e scegli **[!UICONTROL Duplica]**
* **Elimina un&#39;attività**: seleziona l&#39;icona ![](assets/do-not-localize/Smock_More_18_N.svg) e scegli **[!UICONTROL Elimina]**.

  >[!IMPORTANT]
  >
  >È possibile eliminare un&#39;attività anche quando viene utilizzata in una o più sfide. Considera l’impatto sulle sfide che fanno riferimento all’attività prima di eliminarla.
