---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività Cambia dimensione
description: Scopri come utilizzare l’attività Cambia dimensione
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 83e66f10-93dd-4759-840c-2c83abc42a28
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 62%

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

| Benvenuto in Campagne orchestrate | Avviare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](../gs-orchestrated-campaigns.md)<br/><br/>Creazione e gestione di schemi e set di dati relazionali:</br> <ul><li>[Introduzione a schemi e set di dati](../gs-schemas.md)</li><li>[Schema manuale](../manual-schema.md)</li><li>[Schema di caricamento file](../file-upload-schema.md)</li><li>[Acquisire dati](../ingest-data.md)</li></ul>[Accedere e gestire le campagne orchestrate](../access-manage-orchestrated-campaigns.md) | [Passaggi chiave per creare una campagna orchestrata](../gs-campaign-creation.md)<br/><br/>[Creare e pianificare la campagna](../create-orchestrated-campaign.md)<br/><br/>[Orchestrare le attività](../orchestrate-activities.md)<br/><br/>[Avviare e monitorare la campagna](../start-monitor-campaigns.md)<br/><br/>[Generazione rapporti](../reporting-campaigns.md) | [Utilizzare il generatore di regole](../orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](../build-query.md)<br/><br/>[Modificare le espressioni](../edit-expressions.md)<br/><br/>[Retargeting](../retarget.md) | [Introduzione alle attività](about-activities.md)<br/><br/>Attività:<br/>[AND-join](and-join.md) - [Crea pubblico](build-audience.md) - <b>[Modifica dimensione](change-dimension.md)</b> - [Attività canale](channels.md) - [Combina](combine.md) - [Deduplica](deduplication.md) - [Arricchimento](enrichment.md) - [Fork](fork.md) - [Riconciliazione](reconciliation.md) - [Salva pubblico](save-audience.md) - [Dividi](split.md) - [Attendi](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

Il contenuto di questa pagina non è definitivo e potrebbe essere soggetto a modifiche.

>[!ENDSHADEBOX]

In qualità di addetto al marketing, puoi migliorare il targeting del pubblico passando da un’entità dati a una correlata all’interno di una campagna orchestrata. Questo ti consente di andare oltre i profili utente e di concentrarti su comportamenti specifici, come acquisti, prenotazioni o altre interazioni.

A tal fine, utilizza l’attività **[!UICONTROL Modifica dimensione]**. Consente di regolare la dimensione di targeting durante la campagna orchestrata.

<!--
>[!IMPORTANT]
>
>Please note that the **[!UICONTROL Change Dimension]** and **[!UICONTROL Change Data source]** activities should not be added in one row. If you need to use both activities consecutively, make sure you include an **[!UICONTROL Enrichement]** activity in between them. This ensures proper execution and prevents potential conflicts or errors.-->

## Configurare l’attività Cambia dimensione {#configure}

Per configurare l’attività **[!UICONTROL Cambia dimensione]** segui questi passaggi:

1. Aggiungi un&#39;attività **[!UICONTROL Modifica dimensione]** alla campagna orchestrata.

   ![](../assets/orchestrated-change-dimension.png)

1. Definisci la **[!UICONTROL nuova dimensione target]**. Durante la modifica della dimensione, tutti i record vengono mantenuti.


## Esempio {#example}

Questo caso d’uso si incentra sull’invio di un SMS ai profili che hanno creato una wishlist nell’ultimo mese.

Inizia con un’attività **[!UICONTROL Crea pubblico]**, utilizzando la dimensione di targeting **[!UICONTROL Wishlist]** per identificare tutte quelle rilevanti.

Quindi, aggiungi un’attività **[!UICONTROL Cambia dimensione]** per passare dalla dimensione di targeting **[!UICONTROL Wishlist]** a **[!UICONTROL Destinatario].** Questo passaggio assicura che la campagna orchestrata esegua il targeting dei profili corretti collegati a tali elenchi di desideri, consentendo l&#39;invio dell&#39;SMS ai profili desiderati.

![](../assets/orchestrated-change-dimension-example.png)
