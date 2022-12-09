---
solution: Journey Optimizer
product: journey optimizer
title: Report globale della campagna
description: Scopri come utilizzare i dati dal rapporto globale di Campaign
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: fa64f5b8-75f2-40e6-8566-5766fafe6cd6
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '1468'
ht-degree: 0%

---

# Report globale della campagna {#campaign-global-report}

Puoi accedere al rapporto globale di Campaign direttamente dalla tua campagna con **[!UICONTROL All time]** pulsante .

![](assets/campaign_report_global_5.png)

La campagna **[!UICONTROL Global report]** La pagina verrà visualizzata con le seguenti schede:

* [Campaign](#campaign-global)
* [E-mail](#email-global)
* [Push](#push-global)
* [SMS](#sms-global)

La campagna **[!UICONTROL Global report]** è suddiviso in diversi widget che descrivono in dettaglio il successo e gli errori della campagna. Se necessario, ogni widget può essere ridimensionato ed eliminato. Per ulteriori informazioni, consulta questo [sezione](../reports/global-report.md#modify-dashboard).

Per un elenco dettagliato di ogni metrica disponibile in Adobe Journey Optimizer, consulta [questa pagina](global-report.md#list-of-components-global.md)

## Scheda Campaign {#campaign-global}

### Consegna {#delivery-global}

![](assets/campaign_report_global_1.png)

La **[!UICONTROL Campaign's Statistics]** i dettagli del widget forniscono le informazioni principali relative alla campagna:

* **[!UICONTROL Entered profiles]**: Numero di profili che hanno avviato il percorso.

* **[!UICONTROL Actions delivered]**: Numero totale di volte in cui un’azione nel percorso è stata consegnata.

* **[!UICONTROL Actions failed in %]**: Numero totale di volte in cui un’azione non è riuscita nel percorso rispetto al numero totale di volte in cui un’azione è stata consegnata.

## Scheda E-mail {#email-global}

![](assets/campaign_report_global_2.png)

Dalla tua campagna **[!UICONTROL Global report]**, **[!UICONTROL Email]** la scheda descrive le informazioni principali relative alle consegne e-mail inviate nella campagna.

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto E-mail.

La **[!UICONTROL Email Sending Statistics]** il grafico descrive il successo della consegna:

* **[!UICONTROL Targeted]**: Numero totale di messaggi elaborati durante l’analisi della consegna.

* **[!UICONTROL Sent]**: Numero totale di invii per la consegna.

* **[!UICONTROL Delivered]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Delivery Rate]**: Percentuale di messaggi inviati correttamente.

* **[!UICONTROL Bounces]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Bounce Rate]**: Percentuale di e-mail rimbalzate rispetto alle e-mail inviate.

* **[!UICONTROL Errors]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

* **[!UICONTROL Error Rate]**: Percentuale di errori che si sono verificati durante una consegna che ne impedisce l’invio rispetto alle e-mail inviate.

* **[!UICONTROL Retries]**: Numero di e-mail in coda per i nuovi tentativi.

* **[!UICONTROL Excluded]**: Numero di profili esclusi da Adobe Journey Optimizer.

La **[!UICONTROL Email - Tracking statistics]** widget contiene i dati disponibili per l’attività del destinatario per la consegna:

* **[!UICONTROL Opens]**: Numero di volte in cui la consegna è stata aperta in una consegna.

* **[!UICONTROL Unique Opens]**: Percentuale di consegne aperte.

* **[!UICONTROL Open Rate]**: Numero totale di e-mail aperte rispetto al numero di e-mail consegnate.

* **[!UICONTROL Clicks]**: Numero di volte in cui è stato fatto clic su un contenuto in un’e-mail.

* **[!UICONTROL Unique Clicks]**:numero di destinatari che hanno fatto clic su un contenuto in un’e-mail.

* **[!UICONTROL Unique Click Rate]**: Percentuale di utenti che hanno interagito con la consegna.

* **[!UICONTROL Unsubscriptions]**: Numero di clic sul collegamento di annullamento dell’abbonamento.

* **[!UICONTROL Spam complaints]**: Numero di volte in cui un messaggio è stato dichiarato come spam o spazzatura.

La **[!UICONTROL Sending Statistics]** Il grafico contiene i dati disponibili per le e-mail inviate, ad esempio:

* **[!UICONTROL Delivered]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Bounces]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Retries]**: Numero di e-mail in coda per i nuovi tentativi.

* **[!UICONTROL Errors]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

La **[!UICONTROL Bounce Reasons]** e **[!UICONTROL Bounce categories]** I widget contengono i dati disponibili relativi ai messaggi non recapitati, ad esempio:

* **[!UICONTROL Hard bounce]**: Numero totale di errori permanenti, ad esempio un indirizzo e-mail errato. Ciò comporta un messaggio di errore che indica esplicitamente che l’indirizzo non è valido, ad esempio l’utente sconosciuto.

* **[!UICONTROL Soft bounce]**: Numero totale di errori temporanei, ad esempio una casella in entrata completa.

* **[!UICONTROL Ignored]**: Numero totale di temporanei, ad esempio Fuori sede, o un errore tecnico, ad esempio se il tipo di mittente è postmaster.

Per ulteriori informazioni sui messaggi non recapitati, consulta [Elenco di eliminazione](../reports/suppression-list.md) pagina.

La **[!UICONTROL Error Reasons]** grafico e tabella consentono di vedere quale errore si è verificato durante la consegna.

La **[!UICONTROL Excluded reasons]** grafico e tabella mostrano i diversi motivi che impedivano ai profili utente, esclusi dai profili di destinazione, di ricevere il messaggio.

La **[!UICONTROL Email - Top Url]** grafico e tabelle che specificano gli URL della consegna più visitati.

La **[!UICONTROL Email - Top recipient domain]** visualizza i dettagli del grafico e della tabella relativi ai domini più utilizzati dai destinatari per aprire l’e-mail.

>[!NOTE]
>
>La **[!UICONTROL Optimized vs non optimized]** e **[!UICONTROL Send time optimization]**  I widget sono disponibili solo se per la consegna è attivata l’opzione Ottimizzazione del momento di invio . Per ulteriori informazioni sull’ottimizzazione del momento di invio, consulta [questa pagina](../building-journeys/journeys-message.md#send-time-optimization).

La **[!UICONTROL Optimized vs non optimized]** Il grafico descrive le informazioni principali relative al messaggio, siano esse ottimizzate o meno:

* **[!UICONTROL Sent]**: Numero totale di invii per la consegna.
* **[!UICONTROL Opens]**: Numero di volte in cui la consegna è stata aperta in una consegna.
* **[!UICONTROL Clicks]**: Numero di volte in cui è stato fatto clic su un contenuto in un’e-mail.

La **[!UICONTROL Send time optimization]** specifica il successo della consegna in base al metodo di invio: ottimizzato o normale.

* **[!UICONTROL Delivered]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.
* **[!UICONTROL Bounces]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.
+++

## Scheda notifica push {#push-global}

Dalla tua campagna **[!UICONTROL Global report]**, **[!UICONTROL Push notification]** la scheda descrive le informazioni principali relative alle consegne push inviate nella campagna.

![](assets/campaign_report_global_3.png)

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto push.

La **[!UICONTROL Push notification - Sending statistics]** la tabella descrive le informazioni principali relative alle notifiche push con grafici e KPI:

* **[!UICONTROL Targeted]**: Numero totale di messaggi elaborati durante l’analisi della consegna.

* **[!UICONTROL Sent]**: Numero totale di invii per la consegna.

* **[!UICONTROL Delivered]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Delivery Rate]**: Percentuale di messaggi inviati correttamente.

* **[!UICONTROL Bounces]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Bounce Rate]**: Percentuale di notifiche push rimbalzate rispetto alle notifiche push inviate.

* **[!UICONTROL Errors]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

* **[!UICONTROL Error Rate]**: Percentuale di errori che si sono verificati durante una consegna che ne impedisce l’invio rispetto alle notifiche push inviate.

* **[!UICONTROL Excluded]**: Numero di profili esclusi da Adobe Journey Optimizer.

La **[!UICONTROL Push - Tracking statistics]** contiene i dati disponibili per l’attività del destinatario per la consegna:

* **[!UICONTROL Opens]**: Numero di volte in cui un messaggio è stato aperto in una consegna.

* **[!UICONTROL Open Rate]**: Percentuale di notifiche push aperte.

* **[!UICONTROL Actions]**: Numero totale di azioni sulla notifica push consegnata, ad esempio clic su un pulsante o cancellazione.

* **[!UICONTROL Engagements]**: Numero totale di aperture e azioni per questa notifica push, ad esempio se il profilo ha aperto il push o se è stato fatto clic su un pulsante.

* **[!UICONTROL Engagement Rate]**: Percentuale di aperture e azioni per questa notifica push, ad esempio se il profilo ha aperto il push o se è stato fatto clic su un pulsante.

La **[!UICONTROL Push notification summary]** Il grafico contiene i dati disponibili per le notifiche push inviate, ad esempio:

* **[!UICONTROL Opens]**: Numero di volte in cui un messaggio è stato aperto in una consegna.

* **[!UICONTROL Actions]**: Numero totale di azioni sulla notifica push consegnata, ad esempio clic su un pulsante o cancellazione.

* **[!UICONTROL Bounces]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Delivered]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Errors]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

>[!NOTE]
>
>La **[!UICONTROL Optimized vs non optimized]** e **[!UICONTROL Send time optimization]**  I widget sono disponibili solo se per la consegna è attivata l’opzione Ottimizzazione del momento di invio . Per ulteriori informazioni sull’ottimizzazione del momento di invio, consulta [questa pagina](../building-journeys/journeys-message.md#send-time-optimization).

La **[!UICONTROL Optimized vs non optimized]** Il grafico descrive le informazioni principali relative al messaggio, siano esse ottimizzate o meno:

* **[!UICONTROL Delivered]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.
* **[!UICONTROL Opens]**: Numero di volte in cui la consegna è stata aperta in una consegna.
* **[!UICONTROL Actions]**: Numero totale di azioni sulla notifica push consegnata, ad esempio clic su un pulsante o cancellazione.

La **[!UICONTROL Send time optimization]** specifica il successo della consegna in base al metodo di invio: ottimizzato o normale.

* **[!UICONTROL Delivered]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.
* **[!UICONTROL Bounces]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

La **[!UICONTROL Error Reasons]** grafico e tabella consentono di vedere quale errore si è verificato durante la consegna.

La **[!UICONTROL Excluded reasons]** grafico e tabella mostrano i diversi motivi che impedivano ai profili utente, esclusi dai profili di destinazione, di ricevere il messaggio.

La **[!UICONTROL Tracking by platform]**, **[!UICONTROL Sending by platform]** e **[!UICONTROL Breakdown by platform]** grafici e tabelle descrivono il successo della notifica push in base al sistema operativo del destinatario.
+++

## Scheda SMS {#sms-global}

Dalla tua campagna **[!UICONTROL Global report]**, **[!UICONTROL SMS]** la scheda descrive le informazioni principali relative alle consegne SMS inviate nella campagna.

![](assets/campaign_report_global_4.png)

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto SMS.

La **[!UICONTROL SMS - Sending statistics]** la tabella descrive il successo della consegna:

* **[!UICONTROL Targeted]**: Numero di profili utente qualificati come profili di destinazione per questa consegna.

* **[!UICONTROL Excluded]**: Numero di profili utente, esclusi dai profili target, che non hanno ricevuto il messaggio.

* **[!UICONTROL Sent]**: Numero totale di invii per la consegna.

* **[!UICONTROL Delivered]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Bounces]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Errors]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

La **[!UICONTROL SMS Performance by date]** il widget descrive le informazioni principali relative al messaggio con un grafico:

* **[!UICONTROL Sent]**: Numero totale di invii per la consegna.

* **[!UICONTROL Delivered]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Bounces]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Errors]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

La **[!UICONTROL Exclude Reasons]**, **[!UICONTROL Bounces Reasons]** e **[!UICONTROL Error Reasons]** grafici e tabelle ti consentono di vedere quali errori ed esclusioni si sono verificati durante la consegna.
+++

## Risorse aggiuntive

* [Guida introduttiva alle campagne](../campaigns/get-started-with-campaigns.md)
* [Creare una campagna](../campaigns/create-campaign.md)
* [Creare campagne con attivazione API](../campaigns/api-triggered-campaigns.md)
* [Modificare o interrompere una campagna](../campaigns/modify-stop-campaign.md)
* [Report live della campagna](campaign-live-report.md)
