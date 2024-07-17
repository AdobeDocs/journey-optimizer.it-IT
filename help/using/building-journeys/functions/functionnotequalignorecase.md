---
product: journey optimizer
title: notEqualIgnoreCase
description: Scopri la funzione notEqualIgnoreCase
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: notEqualIgnoreCase, funzione, espressione, percorso
exl-id: 74f8cae0-7d2f-4f5e-bc13-837c9bc69ad9
source-git-commit: cb1fed2460ddbf3b226fe191b9695008970937c1
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

## Elemento “parameters”

* stringa

## Firma e tipo restituito

`notEqualIgnoreCase(<string>,<string>)`

Restituisce un valore booleano.

## Esempio

`notEqualIgnoreCase(@event{iOSPushPermissionAllowed.device.model}, "iPad")`
