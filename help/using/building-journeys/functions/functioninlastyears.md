---
product: journey optimizer
title: inLastYears
description: Scopri la funzione inLastYears
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: cdf653d2-967e-4a1b-92e5-37dd22f379f9
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 20%

---

# inLastYears {#inLastYears}

Restituisce true se una data o un valore dateTime specificato è compreso tra ora e ora - anni delta.

## Categoria

Data

## Sintassi della funzione

`inLastYears(<dateTime>,<delta>)`

## Parametri

| Parametro | Tipo |
|-----------|------------------|
| ora | dateTime |
| delta | numero intero |

## Firme e tipo restituito

`inLastYears(<dateTime>,<integer>)`

Restituisce un valore booleano.

## Esempi

`inLastYears(toDateTime('2010-12-12T01:11:00Z'), 4)`

Restituisce true.
