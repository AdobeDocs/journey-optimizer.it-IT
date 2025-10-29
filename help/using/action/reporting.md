---
solution: Journey Optimizer
product: journey optimizer
title: Rapporto percorso
description: Scopri come utilizzare i dati del rapporto sul percorso
feature: Reporting, Journeys
topic: Content Management
role: User
level: Intermediate
badge: label="Disponibilità limitata" type="Informative"
source-git-commit: b93d2288156713ac7479eef491f6104df1955a18
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 1%

---

# Monitorare le azioni personalizzate {#reporting}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_custom_actions_monitor"
>title="Monitorare le azioni personalizzate"
>abstract="La pagina di reporting **[!UICONTROL Azione personalizzata]** consente di monitorare le prestazioni e l&#39;affidabilità delle chiamate API effettuate dai percorsi a sistemi di terze parti."

>[!AVAILABILITY]
>
>Il reporting delle azioni personalizzate è attualmente disponibile solo per un set di organizzazioni (disponibilità limitata).

La pagina di reporting **[!UICONTROL Azione personalizzata]** consente di monitorare l&#39;affidabilità e le prestazioni delle chiamate API effettuate dai percorsi ai sistemi di terze parti. Questi rapporti consentono di identificare rapidamente i problemi di integrazione, i colli di bottiglia della latenza o i limiti di limitazione/limite che possono influire sulla distribuzione.

La pagina per la generazione di rapporti sulle azioni personalizzate funziona come altri rapporti all-time in Journey Optimizer. Per informazioni dettagliate sulle funzionalità del dashboard, consulta [questa documentazione](../reports/report-cja-manage.md).

Per accedere alla pagina di reporting **[!UICONTROL Azione personalizzata]**, fai clic su ![](assets/do-not-localize/Smock_Monitoring_18_N.svg) nella home page **[!UICONTROL Azioni]**.

![](assets/monitor-1.png)

➡️ [Ulteriori informazioni su come configurare le azioni personalizzate](../action/about-custom-action-configuration.md)

## KPI {#kpis}

![](assets/monitor-2.png)

Gli indicatori di prestazioni chiave (KPI, Key Performance Indicators) **[!UICONTROL Azione personalizzata]** fungono da dashboard centralizzato e forniscono una visualizzazione consolidata dello stato operativo e dell&#39;affidabilità delle chiamate di azione personalizzate. Queste metriche consentono di valutare le prestazioni, identificare i colli di bottiglia e garantire integrazioni stabili con i sistemi esterni.

+++ Ulteriori informazioni sui KPI per azioni personalizzate

* **[!UICONTROL Chiamate riuscite]**: numero totale di chiamate HTTP che hanno restituito una risposta valida senza errori.

* **[!UICONTROL Errori 4xx/5xx]**: numero di chiamate non riuscite a causa di errori lato client (4xx) o lato server (5xx), evidenziando problemi di configurazione o errori endpoint.

* **[!UICONTROL Timeout]**: numero di chiamate non riuscite perché hanno superato il tempo di risposta massimo. Questo aiuta a far emergere problemi di latenza o prestazioni con gli endpoint esterni.

* **[!UICONTROL Chiamate limitate]**: numero di chiamate bloccate a causa di limiti di limitazione, per evitare che i sistemi a valle vengano sovraccaricati.

* **[!UICONTROL RPS medio]**: numero di richieste al secondo elaborate dall&#39;azione personalizzata nell&#39;intervallo di tempo selezionato.

+++

## Chiamate straordinarie {#calls}

![](assets/monitor-3.png)

Il grafico **[!UICONTROL Chiamate straordinarie]** mostra la tendenza dell&#39;indicatore KPI per le chiamate HTTP nel periodo di tempo selezionato per il rapporto. La granularità della serie temporale dipende dall’intervallo temporale selezionato. Ad esempio:

* Per un rapporto di 7 giorni, ogni punto dati mostrerà i KPI per un giorno.
* Se selezioni un intervallo di tempo di 1 giorno, il grafico mostra i KPI all’ora.
* Se selezioni un intervallo di tempo di 1 ora, il grafico mostra i KPI al minuto.

➡️[Consulta la sezione KPI per una descrizione delle metriche della chiamata HTTP](#kpis)

## Suddivisione chiamata {#breakdown}

![](assets/monitor-4.png)

La tabella **[!UICONTROL Analisi stratificata chiamate]** fornisce una suddivisione gerarchica delle metriche delle chiamate HTTP, dalle metriche globali per endpoint al livello superiore alle metriche per azione personalizzata che utilizzano ogni endpoint fino ai percorsi che si basano su di esse al livello inferiore.

➡️[Consulta la sezione KPI per una descrizione delle metriche della chiamata HTTP](#kpis)


