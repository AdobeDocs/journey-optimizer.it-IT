---
solution: Journey Optimizer
product: journey optimizer
title: Rapporto campagna
description: Scopri come utilizzare i dati push dal rapporto della campagna
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 43b10f54-0c19-46a1-8d51-eb6bf22e6da9
TQID: https://experienceleague.adobe.com/wsbWXuQT-JWFmKKu-qIG8OgzKQ7mMY4yFcqKLaM3RDc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2:
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 539
ht-degree: 3%

---

# Rapporto sulle notifiche push della campagna {#campaign-global-report-cja-push}

>[!BEGINSHADEBOX]

Per accedere al report della campagna di notifica push, fai clic sul pulsante **[!UICONTROL Report]** nella campagna e seleziona **[!UICONTROL Visualizza report tutto il tempo]**. [Ulteriori informazioni](report-gs-cja.md)

![](assets/report-access.png)

>[!ENDSHADEBOX]

## Statistiche di invio {#sending-statistics-push}

![](assets/cja-campaign-push-sending-stat.png)

La tabella **[!UICONTROL Statistiche di invio]** fornisce un riepilogo completo dei dati essenziali relativi alle campagne di notifica push. Descrive le metriche chiave, ad esempio la dimensione del pubblico target e il numero di notifiche push inviate correttamente, fornendo informazioni utili sull’efficacia e la portata delle notifiche push.

+++ Ulteriori informazioni sull’invio di metriche delle statistiche

* **[!UICONTROL Destinati]**: numero di profili qualificati per il pubblico prima dell&#39;applicazione di esclusioni, eliminazioni o rimozioni del consenso. Nei percorsi in cui è abilitato il rientro, un profilo può essere sottoposto a targeting più volte.

* **[!UICONTROL Invii]**: numero totale di invii per la notifica push.

* **[!UICONTROL Recapitato]**: numero di notifiche push inviate correttamente, in relazione al numero totale di notifiche push inviate.

* **[!UICONTROL Consegna univoca]**: numero di profili che hanno ricevuto almeno una notifica push.

* **[!UICONTROL Errori in uscita]**: numero totale di errori che ne impediscono l&#39;invio ai profili.

* **[!UICONTROL Esclusioni in uscita]**: numero di profili esclusi da Adobe Journey Optimizer.

+++

## Statistiche di tracciamento {#tracking-statistics-push}

![](assets/cja-campaign-push-track-stat.png)

La tabella **[!UICONTROL Statistiche di tracciamento]** offre un&#39;istantanea dettagliata dell&#39;attività di profilo associata alle notifiche push, fornendo informazioni essenziali sull&#39;efficacia delle notifiche push e di coinvolgimento.

+++ Ulteriori informazioni sulle metriche delle statistiche di tracciamento

* **[!UICONTROL Tasso di click-through (CTR)]**: percentuale di utenti che hanno interagito con le notifiche push.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nelle notifiche push.

* **[!UICONTROL Clic univoci]**: numero di profili che hanno fatto clic su un contenuto nelle notifiche push.

* **[!UICONTROL Azioni personalizzate push]**: numero di azioni personalizzate eseguite dai profili in risposta alle notifiche push.

+++

## Etichette tracciate {#track-link-label-push}

![](assets/cja-campaign-push-link-labels.png)

La tabella **[!UICONTROL Etichette di collegamento tracciate]** offre una panoramica completa delle etichette di collegamento all&#39;interno delle notifiche push, evidenziando quelle che generano il traffico di visitatori più elevato. Questa funzione ti consente di identificare e assegnare la priorità ai collegamenti più popolari.

+++ Ulteriori informazioni sulle metriche delle etichette dei collegamenti tracciati

* **[!UICONTROL Clic univoci]**: numero di profili che hanno fatto clic su un contenuto nelle notifiche push.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nelle notifiche push.

+++

## URL collegamenti tracciati {#track-link-url-push}

![](assets/cja-campaign-push-link-urls.png)

La tabella **[!UICONTROL URL di collegamento tracciati]** fornisce una panoramica completa degli URL all&#39;interno delle notifiche push che attirano il traffico più elevato di visitatori. Questo consente di identificare e assegnare la priorità ai collegamenti più popolari, migliorando la comprensione del coinvolgimento del profilo con contenuti specifici nelle notifiche push.

+++ Ulteriori informazioni sulle metriche degli URL di collegamento tracciati

* **[!UICONTROL Clic univoci]**: numero di profili che hanno fatto clic su un contenuto nelle notifiche push.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nelle notifiche push.

+++

## Motivi di mancato recapito {#bounce-reasons-push}

La tabella **[!UICONTROL Motivi di mancato recapito]** fornisce una panoramica completa dei dati relativi alle notifiche push non recapitate, fornendo informazioni utili sulle ragioni specifiche alla base delle istanze di mancato recapito delle notifiche push.

## Motivi di errore {#error-reasons-push}

La tabella **[!UICONTROL Motivi di errore]** consente di identificare gli errori specifici che si sono verificati durante il processo di invio delle notifiche push, semplificando un&#39;analisi approfondita di eventuali problemi riscontrati.

## Motivi di esclusione {#exclude-reasons-push}

![](assets/cja-campaign-push-excluded.png)

La tabella **[!UICONTROL Escludi motivi]** illustra visivamente i diversi fattori che hanno portato all&#39;esclusione dei profili utente dal pubblico di destinazione, impedendo loro di ricevere le notifiche push.

Per un elenco completo dei motivi di esclusione, consulta [questa pagina](exclusion-list.md).
