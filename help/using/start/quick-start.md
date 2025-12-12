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
source-git-commit: 344a5509731b455ee283af22bfdd8c67e028b83e
workflow-type: tm+mt
source-wordcount: '1585'
ht-degree: 14%

---


# Ruoli e responsabilità

Adobe Journey Optimizer consente ai brand di offrire esperienze connesse, contestuali e personalizzate in tutto il percorso di clienti. Progettato per offrire scalabilità, velocità e flessibilità, Journey Optimizer combina tre fattori di valore principali in un&#39;applicazione unificata:

* **Informazioni sul cliente in tempo reale e coinvolgimento** basate sul profilo cliente in tempo reale di Adobe
* **Orchestrazione moderna omni-channel** tramite tele unificate per percorsi in tempo reale e campagne batch, oltre a un moderno Message Designer
* **Decisioning intelligente e personalizzazione** tramite gestione delle decisioni e funzionalità AI/ML

Journey Optimizer offre due approcci di orchestrazione per soddisfare diverse esigenze di marketing:

* **Percorsi**: ideale per un impegno uno-a-uno in tempo reale, in cui ogni cliente si sposta secondo il proprio ritmo, attivato da comportamenti o eventi
* **Campagne orchestrate**: ideale per campagne batch, uno-a-molti in cui il pubblico avanza insieme attraverso flussi di lavoro con più passaggi secondo una pianificazione, ideale per promozioni stagionali, avvii di prodotti e comunicazioni basate su account

Questa esperienza unificata ti consente di implementare interi casi d’uso in un’unica posizione, dalla definizione di tipi di pubblico e la progettazione di percorsi alla creazione di contenuti personalizzati e all’analisi dei risultati. Questa documentazione spiega i ruoli chiave per l’utilizzo efficace di Journey Optimizer, le rispettive responsabilità e come iniziare.

**Nota importante:** Adobe Journey Optimizer definisce ruoli distinti con responsabilità specifiche. Un singolo utente può svolgere più ruoli o tutti i ruoli, a seconda della struttura dell’organizzazione.

## Guide rapide basate sul ruolo

Per semplificare l’implementazione, Adobe Journey Optimizer organizza le attività in ruoli specifici in base alle competenze. Ogni ruolo si incentra sulle attività essenziali necessarie per fornire un’esperienza cliente fluida.

| Ruolo | Responsabilità principali | Competenze chiave | Attività tipiche |
|-------------------|----------------------------------|--------------------------------|-----------------------------------------------|
| **Amministratore** | Configurazione dell’ambiente e gestione degli accessi | Configurazione sistema, gestione utenti, sicurezza | Configurare sandbox, gestire le autorizzazioni utente, configurare canali e predefiniti per messaggi |
| **Data Engineer** | Dati del profilo del cliente e origini dati | Modellazione dati, schemi XDM, connettori di origine | Modellare profilo e dati aziendali in schemi, configurare connettori sorgente, monitorare l’acquisizione dei dati |
| **Sviluppatore** | Implementazione e integrazioni tecniche | Mobile/Web SDK, API, architettura basata su eventi | Integrare gli SDK, implementare gli eventi, generare endpoint di azione personalizzati |
| **Marketer** | Progettazione di percorsi ed esperienze personalizzate | Orchestrazione del percorso, creazione di contenuti, targeting del pubblico | Progetta percorsi di clienti, crea e personalizza messaggi, gestisci offerte e componenti decisionali, definisci tipi di pubblico |

Ogni ruolo affronta una fase specifica dell’implementazione di Adobe Journey Optimizer e garantisce un processo di distribuzione strutturato ed efficiente.

## Dipendenze di ruolo e ordine di implementazione

Un’implementazione di Journey Optimizer di successo in genere segue questa sequenza, che riflette le dipendenze tra i ruoli:

1. **Amministratore**: configura l’ambiente\
   L’amministratore stabilisce le basi configurando le sandbox, impostando i controlli di accesso e preparando le configurazioni dei canali. Questo deve accadere prima per consentire ad altri team di lavorare.
   * Configurare sandbox di sviluppo, staging e produzione
   * Impostare ruoli, autorizzazioni e OLAC (Object-Level Access Control)
   * Configurare le configurazioni del canale (e-mail, SMS, push, in-app, web, schede di contenuto)
   * Delegare i sottodomini e configurare i pool IP
   * Configurare gli elenchi di soppressione e i criteri di consenso

2. **Data Engineer**: crea la base dati\
   I data engineer creano l’infrastruttura di dati che potenzia la personalizzazione, definendo il modo in cui i dati dei clienti fluiscono all’interno e attraverso il sistema.
   * Creare spazi dei nomi di identità per l’identificazione del cliente
   * Progettare schemi XDM (profilo, eventi di esperienza, relazionali)
   * Configurare i set di dati e abilitarli per Real-time Customer Profile
   * Configurare l’acquisizione dei dati (batch e streaming)
   * Creare attributi calcolati per calcoli complessi
   * Configurare eventi e origini dati per i percorsi

3. **Sviluppatore**: implementa integrazioni tecniche\
   Gli sviluppatori collegano le applicazioni a Journey Optimizer integrando SDK, inviando eventi e creando endpoint API. Queste implementazioni consentono ai percorsi di attivarsi ed eseguire.
   * Integrare Mobile SDK (iOS/Android) con la configurazione delle notifiche push
   * Implementare Web SDK per esperienze web
   * Inviare eventi dalle applicazioni ai percorsi di attivazione
   * Creare endpoint di azione personalizzati per integrazioni di sistema esterne
   * Test delle implementazioni tramite Adobe Experience Platform Assurance

4. **Addetto marketing**: progetta ed esegue le esperienze dei clienti\
   Gli addetti al marketing sfruttano tutto il lavoro fondamentale per creare percorsi, contenuti e ottimizzare le esperienze dei clienti su tutti i canali.
   * Creare tipi di pubblico utilizzando segmentazione, caricamento CSV o composizione del pubblico
   * Progettare contenuti personalizzati con l’Assistente IA e i modelli
   * Creazione di percorsi multicanale con trigger di eventi e pubblico
   * Test con flussi di lavoro di approvazione prima dell&#39;avvio
   * Monitorare le prestazioni e ottimizzare in base alle informazioni di reporting

**Nota:** anche se questa sequenza è tipica, alcune attività possono verificarsi in parallelo. Ad esempio, gli sviluppatori possono lavorare sulle integrazioni delle app mentre i data engineer configurano gli schemi.

## Guida introduttiva per ruolo

Ogni ruolo inizia con attività specifiche personalizzate in base al rispettivo punto di interesse. Il completamento di questi passaggi iniziali garantisce un onboarding e un allineamento più fluidi con il processo di implementazione generale:

### Per gli addetti al marketing {#for-marketers}

In qualità di addetto al marketing o di professionista aziendale, puoi progettare percorsi di clienti per offrire esperienze personali e contestuali in tutti i punti di contatto. Lavorerai in un’interfaccia unificata per implementare interi casi d’uso dall’inizio alla fine.

**Funzionalità chiave da utilizzare:**

* **Journey Orchestration**: crea un coinvolgimento cliente uno a uno in tempo reale in cui ogni persona si sposta secondo il proprio ritmo, attivato da comportamenti o eventi tra canali diversi
* **Orchestrazione campagna**: progetta e automatizza campagne batch complesse e in più passaggi su larga scala utilizzando un&#39;area di lavoro visiva. Perfetto per campagne avviate dal marchio come promozioni stagionali, lanci di prodotti e comunicazioni basate su account. Sfrutta la segmentazione tra più entità per creare tipi di pubblico precisi collegando i dati dei clienti con entità correlate (conti, acquisti, prenotazioni)
* **Modern Message Designer**: progetta e personalizza messaggi e-mail e mobili con un&#39;interfaccia a trascinamento. Modificare modelli predefiniti per accelerare il time-to-market
* **Gestione delle decisioni**: crea e gestisci offerte, regole di idoneità e altri componenti in una libreria centralizzata che possono essere incorporati nelle e-mail e nei punti di contatto dei clienti
* **Gestione risorse**: accedi ad Adobe Experience Manager Assets Essentials completamente incorporato in Journey Optimizer per accedere e distribuire le risorse in modo semplice
* **Definizione pubblico**: crea tipi di pubblico on-demand con ottimizzazione immediata utilizzando query relazionali, con visibilità pre-invio per conteggi accurati dei tipi di pubblico
* **Servizi AI/ML**: ottimizzazione del tempo di invio e punteggi di coinvolgimento predittivi per il targeting di clienti di alto valore e per ridurre al minimo il rischio di abbandono

**Inizia con:** modelli di casi d&#39;uso e procedure guidate per creare e distribuire facilmente nuovi percorsi di clienti.

[Introduzione al ruolo di → addetto al marketing](path/marketer.md)

### Per data engineer {#for-data-engineers}

In qualità di architetto o ingegnere di dati, devi impostare e gestire i dati del profilo cliente e altre origini dati che alimentano le esperienze orchestrate da Journey Optimizer.

**Responsabilità chiave:**

* **Dati profilo cliente**: modellare i dati del profilo cliente e i dati aziendali in schemi per creare una visualizzazione unificata a 360 gradi del cliente
* **Modellazione dati relazionali**: per campagne orchestrate, progetta schemi relazionali per abilitare la segmentazione di più entità, collegando i dati dei clienti con entità correlate come account, acquisti, abbonamenti e prenotazioni per una creazione flessibile del pubblico
* **Connettori Source**: configura i connettori di origine per acquisire in Adobe Experience Platform dati da web, CRM, dati offline e altre origini
* **Risoluzione identità**: configura gli spazi dei nomi delle identità per aggiornare continuamente i profili e spostare in tempo reale i clienti da e verso segmenti e percorsi
* **Origini dati**: configura le origini dati per l&#39;ascolto in tempo reale di segnali esterni nel percorso del cliente
* **Gestione profilo**: abilita i set di dati per Real-time Customer Profile per abilitare esperienze personalizzate
* **Qualità dei dati**: monitora l&#39;acquisizione dei dati per garantire che tutto scorra senza problemi in Journey Optimizer

**Inizia con:** modella il tuo primo schema del profilo cliente e configura un connettore di origine per iniziare a acquisire i dati.

[Introduzione al ruolo di data engineer →](path/data-engineer.md)

### Per gli amministratori {#for-administrators}

In qualità di amministratore, devi configurare l’ambiente Journey Optimizer per consentire ai team di lavorare in modo efficiente e sicuro.

**Responsabilità chiave:**

* **Sandbox**: crea e gestisci sandbox per suddividere dati e percorsi per diversi gruppi di utenti (sviluppo, test, produzione)
* **Gestione utenti**: configura gruppi di utenti e autorizzazioni per controllare l&#39;accesso a diverse funzionalità
* **Configurazione canale**: configura i canali di consegna e i predefiniti per messaggi per garantire un branding coerente tra i messaggi e le risorse consegnate tramite Journey Optimizer
* **Sicurezza e governance**: applicazione del controllo degli accessi a livello di oggetto, configurazione dei criteri di consenso e implementazione dei criteri di governance dei dati
* **Recapito messaggi**: delega sottodomini, creazione di pool IP e gestione di elenchi e elenchi Consentiti di soppressione
* **Configurazione Percorso**: configura gli elementi e le configurazioni del percorso per i team

**Inizia con:** Configura le sandbox e le autorizzazioni utente, quindi imposta le configurazioni del primo canale e i predefiniti per messaggi.

[Introduzione al ruolo di → amministratore](path/administrator.md)

### Per sviluppatori {#for-developers}

Implementa integrazioni tecniche che consentono di collegare Journey Optimizer alle applicazioni.

**Responsabilità chiave:**

* Integrare Adobe Experience Platform Mobile SDK (iOS/Android)
* Implementazione di Web SDK per esperienze web e notifiche push web
* Configurare le credenziali e i certificati per le notifiche push
* Inviare eventi dalle applicazioni ai percorsi di attivazione
* Creare endpoint API chiamati da Journey Optimizer tramite azioni personalizzate
* Implementare esperienze basate su codice per web, dispositivi mobili e altre superfici
* Testare ed eseguire il debug delle implementazioni con Adobe Experience Platform Assurance
* Utilizzare le API di Journey Optimizer per l’accesso programmatico

**Inizia con:** Integra Mobile o Web SDK, quindi implementa il tuo primo evento per attivare un percorso.

[Introduzione al ruolo di sviluppatore →](path/developer.md)

## Collaboration tra ruoli

Le implementazioni Journey Optimizer di successo richiedono collaborazione tra tutti i ruoli:

* **Amministratori** abilitano altri ruoli impostando sandbox, autorizzazioni e configurazioni di canale
* **I Data Engineer** forniscono le basi dati su cui sviluppatori e addetti al marketing si basano
* **Sviluppatori** implementano le integrazioni tecniche utilizzate dagli addetti al marketing per attivare i percorsi
* **Gli addetti al marketing** forniscono feedback a tutti i team su qualità dei dati, richieste di funzionalità ed esperienza utente

**Best practice:** organizza riunioni interfunzionali regolari per allineare le priorità, condividere i progressi e affrontare i blocchi tra i team.

## Video dimostrativo {#video}

Per ulteriori informazioni sugli utenti tipo e sulle funzionalità chiave di Journey Optimizer, guarda il video introduttivo. Il video illustra l’interfaccia utente ed evidenzia le funzioni chiave in base ai flussi di lavoro specifici dei ruoli.

>[!VIDEO](https://video.tv.adobe.com/v/3424995?quality=12)

## Risorse aggiuntive

Per ulteriori informazioni approfondite e aggiornamenti, consulta le risorse seguenti:

**Apprendimento e documentazione:**

* [Video tutorial](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=it){target="_blank"}: esercitazioni video dettagliate per tutti i ruoli
* [Libreria dei casi di utilizzo di Percorso](../building-journeys/jo-use-cases.md) - Esempi pratici e modelli di implementazione
* [Funzionalità intelligenti e IA](ai-features.md) - Informazioni su Assistente IA, ottimizzazione dell&#39;ora di invio e generazione di contenuti
* [Guida all&#39;interfaccia utente](user-interface.md) - Esplorare Journey Optimizer in modo efficace

**Rimani aggiornato:**

* [Note sulla versione](../rn/release-notes.md) - Funzioni, miglioramenti e correzioni più recenti
* [Aggiornamenti alla documentazione](../rn/documentation-updates.md) - Tracciare le recenti modifiche alla documentazione
* **Notifiche sui prodotti** - Abilita gli avvisi nel tuo [profilo Adobe Experience Cloud](https://experience.adobe.com/preferences){target="_blank"} per ricevere notifiche su nuove versioni, finestre di manutenzione e annunci importanti. Fai clic sull’icona del profilo > Preferenze > Notifiche per configurare.

**Community e supporto:**

* [Community Experience League](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer){target="_blank"} - Connettersi con altri utenti ed esperti
* [Forum dei prodotti](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer){target="_blank"} - Fai domande e condividi le tue conoscenze
