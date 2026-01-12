---
solution: Journey Optimizer
product: journey optimizer
title: Rapporto percorso
description: Scopri come utilizzare i dati del rapporto sul percorso
feature: Reporting, Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 30d4f967-e085-44f1-973d-11e79f693e6e
source-git-commit: 27de3d2171e6f6575eb66ada20f951f6cb3abc98
workflow-type: tm+mt
source-wordcount: '971'
ht-degree: 1%

---

# Rapporto percorso {#journey-global-report}

Il report **Percorso** funziona come un dashboard completo che fornisce un&#39;analisi delle metriche essenziali associate al percorso. Questo include dettagli quali il conteggio dei profili inseriti e delle istanze di singoli percorsi non riusciti, offrendo un’insight completa per l’efficacia e il livello di coinvolgimento del tuo percorso.

È possibile accedere al report **Percorso** direttamente dal percorso con il pulsante **[!UICONTROL Visualizza report]**.

![](assets/gs-cja-report-3.png)

Per ulteriori informazioni su Customer Journey Analytics Workspace e su come filtrare e analizzare i dati, consultare [questa pagina](https://experienceleague.adobe.com/it/docs/analytics-platform/using/cja-workspace/home).

## Panoramica del percorso {#journey-global}

Il report **[!UICONTROL Percorso]** fornisce una visualizzazione chiara dei dati di tracciamento più importanti sul percorso.

### KPI PERCORSO {#journey-perfomance}

![](assets/cja-journey-kpis.png)

Gli indicatori di prestazioni chiave (KPI, Key Performance Indicators) di **[!UICONTROL Percorso]** funzionano come dashboard completo che fornisce un&#39;analisi delle metriche essenziali associate al percorso. Questo include dettagli quali il conteggio del profilo inserito e delle istanze di singoli percorsi non riusciti, offrendo un’insight completa per l’efficacia e il livello di coinvolgimento del tuo percorso.

+++ Ulteriori informazioni sulle metriche dei KPI di Percorso

* **[!UICONTROL Coinvolgimento di Percorso]**: numero totale di singoli utenti univoci che hanno ricevuto messaggi inviati tramite il percorso, che rappresentano profili distinti che hanno raggiunto un punto di azione designato nel percorso.

* **[!UICONTROL Il Percorso entra]**: numero totale di singoli utenti che hanno raggiunto l&#39;evento di ingresso del percorso.

* **[!UICONTROL Uscite dal Percorso]**: numero totale di singoli utenti che sono usciti dal percorso.

+++

### Statistiche percorso {#journey-stats}

![](assets/cja-journey-stats.png)

La tabella **[!UICONTROL Statistiche Percorso]** offre un riepilogo dettagliato dei dati fondamentali sui percorsi. Include metriche chiave come il numero di errori e di voci di successo, fornendo informazioni utili sulle prestazioni e sulla portata delle e-mail e dei percorsi.

+++ Ulteriori informazioni sulle metriche delle statistiche di Percorso

* **[!UICONTROL Esclusione Percorso]**: numero totale di individui esclusi dal percorso a causa di criteri predefiniti o regole di soppressione.

* **[!UICONTROL Coinvolgimento di Percorso]**: numero totale di singoli utenti univoci che hanno ricevuto messaggi inviati tramite il percorso, che rappresentano profili distinti che hanno raggiunto un punto di azione designato nel percorso.

* **[!UICONTROL Il Percorso entra]**: numero totale di singoli utenti che hanno raggiunto l&#39;evento di ingresso del percorso.

* **[!UICONTROL Uscite dal Percorso]**: numero totale di singoli utenti che sono usciti dal percorso.

* **[!UICONTROL Errori di Percorso]**: numero totale di singoli percorsi non eseguiti correttamente.

* **[!UICONTROL Entrate Percorso univoche]**: numero totale di persone che hanno raggiunto l&#39;evento di ingresso del percorso. Non vengono prese in considerazione più interazioni di un profilo.

* **[!UICONTROL Uscite dal Percorso univoche]**: numero totale di singoli utenti che sono usciti dal percorso. Non vengono prese in considerazione più interazioni di un profilo.

* **[!UICONTROL Errori di Percorso univoci]**: numero totale di singoli percorsi non eseguiti correttamente. Non vengono prese in considerazione più interazioni di un profilo.

+++

## Esclusione percorso {#journey-exclusion}

La tabella **[!UICONTROL Esclusione di Percorso]** presenta una panoramica completa dei diversi fattori che hanno determinato l&#39;esclusione dei profili utente.

## Errore azione {#action-error}

![](assets/cja-journey-action-error.png)

Il widget **[!UICONTROL Errori azione]** descrive i diversi errori che si sono verificati per le azioni del percorso.

## Area di lavoro percorso {#journey-canvas}

![](assets/cja-journey-canvas.png)

Il widget **[!UICONTROL Area di lavoro Percorso]** ti consente di tracciare visivamente la traiettoria dei profili di destinazione durante la navigazione nel percorso. [Ulteriori informazioni nella documentazione di Customer Journey Analytics](https://experienceleague.adobe.com/it/docs/analytics-platform/using/cja-workspace/visualizations/journey-canvas/journey-canvas)

Migliora la personalizzazione dell’area di lavoro con le seguenti opzioni:

* Aggiungere o rimuovere il tipo di attività desiderato, ad esempio messaggi o condizioni, dal menu a discesa **[!UICONTROL Tipo di nodo]**.
* Regola il **[!UICONTROL valore percentuale]** per determinare la distribuzione del flusso tra percorsi di percorso diversi.
* Personalizza le **[!UICONTROL impostazioni freccia]** per includere etichette, condizioni o scegli una visualizzazione pulita.
* Abilita l&#39;opzione **[!UICONTROL Mostra abbandono]** per visualizzare i profili che sono usciti dal percorso direttamente nell&#39;area di lavoro.

Quando si utilizza il filtro **[!UICONTROL Tipo di nodo]** si applicano le seguenti regole:

* Durante la creazione di un segmento su un nodo, esso includerà comunque i nodi delle fasi precedenti del percorso, anche se tali nodi sono stati esclusi tramite il filtro **[!UICONTROL Node type]**.

* Non è possibile creare segmenti formati da una freccia se i nodi nelle fasi precedenti del percorso sono stati esclusi tramite il filtro **[!UICONTROL Tipo di nodo]**. In questo caso, la funzionalità di clic con il pulsante destro del mouse verrà disattivata su tali frecce.

## Prestazione dell’azione {#action-performance}

### Prestazioni nel tempo {#action-overtime}

![](assets/cja-journey-action-performance.png)

Il grafico **[!UICONTROL Prestazioni nel tempo]** ti consente di identificare e analizzare il numero di profili che soddisfano i criteri per essere considerati profili target per le azioni. Questa visualizzazione fornisce informazioni utili sull’efficacia delle strategie e ti aiuta a prendere decisioni basate sui dati per ottimizzare le prestazioni.

### Panoramica delle azioni {#action-overview}

![](assets/cja-journey-action-overview.png)

La tabella **[!UICONTROL Panoramica azioni]** funge da dashboard completo e offre un&#39;analisi delle metriche chiave correlate alle azioni nel percorso. Ciò include dettagli fondamentali come il numero di interazioni e il tasso di click-through

+++ Ulteriori informazioni sulle metriche della panoramica delle azioni

* **[!UICONTROL Il nodo entra]**: numero totale di singoli utenti che hanno immesso un nodo specifico all&#39;interno del percorso.

* **[!UICONTROL Errore di Percorso]**: numero totale di singoli percorsi non eseguiti correttamente.

* **[!UICONTROL Percentuale di click-through]**: percentuale di utenti che hanno interagito con l&#39;azione.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto nelle azioni.

* **[!UICONTROL Consegnato]**: numero di azioni inviate correttamente rispetto al numero totale di azioni inviate.

+++

## Prestazioni degli eventi {#events-performance}

### Prestazioni nel tempo {#event-overtime}

![](assets/cja-journey-performance-event.png)

Il grafico **[!UICONTROL Prestazioni nel tempo]** ti consente di identificare e analizzare il numero di profili idonei come profili target per i tuoi eventi. Questo potente strumento consente di monitorare tendenze e modelli nel tempo, fornendo informazioni utili per ottimizzare le strategie degli eventi.

### Panoramica dell’evento {#event-overview}

![](assets/cja-journey-events-overview.png)

La tabella **[!UICONTROL Panoramica eventi]** mostra quanti profili soddisfano i criteri dell&#39;evento nel tempo. Questo strumento consente di identificare pattern nei tassi di qualificazione per perfezionare la strategia degli eventi.

+++ Ulteriori informazioni sulle metriche delle statistiche di Percorso

* **[!UICONTROL Persone]**: numero di profili utente qualificati come profili target per i tuoi eventi.

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
