---
product: adobe campaign
title: distinctCountWithNull
description: Scopri la funzione distinctCountWithNull
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: d786f3d42515d65a6574f51b6cff4b85063a0126
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 32%

---

# distinctCountWithNull {#distinctCountWithNull}

Conta il numero di valori diversi, inclusi i valori nulli.

## Categoria

Aggregazione

## Sintassi della funzione

`distinctCountWithNull(<listAny>)`

## Parametri

| Parametro | Tipo |
|-----------|------------------|
| Elenco | listString |
| Elenco | listBoolean |
| Elenco | listInteger |
| Elenco | listDecimal |
| Elenco | listDuration |
| Elenco | listDateTime |
| Elenco | listDateTimeOnly |
| Elenco | listDateOnly |

## Firma e tipo restituito

`distinctCountWithNull(<listAny>)`

Restituisce un numero intero.

## Esempio

`distinctCountWithNull([10,2,10,null])`

Restituisce 3.
