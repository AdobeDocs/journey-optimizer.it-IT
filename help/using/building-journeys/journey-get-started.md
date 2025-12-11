---
solution: Journey Optimizer
product: journey optimizer
title: Journey Orchestration - Guida completa
description: Guida introduttiva all’orchestrazione dei percorsi in Adobe Journey Optimizer
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
hide: true
hidefromtoc: true
keywords: percorso, orchestrazione, guida introduttiva, onboarding, funzionalità
source-git-commit: 902790b2e172ef02e868592794fc110d3e14ac07
workflow-type: tm+mt
source-wordcount: '810'
ht-degree: 50%

---


# Journey Orchestration - Guida completa{#journey-orchestration-guide}

I percorsi in Adobe Journey Optimizer consentono di creare percorsi cliente personalizzati e a più passaggi che si adattano in tempo reale al comportamento e alle esigenze del pubblico. Utilizzando un’area di lavoro intuitiva basata su trascinamento, puoi orchestrare messaggi e azioni tra più canali, sfruttando i dati contestuali e il targeting del pubblico per il massimo impatto.

Esplorando trigger in tempo reale, gestendo le proprietà del percorso o utilizzando strumenti avanzati come azioni ed espressioni personalizzate, questa guida fornisce una chiara roadmap per progettare e perfezionare con sicurezza i percorsi che forniscono esperienze cliente significative e tempestive.

➡️ [Scopri Journey Optimizer nel video](#video)

>[!BEGINTABS]

>[!TAB Panoramica]

## Cosa sono i percorsi?

Utilizza [!DNL Journey Optimizer] per generare casi d’uso di orchestrazione in tempo reale, sfruttando i dati contestuali memorizzati in eventi o in origini dati. Progetta scenari avanzati a più passaggi che rispondano in tempo reale al comportamento dei clienti e agli eventi di business.

Il designer del percorso di Journey Optimizer fornisce tutto ciò che serve ai marketer e professionisti del percorso per orchestrare percorsi 1:1 in più passaggi su più canali. Ciò include un’area di lavoro intuitiva con modalità di trascinamento per orchestrare ogni passaggio del percorso, definire il pubblico target e includere messaggi, offerte e contenuti tra i canali che i membri del pubblico target visualizzeranno in base al comportamento, ai dati contestuali e agli eventi di business.

![Interfaccia di Progettazione Percorsi con riquadro palette, area di lavoro e proprietà](assets/journey38.png)

**Iniziare la generazione?** Scopri come creare e progettare il tuo primo percorso in [questa pagina](journey-gs.md).

>[!TAB Funzionalità chiave]

## Cosa si può fare con i percorsi?

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/send-real-time.svg)

**Consegna in tempo reale e in batch**

Invia in tempo reale una **consegna unitaria** attivata quando viene ricevuto un evento o **in batch** utilizzando i tipi di pubblico di Adobe Experience Platform.

[Informazioni sulla voce percorso](entry-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/data.svg)

**Dati contestuali**

Sfrutta **dati contestuali** da eventi, informazioni da Adobe Experience Platform o dati da servizi API di terze parti.

[Utilizzare le origini dati](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/message.svg)

**Azioni incorporate**

Utilizza **azioni di canale integrate** per inviare messaggi progettati in [!DNL Journey Optimizer] tramite e-mail, push, SMS/MMS e altro ancora.

[Inviare messaggi in percorsi](journeys-message.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code.svg)

**Azioni personalizzate**

Crea **azioni personalizzate** se utilizzi un sistema di terze parti per inviare i messaggi o connettersi alle API esterne.

[Utilizzare le azioni personalizzate](../action/about-custom-action-configuration.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/canvas.svg)

**Progettazione percorso visivo**

Con il **designer del percorso**, genera casi d’uso in più passaggi: trascina facilmente un evento di ingresso o un’attività Leggi pubblico, aggiungi delle condizioni e invia messaggi personalizzati.

[Esplora il designer del percorso](using-the-journey-designer.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/test.svg)

**Verifica e ottimizza**

Esegui il test dei percorsi prima di pubblicarli, monitorane le prestazioni e ottimizza la distribuzione con funzioni avanzate come l’ottimizzazione del tempo di invio.

[Test e pubblicazione dei percorsi](testing-the-journey.md)
:::

::::

>[!TAB Casi d&#39;uso]

## Esempi di percorsi reali

Dal designer del percorso, i marketer possono inviare messaggi 1:1 in tempo reale attivati tramite qualsiasi canale quando si verifica un evento. Ad esempio, quando una persona si iscrive a un servizio, può [essere attivata un’e-mail di benvenuto](message-to-subscribers-uc.md), invitandola ad accedere all’app per la prima volta e a impostare le proprie preferenze. Azioni quali il completamento dell’acquisto, l’apertura dell’e-mail e l’accesso all’app possono essere utilizzate per far avanzare i nuovi clienti lungo i relativi percorsi.

### Casi d’uso comuni per i percorsi

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/email.svg)

**Nuovi abbonati**

Invia un percorso di benvenuto personalizzato quando i clienti si abbonano al servizio, guidandoli attraverso i passaggi di onboarding.

[Ulteriori informazioni](message-to-subscribers-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/calendar.svg)

**Ottimizza orari di invio e-mail**

Utilizza l’ottimizzazione del tempo di invio basata sull’intelligenza artificiale per inviare e-mail quando è più probabile che ogni cliente si rivolga a lui.

[Ulteriori informazioni](send-time-optimization.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/delivery.svg)

**Incrementa le consegne**

Aumenta gradualmente il volume dei messaggi per migliorare la reputazione del mittente ed evitare problemi di recapito dei messaggi.

[Ulteriori informazioni](ramp-up-deliveries-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/targeting.svg)

**Destinazione per giorno feriale**

Invia contenuti diversi in base al giorno della settimana in cui i clienti entrano nel percorso.

[Ulteriori informazioni](weekday-email-uc.md)
:::

::::

### Altri casi d’uso

Il [designer del percorso](using-the-journey-designer.md) fornisce [azioni di canale incorporate](journeys-message.md) che supportano i messaggi in uscita, ad esempio e-mail, notifiche push e SMS/MMS, nonché i canali in entrata, inclusi siti web, app per dispositivi mobili ed esperienze basate su codice create direttamente in Journey Optimizer. È inoltre possibile utilizzare sistemi di terze parti per l&#39;invio di messaggi. Journey Optimizer include [azioni personalizzate](using-custom-actions.md) per consentire l&#39;integrazione di tali sistemi nei percorsi direttamente dal progettista del percorso.

**Esplora tutti i casi d&#39;uso del percorso** in [questa pagina](jo-use-cases.md) per scoprire scenari end-to-end da implementare.

>[!NOTE]
>
>I guardrail e le limitazioni applicabili ai percorsi sono descritti in [questa pagina](../start/guardrails.md).

>[!TAB Risorse di apprendimento]

## Creazione percorso principale

### Tutorial video {#video}

Scopri i componenti di un percorso e le nozioni di base sulla creazione di un percorso nell’area di lavoro.

>[!VIDEO](https://video.tv.adobe.com/v/3424996?quality=12)

### Esplora per argomento

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg)

**Crea e gestisci percorsi**

Indicazioni dettagliate sulla progettazione, il test, la pubblicazione e il tracciamento dei percorsi cliente per creare campagne omnicanale personalizzate.

[Esplora creazione percorso](/help/rp_landing_pages/create-journey-landing-page.md) | [Informazioni sulla gestione dei percorsi](/help/rp_landing_pages/manage-journey-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg)

**attività Percorso**

Scopri come configurare e utilizzare attività come trigger, passaggi decisionali, gestione del pubblico e messaggistica personalizzata nei percorsi.

[Esplora le attività](/help/rp_landing_pages/about-journey-building-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

**Espressioni e condizioni**

Diventa esperto nella creazione di espressioni principali per flussi di lavoro dinamici, nella manipolazione di dati e nell’orchestrazione dei percorsi avanzata tramite potenti strumenti e sintassi.

[Informazioni sulle espressioni](/help/rp_landing_pages/building-advanced-conditions-journeys-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/monitor.svg)

**Risoluzione dei problemi e monitoraggio**

Diagnosticare e risolvere i problemi di esecuzione del percorso con strumenti, codici di errore e best practice per il debug e l&#39;ottimizzazione.

[Guida alla risoluzione dei problemi](/help/rp_landing_pages/troubleshoot-journey-landing-page.md)
:::

::::

### Risorse aggiuntive

* **[Domande frequenti sui percorsi](journey-faq.md)**: domande frequenti sui percorsi
* **[Riferimento ai codici di errore](error-codes-reference.md)**: codici di errore del percorso e passaggi per la risoluzione dei problemi
* **[Avvisi](../reports/alerts.md)**: imposta gli avvisi per il monitoraggio del percorso
* **[Risoluzione dei problemi](troubleshooting.md)**: problemi e soluzioni comuni del percorso
* **[Esercitazioni Percorso](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/journeys/journey-designer-overview){target="_blank"}** - Scopri la creazione di percorsi tramite esercitazioni video pratiche

>[!ENDTABS]

