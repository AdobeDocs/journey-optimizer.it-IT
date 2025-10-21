---
product: journey optimizer
title: listSize
description: Scopri la funzione listSize
feature: Journeys
role: Engineer
level: Experienced
keywords: listSize, function, expression, percorsi
exl-id: dd378e4d-f65a-495c-ac10-b4209d6b6b88
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 11%

---

# listSize {#listSize}

Conta il numero di elementi nell&#39;elenco.

## Categoria

Elenco

## Sintassi della funzione

`listSize(<parameters>)`

## Parametri

| Parametro | Tipo | Descrizione |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly o listObject | Elenco da elaborare. Per listObject, deve essere un riferimento di campo. Un listObject non può contenere un oggetto null. |

## Firme e tipo restituito

`listSize(<listInteger>)`

`listSize(<listDecimal>)`

`listSize(<listString>)`

`listSize(<listBoolean>)`

`listSize(<listDateTimeOnly>)`

`listSize(<listDateTime>)`

`listSize(<listDateOnly>)`

`listSize(<listDuration>)`

Restituisce un numero intero.

`listSize(<listObject>)`

## Esempio

`listSize([10,2,3])`

Restituisce 3.

`listSize(@event{my_event.productListItems})`

Restituisce il numero di oggetti nella matrice di oggetti specificata (tipo listObject).
