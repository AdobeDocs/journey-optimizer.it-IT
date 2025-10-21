---
product: journey optimizer
title: toInteger
description: Scopri la funzione toInteger
feature: Journeys
role: Engineer
level: Experienced
keywords: toInteger, funzione, espressione, percorso
exl-id: 901a91d1-13dd-4283-b87f-223196eb072f
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 12%

---

# toInteger {#toInteger}

Converte un valore di argomento in un numero intero.

## Categoria

Conversione

## Sintassi della funzione

`toInteger(<parameter>)`

## Parametri

| Parametro | Descrizione |
|--- |--- |
| stringa | converte il valore stringa come numero intero |
| dateTime | converte la data in millisecondi (millisecondi epoca) |
| decimale | converte in numero intero rimuovendo la parte decimale (ad esempio: 1,5 diventa 1) |
| booleano | converte il valore booleano come 1 se true, 0 se false |

## Firme e tipo restituito

`toInteger(<dateTime>)`

`toInteger(<decimal>)`

`toInteger(<integer>)`

`toInteger(<string>)`

`toInteger(<boolean>)`

Restituisce un numero intero.

## Esempi

`toInteger("4")`

Restituisce 4.
