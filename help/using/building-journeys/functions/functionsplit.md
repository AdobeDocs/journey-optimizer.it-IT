---
product: journey optimizer
title: split
description: Scopri la suddivisione della funzione
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: divisione, funzione, espressione, percorso
exl-id: 37bcdf98-203c-4f82-8d8a-be2b2c45c4e7
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 17%

---

# split {#split}

Divide la prima stringa argomento con una stringa separatore (seconda stringa argomento, che può essere un’espressione regolare) per generare un elenco di stringhe (token).

## Categoria

Stringa

## Sintassi della funzione

`split(<parameters>)`

## Parametri

| Parametro | Tipo |
|-----------|------------------|
| stringa di input | string |
| stringa separatore | string |

## Firme e tipo restituito

`split(<input string>, <separator string>)`

Restituisce un valore listString.

## Esempio

`split(["A_B_C"], "_")`

Restituisce `["A","B","C"]`

Esempio con un campo evento &#39;event.appVersion&#39; con valore: &quot;20.45.2.3434&quot;

`split(@{event.appVersion}, "\\.")`

Restituisce `["20", "45", "2", "3434"]`
