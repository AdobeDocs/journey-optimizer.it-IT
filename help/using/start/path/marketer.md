---
solution: Journey Optimizer
product: journey optimizer
title: Guida introduttiva di Journey Optimizer per marketer
description: In qualità di professionista di percorso, scopri di più su come utilizzare Journey Optimizer
level: Beginner
feature: Get Started
Role: User
exl-id: 34304142-3ee8-4081-94b9-e914968c75ba
source-git-commit: e86fa9f6e62aea9dd1f7e6d35e7cf4b20f79aaa6
workflow-type: tm+mt
source-wordcount: '1192'
ht-degree: 6%

---

# Introduzione per marketer {#get-started-marketers}

Come **marketer** o **esperto di percorsi**, sei responsabile della creazione di offerte e percorsi e della progettazione del contenuto. Una volta che l’[amministratore di sistema](administrator.md) e il [Data Engineer](data-engineer.md) ti avranno concesso l’accesso e avranno preparato il tuo ambiente, puoi iniziare a lavorare con [!DNL Adobe Journey Optimizer].

## Introduzione alle funzionalità di base

Journey Optimizer ti consente di creare esperienze cliente personalizzate e connesse per e-mail, SMS, push, in-app, web, schede di contenuto e altro ancora. Collabora con i tuoi [amministratori](administrator.md) per ottenere l&#39;accesso e con [Data Engineer](data-engineer.md) per configurare tipi di pubblico e dati.

Per iniziare a creare esperienze, segui i passaggi principali seguenti:

1. **Creare tipi di pubblico**. Crea tipi di pubblico tramite le definizioni dei segmenti, carica file CSV o utilizza la composizione del pubblico. Journey Optimizer offre diversi modi per rivolgersi ai clienti giusti. Ulteriori informazioni su [tipi di pubblico](../../audience/about-audiences.md) e [creazione di definizioni di segmenti](../../audience/creating-a-segment-definition.md).

1. **Progetta contenuto**. Creare messaggi convincenti su tutti i canali:
   * Utilizza l&#39;**Assistente AI** per generare contenuti e-mail, oggetti e immagini in base alle linee guida del tuo marchio. [Informazioni sulla generazione di contenuti di IA](../../content-management/gs-generative.md)
   * **Personalizzare i messaggi** con dati del cliente, contenuto dinamico e logica condizionale. [Scopri la personalizzazione](../../personalization/personalize.md)
   * **Sposta i dati contestuali** per visualizzare elenchi dinamici da eventi, azioni personalizzate e ricerche di set di dati. [Informazioni sull&#39;iterazione dei dati contestuali](../../personalization/iterate-contextual-data.md)
   * Crea **modelli di contenuto** e **frammenti** riutilizzabili per mantenere la coerenza del brand. [Utilizzare i modelli](../../content-management/content-templates.md)
   * Gestione delle risorse con l&#39;integrazione di **Adobe Experience Manager Assets**. [Informazioni sulle risorse](../../integrations/assets.md)

   ![](../assets/perso_ee2.png)

1. **Aggiungi offerte e decisioni**. Distribuisci l’offerta migliore a ogni cliente al momento giusto utilizzando le decisioni basate sull’intelligenza artificiale. Scopri di più su [Gestione delle decisioni](../../offers/get-started/starting-offer-decisioning.md) e [Experience Decisioning](../../experience-decisioning/gs-experience-decisioning.md).

   ![](../assets/offers-e2e-offers-displayed.png)

1. **Testare e convalidare**. Anteprima e verifica del contenuto prima dell’invio:
   * Utilizza **profili di test** per visualizzare in anteprima la personalizzazione e controllare il rendering tra dispositivi
   * Prova con **dati di esempio** da file CSV/JSON
   * Anteprima del **rendering di e-mail** tra i client e-mail più popolari
   * Imposta **flussi di lavoro di approvazione** per campagne e percorsi (richiede una licenza aggiuntiva)

   Scopri come [verificare e convalidare i messaggi](../../content-management/preview-test.md).

1. **Crea percorsi di clienti**. Crea esperienze personalizzate in tempo reale utilizzando l’area di lavoro del percorso:

   * Attiva percorsi con **eventi** (azioni del cliente) o **tipi di pubblico** (invii batch)
   * Aggiungi **condizioni** per creare percorsi personalizzati in base ai dati del cliente
   * Utilizza **attività di attesa** per creare un intervallo perfetto tra i messaggi
   * Invia messaggi tra **più canali** in un percorso
   * Applica **Test A/B** per ottimizzare l&#39;efficacia del percorso
   * Utilizza **ricerca set di dati** per arricchire i percorsi con dati in tempo reale da Adobe Experience Platform. [Informazioni sulla ricerca del set di dati](../../building-journeys/dataset-lookup.md)
   * Sfrutta **identificatori supplementari** per consentire allo stesso profilo di immettere più istanze di percorso (ad esempio, ordini o prenotazioni diversi). [Ulteriori informazioni sugli identificatori supplementari](../../building-journeys/supplemental-identifier.md)

   ![](../assets/journey-design.png)

   Scopri come [progettare ed eseguire percorsi](../../building-journeys/journey-gs.md) ed esplorare [casi d&#39;uso percorsi](../../building-journeys/jo-use-cases.md). Comprendere i criteri di [entrata/uscita](../../building-journeys/entry-exit-criteria-guide.md) per controllare il flusso del profilo.

1. **Monitora e ottimizza**. Monitora le prestazioni e migliora i risultati nel tempo:
   * Monitora le prestazioni di **live percorsi** e identifica i colli di bottiglia
   * Analizza **tassi di recapito messaggi** e metriche di coinvolgimento
   * Utilizza **dashboard di reporting** con l&#39;integrazione di Customer Journey Analytics
   * Tracciamento **conversione** e impatto aziendale

   Scopri come [monitorare le prestazioni](../../reports/report-gs-cja.md).

## Sfruttare le funzionalità più recenti

Journey Optimizer si evolve continuamente con nuove funzioni per migliorare l&#39;efficacia del marketing:

* **Schede di contenuto**: consegna di messaggi persistenti e non intrusivi all&#39;interno di app mobili e siti Web che gli utenti possono utilizzare quando lo desiderano. A differenza delle notifiche push, le schede di contenuto rimangono visibili fino a quando non vengono chiuse. [Informazioni sulle schede dei contenuti](../../content-card/create-content-card.md)

* **Gestione dei conflitti e definizione delle priorità**: controlla la frequenza dei messaggi ed evita la comunicazione eccessiva con le regole di limitazione avanzate. Imposta i punteggi di priorità per garantire che i messaggi più importanti arrivino prima ai clienti. [Informazioni sulla gestione dei conflitti](../../conflict-prioritization/gs-conflict-prioritization.md)

* **Ottimizzazione dell&#39;ora di invio basata sull&#39;intelligenza artificiale**: consente all&#39;intelligenza artificiale di prevedere il tempo di invio ottimale per ogni cliente in base ai modelli di coinvolgimento storici, aumentando le percentuali di apertura e clic fino al 10%. [Informazioni sull&#39;ottimizzazione dell&#39;ora di invio](../../building-journeys/send-time-optimization.md)

* **Multi-Armed Bandit Experimentation**: alloca automaticamente più traffico alle varianti vincenti in tempo reale durante il test, ottimizzando i risultati senza attendere il completamento del test. [Informazioni sulla sperimentazione](../../content-management/content-experiment.md)

* **Flussi di lavoro di approvazione**: implementa i processi di revisione per campagne e percorsi prima che vengano pubblicati (disponibili con un&#39;ulteriore licenza). [Informazioni sulle approvazioni](../../test-approve/gs-approval.md)

## Best practice per il successo

### Creazione di contenuti

* **Inizia con i modelli**: utilizza modelli e frammenti di contenuto predefiniti per velocizzare la creazione e mantenere la coerenza
* **Test anticipato, test frequente**: visualizza sempre l&#39;anteprima del contenuto tra i dispositivi e utilizza i profili di test per convalidare la personalizzazione
* **Sfruttare l&#39;intelligenza artificiale con saggezza**: utilizza l&#39;Assistente IA per le bozze e le varianti iniziali, ma rivedi e perfeziona sempre la voce del tuo marchio
* **Semplicità**: i messaggi chiari e concisi con inviti all&#39;azione efficaci offrono prestazioni migliori rispetto ai layout complessi

### Progettazione percorso

* **Definisci obiettivi chiari**: stabilisci le metriche di successo prima di creare il percorso
* **Mappa la customer experience**: visualizza l&#39;intero percorso prima dell&#39;implementazione
* **Utilizzare le attività di attesa in modo strategico**: lascia ai clienti il tempo di interagire prima di inviare i follow-up
* **Pianificare le strategie di uscita**: definire quando e perché i clienti devono uscire dal percorso
* **Test in modalità bozza**: convalida logica di percorso con esecuzione in prova prima dell&#39;attivazione

[Scopri le best practice per i percorsi](../../building-journeys/entry-exit-criteria-guide.md#best-practices)

### Targeting del pubblico

* **Segmento attento**: crea segmenti di pubblico specifici e actionable in base a criteri chiari
* **Aggiorna regolarmente**: assicurati che i tipi di pubblico rimangano aggiornati impostando pianificazioni di valutazione appropriate
* **Bilanciamento dimensioni e precisione**: i tipi di pubblico di destinazione sono sufficientemente grandi per la rilevanza statistica, ma sufficientemente specifici per la rilevanza
* **Usa attributi di arricchimento**: sfrutta attributi calcolati e dati di arricchimento per una personalizzazione più approfondita

### Gestione della frequenza

* **Rispetta le preferenze del cliente**: rispetta le rinunce e le preferenze di comunicazione
* **Impostare i limiti di frequenza**: utilizzare i set di regole per evitare l&#39;affaticamento dei messaggi tra i canali
* **Coordinare le campagne**: utilizza la gestione dei conflitti per garantire che i clienti ricevano il messaggio giusto al momento giusto
* **Coinvolgimento monitor**: verifica la presenza di segni di affaticamento (riduzione dei tassi di apertura, aumento degli annullamenti di abbonamenti)

[Scopri il limite di frequenza](../../conflict-prioritization/channel-capping.md)

## Esplora casi d’uso

Scopri alcuni esempi pratici che illustrano le funzionalità di Journey Optimizer:

**Casi d&#39;uso comuni:**

* **Serie di benvenuto**: consente di integrare nuovi clienti con percorsi personalizzati e in più passaggi. [Visualizza caso d&#39;uso](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding)
* **Ripristino carrello abbandonato**: coinvolgi nuovamente i clienti che hanno lasciato elementi nel carrello. [Visualizza caso d&#39;uso](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart)
* **Campagne di ricoinvolgimento**: riconquista i clienti inattivi con offerte mirate. [Visualizza caso d&#39;uso](https://experienceleague.adobe.com/it/docs/experience-platform/rtcdp/use-cases/personalization-insights-engagement/use-cases-luma)
* **Campagne di compleanno**: invia messaggi di compleanno personalizzati con offerte speciali
* **Consigli sui prodotti**: suggerisci prodotti rilevanti in base alla cronologia di navigazione e acquisto
* **Messaggistica basata su eventi**: rispondi alle azioni dei clienti in tempo reale

**Modelli di Percorso:**

* [Inviare messaggi ai sottoscrittori](../../building-journeys/message-to-subscribers-uc.md): elenchi di sottoscrizioni di destinazione con contenuto personalizzato
* [Messaggistica multicanale](../../building-journeys/journeys-uc.md): combina e-mail e push con eventi di reazione
* [E-mail solo per il giorno feriale](../../building-journeys/weekday-email-uc.md): pianifica le comunicazioni utilizzando condizioni basate sul tempo

Sfoglia la [libreria dei casi d&#39;uso di percorso](../../building-journeys/jo-use-cases.md) completa per altri modelli e implementazioni.

## Collaborare con altri ruoli

Il tuo lavoro di marketing si connette con altri team:

* **Lavora con [Data Engineer](data-engineer.md)**: richiedi nuovi attributi calcolati, fornisci feedback sulla qualità del pubblico e coordina i requisiti dei dati
* **Lavora con [Sviluppatori](developer.md)**: allinea i trigger degli eventi, verifica le implementazioni mobili e convalida il tracciamento
* **Lavora con [Amministratori](administrator.md)**: richiedi configurazioni del canale, segnala i problemi con le autorizzazioni e coordina l&#39;abilitazione della nuova funzionalità

## Rimani aggiornato

Tieniti al passo con le funzionalità di marketing e le funzionalità di Journey Optimizer più recenti:

* **[Note sulla versione](../../rn/release-notes.md)**: rivedi le nuove funzioni, gli aggiornamenti dei canali e i miglioramenti rilasciati ogni mese
* **[Aggiornamenti alla documentazione](../../rn/documentation-updates.md)**: tieni traccia delle modifiche recenti, inclusi nuovi casi d&#39;uso, best practice e documentazione delle funzioni
* **Notifiche prodotto**: abilita le notifiche nel tuo [profilo Adobe Experience Cloud](https://experience.adobe.com/preferences){target="_blank"} per ricevere avvisi su:
   * Nuovi canali e funzionalità disponibili
   * Prossimi avvii di funzionalità e programmi beta
   * Best practice e opportunità di formazione
   * Annunci importanti che influiscono sulle campagne

  Per abilitare le notifiche, fai clic sull&#39;icona del tuo profilo in alto a destra di Adobe Experience Cloud, vai a **Preferenze > Notifiche** e configura le preferenze per le notifiche Journey Optimizer.

## Passaggi successivi

1. **Inizia piccolo**: crea un semplice percorso di benvenuto o una campagna con un singolo messaggio per imparare a utilizzare la piattaforma
2. **Sfrutta l&#39;intelligenza artificiale**: utilizza l&#39;Assistente di intelligenza artificiale per porre domande e accelerare la creazione dei contenuti
3. **Iscriviti alla community**: connettiti con altri utenti Journey Optimizer nella [community Experience League](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer){target="_blank"}
4. **Esplora i tutorial**: guarda i video con istruzioni dettagliate su [Experience League](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=it){target="_blank"}
