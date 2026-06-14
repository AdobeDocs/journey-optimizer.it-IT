---
solution: Journey Optimizer
product: journey optimizer
title: Informazioni su Journey Optimizer
description: Scopri come Adobe Journey Optimizer funziona con Adobe Experience Platform per offrire esperienze cliente personalizzate
feature: Get Started
topic: Content Management
role: Admin, Developer, User
level: Beginner
keywords: Ottimizzatore del percorso, come funziona, architettura, piattaforma di esperienza, aree funzionali
exl-id: 9df179a0-a5f6-4dbd-a9db-a103731b1854
TQID: https://experienceleague.adobe.com/E2ksPVFZBggv1RgEri7jx30G2oSanpmNs77vH9Yuq78
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: fdac7813-bd56-47ae-9f6d-fa94ad1c5dee
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: 46a5a6dc0a3486633a1a71f8bba8a3cd53aaa618
workflow-type: tm+mt
source-wordcount: 986
ht-degree: 3%

---

# Informazioni su Journey Optimizer {#understanding-ajo}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come Adobe Journey Optimizer funziona con Adobe Experience Platform in modo da comprendere il ciclo da dati a esperienze, le aree funzionali e l&#39;architettura alla base dei percorsi personalizzati.

>[!ENDSHADEBOX]

Questa pagina spiega come Adobe Experience Platform e Journey Optimizer lavorano insieme e descrive il ciclo continuo da dati a esperienze, aree funzionali chiave, dettagli dell’architettura e punti di integrazione.

Adobe Journey Optimizer e Adobe Experience Platform collaborano per abilitare la personalizzazione basata sui dati su larga scala. Questa pagina spiega come funzionano questi sistemi e come le loro aree funzionali principali si combinano per offrire ai clienti esperienze eccezionali. [Informazioni sulle funzionalità chiave](get-started.md) | [Esplora la terminologia chiave](terminology.md)

## Come funziona Journey Optimizer {#how-it-works}

Senza una base dati unificata, i brand sono costretti a fare affidamento su più strumenti specifici per canale, rendendo difficile mantenere una visione coerente di ogni cliente o agire sul suo comportamento in tempo reale. Per risolvere questo problema, Journey Optimizer si basa su Adobe Experience Platform per collegare i dati dei clienti, la creazione di contenuti e l’orchestrazione del percorso in un unico sistema continuo. Il risultato sono esperienze di marchio significative che stimolano la fedeltà dei clienti e il valore del ciclo di vita.

Adobe Journey Optimizer funziona come un flusso continuo in cui i dati vengono raccolti, analizzati e applicati per creare percorsi di clienti personalizzati.

![Diagramma che mostra Adobe Experience Platform come livello dati fondamentale, con Journey Optimizer integrato in alto insieme a Real-Time CDP, Customer Journey Analytics e Adobe Mix Modeler, tutti i servizi di base come Real-Time Customer Profile, governance dei dati e risoluzione delle identità.](assets/ajo-aep-architecture-diagram.png)

### Adobe Experience Platform: la base {#aep-foundation}

Adobe Experience Platform funge da spina dorsale e consente ai brand di centralizzare i dati dei clienti e attivarli per esperienze personalizzate:

* **Piattaforma dati**: hub centrale per la raccolta, la gestione e la strutturazione dei dati dei clienti per garantire la coerenza tra i sistemi. [Scopri gli schemi e i set di dati](../data/get-started-schemas.md)
* **Acquisizione dati (origini)** - Importa dati da piattaforme CRM, siti Web, app mobili e archiviazione cloud utilizzando connettori predefiniti. [Esplora origini dati](get-started-sources.md)
* **Profilo cliente in tempo reale** - Crea profili unificati unendo dati provenienti da più origini (interazioni e-mail, acquisti in-store, comportamento Web). [Informazioni sui profili](../audience/get-started-profiles.md)
* **Livello di governance**: disciplina l&#39;accesso ai dati, la conformità alla privacy e la sicurezza nel rispetto delle normative. [Visualizza documentazione sulla privacy](../privacy/get-started-privacy.md)

### Adobe Journey Optimizer: il motore di orchestrazione {#ajo-orchestration}

Adobe Journey Optimizer applica i dati e le informazioni provenienti da Adobe Experience Platform per fornire esperienze cliente intelligenti e personalizzate:

* **Informazioni sui clienti** - I profili cliente in tempo reale consentono la segmentazione in tipi di pubblico per la messaggistica mirata. [Creare tipi di pubblico](../audience/about-audiences.md)
* **Contenuti e offerte** - Una finestra di progettazione visiva integrata, modelli riutilizzabili e una libreria di risorse centralizzata consentono ai team di creare e personalizzare messaggi per qualsiasi canale, senza uscire dalla piattaforma. La personalizzazione dinamica adatta i contenuti in base agli attributi, al comportamento e al contesto del cliente. La logica di decisioning in tempo reale seleziona quindi l’offerta migliore per ogni singolo utente. [Progetta contenuto](../../rp_landing_pages/content-management-landing-page.md) | [Gestione risorse](../integrations/assets.md) | [Gestire le offerte](../offers/get-started/starting-offer-decisioning.md)
* **Gestione Percorsi e campagne** - Automatizza le sequenze di interazioni (percorsi) o pianifica messaggi con targeting occasionale (campagne). [percorsi di compilazione](../building-journeys/journey-gs.md) | [Crea campagne](../campaigns/get-started-with-campaigns.md)
* **Consegna (connessioni)**: consegna messaggi tramite canali quali e-mail, SMS, notifiche push e direct mail; esporta dati in sistemi esterni. [Configurare i canali](../configuration/get-started-configuration.md)
* **Misurazione e analisi** - Tiene traccia del coinvolgimento del cliente e delle prestazioni della campagna con rapporti per un miglioramento continuo. [Visualizza report](../reports/campaign-global-report-cja.md)

### Il ciclo di ottimizzazione continua {#optimization-cycle}

Questo ecosistema funziona come un ciclo continuo di ottimizzazione. I dati favoriscono la comprensione dei clienti, che a sua volta contribuisce a determinare contenuti e decisioni personalizzati. Questi vengono orchestrati in percorsi, distribuiti su canali diversi, misurati per verificarne l’efficacia e perfezionati nel tempo.

![Diagramma che illustra il ciclo di ottimizzazione continua in Journey Optimizer: l&#39;acquisizione dei dati alimenta i profili dei clienti, che informano le decisioni su contenuti e offerte, orchestrati in percorsi, distribuiti tra canali diversi, misurati per le prestazioni e perfezionati nel tempo.](../assets/do-not-localize/get-started-flow.png)

## Aree funzionali chiave {#functional-areas}

Journey Optimizer include sette aree funzionali chiave in cui la collaborazione è perfetta:

| Area funzionale | Scopo | Attività chiave |
|-----------------|---------|----------------|
| **Gestione dati** | Organizzare i dati dei clienti | Definisci gli schemi, crea set di dati, importa dati da vari sistemi. [Ulteriori informazioni](../data/get-started-schemas.md) |
| **Gestione clienti** | Chi sono i clienti | Crea profili unificati, risolvi le identità, crea tipi di pubblico. [Ulteriori informazioni](../audience/get-started-profiles.md) |
| **Gestione dei contenuti** | Creare messaggi personalizzati | Progetta le e-mail, gestisci le risorse, crea modelli e frammenti e personalizza i contenuti. [Ulteriori informazioni](../../rp_landing_pages/content-management-landing-page.md) |
| **Gestione delle decisioni** | Seleziona l’offerta migliore in tempo reale | Gestisci la libreria di offerte, definisci le regole, applica i vincoli, stabilisci la logica di classificazione. [Ulteriori informazioni](../offers/get-started/starting-offer-decisioning.md) |
| **Gestione Percorso** | Progettare esperienze cliente automatizzate | Crea percorsi con la finestra di progettazione visiva, imposta i trigger, aggiungi condizioni e attendi i passaggi. [Ulteriori informazioni](../building-journeys/journey-gs.md) |
| **Connessioni** | Connettere origini dati e canali | Configurare i connettori di origine, impostare i canali, connettersi alle piattaforme esterne. [Ulteriori informazioni](../configuration/get-started-configuration.md) |
| **Amministrazione e privacy** | Configurazione del controllo e conformità | Gestisci gli utenti, configura le sandbox, imposta i canali, gestisci le richieste di accesso a dati personali. [Ulteriori informazioni](../administration/permissions.md) |

### Funzionamento congiunto di queste aree {#working-together}

Queste aree funzionali funzionano in ciclo continuo:

1. **Acquisizione dei dati** - Flussi di dati in Adobe Experience Platform, strutturati tramite Gestione dati
2. **Informazioni sui clienti** - I profili cliente in tempo reale unificano i dati; la gestione clienti crea tipi di pubblico
3. **Strategia di contenuto e offerta** - Gestione contenuto crea messaggi; Gestione decisioni definisce la logica di offerta
4. **Orchestrazione** - Gestione Percorso esegue il mapping delle interazioni tra i canali utilizzando i dati dei clienti, il contenuto e le decisioni
5. **Consegna** - Le connessioni facilitano la consegna dei messaggi tramite canali o la condivisione di dati con sistemi esterni
6. **Misurazione** - I feed di dati sulle prestazioni restituiscono informazioni per perfezionare tipi di pubblico, contenuti, decisioni e percorsi
7. **Governance** - L&#39;amministrazione e i controlli sulla privacy garantiscono la conformità in tutto

## Dettagli dell’architettura {#architecture-details}

Journey Optimizer è una delle quattro applicazioni create in modalità nativa su Adobe Experience Platform, insieme a Real-Time CDP, Customer Journey Analytics e Adobe Mix Modeler. Condivide i servizi di base di AEP: Profilo cliente in tempo reale, Identity Graph, governance dei dati e servizi di query, in modo da accedere a una base dati cliente unificata senza richiedere integrazioni separate. Journey Optimizer può funzionare come applicazione indipendente o interagire con altre applicazioni native di AEP.

Per informazioni approfondite sull&#39;architettura tecnica, inclusi modelli di integrazione, prerequisiti e flussi di dati di sistema, vedere [Blueprint di Adobe Journey Optimizer](https://experienceleague.adobe.com/it/docs/blueprints-learn/architecture/architecture-diagrams/customer-journeys/journey-optimizer/journey-optimizer-overview){target="_blank"}. Per considerazioni sull&#39;implementazione, [controlla guardrail e limitazioni](guardrails.md).

## Privacy e sicurezza {#privacy-security}

Le procedure di privacy e sicurezza di Adobe Experience Cloud si applicano a Adobe Journey Optimizer. Queste misure garantiscono la conformità alle normative sulla privacy come il RGPD, consentendoti di fornire esperienze personalizzate mantenendo al contempo la fiducia dei clienti. [Ulteriori informazioni sulla privacy in Journey Optimizer](../privacy/get-started-privacy.md)
