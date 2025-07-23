---
solution: Journey Optimizer
product: journey optimizer
title: Accesso e gestione delle campagne orchestrate
description: Scopri i principi chiave della creazione di campagne orchestrate con Adobe Journey Optimizer
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 7b42d317-cd01-4c6a-b61e-5b03e5a8ff3c
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 91%

---

# Accesso e gestione delle campagne orchestrate {#orchestrated-campaign-creation}

>[!CONTEXTUALHELP]
>id="ajo_targeting_workflow_list"
>title="Campagna orchestrata"
>abstract="In questa schermata, puoi accedere all’elenco completo delle campagne orchestrate, controllarne lo stato corrente, le date dell’ultima/successiva esecuzione e creare una nuova campagna orchestrata."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_campaign_action"
>title="Azione"
>abstract="In questa sezione sono elencate tutte le azioni utilizzate all’interno della campagna orchestrata."

+++ Sommario

| Ti diamo il benvenuto nelle campagne orchestrate | Avviare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](gs-orchestrated-campaigns.md)<br/><br/>Creazione e gestione di schemi e set di dati relazionali:</br> <ul><li>[Introduzione a schemi e set di dati](gs-schemas.md)</li><li>[Schema manuale](manual-schema.md)</li><li>[Schema di caricamento file](file-upload-schema.md)</li><li>[Acquisire dati](ingest-data.md)</li></ul><br/><br/><b>[Accedere e gestire campagne orchestrate](access-manage-orchestrated-campaigns.md)</b><br/><br/>[Passaggi chiave per creare una campagna orchestrata](gs-campaign-creation.md) | [Creare e pianificare la campagna](create-orchestrated-campaign.md)<br/><br/>[Orchestrare le attività](orchestrate-activities.md)<br/><br/>[Avviare e monitorare la campagna](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | [Utilizzare il generatore di regole](orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](build-query.md)<br/><br/>[Modificare le espressioni](edit-expressions.md)<br/><br/>[Retargeting](retarget.md) | [Introduzione alle attività](activities/about-activities.md)<br/><br/>Attività:<br/>[AND-join](activities/and-join.md) - [Crea pubblico](activities/build-audience.md) - [Modifica dimensione](activities/change-dimension.md) - [Attività canale](activities/channels.md) - [Combina](activities/combine.md) - [Deduplica](activities/deduplication.md) - [Arricchimento](activities/enrichment.md) - [Fork](activities/fork.md) - [Riconciliazione](activities/reconciliation.md) - [Salva pubblico](activities/save-audience.md) - [Dividi](activities/split.md) - [Attendi](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

Il contenuto di questa pagina non è definitivo e potrebbe essere soggetto a modifiche.

>[!ENDSHADEBOX]

## Accedere alle campagne orchestrate

Passa al menu **[!UICONTROL Campagne]** e seleziona la scheda **[!UICONTROL Orchestrazione]** per accedere all’elenco completo delle campagne orchestrate.

![immagine che mostra l’inventario delle campagne orchestrate](assets/inventory.png){zoomable="yes"}{zoomable="yes"}

Ogni campagna orchestrata nell’elenco visualizza informazioni quali lo [stato](#status) corrente della campagna, il canale e i tag associati o l’ultima modifica. È possibile personalizzare le colonne visualizzate facendo clic sul ![pulsante Configura layout](assets/do-not-localize/inventory-configure-layout.svg).

Inoltre, sono disponibili una barra di ricerca e dei filtri per facilitare la ricerca all’interno dell’elenco. Ad esempio, puoi filtrare le campagne orchestrate per visualizzare solo quelle appartenenti a un determinato canale o tag, o quelle elaborati durante un intervallo di date specifico.

Il pulsante ![immagine che mostra il pulsante Altre azioni](assets/do-not-localize/rule-builder-icon-more.svg) nell’inventario delle campagne ti consente di eseguire varie operazioni descritte di seguito.

![immagine dell’inventario delle campagne](assets/inventory-actions.png)

* **[!UICONTROL Visualizza rapporto tutte le ore]** / **[!UICONTROL Visualizza rapporto delle ultime 24 ore]**: accedi ai rapporti per misurare e visualizzare l’impatto e le prestazioni delle campagne orchestrate. [Ulteriori informazioni sul reporting delle campagne orchestrate](../orchestrated/reporting-campaigns.md)
* **[!UICONTROL Modifica tag]**: modifica i tag associati alla campagna.
* **[!UICONTROL Duplica]**: in alcuni casi, potrebbe essere necessario duplicare una campagna orchestrata, ad esempio per eseguire una campagna interrotta o per modificare la frequenza di esecuzione di una campagna pianificata.
* **[!UICONTROL Elimina]**: elimina la campagna. Questa azione è disponibile solo per le campagne nello stato di **[!UICONTROL Bozza]**.
* **[!UICONTROL Archivia]**: archivia la campagna. Tutte le campagne archiviate vengono eliminate con una nuova pianificazione continua 30 giorni dopo la data dell’ultima modifica. Questa azione è disponibile per tutte le campagne ad eccezione delle campagne nello stato **[!UICONTROL Bozza]**.

## Cosa c’è all’interno di una campagna orchestrata? {#gs-ms-campaign-inside}

L’area di lavoro della campagna orchestrata è una rappresentazione di ciò che dovrebbe accadere. Descrive le varie attività da eseguire e il modo in cui vengono collegate tra loro.

![immagine che mostra un’area di lavoro della campagna orchestrata](assets/canvas-example.png)

Ogni campagna orchestrata contiene:

* **Attività**: un’attività è un’attività da eseguire. Le varie attività disponibili sono rappresentate nel diagramma tramite icone. Ogni attività presenta proprietà specifiche e altre proprietà comuni a tutte le attività.

  In un diagramma della campagna orchestrata, una determinata attività può produrre più attività, in particolare in presenza di un ciclo o di azioni ricorrenti.

* **Transizioni**: le transizioni collegano un’attività di origine a un’attività di destinazione e ne definiscono la sequenza.

* **Tabelle di lavoro**: la tabella di lavoro contiene tutte le informazioni riportate dalla transizione. Ogni campagna orchestrata utilizza diverse tabelle di lavoro. I dati trasmessi in queste tabelle possono essere utilizzati in tutto il ciclo di vita della campagna orchestrata.

## Stati delle campagne {#status}

Le campagne orchestrate possono avere più stati:

* **[!UICONTROL Bozza]**: la campagna orchestrata è stata creata. Non è ancora stata pubblicata.
* **[!UICONTROL Pubblicazione]**: la campagna orchestrata è in fase di pubblicazione.
* **[!UICONTROL Live]**: la campagna orchestrata è stata pubblicata ed è in esecuzione.
* **[!UICONTROL Pianificata]**: l’esecuzione della campagna orchestrata è stata pianificata.
* **[!UICONTROL Completata]**: l’esecuzione della campagna orchestrata è stata completata. Lo stato Completata viene assegnato automaticamente fino a 3 giorni dopo il completamento di una campagna e l’invio dei messaggi senza errori.
* **[!UICONTROL Chiusa]**: questo stato viene visualizzato quando una campagna ricorrente è stata chiusa. La campagna continua l’esecuzione fino al completamento di tutte le attività, ma nessun altro profilo può entrare nella campagna.
* **[!UICONTROL Archiviata]**: la campagna orchestrata è stata archiviata. Tutte le campagne archiviate vengono eliminate con una nuova pianificazione continua 30 giorni dopo la data dell’ultima modifica. Se necessario, puoi duplicare una campagna archiviata per continuare a lavorarci.
* **[!UICONTROL Interrotta]**: l’esecuzione della campagna orchestrata è stata interrotta. Per riavviare la campagna, devi duplicarla.
