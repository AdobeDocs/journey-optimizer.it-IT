---
product: journey optimizer
title: now
description: Scopri subito la funzione
feature: Journeys
role: Developer
level: Experienced
keywords: now, funzione, espressione, percorso
exl-id: 16dcc772-e48d-4f10-be75-62dd39473556
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
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

## Parametri

| Parametro | Descrizione |
|--- |--- |
| stringa | Identificatore del fuso orario (facoltativo) |

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
