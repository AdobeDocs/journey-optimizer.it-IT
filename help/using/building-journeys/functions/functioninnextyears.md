---
product: journey optimizer
title: inNextYears
description: Scopri la funzione inNextYears
feature: Journeys
role: Developer
level: Experienced
keywords: inNextYears, funzione, espressione, percorso
exl-id: e4597772-d53c-4e15-8237-b2460ce31170
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inNextYears {#inNextYears}

Restituisce true se una data o un&#39;ora specificata è compresa tra now e now + delta anni.

## Categoria

Data

## Sintassi della funzione

`inNextYears(<dateTime>,<delta>)`

## Parametri

| Parametro | Tipo |
|-----------|------------------|
| data e ora | dateTime |
| delta | intero |

## Firme e tipo restituito

`inNextYears(<dateTime>,<integer>)`

Restituisce un valore booleano.

## Esempi

`inNextYears(toDateTime('2021-12-12T01:11:00Z'), 4)`

Restituisce true.
