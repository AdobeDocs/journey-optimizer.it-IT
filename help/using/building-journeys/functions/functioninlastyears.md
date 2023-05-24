---
product: journey optimizer
title: inLastYears
description: Scopri la funzione inLastYears
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inLastYears, funzione, espressione, percorso
exl-id: cdf653d2-967e-4a1b-92e5-37dd22f379f9
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
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
| delta | numero intero |

## Firme e tipo restituito

`inLastYears(<dateTime>,<integer>)`

Restituisce un valore booleano.

## Esempi

`inLastYears(toDateTime('2010-12-12T01:11:00Z'), 4)`

Restituisce true.
