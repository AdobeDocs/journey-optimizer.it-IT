---
product: journey optimizer
title: inLastMonths
description: Scopri la funzione inLastMonths
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 4933ef43-66b8-462d-867c-03edd4c34947
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 0%

---

# inLastMonths {#inLastMonths}

Restituisce true se una data o un&#39;ora specificata è compresa tra ora e ora - mesi delta.

## Categoria

Data

## Sintassi della funzione

`inLastMonths(<dateTime>,<delta>)`

## Parametri

| Parametro | Tipo |
|-----------|------------------|
| ora | dateTime |
| delta | integer |

## Firme e tipo restituito

`inLastMonths(<dateTime>,<integer>)`

Restituisce un valore booleano.

## Esempi

`inLastMonths(toDateTime('2010-12-12T01:11:00Z'), 4)`

Restituisce true.
