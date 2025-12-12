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
source-git-commit: 5ff7987c00afda3263cb97654967c5b698f726c2
workflow-type: tm+mt
source-wordcount: '1177'
ht-degree: 20%

---


# Ruoli e responsabilità

Adobe Journey Optimizer consente ai brand di offrire percorsi di clienti connessi e contestualizzati per l’intero ciclo di vita del cliente. Consente ai team di personalizzare le interazioni su larga scala e allinea le aspettative della clientela con gli obiettivi aziendali. Questa documentazione spiega i ruoli chiave per l’utilizzo efficace di Journey Optimizer, le rispettive responsabilità e come iniziare.

**Nota importante:** Adobe Journey Optimizer definisce ruoli distinti con responsabilità specifiche. Un singolo utente può svolgere più ruoli o tutti i ruoli, a seconda della struttura dell’organizzazione.

## Guide rapide basate sul ruolo

Per semplificare l’implementazione, Adobe Journey Optimizer organizza le attività in ruoli specifici in base alle competenze. Ogni ruolo si incentra sulle attività essenziali necessarie per fornire un’esperienza cliente fluida.

| Ruolo | Responsabilità principali | Competenze chiave | Attività tipiche |
|-------------------|----------------------------------|--------------------------------|-----------------------------------------------|
| **Amministratore** | Configurazione dell’ambiente e gestione degli accessi | Configurazione sistema, gestione utenti, sicurezza | Configurare le sandbox, gestire le autorizzazioni e configurare le configurazioni dei canali |
| **Data Engineer** | Base dati e architettura | Modellazione dati, schemi XDM, qualità dei dati | Creare schemi e set di dati, configurare l’acquisizione dei dati, gestire il ciclo di vita dei dati |
| **Sviluppatore** | Implementazione e integrazioni tecniche | Mobile/Web SDK, API, architettura basata su eventi | Integrare gli SDK, implementare gli eventi, generare endpoint di azione personalizzati |
| **Marketer** | Progettazione ed esecuzione dell’esperienza del cliente | Progettazione di percorsi, creazione di contenuti, analisi dei dati | Creare percorsi, contenuti personalizzati, ottimizzare le campagne |

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

Concentrati sulla creazione di esperienze cliente personalizzate su tutti i canali.

**Funzionalità chiave da utilizzare:**

* Creare tipi di pubblico e creare segmenti con più metodi (definizioni di segmenti, caricamento CSV, composizione del pubblico)
* Progettare contenuti con l’Assistente AI per la generazione di testo e immagini
* Creare percorsi di clienti multicanale con la finestra di progettazione con trascinamento della selezione
* Ottimizzazione del tempo di invio e gestione dei conflitti per ottimizzare il coinvolgimento
* Test del contenuto e utilizzo dei flussi di lavoro di approvazione prima della pubblicazione
* Monitorare le prestazioni con dashboard di reporting integrate

**Inizia con:** Crea una semplice campagna di benvenuto per il percorso o una campagna di recupero del carrello abbandonata utilizzando modelli predefiniti.

[Introduzione al ruolo di → addetto al marketing](path/marketer.md)

### Per data engineer {#for-data-engineers}

Stabilisci la base di dati che alimenta le esperienze personalizzate.

**Responsabilità chiave:**

* Creare spazi dei nomi delle identità e configurare la risoluzione delle identità
* Progettare schemi XDM per dati di profilo ed eventi (standard e relazionali)
* Configurare i set di dati e abilitarli per Real-time Customer Profile
* Configurare i connettori di origine per l’acquisizione di dati in batch e in streaming
* Creare attributi calcolati per semplificare la segmentazione
* Configurare eventi e origini dati per l&#39;esecuzione del percorso
* Gestione della qualità dei dati, della governance e del ciclo di vita

**Inizia con:** Configura gli spazi dei nomi delle identità e crea il tuo primo schema di profilo con i gruppi di campi richiesti.

[Introduzione al ruolo di data engineer →](path/data-engineer.md)

### Per gli amministratori {#for-administrators}

Imposta e gestisci l’ambiente Journey Optimizer per la tua organizzazione.

**Responsabilità chiave:**

* Creare e gestire sandbox per sviluppo, test e produzione
* Configurare ruoli e autorizzazioni utilizzando ruoli predefiniti o personalizzati
* Applicazione del controllo dell&#39;accesso a livello di oggetto (OLAC) alle risorse protette
* Configurare le configurazioni del canale per le schede e-mail, SMS, push, in-app, web e di contenuto
* Delega dei sottodomini e crea pool IP per il recapito messaggi e-mail
* Gestire elenchi e elenchi Consentiti di soppressione
* Configurare i criteri di consenso e la governance dei dati (con Healthcare/Privacy Shield)

**Inizia con:** Configura le sandbox, imposta i ruoli e le autorizzazioni di base, quindi collabora con il tuo team nelle configurazioni dei canali.

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
