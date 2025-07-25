---
solution: Journey Optimizer
product: journey optimizer
title: Passaggi di configurazione
description: Scopri come creare uno schema relazionale in Adobe Experience Platform caricando una DDL
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 88eb1438-0fe5-4a19-bfb6-2968a427e9e8
source-git-commit: 6447f5d1a060037c0ceaa374db20966097585f9c
workflow-type: tm+mt
source-wordcount: '1101'
ht-degree: 58%

---

# Creare schemi relazionali utilizzando un file DDL {#file-upload-schema}

+++ Sommario

| Ti diamo il benvenuto nelle campagne orchestrate | Avviare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](gs-orchestrated-campaigns.md)<br/><br/>Creazione e gestione di schemi e set di dati relazionali:</br> <ul><li>[Introduzione a schemi e set di dati](gs-schemas.md)</li><li>[Schema manuale](manual-schema.md)</li><li>[Schema di caricamento file](file-upload-schema.md)</li><li>[Acquisire dati](ingest-data.md)</li></ul>[Accedere e gestire campagne orchestrate](access-manage-orchestrated-campaigns.md)<br/><br/>[Passaggi chiave per creare una campagna orchestrata](gs-campaign-creation.md) | [Creare e pianificare la campagna](create-orchestrated-campaign.md)<br/><br/>[Orchestrare le attività](orchestrate-activities.md)<br/><br/>[Avviare e monitorare la campagna](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | [Utilizzare il generatore di regole](orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](build-query.md)<br/><br/>[Modificare le espressioni](edit-expressions.md)<br/><br/>[Retargeting](retarget.md) | [Introduzione alle attività](activities/about-activities.md)<br/><br/>Attività:<br/>[AND-join](activities/and-join.md) - [Crea pubblico](activities/build-audience.md) - [Modifica dimensione](activities/change-dimension.md) - [Attività canale](activities/channels.md) - [Combina](activities/combine.md) - [Deduplica](activities/deduplication.md) - [Arricchimento](activities/enrichment.md) - [Fork](activities/fork.md) - [Riconciliazione](activities/reconciliation.md) - [Salva pubblico](activities/save-audience.md) - [Dividi](activities/split.md) - [Attendi](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

</br>

Il contenuto di questa pagina non è definitivo e potrebbe essere soggetto a modifiche.

>[!ENDSHADEBOX]

Definisci il modello di dati relazionali necessario per le campagne orchestrate creando schemi come **Iscrizioni fedeltà**, **Transazioni fedeltà** e **Premi fedeltà**. Ogni schema deve includere una chiave primaria, un attributo di controllo delle versioni e relazioni appropriate con entità di riferimento quali **Destinatari** o **Marchi**.

Gli schemi possono essere creati manualmente tramite l’interfaccia o importati in blocco utilizzando un file DDL.

Questa sezione fornisce istruzioni dettagliate su come creare uno schema relazionale all’interno di Adobe Experience Platform caricando un file DDL (Data Definition Language). L’utilizzo di un file DDL consente di definire in anticipo la struttura del modello dati, incluse tabelle, attributi, chiavi e relazioni.

1. [Carica un file DDL](#ddl-upload) per creare schemi relazionali e definirne la struttura.

1. [Definisci le relazioni](#relationships) tra le tabelle nel modello dati.

1. [Collega schemi](#link-schema) per collegare i dati relazionali con entità profilo esistenti, ad esempio Destinatari o Marchi.

1. [Acquisisci dati](ingest-data.md) nel set di dati da origini supportate.

## Carica un file DDL{#ddl-upload}

Caricando un file DDL, puoi definire in anticipo la struttura del modello dati, incluse tabelle, attributi, chiavi e relazioni.

Sono supportati i caricamenti di file di schema basati su Excel. Scarica il [modello fornito](assets/template.zip) per preparare facilmente le definizioni dello schema.

+++Le seguenti funzioni sono supportate durante la creazione di schemi relazionali in Adobe Experience Platform

* **ENUM**\
  I campi ENUM sono supportati sia nella creazione manuale dello schema basata su DDL, che consente di definire gli attributi con un set fisso di valori consentiti.

* **Etichetta schema per governance dei dati**\
  L’etichettatura è supportata a livello di campo dello schema per applicare i criteri di governance dei dati, ad esempio il controllo degli accessi e le restrizioni di utilizzo. Per ulteriori dettagli, consulta [Documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it).

* **Chiave composita**\
  Le chiavi primarie composite sono supportate nelle definizioni degli schemi relazionali, consentendo l’utilizzo di più campi insieme per identificare in modo univoco i record.

+++

1. Accedi a Adobe Experience Platform.

1. Passa al menu **Gestione dati** > **Schema**.

1. Fare clic su **Crea schema**.

1. Seleziona **[!UICONTROL Relazionale]** come **tipo di schema**.

   ![](assets/admin_schema_1.png)

1. Seleziona **[!UICONTROL Carica un file DDL]** per definire un diagramma di relazioni tra entità e creare gli schemi

   La struttura della tabella deve contenere:
   * Almeno una chiave primaria
   * Un identificatore di versione, ad esempio un campo `lastmodified` di tipo `datetime` o `number`.
   * Per l&#39;acquisizione Change Data Capture (CDC), una colonna speciale denominata `_change_request_type` di tipo `String` che indica il tipo di modifica dei dati (ad esempio, inserimento, aggiornamento, eliminazione) e abilita l&#39;elaborazione incrementale


   >[!IMPORTANT]
   >
   > Qualsiasi schema utilizzato per il targeting deve includere almeno un campo di identità di tipo `String` con un **spazio dei nomi identità** associato.\
   >Questo garantisce la compatibilità con le funzionalità di targeting e risoluzione delle identità di Adobe Journey Optimizer.

1. Trascina il file DDL e fai clic su **[!UICONTROL Avanti]**.

   La dimensione massima supportata per un file DDL è 10 MB.

1. Digita il **[!UICONTROL nome dello schema]**.

1. Imposta ogni schema e le relative colonne, assicurandoti che sia specificata una chiave primaria.

   Un attributo, ad esempio `lastmodified`, deve essere designato come descrittore di versione. Questo attributo, in genere di tipo `datetime`, `long` o `int`, è essenziale per i processi di acquisizione affinché il set di dati venga aggiornato con la versione più recente.

   ![](assets/admin_schema_2.png)

1. Al termine, fai clic su **[!UICONTROL Fine]**.

Ora puoi verificare le definizioni della tabella e dei campi all’interno dell’area di lavoro. [Ulteriori informazioni sono disponibili nella sezione qui sotto](#entities)

## Definire le relazioni {#relationships}

Per definire connessioni logiche tra tabelle all’interno dello schema, segui i passaggi seguenti.

1. Accedi alla vista area di lavoro del modello dati e scegli le due tabelle da collegare

1. Fai clic sul pulsante ![](assets/do-not-localize/Smock_AddCircle_18_N.svg) accanto a Join di origine, quindi trascina e guida la freccia verso Join di destinazione per stabilire la connessione.

   ![](assets/admin_schema_5.png)

1. Compila il modulo specificato per definire il collegamento e, una volta configurato, fai clic su **Applica**.

   ![](assets/admin_schema_3.png)

   **Cardinalità**:

   * **1-N**: un’occorrenza della tabella di origine può avere diverse occorrenze corrispondenti della tabella target, ma un’occorrenza della tabella target può avere al massimo un’occorrenza corrispondente della tabella di origine.

   * **N-1**: un’occorrenza della tabella di origine può avere diverse occorrenze corrispondenti della tabella target, ma un’occorrenza della tabella target può avere al massimo un’occorrenza corrispondente della tabella di origine.

   * **1-1**: un’occorrenza della tabella di origine può avere al massimo un’occorrenza corrispondente della tabella target.

1. Tutti i collegamenti definiti nel modello dati sono rappresentati da frecce nella vista area di lavoro. Fai clic su una freccia tra due tabelle per visualizzare i dettagli, apportare modifiche o rimuovere il collegamento in base alle esigenze.

   ![](assets/admin_schema_6.png)

1. Utilizza la barra degli strumenti per personalizzare e regolare l’area di lavoro.

   ![](assets/toolbar.png)

   * **Ingrandisci**: ingrandisci l’area di lavoro per visualizzare più chiaramente i dettagli del modello dati.

   * **Riduci**: riduci le dimensioni dell’area di lavoro per una visualizzazione più ampia del modello dati.

   * **Adatta vista**: regola lo zoom per adattarlo a tutti gli schemi all’interno dell’area visibile.

   * **Filtro**: scegli lo schema da visualizzare nell’area di lavoro.

   * **Forza layout automatico**: disponi automaticamente gli schemi per una migliore organizzazione.

   * **Visualizza mappa**: consente di attivare o disattivare la sovrapposizione minima per spostarsi più facilmente nei layout di schema complessi o di grandi dimensioni.

1. Al termine, fai clic su **Salva**. Questa azione crea gli schemi e i set di dati associati e abilita il set di dati da utilizzare nelle campagne orchestrate.

1. Fai clic su **[!UICONTROL Processi aperti]** per monitorare l’avanzamento del processo di creazione. Questo processo può richiedere alcuni minuti, a seconda del numero di tabelle definite nel file DDL.

   Puoi accedere ai tuoi processi relazionali anche aprendo la finestra **[!UICONTROL Carica file DDL]** e selezionando **[!UICONTROL Visualizza tutti i processi relazionali]**.

   ![](assets/admin_schema_4.png)

## Collegare gli schemi {#link-schema}

>[!IMPORTANT]
>
> Solo le relazioni definite in modo esplicito all&#39;interno del file DDL vengono riconosciute dal sistema. Tutte le relazioni di entità esistenti al di fuori del file DDL verranno ignorate e non elaborate.

Stabilisci una relazione tra lo schema **transazioni fedeltà** e lo schema **Destinatari** per associare ogni transazione al record cliente corretto.

1. Passa a **[!UICONTROL Schemi]** e apri le **transazioni fedeltà** create in precedenza.

1. Fai clic su **[!UICONTROL Aggiungi relazione]** dalle proprietà del campo **[!UICONTROL Cliente]**.

   ![](assets/schema_1.png)

1. Seleziona **[!UICONTROL Molti a uno]** come **[!UICONTROL Tipo]** di relazione.

1. Collega allo schema **Destinatari** esistente.

   ![](assets/schema_2.png)

1. Immetti un **[!UICONTROL nome di relazione dallo schema corrente]** e un nome di **[!UICONTROL relazione dallo schema di riferimento]**.

1. Fai clic su **[!UICONTROL Applica]** per salvare le modifiche.

Continua creando una relazione tra lo schema **premi fedeltà** e lo schema **Brand** per associare ogni premio al brand appropriato.

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
