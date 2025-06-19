---
solution: Journey Optimizer
product: journey optimizer
title: Accesso e gestione di una campagna orchestrata
description: Scopri i principi chiave della creazione di campagne orchestrate con Adobe Journey Optimizer
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 7b42d317-cd01-4c6a-b61e-5b03e5a8ff3c
source-git-commit: 979b46eccf77db6e90cd47ceb7a40298bb481cc5
workflow-type: tm+mt
source-wordcount: '567'
ht-degree: 22%

---

# Accesso e gestione di una campagna orchestrata {#orchestrated-campaign-creation}

>[!CONTEXTUALHELP]
>id="ajo_targeting_workflow_list"
>title="Campagna orchestrata"
>abstract="In questa schermata, puoi accedere all’elenco completo delle campagne orchestrate, controllarne lo stato corrente, le date dell’ultima/successiva esecuzione e creare una nuova campagna orchestrata."

+++ Sommario

| Benvenuto in campagne orchestrate | Lanciare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](gs-orchestrated-campaigns.md)<br/><br/>[Passaggi di configurazione](configuration-steps.md)<br/><br/><b>[Accesso e gestione delle campagne orchestrate](access-manage-orchestrated-campaigns.md)</b> | [Passaggi chiave per la creazione di campagne orchestrate](gs-campaign-creation.md)<br/><br/>[Creare e pianificare la campagna](create-orchestrated-campaign.md)<br/><br/>[Orchestrare le attività](orchestrate-activities.md)<br/><br/>[Inviare messaggi con campagne orchestrate](send-messages.md)<br/><br/>[Avviare e monitorare la campagna](start-monitor-campaigns.md)<br/><br/>[Generazione rapporti](reporting-campaigns.md) | [Utilizzare il generatore di regole](orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](build-query.md)<br/><br/>[Modificare le espressioni](edit-expressions.md) | [Inizia a usare le attività](activities/about-activities.md)<br/><br/>Attività:<br/>[Partecipa/Partecipa](activities/and-join.md) - [Genera pubblico](activities/build-audience.md) - [Modifica dimensione](activities/change-dimension.md) - [Combina](activities/combine.md) - [Deduplicazione](activities/deduplication.md) - [Arricchimento](activities/enrichment.md) - [Fork](activities/fork.md) - [Riconciliazione](activities/reconciliation.md) - [Dividi](activities/split.md) - [Attendi](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

## Accedere alle campagne orchestrate

Passa al menu **[!UICONTROL Campagne]** e seleziona la scheda **[!UICONTROL Orchestrazione]** per accedere all&#39;elenco completo delle campagne orchestrate.

![immagine che mostra l&#39;inventario delle campagne orchestrate](assets/inventory.png){zoomable="yes"}{zoomable="yes"}

Ogni campagna orchestrata nell&#39;elenco visualizza informazioni quali il [stato](#status) corrente della campagna, il canale e i tag associati o l&#39;ultima modifica. È possibile personalizzare le colonne visualizzate facendo clic sul pulsante ![Configura layout](assets/do-not-localize/inventory-configure-layout.svg).

Inoltre, sono disponibili una barra di ricerca e dei filtri per facilitare la ricerca all’interno dell’elenco. Ad esempio, puoi filtrare le campagne orchestrate in modo da visualizzare solo quelle associate a un canale o a un tag specifico, o quelle create durante un intervallo di date specifico.

## Cosa c&#39;è all&#39;interno di una campagna orchestrata? {#gs-ms-campaign-inside}

L&#39;area di lavoro orchestrata per la campagna è una rappresentazione di ciò che dovrebbe accadere. Descrive le varie attività da eseguire e il modo in cui vengono collegate tra loro.

![immagine che mostra un&#39;area di lavoro della campagna orchestrata](assets/canvas-example.png){zoomable="yes"}{zoomable="yes"}

Ogni campagna orchestrata contiene:

* **Attività**: un’attività è un’attività da eseguire. Le varie attività disponibili sono rappresentate nel diagramma tramite icone. Ogni attività presenta proprietà specifiche e altre proprietà comuni a tutte le attività.

  In un diagramma di una campagna orchestrata, una determinata attività può produrre più attività, in particolare quando vi è un ciclo continuo o azioni ricorrenti.

* **Transizioni**: le transizioni collegano un’attività di origine a un’attività di destinazione e ne definiscono la sequenza.

* **Tabelle di lavoro**: la tabella di lavoro contiene tutte le informazioni riportate dalla transizione. Ogni campagna orchestrata utilizza diverse tabelle di lavoro. I dati trasmessi in queste tabelle possono essere utilizzati in tutto il ciclo di vita della campagna orchestrata.

## Stati delle campagne {#status}

Le campagne orchestrate possono avere più stati:

* **[!UICONTROL Bozza]**: campagna orchestrata creata. Non è ancora stato pubblicato.
* **[!UICONTROL Pubblicazione]**: è in corso la pubblicazione della campagna orchestrata.
* **[!UICONTROL Live]**: la campagna orchestrata è stata pubblicata ed è in esecuzione.
* **[!UICONTROL Pianificato]**: l&#39;esecuzione della campagna orchestrata è stata pianificata.
* **[!UICONTROL Completato]**: esecuzione della campagna orchestrata completata.
  <!--* **[!UICONTROL Closed]**: The orchestrated campaign xxxx-->
* **[!UICONTROL Archiviata]**: la campagna orchestrata è stata archiviata. Tutte le campagne archiviate vengono eliminate con una ripianificazione continua 30 giorni dopo la data dell’ultima modifica. Se necessario, puoi duplicare una campagna archiviata per continuare a lavorarci.
* **[!UICONTROL Arrestato]**: l&#39;esecuzione della campagna orchestrata è stata interrotta. Per avviare la campagna, devi duplicarla.

## Duplicare ed eliminare campagne orchestrate {#duplicate-delete}

In alcuni casi, potrebbe essere necessario duplicare una campagna orchestrata, ad esempio per eseguire una campagna interrotta o per modificare la frequenza di esecuzione di una campagna pianificata. Per farlo, fai clic sull&#39;immagine ![che mostra il pulsante Altre azioni](assets/do-not-localize/rule-builder-icon-more.svg) nell&#39;inventario delle campagne, quindi seleziona **[!UICONTROL Duplica]**

Per eliminare una campagna, fai clic sull&#39;immagine ![che mostra il pulsante Altre azioni](assets/do-not-localize/rule-builder-icon-more.svg), quindi seleziona **[!UICONTROL Elimina]**.

>[!NOTE]
>
>È possibile eliminare solo **[!UICONTROL campagne bozza]**.
