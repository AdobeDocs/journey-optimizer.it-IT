---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare le attività delle campagne orchestrate
description: Scopri come orchestrare le attività delle campagne
exl-id: 02f986b2-8200-4e0e-8918-44e528a6a3ec
version: Campaign Orchestration
TQID: https://experienceleague.adobe.com/OUKBJeSTaPJKav-NNCCxKZ8esY-62JkdRMmcwoJpZJ0
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: b423a773-0a58-4a77-b65d-3dd4ae6ef841
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
subfeature_v2:
  - id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 530
ht-degree: 56%

---

# Informazioni sulle attività di campagna orchestrate {#orchestrated-campaign-activities}

Le attività della campagna orchestrata sono raggruppate in tre categorie. A seconda del contesto, le attività disponibili possono variare.

Tutte le attività sono descritte nelle sezioni seguenti:

* [Attività di targeting](#targeting)
* [Attività di canale](#channel)
* [Attività di controllo del flusso](#flow-control)

![Elenco delle attività disponibili nell’area di lavoro](../assets/orchestrated-activities.png){width="80%" align="left"}

>[!NOTE]
>
>A seconda del modello di licenza, delle autorizzazioni e dell’implementazione, le attività disponibili possono variare.

## Guardrail e limitazioni {#activity-guardrails}

* **Limite attività canale** - Una campagna orchestrata supporta un massimo di 10 attività canale alla pubblicazione (e-mail, SMS, push o direct mail). Le attività di targeting e controllo del flusso non vengono conteggiate per questo limite.

* **Limite attività area di lavoro** - Il numero massimo di attività è 500. Per garantire prestazioni e manutenibilità, riduci in pratica i flussi di lavoro a 100 attività.

Vedi [Guardrail e limitazioni](../guardrails.md) per tutti i guardrail e le limitazioni della campagna orchestrata.

## Attività di targeting {#targeting}

Queste attività sono specifiche per il targeting. Consentono di creare uno o più target definendo un pubblico e suddividendo o combinando i tipi di pubblico mediante le operazioni di intersezione, unione o esclusione.

![Elenco delle attività di targeting](../assets/targeting-activities.png){width="40%" align="left"}

Le attività di targeting disponibili sono:

* [Crea pubblico](build-audience.md): definisci la popolazione target Puoi selezionare un pubblico esistente o utilizzare il generatore di regole per definire una query personalizzata.
* [Modifica dimensione](change-dimension.md): modifica la dimensione di targeting durante la creazione della campagna orchestrata.
* [Combina](combine.md): esegui la segmentazione della popolazione in entrata. Puoi utilizzare un’unione, un’intersezione o un’esclusione.
* [Deduplica](deduplication.md): elimina i duplicati nei risultati delle attività in entrata.
* [Arricchimento](enrichment.md): definisci i dati aggiuntivi da elaborare nella campagna orchestrata. Questa attività consente di sfruttare la transizione in entrata e può essere configurata in modo da completare la transizione in uscita con dati aggiuntivi.
* [Riconciliazione](reconciliation.md): definisci il collegamento tra i dati nei dati di Journey Optimizer e i dati in una tabella di lavoro, ad esempio i dati caricati da un file esterno.
* [Dividi](split.md): segmenta la popolazione in ingresso in diversi sottoinsiemi.

## Attività di canale {#channel}

Adobe Journey Optimizer consente di automatizzare ed eseguire campagne di marketing su più canali. Puoi combinare [attività canale](channels.md) nell&#39;area di lavoro per creare una campagna orchestrata cross-channel che può attivare azioni in base al comportamento del cliente.

Scopri come [creare un&#39;azione canale in una campagna orchestrata](channels.md).

## Attività di controllo del flusso {#flow-control}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_end"
>title="Attività Fine"
>abstract="L’attività **Fine** contrassegna la fine di un ramo nell’area di lavoro. Facoltativamente, puoi utilizzare **Segnale esterno** per avviare una campagna orchestrata a valle e trasmettere i parametri al completamento del ramo. [Ulteriori informazioni](../trigger-orchestrated-campaign.md#signal-end)"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_signal"
>title="Segnale esterno"
>abstract="Seleziona la campagna orchestrata a valle da avviare al termine di questo ramo e mappa i nomi e i valori dei parametri da inviare nel segnale. La campagna a valle deve essere impostata su **Attivata da un segnale** e pubblicata prima che questa campagna raggiunga l’attività Fine. [Ulteriori informazioni](../trigger-orchestrated-campaign.md#signal-end)"

Le seguenti attività sono specifiche per l’organizzazione e l’esecuzione di campagne orchestrate. Il loro compito principale è quello di coordinare le altre attività.

![Elenco delle attività di controllo del flusso](../assets/flow-control-activities.png){width="20%" align="left"}

Le attività di controllo del flusso disponibili sono:

* [And-join](and-join.md): sincronizza più rami di esecuzione di una campagna orchestrata.
* [Fork](fork.md): crea transizioni in uscita per avviare più attività contemporaneamente.
* [Attendi](wait.md): sospende temporaneamente l&#39;esecuzione di una parte di una campagna orchestrata.
  <!--* [Test](test.md): Enable transitions based on specified conditions.-->

* **[!UICONTROL Fine]**: contrassegna la fine di un ramo nell&#39;area di lavoro. Facoltativamente, puoi utilizzarlo per inviare un segnale a un’altra campagna orchestrata che inizia su un segnale. [Ulteriori informazioni](../trigger-orchestrated-campaign.md#signal-end)
