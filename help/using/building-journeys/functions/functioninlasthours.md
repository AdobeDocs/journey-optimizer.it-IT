---
product: journey optimizer
title: inLastHours
description: Scopri la funzione inLastHours
feature: Journeys
role: Developer
level: Experienced
keywords: inLastHours, funzione, espressione, percorso
exl-id: c648d711-c81b-403b-9adb-792c7e79e4e2
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 18%

---

# inLastHours {#inLastHours}

Restituisce true se la data e l’ora specificate sono comprese tra now e now - delta hours.

## Categoria

Data

## Sintassi della funzione

`inLastHours(<dateTime>,<delta>)`

## Parametri

| Parametro | Tipo |
|-----------|------------------|
| data e ora | dateTime |
| delta | intero |

## Firme e tipo restituito

`inLastHours(<dateTime>,<integer>)`

Restituisce un valore booleano.

## Esempi

`inLastHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

Restituisce true.

`inLastHours(@event{MyEvent.timestamp}, 4)`

Restituisce true.
