---
title: Generazione di rapporti in Customer Journey Analytics
description: Scopri come eseguire la generazione di rapporti in Customer Journey Analytics
feature: Experience Decisioning
topic: Integrations
role: User
level: Experienced
badge: label="Disponibilità limitata"
exl-id: 7c45cd8a-8e86-4646-ba0a-db393e92d9da
source-git-commit: ac8ccb52bd16a26c14dea148f989256e28170765
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 7%

---

# Generazione di rapporti in Customer Journey Analytics {#cja}

Se utilizzi Customer Journey Analytics, puoi creare dashboard di reporting personalizzati per le campagne basate su codice utilizzando Decisioning.

I passaggi principali sono elencati di seguito. Informazioni dettagliate su come lavorare con il Customer Journey Analytics sono disponibili nella [documentazione del Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-landing){target="_blank"}.

1. Crea e configura una **connessione** nel Customer Journey Analytics. Questo ti consente di connettersi al set di dati per il quale desideri creare rapporti. [Scopri come creare una connessione](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/create-connection){target="_blank"}

1. Crea una **visualizzazione dati** e associala alla connessione creata in precedenza. Nella scheda **[!UICONTROL Componenti]**, scegli i campi dello schema che desideri visualizzare nel reporting. Per Decisioning, assicurati di includere i campi **propositioninteract** e **propositiondisplay**. [Scopri come creare e configurare le visualizzazioni dati](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/create-dataview){target="_blank"}

1. Combina componenti dati, tabelle e visualizzazioni in **progetti Workspace** per creare e condividere report per la campagna basata su codice.[Scopri come creare progetti Workspace](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects){target="_blank"}
