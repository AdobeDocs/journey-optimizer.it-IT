---
solution: Journey Optimizer
product: journey optimizer
title: Passaggi di configurazione
description: Scopri come creare uno schema relazionale in Adobe Experience Platform caricando una DDL
badge: label="Alpha"
hide: true
hidefromtoc: true
source-git-commit: 3f92dc721648f822687b8efc302c40989b72b145
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 8%

---

# Introduzione a schemi e set di dati{#gs-schemas}

+++ Sommario

| Benvenuto in campagne orchestrate | Lanciare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](gs-orchestrated-campaigns.md)<br/><br/>Creazione e gestione di schemi e set di dati relazionali:</br> <ul><li>[Introduzione a schemi e set di dati](gs-schemas.md)</li><li>[Schema manuale](manual-schema.md)</li><li>[Schema di caricamento file](file-upload-schema.md)</li><li>[Acquisire dati](ingest-data.md)</li></ul>[Accedere e gestire campagne orchestrate](access-manage-orchestrated-campaigns.md)<br/><br/>[Passaggi chiave per creare una campagna orchestrata](gs-campaign-creation.md) | [Crea e pianifica la campagna](create-orchestrated-campaign.md)<br/><br/>[Orchestrazione attività](orchestrate-activities.md)<br/><br/>[Avvia e monitora la campagna](start-monitor-campaigns.md)<br/><br/>[Generazione rapporti](reporting-campaigns.md) | [Utilizzare il generatore di regole](orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](build-query.md)<br/><br/>[Modificare le espressioni](edit-expressions.md)<br/><br/>[Retargeting](retarget.md) | [Inizia a usare le attività](activities/about-activities.md)<br/><br/>Attività:<br/>[Partecipa e unisci](activities/and-join.md) - [Genera pubblico](activities/build-audience.md) - [Modifica dimensione](activities/change-dimension.md) - [Attività canale](activities/channels.md) - [Combina](activities/combine.md) - [Deduplicazione](activities/deduplication.md) - [Arricchimento](activities/enrichment.md) - [Fork](activities/fork.md) - [Riconciliazione](activities/reconciliation.md) - [Salva pubblico](activities/save-audience.md) - [Dividi](activities/split.md) - [Attendi](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

</br>

Il contenuto di questa pagina non è definitivo e potrebbe essere soggetto a modifiche.

>[!ENDSHADEBOX]

Questa guida illustra i passaggi necessari per creare uno schema relazionale, configurare un set di dati per campagne orchestrate, acquisire dati tramite un’origine S3 ed eseguire query sui dati acquisiti nella piattaforma AP.

<!--
In this example, the setup includes integrating two key entities, **Loyalty Transactions** and **Loyalty Rewards**, and link them to existing core entities **Recipients** and **Brands**. 

![](assets/do-not-localize/schema_admin.png)

1. [Create relational Schema and associated Dataset](#schema)
    
    Define the relational data model for orchestrated campaigns, including the **Loyalty Memberships**, **Loyalty Transactions** and **Loyalty Rewards** entities, along with required keys and versioning attributes.

1. [Link schema](#link-schema)

    Link the **Loyalty Transactions** entity to **Recipients**, and **Loyalty Rewards** to **Brands**, to build a connected data model that supports personalized customer journeys.

1. [Ingest Data](#ingest)

    Bring data into Adobe Experience Platform from supported sources like SFTP, cloud storage, or databases.

-->

<!--### Setting Up Change data capture ingestion {#cdc-ingestion}

If you need to change the data source, you must delete the existing dataflow and create a new one pointing to the same dataset with the new source.

When using Change Data Capture (CDC), it is essential that the source and dataset remain in sync to ensure accurate incremental updates. Follow the steps below:

1. **Schema Requirements**
   - Your schema must include:
     - A **primary key** (e.g., `transaction_id`)
     - A **versioning field** (e.g., `lastmodified` or an incrementing `version_id`)
   - Enable the dataset for **Orchestrated Campaigns** if needed.

2. **CDC Dataflow Setup**
   - During dataflow creation, after choosing your source and files:
     - **Enable the CDC option**
     - Select your CDC-ready dataset
     - Confirm field mappings (especially version field)

3. **Keep Source and Target in Sync**
   - The source system must consistently update the version field so the platform can detect changes accurately.

Once set up, the platform will automatically ingest **only changed or new records** each time the flow runs.
-->
