---
solution: Journey Optimizer
product: journey optimizer
title: Creare campagne con più passaggi con Journey Optimizer
description: Scopri come creare una campagna in più passaggi con Adobe Journey Optimizer
hide: true
hidefromtoc: true
exl-id: 13da680d-fef8-4749-9190-8ca3d77b060a
source-git-commit: 271c4739a5537a99da981913606bc9eb099b5139
workflow-type: tm+mt
source-wordcount: '706'
ht-degree: 13%

---

# Creare una campagna orchestrata {#create-first-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_creation_workflow"
>title="Elenco delle campagne con più passaggi"
>abstract="La scheda **passaggi multipli** elenca tutte le campagne con più passaggi. Fai clic sul nome di una campagna con più passaggi per modificarla. Utilizza il pulsante **Crea campagna con più passaggi** per aggiungere una nuova campagna con più passaggi."

## Prerequisiti

### Autorizzazioni

### Impostazioni

Panoramica dei nuovi schemi, campi di esecuzione e criteri di unione per amministratori. [Ulteriori informazioni](ms-schemas.md)


## Passaggi di creazione

Per creare una campagna in più passaggi, effettua le seguenti operazioni:

1. Per creare una **campagna con più passaggi**, passa al menu **Campagne**.

1. Fai clic sul pulsante **[!UICONTROL Crea campagna con più passaggi]** nell&#39;angolo superiore destro della schermata.

1. Nella finestra di dialogo **Proprietà** per la campagna in più passaggi, seleziona il modello da utilizzare per creare la campagna in più passaggi (puoi anche utilizzare il modello predefinito). [Ulteriori informazioni sui modelli di campagna con più passaggi](#campaign-templates).

1. Immetti un’etichetta per la campagna in più passaggi. Inoltre, ti consigliamo vivamente di aggiungere una descrizione alla campagna in più passaggi, nel campo dedicato della sezione **[!UICONTROL Opzioni aggiuntive]** della schermata.

1. Espandi la sezione **[!UICONTROL Opzioni aggiuntive]** per configurare altre impostazioni per la campagna in più passaggi.

1. Fai clic sul pulsante **[!UICONTROL Crea campagna con più passaggi]** per confermare la creazione della campagna con più passaggi.

La campagna in più passaggi è ora creata e disponibile nell’elenco dei flussi di lavoro. Ora puoi accedere alla relativa area di lavoro visiva e iniziare ad aggiungere, configurare e orchestrare le attività che eseguirà. [Scopri come orchestrare le attività delle campagne in più passaggi](orchestrate-activities.md).

## Utilizzare i modelli di campagna in più passaggi {#campaign-templates}

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_for_campaign"
>title="Modelli di campagna in più passaggi"
>abstract="I modelli di campagna con più passaggi contengono impostazioni e attività preconfigurate che possono essere riutilizzate per creare una nuova campagna con più passaggi."

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_creation_properties"
>title="Proprietà di una campagna in più passaggi"
>abstract="I modelli di campagna con più passaggi contengono impostazioni e attività preconfigurate che possono essere riutilizzate per creare nuove campagne con più passaggi. In questa schermata, immetti l’etichetta del modello di campagna in più passaggi e configurane le impostazioni, ad esempio il nome interno, la cartella e le cartelle di esecuzione, il fuso orario e il gruppo di supervisori."

I modelli di campagna con più passaggi contengono impostazioni e attività preconfigurate che possono essere riutilizzate per creare nuove campagne con più passaggi. Durante la creazione di una campagna in più passaggi, puoi selezionare il modello della campagna in più passaggi dalle proprietà della campagna in più passaggi. Per impostazione predefinita, viene fornito un modello vuoto.

Puoi creare un modello da una campagna con più passaggi esistente o crearne uno nuovo da zero. Entrambi i metodi sono descritti di seguito.

>[!BEGINTABS]

>[!TAB Crea un modello da una campagna con più passaggi esistente]

Per creare un modello di campagna con più passaggi da una campagna con più passaggi esistente, effettua le seguenti operazioni:

1. Apri il menu **Campaign** e passa alla campagna con più passaggi da salvare come modello.
1. Fare clic sui tre punti a destra del nome della campagna con più passaggi e scegliere **Copia come modello**.
1. Conferma la creazione del modello nella finestra a comparsa.
1. Nell’area di lavoro del modello della campagna in più passaggi, seleziona, aggiungi e configura le attività in base alle esigenze.
1. Dal pulsante **Impostazioni**, accedi alle impostazioni per modificare il nome del modello di campagna in più passaggi e immetti una descrizione.
1. Seleziona la **cartella** e la **cartella di esecuzione** del modello. La cartella è il percorso in cui viene salvato il modello di campagna in più passaggi. La cartella di esecuzione è la cartella in cui vengono salvate le campagne con più passaggi create in base a questo modello.
1. Salva le modifiche.

Il modello di campagna in più passaggi è ora disponibile nell’elenco dei modelli. Puoi creare una campagna con più passaggi basata su questo modello. Questa campagna in più passaggi sarà preconfigurata con le impostazioni e le attività definite nel modello.


>[!TAB Creare un modello da zero]


Per creare un modello di campagna con più passaggi da zero, effettua le seguenti operazioni:

1. Apri il menu **Campaign** e passa alla scheda **Modelli**. Puoi visualizzare l’elenco dei modelli di campagna in più passaggi disponibili.
1. Fai clic sul pulsante **[!UICONTROL Crea modello]** nell’angolo in altro a destra della schermata.
1. Inserisci l’etichetta e apri le opzioni aggiuntive per inserire una descrizione del modello di campagna in più passaggi.
1. Seleziona la cartella e la cartella di esecuzione del modello. La cartella è il percorso in cui viene salvato il modello di campagna in più passaggi. La cartella di esecuzione è la cartella in cui vengono salvate le campagne con più passaggi create in base a questo modello.
1. Fai clic sul pulsante **Crea** per confermare le impostazioni.
1. Nell’area di lavoro del modello della campagna in più passaggi, aggiungi e configura le attività in base alle esigenze.

   ![](assets/wf-template-activities.png){zoomable="yes"}

1. Salva le modifiche.

Il modello di campagna in più passaggi è ora disponibile nell’elenco dei modelli. Puoi creare una campagna con più passaggi basata su questo modello. Questa campagna in più passaggi sarà preconfigurata con le impostazioni e le attività definite nel modello.

>[!ENDTABS]
