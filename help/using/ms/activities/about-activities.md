---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare le attività delle campagne in più passaggi
description: Scopri come eseguire attività di campagna in più passaggi
hide: true
hidefromtoc: true
source-git-commit: 658d82820d3f307481c44a142c38727f777fd879
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 23%

---


# Informazioni sulle attività di campagna in più passaggi {#ms-campaign-activities}

Le attività delle campagne in più passaggi sono raggruppate in tre categorie. A seconda del contesto, le attività disponibili possono variare.

Tutte le attività sono descritte nelle sezioni seguenti:

* [Attività di targeting e gestione dei dati](#targeting)
* [Attività di canale](#channel)
* [Attività di controllo del flusso](#flow-control)

![](../assets/workflow-activities.png)

## Attività di targeting {#targeting}

Queste attività sono specifiche per il targeting. Consentono di creare uno o più target definendo un pubblico e suddividendo o combinando i tipi di pubblico mediante le operazioni di intersezione, unione o esclusione.

* [Genera pubblico](build-audience.md): definisci la popolazione target. Puoi selezionare un pubblico esistente o utilizzare il modellatore di query per definire una query personalizzata.
* [Modifica dimensione](change-dimension.md): modifica la dimensione di targeting durante la creazione della campagna in più passaggi.
* [Combina](combine.md): esegui la segmentazione del gruppo in entrata. Puoi utilizzare un’unione, un’intersezione o un’esclusione.
* [Deduplicazione](deduplication.md): elimina i duplicati nei risultati delle attività in entrata.
* [Arricchimento](enrichment.md): definisci i dati aggiuntivi da elaborare nella campagna in più passaggi. Questa attività consente di sfruttare la transizione in entrata e può essere configurata in modo da completare la transizione in uscita con dati aggiuntivi.
* [Riconciliazione](reconciliation.md): definire il collegamento tra i dati nei dati di Journey Optimizer e i dati in una tabella di lavoro, ad esempio i dati caricati da un file esterno.
* [Salva pubblico](save-audience.md): aggiorna un pubblico esistente o creane uno nuovo dalla popolazione calcolata a monte in una campagna in più passaggi.
* [Dividi](split.md): segmenta la popolazione in ingresso in diversi sottoinsiemi.

## Attività di gestione dati {#data}

Queste attività sono specifiche per la manipolazione e l’arricchimento dei dati sulla popolazione.

* [Carica file](load-file.md): utilizzare profili e dati archiviati in un file esterno.
* [Aggiorna dati](update-data.md): esegui aggiornamenti di massa sui campi del database. Diverse opzioni consentono di personalizzare l’aggiornamento dei dati.

## Attività di canale {#channel}

Adobe Journey Optimizer consente di automatizzare ed eseguire campagne di marketing su più canali. Puoi combinare le attività del canale nell’area di lavoro per creare campagne multicanale in più passaggi che possono attivare azioni in base al comportamento del cliente. Sono disponibili le seguenti attività di **Canale**: e-mail, SMS, Android e notifiche push di iOS. [Scopri come impostare una consegna nel contesto di una campagna in più passaggi](channels.md).

## Attività di controllo del flusso {#flow-control}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_end"
>title="Attività Fine"
>abstract="L&#39;attività **End** consente di contrassegnare graficamente la fine di una campagna in più passaggi. Questa attività non ha alcun impatto funzionale ed è pertanto facoltativa."

Le seguenti attività sono specifiche per l’organizzazione e l’esecuzione di campagne in più passaggi. Il loro compito principale è quello di coordinare le altre attività:

* [And-join](and-join.md): sincronizza più rami di esecuzione di una campagna con più passaggi.
* **Fine**: contrassegna graficamente la fine di una campagna con più passaggi. Questa attività non ha alcun impatto funzionale ed è pertanto facoltativa
* [Fork](fork.md): crea transizioni in uscita per avviare più attività contemporaneamente.
* [Scheduler](scheduler.md): pianifica l&#39;avvio della campagna in più passaggi.
* [Test](test.md): abilita le transizioni in base alle condizioni specificate.
* [Attendi](wait.md): sospendi momentaneamente l&#39;esecuzione di una parte di una campagna con più passaggi.
