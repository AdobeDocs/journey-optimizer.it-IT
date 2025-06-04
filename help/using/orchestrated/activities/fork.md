---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività Fork
description: Scopri come utilizzare l’attività Fork in una campagna orchestrata
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: 52e8057b-dac1-45f5-9dd0-1b28a59adde9
source-git-commit: 9606ca5710e6f91159474d76f68cdcbc2128b000
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 60%

---

# Fork {#fork}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_fork"
>title="Attività Fork"
>abstract="L’attività **Fork** consente di creare transizioni in uscita per avviare più attività contemporaneamente."


>[!CONTEXTUALHELP]
>id="ajo_orchestration_fork_transitions"
>title="Transizioni delle attività Fork"
>abstract="Per impostazione predefinita, vengono create due transizioni con attività **Fork**. Fai clic sul pulsante **Aggiungi transizione** per definire una transizione in uscita aggiuntiva e immetterne l’etichetta."

+++ Sommario

| Benvenuto in campagne orchestrate | Avviare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](../gs-orchestrated-campaigns.md)<br/><br/>[Passaggi di configurazione](../configuration-steps.md)<br/><br/>[Passaggi chiave per la creazione di campagne orchestrate](../gs-campaign-creation.md) | [Creare una campagna orchestrata](../create-orchestrated-campaign.md)<br/><br/>[Orchestrare le attività](../orchestrate-activities.md)<br/><br/>[Inviare messaggi con le campagne orchestrate](../send-messages.md)<br/><br/>[Avviare e monitorare la campagna](../start-monitor-campaigns.md)<br/><br/>[Generazione rapporti](../reporting-campaigns.md) | [Utilizzare Query Modeler](../orchestrated-query-modeler.md)<br/><br/>[Creare la prima query](../build-query.md)<br/><br/>[Modificare le espressioni](../edit-expressions.md) | [Inizia a usare le attività](about-activities.md)<br/><br/>Attività:<br/>[Partecipa/Partecipa](and-join.md) - [Genera pubblico](build-audience.md) - [Modifica dimensione](change-dimension.md) - [Combina](combine.md) - [Deduplicazione](deduplication.md) - [Arricchimento](enrichment.md) - [Fork](fork.md) - [Riconciliazione](reconciliation.md) - [Dividi](split.md) - [Attendi](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

L’attività **Fork** è un’attività di **Controllo del flusso**. Ti consente di creare transizioni in uscita per avviare più attività contemporaneamente.

## Configurare l’attività Fork{#fork-configuration}

Per configurare l’attività **Fork** segui questi passaggi:

![](../assets/workflow-fork.png)

1. Aggiungi un&#39;attività **Fork** alla campagna orchestrata.
1. Fai clic su **Aggiungi transizione** per aggiungere una nuova transizione in uscita. Per impostazione predefinita sono definite due transizioni.
1. Aggiungi un’etichetta a ciascuna delle transizioni.

## Esempio{#fork-example}

Nell’esempio seguente vengono utilizzate due attività **Fork**:

* Una prima delle due query, per eseguirle contemporaneamente.
* Una dopo l’intersezione, per inviare contemporaneamente un’e-mail e un SMS alla popolazione target.

![](../assets/workflow-fork-example.png)
