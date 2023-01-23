---
product: journey optimizer
title: inNextYears
description: Scopri la funzione inNextYears
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inNextYears, funzione, espressione, percorso
exl-id: e4597772-d53c-4e15-8237-b2460ce31170
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inNextYears {#inNextYears}

Restituisce true se una data o un valore dateTime specificato è compreso tra ora e ora + anni delta.

## Categoria

Data

## Sintassi della funzione

`inNextYears(<dateTime>,<delta>)`

## Parametri

| Parametro | Tipo |
|-----------|------------------|
| ora | dateTime |
| delta | numero intero |

## Firme e tipo restituito

`inNextYears(<dateTime>,<integer>)`

Restituisce un valore booleano.

## Esempi

`inNextYears(toDateTime('2021-12-12T01:11:00Z'), 4)`

Restituisce true.
