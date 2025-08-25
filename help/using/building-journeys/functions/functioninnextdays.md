---
product: journey optimizer
title: inNextDays
description: Scopri la funzione inNextDays
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inNextDays, funzione, espressione, percorso
exl-id: 0cb3e0db-dc5b-4d4e-a057-af030d9bdb21
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inNextDays {#inNextDays}

Restituisce true se una data o un&#39;ora specificata è compresa tra now e now + delta giorni.

## Categoria

Data

## Sintassi della funzione

`inNextDays(<dateTime>,<delta>)`

## Parametri

| Parametro | Tipo |
|-----------|------------------|
| data e ora | dateTime |
| delta | intero |

## Firme e tipo restituito

`inNextDays(<dateTime>,<integer>)`

Restituisce un valore booleano.

## Esempi

`inNextDays(toDateTime('2023-12-12T01:11:00Z'), 4)`

Restituisce true.
