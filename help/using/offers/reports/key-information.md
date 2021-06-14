---
title: Informazioni chiave sugli eventi di Gestione delle decisioni
description: Ulteriori informazioni sulle informazioni chiave inviate con ogni evento di gestione delle decisioni.
feature: Offerte
topic: Integrazioni
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 91%

---

# Informazioni chiave sugli eventi di Gestione delle decisioni {#events-key-information}

Ogni evento inviato quando viene presa una decisione contiene quattro punti dati chiave che puoi sfruttare a scopo di analisi e reporting.

![](../../assets/events-dataset-preview.png)

* **[!UICONTROL Fallback]**: nome e ID dell’offerta di fallback, se non è stata selezionata alcuna offerta personalizzata
* **[!UICONTROL Placement]**: nome, ID e canale del posizionamento utilizzato per la consegna dell’offerta
* **[!UICONTROL Selections]**: nome e ID dell’offerta selezionata per il profilo
* **[!UICONTROL Activity]**: nome e ID della decisione (precedentemente nota come “attività di offerta”).

Inoltre, puoi sfruttare i campi **[!UICONTROL identityMap]** e **[!UICONTROL Timestamp]** per recuperare informazioni sul profilo e sull’ora in cui è stata consegnata l’offerta.

Per ulteriori informazioni su tutti i campi XDM inviati con ciascuna decisione, consulta [questa sezione](xdm-fields.md).
