---
solution: Journey Optimizer
product: journey optimizer
title: Guardrail e limitazioni delle campagne orchestrate
description: Scopri le limitazioni e i guardrail delle campagne orchestrate
exl-id: 82744db7-7358-4cc6-a9dd-03001759fef7
version: Campaign Orchestration
source-git-commit: a9b790bc833b5819862bf2f3284968d81f595f28
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 1%

---


# Guardrail e limitazioni {#guardrails}

Di seguito sono riportati i guardrail e le limitazioni relativi all’utilizzo delle campagne orchestrate.

## Limitazioni del flusso di dati

### Progettazione e archiviazione dei dati

* L&#39;archivio dati relazionale supporta un massimo di **200 tabelle** (schemi).

* Per le campagne orchestrate, la dimensione totale di ogni singolo schema **non deve superare i 100 GB**.

* Gli aggiornamenti giornalieri a uno schema devono essere **limitati a meno del 20%** del numero totale di record per mantenere prestazioni e stabilità.

* I dati relazionali sono il modello principale supportato per i casi di utilizzo di acquisizione, modellazione di dati e segmentazione.

* Gli schemi utilizzati per il targeting devono contenere almeno **un campo di identità di tipo`String`**, mappato a uno spazio dei nomi di identità definito.

* Il numero medio di attributi per schema **non deve superare le 50 colonne** per mantenere la gestibilità e le prestazioni.

* Impossibile abilitare gli schemi basati su modelli per i **profili** di Adobe Experience Platform. Solo gli schemi XDM standard sono supportati per i **profili** di Adobe Experience Platform. Gli schemi basati su modelli possono essere abilitati per le campagne orchestrate o le campagne d’azione. [Ulteriori informazioni](https://experienceleague.adobe.com/it/docs/experience-platform/catalog/datasets/user-guide#enable-profile)

### Acquisizione dati

* È necessaria l’acquisizione di dati di profilo + relazionali.

* Tutte le acquisizioni devono avvenire tramite **Cambia origine dati**:

   * Per **Basato su file**: il campo `_change_request_type` è obbligatorio. I valori supportati sono `U` (upsert) o `D` (delete).

   * Per **basato su cloud**: la registrazione della tabella deve essere abilitata.

* **Non sono consentiti aggiornamenti di record parziali**. Ogni riga deve essere fornita come record completo.

* L&#39;acquisizione in batch per l&#39;orchestrazione delle campagne è limitata a **una volta ogni 15 minuti**.

* La latenza di acquisizione, nell&#39;archivio relazionale, varia in genere da **15 minuti a 2 ore**, a seconda di:

   * Volume dati

   * Concorrenza del sistema

   * Tipo di operazione. Ad esempio, gli inserti sono più veloci degli aggiornamenti

* **La relazione tra flusso di dati e set di dati è 1-1**. Ciò significa che una sola origine può alimentare un set di dati alla volta. Per cambiare l’origine, è necessario eliminare il flusso di dati esistente e creare un nuovo flusso di dati con la nuova origine.

### Modellazione dati

* Tutti gli schemi, incluse le tabelle dei fatti, devono includere **un descrittore di versione** per garantire il controllo della versione e la tracciabilità corretti.

* Ogni tabella deve avere una **chiave primaria** definita per supportare l&#39;integrità dei dati e le operazioni a valle.

* I `table_name` assegnati durante la creazione del set di dati sono permanenti e vengono utilizzati durante tutte le funzioni di segmentazione e personalizzazione.

* **I gruppi di campi non sono supportati** nel framework di modellazione dati corrente.

* Al momento non è disponibile il supporto per le chiavi primarie composite con flussi di caricamento file.

## Limitazioni delle attività

* Nelle definizioni del pubblico sono supportati solo **attributi scalari**; **mappe e array non sono consentiti**.

* **Le attività di segmentazione si basano principalmente su dati relazionali**. Anche se i dati di profilo possono essere inclusi, l’utilizzo di set di dati di profilo di grandi dimensioni può influire sulle prestazioni.

* **Sono applicati limiti al numero di attributi di profilo** che possono essere utilizzati sia nel pubblico in batch che in quello in streaming per mantenere l&#39;efficienza del sistema.

* **Le enumerazioni** sono completamente supportate.

* **I tipi di pubblico di lettura non sono memorizzati in cache**. Ogni esecuzione della campagna attiva una valutazione completa del pubblico dai dati sottostanti.

* **L&#39;ottimizzazione è fortemente consigliata** quando si lavora con definizioni di pubblico complesse o di grandi dimensioni per garantire le prestazioni.

* **Le attività dei tipi di pubblico salvati sono statiche** e riflettono i dati disponibili al momento dell&#39;esecuzione della campagna.

* **Aggiunta a un&#39;attività Pubblico salvato non supportata**. Qualsiasi modifica richiede la completa sovrascrittura del pubblico.

## Limitazioni del canale

Nelle campagne orchestrate sono supportati solo i canali SMS, push ed e-mail.
