---
product: adobe campaign
title: count
description: Informazioni sul conteggio delle funzioni
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 6980c1ec-3afd-4fc9-ae10-76bcf7364a04
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 30%

---

# count {#count}

Conta gli elementi dell’elenco che non tengono conto dei valori nulli.

## Categoria

Aggregazione

## Sintassi della funzione

`count(<listAny>)`

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

## Firme e tipo restituito

`count(<listAny>)`

Restituisce un numero intero.

## Esempio

`count([10,2,10,null])`

Restituisce 3.
