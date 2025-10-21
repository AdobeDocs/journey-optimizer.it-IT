---
product: journey optimizer
title: setHours
description: Scopri la funzione setHours
feature: Journeys
role: Engineer
level: Experienced
keywords: setHours, funzione, espressione, percorso
exl-id: ed78c2a9-d83a-4fac-a2e9-7383da131a1f
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 9%

---

# setHours {#setHours}

Imposta solo le ore di una data/ora o data/ora. Ad esempio, se desideri aspettare fino a un’ora specifica domani, puoi forzare l’ora.

## Categoria

Data

## Sintassi della funzione

`setHours(<parameter>)`

## Parametri

| Parametro | Tipo |
|--- |--- |
| data e ora | dateTime |
| data e ora senza considerare il fuso orario | dateTimeOnly |
| ore | intero |

## Firme e tipo restituito

`setHours(<dateTime>,<hours>)`

Restituisce un valore datetime.

`setHours(<dateTimeOnly>,<hours>)`

Restituisce un valore datetime senza considerare il fuso orario.

## Esempi

`setHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

Restituisce 2023-12-12T04:11:00Z.

`setHours(nowWithDelta(1, "days"), 20)`

Restituisce domani alle 20.00, dove XY corrisponde ai minuti al momento della valutazione dell&#39;ora corrente. :XY Se la valutazione viene eseguita alle 02:00, l&#39;ora restituita sarà le 20:00.:45:45
