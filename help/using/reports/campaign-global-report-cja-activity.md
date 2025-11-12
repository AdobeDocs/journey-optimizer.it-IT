---
solution: Journey Optimizer
product: journey optimizer
title: Rapporto campagna
description: Scopri come utilizzare i dati delle attività live dal rapporto della campagna
feature: Reporting
topic: Content Management
role: User
level: Intermediate
source-git-commit: ce6bfca78d097588b5958c10c721b29b7013b3e2
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 2%

---

# Rapporto campagna attività live {#campaign-global-report-cja-activity}

>[!BEGINSHADEBOX]

Puoi accedere al report della campagna di attività live facendo clic sul pulsante **[!UICONTROL Report]** nella campagna e selezionando **[!UICONTROL Visualizza report tutto il tempo]**. [Ulteriori informazioni](report-gs-cja.md)

![](assets/report-access.png)

>[!ENDSHADEBOX]

## Statistiche di invio {#sending-statistics-mobile}

![](assets/sending-statistics-mobile-live.png)

La tabella **[!UICONTROL Statistiche di invio]** fornisce una panoramica dettagliata delle metriche chiave relative alle campagne Live Activity. Visualizza informazioni essenziali come le dimensioni del pubblico target e il numero di notifiche push inviate correttamente, consentendoti di valutare la portata e le prestazioni complessive delle notifiche push live.

+++ Ulteriori informazioni sull’invio di metriche delle statistiche

* **[!UICONTROL Target]**: numero totale di profili target durante l&#39;attività Live.

* **[!UICONTROL Invii]**: numero totale di notifiche push tentate da inviare ai profili di destinazione.

* **[!UICONTROL Recapitato]**: numero di notifiche push recapitate correttamente ai dispositivi, rispetto al numero totale di tentativi di invio.

* **[!UICONTROL Errori di invio]**: numero totale di notifiche push che non è stato possibile inviare a causa di errori (ad esempio, token non validi o problemi di connettività).

* **[!UICONTROL Inviare esclusioni]**: numero di profili esclusi dall&#39;invio da parte di Adobe Journey Optimizer (ad esempio, a causa dello stato di rinuncia o delle regole di idoneità).

+++

## Ciclo di vita dell’attività live {#lifecycle}

![](assets/activity-lifecycle.png)

La tabella **[!UICONTROL Ciclo di vita attività in tempo reale]** offre una panoramica completa dell&#39;avanzamento delle attività in tempo reale nel tempo. Fornisce visibilità sugli eventi chiave, ad esempio quando le attività vengono avviate, aggiornate o terminate, consentendoti di comprendere meglio il coinvolgimento degli utenti e il ciclo di vita complessivo delle campagne di attività Live.

+++ Ulteriori informazioni sulle metriche del ciclo di vita delle attività live

* **[!UICONTROL Avvii remoti]**: numero di attività live avviate in remoto, in genere attivate dal server o dal sistema back-end.

* **[!UICONTROL Avvii locali]**: numero di attività live avviate localmente sul dispositivo di un utente, spesso risultanti da interazione dell&#39;utente o da attivatori lato client.

**[!UICONTROL Aggiornamenti]**: numero totale di aggiornamenti delle attività live inviati ai dispositivi. Gli aggiornamenti possono includere modifiche di stato, nuovo contenuto o notifiche di avanzamento.

**[!UICONTROL Fine]**: numero di attività live terminate, automaticamente al completamento o manualmente tramite un trigger definito o un timeout.

**[!UICONTROL Conteggio totali]**: totale complessivo di tutti gli eventi del ciclo di vita dell&#39;attività Live, inclusi gli inizi, gli aggiornamenti e le fine, che fornisce una misura completa del volume dell&#39;attività Live.

+++

## Motivi di errore {#error-reasons}

![](assets/error-reasons-activity.png)

La tabella **[!UICONTROL Motivi di errore]** ti consente di identificare gli errori specifici che si sono verificati durante il processo di invio delle attività live, semplificando un&#39;analisi approfondita di eventuali problemi riscontrati.

## Motivi di esclusione {#excluded-reasons}

![](assets/excluded-activity.png)

La tabella **[!UICONTROL Motivi di esclusione]** illustra visivamente i diversi fattori che hanno portato all&#39;esclusione dei profili utente dal pubblico di destinazione, impedendo loro di ricevere la tua attività live.
