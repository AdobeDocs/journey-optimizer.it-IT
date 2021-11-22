---
product: adobe campaign
title: matchRegExp
description: Scopri la funzione matchRegExp
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 4695c88b4372a0f2a804bef268ae6f2d39eb2f0b
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 18%

---

# matchRegExp {#matchRegExp}

Restituisce true se la stringa nel primo parametro corrisponde all&#39;espressione regolare nel secondo parametro. Per ulteriori informazioni, consulta [questa pagina](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html).

## Categoria

Stringa

## Sintassi della funzione

`matchRegExp(<parameters>)`

## Parametri

| Parametro | Tipo |
|--- |--- |
| stringa | stringa |
| rigexp | stringa |

## Firma e tipo restituito

`matchRegExp(<string>,<string>)`

Restituisce un valore booleano.

## Esempio

`matchRegExp("username@adobe.com", "*adobe")`

Restituisce true.
