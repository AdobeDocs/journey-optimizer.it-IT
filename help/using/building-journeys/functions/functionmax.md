---
product: journey optimizer
title: max
description: Scopri il valore massimo della funzione
feature: Journeys
role: Developer
level: Experienced
keywords: max, funzione, espressione, percorso
exl-id: 5c792d33-32b9-4b1b-ab99-3ebfac391678
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 7%

---

# max{#max}

Restituisce il valore massimo in un insieme di espressioni, sotto forma di elenco o di due espressioni. I valori Null vengono ignorati.

## Categoria

Aggregazione

## Sintassi della funzione

`max(<parameter>)`

## Parametri

* listDuration
* listInteger
* listDecimal
* listDateTime
* listDateTimeOnly
* listDateOnly
* durata
* intero
* decimale
* dateTime
* dateTimeOnly

## Firme e tipi restituiti

`max(<listDuration>)`

Restituisce una durata.

`max(<listInteger>)`

Restituisce una durata.

`max(<listDateTimeOnly>)`

Restituisce un valore datetime senza considerare il fuso orario.

`max(<listDateTime>)`

Restituisce un valore datetime.

`max(<listDateOnly>)`

Restituisce una data.

`max(<listDecimal>)`

Restituisce un valore decimale.

`max(<decimal>,<decimal>)`

Restituisce un valore decimale.

`max(<duration>,<duration>)`

Restituisce una durata.

`max(<dateTime>,<dateTime>)`

Restituisce un valore datetime.

`max(<dateTimeOnly>,<dateTimeOnly>)`

Restituisce un valore datetime senza considerare il fuso orario.

`max(<integer>,<integer>)`

Restituisce un numero intero.

## Esempi

`max(@event{BarBeacon.inventory},5)`

`max([10,3,8])`

Restituisce 10.

`max([10,null,8])`

Restituisce 10.
