---
product: adobe campaign
title: sum
description: Scopri la somma delle funzioni
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: a9085f4d-6434-4bc5-8e5d-3f2b6033defc
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '51'
ht-degree: 13%

---

# sum {#sum}

Restituisce la somma dei valori di un insieme di espressioni. I valori Null vengono ignorati.

## Categoria

Aggregazione

## Sintassi della funzione

`sum(<parameters>)`

## Parametri

* listInteger
* listDecimal
* durata
* numero intero
* decimale

## Firme e tipi restituiti

`sum(<listDecimal>)`

Restituisce un decimale.

`sum(<listInteger>)`

Restituisce un numero intero.

`sum(<integer>,<integer>)`

Restituisce un numero intero.

`sum(<decimal>,<decimal>)`

Restituisce un decimale.

## Esempi

`sum(@{BarBeacon.inventory},5)`

`sum([10,3,8])`

Restituisce 21.

`sum([10.5,null,8.1])`

Restituisce 18,6.
