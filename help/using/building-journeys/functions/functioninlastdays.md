---
product: journey optimizer
title: inLastDays
description: Scopri la funzione inLastDays
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inLastDays, funzione, espressione, percorso
exl-id: 1b150568-17c2-454d-847e-17bac3d0b35d
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inLastDays {#inLastDays}

Restituisce true se una data o un valore dateTime specificato è compreso tra now e now - delta days.

## Categoria

Data

## Sintassi della funzione

`inLastDays(<dateTime>,<delta>)`

## Elemento “parameters”

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
