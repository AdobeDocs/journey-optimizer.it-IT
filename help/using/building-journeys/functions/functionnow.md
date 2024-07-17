---
product: journey optimizer
title: now
description: Scopri subito la funzione
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: now, funzione, espressione, percorso
exl-id: 16dcc772-e48d-4f10-be75-62dd39473556
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 14%

---

# now {#now}

Restituisce la data corrente in formato data e ora. Per ulteriori informazioni sui tipi di dati, consultare [questa pagina](../expression/data-types.md).

## Categoria

Data

## Sintassi della funzione

`now(<parameter>)`

## Elemento “parameters”

| Parametro | Descrizione |
|--- |--- |
| stringa |  |

## Firme e tipo restituito

`now()`

`now("<timeZone id>")`

Restituisce un valore dateTime.

## Esempi

`now()`

Restituisce 2023-06-03T06:30Z.

`toString(now())`

Restituisce &quot;2023-06-03T06:30Z&quot;

`now("Europe/Paris")`

Restituisce 2023-06-03T08:30+02:00.
