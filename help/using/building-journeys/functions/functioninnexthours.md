---
product: journey optimizer
title: inNextHours
description: Scopri la funzione inNextHours
feature: Journeys
role: Developer
level: Experienced
keywords: inNextHours, funzione, espressione, percorso
exl-id: 079a91b6-49c5-4e68-a240-358ed0cded92
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inNextHours {#inNextHours}

Restituisce true se una data o un&#39;ora specificata è compresa tra now e now + delta ore.

## Categoria

Data

## Sintassi della funzione

`inNextHours(<dateTime>,<delta>)`

## Parametri

| Parametro | Tipo |
|-----------|------------------|
| data e ora | dateTime |
| delta | intero |

## Firme e tipo restituito

`inNextHours(<dateTime>,<integer>)`

Restituisce un valore booleano.

## Esempi

`inNextHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

Restituisce true.
