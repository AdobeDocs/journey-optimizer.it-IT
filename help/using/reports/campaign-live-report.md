---
solution: Journey Optimizer
product: journey optimizer
title: Rapporto live della campagna
description: Scopri come utilizzare i dati dal rapporto live della campagna
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 925494b6-e08a-4bd3-8a2f-96a5d9cbc387
source-git-commit: adcfff1cb8bb2ae98d41e4071f56a137e52ee56a
workflow-type: tm+mt
source-wordcount: '1859'
ht-degree: 9%

---

# Rapporto live della campagna {#campaign-live-report}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_report"
>title="Rapporto live della campagna"
>abstract="Il rapporto live delle campagne consente di misurare e visualizzare in tempo reale l’impatto e le prestazioni di una campagna solo nelle ultime 24 ore. Il rapporto è suddiviso in diversi widget che descrivono il successo e gli errori della campagna. Ogni dashboard di reporting può essere modificata ridimensionando o spostando i widget."

I rapporti live, accessibili dalla scheda Ultime 24 ore, visualizzano gli eventi che si sono verificati nelle ultime 24 ore, con un intervallo di tempo minimo di due minuti dall’occorrenza dell’evento. Al confronto, i rapporti globali si concentrano sugli eventi che si sono verificati almeno due ore fa e coprono gli eventi in un periodo di tempo selezionato.

Il rapporto live della campagna è accessibile direttamente dalla campagna con **[!UICONTROL Vista live]** pulsante.

La campagna **[!UICONTROL Rapporto live]** La pagina verrà visualizzata con le seguenti schede:

* [Campaign](#campaign-live)
* [E-mail](#email-live)
* [In-app](#inapp-live)
* [Push](#push-live)
* [SMS](#sms-live)
* [Web](#web-tab)
* [Direct mail](#direct-mail-tab)

La campagna **[!UICONTROL Rapporto live]** è diviso in diversi widget che descrivono nel dettaglio il successo e gli errori della campagna. Ogni widget può essere ridimensionato ed eliminato, se necessario. Per ulteriori informazioni, consulta questa [sezione](../reports/live-report.md#modify-dashboard).

Per un elenco dettagliato di tutte le metriche disponibili in Adobe Journey Optimizer, consulta [questa pagina](live-report.md#list-of-components-live).

## Scheda Campagna {#campaign-live}

### Distribuzione {#delivery-live}

Il **[!UICONTROL Statistiche campagna]** widget fornisce dettagli sulle informazioni principali relative alla campagna:

* **[!UICONTROL Profili immessi]**: numero di profili che hanno avviato il percorso.

<!--
### Experimentation tab (#experimentation-live)

From your Campaign **[!UICONTROL Live report]**, the **[!UICONTROL Experimentation]** tab details the main information relative to how each variant is performing and if there is was winner during the test.
-->

## Scheda E-mail {#email-live}

Dalla campagna **[!UICONTROL Rapporto live]**, il **[!UICONTROL E-mail]** La scheda fornisce i dettagli delle informazioni principali relative alle consegne e-mail inviate nella campagna.

![](assets/campaign_report_live_1.png)

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto e-mail.

Il **[!UICONTROL Statistiche di invio e-mail]** il widget descrive le informazioni principali relative al messaggio:

* **[!UICONTROL Consegnato]**: numero di messaggi inviati correttamente.

* **[!UICONTROL Mancati recapiti]**: totale degli errori accumulati durante la consegna e l’elaborazione automatica della restituzione.

* **[!UICONTROL Errori]**: numero totale di errori che si sono verificati durante una consegna e che ne hanno impedito l’invio ai profili.

Il **[!UICONTROL Metriche di invio per e-mail]** tabella e **[!UICONTROL Riepilogo e-mail]** il grafico descrive il successo della consegna:

* **[!UICONTROL Inviato]**: numero totale di invii per la consegna.

* **[!UICONTROL Consegnato]**: numero di messaggi inviati correttamente.

* **[!UICONTROL Mancati recapiti]**: totale degli errori accumulati durante la consegna e l’elaborazione automatica della restituzione.

* **[!UICONTROL Errori]**: numero totale di errori che si sono verificati durante una consegna e che ne hanno impedito l’invio ai profili.

* **[!UICONTROL Aperture]**: numero di volte in cui un messaggio è stato aperto in una consegna.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto in una consegna.

* **[!UICONTROL Annulla iscrizione]**: numero di clic sul collegamento di annullamento dell’abbonamento.

* **[!UICONTROL Reclami spam]**: numero di volte in cui un messaggio è stato dichiarato come spam o posta indesiderata.

Il **[!UICONTROL Motivi di mancato recapito]**, **[!UICONTROL Categorie di mancato recapito]** e **[!UICONTROL Errore permanente di recapito - Da e-mail]** I widget contengono i dati disponibili relativi ai messaggi non recapitati, ad esempio:

* **[!UICONTROL Mancato recapito permanente]**: numero totale di errori permanenti, ad esempio un indirizzo e-mail errato. Ciò comporta un messaggio di errore che indica esplicitamente che l’indirizzo non è valido, ad esempio Utente sconosciuto.

* **[!UICONTROL Mancato recapito non permanente]**: numero totale di errori temporanei, ad esempio una casella in entrata completa.

* **[!UICONTROL Ignorato]**: numero totale di messaggi temporanei, ad esempio Fuori sede, o un errore tecnico, ad esempio se il tipo di mittente è postmaster.

Il **[!UICONTROL Motivi di errore]** e **[!UICONTROL Escludi motivi]** grafici e tabelle consentono di vedere quali errori ed esclusioni si sono verificati durante la consegna.

Il **[!UICONTROL E-mail - Dominio destinatario principale]** il grafico e la tabella indicano i domini più utilizzati dai destinatari per aprire l’e-mail.
+++

## Scheda In-app {#inapp-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_performance"
>title="Prestazioni in-app"
>abstract="I KPI (Key Performance Indicator) in-app forniscono informazioni essenziali sul coinvolgimento dei visitatori con i messaggi in-app nelle ultime 24 ore."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_interactions"
>title="Interazioni per tipo"
>abstract="Le Interazioni per tipo rappresentano grafici e tabelle che descrivono in dettaglio il modo in cui gli utenti hanno interagito con il messaggio in-app tracciando eventuali clic, eliminazioni o interazioni delle ultime 24 ore."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_summary"
>title="Riepilogo in-app"
>abstract="Il grafico di riepilogo in-app illustra la progressione delle impression e delle interazioni in-app nelle ultime 24 ore."

Dalla campagna **[!UICONTROL Rapporto live]**, il **[!UICONTROL In-app]** Questa scheda contiene le informazioni principali relative alle consegne in-app inviate nella campagna.

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto in-app.

Il **[!UICONTROL Prestazioni in-app]** I KPI descrivono le informazioni principali relative al coinvolgimento dei visitatori con i messaggi in-app, ad esempio:

* **[!UICONTROL Impression]**: numero totale di messaggi in-app consegnati a tutti gli utenti.

* **[!UICONTROL Interazioni]**: numero totale di engagement con il messaggio in-app. Ciò include tutte le azioni intraprese dagli utenti, come clic, revoche o qualsiasi altra interazione.

Il **[!UICONTROL Riepilogo in-app]** Il grafico mostra l’evoluzione delle impression e delle interazioni in-app per il periodo in questione.

Il **[!UICONTROL Interazioni per tipo]** grafici e tabelle dettagliano il modo in cui gli utenti interagivano con il messaggio in-app tracciando i clic, le eliminazioni o le interazioni.

+++

## Scheda Notifica push {#push-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_sending_performance"
>title="Notifica push - Prestazioni di invio"
>abstract="Il grafico Prestazioni invio notifiche push riassume i dati essenziali relativi alle notifiche push, come Errori o Messaggi consegnati nelle ultime 24 ore."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_statistics"
>title="Notifica push - Statistiche"
>abstract="La tabella Statistiche push fornisce dati sull’attività del destinatario per la consegna dalle ultime 24 ore."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_sending_summary"
>title="Notifica push - Riepilogo di invio"
>abstract="Il grafico Riepilogo invio notifiche push visualizza i dati disponibili per le notifiche push inviate dalle ultime 24 ore."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_excluded_reasons"
>title="Notifica push - Motivi di esclusione"
>abstract="I grafici e la tabella dei motivi di esclusione illustrano i vari fattori che hanno portato ai profili utente, esclusi dal pubblico di destinazione, a non ricevere il messaggio nelle ultime 24 ore."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_error_reasons"
>title="Notifica push - Motivi di errore"
>abstract="I grafici e la tabella Motivi di errore consentono di identificare gli errori specifici che si sono verificati nelle ultime 24 ore durante la consegna."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_breakdown_platform"
>title="Notifica push - Raggruppamento per piattaforma"
>abstract="La tabella e i grafici Raggruppamento per piattaforma forniscono un riepilogo del successo delle notifiche push nelle ultime 24 ore in base al sistema operativo del destinatario."

Dalla campagna **[!UICONTROL Rapporto live]**, il **[!UICONTROL Notifica push]** La scheda descrive le informazioni principali relative alle consegne push inviate nella campagna.

![](assets/campaign_report_live_2.png)

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto push.

**[!UICONTROL Prestazione invio notifiche push]**, **[!UICONTROL Riepilogo notifiche push]** e **[!UICONTROL Notifica push - Statistiche]** i widget descrivono le informazioni principali relative al messaggio:

* **[!UICONTROL Inviato]**: numero totale di invii per la consegna.

* **[!UICONTROL Consegnato]**: numero di messaggi inviati correttamente.

* **[!UICONTROL Mancati recapiti]**: totale degli errori accumulati durante la consegna e l’elaborazione automatica della restituzione.

* **[!UICONTROL Errori]**: numero totale di errori che si sono verificati durante una consegna e che ne hanno impedito l’invio ai profili.

* **[!UICONTROL Aperture]**: numero di volte in cui un messaggio è stato aperto in una consegna.

* **[!UICONTROL Azioni]**: numero totale di azioni sulla notifica push consegnata, ad esempio clic su pulsante o rimozione.

* **[!UICONTROL Coinvolgimenti]**: numero totale di aperture e azioni per questa notifica push, ovvero se il profilo ha aperto la notifica push o se è stato fatto clic su un pulsante.

Il **[!UICONTROL Motivi di errore]** e **[!UICONTROL Escludi motivi]** grafici e tabelle consentono di vedere quali errori ed esclusioni si sono verificati durante la consegna.

Il **[!UICONTROL Statistiche di invio - Non riuscito]** Il widget consente di vedere quanti errori e mancati recapiti si sono verificati.

Il **[!UICONTROL Tracciamento per piattaforma]**, **[!UICONTROL Invio per piattaforma]** e **[!UICONTROL Raggruppamento per piattaforma]** grafici e tabelle descrivono in dettaglio l’esito positivo della notifica push, a seconda del sistema operativo.
+++

## Scheda SMS {#sms-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_statistics"
>title="SMS - Statistiche"
>abstract="La tabella Statistiche di invio SMS riepiloga i dati essenziali relativi ai messaggi SMS, ad esempio Messaggi mirati o recapitati, delle ultime 24 ore."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_performance"
>title="SMS - Prestazioni per data"
>abstract="Il widget Prestazioni SMS per data fornisce informazioni chiave sulle ultime 24 ore relative ai messaggi tramite una rappresentazione grafica."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_error_reasons"
>title="SMS - Motivi di errore"
>abstract="I grafici e la tabella SMS - Motivi di errore ti consentono di identificare gli errori specifici che si sono verificati nelle ultime 24 ore durante la consegna."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_excluded_reasons"
>title="SMS - Motivi di esclusione"
>abstract="I grafici e la tabella dei motivi di esclusione illustrano i vari fattori che hanno portato ai profili utente, esclusi dal pubblico di destinazione, a non ricevere il messaggio nelle ultime 24 ore."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_bounces_reasons"
>title="SMS - Motivi di mancato recapito"
>abstract="I grafici e la tabella Motivi di mancato recapito contengono i dati disponibili nelle ultime 24 ore relativi ai messaggi non recapitati."

Dalla campagna **[!UICONTROL Rapporto live]**, il **[!UICONTROL SMS]** Questa scheda fornisce le informazioni principali relative alle consegne di SMS inviate nella campagna.

![](assets/campaign_report_live_3.png)

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto SMS.

Il **[!UICONTROL SMS - Statistiche]** la tabella descrive il successo della consegna:

* **[!UICONTROL Target]**: numero di profili utente qualificati come profili target per questa consegna.

* **[!UICONTROL Escluso]**: numero di profili utente, esclusi dai profili target, che non hanno ricevuto il messaggio.

* **[!UICONTROL Inviato]**: numero totale di invii per la consegna.

* **[!UICONTROL Mancati recapiti]**: totale degli errori accumulati durante la consegna e l’elaborazione automatica della restituzione.

* **[!UICONTROL Errori]**: numero totale di errori che si sono verificati durante una consegna e che ne hanno impedito l’invio ai profili.

* **[!UICONTROL Clic]**: numero totale di visite URL.

Il **[!UICONTROL Prestazioni SMS per data]** un grafico fornisce dettagli sulle informazioni principali relative al messaggio:

* **[!UICONTROL Inviato]**: numero totale di invii per la consegna.

* **[!UICONTROL Mancati recapiti]**: totale degli errori accumulati durante la consegna e l’elaborazione automatica della restituzione.

* **[!UICONTROL Errori]**: numero totale di errori che si sono verificati durante una consegna e che ne hanno impedito l’invio ai profili.

Il **[!UICONTROL Escludi motivi]**, **[!UICONTROL Motivi di mancato recapito]** e **[!UICONTROL Motivi di errore]** grafici e tabelle consentono di vedere quali errori ed esclusioni si sono verificati durante la consegna.
+++

## Scheda Web {#web-tab}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_performance"
>title="Prestazioni web"
>abstract="I KPI per le prestazioni web forniscono informazioni complete sul coinvolgimento dei visitatori con le esperienze web delle ultime 24 ore."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_summary"
>title="Riepilogo web"
>abstract="Il grafico Riepilogo web illustra la progressione delle esperienze web, incluse impression, impression univoche e interazioni, dalle ultime 24 ore."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_interactions"
>title="Interazioni per elemento"
>abstract="La tabella Interazioni per elemento fornisce informazioni chiave sul coinvolgimento dei visitatori con diversi elementi nelle pagine web nelle ultime 24 ore."

Dalla campagna **[!UICONTROL Rapporto live]**, il **[!UICONTROL Web]** Questa scheda fornisce informazioni dettagliate sulle informazioni principali relative alle pagine Web.

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto Web.

Il **[!UICONTROL Prestazioni web]** I KPI descrivono le informazioni principali relative al coinvolgimento dei visitatori con le esperienze web, ad esempio:

* **[!UICONTROL Impression]**: numero totale di esperienze web consegnate a tutti gli utenti.

* **[!UICONTROL Interazioni]**: numero totale di engagement con la pagina web. Ciò include qualsiasi azione eseguita dagli utenti, ad esempio clic o altre interazioni.

Il **[!UICONTROL Riepilogo web]** il grafico mostra l’evoluzione delle esperienze web (impression, impression e interazioni uniche) nelle ultime 24 ore.

Il **[!UICONTROL Interazioni per elemento]** la tabella descrive le informazioni principali relative al coinvolgimento dei visitatori con i vari elementi presenti nelle pagine web.
+++

## Scheda Direct mailing {#direct-mail-tab}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_sending_statistics"
>title="Direct mailing - Statistiche di invio"
>abstract="La tabella Statistiche di invio Direct Mail riepiloga i dati essenziali delle ultime 24 ore relativi ai messaggi Direct Mail, ad esempio i messaggi di destinazione o recapitati."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_error_reasons"
>title="Direct mailing - Motivi di errore"
>abstract="I grafici e la tabella Direct mailing - Error Reasons (Mailing diretto: motivi di errore) consentono di identificare gli errori specifici che si sono verificati nelle ultime 24 ore."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_excluded_reasons"
>title="Direct mailing - Motivi di esclusione"
>abstract="I grafici e la tabella dei motivi di esclusione della direct mailing illustrano i vari fattori che hanno portato ai profili utente, esclusi dal pubblico di destinazione, a non ricevere il messaggio nelle ultime 24 ore."

Dalla campagna **[!UICONTROL Rapporto live]**, il **[!UICONTROL Direct mail]** Questa scheda contiene le informazioni principali relative alle consegne Direct mailing.

![](assets/direct-mail-report_2.png)

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto Direct mail.

Il **[!UICONTROL Direct mailing - Statistiche di invio]** la tabella descrive il successo della consegna:

* **[!UICONTROL Target]**: numero di profili utente qualificati come profili target per questa consegna.

* **[!UICONTROL Inviato]**: numero totale di invii per la consegna.

* **[!UICONTROL Errori]**: numero totale di errori che si sono verificati durante una consegna e che ne hanno impedito l’invio ai profili.

* **[!UICONTROL Escluso]**: numero di profili utente, esclusi dai profili target, che non hanno ricevuto la consegna.

Il **[!UICONTROL Direct mailing - Motivi di esclusione]** e **[!UICONTROL Direct mailing - Motivi di errore]** grafici e tabelle consentono di vedere quali errori ed esclusioni si sono verificati durante la consegna.
+++

## Risorse aggiuntive

* [Introduzione alle campagne](../campaigns/get-started-with-campaigns.md)
* [Creare una campagna](../campaigns/create-campaign.md)
* [Creare campagne attivate da API](../campaigns/api-triggered-campaigns.md)
* [Modificare o interrompere una campagna](../campaigns/modify-stop-campaign.md)
* [Rapporto globale della campagna](campaign-global-report.md)
