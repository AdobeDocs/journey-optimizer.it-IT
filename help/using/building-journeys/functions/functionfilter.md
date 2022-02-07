---
product: adobe campaign
title: filter
description: Scopri il filtro funzione
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 05e3d2ba-1a27-4f27-88cc-3d83eb3b14af
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 10%

---

# filter{#filter}

Restituisce un listObject con oggetti con l’attributo chiave corrispondente a uno dei valori chiave specificati.

## Categoria

Elenco

## Sintassi della funzione

`filter(<parameters>)`

## Parametri

| Parametro | Tipo | Descrizione |
|-----------|------------------|------------------|
| listToFilter | listObject | elenco di oggetti da filtrare. Deve essere un riferimento di campo. |
| keyAttributeName | stringa | nome dell’attributo negli oggetti dell’elenco specificato, utilizzato come chiave per il filtraggio |
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

Restituisce un valore listObject.

## Esempi

Ecco un esempio di payload trasmesso in un evento in arrivo &quot;myevent&quot;:

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
 @{myevent.productListItems},
 "id", 
 ["product2", "product3", "product4"]
)
```

Restituisce un listObject contenente i due oggetti con &quot;product2&quot; e &quot;product3&quot; come id.
