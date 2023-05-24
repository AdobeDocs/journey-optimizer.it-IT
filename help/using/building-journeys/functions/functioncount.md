---
product: journey optimizer
title: count
description: Scopri il conteggio delle funzioni
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: count, function, expression, percorsi
exl-id: 6980c1ec-3afd-4fc9-ae10-76bcf7364a04
source-git-commit: ad113c0414b20ac2f758ad06a44315b24a3d3d0c
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 28%

---

# count {#count}

Conta gli elementi dell’elenco senza tenere conto dei valori nulli.

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
