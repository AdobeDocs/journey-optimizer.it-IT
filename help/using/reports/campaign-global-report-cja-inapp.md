---
solution: Journey Optimizer
product: journey optimizer
title: Rapporto campagna
description: Scopri come utilizzare i dati in-app dal rapporto della campagna
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 51cbe27f-3f3f-471e-a5d9-e3a88fcfdd68
TQID: https://experienceleague.adobe.com/d-n-lFEV-NuTi4mbCjiMgDil5whSWZRX02xp2S2jJ0M
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
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 657
ht-degree: 2%

---

# Rapporto sulla campagna in-app {#campaign-global-report-cja-inapp}

>[!IMPORTANT]
>
>Prima di creare rapporti sulle campagne e i percorsi in-app, assicurati di seguire i prerequisiti per la generazione di rapporti forniti in [questa pagina](../in-app/inapp-configuration.md#experiment-prerequisites).

>[!BEGINSHADEBOX]

Per accedere al report della campagna in-app, fai clic sul pulsante **[!UICONTROL Reports]** nella campagna e seleziona **[!UICONTROL Visualizza report tutto il tempo]**. [Ulteriori informazioni](report-gs-cja.md)

![](assets/report-access.png)

>[!ENDSHADEBOX]

## Tendenza di visualizzazione e clic {#impression-click-trend}

![](assets/cja-inapp-impressions-click.png)

Il grafico **[!UICONTROL Tendenza impression e clic]** presenta un&#39;analisi dettagliata del coinvolgimento dei tuoi profili con i messaggi in-app, fornendo informazioni preziose su come i profili interagiscono con i contenuti.

+++ Ulteriori informazioni sulle metriche della tendenza Impression &amp; Click

* **[!UICONTROL Clic]**: numero di volte in cui l&#39;utente ha interagito con i messaggi in-app.

* **[!UICONTROL Visualizzazioni]**: numero di volte in cui il messaggio in-app è stato visualizzato all&#39;utente.

+++

## Clic {#clicks-inapp}

![](assets/cja-campaign-inapp-clicks.png)

Il grafico **[!UICONTROL Clic]** visualizza le metriche di clic in-app, illustrando sia il numero totale di clic sul contenuto che il numero di profili univoci che hanno fatto clic sul contenuto.

+++ Ulteriori informazioni sulle metriche Clic

* **[!UICONTROL Clic univoci]**: numero di profili che hanno fatto clic su un contenuto nei messaggi in-app

* **[!UICONTROL Clic]**: numero di volte in cui l&#39;utente ha interagito con i messaggi in-app.

+++

## Visualizzazione {#display-inapp}

![](assets/cja-campaign-inapp-displays.png)

Il grafico **[!UICONTROL Displays]** ti aiuta a comprendere sia la portata complessiva del messaggio che il numero di profili univoci coinvolti con esso.

+++ Ulteriori informazioni sulle metriche di visualizzazione

* **[!UICONTROL Visualizzazioni]**: numero di volte in cui il messaggio in-app è stato visualizzato all&#39;utente.

* **[!UICONTROL Visualizzazioni univoche]**: il numero di volte in cui il messaggio è stato aperto; non vengono prese in considerazione più interazioni di un profilo.

+++

## Dati di tracciamento {#tracking-data-inapp}

![](assets/cja-campaign-inapp-tracking-data.png)

La tabella **[!UICONTROL Dati di tracciamento]** offre un&#39;istantanea dettagliata dell&#39;attività del profilo associata ai messaggi in-app, fornendo informazioni essenziali sull&#39;efficacia del coinvolgimento e dei messaggi in-app.

+++ Ulteriori informazioni sul tracciamento delle metriche dei dati

* **[!UICONTROL Persone]**: numero di profili utente idonei come profili di destinazione per i messaggi in-app.

* **[!UICONTROL Tasso di click-through (CTR)]**: percentuale di utenti che hanno interagito con i messaggi in-app.

* **[!UICONTROL Percentuale di apertura dei clic]**: numero di volte in cui i messaggi in-app sono stati aperti.

* **[!UICONTROL Clic]**: numero di volte in cui l&#39;utente ha interagito con i messaggi in-app.

* **[!UICONTROL Clic univoci]**: numero di profili che hanno fatto clic su un contenuto nei messaggi in-app.

* **[!UICONTROL Visualizzazioni]**: numero di volte in cui il messaggio in-app è stato visualizzato all&#39;utente.

* **[!UICONTROL Visualizzazioni univoche]**: il numero di volte in cui il messaggio è stato aperto; non vengono prese in considerazione più interazioni di un profilo.

* **[!UICONTROL Invii]**: numero di volte che l&#39;app ha richiesto la campagna in-app. Più richieste per sessione utente (ad esempio, al momento del lancio o del ricaricamento) possono causare il superamento del numero di utenti univoci se i dati della campagna non sono memorizzati nella cache.

* **[!UICONTROL Attivazione in entrata]**: numero di volte che l&#39;app ha considerato di visualizzare il messaggio in-app. Questo numero può essere inferiore al totale degli invii se le regole lato app impediscono la visualizzazione del messaggio.

* **[!UICONTROL Messaggi in entrata ignorati]**: numero di volte in cui gli utenti hanno ignorato il messaggio in-app senza interagire con esso.


+++

## Etichette collegamenti tracciati {#track-link-label-inapp}

![](assets/cja-inapp-tracked-link-labels.png)

La tabella **[!UICONTROL Etichette di collegamento tracciate]** offre una panoramica completa delle etichette di collegamento all&#39;interno dei messaggi in-app, evidenziando quelle che generano il traffico di visitatori più elevato. Questa funzione ti consente di identificare e assegnare la priorità ai collegamenti più popolari.

+++ Ulteriori informazioni sulle metriche delle etichette dei collegamenti tracciati

* **[!UICONTROL Clic univoci]**: numero di profili che hanno fatto clic su un contenuto nei messaggi in-app.

* **[!UICONTROL Clic]**: numero di volte in cui l&#39;utente ha interagito con i messaggi in-app.

* **[!UICONTROL Visualizzazioni]**: numero di volte in cui il messaggio in-app è stato visualizzato all&#39;utente.

* **[!UICONTROL Visualizzazioni univoche]**: il numero di volte in cui il messaggio è stato aperto; non vengono prese in considerazione più interazioni di un profilo.

+++

## URL collegamenti tracciati {#track-link-url-inapp}

![](assets/cja-inapp-tracked-link-urls.png)

La tabella **[!UICONTROL URL di collegamento tracciati]** fornisce una panoramica completa degli URL all&#39;interno dei messaggi in-app che attraggono il traffico più elevato di visitatori. Questo consente di identificare e assegnare la priorità ai collegamenti più popolari, migliorando la comprensione del coinvolgimento del profilo con contenuti specifici nei messaggi in-app.

+++ Ulteriori informazioni sulle metriche degli URL di collegamento tracciati

* **[!UICONTROL Clic univoci]**: numero di profili che hanno fatto clic su un contenuto nei messaggi in-app.

* **[!UICONTROL Clic]**: numero di volte in cui l&#39;utente ha interagito con i messaggi in-app.

+++
