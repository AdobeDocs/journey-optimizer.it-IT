---
solution: Journey Optimizer
product: journey optimizer
title: Rapporto globale della campagna
description: Scopri come utilizzare i dati dal rapporto globale di Campaign
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: fa64f5b8-75f2-40e6-8566-5766fafe6cd6
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '2036'
ht-degree: 3%

---

# Rapporto globale della campagna {#campaign-global-report}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_report"
>title="Rapporto globale della campagna"
>abstract="Il rapporto globale delle campagne consente di misurare l’impatto di una campagna in un periodo di tempo selezionato. Il rapporto è suddiviso in diversi widget che descrivono il successo e gli errori della campagna. Ogni dashboard di reporting può essere modificata ridimensionando o spostando i widget."

Puoi accedere al rapporto globale di Campaign direttamente dalla tua campagna con **[!UICONTROL Visualizza rapporto]** pulsante .

![](assets/campaign_report_global_5.png)

La campagna **[!UICONTROL Report globale]** La pagina verrà visualizzata con le seguenti schede:

* [Campaign](#campaign-global)
* [E-mail](#email-global)
* [In-app](#inapp-global)
* [Push](#push-global)
* [SMS](#sms-global)
* [Web](#web-tab)

La campagna **[!UICONTROL Report globale]** è suddiviso in diversi widget che descrivono in dettaglio il successo e gli errori della campagna. Se necessario, ogni widget può essere ridimensionato ed eliminato. Per ulteriori informazioni, consulta questo [sezione](../reports/global-report.md#modify-dashboard).

Per un elenco dettagliato di ciascuna metrica disponibile in Adobe Journey Optimizer, consulta [questa pagina](global-report.md#list-of-components-global.md)

## Scheda Campaign {#campaign-global}

### Distribuzione {#delivery-global}

![](assets/campaign_report_global_1.png)

La **[!UICONTROL Statistiche di Campaign]** i dettagli del widget forniscono le informazioni principali relative alla campagna:

* **[!UICONTROL Profili inseriti]**: Numero di profili che hanno avviato il percorso.

* **[!UICONTROL Azioni consegnate]**: Numero totale di volte in cui un’azione nel percorso è stata consegnata.

* **[!UICONTROL Azioni non riuscite in %]**: Numero totale di volte in cui un&#39;azione non è riuscita nel percorso rispetto al numero totale di volte in cui un&#39;azione è stata consegnata.

## Scheda E-mail {#email-global}

![](assets/campaign_report_global_2.png)

Dalla tua campagna **[!UICONTROL Report globale]**, **[!UICONTROL E-mail]** la scheda descrive le informazioni principali relative alle consegne e-mail inviate nella campagna.

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto E-mail.

La **[!UICONTROL Invio di statistiche per e-mail]** il grafico descrive il successo della consegna:

* **[!UICONTROL Target]**: Numero totale di messaggi elaborati durante l’analisi della consegna.

* **[!UICONTROL Inviato]**: Numero totale di invii per la consegna.

* **[!UICONTROL Consegnato]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Tasso di consegna]**: Percentuale di messaggi inviati correttamente.

* **[!UICONTROL Rimbalzi]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Frequenza di rimbalzo]**: Percentuale di e-mail rimbalzate rispetto alle e-mail inviate.

* **[!UICONTROL Errori]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

* **[!UICONTROL Frequenza errori]**: Percentuale di errori che si sono verificati durante una consegna che ne impedisce l’invio rispetto alle e-mail inviate.

* **[!UICONTROL Nuovi tentativi]**: Numero di e-mail in coda per i nuovi tentativi.

* **[!UICONTROL Escluso]**: Numero di profili esclusi da Adobe Journey Optimizer.

La **[!UICONTROL E-mail - Statistiche di tracciamento]** widget contiene i dati disponibili per l’attività del destinatario per la consegna:

* **[!UICONTROL Aperture]**: Numero di volte in cui la consegna è stata aperta in una consegna.

* **[!UICONTROL Aperture univoche]**: Percentuale di consegne aperte.

* **[!UICONTROL Open Rate]**: Numero totale di e-mail aperte rispetto al numero di e-mail consegnate.

* **[!UICONTROL Clic]**: Numero di volte in cui è stato fatto clic su un contenuto in un’e-mail.

* **[!UICONTROL Clic univoci]**:numero di destinatari che hanno fatto clic su un contenuto in un’e-mail.

* **[!UICONTROL Frequenza di clic univoca]**: Percentuale di utenti che hanno interagito con la consegna.

* **[!UICONTROL Annulla abbonamenti]**: Numero di clic sul collegamento di annullamento dell’abbonamento.

* **[!UICONTROL Disturbi dello spam]**: Numero di volte in cui un messaggio è stato dichiarato come spam o spazzatura.

La **[!UICONTROL Invio di statistiche]** Il grafico contiene i dati disponibili per le e-mail inviate, ad esempio:

* **[!UICONTROL Consegnato]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Rimbalzi]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Nuovi tentativi]**: Numero di e-mail in coda per i nuovi tentativi.

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
+++

## Scheda in-app {#inapp-global}

Dalla tua campagna **[!UICONTROL Report globale]**, **[!UICONTROL In-app]** la scheda descrive le informazioni principali relative alle consegne in-app inviate nella campagna.

![](assets/campaign_report_global_6.png)

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto in-app.

La **[!UICONTROL Prestazioni in-app]** I KPI descrivono in dettaglio le informazioni principali relative al coinvolgimento dei visitatori con i messaggi in-app, ad esempio:

* **[!UICONTROL Impressioni univoche]**: numero di utenti univoci a cui è stato recapitato il messaggio in-app.

* **[!UICONTROL Impressioni]**: numero totale di messaggi in-app inviati a tutti gli utenti.

* **[!UICONTROL Frequenza di clic]**: percentuale di utenti che hanno interagito con i pulsanti inclusi nel messaggio in-app rispetto agli utenti che hanno visualizzato il messaggio.

* **[!UICONTROL Tasso di dismissione]**: percentuale di messaggi in-app ignorati dai destinatari.

La **[!UICONTROL Riepilogo in-app]** Il grafico mostra l’evoluzione delle impression in-app per il periodo in questione.

La **[!UICONTROL Clic per pulsante]** grafico e tabella contengono i dati disponibili per il comportamento del destinatario per pulsante:

* **[!UICONTROL Clic]**: numero totale di destinatari che hanno interagito con i pulsanti inclusi nel messaggio in-app.

* **[!UICONTROL Frequenza di clic]**: percentuale di utenti che hanno interagito con i pulsanti inclusi nel messaggio in-app rispetto agli utenti che hanno visualizzato il messaggio.
+++

## Scheda notifica push {#push-global}

Dalla tua campagna **[!UICONTROL Report globale]**, **[!UICONTROL Notifica push]** la scheda descrive le informazioni principali relative alle consegne push inviate nella campagna.

![](assets/campaign_report_global_3.png)

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto push.

La **[!UICONTROL Notifica push - Invio di statistiche]** la tabella descrive le informazioni principali relative alle notifiche push con grafici e KPI:

* **[!UICONTROL Target]**: Numero totale di messaggi elaborati durante l’analisi della consegna.

* **[!UICONTROL Inviato]**: Numero totale di invii per la consegna.

* **[!UICONTROL Consegnato]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Tasso di consegna]**: Percentuale di messaggi inviati correttamente.

* **[!UICONTROL Rimbalzi]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Frequenza di rimbalzo]**: Percentuale di notifiche push rimbalzate rispetto alle notifiche push inviate.

* **[!UICONTROL Errori]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

* **[!UICONTROL Frequenza errori]**: Percentuale di errori che si sono verificati durante una consegna che ne impedisce l’invio rispetto alle notifiche push inviate.

* **[!UICONTROL Escluso]**: Numero di profili esclusi da Adobe Journey Optimizer.

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
+++

## Scheda SMS {#sms-global}

Dalla tua campagna **[!UICONTROL Report globale]**, **[!UICONTROL SMS]** la scheda descrive le informazioni principali relative alle consegne SMS inviate nella campagna.

![](assets/campaign_report_global_4.png)

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto SMS.

La **[!UICONTROL SMS - Invio di statistiche]** la tabella descrive il successo della consegna:

* **[!UICONTROL Target]**: Numero di profili utente qualificati come profili di destinazione per questa consegna.

* **[!UICONTROL Escluso]**: Numero di profili utente, esclusi dai profili target, che non hanno ricevuto il messaggio.

* **[!UICONTROL Inviato]**: Numero totale di invii per la consegna.

* **[!UICONTROL Consegnato]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Rimbalzi]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Errori]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

La **[!UICONTROL Prestazioni SMS per data]** il widget descrive le informazioni principali relative al messaggio con un grafico:

* **[!UICONTROL Inviato]**: Numero totale di invii per la consegna.

* **[!UICONTROL Consegnato]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Rimbalzi]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Errori]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

La **[!UICONTROL Escludi motivi]**, **[!UICONTROL Motivi dei rimbalzi]** e **[!UICONTROL Motivi dell’errore]** grafici e tabelle ti consentono di vedere quali errori ed esclusioni si sono verificati durante la consegna.

La **[!UICONTROL SMS - Clic tramite collegamenti]** e **[!UICONTROL SMS - Statistiche di tracciamento]** I widget descrivono nel dettaglio le informazioni principali relative al coinvolgimento dei visitatori con gli URL.

+++

## Scheda Web {#web-tab}

Dalla tua campagna **[!UICONTROL Report globale]**, **[!UICONTROL Web]** scheda descrive le informazioni principali relative alle pagine Web.

![](assets/web-report.png)

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il report Web.

La **[!UICONTROL Prestazioni web]** I KPI descrivono in dettaglio le informazioni principali relative al coinvolgimento dei visitatori con le esperienze web, ad esempio:

* **[!UICONTROL Impressioni univoche]**: numero di utenti univoci a cui è stata distribuita l’esperienza web.

* **[!UICONTROL Impressioni]**: numero totale di esperienze web distribuite a tutti gli utenti.

* **[!UICONTROL Frequenza di clic]**: percentuale di visitatori che hanno interagito con i vari elementi delle pagine web.

La **[!UICONTROL Riepilogo web]** Il grafico mostra l’evoluzione delle esperienze web (impression, impression univoche e clic) per il periodo in questione.

La **[!UICONTROL Clic per elemento]** la tabella descrive le informazioni principali relative al coinvolgimento dei visitatori con i vari elementi presenti nelle pagine web.
+++

## Risorse aggiuntive

* [Introduzione alle campagne](../campaigns/get-started-with-campaigns.md)
* [Creare una campagna](../campaigns/create-campaign.md)
* [Creare campagne con attivazione API](../campaigns/api-triggered-campaigns.md)
* [Modificare o interrompere una campagna](../campaigns/modify-stop-campaign.md)
* [Rapporto live della campagna](campaign-live-report.md)
