---
product: adobe campaign
title: countOnlyNull
description: Scopri la funzione countOnlyNull
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: d06fc594-33dd-48ce-8c62-2f2892a867da
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 33%

---

# countOnlyNull {#countOnlyNull}

Conta il numero di valori nulli nell’elenco.

## Categoria

Aggregazione

## Sintassi della funzione

`countOnlyNull(<listAny>)`

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

`countOnlyNull(<listAny>)`

Restituisce un numero intero.

## Esempio

`countOnlyNull([10,2,10,null])`

Restituisce 1.
