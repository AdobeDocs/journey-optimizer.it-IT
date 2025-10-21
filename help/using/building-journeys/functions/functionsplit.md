---
product: journey optimizer
title: split
description: Scopri la suddivisione delle funzioni
feature: Journeys
role: Developer
level: Experienced
keywords: split, function, expression, percorsi
exl-id: 37bcdf98-203c-4f82-8d8a-be2b2c45c4e7
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 14%

---

# split {#split}

Divide la prima stringa di argomento con una stringa di separatore (seconda stringa di argomento, che può essere un&#39;espressione regolare) per produrre un elenco di stringhe (token).

## Categoria

Stringa

## Sintassi della funzione

`split(<parameters>)`

## Parametri

| Parametro | Tipo |
|-----------|------------------|
| stringa di input | stringa |
| stringa separatore | stringa |

## Firme e tipo restituito

`split(<input string>, <separator string>)`

Restituisce un valore listString.

## Esempio

`split("A_B_C", "_")`

Restituisce `["A","B","C"]`

Esempio con un campo evento &quot;event.appVersion&quot; con valore: &quot;20.45.2.3434&quot;

`split(@event{event.appVersion}, "\\.")`

Restituisce `["20", "45", "2", "3434"]`
