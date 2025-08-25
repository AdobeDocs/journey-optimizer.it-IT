---
product: journey optimizer
title: sum
description: Informazioni sulla somma delle funzioni
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: sum, function, expression, percorsi
exl-id: a9085f4d-6434-4bc5-8e5d-3f2b6033defc
source-git-commit: cb1fed2460ddbf3b226fe191b9695008970937c1
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 12%

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
* intero
* decimale

## Firme e tipi restituiti

`sum(<listDecimal>)`

Restituisce un valore decimale.

`sum(<listInteger>)`

Restituisce un numero intero.

`sum(<integer>,<integer>)`

Restituisce un numero intero.

`sum(<decimal>,<decimal>)`

Restituisce un valore decimale.

## Esempi

`sum(@event{BarBeacon.inventory},5)`

`sum([10,3,8])`

Restituisce 21.

`sum([10.5,null,8.1])`

Restituisce 18,6.
