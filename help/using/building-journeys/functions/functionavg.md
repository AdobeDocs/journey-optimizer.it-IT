---
product: journey optimizer
title: avg
description: Scopri la funzione media
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: avg, function, expression, percorsi
exl-id: cc70f90c-2d12-42a0-829f-5f28c3c29cad
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 12%

---

# avg {#avg}

Restituisce il valore medio tra un insieme di espressioni, sotto forma di elenco o di due espressioni. I valori Null vengono ignorati.


## Categoria

Aggregazione

## Sintassi della funzione

`avg(<parameter>)`

## Parametri

Tipi supportati:

* listInteger
* listDecimal
* decimale
* intero

## Firme e tipo restituito

`avg(<listInteger>)`

`avg(<listDecimal>)`

`avg(<decimal>,<decimal>)`

`avg(<decimal>,<integer>)`

`avg(<integer>,<decimal>)`

`avg(<integer>,<integer>)`

Restituisce un valore decimale.

## Esempi

`avg(@event{BarBeacon.inventory},5)`

`avg([10,3,8])`

Restituisce 7,0.

`avg(10.2, 3)`

Restituisce 6,6.
