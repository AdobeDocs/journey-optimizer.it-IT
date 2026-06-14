---
solution: Journey Optimizer
product: journey optimizer
title: Domande frequenti sulle campagne orchestrate
description: Domande frequenti sulle campagne orchestrate per Journey Optimizer
version: Campaign Orchestration
exl-id: 6a660605-5f75-4c0c-af84-9c19d82d30a0
TQID: https://experienceleague.adobe.com/25WjNcE8jmkqH2TvJnyST510xamIV-seDXTmHj0QEYs
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
topic_v2:
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: c4147b6e-073b-4d3c-9ab1-d60f2f4434ef
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: cda41058be1eb26538f4b0ef8c7b6c3f1c01eccd
workflow-type: tm+mt
source-wordcount: 2785
ht-degree: 11%

---

# Domande frequenti {#faq-oc}

>[!BEGINSHADEBOX]

**In questa pagina:** Trova le risposte alle domande più frequenti sulle campagne orchestrate, inclusi modelli di dati, canali, attività, pubblicazione e consenso.

>[!ENDSHADEBOX]

Di seguito sono riportate le domande frequenti sulle campagne orchestrate di Adobe Journey Optimizer.

Hai bisogno di altri dettagli? Utilizza le opzioni di feedback nella parte inferiore di questa pagina per porre la tua domanda o connetterti alla [community Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=it){target="_blank"}.

+++ Cos’è l’orchestrazione di Campaign?

L’orchestrazione delle campagne è una funzione di Journey Optimizer che supporta flussi di lavoro in un unico passaggio o in più passaggi che sfruttano l’archivio dati relazionale per creare e segmentare i tipi di pubblico allo scopo di creare un coinvolgimento in batch.

Porta un nuovo tipo di campagne in Journey Optimizer: **Campagne orchestrate**. Le campagne orchestrate aiutano i brand a eseguire campagne di marketing su larga scala, complesse e da uno a molti. Sono progettati per il coinvolgimento avviato dal marchio, ad esempio promozioni, campagne stagionali o comunicazioni basate su account.

Rispetto alle campagne di invio/azione singole, portano **orchestrazione e sequenza** al marketing in uscita: i tipi di pubblico passano attraverso un flusso di lavoro con più passaggi insieme, anziché ricevere un&#39;esplosione una tantum.

**Ulteriori informazioni**

* [Introduzione alle campagne orchestrate](gs-orchestrated-campaigns.md)
* [Creare la prima campagna orchestrata](gs-campaign-creation.md)

+++

+++ Cosa posso fare con una campagna orchestrata?

Le funzionalità principali includono:

* **Tipi di pubblico on demand**: crea e perfeziona immediatamente i gruppi di destinazione utilizzando query relazionali.
* **Segmentazione di più entità**: crea tipi di pubblico precisi connettendo i dati dei clienti con entità correlate (ad esempio account, acquisti, prenotazioni).
* **Visibilità pre-invio**: vedi conteggi dei pubblici precisi prima dell&#39;avvio per ottimizzare il targeting.
* **Flussi di lavoro a più passaggi**: esegui campagne in sequenza, ad esempio promozioni stagionali, avvii di prodotti o offerte fedeltà.

**Procedure consigliate**

* Definisci un **obiettivo campagna di cancellazione** prima di progettare flussi di lavoro.
* Inizia con un **pubblico pilota** per convalidare i conteggi e la logica prima del ridimensionamento.
* Mantieni le regole di segmentazione **il più semplice possibile** per ottimizzare le prestazioni e la trasparenza.
* Utilizza **convenzioni di denominazione coerenti** per tipi di pubblico e campagne per semplificare la gestione.

**Ulteriori informazioni**

* [Creare una campagna orchestrata](create-orchestrated-campaign.md)
* [Utilizzare le attività della campagna](activities/about-activities.md)
* [Creare la regola utilizzando il modellatore di query](build-query.md)

+++

+++ Come ottenere l’accesso all’orchestrazione di Campaign?

Per accedere all’orchestrazione della campagna, la licenza deve includere il pacchetto **Journey Optimizer - Campagne e Percorsi** o **Journey Optimizer - Campagne**. Contatta il tuo rappresentante Adobe per confermare la licenza e aggiornare, se necessario.

**Ulteriori informazioni**

* [Introduzione alle campagne orchestrate](gs-orchestrated-campaigns.md)
* [Descrizione del prodotto Adobe Journey Optimizer](https://helpx.adobe.com/it/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}

+++

+++ Quali sono le differenze tra le campagne orchestrate e i Percorsi?

* **Campagne orchestrate**: ideale per **campagne batch, uno-a-molti**. Il pubblico avanza in blocco, secondo una pianificazione.
* **Percorsi**: soluzione ottimale per **coinvolgimento in tempo reale uno a uno**. Ogni cliente si sposta all’interno del percorso secondo il proprio ritmo, attivato da comportamenti o eventi.

**Best practice**: utilizzali insieme: Percorsi per esperienze attivate e reattive e campagne orchestrate per iniziative pianificate basate su calendario.

**Ulteriori informazioni**

* [Introduzione alle campagne orchestrate](gs-orchestrated-campaigns.md)
* [Creare il primo percorso](../building-journeys/journey-gs.md)
* [Introduzione alle campagne](../campaigns/get-started-with-campaigns.md)

+++

+++ Cos’è la segmentazione con più entità?

L’orchestrazione delle campagne in Adobe Journey Optimizer utilizza un database relazionale. Questo tipo di modello dati dispone di schemi separati di dati connessi tramite relazioni 1:1 o 1:many. Questo consente agli utenti di avviare una query su qualsiasi schema, non solo a livello di destinatario, e quindi di passare a altri schemi correlati, come acquisti, prodotti, prenotazioni o dettagli dei destinatari, fornendo grande flessibilità nel modo in cui è possibile creare e perfezionare segmenti e tipi di pubblico.

**Esempio** - Esegui il targeting di tutti i destinatari con abbonamenti in scadenza nei successivi 30 giorni. In Campaign Orchestration la query può iniziare con lo schema Sottoscrizioni, cercare solo la colonna data di scadenza di tale schema e restituire tutte le sottoscrizioni in scadenza, quindi aggregare i dati del destinatario correlati a tali ID di abbonamenti specifici restituendo i risultati in modo più rapido ed efficiente rispetto ai modelli di dati che iniziano ogni query a livello di destinatario.

**Ulteriori informazioni**

* [Introduzione agli schemi e ai set di dati](gs-schemas.md)
* [Configurare una dimensione di targeting](target-dimension.md)
* [Creare la regola utilizzando il modellatore di query](build-query.md)

+++

+++ Come funziona il modello dati?

Le campagne utilizzano un **database relazionale**. Questo consente di eseguire query su diversi set di dati (ad esempio clienti, prodotti, abbonamenti) e di collegarli in modo flessibile per la segmentazione avanzata.

**Procedure consigliate**

* Organizza i set di dati in modo che **relazioni (join)** riflettano la logica di business.
* Evitare join non necessari per mantenere le query performanti.
* Convalidare i risultati del campione prima di eseguire estrazioni su larga scala.

**Ulteriori informazioni**

* [Introduzione agli schemi e ai set di dati](gs-schemas.md)
* [Creare manualmente uno schema](manual-schema.md)
* [Acquisire i dati](ingest-data.md)

+++

+++ Posso personalizzare i messaggi con dati relazionali?

Sì. In Campaign Orchestration è possibile aggiornare un profilo destinatario noto come &quot;Entità persone&quot; e utilizzare i dati per la personalizzazione. Inoltre, i dati arricchiti da entità collegate nel database relazionale possono essere utilizzati anche per la personalizzazione. Puoi utilizzare i profili dei clienti insieme ai dati collegati (come acquisti o abbonamenti) per personalizzare i contenuti su tutti i canali supportati.

**Consigli**

* Utilizza **dati transazionali e comportamentali** per rendere le offerte rilevanti.
* Combina **attributi statici** (ad esempio, livello fedeltà) con **attributi dinamici** (ad esempio, data ultimo acquisto).
* Personalizzazione concisa: il sovraccarico dei messaggi con i dati può danneggiare la leggibilità.

**Ulteriori informazioni**

* [Utilizzare l’attività Arricchimento](activities/enrichment.md)
* [Aggiungere un’attività canale in una campagna orchestrata](activities/channels.md)

+++

<!--
## Do Orchestrated campaigns integrate with other Adobe solutions? {#integrations}

Yes. Campaign orchestration is natively integrated with:

* **Customer Journey Analytics**: Campaign orchestration reports are available.  
* **Real-Time CDP**: Audiences built in Campaigns can be read in Real-Time CDP.  
* **Federated Audience Composition (FAC)**: Available as an add-on.  
-->

+++ Come posso testare una campagna orchestrata attivata da segnale prima di pubblicarla?

Mentre la campagna si trova in **Bozza**, puoi testarla definendo **parametri** nella pianificazione e fornendo **valori di test** per ciascuno. Avvia il flusso di lavoro, quindi chiama l’API del trigger (utilizzando la richiesta di esempio dalla configurazione della pianificazione o la tua richiesta con lo stesso endpoint) per eseguire la campagna con tali valori di test. [Scopri come completare e testare una campagna attivata dal segnale](trigger-orchestrated-campaign.md#build-and-test).

+++

+++ Posso ripristinare una campagna orchestrata live alla bozza?

Sì, in situazioni specifiche. L&#39;opzione **[!UICONTROL Torna alla bozza]** è progettata come un meccanismo di ripristino per annullare la pubblicazione e ripristinare lo stato bozza di una campagna.

Questa opzione è disponibile per le campagne pianificate in attesa di esecuzione o per le campagne live con errori di esecuzione. [Scopri come ripristinare una campagna live alla bozza](start-monitor-campaigns.md#back-to-draft)

+++

+++ Cosa succede internamente quando si pubblica una campagna orchestrata?

Quando si fa clic su **[!UICONTROL Pubblica]**, si verifica la seguente sequenza:

1. **Attivazione modulo di pianificazione** - Se è configurata una pianificazione, il modulo di pianificazione avvia l&#39;esecuzione all&#39;ora definita.
1. **Le attività Save Audience vengono eseguite per prime**. Tutte le attività Save audience vengono eseguite prima delle attività Message. La shell del pubblico viene creata in Audience Portal e i profili qualificati iniziano l’acquisizione.
1. **Inizio dell&#39;esecuzione del messaggio**: le attività del canale iniziano l&#39;elaborazione per la prima attività messaggio nel flusso di lavoro.
1. **Ricerca snapshot profilo**: i dati del profilo vengono risolti in base a uno snapshot creato al momento della pubblicazione, non in base al profilo in tempo reale, garantendo la coerenza nell&#39;intera esecuzione.
1. **Valutazione del consenso** - Il consenso viene rispettato direttamente dal record del profilo e non viene rivalutato al momento dell&#39;invio.
1. **Riconciliazione profili** — I destinatari vengono riconciliati in base ai profili di Adobe Experience Platform al momento dell&#39;invio.
1. **Creazione del registro di consegna** — Gli eventi di consegna sono registrati nel set di dati `ajo_message_feedback_event`.

**Ulteriori informazioni**

* [Sequenza di esecuzione al momento della pubblicazione](start-monitor-campaigns.md#publication-sequence)
* [Avviare e monitorare le campagne orchestrate](start-monitor-campaigns.md)

+++

+++ Perché i miei messaggi non vengono inviati dopo la pubblicazione della campagna?

Diverse situazioni possono impedire l’invio di messaggi dopo la pubblicazione. Verifica quanto segue nell’ordine:

1. **Invio conferma in sospeso (più comune)** - Per le campagne non ricorrenti, la consegna dei messaggi viene sospesa per impostazione predefinita fino a quando non si conferma esplicitamente l&#39;invio dal riquadro delle proprietà dell&#39;attività del canale. La campagna viene visualizzata come **Live** ma nessun messaggio viene inviato fino alla conferma. [Ulteriori informazioni](start-monitor-campaigns.md#confirm-sending)

1. **La campagna è pianificata per un momento futuro**. Se è configurata una pianificazione, la campagna è attiva ma l&#39;esecuzione non è ancora iniziata. Controlla le impostazioni di pianificazione e attendi l’ora di inizio configurata. [Ulteriori informazioni](create-orchestrated-campaign.md#schedule)

1. **Le attività Save Audience acquisiscono ancora** — Le attività Save Audience vengono eseguite prima delle attività messaggio al momento della pubblicazione. Se l’acquisizione del pubblico è ancora in corso, l’esecuzione del messaggio non è ancora iniziata. Monitora gli indicatori di stato dell’attività nell’area di lavoro. [Ulteriori informazioni](start-monitor-campaigns.md#activities)

1. **Il pubblico è vuoto**. La query di targeting ha restituito zero profili. Rivedi le regole di segmentazione e convalida il conteggio del pubblico prima di ripubblicare.

1. **Tutti i profili hanno rinunciato** — Il consenso viene valutato al momento dell&#39;invio rispetto a ciascun profilo. Se tutti i profili di destinazione hanno rinunciato al canale pertinente, non vengono inviati messaggi. [Ulteriori informazioni](../action/consent.md)

1. **Attività del canale in stato di errore**. Un indicatore di stato arancione o rosso sull&#39;attività del canale segnala un problema di blocco. Apri i **[!UICONTROL registri]** per informazioni dettagliate sull&#39;errore e su come risolverlo. [Ulteriori informazioni](start-monitor-campaigns.md#logs-tasks)

1. **Consegna della limitazione del controllo del tasso** - Se il controllo del tasso è abilitato nell&#39;attività del canale, la consegna potrebbe essere più lenta del previsto. Verificare le impostazioni di controllo della frequenza nel riquadro delle proprietà dell&#39;attività del canale. [Ulteriori informazioni](activities/channels.md#rate-control)

**Ulteriori informazioni**

* [Avviare e monitorare le campagne orchestrate](start-monitor-campaigns.md)
* [Aggiungere un’attività canale in una campagna orchestrata](activities/channels.md)

+++

+++ La pubblicazione utilizza il profilo in tempo reale o uno snapshot?

Al momento della pubblicazione, i dati del profilo vengono risolti rispetto a uno **snapshot acquisito al momento della pubblicazione**, non rispetto al profilo in tempo reale. In questo modo viene garantita la coerenza nell’intera esecuzione della campagna: tutte le attività elaborano lo stesso stato di profilo, indipendentemente dalla durata della campagna.

Il consenso, tuttavia, viene sempre rispettato dal record del profilo corrente e non viene rivalutato al momento dell’invio.

Nelle campagne orchestrate, la segmentazione viene eseguita sui destinatari (archivio relazionale), mentre i controlli di invio e consenso dei messaggi vengono risolti in base al profilo Adobe Experience Platform.

**Ulteriori informazioni**

* [Sequenza di esecuzione al momento della pubblicazione](start-monitor-campaigns.md#publication-sequence)
* [Qual è la relazione tra destinatari ed entità profilo?](#faq-oc)
* [Utilizzare i criteri di consenso](../action/consent.md)

+++

+++ Quali canali sono supportati?

Puoi creare campagne orchestrate per inviare **e-mail**, **SMS**, **notifiche push** e **direct mailing**.

**Ulteriori informazioni**

* [Aggiungere un’attività canale in una campagna orchestrata](activities/channels.md)
* [Utilizzare le attività della campagna](activities/about-activities.md)

+++

+++ È possibile avviare più comunicazioni e canali diversi all’interno della stessa campagna orchestrata?

Sì, le campagne orchestrate supportano l’orchestrazione cross-channel. Puoi combinare le attività e-mail, SMS, notifiche push e direct mailing in un’area di lavoro di campagna in più passaggi per creare esperienze cliente complete.

**Ulteriori informazioni**

* [Aggiungere un’attività canale in una campagna orchestrata](activities/channels.md)
* [Utilizzare le attività della campagna](activities/about-activities.md)

+++

+++ Sono disponibili modelli di campagna orchestrati?

No, non è possibile definire o utilizzare modelli di campagna, ma è possibile utilizzare modelli di contenuto per le comunicazioni.

**Ulteriori informazioni**

* [Aggiungere un’attività canale in una campagna orchestrata](activities/channels.md)
* [Creare una campagna orchestrata](create-orchestrated-campaign.md)

+++

+++ La finestra di progettazione del contenuto per i messaggi è specifica per le campagne orchestrate?

No, il designer di contenuti, incluso E-mail Designer, è comune a tutte le funzionalità di Journey Optimizer.

**Ulteriori informazioni**

* [Aggiungere un’attività canale in una campagna orchestrata](activities/channels.md)
* [Utilizzare l’attività Arricchimento](activities/enrichment.md)

+++

+++ In che modo i diversi canali sono collegati nelle campagne orchestrate?

Il componente canale e il runtime sono comuni a tutte le campagne Journey Optimizer, tuttavia, i canali supportati sono diversi. Le campagne orchestrate supportano e-mail, SMS, notifiche push e direct mail.

**Ulteriori informazioni**

* [Aggiungere un’attività canale in una campagna orchestrata](activities/channels.md)
* [Guardrail e limitazioni](guardrails.md)

+++


+++ Le campagne orchestrate possono connettersi con i canali in uscita (web, inApp)?

No, i canali in entrata come web e in-app non sono supportati nelle campagne orchestrate. Sono supportati solo i canali in uscita (e-mail, SMS, notifiche push e direct mail).

**Ulteriori informazioni**

* [Guardrail e limitazioni](guardrails.md)
* [Aggiungere un’attività canale in una campagna orchestrata](activities/channels.md)

+++

+++ E le autorizzazioni e il consenso?

Le autorizzazioni e il consenso per le campagne e i percorsi orchestrati sono gestiti centralmente in Adobe Experience Platform. Queste impostazioni vengono applicate in entrambe le soluzioni per ciascun destinatario prima dell’invio.

**Procedure consigliate**

* Applica **governance centralizzata**: evita di gestire separatamente il consenso a livello di campagna.
* Controlla periodicamente i dati del consenso per rilevare incongruenze.
* Rispetta **rinunce specifiche per il canale** — non presumere che il consenso globale copra tutti i canali.

**Ulteriori informazioni**

* [Introduzione alle campagne orchestrate](gs-orchestrated-campaigns.md)
* [Guardrail e limitazioni](guardrails.md)

+++


+++ Posso eseguire la segmentazione ad hoc nelle campagne orchestrate?

In Campaign Orchestration, si fa riferimento alla segmentazione ad hoc come &quot;segmentazione live&quot;, in cui è possibile accedere in tempo reale a tutti i dati disponibili nell’archivio relazionale, creare una query complessa e ottenere il risultato per l’attivazione immediata tramite canali in uscita (ad esempio, e-mail + SMS).

**Suggerimenti**

* Utilizza la segmentazione ad hoc per **esigenze urgenti** (ad esempio, promozioni flash).
* Salva e documenta le query utili in modo che possano essere riutilizzate nelle campagne future.
* Convalida il conteggio del pubblico prima dell’attivazione per evitare invii insufficienti o eccessivi.

**Ulteriori informazioni**

* [Creare la regola utilizzando il modellatore di query](build-query.md)
* [Utilizzare l’attività Crea pubblico](activities/build-audience.md)
* [Configurare una dimensione di targeting](target-dimension.md)

+++


+++ Campaign Orchestration accede solo ai dati caricati tramite batch oppure può anche eseguire query su tabelle aggiornate in tempo reale (come i dati di Analytics)?

Journey Optimizer Campaign Orchestration può creare query ad hoc oltre agli schemi relazionali. Per il momento, gli schemi relazionali supportano solo origini batch. Inoltre, supporta le attività Read audience di qualsiasi tipo di pubblico Adobe Experience Platform.

**Ulteriori informazioni**

* [Introduzione agli schemi e ai set di dati](gs-schemas.md)
* [Acquisire i dati](ingest-data.md)
* [Utilizzare l’attività Leggi pubblico](activities/read-audience.md)

+++

+++ Le campagne orchestrate supportano il processo decisionale?

No, le campagne orchestrate non supportano le funzionalità decisionali. Per le funzioni decisionali, utilizza invece percorsi Journey Optimizer standard o campagne di azione.

**Ulteriori informazioni**

* [Introduzione alle decisioni per le esperienze](../experience-decisioning/gs-experience-decisioning.md)
* [Creare il primo percorso](../building-journeys/journey-gs.md)
* [Introduzione alle campagne](../campaigns/get-started-with-campaigns.md)

+++


+++ Come funziona l’implementazione in ambienti diversi?

Gli oggetti creati nelle campagne orchestrate (ad esempio, tipi di pubblico e flussi di lavoro) appartengono alla sandbox in cui sono stati creati. Per riutilizzare una campagna orchestrata in un&#39;altra sandbox (ad esempio sviluppo, stage o produzione), copiala con **Strumenti sandbox**: aggiungi la campagna a un pacchetto, pubblica il pacchetto e importalo nella sandbox di destinazione. La copia importata viene creata in **bozza** e **reimportando lo stesso pacchetto viene creata una nuova campagna** anziché aggiornarne una esistente. Uno spostamento completo richiede spesso **più di un passaggio**: potrebbe essere necessario allineare **configurazioni di canale** (nomi corrispondenti nella destinazione), **schemi** e **set di dati** attraverso lo stesso pacchetto o importazioni di pacchetti aggiuntive. Le configurazioni di canale non vengono copiate con la campagna. Nell&#39;interfaccia utente non è disponibile un elenco di controllo completo per la pre-esportazione. Per completare l&#39;installazione, utilizzare il flusso di mapping delle importazioni e **avvisi post-importazione**. Per informazioni dettagliate e limitazioni, vedere [Copiare oggetti Journey Optimizer tra sandbox](../configuration/copy-objects-to-sandbox.md).

**Procedure consigliate**

* Gestisci **sandbox separate** per sperimentazione, controllo qualità e produzione.
* Subito dopo l&#39;importazione, [duplica la campagna](../campaigns/manage-campaigns.md#duplicate-a-campaign) e lavori dal duplicato in modo che il reporting mostri correttamente i feedback e i dati di tracciamento.
* Dopo ogni importazione, prima di pubblicare, verifica la fine della campagna nella sandbox di destinazione.
* Documentare le configurazioni e allinearle con i team di governance per ridurre la deviazione della configurazione tra gli ambienti.

**Ulteriori informazioni**

* [Copiare oggetti Journey Optimizer tra sandbox](../configuration/copy-objects-to-sandbox.md)
* [Introduzione alle campagne orchestrate](gs-orchestrated-campaigns.md)
* [Guardrail e limitazioni](guardrails.md)

+++

<!--
## Are there recommended practices for running campaigns at scale? {#scale}

Yes, follow the best practices below:  

* **Plan campaigns around business calendars** (product launches, seasonal peaks) to align volume and resources.  
* Use **audience pre-views** before sending to confirm the expected size and avoid surprises.  
* Where possible, **stagger send times** to avoid overwhelming downstream systems (e.g., call centers, websites).  
* Establish a **monitoring routine**—track delivery logs, error rates, and opt-outs after each send.  
* Run **post-campaign analysis** in Customer Journey Analytics to refine targeting and orchestration for the next cycle.  
-->

+++ Qual è la relazione tra destinatari ed entità profilo?

La segmentazione viene eseguita sui destinatari durante l’invio sul profilo Adobe Experience Platform. La dimensione di destinazione Destinatario estende il profilo unificato con dati aggiuntivi utilizzati per la segmentazione all’interno di campagne orchestrate, mentre Destinatario viene riconciliato con Profilo in fase di esecuzione per l’invio di messaggi e la verifica dei criteri di consenso e delle regole aziendali. Questa riconciliazione è utile per unificare le regole aziendali e l’applicazione del consenso a livello di profilo.

![](assets/recipients-and-profiles.png)

**Ulteriori informazioni**

* [Configurare una dimensione di targeting](target-dimension.md)
* [Introduzione agli schemi e ai set di dati](gs-schemas.md)
* [Creare la regola utilizzando il modellatore di query](build-query.md)

+++

+++ In quali casi si consiglia di utilizzare Entità destinatari rispetto a Entità profilo?

La risposta &quot;Sì&quot; suggerisce il migliore archivio dati, ma conferma sempre con il tuo rappresentante Adobe l’approccio migliore in base al caso d’uso e ai vincoli.

| Archivio relazionale | Profilo cliente in tempo reale |
|---------|----------|
| L’origine dei dati è già relazionale? | L’origine dello streaming di dati è? |
| Intendi acquisire dati come tale per i casi di utilizzo di marketing? | L’aggiornamento dei dati è un requisito importante? |
| Esiste un grande volume di dati storici (`>` 2 mesi) necessari per i casi di utilizzo di attivazione marketing? | Esistono scenari in cui l’azione o la decisione nel momento richiedono dati? |
| Sono necessarie attività ad hoc per la creazione, la valutazione e l’attivazione di tipi di pubblico? | I dati comportamentali possono essere limitati a `<` 90 giorni utilizzando aggregati precalcolati? |
|  | Sono necessari dati per personalizzare i messaggi in tempo reale? |

**Ulteriori informazioni**

* [Configurare una dimensione di targeting](target-dimension.md)
* [Introduzione agli schemi e ai set di dati](gs-schemas.md)
* [Creare la regola utilizzando il modellatore di query](build-query.md)

+++

+++ Qual è il numero massimo di attività per campagna orchestrata?

Si applicano due limiti distinti:

* **Attività canale**: massimo 10 attività canale per campagna orchestrata (e-mail, SMS, push o direct mail). Le attività di targeting e controllo del flusso non vengono conteggiate. Se si supera questo limite durante il salvataggio o la pubblicazione, l’operazione non riesce.

* **Dimensione quadro** — Fino a **500 attività** nell&#39;area di lavoro. Per la manutenzione, mantieni in pratica i flussi di lavoro sotto **100 attività**.

**Ulteriori informazioni**

* [Guardrail e limitazioni](guardrails.md)
* [Utilizzare le attività della campagna](activities/about-activities.md)

+++

+++ È possibile eseguire arricchimenti per aggiungere dati aggiuntivi?

Sì, puoi arricchire i dati dall’archivio relazionale e dai tipi di pubblico di Adobe Experience Platform. Utilizza l’attività Enrichment per migliorare i dati sul pubblico con attributi aggiuntivi provenienti da schemi correlati.

**Ulteriori informazioni**

* [Utilizzare l’attività Arricchimento](activities/enrichment.md)
* [Utilizzare l’attività di riconciliazione](activities/reconciliation.md)

+++

+++ Tutti i filtri devono essere definiti tramite tipi di pubblico oppure è possibile configurare un qualche tipo di filtro?

Le campagne orchestrate supportano filtri predefiniti: puoi definire e salvare una query come filtro, aggiungerla ai preferiti e riutilizzarla in ulteriori attività di segmentazione. I filtri predefiniti possono includere parametri che consentono di immettere valori al momento dell’utilizzo. [Scopri come utilizzare i filtri predefiniti](predefined-filters.md).

**Ulteriori informazioni**

* [Creare la regola utilizzando il modellatore di query](build-query.md)
* [Utilizzare l’attività Crea pubblico](activities/build-audience.md)
* [Utilizzare filtri preimpostati](orchestrated-rule-builder.md)

+++


## Risorse aggiuntive

Per ulteriori informazioni e aggiornamenti, consulta le risorse seguenti:

* [Guardrail e limitazioni delle campagne orchestrate](guardrails.md)
* [Introduzione a schemi e set di dati nelle campagne orchestrate](gs-schemas.md)
* [Creare la prima campagna orchestrata](gs-campaign-creation.md)
* [Descrizione del prodotto Journey Optimizer](https://helpx.adobe.com/it/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}
