---
product: journey optimizer
title: inNextHours
description: Scopri la funzione inNextHours
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 079a91b6-49c5-4e68-a240-358ed0cded92
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 20%

---

# inNextHours {#inNextHours}

Restituisce true se una data o un&#39;ora specificata è compresa tra ora e ora + ore delta.

## Categoria

Data

## Sintassi della funzione

`inNextHours(<dateTime>,<delta>)`

## Parametri

| Parametro | Tipo |
|-----------|------------------|
| ora | dateTime |
| delta | numero intero |

## Firme e tipo restituito

`inNextHours(<dateTime>,<integer>)`

Restituisce un valore booleano.

## Esempi

`inNextHours(toDateTime('2010-12-12T01:11:00Z'), 4)`

Restituisce true.
