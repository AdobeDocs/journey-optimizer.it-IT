---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare il generatore di regole
description: Scopri come creare regole per le campagne orchestrate
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: fb7a0eb2-b2ff-49fa-af1f-f1c10f219b00
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 87%

---


# Utilizzare il generatore di regole {#orchestrated-rule-builder}

+++ Sommario

| Ti diamo il benvenuto nelle campagne orchestrate | Avviare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](gs-orchestrated-campaigns.md)<br/><br/>Creazione e gestione di schemi e set di dati relazionali:</br> <ul><li>[Introduzione a schemi e set di dati](gs-schemas.md)</li><li>[Schema manuale](manual-schema.md)</li><li>[Schema di caricamento file](file-upload-schema.md)</li><li>[Acquisire dati](ingest-data.md)</li></ul>[Accedere e gestire campagne orchestrate](access-manage-orchestrated-campaigns.md)<br/><br/>[Passaggi chiave per creare una campagna orchestrata](gs-campaign-creation.md) | [Creare e pianificare la campagna](create-orchestrated-campaign.md)<br/><br/>[Orchestrare le attività](orchestrate-activities.md)<br/><br/>[Avviare e monitorare la campagna](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | <b>[Utilizzare il generatore di regole](orchestrated-rule-builder.md)</b><br/><br/>[Creare la prima query](build-query.md)<br/><br/>[Modificare le espressioni](edit-expressions.md)<br/><br/>[Retargeting](retarget.md) | [Introduzione alle attività](activities/about-activities.md)<br/><br/>Attività:<br/>[AND-join](activities/and-join.md) - [Crea pubblico](activities/build-audience.md) - [Modifica dimensione](activities/change-dimension.md) - [Attività canale](activities/channels.md) - [Combina](activities/combine.md) - [Deduplica](activities/deduplication.md) - [Arricchimento](activities/enrichment.md) - [Fork](activities/fork.md) - [Riconciliazione](activities/reconciliation.md) - [Salva pubblico](activities/save-audience.md) - [Dividi](activities/split.md) - [Attendi](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

Il contenuto di questa pagina non è definitivo e potrebbe essere soggetto a modifiche.

>[!ENDSHADEBOX]

Le campagne orchestrate dispongono di un generatore di regole che semplifica il processo di filtro del database in base a vari criteri. Il generatore di regole gestisce in modo efficiente query molto complesse e lunghe, offrendo maggiore flessibilità e precisione.

Supporta anche filtri preimpostati all’interno di condizioni, consentendoti di perfezionare le query con facilità utilizzando espressioni avanzate e operatori per strategie complete di targeting e segmentazione del pubblico.

## Accedere al generatore di regole

Il query modeler è disponibile in ogni contesto in cui è necessario definire regole per filtrare i dati.

| Utilizzo | Esempio |
|  ---  |  ---  |
| **Crea tipi di pubblico**: specifica la popolazione per la quale desideri eseguire il targeting nelle campagne orchestrate utilizzando un’attività **[!UICONTROL Crea pubblico]** e crea agevolmente nuovi tipi di pubblico in base alle tue esigenze. [Scopri come creare tipi di pubblico](../orchestrated/activities/build-audience.md) | ![Immagine che mostra come accedere all’interfaccia di creazione del pubblico](assets/query-access-audience.png){width="200" align="center" zoomable="yes"} |
| **Creare condizioni nell’area di lavoro della campagna**: applica le regole nell’area di lavoro della campagna utilizzando un’attività **[!UICONTROL Dividi]**, per allinearle ai requisiti specifici. [Scopri come utilizzare l’attività Dividi](../orchestrated/activities/split.md) | ![Immagine che mostra come accedere alle opzioni di personalizzazione del flusso di lavoro](assets/query-access-split.png){width="200" align="center" zoomable="yes"} |
| **Creare filtri avanzati**: creare regole per filtrare i dati visualizzati in elenchi quali i registri del flusso di lavoro o le dimensioni di targeting. | ![Immagine che mostra come personalizzare i filtri elenco](assets/query-access-advanced-filters.png){width="200" align="center" zoomable="yes"} |

## Interfaccia del generatore di regole {#interface}

Il generatore di regole fornisce un’area di lavoro centrale in cui generare la query e un riquadro delle proprietà che fornisce informazioni sulla regola.

![Immagine che mostra l’interfaccia del generatore di regole](assets/rule-builder-interface.png)

* L’**area di lavoro centrale** è il luogo in cui aggiungere e combinare i diversi componenti per generare la regola. [Scopri come creare una regola](../orchestrated/build-query.md)

* Il riquadro **[!UICONTROL Proprietà regola]** fornisce informazioni sulla regola. Consente di eseguire varie operazioni per verificare la regola e assicurarti che si adatti alle tue esigenze.

  Questo riquadro viene visualizzato quando si genera una query per creare un pubblico. [Scopri come controllare e convalidare la query](build-query.md#check-and-validate-your-query)
