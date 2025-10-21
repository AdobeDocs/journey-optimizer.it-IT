---
product: journey optimizer
title: containIgnoreCase
description: Scopri la funzione containIgnoreCase
feature: Journeys
role: Engineer
level: Experienced
keywords: containIgnoreCase, funzione, espressione, percorso
exl-id: 26074584-a215-4515-8a61-7460bd9d4447
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 21%

---

# containIgnoreCase {#containIgnoreCase}

Controlla se la seconda stringa di argomento è contenuta nella prima stringa di argomento, senza tenere conto della distinzione tra maiuscole e minuscole.

## Categoria

Stringa

## Sintassi della funzione

`containIgnoreCase(<parameters>)`

## Parametri

| Parametro | Tipo |
|-----------|------------------|
| stringa | stringa |
| stringa cercata | stringa |

## Firma e tipo restituito

`containIgnoreCase(<string>,<string>)`

Restituisce un valore booleano.

## Esempio

`containIgnoreCase("rowing is great", "GREAT")`

Restituisce true.
