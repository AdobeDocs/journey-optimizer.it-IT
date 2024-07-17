---
product: journey optimizer
title: endWithIgnoreCase
description: Scopri la funzione endWithIgnoreCase
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: endWithIgnoreCase, funzione, espressione, percorso
exl-id: 278ef1a4-571c-4b5f-b4de-0cfc644ac7d7
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 17%

---

# endWithIgnoreCase {#endWithIgnoreCase}

Controlla se la stringa del primo argomento termina con una stringa specifica (stringa del secondo argomento), senza tenere conto delle maiuscole/minuscole.

## Categoria

Stringa

## Sintassi della funzione

`endWithIgnoreCase(<parameters>)`

## Elemento “parameters”

| Parametro | Tipo |
|-----------|------------------|
| stringa | stringa |
| suffisso | stringa |

## Firma e tipo restituito

`endWithIgnoreCase(<string>,<string>)`

Restituisce un valore booleano.

## Esempio

`endWithIgnoreCase("rowing is great", "AT")`

Restituisce true.
