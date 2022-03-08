---
title: Introduzione agli eventi di Gestione delle decisioni
description: Scopri come creare rapporti di gestione delle decisioni in Adobe Experience Platform.
feature: Offers
topic: Integrations
role: User
level: Beginner
exl-id: 51830c63-fa88-47e7-8605-192297fcf6b8
source-git-commit: 51254efaab08a572def118d475dc18f74c9d29b7
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 57%

---

# Introduzione agli eventi di Gestione delle decisioni {#monitor-offer-events}

Ogni volta che la Gestione delle decisioni decide per un determinato profilo, le informazioni relative a tali eventi vengono inviate automaticamente a Adobe Experience Platform.

Puoi quindi esportare questi dati per analizzarli nel tuo sistema di reporting. Puoi anche sfruttare Adobe Experience Platform [Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=it) in combinazione con altri strumenti per migliorare le funzioni di analisi e reporting.

I set di dati contenenti eventi di Gestione decisioni sono accessibili da Adobe Experience Platform **[!UICONTROL Datasets]** menu. Al momento del provisioning di ciascuna istanza viene creato automaticamente un set di dati.

![](../../assets/events-datasets-list.png)

Questi set di dati sono basati su **[!UICONTROL ODE DecisionEvents]** schema, che contiene tutti i campi XDM necessari per inviare informazioni da Gestione decisioni a Adobe Experience Platform.

>[!NOTE]
>
>I set di dati ODE DecisionEvents sono **set di dati non di profilo**, che non possono essere acquisiti in Experience Platform per l’utilizzo da parte di Profilo cliente in tempo reale.

**Argomenti correlati:**

* [Informazioni chiave sugli eventi di Gestione delle decisioni](../reports/key-information.md)
* [Accedere ai campi XDM degli eventi](../reports/xdm-fields.md)
