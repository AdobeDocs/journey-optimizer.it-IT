---
solution: Journey Optimizer
product: journey optimizer
title: Informazioni su Journey Optimizer
description: Scopri come Adobe Journey Optimizer funziona con Adobe Experience Platform per offrire esperienze cliente personalizzate
feature: Get Started
role: Admin, Developer, User
level: Beginner
source-git-commit: 87f714e380957b40df196652ac37d1e6cd611925
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 3%

---

# Informazioni su Journey Optimizer {#understanding-ajo}

Adobe Journey Optimizer e Adobe Experience Platform collaborano per abilitare la personalizzazione basata sui dati su larga scala. Questa pagina spiega come funzionano questi sistemi e come le loro aree funzionali principali si combinano per offrire ai clienti esperienze eccezionali. [Informazioni sulle funzionalità chiave](get-started.md) | [Terminologia chiave](terminology.md)

## Come funziona Journey Optimizer {#how-it-works}

Adobe Journey Optimizer funziona come un flusso continuo in cui i dati vengono raccolti, analizzati e applicati per creare percorsi di clienti personalizzati.

![](assets/ajo-aep-architecture-diagram.png)

### Adobe Experience Platform: la base {#aep-foundation}

Adobe Experience Platform funge da spina dorsale e consente ai brand di centralizzare i dati dei clienti e attivarli per esperienze personalizzate:

* **Piattaforma dati**: hub centrale per la raccolta, la gestione e la strutturazione dei dati dei clienti per garantire la coerenza tra i sistemi. [Informazioni su schemi e set di dati](../data/get-started-schemas.md)
* **Acquisizione dati (origini)** - Importa dati da piattaforme CRM, siti Web, app mobili e archiviazione cloud utilizzando connettori predefiniti. [Esplora origini dati](get-started-sources.md)
* **Profilo cliente in tempo reale** - Crea profili unificati unendo dati provenienti da più origini (interazioni e-mail, acquisti in-store, comportamento Web). [Informazioni sui profili](../audience/get-started-profiles.md)
* **Livello di governance**: disciplina l&#39;accesso ai dati, la conformità alla privacy e la sicurezza nel rispetto delle normative. [Visualizza documentazione sulla privacy](../privacy/get-started-privacy.md)

### Adobe Journey Optimizer: il motore di orchestrazione {#ajo-orchestration}

Adobe Journey Optimizer applica i dati e le informazioni provenienti da Adobe Experience Platform per fornire esperienze cliente intelligenti e personalizzate:

* **Informazioni sui clienti** - I profili cliente in tempo reale consentono la segmentazione in tipi di pubblico per la messaggistica mirata. [Creare tipi di pubblico](../audience/about-audiences.md)
* **Contenuto e offerte** - Strumenti per la creazione, la gestione e la personalizzazione dei contenuti; logica in tempo reale per selezionare l&#39;offerta migliore per ogni persona. [Progetta contenuto](../../rp_landing_pages/content-management-landing-page.md) | [Gestione offerte](../offers/get-started/starting-offer-decisioning.md)
* **Gestione Percorsi e campagne** - Automatizza le sequenze di interazioni (percorsi) o pianifica messaggi con targeting occasionale (campagne). [percorsi di compilazione](../building-journeys/journey-gs.md) | [Crea campagne](../campaigns/get-started-with-campaigns.md)
* **Consegna (connessioni)**: consegna messaggi tramite canali quali e-mail, SMS, notifiche push e direct mail; esporta dati in sistemi esterni. [Configurare i canali &#x200B;](../configuration/get-started-configuration.md)
* **Misurazione e analisi** - Tiene traccia del coinvolgimento del cliente e delle prestazioni della campagna con rapporti per un miglioramento continuo. [Visualizza report](../reports/campaign-global-report-cja.md)

### Ciclo di ottimizzazione continua {#optimization-cycle}

Questo ecosistema funziona come un ciclo continuo di ottimizzazione. I dati favoriscono la comprensione dei clienti, che a sua volta contribuisce a determinare contenuti e decisioni personalizzati. Questi vengono orchestrati in percorsi, distribuiti su canali diversi, misurati per verificarne l’efficacia e perfezionati nel tempo.

![](../assets/do-not-localize/get-started-flow.png)

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

## Dettagli architettura {#architecture-details}

Per i team tecnici, ecco il diagramma dettagliato dell’architettura che mostra come Journey Optimizer si integra con Adobe Experience Platform. [Naviga nell&#39;interfaccia](user-interface.md) per esplorare questi componenti nella pratica.

![Architettura di Adobe Journey Optimizer](assets/ajo-architecture.png)

Quattro applicazioni sono create in modalità nativa su Experience Platform: Adobe Real-Time Customer Data Platform, Journey Optimizer, Customer Journey Analytics e Adobe Mix Modeler. Journey Optimizer funziona perfettamente con queste applicazioni, ma può anche funzionare in modo indipendente. [Rivedi guardrail e limitazioni](guardrails.md) per considerazioni sull&#39;implementazione.

### Punti di integrazione {#integration-points}

Journey Optimizer si integra con Adobe Experience Platform a più livelli:

* **Livello dati** - Condivide lo stesso profilo cliente in tempo reale, lo stesso grafico delle identità e gli stessi set di dati
* **Livello di servizio** - Sfrutta i servizi di governance, privacy e query di Adobe Experience Platform
* **Livello applicazione** - Fornisce l&#39;orchestrazione del percorso, la gestione delle decisioni e la gestione dei contenuti su Adobe Experience Platform

Ulteriori informazioni su [blueprint Adobe Journey Optimizer](https://experienceleague.adobe.com/it/docs/blueprints-learn/architecture/customer-journeys/journey-optimizer/journey-optimizer-overview){target="_blank"}.

## Privacy e sicurezza {#privacy-security}

Le procedure di privacy e sicurezza di Adobe Experience Cloud si applicano a Adobe Journey Optimizer. Queste misure garantiscono la conformità alle normative sulla privacy come il RGPD, consentendoti di fornire esperienze personalizzate mantenendo al contempo la fiducia dei clienti. [Ulteriori informazioni sulla privacy in Journey Optimizer](../privacy/get-started-privacy.md)
