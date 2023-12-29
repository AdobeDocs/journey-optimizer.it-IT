---
solution: Journey Optimizer
product: journey optimizer
title: Rapporto globale dei percorsi
description: Scopri come utilizzare i dati del rapporto globale del percorso
feature: Reporting, Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: e851646e-4cef-45e8-97c2-a8f4c9d2cc08
source-git-commit: 523c0cf8dd32eb9a1d2616258a7f5a142fd3499c
workflow-type: tm+mt
source-wordcount: '2395'
ht-degree: 18%

---

# Rapporto globale dei percorsi {#journey-global-report}

>[!CONTEXTUALHELP]
>id="ajo_journey_global_report"
>title="Rapporto globale dei percorsi"
>abstract="Il rapporto globale dei percorsi consente di misurare l’impatto di un percorso in un periodo di tempo selezionato. Il rapporto è suddiviso in diversi widget che descrivono il successo e gli errori di un percorso. Ogni dashboard di reporting può essere modificata ridimensionando o spostando i widget."

I report globali, accessibili dalla scheda Tutto il tempo, visualizzano gli eventi che si sono verificati almeno due ore fa e coprono gli eventi relativi a un periodo di tempo selezionato. Al confronto, i rapporti live si concentrano sugli eventi che si sono verificati nelle ultime 24 ore, con un intervallo di tempo minimo di due minuti dall’occorrenza dell’evento.

Il rapporto globale del percorso è accessibile direttamente dal percorso con **[!UICONTROL Visualizza rapporto]** pulsante.

![](assets/report_journey.png)

Il percorso **[!UICONTROL Rapporto globale]** La pagina verrà visualizzata con le seguenti schede:

* [Percorso](#journey-global)
* [E-mail](#email-global)
* [Push](#push-global)
* [SMS](#sms-global)
* [In-app](#in-app-global)

Il percorso **[!UICONTROL Rapporto globale]** è diviso in diversi widget che descrivono nel dettaglio il successo e gli errori del percorso. Ogni widget può essere ridimensionato ed eliminato, se necessario. Per ulteriori informazioni, consulta questa [sezione](global-report.md#modify-dashboard).

Per un elenco dettagliato di tutte le metriche disponibili in Adobe Journey Optimizer, consulta [questa pagina](global-report.md#list-of-components-global).

## Scheda percorso {#journey-global}

Dal tuo percorso **[!UICONTROL Rapporto globale]**, il **[!UICONTROL Percorso]** fornisce una visualizzazione chiara dei dati di tracciamento più importanti sul percorso.

![](assets/journey_global_1.png)

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per i rapporti sui Percorsi.

Il **[!UICONTROL Prestazioni percorso]** Il widget consente di visualizzare il percorso dei profili di destinazione passo dopo passo nel percorso.

Il **[!UICONTROL Statistiche percorso]** Il widget visualizza i KPI seguenti:

* **[!UICONTROL Profili immessi]**: numero totale di individui che hanno raggiunto l’evento di ingresso del percorso.

* **[!UICONTROL Profili in uscita]**: numero totale di individui che sono usciti dal percorso.

* **[!UICONTROL Singolo percorso non riuscito]**: numero totale di singoli percorsi non eseguiti correttamente.

Il **[!UICONTROL Eventi ricevuti per evento]**, **[!UICONTROL Eventi per origine]** e **[!UICONTROL Eventi principali]** i widget consentono di vedere quale dei **[!UICONTROL Eventi]** è stato eseguito correttamente tramite grafici e tabella.

**[!UICONTROL Prestazioni azione]**, **[!UICONTROL Motivi di errore azione]** e **[!UICONTROL Azioni principali]** i widget rappresentano l&#39;azione e gli errori più riusciti che si sono verificati quando **[!UICONTROL Azioni]** sono stati attivati.

Il **[!UICONTROL Azioni principali]** la tabella contiene i dati disponibili per **[!UICONTROL Azioni]**, ad esempio:

* **[!UICONTROL Azioni eseguite correttamente]**: numero totale di **[!UICONTROL Azioni]** eseguito correttamente per un percorso.

* **[!UICONTROL Errore nell’azione]**: numero totale di errori che si sono verificati per **[!UICONTROL Azioni]**.

Il **[!UICONTROL Criteri di consenso]** la tabella e il grafico mostrano il numero di profili esclusi da ciascun criterio nelle azioni personalizzate.
Per ulteriori informazioni sulle azioni personalizzate, consulta [la documentazione dettagliata](../action/about-custom-action-configuration.md).

Tieni presente che affinché questi widget vengano visualizzati nei rapporti Percorsi, dovrai reimpostare le dashboard. A tale scopo, fai clic su **[!UICONTROL Modifica]** allora **[!UICONTROL Reimposta]** nella parte superiore del report.
+++

## Scheda e-mail {#email-global}

Dal tuo percorso **[!UICONTROL Rapporto globale]**, il **[!UICONTROL E-mail]** La scheda fornisce informazioni dettagliate sulle informazioni principali relative alle consegne e-mail inviate nel tuo percorso.

![](assets/journey_global_2.png)

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto e-mail.

Il **[!UICONTROL Statistiche di invio e-mail]** il grafico descrive il successo della consegna:

* **[!UICONTROL Tempo di esecuzione]**: ora di inizio di ogni esecuzione del percorso in caso di percorsi ricorrenti. Per eseguire il targeting di una o più ricorrenze, selezionatela dal **[!UICONTROL Tempo di esecuzione]** a discesa.

* **[!UICONTROL Target]**: numero di profili target per qualsiasi azione, ad esempio invio di e-mail o SMS.

* **[!UICONTROL Inviato]**: numero totale di invii per la consegna.

* **[!UICONTROL Consegnato]**: numero di messaggi inviati correttamente rispetto al numero totale di messaggi inviati.

* **[!UICONTROL Percentuale di consegna]**: percentuale di messaggi inviati correttamente.

* **[!UICONTROL Mancati recapiti]**: totale degli errori accumulati durante la consegna e l’elaborazione automatica dei messaggi restituiti rispetto al numero totale di messaggi inviati.

* **[!UICONTROL Percentuale non recapitate]**: percentuale di e-mail non recapitate rispetto alle e-mail inviate.

* **[!UICONTROL Errori]**: numero totale di errori che si sono verificati durante una consegna e che ne hanno impedito l’invio ai profili.

* **[!UICONTROL Frequenza errori]**: percentuale di errori che si sono verificati durante una consegna che ne ha impedito l’invio, rispetto alle e-mail inviate.

Il **[!UICONTROL E-mail - Statistiche di tracciamento]** contiene i dati disponibili per l’attività del destinatario per la consegna:

* **[!UICONTROL Tempo di esecuzione]**: ora di inizio di ogni esecuzione dell’e-mail ricorrente nel percorso. Per eseguire il targeting di una o più e-mail ricorrenti, selezionala dall’opzione **[!UICONTROL Tempo di esecuzione]** a discesa.

* **[!UICONTROL Aperture]**: numero di volte in cui la consegna è stata aperta in una consegna.

* **[!UICONTROL Aperture univoche]**: percentuale di consegne aperte.

* **[!UICONTROL Percentuale aperture univoche]**: numero totale di e-mail aperte rispetto al numero di e-mail consegnate.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto in un’e-mail.

* **[!UICONTROL Clic univoci]**: numero di destinatari che hanno fatto clic su un contenuto in un’e-mail.

* **[!UICONTROL Percentuale di click-through]**: percentuale di utenti che hanno interagito con il percorso.

* **[!UICONTROL Annulla iscrizione]**: numero di clic sul collegamento di annullamento dell’abbonamento.

* **[!UICONTROL Reclami spam]**: numero di volte in cui un messaggio è stato dichiarato come spam o posta indesiderata.

Il **[!UICONTROL Statistiche di invio]** il grafico contiene i dati disponibili per le e-mail inviate, ad esempio:

* **[!UICONTROL Consegnato]**: numero di messaggi inviati correttamente rispetto al numero totale di messaggi inviati.

* **[!UICONTROL Mancati recapiti]**: totale degli errori accumulati durante la consegna e l’elaborazione automatica dei messaggi restituiti rispetto al numero totale di messaggi inviati.

* **[!UICONTROL Errori]**: numero totale di errori che si sono verificati durante una consegna e che ne hanno impedito l’invio ai profili.

Il **[!UICONTROL Motivi di mancato recapito]** e **[!UICONTROL Categorie di mancato recapito]** I widget contengono i dati disponibili relativi ai messaggi non recapitati, ad esempio:

* **[!UICONTROL Mancato recapito permanente]**: numero totale di errori permanenti, ad esempio un indirizzo e-mail errato. Ciò comporta un messaggio di errore che indica esplicitamente che l’indirizzo non è valido, ad esempio Utente sconosciuto.

* **[!UICONTROL Mancato recapito non permanente]**: numero totale di errori temporanei, ad esempio una casella in entrata completa.

* **[!UICONTROL Ignorato]**: numero totale di messaggi temporanei, ad esempio Fuori sede, o un errore tecnico, ad esempio se il tipo di mittente è postmaster.

Per ulteriori informazioni sui mancati recapiti, consulta [Elenco di soppressione](../reports/suppression-list.md) pagina.

Il **[!UICONTROL Motivi di errore]** grafico e tabella ti consentono di vedere quale errore si è verificato durante la consegna.

Il **[!UICONTROL Motivi di esclusione]** il grafico e la tabella mostrano i diversi motivi che hanno impedito ai profili utente, esclusi dai profili target, di ricevere il messaggio.

Il **[!UICONTROL E-Mail - URL principale]** il grafico e la tabella indicano gli URL più visitati della consegna.

Il **[!UICONTROL E-mail - Dominio destinatario principale]** il grafico e la tabella indicano i domini più utilizzati dai destinatari per aprire l’e-mail.

>[!NOTE]
>
>Il **[!UICONTROL Ottimizzato e non ottimizzato]** e **[!UICONTROL Ottimizzazione del tempo di invio]**  I widget sono disponibili solo se per la consegna è attivata l’opzione Ottimizzazione ora di invio. Per ulteriori informazioni sull’ottimizzazione dell’ora di invio, consulta [questa pagina](../building-journeys/journeys-message.md#send-time-optimization).

Il **[!UICONTROL Ottimizzato e non ottimizzato]** il grafico descrive le informazioni principali relative al messaggio, ottimizzate o meno:

* **[!UICONTROL Inviato]**: numero totale di invii per la consegna.
* **[!UICONTROL Aperture]**: numero di volte in cui la consegna è stata aperta in una consegna.
* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto in un’e-mail.

Il **[!UICONTROL Ottimizzazione del tempo di invio]** descrive il successo della consegna in base al metodo di invio: ottimizzato o normale.

* **[!UICONTROL Consegnato]**: numero di messaggi inviati correttamente rispetto al numero totale di messaggi inviati.
* **[!UICONTROL Mancati recapiti]**: totale degli errori accumulati durante la consegna e l’elaborazione automatica dei messaggi restituiti rispetto al numero totale di messaggi inviati.

>[!NOTE]
>
>I widget e le metriche delle offerte sono disponibili solo se è stata inserita una decisione in un messaggio e-mail. Per ulteriori informazioni sulla gestione delle decisioni, consulta questa [pagina](../offers/get-started/starting-offer-decisioning.md).

Il **[!UICONTROL Statistica sulle offerte]** e **[!UICONTROL Statistiche sulle offerte]** nel tempo, i widget misurano il successo e l’impatto dell’offerta sul pubblico di destinazione. Descrive le informazioni principali relative al messaggio con i KPI:

* **[!UICONTROL Offerta inviata]**: numero totale di invii per l’offerta.

* **[!UICONTROL Impression offerta]**: numero di volte in cui l’offerta è stata aperta in una consegna.

* **[!UICONTROL Clic sull’offerta]**: numero di volte in cui è stato fatto clic su un’offerta in una consegna.

Il **[!UICONTROL Statistiche dettagliate sulle offerte]** la tabella contiene i dati disponibili per l’attività del destinatario con l’offerta:

* **[!UICONTROL Nome posizionamento]**: nome del posizionamento utilizzato per visualizzare l’offerta. Per ulteriori informazioni sul posizionamento, consulta questa [pagina](../offers/offer-library/creating-placements.md).

* **[!UICONTROL Nome offerta]**: nome dell’offerta aggiunta alla consegna. Per ulteriori informazioni sul posizionamento, consulta questa [pagina](../offers/offer-library/creating-personalized-offers.md).

* **[!UICONTROL Offerta inviata]**: numero totale di invii per l’offerta.

* **[!UICONTROL Percentuale di impression offerta]**: percentuale di offerte aperte rispetto al numero di offerte inviate.

* **[!UICONTROL Percentuale di clic dell’offerta]**: percentuale di utenti che hanno interagito con l’offerta.
+++

## Scheda notifica push {#push-global}

Dal tuo percorso **[!UICONTROL Rapporto globale]**, il **[!UICONTROL Notifica push]** La scheda descrive le informazioni principali relative alle consegne push inviate nel tuo percorso.

![](assets/journey_global_3.png)

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto push.

Il **[!UICONTROL Notifica push - Statistiche di invio]** la tabella descrive le informazioni principali relative alle notifiche push con grafico e KPI:

* **[!UICONTROL Tempo di esecuzione]**: ora di inizio di ogni esecuzione del percorso in caso di percorsi ricorrenti. Per eseguire il targeting di una o più ricorrenze, selezionatela dal **[!UICONTROL Tempo di esecuzione]** a discesa.

* **[!UICONTROL Target]**: numero di profili target per qualsiasi azione, ad esempio invio di e-mail o SMS.

* **[!UICONTROL Inviato]**: numero totale di invii per la consegna.

* **[!UICONTROL Consegnato]**: numero di messaggi inviati correttamente rispetto al numero totale di messaggi inviati.

* **[!UICONTROL Percentuale di consegna]**: percentuale di messaggi inviati correttamente.

* **[!UICONTROL Mancati recapiti]**: totale degli errori accumulati durante la consegna e l’elaborazione automatica dei messaggi restituiti rispetto al numero totale di messaggi inviati.

* **[!UICONTROL Percentuale non recapitate]**: percentuale di notifiche push non recapitate rispetto alle notifiche push inviate.

* **[!UICONTROL Errori]**: numero totale di errori che si sono verificati durante una consegna e che ne hanno impedito l’invio ai profili.

* **[!UICONTROL Frequenza errori]**: percentuale di errori che si sono verificati durante una consegna che ne ha impedito l’invio, rispetto alle notifiche push inviate.

Il **[!UICONTROL Push - Statistiche di tracciamento]** contiene i dati disponibili per l’attività del destinatario per la consegna:

* **[!UICONTROL Tempo di esecuzione]**: ora di inizio di ogni esecuzione del percorso in caso di percorsi ricorrenti. Per eseguire il targeting di una o più ricorrenze, selezionatela dal **[!UICONTROL Tempo di esecuzione]** a discesa.

* **[!UICONTROL Aperture]**: numero di volte in cui un messaggio è stato aperto in una consegna.

* **[!UICONTROL Percentuale aperture]**: percentuale di notifiche push aperte.

* **[!UICONTROL Azioni]**: numero totale di azioni sulla notifica push consegnata, ad esempio clic su pulsante o rimozione.

* **[!UICONTROL Coinvolgimenti]**: numero totale di aperture e azioni per questa notifica push, ovvero se il profilo ha aperto la notifica push o se è stato fatto clic su un pulsante.

* **[!UICONTROL Tasso di coinvolgimento]**: percentuale di aperture e azioni per questa notifica push, ovvero se il profilo ha aperto la notifica push o se è stato fatto clic su un pulsante.

Il **[!UICONTROL Riepilogo notifiche push]** il grafico contiene i dati disponibili per le notifiche push inviate, ad esempio:

* **[!UICONTROL Aperture]**: numero di volte in cui un messaggio è stato aperto in una consegna.

* **[!UICONTROL Azioni]**: numero totale di azioni sulla notifica push consegnata, ad esempio clic su pulsante o rimozione.

* **[!UICONTROL Mancati recapiti]**: totale degli errori accumulati durante la consegna e l’elaborazione automatica dei messaggi restituiti rispetto al numero totale di messaggi inviati.

* **[!UICONTROL Consegnato]**: numero di messaggi inviati correttamente rispetto al numero totale di messaggi inviati.

* **[!UICONTROL Errori]**: numero totale di errori che si sono verificati durante una consegna e che ne hanno impedito l’invio ai profili.

>[!NOTE]
>
>Il **[!UICONTROL Ottimizzato e non ottimizzato]** e **[!UICONTROL Ottimizzazione del tempo di invio]**  I widget sono disponibili solo se per la consegna è attivata l’opzione Ottimizzazione ora di invio. Per ulteriori informazioni sull’ottimizzazione dell’ora di invio, consulta [questa pagina](../building-journeys/journeys-message.md#send-time-optimization).

Il **[!UICONTROL Ottimizzato e non ottimizzato]** il grafico descrive le informazioni principali relative al messaggio, ottimizzate o meno:

* **[!UICONTROL Consegnato]**: numero di messaggi inviati correttamente rispetto al numero totale di messaggi inviati.
* **[!UICONTROL Aperture]**: numero di volte in cui la consegna è stata aperta in una consegna.
* **[!UICONTROL Azioni]**: numero totale di azioni sulla notifica push consegnata, ad esempio clic su pulsante o rimozione.

Il **[!UICONTROL Ottimizzazione del tempo di invio]** descrive il successo della consegna in base al metodo di invio: ottimizzato o normale.

* **[!UICONTROL Consegnato]**: numero di messaggi inviati correttamente rispetto al numero totale di messaggi inviati.
* **[!UICONTROL Mancati recapiti]**: totale degli errori accumulati durante la consegna e l’elaborazione automatica dei messaggi restituiti rispetto al numero totale di messaggi inviati.

Il **[!UICONTROL Motivi di errore]** grafico e tabella ti consentono di vedere quale errore si è verificato durante la consegna.

Il **[!UICONTROL Motivi di esclusione]** il grafico e la tabella mostrano i diversi motivi che hanno impedito ai profili utente, esclusi dai profili target, di ricevere il messaggio.

Il **[!UICONTROL Tracciamento per piattaforma]**, **[!UICONTROL Invio per piattaforma]** e **[!UICONTROL Raggruppamento per piattaforma]** grafici e tabelle descrivono in dettaglio la riuscita della notifica push in base al sistema operativo del destinatario.

L’SMS **[!UICONTROL Rapporto globale]** è diviso in diversi widget che descrivono nel dettaglio il successo e gli errori della consegna. Ogni widget può essere ridimensionato ed eliminato, se necessario. Per ulteriori informazioni, consulta questa [sezione](global-report.md#modify-dashboard).
+++

## Scheda SMS {#sms-global}

![](assets/journey_global_4.png)

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto SMS.

Il **[!UICONTROL SMS - Statistiche di invio]** la tabella descrive il successo della consegna:

* **[!UICONTROL Tempo di esecuzione]**: ora di inizio di ogni esecuzione del percorso in caso di percorsi ricorrenti. Per eseguire il targeting di una o più ricorrenze, selezionatela dal **[!UICONTROL Tempo di esecuzione]** a discesa.

* **[!UICONTROL Target]**: numero di profili utente qualificati come profili target per questa consegna.

* **[!UICONTROL Escluso]**: numero di profili utente, esclusi dai profili target, che non hanno ricevuto il messaggio.

* **[!UICONTROL Inviato]**: numero totale di invii per la consegna.

* **[!UICONTROL Mancati recapiti]**: totale degli errori accumulati durante la consegna e l’elaborazione automatica dei messaggi restituiti rispetto al numero totale di messaggi inviati.

* **[!UICONTROL Errori]**: numero totale di errori che si sono verificati durante una consegna e che ne hanno impedito l’invio ai profili.

Il **[!UICONTROL Riepilogo SMS]** un grafico fornisce dettagli sulle informazioni principali relative al messaggio:

* **[!UICONTROL Inviato]**: numero totale di invii per la consegna.

* **[!UICONTROL Mancati recapiti]**: totale degli errori accumulati durante la consegna e l’elaborazione automatica dei messaggi restituiti rispetto al numero totale di messaggi inviati.

* **[!UICONTROL Errori]**: numero totale di errori che si sono verificati durante una consegna e che ne hanno impedito l’invio ai profili.

Il **[!UICONTROL Escludi motivi]** grafici e tabelle consentono di vedere quali errori ed esclusioni si sono verificati durante la consegna.

Il **[!UICONTROL SMS - Clic per collegamenti]** e **[!UICONTROL SMS - Statistiche di tracciamento]** i widget descrivono le informazioni principali relative al coinvolgimento dei visitatori con gli URL.

+++

## Scheda in-app {#in-app-global}

Dal tuo Percorso **[!UICONTROL Rapporto globale]**, il **[!UICONTROL In-app]** Questa scheda contiene le informazioni principali relative alle consegne in-app inviate nei tuoi percorsi.

![](assets/in-app-journey-report.png)

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto in-app.

Il **[!UICONTROL Prestazioni in-app]** I KPI descrivono le informazioni principali relative al coinvolgimento dei visitatori con i messaggi in-app, ad esempio:

* **[!UICONTROL Impression univoche]**: numero di utenti univoci a cui è stato visualizzato il messaggio in-app.

* **[!UICONTROL Impression]**: numero totale di messaggi in-app visualizzati a tutti gli utenti.

  >[!NOTE]
  >
  >Per garantire il conteggio di un’impression, l’utente deve soddisfare due criteri:
  >* Qualifica nell’esperienza in-app, ottenuta raggiungendo l’attività in-app specifica nel proprio percorso.
  >* Soddisfa le condizioni specificate nelle regole di attivazione.
  > 
  >A causa del secondo criterio, potrebbero esserci variazioni notevoli tra il numero di profili target e il conteggio di impression univoche.

* **[!UICONTROL Interazione]**: numero di accordi con il messaggio in-app. Ciò include tutte le azioni intraprese dagli utenti, come clic, revoche o qualsiasi altra interazione.

Il **[!UICONTROL Riepilogo in-app]** Il grafico mostra l’evoluzione delle impression e delle interazioni in-app per il periodo in questione.

Il **[!UICONTROL Interazioni per tipo]** grafici e tabelle dettagliano il modo in cui gli utenti interagivano con il messaggio in-app tracciando i clic, le eliminazioni o le interazioni.
+++
