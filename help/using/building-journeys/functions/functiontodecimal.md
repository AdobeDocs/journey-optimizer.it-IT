---
product: adobe campaign
title: toDecimal
description: Scopri la funzione suDecimal
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: d761fa4d-5f99-4dee-b747-3eab464c4071
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 14%

---

# toDecimal {#toDecimal}

Converte un valore di argomento in un valore decimale, a seconda del tipo.

## Categoria

Conversione

## Sintassi della funzione

`toDecimal(<parameter>)`

## Parametri

| Parametro | Descrizione |
|--- |--- |
| stringa | converte il valore della stringa come decimale |
| dateTime | converte la data come numero di millisecondi (epoch millisecondi) |
| booleano | converte il valore booleano in 1 se true, 0 se false |
| integer | converte in un decimale (ad esempio.: 1 diventa 1,0) |

## Firme e tipi restituiti

`toDecimal(<integer>)`

`toDecimal(<decimal>)`

`toDecimal(<string>)`

`toDecimal(<boolean>)`

Restituisce un decimale.

## Esempi

`toDecimal("4.0")`

Restituisce 4,0.
