---
title: Guida introduttiva agli eventi di Gestione delle decisioni
description: Scopri come creare rapporti di gestione delle decisioni in Adobe Experience Platform.
translation-type: tm+mt
source-git-commit: db7fd318b14d01a0369c934a3e01c6e368d7658d
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 47%

---

# Guida introduttiva agli eventi di gestione delle decisioni {#monitor-offer-events}

Ogni volta che la Gestione delle decisioni decide per un determinato profilo, le informazioni relative a tali eventi vengono inviate automaticamente a Adobe Experience Platform.

Puoi quindi esportare questi dati per analizzarli nel tuo sistema di reporting. Puoi anche sfruttare Adobe Experience Platform [Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=it) in combinazione con altri strumenti per migliorare le funzioni di analisi e reporting.

I set di dati contenenti eventi di Gestione decisioni sono accessibili dal menu Adobe Experience Platform **[!UICONTROL Datasets]** . Al momento del provisioning di ciascuna istanza viene creato automaticamente un set di dati.

![](../../assets/events-datasets-list.png)

Questi set di dati si basano sullo schema **[!UICONTROL ODE DecisionEvents]** , che contiene tutti i campi XDM necessari per inviare informazioni da Gestione decisioni a Adobe Experience Platform.

>[!NOTE]
>
>I set di dati ODE DecisionEvents sono **set di dati non di profilo**, che non possono essere acquisiti in Experience Platform per l’utilizzo da parte di Profilo cliente in tempo reale.

**Argomenti correlati:**

* [Informazioni chiave sugli eventi di Gestione decisioni](../reports/key-information.md)
* [Accedere ai campi XDM degli eventi](../reports/xdm-fields.md)
