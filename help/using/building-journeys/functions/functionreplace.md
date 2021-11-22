---
product: adobe campaign
title: replace
description: Informazioni sulla sostituzione della funzione
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 3eb35fd6-2d11-4f24-b0d9-5334e7ed7872
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 15%

---

# replace {#replace}

Sostituisce la prima occorrenza che corrisponde alla stringa di destinazione dalla stringa di sostituzione nella stringa di base.

La sostituzione procede dall’inizio della stringa alla fine, ad esempio sostituendo &quot;aa&quot; con &quot;b&quot; nella stringa &quot;aaa&quot; si otterrà &quot;ba&quot; invece di &quot;ab&quot;.

## Categoria

Stringa

## Sintassi della funzione

`replace(<parameters>)`

## Parametri

| Parametro | Tipo |
|-----------|--------------|
| base | stringa |
| target | stringa |
| sostituzione | stringa |

## Firma e tipo restituito

`replace(<base>,<target>,<replacement>)`

Restituisce una stringa.

## Esempio

`replace("Hello World", "l", "x")`

Restituisce &quot;Hexlo World&quot;.
