---
product: journey optimizer
title: inLastDays
description: Scopri la funzione inLastDays
feature: Journeys
role: Developer
level: Experienced
keywords: inLastDays, funzione, espressione, percorso
exl-id: 1b150568-17c2-454d-847e-17bac3d0b35d
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
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
