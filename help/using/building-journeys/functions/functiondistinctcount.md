---
product: journey optimizer
title: distinctCount
description: Scopri la funzione distinctCount
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinctCount, funzione, espressione, percorso
exl-id: 8796ba91-5c64-43c2-a444-27ac8b719c86
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 7%

---

# distinctCount{#distinctCount}

Conta il numero di valori diversi ignorando i valori Null.

## Categoria

Aggregazione

## Sintassi della funzione

`distinctCount(<listAny>)`

## Elemento “parameters”

| Parametro | Tipo | Descrizione |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly o listObject | Elenco da elaborare. Per listObject, deve essere un riferimento di campo. |
| keyAttributeName | stringa | Questo parametro è facoltativo e solo per listObject. Se il parametro non viene fornito, un oggetto viene considerato duplicato se tutti gli attributi hanno gli stessi valori. In caso contrario, un oggetto viene considerato duplicato se l’attributo specificato ha lo stesso valore. |

## Firma e tipo restituito

`distinctCount(<listAny>)`

Restituisce un numero intero.

`distinctCount(<listObject>)`

`distinctCount(<listObject>,<string>)`

Restituisce un elenco di oggetti.


## Esempio

`distinctCount([10,2,10,null])`

Restituisce 2.

`distinctCount(@event{my_event.productListItems})`

Restituisce il numero di oggetti strettamente distinti nella matrice di oggetti specificata (tipo listObject).

`distinctCount(@event{my_event.productListItems}, "SKU")`

Restituisce il numero di oggetti con un valore di attributo &quot;SKU&quot; distinto{}.
