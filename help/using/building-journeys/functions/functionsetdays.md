---
product: journey optimizer
title: setDays
description: Scopri la funzione setDays
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: c2757e41-8206-44f7-9dbb-1fa79c0ba6e6
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 13%

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
| giorni | numero intero |

## Firme e tipo restituito

`setDays(<dateTime>,<days>)`

Restituisce un valore datetime.

`setDays(<dateTimeOnly>,<days>)`

Restituisce un valore datetime senza considerare il fuso orario.

## Esempi

`setDays(toDateTime('2010-12-12T01:11:00Z'), 25)`

Restituisce 2010-12-25T01:11:00Z.

`setDays(toDateTimeOnly(@{MyEvent.registrationDate}), 1)`
