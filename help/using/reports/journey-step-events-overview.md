---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare gli eventi dei passaggi del percorso
description: 'Scopri come utilizzare gli eventi dei passaggi di percorso in Adobe Journey Optimizer: cosa sono, perché sono importanti e come utilizzarli per l’analisi e l’ottimizzazione'
feature: Journeys, Reporting
role: Developer, Admin, User
level: Intermediate, Experienced
keywords: percorso, eventi dei passaggi, analisi, reporting, monitoraggio, XDM
exl-id: 2e7c5ea5-d8c5-416d-ab88-d2bc02043558
TQID: https://experienceleague.adobe.com/PSXSN-31GNlM0zBKcCvdKPciHt5zhQPPCffFrUoIxUs
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
subfeature_v2:
  - id: b15c7c2e-788c-4eb7-86a8-390565b0d2c9
  - id: b32bb433-f8c6-4931-8e52-e657230a3bf2
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: ba62ad25-65cb-4ea9-b7aa-0fa87c4a9fa0
  - id: cfba2953-2ce9-4b00-a00c-71cd338ae63f
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b4dd41a7-ccf8-4e9d-918e-acaab534a307
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 937
ht-degree: 5%

---

# Utilizzare gli eventi dei passaggi del percorso {#work-with-journey-step-events}

Gli eventi dei passaggi di percorso sono eventi generati automaticamente che acquisiscono informazioni dettagliate su ogni passaggio di un [profilo](../audience/get-started-profiles.md) durante l&#39;avanzamento in un [percorso](../building-journeys/journey.md) in Adobe Journey Optimizer. Questi eventi forniscono visibilità completa sulle prestazioni di [percorso](../building-journeys/report-journey.md) e abilitano potenti funzionalità di analisi.

## Cosa sono gli eventi delle fasi del percorso {#what-are-step-events}

Gli eventi dei passaggi di percorso sono eventi [XDM (Experience Data Model)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target="_blank"} generati dal sistema e che Adobe Journey Optimizer crea e invia automaticamente a [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html?lang=it){target="_blank"} ogni volta che un profilo si sposta da un nodo a un altro in un percorso. Ogni evento corrisponde a una [attività di percorso](../building-journeys/about-journey-activities.md) specifica o a una transizione nell&#39;esperienza di percorso del cliente.

Esistono due tipi principali di eventi dei passaggi del percorso:

- **journeyStepEvent**: eventi relativi alla progressione di singoli profili attraverso passaggi del percorso
- **journeyStepProfileEvent**: eventi che includono informazioni aggiuntive sul contesto del profilo

### Cosa attiva gli eventi dei passaggi del percorso? {#event-triggers}

Gli eventi delle fasi del percorso vengono generati automaticamente per varie attività del percorso:

- **Eventi di ingresso**: quando un profilo [entra in un percorso](../building-journeys/entry-management.md)
- **Esecuzione dell&#39;azione**: quando [vengono inviati messaggi](../building-journeys/journey-action.md) o vengono eseguite [azioni personalizzate](../building-journeys/using-custom-actions.md)
- **Valutazione condizione**: quando i profili passano attraverso [condizioni](../building-journeys/conditions.md) e punti decisionali
- **Attività di attesa**: quando i profili entrano ed escono [attendi nodi](../building-journeys/wait-activity.md)
- **Eventi di uscita**: al completamento dei profili o [all&#39;uscita da un percorso](../building-journeys/end-journey.md)
- **Gestione degli errori**: quando si verificano errori durante l&#39;esecuzione del percorso

>[!NOTE]
>
>Gli eventi delle fasi di percorso vengono attivati per impostazione predefinita su tutte le istanze. Non puoi modificare o aggiornare [schemi e set di dati](sharing-overview.md) creati durante il provisioning per gli eventi dei passaggi. Questi schemi e set di dati sono in modalità di sola lettura.

Ulteriori informazioni sugli schemi evento di [percorsi](sharing-field-list.md).

## Perché gli eventi dei passaggi di percorso contano {#why-step-events-matter}

Gli eventi delle fasi di percorso forniscono un valore critico per le organizzazioni che utilizzano Adobe Journey Optimizer:

### Analisi e monitoraggio in tempo reale {#real-time-analytics}

- **Monitoraggio delle prestazioni del Percorso**: monitora il flusso dei profili nei tuoi percorsi in tempo reale utilizzando [rapporti live](live-report.md)
- **Analisi della conversione**: comprendi i punti di riconversione e i percorsi di conversione riusciti con [analisi del percorso](journey-global-report-cja.md)
- **Rilevamento errori**: identifica e risolve i problemi quando si verificano tramite [monitoraggio e avvisi](alerts.md)

### Integrazione dei dati e approfondimenti {#data-integration}

- **Analisi multipiattaforma**: combina i dati del percorso con altre [origini dati Adobe Experience Platform](../datasource/adobe-experience-platform-data-source.md)
- **Visualizzazione 360 clienti**: creazione di [profili cliente](../audience/get-started-profiles.md) completi che includono interazioni di percorso
- **Modellazione attribuzione**: collega i punti di contatto del percorso ai risultati di business a valle tramite [Customer Journey Analytics](cja-ajo.md)

### Opportunità di ottimizzazione {#optimization}

- **Approfondimenti test A/B**: analizza le prestazioni di diversi percorsi di percorso utilizzando [sperimentazione](campaign-global-report-cja-experimentation.md)
- **Miglioramento di Personalization**: utilizza i dati sul comportamento del percorso per migliorare le esperienze future con [contenuto dinamico](../personalization/dynamic-content.md)
- **Efficienza operativa**: identificazione dei colli di bottiglia e ottimizzazione della progettazione di [percorsi](../building-journeys/using-the-journey-designer.md)

## Come utilizzare gli eventi dei passaggi del percorso {#how-to-use-step-events}

### Accesso ai dati evento del passaggio del percorso {#accessing-data}

I dati dell’evento del passaggio di percorso vengono memorizzati automaticamente in Adobe Experience Platform e sono accessibili tramite:

1. **Query Data Lake**: utilizzare SQL per eseguire query sul set di dati `journey_step_events` con [Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=it){target="_blank"}
2. **Customer Journey Analytics**: Analizza i dati del percorso tramite [strumenti di analisi avanzati](cja-ajo.md)
3. **Rapporti in tempo reale**: accesso ai dati tramite le [funzionalità di reporting integrate di Journey Optimizer](gs-reports.md)
4. **API**: accesso programmatico ai dati evento per le applicazioni personalizzate

Ulteriori informazioni sull&#39;[accesso ai set di dati](../data/datasets-query-examples.md).

### Punti dati chiave disponibili {#key-data-points}

Gli eventi delle fasi del percorso acquisiscono informazioni complete, tra cui:

- **Identificazione Percorso**: [ID Percorso, versione e nome](sharing-journey-fields.md)
- **Informazioni sul profilo**: [ID profilo e identità associate](sharing-identity-fields.md)
- **Dettagli del passaggio**: [Nome del nodo, tipo di passaggio e stato di esecuzione](sharing-common-fields.md)
- **Marca temporale**: tempistica precisa di ogni passaggio del percorso
- **Risultati azione**: [Stato di esito positivo/negativo e dettagli di esecuzione](sharing-execution-fields.md)
- **Informazioni sull&#39;errore**: dettagliati [codici di errore e descrizioni](sharing-field-list.md#discarded-events) in caso di problemi

Esplora tutte le [definizioni di campo disponibili](sharing-field-list.md).

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

Ulteriori informazioni [tecniche di query per analisi funnel](query-examples.md#common-queries).

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

- Utilizza `journeyVersionID` invece di `journeyVersionName` per migliorare le prestazioni delle query ([ulteriori informazioni sulle proprietà del percorso](../building-journeys/expression/journey-properties.md))
- Filtra per intervalli di date per migliorare la velocità delle query su set di dati di grandi dimensioni
- Sfrutta le identità di profilo corrispondenti alla configurazione dello spazio dei nomi di [percorso](../building-journeys/entry-management.md)

**Qualità dei dati**

- Monitora regolarmente [eventi eliminati](sharing-field-list.md#discarded-events) per identificare i problemi relativi ai dati
- Convalidare che gli schemi evento soddisfino i requisiti di analisi
- Implementare la corretta gestione degli errori nelle query personalizzate

**Strategie di Analytics**

- Combina gli eventi dei passaggi del percorso con [dati di feedback del messaggio](../data/datasets-query-examples.md#message-feedback-event-dataset) per un&#39;attribuzione completa
- Utilizzare l&#39;analisi basata sul tempo per comprendere la velocità del percorso e i colli di bottiglia

### Funzionalità di analisi avanzate {#advanced-analytics}

Integrazione con **Customer Journey Analytics**
Gli eventi dei passaggi di percorso possono essere analizzati utilizzando [Customer Journey Analytics](cja-ajo.md) per:

- Modellazione di attribuzione avanzata
- Visualizzazione percorso cross-channel
- Analisi predittive sui risultati di percorso

Scopri come [configurare Customer Journey Analytics](report-gs-cja.md) per i dati di Journey Optimizer.

## Risorse aggiuntive {#additional-resources}

### Collegamenti alla documentazione {#documentation-links}

- **[Panoramica sulla condivisione dei passaggi di Percorso](sharing-overview.md)**: informazioni sul flusso dei dati di percorso in Adobe Experience Platform
- **[Dizionario schemi incorporato](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=it){target="_blank"}**: riferimento schema XDM completo
- **[Rapporti di Journey Optimizer](report-gs-cja.md)**: panoramica delle funzionalità di reporting in Journey Optimizer

### Guide all’integrazione {#integration-guides}

- **[Adobe Customer Journey Analytics](cja-ajo.md)**: analisi dei dati di Journey Optimizer in CJA
- **[Gestione dati](../data/export-datasets.md)**: esportazione e gestione dei dati di percorso
- **[Privacy e governance](../privacy/audit-logs.md)**: considerazioni sulla governance dei dati per gli eventi di percorso


**Passaggi successivi:**

- Inizia con [creare i report del primo percorso](sharing-overview.md)
- Esplora [esempi di query](query-examples.md) per casi d&#39;uso specifici
- Scopri le [best practice per la gestione dei percorsi](../building-journeys/journey.md)
