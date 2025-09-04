---
product: journey optimizer
title: inLastYears
description: Scopri la funzione inLastYears
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inLastYears, funzione, espressione, percorso
exl-id: cdf653d2-967e-4a1b-92e5-37dd22f379f9
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inLastYears {#inLastYears}

Restituisce true se una data o un valore dateTime specificato è compreso tra now e now - delta years.

## Categoria

Data

## Sintassi della funzione

`inLastYears(<dateTime>,<delta>)`

## Parametri

| Parametro | Tipo |
|-----------|------------------|
| data e ora | dateTime |
| delta | intero |

## Firme e tipo restituito

`inLastYears(<dateTime>,<integer>)`

Restituisce un valore booleano.

## Esempi

`inLastYears(toDateTime('2023-12-12T01:11:00Z'), 4)`

Restituisce true.
