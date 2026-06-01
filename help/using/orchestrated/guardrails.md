---
solution: Journey Optimizer
product: journey optimizer
title: Guardrail e limitazioni delle campagne orchestrate
description: Scopri le limitazioni e i guardrail delle campagne orchestrate
exl-id: 82744db7-7358-4cc6-a9dd-03001759fef7
version: Campaign Orchestration
TQID: https://experienceleague.adobe.com/ViPJaOPo-AT-naQqq-PaPw-BI5YupYuYAEy56AUEp2A
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
topic_v2:
  - id: b23e006f-0a29-4f1d-8fd0-77aa56f3d12b
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2:
  - id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
source-git-commit: 18f6b23dbbe53e486e5af76ef7cc61fa1784475d
workflow-type: tm+mt
source-wordcount: 734
ht-degree: 2%

---

# Guardrail e limitazioni {#guardrails}

Di seguito sono riportati i guardrail e le limitazioni relativi all’utilizzo delle campagne orchestrate.

## Limitazioni del flusso di dati

### Progettazione e archiviazione dei dati

* **Numero massimo di tabelle** - L&#39;archivio dati relazionale supporta un massimo di 200 tabelle (schemi).

* **Dimensione schema** - Per le campagne orchestrate, la dimensione totale di ogni singolo schema non deve superare i 100 GB.

* **Volume di aggiornamento giornaliero** - Gli aggiornamenti giornalieri a uno schema devono essere limitati a meno del 20% del numero totale di record per mantenere le prestazioni e la stabilità.

* **Modello dati relazionale** - I dati relazionali sono il modello principale supportato per i casi di utilizzo di acquisizione, modellazione dati e segmentazione.

* **Campo di identità** - Gli schemi utilizzati per il targeting devono contenere almeno un campo di identità di tipo `String`, mappato a uno spazio dei nomi di identità definito.

* **Attributi per schema** - Il numero medio di attributi per schema non deve superare le 50 colonne per mantenere la gestibilità e le prestazioni.

* **Abilitazione dei profili** - Gli schemi relazionali non possono essere abilitati per i profili Adobe Experience Platform. Per i profili Adobe Experience Platform sono supportati solo gli schemi XDM standard. Gli schemi relazionali possono essere abilitati per campagne orchestrate o campagne di azione. [Ulteriori informazioni](https://experienceleague.adobe.com/it/docs/experience-platform/catalog/datasets/user-guide#enable-profile)

### Acquisizione dei dati {#data-ingestion}

* **Acquisizione profilo e relazionale** - È richiesta l&#39;acquisizione di dati profilo + relazionali.

* **Cambia origini di acquisizione dati** - L&#39;acquisizione deve essere eseguita tramite Cambia origini di acquisizione dati:

   * **Origini basate su file** - Il campo `_change_request_type` è obbligatorio. I valori supportati sono `u` (upsert) o `d` (delete). Questi valori devono essere minuscoli `u` e `d`, non maiuscoli `U` e `D`.

   * **Origini basate su cloud** - La registrazione delle tabelle deve essere abilitata.

* **Solo record completi** - Non sono consentiti aggiornamenti di record parziali. Ogni riga deve essere fornita come record completo.

* **Frequenza di acquisizione batch** - L&#39;acquisizione batch per l&#39;orchestrazione delle campagne è limitata a una volta ogni 15 minuti.

* **Latenza di acquisizione** - La latenza di acquisizione nell&#39;archivio relazionale varia in genere da 15 minuti a 2 ore, a seconda di:

   * Volume dati

   * Concorrenza del sistema

   * Tipo di operazione (ad esempio, gli inserti sono più veloci degli aggiornamenti)

* **Flusso di dati per relazione set di dati** - Il flusso di dati per la relazione set di dati è 1-1. Una sola origine può alimentare un set di dati alla volta. Per cambiare l’origine, elimina il flusso di dati esistente e crea un nuovo flusso di dati con la nuova origine.

### Modellazione dati

* **Descrittore versione** - Tutti gli schemi, incluse le tabelle dei fatti, devono includere un descrittore di versione per garantire il controllo della versione e la tracciabilità corretti.

* **Chiave primaria** - Ogni tabella deve avere una chiave primaria definita per supportare l&#39;integrità dei dati e le operazioni a valle.

* **Nome tabella permanente** - L&#39;elemento `table_name` assegnato durante la creazione del set di dati è permanente e viene utilizzato nelle funzioni di segmentazione e personalizzazione.

* **Gruppi di campi** - I gruppi di campi non sono supportati nel framework di modellazione dati corrente.

* **Chiavi primarie composite** - Al momento non è disponibile il supporto per le chiavi primarie composite con flussi di caricamento file.

## Limitazioni delle attività {#activities-limitations}

* **Limite attività canale** - Una campagna orchestrata supporta un massimo di 10 attività canale (e-mail, SMS, push o direct mail). Per questo limite vengono conteggiate solo le attività del canale. Le attività di targeting e controllo del flusso non vengono conteggiate (ad esempio, Genera pubblico, Attendi, Dividi, Arricchimento, Riconciliazione, Fork, Fine o Test).

  Se si supera il limite durante il salvataggio o la pubblicazione, l’operazione non riesce. Per non superare il limite, riduci il numero di attività del canale o la consegna dei messaggi suddivisi tra più campagne orchestrate.

* **Limite attività area di lavoro** - Il numero di attività in un&#39;area di lavoro della campagna orchestrata è limitato a 500. Questo limite si applica a tutti i tipi di attività nell’area di lavoro. È separato dal limite delle attività del canale applicato alla pubblicazione. Per garantire prestazioni e manutenibilità, riduci in pratica i flussi di lavoro a 100 attività.

* **Solo attributi scalari**: nelle definizioni del pubblico sono supportati solo attributi scalari; mappe e array non sono consentiti.

* **Dati relazionali per la segmentazione** - Le attività di segmentazione si basano principalmente su dati relazionali. Anche se i dati di profilo possono essere inclusi, l’utilizzo di set di dati di profilo di grandi dimensioni può influire sulle prestazioni.

* **Limiti degli attributi di profilo** - Vengono applicati limiti al numero di attributi di profilo che possono essere utilizzati sia nel pubblico in batch che in quello in streaming per mantenere l&#39;efficienza del sistema.

* **Enumerazioni** - Le enumerazioni sono completamente supportate.

* **Tipi di pubblico di lettura non memorizzati in cache** - I tipi di pubblico di lettura non sono memorizzati in cache; ogni esecuzione della campagna attiva una valutazione completa del pubblico dai dati sottostanti.

* **Ottimizzazione del pubblico**: si consiglia vivamente di ottimizzare l&#39;utilizzo di definizioni di pubblico complesse o di grandi dimensioni per garantire le prestazioni.

* **I tipi di pubblico salvati sono statici**. Le attività dei tipi di pubblico salvati sono statiche e riflettono i dati disponibili al momento dell&#39;esecuzione della campagna.

* **Nessuna aggiunta al pubblico salvato** - L&#39;aggiunta a un&#39;attività Pubblico salvato non è supportata. Qualsiasi modifica richiede la completa sovrascrittura del pubblico.

## Limitazioni del canale

Nelle campagne orchestrate sono supportati solo i canali SMS, push, e-mail e direct mail.
