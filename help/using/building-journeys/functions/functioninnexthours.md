---
product: journey optimizer
title: inNextHours
description: Scopri la funzione inNextHours
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inNextHours, funzione, espressione, percorso
exl-id: 079a91b6-49c5-4e68-a240-358ed0cded92
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

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
