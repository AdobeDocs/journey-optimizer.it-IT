---
solution: Journey Optimizer
product: journey optimizer
title: Guardrail e limitazioni delle campagne orchestrate
description: Scopri le limitazioni e i guardrail delle campagne orchestrate
hide: true
hidefromtoc: true
exl-id: 82744db7-7358-4cc6-a9dd-03001759fef7
source-git-commit: 2ad659b391515c193418325c34a9dd56133b90d6
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 2%

---

# Guardrail e limitazioni {#guardrails}

+++ Sommario

| Benvenuto in campagne orchestrate | Lanciare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](gs-orchestrated-campaigns.md)<br/><br/>Creazione e gestione di schemi e set di dati relazionali:</br> <ul><li>[Introduzione a schemi e set di dati](gs-schemas.md)</li><li>[Schema manuale](manual-schema.md)</li><li>[Schema di caricamento file](file-upload-schema.md)</li><li>[Acquisire dati](ingest-data.md)</li></ul>[Accedere e gestire campagne orchestrate](access-manage-orchestrated-campaigns.md)<br/><br/>[Passaggi chiave per creare una campagna orchestrata](gs-campaign-creation.md) | [Crea e pianifica la campagna](create-orchestrated-campaign.md)<br/><br/>[Orchestrazione attività](orchestrate-activities.md)<br/><br/>[Avvia e monitora la campagna](start-monitor-campaigns.md)<br/><br/>[Generazione rapporti](reporting-campaigns.md) | [Utilizzare il generatore di regole](orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](build-query.md)<br/><br/>[Modificare le espressioni](edit-expressions.md)<br/><br/>[Retargeting](retarget.md) | [Inizia a usare le attività](activities/about-activities.md)<br/><br/>Attività:<br/>[Partecipa e unisci](activities/and-join.md) - [Genera pubblico](activities/build-audience.md) - [Modifica dimensione](activities/change-dimension.md) - [Attività canale](activities/channels.md) - [Combina](activities/combine.md) - [Deduplicazione](activities/deduplication.md) - [Arricchimento](activities/enrichment.md) - [Fork](activities/fork.md) - [Riconciliazione](activities/reconciliation.md) - [Salva pubblico](activities/save-audience.md) - [Dividi](activities/split.md) - [Attendi](activities/wait.md) |

{style="table-layout:fixed"}

+++

## Limitazioni del flusso di dati rispetto al set di dati

Ogni set di dati in Adobe Experience Platform può essere associato a un solo flusso di dati attivo alla volta. Questa cardinalità 1:1 è rigorosamente applicata dalla piattaforma.

Se devi cambiare origine dati (ad esempio, da Amazon S3 a Salesforce):

Devi eliminare il flusso di dati esistente connesso al set di dati.

Quindi, crea un nuovo flusso di dati con la nuova origine mappata sullo stesso set di dati.

Questo garantisce l’acquisizione affidabile dei dati ed è essenziale quando si utilizza Change Data Capture (CDC), che dipende da una chiave primaria definita e da un attributo di controllo delle versioni (ad esempio, lastmodified) per gli aggiornamenti incrementali.


## Schemi relazionali/limitazioni dell’acquisizione dei dati

* Nell’archivio dati relazionale sono supportati fino a 200 schemi (tabelle) relazionali.

* La dimensione totale di uno schema relazionale utilizzato per l’orchestrazione delle campagne non deve superare i 100 GB.

* L’acquisizione in batch per l’orchestrazione delle campagne deve avvenire non più di una volta ogni 15 minuti.

* Le modifiche giornaliere a uno schema relazionale devono rimanere inferiori al 20% del conteggio totale dei record.

## Modellazione dati

* Il descrittore di versione è obbligatorio in tutti gli schemi, incluse le tabelle dei fatti.

* Per ogni tabella è necessaria una chiave primaria.

* Il nome_tabella assegnato durante la creazione del set di dati viene utilizzato nell’interfaccia utente di segmentazione e nelle funzioni di personalizzazione.

  Questo nome è permanente e non può essere modificato dopo la creazione.

* I gruppi di campi non sono attualmente supportati.

## Acquisizione dei dati

* È necessaria l’acquisizione di dati di profilo + relazionali.

* Per l’acquisizione basata su file è necessario un campo del tipo di modifica, mentre per l’acquisizione Cloud DB deve essere abilitata la registrazione delle tabelle. Questa operazione è necessaria per Change Data Capture (CDC).

* La latenza dall’acquisizione alla disponibilità dei dati in Snowflake varia da 15 minuti a 2 ore, a seconda del volume dei dati, della concorrenza e del tipo di operazioni (gli inserimenti sono più veloci degli aggiornamenti).

* Il monitoraggio dei dati in Snowflake è in fase di sviluppo; al momento, non esiste alcuna conferma nativa per la corretta acquisizione.

* Gli aggiornamenti diretti a Snowflake o al set di dati non sono supportati. Tutte le modifiche devono passare attraverso le origini CDC.

  Il servizio query è di sola lettura.

* ETL non è supportato: i clienti devono fornire i dati nel formato richiesto.

* Non sono consentiti aggiornamenti parziali. Ogni riga deve essere fornita come record completo.

* L’acquisizione si basa su Query Service e Data Distiller.

## Segmentazione

* L’elenco di valori e le enumerazioni sono attualmente disponibili.

* I tipi di pubblico salvati sono elenchi statici e il loro contenuto riflette i dati disponibili al momento dell’esecuzione della campagna.

* L&#39;aggiunta a un pubblico salvato non è supportata. Gli aggiornamenti richiedono una sovrascrittura completa.

* I tipi di pubblico devono essere costituiti solo da attributi scalari; mappe e array non sono supportati.

* La segmentazione supporta principalmente i dati relazionali. Anche se è consentito combinare dati di profilo, l’inserimento di set di dati di profilo di grandi dimensioni può influire sulle prestazioni. Per evitare questo problema:

* Sono attivati dei guardrail, ad esempio per limitare il numero di attributi di profilo selezionati in batch o per tipi di pubblico in streaming.

* I tipi di pubblico di lettura non sono memorizzati in cache - ogni esecuzione di una campagna attiva una lettura completa.

  L’ottimizzazione è necessaria per tipi di pubblico grandi o complessi.