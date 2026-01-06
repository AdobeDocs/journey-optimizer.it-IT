---
solution: Journey Optimizer
product: journey optimizer
title: Guida introduttiva di Journey Optimizer per marketer
description: In qualità di professionista di percorso, scopri di più su come utilizzare Journey Optimizer
level: Beginner
feature: Get Started
Role: User
exl-id: 34304142-3ee8-4081-94b9-e914968c75ba
source-git-commit: d1fd0b60ae60c2642108a1eb308564c9d04f5f9e
workflow-type: tm+mt
source-wordcount: '1476'
ht-degree: 98%

---

# Introduzione per marketer {#get-started-marketers}

In qualità di **marketer** o **professionista di business**, progetti percorsi cliente per fornire esperienze personali e contestuali alla clientela. Puoi creare e gestire tutti i vari componenti di questi percorsi personalizzati, inclusi e-mail e messaggi push, offerte e componenti decisionali, per personalizzare in modo intelligente il contenuto dei messaggi. Journey Optimizer offre un’esperienza utente unificata in cui puoi implementare interi casi d’uso end-to-end in un’unica posizione. Una volta che l’[amministratore di sistema](administrator.md) e il [Data Engineer](data-engineer.md) ti avranno concesso l’accesso e avranno preparato il tuo ambiente, puoi iniziare a utilizzare [!DNL Adobe Journey Optimizer].

## Introduzione alle basi

Journey Optimizer riunisce in un’unica applicazione insight cliente in tempo reale, orchestrazione omnicanale moderna e processi decisionali intelligenti. Crea esperienze cliente personalizzate e connesse tramite e-mail, SMS, push, in-app, web, schede contenuto e altro ancora.

Journey Optimizer offre due potenti approcci di orchestrazione:

* **Percorsi**: coinvolgimento in tempo reale e individuale, in cui ogni cliente procede secondo il proprio ritmo, attivato da comportamenti o eventi
* **Campagne orchestrate**: campagne batch complesse e in più passaggi su larga scala in cui il pubblico procede insieme attraverso i flussi di lavoro; perfetto per campagne avviate dal brand come promozioni stagionali, lanci di prodotti o comunicazioni basate su account

Collabora con i tuoi [amministratori](administrator.md) per ottenere l’accesso e con i [data engineer](data-engineer.md) per impostare tipi di pubblico, dati e schemi relazionali per la segmentazione avanzata.

Per iniziare a creare esperienze, segui i passaggi di base seguenti:

1. **Crea tipi di pubblico**. Crea tipi di pubblico tramite le definizioni dei segmenti, carica file CSV o utilizza la composizione del pubblico. Journey Optimizer offre diversi modi per eseguire il targeting dei clienti giusti. Scopri di più sui [tipi di pubblico](../../audience/about-audiences.md) e sulla [creazione di definizioni di segmenti](../../audience/creating-a-segment-definition.md).

1. **Progettare contenuti**. Crea messaggi coinvolgenti su tutti i canali, incluse e-mail, SMS, push, in-app, web e schede contenuto:
   * Utilizza l’**Assistente IA** per generare contenuti, oggetti e immagini e-mail in base alle linee guida del tuo brand. [Scopri la generazione di contenuti IA](../../content-management/gs-generative.md)
   * **Personalizza i messaggi** con dati cliente, contenuto dinamico e logica condizionale. [Scopri la personalizzazione](../../personalization/personalize.md)
   * **Esegui l’iterazione di dati contestuali** per visualizzare elenchi dinamici da eventi, azioni personalizzate e ricerche nei set di dati. [Scopri l’iterazione di dati contestuali](../../personalization/iterate-contextual-data.md)
   * Crea **modelli di contenuto** e **frammenti** riutilizzabili per mantenere la coerenza del brand. [Utilizzare i modelli](../../content-management/content-templates.md)
   * Distribuisci **schede contenuto** persistenti e non intrusive all’interno di app per dispositivi mobili e siti web. A differenza delle notifiche push, le schede contenuto rimangono visibili fino a quando non vengono chiuse. [Scopri le schede contenuto](../../content-card/create-content-card.md)
   * Gestisci le risorse con l’integrazione di **Adobe Experience Manager Assets**. [Scopri le risorse](../../integrations/assets.md)

   ![](../assets/perso_ee2.png)

1. **Aggiungere offerte e decisioni**. Distribuisci al momento giusto l’offerta migliore a ogni cliente utilizzando le decisioni basate sull’intelligenza artificiale. Scopri la [gestione delle decisioni](../../offers/get-started/starting-offer-decisioning.md) e le [decisioni per le esperienze](../../experience-decisioning/gs-experience-decisioning.md).

   ![](../assets/offers-e2e-offers-displayed.png)

1. **Testare e convalidare**. Visualizza l’anteprima e verifica il contenuto prima dell’invio:
   * Utilizza i **profili di test** per visualizzare in anteprima la personalizzazione e controllare il rendering tra dispositivi
   * Test con **dati di esempio** da file CSV/JSON
   * Anteprima del **rendering e-mail** tra i client e-mail popolari
   * Esegui i **test A/B ed esperimenti** per ottimizzare le varianti di contenuto. Utilizza la sperimentazione multi-armed bandit per allocare automaticamente più traffico alle varianti vincenti in tempo reale. [Scopri la sperimentazione](../../content-management/content-experiment.md)
   * Imposta **flussi di lavoro di approvazione** per campagne e percorsi (richiede una licenza aggiuntiva). [Scopri le approvazioni](../../test-approve/gs-approval.md)

   Scopri come [testare e convalidare i messaggi](../../content-management/preview-test.md).

1. **Creare percorsi cliente**. Crea esperienze personalizzate in tempo reale utilizzando l’area di lavoro del percorso:

   * Attiva percorsi con **eventi** (azioni del cliente) o **tipi di pubblico** (invii batch)
   * Aggiungi **condizioni** per creare percorsi personalizzati in base ai dati cliente
   * Utilizza **attività di attesa** per creare una tempistica perfetta tra i messaggi
   * Invia messaggi tra **più canali** in un percorso
   * Applica **Test A/B** e ottimizza i tempi di invio per massimizzare il coinvolgimento
   * Utilizza la **ricerca nei set di dati** per arricchire i percorsi con dati in tempo reale da Adobe Experience Platform. [Scopri la ricerca nei set di dati](../../building-journeys/dataset-lookup.md)
   * Sfrutta gli **identificatori supplementari** per consentire allo stesso profilo di inserire più istanze di percorso (ad esempio, ordini o prenotazioni diversi). [Scopri gli identificatori supplementari](../../building-journeys/supplemental-identifier.md)

   ![](../assets/journey-design.png)

   Scopri come [progettare ed eseguire percorsi](../../building-journeys/journey-gs.md) ed esplorare [casi d’uso del percorso](../../building-journeys/jo-use-cases.md). Comprendi i [criteri di entrata/uscita](../../building-journeys/entry-exit-criteria-guide.md) per controllare il flusso del profilo.

1. **Avviare campagne orchestrate**. Progetta campagne batch complesse e in più passaggi su larga scala utilizzando un’area di lavoro visiva:

   * Crea immediatamente **tipi di pubblico on-demand** utilizzando query relazionali per collegare i dati cliente con account, acquisti, iscrizioni e altre entità
   * Crea una **segmentazione di più entità** per il targeting preciso (ad esempio, “clienti con abbonamenti in scadenza tra 30 giorni” o “account con acquisti di valore elevato recenti”)
   * Ottieni **visibilità pre-invio** con conteggi accurati del pubblico prima del lancio
   * Progetta **flussi di lavoro con più passaggi** per promozioni stagionali, lanci di prodotti, offerte fedeltà o account-based marketing
   * Pianifica l’esecuzione immediata delle campagne, in orari specifici o secondo pianificazioni ricorrenti (giornaliere, settimanali, mensili)
   * Elabora i tipi di pubblico in **modalità batch** in cui tutti i profili avanzano insieme attraverso il flusso di lavoro

   Scopri come [iniziare a utilizzare le campagne orchestrate](../../orchestrated/gs-orchestrated-campaigns.md) e quando [utilizzare le campagne rispetto ai percorsi](../../orchestrated/orchestrated-campaigns-faq.md).

1. **Monitorare e ottimizzare**. Tieni traccia delle prestazioni e migliora i risultati nel tempo:
   * Monitora le prestazioni del **percorso live** e identifica gli ostacoli
   * Analizza **tassi di consegna dei messaggi** e metriche di coinvolgimento
   * Utilizza **dashboard di reporting** con l’integrazione di Customer Journey Analytics
   * Traccia **conversione** e impatto aziendale
   * Gestisci **la frequenza e la priorità dei messaggi** con regole di gestione dei conflitti per evitare comunicazioni eccessive. [Scopri la gestione dei conflitti](../../conflict-prioritization/gs-conflict-prioritization.md)

   Scopri come [monitorare le prestazioni](../../reports/report-gs-cja.md).

## Best practice per il successo

### Creazione di contenuti

* **Iniziare con i modelli**: utilizza modelli e frammenti di contenuto predefiniti per velocizzare la creazione e mantenere la coerenza
* **Test anticipato, test frequente**: visualizza sempre l’anteprima del contenuto tra i dispositivi e utilizza i profili di test per convalidare la personalizzazione
* **Sfrutta l’IA in modo intelligente**: utilizza l’Assistente IA per le bozze e le varianti iniziali, ma rivedile sempre per mantenere la voce del tuo brand
* **Semplicità**: i messaggi chiari e concisi con efficaci inviti all’azione offrono risultati migliori rispetto ai layout complessi

### Progettazione percorso

* **Definire obiettivi chiari**: stabilisci le metriche di successo prima di creare il percorso
* **Mappare l’esperienza cliente**: visualizza l’intero percorso prima dell’implementazione
* **Utilizzare le attività di attesa in modo strategico**: lascia alla clientela il tempo di interagire prima di inviare i follow-up
* **Pianificare le strategie di uscita**: definisci quando e perché la clientela deve uscire dal percorso
* **Test in modalità bozza**: convalida la logica di percorso con esecuzione di prova prima dell’attivazione

[Scopri le best practice del percorso](../../building-journeys/entry-exit-criteria-guide.md#best-practices)

### Orchestrazione della campagna

* **Scegli l&#39;approccio corretto**: [Confronta tipi di percorso](../../building-journeys/journey.md#journey-types) per esperienze attivate dal comportamento in tempo reale o [tipi di campagna](../../campaigns/get-started-with-campaigns.md#campaign-types) per campagne pianificate in batch
* **Definire obiettivi chiari della campagna**: stabilisci gli obiettivi prima di progettare flussi di lavoro in più passaggi
* **Iniziare con tipi di pubblico pilota**: convalida i conteggi e la logica di segmentazione prima del ridimensionamento
* **Sfruttare i dati relazionali**: utilizza la segmentazione di più entità per collegare i dati cliente con account, acquisti e abbonamenti per un targeting preciso
* **Segmentazione semplice**: ottimizza le prestazioni e la trasparenza con regole chiare e gestibili
* **Utilizzare denominazioni coerenti**: semplifica la gestione delle campagne con convenzioni di denominazione chiare

### Targeting del pubblico

* **Segmentazione attenta**: crea segmenti di pubblico specifici e actionable in base a criteri chiari
* **Aggiornamento regolare**: assicurati che i tipi di pubblico rimangano aggiornati impostando pianificazioni di valutazione appropriate
* **Bilanciamento tra dimensioni e precisione**: tipi di pubblico mirati sufficientemente grandi per la significatività statistica, ma sufficientemente specifici per la rilevanza
* **Usare attributi di arricchimento**: sfrutta attributi calcolati e dati di arricchimento per una personalizzazione più approfondita

### Gestione della frequenza

* **Rispettare le preferenze cliente**: tieni conto delle preferenze di comunicazione e delle rinunce
* **Impostare le quote limite**: utilizza i set di regole per evitare l’eccesso di messaggi tra i canali
* **Coordinare le campagne**: utilizza la gestione dei conflitti per garantire che la clientela riceva il messaggio giusto al momento giusto
* **Monitorare il coinvolgimento**: verifica la presenza di segni di affaticamento (riduzione dei tassi di apertura, aumento degli annullamenti di abbonamenti)

[Scopri la quota limite](../../conflict-prioritization/channel-capping.md)

## Esplora altri casi d’uso

Scopri alcuni esempi pratici che illustrano le funzionalità di Journey Optimizer:

**Casi d’uso dei percorsi** (in tempo reale, individuale):

* **Serie di benvenuto**: dai il benvenuto alla nuova clientela con percorsi personalizzati e in più passaggi. [Visualizza caso d’uso](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding)
* **Recupero carrello abbandonato**: coinvolgi nuovamente la clientela che ha lasciato articoli nel carrello. [Visualizza caso d’uso](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart)
* **Messaggistica basata su eventi**: rispondi in tempo reale alle azioni della clientela
* **Campagne di compleanno**: invia messaggi di compleanno personalizzati attivati dalle date nel profilo
* **Consigli sui prodotti**: suggerisci prodotti rilevanti in base alla cronologia di navigazione e acquisto

**Casi d’uso di campagne orchestrate** (batch, uno-a-molti):

* **Promozioni stagionali**: avvia campagne coordinate tra i segmenti di clienti (ad esempio, saldi festivi, ritorno a scuola)
* **Lanci di prodotti**: annuncia nuovi prodotti a tipi di pubblico mirati con messaggistica in sequenza
* **Offerte del programma fedeltà**: ricompensa la clientela di valore elevato con offerte su più livelli basate sulla cronologia degli acquisti
* **Account-based marketing**: account mirati con caratteristiche specifiche e contatti correlati
* **Rinnovi degli abbonamenti**: raggiungi la clientela con abbonamenti in scadenza a breve utilizzando query con più entità
* **Campagne per nuovo coinvolgimento**: riconquista la clientela inattiva con offerte mirate in modalità batch. [Visualizza caso d’uso](https://experienceleague.adobe.com/it/docs/experience-platform/rtcdp/use-cases/personalization-insights-engagement/use-cases-luma)

**Modelli di percorso:**

* [Invia messaggi agli iscritti](../../building-journeys/message-to-subscribers-uc.md): esegui il targeting di elenchi di iscrizioni con contenuti personalizzati
* [Messaggistica multicanale](../../building-journeys/journeys-uc.md): combina e-mail e push con eventi di reazione
* [E-mail solo nei giorni feriali](../../building-journeys/weekday-email-uc.md): pianifica le comunicazioni utilizzando condizioni basate sul tempo

Sfoglia la [libreria completa dei casi d’uso del percorso](../../building-journeys/jo-use-cases.md) e scopri di più sulle [campagne orchestrate](../../orchestrated/gs-orchestrated-campaigns.md).

## Collaborare tra ruoli

Il tuo lavoro di marketing si connette con altri team:

>[!BEGINTABS]

>[!TAB Lavorare con i data engineer]

Collabora con i [data engineer](data-engineer.md) sulle configurazioni di dati e pubblico:

* Richiedi nuovi attributi calcolati per la personalizzazione e la segmentazione
* Coordina gli schemi relazionali per campagne orchestrate
* Fornisci feedback sulla qualità del pubblico e sulla precisione dei dati
* Allinea i requisiti di dati in più entità per la segmentazione avanzata

>[!TAB Lavorare con gli sviluppatori]

Collabora con gli [sviluppatori](developer.md) per il tracciamento degli eventi e l’implementazione:

* Allinea le interazioni utente che devono attivare gli eventi del percorso
* Testa le implementazioni per dispositivi mobili e web prima del lancio
* Convalidare il tracciamento per le prestazioni dei contenuti e il coinvolgimento utente
* Risolvere i problemi relativi alla consegna o alla personalizzazione dei messaggi

>[!TAB Lavorare con gli amministratori]

Collabora con gli [amministratori](administrator.md) per l’accesso e le configurazioni:

* Richiedi configurazioni dei canali per campagne e percorsi
* Conferma l’accesso alla licenza per le campagne orchestrate e altre funzioni
* Segnala i problemi relativi alle autorizzazioni o all’accesso
* Coordina l’abilitazione di nuove funzioni e ambienti di test

>[!ENDTABS]

## Passaggi successivi

1. **Iniziare in piccolo**: crea un semplice percorso di benvenuto o una campagna con un singolo messaggio per imparare a utilizzare la piattaforma
2. **Sfrutta l’intelligenza artificiale**: utilizza l’Assistente IA per porre domande e accelerare la creazione di contenuti
3. **Iscrizione alla community**: connettiti con altri utenti Journey Optimizer nella [community Experience League](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer){target="_blank"}
4. **Esplorare i tutorial**: guarda i video con istruzioni dettagliate su [Experience League](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/overview){target="_blank"}
