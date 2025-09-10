---
solution: Journey Optimizer
product: journey optimizer
title: Domande frequenti sulle campagne orchestrate
description: Domande frequenti sulle campagne orchestrate per Journey Optimizer
hide: true
hidefromtoc: true
version: Campaign Orchestration
exl-id: 6a660605-5f75-4c0c-af84-9c19d82d30a0
source-git-commit: 96b8813ebad35f51986cc62d847d9d3d256b08be
workflow-type: tm+mt
source-wordcount: '1102'
ht-degree: 4%

---

# Domande frequenti {#faq-oc}

Di seguito sono riportate le domande frequenti sulle campagne orchestrate di Adobe Journey Optimizer.

Hai bisogno di ulteriori dettagli? Utilizza le opzioni di feedback in fondo a questa pagina per sollevare la tua domanda.

## Cos’è l’orchestrazione di Campaign? {#what-are-oc}

L’orchestrazione delle campagne è una funzione di Journey Optimizer che supporta flussi di lavoro in un unico passaggio o in più passaggi che sfruttano l’archivio dati relazionale per creare e segmentare i tipi di pubblico allo scopo di creare un coinvolgimento in batch.

Porta un nuovo tipo di campagne in Journey Optimizer: **Campagne orchestrate**. Le campagne orchestrate aiutano i brand a eseguire campagne di marketing su larga scala, complesse e da uno a molti. Sono progettati per il coinvolgimento avviato dal marchio, ad esempio promozioni, campagne stagionali o comunicazioni basate su account.

Rispetto alle campagne di invio/azione singole, portano **orchestrazione e sequenza** al marketing in uscita: i tipi di pubblico passano attraverso un flusso di lavoro con più passaggi insieme, anziché ricevere un&#39;esplosione una tantum.

## Cosa posso fare con una campagna orchestrata? {#what-can-i-do}

Le funzionalità principali includono:

* **Tipi di pubblico on demand**: crea e perfeziona immediatamente i gruppi di destinazione utilizzando query relazionali.
* **Segmentazione di più entità**: crea tipi di pubblico precisi connettendo i dati dei clienti con entità correlate (ad esempio account, acquisti, prenotazioni).
* **Visibilità pre-invio**: consulta conteggi accurati del pubblico prima dell&#39;avvio per ottimizzare il targeting.
* **Flussi di lavoro a più passaggi**: esegui campagne in sequenza, ad esempio promozioni stagionali, avvii di prodotti o offerte fedeltà.

>[!BEGINSHADEBOX]

**Procedure consigliate**

* Definisci un **obiettivo campagna di cancellazione** prima di progettare flussi di lavoro.
* Inizia con un **pubblico pilota** per convalidare i conteggi e la logica prima del ridimensionamento.
* Mantieni le regole di segmentazione **il più semplice possibile** per ottimizzare le prestazioni e la trasparenza.
* Utilizza **convenzioni di denominazione coerenti** per tipi di pubblico e campagne per semplificare la gestione.

>[!ENDSHADEBOX]

## Come accedere all’orchestrazione di Campaign? {#access-oc}

Per accedere all’orchestrazione della campagna, la licenza deve includere il pacchetto **Journey Optimizer - Campagne e Percorsi** o **Journey Optimizer - Campagne**. Contatta il tuo rappresentante Adobe per confermare la licenza e aggiornare, se necessario.


## Quali canali sono supportati? {#channels}

Puoi creare campagne orchestrate per inviare **e-mail**, **SMS** e **notifiche push**.


>[!BEGINSHADEBOX]

**Consigli**

* Abbina il canale alla natura **del messaggio** (ad esempio, urgente = SMS, offerte personalizzate = e-mail, contestuale = push).
* Convalida sempre le preferenze di consenso e abbonamento prima di attivare un canale.
* Test del rendering dei messaggi su più dispositivi e client per garantire un&#39;esperienza coerente.

>[!ENDSHADEBOX]


## Quali sono le differenze tra le campagne orchestrate e i Percorsi? {#oc-vs-journeys}

* **Campagne orchestrate**: ideale per **campagne batch, uno-a-molti**. Il pubblico avanza in blocco, secondo una pianificazione.
* **Percorsi**: soluzione ottimale per **coinvolgimento in tempo reale uno a uno**. Ogni cliente si sposta all’interno del percorso secondo il proprio ritmo, attivato da comportamenti o eventi.

>[!BEGINSHADEBOX]

**Best practice**: utilizzali insieme: Percorsi per esperienze attivate e reattive e campagne orchestrate per iniziative pianificate basate su calendario.

>[!ENDSHADEBOX]

## Cos’è la segmentazione con più entità? {#multi-entity}

L’orchestrazione delle campagne in Adobe Journey Optimizer utilizza un database relazionale. Questo tipo di modello dati dispone di schemi separati di dati connessi tramite relazioni 1:1 o 1:many. Questo consente agli utenti di avviare una query su qualsiasi schema, non solo a livello di destinatario, e quindi di passare a altri schemi correlati, come acquisti, prodotti, prenotazioni o dettagli dei destinatari, fornendo grande flessibilità nella creazione di segmenti e tipi di pubblico e
raffinato.

>[!BEGINSHADEBOX]

**Esempio** - Esegui il targeting di tutti i destinatari con abbonamenti in scadenza nei successivi 30 giorni. In Campaign Orchestration la query può iniziare con lo schema Sottoscrizioni, cercare solo la colonna data di scadenza di tale schema e restituire tutte le sottoscrizioni in scadenza, quindi aggregare i dati del destinatario correlati a tali ID di abbonamenti specifici restituendo i risultati in modo più rapido ed efficiente rispetto ai modelli di dati che iniziano ogni query a livello di destinatario.

>[!ENDSHADEBOX]


## Come funziona il modello dati? {#data-model}

Le campagne utilizzano un **database relazionale**. Questo consente di eseguire query su diversi set di dati (ad esempio clienti, prodotti, abbonamenti) e di collegarli in modo flessibile per la segmentazione avanzata.

>[!BEGINSHADEBOX]

**Procedure consigliate**

* Organizza i set di dati in modo che **relazioni (join)** riflettano la logica di business.
* Evitare join non necessari per mantenere le query performanti.
* Convalidare i risultati del campione prima di eseguire estrazioni su larga scala.

>[!ENDSHADEBOX]

## Posso personalizzare i messaggi con questi dati? {#personalization}

Sì.  In Campaign Orchestration è possibile aggiornare un profilo destinatario noto come &quot;Entità persone&quot; e utilizzare i dati per la personalizzazione. Inoltre, i dati arricchiti da entità collegate nel database relazionale possono essere utilizzati anche per la personalizzazione. Puoi utilizzare i profili dei clienti insieme ai dati collegati (come acquisti o abbonamenti) per personalizzare i contenuti su tutti i canali supportati.

>[!BEGINSHADEBOX]

**Consigli**

* Utilizza **dati transazionali e comportamentali** per rendere le offerte rilevanti.
* Combina **attributi statici** (ad esempio, livello fedeltà) con **attributi dinamici** (ad esempio, data ultimo acquisto).
* Personalizzazione concisa: il sovraccarico dei messaggi con i dati può danneggiare la leggibilità.

>[!ENDSHADEBOX]


## Si integra con altre soluzioni Adobe? {#integrations}

Sì.  L’orchestrazione delle campagne è integrata in modo nativo con:

* **Customer Journey Analytics**: sono disponibili i report di orchestrazione campagna.
* **Real-Time CDP**: i tipi di pubblico generati nelle campagne possono essere letti in Real-Time CDP.
* **Federated Audience Composition (FAC)**: disponibile come componente aggiuntivo.

## E le autorizzazioni e il consenso? {#permissions}

Le autorizzazioni e il consenso per le campagne e i percorsi orchestrati sono gestiti centralmente in Adobe Experience Platform. Queste impostazioni vengono applicate in entrambe le soluzioni per ciascun destinatario prima dell’invio.

>[!BEGINSHADEBOX]

**Procedure consigliate**

* Applica **governance centralizzata**: evita di gestire separatamente il consenso a livello di campagna.
* Controlla periodicamente i dati del consenso per rilevare incongruenze.
* Rispetta **rinunce specifiche per il canale** — non presumere che il consenso globale copra tutti i canali.

>[!ENDSHADEBOX]

## Posso eseguire la segmentazione ad hoc? {#ad-hoc}

In Campaign Orchestration, si fa riferimento alla segmentazione ad hoc come &quot;segmentazione live&quot;, in cui è possibile accedere in tempo reale a tutti i dati disponibili nell’archivio relazionale, creare una query complessa e ottenere il risultato per l’attivazione immediata tramite canali in uscita (ad esempio, e-mail + SMS).

>[!BEGINSHADEBOX]

**Suggerimenti**

* Utilizza la segmentazione ad hoc per **esigenze urgenti** (ad esempio, promozioni flash).
* Salva e documenta le query utili in modo che possano essere riutilizzate nelle campagne future.
* Convalida il conteggio del pubblico prima dell’attivazione per evitare invii insufficienti o eccessivi.

>[!ENDSHADEBOX]



## Questo supporta le decisioni? {#decisioning}

Sì.  Il processo decisionale può utilizzare dati relazionali provenienti da campagne orchestrate. Una volta che lo schema relazionale è stato connesso con gli schemi XDM, i dati XDM possono essere utilizzati nel processo decisionale.

## Come funziona l’implementazione in ambienti diversi? {#deployment}

Gli oggetti creati nelle campagne orchestrate (ad esempio, tipi di pubblico e flussi di lavoro) sono legati alla sandbox in cui vengono generati. I flussi di lavoro standard per la creazione di pacchetti e l’implementazione in ambienti diversi (dev, stage, prod) non sono attualmente disponibili per le campagne orchestrate.

>[!BEGINSHADEBOX]

**Procedure consigliate**

* Gestisci **sandbox separate** per sperimentazione, controllo qualità e produzione.
* Configurazioni dei documenti complete per abilitare la replica manuale, se necessario.
* Allineati ai team di governance per ridurre la deviazione della configurazione tra gli ambienti.

>[!ENDSHADEBOX]

## Esistono procedure consigliate per l’esecuzione di campagne su larga scala? {#scale}

Sì, segui le best practice riportate di seguito:

* **Pianifica le campagne relative ai calendari aziendali** (lanci di prodotti, picchi stagionali) per allineare volume e risorse.
* Utilizza **anteprime del pubblico** prima di inviare per confermare le dimensioni previste ed evitare sorprese.
* Se possibile, **scagliona i tempi di invio** per evitare di sovraccaricare i sistemi a valle (ad esempio call center, siti Web).
* Stabilisci una **routine di monitoraggio**—tieni traccia dei registri di consegna, dei tassi di errore e delle rinunce dopo ogni invio.
* Esegui **analisi post-campagna** in Customer Journey Analytics per perfezionare il targeting e l&#39;orchestrazione per il ciclo successivo.



>[!MORELIKETHIS]
>
>* [Guardrail e limitazioni per campagne orchestrate](../orchestrated/guardrails.md)
>* [Introduzione a schemi e set di dati nelle campagne orchestrate](../orchestrated/gs-schemas.md)
>* [Crea la tua prima campagna orchestrata](../orchestrated/gs-campaign-creation.md)
>* [Descrizione del prodotto Journey Optimizer](https://helpx.adobe.com/it/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}
