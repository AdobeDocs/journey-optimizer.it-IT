---
product: journey optimizer
title: countWithNull
description: Scopri la funzione countWithNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: countWithNull, funzione, espressione, percorso
exl-id: 8d53b6d8-f00f-4d1a-b6df-951f84a15430
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 14%

---

# countWithNull {#countWithNull}

Conta tutti gli elementi dell’elenco, inclusi i valori Null.

Il parametro `<listObject>` non è supportato in questa funzione.

## Categoria

Aggregazione

## Sintassi della funzione

`countWithNull(<listAny>)`

## Elemento “parameters”

| Parametro | Tipo |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

## Firma e tipo restituito

`countWithNull(<listAny>)`

Restituisce un numero intero.

## Esempio

`countWithNull([10,2,10,null])`

Restituisce 4.
