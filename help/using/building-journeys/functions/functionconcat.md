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
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
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
