---
product: journey optimizer
title: concatena
description: Informazioni sulla concatenazione delle funzioni
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: concat, funzione, espressione, percorso
exl-id: 690c8aa9-f754-4720-b4ed-a338e5d3b79d
version: Journey Orchestration
source-git-commit: 7ac246c0aa6776d3ec67223c4b07536b8ed0c881
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 25%

---

# concatena {#concat}

Concatena due parametri di stringa o un elenco di stringhe.

## Categoria

Stringa

## Sintassi della funzione

`concat(<parameters>)`

## Parametri

| Parametro | Tipo |
|-----------|------------------|
| Elenco | listString |
| stringa | stringa |

## Firma e tipo restituito

`concat(<string>,<string>)`

`concat(<listString>)`

Restituisce una stringa.

## Esempio

`concat("Hello","World")`

Restituisce &quot;HelloWorld&quot;.

`concat(["Hello"," ","World"])`

Restituisce &quot;Hello World&quot;.
