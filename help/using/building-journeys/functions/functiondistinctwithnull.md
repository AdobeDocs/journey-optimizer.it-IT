---
product: journey optimizer
title: distinctWithNull
description: Scopri la funzione distinctWithNull
feature: Journeys
role: Developer
level: Experienced
keywords: distinctWithNull, funzione, espressione, percorso
exl-id: 73fa9837-d2e1-4f0a-a423-cf7728882eba
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 7%

---

# distinctWithNull {#distinctWithNull}

Restituisce i valori o gli oggetti distinti di un elenco specifico. Se l&#39;elenco include almeno una voce Null, nell&#39;elenco restituito sarà presente una voce Null.

Il parametro `<listObject>` non è supportato in questa funzione.

## Categoria

Elenco

## Sintassi della funzione

`distinctWithNull(<parameters>)`

## Parametri

| Parametro | Tipo | Descrizione |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly | Elenco da elaborare. |

## Firme e tipi restituiti

`distinctWithNull(<listInteger>)`

Restituisce un elenco di numeri interi.

`distinctWithNull(<listDecimal>)`

Restituisce un elenco di decimali.

`distinctWithNull(<listString>)`

Restituisce un elenco di stringhe.

`distinctWithNull(<listDateTimeOnly>)`

Restituisce un elenco di date senza considerare il fuso orario.

`distinctWithNull(<listDateTime>)`

Restituisce un elenco di date.

`distinctWithNull(<listDateOnly>)`

Restituisce un elenco di date.

`distinctWithNull(<listBoolean>)`

Restituisce un elenco di booleani.

`distinctWithNull(<listDuration>)`

Restituisce un elenco di durate.

## Esempi

`distinctWithNull([10,2,10,null])`

Restituisce [10, 2, null]
