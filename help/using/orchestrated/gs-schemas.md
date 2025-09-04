---
solution: Journey Optimizer
product: journey optimizer
title: Passaggi di configurazione
description: Scopri come creare uno schema relazionale in Adobe Experience Platform caricando una DDL
exl-id: 327597f6-8a53-42dc-966a-baae49b58bb3
version: Campaign Orchestration
source-git-commit: 07ec28f7d64296bdc2020a77f50c49fa92074a83
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 31%

---


# Introduzione a schemi e set di dati relazionali{#gs-schemas}

Questa guida illustra i passaggi necessari per creare uno schema relazionale, configurare un set di dati per le campagne orchestrate e acquisire i dati.

![](assets/do-not-localize/schema_admin.png)

Un set di dati è un costrutto di archiviazione e gestione per una raccolta di dati, in genere una tabella, che contiene uno schema (colonne) e dei campi (righe). I dati acquisiti correttamente in Experience Platform vengono memorizzati nel data lake come set di dati.

Uno schema rappresenta e convalida la struttura e il formato dei dati. Fornisce una definizione astratta di un oggetto reale (come una persona) e delinea quali dati devono essere inclusi in ogni istanza di tale oggetto (come nome, data di nascita e così via).


1. Crea [schema relazionale manualmente](manual-schema.md) o [utilizzando un file DDL](file-upload-schema.md)

   Definisci la struttura del modello dati, incluse tabelle, attributi e relazioni. Scegli se creare lo schema manualmente nell&#39;interfaccia utente o caricare un file DDL per velocizzare l&#39;installazione.

   Quando crei manualmente lo schema, anche il set di dati deve essere creato e abilitato manualmente. Quando si utilizza un file DDL, la creazione e l’abilitazione dei set di dati sono automatiche.

1. [Collegare lo schema](file-upload-schema.md)

   Stabilisci relazioni tra gli schemi per garantire la coerenza dei dati e abilitare query tra più entità. Ad esempio, puoi collegare le transazioni di fidelizzazione a destinatari o premi a marchi.

1. [Acquisire i dati](ingest-data.md)

   Importa dati in Adobe Experience Platform da origini supportate come SFTP, archiviazione cloud o database.

