---
product: journey optimizer
title: startWith
description: Scopri la funzione startWith
feature: Journeys
role: Developer
level: Experienced
keywords: startWith, funzione, espressione, percorso
exl-id: 1abdf947-2873-4e45-a26c-cb895980e76a
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 23%

---

# startWith {#startWith}

Restituisce true se il secondo parametro è un prefisso del primo.

## Categoria

Stringa

## Sintassi della funzione

`startWith(<parameters>)`

## Parametri

| Parametro | Tipo |
|-------------|--------|
| stringa | stringa |
| prefisso | stringa |

## Firma e tipo restituito

`startWith(<string>,<string>)`

Restituisce un valore booleano.

## Esempio

`startWith("Hello World", "Hello")`

Restituisce true.

`startWith("Hello World", "World")`

Restituisce false.
