---
solution: Journey Optimizer
product: journey optimizer
title: Architettura di AJO
description: Architettura e relazione con AEP
feature: Get Started
role: Admin, Developer, User
level: Beginner
redpen-status: PASS_||_2025-04-28_15-13-07
exl-id: f792fdf9-8038-4dd7-a7d5-d931dbf35c3e
hide: true
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 0%

---

# Architettura

## Il quadro generale: come Adobe Journey Optimizer si inserisce

Adobe Journey Optimizer (AJO) e Adobe Experience Platform (AEP) collaborano per abilitare la personalizzazione basata sui dati su larga scala. Questo ecosistema funziona come un flusso continuo in cui i dati vengono raccolti, analizzati e applicati per creare percorsi di clienti personalizzati.

![](../assets/do-not-localize/get-started-big-picture.png)


### Foundation: Adobe Experience Platform (AEP)

Adobe Experience Platform funge da spina dorsale e consente ai brand di centralizzare i dati dei clienti e attivarli per esperienze personalizzate.

- **Piattaforma dati**: AEP funge da hub centrale per la raccolta, la gestione e la strutturazione dei dati dei clienti al fine di garantire la coerenza tra i sistemi.
- **Acquisizione dati (origini)**: i brand importano dati da vari sistemi, ad esempio piattaforme CRM, siti web, app mobili e archiviazione cloud, utilizzando connettori predefiniti. Ad esempio, un connettore Source acquisisce i dati di acquisto da una piattaforma di e-commerce.
- **Profilo cliente in tempo reale**: questa funzione crea profili unificati unendo dati provenienti da più origini. Ad esempio, un profilo combina interazioni e-mail e acquisti in-store per fornire una visione completa di un cliente.
- **Livello di governance**: questo livello disciplina l&#39;accesso ai dati, la conformità alla privacy e la sicurezza. Garantisce che i brand utilizzino in modo sicuro i dati dei clienti rispettando al contempo le normative.

### Motore di orchestrazione: Adobe Journey Optimizer (AJO)

Adobe Journey Optimizer applica i dati e le informazioni provenienti da AEP per fornire esperienze cliente intelligenti e personalizzate su vari canali.

- **Informazioni sui clienti**: i profili cliente in tempo reale consentono la segmentazione in tipi di pubblico per la messaggistica mirata. Ad esempio, un pubblico include gli acquirenti frequenti identificati nella cronologia degli acquisti.
- **Contenuto e offerte**:
   - **Gestione dei contenuti**: questa funzionalità fornisce gli strumenti per la creazione, la gestione e la personalizzazione dei contenuti tra canali diversi. Ad esempio, puoi creare un Frammento di contenuto riutilizzabile per un’intestazione e-mail promozionale.
   - **Gestione delle decisioni**: questo sistema utilizza una logica in tempo reale per selezionare l&#39;offerta o il messaggio migliore per ogni individuo. Ad esempio, un cliente idoneo potrebbe ricevere un’offerta di sconto in base alla cronologia di navigazione.
- **Gestione Percorsi e campagne**: questa funzionalità automatizza le sequenze di interazioni (Percorsi) o pianifica messaggi con targeting occasionale (campagne). Ad esempio, un Percorso attiva le e-mail di follow-up dopo la visualizzazione di un prodotto.
- **Consegna (connessioni)**:
   - **Canali**: questa funzionalità consente di inviare messaggi e offerte tramite piattaforme di comunicazione quali e-mail, SMS, notifiche push e direct mail.
   - **Destinazioni**: questa funzione esporta i dati di profilo e pubblico in sistemi esterni per l&#39;attivazione o l&#39;analisi. Ad esempio, i dati sul pubblico vengono inviati a una piattaforma di social media per il targeting degli annunci.
- **Misurazione e analisi**: questa funzione tiene traccia del coinvolgimento del cliente e delle prestazioni della campagna con i rapporti. Queste informazioni consentono un miglioramento continuo.

## Ciclo di ottimizzazione continua

Questo ecosistema funziona come un ciclo continuo di ottimizzazione. I dati favoriscono la comprensione dei clienti, che a sua volta contribuisce a determinare contenuti e decisioni personalizzati. Questi vengono orchestrati in percorsi, distribuiti su canali diversi, misurati per verificarne l’efficacia e perfezionati nel tempo.

![](../assets/do-not-localize/get-started-flow.png)

## Architettura dettagliata

![Architettura di Adobe Journey Optimizer](assets/ajo-architecture.png)


## Privacy e sicurezza

Le procedure di privacy e sicurezza di Adobe Experience Cloud si applicano a Adobe Journey Optimizer. Queste misure garantiscono la conformità alle normative sulla privacy, consentendo ai brand di offrire esperienze personalizzate mantenendo al contempo la fiducia dei clienti.
