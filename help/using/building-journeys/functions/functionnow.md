---
product: journey optimizer
title: now
description: Scopri subito la funzione
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: now, funzione, espressione, percorso
exl-id: 16dcc772-e48d-4f10-be75-62dd39473556
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 16%

---

# now {#now}

Restituisce la data corrente in formato data e ora. Per ulteriori informazioni sui tipi di dati, consulta [questa pagina](../expression/data-types.md).

## Categoria

Data

## Sintassi della funzione

`now(<parameter>)`

## Parametri

| Parametro | Descrizione |
|--- |--- |
| string |  |

## Firme e tipo restituito

`now()`

`now("<timeZone id>")`

Restituisce un valore dateTime.

## Esempi

`now()`

Restituisce 2019-06-03T06:30Z.

`toString(now())`

Restituisce &quot;2019-06-03T06:30Z&quot;

`now("Europe/Paris")`

Restituisce 2019-06-03T08:30+02:00.
