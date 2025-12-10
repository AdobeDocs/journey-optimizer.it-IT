---
solution: Journey Optimizer
product: journey optimizer
title: Terminologia chiave
description: Termini e concetti essenziali in Adobe Journey Optimizer
feature: Get Started
role: Admin, Developer, User
level: Beginner
source-git-commit: 4ae9e908d259dbd266417242cf9e65d693227061
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 9%

---

# Terminologia chiave {#key-terminology}

Questa guida di riferimento definisce i termini essenziali che si incontrano quando si utilizza Adobe Journey Optimizer. Comprendere questi concetti consente di navigare nella piattaforma in tutta sicurezza e di collaborare in modo efficace con il team.

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
| **Campaign** | Una singola comunicazione o un insieme di comunicazioni inviate a un pubblico specifico. A differenza dei percorsi che si svolgono nel tempo, le campagne distribuiscono i messaggi secondo una pianificazione o un’attivazione, immediatamente o in un momento specifico. [Ulteriori informazioni](../campaigns/get-started-with-campaigns.md) |
| **Evento** | Azione o occorrenza che attiva o avanza un percorso. Gli eventi possono essere azioni del cliente (acquisto, abbandono di un carrello) o eventi di sistema (data/ora, modifica dei dati). [Ulteriori informazioni](../event/about-events.md) |
| **Canale** | Il metodo utilizzato per comunicare con i clienti: e-mail, SMS, notifiche push, messaggi in-app, web o direct mail. Ogni canale richiede una configurazione specifica. [Ulteriori informazioni](../configuration/get-started-configuration.md) |

## Termini cliente e pubblico {#customer-audience-terms}

| Termine | Definizione |
|------|------------|
| **Pubblico** | Un gruppo di clienti che condividono caratteristiche o comportamenti comuni, ad esempio &quot;clienti che hanno acquistato negli ultimi 30 giorni&quot; o &quot;membri di programmi fedeltà&quot;. I tipi di pubblico vengono utilizzati per eseguire il targeting di segmenti di clienti specifici. [Ulteriori informazioni](../audience/about-audiences.md) |
| **Qualificazione del pubblico** | Il processo automatico che si verifica quando un cliente si unisce o esce da un pubblico. Journey Optimizer può attivare azioni quando qualcuno entra o esce da un pubblico, garantendo comunicazioni tempestive e pertinenti. [Ulteriori informazioni](../building-journeys/audience-qualification-events.md) |
| **Pubblico coinvolgibile** | Il numero di profili cliente che è possibile contattare attivamente tramite Adobe Journey Optimizer in base al contratto di licenza. In genere si tratta di profili coinvolti negli ultimi 12 mesi. |
| **Profilo di prova** | Profili fittizi utilizzati per testare e visualizzare in anteprima i messaggi prima di inviarli a clienti reali. I profili di test consentono di verificare la personalizzazione, il contenuto e la logica di percorso. [Ulteriori informazioni](../audience/creating-test-profiles.md) |

## Termini e condizioni per contenuto e Personalization {#content-terms}

| Termine | Definizione |
|------|------------|
| **Personalizzazione** | Il processo di personalizzazione dei contenuti per singoli clienti utilizzando i dati di profilo, le preferenze e i comportamenti. Ad esempio, inserendo il nome di un cliente o mostrando i consigli di prodotto in base alla cronologia di navigazione. [Ulteriori informazioni](../personalization/personalize.md) |
| **Modello contenuto** | Un design di messaggi riutilizzabile che può essere utilizzato in più campagne e percorsi per mantenere la coerenza del brand e accelerare la creazione di contenuti. [Ulteriori informazioni](../content-management/content-templates.md) |
| **Frammento** | Un blocco di contenuto riutilizzabile (ad esempio un’intestazione, un piè di pagina o un banner promozionale) che può essere utilizzato in più messaggi per garantire la coerenza e abilitare gli aggiornamenti centralizzati. [Ulteriori informazioni](../content-management/fragments.md) |
| **Pagina di destinazione** | Pagina Web autonoma in cui i clienti possono acconsentire o rinunciare alle comunicazioni, abbonarsi ai servizi o fornire informazioni tramite moduli online. [Ulteriori informazioni](../landing-pages/get-started-lp.md) |

## Decisione e condizioni dell’offerta {#decision-terms}

| Termine | Definizione |
|------|------------|
| **Gestione delle decisioni** | Funzione che seleziona automaticamente il contenuto o l’offerta migliore per ciascun cliente in base ai dati di profilo in tempo reale, al contesto e alle regole aziendali. [Ulteriori informazioni](../offers/get-started/starting-offer-decisioning.md) |
| **Offerta** | Un messaggio di marketing, uno sconto o una promozione che può essere presentato ai clienti. Le offerte includono regole di idoneità che determinano quali clienti possono riceverle. [Ulteriori informazioni](../offers/offer-library/creating-personalized-offers.md) |
| **Criteri di decisione** | Un insieme di regole e strategie che determinano quale offerta mostrare a quale cliente in un determinato momento, in base a vincoli come idoneità, priorità e regole di limitazione. [Ulteriori informazioni](../experience-decisioning/create-decision.md) |

## Dati e termini di configurazione {#data-config-terms}

| Termine | Definizione |
|------|------------|
| **Schema** | Struttura che definisce il modo in cui i dati vengono organizzati in Adobe Experience Platform, inclusi i nomi dei campi, i tipi di dati e le relazioni. Gli schemi garantiscono la coerenza dei dati tra i sistemi. [Ulteriori informazioni](../data/get-started-schemas.md) |
| **Set di dati** | Una raccolta di dati (in genere una tabella) che segue uno schema specifico. I set di dati memorizzano i dati dei clienti, gli eventi di interazione e altre informazioni utilizzate per la personalizzazione. [Ulteriori informazioni](../data/get-started-datasets.md) |

>[!NOTE]
>
>Per un glossario completo dei termini di Adobe Experience Platform, consulta il [glossario di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/glossary.html?lang=it){target="_blank"}.

## Argomenti correlati {#related-topics}

* [Come funziona Journey Optimizer](understanding-ajo.md)
* [Introduzione all’interfaccia utente](user-interface.md)
* [Scegli il tuo ruolo e il percorso di apprendimento](quick-start.md)

