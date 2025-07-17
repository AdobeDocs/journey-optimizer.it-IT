---
solution: Journey Optimizer
product: journey optimizer
title: Passaggi di configurazione
description: Scopri come inserire in Adobe Experience Platform dati provenienti da origini supportate, come SFTP, archiviazione cloud o database.
badge: label="Alpha"
hide: true
hidefromtoc: true
source-git-commit: 3f92dc721648f822687b8efc302c40989b72b145
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 17%

---

# Acquisire dati {#ingest-data}

+++ Sommario

| Benvenuto in campagne orchestrate | Lanciare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](gs-orchestrated-campaigns.md)<br/><br/>Creazione e gestione di schemi e set di dati relazionali</br> <ul><li>[Introduzione a schemi e set di dati](gs-schemas.md)</li><li>[Schema manuale](manual-schema.md)</li><li>[Schema di caricamento file](file-upload-schema.md)</li><li>[Acquisire dati](ingest-data.md)</li></ul>[Accedere e gestire campagne orchestrate](access-manage-orchestrated-campaigns.md)<br/><br/>[Passaggi chiave per creare una campagna orchestrata](gs-campaign-creation.md) | [Crea e pianifica la campagna](create-orchestrated-campaign.md)<br/><br/>[Orchestrazione attività](orchestrate-activities.md)<br/><br/>[Avvia e monitora la campagna](start-monitor-campaigns.md)<br/><br/>[Generazione rapporti](reporting-campaigns.md) | [Utilizzare il generatore di regole](orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](build-query.md)<br/><br/>[Modificare le espressioni](edit-expressions.md)<br/><br/>[Retargeting](retarget.md) | [Inizia a usare le attività](activities/about-activities.md)<br/><br/>Attività:<br/>[Partecipa e unisci](activities/and-join.md) - [Genera pubblico](activities/build-audience.md) - [Modifica dimensione](activities/change-dimension.md) - [Attività canale](activities/channels.md) - [Combina](activities/combine.md) - [Deduplicazione](activities/deduplication.md) - [Arricchimento](activities/enrichment.md) - [Fork](activities/fork.md) - [Riconciliazione](activities/reconciliation.md) - [Salva pubblico](activities/save-audience.md) - [Dividi](activities/split.md) - [Attendi](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

</br>

Il contenuto di questa pagina non è definitivo e potrebbe essere soggetto a modifiche.

>[!ENDSHADEBOX]

Adobe Experience Platform consente di acquisire dati da origini esterne e allo stesso tempo di strutturare, etichettare e migliorare i dati in arrivo tramite i servizi Experience Platform. È possibile acquisire dati da diverse origini, ad esempio applicazioni Adobe, archivi basati su cloud, database e molte altre.

<!--
## With Cloud storage {#ingest}


>[!IMPORTANT]
>
>Each dataset in Adobe Experience Platform supports only one active dataflow at a time. For detailed setup guidance on how to switch data sources, refer to this [section](#cdc-ingestion).


You can configure a data flow to ingest data from an Amazon S3 source into Adobe Experience Platform. Once configured, the data flow enables automated, scheduled ingestion of structured data and supports real-time updates.

1. From the **[!UICONTROL Connections]** menu, access the **[!UICONTROL Sources]** menu.

1. Select the **[!UICONTROL Cloud storage]** category then Amazon S3 and click **[!UICONTROL Add Data]**.

    ![](assets/admin_sources_1.png)

1. Connect your S3 Account:

    * With an existing account

    * With a new account

    [Learn more in Adobe Experience Platform documentation](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3#connect)

    ![](assets/admin_sources_2.png)

1. Choose your folder **[!UICONTROL Data format]**, **[!UICONTROL Delimiter]** and **[!UICONTROL Compression type]**.

1. Navigate through the connected S3 source until you locate the two folders created earlier i.e. **loyalty rewards** and **loyalty transactions**.

1. Select the folder that contains your data.
    
    Selecting a folder ensures that all current and future files with the same structure are automatically processed. Selecting a single file, however, requires manually uploading each new data increment.

    ![](assets/S3_config_2.png)

1. Choose your folder **[!UICONTROL Data format]**, **[!UICONTROL Delimiter]** and **[!UICONTROL Compression type]**. Review your sample data for accuracy, then click **[!UICONTROL Next]**.

    ![](assets/S3_config_1.png)

1. Check **[!UICONTROL Enable Change data capture]** to select from datasets that are mapped to relational schemas and have both a primary key and a version descriptor defined.

1. Select your [previously created Dataset](#entities) and click **[!UICONTROL Next]**.

    ![](assets/S3_config_3.png)

1. In the **[!UICONTROL Mapping]** window, verify that each source file attribute is correctly mapped with the corresponding fields in the target schema.

    Click **[!UICONTROL Next]** once done.

    ![](assets/S3_config_4.png)

1. Configure the data flow **[!UICONTROL Schedule]** based on your desired frequency.

1. Click **[!UICONTROL Finish]** to create the data flow. It will execute automatically according to the defined schedule.

1. From the **[!UICONTROL Connections]** menu, select **[!UICONTROL Sources]** and access the **[!UICONTROL Data Flows]** tab to track flow execution, review ingested records, and troubleshoot any errors.

    ![](assets/S3_config_5.png)

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