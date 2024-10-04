---
solution: Journey Optimizer
product: journey optimizer
title: Rapporto globale della campagna
description: Scopri come utilizzare i dati del rapporto globale della campagna
feature: Reporting
topic: Content Management
role: User
level: Intermediate
badge: label="Disponibilità limitata" type="Informative"
exl-id: 51cbe27f-3f3f-471e-a5d9-e3a88fcfdd68
source-git-commit: d816b12ea88631d6682cf444e176622f8fc36d85
workflow-type: tm+mt
source-wordcount: '4540'
ht-degree: 2%

---

# Rapporto campagna {#campaign-global-report-cja}

Il report **Campaign** funge da dashboard completo e fornisce un&#39;analisi dettagliata delle metriche chiave associate alla campagna. Include dati quali il conteggio dei clic, i messaggi consegnati, i numeri di profilo e le azioni intraprese. Offrendo una panoramica completa dell’efficacia e dei livelli di coinvolgimento della campagna, il rapporto assicura una comprensione approfondita delle prestazioni complessive della campagna.

I report delle campagne sono accessibili direttamente dalla campagna con il pulsante **[!UICONTROL Report]**.

![](assets/gs-cja-report-2.png)

La pagina **Report campagna** verrà visualizzata con le seguenti schede, a seconda del canale scelto:

* [Campaign](#campaign-global)
* [Sperimentazione](#experimentation)
* [E-mail](#email-global)
* [SMS](#sms)
* [Notifica push](#push-notification)
* [Direct mail](#direct-mail)
* [Web](#web)
* [Scheda contenuto](#content-card)

Per ulteriori informazioni su Customer Journey Analytics Workspace e su come filtrare e analizzare i dati, fare riferimento a [questa pagina](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/home).

## Campaign {#campaign-global}

### KPI della campagna {#campaign-kpis}

![](assets/cja-email-kpis.png)

I **[!UICONTROL indicatori di prestazioni chiave (KPI, Key Performance Indicators) di Campaign]** funzionano come dashboard completo che fornisce un&#39;analisi delle metriche essenziali associate alla campagna. Questo include dettagli quali il numero di clic e il numero di messaggi consegnati, offrendo una visione completa dell’efficacia della campagna e del livello di coinvolgimento.

I KPI variano in base ai canali utilizzati nella campagna.

+++ Ulteriori informazioni sulle metriche dei KPI per Campaign

* **[!UICONTROL Percentuale di click-through]**: percentuale di utenti che hanno interagito con il messaggio.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nel messaggio.

* **[!UICONTROL Recapitato]**: numero di e-mail inviate correttamente, in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Visualizzazioni]**: numero di volte in cui il messaggio è stato aperto.

+++

### Panoramica della campagna {#delivery-global}

![](assets/cja-campaign-overview.png)

La tabella **[!UICONTROL Panoramica campagna]** funge da dashboard completo e offre una suddivisione dettagliata delle metriche chiave correlate alla campagna. Ciò include informazioni essenziali come il numero di profili e le azioni consegnate, fornendo una comprensione approfondita delle prestazioni e del coinvolgimento della campagna.

Tieni presente che le metriche variano in base ai canali utilizzati nella campagna.

+++ Ulteriori informazioni sulle metriche della panoramica di Campaign

* **[!UICONTROL Persone]**: numero di profili utente qualificati come profili target per i messaggi.

* **[!UICONTROL Percentuale di click-through]**: percentuale di utenti che hanno interagito con il messaggio.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nel messaggio.

* **[!UICONTROL Clic univoci]**: numero di profili che hanno fatto clic su un contenuto del messaggio.

* **[!UICONTROL Recapitato]**: numero di e-mail inviate correttamente, in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Mancati recapiti per i canali in uscita]**: numero totale di errori accumulati durante il processo di invio e l&#39;elaborazione automatica dei resi in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Errori in uscita]**: numero totale di errori che si sono verificati durante il processo di invio e che ne hanno impedito l&#39;invio ai profili.

* **[!UICONTROL Esclusioni in uscita]**: numero di profili esclusi da Adobe Journey Optimizer.

* **[!UICONTROL Visualizzazioni]**: numero di volte in cui il messaggio è stato aperto.

* **[!UICONTROL Visualizzazioni univoche]**: il numero di volte in cui il messaggio è stato aperto; non vengono prese in considerazione più interazioni di un profilo.

+++

### Risultati funnel della campagna {#campaign-funnel}

![](assets/cja-campaign-funnel.png)

Il grafico **[!UICONTROL Risultati funnel campagna]** presenta un&#39;analisi dettagliata del coinvolgimento dei profili con i messaggi, fornendo informazioni utili sulle interazioni tra vari profili e il contenuto.

+++ Ulteriori informazioni sulle metriche dei risultati del funnel di Campaign

* **[!UICONTROL Recapitato]**: numero di e-mail inviate correttamente, in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nel messaggio.
+++

### Etichetta collegamento tracciato {#campaign-track}

![](assets/cja-campaign-tracked-link.png)

La tabella **[!UICONTROL Tracked link label]** offre informazioni essenziali sul coinvolgimento dei visitatori con gli URL inclusi nei messaggi, fornendo informazioni utili su quali collegamenti attraggono il maggior numero di interazioni.

+++ Ulteriori informazioni sulle metriche delle etichette dei collegamenti tracciati

* **[!UICONTROL Clic univoci]**: numero di profili che hanno fatto clic su un contenuto del messaggio.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nel messaggio.

+++

## Sperimentazione {#experimentation}

La scheda **[!UICONTROL Sperimentazione]** fornisce informazioni chiave sulle prestazioni di ogni variante e identifica quella che ha avuto maggior successo.

Si noti che la definizione dell&#39;esecutore migliore potrebbe richiedere un po&#39; di tempo. Se l&#39;esperimento non ha esito positivo, verrà impostato su **Non conclusivo**.

![](assets/cja-experimentation-1.png)

### KPI della sperimentazione {#experimentation-kpis}

![](assets/cja-experimentation-kpis.png)

I **[!UICONTROL Indicatori prestazioni chiave (KPI, Key Performance Indicators) della sperimentazione]** funzionano come dashboard completo che fornisce un&#39;analisi delle metriche essenziali associate alla sperimentazione.

+++ Ulteriori informazioni sulle metriche dei KPI nella sperimentazione

* **[!UICONTROL Incremento]**: misura del miglioramento percentuale del tasso di conversione di un determinato trattamento rispetto al basale.

* **[!UICONTROL Affidabilità]**: prova che un determinato trattamento è uguale al trattamento basale. [Ulteriori informazioni](../content-management/experiment-calculations.md#understand-confidence)

+++

### Variante per clic in entrata {#variant-inbound}

![](assets/cja-experimentation-variants.png)

Il widget **[!UICONTROL Variante per clic in entrata]** descrive le prestazioni di ogni variante.
Per informazioni approfondite su questi risultati e su come interpretarli, consulta [questa pagina](../content-management/get-started-experiment.md#interpret-results).

+++ Ulteriori informazioni sulla variante per metriche di clic in entrata

* **[!UICONTROL Persone]**: numero di profili utente qualificati come profili target per i messaggi.

* **[!UICONTROL Clic in entrata]**: numero totale di clic tra i canali in uscita.

* **[!UICONTROL Tasso di conversione]**: valore totale della metrica di successo, precedentemente selezionata durante la creazione degli esperimenti, diviso per il numero di profili.

* **[!UICONTROL Incremento]**: misura del miglioramento percentuale del tasso di conversione di un determinato trattamento rispetto al basale.

* **[!UICONTROL Affidabilità]**: prova che un determinato trattamento è uguale al trattamento basale. [Ulteriori informazioni](../content-management/experiment-calculations.md#understand-confidence)

<!--
* **[!UICONTROL Confidence Upper bound]**:

* **[!UICONTROL Confidence Lower bound]**:
-->
+++

### Tasso di conversione per i clic in entrata {#conversion-rate}

![](assets/cja-experimentation-conversion.png)

Il grafico **[!UICONTROL Intervallo di affidabilità]** misura l&#39;incertezza sul miglioramento. Descrive la differenza percentuale nelle prestazioni tra la linea di base e il trattamento dalle prestazioni migliori. [Ulteriori informazioni](../content-management/experiment-calculations.md#confidence-intervals).

## E-mail {#email-global}

### Tendenza consegne e clic {#delivered-click}

![](assets/cja-email-delivered-click.png)

Il grafico **[!UICONTROL Tendenza consegna vs clic]** presenta un&#39;analisi dettagliata del coinvolgimento dei tuoi profili con le e-mail, fornendo informazioni utili sul modo in cui i profili interagiscono con il contenuto.

+++ Ulteriori informazioni sulle metriche di tendenza Consegne e Clic

* **[!UICONTROL Recapitato]**: numero di e-mail inviate correttamente rispetto al numero totale di e-mail inviate.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nelle e-mail.

+++


### Stato consegna {#delivery-status}

![](assets/cja-email-delivery-status.png)

Il grafico **[!UICONTROL Stato consegna]** fornisce una visualizzazione completa dei dati relativi alle e-mail inviate nella campagna, offrendo informazioni approfondite sulle metriche chiave, ad esempio consegnate e non recapitate. Ciò consente un’analisi dettagliata del processo di invio delle e-mail, fornendo informazioni preziose sull’efficienza e le prestazioni delle campagne.

+++ Ulteriori informazioni sulle metriche dello stato della consegna

* **[!UICONTROL Recapitato]**: numero di e-mail inviate correttamente rispetto al numero totale di e-mail inviate.

* **[!UICONTROL Mancati recapiti per i canali in uscita]**:Totale degli errori accumulati durante il processo di invio e l&#39;elaborazione automatica dei resi in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Errori in uscita]**: numero totale di errori che si sono verificati durante un processo di invio e che ne hanno impedito l&#39;invio ai profili.

* **[!UICONTROL Esclusioni in uscita]**: numero di profili esclusi da Adobe Journey Optimizer.

+++

### Statistiche di invio {#sending-statistics-email}

![](assets/cja-email-sending-stat.png)

La tabella **[!UICONTROL Statistiche di invio]** fornisce un riepilogo completo dei dati essenziali relativi alle e-mail nelle campagne. Descrive le metriche chiave, ad esempio le interazioni con le e-mail e il numero di e-mail inviate correttamente, fornendo informazioni utili sull’efficacia e la portata delle e-mail e delle campagne.

+++ Ulteriori informazioni sull’invio di metriche delle statistiche

* **[!UICONTROL Persone]**: numero di profili utente qualificati come profili target per i messaggi.

* **[!UICONTROL Destinato]**: numero totale di e-mail elaborate durante il processo di invio.

* **[!UICONTROL Invii]**: numero totale di invii per e-mail.

* **[!UICONTROL Recapitato]**: numero di e-mail inviate correttamente, in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Mancati recapiti per i canali in uscita]**: totale degli errori accumulati durante il processo di invio e l&#39;elaborazione automatica dei resi in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Errori in uscita]**: numero totale di errori che si sono verificati durante il processo di invio e che ne hanno impedito l&#39;invio ai profili.

* **[!UICONTROL Esclusioni in uscita]**: numero di profili esclusi da Adobe Journey Optimizer.

+++

### Statistiche di tracciamento {#tracking-statistics-email}

![](assets/cja-email-track-stat.png)

La tabella **[!UICONTROL E-mail - Statistiche di tracciamento]** offre un account dettagliato dell&#39;attività profilo relativa alle e-mail incluse nella campagna. Ciò include metriche su aperture, clic e altri indicatori di coinvolgimento rilevanti, che offrono una visualizzazione completa del modo in cui i profili interagiscono con il contenuto dell’e-mail.

+++ Ulteriori informazioni sulle metriche delle statistiche di tracciamento

* **[!UICONTROL Tasso di click-through (CTR)]**: percentuale di utenti che hanno interagito con l&#39;e-mail.

* **[!UICONTROL Percentuale di apertura dei clic]**: numero di volte in cui l&#39;e-mail è stata aperta.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nelle e-mail.

* **[!UICONTROL Clic univoci]**: numero di profili che hanno fatto clic su un contenuto in un messaggio e-mail.

* **[!UICONTROL Aperture e-mail]**: il numero di volte in cui le e-mail sono state aperte in una campagna.

* **[!UICONTROL Aperture e-mail univoche]**: percentuale di messaggi e-mail aperti.

* **[!UICONTROL Reclami spam]**: numero di volte in cui un messaggio è stato dichiarato come spam o posta indesiderata.

* **[!UICONTROL Annullamenti iscrizione]**: numero di clic sul collegamento di annullamento dell&#39;iscrizione.

+++


### Domini e-mail {#email-domains}

![](assets/cja-email-email-domains.png)

La tabella **[!UICONTROL Domini e-mail]** offre una suddivisione approfondita delle e-mail suddivise per dominio, fornendo informazioni approfondite sulle metriche delle prestazioni delle campagne e-mail. Questa analisi completa ti consente di comprendere il comportamento di diversi domini in risposta al contenuto delle e-mail.

+++ Ulteriori informazioni sulle metriche dei domini e-mail

* **[!UICONTROL Invii]**: numero totale di invii per e-mail.

* **[!UICONTROL Recapitato]**: numero di e-mail inviate correttamente rispetto al numero totale di e-mail inviate.

* **[!UICONTROL Aperture e-mail]**: il numero di volte in cui le e-mail sono state aperte in una campagna.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nelle e-mail.

* **[!UICONTROL Mancati recapiti per i canali in uscita]**: numero totale di errori accumulati durante il processo di invio e l&#39;elaborazione della restituzione automatica in relazione al numero totale di e-mail inviate.

* **[!UICONTROL Errori in uscita]**: numero totale di errori che si sono verificati durante il processo di invio e che ne hanno impedito l&#39;invio ai profili.
+++

### Etichette collegamenti tracciati {#track-link-label}

![](assets/cja-email-tracked-link.png)

La tabella **[!UICONTROL Etichette di collegamento tracciate]** offre una panoramica completa delle etichette di collegamento all&#39;interno delle e-mail, evidenziando quelle che generano il traffico di visitatori più elevato. Questa funzione ti consente di identificare e assegnare la priorità ai collegamenti più popolari.

+++ Ulteriori informazioni sulle metriche delle etichette dei collegamenti tracciati

* **[!UICONTROL Clic univoci]**: numero di profili che hanno fatto clic su un contenuto in un messaggio e-mail.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nelle e-mail.

+++

### URL collegamenti tracciati {#track-link-url}

![](assets/cja-journey-tracked-link-urls.png)

La tabella **[!UICONTROL URL di collegamento tracciati]** fornisce una panoramica completa degli URL all&#39;interno dell&#39;e-mail che attraggono il traffico più elevato dei visitatori. Questo consente di identificare e assegnare la priorità ai collegamenti più popolari, migliorando la comprensione del coinvolgimento del profilo con contenuti specifici nelle e-mail.

+++ Ulteriori informazioni sulle metriche degli URL di collegamento tracciati

* **[!UICONTROL Clic univoci]**: numero di profili che hanno fatto clic su un contenuto in un messaggio e-mail.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nelle e-mail.

* **[!UICONTROL Visualizzazioni]**: numero di volte in cui l&#39;e-mail è stata aperta.

* **[!UICONTROL Visualizzazioni univoche]**: numero di volte in cui l&#39;e-mail è stata aperta, non vengono prese in considerazione più interazioni di un profilo.

+++

### Oggetti e-mail {#email-subjects}

![](assets/cja-email-subject.png)

La tabella **[!UICONTROL Oggetti e-mail]** presenta una panoramica completa degli oggetti e-mail che hanno attirato il traffico visitatore più elevato. Questa risorsa offre informazioni preziose sulle dinamiche di coinvolgimento del pubblico.

+++ Ulteriori informazioni sulle metriche degli oggetti e-mail

* **[!UICONTROL Persone]**: numero di profili utente qualificati come profili target per le e-mail.

+++

### Motivi di esclusione {#excluded-reasons}

La tabella **[!UICONTROL Motivi di esclusione]** presenta una visualizzazione completa dei diversi fattori che hanno determinato l&#39;esclusione dei profili utente dal pubblico di destinazione, causando la mancata ricezione del messaggio.

Per un elenco completo dei motivi di esclusione, consulta [questa pagina](exclusion-list.md).

### Motivi di mancato recapito {#bounce-reasons-email}

La tabella **[!UICONTROL Motivi di mancato recapito]** compila i dati disponibili relativi ai messaggi non recapitati, fornendo informazioni dettagliate sui motivi specifici alla base dei mancati recapiti e-mail.

Per ulteriori informazioni sui mancati recapiti, consulta la pagina [Elenco di soppressione](../reports/suppression-list.md).

### Motivi di errore {#error-reasons-email}

La tabella **[!UICONTROL Motivi di errore]** offre visibilità sugli errori specifici che si sono verificati durante il processo di invio, fornendo informazioni utili sulla natura e sulla ricorrenza degli errori.

## SMS {#sms}

### Tendenza consegne e clic {#delivered-click-sms}

Il grafico **[!UICONTROL Tendenza consegna vs clic]** presenta un&#39;analisi dettagliata del coinvolgimento dei tuoi profili con le e-mail, fornendo informazioni utili sul modo in cui i profili interagiscono con il contenuto.

+++ Ulteriori informazioni sulle metriche di tendenza Consegne e Clic

* **[!UICONTROL Recapitato]**: numero di messaggi SMS inviati correttamente, in relazione al numero totale di messaggi SMS.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nei messaggi SMS.

+++

### Stato consegna {#delivery-status-sms}

La tabella **[!UICONTROL Stato consegna]** offre un account dettagliato dell&#39;attività del profilo correlata alle campagne SMS. Ciò include metriche su consegnati, clic e altri indicatori di coinvolgimento rilevanti, che offrono una panoramica completa del modo in cui i profili interagiscono con il contenuto SMS.

+++ Ulteriori informazioni sulle metriche dello stato della consegna

* **[!UICONTROL Recapitato]**: numero di messaggi SMS inviati correttamente, in relazione al numero totale di messaggi SMS.

* **[!UICONTROL Mancati recapiti per i canali in uscita]**: totale degli errori accumulati durante il processo di invio e l&#39;elaborazione automatica dei resi in relazione al numero totale di messaggi SMS inviati.

* **[!UICONTROL Errori in uscita]**: numero totale di errori che ne impediscono l&#39;invio ai profili.

* **[!UICONTROL Esclusioni in uscita]**: numero di profili esclusi da Adobe Journey Optimizer.

+++

### Etichette collegamenti tracciati {#track-link-label-sms}

La tabella **[!UICONTROL Etichette di collegamento tracciate]** offre una panoramica completa delle etichette di collegamento all&#39;interno dei messaggi SMS, evidenziando quelle che generano il traffico di visitatori più elevato. Questa funzione ti consente di identificare e assegnare la priorità ai collegamenti più popolari.

+++ Ulteriori informazioni sulle metriche delle etichette dei collegamenti tracciati

* **[!UICONTROL Clic univoci]**: numero di profili che hanno fatto clic su un contenuto nel messaggio SMS.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nei messaggi SMS.

+++

### URL collegamenti tracciati {#track-link-url-sms}

La tabella **[!UICONTROL URL di collegamento tracciati]** fornisce una panoramica completa degli URL all&#39;interno dei messaggi SMS che attraggono il traffico più elevato dei visitatori. Questo consente di identificare e assegnare la priorità ai collegamenti più popolari, migliorando la comprensione del coinvolgimento del profilo con contenuti specifici nei messaggi SMS.

+++ Ulteriori informazioni sulle metriche degli URL di collegamento tracciati

* **[!UICONTROL Clic univoci]**: numero di profili che hanno fatto clic su un contenuto nel messaggio SMS.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nei messaggi SMS.

* **[!UICONTROL Visualizzazioni]**: numero di volte in cui il messaggio è stato aperto.

* **[!UICONTROL Visualizzazioni univoche]**: il numero di volte in cui il messaggio è stato aperto; non vengono prese in considerazione più interazioni di un profilo.

+++

### Messaggio SMS in entrata {#sms-inbound}

La tabella **[!UICONTROL Messaggio SMS in entrata]** presenta una panoramica completa dei messaggi SMS che hanno attirato il traffico più elevato. Questa risorsa offre informazioni preziose sulle dinamiche di coinvolgimento del pubblico.

+++ Ulteriori informazioni sulle metriche dei messaggi SMS in entrata

* **[!UICONTROL Persone]**: numero di profili utente qualificati come profili target per i messaggi SMS.

+++

### Tipo di messaggio SMS {#sms-message-type}

La tabella **[!UICONTROL Tipo di messaggio SMS]** presenta una panoramica completa del tipo di messaggio SMS che ha attirato il traffico più elevato. Questa risorsa offre informazioni preziose sulle dinamiche di coinvolgimento del pubblico.

+++ Ulteriori informazioni sulle metriche del tipo di messaggio SMS

* **[!UICONTROL Persone]**: numero di profili utente qualificati come profili target per i messaggi SMS.

+++

### Provider SMS {#sms-providers}

La tabella **[!UICONTROL Provider SMS]** presenta una panoramica completa dei provider SMS che hanno attirato il traffico più elevato. Questa risorsa offre informazioni preziose sulle dinamiche di coinvolgimento del pubblico.

+++ Ulteriori informazioni sulle metriche dei provider SMS

* **[!UICONTROL Persone]**: numero di profili utente qualificati come profili target per i messaggi SMS.

+++

### Motivi di mancato recapito {#bounce-reasons-sms}

La tabella **[!UICONTROL Motivi di mancato recapito]** fornisce una panoramica completa dei dati relativi ai messaggi SMS non recapitati, fornendo informazioni utili sulle ragioni specifiche alla base delle istanze di mancato recapito dei messaggi SMS.

### Motivi di errore {#error-reasons-sms}

La tabella **[!UICONTROL Motivi di errore]** consente di identificare gli errori specifici che si sono verificati durante il processo di invio dei messaggi SMS, facilitando un&#39;analisi approfondita di eventuali problemi riscontrati.

### Motivi di esclusione {#excluded-reasons-sms}

La tabella **[!UICONTROL Escludi motivi]** mostra visivamente i diversi fattori che hanno portato all&#39;esclusione dei profili utente dal pubblico di destinazione, impedendo loro di ricevere i messaggi SMS.

Per un elenco completo dei motivi di esclusione, consulta [questa pagina](exclusion-list.md).

## Notifica push {#push-notification}

### Statistiche di invio {#sending-statistics-push}

![](assets/cja-campaign-push-sending-stat.png)

La tabella **[!UICONTROL Statistiche di invio]** fornisce un riepilogo completo dei dati essenziali relativi alle campagne di notifica push. Descrive le metriche chiave, ad esempio la dimensione del pubblico target e il numero di notifiche push inviate correttamente, fornendo informazioni utili sull’efficacia e la portata delle notifiche push.

+++ Ulteriori informazioni sull’invio di metriche delle statistiche

* **[!UICONTROL Persone]**: numero di profili utente idonei come profili di destinazione per le notifiche push.

* **[!UICONTROL Target]**: numero totale di notifiche push elaborate durante l&#39;analisi.

* **[!UICONTROL Invii]**: numero totale di invii per la notifica push.

* **[!UICONTROL Recapitato]**: numero di notifiche push inviate correttamente, in relazione al numero totale di notifiche push inviate.

* **[!UICONTROL Mancati recapiti per i canali in uscita]**: totale degli errori accumulati durante il processo di invio ed elaborazione automatica dei resi in relazione al numero totale di notifiche push.

* **[!UICONTROL Errori in uscita]**: numero totale di errori che ne impediscono l&#39;invio ai profili.

* **[!UICONTROL Esclusioni in uscita]**: numero di profili esclusi da Adobe Journey Optimizer.

+++

### Statistiche di tracciamento {#tracking-statistics-push}

![](assets/cja-campaign-push-track-stat.png)

La tabella **[!UICONTROL Statistiche di tracciamento]** offre un&#39;istantanea dettagliata dell&#39;attività di profilo associata alle notifiche push, fornendo informazioni essenziali sull&#39;efficacia delle notifiche push e di coinvolgimento.

+++ Ulteriori informazioni sulle metriche delle statistiche di tracciamento

* **[!UICONTROL Tasso di click-through (CTR)]**: percentuale di utenti che hanno interagito con le notifiche push.

* **[!UICONTROL Percentuale di apertura click-through (CTOR)]**: numero di volte in cui sono state aperte le notifiche push.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nelle notifiche push.

* **[!UICONTROL Clic univoci]**: numero di profili che hanno fatto clic su un contenuto nelle notifiche push.

<!--
* **[!UICONTROL Push custom actions]**: 
-->
+++

### Etichette collegamenti tracciati {#track-link-label-push}

![](assets/cja-campaign-push-link-labels.png)

La tabella **[!UICONTROL Etichette di collegamento tracciate]** offre una panoramica completa delle etichette di collegamento all&#39;interno delle notifiche push, evidenziando quelle che generano il traffico di visitatori più elevato. Questa funzione ti consente di identificare e assegnare la priorità ai collegamenti più popolari.

+++ Ulteriori informazioni sulle metriche delle etichette dei collegamenti tracciati

* **[!UICONTROL Clic univoci]**: numero di profili che hanno fatto clic su un contenuto nelle notifiche push.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nelle notifiche push.

+++

### URL collegamenti tracciati {#track-link-url-push}

![](assets/cja-campaign-push-link-urls.png)

La tabella **[!UICONTROL URL di collegamento tracciati]** fornisce una panoramica completa degli URL all&#39;interno delle notifiche push che attirano il traffico più elevato di visitatori. Questo consente di identificare e assegnare la priorità ai collegamenti più popolari, migliorando la comprensione del coinvolgimento del profilo con contenuti specifici nelle notifiche push.

+++ Ulteriori informazioni sulle metriche degli URL di collegamento tracciati

* **[!UICONTROL Clic univoci]**: numero di profili che hanno fatto clic su un contenuto nelle notifiche push.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nelle notifiche push.

+++

### Motivi di mancato recapito {#bounce-reasons-push}

La tabella **[!UICONTROL Motivi di mancato recapito]** fornisce una panoramica completa dei dati relativi alle notifiche push non recapitate, fornendo informazioni utili sulle ragioni specifiche alla base delle istanze di mancato recapito delle notifiche push.

### Motivi di errore {#error-reasons-push}

La tabella **[!UICONTROL Motivi di errore]** consente di identificare gli errori specifici che si sono verificati durante il processo di invio delle notifiche push, semplificando un&#39;analisi approfondita di eventuali problemi riscontrati.

### Motivi di esclusione {#exclude-reasons-push}

![](assets/cja-campaign-push-excluded.png)

La tabella **[!UICONTROL Escludi motivi]** illustra visivamente i diversi fattori che hanno portato all&#39;esclusione dei profili utente dal pubblico di destinazione, impedendo loro di ricevere le notifiche push.

Per un elenco completo dei motivi di esclusione, consulta [questa pagina](exclusion-list.md).

## In-app {#in-app}

### Tendenza impression e clic {#impression-click-trend}

![](assets/cja-inapp-impressions-click.png)

Il grafico **[!UICONTROL Tendenza impression e clic]** presenta un&#39;analisi dettagliata del coinvolgimento dei tuoi profili con i messaggi in-app, fornendo informazioni preziose su come i profili interagiscono con i contenuti.

+++ Ulteriori informazioni sulle metriche della tendenza Impression &amp; Click

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nei messaggi in-app.

* **[!UICONTROL Visualizzazioni]**: numero di volte in cui il messaggio è stato aperto.

+++

### Clic {#clicks-inapp}

Il grafico **[!UICONTROL Clic]** visualizza le metriche di clic in-app, illustrando sia il numero totale di clic sul contenuto che il numero di profili univoci che hanno fatto clic sul contenuto.

+++ Ulteriori informazioni sulle metriche Clic

* **[!UICONTROL Clic univoci]**: numero di profili che hanno fatto clic su un contenuto nei messaggi in-app

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nei messaggi in-app.

+++

### Visualizzazione {#display-inapp}

Il grafico **[!UICONTROL Displays]** ti aiuta a comprendere sia la portata complessiva del messaggio che il numero di profili univoci coinvolti con esso.

+++ Ulteriori informazioni sulle metriche di visualizzazione

* **[!UICONTROL Visualizzazioni]**: numero di volte in cui il messaggio è stato aperto.

* **[!UICONTROL Visualizzazioni univoche]**: il numero di volte in cui il messaggio è stato aperto; non vengono prese in considerazione più interazioni di un profilo.

+++

### Dati di tracciamento {#tracking-data-inapp}

La tabella **[!UICONTROL Dati di tracciamento]** offre un&#39;istantanea dettagliata dell&#39;attività del profilo associata ai messaggi in-app, fornendo informazioni essenziali sull&#39;efficacia del coinvolgimento e dei messaggi in-app.

+++ Ulteriori informazioni sul tracciamento delle metriche dei dati

* **[!UICONTROL Persone]**: numero di profili utente idonei come profili di destinazione per i messaggi in-app.

* **[!UICONTROL Tasso di click-through (CTR)]**: percentuale di utenti che hanno interagito con i messaggi in-app.

* **[!UICONTROL Percentuale di apertura dei clic]**: numero di volte in cui i messaggi in-app sono stati aperti.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nei messaggi in-app.

* **[!UICONTROL Clic univoci]**: numero di profili che hanno fatto clic su un contenuto nei messaggi in-app.

* **[!UICONTROL Visualizzazioni]**: numero di volte in cui il messaggio è stato aperto.

* **[!UICONTROL Visualizzazioni univoche]**: il numero di volte in cui il messaggio è stato aperto; non vengono prese in considerazione più interazioni di un profilo.

* **[!UICONTROL Invii]**: numero totale di invii per i messaggi in-app.

<!--
* **[!UICONTROL Inbound triggered]**: 

* **[!UICONTROL Inbound dismisses]**: 
-->
+++

### Etichette collegamenti tracciati {#track-link-label-inapp}

![](assets/cja-inapp-tracked-link-labels.png)

La tabella **[!UICONTROL Etichette di collegamento tracciate]** offre una panoramica completa delle etichette di collegamento all&#39;interno dei messaggi in-app, evidenziando quelle che generano il traffico di visitatori più elevato. Questa funzione ti consente di identificare e assegnare la priorità ai collegamenti più popolari.

+++ Ulteriori informazioni sulle metriche delle etichette dei collegamenti tracciati

* **[!UICONTROL Clic univoci]**: numero di profili che hanno fatto clic su un contenuto nei messaggi in-app.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nei messaggi in-app.

* **[!UICONTROL Visualizzazioni]**: numero di volte in cui il messaggio è stato aperto.

* **[!UICONTROL Visualizzazioni univoche]**: il numero di volte in cui il messaggio è stato aperto; non vengono prese in considerazione più interazioni di un profilo.

+++

### URL collegamenti tracciati {#track-link-url-inapp}

![](assets/cja-inapp-tracked-link-urls.png)

La tabella **[!UICONTROL URL di collegamento tracciati]** fornisce una panoramica completa degli URL all&#39;interno dei messaggi in-app che attraggono il traffico più elevato di visitatori. Questo consente di identificare e assegnare la priorità ai collegamenti più popolari, migliorando la comprensione del coinvolgimento del profilo con contenuti specifici nei messaggi in-app.

+++ Ulteriori informazioni sulle metriche degli URL di collegamento tracciati

* **[!UICONTROL Clic univoci]**: numero di profili che hanno fatto clic su un contenuto nei messaggi in-app.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nei messaggi in-app.

+++

## Direct mail {#direct-mail}

### Statistiche di invio {#sending-statistics-directmail}

![](assets/cja-direct-sending-stat.png)

La tabella **[!UICONTROL Statistiche di invio]** fornisce un riepilogo completo dei dati essenziali relativi alle campagne direct mailing. Descrive metriche chiave quali le dimensioni del pubblico target e il numero di direct mailing consegnati correttamente, fornendo informazioni preziose sull’efficacia e la portata dei messaggi di direct mailing.

+++ Ulteriori informazioni sull’invio di metriche delle statistiche

* **[!UICONTROL Persone]**: numero di profili utente qualificati come profili target per i messaggi.

* **[!UICONTROL Destinati]**: numero totale di messaggi di direct mailing elaborati durante il processo di invio.

* **[!UICONTROL Invii]**: numero totale di invii per i messaggi di direct mailing.

* **[!UICONTROL Recapitato]**: numero di messaggi di direct mailing inviati correttamente, in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Errori in uscita]**: numero totale di errori che si sono verificati durante il processo di invio e che ne hanno impedito l&#39;invio ai profili.

* **[!UICONTROL Esclusioni in uscita]**: numero di profili esclusi da Adobe Journey Optimizer.

+++

### Stato consegna {#delivery-status-directmail}

![](assets/cja-direct-delivery-status.png)

Il grafico **[!UICONTROL Stato consegna]** fornisce una visualizzazione completa dei dati relativi ai messaggi di direct mailing inviati nella campagna, offrendo informazioni approfondite sulle metriche chiave, come consegnati ed errori. Ciò consente un’analisi dettagliata del processo di invio dei messaggi di direct mailing, fornendo informazioni preziose sull’efficienza e le prestazioni delle campagne.

+++ Ulteriori informazioni sulle metriche dello stato della consegna

* **[!UICONTROL Recapitato]**: numero di messaggi di direct mailing inviati correttamente, in relazione al numero totale di messaggi di direct mailing inviati.

* **[!UICONTROL Errori in uscita]**: numero totale di errori che si sono verificati durante il processo di invio e che impediscono l&#39;invio dei messaggi di direct mailing ai profili.

* **[!UICONTROL Esclusioni non associate]**: numero di profili esclusi da Adobe Journey Optimizer.

+++

### Motivi di errore {#error-reasons-directmail}

La tabella **[!UICONTROL Motivi di errore]** consente di identificare gli errori specifici che si sono verificati durante il processo di invio dei messaggi di direct mailing, semplificando un&#39;analisi approfondita di eventuali problemi riscontrati.

### Motivi di esclusione {#exclude-reasons-directmail}

[](assets/cja-direct-excluded.png)

La tabella **[!UICONTROL Escludi motivi]** mostra visivamente i diversi fattori che hanno portato all&#39;esclusione dei profili utente dal pubblico di destinazione, impedendo loro di ricevere i messaggi di direct mailing.

Per un elenco completo dei motivi di esclusione, consulta [questa pagina](exclusion-list.md).

## Web {#web}

### Tendenza impression e clic {#impressions-web}

![](assets/cja-web-impression.png)

Il grafico **[!UICONTROL Tendenza impression e clic]** presenta un&#39;analisi dettagliata del coinvolgimento dei profili con le pagine Web, fornendo informazioni utili sul modo in cui i profili interagiscono con i contenuti.

+++ Ulteriori informazioni sulle metriche della tendenza Impression &amp; Click

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nelle pagine Web.

* **[!UICONTROL Visualizzazioni]**: numero di volte in cui il messaggio è stato aperto.

+++

### Clic {#clicks-web}

![](assets/cja-web-clicks.png)

Il grafico **[!UICONTROL Clic]** visualizza le metriche di clic delle pagine Web, illustrando sia il numero totale di clic sul contenuto che il numero di profili univoci che hanno fatto clic sul contenuto.

+++ Ulteriori informazioni sulle metriche Clic

* **[!UICONTROL Clic univoci]**: numero di profili che hanno fatto clic su un contenuto nelle pagine Web.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nelle pagine Web.

+++

### Visualizzazioni {#displays-web}

![](assets/cja-web-displays.png)

Il grafico **[!UICONTROL Displays]** ti aiuta a comprendere sia la portata complessiva del messaggio che il numero di profili univoci coinvolti con esso.

+++ Ulteriori informazioni sulle metriche di visualizzazione

* **[!UICONTROL Visualizzazioni]**: numero di volte in cui il messaggio è stato aperto.

* **[!UICONTROL Visualizzazioni univoche]**: il numero di volte in cui il messaggio è stato aperto; non vengono prese in considerazione più interazioni di un profilo.

+++


### Dati di tracciamento {#track-data-web}

![](assets/cja-web-tracking-data.png)

La tabella **[!UICONTROL Dati di tracciamento]** offre un&#39;istantanea dettagliata dell&#39;attività di profilo associata alle pagine Web, fornendo informazioni essenziali sull&#39;efficacia del coinvolgimento e delle pagine Web.

+++ Ulteriori informazioni sul tracciamento delle metriche dei dati

* **[!UICONTROL Persone]**: numero di profili utente qualificati come profili target per le pagine Web.

* **[!UICONTROL Tasso di click-through (CTR)]**: percentuale di utenti che hanno interagito con le pagine Web.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nelle pagine Web.

* **[!UICONTROL Clic univoci]**: numero di profili che hanno fatto clic su un contenuto nelle pagine Web.

* **[!UICONTROL Visualizzazioni]**: numero di volte in cui la pagina Web è stata aperta.

* **[!UICONTROL Visualizzazioni univoche]**: numero di volte in cui la pagina Web è stata aperta, non vengono prese in considerazione più interazioni di un profilo.

+++

### Etichette collegamenti tracciati {#track-link-web}

![](assets/cja-web-tracked-link-labels.png)

La tabella **[!UICONTROL Etichette di collegamento tracciate]** offre una panoramica completa delle etichette di collegamento all&#39;interno delle pagine Web, evidenziando quelle che generano il traffico di visitatori più elevato. Questa funzione ti consente di identificare e assegnare la priorità ai collegamenti più popolari.

+++ Ulteriori informazioni sulle metriche delle etichette dei collegamenti tracciati

* **[!UICONTROL Clic univoci]**: numero di profili che hanno fatto clic su un contenuto nelle pagine Web.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nelle pagine Web.

* **[!UICONTROL Visualizzazioni]**: numero di volte in cui il messaggio è stato aperto.

* **[!UICONTROL Visualizzazioni univoche]**: il numero di volte in cui il messaggio è stato aperto; non vengono prese in considerazione più interazioni di un profilo.

+++

### URL collegamenti tracciati {#track-url-web}

![](assets/cja-web-tracked-link-urls.png)

La tabella **[!UICONTROL URL di collegamento tracciati]** fornisce una panoramica completa degli URL all&#39;interno delle pagine Web che attirano il traffico più elevato di visitatori. Questo consente di identificare e assegnare la priorità ai collegamenti più popolari, migliorando la comprensione del coinvolgimento del profilo con contenuti specifici nelle pagine web.

+++ Ulteriori informazioni sulle metriche degli URL di collegamento tracciati

* **[!UICONTROL Clic univoci]**: numero di profili che hanno fatto clic su un contenuto nelle pagine Web.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nelle pagine Web.

* **[!UICONTROL Visualizzazioni]**: numero di volte in cui il messaggio è stato aperto.

* **[!UICONTROL Visualizzazioni univoche]**: il numero di volte in cui il messaggio è stato aperto; non vengono prese in considerazione più interazioni di un profilo.

+++

## Scheda contenuto {#content-card}

### Tendenza di visualizzazione e clic {#display-click}

![](assets/content-card-report-1.png)

I grafici **[!UICONTROL Tendenza visualizzazione e clic]** consentono di comprendere sia la portata complessiva del messaggio che il numero di profili univoci coinvolti.

+++ Ulteriori informazioni sulle metriche di visualizzazione e clic

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nella scheda Contenuto.

* **[!UICONTROL Visualizzazioni]**: numero di volte in cui il messaggio è stato aperto.

* **[!UICONTROL Visualizzazioni univoche]**: il numero di volte in cui il messaggio è stato aperto; non vengono prese in considerazione più interazioni di un profilo.

+++

### Dati di tracciamento {#tracking-data}

![](assets/content-card-report-2.png)

La tabella **[!UICONTROL Dati di tracciamento]** offre un&#39;istantanea dettagliata dell&#39;attività di profilo associata alle schede Contenuto, fornendo informazioni essenziali sull&#39;efficacia di questa scheda.

+++ Ulteriori informazioni sul tracciamento delle metriche dei dati

* **[!UICONTROL Persone]**: numero di profili utente qualificati come profili target per le schede Contenuto.

* **[!UICONTROL Tasso di click-through (CTR)]**: percentuale di utenti che hanno interagito con la scheda Contenuto.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nella scheda Contenuto.

* **[!UICONTROL Clic univoci]**: numero di profili che hanno fatto clic su un contenuto nella scheda Contenuto.

* **[!UICONTROL Visualizzazioni]**: numero di volte in cui il messaggio è stato aperto.

* **[!UICONTROL Visualizzazioni univoche]**: il numero di volte in cui il messaggio è stato aperto; non vengono prese in considerazione più interazioni di un profilo.

+++

### Etichette tracciate {#tracked-labels}

La tabella **[!UICONTROL Etichette tracciate]** offre una panoramica completa delle etichette di collegamento all&#39;interno delle schede Contenuto, evidenziando quelle che generano il traffico visitatore più elevato. Questa funzione ti consente di identificare e assegnare la priorità ai collegamenti più popolari.

+++ Ulteriori informazioni sulle metriche delle etichette tracciate

* **[!UICONTROL Clic univoci]**: numero di profili che hanno fatto clic su un contenuto nelle schede Contenuto.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nelle schede Contenuto.

* **[!UICONTROL Visualizzazioni]**: numero di volte in cui il messaggio è stato aperto.

* **[!UICONTROL Visualizzazioni univoche]**: il numero di volte in cui il messaggio è stato aperto; non vengono prese in considerazione più interazioni di un profilo.

+++

