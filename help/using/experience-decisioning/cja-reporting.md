---
title: Rapporto sulla funzione Decisioni
description: Scopri come creare rapporti su Decisioning.
feature: Decisioning
topic: Integrations
role: User
level: Experienced
badge: label="Disponibilità limitata"
exl-id: 7c45cd8a-8e86-4646-ba0a-db393e92d9da
source-git-commit: bfc16476f525328b2b8451bfdd57b6b2027db916
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 5%

---


# Rapporto sulla funzione Decisioni {#decisioning-report}

## Generazione di rapporti per campagne basate su codice {#campaigns}

Una volta che l’esperienza basata su codice è attiva, puoi accedere a rapporti dedicati per monitorare gli indicatori prestazioni chiave (KPI, Key Performance Indicators) come dashboard completo, che fornisce un’analisi delle metriche essenziali associate alla campagna.

Questo include dettagli relativi alle prestazioni degli elementi decisionali e al modo in cui gli utenti hanno interagito con loro. [Scopri come utilizzare i report esperienza basati su codice](../reports/campaign-global-report-cja-code.md)

![](../reports/assets/cja-decisioning-item-performance.png)

## Generazione di rapporti in Customer Journey Analytics {#cja}

Se utilizzi Customer Journey Analytics, puoi creare dashboard di reporting personalizzati per le campagne basate su codice utilizzando Decisioning.

I passaggi principali sono elencati di seguito. Informazioni dettagliate su come lavorare con il Customer Journey Analytics sono disponibili nella [documentazione del Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-landing){target="_blank"}.

1. Crea e configura una **connessione** nel Customer Journey Analytics. Questo ti consente di connettersi al set di dati per il quale desideri creare rapporti. [Scopri come creare una connessione](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/create-connection){target="_blank"}

1. Crea una **visualizzazione dati** e associala alla connessione creata in precedenza. Nella scheda **[!UICONTROL Componenti]**, scegli i campi dello schema che desideri visualizzare nel reporting. Per Decisioning, assicurati di includere i campi **propositioninteract** e **propositiondisplay**. [Scopri come creare e configurare le visualizzazioni dati](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/create-dataview){target="_blank"}

1. Combina componenti dati, tabelle e visualizzazioni in **progetti Workspace** per creare e condividere report per la campagna basata su codice. [Scopri come creare progetti Workspace](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects){target="_blank"}
