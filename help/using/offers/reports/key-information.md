---
title: Informazioni chiave sugli eventi di Gestione decisioni
description: Ulteriori informazioni sulle informazioni chiave inviate con ogni evento di gestione delle decisioni.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 07be59e8-e994-4854-8089-25614d005dbe
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---

# Informazioni chiave sugli eventi di Gestione decisioni {#events-key-information}

Ogni evento inviato quando viene presa una decisione contiene quattro punti dati chiave che puoi sfruttare a scopo di analisi e reporting.

![](../assets/events-dataset-preview.png)

* **[!UICONTROL Fallback]**: Nome e ID dell’offerta di fallback, se non è stata selezionata alcuna offerta personalizzata,
* **[!UICONTROL Placement]**: Nome, ID e canale del posizionamento utilizzato per la consegna dell’offerta,
* **[!UICONTROL Selections]**: Nome e ID dell’offerta selezionata per il profilo,
* **[!UICONTROL Activity]**: Nome e ID della decisione.

Inoltre, puoi anche sfruttare il **[!UICONTROL identityMap]** e **[!UICONTROL Timestamp]** campi per recuperare informazioni sul profilo e l’ora in cui è stata consegnata l’offerta.

Per ulteriori informazioni su tutti i campi XDM inviati con ciascuna decisione, consulta [questa sezione](xdm-fields.md).
