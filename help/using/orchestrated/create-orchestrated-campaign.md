---
solution: Journey Optimizer
product: journey optimizer
title: Creare campagne orchestrate con Journey Optimizer
description: Scopri come creare una campagna orchestrata con Adobe Journey Optimizer
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 13da680d-fef8-4749-9190-8ca3d77b060a
source-git-commit: 2935e611bb9682256a324485b28e7dd2552e1dd2
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 28%

---


# Creare una campagna orchestrata {#create-first-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_creation_workflow"
>title="Elenco delle campagne orchestrate"
>abstract="Nella scheda **multifase** sono elencate tutte le campagne orchestrate. Fai clic sul nome di una campagna orchestrata per modificarla. Fai clic sul pulsante **Crea campagna orchestrata** per aggiungerne una nuova."

+++ Sommario

| Benvenuto in campagne orchestrate | Avviare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](gs-orchestrated-campaigns.md)<br/><br/>[Passaggi di configurazione](configuration-steps.md)<br/><br/>[Passaggi chiave per la creazione di campagne orchestrate](gs-campaign-creation.md) | [Creare una campagna orchestrata](create-orchestrated-campaign.md)<br/><br/>[Orchestrare le attività](orchestrate-activities.md)<br/><br/>[Inviare messaggi con le campagne orchestrate](send-messages.md)<br/><br/>[Avviare e monitorare la campagna](start-monitor-campaigns.md)<br/><br/>[Generazione rapporti](reporting-campaigns.md) | [Utilizzare Query Modeler](orchestrated-query-modeler.md)<br/><br/>[Creare la prima query](build-query.md)<br/><br/>[Modificare le espressioni](edit-expressions.md) | [Inizia a usare le attività](activities/about-activities.md)<br/><br/>Attività:<br/>[Partecipa/Partecipa](activities/and-join.md) - [Genera pubblico](activities/build-audience.md) - [Modifica dimensione](activities/change-dimension.md) - [Combina](activities/combine.md) - [Deduplicazione](activities/deduplication.md) - [Arricchimento](activities/enrichment.md) - [Fork](activities/fork.md) - [Riconciliazione](activities/reconciliation.md) - [Dividi](activities/split.md) - [Attendi](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/><br/>

## Crea la campagna

Per creare una campagna orchestrata, effettua le seguenti operazioni:

1. Per creare una **campagna orchestrata**, passa al menu **Campagne**.

1. Fai clic sul pulsante **[!UICONTROL Crea campagna orchestrata]** nell&#39;angolo superiore destro della schermata.

1. Nella finestra di dialogo **Proprietà** della campagna orchestrata, seleziona il modello da utilizzare per creare la campagna orchestrata (puoi anche utilizzare il modello predefinito). [Ulteriori informazioni sui modelli di campagna orchestrati](#campaign-templates).

1. Immetti un’etichetta per la campagna orchestrata. Inoltre, ti consigliamo vivamente di aggiungere una descrizione alla campagna orchestrata, nel campo dedicato della sezione **[!UICONTROL Opzioni aggiuntive]** della schermata.

1. Espandi la sezione **[!UICONTROL Opzioni aggiuntive]** per configurare altre impostazioni per la campagna orchestrata.

1. Fai clic sul pulsante **[!UICONTROL Crea campagna orchestrata]** per confermare la creazione della campagna orchestrata.

La campagna orchestrata è ora creata ed è disponibile nell’elenco dei flussi di lavoro. Ora puoi accedere alla relativa area di lavoro visiva e iniziare ad aggiungere, configurare e orchestrare le attività che eseguirà. [Scopri come orchestrare le attività delle campagne orchestrate](orchestrate-activities.md).

## Configurare le impostazioni della campagna

Panoramica dei nuovi schemi, campi di esecuzione e criteri di unione per amministratori. [Ulteriori informazioni](configuration-steps.md)

## Utilizzare i modelli per campagna orchestrata {#campaign-templates}

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_for_campaign"
>title="Modelli per campagna orchestrata"
>abstract="I modelli per campagna orchestrata contengono impostazioni e attività preconfigurate che possono essere riutilizzate per creare nuove campagne orchestrate."

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_creation_properties"
>title="Proprietà della campagna orchestrata"
>abstract="I modelli per campagna orchestrata contengono impostazioni e attività preconfigurate che possono essere riutilizzate per creare nuove campagne orchestrate. In questa schermata, immetti l’etichetta del modello per campagna orchestrata e configurane le impostazioni, ad esempio il nome interno, la cartella e le cartelle di esecuzione, il fuso orario e il gruppo di supervisori."

I modelli per campagna orchestrata contengono impostazioni e attività preconfigurate che possono essere riutilizzate per creare nuove campagne orchestrate. Durante la creazione di una campagna orchestrata, puoi selezionare il modello della campagna orchestrata dalle relative proprietà. Per impostazione predefinita, viene fornito un modello vuoto.

Puoi creare un modello da una campagna orchestrata esistente o crearne uno nuovo da zero. Entrambi i metodi sono descritti di seguito.

>[!BEGINTABS]

>[!TAB Crea un modello da una campagna orchestrata esistente]

Per creare un modello di campagna orchestrata da una campagna orchestrata esistente, effettua le seguenti operazioni:

1. Apri il menu **Campaign** e passa alla campagna orchestrata da salvare come modello.
1. Fare clic sui tre punti a destra del nome della campagna orchestrata e scegliere **Copia come modello**.
1. Conferma la creazione del modello nella finestra a comparsa.
1. Nell’area di lavoro del modello della campagna orchestrata, seleziona, aggiungi e configura le attività in base alle esigenze.
1. Dal pulsante **Impostazioni**, individua le impostazioni per modificare il nome del modello della campagna orchestrata e immetti una descrizione.
1. Seleziona la **cartella** e la **cartella di esecuzione** del modello. La cartella è il percorso in cui viene salvato il modello di campagna orchestrato. La cartella di esecuzione è la cartella in cui vengono salvate le campagne orchestrate create in base a questo modello.
1. Salva le modifiche.

Il modello di campagna orchestrato è ora disponibile nell’elenco dei modelli. Puoi creare una campagna orchestrata basata su questo modello. Questa campagna orchestrata verrà preconfigurata con le impostazioni e le attività definite nel modello.


>[!TAB Creare un modello da zero]


Per creare un modello di campagna orchestrato da zero, effettua le seguenti operazioni:

1. Apri il menu **Campaign** e passa alla scheda **Modelli**. Puoi visualizzare l’elenco dei modelli di campagna orchestrati disponibili.
1. Fai clic sul pulsante **[!UICONTROL Crea modello]** nell’angolo in altro a destra della schermata.
1. Inserisci l’etichetta e apri le opzioni aggiuntive per immettere una descrizione del modello di campagna orchestrato.
1. Seleziona la cartella e la cartella di esecuzione del modello. La cartella è il percorso in cui viene salvato il modello di campagna orchestrato. La cartella di esecuzione è la cartella in cui vengono salvate le campagne orchestrate create in base a questo modello.
1. Fai clic sul pulsante **Crea** per confermare le impostazioni.
1. Nell’area di lavoro del modello della campagna orchestrata, aggiungi e configura le attività in base alle esigenze.

   ![](assets/wf-template-activities.png){zoomable="yes"}

1. Salva le modifiche.

Il modello di campagna orchestrato è ora disponibile nell’elenco dei modelli. Puoi creare una campagna orchestrata basata su questo modello. Questa campagna orchestrata verrà preconfigurata con le impostazioni e le attività definite nel modello.

>[!ENDTABS]
