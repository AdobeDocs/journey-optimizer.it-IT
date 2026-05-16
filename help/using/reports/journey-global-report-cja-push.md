---
solution: Journey Optimizer
product: journey optimizer
title: Rapporto percorso
description: Scopri come utilizzare i dati delle notifiche push dal rapporto di percorso
feature: Reporting, Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 6d4b7669-7852-42f0-9347-399a3994011f
TQID: https://experienceleague.adobe.com/rvjOY50CuIvkgBk4BEL5bGrXwpFWaBHcbT80NUOkXyw
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4ebid: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2: id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 562
ht-degree: 3%

---

# Rapporto percorso notifiche push {#journey-global-report}

>[!BEGINSHADEBOX]

Puoi accedere al report del percorso di notifiche push facendo clic sul pulsante **[!UICONTROL Visualizza report]** all&#39;interno del percorso. [Ulteriori informazioni](report-gs-cja.md)

![](assets/report-access-jo.png)

>[!ENDSHADEBOX]

## Statistiche di invio {#sending-statistics-push}

![](assets/cja-campaign-push-sending-stat.png)

La tabella **[!UICONTROL Statistiche di invio]** consente di comprendere le prestazioni delle notifiche push. Include metriche chiave come il tasso di consegna e la dimensione del pubblico, che ti forniscono informazioni preziose sull’efficacia e la portata dei tuoi percorsi.

+++ Ulteriori informazioni sull’invio di metriche delle statistiche

* **[!UICONTROL Persone]**: numero di profili utente qualificati come profili target per i messaggi SMS.

* **[!UICONTROL Destinati]**: numero di profili qualificati per il pubblico prima dell&#39;applicazione di esclusioni, eliminazioni o rimozioni del consenso. Nei percorsi in cui è abilitato il rientro, un profilo può essere sottoposto a targeting più volte.

* **[!UICONTROL Invii]**: numero totale di invii per la notifica push.

* **[!UICONTROL Recapitato]**: numero di notifiche push inviate correttamente, in relazione al numero totale di notifiche push inviate.

* **[!UICONTROL Mancati recapiti per i canali in uscita]**: totale degli errori accumulati durante il processo di invio ed elaborazione automatica dei resi in relazione al numero totale di notifiche push.

* **[!UICONTROL Errori in uscita]**: numero totale di errori che ne impediscono l&#39;invio ai profili.

* **[!UICONTROL Esclusioni in uscita]**: numero di profili esclusi da Adobe Journey Optimizer.

+++

## Statistiche di tracciamento {#tracking-statistics-push}

![](assets/cja-campaign-push-track-stat.png)

La tabella **[!UICONTROL Statistiche di tracciamento]** offre un&#39;istantanea dettagliata dell&#39;attività di profilo associata alle notifiche push, fornendo informazioni essenziali sull&#39;efficacia delle notifiche push e di coinvolgimento.

+++ Ulteriori informazioni sulle metriche delle statistiche di tracciamento

* **[!UICONTROL Tasso di click-through (CTR)]**: percentuale di utenti che hanno interagito con la notifica push.

* **[!UICONTROL Tasso di apertura click-through (CTOR)]**: numero di volte in cui la notifica push è stata aperta.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nella notifica push.

* **[!UICONTROL Clic univoci]**: numero di profili che hanno fatto clic su un contenuto nella notifica push.

* **[!UICONTROL Azioni personalizzate push]**: numero di azioni personalizzate eseguite dai profili in risposta alle notifiche push.
+++

## Etichette collegamenti tracciati {#track-link-label-push}

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
