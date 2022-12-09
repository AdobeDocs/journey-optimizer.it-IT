---
title: Guida introduttiva agli eventi di Gestione delle decisioni
description: Scopri come creare rapporti di gestione delle decisioni in Adobe Experience Platform.
feature: Offers
topic: Integrations
role: User
level: Beginner
exl-id: 51830c63-fa88-47e7-8605-192297fcf6b8
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---

# Guida introduttiva agli eventi di Gestione delle decisioni {#monitor-offer-events}

Ogni volta che la gestione delle decisioni prende una decisione per un determinato profilo, le informazioni relative a tali eventi vengono inviate automaticamente ad Adobe Experience Platform.

Ciò ti consente di esportare questi dati per analizzarli nel tuo sistema di reporting. Puoi anche sfruttare Adobe Experience Platform [Servizio query](https://experienceleague.adobe.com/docs/experience-platform/query/home.html) in combinazione con altri strumenti per analisi e reporting migliorati.

I set di dati contenenti eventi di Gestione delle decisioni sono accessibili da Adobe Experience Platform **[!UICONTROL Datasets]** menu. Al momento del provisioning di ciascuna istanza viene creato automaticamente un set di dati.

![](../assets/events-datasets-list.png)

Questi set di dati sono basati su **[!UICONTROL ODE DecisionEvents]** schema, che contiene tutti i campi XDM necessari per inviare informazioni da Gestione decisioni ad Adobe Experience Platform.

>[!NOTE]
>
>I set di dati ODE DecisionEvents sono **set di dati non di profilo**, ovvero non possono essere acquisiti in Experience Platform per l’utilizzo da parte di Profilo cliente in tempo reale.

**Argomenti correlati:**

* [Informazioni chiave sugli eventi di Gestione decisioni](../reports/key-information.md)
* [Accedere ai campi XDM degli eventi](../reports/xdm-fields.md)
