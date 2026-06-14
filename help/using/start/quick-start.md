---
solution: Journey Optimizer
product: journey optimizer
title: Ruoli e responsabilità
description: Scopri i diversi ruoli coinvolti in Adobe Journey Optimizer e le rispettive responsabilità
feature: Get Started
topic: Get Started
role: Admin, Developer, User
level: Beginner
keywords: ruoli, responsabilità, marketer, amministratore, data engineer, sviluppatore, avvio rapido
exl-id: 71ab7369-fd84-46eb-95d2-941bd887d565
redpen-status: PASS_||_2025-04-28_15-13-07
TQID: https://experienceleague.adobe.com/q9oP-s1hGrvEkbJ-JIOUReaOeSj2k79W3mw6MbvGvYY
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
subfeature_v2:
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b23e006f-0a29-4f1d-8fd0-77aa56f3d12b
  - id: b4dd41a7-ccf8-4e9d-918e-acaab534a307
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: e9001ce2-5245-4a8e-8601-dd958009072f
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
source-git-commit: 46a5a6dc0a3486633a1a71f8bba8a3cd53aaa618
workflow-type: tm+mt
source-wordcount: 2300
ht-degree: 98%

---

# Ruoli e responsabilità

>[!BEGINSHADEBOX]

**In questa pagina:** Comprendi i ruoli chiave in un&#39;implementazione di Adobe Journey Optimizer e le relative responsabilità in modo da trovare il punto di partenza e le attività di avvio rapido corretti per il tuo team.

>[!ENDSHADEBOX]

Adobe Journey Optimizer consente ai brand di offrire esperienze connesse, contestuali e personalizzate per l’intero percorso cliente. Sviluppato con un approccio end-to-end orientato alla scalabilità, alla velocità e alla flessibilità, Journey Optimizer combina tre principali fattori di valore in un’applicazione unificata:

* **Insight cliente in tempo reale e coinvolgimento** basati sul profilo cliente in tempo reale di Adobe
* **Orchestrazione omnicanale moderna** tramite aree di lavoro unificate per percorsi in tempo reale e campagne batch, oltre a un moderno designer messaggi
* **Decisioni intelligenti e personalizzazione** tramite gestione delle decisioni e funzionalità IA/ML

Journey Optimizer offre due approcci principali per raggiungere e coinvolgere la clientela:

* **Percorsi**: orchestrazione in tempo reale e individuale, in cui ogni cliente procede secondo il proprio ritmo, attivata in base a comportamento o eventi. Ideale per sequenze di onboarding, abbandono del carrello e coinvolgimento nel ciclo di vita.
* **Campagne**: messaggistica basata sul pubblico con tre modalità di consegna a seconda del caso d’uso:
   * **Campagne di azione**: messaggi pianificati o ricorrenti inviati contemporaneamente a un pubblico definito. Ideale per newsletter, annunci promozionali e lanci di prodotti.
   * **Campagne attivate da API**: messaggi su richiesta attivati da un sistema esterno tramite API. Ideale per messaggi transazionali come conferme d’ordine, avvisi di spedizione e notifiche dell’account.
   * **Campagne orchestrate**: flussi di lavoro batch complessi con segmentazione di più entità ed esecuzione basata su area di lavoro. Ideale per promozioni stagionali, programmi batch con più passaggi e campagne che richiedono conteggi precisi prima dell’invio.

Questa esperienza unificata ti consente di implementare interi casi d’uso in un’unica posizione, dalla definizione di tipi di pubblico e la progettazione di percorsi alla creazione di contenuti personalizzati e all’analisi dei risultati. Questa documentazione spiega i ruoli chiave per l’utilizzo efficace di Journey Optimizer, le rispettive responsabilità e come iniziare.

**Nota importante:** Adobe Journey Optimizer definisce ruoli distinti con responsabilità specifiche. Un singolo utente può svolgere più ruoli o tutti i ruoli, a seconda della struttura dell’organizzazione.

>[!NOTE]
>
>* I componenti e le funzionalità disponibili nell’ambiente dipendono dalle [autorizzazioni](../administration/permissions.md) e dal [pacchetto di licenze](https://helpx.adobe.com/it/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}. Per qualsiasi domanda, contatta il tuo Adobe Customer Success Manager o il tuo rappresentante Adobe.
>
>* Le linee guida e le procedure generali sulla privacy di Adobe Experience Cloud sono applicabili anche a [!DNL Journey Optimizer]. [Ulteriori informazioni sulla privacy di Adobe Experience Cloud](https://www.adobe.com/it/privacy/experience-cloud.html){target="_blank"}.

## Prima di iniziare {#before-you-begin}

Un’implementazione di successo inizia con la preparazione. Prima di configurare Journey Optimizer, allinea il team a quanto segue:

* **Definire prima i casi d’uso**: identifica quali scenari cliente desideri affrontare e assegna loro un ordine di priorità. Questo guida ogni decisione di configurazione, dalla [gestione dati](../data/gs-data.md) alla [configurazione del canale](../configuration/get-started-configuration.md).
* **Coinvolgere tutti i team hanno un impatto sull’esperienza cliente**: un’implementazione di Journey Optimizer in genere coinvolge i reparti di marketing, IT, dati e operazioni. L’allineamento anticipato tra i team evita eventuali rielaborazioni.
* **Stabilire un identificatore cliente condiviso**: concorda un identificatore comune (ad esempio un ID CRM o un indirizzo e-mail) esistente in tutte le origini dati. Questo costituisce la base dei [profili cliente unificati](../audience/get-started-profiles.md).
* **Verificare la conformità alla privacy dei dati**: prima dell’acquisizione, assicurati che tutte le origini dati che intendi connettere siano conformi alle [normative sulla privacy](../privacy/get-started-privacy.md) applicabili.
* **Pianificare il test prima del lancio**: verifica che i [trigger di evento, le condizioni di percorso e le azioni di canale](../building-journeys/journey-gs.md) si comportino come previsto in una sandbox di sviluppo o di staging.
* **Preparare i contenuti del brand e la libreria di risorse**: identifica le risorse digitali, i modelli e le linee guida del brand che il tuo team utilizzerà nei percorsi e nelle campagne. Caricandoli prima del lancio nella [libreria di risorse integrata](../integrations/assets.md) di Journey Optimizer, accelera la creazione dei messaggi e garantisce la coerenza del brand fin dal primo giorno.

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
   * Configurare le configurazioni dei canali (e-mail, SMS, push, push web, in-app, web, direct mail, schede contenuto)
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
   * Implementare Web SDK per esperienze web e notifiche push web
   * Inviare eventi dalle applicazioni per attivare i percorsi
   * Creare endpoint delle azioni personalizzate per le integrazioni di sistemi esterni
   * Monitorare lo stato e le prestazioni delle azioni personalizzate
   * Testare le implementazioni tramite Adobe Experience Platform Assurance

4. **Marketer**: progetta ed esegue le esperienze cliente\
   I marketer sfruttano tutto il lavoro di base per creare percorsi, contenuti e ottimizzare le esperienze cliente su tutti i canali.
   * Creare tipi di pubblico utilizzando segmentazione, caricamento CSV o composizione del pubblico
   * Progettare contenuti personalizzati con l’Assistente IA e i modelli
   * Creare percorsi multicanale con trigger di eventi e pubblico
   * Testare con flussi di lavoro di approvazione prima del lancio
   * Monitorare le prestazioni e ottimizzare in base agli insight di reporting

**Nota:** anche se questa sequenza è tipica, alcune attività possono verificarsi in parallelo. Ad esempio, gli sviluppatori possono lavorare sulle integrazioni delle app mentre i data engineer configurano gli schemi.

## Introduzione per ruolo

Ogni ruolo inizia con attività specifiche personalizzate in base al rispettivo punto di interesse. Il completamento di questi passaggi iniziali garantisce un onboarding e un allineamento più fluidi con il processo di implementazione generale:

### Per i marketer {#for-marketers}

In qualità di marketer o di professionista di business, puoi progettare percorsi cliente per offrire esperienze personali e contestuali in tutti i punti di contatto. Lavorerai in un’interfaccia unificata per implementare interi casi d’uso dall’inizio alla fine.

**Funzionalità principali che utilizzerai:**

* **Journey Orchesration**: crea un coinvolgimento cliente individuale e in tempo reale in cui ogni persona procede secondo il proprio ritmo, attivato in base al comportamenti o agli eventi nei vari canali. Utilizza l’attività Azione unificata per tutte le azioni dei canali, l’attività Decisione sul contenuto per integrare le offerte nei percorsi e Agente Journey per creare percorsi da prompt in linguaggio naturale
* **Orchestrazione della campagna**: progetta e automatizza campagne batch complesse e in più passaggi su larga scala utilizzando un’area di lavoro visiva. Perfetto per campagne avviate dal brand come promozioni stagionali, lanci di prodotti e comunicazioni basate su account. Sfrutta la segmentazione di più entità per creare tipi di pubblico precisi collegando i dati cliente a entità correlate (account, acquisti, prenotazioni). Utilizzare l’invio in scaglioni per inviare messaggi in batch controllati
* **Designer messaggi moderno**: progetta e personalizza messaggi e-mail e per dispositivi mobili con un’interfaccia a trascinamento. Modificare modelli predefiniti per accelerare il time-to-market
* **Gestione delle decisioni**: crea e gestisci offerte, regole di idoneità e altri componenti in una libreria centralizzata che possono essere incorporati nelle e-mail e nei punti di contatto cliente. Utilizzare la funzione Decisioni per la personalizzazione push e SMS
* **Gestione risorse**: accedi ad Adobe Experience Manager Assets Essentials completamente incorporato in Journey Optimizer per accedere e consegnare le risorse in modo semplice
* **Definizione pubblico**: crea tipi di pubblico on-demand con ottimizzazione immediata utilizzando query relazionali, con visibilità pre-invio per conteggi accurati del pubblico
* **Servizi IA/ML**: sfrutta l’ottimizzazione dell’ora di invio e punteggi di coinvolgimento predittivi per il targeting di clienti di alto valore e per ridurre al minimo il rischio di abbandono
* **Controllo della consegna**: utilizza le ore di silenzio (esclusioni basate sul tempo) e la gestione dei conflitti per rispettare le preferenze del cliente ed evitare comunicazioni eccessive

**Inizia con:** modelli di casi d’uso e procedure guidate per creare e implementare facilmente nuovi percorsi cliente. Utilizza Agente Journey per creare percorsi dai prompt in linguaggio naturale.

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

**Inizia con:** la revisione della panoramica di [Introduzione alla gestione dei dati](../data/gs-data.md) per comprendere schemi, set di dati, identità e l’elenco di controllo completo per la configurazione dei dati. Quindi modella il tuo primo schema del profilo cliente e configura un connettore di origine per iniziare ad acquisire i dati.

[Introduzione al ruolo di data engineer →](path/data-engineer.md)

### Per amministratori {#for-administrators}

In qualità di amministratore, devi impostare l’ambiente Journey Optimizer per consentire ai team di lavorare in modo efficiente e sicuro.

**Responsabilità chiave:**

* **Sandbox**: crea e gestisci sandbox per partizionare dati e percorsi per diversi gruppi di utenti (sviluppo, test, produzione)
* **Gestione utenti**: imposta gruppi di utenti e autorizzazioni per controllare l’accesso a diverse funzionalità
* **Impostazione canale**: configura i canali di consegna e i predefiniti per messaggi per garantire un branding coerente tra i messaggi e le risorse consegnate tramite Journey Optimizer
* **Sicurezza e governance**: applica il controllo degli accessi a livello di oggetto (OLAC), configura i criteri di consenso e implementa i criteri di governance dei dati
* **Recapitabilità**: delega sottodomini, esegui la migrazione dei sottodomini verso una delega personalizzata quando necessario, crea pool IP e gestisci elenchi di soppressione ed elenchi consentiti
* **Configurazione dei percorsi**: configura gli elementi e le configurazioni dei percorsi per i team
* **Configurazione dei canali**: configura notifiche push web, direct mail ed esportazione dei messaggi (e-mail/SMS) quando necessario

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
* [Introduzione alla gestione dei dati](../data/gs-data.md): schemi, set di dati, identità ed elenco di controllo della preparazione dei dati per Journey Optimizer
* [Libreria casi d’uso del percorso](../building-journeys/jo-use-cases.md): esempi pratici e modelli di implementazione
* [Funzioni intelligenti e IA](ai-features.md): scopri l’Assistente IA, l’ottimizzazione dell’ora di invio e la generazione di contenuti
* [Guida all’interfaccia utente](user-interface.md): esplora Journey Optimizer in modo efficace

>[!TAB Resta aggiornato]

* [Note sulla versione](../rn/release-notes.md): funzioni, miglioramenti e correzioni più recenti
* [Aggiornamenti della documentazione](../rn/documentation-updates.md): tieni traccia delle modifiche più recenti alla documentazione
* [Notifiche sui prodotti](../rn/releases.md#staying-informed): scopri come abbonarti agli avvisi e-mail e nel prodotto per gli aggiornamenti di Journey Optimizer

>[!TAB Community e supporto]

* [Community Experience League](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer?profile.language=it){target="_blank"}: connettiti con altri utenti ed esperti
* [Forum prodotti](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer?profile.language=it){target="_blank"}: fai domande e condividi le tue conoscenze

>[!ENDTABS]
