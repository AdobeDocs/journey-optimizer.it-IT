---
product: journey optimizer
title: filter
description: Scopri il filtro funzione
feature: Journeys
role: Engineer
level: Experienced
keywords: filter, function, expression, percorsi
exl-id: 05e3d2ba-1a27-4f27-88cc-3d83eb3b14af
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 9%

---

# filter{#filter}

Restituisce un oggetto listObject con oggetti il cui attributo chiave corrisponde a uno dei valori chiave specificati.

## Categoria

Elenco

## Sintassi della funzione

`filter(<parameters>)`

## Parametri

| Parametro | Tipo | Descrizione |
|-----------|------------------|------------------|
| listToFilter | listObject | elenco di oggetti da filtrare. Deve essere un riferimento di campo. |
| keyAttributeName | stringa | nome attributo negli oggetti dell’elenco specificato, utilizzato come chiave per il filtro |
| keyValueList | list | array di valori chiave per il filtro |

## Firme e tipi restituiti

`filter(listObject, string, listString)`

`filter(listObject, string, listInteger)`

`filter(listObject, string, listDecimal)`

`filter(listObject, string, listDateTime)`

`filter(listObject, string, listDateTimeOnly)`

`filter(listObject, string, listDateOnly)`

`filter(listObject, string, listDuration)`

`filter(listObject, string, listBoolean)`

Restituisce un oggetto listObject.

## Esempi

Ecco un esempio di payload passato in un evento in ingresso &quot;myevent&quot;:

```json
"productListItems": [{
   "id": "product1",
   "name": "the product 1",
   "price": 20
},{
   "id": "product2",
   "name": "the product 2",
   "price": 30
},{
   "id": "product3",
   "name": "the product 3",
   "price": 50
}]
```

È possibile utilizzare la seguente espressione:

```json
filter(
 @event{myevent.productListItems},
 "id", 
 ["product2", "product3", "product4"]
)
```

Restituisce un oggetto listObject contenente i due oggetti con &quot;product2&quot; e &quot;product3&quot; come id.
