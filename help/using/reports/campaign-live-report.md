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
source-git-commit: 0d8a19568e52952f3bc8af3c768cef4804a31749
workflow-type: tm+mt
source-wordcount: '1088'
ht-degree: 15%

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
* [Push](#push-live)
* [SMS](#sms-live)
* [Web](#web-tab)

La campagna **[!UICONTROL Rapporto live]** è diviso in diversi widget che descrivono nel dettaglio il successo e gli errori della campagna. Ogni widget può essere ridimensionato ed eliminato, se necessario. Per ulteriori informazioni, consulta questa [sezione](../reports/live-report.md#modify-dashboard).

Per un elenco dettagliato di tutte le metriche disponibili in Adobe Journey Optimizer, consulta [questa pagina](live-report.md#list-of-components-live).

## Scheda Campagna {#campaign-global}

### Distribuzione {#delivery-global}

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

## Scheda Notifica push {#push-live}

Dalla campagna **[!UICONTROL Rapporto live]**, il **[!UICONTROL Notifica push]** La scheda descrive le informazioni principali relative alle consegne push inviate nella campagna.

![](assets/campaign_report_live_2.png)

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto push.

**[!UICONTROL Prestazione invio notifiche push]**, **[!UICONTROL Riepilogo notifiche push]** e **[!UICONTROL Metriche di invio - modalità push]** i widget descrivono le informazioni principali relative al messaggio:

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

Dalla campagna **[!UICONTROL Rapporto globale]**, il **[!UICONTROL Web]** Questa scheda fornisce informazioni dettagliate sulle informazioni principali relative alle pagine Web.

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto Web.

Il **[!UICONTROL Prestazioni web]** I KPI descrivono le informazioni principali relative al coinvolgimento dei visitatori con le esperienze web, ad esempio:

* **[!UICONTROL Impression univoche]**: numero di utenti univoci a cui è stata consegnata l’esperienza web.

* **[!UICONTROL Impression]**: numero totale di esperienze web consegnate a tutti gli utenti.

* **[!UICONTROL Clic]**: numero totale di visite URL.

Il **[!UICONTROL Riepilogo web]** il grafico mostra l’evoluzione delle esperienze web (impression, impression univoche e clic) per il periodo in questione.

Il **[!UICONTROL Clic per elemento]** la tabella descrive le informazioni principali relative al coinvolgimento dei visitatori con i vari elementi presenti nelle pagine web.
+++

## Risorse aggiuntive

* [Introduzione alle campagne](../campaigns/get-started-with-campaigns.md)
* [Creare una campagna](../campaigns/create-campaign.md)
* [Creare campagne attivate da API](../campaigns/api-triggered-campaigns.md)
* [Modificare o interrompere una campagna](../campaigns/modify-stop-campaign.md)
* [Rapporto globale della campagna](campaign-global-report.md)
