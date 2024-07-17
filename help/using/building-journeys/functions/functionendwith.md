---
product: journey optimizer
title: endWith
description: Scopri la funzione endWith
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: endWith, funzione, espressione, percorso
exl-id: ae54c127-9de2-42fd-942c-664d2cfe66d2
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 23%

---

# endWith {#endWith}

Restituisce true se il secondo parametro è un suffisso del primo.

## Categoria

Stringa

## Sintassi della funzione

`endWith(<parameters>)`

## Elemento “parameters”

| Parametro | Tipo |
|-----------|------------------|
| stringa | stringa |
| suffisso | stringa |

## Firma e tipo restituito

`endWith(<string>,<string>)`

Restituisce un valore booleano.

## Esempio

`endWith("Hello World", "World")`

Restituisce true.

`endWith("Hello World", "Hello")`

Restituisce false.
