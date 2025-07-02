---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività Modifica dimensione
description: Scopri come utilizzare l’attività Modifica dimensione
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 83e66f10-93dd-4759-840c-2c83abc42a28
source-git-commit: e01715416659270ddf75eb9fdb8f0eb03063bd7b
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 29%

---

# Cambiare dimensione {#change-dimension}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_dimension_complement"
>title="Generare un complemento"
>abstract="Puoi generare una transizione in uscita aggiuntiva con la popolazione rimanente, che è stata esclusa come duplicato. A tale scopo, attiva l’opzione **Genera complemento**"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_change_dimension"
>title="Attività Cambia dimensione"
>abstract="Questa attività ti consente di modificare la dimensione targeting durante la creazione di un pubblico. Sposta l’asse in base al modello di dati e alla dimensione di input. Ad esempio, puoi passare dalla dimensione “contratti” alla dimensione “clienti”."

+++ Sommario

| Benvenuto in campagne orchestrate | Lanciare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](../gs-orchestrated-campaigns.md)<br/><br/>[Passaggi di configurazione](../configuration-steps.md)<br/><br/>[Passaggi chiave per la creazione di campagne orchestrate](../gs-campaign-creation.md) | [Creare una campagna orchestrata](../create-orchestrated-campaign.md)<br/><br/>[Orchestrare le attività](../orchestrate-activities.md)<br/><br/><br/>[Avviare e monitorare la campagna](../start-monitor-campaigns.md)<br/><br/>[Generazione rapporti](../reporting-campaigns.md) | [Utilizzare Query Modeler](../orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](../build-query.md)<br/><br/>[Modificare le espressioni](../edit-expressions.md) | [Inizia a usare le attività](about-activities.md)<br/><br/>Attività:<br/>[Partecipa/Partecipa](and-join.md) - [Genera pubblico](build-audience.md) - **[Modifica dimensione](change-dimension.md)** - [Combina](combine.md) - [Deduplicazione](deduplication.md) - [Arricchimento](enrichment.md) - [Fork](fork.md) - [Riconciliazione](reconciliation.md) - [Dividi](split.md) - [Attendi](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

In qualità di addetto al marketing, puoi perfezionare il targeting del pubblico passando da un’entità di dati a un’altra entità collegata all’interno di una campagna orchestrata. Questo consente di passare dal targeting dei profili utente ad azioni specifiche, come acquisti, prenotazioni o altre interazioni.

A tale scopo, utilizzare l&#39;attività **[!UICONTROL Modifica dimensione]**. Ti consente di modificare la dimensione di targeting durante la campagna orchestrata, in base alla struttura del modello di dati e alla dimensione di input.

<!--
>[!IMPORTANT]
>
>Please note that the **[!UICONTROL Change Dimension]** and **[!UICONTROL Change Data source]** activities should not be added in one row. If you need to use both activities consecutively, make sure you include an **[!UICONTROL Enrichement]** activity in between them. This ensures proper execution and prevents potential conflicts or errors.-->

## Configurare l’attività Cambia dimensione {#configure}

Per configurare l’attività **[!UICONTROL Cambia dimensione]** segui questi passaggi:

1. Aggiungi un&#39;attività **[!UICONTROL Modifica dimensione]** alla campagna orchestrata.

   ![](../assets/change-dimension.png)

1. Definisci la **[!UICONTROL Nuova dimensione target]**. Durante la modifica della dimensione vengono conservati tutti i record.

1. Esegui la campagna orchestrata per visualizzare il risultato. Confronta i dati nelle tabelle prima e dopo l’attività di modifica della dimensione e confronta la struttura delle tabelle delle campagne orchestrate.

## Esempio {#example}

Questo caso d’uso prevede l’invio di un SMS ai profili che hanno creato una lista dei desideri nel mese scorso.

Inizia con un&#39;attività **[!UICONTROL Genera pubblico]** utilizzando la dimensione di targeting **[!UICONTROL Elenco desideri]** per selezionare tutti gli elenchi desideri pertinenti.

Quindi, inserisci un&#39;attività di **[!UICONTROL Modifica dimensione]** per cambiare la dimensione di targeting da **[!UICONTROL Elenco desideri]** a ****[!UICONTROL Destinatario]**. In questo modo la campagna orchestrata può inviare l’SMS ai profili associati a tali elenchi di desideri.

![](../assets/change-dimension-example.png)
