---
solution: Journey Optimizer
product: journey optimizer
title: Ruoli e responsabilità di AJO
description: Scopri i diversi ruoli coinvolti in Adobe Journey Optimizer e le loro responsabilità
feature: Get Started
role: Admin, Data Engineer, Developer, User
level: Beginner
exl-id: 71ab7369-fd84-46eb-95d2-941bd887d565
redpen-status: PASS_||_2025-04-28_15-13-07
source-git-commit: d2cdafef6f2d69ea85d9d042c859a8b1e7654d7d
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 1%

---


# Ruoli e responsabilità di AJO

Adobe Journey Optimizer (AJO) consente ai brand di offrire percorsi di clienti connessi e contestualizzati per l’intero ciclo di vita del cliente. Consente ai team di personalizzare le interazioni su larga scala e allinea le aspettative dei clienti con gli obiettivi aziendali. Questa documentazione spiega i ruoli chiave nell’utilizzo efficace di Journey Optimizer, le loro responsabilità e come iniziare.

**Nota importante:** Adobe Journey Optimizer definisce ruoli distinti con responsabilità specifiche. Un singolo utente può eseguire più ruoli o tutti i ruoli, a seconda della struttura dell’organizzazione.

## Guide rapide basate sul ruolo

Per semplificare l’implementazione, AJO organizza le attività in ruoli specifici in base alle competenze. Ogni ruolo si concentra sulle attività essenziali necessarie per fornire un’esperienza del cliente fluida.

| Ruolo | Responsabilità principali | Abilità chiave | Attività tipiche |
|-------------------|----------------------------------|--------------------------------|-----------------------------------------------|
| **Amministratore** | Configurazione del sistema e gestione delle autorizzazioni | Configurazione del sistema, gestione degli utenti, protezione | Configurare le sandbox, gestire gli utenti e configurare i canali |
| **Ingegnere dati** | Configurare la struttura e i flussi di dati | Modellazione dati, progettazione schema, integrazione API | Configurare schemi, gestire set di dati e configurare origini dati |
| **Sviluppatore** | Integrazioni tecniche e personalizzazioni | Sviluppo mobile, implementazione API, codifica | Integrare le app mobili, implementare le API, creare azioni personalizzate |
| **Addetto marketing** | Progettare ed eseguire percorsi di clienti | Strategia di marketing, creazione di contenuti, progettazione di percorsi | Creazione di campagne, progettazione di percorsi, analisi di rapporti |

Ogni ruolo affronta una fase specifica dell’implementazione di AJO e garantisce un processo di distribuzione strutturato ed efficiente.

## Dipendenze di ruolo e ordine di implementazione

Un’implementazione di Journey Optimizer di successo in genere segue questa sequenza, che riflette le dipendenze tra i ruoli:

1. **Amministratore**: imposta l&#39;ambiente\
   L&#39;amministratore pone le basi tecniche per il sistema e garantisce l&#39;accesso e la configurazione corretti per tutti gli utenti.
   * Configurare sandbox e autorizzazioni
   * Configurare l’accesso utente
   * Configurare i canali di messaggistica e le impostazioni tecniche

2. **Ingegnere dati**: crea la base dati\
   I Data Engineer definiscono la struttura e il flusso dei dati, essenziali per le esperienze personalizzate.
   * Progettare e implementare gli schemi
   * Impostare gli spazi dei nomi delle identità
   * Configurare l’acquisizione dei dati
   * Creare profili di test

3. **Sviluppatore**: gestisce le integrazioni tecniche\
   Gli sviluppatori consentono ad AJO di interagire con app mobili, siti web e sistemi esterni implementando integrazioni tecniche. Le notifiche push, ad esempio, si basano su configurazioni guidate da sviluppatori.
   * Integrare le applicazioni mobili per le notifiche push
   * Implementare gli SDK web
   * Sviluppare integrazioni personalizzate utilizzando API
   * Creare azioni personalizzate per sistemi di terze parti

4. **Addetto marketing**: crea e avvia percorsi\
   Gli addetti al marketing utilizzano le basi poste da altri ruoli per progettare e distribuire le esperienze dei clienti. Si concentrano sulla segmentazione del pubblico, sui contenuti personalizzati e sull’ottimizzazione del percorso.
   * Progettare segmenti di pubblico
   * Creare contenuti personalizzati
   * Generare e testare percorsi
   * Analisi delle prestazioni e ottimizzazione

**Nota:** Anche se questa sequenza è tipica, alcune attività possono verificarsi in parallelo. Ad esempio, gli sviluppatori possono lavorare sulle integrazioni delle app mentre i Data Engineer configurano gli schemi.

## Guida introduttiva per ruolo

Ogni ruolo inizia con attività specifiche personalizzate in base al suo focus. Il completamento di questi passaggi iniziali garantisce un onboarding e un allineamento più fluidi con il processo di implementazione generale:

1. **Per gli addetti al marketing**: concentrarsi sulla creazione del percorso, sulla progettazione dei messaggi e sull&#39;esecuzione della campagna.\
   Esempio: inizia creando una campagna e-mail di benvenuto per i nuovi clienti.

2. **Per data engineer**: stabilisce le basi di dati, configura gli schemi e integra le origini dati.\
   Esempio: imposta uno schema per tenere traccia della cronologia degli acquisti dei clienti per i consigli personalizzati.

3. **Per gli amministratori**: configurare gli ambienti, gestire le autorizzazioni e configurare i canali di messaggistica.\
   Esempio: configura ambienti sandbox per testare diverse strategie di messaggistica.

4. **Per sviluppatori**: integra app mobili, implementa API e crea integrazioni personalizzate.\
   Esempio: utilizza l’API AJO per attivare le notifiche push in base alle azioni dei clienti all’interno della tua app mobile.

Fai clic sul tuo ruolo qui sotto per accedere a indicazioni specifiche su misura per le tue responsabilità:

* [Introduzione al ruolo di addetto marketing](path/marketer.md)
* [Introduzione al ruolo di ingegnere dati](path/data-engineer.md)
* [Introduzione come amministratore](path/administrator.md)

## Video tutorial {#video}

Per ulteriori informazioni sulle funzionalità e sugli utenti tipo di Journey Optimizer, guarda il video introduttivo. Il video illustra l’interfaccia utente ed evidenzia le funzioni chiave in base ai flussi di lavoro specifici dei ruoli.

>[!VIDEO](https://video.tv.adobe.com/v/3424995?quality=12)

## Risorse aggiuntive

Per ulteriori informazioni approfondite e aggiornamenti, consulta le risorse seguenti:
* [Note sulla versione](https://experienceleague.adobe.com/docs/journey-optimizer/using/rn/release-notes.html)
* [Video tutorial](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=it)