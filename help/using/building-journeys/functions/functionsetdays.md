---
product: journey optimizer
title: setDays
description: Scopri la funzione setDays
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: setDays, funzione, espressione, percorso
exl-id: c2757e41-8206-44f7-9dbb-1fa79c0ba6e6
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 11%

---

# setDays {#setDays}

Imposta solo il giorno di un&#39;ora o di una data. Ad esempio, se desideri attendere fino a un determinato giorno del mese, puoi forzare il giorno.

## Categoria

Data

## Sintassi della funzione

`setDays(<parameter>)`

## Parametri

| Parametro | Tipo |
|--- |--- |
| data e ora | dateTime |
| data e ora senza considerare il fuso orario | dateTimeOnly |
| giorni | numero intero |

## Firme e tipo restituito

`setDays(<dateTime>,<days>)`

Restituisce un valore datetime.

`setDays(<dateTimeOnly>,<days>)`

Restituisce un valore datetime senza considerare il fuso orario.

## Esempi

`setDays(toDateTime('2023-12-12T01:11:00Z'), 25)`

Restituisce 2023-12-25T01:11:00Z

`setDays(toDateTimeOnly(@event{MyEvent.registrationDate}), 1)`
