---
product: journey optimizer
title: inLastMonths
description: Scopri la funzione inLastMonths
feature: Journeys
role: Engineer
level: Experienced
keywords: inLastMonths, funzione, espressione, percorso
exl-id: 4933ef43-66b8-462d-867c-03edd4c34947
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inLastMonths {#inLastMonths}

Restituisce true se una data o un&#39;ora specificata è compresa tra now e now - delta mesi.

## Categoria

Data

## Sintassi della funzione

`inLastMonths(<dateTime>,<delta>)`

## Parametri

| Parametro | Tipo |
|-----------|------------------|
| data e ora | dateTime |
| delta | intero |

## Firme e tipo restituito

`inLastMonths(<dateTime>,<integer>)`

Restituisce un valore booleano.

## Esempi

`inLastMonths(toDateTime('2023-12-12T01:11:00Z'), 4)`

Restituisce true.
