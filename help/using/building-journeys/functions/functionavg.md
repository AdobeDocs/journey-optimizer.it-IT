---
product: adobe campaign
title: avg
description: Scopri l’avg della funzione
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 12%

---

# avg {#avg}

Restituisce il valore medio tra un insieme di espressioni, dato come elenco o due espressioni. I valori Null vengono ignorati.


## Categoria

Aggregazione

## Sintassi della funzione

`avg(<parameter>)`

## Parametri

Tipi supportati:

* listInteger
* listDecimal
* decimale
* integer

## Firme e tipo restituito

`avg(<listInteger>)`

`avg(<listDecimal>)`

`avg(<decimal>,<decimal>)`

`avg(<decimal>,<integer>)`

`avg(<integer>,<decimal>)`

`avg(<integer>,<integer>)`

Restituisce un decimale.

## Esempi

`avg(@{BarBeacon.inventory},5)`

`avg([10,3,8])`

Restituisce 7,0.

`avg(10.2, 3)`

Restituisce 6.6.
