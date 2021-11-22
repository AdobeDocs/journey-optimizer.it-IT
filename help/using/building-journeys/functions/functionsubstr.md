---
product: adobe campaign
title: substr
description: Informazioni sul substr funzione
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 15%

---

# substr {#substr}

Restituisce la sottostringa dell&#39;espressione stringa tra l&#39;indice begin e l&#39;indice end. Se l&#39;indice finale non è definito, si trova tra l&#39;indice iniziale e la fine.

## Categoria

Stringa

## Sintassi della funzione

`substr(<parameters>)`

## Parametri

| Parametro | type |
|-------------|----------|
| stringa | stringa |
| beginIndex | integer |
| endIndex | integer |

## Firma e tipo restituito

`substr(<string>,<beginIndex>)`

`substr(<string>,<beginIndex>,<endIndex>)`

Restituisce una stringa.

## Esempio

`substr("Hello World",6)`

Restituisce &quot;World&quot;.

`substr("Hello World", 0, 5)`

Restituisce &quot;Hello&quot;.
