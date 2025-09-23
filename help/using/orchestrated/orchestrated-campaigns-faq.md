---
solution: Journey Optimizer
product: journey optimizer
title: Domande frequenti sulle campagne orchestrate
description: Domande frequenti sulle campagne orchestrate per Journey Optimizer
version: Campaign Orchestration
exl-id: 6a660605-5f75-4c0c-af84-9c19d82d30a0
source-git-commit: c584ce48029bd298b503a342a1e663eeeedbba42
workflow-type: tm+mt
source-wordcount: '1430'
ht-degree: 4%

---

# Domande frequenti {#faq-oc}

Di seguito sono riportate le domande frequenti sulle campagne orchestrate di Adobe Journey Optimizer.

Hai bisogno di ulteriori dettagli? Utilizza le opzioni di feedback nella parte inferiore di questa pagina per porre la tua domanda o connetterti alla [community Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=en){target="_blank"}.

+++ Cos’è l’orchestrazione di Campaign?

L’orchestrazione delle campagne è una funzione di Journey Optimizer che supporta flussi di lavoro in un unico passaggio o in più passaggi che sfruttano l’archivio dati relazionale per creare e segmentare i tipi di pubblico allo scopo di creare un coinvolgimento in batch.

Porta un nuovo tipo di campagne in Journey Optimizer: **Campagne orchestrate**. Le campagne orchestrate aiutano i brand a eseguire campagne di marketing su larga scala, complesse e da uno a molti. Sono progettati per il coinvolgimento avviato dal marchio, ad esempio promozioni, campagne stagionali o comunicazioni basate su account.

Rispetto alle campagne di invio/azione singole, portano **orchestrazione e sequenza** al marketing in uscita: i tipi di pubblico passano attraverso un flusso di lavoro con più passaggi insieme, anziché ricevere un&#39;esplosione una tantum.

+++

+++ Cosa posso fare con una campagna orchestrata?

Le funzionalità principali includono:

* **Tipi di pubblico on demand**: crea e perfeziona immediatamente i gruppi di destinazione utilizzando query relazionali.
* **Segmentazione di più entità**: crea tipi di pubblico precisi connettendo i dati dei clienti con entità correlate (ad esempio account, acquisti, prenotazioni).
* **Visibilità pre-invio**: consulta conteggi accurati del pubblico prima dell&#39;avvio per ottimizzare il targeting.
* **Flussi di lavoro a più passaggi**: esegui campagne in sequenza, ad esempio promozioni stagionali, avvii di prodotti o offerte fedeltà.

**Procedure consigliate**

* Definisci un **obiettivo campagna di cancellazione** prima di progettare flussi di lavoro.
* Inizia con un **pubblico pilota** per convalidare i conteggi e la logica prima del ridimensionamento.
* Mantieni le regole di segmentazione **il più semplice possibile** per ottimizzare le prestazioni e la trasparenza.
* Utilizza **convenzioni di denominazione coerenti** per tipi di pubblico e campagne per semplificare la gestione.

+++

+++ Come accedere all’orchestrazione di Campaign?

Per accedere all’orchestrazione della campagna, la licenza deve includere il pacchetto **Journey Optimizer - Campagne e Percorsi** o **Journey Optimizer - Campagne**. Contatta il tuo rappresentante Adobe per confermare la licenza e aggiornare, se necessario.

Ulteriori informazioni sul modello di gestione licenze di Campaign Orchestration in [Descrizione prodotto Adobe Journey Optimizer](https://helpx.adobe.com/it/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

+++

+++ Quali sono le differenze tra le campagne orchestrate e i Percorsi?

* **Campagne orchestrate**: ideale per **campagne batch, uno-a-molti**. Il pubblico avanza in blocco, secondo una pianificazione.
* **Percorsi**: soluzione ottimale per **coinvolgimento in tempo reale uno a uno**. Ogni cliente si sposta all’interno del percorso secondo il proprio ritmo, attivato da comportamenti o eventi.

**Best practice**: utilizzali insieme: Percorsi per esperienze attivate e reattive e campagne orchestrate per iniziative pianificate basate su calendario.


+++

+++ Cos’è la segmentazione con più entità?

L’orchestrazione delle campagne in Adobe Journey Optimizer utilizza un database relazionale. Questo tipo di modello dati dispone di schemi separati di dati connessi tramite relazioni 1:1 o 1:many. Questo consente agli utenti di avviare una query su qualsiasi schema, non solo a livello di destinatario, e quindi di passare a altri schemi correlati, come acquisti, prodotti, prenotazioni o dettagli dei destinatari, fornendo grande flessibilità nella creazione di segmenti e tipi di pubblico e
raffinato.


**Esempio** - Esegui il targeting di tutti i destinatari con abbonamenti in scadenza nei successivi 30 giorni. In Campaign Orchestration la query può iniziare con lo schema Sottoscrizioni, cercare solo la colonna data di scadenza di tale schema e restituire tutte le sottoscrizioni in scadenza, quindi aggregare i dati del destinatario correlati a tali ID di abbonamenti specifici restituendo i risultati in modo più rapido ed efficiente rispetto ai modelli di dati che iniziano ogni query a livello di destinatario.

+++

+++ Come funziona il modello dati?

Le campagne utilizzano un **database relazionale**. Questo consente di eseguire query su diversi set di dati (ad esempio clienti, prodotti, abbonamenti) e di collegarli in modo flessibile per la segmentazione avanzata.

**Procedure consigliate**

* Organizza i set di dati in modo che **relazioni (join)** riflettano la logica di business.
* Evitare join non necessari per mantenere le query performanti.
* Convalidare i risultati del campione prima di eseguire estrazioni su larga scala.


+++

+++ Posso personalizzare i messaggi con dati relazionali?

Sì.  In Campaign Orchestration è possibile aggiornare un profilo destinatario noto come &quot;Entità persone&quot; e utilizzare i dati per la personalizzazione. Inoltre, i dati arricchiti da entità collegate nel database relazionale possono essere utilizzati anche per la personalizzazione. Puoi utilizzare i profili dei clienti insieme ai dati collegati (come acquisti o abbonamenti) per personalizzare i contenuti su tutti i canali supportati.


**Consigli**

* Utilizza **dati transazionali e comportamentali** per rendere le offerte rilevanti.
* Combina **attributi statici** (ad esempio, livello fedeltà) con **attributi dinamici** (ad esempio, data ultimo acquisto).
* Personalizzazione concisa: il sovraccarico dei messaggi con i dati può danneggiare la leggibilità.


+++

<!--
## Do Orchestrated campaigns integrate with other Adobe solutions? {#integrations}

Yes. Campaign orchestration is natively integrated with:

* **Customer Journey Analytics**: Campaign orchestration reports are available.  
* **Real-Time CDP**: Audiences built in Campaigns can be read in Real-Time CDP.  
* **Federated Audience Composition (FAC)**: Available as an add-on.  -->

+++ Quali canali sono supportati?

Puoi creare campagne orchestrate per inviare **e-mail**, **SMS** e **notifiche push**.

+++

+++ È possibile avviare più comunicazioni e canali diversi all’interno della stessa campagna orchestrata?

Sì, le campagne orchestrate supportano l’orchestrazione cross-channel.

+++

+++ Sono disponibili modelli di campagna orchestrati?

No, non è possibile definire o utilizzare modelli di campagna, ma è possibile utilizzare modelli di contenuto per le comunicazioni.

+++

+++ La finestra di progettazione del contenuto per i messaggi è specifica per le campagne orchestrate?

No, il designer di contenuti, incluso E-mail Designer, è comune a tutte le funzionalità di Journey Optimizer.

+++

+++ In che modo i diversi canali sono collegati nelle campagne orchestrate?

Il componente canale e il runtime sono comuni a tutte le campagne Journey Optimizer, tuttavia, i canali supportati sono diversi.

+++


+++ Le campagne orchestrate possono connettersi con i canali in uscita (web, inApp)?

No, i canali in uscita non sono supportati nelle campagne orchestrate.

+++

+++ E le autorizzazioni e il consenso?

Le autorizzazioni e il consenso per le campagne e i percorsi orchestrati sono gestiti centralmente in Adobe Experience Platform. Queste impostazioni vengono applicate in entrambe le soluzioni per ciascun destinatario prima dell’invio.


**Procedure consigliate**

* Applica **governance centralizzata**: evita di gestire separatamente il consenso a livello di campagna.
* Controlla periodicamente i dati del consenso per rilevare incongruenze.
* Rispetta **rinunce specifiche per il canale** — non presumere che il consenso globale copra tutti i canali.

+++


+++ Posso eseguire la segmentazione ad hoc nelle campagne orchestrate?

In Campaign Orchestration, si fa riferimento alla segmentazione ad hoc come &quot;segmentazione live&quot;, in cui è possibile accedere in tempo reale a tutti i dati disponibili nell’archivio relazionale, creare una query complessa e ottenere il risultato per l’attivazione immediata tramite canali in uscita (ad esempio, e-mail + SMS).


**Suggerimenti**

* Utilizza la segmentazione ad hoc per **esigenze urgenti** (ad esempio, promozioni flash).
* Salva e documenta le query utili in modo che possano essere riutilizzate nelle campagne future.
* Convalida il conteggio del pubblico prima dell’attivazione per evitare invii insufficienti o eccessivi.

+++


+++ Campaign Orchestration accede solo ai dati caricati tramite batch oppure può anche eseguire query su tabelle aggiornate in tempo reale (come i dati di Analytics)?

Journey Optimizer Campaign Orchestration può innanzitutto creare query ad hoc sugli schemi basati su modelli. Per il momento, gli schemi basati su modelli supportano solo origini batch. Inoltre, supporta la funzione Read audience (Lettura pubblico) di qualsiasi tipo di pubblico di Adobe Experience Platform.

+++

+++ Le campagne orchestrate supportano il processo decisionale?

Sì.  Il processo decisionale può utilizzare dati relazionali provenienti da campagne orchestrate. Una volta che lo schema basato su modello è stato connesso con gli schemi XDM, i dati XDM possono essere utilizzati nel processo decisionale.

+++


+++ Come funziona l’implementazione in ambienti diversi?

Gli oggetti creati nelle campagne orchestrate (ad esempio, tipi di pubblico e flussi di lavoro) sono legati alla sandbox in cui vengono generati. I flussi di lavoro standard per la creazione di pacchetti e l’implementazione in ambienti diversi (dev, stage, prod) non sono attualmente disponibili per le campagne orchestrate.

**Procedure consigliate**

* Gestisci **sandbox separate** per sperimentazione, controllo qualità e produzione.
* Configurazioni dei documenti complete per abilitare la replica manuale, se necessario.
* Allineati ai team di governance per ridurre la deviazione della configurazione tra gli ambienti.

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

La segmentazione viene eseguita sui destinatari durante l’invio sul profilo Adobe Experience Platform. La dimensione di destinazione Destinatario estende il profilo unificato con dati aggiuntivi utilizzati per la segmentazione all’interno di campagne orchestrate, mentre Destinatario viene riconciliato con Profilo in fase di esecuzione per l’invio di messaggi e la verifica dei criteri di consenso e delle regole aziendali. Questa riconciliazione è utile per unificare le regole aziendali e l’applicazione del consenso a livello di profilo

![](assets/recipients-and-profiles.png)

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

+++

+++ Qual è il numero massimo di attività per campagna orchestrata?

Il numero di attività in una campagna orchestrata è limitato a 500.

+++

+++ È possibile eseguire arricchimenti per aggiungere dati aggiuntivi?

Sì, puoi arricchire i dati dall’archivio relazionale e dai tipi di pubblico di Adobe Experience Platform.

+++

+++ Tutti i filtri devono essere definiti tramite tipi di pubblico oppure è possibile configurare un qualche tipo di filtro?

Le campagne orchestrate supportano i filtri predefiniti: puoi definire e salvare una query come filtro e aggiungerla ai preferiti per riutilizzarla in ulteriori attività di segmentazione.

+++


## Risorse aggiuntive

Per ulteriori informazioni e aggiornamenti, consulta le risorse seguenti:

* [Guardrail e limitazioni delle campagne orchestrate](../orchestrated/guardrails.md)
* [Introduzione a schemi e set di dati nelle campagne orchestrate](../orchestrated/gs-schemas.md)
* [Creare la prima campagna orchestrata](../orchestrated/gs-campaign-creation.md)
* [Descrizione del prodotto Journey Optimizer](https://helpx.adobe.com/it/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}
