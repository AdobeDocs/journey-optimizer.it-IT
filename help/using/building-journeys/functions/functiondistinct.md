---
product: journey optimizer
title: distinct
description: Scopri il distinto della funzione
feature: Journeys
role: Engineer
level: Experienced
keywords: distinct, function, expression, percorsi
exl-id: f4e2dd34-b634-4a91-af53-60be155a65d0
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 6%

---

# distinct {#distinct}

Restituisce i valori o gli oggetti distinti di un elenco specifico. Le voci Null vengono ignorate.

## Categoria

Elenco

## Sintassi della funzione

`distinct(<parameters>)`

## Parametri

| Parametro | Tipo | Descrizione |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly o listObject | Elenco da elaborare. Per listObject, deve essere un riferimento di campo. |
| keyAttributeName | stringa | Questo parametro è facoltativo e solo per listObject. Se il parametro non viene fornito, un oggetto viene considerato duplicato se tutti gli attributi hanno gli stessi valori. In caso contrario, un oggetto viene considerato duplicato se l’attributo specificato ha lo stesso valore. |

## Firme e tipi restituiti

`distinct(<listInteger>)`

Restituisce un elenco di numeri interi.

`distinct(<listDecimal>)`

Restituisce un elenco di decimali.

`distinct(<listString>)`

Restituisce un elenco di stringhe.

`distinct(<listDateTimeOnly>)`

Restituisce un elenco di date senza considerare il fuso orario.

`distinct(<listDateTime>)`

Restituisce un elenco di date.

`distinct(<listDateOnly>)`

Restituisce un elenco di date.

`distinct(<listBoolean>)`

Restituisce un elenco di booleani.

`distinct(<listDuration>)`

Restituisce un elenco di durate.

`distinct(<listObject>)`

`distinct(<listObject>,<string>)`

Restituisce un elenco di oggetti.


## Esempi

`distinct([10,2,10,null])`

Restituisce `[10, 2]`.
