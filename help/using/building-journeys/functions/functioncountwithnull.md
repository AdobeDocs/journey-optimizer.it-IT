---
product: journey optimizer
title: countWithNull
description: Scopri la funzione countWithNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: countWithNull, funzione, espressione, percorso
exl-id: 8d53b6d8-f00f-4d1a-b6df-951f84a15430
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 29%

---

# countWithNull {#countWithNull}

Conta tutti gli elementi dell’elenco, inclusi i valori Null.

## Categoria

Aggregazione

## Sintassi della funzione

`countWithNull(<listAny>)`

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

`countWithNull(<listAny>)`

Restituisce un numero intero.

## Esempio

`countWithNull([10,2,10,null])`

Restituisce 4.
