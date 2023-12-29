---
product: journey optimizer
title: startWith
description: Scopri la funzione startWith
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: startWith, funzione, espressione, percorso
exl-id: 1abdf947-2873-4e45-a26c-cb895980e76a
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
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
| string | string |
| prefisso | string |

## Firma e tipo restituito

`startWith(<string>,<string>)`

Restituisce un valore booleano.

## Esempio

`startWith("Hello World", "Hello")`

Restituisce true.

`startWith("Hello World", "World")`

Restituisce false.
