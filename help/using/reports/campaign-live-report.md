---
solution: Journey Optimizer
product: journey optimizer
title: Report live della campagna
description: Scopri come utilizzare i dati dal rapporto live di Campaign
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 925494b6-e08a-4bd3-8a2f-96a5d9cbc387
source-git-commit: 2160d52f24af50417cdcf8c6ec553b746a544c2f
workflow-type: tm+mt
source-wordcount: '750'
ht-degree: 0%

---

# Report live della campagna {#campaign-live-report}

Puoi accedere al rapporto live della campagna direttamente dalla tua campagna con **[!UICONTROL Live view]** pulsante .

La campagna **[!UICONTROL Live report]** La pagina verrà visualizzata con le seguenti schede:

* [Campaign](#campaign-live)
* [E-mail](#email-live)
* [Push](#push-live)
* [SMS](#sms-live)


La campagna **[!UICONTROL Live report]** è suddiviso in diversi widget che descrivono in dettaglio il successo e gli errori della campagna. Se necessario, ogni widget può essere ridimensionato ed eliminato. Per ulteriori informazioni, consulta questo [sezione](../reports/live-report.md#modify-dashboard).

Per un elenco dettagliato di ogni metrica disponibile in Adobe Journey Optimizer, consulta [questa pagina](live-report.md#list-of-components-live).

## Scheda Campaign {#campaign-global}

### Consegna {#delivery-global}

La **[!UICONTROL Campaign Statistics]** i dettagli del widget forniscono le informazioni principali relative alla campagna:

* **[!UICONTROL Entered profiles]**: Numero di profili che hanno avviato il percorso.

<!--
### Experimentation tab (#experimentation-live)

From your Campaign **[!UICONTROL Live report]**, the **[!UICONTROL Experimentation]** tab details the main information relative to how each variant is performing and if there is was winner during the test.
-->

## Scheda E-mail {#email-live}

Dalla tua campagna **[!UICONTROL Live report]**, **[!UICONTROL Email]** la scheda descrive le informazioni principali relative alle consegne e-mail inviate nella campagna.

![](assets/campaign_report_live_1.png)

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto E-mail.

La **[!UICONTROL Email Sending Statistics]** widget fornisce informazioni principali relative al messaggio:

* **[!UICONTROL Delivered]**: Numero di messaggi inviati correttamente.

* **[!UICONTROL Bounces]**: Totale degli errori cumulati durante la consegna e l&#39;elaborazione automatica della restituzione.

* **[!UICONTROL Errors]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

La **[!UICONTROL Sending metrics by Email]** tabella e **[!UICONTROL Email Summary]** il grafico descrive il successo della consegna:

* **[!UICONTROL Sent]**: Numero totale di invii per la consegna.

* **[!UICONTROL Delivered]**: Numero di messaggi inviati correttamente.

* **[!UICONTROL Bounces]**: Totale degli errori cumulati durante la consegna e l&#39;elaborazione automatica della restituzione.

* **[!UICONTROL Errors]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

* **[!UICONTROL Opens]**: Numero di volte in cui un messaggio è stato aperto in una consegna.

* **[!UICONTROL Clicks]**: Numero di volte in cui è stato fatto clic su un contenuto in una consegna.

* **[!UICONTROL Unsubscribe]**: Numero di clic sul collegamento di annullamento dell’abbonamento.

* **[!UICONTROL Spam complaints]**: Numero di volte in cui un messaggio è stato dichiarato come spam o spazzatura.

La **[!UICONTROL Bounce Reasons]**, **[!UICONTROL Bounce categories]** e **[!UICONTROL Hard and bounce - by Email]** I widget contengono i dati disponibili relativi ai messaggi non recapitati, ad esempio:

* **[!UICONTROL Hard bounce]**: Numero totale di errori permanenti, ad esempio un indirizzo e-mail errato. Ciò comporta un messaggio di errore che indica esplicitamente che l’indirizzo non è valido, ad esempio l’utente sconosciuto.

* **[!UICONTROL Soft bounce]**: Numero totale di errori temporanei, ad esempio una casella in entrata completa.

* **[!UICONTROL Ignored]**: Numero totale di temporanei, ad esempio Fuori sede, o un errore tecnico, ad esempio se il tipo di mittente è postmaster.

La **[!UICONTROL Error Reasons]** e **[!UICONTROL Exclude Reasons]** grafici e tabelle ti consentono di vedere quali errori ed esclusioni si sono verificati durante la consegna.

La **[!UICONTROL Email - Top recipient domain]** visualizza i dettagli del grafico e della tabella relativi ai domini più utilizzati dai destinatari per aprire l’e-mail.
+++

## Scheda notifica push {#push-live}

Dalla tua campagna **[!UICONTROL Live report]**, **[!UICONTROL Push notification]** la scheda descrive le informazioni principali relative alle consegne push inviate nella campagna.

![](assets/campaign_report_live_2.png)

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto push.

**[!UICONTROL Push notification sending performance]**, **[!UICONTROL Push notification summary]** e **[!UICONTROL Sending metrics - by Push]** i widget descrivono nel dettaglio le informazioni principali relative al messaggio:

* **[!UICONTROL Sent]**: Numero totale di invii per la consegna.

* **[!UICONTROL Delivered]**: Numero di messaggi inviati correttamente.

* **[!UICONTROL Bounces]**: Totale degli errori cumulati durante la consegna e l&#39;elaborazione automatica della restituzione.

* **[!UICONTROL Errors]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

* **[!UICONTROL Opens]**: Numero di volte in cui un messaggio è stato aperto in una consegna.

* **[!UICONTROL Actions]**: Numero totale di azioni sulla notifica push consegnata, ad esempio clic su un pulsante o cancellazione.

* **[!UICONTROL Engagements]**: Numero totale di aperture e azioni per questa notifica push, ad esempio se il profilo ha aperto il push o se è stato fatto clic su un pulsante.

La **[!UICONTROL Error Reasons]** e **[!UICONTROL Exclude Reasons]** grafici e tabelle ti consentono di vedere quali errori ed esclusioni si sono verificati durante la consegna.

La **[!UICONTROL Sending statistics - Failed]** widget consente di vedere quanti errori e mancati riscontri si sono verificati.

La **[!UICONTROL Tracking by platform]**, **[!UICONTROL Sending by platform]** e **[!UICONTROL Breakdown by platform]** grafici e tabelle descrivono in dettaglio il successo della notifica push in base al sistema operativo.
+++

## Scheda SMS {#sms-live}

Dalla tua campagna **[!UICONTROL Live report]**, **[!UICONTROL SMS]** la scheda descrive le informazioni principali relative alle consegne SMS inviate nella campagna.

![](assets/campaign_report_live_3.png)

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto SMS.

La **[!UICONTROL SMS - Sending statistics]** la tabella descrive il successo della consegna:

* **[!UICONTROL Targeted]**: Numero di profili utente qualificati come profili di destinazione per questa consegna.

* **[!UICONTROL Excluded]**: Numero di profili utente, esclusi dai profili target, che non hanno ricevuto il messaggio.

* **[!UICONTROL Sent]**: Numero totale di invii per la consegna.

* **[!UICONTROL Delivered]**: Numero di messaggi inviati correttamente.

* **[!UICONTROL Bounces]**: Totale degli errori cumulati durante la consegna e l&#39;elaborazione automatica della restituzione.

* **[!UICONTROL Errors]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

La **[!UICONTROL SMS Performance by date]** il widget descrive le informazioni principali relative al messaggio con un grafico:

* **[!UICONTROL Sent]**: Numero totale di invii per la consegna.

* **[!UICONTROL Delivered]**: Numero di messaggi inviati correttamente.

* **[!UICONTROL Bounces]**: Totale degli errori cumulati durante la consegna e l&#39;elaborazione automatica della restituzione.

* **[!UICONTROL Errors]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

La **[!UICONTROL Exclude Reasons]**, **[!UICONTROL Bounces Reasons]** e **[!UICONTROL Error Reasons]** grafici e tabelle ti consentono di vedere quali errori ed esclusioni si sono verificati durante la consegna.
+++

## Risorse aggiuntive

* [Guida introduttiva alle campagne](../campaigns/get-started-with-campaigns.md)
* [Creare una campagna](../campaigns/create-campaign.md)
* [Creare campagne con attivazione API](../campaigns/api-triggered-campaigns.md)
* [Modificare o interrompere una campagna](../campaigns/modify-stop-campaign.md)
* [Report globale di Campaign](campaign-global-report.md)
