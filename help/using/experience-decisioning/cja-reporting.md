---
title: Rapporto sulla funzione Decisioni
description: Scopri come creare rapporti su Decisioning.
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 7c45cd8a-8e86-4646-ba0a-db393e92d9da
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/jbakmb7S9cFitmpa7ypVe8YrYvbZh0E0VogYi3KpNbo
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 270
ht-degree: 4%

---

# Rapporto sulla funzione Decisioni {#decisioning-report}

## Reporting sulle decisioni {#campaigns}

Una volta che sono attivi percorsi o campagne con strategie di selezione, puoi accedere a rapporti dedicati per monitorare gli indicatori prestazioni chiave (KPI, Key Performance Indicators) di Decisioning.

<!--
Once code-based experiences are live, you can access dedicated reports to monitor Key Performance Indicators (KPIs) as an all-encompassing dashboard, delivering an analysis of essential metrics associated with your campaign.

This encompasses details related to the decision items performances and how users interacted with them. [Learn how to work with Code-based experience reports](../reports/campaign-global-report-cja-code.md)
-->

![](../reports/assets/cja-decisioning-kpis.png)

Puoi anche accedere ai dettagli relativi alle prestazioni degli elementi decisionali e al modo in cui gli utenti hanno interagito con loro, fornendo un’analisi delle metriche essenziali associate alla campagna.

![](../reports/assets/cja-decisioning-item-performance.png)

Scopri come utilizzare i rapporti di esperienza basati su codice su Decisioning in [questa sezione](../reports/campaign-global-report-cja-code.md#decisioning-reporting).

## Generazione di rapporti in Customer Journey Analytics {#cja}

Se utilizzi Customer Journey Analytics, puoi creare dashboard di reporting personalizzati per le campagne basate su codice utilizzando Decisioning.

I passaggi principali sono elencati di seguito. Informazioni dettagliate su come lavorare con Customer Journey Analytics sono disponibili nella [documentazione di Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-landing){target="_blank"}.

1. Crea e configura una **connessione** in Customer Journey Analytics. Questo ti consente di connettersi al set di dati per il quale desideri creare rapporti. [Scopri come creare una connessione](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/create-connection){target="_blank"}

1. Crea una **visualizzazione dati** e associala alla connessione creata in precedenza. Nella scheda **[!UICONTROL Componenti]**, scegli i campi dello schema che desideri visualizzare nel reporting. Per Decisioning, assicurati di includere i campi **propositioninteract** e **propositiondisplay**. [Scopri come creare e configurare le visualizzazioni dati](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/create-dataview){target="_blank"}

1. Combina componenti dati, tabelle e visualizzazioni in **progetti Workspace** per creare e condividere report per la campagna basata su codice. [Scopri come creare progetti Workspace](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects){target="_blank"}
