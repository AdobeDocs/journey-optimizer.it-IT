---
product: journey optimizer
title: countOnlyNull
description: Scopri la funzione countOnlyNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: countOnlyNull, funzione, espressione, percorso
exl-id: d06fc594-33dd-48ce-8c62-2f2892a867da
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 14%

---

# countOnlyNull {#countOnlyNull}

Conta il numero di valori Null nell&#39;elenco.

Il parametro `<listObject>` non è supportato in questa funzione.

## Categoria

Aggregazione

## Sintassi della funzione

`countOnlyNull(<listAny>)`

## Elemento “parameters”

| Parametro | Tipo |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

## Firma e tipo restituito

`countOnlyNull(<listAny>)`

Restituisce un numero intero.

## Esempio

`countOnlyNull([10,2,10,null])`

Restituisce 1.
