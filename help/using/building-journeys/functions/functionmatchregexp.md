---
product: journey optimizer
title: matchRegExp
description: Scopri la funzione matchRegExp
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: matchRegExp, funzione, espressione, percorso
exl-id: 24cf362c-f390-4bb1-be82-a079bc27fa1f
source-git-commit: 9e6b3fc5c91e360a9bd7e727949ac5445cd79654
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 19%

---

# matchRegExp {#matchRegExp}

Restituisce true se la stringa nel primo parametro corrisponde all&#39;espressione regolare nel secondo parametro. Per ulteriori informazioni, vedere [questa pagina](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html).

## Categoria

Stringa

## Sintassi della funzione

`matchRegExp(<parameters>)`

## Parametri

| Parametro | Tipo |
|--- |--- |
| stringa | stringa |
| regexp | stringa |

## Firma e tipo restituito

`matchRegExp(<string>,<string>)`

Restituisce un valore booleano.

## Esempio

`matchRegExp("12345", "\\d+")`

Restituisce true.
