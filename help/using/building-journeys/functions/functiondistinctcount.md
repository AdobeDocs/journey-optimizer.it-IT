---
product: adobe campaign
title: distinctCount
description: Scopri la funzione distinctCount
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 8796ba91-5c64-43c2-a444-27ac8b719c86
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 32%

---

# distinctCount{#distinctCount}

Conta il numero di valori diversi ignorando i valori nulli.

## Categoria

Aggregazione

## Sintassi della funzione

`distinctCount(<listAny>)`

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

`distinctCount(<listAny>)`

Restituisce un numero intero.

## Esempio

`distinctCount([10,2,10,null])`

Restituisce 2.
