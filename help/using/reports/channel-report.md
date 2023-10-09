---
solution: Journey Optimizer
product: journey optimizer
title: Rapporti a livello di canale
description: Scopri come utilizzare i dati dei rapporti sul canale
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: ead9359b-cdab-43ed-a469-d98b0ca19a17
source-git-commit: 6bceccc561daac594f5c84d3d3250d887a349b7b
workflow-type: tm+mt
source-wordcount: '2664'
ht-degree: 3%

---

# Rapporti sul canale {#channel-report}

>[!CONTEXTUALHELP]
>id="ajo_channel_level_report"
>title="Rapporto a livello di canale"
>abstract="I rapporti sul canale offrono una panoramica completa delle metriche del traffico e del coinvolgimento su tutti i canali. I rapporti sono suddivisi in diversi widget che descrivono nel dettaglio i successi e gli errori della campagna e dei percorsi. Ogni dashboard di reporting può essere modificata ridimensionando o spostando i widget."

>[!IMPORTANT]
>
> Per accedere al menu **Rapporto**, è necessario disporre dell’autorizzazione **[!UICONTROL Visualizza rapporti sui canali.]** [Ulteriori informazioni](channel-report-gs.md#before-starting-manage-reports-prereq)

I rapporti sul canale forniscono agli utenti una panoramica completa delle metriche del traffico e del coinvolgimento a livello di canale. Le metriche vengono aggregate per presentare valori consolidati per le azioni provenienti dal canale scelto, che si estendono su vari percorsi e campagne.

Puoi accedere ai rapporti sul canale navigando su **Rapporti** menu all&#39;interno di **Gestione percorso** sezione. È completamente personalizzabile, puoi filtrare i dati a seconda della data del rapporto o dell’azione. [Ulteriori informazioni](channel-report-gs.md)

La pagina del rapporto viene visualizzata con le seguenti schede:

* [E-mail](#email)
* [Notifiche push](#push)
* [SMS](#sms)
* [In-app](#inapp)
* [Web](#web)
* [Direct mail](#direct-mail)

➡️ [Scopri questa funzione nel video](#channel-report-video)

## E-mail {#email}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_sending_statistics"
>title="E-mail - Statistiche di invio totali"
>abstract="I KPI E-mail - Statistiche di invio totali riepilogano i dati essenziali sulle notifiche push, come i messaggi di destinazione o recapitati."

>[!CONTEXTUALHELP]
>id="ajo_channel_email_tracking_statistics"
>title="E-mail - Statistiche di tracciamento totali"
>abstract="I KPI E-mail - Statistiche di tracciamento totali forniscono dati sull’attività del profilo per le e-mail."

>[!CONTEXTUALHELP]
>id="ajo_channel_email_sending_statistics_overtime"
>title="E-mail - Statistiche di invio nel tempo"
>abstract="Il grafico E-mail - Statistiche di invio nel tempo presenta i dati relativi alle e-mail inviate, suddivisi su base oraria, giornaliera, settimanale o mensile."

>[!CONTEXTUALHELP]
>id="ajo_channel_email_tracking_statistics_overtime"
>title="E-mail - Statistiche di tracciamento nel tempo"
>abstract="Il grafico E-mail - Tracciamento delle statistiche nel tempo fornisce dati sull’attività del profilo per le e-mail, suddivisi su base oraria, giornaliera, settimanale o mensile."

>[!CONTEXTUALHELP]
>id="ajo_channel_email_bounce_categories"
>title="Categorie di mancato recapito"
>abstract="I grafici e la tabella delle categorie di mancato recapito forniscono dati sugli errori temporanei e permanenti."

>[!CONTEXTUALHELP]
>id="ajo_channel_email_bounce_reasons"
>title="Motivi di mancato recapito"
>abstract="I grafici e la tabella Motivi di mancato recapito contengono i dati disponibili relativi ai messaggi non recapitati."

>[!CONTEXTUALHELP]
>id="ajo_channel_email_error_reasons"
>title="Motivi di errore"
>abstract="I grafici e la tabella Motivi di errore consentono di identificare gli errori specifici che si sono verificati durante il processo di invio."

>[!CONTEXTUALHELP]
>id="ajo_channel_email_excluded_reasons"
>title="Motivi di esclusione"
>abstract="I grafici e la tabella dei motivi di esclusione illustrano i vari fattori che hanno portato ai profili utente, esclusi dal pubblico di destinazione, a non ricevere il messaggio."

>[!CONTEXTUALHELP]
>id="ajo_channel_email_sending_delivered_domains"
>title="Inviato e consegnato da domini"
>abstract="Il grafico e la tabella Inviato e consegnato da domini rappresentano il raggruppamento a livello di dominio di ogni dato importante relativo all’invio di e-mail."

>[!CONTEXTUALHELP]
>id="ajo_channel_email_bounces_errors_domains"
>title="Mancati recapiti ed errori per domini"
>abstract="Il grafico e la tabella Mancati recapiti ed errori per domini rappresentano il raggruppamento a livello di dominio degli errori specifici che si sono verificati durante il processo di invio."

>[!CONTEXTUALHELP]
>id="ajo_channel_email_open_clicks_domains"
>title="Apri e fai clic per domini"
>abstract="Il grafico e la tabella Apri e clic per domini rappresentano il raggruppamento a livello di dominio del coinvolgimento dei visitatori con la tua e-mail."

>[!CONTEXTUALHELP]
>id="ajo_channel_email_bounce_reasons_domains"
>title="Motivi di mancato recapito per dominio"
>abstract="Il grafico e la tabella Motivi di mancato recapito per dominio rappresentano il raggruppamento a livello di dominio dei dati su errori temporanei e permanenti."

Dai rapporti sul canale, il menu E-mail fornisce i dettagli delle informazioni principali relative alle e-mail inviate nelle campagne e nei Percorsi. Le metriche sono descritte di seguito.

![](assets/email_channel_1.png)

+++ Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto e-mail.

Il **[!UICONTROL Statistiche di invio totali e-mail]** Il grafico descrive il successo delle e-mail:

* **[!UICONTROL Target]**: numero totale di e-mail elaborate.

* **[!UICONTROL Inviato]**: numero totale di invii.

* **[!UICONTROL Consegnato]**: numero di e-mail inviate correttamente, in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Percentuale di consegna]**: percentuale di e-mail inviate correttamente.

* **[!UICONTROL Mancati recapiti]**: totale degli errori accumulati e dell’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Percentuale non recapitate]**: percentuale di e-mail non recapitate rispetto alle e-mail inviate.

* **[!UICONTROL Errori]**: numero totale di errori che ne hanno impedito l’invio ai profili.

* **[!UICONTROL Frequenza errori]**: percentuale di errori che ne hanno impedito l’invio rispetto alle e-mail inviate.

* **[!UICONTROL Escluso]**: numero di profili che sono stati esclusi da Adobe Journey Optimizer.

* **[!UICONTROL Percentuale di esclusione]**: percentuale di profili che sono stati esclusi da Adobe Journey Optimizer.

Il **[!UICONTROL Statistiche di tracciamento del totale delle e-mail]** Il widget contiene i dati disponibili per l’attività profilo per le e-mail:

* **[!UICONTROL Aperture]**: numero di volte in cui il messaggio è stato aperto.

* **[!UICONTROL Percentuale aperture]**: numero totale di e-mail aperte rispetto al numero di e-mail consegnate.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto in un messaggio.

* **[!UICONTROL Percentuale di clic]**: percentuale di utenti che hanno interagito con l’e-mail.

* **[!UICONTROL Reclami spam]**: numero di volte in cui un messaggio è stato dichiarato come spam o posta indesiderata.

* **[!UICONTROL Percentuale reclami spam]**: percentuale di messaggi dichiarati come spam o posta indesiderata rispetto al numero di e-mail inviate.

* **[!UICONTROL Annulla iscrizione]**: numero di clic sul collegamento di abbonamento.

* **[!UICONTROL Percentuale di annullamento abbonamento]**: percentuale di annullamento dell’abbonamento rispetto al numero di e-mail inviate.

Il **[!UICONTROL Invio di statistiche nel tempo]** il grafico contiene i dati disponibili per le e-mail inviate, ad esempio:

* **[!UICONTROL Inviato]**: numero totale di invii.

* **[!UICONTROL Consegnato]**: numero di e-mail inviate correttamente, in relazione al numero totale di e-mail inviate.

* **[!UICONTROL Mancati recapiti]**: totale degli errori cumulativi e dell’elaborazione automatica della restituzione in relazione al numero totale di e-mail inviate.

* **[!UICONTROL Errori]**: numero totale di errori che ne hanno impedito l’invio ai profili.

Il **[!UICONTROL Statistiche di tracciamento e-mail nel tempo]** il grafico contiene i dati disponibili per le aperture e i clic.

Il **[!UICONTROL Motivi di mancato recapito]** e **[!UICONTROL Categorie di mancato recapito]** I widget contengono i dati disponibili relativi ai messaggi non recapitati, ad esempio:

* **[!UICONTROL Mancato recapito permanente]**: numero totale di errori permanenti, ad esempio un indirizzo e-mail errato. Ciò comporta un messaggio di errore che indica esplicitamente che l’indirizzo non è valido, ad esempio Utente sconosciuto.

* **[!UICONTROL Mancato recapito non permanente]**: numero totale di errori temporanei, ad esempio una casella in entrata completa.

* **[!UICONTROL Ignorato]**: numero totale di messaggi temporanei, ad esempio Fuori sede, o un errore tecnico, ad esempio se il tipo di mittente è postmaster.

Per ulteriori informazioni sui mancati recapiti, consulta [Elenco di soppressione](../reports/suppression-list.md) pagina.

Il **[!UICONTROL Motivi di errore]** grafico e tabella consentono di vedere quale errore si è verificato.

Il **[!UICONTROL Motivi di esclusione]** il grafico e la tabella mostrano i diversi motivi che hanno impedito ai profili utente, esclusi dai profili target, di ricevere il messaggio.

Il **[!UICONTROL Motivi di mancato recapito per dominio]**, **[!UICONTROL Inviato e consegnato da domini]**, **[!UICONTROL Aperture e clic per dominio]**  e **[!UICONTROL Mancato recapito ed errori per dominio]** tabelle e grafici rappresentano il raggruppamento a livello di dominio di ogni importante consegna e-mail e dati di tracciamento.
+++

## Notifica push {#push}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_sending_statistics"
>title="Notifiche push - Statistiche di invio totali"
>abstract="I KPI per le notifiche push - Statistiche di invio totali riepilogano i dati essenziali sulle notifiche push, come Destinato o Consegnato."

>[!CONTEXTUALHELP]
>id="ajo_channel_push_tracking_statistics"
>title="Notifica push - Statistiche di tracciamento totali"
>abstract="Le statistiche di tracciamento notifica push - Totale forniscono dati sull’attività del profilo per le notifiche push."

>[!CONTEXTUALHELP]
>id="ajo_channel_push_sending_statistics_overtime"
>title="Notifiche push - Statistiche di invio nel tempo"
>abstract="Il grafico Invio di notifiche push con statistiche nel tempo presenta i dati relativi alle notifiche push inviate, suddivisi su base oraria, giornaliera, settimanale o mensile."

>[!CONTEXTUALHELP]
>id="ajo_channel_push_tracking_statistics_overtime"
>title="Notifiche push - Tracciamento delle statistiche nel tempo"
>abstract="Il grafico Notifiche push - Tracciamento delle statistiche nel tempo fornisce dati sull’attività del profilo per le notifiche push, suddivisi su base oraria, giornaliera, settimanale o mensile."

>[!CONTEXTUALHELP]
>id="ajo_channel_push_excluded_reasons"
>title="Motivi di esclusione"
>abstract="I grafici e la tabella dei motivi di esclusione illustrano i vari fattori che hanno portato ai profili utente, esclusi dal pubblico di destinazione, a non ricevere il messaggio."

>[!CONTEXTUALHELP]
>id="ajo_channel_push_error_reasons"
>title="Motivi di errore"
>abstract="I grafici e la tabella Motivi di errore consentono di identificare gli errori specifici che si sono verificati durante il processo di invio."

>[!CONTEXTUALHELP]
>id="ajo_channel_push_tracking_statistics_platform"
>title="Statistiche di tracciamento per piattaforma"
>abstract="Le statistiche di tracciamento per grafico e tabella della piattaforma forniscono dati sull’attività del profilo per le notifiche push a seconda del sistema operativo del profilo."

>[!CONTEXTUALHELP]
>id="ajo_channel_push_sending_statistics_platform"
>title="Statistiche di invio per piattaforma"
>abstract="Le statistiche di invio per grafico e tabella della piattaforma presentano i dati relativi alle notifiche push inviate."

Dai rapporti sul canale, il menu Notifica push fornisce i dettagli delle informazioni principali relative alle notifiche push inviate nelle campagne e nei Percorsi. Le metriche sono descritte di seguito.

![](assets/push_channel_1.png)

+++  Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto push.

Il **[!UICONTROL Notifiche push - Statistiche di invio totali]** la tabella descrive le informazioni principali relative alle notifiche push con grafico e KPI:

* **[!UICONTROL Target]**: numero totale di notifiche push elaborate.

* **[!UICONTROL Inviato]**: numero totale di notifiche push inviate.

* **[!UICONTROL Consegnato]**: numero di notifiche push inviate correttamente, in relazione al numero totale di notifiche push inviate.

* **[!UICONTROL Percentuale di consegna]**: percentuale di notifiche push inviate correttamente.

* **[!UICONTROL Mancati recapiti]**: totale degli errori accumulati e dell’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Percentuale non recapitate]**: percentuale di notifiche push non recapitate rispetto alle notifiche push inviate.

* **[!UICONTROL Errori]**: numero totale di errori che ne hanno impedito l’invio ai profili.

* **[!UICONTROL Frequenza errori]**: percentuale di errori che ne hanno impedito l’invio rispetto alle notifiche push inviate.

* **[!UICONTROL Escluso]**: numero di profili che sono stati esclusi da Adobe Journey Optimizer.

* **[!UICONTROL Percentuale di esclusione]**: percentuale di profili che sono stati esclusi da Adobe Journey Optimizer.

Il **[!UICONTROL Notifica push - Statistiche di tracciamento totali]** contiene i dati disponibili per l’attività profilo per le notifiche push:

* **[!UICONTROL Aperture]**: numero di volte in cui è stata aperta una notifica push.

* **[!UICONTROL Percentuale aperture]**: percentuale di notifiche push aperte.

* **[!UICONTROL Azioni]**: numero totale di azioni sulla notifica push consegnata, ad esempio clic su pulsante o rimozione.

* **[!UICONTROL Percentuale azioni]**: percentuale di azioni sulla notifica push consegnata rispetto alle notifiche push inviate.

* **[!UICONTROL Tasso di coinvolgimento]**: percentuale di aperture e azioni per questa notifica push, ovvero se il profilo ha aperto la notifica push o se è stato fatto clic su un pulsante.

Il **[!UICONTROL Notifiche push - Statistiche di invio nel tempo]** il grafico contiene i dati disponibili per le notifiche push inviate, ad esempio:

* **[!UICONTROL Inviato]**: numero totale di notifiche push inviate.

* **[!UICONTROL Consegnato]**: numero di notifiche push inviate correttamente, in relazione al numero totale di notifiche push inviate.

* **[!UICONTROL Mancati recapiti]**: totale degli errori accumulati e dell’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Errori]**: numero totale di errori che ne hanno impedito l’invio ai profili.

Il **[!UICONTROL Motivi di esclusione]** il grafico e la tabella mostrano i diversi motivi che hanno impedito ai profili utente, esclusi dai profili target, di ricevere il messaggio.

Il **[!UICONTROL Motivi di errore]** grafico e tabella consentono di vedere quale errore si è verificato.

Il **[!UICONTROL Tracciamento per piattaforma]** e **[!UICONTROL Invio per piattaforma]** grafici e tabelle descrivono in dettaglio il successo della notifica push in base al sistema operativo del profilo.
+++

## SMS {#sms}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_sending_statistics"
>title="SMS - Statistiche di invio totali"
>abstract="I KPI SMS - Statistiche di invio totali riepilogano dati essenziali sui messaggi SMS come Target o Delivered."

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_tracking_statistics"
>title="SMS - Statistiche di tracciamento totali"
>abstract="Le statistiche di tracciamento SMS - Totale forniscono dati sull’attività del profilo per i messaggi SMS."

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_sending_statistics_overtime"
>title="SMS - Statistiche di invio nel tempo"
>abstract="Il grafico SMS - Statistiche di invio nel tempo presenta i dati relativi ai messaggi SMS inviati, suddivisi su base oraria, giornaliera, settimanale o mensile."

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_tracking_statistics_overtime"
>title="SMS - Statistiche di tracciamento nel tempo"
>abstract="Il grafico SMS - Tracciamento statistiche nel tempo fornisce dati sull’attività del profilo per i messaggi SMS, suddivisi su base oraria, giornaliera, settimanale o mensile."

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_excluded_reasons"
>title="Motivi di esclusione"
>abstract="I grafici e la tabella dei motivi di esclusione illustrano i vari fattori che hanno portato ai profili utente, esclusi dal pubblico di destinazione, a non ricevere il messaggio."

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_bounce_reasons"
>title="Motivi di mancato recapito"
>abstract="I grafici e la tabella Motivi di mancato recapito contengono i dati disponibili relativi ai messaggi non recapitati."

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_error_reasons"
>title="Motivi di errore"
>abstract="I grafici e la tabella Motivi di errore consentono di identificare gli errori specifici che si sono verificati durante il processo di invio."

Dai rapporti sul canale, il menu SMS fornisce i dettagli delle informazioni principali relative agli SMS inviati nelle campagne e nei Percorsi. Le metriche sono descritte di seguito.

![](assets/sms_channel_1.png)

+++ Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto SMS.

Il **[!UICONTROL SMS - Statistiche di invio totali]** la tabella descrive il successo del tuo SMS:

* **[!UICONTROL Target]**: numero di profili utente qualificati come profili target per il canale SMS.

* **[!UICONTROL Inviato]**: numero totale di messaggi SMS inviati.

* **[!UICONTROL Consegnato]**: numero di messaggi SMS inviati correttamente, in relazione al numero totale di messaggi SMS inviati.

* **[!UICONTROL Percentuale di consegna]**: percentuale di messaggi SMS inviati correttamente.

* **[!UICONTROL Mancati recapiti]**: totale degli errori accumulati e dell’elaborazione automatica della restituzione in relazione al numero totale di messaggi SMS inviati.

* **[!UICONTROL Percentuale non recapitate]**: percentuale di messaggi SMS non recapitati rispetto ai messaggi SMS inviati.

* **[!UICONTROL Errori]**: numero totale di errori che ne hanno impedito l’invio ai profili.

* **[!UICONTROL Frequenza errori]**: percentuale di errori che ne impedivano l’invio rispetto ai messaggi SMS inviati.

* **[!UICONTROL Escluso]**: numero di profili utente, esclusi dai profili target, che non hanno ricevuto il messaggio.

* **[!UICONTROL Percentuale di esclusione]**: percentuale di profili che sono stati esclusi da Adobe Journey Optimizer.

Il **[!UICONTROL SMS - Statistiche di tracciamento totali]** widget descrive le informazioni principali relative al coinvolgimento dei visitatori con gli URL:

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nel messaggio SMS.

* **[!UICONTROL Percentuale di clic]**: percentuale di utenti che hanno interagito con il messaggio SMS.

Il **[!UICONTROL SMS - Statistiche di invio nel tempo]** un grafico fornisce dettagli sulle informazioni principali relative al messaggio:

* **[!UICONTROL Inviato]**: numero totale di messaggi SMS inviati.

* **[!UICONTROL Consegnato]**: numero di messaggi SMS inviati correttamente, in relazione al numero totale di messaggi SMS inviati.

* **[!UICONTROL Mancati recapiti]**: totale degli errori accumulati e dell’elaborazione automatica della restituzione in relazione al numero totale di messaggi SMS inviati.

* **[!UICONTROL Errori]**: numero totale di errori che ne hanno impedito l’invio ai profili.

Il **[!UICONTROL Escludi motivi]**, **[!UICONTROL Motivi di mancato recapito]** e **[!UICONTROL Motivi di errore]** grafici e tabelle consentono di vedere quali errori ed esclusioni si sono verificati.

+++

## Direct mail {#direct-mail}

>[!CONTEXTUALHELP]
>id="ajo_channel_direct_sending_statistics"
>title="Direct mailing - Statistiche di invio totali"
>abstract="I KPI per le statistiche di invio Direct mailing - Totale riepilogano i dati essenziali relativi ai messaggi di direct mailing, ad esempio Destinato o Consegnato."

>[!CONTEXTUALHELP]
>id="ajo_channel_direct_excluded_reasons"
>title="Motivi di esclusione"
>abstract="I grafici e la tabella dei motivi di esclusione illustrano i vari fattori che hanno portato ai profili utente, esclusi dal pubblico di destinazione, a non ricevere il messaggio."

>[!CONTEXTUALHELP]
>id="ajo_channel_direct_error_reasons"
>title="Motivi di errore"
>abstract="I grafici e la tabella Motivi di errore consentono di identificare gli errori specifici che si sono verificati durante il processo di invio."

Dai rapporti sul canale, il menu Direct mailing fornisce i dettagli delle informazioni principali relative ai messaggi di direct mailing inviati nelle campagne e nei Percorsi. Le metriche sono descritte di seguito.

![](assets/direct_mail_channel_1.png)

+++ Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto Direct mail.

Il **[!UICONTROL Direct mailing - Statistiche di invio totali]** la tabella descrive il successo dei messaggi:

* **[!UICONTROL Target]**: numero di profili utente idonei come profili target per i messaggi Direct mail.

* **[!UICONTROL Inviato]**: numero totale di invii.

* **[!UICONTROL Errori]**: numero totale di errori che ne hanno impedito l’invio ai profili.

* **[!UICONTROL Frequenza errori]**: percentuale di errori che ne hanno impedito l’invio rispetto alle notifiche push inviate.

* **[!UICONTROL Escluso]**: numero di profili utente, esclusi dai profili target, che non hanno ricevuto il messaggio.

* **[!UICONTROL Percentuale di esclusione]**: percentuale di profili che sono stati esclusi da Adobe Journey Optimizer.

Il **[!UICONTROL Escludi motivi]** e **[!UICONTROL Motivi di errore]** grafici e tabelle consentono di vedere quali errori ed esclusioni si sono verificati.
+++

## In-app {#in-app}

>[!CONTEXTUALHELP]
>id="ajo_channel_inapp_engagement"
>title="In-app - Coinvolgimento totale"
>abstract="I KPI per il coinvolgimento totale in-app forniscono informazioni complete sul coinvolgimento dei visitatori con i messaggi in-app, incluse metriche quali impressioni e interazioni."

>[!CONTEXTUALHELP]
>id="ajo_channel_inapp_engagement_overtime"
>title="In-app - Coinvolgimento nel tempo"
>abstract="Il grafico In-app - Coinvolgimento nel tempo eccessivo tiene traccia delle impression e delle interazioni in-app, fornendo raggruppamenti orari, giornalieri, settimanali e mensili."

Dai rapporti sul canale, il menu in-app fornisce i dettagli delle informazioni principali relative ai messaggi in-app inviati nelle campagne e nei Percorsi. Le metriche sono descritte di seguito.

![](assets/inapp_channel_1.png)

+++  Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto in-app.

Il **[!UICONTROL Coinvolgimento totale in-app]** I KPI descrivono le informazioni principali relative al coinvolgimento dei visitatori con i messaggi in-app, ad esempio:

* **[!UICONTROL Impression]**: numero totale di messaggi in-app consegnati a tutti gli utenti.

* **[!UICONTROL Interazioni]**: numero totale di engagement con il messaggio in-app. Ciò include tutte le azioni intraprese dagli utenti, come clic, revoche o qualsiasi altra interazione.

* **[!UICONTROL Respinge]**: numero totale di messaggi in-app che i profili hanno chiuso facendo clic sul pulsante Chiudi o Chiudi automaticamente.

* **[!UICONTROL Percentuale ignorati]**: percentuale di messaggi in-app ignorati dai profili.

Il **[!UICONTROL Intervento in-app straordinario]** Il grafico mostra l’evoluzione delle impression e delle interazioni in-app per il periodo in questione, tenendo traccia di eventuali impression, ignoramenti o interazioni.

+++

## Web {#web}

>[!CONTEXTUALHELP]
>id="ajo_channel_web_engagement"
>title="Web - Coinvolgimento totale"
>abstract="I KPI (Key Performance Indicator) Web - Coinvolgimento totale forniscono informazioni complete sul coinvolgimento dei visitatori con le pagine Web, incluse metriche quali impressioni e interazioni."

>[!CONTEXTUALHELP]
>id="ajo_channel_web_engagement_overtime"
>title="Web - Straordinari di coinvolgimento totali"
>abstract="Il grafico Web - Coinvolgimento nel tempo libero tiene traccia delle impression e delle interazioni delle pagine Web, fornendo raggruppamenti orari, giornalieri, settimanali e mensili."

Dai rapporti sul canale, il menu Web fornisce i dettagli delle informazioni principali relative alle pagine Web incluse nelle campagne e nei Percorsi. Le metriche sono descritte di seguito.

![](assets/web_channel_1.png)

+++ Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto Web.

Il **[!UICONTROL Coinvolgimento totale web]** I KPI descrivono le informazioni principali relative al coinvolgimento dei visitatori con le esperienze web, ad esempio:

* **[!UICONTROL Impression]**: numero totale di esperienze web consegnate a tutti gli utenti.

* **[!UICONTROL Interazioni]**: numero totale di engagement con la pagina web. Ciò include qualsiasi azione eseguita dagli utenti, ad esempio clic o altre interazioni.

* **[!UICONTROL Respinge]**: numero totale di pagine web che i profili hanno chiuso.

* **[!UICONTROL Percentuale ignorati]**: percentuale di pagine web che i profili hanno chiuso.

Il **[!UICONTROL Straordinari di coinvolgimento sul web]** il grafico descrive le informazioni principali relative al coinvolgimento dei visitatori con le tue pagine web.

+++

## Rapporto sul canale (video) {#channel-report-video}

Scopri come accedere, navigare ed esportare i rapporti a livello di canale in questo video

>[!VIDEO](https://video.tv.adobe.com/v/3424537?quality=12)
