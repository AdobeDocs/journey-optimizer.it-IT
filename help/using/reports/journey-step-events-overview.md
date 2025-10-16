---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare gli eventi dei passaggi del percorso
description: 'Scopri come utilizzare gli eventi dei passaggi di percorso in Adobe Journey Optimizer: cosa sono, perché sono importanti e come utilizzarli per l’analisi e l’ottimizzazione'
feature: Journeys, Reporting
topic: Content Management
role: Data Engineer, Data Architect, Admin, User
level: Intermediate, Experienced
keywords: percorso, eventi dei passaggi, analisi, reporting, monitoraggio, XDM
hide: true
hidefromtoc: true
exl-id: 9f8e7d6c-5b4a-3928-1756-849302a11c2b
source-git-commit: df3abb7da17eb21e5e4120b55bdeb61fec3e202d
workflow-type: tm+mt
source-wordcount: '875'
ht-degree: 1%

---

# Utilizzare gli eventi dei passaggi del percorso {#work-with-journey-step-events}

Gli eventi dei passaggi di percorso sono eventi generati automaticamente che acquisiscono informazioni dettagliate su ciascun passaggio che un profilo compie durante l’avanzamento in un percorso in Adobe Journey Optimizer. Questi eventi forniscono visibilità completa sulle prestazioni del percorso e abilitano potenti funzionalità di analisi.

## Cosa sono gli eventi delle fasi di percorso? {#what-are-step-events}

Gli eventi delle fasi di percorso sono eventi XDM (Experience Data Model) generati dal sistema che Adobe Journey Optimizer crea e invia automaticamente a Adobe Experience Platform ogni volta che un profilo si sposta da un nodo a un altro in un percorso. Ogni evento corrisponde a un’azione o a una transizione specifica nell’esperienza di percorso del cliente.

Esistono due tipi principali di eventi dei passaggi del percorso:

- **journeyStepEvent**: eventi relativi alla progressione di singoli profili attraverso passaggi del percorso
- **journeyStepProfileEvent**: eventi che includono informazioni aggiuntive sul contesto del profilo

### Cosa attiva gli eventi dei passaggi del percorso? {#event-triggers}

Gli eventi delle fasi del percorso vengono generati automaticamente per varie attività del percorso:

- **Eventi di ingresso**: quando un profilo entra in un percorso
- **Esecuzione dell&#39;azione**: quando vengono inviati messaggi o vengono eseguite azioni personalizzate
- **Valutazione delle condizioni**: quando i profili passano attraverso i punti decisionali
- **Attività di attesa**: quando i profili entrano ed escono dai nodi di attesa
- **Eventi di uscita**: quando i profili completano o escono da un percorso
- **Gestione degli errori**: quando si verificano errori durante l&#39;esecuzione del percorso

>[!NOTE]
>
>Gli eventi delle fasi di percorso vengono attivati per impostazione predefinita su tutte le istanze. Non è possibile modificare o aggiornare gli schemi e i set di dati creati durante il provisioning per gli eventi dei passaggi. Questi schemi e set di dati sono in modalità di sola lettura.

## Perché gli eventi dei passaggi di percorso contano {#why-step-events-matter}

Gli eventi delle fasi di percorso forniscono un valore critico per le organizzazioni che utilizzano Adobe Journey Optimizer:

### Analisi e monitoraggio in tempo reale {#real-time-analytics}

- **Monitoraggio delle prestazioni del Percorso**: monitora il flusso dei profili nei percorsi in tempo reale
- **Analisi della conversione**: comprendere i punti di riconversione e i percorsi di conversione riusciti
- **Rilevamento errori**: identifica e risolve i problemi non appena si verificano

### Integrazione dei dati e approfondimenti {#data-integration}

- **Analisi multipiattaforma**: combinare i dati di percorso con altre origini dati Adobe Experience Platform
- **Visualizzazione 360 del cliente**: creazione di profili cliente completi che includono interazioni di percorso
- **Modellazione attribuzione**: connettere i punti di contatto del percorso ai risultati di business a valle

### Opportunità di ottimizzazione {#optimization}

- **Informazioni sul test A/B**: analizza le prestazioni di diversi percorsi di percorso
- **Miglioramento Personalization**: utilizza i dati di comportamento del percorso per migliorare le esperienze future
- **Efficienza operativa**: identificazione dei colli di bottiglia e ottimizzazione della progettazione del percorso

## Come utilizzare gli eventi dei passaggi del percorso {#how-to-use-step-events}

### Accesso ai dati evento del passaggio del percorso {#accessing-data}

I dati dell’evento del passaggio di percorso vengono memorizzati automaticamente in Adobe Experience Platform e sono accessibili tramite:

1. **Query Data Lake**: utilizzare SQL per eseguire query sul set di dati `journey_step_events`
2. **Customer Journey Analytics**: Analizza i dati del percorso tramite strumenti di analisi avanzati
3. **Rapporti in tempo reale**: accesso ai dati tramite le funzionalità di reporting integrate di Journey Optimizer
4. **API**: accesso programmatico ai dati evento per le applicazioni personalizzate

### Punti dati chiave disponibili {#key-data-points}

Gli eventi delle fasi del percorso acquisiscono informazioni complete, tra cui:

- **Identificazione Percorso**: ID Percorso, versione e nome
- **Informazioni sul profilo**: ID profilo e identità associate
- **Dettagli del passaggio**: nome del nodo, tipo di passaggio e stato di esecuzione
- **Marca temporale**: tempistica precisa di ogni passaggio del percorso
- **Risultati azione**: stato di operazione/errore e dettagli di esecuzione
- **Informazioni sull&#39;errore**: codici di errore dettagliati e descrizioni in caso di problemi

### Casi d’uso comuni {#common-use-cases}

**Monitoraggio delle prestazioni**

```sql
-- Example: Count profiles entering a journey in the last 24 hours
SELECT count(distinct _experience.journeyOrchestration.stepEvents.profileID)
FROM journey_step_events 
WHERE _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-id>'
AND _experience.journeyOrchestration.stepEvents.nodeType='start'
AND DATE(timestamp) > (now() - interval '24' hour);
```

**Analisi degli errori**

```sql
-- Example: Identify errors by journey node
SELECT _experience.journeyOrchestration.stepEvents.nodeName,
       count(distinct _experience.journeyOrchestration.stepEvents.profileID)
FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.actionExecutionError IS NOT NULL
GROUP BY _experience.journeyOrchestration.stepEvents.nodeName;
```

**Analisi funnel di Percorso**

- Tieni traccia dei tassi di conversione a ogni passaggio del percorso
- Identifica dove i profili escono più comunemente dal percorso
- Misura il tempo trascorso in diverse fasi del percorso

## Esempi e risorse {#samples-resources}

### Esempi e modelli di query {#query-examples}

Esplora esempi di query completi per l’analisi degli eventi delle fasi di percorso comuni:

- **[Esempi di query evento del passaggio del Percorso](query-examples.md)**: query SQL pronte all&#39;uso per scenari di analisi comuni
- **[Esempi di query del set di dati](../data/datasets-query-examples.md#journey-step-event)**: esempi di query sui set di dati evento del passaggio di percorso
- **[Query basate su profili](query-examples.md#profile-based-queries)**: tenere traccia di singoli percorsi di profili e interazioni

### Documentazione sul campo {#field-documentation}

Comprendere la struttura completa dei dati degli eventi dei passaggi del percorso:

- **[Elenco campi evento passaggio di Percorso](sharing-field-list.md)**: riferimento completo di tutti i campi disponibili
- **[Campi comuni](sharing-common-fields.md)**: campi condivisi tra journeyStepEvent e journeyStepProfileEvent
- **[Campi di esecuzione azione](sharing-execution-fields.md)**: campi specifici del tracciamento dell&#39;esecuzione delle azioni
- **[Campi Percorso](sharing-journey-fields.md)**: metadati e identificatori specifici del Percorso

### Best practice e risoluzione dei problemi {#best-practices}

**Ottimizzazione delle prestazioni**

- Utilizza `journeyVersionID` invece di `journeyVersionName` per migliorare le prestazioni delle query
- Filtra per intervalli di date per migliorare la velocità delle query su set di dati di grandi dimensioni
- Sfruttare le identità di profilo corrispondenti alla configurazione dello spazio dei nomi del percorso

**Qualità dei dati**

- Monitora regolarmente [eventi eliminati](sharing-field-list.md#discarded-events) per identificare i problemi relativi ai dati
- Convalidare che gli schemi evento soddisfino i requisiti di analisi
- Implementare la corretta gestione degli errori nelle query personalizzate

**Strategie di Analytics**

- Combina eventi delle fasi del percorso con i dati di feedback del messaggio per un’attribuzione completa
- Utilizzare l&#39;analisi basata sul tempo per comprendere la velocità del percorso e i colli di bottiglia
- Creazione di analisi per coorte per confrontare diverse varianti di percorso

### Funzionalità di analisi avanzate {#advanced-analytics}

**Integrazione Customer Journey Analytics**
Gli eventi dei passaggi di percorso possono essere analizzati utilizzando Customer Journey Analytics per:

- Modellazione di attribuzione avanzata
- Visualizzazione percorso cross-channel
- Analisi predittive sui risultati di percorso

**Decisioning in tempo reale**
Utilizza i pattern di evento del passaggio di percorso per:

- Attivare la personalizzazione in tempo reale
- Implementare l&#39;ottimizzazione dinamica del percorso
- Abilitare i consigli contestuali sulle azioni migliori successive

## Risorse aggiuntive {#additional-resources}

### Collegamenti alla documentazione {#documentation-links}

- **[Panoramica sulla condivisione dei passaggi di Percorso](sharing-overview.md)**: informazioni sul flusso dei dati di percorso in Adobe Experience Platform
- **[Dizionario schemi incorporato](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=it)**: riferimento schema XDM completo
- **[Rapporti di Journey Optimizer](report-gs-cja.md)**: panoramica delle funzionalità di reporting in Journey Optimizer

### Guide all’integrazione {#integration-guides}

- **[Adobe Customer Journey Analytics](cja-ajo.md)**: analisi dei dati di Journey Optimizer in CJA
- **[Gestione dati](../data/export-datasets.md)**: esportazione e gestione dei dati di percorso
- **[Privacy e governance](../privacy/audit-logs.md)**: considerazioni sulla governance dei dati per gli eventi di percorso

Gli eventi dei passaggi di percorso costituiscono la base di analisi avanzate dei percorsi in Adobe Journey Optimizer. Grazie alla comprensione e all’utilizzo efficace di questi eventi, puoi acquisire informazioni approfondite sul comportamento dei clienti, ottimizzare le prestazioni del percorso e creare esperienze più personalizzate per i clienti.
