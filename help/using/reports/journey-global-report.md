---
solution: Journey Optimizer
product: journey optimizer
title: Rapporto globale dei percorsi
description: Scopri come utilizzare i dati del report globale del percorso
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: e851646e-4cef-45e8-97c2-a8f4c9d2cc08
source-git-commit: 4f3d22c9ce3a5b77969a2a04dafbc28b53f95507
workflow-type: tm+mt
source-wordcount: '2044'
ht-degree: 2%

---

# Rapporto globale dei percorsi {#journey-global-report}

>[!CONTEXTUALHELP]
>id="ajo_journey_global_report"
>title="Rapporto globale dei percorsi"
>abstract="Il rapporto globale dei percorsi consente di misurare l’impatto di un percorso in un periodo di tempo selezionato. Il rapporto è suddiviso in diversi widget che descrivono il successo e gli errori di un percorso. Ogni dashboard di reporting può essere modificata ridimensionando o spostando i widget."

È possibile accedere al report globale di percorso direttamente dal percorso con **[!UICONTROL Visualizza rapporto]** pulsante .

![](assets/report_journey.png)

Il percorso **[!UICONTROL Report globale]** La pagina verrà visualizzata con le seguenti schede:

* [Percorso](#journey-global)
* [E-mail](#email-global)
* [Push](#push-global)
* [SMS](#sms-global)

Il percorso **[!UICONTROL Report globale]** è diviso in diversi widget che descrivono il successo e gli errori del tuo percorso. Se necessario, ogni widget può essere ridimensionato ed eliminato. Per ulteriori informazioni, consulta questo [sezione](global-report.md#modify-dashboard).

Per un elenco dettagliato di ciascuna metrica disponibile in Adobe Journey Optimizer, consulta [questa pagina](global-report.md#list-of-components-global).

## scheda percorso {#journey-global}

Dal tuo percorso **[!UICONTROL Report globale]**, **[!UICONTROL Percorso]** tab ti offre una visualizzazione chiara dei dati di tracciamento più importanti sul tuo percorso.

![](assets/journey_global_1.png)

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per i rapporti di Percorso.

La **[!UICONTROL Prestazioni del percorso]** widget consente di visualizzare il percorso dei profili di destinazione passo dopo passo nel percorso.

La **[!UICONTROL Statistiche percorso]** widget visualizza i KPI seguenti:

* **[!UICONTROL Profili inseriti]**: Numero totale di persone che hanno raggiunto l&#39;evento di ingresso del percorso.

* **[!UICONTROL Profili usciti]**: Numero totale di persone uscite dal percorso.

* **[!UICONTROL Percorso singolo non riuscito]**: Numero totale di singoli percorsi che non sono stati eseguiti correttamente.

La **[!UICONTROL Eventi ricevuti per evento]**, **[!UICONTROL Eventi per origine]** e **[!UICONTROL Eventi principali]** i widget consentono di vedere quale dei **[!UICONTROL Eventi]** è stato eseguito correttamente tramite grafici e tabelle.

**[!UICONTROL Prestazioni azione]**, **[!UICONTROL Motivi dell’errore azione]** e **[!UICONTROL Azioni principali]** i widget rappresentano l&#39;azione e gli errori più riusciti che si sono verificati quando **[!UICONTROL Azioni]** sono stati attivati.

La **[!UICONTROL Azioni principali]** la tabella contiene i dati disponibili per **[!UICONTROL Azioni]**, ad esempio:

* **[!UICONTROL Azioni eseguite]**: Numero totale di **[!UICONTROL Azioni]** esecuzione corretta per un percorso.

* **[!UICONTROL Errore in azione]**: Numero totale di errori verificatisi per **[!UICONTROL Azioni]**.

La **[!UICONTROL Criteri di consenso]** tabella e grafico mostrano il numero di profili esclusi da ogni criterio nelle azioni personalizzate.
Per ulteriori informazioni sulle azioni personalizzate, consulta [la documentazione dettagliata](../action/about-custom-action-configuration.md).

Tieni presente che per visualizzare questi widget nei rapporti dei Percorsi, dovrai reimpostare le dashboard. A tale scopo, fai clic su **[!UICONTROL Modifica]** then **[!UICONTROL Reimposta]** in cima al tuo report.
+++

## Scheda E-mail {#email-global}

Dal tuo percorso **[!UICONTROL Report globale]**, **[!UICONTROL E-mail]** scheda descrive le informazioni principali relative alle consegne e-mail inviate nel percorso.

![](assets/journey_global_2.png)

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto E-mail.

La **[!UICONTROL Invio di statistiche per e-mail]** il grafico descrive il successo della consegna:

* **[!UICONTROL Target]**: Numero di profili interessati dal Journey Orchestration di Adobi per qualsiasi azione, ad esempio invia e-mail o SMS.

* **[!UICONTROL Inviato]**: Numero totale di invii per la consegna.

* **[!UICONTROL Consegnato]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Tasso di consegna]**: Percentuale di messaggi inviati correttamente.

* **[!UICONTROL Rimbalzi]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Frequenza di rimbalzo]**: Percentuale di e-mail rimbalzate rispetto alle e-mail inviate.

* **[!UICONTROL Errori]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

* **[!UICONTROL Frequenza errori]**: Percentuale di errori che si sono verificati durante una consegna che ne impedisce l’invio rispetto alle e-mail inviate.

La **[!UICONTROL E-mail - Statistiche di tracciamento]** contiene i dati disponibili per l’attività del destinatario per la consegna:

* **[!UICONTROL Aperture]**: Numero di volte in cui la consegna è stata aperta in una consegna.

* **[!UICONTROL Aperture univoche]**: Percentuale di consegne aperte.

* **[!UICONTROL Open rate univoco]**: Numero totale di e-mail aperte rispetto al numero di e-mail consegnate.

* **[!UICONTROL Clic]**: Numero di volte in cui è stato fatto clic su un contenuto in un’e-mail.

* **[!UICONTROL Clic univoci]**:numero di destinatari che hanno fatto clic su un contenuto in un’e-mail.

* **[!UICONTROL Frequenza di click-through]**: Percentuale di utenti che hanno interagito con il percorso.

* **[!UICONTROL Annulla sottoscrizione]**: Numero di clic sul collegamento di annullamento dell’abbonamento.

* **[!UICONTROL Disturbi dello spam]**: Numero di volte in cui un messaggio è stato dichiarato come spam o spazzatura.

La **[!UICONTROL Invio di statistiche]** Il grafico contiene i dati disponibili per le e-mail inviate, ad esempio:

* **[!UICONTROL Consegnato]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Rimbalzi]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Errori]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

La **[!UICONTROL Ragioni di mancato recapito]** e **[!UICONTROL Categorie di rimbalzi]** I widget contengono i dati disponibili relativi ai messaggi non recapitati, ad esempio:

* **[!UICONTROL Rimbalzo duro]**: Numero totale di errori permanenti, ad esempio un indirizzo e-mail errato. Ciò comporta un messaggio di errore che indica esplicitamente che l’indirizzo non è valido, ad esempio l’utente sconosciuto.

* **[!UICONTROL Rimbalzo morbido]**: Numero totale di errori temporanei, ad esempio una casella in entrata completa.

* **[!UICONTROL Ignorato]**: Numero totale di temporanei, ad esempio Fuori sede, o un errore tecnico, ad esempio se il tipo di mittente è postmaster.

Per ulteriori informazioni sui messaggi non recapitati, consulta [Elenco di eliminazione](../reports/suppression-list.md) pagina.

La **[!UICONTROL Motivi dell’errore]** grafico e tabella consentono di vedere quale errore si è verificato durante la consegna.

La **[!UICONTROL Motivi esclusi]** grafico e tabella mostrano i diversi motivi che impedivano ai profili utente, esclusi dai profili di destinazione, di ricevere il messaggio.

La **[!UICONTROL E-Mail - Url Principale]** grafico e tabelle che specificano gli URL della consegna più visitati.

La **[!UICONTROL E-mail - Dominio principale destinatario]** visualizza i dettagli del grafico e della tabella relativi ai domini più utilizzati dai destinatari per aprire l’e-mail.

>[!NOTE]
>
>La **[!UICONTROL Ottimizzato e non ottimizzato]** e **[!UICONTROL Ottimizzazione del tempo di invio]**  I widget sono disponibili solo se per la consegna è attivata l’opzione Ottimizzazione del momento di invio . Per ulteriori informazioni sull’ottimizzazione del momento di invio, consulta [questa pagina](../building-journeys/journeys-message.md#send-time-optimization).

La **[!UICONTROL Ottimizzato e non ottimizzato]** Il grafico descrive le informazioni principali relative al messaggio, siano esse ottimizzate o meno:

* **[!UICONTROL Inviato]**: Numero totale di invii per la consegna.
* **[!UICONTROL Aperture]**: Numero di volte in cui la consegna è stata aperta in una consegna.
* **[!UICONTROL Clic]**: Numero di volte in cui è stato fatto clic su un contenuto in un’e-mail.

La **[!UICONTROL Ottimizzazione del tempo di invio]** specifica il successo della consegna in base al metodo di invio: ottimizzato o normale.

* **[!UICONTROL Consegnato]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.
* **[!UICONTROL Rimbalzi]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

>[!NOTE]
>
>I widget e le metriche Offerte sono disponibili solo se una decisione è stata inserita in un’e-mail. Per ulteriori informazioni sulla gestione delle decisioni, consulta questo [page](../offers/get-started/starting-offer-decisioning.md).

La **[!UICONTROL Statistiche sulle offerte]** e **[!UICONTROL Statistiche sulle offerte]** i widget nel tempo misurano il successo e l’impatto dell’offerta sul pubblico di destinazione. Vengono descritte in dettaglio le informazioni principali relative al messaggio con i KPI:

* **[!UICONTROL Offerta inviata]**: Numero totale di invii per l’offerta.

* **[!UICONTROL Immagine dell’offerta]**: Numero di volte in cui l’offerta è stata aperta in una consegna.

* **[!UICONTROL Clic sull’offerta]**: Numero di volte in cui un’offerta è stata selezionata in una consegna.

La **[!UICONTROL Offre statistiche dettagliate]** La tabella contiene i dati disponibili per l’attività del destinatario con l’offerta:

* **[!UICONTROL Nome del posizionamento]**: Nome del posizionamento utilizzato per visualizzare l’offerta. Per ulteriori informazioni sul posizionamento, consulta questo [page](../offers/offer-library/creating-placements.md).

* **[!UICONTROL Nome offerta]**: Nome dell’offerta aggiunta nella consegna. Per ulteriori informazioni sul posizionamento, consulta questo [page](../offers/offer-library/creating-personalized-offers.md).

* **[!UICONTROL Offerta inviata]**: Numero totale di invii per l’offerta.

* **[!UICONTROL Tasso di impression dell’offerta]**: Percentuale di offerte aperte rispetto al numero di offerte inviate.

* **[!UICONTROL Frequenza clic offerta]**: Percentuale di utenti che hanno interagito con l’offerta.
+++

## Scheda notifica push {#push-global}

Dal tuo percorso **[!UICONTROL Report globale]**, **[!UICONTROL Notifica push]** la scheda descrive le informazioni principali relative alle consegne push inviate nel percorso.

![](assets/journey_global_3.png)

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto push.

La **[!UICONTROL Notifica push - Invio di statistiche]** la tabella descrive le informazioni principali relative alle notifiche push con grafici e KPI:

* **[!UICONTROL Target]**: Numero di profili interessati dal Journey Orchestration di Adobi per qualsiasi azione, ad esempio invia e-mail o SMS.

* **[!UICONTROL Inviato]**: Numero totale di invii per la consegna.

* **[!UICONTROL Consegnato]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Tasso di consegna]**: Percentuale di messaggi inviati correttamente.

* **[!UICONTROL Rimbalzi]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Frequenza di rimbalzo]**: Percentuale di notifiche push rimbalzate rispetto alle notifiche push inviate.

* **[!UICONTROL Errori]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

* **[!UICONTROL Frequenza errori]**: Percentuale di errori che si sono verificati durante una consegna che ne impedisce l’invio rispetto alle notifiche push inviate.

La **[!UICONTROL Statistiche di tracciamento push]** contiene i dati disponibili per l’attività del destinatario per la consegna:

* **[!UICONTROL Aperture]**: Numero di volte in cui un messaggio è stato aperto in una consegna.

* **[!UICONTROL Open Rate]**: Percentuale di notifiche push aperte.

* **[!UICONTROL Azioni]**: Numero totale di azioni sulla notifica push consegnata, ad esempio clic su un pulsante o cancellazione.

* **[!UICONTROL Coinvolgimento]**: Numero totale di aperture e azioni per questa notifica push, ad esempio se il profilo ha aperto il push o se è stato fatto clic su un pulsante.

* **[!UICONTROL Tasso di coinvolgimento]**: Percentuale di aperture e azioni per questa notifica push, ad esempio se il profilo ha aperto il push o se è stato fatto clic su un pulsante.

La **[!UICONTROL Riepilogo delle notifiche push]** Il grafico contiene i dati disponibili per le notifiche push inviate, ad esempio:

* **[!UICONTROL Aperture]**: Numero di volte in cui un messaggio è stato aperto in una consegna.

* **[!UICONTROL Azioni]**: Numero totale di azioni sulla notifica push consegnata, ad esempio clic su un pulsante o cancellazione.

* **[!UICONTROL Rimbalzi]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Consegnato]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Errori]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

>[!NOTE]
>
>La **[!UICONTROL Ottimizzato e non ottimizzato]** e **[!UICONTROL Ottimizzazione del tempo di invio]**  I widget sono disponibili solo se per la consegna è attivata l’opzione Ottimizzazione del momento di invio . Per ulteriori informazioni sull’ottimizzazione del momento di invio, consulta [questa pagina](../building-journeys/journeys-message.md#send-time-optimization).

La **[!UICONTROL Ottimizzato e non ottimizzato]** Il grafico descrive le informazioni principali relative al messaggio, siano esse ottimizzate o meno:

* **[!UICONTROL Consegnato]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.
* **[!UICONTROL Aperture]**: Numero di volte in cui la consegna è stata aperta in una consegna.
* **[!UICONTROL Azioni]**: Numero totale di azioni sulla notifica push consegnata, ad esempio clic su un pulsante o cancellazione.

La **[!UICONTROL Ottimizzazione del tempo di invio]** specifica il successo della consegna in base al metodo di invio: ottimizzato o normale.

* **[!UICONTROL Consegnato]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.
* **[!UICONTROL Rimbalzi]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

La **[!UICONTROL Motivi dell’errore]** grafico e tabella consentono di vedere quale errore si è verificato durante la consegna.

La **[!UICONTROL Motivi esclusi]** grafico e tabella mostrano i diversi motivi che impedivano ai profili utente, esclusi dai profili di destinazione, di ricevere il messaggio.

La **[!UICONTROL Tracciamento per piattaforma]**, **[!UICONTROL Invio per piattaforma]** e **[!UICONTROL Suddivisione per piattaforma]** grafici e tabelle descrivono il successo della notifica push in base al sistema operativo del destinatario.

SMS **[!UICONTROL Report globale]** è suddiviso in diversi widget che descrivono in dettaglio il successo e gli errori della consegna. Se necessario, ogni widget può essere ridimensionato ed eliminato. Per ulteriori informazioni su questo consulta [sezione](global-report.md#modify-dashboard).
+++

## Scheda SMS {#sms-global}

![](assets/journey_global_4.png)

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto SMS.

La **[!UICONTROL SMS - Invio di statistiche]** la tabella descrive il successo della consegna:

* **[!UICONTROL Target]**: Numero di profili utente qualificati come profili di destinazione per questa consegna.

* **[!UICONTROL Escluso]**: Numero di profili utente, esclusi dai profili target, che non hanno ricevuto il messaggio.

* **[!UICONTROL Inviato]**: Numero totale di invii per la consegna.

* **[!UICONTROL Consegnato]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Rimbalzi]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Errori]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

La **[!UICONTROL Riepilogo SMS]** il widget descrive le informazioni principali relative al messaggio con un grafico:

* **[!UICONTROL Inviato]**: Numero totale di invii per la consegna.

* **[!UICONTROL Consegnato]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Rimbalzi]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Errori]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

La **[!UICONTROL Escludi motivi]** grafici e tabelle ti consentono di vedere quali errori ed esclusioni si sono verificati durante la consegna.

La **[!UICONTROL SMS - Clic tramite collegamenti]** e **[!UICONTROL SMS - Statistiche di tracciamento]** I widget descrivono nel dettaglio le informazioni principali relative al coinvolgimento dei visitatori con gli URL.

+++
