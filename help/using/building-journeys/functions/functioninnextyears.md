---
product: adobe campaign
title: inNextYears
description: Scopri la funzione inNextYears
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: e4597772-d53c-4e15-8237-b2460ce31170
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '44'
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
| delta | integer |

## Firme e tipo restituito

`inNextYears(<dateTime>,<integer>)`

Restituisce un valore booleano.

## Esempi

`inNextYears(toDateTime('2021-12-12T01:11:00Z'), 4)`

Restituisce true.
