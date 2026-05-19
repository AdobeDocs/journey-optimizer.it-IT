---
solution: Journey Optimizer
product: journey optimizer
title: Terminologia chiave
description: Termini e concetti essenziali in Adobe Journey Optimizer
feature: Get Started
role: Admin, Developer, User
level: Beginner
exl-id: 14e72376-87ad-4fae-bf8c-f347109d7903
TQID: https://experienceleague.adobe.com/-aDvt4RUXyf0EnPfFTJkG1CvWgte-1Fr6YaWvgcNNu4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: d2e8a157-b3b0-4143-9ff3-809bf400be56
  - id: e23d48b5-7858-4d45-9c56-9e2b4be8500e
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: b4ce14492d56e7121f827cf6a46abc5c222180e5
workflow-type: tm+mt
source-wordcount: 1760
ht-degree: 8%

---

# Terminologia chiave {#key-terminology}

Questa guida di riferimento definisce i termini essenziali che si incontrano quando si utilizza Adobe Journey Optimizer. Comprendere questi concetti consente di navigare nella piattaforma in tutta sicurezza e di collaborare in modo efficace con il team.

Per coppie di termini simili che vengono spesso confusi, ad esempio **Decisioning vs Decision Management** o **Schede di contenuto vs Messaggi in-app**, vedere [Quando i termini sono simili](#disambiguation) nella parte inferiore della pagina.

>[!TIP]
>
>Per spiegazioni dettagliate sulle funzioni e sui flussi di lavoro, consulta le sezioni specifiche della documentazione collegate in questa guida.

## Termini della piattaforma core {#core-terms}

| Termine | Definizione |
|------|------------|
| **Adobe Journey Optimizer** | Un’applicazione per creare e inviare messaggi personalizzati ai clienti su più canali (e-mail, SMS, notifiche push, web). Consente di progettare percorsi di clienti che rispondono alle azioni dei clienti in tempo reale. |
| **Adobe Experience Platform** | La base di Adobe Journey Optimizer che raccoglie e organizza tutti i dati dei clienti in un’unica posizione. Crea profili cliente unificati che Journey Optimizer utilizza per la personalizzazione. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html?lang=it){target="_blank"} |
| **Profilo cliente in tempo reale** | Vista unificata e in tempo reale di ciascun cliente che combina dati provenienti da più canali, inclusi dati online, offline, del sistema CRM e di terze parti. Ogni profilo viene aggiornato in modo dinamico man mano che i clienti interagiscono con il tuo marchio. [Ulteriori informazioni](../audience/get-started-profiles.md) |
| **Sandbox** | Un’area di lavoro separata per il test e la sperimentazione senza influire sulle comunicazioni live dei clienti. Adobe Journey Optimizer fornisce più sandbox per ambienti di sviluppo, test e produzione. [Ulteriori informazioni](../administration/sandboxes.md) |

## Termini di percorso e campagna {#journey-campaign-terms}

| Termine | Definizione |
|------|------------|
| **Percorso** | Una serie di passaggi collegati che guidano i clienti attraverso esperienze con il tuo marchio nel tempo. Ogni passaggio si verifica in base alle azioni del cliente o ai trigger temporali, abilitando interazioni sequenziali e personalizzate. [Ulteriori informazioni](../building-journeys/journey.md) |
| **Campaign** | Azione di marketing coordinata che fornisce contenuti a un pubblico specifico su uno o più canali. A differenza dei percorsi, le campagne eseguono azioni simultaneamente. Journey Optimizer supporta tre tipi di campagne: **Campagne azione** (invii batch pianificati), **Campagne attivate da API** (messaggistica basata su eventi in tempo reale tramite API) e **Campagne orchestrate** (flussi di lavoro complessi, con più passaggi e un&#39;area di lavoro visiva). [Ulteriori informazioni](../campaigns/get-started-with-campaigns.md) |
| **Evento** | Azione o occorrenza che attiva o avanza un percorso. Gli eventi possono essere azioni del cliente (acquisto, abbandono di un carrello) o eventi di sistema (data/ora, modifica dei dati). [Ulteriori informazioni](../event/about-events.md) |
| **Canale** | Il metodo utilizzato per comunicare con i clienti: e-mail, SMS, notifiche push, messaggi in-app, web o direct mail. Ogni canale richiede una configurazione specifica. [Ulteriori informazioni](../configuration/get-started-configuration.md) |

## Termini cliente e pubblico {#customer-audience-terms}

| Termine | Definizione |
|------|------------|
| **Pubblico** | Un gruppo di clienti che condividono caratteristiche o comportamenti comuni, ad esempio &quot;clienti che hanno acquistato negli ultimi 30 giorni&quot; o &quot;membri di programmi fedeltà&quot;. I tipi di pubblico vengono utilizzati per eseguire il targeting di segmenti di clienti specifici. [Ulteriori informazioni](../audience/about-audiences.md) |
| **Qualificazione del pubblico** | Il processo automatico che si verifica quando un cliente si unisce o esce da un pubblico. Journey Optimizer può attivare azioni quando qualcuno entra o esce da un pubblico, garantendo comunicazioni tempestive e pertinenti. [Ulteriori informazioni](../building-journeys/audience-qualification-events.md) |
| **Pubblico coinvolgibile** | Il numero di profili cliente che è possibile contattare attivamente tramite Adobe Journey Optimizer in base al contratto di licenza. In genere si tratta di profili coinvolti negli ultimi 12 mesi. |
| **Profilo di prova** | Profili fittizi utilizzati per testare e visualizzare in anteprima i messaggi prima di inviarli a clienti reali. I profili di test consentono di verificare la personalizzazione, il contenuto e la logica di percorso. [Ulteriori informazioni](../audience/creating-test-profiles.md) |

## Contenuto e termini di personalizzazione {#content-terms}

| Termine | Definizione |
|------|------------|
| **Personalizzazione** | Il processo di personalizzazione dei contenuti per singoli clienti utilizzando i dati di profilo, le preferenze e i comportamenti. Ad esempio, inserendo il nome di un cliente o mostrando i consigli di prodotto in base alla cronologia di navigazione. [Ulteriori informazioni](../personalization/personalize.md) |
| **Modello contenuto** | Un design di messaggi riutilizzabile che può essere utilizzato in più campagne e percorsi per mantenere la coerenza del brand e accelerare la creazione di contenuti. [Ulteriori informazioni](../content-management/content-templates.md) |
| **Frammento** | Un blocco di contenuto riutilizzabile (ad esempio un’intestazione, un piè di pagina o un banner promozionale) che può essere utilizzato in più messaggi per garantire la coerenza e abilitare gli aggiornamenti centralizzati. [Ulteriori informazioni](../content-management/fragments.md) |
| **Pagina di destinazione** | Pagina Web autonoma in cui i clienti possono acconsentire o rinunciare alle comunicazioni, abbonarsi ai servizi o fornire informazioni tramite moduli online. [Ulteriori informazioni](../landing-pages/get-started-lp.md) |
| **Esperimento contenuti** | Un framework di test A/B che divide un pubblico in gruppi casuali e distribuisce diverse varianti di messaggio (contenuto, oggetto o offerta) a ciascun gruppo, quindi identifica la variante con le prestazioni migliori in base a una metrica di successo definita. [Ulteriori informazioni](../content-management/get-started-experiment.md) |
| **Sperimentazione** | La più ampia funzionalità di Journey Optimizer per testare e ottimizzare le decisioni: gli esperimenti sui contenuti testano le varianti dei messaggi in campagne e percorsi, mentre i test di sperimentazione decisionali offrono strategie di selezione. Entrambi utilizzano l’analisi statistica per identificare gli approcci vincenti. [Ulteriori informazioni](../content-management/get-started-experiment.md) |

## Decisione e condizioni dell’offerta {#decision-terms}

| Termine | Definizione |
|------|------------|
| **Funzione Decisioni** | Il framework decisionale di ultima generazione in Journey Optimizer, consigliato per le nuove implementazioni. Offre gestione del catalogo di elementi basata su schema, regole di raccolta flessibili, componenti decisionali riutilizzabili e funzionalità di sperimentazione. Disponibile per esperienze basate su codice, push, SMS ed e-mail (disponibilità limitata). [Ulteriori informazioni](../experience-decisioning/gs-experience-decisioning.md) |
| **Gestione delle decisioni** | La funzionalità legacy di Offer Decisioning in Journey Optimizer. Utilizza una libreria centrale di offerte di marketing e un motore decisionale basato su regole che applica vincoli ai profili cliente in tempo reale. È ancora supportato per le implementazioni esistenti, ma le nuove implementazioni devono utilizzare il decisioning. Supporta e-mail, in-app, push, SMS e direct mail. [Ulteriori informazioni](../offers/get-started/starting-offer-decisioning.md) |
| **Offerta** | Un messaggio di marketing, uno sconto o una promozione che può essere presentato ai clienti. Le offerte includono regole di idoneità che determinano quali clienti possono riceverle. [Ulteriori informazioni](../offers/offer-library/creating-personalized-offers.md) |
| **Criteri di decisione** | Un insieme di regole e strategie che determinano quale offerta mostrare a quale cliente in un determinato momento, in base a vincoli come idoneità, priorità e regole di limitazione. [Ulteriori informazioni](../experience-decisioning/create-decision.md) |

## Dati e termini di configurazione {#data-config-terms}

| Termine | Definizione |
|------|------------|
| **Schema** | Struttura che definisce il modo in cui i dati vengono organizzati in Adobe Experience Platform, inclusi i nomi dei campi, i tipi di dati e le relazioni. Gli schemi garantiscono la coerenza dei dati tra i sistemi. [Ulteriori informazioni](../data/get-started-schemas.md) |
| **Set di dati** | Una raccolta di dati (in genere una tabella) che segue uno schema specifico. I set di dati memorizzano i dati dei clienti, gli eventi di interazione e altre informazioni utilizzate per la personalizzazione. [Ulteriori informazioni](../data/get-started-datasets.md) |
| **Configurazione canale** | Le impostazioni che definiscono il modo in cui i messaggi vengono consegnati per un canale specifico, inclusi i dettagli del mittente, il sottodominio, il pool IP e il tipo di messaggio (marketing o transazionale). Precedentemente denominati &quot;surface&quot; o &quot;preset&quot; nella documentazione precedente. [Ulteriori informazioni](../configuration/channel-surfaces.md) |
| **Elenco di eliminazione** | Un elenco di indirizzi e-mail e domini automaticamente esclusi dalla consegna dei messaggi a causa di mancati recapiti permanenti, segnalazioni di spam o aggiunte manuali. L’invio a indirizzi soppressi è bloccato per proteggere il recapito messaggi e la reputazione del mittente. [Ulteriori informazioni](../reports/suppression-list.md) |

## Termini di conflitto e definizione delle priorità {#conflict-terms}

| Termine | Definizione |
|------|------------|
| **Set di regole** | Un gruppo denominato di regole aziendali applicate a percorsi e campagne per gestire il comportamento di messaggistica. Un set di regole può combinare il limite di frequenza, i limiti di ingresso del percorso e le ore non interattive in un unico criterio riutilizzabile. [Ulteriori informazioni](../conflict-prioritization/rule-sets.md) |
| **Limite di frequenza** | Una regola all’interno di un set di regole che limita il numero di messaggi che un profilo può ricevere in un dato periodo di tempo, per canale o tipo di comunicazione (vendite, promozioni, ecc.). I profili che superano il limite vengono automaticamente esclusi dalla consegna. [Ulteriori informazioni](../conflict-prioritization/channel-capping.md) |

>[!NOTE]
>
>Per un glossario completo dei termini di Adobe Experience Platform, consulta il [glossario di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/glossary.html?lang=it){target="_blank"}.

## Quando i termini sono simili: guida alla disambiguazione {#disambiguation}

Adobe Journey Optimizer è cresciuto nel corso degli anni, il che significa che alcune aree funzionali condividono nomi simili. Utilizza le tabelle seguenti per identificare rapidamente quale funzionalità soddisfa le tue esigenze.

### Decisioning e gestione delle decisioni {#decisioning-vs-dm}

Entrambe le funzionalità selezionano e forniscono le offerte, ma servono diverse fasi del ciclo di vita del prodotto.

| | Funzione Decisioni | Gestione delle decisioni |
|---|---|---|
| **Stato** | Corrente: consigliata per tutte le nuove implementazioni | **Legacy** — ancora supportato, ma non più consigliato per le nuove implementazioni |
| **Introdotto** | 2024 | 2021 |
| **Catalogo elementi** | Metadati flessibili basati su schema | Libreria di offerte centralizzata |
| **Canali supportati** | Esperienza basata su codice, push, SMS, e-mail (disponibilità limitata) | E-mail, In-app, push, SMS, direct mail |
| **Differenziatore chiave** | Componenti decisionali riutilizzabili, sperimentazione, roadmap di canale più ampia | Motore di vincoli collaudato; migrazione a Decisioning per nuovi progetti |
| **Introduzione** | [Funzione Decisioni](../experience-decisioning/gs-experience-decisioning.md) | [Gestione delle decisioni](../offers/get-started/starting-offer-decisioning.md) |

Se stai utilizzando la funzione di gestione delle decisioni e desideri effettuare il passaggio, consulta la [guida alla migrazione](../experience-decisioning/migrate-to-decisioning.md).

### Tipi di campagna {#campaign-types-disambiguation}

Journey Optimizer offre tre tipi di campagne attivate in modo diverso e distribuite per casi d’uso distinti.

| | Campagne di azione (campagne pianificate) | Campagne attivate da API | Campagne orchestrate |
|---|---|---|---|
| **Attivazione** | Manuale o programmato | Chiamata API esterna | Area di lavoro del flusso di lavoro visivo |
| **Ottimo per** | Invii in batch una tantum o ricorrenti (newsletter, promozioni) | Messaggistica basata su eventi in tempo reale (conferme d&#39;ordine, reimpostazioni password) | Programmi cross-channel complessi e con più passaggi |
| **Origine Personalization** | Attributi del profilo | Attributi del profilo + contesto del payload API | Attributi del profilo + dati relazionali |
| **Introduzione** | [Campagne con azioni](../campaigns/create-campaign.md) | [Campagne attivate da API](../campaigns/api-triggered-campaigns.md) | [Campagne orchestrate](../orchestrated/gs-orchestrated-campaigns.md) |

Per una panoramica completa di tutti i tipi di campagna e di quando utilizzarli, consulta [Introduzione alle campagne](../campaigns/get-started-with-campaigns.md).

### Limitazione di frequenza e arbitrato di percorso {#capping-vs-arbitration}

Entrambi sono meccanismi di set di regole nel set di strumenti per conflitti e definizione delle priorità, ma affrontano problemi diversi.

| | Quota limite | Arbitrato del percorso |
|---|---|---|
| **Problema risolto** | Un profilo riceve troppi messaggi nel tempo | Un profilo è idoneo per più percorsi contemporaneamente |
| **Ambito** | Per canale e tipo di comunicazione (vendite, promozioni, ecc.) | Iscrizione percorso: numero di percorsi simultanei o percorso vincitore |
| **Meccanismo** | Limita il numero di messaggi per periodo; esclude automaticamente i profili sollecitati eccessivamente | Utilizza punteggi di priorità e regole di limitazione per decidere quale percorso inserire in un profilo |
| **Configurato in** | Set di regole → limite di frequenza | Imposta regole → limite e arbitrato del Percorso |
| **Ulteriori informazioni** | [Imposta il limite di frequenza per canale](../conflict-prioritization/channel-capping.md) | [Gestione limite percorso e arbitrato](../conflict-prioritization/journey-capping.md) |

### Schede di contenuto e messaggi in-app {#content-cards-vs-in-app}

Entrambi i canali distribuiscono messaggi all’interno di un’app mobile o web, ma presentano diversi modelli di rendering e comportamenti di persistenza.

| | Schede di contenuto | Messaggi in-app |
|---|---|---|
| **Modello di visualizzazione** | Schede persistenti incorporate nell’interfaccia utente dell’app (feed, casella in entrata o superficie personalizzata) | Sovrapposizioni, banner o moduli transitori mostrati sopra l’app |
| **Persistenza** | Rimane visibile fino a quando non viene esplicitamente ignorato o scaduto | Scompare quando l’utente interagisce o lo chiude |
| **Trigger** | SDK esegue il rendering al caricamento; le regole controllano la visualizzazione e l’eliminazione | Un evento in tempo reale nel percorso o nella campagna attiva la consegna |
| **Ottimo per** | Promozioni in corso, stato di fedeltà, avvisi persistenti | Suggerimenti per l’onboarding, offerte a tempo limitato, notifiche transitorie |
| **Introduzione** | [Schede contenuto](../content-card/create-content-card.md) | [Messaggi in-app](../in-app/get-started-in-app.md) |

>[!NOTE]
>
>**Adobe Journey Optimizer e Journey Optimizer B2B edition:** si tratta di due prodotti distinti della stessa famiglia di marchi. Adobe Journey Optimizer (questa documentazione) è destinato ai percorsi di clienti B2C. Journey Optimizer B2B edition è progettato appositamente per il marketing basato su account, per lavorare con gruppi di acquisto e tipi di pubblico di account. Se stai cercando la documentazione di B2B edition, visita la [guida di Journey Optimizer B2B edition](https://experienceleague.adobe.com/it/docs/journey-optimizer-b2b/user/guide-overview){target="_blank"}.

## Argomenti correlati {#related-topics}

* [Comprensione del funzionamento di Journey Optimizer](understanding-ajo.md): scopri come percorsi, campagne, profili e canali si adattano all&#39;architettura del prodotto.
* [Introduzione alle funzionalità decisionali](../experience-decisioning/gs-decision.md): confronto affiancato di decisioning e gestione delle decisioni e scelta dell&#39;approccio corretto per l&#39;implementazione.
* [Introduzione ai percorsi](../building-journeys/journey.md): scopri come creare esperienze cliente sequenziali e attivate da eventi, passo dopo passo.
* [Guida introduttiva alle campagne](../campaigns/get-started-with-campaigns.md): scopri i tre tipi di campagne (Azione, Attivata da API, Orchestrata) e quando utilizzarle.
* [Gestione dei conflitti e definizione delle priorità](../conflict-prioritization/gs-conflict-prioritization.md): scopri come utilizzare i set di regole, i limiti di frequenza, i punteggi di priorità e le ore non interattive per evitare messaggi eccessivi.
* [Introduzione ai canali di comunicazione](../channels/gs-channels.md): sfoglia tutti i canali disponibili, i relativi prerequisiti e come configurarli.
