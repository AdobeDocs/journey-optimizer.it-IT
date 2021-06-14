---
title: Rapporto globale dei percorsi
description: Scopri come utilizzare i dati del report globale del percorso
feature: Reporting
topic: Gestione dei contenuti
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '936'
ht-degree: 1%

---

# Rapporto globale dei percorsi {#journey-global-report}

![](../assets/do-not-localize/badge.png)

Puoi accedere al report globale di percorso direttamente dal tuo percorso con il pulsante **[!UICONTROL Global report]** .

![](../assets/global_report_1.png)

La pagina percorso **[!UICONTROL Global report]** verrà visualizzata con le seguenti schede:

* [Percorso](#journey-global)
* [E-mail](#email-global)
* [Push](#push-global)

Il percorso **[!UICONTROL Global report]** è suddiviso in diversi widget che descrivono il successo e gli errori del percorso. Se necessario, ogni widget può essere ridimensionato ed eliminato. Per ulteriori informazioni, consulta questa [sezione](global-report.md#modify-dashboard).

## Scheda percorso {#journey-global}

Dal percorso **[!UICONTROL Global report]**, la scheda **[!UICONTROL Journey]** ti offre una visualizzazione chiara dei dati di tracciamento più importanti sul percorso.

![](../assets/global_report_2.png)

Il widget **[!UICONTROL Journey`s performance]** ti consente di visualizzare il percorso dei profili di destinazione passo per passo nel percorso.

Il widget **[!UICONTROL Journey`s statistics]** visualizza i KPI seguenti:

* **[!UICONTROL Entered profiles]**: Numero totale di persone che hanno raggiunto l&#39;evento di ingresso del percorso.

* **[!UICONTROL Exited profiles]**: Numero totale di persone uscite dal percorso.

* **[!UICONTROL Failed individual journey]**: Numero totale di singoli percorsi che non sono stati eseguiti correttamente.

I widget **[!UICONTROL Event Performance]** e **[!UICONTROL Top events]** consentono di vedere quale dei **[!UICONTROL Events]** è stato eseguito correttamente tramite grafici e tabelle.

**[!UICONTROL Action Performance]** e  **[!UICONTROL Top Actions]** i widget rappresentano l&#39;azione e gli errori più riusciti che si verificavano quando  **[!UICONTROL Actions]** venivano attivati. La tabella **[!UICONTROL Top Actions]** contiene i dati disponibili per **[!UICONTROL Actions]**, ad esempio:

* **[!UICONTROL Actions successfully executed]**: Numero totale di esecuzioni  **[!UICONTROL Actions]** completate per un percorso.

* **[!UICONTROL Error in action]**: Numero totale di errori verificatisi per  **[!UICONTROL Actions]**.

Il grafico **[!UICONTROL Error Reasons]** descrive il tipo di errori che si sono verificati per **[!UICONTROL Actions]**.

<!--Events by origin-->

## Scheda E-mail {#email-global}

Dal percorso **[!UICONTROL Global report]**, la scheda **[!UICONTROL Email]** descrive le informazioni principali relative alle consegne e-mail inviate nel percorso.

Per un rapporto dettagliato su una consegna e-mail specifica, consulta la sezione [Rapporto globale e-mail](#email-global-report) .

Il grafico **[!UICONTROL Email Sending Statistics]** descrive il successo della consegna:

* **[!UICONTROL Sent]**: Numero totale di invii per la consegna.

* **[!UICONTROL Delivered]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Delivery Rate]**: Percentuale di messaggi inviati correttamente.

* **[!UICONTROL Bounces]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Bounce Rate]**: Percentuale di e-mail rimbalzate rispetto alle e-mail inviate.

* **[!UICONTROL Errors]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

* **[!UICONTROL Error Rate]**: Percentuale di errori che si sono verificati durante una consegna che ne impedisce l’invio rispetto alle e-mail inviate.

Il **[!UICONTROL Email - Tracking statistics]** contiene i dati disponibili per l’attività del destinatario per la consegna:

* **[!UICONTROL Opens]**: Numero di volte in cui la consegna è stata aperta in una consegna.

* **[!UICONTROL Unique Opens]**: Percentuale di consegne aperte.

* **[!UICONTROL Open Rate]**: Numero totale di e-mail aperte rispetto al numero di e-mail consegnate.

* **[!UICONTROL Clicks]**: Numero di volte in cui è stato fatto clic su un contenuto in un’e-mail.

* **[!UICONTROL Unique Clicks]**:numero di destinatari che hanno fatto clic su un contenuto in un’e-mail.

* **[!UICONTROL Click through rate]**: Percentuale di utenti che hanno interagito con il percorso.

Il grafico **[!UICONTROL Sending Statistics]** contiene i dati disponibili per le e-mail inviate, ad esempio:

* **[!UICONTROL Delivered]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Bounces]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Errors]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

I widget **[!UICONTROL Bounce Reasons]** e **[!UICONTROL Bounce categories]** contengono i dati disponibili relativi ai messaggi non recapitati, ad esempio:

* **[!UICONTROL Hard bounce]**: Numero totale di errori permanenti, ad esempio un indirizzo e-mail errato. Ciò comporta un messaggio di errore che indica esplicitamente che l’indirizzo non è valido, ad esempio l’utente sconosciuto.

* **[!UICONTROL Soft bounce]**: Numero totale di errori temporanei, ad esempio una casella in entrata completa.

* **[!UICONTROL Ignored]**: Numero totale di temporanei, ad esempio Fuori sede, o un errore tecnico, ad esempio se il tipo di mittente è postmaster.

Per ulteriori informazioni sui messaggi non recapitati, consulta la pagina [Elenco di eliminazione](../suppression-list.md) .

Il grafico e la tabella **[!UICONTROL Email - Top Url]** mostrano gli URL della consegna più visitati.

Il grafico **[!UICONTROL Email - Best recipient domain]** e la tabella mostrano i dettagli dei domini più utilizzati dai destinatari per aprire l’e-mail.

## Scheda push {#push-global}

Dal percorso **[!UICONTROL Global report]**, la scheda **[!UICONTROL Push]** descrive le informazioni principali relative alle consegne push inviate nel percorso.

Per un rapporto dettagliato su una consegna push specifica, consulta il [Rapporto globale push](#push-global-report).

La tabella **[!UICONTROL Push notification - Sending statistics]** descrive le informazioni principali relative alle notifiche push con grafici e KPI:

* **[!UICONTROL Sent]**: Numero totale di invii per la consegna.

* **[!UICONTROL Delivered]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Delivery Rate]**: Percentuale di messaggi inviati correttamente.

* **[!UICONTROL Bounces]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Bounce Rate]**: Percentuale di notifiche push rimbalzate rispetto alle notifiche push inviate.

* **[!UICONTROL Errors]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

* **[!UICONTROL Error Rate]**: Percentuale di errori che si sono verificati durante una consegna che ne impedisce l’invio rispetto alle notifiche push inviate.

Il **[!UICONTROL Push - Tracking statistics]** contiene i dati disponibili per l’attività del destinatario per la consegna:

* **[!UICONTROL Opens]**: Numero di volte in cui un messaggio è stato aperto in una consegna.

* **[!UICONTROL Open Rate]**: Percentuale di notifiche push aperte.

* **[!UICONTROL Actions]**: Numero totale di azioni sulla notifica push consegnata, ad esempio clic su un pulsante o cancellazione.

* **[!UICONTROL Engagements]**: Numero totale di aperture e azioni per questa notifica push, ad esempio se il profilo ha aperto il push o se è stato fatto clic su un pulsante.

* **[!UICONTROL Engagement Rate]**: Percentuale di aperture e azioni per questa notifica push, ad esempio se il profilo ha aperto il push o se è stato fatto clic su un pulsante.

Il grafico **[!UICONTROL Push notification summary]** contiene i dati disponibili per le notifiche push inviate, ad esempio:

* **[!UICONTROL Opens]**: Numero di volte in cui un messaggio è stato aperto in una consegna.

* **[!UICONTROL Actions]**: Numero totale di azioni sulla notifica push consegnata, ad esempio clic su un pulsante o cancellazione.

* **[!UICONTROL Bounces]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Delivered]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Errors]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

Il grafico e la tabella **[!UICONTROL Error Reasons]** ti consentono di vedere quale errore si è verificato durante la consegna.

I grafici e le tabelle **[!UICONTROL Tracking by platform]**, **[!UICONTROL Sending by platform]** e **[!UICONTROL Breakdown by platform]** descrivono in dettaglio il successo della notifica push in base al sistema operativo del destinatario.
