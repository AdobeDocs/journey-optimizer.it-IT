---
product: journey optimizer
title: distinctCountWithNull
description: Scopri la funzione distinctCountWithNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinctCountWithNull, funzione, espressione, percorso
exl-id: 2c3f629f-2220-44a4-9b0c-8aa602301098
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 14%

---

# distinctCountWithNull {#distinctCountWithNull}

Conta il numero di valori diversi, inclusi i valori Null.

Il parametro `<listObject>` non è supportato in questa funzione.

## Categoria

Aggregazione

## Sintassi della funzione

`distinctCountWithNull(<listAny>)`

## Elemento “parameters”

| Parametro | Tipo |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

## Firma e tipo restituito

`distinctCountWithNull(<listAny>)`

Restituisce un numero intero.

## Esempio

`distinctCountWithNull([10,2,10,null])`

Restituisce 3.
