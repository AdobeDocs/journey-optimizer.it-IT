---
product: adobe campaign
title: toDateOnly
description: Scopri la funzione toDateOnly
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 21%

---

# toDateOnly{#toDateOnly}

Converte un valore di argomento in un valore di sola data.

## Categoria

Conversione

## Sintassi della funzione

`toDateOnly(<parameters>)`

## Parametri

| Parametro | Tipo |
|-----------|------------------|
| data in formato ISO-8601 o &quot;AAAA-MM-GG&quot; (formato XDM Data) | stringa |
| data | data |

## Firme e tipi restituiti

`toDateOnly(<date>)`

`toDateOnly(<string>)`

Restituisce un datetime senza considerare il fuso orario.

## Esempi

`toDateOnly("2016-08-18")`

restituisce un oggetto dateOnly che rappresenta 2016-08-18.
