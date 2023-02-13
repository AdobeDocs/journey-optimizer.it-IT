---
product: journey optimizer
title: toInteger
description: Scopri la funzione toInteger
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: toInteger, funzione, espressione, percorso
exl-id: 901a91d1-13dd-4283-b87f-223196eb072f
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 14%

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
| string | converte il valore della stringa in un numero intero |
| dateTime | converte la data come numero di millisecondi (epoch millisecondi) |
| decimal | converte in numero intero rimuovendo la parte decimale (ad esempio: 1,5 diventa 1) |
| booleano | converte il valore booleano in 1 se true, 0 se false |

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
