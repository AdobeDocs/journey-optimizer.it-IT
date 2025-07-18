---
solution: Journey Optimizer
product: journey optimizer
title: Passaggi di configurazione
description: Scopri come inserire in Adobe Experience Platform dati provenienti da origini supportate, come SFTP, archiviazione cloud o database.
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 7f1e7985-b68e-43d6-9c8f-fea2469f8af9
source-git-commit: 3dc0bf4acc4976ca1c46de46cf6ce4f2097f3721
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 6%

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

## Con archiviazione cloud {#ingest}


>[!IMPORTANT]
>
>Ogni set di dati in Adobe Experience Platform supporta un solo flusso di dati attivo alla volta. Per istruzioni dettagliate su come cambiare origine dati, consulta questa [sezione](#cdc-ingestion).


Puoi configurare un flusso di dati per acquisire i dati da un’origine Amazon S3 a Adobe Experience Platform. Una volta configurato, il flusso di dati consente l’acquisizione automatica e pianificata di dati strutturati e supporta gli aggiornamenti in tempo reale.

1. Dal menu **[!UICONTROL Connessioni]**, accedere al menu **[!UICONTROL Origini]**.

1. Seleziona la categoria **[!UICONTROL Archiviazione cloud]**, quindi Amazon S3 e fai clic su **[!UICONTROL Aggiungi dati]**.

   ![](assets/admin_sources_1.png)

1. Connetti il tuo account S3:

   * Con un account esistente

   * Con un nuovo account

   [Ulteriori informazioni nella documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3#connect)

   ![](assets/admin_sources_2.png)

1. Scegli la cartella **[!UICONTROL Formato dati]**, **[!UICONTROL Delimitatore]** e **[!UICONTROL Tipo di compressione]**.

1. Naviga nell&#39;origine S3 connessa fino a individuare le cartelle desiderate, ad esempio **premi fedeltà** e **transazioni fedeltà**.

1. Selezionare la cartella contenente i dati.

   La selezione di una cartella garantisce che tutti i file correnti e futuri con la stessa struttura vengano elaborati automaticamente. La selezione di un singolo file, tuttavia, richiede il caricamento manuale di ogni nuovo incremento di dati.

   ![](assets/S3_config_2.png)

1. Scegli la cartella **[!UICONTROL Formato dati]**, **[!UICONTROL Delimitatore]** e **[!UICONTROL Tipo di compressione]**. Verifica la precisione dei dati di esempio, quindi fai clic su **[!UICONTROL Avanti]**.

   ![](assets/S3_config_1.png)

1. Selezionare **[!UICONTROL Abilita Change data capture]** per effettuare una selezione da set di dati mappati a schemi relazionali e per i quali sono definiti sia una chiave primaria che un descrittore di versione.

1. Seleziona il [set di dati creato in precedenza](#entities) e fai clic su **[!UICONTROL Avanti]**.

   ![](assets/S3_config_3.png)

1. Nella finestra **[!UICONTROL Mapping]**, verifica che ogni attributo del file di origine sia mappato correttamente con i campi corrispondenti nello schema di destinazione.

   Al termine, fai clic su **[!UICONTROL Avanti]**.

   ![](assets/S3_config_4.png)

1. Configura il flusso di dati **[!UICONTROL Pianificazione]** in base alla frequenza desiderata.

1. Fare clic su **[!UICONTROL Fine]** per creare il flusso di dati. Viene eseguito automaticamente in base alla pianificazione definita.

1. Dal menu **[!UICONTROL Connessioni]**, seleziona **[!UICONTROL Origini]** e accedi alla scheda **[!UICONTROL Flussi di dati]** per monitorare l&#39;esecuzione del flusso, esaminare i record acquisiti e risolvere eventuali errori.

   ![](assets/S3_config_5.png)

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
