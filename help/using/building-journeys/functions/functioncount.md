---
product: journey optimizer
title: conteggio
description: Scopri il conteggio delle funzioni
feature: Journeys
role: Developer
level: Experienced
keywords: count, function, expression, percorsi
exl-id: 6980c1ec-3afd-4fc9-ae10-76bcf7364a04
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 10%

---

# conteggio {#count}

Conta gli elementi dell’elenco senza tenere conto dei valori nulli.

## Categoria

Aggregazione

## Sintassi della funzione

`count(<listAny>)`

`count(<listObject>)`

## Parametri

| Parametro | Tipo | Descrizione |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly o listObject | Elenco da elaborare. Per listObject, deve essere un riferimento di campo. Un listObject non può contenere un oggetto null. |

## Firme e tipo restituito

`count(<listAny>)`

Restituisce un numero intero.

## Esempio

`count([10,2,10,null])`

Restituisce 3.

`count(@event{my_event.productListItems})`

Restituisce il numero di oggetti nella matrice di oggetti specificata (tipo listObject). Nota: listObject non può contenere un oggetto null
