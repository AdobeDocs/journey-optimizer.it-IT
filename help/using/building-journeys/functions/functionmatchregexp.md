---
product: journey optimizer
title: matchRegExp
description: Scopri la funzione matchRegExp
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: matchRegExp, funzione, espressione, percorso
exl-id: 24cf362c-f390-4bb1-be82-a079bc27fa1f
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 19%

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
| regexp | string |

## Firma e tipo restituito

`matchRegExp(<string>,<string>)`

Restituisce un valore booleano.

## Esempio

`matchRegExp("username@adobe.com", "*adobe")`

Restituisce true.
