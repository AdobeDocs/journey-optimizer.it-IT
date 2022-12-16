---
product: journey optimizer
title: notEqualIgnoreCase
description: Scopri la funzione notEqualIgnoreCase
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 74f8cae0-7d2f-4f5e-bc13-837c9bc69ad9
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '37'
ht-degree: 13%

---

# notEqualIgnoreCase {#notEqualIgnoreCase}

Verificare che la prima stringa di argomento con la seconda stringa di argomento sia diversa, ignorando le considerazioni relative a maiuscole e minuscole.

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

`notEqualIgnoreCase(@{iOSPushPermissionAllowed.device.model}, "iPad")`
