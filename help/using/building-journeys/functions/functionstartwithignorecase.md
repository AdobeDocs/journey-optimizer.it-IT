---
product: journey optimizer
title: startWithIgnoreCase
description: Scopri la funzione startWithIgnoreCase
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: startWithIgnoreCase, funzione, espressione, percorso
exl-id: b6bd9f77-272f-4c2b-b085-20ab5f043793
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
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

## Elemento “parameters”

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
