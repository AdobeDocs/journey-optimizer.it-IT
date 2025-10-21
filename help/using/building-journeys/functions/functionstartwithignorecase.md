---
product: journey optimizer
title: startWithIgnoreCase
description: Scopri la funzione startWithIgnoreCase
feature: Journeys
role: Engineer
level: Experienced
keywords: startWithIgnoreCase, funzione, espressione, percorso
exl-id: b6bd9f77-272f-4c2b-b085-20ab5f043793
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 22%

---

# startWithIgnoreCase {#startWithIgnoreCase}

Restituisce true se il secondo parametro è un prefisso del primo senza considerare la distinzione tra maiuscole e minuscole.

## Categoria

Stringa

## Sintassi della funzione

`startWithIgnoreCase(<parameters>)`

## Parametri

| Parametro | Tipo |
|-------------|--------|
| stringa | stringa |
| prefisso | stringa |

## Firma e tipo restituito

`startWithIgnoreCase(<string>,<string>)`

Restituisce un valore booleano.

## Esempio

`startWithIgnoreCase("rowing is great", "RO")`

Restituisce true.
