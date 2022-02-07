---
product: adobe campaign
title: endWith
description: Scopri la funzione endWith
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: ae54c127-9de2-42fd-942c-664d2cfe66d2
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '43'
ht-degree: 25%

---

# endWith {#endWith}

Restituisce true se il secondo parametro è un suffisso del primo.

## Categoria

Stringa

## Sintassi della funzione

`endWith(<parameters>)`

## Parametri

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
