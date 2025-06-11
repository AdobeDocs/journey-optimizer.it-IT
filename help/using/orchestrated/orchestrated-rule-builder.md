---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare il generatore di regole
description: Scopri come creare regole per le campagne orchestrate
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: fb7a0eb2-b2ff-49fa-af1f-f1c10f219b00
source-git-commit: 435b4a7eee9428c7f0efeb62c72b39c0e2aaabba
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 4%

---


# Utilizzare il generatore di regole {#orchestrated-rule-builder}

+++ Sommario

| Benvenuto in campagne orchestrate | Avviare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](gs-orchestrated-campaigns.md)<br/><br/>[Passaggi di configurazione](configuration-steps.md)<br/><br/>[Accesso e gestione delle campagne orchestrate](access-manage-orchestrated-campaigns.md) | [Passaggi chiave per la creazione di campagne orchestrate](gs-campaign-creation.md)<br/><br/>[Creare e pianificare la campagna](create-orchestrated-campaign.md)<br/><br/>[Orchestrare le attività](orchestrate-activities.md)<br/><br/>[Inviare messaggi con campagne orchestrate](send-messages.md)<br/><br/>[Avviare e monitorare la campagna](start-monitor-campaigns.md)<br/><br/>[Generazione rapporti](reporting-campaigns.md) | <b>[Utilizzare il generatore di regole](orchestrated-rule-builder.md)</b><br/><br/>[Creare la prima query](build-query.md)<br/><br/>[Modificare le espressioni](edit-expressions.md) | [Inizia a usare le attività](activities/about-activities.md)<br/><br/>Attività:<br/>[Partecipa/Partecipa](activities/and-join.md) - [Genera pubblico](activities/build-audience.md) - [Modifica dimensione](activities/change-dimension.md) - [Combina](activities/combine.md) - [Deduplicazione](activities/deduplication.md) - [Arricchimento](activities/enrichment.md) - [Fork](activities/fork.md) - [Riconciliazione](activities/reconciliation.md) - [Dividi](activities/split.md) - [Attendi](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

Le campagne orchestrate dispongono di un generatore di regole che semplifica il processo di filtraggio del database in base a vari criteri. Il generatore di regole gestisce in modo efficiente query molto complesse e lunghe, offrendo maggiore flessibilità e precisione.

Inoltre, supporta filtri predefiniti all’interno di condizioni, consentendo agli utenti di perfezionare le query con facilità e allo stesso tempo utilizzare espressioni avanzate e operatori per strategie complete di targeting del pubblico e segmentazione.

## Accedere al generatore di regole

Il generatore di regole è disponibile quando si crea una query in un&#39;attività **[!UICONTROL Genera pubblico]** per eseguire il targeting di un pubblico. Consente di specificare la popolazione di destinazione e di creare facilmente nuovi tipi di pubblico personalizzati in base alle tue esigenze.

![immagine che mostra un&#39;attività del pubblico di compilazione](assets/rule-builder-query.png)

## Interfaccia del generatore di regole {#interface}

Il generatore di regole fornisce un&#39;area di lavoro centrale in cui generare la query e un riquadro delle proprietà che fornisce informazioni sulla regola.

![Immagine che mostra l&#39;interfaccia del generatore di regole](assets/rule-builder-interface.png)

* L&#39;**area di lavoro centrale** è il luogo in cui aggiungere e combinare i diversi componenti per generare la regola. [Scopri come creare una regola](../orchestrated/build-query.md)

* Il riquadro **[!UICONTROL Proprietà regola]** fornisce informazioni sulla regola. Ti consente di eseguire varie operazioni per controllare la regola e assicurarti che sia adatta alle tue esigenze.

  Questo riquadro viene visualizzato quando si crea una query per creare un pubblico. [Scopri come controllare e convalidare la query](build-query.md#check-and-validate-your-query)
