---
title: Utilizzare gli eventi di gestione delle decisioni
description: Scopri come creare rapporti di gestione delle decisioni in Adobe Experience Platform.
feature: Offers
topic: Integrations
role: User
level: Beginner
exl-id: 51830c63-fa88-47e7-8605-192297fcf6b8
source-git-commit: a6a892ec20dfeb6879bef2f4c2eb4a0f8f54885f
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 29%

---

# Introduzione agli eventi di gestione delle decisioni {#monitor-offer-events}

Ogni volta che la gestione delle decisioni decide per un determinato profilo, le informazioni relative a tali eventi vengono inviate automaticamente a Adobe Experience Platform.

Questo ti consente di ottenere informazioni sulle tue decisioni, ad esempio per sapere quale offerta è stata presentata a un dato profilo. Puoi esportare questi dati per analizzarli nel tuo sistema di reporting o sfruttare Adobe Experience Platform [Servizio query](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=it) in combinazione con altri strumenti per analisi e reporting migliorati.

## Informazioni chiave disponibili nei set di dati {#key-information}

Ogni evento inviato quando viene presa una decisione contiene quattro punti dati chiave che puoi sfruttare a scopo di analisi e reporting:

![](../assets/events-dataset-preview.png)

* **[!UICONTROL Fallback]**: Nome e ID dell’offerta di fallback, se non è stata selezionata alcuna offerta personalizzata,
* **[!UICONTROL Posizionamento]**: Nome, ID e canale del posizionamento utilizzato per la consegna dell’offerta,
* **[!UICONTROL Selezioni]**: Nome e ID dell’offerta selezionata per il profilo,
* **[!UICONTROL Attività]**: Nome e ID della decisione.

Inoltre, puoi anche sfruttare il **[!UICONTROL identityMap]** e **[!UICONTROL Timestamp]** campi per recuperare informazioni sul profilo e l’ora in cui è stata consegnata l’offerta.

Per ulteriori informazioni su tutti i campi XDM inviati con ciascuna decisione, consulta [questa sezione](xdm-fields.md).

## Accedere ai set di dati {#access-datasets}

I set di dati contenenti eventi di gestione delle decisioni sono accessibili da Adobe Experience Platform **[!UICONTROL Set di dati]** menu. Al momento del provisioning di ciascuna istanza viene creato automaticamente un set di dati.

![](../assets/events-datasets-list.png)

Questi set di dati sono basati su **[!UICONTROL Decisioni ODE]** schema, che contiene tutti i campi XDM necessari per inviare informazioni da Gestione decisioni a Adobe Experience Platform.

>[!NOTE]
>
>I set di dati ODE DecisionEvents sono **set di dati non di profilo**, che non possono essere acquisiti in Experience Platform per l’utilizzo da parte di Profilo cliente in tempo reale.
