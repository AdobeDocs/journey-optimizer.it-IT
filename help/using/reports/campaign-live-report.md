---
solution: Journey Optimizer
product: journey optimizer
title: Rapporto live della campagna
description: Scopri come utilizzare i dati dal rapporto live di Campaign
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 925494b6-e08a-4bd3-8a2f-96a5d9cbc387
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '1049'
ht-degree: 7%

---

# Rapporto live della campagna {#campaign-live-report}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_report"
>title="Rapporto live della campagna"
>abstract="Il rapporto live delle campagne consente di misurare e visualizzare in tempo reale l’impatto e le prestazioni di una campagna solo nelle ultime 24 ore. Il rapporto è suddiviso in diversi widget che descrivono il successo e gli errori della campagna. Ogni dashboard di reporting può essere modificata ridimensionando o spostando i widget."

Puoi accedere al rapporto live della campagna direttamente dalla tua campagna con **[!UICONTROL Vista dal vivo]** pulsante .

La campagna **[!UICONTROL Report live]** La pagina verrà visualizzata con le seguenti schede:

* [Campaign](#campaign-live)
* [E-mail](#email-live)
* [Push](#push-live)
* [SMS](#sms-live)
* [Web](#web-tab)

La campagna **[!UICONTROL Report live]** è suddiviso in diversi widget che descrivono in dettaglio il successo e gli errori della campagna. Se necessario, ogni widget può essere ridimensionato ed eliminato. Per ulteriori informazioni, consulta questo [sezione](../reports/live-report.md#modify-dashboard).

Per un elenco dettagliato di ciascuna metrica disponibile in Adobe Journey Optimizer, consulta [questa pagina](live-report.md#list-of-components-live).

## Scheda Campaign {#campaign-global}

### Distribuzione {#delivery-global}

La **[!UICONTROL Statistiche campagna]** i dettagli del widget forniscono le informazioni principali relative alla campagna:

* **[!UICONTROL Profili inseriti]**: Numero di profili che hanno avviato il percorso.

<!--
### Experimentation tab (#experimentation-live)

From your Campaign **[!UICONTROL Live report]**, the **[!UICONTROL Experimentation]** tab details the main information relative to how each variant is performing and if there is was winner during the test.
-->

## Scheda E-mail {#email-live}

Dalla tua campagna **[!UICONTROL Report live]**, **[!UICONTROL E-mail]** la scheda descrive le informazioni principali relative alle consegne e-mail inviate nella campagna.

![](assets/campaign_report_live_1.png)

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto E-mail.

La **[!UICONTROL Invio di statistiche per e-mail]** widget fornisce informazioni principali relative al messaggio:

* **[!UICONTROL Consegnato]**: Numero di messaggi inviati correttamente.

* **[!UICONTROL Rimbalzi]**: Totale degli errori cumulati durante la consegna e l&#39;elaborazione automatica della restituzione.

* **[!UICONTROL Errori]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

La **[!UICONTROL Invio di metriche per e-mail]** tabella e **[!UICONTROL Riepilogo e-mail]** il grafico descrive il successo della consegna:

* **[!UICONTROL Inviato]**: Numero totale di invii per la consegna.

* **[!UICONTROL Consegnato]**: Numero di messaggi inviati correttamente.

* **[!UICONTROL Rimbalzi]**: Totale degli errori cumulati durante la consegna e l&#39;elaborazione automatica della restituzione.

* **[!UICONTROL Errori]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

* **[!UICONTROL Aperture]**: Numero di volte in cui un messaggio è stato aperto in una consegna.

* **[!UICONTROL Clic]**: Numero di volte in cui è stato fatto clic su un contenuto in una consegna.

* **[!UICONTROL Annulla sottoscrizione]**: Numero di clic sul collegamento di annullamento dell’abbonamento.

* **[!UICONTROL Disturbi dello spam]**: Numero di volte in cui un messaggio è stato dichiarato come spam o spazzatura.

La **[!UICONTROL Ragioni di mancato recapito]**, **[!UICONTROL Categorie di rimbalzi]** e **[!UICONTROL Rigido e non recapitato - per e-mail]** I widget contengono i dati disponibili relativi ai messaggi non recapitati, ad esempio:

* **[!UICONTROL Rimbalzo duro]**: Numero totale di errori permanenti, ad esempio un indirizzo e-mail errato. Ciò comporta un messaggio di errore che indica esplicitamente che l’indirizzo non è valido, ad esempio l’utente sconosciuto.

* **[!UICONTROL Rimbalzo morbido]**: Numero totale di errori temporanei, ad esempio una casella in entrata completa.

* **[!UICONTROL Ignorato]**: Numero totale di temporanei, ad esempio Fuori sede, o un errore tecnico, ad esempio se il tipo di mittente è postmaster.

La **[!UICONTROL Motivi dell’errore]** e **[!UICONTROL Escludi motivi]** grafici e tabelle ti consentono di vedere quali errori ed esclusioni si sono verificati durante la consegna.

La **[!UICONTROL E-mail - Dominio principale destinatario]** visualizza i dettagli del grafico e della tabella relativi ai domini più utilizzati dai destinatari per aprire l’e-mail.
+++

## Scheda notifica push {#push-live}

Dalla tua campagna **[!UICONTROL Report live]**, **[!UICONTROL Notifica push]** la scheda descrive le informazioni principali relative alle consegne push inviate nella campagna.

![](assets/campaign_report_live_2.png)

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto push.

**[!UICONTROL Prestazioni invio notifiche push]**, **[!UICONTROL Riepilogo delle notifiche push]** e **[!UICONTROL Invio di metriche - da push]** i widget descrivono nel dettaglio le informazioni principali relative al messaggio:

* **[!UICONTROL Inviato]**: Numero totale di invii per la consegna.

* **[!UICONTROL Consegnato]**: Numero di messaggi inviati correttamente.

* **[!UICONTROL Rimbalzi]**: Totale degli errori cumulati durante la consegna e l&#39;elaborazione automatica della restituzione.

* **[!UICONTROL Errori]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

* **[!UICONTROL Aperture]**: Numero di volte in cui un messaggio è stato aperto in una consegna.

* **[!UICONTROL Azioni]**: Numero totale di azioni sulla notifica push consegnata, ad esempio clic su un pulsante o cancellazione.

* **[!UICONTROL Coinvolgimento]**: Numero totale di aperture e azioni per questa notifica push, ad esempio se il profilo ha aperto il push o se è stato fatto clic su un pulsante.

La **[!UICONTROL Motivi dell’errore]** e **[!UICONTROL Escludi motivi]** grafici e tabelle ti consentono di vedere quali errori ed esclusioni si sono verificati durante la consegna.

La **[!UICONTROL Invio di statistiche - Non riuscito]** widget consente di vedere quanti errori e mancati riscontri si sono verificati.

La **[!UICONTROL Tracciamento per piattaforma]**, **[!UICONTROL Invio per piattaforma]** e **[!UICONTROL Suddivisione per piattaforma]** grafici e tabelle descrivono in dettaglio il successo della notifica push in base al sistema operativo.
+++

## Scheda SMS {#sms-live}

Dalla tua campagna **[!UICONTROL Report live]**, **[!UICONTROL SMS]** la scheda descrive le informazioni principali relative alle consegne SMS inviate nella campagna.

![](assets/campaign_report_live_3.png)

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto SMS.

La **[!UICONTROL SMS - Statistiche]** la tabella descrive il successo della consegna:

* **[!UICONTROL Target]**: Numero di profili utente qualificati come profili di destinazione per questa consegna.

* **[!UICONTROL Escluso]**: Numero di profili utente, esclusi dai profili target, che non hanno ricevuto il messaggio.

* **[!UICONTROL Inviato]**: Numero totale di invii per la consegna.

* **[!UICONTROL Consegnato]**: Numero di messaggi inviati correttamente.

* **[!UICONTROL Rimbalzi]**: Totale degli errori cumulati durante la consegna e l&#39;elaborazione automatica della restituzione.

* **[!UICONTROL Errori]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

* **[!UICONTROL Clic]**: Numero totale di visite URL.

La **[!UICONTROL Prestazioni SMS per data]** il widget descrive le informazioni principali relative al messaggio con un grafico:

* **[!UICONTROL Inviato]**: Numero totale di invii per la consegna.

* **[!UICONTROL Consegnato]**: Numero di messaggi inviati correttamente.

* **[!UICONTROL Rimbalzi]**: Totale degli errori cumulati durante la consegna e l&#39;elaborazione automatica della restituzione.

* **[!UICONTROL Errori]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

La **[!UICONTROL Escludi motivi]**, **[!UICONTROL Motivi dei rimbalzi]** e **[!UICONTROL Motivi dell’errore]** grafici e tabelle ti consentono di vedere quali errori ed esclusioni si sono verificati durante la consegna.
+++

## Scheda Web {#web-tab}

Dalla tua campagna **[!UICONTROL Report globale]**, **[!UICONTROL Web]** scheda descrive le informazioni principali relative alle pagine Web.

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il report Web.

La **[!UICONTROL Prestazioni web]** I KPI descrivono in dettaglio le informazioni principali relative al coinvolgimento dei visitatori con le esperienze web, ad esempio:

* **[!UICONTROL Impressioni univoche]**: numero di utenti univoci a cui è stata distribuita l’esperienza web.

* **[!UICONTROL Impressioni]**: numero totale di esperienze web distribuite a tutti gli utenti.

* **[!UICONTROL Clic]**: numero totale di visite URL.

La **[!UICONTROL Riepilogo web]** Il grafico mostra l’evoluzione delle esperienze web (impression, impression univoche e clic) per il periodo in questione.

La **[!UICONTROL Clic per elemento]** la tabella descrive le informazioni principali relative al coinvolgimento dei visitatori con i vari elementi presenti nelle pagine web.
+++

## Risorse aggiuntive

* [Introduzione alle campagne](../campaigns/get-started-with-campaigns.md)
* [Creare una campagna](../campaigns/create-campaign.md)
* [Creare campagne con attivazione API](../campaigns/api-triggered-campaigns.md)
* [Modificare o interrompere una campagna](../campaigns/modify-stop-campaign.md)
* [Rapporto globale della campagna](campaign-global-report.md)
