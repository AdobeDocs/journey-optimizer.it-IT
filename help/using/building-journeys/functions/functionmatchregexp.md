---
product: journey optimizer
title: matchRegExp
description: Scopri la funzione matchRegExp
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 24cf362c-f390-4bb1-be82-a079bc27fa1f
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 0%

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
| string | string |
| rigexp | string |

## Firma e tipo restituito

`matchRegExp(<string>,<string>)`

Restituisce un valore booleano.

## Esempio

`matchRegExp("username@adobe.com", "*adobe")`

Restituisce true.
