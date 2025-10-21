---
product: journey optimizer
title: startWithIgnoreCase
description: Scopri la funzione startWithIgnoreCase
feature: Journeys
role: Developer
level: Experienced
keywords: startWithIgnoreCase, funzione, espressione, percorso
exl-id: b6bd9f77-272f-4c2b-b085-20ab5f043793
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
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
