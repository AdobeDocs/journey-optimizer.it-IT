---
title: Rapporto live dei percorsi
description: Scopri come utilizzare i dati del report live del percorso
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: e3781f79-7c8d-4512-b44f-835639b1471f
source-git-commit: ffa1da19732f4c0bd5297e2d123140b9ba1b0103
workflow-type: tm+mt
source-wordcount: '896'
ht-degree: 1%

---

# Rapporto live dei percorsi {#journey-live-report}

È possibile accedere al rapporto percorso live direttamente dal percorso con **[!UICONTROL Live report]** pulsante .

![](assets/report_1.png)

Il percorso **[!UICONTROL Live report]** La pagina verrà visualizzata con le seguenti schede:

* [Percorso](#journey-live)
* [E-mail](#email-live)
* [Push](#push-live)
* [SMS](#sms-live)

Il percorso **[!UICONTROL Live report]** è diviso in diversi widget che descrivono il successo e gli errori del tuo percorso. Se necessario, ogni widget può essere ridimensionato ed eliminato. Per ulteriori informazioni, consulta questo [sezione](live-report.md#modify-dashboard).

## scheda percorso {#journey-live}

Dal tuo percorso **[!UICONTROL Live report]**, **[!UICONTROL Journey]** tab ti offre una visualizzazione chiara dei dati di tracciamento più importanti sul tuo percorso.

![](assets/report_journey_2.png)

**[!UICONTROL Journey Performance]** ti consente di visualizzare il percorso dei profili di destinazione passo dopo passo nel percorso.

La **[!UICONTROL Journey Statistics]** widget visualizza i KPI seguenti:

* **[!UICONTROL Entered profiles]**: Numero totale di persone che hanno raggiunto l&#39;evento di ingresso del percorso.

* **[!UICONTROL Exited profiles]**: Numero totale di persone uscite dal percorso.

* **[!UICONTROL Failed individual journeys]**: Numero totale di singoli percorsi che non sono stati eseguiti correttamente.

![](assets/report_journey_3.png)

La **[!UICONTROL Event executed over the last 24 hours]** e **[!UICONTROL Events]** I widget consentono di vedere quale degli eventi è stato eseguito correttamente tramite numero di riepilogo, grafico e tabella.

![](assets/report_journey_4.png)

La **[!UICONTROL Action executed over the last 24 hours]** e **[!UICONTROL Actions executed and errors]** I widget rappresentano l&#39;azione e gli errori più riusciti che si sono verificati quando le azioni sono state attivate. I numeri di grafico, tabella e riepilogo delle azioni contengono i dati disponibili per le azioni, ad esempio:

* **[!UICONTROL Actions executed]**: Numero totale di azioni eseguite correttamente per un percorso.

* **[!UICONTROL Error in actions]**: Numero totale di errori che si sono verificati per le azioni.

## Scheda E-mail {#email-live}

Dal tuo percorso **[!UICONTROL Live report]**, **[!UICONTROL Email]** scheda descrive le informazioni principali relative alle consegne e-mail inviate nel percorso.

Per un rapporto dettagliato su una consegna e-mail specifica, consulta la sezione [Report live e-mail](email-live-report.md) sezione .

![](assets/report_email_1.png)

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

![](assets/report_email_2.png)

La **[!UICONTROL Bounce Reasons]**, **[!UICONTROL Bounce categories]** e **[!UICONTROL Hard and bounce - by Email]** I widget contengono i dati disponibili relativi ai messaggi non recapitati, ad esempio:

* **[!UICONTROL Hard bounce]**: Numero totale di errori permanenti, ad esempio un indirizzo e-mail errato. Ciò comporta un messaggio di errore che indica esplicitamente che l’indirizzo non è valido, ad esempio l’utente sconosciuto.

* **[!UICONTROL Soft bounce]**: Numero totale di errori temporanei, ad esempio una casella in entrata completa.

* **[!UICONTROL Ignored]**: Numero totale di temporanei, ad esempio Fuori sede, o un errore tecnico, ad esempio se il tipo di mittente è postmaster.

![](assets/report_email_3.png)

La **[!UICONTROL Error Reasons]** e **[!UICONTROL Exclude Reasons]** grafici e tabelle ti consentono di vedere quali errori ed esclusioni si sono verificati durante la consegna.

La **[!UICONTROL Email - Top recipient domain]** visualizza i dettagli del grafico e della tabella relativi ai domini più utilizzati dai destinatari per aprire l’e-mail.

![](assets/live_report_7.png)

>[!NOTE]
>
>I widget e le metriche Offerte sono disponibili solo se una decisione è stata inserita in un’e-mail. Per ulteriori informazioni sulla gestione delle decisioni, consulta questo [page](../offers/get-started/starting-offer-decisioning.md).

La **[!UICONTROL Offers statistic]** e **[!UICONTROL Offers statistics]** i widget nel tempo misurano il successo e l’impatto dell’offerta sul pubblico di destinazione. Vengono descritte in dettaglio le informazioni principali relative al messaggio con i KPI:

* **[!UICONTROL Offer sent]**: Numero totale di invii per l’offerta.

* **[!UICONTROL Offer impression]**: Numero di volte in cui l’offerta è stata aperta in una consegna.

* **[!UICONTROL Offer clicks]**: Numero di volte in cui un’offerta è stata selezionata in una consegna.

## Scheda push {#push-live}

Dal tuo percorso **[!UICONTROL Live report]**, **[!UICONTROL Push]** la scheda descrive le informazioni principali relative alle consegne push inviate nel percorso.

Per un rapporto dettagliato su una consegna push specifica, consulta la sezione [Report live push](push-live-report.md) sezione .

![](assets/report_push_1.png)

**[!UICONTROL Push notification sending performance]**, **[!UICONTROL Push notification summary]** e **[!UICONTROL Sending metrics - by Push]** i widget descrivono nel dettaglio le informazioni principali relative al messaggio:

* **[!UICONTROL Sent]**: Numero totale di invii per la consegna.

* **[!UICONTROL Delivered]**: Numero di messaggi inviati correttamente.

* **[!UICONTROL Bounces]**: Totale degli errori cumulati durante la consegna e l&#39;elaborazione automatica della restituzione.

* **[!UICONTROL Errors]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

* **[!UICONTROL Opens]**: Numero di volte in cui un messaggio è stato aperto in una consegna.

* **[!UICONTROL Actions]**: Numero totale di azioni sulla notifica push consegnata, ad esempio clic su un pulsante o cancellazione.

* **[!UICONTROL Engagements]**: Numero totale di aperture e azioni per questa notifica push, ad esempio se il profilo ha aperto il push o se è stato fatto clic su un pulsante.

![](assets/report_push_3.png)

La **[!UICONTROL Error Reasons]** e **[!UICONTROL Exclude Reasons]** grafici e tabelle ti consentono di vedere quali errori ed esclusioni si sono verificati durante la consegna.

La **[!UICONTROL Sending statistics - Failed]** widget consente di vedere quanti errori e mancati riscontri si sono verificati.

![](assets/report_push_2.png)

La **[!UICONTROL Tracking by platform]**, **[!UICONTROL Sending by platform]** e **[!UICONTROL Breakdown by platform]** grafici e tabelle descrivono in dettaglio il successo della notifica push in base al sistema operativo.

## Scheda SMS {#sms-live}

![](assets/report_sms_live.png)

La **[!UICONTROL SMS - Sending statistics]** la tabella descrive il successo della consegna:

* **[!UICONTROL Targeted]**: Numero di profili utente qualificati come profili di destinazione per questa consegna.

* **[!UICONTROL Excluded]**: Numero di profili utente, esclusi dai profili target, che non hanno ricevuto il messaggio.

* **[!UICONTROL Sent]**: Numero totale di invii per la consegna.

* **[!UICONTROL Delivered]**: Numero di messaggi inviati correttamente.

* **[!UICONTROL Opens]**: Numero di volte in cui un messaggio è stato aperto in una consegna.

* **[!UICONTROL Clicks]**: Numero di volte in cui è stato fatto clic su un contenuto in una consegna.

* **[!UICONTROL Bounces]**: Totale degli errori cumulati durante la consegna e l&#39;elaborazione automatica della restituzione.

* **[!UICONTROL Errors]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

La **[!UICONTROL SMS Summary]** il grafico descrive il successo della consegna:

* **[!UICONTROL Delivered]**: Numero di messaggi inviati correttamente.

* **[!UICONTROL Bounces]**: Totale degli errori cumulati durante la consegna e l&#39;elaborazione automatica della restituzione.

* **[!UICONTROL Errors]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

La **[!UICONTROL Exclude Reasons]** grafici e tabelle ti consentono di vedere quali errori ed esclusioni si sono verificati durante la consegna.
