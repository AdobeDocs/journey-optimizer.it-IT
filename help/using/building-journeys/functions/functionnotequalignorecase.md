---
product: journey optimizer
title: notEqualIgnoreCase
description: Scopri la funzione notEqualIgnoreCase
feature: Journeys
role: Engineer
level: Experienced
keywords: notEqualIgnoreCase, funzione, espressione, percorso
exl-id: 74f8cae0-7d2f-4f5e-bc13-837c9bc69ad9
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '41'
ht-degree: 12%

---

# notEqualIgnoreCase {#notEqualIgnoreCase}

Verificare se la prima stringa di argomento con la seconda stringa di argomento è diversa, ignorando le considerazioni relative alle maiuscole e minuscole.

## Categoria

Stringa

## Sintassi della funzione

`notEqualIgnoreCase(<parameters>)`

## Parametri

* stringa

## Firma e tipo restituito

`notEqualIgnoreCase(<string>,<string>)`

Restituisce un valore booleano.

## Esempio

`notEqualIgnoreCase(@event{iOSPushPermissionAllowed.device.model}, "iPad")`
