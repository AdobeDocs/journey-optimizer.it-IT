---
solution: Journey Optimizer
product: journey optimizer
title: Passaggi di configurazione
description: Scopri come inserire in Adobe Experience Platform dati provenienti da origini supportate, come SFTP, archiviazione cloud o database.
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 7f1e7985-b68e-43d6-9c8f-fea2469f8af9
source-git-commit: 6447f5d1a060037c0ceaa374db20966097585f9c
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 38%

---

# Acquisire i dati {#ingest-data}

+++ Sommario

| Ti diamo il benvenuto nelle campagne orchestrate | Avviare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](gs-orchestrated-campaigns.md)<br/><br/>Creazione e gestione di schemi e set di dati relazionali</br> <ul><li>[Introduzione a schemi e set di dati](gs-schemas.md)</li><li>[Schema manuale](manual-schema.md)</li><li>[Schema di caricamento file](file-upload-schema.md)</li><li>[Acquisire dati](ingest-data.md)</li></ul>[Accedere e gestire campagne orchestrate](access-manage-orchestrated-campaigns.md)<br/><br/>[Passaggi chiave per creare una campagna orchestrata](gs-campaign-creation.md) | [Creare e pianificare la campagna](create-orchestrated-campaign.md)<br/><br/>[Orchestrare le attività](orchestrate-activities.md)<br/><br/>[Avviare e monitorare la campagna](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | [Utilizzare il generatore di regole](orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](build-query.md)<br/><br/>[Modificare le espressioni](edit-expressions.md)<br/><br/>[Retargeting](retarget.md) | [Introduzione alle attività](activities/about-activities.md)<br/><br/>Attività:<br/>[AND-join](activities/and-join.md) - [Crea pubblico](activities/build-audience.md) - [Modifica dimensione](activities/change-dimension.md) - [Attività canale](activities/channels.md) - [Combina](activities/combine.md) - [Deduplica](activities/deduplication.md) - [Arricchimento](activities/enrichment.md) - [Fork](activities/fork.md) - [Riconciliazione](activities/reconciliation.md) - [Salva pubblico](activities/save-audience.md) - [Dividi](activities/split.md) - [Attendi](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

</br>

Il contenuto di questa pagina non è definitivo e potrebbe essere soggetto a modifiche.

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>Per modificare l’origine dati per un set di dati, devi prima eliminare il flusso di dati esistente prima di crearne uno nuovo che faccia riferimento allo stesso set di dati e alla nuova origine.
>
>Adobe Experience Platform applica una stretta relazione uno-a-uno tra flussi di dati e set di dati. Questo consente di mantenere la sincronizzazione tra l’origine e il set di dati per un’acquisizione incrementale accurata.

Adobe Experience Platform consente di acquisire dati da origini esterne e allo stesso tempo di strutturare, etichettare e migliorare i dati in arrivo tramite i servizi Platform. È possibile acquisire dati da diverse origini, ad esempio applicazioni Adobe, archivi basati su cloud, database e molte altre.

## Origini supportate per le campagne orchestrate {#supported}

Le seguenti origini sono supportate per l’utilizzo con campagne orchestrate:

<table>
  <thead>
    <tr>
      <th>Tipo</th>
      <th>Origine</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="3">Archiviazione cloud</td>
      <td><a href="https://experienceleague.adobe.com/it/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/s3">Amazon S3</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/it/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/google-cloud-storage">Google Cloud Storage</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/it/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/sftp">SFTP</a></td>
    </tr>
      <td rowspan="4">Data Warehouse cloud</td>
      <td><a href="https://experienceleague.adobe.com/it/docs/experience-platform/sources/ui-tutorials/create/databases/snowflake">Snowflake</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/it/docs/experience-platform/sources/ui-tutorials/create/databases/bigquery">Google BigQuery</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/it/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/data-landing-zone">Data Landing Zone<a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/it/docs/experience-platform/sources/ui-tutorials/create/databases/databricks">Azure Databricks</a></td>
    </tr>
    <tr>
      <td rowspan="3">Caricamenti basati su file</td>
      <td><a href="https://experienceleague.adobe.com/it/docs/experience-platform/sources/ui-tutorials/create/local-system/local-file-upload">Caricamento file locale<a></td>
    </tr>

</tbody>
</table>

## Configurare un flusso di dati

In questo esempio viene illustrato come configurare un flusso di dati per l’acquisizione di dati strutturati in Adobe Experience Platform. Il flusso di dati configurato supporta l’acquisizione automatizzata e pianificata e consente aggiornamenti in tempo reale.

1. Dal menu **[!UICONTROL Connessioni]**, accedi al menu **[!UICONTROL Origini]**.

1. Scegli la tua origine in base alle [origini supportate per le campagne orchestrate](#supported).

   ![](assets/admin_sources_1.png)

1. Connetti l’account Cloud Storage o Google Cloud Storage se hai scelto sorgenti basate su cloud.

   ![](assets/admin_sources_2.png)

1. Scegli i dati da acquisire in Adobe Experience Platform.

   ![](assets/S3_config_1.png)

1. Dalla pagina **[!UICONTROL Dettagli set di dati]**, selezionare **[!UICONTROL Abilita acquisizione dati modifica]** per visualizzare solo i set di dati mappati a schemi relazionali e che includono sia una chiave primaria che un descrittore di versione.

   >[!IMPORTANT]
   >
   > Solo per **origini basate su file**, ogni riga nel file di dati deve includere una colonna `_change_request_type` con valori `U` (upsert) o `D` (delete). Senza questa colonna, il sistema non riconoscerà i dati come supporto del rilevamento delle modifiche e l’interruttore Campagna orchestrata non verrà visualizzato, impedendo al set di dati di essere selezionato per il targeting.

   ![](assets/S3_config_6.png)

1. Seleziona il set di dati creato in precedenza e fai clic su **[!UICONTROL Avanti]**.

   ![](assets/S3_config_3.png)

1. Se utilizzi solo origini basate su file, dalla finestra **[!UICONTROL Seleziona dati]**, carica i file locali e visualizzane in anteprima la struttura e il contenuto.

   La dimensione massima supportata è 100 MB.

1. Nella finestra **[!UICONTROL Mappatura]**, verifica che ogni attributo del file di origine sia mappato correttamente ai campi corrispondenti nello schema di destinazione.

   Al termine, fai clic su **[!UICONTROL Avanti]**.

   ![](assets/S3_config_4.png)

1. Configura il flusso di dati **[!UICONTROL Pianificazione]** in base alla frequenza desiderata.

1. Fai clic su **[!UICONTROL Fine]** per creare il flusso di dati. Viene eseguito automaticamente in base alla pianificazione definita.

1. Dal menu **[!UICONTROL Connessioni]**, seleziona **[!UICONTROL Origini]** e accedi alla scheda **[!UICONTROL Flussi di dati]** per monitorare l’esecuzione del flusso, rivedere i record acquisiti e risolvere eventuali errori.

   ![](assets/S3_config_5.png)

