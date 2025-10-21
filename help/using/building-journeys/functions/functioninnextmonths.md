---
product: journey optimizer
title: inNextMonths
description: Scopri la funzione inNextMonths
feature: Journeys
role: Engineer
level: Experienced
keywords: inNextMonths, funzione, espressione, percorso
exl-id: e2e520ec-ae9e-4ed6-b50d-606fc6861d56
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inNextMonths {#inNextMonths}

Restituisce true se una data o un&#39;ora specificata è compresa tra now e now + delta mesi.

## Categoria

Data

## Sintassi della funzione

`inNextMonths(<dateTime>,<delta>)`

## Parametri

| Parametro | Tipo |
|-----------|------------------|
| data e ora | dateTime |
| delta | intero |

## Firme e tipo restituito

`inNextMonths(<dateTime>,<integer>)`

Restituisce un valore booleano.

## Esempi

`inNextMonths(toDateTime('2023-01-12T01:11:00Z'), 4)`

Restituisce true.
