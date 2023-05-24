---
product: journey optimizer
title: serializeList
description: Scopri la funzione serializeList
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: serializeList, funzione, espressione, percorso
exl-id: 7ead9fa1-59b3-4960-818c-fe6321422952
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 21%

---

# serializeList {#serializeList}

Converte l&#39;elenco (qualsiasi tipo) specificato nel primo parametro in una stringa. Il secondo parametro rappresenta il separatore da utilizzare. Il terzo parametro è un valore booleano che indica se ogni elemento dell’espressione deve includere virgolette.

## Categoria

Elenco

## Sintassi della funzione

`serializeList(<parameters>)`

## Parametri

| Parametro | Tipo |
|-----------|------------------|
| Stringa | Stringa |
| Booleano | Booleano |
| DateTimeOnly | DateTimeOnly |
| Elenco | listString |
| Elenco | listBoolean |
| Elenco | listPoint |
| Elenco | listDecimal |
| Elenco | listDuration |
| Elenco | listDateTime |
| Elenco | listDateTimeOnly |
| Elenco | listDateOnly |

## Firma e tipo restituito

`serializeList(<listInteger>,<string>,<boolean>)`

`serializeList(<listDecimal>,<string>,<boolean>)`

`serializeList(<listString>,<string>,<boolean>)`

`serializeList(<listBoolean>,<string>,<boolean>)`

`serializeList(<listDateTimeOnly>,<string>,<boolean>)`

`serializeList(<listDateTime>,<string>,<boolean>)`

`serializeList(<listDateOnly>,<string>,<boolean>)`

`serializeList(<listDuration>,<string>,<boolean>)`

`serializeList(<listPoint>,<string>,<boolean>)`

Restituisce una stringa.

## Esempio

`serializeList(["Hello","World"], " ", false)`

Restituisce &quot;Hello World&quot;.

`serializeList(["Hello", "World"], ",", true)`

Restituisce &quot;&quot;Hello&quot;,&quot;World&quot;&quot;.
