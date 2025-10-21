---
product: journey optimizer
title: substr
description: Informazioni sul sottoster della funzione
feature: Journeys
role: Developer
level: Experienced
keywords: substr, function, expression, percorsi
exl-id: 58a3107a-b4f3-43da-b454-5ce597515847
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 17%

---

# substr {#substr}

Restituisce la sottostringa dell&#39;espressione stringa tra l&#39;indice iniziale e l&#39;indice finale. Se l&#39;indice finale non è definito, si trova tra l&#39;indice iniziale e la fine.

## Categoria

Stringa

## Sintassi della funzione

`substr(<parameters>)`

## Parametri

| Parametro | tipo |
|-------------|----------|
| stringa | stringa |
| beginIndex | intero |
| endIndex | intero |

## Firma e tipo restituito

`substr(<string>,<beginIndex>)`

`substr(<string>,<beginIndex>,<endIndex>)`

Restituisce una stringa.

## Esempio

`substr("Hello World",6)`

Restituisce &quot;World&quot;.

`substr("Hello World", 0, 5)`

Restituisce &quot;Hello&quot;.
