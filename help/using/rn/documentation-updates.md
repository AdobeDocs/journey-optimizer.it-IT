---
solution: Journey Optimizer
product: journey optimizer
title: Aggiornamenti alla documentazione
description: Scopri gli ultimi aggiornamenti della documentazione
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 83c8f206-bce3-4cc8-94a3-575ec1d999bc
source-git-commit: bbea90bd21bd19941e8c8df93c8ec7a8a2769d77
workflow-type: tm+mt
source-wordcount: '2457'
ht-degree: 95%

---

# Aggiornamenti alla documentazione {#latest-updates}

Questa pagina elenca tutti gli ultimi aggiornamenti alla documentazione di [!DNL Journey Optimizer].

## Ottobre 2025 {#october-2025}

* È stata aggiunta una nota nella sezione dell’attività Condizione del percorso per documentare che la valutazione della condizione non riuscirà per i profili contenenti più di due identità multi-dispositivo. [Ulteriori informazioni](../building-journeys/condition-activity.md)

* È stata aggiunta una nuova pagina che descrive come utilizzare i criteri di consenso per rispettare le preferenze dei clienti in base alle loro scelte, rispettando al contempo il consenso. [Ulteriori informazioni](../action/preference-center.md)

* È stata aggiunta una nota alle pagine Introduzione a profili e Guardrail per specificare che, durante l’acquisizione dei dati, le e-mail distinguono tra maiuscole e minuscole, il che significa che è possibile creare e utilizzare profili duplicati per il targeting del destinatario corrispondente. [Ulteriori informazioni](../audience/get-started-profiles.md)

* Nell’editor di personalizzazione, è stato introdotto un nuovo attributo `render`. Impostalo su `false` nei casi in cui desideri nascondere il contenuto di un frammento di espressione. [Ulteriori informazioni](../personalization/use-expression-fragments.md#use-expression-fragment)

* Alla sezione è stato aggiunto un elenco di guardrail che descrive come sfruttare i frammenti allegati agli elementi decisionali all’interno dei criteri di decisione. [Ulteriori informazioni](../experience-decisioning/create-decision.md#fragments-guardrails)

* Sono state aggiunte le best practice per le ricerche di set di dati: mantieni le opzioni attive per evitare problemi di indicizzazione e capire in che modo le eliminazioni in batch influiscono sui dati di ricerca. [Ulteriori informazioni](../data/lookup-aep-data.md#guardrails--guidelines-guidelines)

* È stata aggiunta una limitazione che specifica che durante l’utilizzo di percorsi Leggi pubblico con identificatori supplementari, vengono supportati solo i tipi di pubblico del servizio Profilo unificato. [Ulteriori informazioni](../building-journeys/supplemental-identifier.md#guardrails--limitations-guardrails)

* La documentazione di Experimentation Accelerator è stata trasferita in una raccolta separata. [Ulteriori informazioni](https://experienceleague.adobe.com/en/docs/experimentation-accelerator/using/overview)

## Settembre 2025 {#september-2025}

* Alla pagina Guardrail e limitazioni è stata aggiunta una nuova sezione Canale in entrata per raccogliere tutte le limitazioni applicabili ai canali web, in-app, esperienze basate su codice e schede di contenuto. Include il limite massimo di volume di 5.000 richieste in entrata al secondo per tutte le richieste in entrata e il massimo di 500 azioni in entrata attive. [Ulteriori informazioni](../start/guardrails.md#inbound-guardrails)

* Per le campagne orchestrate è stata pubblicata la pagina delle Domande frequenti. [Ulteriori informazioni](../orchestrated/orchestrated-campaigns-faq.md)

* Alla documentazione degli eventi Passaggio del percorso è stata aggiunta una sezione sulla risoluzione dei problemi con definizioni, cause comuni e passaggi di risoluzione dei problemi per i tipi di evento di eliminazione più frequenti. [Ulteriori informazioni](../reports/sharing-field-list.md#troubleshoot-discarded-event-types-in-journey_step_events)

* La documentazione su come utilizzare gli identificatori supplementari nei percorsi ora include una tabella che descrive il comportamento dei profili quando i criteri di uscita vengono applicati nei percorsi utilizzando ID supplementari. [Ulteriori informazioni](../building-journeys/supplemental-identifier.md#exit-criteria)

* È stata aggiunta una sezione per la risoluzione dei problemi relativa alle eliminazioni dei profili nei percorsi in pausa. [Ulteriori informazioni](../building-journeys/journey-pause.md#troubleshoot-profile-discards-in-paused-journeys)

* Nella documentazione della panoramica sugli schemi sono state aggiunte informazioni per differenziare gli schemi standard e relazionali utilizzati per le campagne orchestrate. [Ulteriori informazioni](../data/gs-data.md)

* Nella documentazione relativa alla funzione e alla gestione delle decisioni sono state aggiunte informazioni sui requisiti per addestrare correttamente modelli di ottimizzazione [automatica](../experience-decisioning/ranking/auto-optimization-model.md) e [personalizzata](../experience-decisioning/ranking/personalized-optimization-model.md).

* È stato chiarito che le chiamate API REST per l’esecuzione di messaggi interattivi hanno un timeout di 60 secondi, con nuovi tentativi interni per garantire la consegna. [Ulteriori informazioni](../campaigns/trigger-campaigns.md)

* La pagina Raccolte elementi della funzione Decisioni è stata aggiornata per chiarire il comportamento dell’operatore **CONTAINS** durante la definizione delle regole. [Ulteriori informazioni](../experience-decisioning/collections.md)

* La pagina Assegna punteggi di priorità è stata aggiornata con i passaggi specifici per definire un punteggio di priorità per le azioni del canale in entrata nell’attività **Azione**. [Ulteriori informazioni](../conflict-prioritization/priority-scores.md#priority-action)

## Agosto 2025 {#august-2025}

* È stata aggiunta una nuova pagina che elenca le best practice per la progettazione di contenuti accessibili per e-mail e pagine di destinazione con [!DNL Journey Optimizer]. [Ulteriori informazioni](../email/accessible-content.md)

* La documentazione relativa agli identificatori supplementari nei percorsi è stata aggiornata con i seguenti chiarimenti:

   * Dopo l’aggiunta di un identificatore supplementare a uno schema, è necessario creare un nuovo evento (per percorsi attivati da eventi) o un nuovo gruppo di campi (per percorsi Leggi pubblico). Le entità esistenti non vengono aggiornate automaticamente e non riconosceranno il nuovo identificatore.

   * Gli identificatori supplementari non vengono convalidati in base ai criteri del framework di governance per l’etichettatura e l’applicazione dell’utilizzo di dati (DULE) e non vengono considerati durante i controlli di governance dei dati nei percorsi.

[Maggiori informazioni](../building-journeys/supplemental-identifier.md)

* La pagina Ottimizzazione nelle campagne è stata aggiornata per riflettere il fatto che l’ottimizzazione è ora disponibile anche nei percorsi. [Ulteriori informazioni](../campaigns/campaigns-message-optimization.md)

* È stato aggiunto un collegamento al video tutorial che descrive come sfruttare l’ottimizzazione dei messaggi in una campagna. [Ulteriori informazioni](../campaigns/campaigns-message-optimization.md)

## luglio 2025 {#july-2025}

* L’interfaccia delle campagne ora dispone di due schede separate: **Azione** e **Attivate da API**. La documentazione è stata aggiornata di conseguenza, con informazioni per ogni tipo di campagna organizzate in sezioni dedicate per migliorarne la chiarezza e la fruibilità. [Ulteriori informazioni](../campaigns/get-started-with-campaigns.md)

* Le pagine [Introduzione alla delega del sottodominio](../configuration/about-subdomain-delegation.md) e [Delegare un sottodominio](../configuration/delegate-subdomain.md) sono state aggiornate per presentare meglio i diversi metodi di delega e i passaggi per configurarli.

* È stata aggiunta una nota alla sezione Frammenti che specifica che, quando il tracciamento è abilitato in un percorso o in una campagna, se i collegamenti sono presenti in un frammento e quest’ultimo viene utilizzato in un messaggio, tali collegamenti vengono tracciati come tutti gli altri collegamenti inclusi nel messaggio. [Ulteriori informazioni](../content-management/create-fragments.md#content)

* I guardrail e le limitazioni applicabili alla delega di un sottodominio in Journey Optimizer sono stati arricchiti e consolidati in una sezione dedicata. [Ulteriori informazioni](../configuration/delegate-subdomain.md#guardrails)

* È stata aggiunta una nota alle pagine Creare offerte di fallback e Creare decisioni per indicare che le offerte di fallback devono contenere tutte le rappresentazioni utilizzate all’interno di una decisione. [Ulteriori informazioni](../offers/offer-library/creating-fallback-offers.md)

* I guardrail applicati ai frammenti sono stati arricchiti. [Ulteriori informazioni](../start/guardrails.md#fragments-guardrails).

* È stata aggiunta una nota per specificare che i collegamenti aggiunti ai messaggi scadono dopo 25 mesi e i collegamenti alle pagine mirror dopo 90 giorni. [Ulteriori informazioni](../email/message-tracking.md)

<!--* The possible email error types that could happen upon sending email deliveries with are now listed in a dedicated section. [Read more](../configuration/email-error-types.md)-->

## Giugno 2025 {#june-2025}

* È stata aggiunta una nuova sezione su come aggiungere e utilizzare il testo formattato, ad esempio interruzioni di riga, grassetto, corsivo e così via, nei frammenti personalizzabili utilizzando i componenti di HTML. [Ulteriori informazioni](../content-management/customizable-fragments.md#rich-text)

* La parte sulla funzione Decisioni è stata aggiornata con una sezione specifica dedicata alla creazione di modelli di IA. [Ulteriori informazioni](../experience-decisioning/ranking/ai-models.md)

* È stato aggiunto un consiglio sull’utilizzo del campo `actionExecutionTime` nell’azione eventi journeyStep. [Ulteriori informazioni](../reports/sharing-execution-fields.md#actionexecutiontime-actionexecutiontime-field)

* È stata aggiunta una nota su `messageID` che potrebbe non essere univoca per ogni singola consegna. [Ulteriori informazioni](../data/datasets-query-examples.md)

* È stato aggiunto un consiglio sulla gestione degli eventi storici nelle operazioni di igiene dei dati. [Ulteriori informazioni](../privacy/data-hygiene.md#recommendations-data-hygiene-recommendations)

* È stato aggiunto un guardrail relativo al mancato supporto delle pagine di destinazione per la migrazione tra sandbox. [Ulteriori informazioni](../configuration/copy-objects-to-sandbox.md#general-best-practices-global)

* È stata aggiunta una nota di attenzione relativa agli oggetti JSON nidificati non supportati nell’autenticazione personalizzata per le azioni personalizzate. [Ulteriori informazioni](../datasource/external-data-sources.md)

* È stata aggiunta una nota di attenzione sulla denominazione delle varianti di contenuto condizionale in E-mail designer. [Ulteriori informazioni](../personalization/create-conditions.md)

* È stata aggiornata la sezione “Annullare la delega di un sottodominio di una pagina di destinazione”. [Ulteriori informazioni](../landing-pages/lp-subdomains.md#undelegate-subdomain)

* Sono state chiarite le regole di reingresso nel percorso quando si utilizzano identificatori supplementari. [Ulteriori informazioni](../building-journeys/supplemental-identifier.md#guardrails--limitations)

* È stata aggiunta una nuova nota per chiarire che è necessario utilizzare l’editor di espressioni in modalità avanzata quando si seleziona l’attributo dell’identificatore supplementare durante la configurazione dell’evento. [Ulteriori informazioni](../building-journeys/supplemental-identifier.md#add)

* Sono stati aggiunti chiarimenti sul funzionamento del reingresso nel percorso con identificatori supplementari. [Ulteriori informazioni](../building-journeys/supplemental-identifier.md#guardrails)

## Maggio 2025 {#may-2025}

* Le integrazioni Adobe disponibili con Journey Optimizer sono ora elencate nella sezione “Collegare i sistemi e gli ambienti”. [Ulteriori informazioni](../integrations/ajo-integrations.md)

* Le integrazioni relative ai contenuti sono ora raggruppate nella sezione Gestione dei contenuti. [Ulteriori informazioni](../integrations/content-integrations.md)

* I diagrammi dell’architettura per Adobe Experience Platform e Journey Optimizer sono stati aggiornati. [Ulteriori informazioni](../start/get-started.md#architecture-architecture)

* È stato aggiunto un video sul playgroung dell’editor di personalizzazione per aiutarti a scoprire come scrivere e testare il codice di personalizzazione utilizzando dati di esempio. [Ulteriori informazioni](../personalization/personalize.md#how-to-videosvideo-perso)

* Il numero massimo di indirizzi consentito in un elenco di seed è stato aumentato da 50 a 300. [Ulteriori informazioni](../configuration/seed-lists.md#create-seed-list)

* Nella pagina Creare criteri di decisione è stato aggiunto un nuovo passaggio che descrive come eseguire il wrapping del codice quando si utilizzano i criteri di decisione nell’editor di esperienze basate su codice. [Ulteriori informazioni](../experience-decisioning/create-decision.md#use-decision-policy)

* È stata aggiunta una nota alla documentazione delle esperienze basate su codice per specificare che, quando più azioni di esperienza basate su codice vengono eseguite sulla stessa superficie, il punteggio di priorità della campagna o del percorso determina ciò che viene consegnato agli utenti finali che risultano idonei per più azioni. [Ulteriori informazioni](../code-based/code-based-surface.md#surface-definition)

* È stata aggiunta una pagina sulla risoluzione dei problemi relativi alle azioni in entrata nei percorsi, con una guida dettagliata su come identificare e risolvere i problemi in autonomia prima di contattare l’assistenza supporto tecnica. [Ulteriori informazioni](../building-journeys/troubleshooting-inbound.md)

* È stata aggiunta una nuova [pagina](../code-based/code-based-decisioning-implementations.md) che descrive come aggiungere i seguenti flag all’implementazione client quando si utilizzano decisioni nelle esperienze basate su codice:

   * Aggiunta del flag `dryRun` per testare le decisioni nelle esperienze basate su codice. [Ulteriori informazioni](../code-based/code-based-decisioning-implementations.md#code-based-test-decisions)

   * Applica la deduplica alle richieste di decisioning nelle esperienze basate su codice. [Ulteriori informazioni](../code-based/code-based-decisioning-implementations.md#code-based-decisioning-deduplication)

## Aprile 2025 {#apr-2025}

* Il capitolo Configurazione è ora suddiviso in tre capitoli: [Configurazione dei canali](../configuration/get-started-configuration.md), [Configurazione percorso](../configuration/about-data-sources-events-actions.md) e [Collegamento dei sistemi](../configuration/ajo-apis.md).
* È stata aggiunta una nota di avviso sull’utilizzo degli eventi di esperienza nelle espressioni e nelle condizioni del percorso. [Ulteriori informazioni](../building-journeys/expression/expressionadvanced.md#discovering-the-interface)
* È stata aggiunta una nota sulla pagina di configurazione di direct mail relativa all’archiviazione temporanea del file di output. [Ulteriori informazioni](../direct-mail/direct-mail-configuration.md)
* Nella sezione dell’editor di espressioni avanzato del percorso è stato aggiunto un suggerimento sulle linee guida per il formato della condizione. [Ulteriori informazioni](../building-journeys/expression/expressionadvanced.md)
* È stata aggiunta una nota di avviso nella sezione della funzione `inAudience` relativa agli impatti e alle best practice per la ridenominazione di un pubblico. [Ulteriori informazioni](../building-journeys/functions/functioninaudience.md)
* È stata aggiunto un consiglio relativo alle parole chiave native durante l’utilizzo degli SMS bidirezionali. [Ulteriori informazioni](../sms/sms-opt-out.md)
* È stata aggiornata la pagina del test di percorso con una nota sulla necessità di includere uno spazio dei nomi identità nell’evento utilizzato. [Ulteriori informazioni](../building-journeys/testing-the-journey.md)
* Al momento non è possibile annullare la delega dei sottodomini tramite l’interfaccia utente di [!UICONTROL Journey Optimizer]. È necessario contattare il rappresentante Adobe. I passaggi per annullare la delega di un sottodominio sono ora descritti in modo dettagliato per [e-mail](../configuration/delegate-subdomain.md#undelegate-subdomain), [SMS](../sms/sms-subdomains.md#undelegate-a-subdomain-undelegate-subdomain), [esperienze web](../web/web-delegated-subdomains.md#undelegate-a-subdomain-undelegate-subdomain) e [pagine di destinazione](../landing-pages/lp-subdomains.md#undelegate-subdomain).<!--[Read more](../configuration/delegate-subdomain.md#undelegate-subdomain)-->
* Sono stati aggiunti chiarimenti sul parametro opzionale `maxHttpConnections` nell’API di limitazione dei percorsi, incluse indicazioni su come utilizzarlo insieme alle configurazioni del limite per lo stesso endpoint. [Ulteriori informazioni](../configuration/throttling.md)
* Nella sezione Decisioni per le esperienze sono state aggiunte indicazioni che spiegano che gli elementi di offerta approvati non possono essere eliminati se vengono utilizzati in una raccolta o in una decisione. Sono stati inclusi i passaggi per cambiarne lo stato in “Bozza” utilizzando l’opzione **[!UICONTROL Annulla approvazione]**. [Ulteriori informazioni](../experience-decisioning/items.md#manage)
* Le informazioni sulle sandbox sono state raggruppate nella nuova sezione “Gestione delle sandbox”. Questa nuova sezione fornisce informazioni su come utilizzare e assegnare le sandbox e su come usare le funzionalità di esportazione e importazione dei pacchetti per copiare oggetti quali percorsi, modelli di contenuto o frammenti in più sandbox. [Ulteriori informazioni](../administration/sandboxes.md)

## Marzo 2025 {#mar-2025}

* La pagina relativa agli eventi di qualificazione del pubblico è stata aggiornata con nuovi consigli. [Ulteriori informazioni](../building-journeys/audience-qualification-events.md)
* La funzionalità di risoluzione dei problemi delle azioni personalizzate è ora disponibile per tutta la clientela (GA). [Ulteriori informazioni](../action/troubleshoot-custom-action.md)
* Igiene dei dati è ora Ciclo di vita dei dati nell’interfaccia utente del prodotto. La documentazione è stata aggiornata per riflettere questa modifica. [Ulteriori informazioni](../privacy/data-hygiene.md)
* Le autorizzazioni incorporate mancanti per la pagina di destinazione sono state aggiunte alla documentazione. [Ulteriori informazioni](../administration/ootb-permissions.md)
* È stata aggiunta una nota sulla pianificazione di campagne ricorrenti. [Ulteriori informazioni](../campaigns/create-campaign.md)
* La sezione sull’inserimento di collegamenti e sull’abilitazione del tracciamento in un messaggio e-mail è stata aggiornata e riorganizzata. [Ulteriori informazioni](../email/message-tracking.md)
* La sezione sulle funzionalità di personalizzazione in Adobe Journey Optimizer è stata riorganizzata e migliorata. [Ulteriori informazioni](../personalization/personalize.md)
* L’API di gestione delle decisioni per elencare le offerte personalizzate è stata aggiornata con un esempio per eseguire l’impaginazione nel caso in cui manchino più offerte personalizzate nella risposta. [Ulteriori informazioni](../offers/api-reference/offers-api/personalized-offers/offers-list.md)
* Per maggiore chiarezza, è stata creata una nuova pagina che raccoglie tutte le informazioni relative alla funzione di annullamento dell’iscrizione alla mailing list. [Ulteriori informazioni](../email/list-unsubscribe.md)
* La sezione Quota limite è stata aggiornata con informazioni su come viene aggiornato il contatore della quota limite per le API Decisioning e Batch Decisioning, oltre all’API Edge Decisioning. [Ulteriori informazioni](../offers/offer-library/add-constraints.md#frequency-capping)

## Febbraio 2025 {#feb-2025}

* I guardrail dell’attività Leggi pubblico sono stati aggiornati per specificare che solo un’attività può essere utilizzata in un percorso e che può essere indirizzata a un solo pubblico. [Ulteriori informazioni](../building-journeys/read-audience.md)
* Sono stati aggiornati i guardrail di percorso relativi all’utilizzo delle attività di Adobe Campaign. [Ulteriori informazioni](../start/guardrails.md#ac-g)
* Sono stati descritti i passaggi per creare i primi percorsi e sono stati aggiunti i collegamenti alla relativa sezione della documentazione. [Ulteriori informazioni](../building-journeys/journey-gs.md)
* Una nuova pagina descrive nel dettaglio la dashboard del percorso e l’interfaccia utente per il filtraggio. [Ulteriori informazioni](../building-journeys/journey-ui.md)
* La documentazione relativa all’**[!UICONTROL ottimizzazione dell’ora di invio]** e le relative domande frequenti sono state aggiornate, migliorate e spostate in una nuova pagina dedicata. [Ulteriori informazioni](../building-journeys/send-time-optimization.md)
* Sono stati aggiunti nuovi guardrail per gli eventi di percorso. [Ulteriori informazioni](../start/guardrails.md#events-g)
* La pagina delle azioni del canale incorporate è stata riorganizzata. [Ulteriori informazioni](../building-journeys/journeys-message.md)
* Sono stati aggiunti guardrail e limitazioni nelle sezioni Funzione Decisioni e Gestione delle decisioni.
   * [Guardrail e limitazioni per la funzione Decisioni](../experience-decisioning/decisioning-guardrails.md)
   * [Guardrail e limitazioni per la gestione delle decisioni](../offers/decision-management-guardrails.md)
* Nella documentazione relativa alla gestione delle decisioni è stata aggiunta una nuova sezione sui dati contestuali. Fornisce informazioni su come sfruttare i dati contestuali nel motore decisionale, ad esempio per progettare una regola di decisione che richiede che la temperatura corrente sia di ≥26 °C al momento della richiesta di decisione. [Ulteriori informazioni](../offers/context-data.md)

## Gennaio 2025 {#jan-2025}

* È stata aggiunta una nuova sezione nell’opzione **[!UICONTROL Indirizzo di esecuzione]** nella configurazione e-mail. L’indirizzo principale è definito a livello di sandbox, ma l’impostazione predefinita può essere sovrascritta per una configurazione e-mail specifica. [Ulteriori informazioni](../email/email-settings.md#execution-address)

* La pagina **Introduzione alla recapitabilità** è stata aggiornata con la possibilità di creare flussi di lavoro di preparazione IP direttamente dall’interfaccia utente. [Ulteriori informazioni](../reports/deliverability.md#reputation)

* La sezione **Parametri intestazione** è stata aggiornata per riflettere le nuove etichette e le modifiche nell’interfaccia utente. [Ulteriori informazioni](../email/email-settings.md#email-header)

* La sezione **Inoltra e-mail** è stata aggiornata per specificare che tutte le e-mail inviate all’indirizzo **Da e-mail** vengano inoltrate all’indirizzo e-mail di inoltro. Se non specifichi alcuna e-mail di inoltro, queste e-mail verranno eliminate. [Ulteriori informazioni](../email/email-settings.md#forward-email)

* La dimensione massima degli attributi contestuali trasmessi in una richiesta di campagna attivata da API è stata aggiornata a 200 kb. [Ulteriori informazioni](../campaigns/api-triggered-campaigns.md#contextual)

* È stata aggiunta una nuova sezione alla pagina **Gestire i frammenti** per descrivere come aggiungere nuovi attributi a un frammento attivo. Inoltre, l’intera pagina è stata migliorata. [Ulteriori informazioni](../content-management/manage-fragments.md#adding-new-attributes)

* È stata aggiunta una sezione “Guardrail e limitazioni” alla documentazione relativa agli strumenti di gestione dei conflitti e delle priorità. [Ulteriori informazioni](../conflict-prioritization/gs-conflict-prioritization.md)

* È stato aggiunto un nuovo caso d&#39;uso end-to-end per presentare tutti i passaggi necessari all’utilizzo della funzione Decisioni negli esperimenti di contenuto con il canale di esperienza di [!DNL Journey Optimizer] basato su codice. [Ulteriori informazioni](../experience-decisioning/experience-decisioning-uc.md)

* La pagina **Configurare le impostazioni e-mail** è stata suddivisa in diverse sottopagine per migliorarne la leggibilità, comprese le nuove pagine specifiche dedicate a [Annullamento iscrizione a mailing list](../email/list-unsubscribe.md), [Parametri intestazione](../email/header-parameters.md) e [Tracciamento URL](../email/url-tracking.md).

## Dicembre 2024 {#nov-2024}

* È stata aggiunta una nota su come risolvere un potenziale messaggio di errore durante una chiamata API per abilitare i set di dati per la personalizzazione utilizzando i dati di Adobe Experience Platform. [Ulteriori informazioni](../personalization/aep-data-perso.md)

## Ottobre 2024 {#oct-2024}

* Tutte le nuove funzioni e i miglioramenti apportati alla versione di ottobre 2024 di [!DNL Journey Optimizer] sono elencati in dettaglio nella documentazione. [Ulteriori informazioni](release-notes.md)
* Tutti i canali di comunicazione disponibili in [!DNL Journey Optimizer] sono ora raggruppati in una sezione dedicata della documentazione. [Ulteriori informazioni](../channels/gs-channels.md)
* La pagina **Configura l’esperienza basata su codice** è stata migliorata per rendere più chiaro il processo, inclusa la sezione che spiega che cos’è un URI di superficie. [Ulteriori informazioni](../code-based/code-based-configuration.md)
* La pagina **Crea configurazione canale web** è stata aggiornata per chiarire i passaggi della creazione di una regola di corrispondenza delle pagine, che si applicano anche alla configurazione dell’esperienza basata su codice. [Ulteriori informazioni](../web/web-configuration.md#web-page-matching-rule)
* È stata aggiunta una nota sull’imminente guardrail time-to-live (TTL) per i set di dati generati dal sistema. [Ulteriori informazioni](../data/get-started-datasets.md)
* È stata aggiunta una nuova sezione che descrive come visualizzare in anteprima le esperienze personalizzate basate su codice direttamente sul browser o sui dispositivi mobili, utilizzando l’opzione **Anteprima sul dispositivo** durante la simulazione di contenuti in un percorso o in una campagna. [Ulteriori informazioni](../code-based/test-code-based.md#preview-on-device)
* È stata aggiunta una nuova pagina su come sfruttare i tipi di pubblico con caricamento personalizzato per la funzione Decisioni. [Ulteriori informazioni](../offers/custom-upload-decisioning.md)
* È stata aggiunta una nuova pagina per introdurre le funzionalità decisionali disponibili in Journey Optimizer. [Ulteriori informazioni](../experience-decisioning/gs-decision.md)
* Sono stati aggiunti guardrails e limitazioni alla documentazione della funzione Decisioni. [Ulteriori informazioni](../experience-decisioning/gs-experience-decisioning.md#guardrails)

## Settembre 2024 {#sept-2024}

* Tutte le nuove funzioni e i miglioramenti apportati alla versione di settembre 2024 di [!DNL Journey Optimizer] sono elencati in modo dettagliato nella documentazione. [Ulteriori informazioni](release-notes.md)
* È stata aggiunta una sezione sulla gestione dei nuovi tentativi per i percorsi. [Ulteriori informazioni](../building-journeys/read-audience.md#read-audience-retry)
* Le domande frequenti sulle regole di limitazione per le azioni personalizzate sono state aggiornate per menzionare la regola di limitazione predefinita. [Ulteriori informazioni](../configuration/external-systems.md#faq)
* La sezione Controllo degli accessi è stata aggiornata con le autorizzazioni relative alla generazione di contenuti dell’Assistente IA. [Ulteriori informazioni](../administration/high-low-permissions.md#ai-permission)
* È stato aggiunto un video relativo alla generazione di contenuti dell’Assistente IA per la creazione di e-mail. [Ulteriori informazioni](../content-management/generative-email.md#video)

<!--

## August 2024 {#aug-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] August '24 release have been detailed in the documentation. [Read more](release-notes.md)
* Performance guardrails for Decision Management have been updated to mention Decisioning APIs delivery throughputs with/without Edge Segmentation. [Read more](../start/guardrails.md#decision-management)
* Journey guardrails have been updated. [Read more](../start/guardrails.md#journeys-guardrails-journeys)


## July 2024 {#july-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] July '24 release have been detailed in the documentation. [Read more](release-notes.md)
* A personalization use case has been added on how to personalize an email with information related health plans and prescriptions. [Read more](../personalization/perso-uc-plan-prescriptions.md)

## June 2024 {#june-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] June '24 release have been detailed in the documentation. [Read more](release-notes.md)
* A note about the usage of merge policies in journeys has been added on [this page](../building-journeys/journey-properties.md#merge-policies).
* The page about how to configure a **Wait** activity in a journey has been reorganized and improved. [Read more](../building-journeys/wait-activity.md)
* A new page has been created to detail journey's properties. [Read more](../building-journeys/journey-properties.md)

## May 2024 {#may-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] May '24 release have been detailed in the documentation. [Read more](release-notes.md)
* The section on seed lists has been updated regarding recurring journeys. [Read more](../configuration/seed-lists.md#use-seed-list)
* The setion on external data sources has been updated. [Read more](../datasource/external-data-sources.md#custom-authentication-access-token)
* The global journey timeout of 30 days has been added to the Guardrail and limitation page. [Read more](../start/guardrails.md#journeys-guardrails-journeys)
* The section on the Adobe Campaign v7/v8 integration has been updated with information on provisionning. [Read more](../action/acc-action.md#access)
* The expression editor used to personalize content has been renamed in the documentation to "personalization editor" to clearly differenciate it from the [Journey expression editor](../building-journeys/expression/expressionadvanced.md). [Read more](../personalization/personalization-build-expressions.md)

## April 2024 {#april-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] April '24 release have been detailed in the documentation. [Read more](release-notes.md#apr-2024)
* Configuration steps for In-app messaging have been detailed. [Read more](../in-app/inapp-configuration.md)
* Documentation for [Offer decisioning APIs](../offers/api-reference/offer-delivery-api/decisioning-api.md) and [Batch decisioning APIs](../offers/api-reference/offer-delivery-api/batch-decisioning-api.md) have been updated.
* Information has been added in the Decision Management documentation regarding edge and hub regions management when using frequency capping with the Edge Decisioning API. [Read more](../offers/offer-library/add-constraints.md#frequency-capping)
* Information has been added on identity creation with custom namespaces when working with API-triggered campaigns. [Read more](../campaigns/api-triggered-campaigns.md)
* Screeshots have been updated to reflect the improved Journey canvas.
* Naming constraints has been updated in the following page: [Configure a unitary event](../event/about-creating.md), [Configure a business event](../event/about-creating-business.md#gs-business-events), [Configure a custom action](../action/about-custom-action-configuration.md#configuration-steps), [External data sources](../datasource/external-data-sources.md)
* A note has been added on Send Time Optimization availability. [Read more](../building-journeys/send-time-optimization.md)
* A new technical use case has been added on how to create a custom action to send data to Experience Platform. [Read more](../building-journeys/custom-action-aep.md)

## March 2024 {#march-2024}
 
* A Frequently Asked Questions section has been added to address common questions regarding the use of audience composition and custom upload audiences in Journey Optimizer. [Read more](../audience/about-audiences.md#faq)
* All new features and improvements coming with [!DNL Journey Optimizer] March '24 release have been detailed in the documentation. [Read more](release-notes.md#mar-2024)
* The page on profile entrance management has been improved. [Read more](../building-journeys/entry-management.md)
* Troubleshooting information has been added to the Alerts page. [Read more](../reports/alerts.md#alert-troubleshooting)
* Information on the Wait activity has been added to the page on journey reports. [Read more](../reports/sharing-overview.md)
* For Journeys in test mode, following shortcuts have been disabled:
    * T: Shortcut to toggle the test mode on or off.
    * E: Shortcut used to trigger an event in an event-based journey.
    * P: Shortcut to trigger an event in an audience-based journey for which the Single profile at a time option is turned on.
    * L: Shortcut designated to display the test logs.
* The Message frequency rules page has been updated with a new subsection on daily frequency cap, which is available on demand in addition to weekly or monthly capping.
* The Work with consent policies page has been improved and updated with useful links to the Experience Platform documentation. [Read more](../action/consent.md)
* A new section has been added to reflect the fact that you can display HTML email content templates as thumbnails with the Grid view mode (Limited Availability). [Read more](../content-management/content-templates.md#template-thumbnails)
* A new section has been added to the Deliverability page to explain what feedback loops are and how to leverage them. [Read more](../reports/deliverability.md#feedback-loops)
* A note has been added to the Create personalized offers section to specify that the size of an offer including all its representations cannot exceed 300KB. [Read more](../offers/offer-library/creating-personalized-offers.md#create-offer)

## February 2024 {#feb-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] February '24 release have been detailed in the documentation. [Read more](release-notes.md#feb-2024)
* The Journey Optimizer + Workfront integration has been added to the integrations page. [Read more](../integrations/ajo-integrations.md)
* Information has been added on how to personalize offers' representations based on context data. [Read more](../offers/offer-library/add-representations.md#context-data)
* The guardrails page has ben updated with a note on custom actions which support JSON format only when using request or response payloads. [Read more](../start/guardrails.md#custom-actions-g)
* Additional information has been added about the basic authentication type in external datasources. [Read more](../datasource/external-data-sources.md)
* A note has been added to clearly differenciate the [Journey expression editor](../building-journeys/expression/expressionadvanced.md) from the [personalization editor](../personalization/functions/functions.md).
* The list of functions available in the advanced expression editor has been updated. [Read more](../building-journeys/expression/functions.md)
* The page on the Split function has been updated. [Read more](../building-journeys/functions/functioninaudience.md)
* Information has been added regarding the impact of the opt-in or opt-out of push notifications on In-app messages. [Read more](../in-app/create-in-app.md)
* The Message frequency rules page has been updated to reflect the Duration options available in the user interface (weekly or monthly).
* The Edit a PTR record section has been updated to clarify the fact that PTR records cannot be created manually and that you need to edit PTR records to assign them new subdomains. [Read more](../configuration/ptr-records.md#edit-ptr-record)

## January 2024 {#jan-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] January '24 release have been detailed in the documentation. [Read more](release-notes.md)
* A guardrail about the journey size has been added. [Read more](../start/guardrails.md#journeys-guardrails-journeys)
* Journey timeout management has been detailed [in the following section](../building-journeys/journey-properties.md#global_timeout).
* Journey Optimizer [documentation home](../../ajo-home.md) page has been redesigned.
* Recommendations about the Update Profiles activity have been added. [Read more](../building-journeys/update-profiles.md) 
* Information has been added regarding the behaviour of timeouts on event activities in journeys. When no event is received during the specified timeout period, individuals will continue the journey if no timeout path is defined. [Read more](../building-journeys/general-events.md#events-specific-time)
* In-app channel configuration prerequisites have been updated with a note about the usage of a custom Dataset preference merge policy. [Read more](../in-app/inapp-configuration.md)
* More details have been added about how to manipulate collections in a custom action response. [Read more](../action/action-response.md#exp-syntax).
* A link to the [Schema Dictionary for Adobe Journey Optimizer](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html) has been added to the home page.
* An outdated reference to the AJO Message resource has been removed from the list of resources available in the Audit Log. When an update is done on a message in a journey, a **Journey** log is created. [Read more](../privacy/audit-logs.md)
* Additional recommendations have been added about the usage of the **Read Audience** activity. [Read more](../building-journeys/read-audience.md#must-read)
* The Get started with Adobe Experience Platform audiences page has been improved with a list of audience generation methods. [Read more](../audience/about-audiences.md)
* Best practices have been added when choosing an endpoint to target using a custom action. [Read more](../action/about-custom-action-configuration.md)
* An note has been added to notify users that events cannot be fired from external systems using an API. [Read more](../building-journeys/testing-the-journey.md#important-notes)
* Information on the **currentActionField** function has been added to the list of [collection management functions](../building-journeys/expression/collection-management-functions.md). An expression sample leveraging the function has been added in the [Use API call reponses in custom actions](../action/action-response.md) page.
* Update custom authentication doc regarding cache duration. [Read more] (../datasource/external-data-sources.md)
* Support of `<listObject>` has been modified in multiple functions.
* Update the **duration** parameter in the `toString` function. [Read more](../building-journeys/functions/functiontostring.md)
* For some external data sources use-cases, usage of custom actions is recommended.
* Event field syntax has been updated. The following syntax is deprecated `@(my_event.myfield}` and replaced by `@event{my_event.myfield}`. [Read more](../building-journeys/expression/field-references.md)

+++ 2023

## November 2023 {#nov-2023}

* The guardrail that limits all custom actions has been changed from 150,000 calls over 30 seconds to 300,000 calls over one minute. In addition, the default capping no longer applies to each endpoint. It is now performed per host and per sandbox. For example, on a sandbox, if you have two endpoints with the same host (eg: `https://www.adobe.com/endpoint1` and `https://www.adobe.com/endpoint2`), the capping will apply for all endpoints under the adobe.com host. "endpoint1" and "endpoint2" will share the same capping configuration and having one endpoint reach the limit will have an impact on the other endpoint. [Read more](../action/about-custom-action-configuration.md)
* A new status for email campaigns has been added to the list of campaigns' statuses. [Read more](../campaigns/manage-campaigns.md#campaign-statuses-and-alerts-statuses)
* The Get started with Adobe Experience Platform audiences section has been updated to reflect the audience evaluation methods available and how to select them. [Read more](../audience/about-audiences.md#evaluation-method-in-journey-optimizer)
* A new subsection has been added to specify which events should be avoided when building your audience if you are using the streaming segmentation evaluation method. [Read more](../audience/about-audiences.md#streaming-segmentation-events-guardrails)

## October 2023 {#oct-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] October '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Added GIFs to illustrate some key capabilities, such as: [Content templates](../content-management/content-templates.md), [Fragments](../content-management/fragments.md), [Computed attributes](../audience/computed-attributes.md), [Direct mail](../direct-mail/get-started-direct-mail.md), [Tags](../start/search-filter-categorize.md#tags), [Decision management optimization models](../offers/ranking/personalized-optimization-model.md), [API-triggered campaigns](../campaigns/api-triggered-campaigns.md), and [Content experiment](../content-management/content-experiment.md).
* The Schema creation process has been updated to reflect latest updates in the user interface, coming with Adobe Experience Platform changes. [Read more](../audience/creating-test-profiles.md) 
* Decision Management guardrails have been added to the Guardrails and limitations page. [Read more](../start/guardrails.md#decision-management)
* The Header parameters section has been updated to reflect how out-of-office notifications and challenge responses are handled (they are received on the **[!UICONTROL Error email]**). [Read more](../email/email-settings.md#email-header)
* A new section on how to preview and test your content has been created. [Read more](../content-management/preview-test.md)
* The Implement single-page applications page has been moved to the Adobe Experience Paltform Web SDK documentation. [Read more](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/ajo/web-spa-implementation.html){target="_blank"}
* The Capping section has been updated to reflect the label changes relating to offer capping in the decision management interface. [Read more](../offers/offer-library/add-constraints.md#capping)
* The Add dynamic content into emails has been updated with details on how to delete a variant. [Read more](../personalization/dynamic-content.md#emails)
* The example for capping & throttling configurations has been updated. [Read more](../configuration/external-systems.md)
* The limitation regarding scalar arrays has been removed from the external data source section. [Read more](../datasource/external-data-sources.md)
* The multi-channel journey use case has been updated. [Read more](../building-journeys/journeys-uc.md)
* The Journey Optimizer documentation set has been updated to reflect the new Experience Platform schema creation process. 

## September 2023 {#september-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] September '23 release have been detailed in the documentation. [Read more](release-notes.md)
* A new page has been added with scaling best practices and real-time stitching guidance. [Read more](../start/best-practices.md)
* A Frequently-Asked-Questions section has been added for Send-Time Optimization. [Read more](../building-journeys/journeys-message.md#faq-send-time)
* A note has been added for the audience qualification activity. It may take up to 10 minutes to be active and listen to profiles entering or exiting the audience. [Read more](../building-journeys/audience-qualification-events.md#important-notes-segment-qualification)
* A list of limitations to be aware of when creating decision rules has been added to the decision management documentation. [Read more](../offers/offer-library/creating-decision-rules.md)
* Links to access control documentation have been updated. [Read more](../administration/permissions.md)
* In-app channel prerequisites have been updated with Adobe Experience Platform Data Collection details. [Read more](../in-app/inapp-configuration.md)
* Some expressions presented in ranking formula examples have been updated to avoid validation errors. [Read more](../offers/ranking/create-ranking-formulas.md#ranking-formula-examples)
* A warning has been added to the Define decision scopes section to specify that if AI model is used in an evaluation criteria group, all the evaluation criteria in that group must use the AI ranking method, with the same specific AI model. Moreover, only one evaluation criteria group can use AI model. [Read more](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

## August 2023 {#august-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] August '23 release have been detailed in the documentation. [Read more](release-notes.md)
* The note about **authentication cache management** in journey has been updated to detail that the token is not shared between different journeys. [Read more](../datasource/external-data-sources.md#custom-authentication-mode)
* The page about journey **entry management** has been updated to clarify behaviour. [Read more](../building-journeys/entry-management.md)
* Offer decisioning **export datasets** are now enabled by default. The note about the previous behavior has been removed.  [Read more](../offers/export-catalog/get-started-export.md)
* Various **campaign report metrics** have been renamed, in both Live and Global reports. [Read more](../reports/campaign-live-report.md)
* A new section has been added on content experiment prerequisites for the web channel. [Read more](../web/web-prerequisites.md#experiment-prerequisites)
* A warning has been added on the **Work with content templates** page to indicate that currently tracking is not supported when testing email content templates. To test tracking, you must use the content template in an email and send a proof. [Read more](../content-management/content-templates.md#test-template)
* Several warnings have been added in the **Create and publish landing pages** section to specify that you cannot access your landing page by simply copy-pasting into a web browser the URL defined when creating the page, even if published. Instead you can test it using the preview function. [Read more](../landing-pages/create-lp.md)
* A new section has been added on how to **manage consent** for the direct mail channel. [Read more](../direct-mail/test-send-direct-mail.md)

## July 2023 {#july-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] July '23 release have been detailed in the documentation. [Read more](release-notes.md)
* The wait activity documentation page has been improved with additional information and best practices related to the global timeout and reentrance usage. [Read more](../building-journeys/wait-activity.md)
* The page on entry management has been improved. [Read more](../building-journeys/entry-management.md)
* Additional information has been added about the throttling rate in the Read audience activity documentation. [Read more](../building-journeys/read-audience.md)
* Additional information has been added about retries. [Read more](../start/guardrails.md#general-actions-g)
* The **Implement personalization consent** section has been updated to describe how to manually enforce personalization consent in campaigns: you can use the segment rule builder to create an audience containing opt-out profiles or add a split activity to a composition workflow. [Read more](../privacy/opt-out.md#opt-out-expression-editor)

## June 2023 {#june-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] June '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Information has been added about the discard rate ratio in the Journeys overview screen. [Read more](../building-journeys/journey-gs.md#journey-access)
* A note has been added with the steps to follow if you modify your schema with new enumeration values after creating an event [Read more](../event/about-creating.md)
* A recommendation has been added to use journeyVersionID instead of journeyVersionName when querying journeys. [Read more](../reports/sharing-common-fields.md#journeyversionid-field)
* Additional examples on the evaluation criteria order have been added to the **Create decisions** section to illustrate cases where multiple criteria and multiple decision scopes are used. [Read more](../offers/offer-activities/create-offer-activities.md#evaluation-criteria-order)
* Decision Management documentation has been clarified with a note specifying that the use of Object Level Access Control is not available for dynamic collections. [Read more](../offers/offer-library/creating-collections.md)

## May 2023 {#may-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] May '23 release have been detailed in the documentation. [Read more](release-notes.md)
* A new page has been added to describe how to set up the subdomain that will be used to publish content coming from the Adobe Experience Manager Assets Essentials in your web experiences. [Read more](../web/web-delegated-subdomains.md)
* A new subsection has been added to explain how to add personalized tracking parameters to URLs in the Email Designer. [Read more](../email/message-tracking.md#url-tracking)
* A new section has been added to describe how to ensure that the choice of your customers who opt out from having their profile data used for personalization is honored. [Read more](../privacy/opt-out.md#opt-out-personalization)
* A note has been added about using special international characters in URLs included in email contents. [Read more](../email/message-tracking.md#insert-links)
* The permission needed to test and publish landing pages has been added. [Read more](../landing-pages/create-lp.md)
* A note has been added about the Adobe Experience Platform endpoints needed to have your custom events accounted for in Decision Management frequency capping. [Read more](../offers/data-collection/schema-requirement.md#track-custom-events)

## April 2023 {#apr-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] April '23 release have been detailed in the documentation. [Read more](release-notes.md)
* A note has been added to specify that built-in actions cannot be removed. [Read more](../start/guardrails.md#custom-actions-g)
* Information has been added on serviceEvents as well as a query example to check the details of a serviceEvent. [Read more](../reports/query-examples.md#common-queries) 
* A note has been added to specify that you cannot perform queries on time series. [Read more](../building-journeys/condition-activity.md)
* Adobe Experience Manager Assets Essentials and Adobe Stock have been added to the multi-solution integration page. [Read more](../integrations/ajo-integrations.md)
* The warning on multi-level email subdomains not being allowed has been removed as they are now supported. [Read more](../configuration/delegate-subdomain.md)
* A note has been added to specify that, if changes are made to an offer decision which is being used in a journey's message, you need to unpublish the journey and republish it. [Read more](../building-journeys/publishing-the-journey.md)
* Explanation on how to make sure events are correctly accounted for in the capping counter has been clarified in the decision management **Capping event** section. [Read more](../offers/offer-library/add-constraints.md#capping-event)
* A new section has been added to the **Change execution addresses** page. It specifies that it is possible to override the execution field set globally in the journey advanced parameters, but the email address override should only be used for specific use cases. Most of the time, the value defined as the primary address in the **Execution fields** is the one that should be used. [Read more](../configuration/primary-email-addresses.md#journey-parameters)
* The **URL tracking** section now provides the list and description of all contextual attributes that can be set for URL tracking in an email channel configuration. [Read more](../email/email-settings.md#url-tracking)

## March 2023 {#march-2023}

* The Journey Optimizer schema dictionary is now available. You will find the complete list of fields and attributes for each schema.  [Read more](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html)
* All new features and improvements coming with [!DNL Journey Optimizer] March '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Added a step to enable Adobe Analytics events in your journeys. [Read more](../event/about-analytics.md)
* A new section has been created in the Decision management guide on how to collect offer decisioning feedback in Adobe Experience Platform, including which offers are displayed and how users interact with them. [Read more](../offers/data-collection/data-collection.md)
* A new subsection has been added to the **Create decision** section to explain the difference between evaluating criteria in a sequential order or at the same time. [Read more](../offers/offer-activities/create-offer-activities.md#evaluation-criteria-order)
* A guardrail has been added for read audience journeys with incremental read. You cannot create a new version, you need to duplicate the journey. [Read more](../start/guardrails.md#journey-versions-g)
* The use case on how to limit throughput put has been updated with information on throttling capabilities. [Read more](../building-journeys/limit-throughput.md)
* A note has been added to specify that scalar arrays are not supported in response payload definition. [Read more](../datasource/external-data-sources.md)
* The section on profile cap conditions has been updated. [Read more](../building-journeys/condition-activity.md#profile_cap)

## February 2023 {#feb-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] Feb '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Information has been added about the canvas toolbar. [Read more](../building-journeys/using-the-journey-designer.md#gs-journey-design)
* Information has been added to state that internal Adobe addresses are not allowed in URLs and APIs. [Read more](../start/guardrails.md)
* A note has been added in the API-triggered campaigns documentation to specify that contextual attributes passed into the request cannot exceed 50kb. [Read more](../campaigns/api-triggered-campaigns.md#contextual)
* Information was added on how opt-out information is stored in the **Consent Service Dataset** after recipients are unsubscribed through a landing page. [Read more](../landing-pages/lp-use-cases.md#configure-opt-out)

## January 2023 {#jan-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] Jan '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Information has been added on custom authentication endpoints in the capping documentation. [Read more](../configuration/external-systems.md)
* A new custom authentication example has been added in the external datasources section. [Read more](../datasource/external-data-sources.md#custom-authentication-mode)
* A note has been added about Data Collection Core Service (DCCS) for event-triggered journeys. [Read more](../start/guardrails.md#events-g)
* A note on identity namespace retrieval has been added in the [Read audience](../building-journeys/read-audience.md), [Audience qualification](../building-journeys/audience-qualification-events.md) and [Event creation](../event/about-creating.md) sections.
* Accessibility features in [!DNL Journey Optimizer] are now grouped in a dedicated page. [Read more](../start/accessibility.md)
* The examples have been updated in the Operators section of the advanced expression editor documentation. [Read more](../building-journeys/expression/operators.md)
* A note has been added about the limitation on lookup with array of objects. [Read more](../event/experience-event-schema.md#relationships_limitations)
* Added a new page about data management in [!DNL Journey Optimizer]. [Read more](../data/gs-data.md)
* Added a table listing all codes that can be returned in the response when delivering offers using the Decisioning API. [Read more](../offers/api-reference/offer-delivery-api/decisioning-api.md)

+++

+++ 2022

## December 2022 {#december-2022}

* The Messages guide has been reorganized and split into dedicated guides for each channel:

    * [Email channel](../email/get-started-email.md)
    * [Push notification channel](../../rp_landing_pages/push-landing-page.md)
    * [SMS channel](../sms/get-started-sms.md)

* The Configuration guide has been reorganized for improved readability. [Read more](../configuration/get-started-configuration.md)

## November 2022 {#november-2022}

* Added a new page about Journey Optimizer integrations. [Read more](../integrations/ajo-integrations.md)
* Added a recommendation about the length of mirror pages URLs. [Read more](../email/message-tracking.md)
* A new subsection in the email settings configuration has been added on the reply to email address, including recommendations to ensure proper reply management. [Read more](../email/email-settings.md#reply-to-email)
* Added a section on how to modify the content of a message in a live journey. [Read more](../building-journeys/journeys-message.md#update-live-content)

## October 2022 {#october-2022}

* Added a journey use case on how to limit throughput using External Data Sources and Custom Actions. [Read more](../building-journeys/limit-throughput.md)
* The journey use case section has been reorganized into two categories: [Business use cases](../building-journeys/journeys-uc.md) and [Technical use cases](../building-journeys/collections.md).
* The **Entity Dataset** section has been updated with more details. [Read more](../data/datasets-query-examples.md#entity-dataset)
* The opt-out management and consent policies sections have been reorganized. [Read more](../privacy/opt-out.md)
* The section on advanced parameters in journey messages has been clarified and now specifies that email address override should only be used for specific use cases. Most of the time, the value defined as the primary address in the **Execution fields** is the one that should be used. 
* Added a note to the **Configure landing page subdomains** section to specify that capital letters are not allowed in landing page subdomains. [Read more](../landing-pages/lp-subdomains.md)

## September 2022 {#september-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] September '22 release have been detailed in the documentation. [Read more](release-notes.md)
* Added a best practice related to the use of wait activities in recurring read audience journeys. [Read more](../building-journeys/read-audience.md#configuring-segment-trigger-activity)
* Added new step event query examples as well as information on the difference between id, instanceid and profileid. [Read more](../reports/query-examples.md).
* Updated the pages related to the [toDateOnly](../building-journeys/functions/functiontodateonly.md) and [toString](../building-journeys/functions/functiontostring.md) functions.
* Added details on the time condition parameters. [Read more](../building-journeys/condition-activity.md#time_condition)
* Added information on built-in datasets. [Read more](../data/get-started-datasets.md#access-datasets)
* The Global report and Live report sections have been improved and reorganized. [Read more](../reports/report-gs-cja.md)
* A list of every reporting metric available in Adobe Journey Optimizer has been added.
[Read more](../reports/report-gs-cja.md#email-and-sms-metrics)
* The BCC email section has been moved to the new Support for archiving page. [Read more](../configuration/archiving-support.md)

## August 2022 {#august-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] August '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The Frequency rules section has been updated to reflect the new in-line messaging flow.
* A video showing how to configure subscriptions and create landing pages is now referenced in the Get started with landing pages section. [Read more](../landing-pages/get-started-lp.md#video)
* A limitation has been added for journeys using Read Audience activities. [Read more](../building-journeys/read-audience.md)
* The expression editor operators page has been improved. [Read more](../building-journeys/expression/operators.md)
* A section on how to schedule a campaign has been added. [Read more](../campaigns/create-campaign.md)
* General syntax rules section for expression editor has been updated to take into account the new rule regarding the backslash symbol escaping in literal functions. The existing published messages are not impacted by this change. Only the new or draft messages must be updated. [Read more](../personalization/personalization-syntax.md#general-rules)

## July 2022 {#july-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] July '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The **Set up channel configurations** section has been clarified and updated with links to the page describing how to configure the SMS channel. [Read more](../configuration/channel-surfaces.md#create-channel-surface)
* In the journey properties, the **Profile Time zone** option is now disabled by default. [Read more](../building-journeys/timezone-management.md#timezone-from-profiles)
* In the **Wait** activity, the **Fixed date** option is no longer available. [Read more](../building-journeys/wait-activity.md)
* Added more information on the **Incremental read** option in the **Read audience** activity. [Read more](../building-journeys/read-audience.md#configuring-segment-trigger-activity)
* Added recommendations on the **Profile cap** condition type. [Read more](../building-journeys/condition-activity.md#profile_cap)
* Added a limitation on business events. [Read more](../start/guardrails.md#events-g)

## June 2022 {#june-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] June '22 release have been detailed in the documentation. [Read more](release-notes.md)
* A new section about Privacy requests has been added to the documentation. [Read more](../privacy/requests.md)
* A new section about Audit logs on resources has been added to the documentation. [Read more](../privacy/audit-logs.md)
* A new section about how to add HTML or JSON content coming from Adobe Experience Cloud Asset library to an offer representation has been added to the documentation. [Read more](../offers/offer-library/add-representations.md#html-json)
* Added a new page on journey lifecyle. [Read more](../building-journeys/journey.md#journey-versions)
* Updated the Wait activity page. [Read more](../building-journeys/wait-activity.md)
* Added the list of Adobe Journey Optimizer datasets with query examples. [Read more](../data/datasets-query-examples.md)
* The Allowed list page has been moved to the Configuration section. [Read more](../configuration/allow-list.md)
* The Suppression list page has been updated to clarify some information, including the fact that all ASCII characters comprised between 32 and 126 are allowed in the reason for suppression field. [Read more](../configuration/manage-suppression-list.md)
* The link to guardrails and static limits for Decision management has been added. [Read more](../start/guardrails.md)
* Send-Time Optimization is now available for all customers. The beta mention has been removed. [Read more](../building-journeys/send-time-optimization.md)
* The Batch Decisioning API has been added to the list of available APIs to delivery personalized offers. [Read more](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)

## May 2022 {#may-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] May '22 release have been detailed in the documentation. [Read more](release-notes.md)
* New query examples related to [audience qualification](../reports/query-examples.md#segment-qualification-queries) and [events](../reports/query-examples.md#event-based-queries) have been added.
* The email design section now mentions new built-in templates available to start content with. Related screenshots have been updated. [Read more](../email/get-started-email-design.md)
* Links to key resources have been updated in Journey Optimizer documentation home page.
* Screenshots for landing page and subscription reporting have been updated. [Read more](../reports/live-report.md)
* A note has been added stating that the Delete method is not supported in custom actions. [Read more](../action/about-custom-action-configuration.md)
* Links to how-to videos have been updated.
* The [Email configuration](../configuration/about-subdomain-delegation.md), [Message presets](../configuration/channel-surfaces.md) and [Configure landing pages](../landing-pages/lp-subdomains.md) sections have been reorganized for improved readability.
* The URL tracking section has been updated and improved with examples. [Read more](../email/email-settings.md#url-tracking)
* A new subsection on setting up a forward email address has been added. Note that you cannot do it through the user interface. [Read more](../email/email-settings.md#forward-email)

## April 2022 {#april-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] April '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The **reactions** event documentation page has been updated. [Read more](../building-journeys/reaction-events.md)
* Videos for Decision Management capabilities have been updated to reflect Journey Optimizer user interface. [Read more](../offers/get-started/starting-offer-decisioning.md)
* The **Get Started with Datasets** section has been improved to detail how to access and create datasets. [Read more](../data/get-started-datasets.md)
* Links to help guides and product release notes have been added to the **Adobe Journey Optimizer Documentation** home page. [Read more](https://experienceleague.adobe.com/docs/journey-optimizer.html)
* The **Create message presets** section now specifies that you cannot proceed with preset creation while the selected IP pool is under edition (**[!UICONTROL Processing]** status) and has never been associated with the selected subdomain. [Read more](../configuration/channel-surfaces.md#subdomains-and-ip-pools)
* The message presets **URL tracking** section has been updated to reflect minor changes in the user interface. [Read more](../configuration/channel-surfaces.md#url-tracking)

## March 2022 {#march-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] March '22 release have been detailed in the documentation. [Read more](release-notes.md)
* A new page on getting started with AI models has been added to the **Offer decisioning** section, including a thorough description of the [auto-optimization model](../offers/ranking/auto-optimization-model.md), the algorithm it uses and more technical details. [Read more](../offers/ranking/ai-models.md)
* The test profile creation page has been moved to the  **Audience, profiles and identity** section. [Read more](../audience/creating-test-profiles.md)
* Added an example on how to add an expression as a default value in the expression editor. [Read more](../building-journeys/expression/field-references.md#default-value)
* The **Create personalized offers** section has been reorganized for improved readability. [Read more](../offers/offer-library/creating-personalized-offers.md)
* A new section has been added to describe the impacts that changing an offer's start and/or end dates may have on this offer's frequency capping. [Read more](../offers/offer-library/add-constraints.md#capping-change-date)
* The **Change the primary email addresses** section has been updated to reflect the user interface changes. [Read more](../configuration/primary-email-addresses.md)

## February 2022 {#feb-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] Feb '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The [replace](../building-journeys/functions/functionreplace.md#example_2) and [replaceAll](../building-journeys/functions/functionreplaceall.md#example) function documentation pages have been updated with additional information and examples regarding the target parameter.
* Best practices have been added to the [Operators](../building-journeys/expression/operators.md#important-notes) page.

## January 2022 {#january-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] Jan '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The **Offer decisioning AI rankings** section has been updated with a more detailed description of the auto-optimization model. [Read more](../offers/ranking/auto-optimization-model.md)
* A new section on the schema requirements needed to be able to send in event types when using an AI model has been added. [Read more](../offers/data-collection/schema-requirement.md)
* The section related to [!DNL Journey Optimizer] personalization capabilities has been reorganized for better readability. [Read more](../personalization/personalize.md)
* The **Create message presets** section has been divided into several sections for improved clarity. [Read more](../configuration/channel-surfaces.md#create-channel-surface)
* The **Opt-out management** section has been clarified and slightly reorganized. [Read more](../privacy/opt-out.md#opt-out-management)
* The **Insert links** section has been updated to reflect the recent user interface changes. [Read more](../email/message-tracking.md#insert-links)

+++

+++ 2021

## November 2021 {#november-2021}

* A full description of the **advanced expression editor** used in journeys is now available. [Read more](../building-journeys/expression/expressionadvanced.md)
* A new section about **CNAME subdomain delegation method** has been added. [Read more](../configuration/delegate-subdomain.md#cname-subdomain-setup)

## October 2021 {#october-2021}

* All new features and improvements coming with [!DNL Journey Optimizer] Oct '21 release have been detailed in the documentation. [Read more](release-notes.md)
* Added **Date time function** list. [Read more](../personalization/functions/dates.md)
* New **Get Started sections per user persona**. Take your own path to get to your goals faster! [Read more](../start/quick-start.md)
* New **Edit a message preset** section. [Read more](../configuration/channel-surfaces.md#edit-channel-surface)
* New **Edit a PTR record** section. [Read more](../configuration/ptr-records.md#edit-ptr-record)
* New **Deactivate a message preset** section. [Read more](../configuration/channel-surfaces.md#edit-channel-surface#deactivate-a-surface)
* New limitations added to the **Decision Management API developer guide** on offer constraints not supported with the mobile [!DNL Experience Edge] workflows. [Read more](../offers/api-reference/offers-api/personalized-offers/create.md#limitations)
* New **Create simulations** section. [Read more](../offers/offer-activities/simulation.md)
* Updated **Add decision scopes** section. [Read more](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)
* Updated **Define content for your representations** section, including a new [subsection](../offers/offer-library/creating-personalized-offers.md#custom-text) on how to define and personalize custom text. [Read more](../offers/offer-library/creating-personalized-offers.md#content)

## September 2021 {#september-2021}

* The following function pages have been updated: [sethours](../building-journeys/functions/functionsethours.md), [getListItem](../building-journeys/functions/functiongetlistitem.md), [inSegment](../building-journeys/functions/functioninaudience.md)

* The following functions have been added: [filter](../building-journeys/functions/functionfilter.md), [intersect](../building-journeys/functions/functionintersect.md), [toDateOnly](../building-journeys/functions/functiontodateonly.md)

* The dateOnly date type has been added in the expression editor documentation. [Read more](../building-journeys/expression/data-types.md)

* Added details on custom action cache duration. [Read more](../datasource/external-data-sources.md#custom-authentication-mode)

* Added information on custom action default ports. [Read more](../action/about-custom-action-configuration.md#url-configuration)

* Added information on multiple business event use cases. [Read more](../event/about-creating-business.md#multiple-business-events)

* Added commonly used examples to query Journey Step Events in Data Lake. [Read more](../reports/query-examples.md)

* Added a new **Limitations** page. [Read more](../start/guardrails.md)

* Improved the **Quick start** page with steps for different personas. [Read more](../start/quick-start.md)

* Now all the Decision Management features described in the dedicated section also apply to the Adobe Experience Platform users leveraging the Offer Decisioning application. [Read more](../offers/get-started/starting-offer-decisioning.md)

* Added a subsection to clarify the differences between using audiences versus decision rules when applying a constraint to restrict the selection of offers for a given placement. [Read more](../offers/offer-activities/create-offer-activities.md#segments-vs-decision-rules)

* Added specific ranking formula examples to illustrate some real-life use cases. [Read more](../offers/ranking/create-ranking-formulas.md#ranking-formula-examples)

* Added a subsection on how to edit IP pools. [Read more](../configuration/ip-pools.md#edit-ip-pool)

## August 2021 {#august-2021}

* All new features and improvements coming with [!DNL Journey Optimizer] August '21 release have been detailed in the documentation. [Read more](release-notes.md)
* Updated Decision management permissions. [Read more](../administration/ootb-product-profiles.md)
* Updated Email Designer screenshots with latest UI.
* Updated the configuration procedure for custom actions with dynamic URL paths and dynamic headers. [Read more](../action/about-custom-action-configuration.md#url-configuration)
* Added a section about accessibility features and shortcuts. [Read more](../start/user-interface.md#accessibility)
* Added a section about audience evaluation methods. [Read more](../audience/about-audiences.md#evaluation-method-in-journey-optimizer)
* Added notes to the Suppression list, Allowed list and Email global/live report sections to specify that profiles with Suppressed and Not allowed statuses are excluded from the Email report Sent metrics. [Read more](../reports/report-gs-cja.md)
* Added a new section to describe how to retrieve email addresses or domains that were excluded from a sending because they were not on the allowed list. [Read more](../configuration/allow-list.md#reporting)
* Updated the Enable the allow list section. [Learn more](../configuration/allow-list.md#enable-allow-list)
* Updated the Monitor message presets section with the possible preset creation failure reasons and details on such errors. [Read more](../configuration/channel-surfaces.md#monitor-channel-surfaces)
* Updated and renamed the Retry time period section to reflect the fact that you can now adjust the email retry setting in the message presets. [Read more](../configuration/retries.md#retry-duration)
* Updated the Delegate a subdomain section with more detailed information on the validation process performed by Adobe. [Read more](../configuration/delegate-subdomain.md#subdomain-validation)
* Added a section to describe how to manually add email addresses and domains to the suppression list. [Read more](../configuration/manage-suppression-list.md#add-addresses-and-domains)
* Updated the [Access the suppression list](../configuration/manage-suppression-list.md#access-suppression-list) section and [Retries](../configuration/retries.md) sections to reflect the new user interface.
* The new flow to add and configure representations when creating an offer has been documented. [Read more](../offers/offer-library/creating-personalized-offers.md#representations)

## July 2021 {#july-2021}

* All new features and improvements coming with [!DNL Journey Optimizer] July '21 release have been detailed in the documentation. [Read more](release-notes.md)
* Added direct links to Experience Platform services documentation in [!DNL Journey Optimizer] home page and table of contents
* New landing pages for Experience Platform services available in [!DNL Journey Optimizer] 
* Added links to [!DNL Journey Optimizer] product description in the home page
* Added tutorial videos in multiple pages
* Optimized home page imagery
* Moved, improved and renamed 'Message tracking' section to 'Add links and track messages'. [Read more](../email/message-tracking.md)
* Added a subsection on mirror pages. [Read more](../email/message-tracking.md#mirror-page)
* Renamed 'offer activities' as 'decisions' and 'decisions' as 'decision scopes' in documentation and screens. [Read more](../offers/get-started/starting-offer-decisioning.md)
* New use case: [personalize a message with helper functions](../personalization/personalization-use-case-helper-functions.md)
* Updated the Read audience documentation to reflect materialized segment impacts. [Read more](../building-journeys/read-audience.md)
* Updated the Journey limitations. [Read more](../start/guardrails.md)
* Updated the Configure offers selection in decisions section. [Read more](../offers/offer-activities/configure-offer-selection.md)
* Added a warning to mention that event-based offers are not currently supported. [Read more](../offers/offer-library/creating-personalized-offers.md#eligibility)
* Documented the Decision Management new **[!UICONTROL Overview]** tab. [Read more](../offers/get-started/user-interface.md#overview)
* Added new sections to describe the actions available from the offer and decision lists: [Offer list](../offers/offer-library/creating-personalized-offers.md#offer-list) and [Decision list](../offers/offer-activities/create-offer-activities.md#decision-list).

+++
-->
