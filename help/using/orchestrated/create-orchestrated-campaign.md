---
solution: Journey Optimizer
product: journey optimizer
title: Creare e pianificare campagne orchestrate con Journey Optimizer
description: Scopri come creare una campagna orchestrata con Adobe Journey Optimizer
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 13da680d-fef8-4749-9190-8ca3d77b060a
source-git-commit: 435b4a7eee9428c7f0efeb62c72b39c0e2aaabba
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 14%

---


# Creare e pianificare una campagna orchestrata {#create-first-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_creation_workflow"
>title="Elenco delle campagne orchestrate"
>abstract="Nella scheda **Orchestrazione** sono elencate tutte le campagne orchestrate. Fai clic sul nome di una campagna orchestrata per modificarla. Fai clic sul pulsante **Crea campagna orchestrata** per aggiungerne una nuova."

+++ Sommario

| Benvenuto in campagne orchestrate | Avviare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](gs-orchestrated-campaigns.md)<br/><br/>[Passaggi di configurazione](configuration-steps.md)<br/><br/>[Accesso e gestione delle campagne orchestrate](access-manage-orchestrated-campaigns.md) | [Passaggi chiave per la creazione di campagne orchestrate](gs-campaign-creation.md)<br/><br/><b>[Creare e pianificare la campagna](create-orchestrated-campaign.md)</b><br/><br/>[Orchestrare le attività](orchestrate-activities.md)<br/><br/>[Inviare messaggi con campagne orchestrate](send-messages.md)<br/><br/>[Avviare e monitorare la campagna](start-monitor-campaigns.md)<br/><br/>[Generazione rapporti](reporting-campaigns.md) | [Utilizzare il generatore di regole](orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](build-query.md)<br/><br/>[Modificare le espressioni](edit-expressions.md) | [Inizia a usare le attività](activities/about-activities.md)<br/><br/>Attività:<br/>[Partecipa/Partecipa](activities/and-join.md) - [Genera pubblico](activities/build-audience.md) - [Modifica dimensione](activities/change-dimension.md) - [Combina](activities/combine.md) - [Deduplicazione](activities/deduplication.md) - [Arricchimento](activities/enrichment.md) - [Fork](activities/fork.md) - [Riconciliazione](activities/reconciliation.md) - [Dividi](activities/split.md) - [Attendi](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

Documentazione in corso

>[!ENDSHADEBOX]

## Crea la campagna {#create}

Per creare una campagna orchestrata, effettua le seguenti operazioni:

1. Passa al menu **[!UICONTROL Campagne]**, seleziona la scheda **[!UICONTROL Orchestrazione]** e seleziona **[!UICONTROL Crea campagna]**.

   ![](assets/inventory-create.png)

1. Immetti un nome per la campagna orchestrata. Inoltre, ti consigliamo vivamente di aggiungere una descrizione nel campo dedicato.

1. (facoltativo) Utilizza il campo **Tag** per assegnare tag unificati Adobe Experience Platform alla tua campagna orchestrata. Questo consente di classificarle facilmente e migliorare la ricerca dall’elenco delle campagne. [Scopri come utilizzare i tag](../start/search-filter-categorize.md#tags).

1. Fai clic sul pulsante **[!UICONTROL Crea]** per confermare.


La campagna orchestrata è ora creata e disponibile nell’elenco delle campagne. Puoi modificare queste proprietà in qualsiasi momento facendo clic sull&#39;icona ![Impostazioni campagna](assets/do-not-localize/campaign-settings.svg) nell&#39;area di lavoro della campagna.


## Pianificare la campagna {#schedule}

Per impostazione predefinita, le campagne orchestrate iniziano una volta attivate manualmente e terminano non appena le loro attività sono state eseguite.

Se non desideri eseguire una campagna orchestrata subito dopo la sua attivazione, puoi specificare la data e l’ora in cui deve essere eseguita. Puoi anche eseguire la campagna a frequenze regolari in base a vari criteri.

Per configurare la pianificazione della campagna, apri la campagna orchestrata e fai clic sul pulsante **[!UICONTROL Appena possibile]**.

![](assets/create-schedule.png)

<!--In the Execution frequency field, select 

time zone

daily, weekly, monthly
several times a day based on specific hours or periodically

recurring frequencies (all except as soon and once)
preview launch times
validity period

>[!NOTE]
>
>When scheduling campaigns in [!DNL Adobe Journey Optimizer], ensure your start date/time aligns with the desired first delivery. For recurring campaigns, if the initial scheduled time has already passed, the campaigns will roll over to the next available time slot according to their recurrence rules.

## Work with orchestrated campaign templates {#campaign-templates}

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_for_campaign"
>title="Orchestrated campaign templates"
>abstract="Orchestrated campaign templates contain pre-configured settings and activities which can be reused for creating new orchestrated campaign."

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_creation_properties"
>title="Orchestrated campaign properties"
>abstract="Orchestrated campaign templates contain pre-configured settings and activities which can be reused for creating new orchestrated campaigns. In this screen, enter the label of the orchestrated campaign template and configure its settings such as its internal name, folder and execution folders, timezone, and supervisor group."

Orchestrated campaign templates contain pre-configured settings and activities which can be reused for creating new orchestrated campaigns. You can select the template of your orchestrated campaign from the orchestrated campaign properties, when creating an orchestrated campaign. An empty template is provided by default.

You can create a template from an existing orchestrated campaign, or create a new template from scratch. Both methods are detailed below.

>[!BEGINTABS]

>[!TAB Create a template from an existing orchestrated campaign]

To create an orchestrated campaign template from an existing orchestrated campaign, follow these steps:

1. Open to the **Campaign** menu and browse to the orchestrated campaign to save as a template.
1. Click the three dots on the right of the name of the orchestrated campaign, and choose **Copy as template**.
1. In the popup window, confirm the template creation.
1. In the orchestrated campaign template canvas, check, add, and configure the activities as needed.
1. Browse to the settings, from the **Settings** button, to change the name of the orchestrated campaign template, and enter a description.
1. Select the **folder** and **execution folder** of the template. The folder is the location where the orchestrated campaign template is saved. The execution folder is the folder where orchestrated campaigns created based on this template are saved.
1. Save your changes. 

The orchestrated campaign template is now available in the template list. You can create an orchestrated campaign based on this template. This orchestrated campaign will be pre-configured with the settings and activities defined in the template.


>[!TAB Create a template from scratch]


To create an orchestrated campaign template from scratch, follow these steps:

1. Open to the **Campaign** menu and browse to the **Templates** tab. You can see the list of available orchestrated campaign templates.
1. Click the **[!UICONTROL Create template]** button in the upper-right corner of the screen.
1. Enter the label and open the additional options to enter a description of your orchestrated campaign template.
1. Select the folder and execution folder of the template. The folder is the location where the orchestrated campaign template is saved. The execution folder is the folder where orchestrated campaigns created based on this template are saved.
1. Click the **Create** button to confirm your settings.
1. In the orchestrated campaign template canvas, add and configure the activities as needed.

     ![](assets/wf-template-activities.png){zoomable="yes"}

1. Save your changes. 

The orchestrated campaign template is now available in the template list. You can create an orchestrated campaign based on this template. This orchestrated campaign will be pre-configured with the settings and activities defined in the template.

>[!ENDTABS]






## Next steps {#next}

Once your campaign configuration and content are ready, you can review and activate it. [Learn more](review-activate-campaign.md)

-->