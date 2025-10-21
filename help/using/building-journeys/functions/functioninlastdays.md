---
product: journey optimizer
title: inLastDays
description: Scopri la funzione inLastDays
feature: Journeys
role: Engineer
level: Experienced
keywords: inLastDays, funzione, espressione, percorso
exl-id: 1b150568-17c2-454d-847e-17bac3d0b35d
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '46'
ht-degree: 19%

---

# inLastDays {#inLastDays}

Restituisce true se un dato dateTime è compreso tra now e now - delta days.

## Categoria

Data

## Sintassi della funzione

`inLastDays(<dateTime>,<delta>)`

## Parametri

| Parametro | Tipo |
|-----------|------------------|
| data e ora | dateTime |
| delta | intero |

## Firme e tipo restituito

`inLastDays(<dateTime>,<integer>)`

Restituisce un valore booleano.

## Esempi

`inLastDays(toDateTime('2023-12-12T01:11:00Z'), 4)`

Restituisce true.
