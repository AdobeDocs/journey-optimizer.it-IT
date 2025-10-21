---
product: journey optimizer
title: toDecimal
description: Scopri la funzione toDecimal
feature: Journeys
role: Engineer
level: Experienced
keywords: decimal, function, expression, percorsi
exl-id: d761fa4d-5f99-4dee-b747-3eab464c4071
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 13%

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
| stringa | converte il valore stringa come decimale |
| dateTime | converte la data in millisecondi (millisecondi epoca) |
| booleano | converte il valore booleano come 1 se true, 0 se false |
| intero | converte in un decimale (ad esempio.: 1 diventa 1,0) |

## Firme e tipi restituiti

`toDecimal(<integer>)`

`toDecimal(<decimal>)`

`toDecimal(<string>)`

`toDecimal(<boolean>)`

Restituisce un decimale.

## Esempi

`toDecimal("4.0")`

Restituisce 4,0.
