---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Utilizzare gli eventi di gestione delle decisioni
description: Scopri come creare rapporti di gestione delle decisioni in Adobe Experience Platform.
badge: label="Legacy" type="Informative"
feature: Decision Management, Datasets
topic: Integrations
role: User, Developer
level: Intermediate
exl-id: 51830c63-fa88-47e7-8605-192297fcf6b8
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/r3bOKyWcAT-sqI7KXA3J-Yi5TUax9KGi-8JY62QD6tA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
feature_v2:
  - id: c132d929-fa62-4271-803e-b823be07b914
  - id: c20d46e7-1c7d-476c-a50e-3961d4dce35f
  - id: ed0d8d0e-04b9-4326-be72-a0fbca265377
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 321
ht-degree: 100%

---

# Introduzione agli eventi di gestione delle decisioni {#monitor-offer-events}

>[!TIP]
>
>La funzione Decisioni, la nuova funzionalità decisionale di [!DNL Adobe Journey Optimizer], è ora disponibile tramite i canali e-mail e di esperienza basati su codice. [Ulteriori informazioni](../../experience-decisioning/gs-experience-decisioning.md)

Ogni volta che il servizio per la gestione delle decisioni prende una decisione per un determinato profilo, le informazioni relative a tali eventi vengono inviate automaticamente ad Adobe Experience Platform.

Questo ti consente di ottenere informazioni approfondite sulle tue decisioni, ad esempio per sapere quale offerta è stata presentata a un dato profilo. Puoi esportare questi dati per analizzarli nel tuo sistema di reporting o sfruttare il servizio [Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=it) di Adobe Experience Platform in combinazione con altri strumenti per analisi e reporting migliorati.

## Informazioni chiave disponibili nei set di dati {#key-information}

Ogni evento inviato quando viene presa una decisione contiene quattro punti dati chiave che puoi sfruttare a scopo di analisi e reporting:

![](../assets/events-dataset-preview.png)

* **[!UICONTROL Fallback]**: nome e ID dell’offerta di fallback, se non è stata selezionata alcuna offerta personalizzata
* **[!UICONTROL Posizionamento]**: nome, ID e canale del posizionamento utilizzato per la consegna dell’offerta
* **[!UICONTROL Selezioni]**: nome e ID dell’offerta selezionata per il profilo
* **[!UICONTROL Attività]**: Nome e ID della decisione.

Inoltre, puoi sfruttare i campi **[!UICONTROL identityMap]** e **[!UICONTROL Timestamp]** per recuperare informazioni sul profilo e sull’ora in cui è stata consegnata l’offerta.

Per ulteriori informazioni su tutti i campi XDM inviati con ciascuna decisione, consulta [questa sezione](xdm-fields.md).

## Accedere ai set di dati {#access-datasets}

I set di dati contenenti eventi di gestione delle decisioni sono accessibili dal menu **[!UICONTROL set di dati]** di Adobe Experience Platform. Al momento del provisioning di ciascuna istanza viene creato automaticamente un set di dati.

![](../assets/events-datasets-list.png)

Questi set di dati si basano sullo schema **[!UICONTROL ODE DecisionEvents]**, che contiene tutti i campi XDM necessari per inviare informazioni dal servizio di gestione delle decisioni ad Adobe Experience Platform.

>[!NOTE]
>
>I set di dati ODE DecisionEvents sono **set di dati non di profilo**, che non possono essere acquisiti in Experience Platform per l’utilizzo da parte di Profilo cliente in tempo reale.
