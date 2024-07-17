---
product: journey optimizer
title: min
description: Informazioni sulla funzione min
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: min, funzione, espressione, percorso
exl-id: 1c425d1d-08b4-446b-83ce-db376b2bf39f
source-git-commit: cb1fed2460ddbf3b226fe191b9695008970937c1
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 7%

---

# min {#min}

Restituisce il valore minimo in un insieme di espressioni, sotto forma di elenco o di due espressioni. I valori Null vengono ignorati.

## Categoria

Aggregazione

## Sintassi della funzione

`min(<parameters>)`

## Elemento “parameters”

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

`min(<listDuration>)`

Restituisce una durata.

`min(<listInteger>)`

Restituisce una durata.

`min(<listDateTimeOnly>)`

Restituisce un valore datetime senza considerare il fuso orario.

`min(<listDateTime>)`

Restituisce un valore datetime.

`min(<listDateOnly>)`

Restituisce una data.

`min(<listDecimal>)`

Restituisce un valore decimale.

`min(<decimal>,<decimal>)`

Restituisce un valore decimale.

`min(<duration>,<duration>)`

Restituisce una durata.

`min(<dateTime>,<dateTime>)`

Restituisce un valore datetime.

`min(<dateTimeOnly>,<dateTimeOnly>)`

Restituisce un valore datetime senza considerare il fuso orario.

`min(<integer>,<integer>)`

Restituisce un numero intero.

## Esempi

`min(@event{BarBeacon.inventory},5)`

`min([10,3,8])`

Restituisce 3.

`min([10,null,8])`

Restituisce 8.
