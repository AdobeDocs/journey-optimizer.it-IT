---
solution: Journey Optimizer
product: journey optimizer
title: Passaggi chiave per la creazione di campagne orchestrate
description: Scopri i principi chiave della creazione di campagne orchestrate con Adobe Journey Optimizer
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: b04aa15a-71bf-4683-bcbf-f611c189ffe1
source-git-commit: 5872e192c849b7a7909f0b50caa1331b15490d79
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 27%

---


# Passaggi chiave per la creazione di campagne orchestrate {#orchestrated-campaign-creation}

>[!CONTEXTUALHELP]
>id="ajo_targeting_workflow_list"
>title="Campagna orchestrata"
>abstract="In questa schermata, puoi accedere all’elenco completo delle campagne orchestrate, controllarne lo stato corrente, le date dell’ultima/successiva esecuzione e creare una nuova campagna orchestrata."

+++ Sommario

| Benvenuto in campagne orchestrate | Avviare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](gs-orchestrated-campaigns.md)<br/><br/>[Passaggi di configurazione](configuration-steps.md)<br/><br/>[Passaggi chiave per la creazione di campagne orchestrate](gs-campaign-creation.md) | [Creare una campagna orchestrata](create-orchestrated-campaign.md)<br/><br/>[Orchestrare le attività](orchestrate-activities.md)<br/><br/>[Inviare messaggi con le campagne orchestrate](send-messages.md)<br/><br/>[Avviare e monitorare la campagna](start-monitor-campaigns.md)<br/><br/>[Generazione rapporti](reporting-campaigns.md) | [Utilizzare il generatore di regole](orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](build-query.md)<br/><br/>[Modificare le espressioni](edit-expressions.md) | [Inizia a usare le attività](activities/about-activities.md)<br/><br/>Attività:<br/>[Partecipa/Partecipa](activities/and-join.md) - [Genera pubblico](activities/build-audience.md) - [Modifica dimensione](activities/change-dimension.md) - [Combina](activities/combine.md) - [Deduplicazione](activities/deduplication.md) - [Arricchimento](activities/enrichment.md) - [Fork](activities/fork.md) - [Riconciliazione](activities/reconciliation.md) - [Dividi](activities/split.md) - [Attendi](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

Puoi creare campagne orchestrate in un’area di lavoro visiva per progettare processi cross-channel come segmentazione, esecuzione di campagne, elaborazione di file.

## Accedere alle campagne orchestrate

Nel menu **[!UICONTROL Campagne]**, passa alla scheda Passaggi multipli per accedere all&#39;elenco completo delle campagne orchestrate.

Ogni campagna orchestrata nell&#39;elenco visualizza informazioni sul suo [stato](#status) corrente, sull&#39;ultima volta che è stata eseguita o modificata e sulla data e ora di esecuzione pianificate successive.

Puoi personalizzare le colonne visualizzate facendo clic sull’icona **[!UICONTROL Configura le colonne per un layout personalizzato]**, nell’angolo superiore a destra dell’elenco. Ciò ti consente di aggiungere ulteriori informazioni all’elenco, ad esempio l’ultima attività che ha generato un errore per ogni campagna orchestrata o la dimensione di targeting applicata.

Inoltre, sono disponibili una barra di ricerca e dei filtri per facilitare la ricerca all’interno dell’elenco. Ad esempio, puoi filtrare le campagne orchestrate in modo da visualizzare solo quelle appartenenti a una campagna o quelle elaborate durante un intervallo di date specifico.

Per duplicare o eliminare una campagna orchestrata, fai clic sul pulsante con i puntini di sospensione, quindi seleziona **[!UICONTROL Duplica]** o **[!UICONTROL Elimina]**.

>[!NOTE]
>
>Quando è in corso una campagna orchestrata, puoi duplicarla, ma non eliminarla.

## Cosa c&#39;è all&#39;interno di una campagna orchestrata? {#gs-ms-campaign-inside}

L&#39;area di lavoro orchestrata per la campagna è una rappresentazione di ciò che dovrebbe accadere. Descrive le varie attività da eseguire e il modo in cui vengono collegate tra loro.

![](assets/workflow-example.png){zoomable="yes"} {zoomable="yes"}

Ogni campagna orchestrata contiene:

* **Attività**: un’attività è un’attività da eseguire. Le varie attività disponibili sono rappresentate nel diagramma tramite icone. Ogni attività presenta proprietà specifiche e altre proprietà comuni a tutte le attività.

  In un diagramma di una campagna orchestrata, una determinata attività può produrre più attività, in particolare quando vi è un ciclo continuo o azioni ricorrenti.

* **Transizioni**: le transizioni collegano un’attività di origine a un’attività di destinazione e ne definiscono la sequenza.

* **Tabelle di lavoro**: la tabella di lavoro contiene tutte le informazioni riportate dalla transizione. Ogni campagna orchestrata utilizza diverse tabelle di lavoro. I dati trasmessi in queste tabelle possono essere utilizzati in tutto il ciclo di vita della campagna orchestrata.

## Stati e ciclo di vita {#status}

Le campagne possono avere più stati:

* **[!UICONTROL Bozza]**: la campagna orchestrata è stata creata e salvata.
* **[!UICONTROL In corso]**: la campagna orchestrata è attualmente in esecuzione.
* **[!UICONTROL Completata]**: esecuzione della campagna orchestrata completata.
* **[!UICONTROL Sospeso]**: la campagna orchestrata è stata sospesa.
* **[!UICONTROL Errore]**: la campagna orchestrata ha rilevato un errore. Apri la campagna orchestrata e accedi ai registri e alle attività per identificare l’errore e risolverlo.
