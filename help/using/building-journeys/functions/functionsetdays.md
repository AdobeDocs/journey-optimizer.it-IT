---
product: adobe campaign
title: setDays
description: Scopri la funzione setDays
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 12%

---

# setDays {#setDays}

Imposta solo il giorno dell’ora o dell’ora della data. Ad esempio, se desideri attendere fino a un determinato giorno del mese, puoi forzare il giorno .

## Categoria

Data

## Sintassi della funzione

`setDays(<parameter>)`

## Parametri

| Parametro | Tipo |
|--- |--- |
| ora | dateTime |
| data e ora senza considerare il fuso orario | dateTimeOnly |
| giorni | integer |

## Firme e tipo restituito

`setDays(<dateTime>,<days>)`

Restituisce un valore datetime.

`setDays(<dateTimeOnly>,<days>)`

Restituisce un valore datetime senza considerare il fuso orario.

## Esempi

`setDays(toDateTime('2010-12-12T01:11:00Z'), 25)`

Restituisce 2010-12-25T01:11:00Z.

`setDays(toDateTimeOnly(@{MyEvent.registrationDate}), 1)`
