---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione ai percorsi
description: Introduzione ai percorsi
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: percorsi, scopri, inizia
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
version: Journey Orchestration
source-git-commit: cfac40f73a68362f8490de28cf1865f3dd4952f7
workflow-type: tm+mt
source-wordcount: '1139'
ht-degree: 30%

---


# Introduzione ai percorsi{#jo-general-principle}

I percorsi in Adobe Journey Optimizer consentono di creare percorsi cliente personalizzati e a più passaggi che si adattano in tempo reale al comportamento e alle esigenze del pubblico. Utilizzando un’area di lavoro intuitiva basata su trascinamento, puoi orchestrare messaggi e azioni tra più canali, sfruttando i dati contestuali e il targeting del pubblico per il massimo impatto. Esplorando trigger in tempo reale, gestendo le proprietà del percorso o utilizzando strumenti avanzati come azioni ed espressioni personalizzate, questa sezione fornisce una chiara roadmap per aiutarti a progettare e perfezionare percorsi che forniscano esperienze cliente significative e tempestive.

Utilizza [!DNL Journey Optimizer] per generare casi d’uso di orchestrazione in tempo reale, sfruttando i dati contestuali memorizzati in eventi o in origini dati. Puoi progettare scenari avanzati in più passaggi con le seguenti funzionalità:

* Invia **consegna unitaria** in tempo reale attivata quando viene ricevuto un [evento](general-events.md) o **in batch** utilizzando [tipi di pubblico](read-audience.md) di Adobe Experience Platform.

* Sfrutta **dati contestuali** da [eventi](../event/about-events.md), informazioni da Adobe Experience Platform o dati da servizi API di terze parti tramite [origini dati](../datasource/about-data-sources.md).

* Utilizza le **[azioni incorporate](journeys-message.md)** per inviare messaggi progettati in [!DNL Journey Optimizer] o crea **[azioni personalizzate](using-custom-actions.md)** se utilizzi un sistema di terze parti l’invio dei messaggi.

* Con **[Progettazione percorsi](using-the-journey-designer.md)**, genera i tuoi casi d&#39;uso a più passaggi: trascina facilmente un evento di partecipazione o un&#39;attività [Read audience](read-audience.md), aggiungi [condizioni](condition-activity.md) e invia messaggi personalizzati.

Journey Optimizer [Progettazione percorsi](using-the-journey-designer.md) fornisce tutto ciò di cui gli addetti al marketing e i professionisti del percorso hanno bisogno per orchestrare più passaggi di 1:1 percorsi tra i canali. Ciò include un’area di lavoro intuitiva con trascinamento per orchestrare ogni passaggio del percorso, definire il pubblico target e includere messaggi, offerte e contenuti tra i canali visualizzati dai membri del pubblico target in base a comportamento, dati contestuali ed eventi di business. Esplora [casi d&#39;uso reali](jo-use-cases.md) per scoprire come applicare queste funzionalità.

➡️ [Scopri Journey Optimizer nel video](#video)

## Panoramica sui percorsi

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=it)

Guida introduttiva alla creazione di Percorsi

Indicazioni dettagliate sulla progettazione, il test, la pubblicazione e il tracciamento dei percorsi cliente per creare campagne omnicanale personalizzate.

[Creare il primo percorso](journey-gs.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=it)

Journey Orchestration - Guida completa

Documentazione completa che tratta tutti gli aspetti relativi alla creazione, alla gestione e all&#39;ottimizzazione del percorso in Adobe Journey Optimizer.

[Esplora la guida completa](journey-get-started.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=it)

Gestione dei Percorsi

Gestisci i percorsi cliente in modo efficiente con strumenti per filtrare, gestire i profili, i fusi orari e le tecniche di ottimizzazione.

[Scopri la gestione del percorso](/help/rp_landing_pages/manage-journey-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=it)

Attività percorso

Scopri come configurare e utilizzare attività come trigger, passaggi decisionali, gestione del pubblico e messaggistica personalizzata nei percorsi.

[Esplora le attività](/help/rp_landing_pages/about-journey-building-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=it)

Creazione di espressioni

Diventa esperto nella creazione di espressioni principali per flussi di lavoro dinamici, nella manipolazione di dati e nell’orchestrazione dei percorsi avanzata tramite potenti strumenti e sintassi.

[Informazioni sulle espressioni](/help/rp_landing_pages/building-advanced-conditions-journeys-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=it)

Casi d’uso percorso

Esplora le applicazioni reali di Adobe Journey Optimizer, inclusa la messaggistica multicanale e l’integrazione con sistemi esterni.

[Scopri i casi d’uso](/help/rp_landing_pages/journey-use-cases-landing-page.md)
:::

::::

## Cosa si può fare con i percorsi?

Dal designer del percorso, i marketer possono inviare messaggi 1:1 in tempo reale attivati tramite qualsiasi canale quando si verifica un evento. Ad esempio, quando una persona si iscrive a un servizio, può [essere attivata un’e-mail di benvenuto](message-to-subscribers-uc.md), invitandola ad accedere all’app per la prima volta e a impostare le proprie preferenze. Azioni quali il completamento dell’acquisto, l’apertura dell’e-mail e l’accesso all’app possono essere utilizzate per far avanzare i nuovi clienti lungo i relativi percorsi.

## Tipi di percorso

Adobe Journey Optimizer supporta quattro tipi di percorsi, ciascuno progettato per casi d&#39;uso e meccanismi di accesso diversi. Scegli il tipo giusto in base a come desideri che i profili entrino e progrediscano nelle esperienze dei clienti.

>[!BEGINTABS]

>[!TAB percorsi unitari]

**I percorsi unitari** vengono attivati singolarmente da un evento quando si verifica un&#39;azione specifica, ad esempio un acquisto, l&#39;accesso all&#39;app o l&#39;invio di un modulo. I profili entrano nel percorso uno alla volta in tempo reale quando viene ricevuto l’evento, rendendolo ideale per esperienze personalizzate e guidate dal comportamento.

**Caratteristiche chiave:**

* Immissione in tempo reale basata su eventi
* Elaborazione di singoli profili
* Ideale per messaggi transazionali e risposte immediate
* Supporta dati contestuali dall&#39;evento che attiva

**Casi d&#39;uso:**

* Conferma ordine dopo l’acquisto
* E-mail di benvenuto quando qualcuno si abbona
* Abbandono del carrello attivato dal comportamento di navigazione
* Notifiche di reimpostazione della password

➡️ [Informazioni sulla configurazione dell&#39;evento](../event/about-events.md) | [Eventi generali](general-events.md) | [Caso di utilizzo: messaggio agli abbonati](message-to-subscribers-uc.md)

>[!TAB Leggi percorsi di pubblico]

**Leggi percorsi di pubblico** inizia con un pubblico da Adobe Experience Platform e invia messaggi in batch a tutti i profili del pubblico. Questo tipo di percorso elabora l’intero pubblico contemporaneamente, rendendolo ideale per campagne pianificate e comunicazioni ricorrenti.

**Caratteristiche chiave:**

* Elaborazione in batch di segmenti di pubblico
* Esecuzione pianificata o occasionale
* Tutti i profili entrano contemporaneamente
* Supporto di comunicazioni su larga scala

**Casi d&#39;uso:**

* Newsletter mensili
* Campagne promozionali per il targeting dei segmenti
* Annunci di prodotti a tutti i clienti
* Campagne di marketing stagionale

➡️ [Scopri l&#39;attività Read Audience](read-audience.md) | [Introduzione ai tipi di pubblico](../audience/about-audiences.md) | [Caso di utilizzo della messaggistica multicanale](journeys-uc.md)

>[!TAB percorsi di qualificazione del pubblico]

**I percorsi di qualificazione del pubblico** vengono attivati quando i profili si qualificano per (o escono da) un segmento di pubblico specifico. I profili entrano nel percorso singolarmente in quanto soddisfano i criteri di pubblico in tempo reale, consentendo un coinvolgimento immediato quando il comportamento del cliente cambia.

**Caratteristiche chiave:**

* Immissione in tempo reale basata sulla qualifica
* Monitoraggio continuo dell’iscrizione al pubblico
* Elaborazione di singoli profili in base ai requisiti
* Il meglio con i tipi di pubblico in streaming

**Casi d&#39;uso:**

* Notifiche di aggiornamento livello VIP
* Nuovo coinvolgimento quando i clienti diventano inattivi
* Messaggi celebrativi per il primo acquisto
* Targeting geografico quando i clienti si spostano

➡️ [Scopri le qualificazioni per il pubblico](audience-qualification-events.md) | [Attività condizione](condition-activity.md) | [Creazione delle definizioni dei segmenti](../audience/creating-a-segment-definition.md)

>[!TAB percorsi di eventi di business]

**I percorsi di eventi di business** sono attivati da eventi di business (come aggiornamenti delle azioni, avvisi meteo o variazioni di prezzo) che interessano più profili contemporaneamente. Anziché reagire alle azioni dei singoli clienti, questi percorsi rispondono a condizioni aziendali più ampie o a fattori esterni.

**Caratteristiche chiave:**

* Attivato da eventi a livello aziendale, non da singole azioni
* Interessa più profili contemporaneamente
* Indirizza un pubblico specifico quando si verifica l&#39;evento
* Combina la tempistica basata sugli eventi con il targeting del pubblico

**Casi d&#39;uso:**

* Avvisi di inventario ridotti per i clienti interessati
* Annunci di vendita flash
* Promozioni in base al tempo
* Notifiche di riduzione prezzo
* Avvisi back-in-stock del prodotto

➡️ [Informazioni sugli eventi di business](general-events.md) | [Configura eventi di business](../event/about-creating-business.md) | [Gestione delle voci](entry-management.md)

>[!ENDTABS]

## Designer percorso{#journey-designer}

[Progettazione percorsi](using-the-journey-designer.md) è un&#39;area di lavoro intuitiva che consente di creare e orchestrare visivamente i percorsi di clienti. Offre tutto il necessario per progettare esperienze in più passaggi:

* **[Azioni canale incorporate](journeys-message.md)** - Invia messaggi tramite e-mail, notifiche push, SMS/MMS, in-app, web, esperienze basate su codice e altro ancora, tutte progettate direttamente in Journey Optimizer
* **[Azioni personalizzate](using-custom-actions.md)** - Integra sistemi di terze parti per inviare messaggi o attivare flussi di lavoro in piattaforme esterne
* **[Attività di orchestrazione](about-journey-activities.md)** - Aggiungi logica, condizioni, tempi di attesa e targeting del pubblico per creare esperienze cliente sofisticate
* **[Condizioni](condition-activity.md)** - Crea un ramo del percorso in base agli attributi del profilo, all&#39;iscrizione al pubblico o a eventi in tempo reale
* **[Espressioni](expression/expressionadvanced.md)** - Crea logica e personalizzazione avanzate utilizzando l&#39;editor espressioni

Scopri come utilizzare la finestra di progettazione del percorso [in questi casi d&#39;uso end-to-end](jo-use-cases.md).

>[!NOTE]
>
>I guardrail e le limitazioni applicabili ai percorsi sono descritti in [questa pagina](../start/guardrails.md).

## Video dimostrativo {#video}

Scopri i componenti di un percorso e le nozioni di base sulla creazione di un percorso nell’area di lavoro.

>[!VIDEO](https://video.tv.adobe.com/v/3430348?captions=ita&quality=12)

## Risorse aggiuntive {#additional-resources}

* **[Risoluzione dei problemi dei Percorsi di clienti](/help/rp_landing_pages/troubleshoot-journey-landing-page.md)** - Diagnosi e risoluzione dei problemi di esecuzione del percorso con strumenti, codici di errore e best practice per il debug e l&#39;ottimizzazione
* **[Domande frequenti sui percorsi](journey-faq.md)**: domande frequenti sui percorsi
* **[Avvisi Percorso](../reports/alerts.md)** - Imposta gli avvisi per il monitoraggio del percorso e invia notifiche per aggiornamenti in tempo reale
* **[Riferimento ai codici di errore](error-codes-reference.md)**: codici di errore del percorso e passaggi per la risoluzione dei problemi
* **[Risoluzione dei problemi](troubleshooting.md)**: problemi e soluzioni comuni del percorso
* **[Esercitazioni Percorso (video)](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/journeys/journey-designer-overview){target="_blank"}** - Scopri la creazione di percorsi tramite esercitazioni video pratiche che includono funzionalità, funzionalità e best practice
