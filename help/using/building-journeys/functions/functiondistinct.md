---
product: adobe campaign
title: distinct
description: Scopri il distinto funzione
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: f4e2dd34-b634-4a91-af53-60be155a65d0
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 18%

---

# distinto {#distinct}

Restituisce i valori distinti dell’elenco senza valori nulli.

## Categoria

Elenco

## Sintassi della funzione

`distinct(<parameter>)`

## Parametri

| Parametro | Tipo |
|-----------|------------------|
| Elenco | listString |
| Elenco | listBoolean |
| Elenco | listInteger |
| Elenco | listDecimal |
| Elenco | listDuration |
| Elenco | listDateTime |
| Elenco | listDateTimeOnly |
| Elenco | listDateOnly |

## Firme e tipi restituiti

`distinct(<listInteger>)`

Restituisce un elenco di numeri interi.

`distinct(<listDecimal>)`

Restituisce un elenco di decimali.

`distinct(<listString>)`

Restituisce un elenco di stringhe.

`distinct(<listDateTimeOnly>)`

Restituisce un elenco di date senza considerare il fuso orario.

`distinct(<listDateTime>)`

Restituisce un elenco di date.

`distinct(<listDateOnly>)`

Restituisce un elenco di date.

`distinct(<listBoolean>)`

Restituisce un elenco di booleani.

`distinct(<listDuration>)`

Restituisce un elenco di durate.

## Esempi

`distinct([10,2,10,null])`

Restituisce `[10, 2]`.
