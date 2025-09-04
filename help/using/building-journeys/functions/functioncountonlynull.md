---
product: journey optimizer
title: countOnlyNull
description: Scopri la funzione countOnlyNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: countOnlyNull, funzione, espressione, percorso
exl-id: d06fc594-33dd-48ce-8c62-2f2892a867da
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
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

## Parametri

| Parametro | Tipo |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

## Firma e tipo restituito

`countOnlyNull(<listAny>)`

Restituisce un numero intero.

## Esempio

`countOnlyNull([10,2,10,null])`

Restituisce 1.
