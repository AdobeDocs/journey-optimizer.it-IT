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
source-git-commit: d3765f66beff13aaf77cd585c5da5f93c44fa1df
workflow-type: ht
source-wordcount: '1724'
ht-degree: 100%

---


# Ruoli e responsabilità

Adobe Journey Optimizer consente ai brand di offrire esperienze connesse, contestuali e personalizzate per l’intero percorso cliente. Sviluppato con un approccio end-to-end orientato alla scalabilità, alla velocità e alla flessibilità, Journey Optimizer combina tre principali fattori di valore in un’applicazione unificata:

* **Insight cliente in tempo reale e coinvolgimento** basati sul profilo cliente in tempo reale di Adobe
* **Orchestrazione omnicanale moderna** tramite aree di lavoro unificate per percorsi in tempo reale e campagne batch, oltre a un moderno designer messaggi
* **Decisioni intelligenti e personalizzazione** tramite gestione delle decisioni e funzionalità IA/ML

Journey Optimizer offre due approcci di orchestrazione per soddisfare diverse esigenze di marketing:

* **Percorsi**: ideale per un coinvolgimento individuale in tempo reale, in cui ogni cliente procede secondo il proprio ritmo, attivato da comportamenti o eventi
* **Campagne orchestrate**: ideale per campagne batch, uno-a-molti in cui il pubblico procede insieme attraverso flussi di lavoro con più passaggi secondo una pianificazione, ideale per promozioni stagionali, lanci di prodotti e comunicazioni basate su account

Questa esperienza unificata ti consente di implementare interi casi d’uso in un’unica posizione, dalla definizione di tipi di pubblico e la progettazione di percorsi alla creazione di contenuti personalizzati e all’analisi dei risultati. Questa documentazione spiega i ruoli chiave per l’utilizzo efficace di Journey Optimizer, le rispettive responsabilità e come iniziare.

**Nota importante:** Adobe Journey Optimizer definisce ruoli distinti con responsabilità specifiche. Un singolo utente può svolgere più ruoli o tutti i ruoli, a seconda della struttura dell’organizzazione.

## Guide rapide basate sul ruolo

Per semplificare l’implementazione, Adobe Journey Optimizer organizza le attività in ruoli specifici in base all’esperienza. Ogni ruolo si incentra sulle attività essenziali necessarie per fornire un’esperienza cliente fluida.

| Ruolo | Responsabilità principali | Competenze chiave | Attività tipiche |
|-------------------|----------------------------------|--------------------------------|-----------------------------------------------|
| **Amministratore** | Impostazione dell’ambiente e gestione degli accessi | Configurazione sistema, gestione utenti, sicurezza | Impostare sandbox, gestire le autorizzazioni utente, configurare canali e predefiniti per messaggi |
| **Data Engineer** | Dati del profilo cliente e origini dati | Modellazione dati, schemi XDM, connettori di origine | Modellare profilo e dati aziendali in schemi, configurare connettori di origine, monitorare l’acquisizione di dati |
| **Sviluppatore** | Implementazione tecnica e integrazioni | Mobile/Web SDK, API, architettura basata su eventi | Integrare gli SDK, implementare gli eventi, generare endpoint di azioni personalizzate |
| **Marketer** | Progettazione di percorsi ed esperienze personalizzate | Orchestrazione di percorsi, creazione di contenuti, targeting del pubblico | Progettare percorsi cliente, creare e personalizzare messaggi, gestire offerte e componenti decisionali, definire i tipi di pubblico |

Ogni ruolo affronta una fase specifica dell’implementazione di Adobe Journey Optimizer e garantisce un processo di implementazione strutturato ed efficiente.

## Dipendenze di ruolo e ordine di implementazione

Un’implementazione di Journey Optimizer di successo in genere segue questa sequenza, che riflette le dipendenze tra i ruoli:

1. **Amministratore**: configura l’ambiente\
   L’amministratore stabilisce le basi configurando le sandbox, impostando i controlli di accesso e preparando le configurazioni dei canali. Deve avvenire prima per consentire ad altri team di lavorare.
   * Configurare sandbox di sviluppo, staging e produzione
   * Impostare ruoli, autorizzazioni e controllo degli accessi a livello di oggetto (OLAC)
   * Configurare le configurazioni del canale (e-mail, SMS, push, in-app, web, schede contenuto)
   * Delegare i sottodomini e impostare i pool IP
   * Configurare gli elenchi di soppressione e i criteri di consenso

2. **Data Engineer**: crea la base dati\
   I data engineer creano l’infrastruttura di dati che alimenta la personalizzazione, definendo il modo in cui i dati cliente fluiscono all’interno e attraverso il sistema.
   * Creare spazi dei nomi di identità per l’identificazione cliente
   * Progettare schemi XDM (profilo, eventi esperienza, relazionali)
   * Impostare i set di dati e abilitarli per il profilo cliente in tempo reale
   * Configurare l’acquisizione di dati (batch e streaming)
   * Creare attributi calcolati per calcoli complessi
   * Configurare eventi e origini dati per i percorsi

3. **Sviluppatore**: implementa le integrazioni tecniche\
   Gli sviluppatori collegano le applicazioni a Journey Optimizer integrando SDK, inviando eventi e creando endpoint API. Queste implementazioni consentono l’attivazione e l’esecuzione dei percorsi.
   * Integrare Mobile SDK (iOS/Android) con l’impostazione delle notifiche push
   * Implementare Web SDK per esperienze web
   * Inviare eventi dalle applicazioni per attivare i percorsi
   * Creare endpoint delle azioni personalizzate per le integrazioni di sistemi esterni
   * Testare le implementazioni tramite Adobe Experience Platform Assurance

4. **Marketer**: progetta ed esegue le esperienze cliente\
   I marketer sfruttano tutto il lavoro di base per creare percorsi, contenuti e ottimizzare le esperienze cliente su tutti i canali.
   * Creare tipi di pubblico utilizzando segmentazione, caricamento CSV o composizione del pubblico
   * Progettare contenuti personalizzati con l’Assistente IA e i modelli
   * Creare percorsi multicanale con trigger di eventi e pubblico
   * Testare con flussi di lavoro di approvazione prima del lancio
   * Monitorare le prestazioni e ottimizzare in base agli insight di reporting

**Nota:** anche se questa sequenza è tipica, alcune attività possono verificarsi in parallelo. Ad esempio, gli sviluppatori possono lavorare sulle integrazioni delle app mentre i data engineer configurano gli schemi.

## Guida introduttiva per ruolo

Ogni ruolo inizia con attività specifiche personalizzate in base al rispettivo punto di interesse. Il completamento di questi passaggi iniziali garantisce un onboarding e un allineamento più fluidi con il processo di implementazione generale:

### Per i marketer {#for-marketers}

In qualità di marketer o di professionista di business, puoi progettare percorsi cliente per offrire esperienze personali e contestuali in tutti i punti di contatto. Lavorerai in un’interfaccia unificata per implementare interi casi d’uso dall’inizio alla fine.

**Funzionalità principali che utilizzerai:**

* **Journey Orchestration**: crea un coinvolgimento cliente individuale in tempo reale in cui ogni persona procede secondo il proprio ritmo, attivato da comportamenti o eventi nei vari canali
* **Orchestrazione della campagna**: progetta e automatizza campagne batch complesse e in più passaggi su larga scala utilizzando un’area di lavoro visiva. Perfetto per campagne avviate dal brand come promozioni stagionali, lanci di prodotti e comunicazioni basate su account. Sfrutta la segmentazione in più entità per creare tipi di pubblico precisi collegando i dati cliente con entità correlate (account, acquisti, prenotazioni)
* **Designer messaggi moderno**: progetta e personalizza messaggi e-mail e per dispositivi mobili con un’interfaccia a trascinamento. Modificare modelli predefiniti per accelerare il time-to-market
* **Gestione delle decisioni**: crea e gestisci offerte, regole di idoneità e altri componenti in una libreria centralizzata che possono essere incorporati nelle e-mail e nei punti di contatto cliente
* **Gestione risorse**: accedi ad Adobe Experience Manager Assets Essentials completamente incorporato in Journey Optimizer per accedere e consegnare le risorse in modo semplice
* **Definizione pubblico**: crea tipi di pubblico on-demand con ottimizzazione immediata utilizzando query relazionali, con visibilità pre-invio per conteggi accurati del pubblico
* **Servizi IA/ML**: sfrutta l’ottimizzazione dell’ora di invio e punteggi di coinvolgimento predittivi per il targeting di clienti di alto valore e per ridurre al minimo il rischio di abbandono

**Inizia con:** modelli di casi d’uso e procedure guidate per creare e implementare facilmente nuovi percorsi clienti.

[Introduzione al ruolo di marketer →](path/marketer.md)

### Per data engineer {#for-data-engineers}

In qualità di data architect o data engineer, devi impostare e gestire i dati del profilo cliente e altre origini dati che alimentano le esperienze orchestrate da Journey Optimizer.

**Responsabilità chiave:**

* **Dati profilo cliente**: modella i dati del profilo cliente e i dati aziendali in schemi per creare una visualizzazione cliente unificata a 360°
* **Modellazione dati relazionali**: per campagne orchestrate, progetta schemi relazionali per abilitare la segmentazione in più entità, collegando i dati cliente con entità correlate come account, acquisti, abbonamenti e prenotazioni per una creazione flessibile del pubblico
* **Connettori di origine**: configura i connettori di origine per acquisire in Adobe Experience Platform dati da web, CRM, dati offline e altre origini
* **Risoluzione identità**: imposta gli spazi dei nomi di identità per aggiornare continuamente i profili e spostare in tempo reale i clienti dentro e fuori i segmenti e percorsi
* **Origini dati**: configura le origini dati per l’ascolto in tempo reale di segnali esterni nel percorso cliente
* **Gestione profilo**: abilita i set di dati per il profilo cliente in tempo reale per fornire esperienze personalizzate
* **Qualità dei dati**: monitora l’acquisizione dei dati per garantire che tutto scorra senza problemi in Journey Optimizer

**Inizia con:** modella il tuo primo schema del profilo cliente e configura un connettore di origine per iniziare ad acquisire i dati.

[Introduzione al ruolo di data engineer →](path/data-engineer.md)

### Per amministratori {#for-administrators}

In qualità di amministratore, devi impostare l’ambiente Journey Optimizer per consentire ai team di lavorare in modo efficiente e sicuro.

**Responsabilità chiave:**

* **Sandbox**: crea e gestisci sandbox per partizionare dati e percorsi per diversi gruppi di utenti (sviluppo, test, produzione)
* **Gestione utenti**: imposta gruppi di utenti e autorizzazioni per controllare l’accesso a diverse funzionalità
* **Impostazione canale**: configura i canali di consegna e i predefiniti per messaggi per garantire un branding coerente tra i messaggi e le risorse consegnate tramite Journey Optimizer
* **Sicurezza e governance**: applica il controllo degli accessi a livello di oggetto (OLAC), configura i criteri di consenso e implementa i criteri di governance dei dati
* **Recapitabilità**: delega sottodomini, crea pool IP e gestisci elenchi soppressione ed elenchi consentiti
* **Configurazione dei percorsi**: configura gli elementi e le configurazioni del percorso per i team

**Inizia con:** configura le sandbox e le autorizzazioni utente, quindi imposta le configurazioni del primo canale e i predefiniti per messaggi.

[Introduzione al ruolo di amministratore →](path/administrator.md)

### Per sviluppatori {#for-developers}

Implementa integrazioni tecniche che consentono di collegare Journey Optimizer alle applicazioni.

**Responsabilità chiave:**

* Integrare Adobe Experience Platform Mobile SDK (iOS/Android)
* Implementare Web SDK per esperienze web e notifiche push web
* Configurare le credenziali e i certificati per le notifiche push
* Inviare eventi dalle applicazioni per attivare i percorsi
* Creare endpoint API che Journey Optimizer rchiama tramite azioni personalizzate
* Implementare esperienze basate su codice per web, dispositivi mobili e altre superfici
* Testare ed eseguire il debug delle implementazioni con Adobe Experience Platform Assurance
* Utilizzare le API di Journey Optimizer per l’accesso programmatico

**Inizia con:** integra Mobile o Web SDK, quindi implementa il tuo primo evento per attivare un percorso.

[Introduzione al ruolo di sviluppatore →](path/developer.md)

## Collaborazione tra ruoli

Le corrette implementazioni di Journey Optimizer richiedono collaborazione tra tutti i ruoli. Ciascun ruolo lavora con altri per fornire esperienze cliente complete:

>[!BEGINTABS]

>[!TAB Amministratori]

**Amministratori** abilita tutti i team gestendo accessi e configurazioni. Collaborano con:

* **Data engineer**: concedi autorizzazioni per la gestione dei dati, approva l’accesso sandbox, coordina i criteri di governance
* **Sviluppatori**: fornisci credenziali API, imposta ambienti di test, approva configurazioni canale
* **Marketer**: assegna autorizzazioni per percorsi/campagne, configura canali, supporta ambienti di test

>[!TAB Data engineer]

**I data engineer** forniscono le basi dati per tutti. Collaborano con:

* **Amministratori**: richiedi autorizzazioni per la gestione dei dati, coordina la governance e i criteri di conservazione
* **Sviluppatori**: fornisci schemi XDM e strutture di eventi, definisci i formati del payload dell’evento, verifica l’acquisizione dei dati
* **Marketer**: crea attributi calcolati per la personalizzazione, crea tipi di pubblico e configura schemi relazionali

>[!TAB Sviluppatori]

**Sviluppatori** implementano integrazioni tecniche che alimentano i percorsi. Collaborano con:

* **Data engineer**: ottengono schemi XDM e strutture di eventi, allineano i requisiti di raccolta dati, verificano la consegna degli eventi
* **Amministratori**: forniscono le specifiche API, richiedono autorizzazioni e credenziali, coordinano la strategia di test
* **Marketer**: comprendono i trigger degli eventi, implementano il tracciamento, supportano i test del percorso e risolvono i problemi

>[!TAB Marketer]

**Marketer** progettano le esperienze della clientela e forniscono feedback. Collaborano con:

* **Data engineer**: richiedono attributi calcolati, coordinano i requisiti del pubblico, forniscono feedback sulla qualità dei dati
* **Sviluppatori**: allineano sui trigger evento, verificano le implementazioni, convalidano il tracciamento
* **Amministratori**: richiedono le configurazioni canale, confermano l’accesso alle funzioni, coordinano l’abilitazione

>[!ENDTABS]

**Best practice:** organizza riunioni interfunzionali regolari per allineare le priorità, condividere i progressi e affrontare i blocchi tra i team.

## Video dimostrativo {#video}

Per ulteriori informazioni sugli utenti tipo e sulle funzionalità chiave di Journey Optimizer, guarda il video introduttivo. Il video illustra l’interfaccia utente ed evidenzia le funzioni chiave in base ai flussi di lavoro specifici dei ruoli.

>[!VIDEO](https://video.tv.adobe.com/v/3424995?quality=12)

## Risorse aggiuntive

Per ulteriori informazioni approfondite e aggiornamenti, consulta le risorse seguenti:

>[!BEGINTABS]

>[!TAB Apprendimento e documentazione]

* [Video tutorial](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/overview){target="_blank"}: video tutorial dettagliati per tutti i ruoli
* [Libreria casi d’uso del percorso](../building-journeys/jo-use-cases.md): esempi pratici e modelli di implementazione
* [Funzioni intelligenti e IA](ai-features.md): scopri l’Assistente IA, l’ottimizzazione dell’ora di invio e la generazione di contenuti
* [Guida all’interfaccia utente](user-interface.md): esplora Journey Optimizer in modo efficace

>[!TAB Resta aggiornato]

* [Note sulla versione](../rn/release-notes.md): funzioni, miglioramenti e correzioni più recenti
* [Aggiornamenti della documentazione](../rn/documentation-updates.md): tieni traccia delle modifiche più recenti alla documentazione
* [Notifiche sui prodotti](../rn/releases.md#staying-informed): scopri come abbonarti agli avvisi e-mail e nel prodotto per gli aggiornamenti di Journey Optimizer

>[!TAB Community e supporto]

* [Community Experience League](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer){target="_blank"}: connettiti con altri utenti ed esperti
* [Forum prodotti](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer){target="_blank"}: fai domande e condividi le tue conoscenze

>[!ENDTABS]
