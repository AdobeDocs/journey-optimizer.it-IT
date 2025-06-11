---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare le attività delle campagne orchestrate
description: Scopri come orchestrare le attività della campagna
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 02f986b2-8200-4e0e-8918-44e528a6a3ec
source-git-commit: d59643f18a335fe1e094156a1cfee65b717b9fce
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 27%

---

# Informazioni sulle attività della campagna orchestrata {#orchestrated-campaign-activities}

+++ Sommario

| Benvenuto in campagne orchestrate | Avviare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](../gs-orchestrated-campaigns.md)<br/><br/>[Passaggi di configurazione](../configuration-steps.md)<br/><br/>[Passaggi chiave per la creazione di campagne orchestrate](../gs-campaign-creation.md) | [Creare una campagna orchestrata](../create-orchestrated-campaign.md)<br/><br/>[Orchestrare le attività](../orchestrate-activities.md)<br/><br/>[Inviare messaggi con le campagne orchestrate](../send-messages.md)<br/><br/>[Avviare e monitorare la campagna](../start-monitor-campaigns.md)<br/><br/>[Generazione rapporti](../reporting-campaigns.md) | [Utilizzare Query Modeler](../orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](../build-query.md)<br/><br/>[Modificare le espressioni](../edit-expressions.md) | [Inizia a usare le attività](about-activities.md)<br/><br/>Attività:<br/>[Partecipa/Partecipa](and-join.md) - [Genera pubblico](build-audience.md) - [Modifica dimensione](change-dimension.md) - [Combina](combine.md) - [Deduplicazione](deduplication.md) - [Arricchimento](enrichment.md) - [Fork](fork.md) - [Riconciliazione](reconciliation.md) - [Dividi](split.md) - [Attendi](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

Le attività delle campagne orchestrate sono raggruppate in tre categorie. A seconda del contesto, le attività disponibili possono variare.

Tutte le attività sono descritte nelle sezioni seguenti:

* [Attività di targeting](#targeting)
* [Attività di canale](#channel)
* [Attività di controllo del flusso](#flow-control)

![Elenco delle attività disponibili nell&#39;area di lavoro](../assets/orchestrated-activities.png){width="80%" align="left"}

## Attività di targeting {#targeting}

Queste attività sono specifiche per il targeting. Consentono di creare uno o più target definendo un pubblico e suddividendo o combinando i tipi di pubblico mediante le operazioni di intersezione, unione o esclusione.

![Elenco delle attività di targeting](../assets/targeting-activities.png){width="40%" align="left"}

* [Genera pubblico](build-audience.md): definisci la popolazione target. Puoi selezionare un pubblico esistente o utilizzare il modellatore di query per definire una query personalizzata.
* [Modifica dimensione](change-dimension.md): modifica la dimensione di targeting durante la creazione della campagna orchestrata.
* [Combina](combine.md): esegui la segmentazione del gruppo in entrata. Puoi utilizzare un’unione, un’intersezione o un’esclusione.
* [Deduplicazione](deduplication.md): elimina i duplicati nei risultati delle attività in entrata.
* [Arricchimento](enrichment.md): definisci i dati aggiuntivi da elaborare nella campagna orchestrata. Questa attività consente di sfruttare la transizione in entrata e può essere configurata in modo da completare la transizione in uscita con dati aggiuntivi.
* [Riconciliazione](reconciliation.md): definire il collegamento tra i dati nei dati di Journey Optimizer e i dati in una tabella di lavoro, ad esempio i dati caricati da un file esterno.
* [Dividi](split.md): segmenta la popolazione in ingresso in diversi sottoinsiemi.

## Attività di canale {#channel}

Adobe Journey Optimizer consente di automatizzare ed eseguire campagne di marketing su più canali. Puoi combinare le attività dei canali nell’area di lavoro per creare una campagna orchestrata cross-channel che può attivare azioni in base al comportamento del cliente. Sono disponibili le seguenti attività di **Canale**: e-mail e SMS. [Scopri come creare un&#39;azione del canale nel contesto di una campagna orchestrata](channels.md).

## Attività di controllo del flusso {#flow-control}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_end"
>title="Attività Fine"
>abstract="L’attività **Fine** consente di contrassegnare graficamente la fine di una campagna orchestrata. Questa attività non ha alcun impatto funzionale ed è pertanto facoltativa."

![Elenco delle attività di controllo del flusso](../assets/flow-control-activities.png){width="30%" align="left"}

Le seguenti attività sono specifiche per l’organizzazione e l’esecuzione di campagne orchestrate. Il loro compito principale è quello di coordinare le altre attività:

* [And-join](and-join.md): sincronizza più rami di esecuzione di una campagna orchestrata.
* [Fork](fork.md): crea transizioni in uscita per avviare più attività contemporaneamente.
* [Attendi](wait.md): sospende temporaneamente l&#39;esecuzione di una parte di una campagna orchestrata.
  <!--* [Test](test.md): Enable transitions based on specified conditions.-->

>[!NOTE]
>L&#39;attività **End** contrassegna graficamente la fine di una campagna orchestrata. Questa attività non ha alcun impatto funzionale ed è pertanto facoltativa
