---
title: Rapporto globale dei percorsi
description: Scopri come utilizzare i dati del report globale del percorso
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: e851646e-4cef-45e8-97c2-a8f4c9d2cc08
source-git-commit: 40c42303b8013c1d9f4dd214ab1acbec2942e094
workflow-type: tm+mt
source-wordcount: '1242'
ht-degree: 0%

---

# Rapporto globale dei percorsi {#journey-global-report}

È possibile accedere al report globale di percorso direttamente dal percorso con **[!UICONTROL Global report]** pulsante .

![](assets/global_report_1.png)

Il percorso **[!UICONTROL Global report]** La pagina verrà visualizzata con le seguenti schede:

* [Percorso](#journey-global)
* [E-mail](#email-global)
* [Push](#push-global)

Il percorso **[!UICONTROL Global report]** è diviso in diversi widget che descrivono il successo e gli errori del tuo percorso. Se necessario, ogni widget può essere ridimensionato ed eliminato. Per ulteriori informazioni, consulta questo [sezione](global-report.md#modify-dashboard).

## scheda percorso {#journey-global}

Dal tuo percorso **[!UICONTROL Global report]**, **[!UICONTROL Journey]** tab ti offre una visualizzazione chiara dei dati di tracciamento più importanti sul tuo percorso.

![](assets/global_report_2.png)

La **[!UICONTROL Journey Performance]** widget consente di visualizzare il percorso dei profili di destinazione passo dopo passo nel percorso.

La **[!UICONTROL Journey Statistics]** widget visualizza i KPI seguenti:

* **[!UICONTROL Entered profiles]**: Numero totale di persone che hanno raggiunto l&#39;evento di ingresso del percorso.

* **[!UICONTROL Exited profiles]**: Numero totale di persone uscite dal percorso.

* **[!UICONTROL Failed individual journey]**: Numero totale di singoli percorsi che non sono stati eseguiti correttamente.

![](assets/global_report_12.png)

La **[!UICONTROL Events received by event]**, **[!UICONTROL Events by origin]** e **[!UICONTROL Top events]** i widget consentono di vedere quale dei **[!UICONTROL Events]** è stato eseguito correttamente tramite grafici e tabelle.

![](assets/global_report_13.png)

**[!UICONTROL Action Performance]**, **[!UICONTROL Action Error Reasons]** e **[!UICONTROL Top Actions]** i widget rappresentano l&#39;azione e gli errori più riusciti che si sono verificati quando **[!UICONTROL Actions]** sono stati attivati.

La **[!UICONTROL Top Actions]** la tabella contiene i dati disponibili per **[!UICONTROL Actions]**, ad esempio:

* **[!UICONTROL Actions successfully executed]**: Numero totale di **[!UICONTROL Actions]** esecuzione corretta per un percorso.

* **[!UICONTROL Error in action]**: Numero totale di errori verificatisi per **[!UICONTROL Actions]**.

## Scheda E-mail {#email-global}

Dal tuo percorso **[!UICONTROL Global report]**, **[!UICONTROL Email]** scheda descrive le informazioni principali relative alle consegne e-mail inviate nel percorso.

Per un rapporto dettagliato su una consegna e-mail specifica, consulta la sezione [Report globale e-mail](#email-global-report) sezione .

![](assets/global_report_14.png)

La **[!UICONTROL Email Sending Statistics]** il grafico descrive il successo della consegna:

* **[!UICONTROL Sent]**: Numero totale di invii per la consegna.

* **[!UICONTROL Delivered]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Delivery Rate]**: Percentuale di messaggi inviati correttamente.

* **[!UICONTROL Bounces]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Bounce Rate]**: Percentuale di e-mail rimbalzate rispetto alle e-mail inviate.

* **[!UICONTROL Errors]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

* **[!UICONTROL Error Rate]**: Percentuale di errori che si sono verificati durante una consegna che ne impedisce l’invio rispetto alle e-mail inviate.

La **[!UICONTROL Email - Tracking statistics]** contiene i dati disponibili per l’attività del destinatario per la consegna:

* **[!UICONTROL Opens]**: Numero di volte in cui la consegna è stata aperta in una consegna.

* **[!UICONTROL Unique Opens]**: Percentuale di consegne aperte.

* **[!UICONTROL Open Rate]**: Numero totale di e-mail aperte rispetto al numero di e-mail consegnate.

* **[!UICONTROL Clicks]**: Numero di volte in cui è stato fatto clic su un contenuto in un’e-mail.

* **[!UICONTROL Unique Clicks]**:numero di destinatari che hanno fatto clic su un contenuto in un’e-mail.

* **[!UICONTROL Click through rate]**: Percentuale di utenti che hanno interagito con il percorso.

* **[!UICONTROL Unsubscribe]**: Numero di clic sul collegamento di annullamento dell’abbonamento.

* **[!UICONTROL Spam complaints]**: Numero di volte in cui un messaggio è stato dichiarato come spam o spazzatura.

La **[!UICONTROL Sending Statistics]** Il grafico contiene i dati disponibili per le e-mail inviate, ad esempio:

* **[!UICONTROL Delivered]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Bounces]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Errors]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

![](assets/global_report_15.png)

La **[!UICONTROL Bounce Reasons]** e **[!UICONTROL Bounce categories]** I widget contengono i dati disponibili relativi ai messaggi non recapitati, ad esempio:

* **[!UICONTROL Hard bounce]**: Numero totale di errori permanenti, ad esempio un indirizzo e-mail errato. Ciò comporta un messaggio di errore che indica esplicitamente che l’indirizzo non è valido, ad esempio l’utente sconosciuto.

* **[!UICONTROL Soft bounce]**: Numero totale di errori temporanei, ad esempio una casella in entrata completa.

* **[!UICONTROL Ignored]**: Numero totale di temporanei, ad esempio Fuori sede, o un errore tecnico, ad esempio se il tipo di mittente è postmaster.

Per ulteriori informazioni sui messaggi non recapitati, consulta [Elenco di eliminazione](../reports/suppression-list.md) pagina.

![](assets/global_report_22.png)

La **[!UICONTROL Error Reasons]** grafico e tabella consentono di vedere quale errore si è verificato durante la consegna.

La **[!UICONTROL Excluded reasons]** grafico e tabella mostrano i diversi motivi che impedivano ai profili utente, esclusi dai profili di destinazione, di ricevere il messaggio.

![](assets/global_report_16.png)

La **[!UICONTROL Email - Top Url]** grafico e tabelle che specificano gli URL della consegna più visitati.

La **[!UICONTROL Email - Top recipient domain]** visualizza i dettagli del grafico e della tabella relativi ai domini più utilizzati dai destinatari per aprire l’e-mail.

![](assets/global_report_23.png)

>[!NOTE]
>
>La **[!UICONTROL Optimized vs non optimized]** e **[!UICONTROL Send time optimization]**  I widget sono disponibili solo se per la consegna è attivata l’opzione Ottimizzazione del momento di invio . Per ulteriori informazioni sull’ottimizzazione del momento di invio, consulta questo [page](../building-journeys/journeys-message.md#send-time-optimization).

La **[!UICONTROL Optimized vs non optimized]** Il grafico descrive le informazioni principali relative al messaggio, siano esse ottimizzate o meno:

* **[!UICONTROL Sent]**: Numero totale di invii per la consegna.
* **[!UICONTROL Opens]**: Numero di volte in cui la consegna è stata aperta in una consegna.
* **[!UICONTROL Clicks]**: Numero di volte in cui è stato fatto clic su un contenuto in un’e-mail.

La **[!UICONTROL Send time optimization]** specifica il successo della consegna in base al metodo di invio: ottimizzato o normale.

* **[!UICONTROL Delivered]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.
* **[!UICONTROL Bounces]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

<!--
![](assets/global_report_21.png)

>[!NOTE]
>
>The Offers widgets and metrics are only available if a decision was inserted in an email. For more information on Decision Management, refer to this [page](../offers/get-started/starting-offer-decisioning.md).

The **[!UICONTROL Offers statistic]** and **[!UICONTROL Offers statistics]** over time widgets measure your offer's success and impact on your targeted audience. It detail the main information relative to your message with KPIs:

* **[!UICONTROL Offer sent]**: Total number of sends for the offer.

* **[!UICONTROL Offer impression]**: Number of times the offer was opened in a delivery.

* **[!UICONTROL Offer clicks]**: Number of times an offer was clicked on in a delivery.

The **[!UICONTROL Offers detailed statistic]** table contains the available data for recipient activity with your offer:

* **[!UICONTROL Placement name]**: Name of your placement used to display your offer. For more information on placement, refer to this [page](../offers/offer-library/creating-placements.md).

* **[!UICONTROL Offer name]**: Name of the offer added in the delivery. For more information on placement, refer to this [page](../offers/offer-library/creating-personalized-offers.md).

* **[!UICONTROL Offer sent]**: Total number of sends for the offer.

* **[!UICONTROL Offer impression rate]**: Percentage of opened offers compared to the number of sent offers.

* **[!UICONTROL Offer click rate]**: Percentage of users who interacted with the offer.
-->

## Scheda push {#push-global}

Dal tuo percorso **[!UICONTROL Global report]**, **[!UICONTROL Push]** la scheda descrive le informazioni principali relative alle consegne push inviate nel percorso.

Per un rapporto dettagliato su una consegna push specifica, consulta la sezione [Report globale push](#push-global-report).

![](assets/global_report_17.png)

La **[!UICONTROL Push notification - Sending statistics]** la tabella descrive le informazioni principali relative alle notifiche push con grafici e KPI:

* **[!UICONTROL Sent]**: Numero totale di invii per la consegna.

* **[!UICONTROL Delivered]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Delivery Rate]**: Percentuale di messaggi inviati correttamente.

* **[!UICONTROL Bounces]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Bounce Rate]**: Percentuale di notifiche push rimbalzate rispetto alle notifiche push inviate.

* **[!UICONTROL Errors]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

* **[!UICONTROL Error Rate]**: Percentuale di errori che si sono verificati durante una consegna che ne impedisce l’invio rispetto alle notifiche push inviate.

La **[!UICONTROL Push - Tracking statistics]** contiene i dati disponibili per l’attività del destinatario per la consegna:

* **[!UICONTROL Opens]**: Numero di volte in cui un messaggio è stato aperto in una consegna.

* **[!UICONTROL Open Rate]**: Percentuale di notifiche push aperte.

* **[!UICONTROL Actions]**: Numero totale di azioni sulla notifica push consegnata, ad esempio clic su un pulsante o cancellazione.

* **[!UICONTROL Engagements]**: Numero totale di aperture e azioni per questa notifica push, ad esempio se il profilo ha aperto il push o se è stato fatto clic su un pulsante.

* **[!UICONTROL Engagement Rate]**: Percentuale di aperture e azioni per questa notifica push, ad esempio se il profilo ha aperto il push o se è stato fatto clic su un pulsante.

![](assets/global_report_24.png)

La **[!UICONTROL Push notification summary]** Il grafico contiene i dati disponibili per le notifiche push inviate, ad esempio:

* **[!UICONTROL Opens]**: Numero di volte in cui un messaggio è stato aperto in una consegna.

* **[!UICONTROL Actions]**: Numero totale di azioni sulla notifica push consegnata, ad esempio clic su un pulsante o cancellazione.

* **[!UICONTROL Bounces]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Delivered]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Errors]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

>[!NOTE]
>
>La **[!UICONTROL Optimized vs non optimized]** e **[!UICONTROL Send time optimization]**  I widget sono disponibili solo se per la consegna è attivata l’opzione Ottimizzazione del momento di invio . Per ulteriori informazioni sull’ottimizzazione del momento di invio, consulta questo [page](../building-journeys/journeys-message.md#send-time-optimization).

La **[!UICONTROL Optimized vs non optimized]** Il grafico descrive le informazioni principali relative al messaggio, siano esse ottimizzate o meno:

* **[!UICONTROL Delivered]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.
* **[!UICONTROL Opens]**: Numero di volte in cui la consegna è stata aperta in una consegna.
* **[!UICONTROL Actions]**: Numero totale di azioni sulla notifica push consegnata, ad esempio clic su un pulsante o cancellazione.

La **[!UICONTROL Send time optimization]** specifica il successo della consegna in base al metodo di invio: ottimizzato o normale.

* **[!UICONTROL Delivered]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.
* **[!UICONTROL Bounces]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

![](assets/global_report_18.png)

La **[!UICONTROL Error Reasons]** grafico e tabella consentono di vedere quale errore si è verificato durante la consegna.

La **[!UICONTROL Excluded reasons]** grafico e tabella mostrano i diversi motivi che impedivano ai profili utente, esclusi dai profili di destinazione, di ricevere il messaggio.

![](assets/global_report_19.png)

La **[!UICONTROL Tracking by platform]**, **[!UICONTROL Sending by platform]** e **[!UICONTROL Breakdown by platform]** grafici e tabelle descrivono il successo della notifica push in base al sistema operativo del destinatario.
