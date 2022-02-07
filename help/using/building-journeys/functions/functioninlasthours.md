---
product: adobe campaign
title: inLastHours
description: Scopri la funzione inLastHours
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: c648d711-c81b-403b-9adb-792c7e79e4e2
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '45'
ht-degree: 17%

---

# inLastHours {#inLastHours}

Restituisce true se l&#39;ora data specificata è compresa tra ora e ora - ore delta.

## Categoria

Data

## Sintassi della funzione

`inLastHours(<dateTime>,<delta>)`

## Parametri

| Parametro | Tipo |
|-----------|------------------|
| ora | dateTime |
| delta | integer |

## Firme e tipo restituito

`inLastHours(<dateTime>,<integer>)`

Restituisce un valore booleano.

## Esempi

`inLastHours(toDateTime('2019-12-12T01:11:00Z'), 4)`

Restituisce true.

`inLastHours(@{MyEvent.timestamp}, 4)`

Restituisce true.
