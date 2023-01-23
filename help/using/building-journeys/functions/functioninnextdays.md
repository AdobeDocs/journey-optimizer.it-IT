---
product: journey optimizer
title: inNextDays
description: Scopri la funzione inNextDays
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inNextDays, funzione, espressione, percorso
exl-id: 0cb3e0db-dc5b-4d4e-a057-af030d9bdb21
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inNextDays {#inNextDays}

Restituisce true se una data o un valore dateTime specificato è compreso tra ora e ora + giorni delta.

## Categoria

Data

## Sintassi della funzione

`inNextDays(<dateTime>,<delta>)`

## Parametri

| Parametro | Tipo |
|-----------|------------------|
| ora | dateTime |
| delta | numero intero |

## Firme e tipo restituito

`inNextDays(<dateTime>,<integer>)`

Restituisce un valore booleano.

## Esempi

`inNextDays(toDateTime('2010-12-12T01:11:00Z'), 4)`

Restituisce true.
