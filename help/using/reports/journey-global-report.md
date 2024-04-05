---
solution: Journey Optimizer
product: journey optimizer
title: Rapporto globale dei percorsi
description: Scopri come utilizzare i dati del rapporto globale del percorso
feature: Reporting, Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: e851646e-4cef-45e8-97c2-a8f4c9d2cc08
source-git-commit: 90b08388d3b43ad8d8cfc7efec119217f531860f
workflow-type: tm+mt
source-wordcount: '4412'
ht-degree: 27%

---

# Rapporto globale dei percorsi {#journey-global-report}

>[!CONTEXTUALHELP]
>id="ajo_journey_global_report"
>title="Rapporto globale dei percorsi"
>abstract="Il rapporto globale dei percorsi consente di misurare l’impatto di un percorso in un periodo di tempo selezionato. Il rapporto è suddiviso in diversi widget che descrivono il successo e gli errori di un percorso. Ogni dashboard di reporting può essere modificata ridimensionando o spostando i widget."

I report globali, accessibili dalla scheda Tutto il tempo, visualizzano gli eventi che si sono verificati almeno due ore fa e coprono gli eventi relativi a un periodo di tempo selezionato. Al confronto, i rapporti live si concentrano sugli eventi che si sono verificati nelle ultime 24 ore, con un intervallo di tempo minimo di due minuti dall’occorrenza dell’evento.

Il rapporto globale del percorso è accessibile direttamente dal percorso con **[!UICONTROL Visualizza rapporto]** pulsante.

![](assets/report_journey.png)

Il percorso **[!UICONTROL Rapporto globale]** La pagina verrà visualizzata con le seguenti schede:

* [Percorso](#journey-global)
* [E-mail](#email-global)
* [Push](#push-global)
* [SMS](#sms-global)
* [In-app](#in-app-global)

Il percorso **[!UICONTROL Rapporto globale]** è diviso in diversi widget che descrivono nel dettaglio il successo e gli errori del percorso. Ogni widget può essere ridimensionato ed eliminato, se necessario. Per ulteriori informazioni, consulta questa [sezione](global-report.md#modify-dashboard).

Per un elenco dettagliato di tutte le metriche disponibili in Adobe Journey Optimizer, consulta [questa pagina](global-report.md#list-of-components-global).

## Scheda percorso {#journey-global}

Dal tuo percorso **[!UICONTROL Rapporto globale]**, il **[!UICONTROL Percorso]** fornisce una visualizzazione chiara dei dati di tracciamento più importanti sul percorso.

### Prestazione percorso {#journey-perfomance}

>[!CONTEXTUALHELP]
>id="ajo_journey_performance"
>title="Prestazione percorso"
>abstract="Il widget Prestazione percorso consente di monitorare visivamente il percorso dei profili di destinazione durante l’avanzamento nel percorso."

![](assets/journey_performance.png)

Il **[!UICONTROL Prestazioni percorso]** Il widget consente di tracciare visivamente la traiettoria dei profili target durante la navigazione nel percorso.

Il conteggio dei profili per un nodo viene aggiornato solo dopo che il profilo ha completato il nodo, non al momento dell’immissione. Ad esempio, un profilo su un **Wait** Il nodo viene conteggiato solo una volta raggiunta la data specificata e usciti dal nodo del profilo.

### Statistiche del percorso {#journey-statistics}

>[!CONTEXTUALHELP]
>id="ajo_journey_statistics"
>title="Statistiche del percorso"
>abstract="Gli indicatori chiave di prestazione (KPI) delle statistiche del percorso fungono da dashboard completo e forniscono un’analisi approfondita delle metriche essenziali correlate al percorso."

![](assets/journey_statistics.png)

Il **[!UICONTROL Statistiche percorso]** Gli indicatori di prestazioni chiave (KPI, Key Performance Indicators) funzionano come un dashboard completo che fornisce un’analisi delle metriche essenziali associate al percorso. Questo include dettagli quali il conteggio del profilo inserito e delle istanze di singoli percorsi non riusciti, offrendo una visione completa dell’efficacia e del livello di coinvolgimento del percorso.

+++ Ulteriori informazioni sulle metriche delle statistiche di Percorso

* **[!UICONTROL Profili immessi]**: numero totale di individui che hanno raggiunto l’evento di ingresso del percorso.

* **[!UICONTROL Profili in uscita]**: numero totale di individui che sono usciti dal percorso.

* **[!UICONTROL Singolo percorso non riuscito]**: numero totale di singoli percorsi non eseguiti correttamente.

+++

### Prestazione dell’azione {#action-performance}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_performance"
>title="Prestazione dell’azione"
>abstract="Il widget Prestazione dell’azione illustra le azioni più riuscite che hanno avuto luogo quando sono state avviate le azioni."

![](assets/journey_action_performance.png)

Il **[!UICONTROL Prestazioni azione]** widget rappresenta le azioni di maggior successo che si sono verificate quando **[!UICONTROL azioni]** sono stati attivati.

### Azioni principali {#top-actions}

>[!CONTEXTUALHELP]
>id="ajo_journey_top_actions"
>title="Azioni principali"
>abstract="La tabella Azioni principali consolida le informazioni indispensabili sulle azioni, offrendo osservazioni concise sulla frequenza e sull’efficacia di ciascuna azione."

![](assets/journey_top_actions.png)

Il **[!UICONTROL Azioni principali]** compila i dati essenziali sul tuo **[!UICONTROL Azioni]**. Fornisce informazioni succinte sulla frequenza e sulle prestazioni di ogni azione.

+++ Ulteriori informazioni sulle metriche Azioni principali

* **[!UICONTROL Azioni eseguite correttamente]**: numero totale di **[!UICONTROL Azioni]** eseguito correttamente per un percorso.

* **[!UICONTROL Errore nell’azione]**: numero totale di errori che si sono verificati per **[!UICONTROL Azioni]**.

+++

### Motivi di errore delle azioni {#action-error}

>[!CONTEXTUALHELP]
>id="ajo_journey_actions_error_reasons"
>title="Motivi di errore delle azioni"
>abstract="La tabella e il grafico Motivi di errore delle azioni forniscono un riepilogo dettagliato degli errori riscontrati durante l’esecuzione delle azioni, offrendo una panoramica completa dei problemi che potrebbero verificarsi."

![](assets/journey_action_error.png)

Il **[!UICONTROL Motivi di errore azione]** tabella e grafico offrono una panoramica completa degli errori che si sono verificati durante l’esecuzione **[!UICONTROL Azioni]**.

### Eventi per origine {#events-origin}

>[!CONTEXTUALHELP]
>id="ajo_journey_events_origin"
>title="Eventi per origine"
>abstract="La tabella e i grafici Eventi per origine offrono una visualizzazione della ricezione avvenuta con successo degli eventi. Queste rappresentazioni visive consentono di identificare con precisione gli eventi effettivamente ricevuti, fornendo informazioni valide e approfondite sulla prestazione e sull’impatto di ogni evento all’interno del percorso."

![](assets/journey_events_origin.png)

Il **[!UICONTROL Eventi per origine]** la tabella e i grafici forniscono una prospettiva dettagliata sulla ricezione **[!UICONTROL Eventi]**. Attraverso queste rappresentazioni visive, puoi distinguere con precisione quale **[!UICONTROL Eventi]** sono stati ricevuti in modo efficace, fornendo informazioni preziose sulle prestazioni e sull’impatto dei singoli eventi all’interno del tuo percorso.

### Eventi ricevuti per evento {#events-received}

>[!CONTEXTUALHELP]
>id="ajo_journey_events_received"
>title="Eventi ricevuti per evento"
>abstract="Il grafico Eventi ricevuti per evento consente di identificare e analizzare gli eventi specifici all’interno del percorso che è stato eseguito in modo efficace, fornendo informazioni valide e approfondite sulla prestazione e sui tassi di successo dei singoli eventi."

![](assets/journey_event_received.png)

Il **[!UICONTROL Eventi ricevuti per evento]** grafico consente di identificare e analizzare quali **[!UICONTROL evento]** all’interno del tuo percorso è stato eseguito in modo efficace, fornendo informazioni preziose sulle prestazioni e sui tassi di successo dei singoli eventi.

### Eventi principali {#top-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_top_events"
>title="Eventi principali"
>abstract="La tabella Eventi principali consolida i dati essenziali sugli eventi, offrendo osservazioni concise sia sulla frequenza che sulla prestazione di ogni singolo evento."

![](assets/journey_top_events.png)

Il **[!UICONTROL Eventi principali]** compila i dati essenziali sul tuo **[!UICONTROL Eventi]**. Fornisce informazioni succinte sulla frequenza e sulle prestazioni di ciascuno **[!UICONTROL Evento]**.

### Criteri di consenso {#consent-policies}

>[!CONTEXTUALHELP]
>id="ajo_journey_consent_policies"
>title="Criteri di consenso"
>abstract="La tabella e il grafico Criteri di consenso visualizzano la quantità di profili esclusi da ciascun criterio all’interno delle azioni personalizzate. Questa presentazione offre informazioni approfondite e chiare sull’influenza di ogni criterio di consenso sulle esclusioni del profilo."

![](assets/journey_consent.png)

Il **[!UICONTROL Criteri di consenso]** la tabella e il grafico mostrano il numero di profili esclusi da ciascun criterio all’interno delle azioni personalizzate. Questo fornisce una chiara comprensione dell’impatto di ogni criterio di consenso sulle esclusioni di profilo.

Per ulteriori informazioni sulle azioni personalizzate, consulta [la documentazione dettagliata](../action/about-custom-action-configuration.md).

Tieni presente che affinché questi widget vengano visualizzati nei rapporti Percorsi, dovrai reimpostare le dashboard. A tale scopo, fai clic su **[!UICONTROL Modifica]** allora **[!UICONTROL Reimposta]** nella parte superiore del report.

## Scheda e-mail {#email-global}

Dal tuo percorso **[!UICONTROL Rapporto globale]**, il **[!UICONTROL E-mail]** Questa scheda contiene le informazioni principali relative alle e-mail inviate nel percorso.

### E-mail: statistiche di invio {#email-sending-statistics}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_sending_statistics"
>title="E-mail: statistiche di invio"
>abstract="La tabella della sezione E-mail - Statistiche di invio riepiloga dati essenziali sulle e-mail, ad esempio Target o Consegnati."

![](assets/journey_email_statistics.png)

Il **[!UICONTROL Statistiche di invio e-mail]** La tabella fornisce un riepilogo completo dei dati essenziali relativi alle e-mail nei tuoi percorsi. Descrive le metriche chiave, come la dimensione del pubblico target e il numero di e-mail inviate con successo, fornendo informazioni utili sull’efficacia e la portata delle e-mail e dei percorsi.

+++ Ulteriori informazioni sulle metriche delle statistiche di invio di e-mail

* **[!UICONTROL Tempo di esecuzione]**: ora di inizio di ogni esecuzione del percorso in caso di percorsi ricorrenti. Per eseguire il targeting di una o più ricorrenze, selezionatela dal **[!UICONTROL Tempo di esecuzione]** a discesa.

* **[!UICONTROL Target]**: numero di profili target per qualsiasi azione, ad esempio invio di e-mail o SMS.

* **[!UICONTROL Inviato]**: numero totale di e-mail inviate per il percorso.

* **[!UICONTROL Consegnato]**: numero di e-mail inviate correttamente, in relazione al numero totale di e-mail inviate.

* **[!UICONTROL Percentuale di consegna]**: percentuale di e-mail inviate correttamente.

* **[!UICONTROL Mancati recapiti]**: totale degli errori accumulati durante il processo di invio e l’elaborazione automatica della restituzione in relazione al numero totale di e-mail inviate.

* **[!UICONTROL Percentuale non recapitate]**: percentuale di e-mail non recapitate rispetto alle e-mail inviate.

* **[!UICONTROL Errori]**: numero totale di errori che si sono verificati durante il processo di invio e che ne hanno impedito l’invio ai profili.

* **[!UICONTROL Frequenza errori]**: percentuale di errori che si sono verificati durante il processo di invio e che ne hanno impedito l’invio, rispetto alle e-mail inviate.

* **[!UICONTROL Nuovi tentativi]**: numero di e-mail nella coda per i nuovi tentativi.

* **[!UICONTROL Escluso]**: numero di profili che sono stati esclusi da Adobe Journey Optimizer.

+++

### E-mail - Statistiche di tracciamento {#email-tracking}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_tracking_statistics"
>title="E-mail - Statistiche di tracciamento"
>abstract="La tabella della sezione E-mail - Statistiche di tracciamento e-mail fornisce i dati sulle attività dei profili per l’e-mail."

![](assets/journey_email_tracking.png)

Il **[!UICONTROL E-mail - Statistiche di tracciamento]** la tabella offre un account dettagliato dell’attività del profilo relativa alle e-mail incluse nel percorso. Ciò include metriche su aperture, clic e altri indicatori di coinvolgimento rilevanti, che offrono una visualizzazione completa del modo in cui i profili interagiscono con il contenuto dell’e-mail.

+++ Ulteriori informazioni su E-mail - Metriche delle statistiche di tracciamento

* **[!UICONTROL Tempo di esecuzione]**: ora di inizio di ogni esecuzione dell’e-mail ricorrente nel percorso. Per eseguire il targeting di una o più e-mail ricorrenti, selezionala dall’opzione **[!UICONTROL Tempo di esecuzione]** a discesa.

* **[!UICONTROL Aperture]**: numero di volte in cui le e-mail sono state aperte in un percorso.

* **[!UICONTROL Aperture univoche]**: percentuale di e-mail aperte.

* **[!UICONTROL Percentuale aperture univoche]**: numero totale di e-mail aperte rispetto al numero di e-mail consegnate.

* **[!UICONTROL Clic]**: numero di volte in cui hai fatto clic su un contenuto nelle e-mail.

* **[!UICONTROL Clic univoci]**: numero di destinatari che hanno fatto clic su un contenuto nelle e-mail.

* **[!UICONTROL Percentuale di click-through]**: percentuale di utenti che hanno interagito con il percorso.

* **[!UICONTROL Annullamenti iscrizione]**: numero di clic sul collegamento di annullamento dell’abbonamento.

* **[!UICONTROL Reclami spam]**: numero di volte in cui le e-mail sono state dichiarate come spam o posta indesiderata.

+++

### E-mail: prestazioni di invio {#email-performance}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_sending_performance"
>title="E-mail: prestazioni di invio"
>abstract="Il grafico E-mail: prestazioni di invio presenta dati completi sulle e-mail inviate, fornendo informazioni approfondite sulle metriche chiave, come consegnati e mancati recapiti, e consentendo un’analisi dettagliata del processo di consegna delle e-mail."

![](assets/journey_email_performance.png)

Il **[!UICONTROL E-mail - Prestazioni di invio]** graph fornisce una visualizzazione completa dei dati relativi alle e-mail inviate nel tuo percorso, offrendo informazioni approfondite sulle metriche chiave, quali consegna e mancati recapiti. Ciò consente un’analisi dettagliata del processo di invio delle e-mail, fornendo informazioni preziose sull’efficienza e le prestazioni dei percorsi.

+++ Ulteriori informazioni sull’e-mail - Invio delle metriche delle prestazioni

* **[!UICONTROL Consegnato]**: numero di e-mail inviate correttamente, in relazione al numero totale di e-mail inviate.

* **[!UICONTROL Mancati recapiti]**: totale degli errori accumulati durante il processo di invio e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Nuovi tentativi]**: numero di e-mail nella coda per i nuovi tentativi.

* **[!UICONTROL Errori]**: numero totale di errori che si sono verificati durante un processo di invio e che ne hanno impedito l’invio ai profili.

+++

### E-mail: categorie e motivi di mancato recapito {#email-bounce-categories}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_bounces"
>title="E-mail: categorie e motivi di mancato recapito"
>abstract="I widget E-mail: categorie e motivi di mancato recapito aggregano i dati relativi ai messaggi non recapitati, offrendo informazioni approfondite e dettagliate sui motivi e sulle categorie specifici che contribuiscono ai mancati recapiti delle e-mail"

![](assets/journey_email_bounce_categories.png)

Il **[!UICONTROL Motivi di mancato recapito]** e **[!UICONTROL Categorie di mancato recapito]** I widget compilano i dati disponibili relativi ai messaggi non recapitati, fornendo informazioni dettagliate sui motivi e sulle categorie specifici alla base dei messaggi non recapitati.

Per ulteriori informazioni sui mancati recapiti, consulta [Elenco di soppressione](../reports/suppression-list.md) pagina.

+++ Ulteriori informazioni su E-mail - Metriche delle categorie di mancato recapito

* **[!UICONTROL Mancato recapito permanente]**: numero totale di errori permanenti, ad esempio un indirizzo e-mail errato. Ciò comporta un messaggio di errore che indica esplicitamente che l’indirizzo non è valido, ad esempio Utente sconosciuto.

* **[!UICONTROL Mancato recapito non permanente]**: numero totale di errori temporanei, ad esempio una casella in entrata completa.

* **[!UICONTROL Ignorato]**: numero totale di messaggi temporanei, ad esempio Fuori sede, o un errore tecnico, ad esempio se il tipo di mittente è postmaster.

+++

### E-mail: motivi di errore {#email-errors}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_error_reasons"
>title="E-mail: motivi di errore"
>abstract="I grafici e la tabella della sezione E-mail - Motivi di errore consentono di identificare gli errori specifici che si sono verificati durante l’invio."

![](assets/journey_email_error.png)

Il **[!UICONTROL Motivi di errore]** grafici e tabelle offrono visibilità sugli errori specifici che si sono verificati durante il processo di invio, fornendo informazioni preziose sulla natura e sul verificarsi degli errori.

### E-mail - Motivi di esclusione {#email-excluded}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_excluded_reasons"
>title="E-mail - Motivi di esclusione"
>abstract="I grafici e la tabella della sezione Motivi di esclusione illustrano i vari fattori a causa dei quali il messaggio non è stato ricevuto dai profili utente che sono stati esclusi dal pubblico target."

![](assets/journey_email_excluded.png)

Il **[!UICONTROL Motivi di esclusione]** grafici e tabelle presentano una visione completa dei diversi fattori che hanno determinato l’esclusione dei profili utente dal pubblico di destinazione, causando la mancata ricezione del messaggio.

Fai riferimento a [questa pagina](exclusion-list.md) per l’elenco completo dei motivi di esclusione.

### Inviato e consegnato per dominio {#sent-domains}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_sent_delivered_domains"
>title="Inviato e consegnato per dominio"
>abstract="La tabella e il grafico Inviato e consegnato per domini forniscono un raggruppamento delle e-mail categorizzate per domini, presentando informazioni approfondite e dettagliate sulla prestazione complessiva delle comunicazioni via e-mail."

![](assets/journey_email_sent_domains.png)

Il **[!UICONTROL Inviato e consegnato da domini]** la tabella e il grafico forniscono un raggruppamento dettagliato delle e-mail a livello di dominio, offrendo informazioni complete sulle prestazioni delle e-mail.

+++ Ulteriori informazioni sulle metriche Inviato e Consegnato per domini

* **[!UICONTROL Inviato]**: numero totale di invii per le e-mail.

* **[!UICONTROL Consegnato]**: numero di e-mail inviate correttamente, in relazione al numero totale di e-mail inviate.

+++

### Aperture e clic per domini {#open-domains}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_open_clicks_domains"
>title="Aperture e clic per domini"
>abstract="Il grafico e la tabella Aperture e clic per domini offrono un raggruppamento dettagliato a livello di dominio, presentando una panoramica completa del modo in cui il pubblico si relaziona con le e-mail."

![](assets/journey_email_open_domains.png)

Il **[!UICONTROL Apri e fai clic per domini]** un grafico con una tabella mostra un raggruppamento a livello di dominio del coinvolgimento dei profili con la tua e-mail, fornendo informazioni utili su come diversi domini interagiscono con i contenuti.

+++ Ulteriori informazioni sulle metriche Apri e clic per domini

* **[!UICONTROL Aperture]**: numero di volte in cui l’e-mail è stata aperta.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto in un’e-mail.

+++

### Mancati recapiti ed errori per domini {#bounces-domains}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_bounces_errors_domains"
>title="Mancati recapiti ed errori per domini"
>abstract="Il grafico e la tabella Mancati recapiti ed errori per domini forniscono un raggruppamento dettagliato a livello di dominio, fornendo informazioni approfondite su errori specifici riscontrati durante il processo di invio delle e-mail."

![](assets/journey_email_bounce_domains.png)

Il **[!UICONTROL Mancati recapiti ed errori per domini]** grafico e tabella offrono un raggruppamento a livello di dominio degli errori specifici riscontrati durante il processo di invio, fornendo un’analisi dettagliata dei problemi che si sono verificati.

+++ Ulteriori informazioni su mancati recapiti ed errori per domini e metriche

* **[!UICONTROL Mancati recapiti]**: totale degli errori accumulati durante il processo di invio e l’elaborazione automatica della restituzione in relazione al numero totale di e-mail inviate.

* **[!UICONTROL Errori]**: numero totale di errori che si sono verificati durante il processo di invio e che ne hanno impedito l’invio ai profili.

+++

### Motivi di mancato recapito per dominio {#bounce-reasons-domains}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_bounces_reasons_domains"
>title="Motivi di mancati recapiti per domini"
>abstract="Il grafico e la tabella dei Motivi di mancato recapito per dominio forniscono un raggruppamento a livello di dominio, offrendo informazioni approfondite e complete su errori temporanei e permanenti. Questa analisi dettagliata offre informazioni utili sulle ragioni specifiche alla base dei messaggi non recapitati."

![](assets/journey_email_bounce_reasons_domain.png)

Il **[!UICONTROL Motivi di mancato recapito per dominio]** Il grafico e la tabella forniscono un raggruppamento dei dati a livello di dominio relativi a errori temporanei e permanenti, fornendo informazioni dettagliate sui motivi alla base dei messaggi non recapitati.

### E-mail: URL principale {#email-top}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_top_url"
>title="E-mail: URL principale"
>abstract="Il grafico e la tabella della sezione E-mail - URL principale offrono una panoramica completa degli URL all’interno dell’e-mail che vengono visitati di più, consentendoti di individuare i collegamenti più popolari."

![](assets/journey_email_top.png)

Il **[!UICONTROL E-Mail - URL principale]** Il grafico e la tabella forniscono una panoramica completa degli URL all’interno dell’e-mail che attraggono il traffico di visitatori più elevato. Questo consente di identificare e assegnare la priorità ai collegamenti più popolari, migliorando la comprensione del coinvolgimento del profilo con contenuti specifici nelle e-mail.

### E-mail: ottimizzazione {#email-sto}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_optimization"
>title="E-mail: ottimizzazione"
>abstract="L’ottimizzazione dell’ora di invio e i widget ottimizzati e non ottimizzati forniscono informazioni dettagliate sui messaggi, evidenziando se sono stati ottimizzati o meno."

![](assets/journey_email_sto.png)

>[!NOTE]
>
>Il **[!UICONTROL Ottimizzazione del tempo di invio]** e **[!UICONTROL Ottimizzato e non ottimizzato]** I widget sono disponibili solo se per la consegna è attivata l’opzione Ottimizzazione ora di invio. Per ulteriori informazioni sull’ottimizzazione dell’ora di invio, consulta [questa pagina](../building-journeys/journeys-message.md#send-time-optimization).

Il **[!UICONTROL Ottimizzazione del tempo di invio]** e **[!UICONTROL Ottimizzato e non ottimizzato]** i widget descrivono nel dettaglio il successo delle e-mail a seconda del metodo di invio: ottimizzato o normale.

+++ Ulteriori informazioni sull’ottimizzazione dell’ora di invio e sulle metriche ottimizzate e non ottimizzate

* **[!UICONTROL Consegnato]**: numero di messaggi inviati correttamente rispetto al numero totale di messaggi inviati.
* **[!UICONTROL Mancati recapiti]**: totale degli errori accumulati durante il processo di invio e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Inviato]**: numero totale di e-mail inviate per il percorso.

* **[!UICONTROL Aperture]**: numero di volte in cui le e-mail sono state aperte nel percorso.

* **[!UICONTROL Clic]**: numero di volte in cui hai fatto clic su un contenuto nelle e-mail.

+++

### E-mail: offerte {#email-offers}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_offers"
>title="E-mail: offerte"
>abstract="I widget statistici Statistiche offerte e Dettagli offerte forniscono informazioni complete sulle prestazioni delle offerte, offrendo un’analisi dettagliata del loro impatto nel tempo e presentando statistiche dettagliate per una comprensione più approfondita."

>[!NOTE]
>
>I widget e le metriche delle offerte sono disponibili solo se è stata inserita una decisione in un messaggio e-mail. Per ulteriori informazioni sulla gestione delle decisioni, consulta questa [pagina](../offers/get-started/starting-offer-decisioning.md).

Il **[!UICONTROL Statistica sulle offerte]** e **[!UICONTROL Statistiche dettagliate sulle offerte]** nel tempo, i widget misurano il successo e l’impatto dell’offerta sul pubblico di destinazione. Descrive le informazioni principali relative al messaggio con i KPI.

+++ Ulteriori informazioni su E-mail - Metriche delle offerte

* **[!UICONTROL Offerta inviata]**: numero totale di invii per l’offerta.

* **[!UICONTROL Impression offerta]**: numero di volte in cui l’offerta è stata aperta nelle e-mail.

* **[!UICONTROL Clic sull’offerta]**: numero di volte in cui hai fatto clic su un’offerta nelle e-mail.

* **[!UICONTROL Nome posizionamento]**: nome del posizionamento utilizzato per visualizzare l’offerta. Per ulteriori informazioni sul posizionamento, consulta questa [pagina](../offers/offer-library/creating-placements.md).

* **[!UICONTROL Nome offerta]**: nome dell’offerta aggiunta nelle e-mail. Per ulteriori informazioni sul posizionamento, consulta questa [pagina](../offers/offer-library/creating-personalized-offers.md).

* **[!UICONTROL Offerta inviata]**: numero totale di invii per l’offerta.

* **[!UICONTROL Percentuale di impression offerta]**: percentuale di offerte aperte rispetto al numero di offerte inviate.

* **[!UICONTROL Percentuale di clic dell’offerta]**: percentuale di utenti che hanno interagito con l’offerta.

+++

## Scheda notifica push {#push-global}

Dal tuo percorso **[!UICONTROL Rapporto globale]**, il **[!UICONTROL Notifica push]** La scheda fornisce informazioni dettagliate sulle informazioni principali relative alle notifiche push inviate nel percorso.

### Notifica push: statistiche di invio {#push-sending-stat}

>[!CONTEXTUALHELP]
>id="ajo_journey_push_sending_statistics"
>title="Notifica push: statistiche di invio"
>abstract="La tabella Statistiche di invio delle notifiche push riepiloga i dati essenziali sulle notifiche push, come i messaggi di mirati o recapitati."

![](assets/journey_push_sending.png)

Il **[!UICONTROL Notifica push - Statistiche di invio]** La tabella fornisce un riepilogo sintetico dei dati essenziali relativi alle notifiche push, incluse metriche chiave quali il numero di messaggi target e il numero di messaggi consegnati correttamente.

+++ Ulteriori informazioni sulla notifica push - Metriche delle statistiche di invio

* **[!UICONTROL Tempo di esecuzione]**: ora di inizio di ogni esecuzione del percorso in caso di percorsi ricorrenti. Per eseguire il targeting di una o più ricorrenze, selezionatela dal **[!UICONTROL Tempo di esecuzione]** a discesa.

* **[!UICONTROL Target]**: numero di profili target per qualsiasi azione, ad esempio invio di e-mail o SMS.

* **[!UICONTROL Inviato]**: numero totale di notifiche push inviate.

* **[!UICONTROL Consegnato]**: numero di notifiche push inviate correttamente, in relazione al numero totale di notifiche push inviate.

* **[!UICONTROL Percentuale di consegna]**: percentuale di notifiche push inviate correttamente.

* **[!UICONTROL Mancati recapiti]**: totale degli errori accumulati durante il processo di invio e l’elaborazione automatica della restituzione in relazione al numero totale di notifiche push inviate.

* **[!UICONTROL Percentuale non recapitate]**: percentuale di notifiche push non recapitate rispetto alle notifiche push inviate.

* **[!UICONTROL Errori]**: numero totale di errori che si sono verificati durante il processo di invio e che ne hanno impedito l’invio ai profili.

* **[!UICONTROL Frequenza errori]**: percentuale di errori che si sono verificati durante il processo di invio e ne hanno impedito l’invio, rispetto alle notifiche push inviate.

* **[!UICONTROL Escluso]**: numero di profili che sono stati esclusi da Adobe Journey Optimizer.

+++

### Notifica push: statistiche di tracciamento {#push-tracking-stat}

>[!CONTEXTUALHELP]
>id="ajo_journey_push_tracking_statistics"
>title="Notifica push: statistiche di tracciamento"
>abstract="Le statistiche di tracciamento push forniscono dati sulle attività dei profili per le notifiche push."

Il **[!UICONTROL Push - Statistiche di tracciamento]** widget offre un’istantanea dettagliata dell’attività del profilo associata alle notifiche push, fornendo informazioni essenziali sull’efficacia delle notifiche push e di coinvolgimento.

+++ Ulteriori informazioni sulla notifica push - Metriche delle statistiche di tracciamento

* **[!UICONTROL Tempo di esecuzione]**: ora di inizio di ogni esecuzione del percorso in caso di percorsi ricorrenti. Per eseguire il targeting di una o più ricorrenze, selezionatela dal **[!UICONTROL Tempo di esecuzione]** a discesa.

* **[!UICONTROL Aperture]**: numero di volte in cui le notifiche push sono state aperte nel percorso.

* **[!UICONTROL Azioni]**: numero totale di azioni sulla notifica push consegnata, ad esempio clic su pulsante o rimozione.

+++

### Notifica push: riepilogo di invio {#push-summary}

>[!CONTEXTUALHELP]
>id="ajo_journey_push_sending_summary"
>title="Notifica push: riepilogo di invio"
>abstract="Il grafico Riepilogo invio notifiche push visualizza i dati disponibili per le notifiche push inviate."

![](assets/journey_push_summary.png)

Il **[!UICONTROL Notifica push - Riepilogo di invio]** graph offre una rappresentazione dinamica che mostra un’analisi dell’attività delle notifiche push. Questa rappresentazione grafica fornisce un raggruppamento completo delle notifiche push inviate.

+++ Ulteriori informazioni sulla notifica push - Invio di metriche di riepilogo

* **[!UICONTROL Aperture]**: numero di volte in cui le notifiche push sono state aperte nel percorso.

* **[!UICONTROL Azioni]**: numero totale di azioni sulla notifica push consegnata, ad esempio clic su pulsante o rimozione.

* **[!UICONTROL Mancati recapiti]**: totale degli errori accumulati durante il processo di invio e l’elaborazione automatica della restituzione in relazione al numero totale di notifiche push inviate.

* **[!UICONTROL Consegnato]**: numero di notifiche push inviate correttamente, in relazione al numero totale di notifiche push inviate.

* **[!UICONTROL Errori]**: numero totale di errori che si sono verificati durante il processo di invio e che ne hanno impedito l’invio ai profili.

+++

### Notifica push: motivi di errore {#push-error-reasons}

>[!CONTEXTUALHELP]
>id="ajo_journey_push_error_reasons"
>title="Notifica push: motivi di errore"
>abstract="I grafici e la tabella Motivi di errore consentono di identificare gli errori specifici che si sono verificati durante il processo di invio"

![](assets/journey_push_error.png)

Il **[!UICONTROL Motivi di errore]** tabelle e grafici consentono di identificare gli errori specifici che si sono verificati durante il processo di invio delle notifiche push, fornendo informazioni dettagliate su eventuali problemi riscontrati durante il processo.

### Notifica push: motivi di esclusione {#push-excluded}

>[!CONTEXTUALHELP]
>id="ajo_journey_push_excluded_reasons"
>title="Notifica push: motivi di esclusione"
>abstract="Il grafico e la tabella Motivi di esclusione mostrano le varie cause che hanno impedito ai profili utente, esclusi dal pubblico target, di ricevere il messaggio."

![](assets/journey_push_excluded.png)

Il **[!UICONTROL Motivi di esclusione]** i grafici e le tabelle mostrano i diversi motivi che hanno impedito ai profili utente, esclusi dai profili target, di ricevere le notifiche push.

Fai riferimento a [questa pagina](exclusion-list.md) per l’elenco completo dei motivi di esclusione.

### Notifica push: raggruppamento per piattaforma {#push-breakdown}

>[!CONTEXTUALHELP]
>id="ajo_journey_push_breakdown_platform"
>title="Notifica push: raggruppamento per piattaforma"
>abstract="La tabella e i grafici della Notifica push: raggruppamento per piattaforma forniscono un raggruppamento del successo delle notifiche push in base al sistema operativo del profilo."

![](assets/journey_push_breakdown.png)

Il **[!UICONTROL Raggruppamento per piattaforma]** grafico e tabella forniscono un’analisi dettagliata del successo delle notifiche push, con informazioni basate sul sistema operativo del profilo. Questo raggruppamento migliora la comprensione delle prestazioni delle notifiche push tra le diverse piattaforme.

### Notifica push - Ottimizzazione {#push-sto}

>[!NOTE]
>
>Il **[!UICONTROL Ottimizzato e non ottimizzato]** e **[!UICONTROL Ottimizzazione del tempo di invio]** I widget sono disponibili solo se per la consegna è attivata l’opzione Ottimizzazione ora di invio. Per ulteriori informazioni sull’ottimizzazione dell’ora di invio, consulta [questa pagina](../building-journeys/journeys-message.md#send-time-optimization).

Il **[!UICONTROL Ottimizzato e non ottimizzato]** e **[!UICONTROL Ottimizzazione del tempo di invio]** i widget descrivono nel dettaglio le informazioni principali relative al messaggio, ottimizzate o meno.

+++ Ulteriori informazioni sulla notifica push: metriche di ottimizzazione

* **[!UICONTROL Consegnato]**: numero di messaggi inviati correttamente rispetto al numero totale di messaggi inviati.

* **[!UICONTROL Aperture]**: numero di volte in cui le notifiche push sono state aperte nel percorso.

* **[!UICONTROL Azioni]**: numero totale di azioni sulla notifica push consegnata, ad esempio clic su pulsante o rimozione.

* **[!UICONTROL Consegnato]**: numero di messaggi inviati correttamente rispetto al numero totale di messaggi inviati.

* **[!UICONTROL Mancati recapiti]**: totale degli errori accumulati durante il processo di invio e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

+++

## Scheda SMS {#sms-global}

### SMS: statistiche di invio {#sms-sending-stat}

>[!CONTEXTUALHELP]
>id="ajo_journey_sms_sending_statistics"
>title="SMS: statistiche di invio"
>abstract="La tabella SMS: statistiche di invio riepiloga i dati essenziali sui messaggi SMS, ad esempio i messaggi mirati o recapitati."

![](assets/journey_sms_sending.png)

Il **[!UICONTROL SMS - Statistiche di invio]** La tabella fornisce un riepilogo conciso dei dati essenziali relativi ai messaggi SMS, includendo metriche chiave quali il numero di messaggi target e il numero di messaggi consegnati correttamente.

+++ Ulteriori informazioni sugli SMS - Metriche delle statistiche di invio

* **[!UICONTROL Tempo di esecuzione]**: ora di inizio di ogni esecuzione del percorso in caso di percorsi ricorrenti. Per eseguire il targeting di una o più ricorrenze, selezionatela dal **[!UICONTROL Tempo di esecuzione]** a discesa.

* **[!UICONTROL Target]**: numero di profili utente qualificati come profili target per i messaggi SMS.

* **[!UICONTROL Escluso]**: numero di profili utente, esclusi dai profili target, che non hanno ricevuto i messaggi SMS.

* **[!UICONTROL Inviato]**: numero totale di messaggi SMS inviati per il percorso.

* **[!UICONTROL Mancati recapiti]**: totale degli errori accumulati durante il processo di invio e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi SMS inviati.

* **[!UICONTROL Errori]**: numero totale di errori che si sono verificati durante il processo di invio e che ne hanno impedito l’invio ai profili.

+++

### SMS: statistiche di tracciamento {#sms-tracking-stat}

>[!CONTEXTUALHELP]
>id="ajo_journey_sms_tracking_statistics"
>title="SMS: statistiche di tracciamento"
>abstract="Il widget SMS: statistiche di tracciamento fornisce una panoramica completa delle informazioni essenziali relative all’interazione dei visitatori con l’URL."

![](assets/journey_sms_tracking.png)

Il **[!UICONTROL SMS - Statistiche di tracciamento]** Il widget fornisce una panoramica dettagliata delle informazioni chiave relative al coinvolgimento dei visitatori con gli URL, fornendo informazioni sull’efficacia dei messaggi SMS.

* **[!UICONTROL Tempo di esecuzione]**: ora di inizio di ogni esecuzione dell’SMS ricorrente. Per eseguire il targeting di uno o più SMS ricorrenti, selezionali dall’elenco **[!UICONTROL Tempo di esecuzione]** a discesa.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nei messaggi SMS.

### SMS: prestazione per data {#sms-performance-date}

>[!CONTEXTUALHELP]
>id="ajo_journey_sms_perfomance_date"
>title="SMS: prestazione per data"
>abstract="Il widget Prestazioni SMS per data fornisce informazioni chiave sui messaggi tramite una rappresentazione grafica."

![](assets/journey_sms_performance.png)

Il **[!UICONTROL SMS - Prestazioni per data]** Il widget offre una panoramica dettagliata delle informazioni chiave relative ai messaggi, presentate tramite un grafico, che fornisce informazioni sulle tendenze delle prestazioni in periodi di tempo specifici.

+++ Ulteriori informazioni sugli SMS - Metriche delle prestazioni per data

* **[!UICONTROL Inviato]**: numero totale di messaggi SMS inviati per il percorso

* **[!UICONTROL Mancati recapiti]**: totale degli errori accumulati durante il processo di invio e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi SMS inviati.

* **[!UICONTROL Errori]**: numero totale di errori che si sono verificati durante il processo di invio e che ne hanno impedito l’invio ai profili.

+++

### SMS: motivi di mancato recapito {#sms-bounce}

>[!CONTEXTUALHELP]
>id="ajo_journey_sms_bounces_reasons"
>title="SMS: motivi di mancato recapito"
>abstract="I grafici e la tabella Motivi di mancato recapito contengono i dati disponibili relativi ai messaggi non recapitati."

![](assets/journey_sms_bounce_reasons.png)

Il **[!UICONTROL Motivi di mancato recapito]** I grafici e le tabelle forniscono una panoramica completa dei dati relativi ai messaggi SMS non recapitati, fornendo informazioni utili sulle ragioni specifiche alla base delle istanze di messaggi SMS non recapitati.

### SMS: motivi di errore {#sms-error}

>[!CONTEXTUALHELP]
>id="ajo_journey_sms_error_reasons"
>title="SMS: motivi di errore"
>abstract="I grafici e la tabella della sezione SMS - Motivi di errore consentono di individuare gli errori specifici che si sono verificati durante il processo di invio."

![](assets/journey_sms_error.png)

Il **[!UICONTROL Motivi di errore]** I grafici e le tabelle ti consentono di identificare gli errori specifici che si sono verificati durante il processo di invio dei messaggi SMS, semplificando un’analisi approfondita di eventuali problemi riscontrati.

### SMS: motivi di esclusione {#sms-excluded}

>[!CONTEXTUALHELP]
>id="ajo_journey_sms_excluded_reasons"
>title="SMS: motivi di esclusione"
>abstract="I grafici e la tabella dei motivi di esclusione illustrano i vari fattori che hanno portato ai profili utente, esclusi dal pubblico mirato, a non ricevere il messaggio."

![](assets/journey_sms_excluded.png)

Il **[!UICONTROL Motivi di esclusione]** I grafici e le tabelle illustrano visivamente i diversi fattori che hanno portato all’esclusione dei profili utente dal pubblico di destinazione, impedendo loro di ricevere i messaggi SMS.

Fai riferimento a [questa pagina](exclusion-list.md) per l’elenco completo dei motivi di esclusione.

### SMS: clic per collegamenti {#sms-clicks}

>[!CONTEXTUALHELP]
>id="ajo_journey_sms_clicks"
>title="SMS: clic per collegamenti"
>abstract="Il widget SMS: clic per collegamenti fornisce informazioni approfondite essenziali sul coinvolgimento dei visitatori con gli URL nei messaggi."

![](assets/journey_sms_clicks.png)

Il **[!UICONTROL SMS - Clic per collegamenti]** widget offre informazioni essenziali sul coinvolgimento dei visitatori con gli URL inclusi nei messaggi, fornendo informazioni preziose su quali collegamenti attraggono maggiormente l’interazione.

## Scheda in-app {#in-app-global}

Dal tuo Percorso **[!UICONTROL Rapporto globale]**, il **[!UICONTROL In-app]** Questa scheda contiene le informazioni principali relative ai messaggi in-app inviati nei tuoi percorsi.

### Prestazione in-app {#inapp-performance}

>[!CONTEXTUALHELP]
>id="ajo_journey_inapp_performance"
>title="Prestazione in-app"
>abstract="I KPI (Key Performance Indicator) in-app forniscono informazioni essenziali sul coinvolgimento dei visitatori con i messaggi in-app."

![](assets/journey_inapp_performance.png)

Il **[!UICONTROL Prestazioni in-app]** I KPI forniscono informazioni essenziali sul coinvolgimento dei profili con i messaggi in-app, fornendo metriche essenziali per valutare l’efficacia e l’impatto dei messaggi in-app inclusi nel percorso.

+++ Ulteriori informazioni su In-app - Metriche delle prestazioni per data

* **[!UICONTROL Impression univoche]**: numero di utenti univoci a cui è stato visualizzato il messaggio in-app.

* **[!UICONTROL Impression]**: numero totale di messaggi in-app visualizzati a tutti gli utenti.

  >[!NOTE]
  >
  >Per garantire il conteggio di un’impression, l’utente deve soddisfare due criteri:
  >* Qualifica nell’esperienza in-app, ottenuta raggiungendo l’attività in-app specifica nel proprio percorso.
  >* Soddisfa le condizioni specificate nelle regole di attivazione.
  > 
  >A causa del secondo criterio, potrebbero esserci variazioni notevoli tra il numero di profili target e il conteggio di impression univoche.

* **[!UICONTROL Interazione]**: numero di accordi con il messaggio in-app. Ciò include tutte le azioni intraprese dagli utenti, come clic, revoche o qualsiasi altra interazione.
+++

### Riepilogo in-app {#inapp-summary}

>[!CONTEXTUALHELP]
>id="ajo_journey_inapp_summary"
>title="Riepilogo in-app"
>abstract="Il grafico di riepilogo in-app illustra la progressione delle impression e delle interazioni in-app nel periodo specificato."

![](assets/journey_inapp_summary.png)

Il **[!UICONTROL Riepilogo in-app]** Il grafico illustra la progressione delle impression e delle interazioni in-app nel periodo specificato, fornendo una panoramica completa delle prestazioni dei messaggi in-app.

### Interazioni per tipo {#interactions-type}

>[!CONTEXTUALHELP]
>id="ajo_journey_inapp_interactions"
>title="Interazioni per tipo"
>abstract="Le Interazioni per tipo rappresentano grafici e tabelle che descrivono il modo in cui gli utenti hanno interagito con il messaggio in-app tracciando eventuali clic, eliminazioni o interazioni."

![](assets/journey_inapp_interactions.png)

Il **[!UICONTROL Interazioni per tipo]** grafici e tabelle forniscono un resoconto dettagliato del modo in cui i profili interagivano con il messaggio in-app, le azioni di tracciamento come clic, licenziamenti o qualsiasi altra forma di coinvolgimento.
