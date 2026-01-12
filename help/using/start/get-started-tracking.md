---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione al tracciamento in Journey Optimizer
description: Scopri le funzionalità di monitoraggio disponibili in Journey Optimizer
feature: Monitoring
topic: Administration
role: User
level: Beginner
keywords: tracciamento, monitoraggio, analisi, reporting, recapito messaggi
source-git-commit: fec72c63d41a41adce5107082c50a68a7b8c0af2
workflow-type: tm+mt
source-wordcount: '1916'
ht-degree: 3%

---

# Introduzione al tracciamento in Journey Optimizer {#get-started-tracking}

Il tracciamento consente di misurare l’efficacia della campagna, ottimizzare le esperienze dei clienti e garantire che i messaggi raggiungano i destinatari desiderati. Journey Optimizer fornisce funzionalità di tracciamento complete che acquisiscono le interazioni dei clienti, le prestazioni di consegna e lo stato del sistema, consentendo di prendere decisioni basate sui dati nel rispetto della privacy e mantenendo la conformità.

La maggior parte del tracciamento viene configurata automaticamente durante la creazione di messaggi e percorsi. Per scenari avanzati, puoi impostare metriche personalizzate, configurare parametri URL e integrarli con piattaforme di analisi esterne. Accedi ai dati di tracciamento tramite rapporti incorporati o esportali per un’analisi più approfondita in Customer Journey Analytics.

>[!BEGINSHADEBOX]

Cosa puoi tracciare in Journey Optimizer:

📧 **Interazioni e-mail** - Aperture, clic e prestazioni del collegamento

🌐 **Comportamento Web** - Visualizzazioni pagina, clic e modelli di coinvolgimento

🛤️ **Prestazioni Percorso** - Metriche personalizzate, eventi passaggio e percorsi di conversione

📊 **Integrità del recapito messaggi** - Percentuali non recapitate, segnalazioni di posta indesiderata e reputazione mittente

⚙️ **Operazioni di sistema** - Avvisi, errori e prestazioni delle azioni personalizzate

>[!ENDSHADEBOX]

Per aiutarti a iniziare, esplora questi argomenti essenziali relativi al tracciamento e al monitoraggio:

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="../building-journeys/success-metrics.md">
    <img alt="Metriche" src="../assets/do-not-localize/success-metrics.jpeg">
    </a>
    <div>
    <a href="../building-journeys/success-metrics.md"><strong>Configurare le metriche di successo</strong></a>
    </div>
    <p>
    <em>Tieni traccia dei KPI personalizzati allineati agli obiettivi aziendali</em>
    <p>
  </td>
  <td>
    <a href="../reports/deliverability.md">
    <img alt="Recapitabilità" src="../assets/do-not-localize/deliverability.jpeg">
    </a>
    <div>
    <a href="../reports/deliverability.md"><strong>Monitorare il recapito messaggi</strong></a>
    </div>
    <p>
    <em>Assicurati che i tuoi messaggi raggiungano le caselle in entrata del cliente</em>
    <p>
  </td>
  <td>
    <a href="../reports/gs-reports.md">
    <img alt="Reporting" src="../assets/do-not-localize/reporting.jpeg">
    </a>
    <div>
    <a href="../reports/gs-reports.md"><strong>Esplora reporting</strong></a>
    </div>
    <p>
    <em>Accedi ai report live e cronologici per i tuoi percorsi e campagne</em>
    <p>
  </td>
</tr>
</table>

## Tracciare le interazioni dei clienti nei diversi canali {#tracking-by-channel}

Journey Optimizer fornisce funzionalità di tracciamento specifiche per il canale. Ecco come configurare e utilizzare il tracciamento per ogni canale.

+++Tracciamento e-mail

Il tracciamento e-mail viene attivato automaticamente quando crei un messaggio e-mail. Per impostazione predefinita, Journey Optimizer tiene traccia di aperture, clic e annullamenti di abbonamenti, senza alcuna configurazione aggiuntiva.

**Configurare le opzioni di tracciamento:**

* **Attiva/disattiva il tracciamento** - Controlla il tracciamento a livello di messaggio durante la progettazione dell&#39;e-mail. Puoi scegliere di tenere traccia di aperture, clic o entrambi. [Ulteriori informazioni](../email/message-tracking.md)

* **Configura i parametri di tracciamento URL** - Configura i parametri di tracciamento a livello di superficie per aggiungere automaticamente gli identificatori della campagna (utm_campaign, utm_source, ecc.) a tutti i collegamenti e-mail. Questo consente il tracciamento dell’attribuzione in tutto l’ecosistema digitale. [Ulteriori informazioni](../email/url-tracking.md)

* **Traccia collegamenti nei frammenti salvati** - Quando salvi un frammento da un contenuto per il quale è abilitato il tracciamento, i collegamenti in tale frammento rimangono tracciati quando lo riutilizzi in altri percorsi o campagne. [Ulteriori informazioni](../content-management/save-fragments.md)

* **Aggiungi tracciamento pagina mirror** - Abilita l&#39;opzione della pagina mirror per creare una versione Web dell&#39;e-mail con tracciamento automatico di chi la visualizza. [Ulteriori informazioni](../email/message-tracking.md#mirror-page)

**Monitora le prestazioni:** Visualizza le metriche in tempo reale nei report di campagne e percorsi, incluse le aperture, i clic e le prestazioni a livello di collegamento. [Rapporti sulle campagne](../reports/campaign-global-report-cja-email.md) | [Rapporti Percorso](../reports/journey-global-report-cja-email.md)

+++

+++Tracciamento web

Il tracciamento web richiede una configurazione esplicita per tenere traccia delle interazioni dell’utente con le modifiche web.

**Configura tracciamento clic:**

Durante l’authoring di una pagina web, puoi selezionare elementi specifici (pulsanti, immagini, collegamenti) di cui desideri tenere traccia. Questo consente il tracciamento dei clic per tali elementi senza richiedere codice aggiuntivo. [Ulteriori informazioni](../web/monitor-web-experiences.md)

* **Tieni traccia di qualsiasi elemento cliccabile** - Seleziona pulsanti, immagini, collegamenti o qualsiasi elemento interattivo nella personalizzazione Web.
* **Raccolta dati automatica** - Una volta configurata, Journey Optimizer acquisisce automaticamente gli eventi di clic e li associa ai profili.
* **Monitoraggio in tempo reale** - Tieni traccia delle interazioni degli utenti quando convalidano l&#39;efficacia della personalizzazione.

**Visualizza dati di tracciamento:** Accedi a metriche di visualizzazione, tassi di click-through e prestazioni a livello di elemento nei rapporti. [Rapporti sulle campagne](../reports/campaign-global-report-cja-web.md) | [Rapporti Percorso](../reports/journey-global-report-cja-web.md)

+++

+++Tracciamento delle notifiche push

Il tracciamento push viene abilitato automaticamente e acquisisce impression (consegnate), clic (toccate) e aperture (app avviata). Per massimizzare il valore di tracciamento, configura gli elementi cliccabili nel contenuto push.

**Configura elementi tracciati:**

* **Comportamento clic corpo** - Imposta cosa accade quando gli utenti toccano la notifica: apri l&#39;app, passa a un collegamento diretto o apri un URL web. Ogni azione viene tracciata automaticamente. [Ulteriori informazioni](../push/design-push.md#on-click-behavior)

* **Aggiungi pulsanti azione** - Includi fino a 3 pulsanti (Android) o più pulsanti (iOS) con tracciamento indipendente per ogni azione pulsante (apri app, collegamento diretto, URL web). [Ulteriori informazioni](../push/design-push.md#add-buttons-push)

* **Abilita tracciamento** - Verifica che il tracciamento sia abilitato nelle impostazioni di tracciamento dell&#39;attività del percorso push o della campagna. [Ulteriori informazioni](../push/create-push.md#create)

>[!NOTE]
>
>Il tracciamento push richiede l’implementazione di un SDK mobile. Assicurati che l’app disponga del SDK mobile di Adobe Experience Platform configurato correttamente. [Ulteriori informazioni](../push/push-configuration.md#integrate-mobile-app)

**Analisi del coinvolgimento:** Visualizza i tassi di click-through, le prestazioni dei pulsanti e i dettagli dei collegamenti tracciati nei report. [Rapporti sulle campagne](../reports/campaign-global-report-cja-push.md) | [Rapporti Percorso](../reports/journey-global-report-cja-push.md)

+++

+++Tracciamento dei messaggi in-app

I messaggi in-app tengono automaticamente traccia delle visualizzazioni e delle interazioni degli utenti. Configura trigger e contenuti per massimizzare l’efficacia del tracciamento.

**Configura tracciamento:**

* **Definisci le regole di visualizzazione** - Imposta quando e dove vengono visualizzati i messaggi in-app utilizzando trigger (avvio app, caricamento schermo), regole di frequenza e condizioni di pubblico. La corretta configurazione garantisce il tracciamento accurato dei messaggi attivati e visualizzati.

* **Aggiungi elementi tracciati** - Includi pulsanti, collegamenti ed elementi interattivi nel contenuto del messaggio. Ogni interazione viene tracciata automaticamente con etichette dettagliate.

* **Ottimizza tempo di visualizzazione** - Configura le regole del giorno della settimana e dell&#39;ora del giorno per aumentare la probabilità che i messaggi attivati vengano effettivamente visualizzati agli utenti.

[Scopri come configurare i messaggi in-app](../in-app/create-in-app.md)

**Elementi tracciati:** Journey Optimizer acquisisce automaticamente visualizzazioni, clic su pulsanti, chiusure, metriche attivate e visualizzate e prestazioni dei collegamenti. [Rapporti sulle campagne](../reports/campaign-global-report-cja-inapp.md) | [Rapporti Percorso](../reports/journey-global-report-cja-inapp.md)

+++

+++Tracciamento di SMS e MMS

Il tracciamento SMS richiede una configurazione minima: Journey Optimizer abbrevia e tiene traccia automaticamente dei collegamenti inclusi nei messaggi.

**Funzionamento:**

* **Tracciamento automatico dei collegamenti** - Aggiungi qualsiasi URL al contenuto SMS utilizzando la funzione URL helper. Journey Optimizer accorcia automaticamente il collegamento e tiene traccia dei clic senza configurazioni aggiuntive. Per utilizzare la riduzione degli URL, devi prima configurare un sottodominio SMS. [Ulteriori informazioni](../sms/sms-subdomains.md)

* **Tracciamento messaggi in entrata** - Le risposte dei destinatari vengono acquisite automaticamente, consentendo di monitorare le conversazioni bidirezionali e i modelli di risposta. [Ulteriori informazioni](../sms/sms-opt-out.md#sms-native-keywords)

**Visualizza metriche:** Accedi ai dati dei clic sui collegamenti, ai volumi dei messaggi in entrata e alle prestazioni del tipo di messaggio nei report. [Rapporti sulle campagne](../reports/campaign-global-report-cja-sms.md) | [Rapporti Percorso](../reports/journey-global-report-cja-sms.md)

+++

+++Tracciamento delle esperienze basato su codice

Le esperienze basate su codice richiedono la configurazione dell’implementazione per inviare i dati di tracciamento a Adobe Experience Platform.

**Prerequisiti:**

Prima che il tracciamento funzioni, devi configurare l’implementazione per inviare eventi di interazione (visualizzazioni, clic) a Adobe Experience Platform. Ciò richiede:

* Configurazione di uno stream di dati configurato per Adobe Experience Platform. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=it)
* Implementazione della raccolta di eventi nel codice utilizzando Web SDK o Mobile SDK.
* Invio di eventi di visualizzazione e interazione quando il contenuto viene visualizzato o selezionato.

[Ulteriori informazioni sui prerequisiti per l’implementazione](../code-based/code-based-prerequisites.md#reporting-prerequisites)

**Elementi da tracciare:** Una volta implementato, tieni traccia di visualizzazioni, clic, percentuali di click-through e prestazioni a livello di elemento in qualsiasi punto di contatto digitale (siti web, app mobili, dispositivi IoT, ecc.). [Rapporti sulle campagne](../reports/campaign-global-report-cja-code.md) | [Rapporti Percorso](../reports/journey-global-report-cja-code.md)

+++

+++Tracciamento delle schede di contenuto

Le schede di contenuto tengono traccia automaticamente delle interazioni degli utenti. Configura il contenuto e visualizza le regole per controllare il comportamento di tracciamento.

**Come implementare:**

* **Progetta contenuti tracciati** - Aggiungi pulsanti e collegamenti alla scheda dei contenuti. Ogni elemento interattivo viene tracciato automaticamente con etichette e URL.

* **Configura la persistenza** - Le schede dei contenuti persistono nelle sessioni dell&#39;app, consentendo di tenere traccia dei pattern di coinvolgimento a lungo termine. Imposta le regole di scadenza per controllare per quanto tempo le schede rimangono tracciabili.

* **Imposta regole di visualizzazione**: definisci quando e dove vengono visualizzate le schede per garantire un tracciamento accurato delle visualizzazioni rispetto alle interazioni.

[Scopri come configurare le schede di contenuto](../content-card/create-content-card.md)

**Coinvolgimento monitor:** tieni traccia di visualizzazioni, clic, tassi di click-through e pattern di coinvolgimento in più sessioni. [Rapporti sulle campagne](../reports/campaign-global-report-cja-content.md) | [Rapporti Percorso](../reports/journey-global-report-cja-content.md)

+++

+++Tracciamento della pagina di destinazione

Le pagine di destinazione sono dotate di tracciamento integrato che non richiede alcuna configurazione aggiuntiva. Journey Optimizer acquisisce automaticamente visite, conversioni e tassi di mancato recapito.

**Elementi tracciati automaticamente:**

* **Visite** - Visite totali e univoche per misurare la portata
* **Conversioni** - Invio di moduli, conferme di abbonamento o altre azioni definite
* **Percentuale non recapitate** - Percentuale di visitatori che partono senza interagire
* **Tendenze delle prestazioni** - Dati della serie temporale che mostrano l&#39;evoluzione delle metriche

[Scopri come configurare le pagine di destinazione](../landing-pages/create-lp.md)

**Monitora le prestazioni:** tieni traccia di pattern di visite, tassi di conversione e tassi di mancato recapito nel tempo per comprendere in che modo gli utenti interagiscono con i moduli e identificare aree da migliorare. [Rapporti sulla campagna](../reports/lp-report-global-cja.md)

+++

## Tracciare il percorso e l’attività della campagna {#journey-campaign-tracking}

Oltre al tracciamento a livello di canale, configura il tracciamento per misurare le prestazioni generali e comprendere il comportamento dei clienti nelle iniziative di marketing.

* **Definisci metriche di successo personalizzate**: configura KPI specifici allineati agli obiettivi aziendali (acquisti, iscrizioni, rinnovi, ecc.) oltre le metriche di coinvolgimento standard. [Ulteriori informazioni](../building-journeys/success-metrics.md)

* **Attiva eventi dei passaggi del percorso** - Attiva il tracciamento dettagliato di ogni azione intrapresa dai clienti durante il passaggio nei percorsi. Questo fornisce una visibilità granulare dei punti di entrata/uscita, della selezione del percorso e delle posizioni di rilascio. [Ulteriori informazioni](../reports/journey-step-events-overview.md)

* **Imposta pianificazione**: configura l&#39;ottimizzazione del tempo di invio per tenere traccia delle prestazioni in diverse strategie di tempo e identificare le finestre di invio ottimali. [Ulteriori informazioni](../building-journeys/send-time-optimization.md)

* **Configurare il monitoraggio delle azioni personalizzate** - Configurare il monitoraggio per le integrazioni con i sistemi esterni per monitorare le chiamate API, i tempi di risposta e i modelli di errore. [Ulteriori informazioni](../action/reporting.md)

* **Creazione di report personalizzati ed esportazione di dati** - Creazione di report personalizzati ed esportazione di dati di tracciamento in sistemi esterni per analisi più approfondite. [Ulteriori informazioni](../reports/sharing-overview.md)

* **Visualizza prestazioni unificate:** Accedi a report completi sia per le campagne che per i percorsi per confrontare le prestazioni per e-mail, push, SMS e altri canali e per capire quali combinazioni generano i risultati migliori. [Rapporti sulle campagne](../reports/campaign-global-report-cja.md) | [Rapporti Percorso](../reports/journey-global-report-cja.md)

## Tracciare le prestazioni di ottimizzazione e decisioning {#optimization-decisioning-tracking}

Journey Optimizer tiene traccia automaticamente degli esperimenti di ottimizzazione, delle strategie di targeting e delle prestazioni del processo decisionale. Configura le impostazioni per garantire la corretta raccolta dei dati.

### Configurare il tracciamento dell’ottimizzazione {#optimization-tracking}

* **Ottimizzazione nelle campagne e nei percorsi**:

   * Durante la creazione di esperimenti, definisci le metriche da monitorare (conversioni, clic, eventi personalizzati). Journey Optimizer raccoglie automaticamente i dati sulle prestazioni per ogni trattamento. [Ulteriori informazioni](../campaigns/optimization-experimentation.md)

   * Crea regole di targeting per fornire contenuti diversi a segmenti di pubblico diversi. Journey Optimizer tiene traccia automaticamente delle metriche di coinvolgimento per ogni gruppo target, consentendo di confrontare le prestazioni tra segmenti diversi. [Ulteriori informazioni](../campaigns/optimization-targeting.md)

* **Ottimizzazione percorso Percorso**: aggiungi un&#39;attività **Ottimizza** al percorso e configura più percorsi. Journey Optimizer tiene traccia automaticamente dei percorsi seguiti dai profili e misura le prestazioni. [Ulteriori informazioni](../building-journeys/optimize.md)

Per analizzare i risultati: visualizza i tassi di conversione, la significatività statistica e l’incremento tra i trattamenti nei rapporti di sperimentazione oppure confronta le metriche di coinvolgimento tra i segmenti target. [Rapporto sulla campagna di sperimentazione](../reports/campaign-global-report-cja-experimentation.md) | [Rapporto percorso sperimentazioni](../reports/journey-global-report-cja-experimentation.md) | [Rapporto targeting Percorso](../reports/journey-global-report-cja.md#targeting)

### Tracciare le prestazioni di decisioning {#decisioning-tracking}

Quando si utilizza Decisioning per personalizzare il contenuto, Journey Optimizer tiene traccia automaticamente di eventi decisionali, impression e clic senza richiedere alcuna configurazione aggiuntiva.

* **Acquisizione automatica degli eventi** - Journey Optimizer acquisisce automaticamente gli eventi di decisione ogni volta che viene selezionato un elemento di decisione per un profilo.
* **Tracciamento impression** - Per le e-mail, le impression vengono tracciate automaticamente. Per le esperienze basate su codice, devi implementare gli eventi di visualizzazione delle proposte nel codice. [Ulteriori informazioni](../code-based/code-based-implementation-samples.md#client-side-how)
* **Tracciamento dei clic** - I clic sugli elementi decisionali vengono tracciati automaticamente nelle e-mail; le esperienze basate su codice richiedono l&#39;implementazione di eventi di clic.

>[!NOTE]
>
>Per tenere traccia delle decisioni nelle **esperienze basate su codice**, assicurati che l&#39;implementazione invii eventi di interazione della proposta (visualizzazioni e clic) a Adobe Experience Platform utilizzando Web SDK o Mobile SDK. [Ulteriori informazioni](../experience-decisioning/data-collection/schema-requirement.md)

Per monitorare le prestazioni: visualizza i KPI di decisioning, confronta gli elementi decisionali, analizza le strategie di selezione e monitora le prestazioni del modello di IA nei rapporti. [Ulteriori informazioni](../experience-decisioning/cja-reporting.md)

## Controllare l’utilizzo dei dati di tracciamento {#data-governance}

I criteri di governance dei dati ti consentono di controllare come utilizzare i dati di tracciamento in tutta l’organizzazione:

* **Etichettare i dati di tracciamento sensibili** - Applicare etichette di governance ai dati comportamentali tracciati (ad esempio, clic sul contenuto sanitario, interazioni con prodotti finanziari) per contrassegnarli come sensibili o regolamentati.

* **Limita l&#39;utilizzo dei dati** - Crea criteri che impediscono l&#39;utilizzo dei dati di tracciamento con etichetta in alcuni canali, l&#39;esportazione in sistemi di terze parti o l&#39;utilizzo in scenari di personalizzazione specifici.

* **Applicazione automatica** - Journey Optimizer controlla automaticamente i criteri di governance durante la creazione di percorsi e campagne, bloccando la pubblicazione se i dati tracciati vengono utilizzati in violazione dei criteri definiti.

La governance dei dati garantisce la conformità a normative come RGPD e CCPA, consentendo al contempo di monitorare e analizzare il comportamento dei clienti entro i limiti approvati. [Ulteriori informazioni](../action/action-privacy.md)

## Monitorare il recapito messaggi e lo stato del sistema {#monitoring-capabilities}

Oltre a monitorare il coinvolgimento, configura il monitoraggio per garantire che i messaggi raggiungano le caselle in entrata e che i sistemi funzionino in modo ottimale.

Il monitoraggio del recapito messaggi consente di garantire che i messaggi raggiungano le caselle in entrata dei destinatari e mantengano una buona reputazione del mittente tenendo traccia degli indicatori chiave:

* **Rivedi regolarmente l&#39;elenco di soppressione** per capire perché gli indirizzi sono bloccati e mantenere l&#39;igiene degli elenchi. [Ulteriori informazioni](../reports/suppression-list.md)

* **Analizza gli errori di consegna** per diagnosticare gli errori e intraprendere azioni correttive. [Ulteriori informazioni](../configuration/email-error-types.md)

* **Segui le best practice** per DMARC, SPF e DKIM per massimizzare il posizionamento della casella in entrata. [Ulteriori informazioni](../reports/deliverability.md)

Imposta il monitoraggio proattivo per ricevere notifiche in tempo reale su eventi critici e problemi di sistema, consentendo di rispondere rapidamente prima che influiscano sull’esperienza del cliente:

* **Configura avvisi** - Imposta le notifiche in tempo reale per gli errori di percorso, gli errori delle azioni personalizzate e i problemi critici, in modo da rispondere rapidamente ai problemi. [Ulteriori informazioni](../reports/alerts.md)

* **Abilita registri di controllo** - Attiva la registrazione di controllo per tenere traccia di tutte le azioni sulle risorse per la conformità e la risoluzione dei problemi. [Ulteriori informazioni](../privacy/audit-logs.md)

* **Monitora le integrazioni** - Tieni traccia delle prestazioni delle azioni personalizzate e della connettività di sistema esterna per identificare in anticipo i problemi di integrazione. [Ulteriori informazioni](../action/reporting.md)

