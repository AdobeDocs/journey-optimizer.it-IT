---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare il generatore di regole
description: Scopri come creare regole per le campagne orchestrate
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: fb7a0eb2-b2ff-49fa-af1f-f1c10f219b00
source-git-commit: 6439be00315dfde7ab385d7f848b7031d95060f4
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 10%

---


# Utilizzare il generatore di regole {#orchestrated-rule-builder}

+++ Sommario

| Benvenuto in campagne orchestrate | Lanciare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](gs-orchestrated-campaigns.md)<br/><br/>[Passaggi di configurazione](configuration-steps.md)<br/><br/>[Accedere e gestire le campagne orchestrate](access-manage-orchestrated-campaigns.md) | [Passaggi chiave per la creazione orchestrata della campagna](gs-campaign-creation.md)<br/><br/>[Creare e pianificare la campagna](create-orchestrated-campaign.md)<br/><br/>[Orchestrare le attività](orchestrate-activities.md)<br/><br/><b>[Avviare e monitorare la campagna](start-monitor-campaigns.md)</b><br/><br/>[Generazione rapporti](reporting-campaigns.md) | [Utilizzare il generatore di regole](orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](build-query.md)<br/><br/>[Modificare le espressioni](edit-expressions.md)<br/><br/>[Retargeting](retarget.md) | [Inizia a usare le attività](activities/about-activities.md)<br/><br/>Attività:<br/>[Partecipa e unisci](activities/and-join.md) - [Genera pubblico](activities/build-audience.md) - [Modifica dimensione](activities/change-dimension.md) - [Attività canale](activities/channels.md) - [Combina](activities/combine.md) - [Deduplicazione](activities/deduplication.md) - [Arricchimento](activities/enrichment.md) - [Fork](activities/fork.md) - [Riconciliazione](activities/reconciliation.md) - [Salva pubblico](save-audience.md) - [Dividi](activities/split.md) - [Attendi](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

Le campagne orchestrate dispongono di un generatore di regole che semplifica il processo di filtraggio del database in base a vari criteri. Il generatore di regole gestisce in modo efficiente query molto complesse e lunghe, offrendo maggiore flessibilità e precisione.

Supporta anche filtri predefiniti all’interno di condizioni, consentendoti di perfezionare le query con facilità utilizzando espressioni avanzate e operatori per strategie complete di targeting del pubblico e segmentazione.

## Accedere al generatore di regole

Il query modeler è disponibile in ogni contesto in cui è necessario definire regole per filtrare i dati.

| Utilizzo | Esempio |
|  ---  |  ---  |
| **Genera tipi di pubblico**: specifica la popolazione di cui desideri eseguire il targeting nelle campagne orchestrate utilizzando un&#39;attività **[!UICONTROL Genera pubblico]** e crea facilmente nuovi tipi di pubblico su misura per le tue esigenze. [Scopri come creare tipi di pubblico](../orchestrated/activities/build-audience.md) | ![Immagine che mostra come accedere all&#39;interfaccia di creazione del pubblico](assets/query-access-audience.png){width="200" align="center" zoomable="yes"} |
| **Crea condizione nell&#39;area di lavoro della campagna**: applica le regole nell&#39;area di lavoro della campagna utilizzando un&#39;attività **[!UICONTROL Dividi]**, per allinearle ai requisiti specifici. [Scopri come utilizzare un&#39;attività Split](../orchestrated/activities/split.md) | ![Immagine che mostra come accedere alle opzioni di personalizzazione del flusso di lavoro](assets/query-access-split.png){width="200" align="center" zoomable="yes"} |
| **Creare filtri avanzati**: creare regole per filtrare i dati visualizzati in elenchi quali i registri del flusso di lavoro o le dimensioni di targeting. | ![Immagine che mostra come personalizzare i filtri elenco](assets/query-access-advanced-filters.png){width="200" align="center" zoomable="yes"} |

## Interfaccia del generatore di regole {#interface}

Il generatore di regole fornisce un&#39;area di lavoro centrale in cui generare la query e un riquadro delle proprietà che fornisce informazioni sulla regola.

![Immagine che mostra l&#39;interfaccia del generatore di regole](assets/rule-builder-interface.png)

* L&#39;**area di lavoro centrale** è il luogo in cui aggiungere e combinare i diversi componenti per generare la regola. [Scopri come creare una regola](../orchestrated/build-query.md)

* Il riquadro **[!UICONTROL Proprietà regola]** fornisce informazioni sulla regola. Ti consente di eseguire varie operazioni per controllare la regola e assicurarti che sia adatta alle tue esigenze.

  Questo riquadro viene visualizzato quando si crea una query per creare un pubblico. [Scopri come controllare e convalidare la query](build-query.md#check-and-validate-your-query)
