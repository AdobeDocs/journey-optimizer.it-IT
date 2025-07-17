---
solution: Journey Optimizer
product: journey optimizer
title: Passaggi di configurazione
description: Scopri come creare uno schema relazionale in Adobe Experience Platform caricando una DDL
badge: label="Alpha"
hide: true
hidefromtoc: true
source-git-commit: 25120dd71159d0233783ac4c189f528ff2c93ae3
workflow-type: tm+mt
source-wordcount: '827'
ht-degree: 1%

---

# Caricamento di file {#file-upload-schema}

+++ Sommario

| Benvenuto in campagne orchestrate | Lanciare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](gs-orchestrated-campaigns.md)<br/><br/>Creazione e gestione di schemi e set di dati relazionali:</br> <ul><li>[Schema manuale](manual-schema.md)</li><li>[Schema di caricamento file](file-upload-schema.md)</li><li>[Acquisire dati](ingest-data.md)</li></ul>[Accedere e gestire campagne orchestrate](access-manage-orchestrated-campaigns.md)<br/><br/>[Passaggi chiave per creare una campagna orchestrata](gs-campaign-creation.md) | [Crea e pianifica la campagna](create-orchestrated-campaign.md)<br/><br/>[Orchestrazione attività](orchestrate-activities.md)<br/><br/>[Avvia e monitora la campagna](start-monitor-campaigns.md)<br/><br/>[Generazione rapporti](reporting-campaigns.md) | [Utilizzare il generatore di regole](orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](build-query.md)<br/><br/>[Modificare le espressioni](edit-expressions.md)<br/><br/>[Retargeting](retarget.md) | [Inizia a usare le attività](activities/about-activities.md)<br/><br/>Attività:<br/>[Partecipa e unisci](activities/and-join.md) - [Genera pubblico](activities/build-audience.md) - [Modifica dimensione](activities/change-dimension.md) - [Attività canale](activities/channels.md) - [Combina](activities/combine.md) - [Deduplicazione](activities/deduplication.md) - [Arricchimento](activities/enrichment.md) - [Fork](activities/fork.md) - [Riconciliazione](activities/reconciliation.md) - [Salva pubblico](activities/save-audience.md) - [Dividi](activities/split.md) - [Attendi](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

Il contenuto di questa pagina non è definitivo e potrebbe essere soggetto a modifiche.

>[!ENDSHADEBOX]

Definisci il modello di dati relazionali necessario per le campagne orchestrate creando schemi come **Iscrizioni fedeltà**, **Transazioni fedeltà** e **Premi fedeltà**. Ogni schema deve includere una chiave primaria, un attributo di controllo delle versioni e relazioni appropriate con entità di riferimento come **Destinatari** o **Marchi**.

Gli schemi possono essere creati manualmente tramite l’interfaccia o importati in blocco utilizzando un file DDL.

Questa sezione fornisce istruzioni dettagliate su come creare uno schema relazionale all’interno di Adobe Experience Platform caricando un file DDL (Data Definition Language). L&#39;utilizzo di un file DDL consente di definire in anticipo la struttura del modello dati, incluse tabelle, attributi, chiavi e relazioni.

## Carica un file DDL{#ddl-upload}

Caricando un file DDL, puoi definire in anticipo la struttura del modello dati, incluse tabelle, attributi, chiavi e relazioni.

1. Accedi a Adobe Experience Platform.

1. Passa a **Gestione dati** > **Schema**.

1. Fai clic su **Crea schema**.

1. Viene richiesto di selezionare due tipi di schema:

   * **Standard**
   * **Relazionale**, utilizzato in modo specifico per le campagne orchestrate

   ![](assets/admin_schema_1.png)

1. Selezionare **Carica file DDL** per definire un diagramma delle relazioni tra entità e creare schemi.

   La struttura della tabella deve contenere:
   * Almeno una chiave primaria
   * Identificatore di versione, ad esempio un campo `lastmodified` di tipo `datetime` o `number`.

1. Trascina il file DDL e fai clic su **[!UICONTROL Avanti]**.

1. Digita il tuo **[!UICONTROL nome schema]**.

1. Imposta ogni schema e le relative colonne, assicurandoti che sia specificata una chiave primaria.

   Un attributo, ad esempio `lastmodified`, deve essere designato come descrittore di versione. Questo attributo, in genere di tipo `datetime`, `long` o `int`, è essenziale per i processi di acquisizione affinché il set di dati venga aggiornato con la versione più recente.

   ![](assets/admin_schema_2.png)

1. Al termine, fai clic su **[!UICONTROL Fine]**.

Ora puoi verificare le definizioni della tabella e dei campi all’interno dell’area di lavoro. [Ulteriori informazioni nella sezione seguente](#entities)

## Definire le relazioni {#relationships}

Per definire connessioni logiche tra tabelle all’interno dello schema, segui la procedura riportata di seguito.

1. Accedi alla vista area di lavoro del modello dati e scegli le due tabelle da collegare

1. Fai clic sul pulsante ![](assets/do-not-localize/Smock_AddCircle_18_N.svg) accanto a Source Join, quindi trascina e guida la freccia verso Target Join per stabilire la connessione.

   ![](assets/admin_schema_5.png)

1. Compila il modulo specificato per definire il collegamento e fai clic su **Applica** una volta configurato.

   ![](assets/admin_schema_3.png)

   **Cardinalità**:

   * **1-N**: una occorrenza della tabella di origine può avere diverse occorrenze corrispondenti della tabella di destinazione, ma una occorrenza della tabella di destinazione può avere al massimo una occorrenza corrispondente della tabella di origine.

   * **N-1**: una occorrenza della tabella di destinazione può avere diverse occorrenze corrispondenti della tabella di origine, ma una occorrenza della tabella di origine può avere al massimo una occorrenza corrispondente della tabella di destinazione.

   * **1-1**: una occorrenza della tabella di origine può avere al massimo una occorrenza corrispondente della tabella di destinazione.

1. Tutti i collegamenti definiti nel modello dati sono rappresentati da frecce nella vista area di lavoro. Fai clic su una freccia tra due tabelle per visualizzare i dettagli, apportare modifiche o rimuovere il collegamento in base alle esigenze.

   ![](assets/admin_schema_6.png)

1. Utilizza la barra degli strumenti per personalizzare e regolare l’area di lavoro.

   ![](assets/toolbar.png)

   * **Zoom in**: ingrandisci l&#39;area di lavoro per visualizzare più chiaramente i dettagli del modello dati.

   * **Zoom indietro**: riduci le dimensioni dell&#39;area di lavoro per una visualizzazione più ampia del modello dati.

   * **Adatta visualizzazione**: regola lo zoom per adattarlo a tutti gli schemi all&#39;interno dell&#39;area visibile.

   * **Filtro**: scegliere lo schema da visualizzare nell&#39;area di lavoro.

   * **Forza layout automatico**: disponi automaticamente gli schemi per una migliore organizzazione.

   * **Visualizza mappa**: consente di attivare o disattivare la sovrapposizione minima per spostarsi più facilmente nei layout di schema complessi o di grandi dimensioni.

1. Al termine, fai clic su **Salva**. Questa azione crea gli schemi e i set di dati associati e abilita il set di dati da utilizzare nelle campagne orchestrate.

1. Fai clic su **[!UICONTROL Processi aperti]** per monitorare l&#39;avanzamento del processo di creazione. Questo processo può richiedere alcuni minuti, a seconda del numero di tabelle definite nel file DDL.

   ![](assets/admin_schema_4.png)

## Schema collegamento {#link-schema}

Stabilisci una relazione tra lo schema **transazioni fedeltà** e lo schema **Destinatari** per associare ogni transazione al record cliente corretto.

1. Passa a **[!UICONTROL Schemi]** e apri le **transazioni fedeltà** create in precedenza.

1. Fare clic su **[!UICONTROL Aggiungi relazione]** dalle proprietà del campo **[!UICONTROL Cliente]**.

   ![](assets/schema_1.png)

1. Selezionare **[!UICONTROL Many-to-One]** come relazione **[!UICONTROL Type]**.

1. Collegamento allo schema **Destinatari** esistente.

   ![](assets/schema_2.png)

1. Immetti un nome di relazione **[!UICONTROL dallo schema corrente]** e un nome di relazione **[!UICONTROL dallo schema di riferimento]**.

1. Fai clic su **[!UICONTROL Applica]** per salvare le modifiche.

Continua creando una relazione tra lo schema **premi fedeltà** e lo schema **Marchi** per associare ogni premio al marchio appropriato.

![](assets/schema_3.png)

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