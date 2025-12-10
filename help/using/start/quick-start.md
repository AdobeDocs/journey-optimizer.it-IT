---
solution: Journey Optimizer
product: journey optimizer
title: Ruoli e responsabilità
description: Scopri i diversi ruoli coinvolti in Adobe Journey Optimizer e le rispettive responsabilità
feature: Get Started
role: Admin, Developer, User
level: Beginner
exl-id: 71ab7369-fd84-46eb-95d2-941bd887d565
redpen-status: PASS_||_2025-04-28_15-13-07
source-git-commit: 4ae9e908d259dbd266417242cf9e65d693227061
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 86%

---


# Ruoli e responsabilità

Adobe Journey Optimizer consente ai brand di offrire percorsi di clienti connessi e contestualizzati per l’intero ciclo di vita del cliente. Consente ai team di personalizzare le interazioni su larga scala e allinea le aspettative della clientela con gli obiettivi aziendali. Questa documentazione spiega i ruoli chiave per l’utilizzo efficace di Journey Optimizer, le rispettive responsabilità e come iniziare.

**Nota importante:** Adobe Journey Optimizer definisce ruoli distinti con responsabilità specifiche. Un singolo utente può svolgere più ruoli o tutti i ruoli, a seconda della struttura dell’organizzazione.

## Guide rapide basate sul ruolo

Per semplificare l’implementazione, Adobe Journey Optimizer organizza le attività in ruoli specifici in base alle competenze. Ogni ruolo si incentra sulle attività essenziali necessarie per fornire un’esperienza cliente fluida.

| Ruolo | Responsabilità principali | Competenze chiave | Attività tipiche |
|-------------------|----------------------------------|--------------------------------|-----------------------------------------------|
| **Amministratore** | Configurazione sistema e gestione delle autorizzazioni | Configurazione sistema, gestione utenti, sicurezza | Configurazione sandbox, gestione utenti, impostazione dei canali |
| **Data Engineer** | Configurazione della struttura e dei flussi di dati | Modellazione dati, progettazione schema, integrazione API | Impostazione schemi, gestione set di dati e configurazione origini dati |
| **Sviluppatore** | Integrazioni tecniche e personalizzazioni | Sviluppo per dispositivi mobili, implementazione API, codifica | Integrazione app per dispositivi mobili, implementazione API, creazione di azioni personalizzate |
| **Marketer** | Progettazione ed esecuzione dei percorsi cliente | Strategia di marketing, creazione contenuti, progettazione percorsi | Creazione di campagne, progettazione di percorsi, analisi di rapporti |

Ogni ruolo affronta una fase specifica dell’implementazione di Adobe Journey Optimizer e garantisce un processo di distribuzione strutturato ed efficiente.

## Dipendenze di ruolo e ordine di implementazione

Un’implementazione di Journey Optimizer di successo in genere segue questa sequenza, che riflette le dipendenze tra i ruoli:

1. **Amministratore**: configura l’ambiente\
   L’amministratore pone le basi tecniche per il sistema e garantisce l’accesso e la configurazione corretti per tutti gli utenti.
   * Configurare sandbox e autorizzazioni
   * Configurare l’accesso utente
   * Configurare i canali di messaggistica e le impostazioni tecniche

2. **Data Engineer**: crea la base dati\
   I data engineer definiscono la struttura e il flusso dei dati, essenziali per le esperienze personalizzate.
   * Progettare e implementare gli schemi
   * Impostare lo spazio dei nomi di identità
   * Configurare l’acquisizione di dati
   * Creare profili di test

3. **Sviluppatore**: gestisce le integrazioni tecniche\
   Gli sviluppatori consentono a Adobe Journey Optimizer di interagire con app mobili, siti web e sistemi esterni implementando integrazioni tecniche. Le notifiche push, ad esempio, si basano su configurazioni guidate da sviluppatori.
   * Integrare le applicazioni per dispositivi mobili per le notifiche push
   * Implementare gli SDK web
   * Sviluppare integrazioni personalizzate utilizzando API
   * Creare azioni personalizzate per sistemi di terze parti

4. **Marketer**: crea e avvia percorsi\
   I marketer utilizzano le basi poste da altri ruoli per progettare e distribuire le esperienze cliente. Si concentrano sulla segmentazione del pubblico, sui contenuti personalizzati e sull’ottimizzazione del percorso.
   * Progettare i segmenti di pubblico
   * Creare contenuti personalizzati
   * Creare e testare percorsi
   * Analisi delle prestazioni e ottimizzazione

**Nota:** anche se questa sequenza è tipica, alcune attività possono verificarsi in parallelo. Ad esempio, gli sviluppatori possono lavorare sulle integrazioni delle app mentre i data engineer configurano gli schemi.

## Guida introduttiva per ruolo

Ogni ruolo inizia con attività specifiche personalizzate in base al rispettivo punto di interesse. Il completamento di questi passaggi iniziali garantisce un onboarding e un allineamento più fluidi con il processo di implementazione generale:

1. **Per i marketer**: concentrarsi sulla creazione del percorso, sulla progettazione dei messaggi e sull’esecuzione della campagna.\
   Esempio: iniziare creando una campagna e-mail di benvenuto per la nuova clientela.

2. **Per i data engineer**: stabilire le basi di dati, configurare gli schemi e integrare le origini dati.\
   Esempio: impostare uno schema per tenere traccia della cronologia degli acquisti della clientela per i consigli personalizzati.

3. **Per gli amministratori**: configurare gli ambienti, gestire le autorizzazioni e configurare i canali di messaggistica.\
   Esempio: configurare ambienti sandbox per testare diverse strategie di messaggistica.

4. **Per gli sviluppatori**: integrare app per dispositivi mobili, implementare API e creare integrazioni personalizzate.\
   Esempio: utilizza l’API Adobe Journey Optimizer per attivare le notifiche push in base alle azioni dei clienti all’interno della tua app mobile.

Fai clic sul tuo ruolo qui sotto per accedere a istruzioni specifiche su misura per le tue responsabilità:

* [Iniziare come marketer](path/marketer.md)
* [Iniziare come data engineer](path/data-engineer.md)
* [Iniziare come amministratore](path/administrator.md)

## Video dimostrativo {#video}

Per ulteriori informazioni sugli utenti tipo e sulle funzionalità chiave di Journey Optimizer, guarda il video introduttivo. Il video illustra l’interfaccia utente ed evidenzia le funzioni chiave in base ai flussi di lavoro specifici dei ruoli.

>[!VIDEO](https://video.tv.adobe.com/v/3424995?quality=12)

## Risorse aggiuntive

Per ulteriori informazioni approfondite e aggiornamenti, consulta le risorse seguenti:

* [Note sulla versione](../rn/release-notes.md)
* [Video tutorial](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=it)