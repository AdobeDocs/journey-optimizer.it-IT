---
product: adobe campaign
title: inLastMonths
description: Scopri la funzione inLastMonths
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 18%

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
