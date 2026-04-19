---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer
description: Scopri le funzioni principali e i casi d'uso di Adobe Journey Optimizer
feature: Get Started
topic: Content Management
role: User
level: Beginner
keywords: ottimizzatore percorso, ajo, adobe percorsi optimizer, guida introduttiva, omni-channel, personalizzazione, percorso cliente
exl-id: 956178c0-9985-4ff8-a29e-17dd367ce4d4
source-git-commit: a528fba262dccf93edb4eb2b04dba83c72793206
workflow-type: tm+mt
source-wordcount: '1216'
ht-degree: 14%

---

# Introduzione a Journey Optimizer {#ajo-gs}

Questa pagina presenta Adobe Journey Optimizer: cos’è, a chi serve, le sue funzionalità chiave e come si inserisce nell’architettura di Adobe Experience Platform. È il punto di partenza consigliato per i nuovi utenti.

## Cos’è [!DNL Adobe Journey Optimizer]?{#about-ajo}

[!DNL Adobe Journey Optimizer] è un&#39;applicazione aziendale per la creazione e la distribuzione di esperienze cliente connesse, contestuali e personalizzate su tutti i canali e punti di contatto. È stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e sfrutta un profilo cliente unificato in tempo reale, un framework aperto API-first, offer decisioning centralizzato e funzionalità AI/ML. Journey Optimizer consente ai brand di orchestrare sia campagne di marketing pianificate che comunicazioni attivate da eventi in tempo reale, da una singola applicazione su larga scala. Il risultato sono esperienze di marchio significative che incrementano la fedeltà dei clienti e il valore del ciclo di vita.

Questa guida si applica ai professionisti del marketing, ai team operativi e agli amministratori che non hanno mai utilizzato Journey Optimizer.

➡️ [Scopri Journey Optimizer](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/introduction-to-journey-optimizer/introduction.html?lang=it){target="_blank"} (video)


<!--
 Use [!DNL Adobe Journey Optimizer] to build multi-step customer journeys that initiate a sequence of interactions, offers, and messages across channels in real time. This approach ensures customers are engaged at the optimal moments based on their actions and relevant business signals. Learn how to build journeys in [this section](../building-journeys/journey-gs.md).

You can also create audience-based campaigns to send messages.
-->


## Funzionalità principali {#key-capabilities}

[!DNL Adobe Journey Optimizer] è un’applicazione agile e scalabile per la creazione e la distribuzione personalizzata, connessa e tempestiva di esperienze cliente tramite qualsiasi app, dispositivo o canale.

![Diagramma che mostra le tre aree di funzionalità principali di Journey Optimizer: Real-time Customer Insights &amp; Engagement, Modern Omnichannel Orchestration &amp; Execution e Intelligent Decisioning &amp; Personalization, tutti basati su Adobe Experience Platform.](assets/ajo-capabilities.png)

Le funzionalità principali includono:

### Approfondimenti sul cliente in tempo reale e coinvolgimento

Un profilo integrato riunisce i dati live provenienti da tutte le origini nei diversi punti di contatto dei clienti, inclusi i dati comportamentali, transazionali, finanziari e operativi, per ottimizzare le esperienze personali e contestuali dei clienti in tempo reale. [Informazioni su profili e pubblico](../audience/get-started-profiles.md)

### Orchestrazione moderna omni-channel ed esecuzione

Un’unica area di lavoro su cui armonizzare e ottimizzare il percorso del cliente per un coinvolgimento e un’attività di marketing di 1:1, per consentire ai brand di offrire più valore nel ciclo di vita del cliente. I percorsi di clienti progettati in [!DNL Adobe Journey Optimizer] possono essere dinamici e basati su eventi per consentire ai brand di reagire ai segnali in tempo reale e di collegare tali interazioni con campagne pianificate in modo da poter prendere le decisioni giuste in merito a quali comunicazioni inviare ai clienti, quando inviarle e attraverso quali canali. Gli strumenti per la creazione di contenuti incorporati, tra cui una finestra di progettazione visiva con trascinamento della selezione, modelli riutilizzabili, frammenti di contenuto e un editor di personalizzazione, consentono ai team di creare, personalizzare e gestire messaggi per ogni canale direttamente all’interno dello stesso flusso di lavoro. [Crea il tuo primo percorso](../building-journeys/journey-gs.md) | [Progetta il tuo contenuto](../../rp_landing_pages/content-management-landing-page.md)

### Intelligent Decisioning e Personalization

I brand possono applicare decisioni centralizzate e incorporare intelligenza artificiale e machine learning per configurare informazioni predittive in tutta l’esperienza del cliente, semplificando l’automazione delle decisioni e ottimizzando l’esperienza su larga scala. Decisioning potenzia le offerte centralizzate su tutti i canali e su larga scala attraverso [!DNL Adobe Journey Optimizer]. [Esplora Offer Decisioning](../offers/get-started/starting-offer-decisioning.md) | [Scopri le funzionalità di intelligenza artificiale](ai-features.md)


## Casi d’uso {#use-cases}

Questi esempi illustrano il modo in cui le funzionalità di Journey Optimizer interagiscono tra ruoli, settori e canali diversi.

### Recupero spedizione ritardata {#uc-delayed-shipment}

**Ruolo:** Addetto marketing | **Funzionalità di base:** [Profilo unificato + esclusione pubblico](../audience/get-started-profiles.md)

Un negozio di abbigliamento invia in genere sondaggi post-acquisto a tutti i clienti che hanno acquistato prodotti nell’ultima settimana. A causa delle condizioni climatiche avverse, alcune spedizioni hanno avuto ritardi. Potendo sapere chi non ha ancora ricevuto le proprie spedizioni, il negozio di abbigliamento può escludere queste persone dall’invio del questionario pianificato sulla soddisfazione, inviando invece un’e-mail personalizzata di scuse per il ritardo e offrendo un codice sconto con prodotti consigliati in base agli acquisti precedenti.

[Introduzione alle campagne](../campaigns/get-started-with-campaigns.md)

### Coinvolgimento in-store in tempo reale {#uc-instore}

**Ruolo:** Addetto marketing | **Funzionalità di base:** [Attivazione recinto geografico + push](../push/get-started-push.md)

Lo stesso retailer può coinvolgere un cliente fedele che entra nel parcheggio del negozio in tempo reale inviando una notifica push su un maglione che è di nuovo in magazzino nella dimensione del cliente.

[Introduzione alle notifiche push](../push/get-started-push.md)

### Recupero abbandono carrello {#uc-cart}

**Ruolo:** Addetto marketing | **Funzionalità di base:** [percorso con più passaggi attivato da evento](../building-journeys/journey-gs.md)

Quando un cliente aggiunge articoli a un carrello online ma lascia senza completare l’acquisto, Journey Optimizer rileva l’evento in tempo reale e avvia automaticamente un percorso di ripristino. Il cliente riceve un’e-mail personalizzata in cui gli vengono ricordati gli articoli rimasti indietro. Se il visitatore non riceve il click-through entro 24 ore, viene inviata una notifica push di follow-up, personalizzata in base alla cronologia di navigazione e allo stato di fidelizzazione.

[Creare il primo percorso](../building-journeys/journey-gs.md)

### Serie di benvenuto del servizio di streaming {#uc-welcome}

**Ruolo:** Addetto marketing | **Funzionalità di base:** [percorso di benvenuto attivato da eventi](../building-journeys/journey-gs.md)

Quando un cliente si abbona a un servizio di streaming, Journey Optimizer rileva l’evento di abbonamento e avvia immediatamente un percorso di benvenuto in più passaggi. Il cliente riceve un’e-mail di benvenuto che lo invita ad aprire l’app per la prima volta. Se non viene rilevata alcuna attività di accesso entro 48 ore, viene inviata una notifica push di follow-up con contenuti personalizzati consigliati in base agli interessi dichiarati durante l’iscrizione, convertendo un abbonato passivo in un utente attivo e attivo dal primo giorno.

[Creare il primo percorso](../building-journeys/journey-gs.md)

### Promemoria prenotazione con indicazioni {#uc-reservation}

**Ruolo:** Addetto marketing | **Funzionalità di base:** [Pianificato + Messaggistica in base alla posizione](../campaigns/get-started-with-campaigns.md)

Un marchio di ospitalità invia a ogni ospite un promemoria puntuale un’ora prima della prenotazione. La notifica include il nome dell’ospite, il tempo di prenotazione e le indicazioni sulla posizione per la sede, assemblate automaticamente dal profilo cliente e dai dati di prenotazione, senza alcuno sforzo manuale da parte del team di marketing.

[Introduzione alle campagne](../campaigns/get-started-with-campaigns.md)

### Notifica proattiva di interruzione del servizio {#uc-outage}

**Ruolo:** Operazioni | **Funzionalità di base:** [Selezione automatizzata del pubblico su larga scala](../audience/about-audiences.md)

Quando si verifica un’interruzione del servizio, Journey Optimizer identifica automaticamente i clienti interessati in base ai dati del loro account e ai pattern di utilizzo. Questi clienti ricevono una notifica proattiva che riconosce il problema e delinea le fasi successive, trasformando un’esperienza potenzialmente negativa in un momento di trasparenza e fiducia, consegnato su larga scala.

[Creare il primo percorso](../building-journeys/journey-gs.md)

### Campagna promozionale basata sull’intelligenza artificiale {#uc-ai-campaign}

**Ruolo:** Addetto marketing | **Funzionalità di base:** [Generazione contenuti IA + sperimentazione](ai-features.md)

La pianificazione del brand nel settore retail per il lancio di un prodotto si avvale dell’Assistente AI di Journey Optimizer per generare in pochi minuti più varianti di oggetto e copia del corpo, guidate da un prompt in linguaggio naturale e dalle linee guida del brand caricate. La sperimentazione di contenuti incorporata identifica automaticamente la variante con le prestazioni migliori tra un campione di pubblico iniziale. Il messaggio vincente viene quindi distribuito ai destinatari rimanenti, massimizzando il coinvolgimento senza ulteriore sforzo di scrittura.

[Esplora intelligenza artificiale e funzioni intelligenti](ai-features.md) | [Scopri la sperimentazione sui contenuti](../content-management/experiment-accelerator-gs.md)

### Avvisi di manutenzione tramite app mobile {#uc-maintenance}

**Ruolo:** Operazioni | **Funzionalità di base:** [Orchestrazione del percorso non di marketing](../building-journeys/journey-gs.md)

I non addetti al marketing, come i team operativi e l&#39;assistenza clienti, possono utilizzare [!DNL Adobe Journey Optimizer] per gestire le notifiche operative o monitorare i processi di onboarding. Ad esempio, un parco divertimenti in cui i visitatori scaricano un’app mobile come parte della loro esperienza: il personale di manutenzione può utilizzare Journey Optimizer per informare i visitatori dei percorsi attualmente chiusi a causa di manutenzione.

[Creare il primo percorso](../building-journeys/journey-gs.md)


## Disponibilità e licenze {#availability}

Questa documentazione tratta la versione corrente di Journey Optimizer e si applica sia agli utenti B2C che a quelli di B2B edition, a meno che non venga indicato diversamente. I componenti e le funzionalità disponibili nell’ambiente dipendono dalle [autorizzazioni](../administration/permissions.md) e dal [pacchetto di licenze](https://helpx.adobe.com/it/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}. Per qualsiasi domanda, contatta il tuo Adobe Customer Success Manager o il tuo rappresentante Adobe.

Le linee guida e le procedure generali sulla privacy di Adobe Experience Cloud sono applicabili anche a [!DNL Journey Optimizer]. [Ulteriori informazioni sulla privacy di Adobe Experience Cloud](https://www.adobe.com/it/privacy/experience-cloud.html){target="_blank"}.


## Architettura {#architecture}

Journey Optimizer è stato sviluppato in modalità nativa su Adobe Experience Platform e ne condivide le basi dati, il grafo delle identità e i servizi di governance. Per informazioni dettagliate sulla collaborazione tra questi sistemi, vedere [Informazioni su Journey Optimizer](understanding-ajo.md).


>[!MORELIKETHIS]
>
>* [Passaggi chiave per iniziare](quick-start.md): guide rapide basate sul ruolo per amministratori, addetti al marketing e data engineer.
>* [Introduzione alla gestione dei dati](../data/gs-data.md): scopri come i dati vengono acquisiti, unificati e attivati in Journey Optimizer.
>* [Progetta percorsi e invia messaggi](../building-journeys/journey-gs.md): crea il tuo primo percorso di clienti e configura le azioni del canale.
>* [Rapporti live](../reports/live-report.md): monitora le prestazioni di campagne e percorsi in tempo reale.
>* [Introduzione al tutorial su Journey Optimizer](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/introduction-to-journey-optimizer/introduction){target="_blank"}: video guidato sui concetti fondamentali di Journey Optimizer.
>* [Panoramica sulla sicurezza di Journey Optimizer](https://www.adobe.com/content/dam/cc/en/security/pdfs/AJO_SecurityOverview.pdf) (PDF): architettura di sicurezza, protezione dei dati e dettagli sulla conformità.
>* [Descrizione del prodotto Journey Optimizer](https://helpx.adobe.com/it/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}: termini ufficiali di licenza e suddivisione delle funzionalità di edizione.
