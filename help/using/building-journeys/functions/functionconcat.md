---
product: adobe campaign
title: concat
description: Scopri la funzione concat
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
workflow-type: tm+mt
source-wordcount: '40'
ht-degree: 27%

---

# concat {#concat}

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
