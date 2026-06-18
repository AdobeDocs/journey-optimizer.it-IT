---
solution: Journey Optimizer
product: journey optimizer
title: Rapporto campagna
description: Scopri come utilizzare i dati SMS dal rapporto Campaign
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: bd743a3b-0317-45d9-8e76-98d5cc258752
TQID: https://experienceleague.adobe.com/dFM14bh1Yil9GUsCk3mkcqz6QNH3fUWmQCNtj-FnWfA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a9f73820-6899-47c2-a597-3fec28ab756a
  - id: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
subfeature_v2:
  - id: d145add9-d5b9-481b-aa8a-e15e6bb7f813
  - id: a7289281-9ae4-47b1-b8cf-4028b98af776
  - id: b5afe8bf-bda6-41b5-ba06-922638872d63
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: f10f2b6cbad242efca31c84ce8adf5a615f57c1e
workflow-type: tm+mt
source-wordcount: 955
ht-degree: 2%

---

# Rapporto sulla campagna SMS {#campaign-global-report-cja-sms}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come leggere il report della campagna SMS in Adobe Journey Optimizer per analizzare le tendenze di consegna e clic, lo stato della consegna, i collegamenti tracciati, i messaggi in entrata e i motivi di mancato recapito, errore ed esclusione dei messaggi SMS.

>[!ENDSHADEBOX]

>[!BEGINSHADEBOX]

Per accedere al report della campagna SMS, fai clic sul pulsante **[!UICONTROL Report]** nella campagna e seleziona **[!UICONTROL Visualizza report completo]**. [Ulteriori informazioni](report-gs-cja.md)

![](assets/report-access.png)

>[!ENDSHADEBOX]

## Tendenza consegne e clic {#delivered-click-sms}

![](assets/cja-campaign-sms-delivered.png)

Il grafico **[!UICONTROL Tendenza consegna vs clic]** presenta un&#39;analisi dettagliata del coinvolgimento dei tuoi profili con le e-mail, fornendo informazioni utili sul modo in cui i profili interagiscono con il contenuto.

+++ Ulteriori informazioni sulle metriche di tendenza Consegne e Clic

* **[!UICONTROL Recapitato]**: numero di messaggi SMS inviati correttamente, in relazione al numero totale di messaggi SMS.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nei messaggi SMS.

+++

## Stato consegna {#delivery-status-sms}

![](assets/cja-campaign-sms-status.png)

La tabella **[!UICONTROL Stato consegna]** offre un account dettagliato dell&#39;attività del profilo correlata alle campagne SMS. Ciò include metriche su consegnati, clic e altri indicatori di coinvolgimento rilevanti, che offrono una panoramica completa del modo in cui i profili interagiscono con il contenuto SMS.

+++ Ulteriori informazioni sulle metriche dello stato della consegna

* **[!UICONTROL Recapitato]**: numero di messaggi SMS inviati correttamente, in relazione al numero totale di messaggi SMS.

* **[!UICONTROL Mancati recapiti]**: totale degli errori accumulati durante il processo di invio e l&#39;elaborazione automatica dei resi in relazione al numero totale di messaggi SMS inviati.

* **[!UICONTROL Errori di invio]**: numero totale di errori che ne impediscono l&#39;invio ai profili.

* **[!UICONTROL Invia esclusioni]**: numero di profili esclusi da Adobe Journey Optimizer.

+++

## Panoramica della campagna {#campaign-global}

La tabella **[!UICONTROL Panoramica campagna]** funge da dashboard per le prestazioni SMS nella campagna. Vengono riepilogati i profili target, le metriche di click-through (compresi i clic stimati che escludono il traffico di interazione da bot e non umani) e i risultati di consegna come mancati recapiti, errori di invio ed esclusioni.

+++ Ulteriori informazioni sulle metriche della panoramica di Campaign

* **[!UICONTROL Persone]**: numero di profili utente qualificati come profili target per i messaggi.

* **[!UICONTROL Percentuale di click-through]**: percentuale di utenti che hanno interagito con il messaggio.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nel messaggio.

* **[!UICONTROL Clic univoci]**: numero di profili univoci che hanno fatto clic su almeno un contenuto nel messaggio mobile.

* **[!UICONTROL Clic stimati]**: numero di volte in cui è stato fatto clic su un contenuto nel messaggio, escluso il traffico identificato di bot e di interazione non umana (NHI).

* **[!UICONTROL Recapitato]**: numero di e-mail inviate correttamente, in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Mancati recapiti]**: numero totale di errori cumulati durante il processo di invio e l&#39;elaborazione della restituzione automatica in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Errori di invio]**: numero totale di errori che si sono verificati durante il processo di invio e che ne hanno impedito l&#39;invio ai profili.

* **[!UICONTROL Invia esclusioni]**: numero di profili esclusi da Adobe Journey Optimizer. [Ulteriori informazioni sul conteggio delle esclusioni](exclusion-list.md#exclusion-list).

+++

## Etichette tracciate {#track-label-sms}

La tabella **[!UICONTROL Etichette tracciate]** offre una panoramica completa delle etichette di collegamento all&#39;interno dei messaggi SMS, evidenziando quelle che generano il traffico visitatore più elevato. Questa funzione ti consente di identificare e assegnare la priorità ai collegamenti più popolari.

+++ Ulteriori informazioni sulle metriche delle etichette dei collegamenti tracciati

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nei messaggi SMS.

* **[!UICONTROL Clic stimati]**: numero di volte in cui è stato fatto clic su un contenuto nel messaggio, escluso il traffico identificato di bot e di interazione non umana (NHI).

* **[!UICONTROL Clic univoci]**: numero di profili univoci che hanno fatto clic su almeno un contenuto nel messaggio mobile.

+++

## URL collegamenti tracciati {#track-link-url-sms}

La tabella **[!UICONTROL URL di collegamento tracciati]** fornisce una panoramica completa degli URL all&#39;interno dei messaggi SMS che attraggono il traffico più elevato dei visitatori. Questo consente di identificare e assegnare la priorità ai collegamenti più popolari, migliorando la comprensione del coinvolgimento del profilo con contenuti specifici nei messaggi SMS.

+++ Ulteriori informazioni sulle metriche degli URL di collegamento tracciati

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nei messaggi SMS.

* **[!UICONTROL Clic stimati]**: numero di volte in cui è stato fatto clic su un contenuto nel messaggio, escluso il traffico identificato di bot e di interazione non umana (NHI).

* **[!UICONTROL Clic univoci]**: numero di profili univoci che hanno fatto clic su almeno un contenuto nel messaggio mobile.

* **[!UICONTROL Visualizzazioni]**: numero di volte in cui il messaggio è stato aperto.

* **[!UICONTROL Visualizzazioni univoche]**: il numero di volte in cui il messaggio è stato aperto; non vengono prese in considerazione più interazioni di un profilo.

+++

## Messaggio SMS in entrata {#sms-inbound}

La tabella **[!UICONTROL Messaggio SMS in entrata]** presenta una panoramica completa dei messaggi SMS che hanno attirato il traffico più elevato. Questa risorsa offre informazioni preziose sulle dinamiche di coinvolgimento del pubblico.

+++ Ulteriori informazioni sulle metriche dei messaggi SMS in entrata

* **[!UICONTROL Persone]**: numero di profili utente qualificati come profili target per i messaggi SMS.

+++

## Tipo di messaggio SMS {#sms-message-type}

La tabella **[!UICONTROL Tipo di messaggio SMS]** presenta una panoramica completa del tipo di messaggio SMS che ha attirato il traffico più elevato. Questa risorsa offre informazioni preziose sulle dinamiche di coinvolgimento del pubblico.

+++ Ulteriori informazioni sulle metriche del tipo di messaggio SMS

* **[!UICONTROL Persone]**: numero di profili utente qualificati come profili target per i messaggi SMS.

+++

## Provider SMS {#sms-providers}

La tabella **[!UICONTROL Provider SMS]** presenta una panoramica completa dei provider SMS che hanno attirato il traffico più elevato. Questa risorsa offre informazioni preziose sulle dinamiche di coinvolgimento del pubblico.

+++ Ulteriori informazioni sulle metriche dei provider SMS

* **[!UICONTROL Persone]**: numero di profili utente qualificati come profili target per i messaggi SMS.

+++

## Motivi di mancato recapito {#bounce-reasons-sms}

La tabella **[!UICONTROL Motivi di mancato recapito]** fornisce una panoramica completa dei dati relativi ai messaggi SMS non recapitati, fornendo informazioni utili sulle ragioni specifiche alla base delle istanze di mancato recapito dei messaggi SMS.

## Motivi di errore {#error-reasons-sms}

La tabella **[!UICONTROL Motivi di errore]** consente di identificare gli errori specifici che si sono verificati durante il processo di invio dei messaggi SMS, facilitando un&#39;analisi approfondita di eventuali problemi riscontrati.

## Motivi di esclusione {#excluded-reasons-sms}

La tabella **[!UICONTROL Escludi motivi]** mostra visivamente i diversi fattori che hanno portato all&#39;esclusione dei profili utente dal pubblico di destinazione, impedendo loro di ricevere i messaggi SMS.

Per un elenco completo dei motivi di esclusione, consulta [questa pagina](exclusion-list.md).
