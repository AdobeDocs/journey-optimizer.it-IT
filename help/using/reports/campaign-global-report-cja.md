---
solution: Journey Optimizer
product: journey optimizer
title: Rapporto campagna
description: Scopri come utilizzare i dati di Campaign dal rapporto Campaign
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: b74d3137-2dd9-4302-a56e-73503d318d18
TQID: https://experienceleague.adobe.com/-1IfHcdK07JLG54DYR1GNNN-sU0VyHjfBjCLbNdKA-8
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 612
ht-degree: 1%

---

# Rapporto campagna {#campaign-global-report-cja}

>[!BEGINSHADEBOX]

Per accedere al report della campagna, fai clic sul pulsante **[!UICONTROL Reports]** nella campagna e seleziona **[!UICONTROL Visualizza report completo]**. [Ulteriori informazioni](report-gs-cja.md)

![](assets/report-access.png)

>[!ENDSHADEBOX]

## KPI della campagna {#campaign-kpis}

![](assets/cja-email-kpis.png)

I **[!UICONTROL indicatori di prestazioni chiave (KPI, Key Performance Indicators) di Campaign]** funzionano come dashboard completo che fornisce un&#39;analisi delle metriche essenziali associate alla campagna. Questo include dettagli quali il numero di clic e il numero di messaggi consegnati, offrendo un’insight completa sull’efficacia e il livello di coinvolgimento della tua campagna.

I KPI variano in base ai canali utilizzati nella campagna.

+++ Ulteriori informazioni sulle metriche dei KPI per Campaign

* **[!UICONTROL Percentuale di click-through]**: percentuale di utenti che hanno interagito con il messaggio.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nel messaggio.

* **[!UICONTROL Recapitato]**: numero di e-mail inviate correttamente, in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Visualizzazioni]**: numero di volte in cui il messaggio è stato aperto.

+++

>[!AVAILABILITY]
>Le campagne orchestrate supportano solo i canali SMS, E-mail e push. Altri canali (in-app, web, direct mailing, ecc.) non sono disponibili nelle campagne orchestrate e non vengono visualizzate nella reportistica.

### Panoramica della campagna {#delivery-global}

![](assets/cja-campaign-overview.png)

La tabella **[!UICONTROL Panoramica campagna]** funge da dashboard completo e offre una suddivisione dettagliata delle metriche chiave correlate alla campagna. Ciò include informazioni essenziali come il numero di profili e le azioni consegnate, fornendo una comprensione approfondita delle prestazioni e del coinvolgimento della campagna.

Tieni presente che le metriche variano in base ai canali utilizzati nella campagna.

+++ Ulteriori informazioni sulle metriche della panoramica di Campaign

* **[!UICONTROL Persone]**: numero di profili utente qualificati come profili target per i messaggi.

* **[!UICONTROL Percentuale di click-through]**: percentuale di utenti che hanno interagito con il messaggio.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nel messaggio.

* **[!UICONTROL Clic univoci]**: numero di profili che hanno fatto clic su un contenuto del messaggio.

* **[!UICONTROL Recapitato]**: numero di e-mail inviate correttamente, in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Mancati recapiti per i canali in uscita]**: numero totale di errori accumulati durante il processo di invio e l&#39;elaborazione automatica dei resi in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Errori in uscita]**: numero totale di errori che si sono verificati durante il processo di invio e che ne hanno impedito l&#39;invio ai profili.

* **[!UICONTROL Esclusioni in uscita]**: numero di profili esclusi da Adobe Journey Optimizer. [Ulteriori informazioni sul conteggio delle esclusioni](exclusion-list.md#exclusion-list).

* **[!UICONTROL Visualizzazioni]**: numero di volte in cui il messaggio è stato aperto.

* **[!UICONTROL Visualizzazioni univoche]**: il numero di volte in cui il messaggio è stato aperto; non vengono prese in considerazione più interazioni di un profilo.

+++

### Risultati funnel della campagna {#campaign-funnel}

![](assets/cja-campaign-funnel.png)

Il grafico dei risultati di **[!UICONTROL Campaign funnel]** presenta un&#39;analisi dettagliata del coinvolgimento dei profili con i messaggi, fornendo informazioni utili sulle interazioni tra vari profili e il contenuto.

+++ Ulteriori informazioni sulle metriche dei risultati di Campaign funnel

* **[!UICONTROL Recapitato]**: numero di e-mail inviate correttamente, in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nel messaggio.
+++

### Etichetta collegamento tracciato {#campaign-track}

![](assets/cja-campaign-tracked-link.png)

La tabella **[!UICONTROL Tracked link label]** offre informazioni essenziali sul coinvolgimento dei visitatori con gli URL inclusi nei messaggi, fornendo informazioni utili su quali collegamenti attraggono il maggior numero di interazioni.

+++ Ulteriori informazioni sulle metriche delle etichette dei collegamenti tracciati

* **[!UICONTROL Clic univoci]**: numero di profili che hanno fatto clic su un contenuto del messaggio.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nel messaggio.

+++

## Panoramica sul targeting {#targeting}

![](assets/cja-journey-targeting-overview.png)

Se imposti **[!UICONTROL Regole di targeting]** per il contenuto, la tabella **[!UICONTROL Panoramica targeting]** fornisce una visualizzazione dettagliata delle metriche chiave di coinvolgimento, mostrando come i profili target per ogni regola interagivano con il contenuto.

➡️ [Ulteriori informazioni sulle regole di targeting](../content-management/optimization-targeting.md)

+++ Ulteriori informazioni sulle metriche di panoramica del targeting

* **[!UICONTROL Persone]**: numero di profili utente qualificati come profili target per i tuoi eventi.

* **[!UICONTROL Clic univoci]**: numero di profili che hanno fatto clic su un contenuto in un messaggio e-mail.

* **[!UICONTROL Percentuale clic univoci]**: percentuale di profili target che hanno fatto clic almeno una volta.

+++
