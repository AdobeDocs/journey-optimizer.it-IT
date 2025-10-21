---
product: journey optimizer
title: toDateTimeOnly
description: Scopri la funzione toDateTime
feature: Journeys
role: Developer
level: Experienced
keywords: toDateTimeOnly, funzione, espressione, percorso
exl-id: db54c119-5080-403a-b254-43645be6b4a8
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 14%

---

# toDateTimeOnly{#toDateTimeOnly}

Converte un valore di argomento in un valore di sola data e ora.

## Categoria

Conversione

## Sintassi della funzione

`toDateTimeOnly(<parameters>)`

## Parametri

| Parametro | Tipo |
|-----------|------------------|
| data e ora in formato ISO-8601 o &quot;AAAA-MM-GG&quot; (formato data XDM) | stringa |
| data e ora | dateTime |

## Firme e tipi restituiti

`toDateTimeOnly(<dateTime>)`

`toDateTimeOnly(<string>)`
<!--`toDateTimeOnly(<integer>,<integer>,<integer>)`
`toDateTimeOnly(<integer>,<integer>,<integer>,<integer>,<integer>,<integer>)`-->

Restituisce un valore datetime senza considerare il fuso orario.

## Esempi

`toDateTimeOnly ("2023-08-18")`

restituisce un valore dateTime che rappresenta 2023-08-18T00:00:00.000

`toDateTimeOnly(now())`

<!--`toDateTimeOnly(2016,8,18,23,17,59)`

Returns 2016-08-18T23:17:59.000.

`toDateTimeOnly(2016,8,18)`

Returns 2016-08-18T00:00:00.000.-->
