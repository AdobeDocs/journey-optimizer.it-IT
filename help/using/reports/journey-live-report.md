---
solution: Journey Optimizer
product: journey optimizer
title: Rapporto live dei percorsi
description: Scopri come utilizzare i dati del report live del percorso
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: e3781f79-7c8d-4512-b44f-835639b1471f
source-git-commit: 0ec122bbf134c41f95755a3b6f08eb7ef68506df
workflow-type: tm+mt
source-wordcount: '1138'
ht-degree: 5%

---

# Rapporto live dei percorsi {#journey-live-report}

>[!CONTEXTUALHELP]
>id="ajo_journey_live_report"
>title="Rapporto live dei percorsi"
>abstract="Il rapporto live dei percorsi consente di misurare e visualizzare in tempo reale l’impatto e le prestazioni dei percorsi solo nelle ultime 24 ore. Il rapporto è suddiviso in diversi widget che descrivono il successo e gli errori di un percorso. Ogni dashboard di reporting può essere modificata ridimensionando o spostando i widget."

È possibile accedere al rapporto percorso live direttamente dal percorso con **[!UICONTROL Visualizza rapporto]** pulsante .

![](assets/report_journey.png)

Il percorso **[!UICONTROL Report live]** La pagina verrà visualizzata con le seguenti schede:

* [Percorso](#journey-live)
* [E-mail](#email-live)
* [Push](#push-live)
* [SMS](#sms-live)

Il percorso **[!UICONTROL Report live]** è diviso in diversi widget che descrivono il successo e gli errori del tuo percorso. Se necessario, ogni widget può essere ridimensionato ed eliminato. Per ulteriori informazioni, consulta questo [sezione](live-report.md#modify-dashboard).

Per un elenco dettagliato di ciascuna metrica disponibile in Adobe Journey Optimizer, consulta [questa pagina](live-report.md#list-of-components-live).

## scheda percorso {#journey-live}

Dal tuo percorso **[!UICONTROL Report live]**, **[!UICONTROL Percorso]** tab ti offre una visualizzazione chiara dei dati di tracciamento più importanti sul tuo percorso.

![](assets/journey_live_1.png)

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il report di Percorso.

**[!UICONTROL Prestazioni del percorso]** ti consente di visualizzare il percorso dei profili di destinazione passo dopo passo nel percorso.

La **[!UICONTROL Statistiche percorso]** widget visualizza i KPI seguenti:

* **[!UICONTROL Profili inseriti]**: Numero totale di persone che hanno raggiunto l&#39;evento di ingresso del percorso.

* **[!UICONTROL Profili usciti]**: Numero totale di persone uscite dal percorso.

* **[!UICONTROL Singoli percorsi non riusciti]**: Numero totale di singoli percorsi che non sono stati eseguiti correttamente.

La **[!UICONTROL Evento eseguito nelle ultime 24 ore]** e **[!UICONTROL Eventi]** I widget consentono di vedere quale degli eventi è stato eseguito correttamente tramite numero di riepilogo, grafico e tabella.

La **[!UICONTROL Azione eseguita nelle ultime 24 ore]** e **[!UICONTROL Azioni eseguite ed errori]** I widget rappresentano l&#39;azione e gli errori più riusciti che si sono verificati quando le azioni sono state attivate. I numeri di grafico, tabella e riepilogo delle azioni contengono i dati disponibili per le azioni, ad esempio:

* **[!UICONTROL Azioni eseguite]**: Numero totale di azioni eseguite correttamente per un percorso.

* **[!UICONTROL Errore nelle azioni]**: Numero totale di errori che si sono verificati per le azioni.
+++

## Scheda E-mail {#email-live}

Dal tuo percorso **[!UICONTROL Report live]**, **[!UICONTROL E-mail]** scheda descrive le informazioni principali relative alle consegne e-mail inviate nel percorso.

![](assets/journey_live_2.png)

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

>[!NOTE]
>
>I widget e le metriche Offerte sono disponibili solo se una decisione è stata inserita in un’e-mail. Per ulteriori informazioni sulla gestione delle decisioni, consulta questo [page](../offers/get-started/starting-offer-decisioning.md).

La **[!UICONTROL Statistiche sulle offerte]** e **[!UICONTROL Statistiche sulle offerte]** i widget nel tempo misurano il successo e l’impatto dell’offerta sul pubblico di destinazione. Vengono descritte in dettaglio le informazioni principali relative al messaggio con i KPI:

* **[!UICONTROL Offerta inviata]**: Numero totale di invii per l’offerta.

* **[!UICONTROL Immagine dell’offerta]**: Numero di volte in cui l’offerta è stata aperta in una consegna.

* **[!UICONTROL Clic sull’offerta]**: Numero di volte in cui un’offerta è stata selezionata in una consegna.
+++

## Scheda notifica push {#push-live}

Dal tuo percorso **[!UICONTROL Report live]**, **[!UICONTROL Notifica push]** la scheda descrive le informazioni principali relative alle consegne push inviate nel percorso.

![](assets/journey_live_3.png)

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

![](assets/journey_live_4.png)

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto SMS.

La **[!UICONTROL SMS - Invio di statistiche]** la tabella descrive il successo della consegna:

* **[!UICONTROL Target]**: Numero di profili utente qualificati come profili di destinazione per questa consegna.

* **[!UICONTROL Escluso]**: Numero di profili utente, esclusi dai profili target, che non hanno ricevuto il messaggio.

* **[!UICONTROL Inviato]**: Numero totale di invii per la consegna.

* **[!UICONTROL Consegnato]**: Numero di messaggi inviati correttamente.

* **[!UICONTROL Aperture]**: Numero di volte in cui un messaggio è stato aperto in una consegna.

* **[!UICONTROL Clic]**: Numero di volte in cui è stato fatto clic su un contenuto in una consegna.

* **[!UICONTROL Rimbalzi]**: Totale degli errori cumulati durante la consegna e l&#39;elaborazione automatica della restituzione.

* **[!UICONTROL Errori]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

La **[!UICONTROL Riepilogo SMS]** il grafico descrive il successo della consegna:

* **[!UICONTROL Consegnato]**: Numero di messaggi inviati correttamente.

* **[!UICONTROL Rimbalzi]**: Totale degli errori cumulati durante la consegna e l&#39;elaborazione automatica della restituzione.

* **[!UICONTROL Errori]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

La **[!UICONTROL Escludi motivi]** grafici e tabelle ti consentono di vedere quali errori ed esclusioni si sono verificati durante la consegna.
+++
