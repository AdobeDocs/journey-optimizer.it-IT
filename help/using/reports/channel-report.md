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
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: tm+mt
source-wordcount: '1867'
ht-degree: 2%

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


Dai rapporti sul canale, il menu E-mail fornisce i dettagli delle informazioni principali relative alle e-mail inviate nelle campagne e nei Percorsi. Le metriche sono descritte di seguito.

![](assets/email_channel_1.png)

+++  Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto e-mail.

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

Il **[!UICONTROL Statistiche di tracciamento del totale delle e-mail]** Il widget contiene i dati disponibili per l’attività del destinatario per le e-mail:

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

Il **[!UICONTROL Notifica push - Statistiche di tracciamento totali]** contiene i dati disponibili per l’attività del destinatario per le notifiche push:

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

Il **[!UICONTROL Tracciamento per piattaforma]** e **[!UICONTROL Invio per piattaforma]** grafici e tabelle descrivono in dettaglio la riuscita della notifica push in base al sistema operativo del destinatario.
+++

## SMS {#sms}


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

## In-app {#in-app}


Dai rapporti sul canale, il menu in-app fornisce i dettagli delle informazioni principali relative ai messaggi in-app inviati nelle campagne e nei Percorsi. Le metriche sono descritte di seguito.

![](assets/inapp_channel_1.png)


+++  Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto in-app.

Il **[!UICONTROL Coinvolgimento totale in-app]** I KPI descrivono le informazioni principali relative al coinvolgimento dei visitatori con i messaggi in-app, ad esempio:

* **[!UICONTROL Impression]**: numero totale di messaggi in-app consegnati a tutti gli utenti.

* **[!UICONTROL Interazioni]**: numero totale di engagement con il messaggio in-app. Ciò include tutte le azioni intraprese dagli utenti, come clic, revoche o qualsiasi altra interazione.

* **[!UICONTROL Respinge]**: numero totale di messaggi in-app che i destinatari hanno chiuso facendo clic sul pulsante Chiudi o chiudi automaticamente.

* **[!UICONTROL Percentuale ignorati]**: percentuale di messaggi in-app ignorati dai destinatari.

Il **[!UICONTROL Intervento in-app straordinario]** Il grafico mostra l’evoluzione delle impression e delle interazioni in-app per il periodo in questione, tenendo traccia di eventuali impression, ignoramenti o interazioni.

+++

## Web {#web}


Dai rapporti sul canale, il menu Web fornisce i dettagli delle informazioni principali relative alle pagine Web incluse nelle campagne e nei Percorsi. Le metriche sono descritte di seguito.

![](assets/web_channel_1.png)


+++ Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto Web.

Il **[!UICONTROL Coinvolgimento totale web]** I KPI descrivono le informazioni principali relative al coinvolgimento dei visitatori con le esperienze web, ad esempio:

* **[!UICONTROL Impression]**: numero totale di esperienze web consegnate a tutti gli utenti.

* **[!UICONTROL Interazioni]**: numero totale di engagement con la pagina web. Ciò include qualsiasi azione eseguita dagli utenti, ad esempio clic o altre interazioni.

* **[!UICONTROL Respinge]**: numero totale di pagine Web ignorate dai destinatari.

* **[!UICONTROL Percentuale ignorati]**: percentuale di pagine Web ignorate dai destinatari.

Il **[!UICONTROL Straordinari di coinvolgimento sul web]** il grafico descrive le informazioni principali relative al coinvolgimento dei visitatori con le tue pagine web.

+++

## Direct mail {#direct-mail}


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


## Rapporto sul canale (video) {#channel-report-video}

Scopri come accedere, navigare ed esportare i rapporti a livello di canale in questo video

>[!VIDEO](https://video.tv.adobe.com/v/3424537?quality=12)
