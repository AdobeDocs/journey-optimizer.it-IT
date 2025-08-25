---
product: journey optimizer
title: serializeList
description: Scopri la funzione serializeList
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: serializeList, funzione, espressione, percorso
exl-id: 7ead9fa1-59b3-4960-818c-fe6321422952
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 12%

---

# serializeList {#serializeList}

Converte un elenco specifico (qualsiasi tipo eccetto listObject) in una stringa.

## Categoria

Elenco

## Sintassi della funzione

`serializeList(<parameters>)`

## Parametri

| Parametro | Tipo | Descrizione |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly | Elenco da convertire in stringa. |
| separatore | stringa | Separatore tra ciascun elemento elenco nella stringa di output. |
| addQuotes | booleano | Questo parametro indica se ogni elemento nella stringa di output deve includere virgolette (true) o meno (false). |

## Firma e tipo restituito

`serializeList(<listInteger>,<string>,<boolean>)`

`serializeList(<listDecimal>,<string>,<boolean>)`

`serializeList(<listString>,<string>,<boolean>)`

`serializeList(<listBoolean>,<string>,<boolean>)`

`serializeList(<listDateTimeOnly>,<string>,<boolean>)`

`serializeList(<listDateTime>,<string>,<boolean>)`

`serializeList(<listDateOnly>,<string>,<boolean>)`

`serializeList(<listDuration>,<string>,<boolean>)`

Restituisce una stringa.

## Esempio

`serializeList(["Hello","World"], " ", false)`

Restituisce &quot;Hello World&quot;.

`serializeList(["Hello", "World"], ",", true)`

Restituisce &quot;&quot;Hello&quot;,&quot;World&quot;&quot;.
