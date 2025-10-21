---
product: journey optimizer
title: getListItem
description: Scopri la funzione gstListItem
feature: Journeys
role: Developer
level: Experienced
keywords: getListItem, funzione, espressione, percorso
exl-id: e995f479-bbaa-45f3-9531-e05680c5a723
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 18%

---

# getListItem {#gestListItem}

Restituisce l&#39;elemento dell&#39;elenco in corrispondenza dell&#39;indice specificato.

## Categoria

Elenco

## Sintassi della funzione

`getListItem(<parameters>)`

## Parametri

| Parametro | Tipo |
|-----------|------------------|
| list | listString |
| list | listBoolean |
| list | listInteger |
| list | listDecimal |
| list | listDuration |
| list | listDateTime |
| list | listDateTimeOnly |
| list | listDateOnly |
| index | intero |

## Firme e tipo restituito

`getListItem(<listInteger>,<index>)`

Restituisce un numero intero.

`getListItem(<listDecimal>,<index>)`

Restituisce un valore decimale.

`getListItem(<listString>,<index>)`

Restituisce una stringa.

`getListItem(<listDateTimeOnly>,<index>)`

Restituisce un valore datetime senza considerare il fuso orario.

`getListItem(<listDateTime>,<index>)`

Restituisce un valore datetime.

`getListItem(<listDateOnly>,<index>)`

Restituisce un elenco di date.

`getListItem(<listBoolean>,<index>)`

Restituisce un valore booleano.

`getListItem(<listDuration>,<index>)`

Restituisce una durata.

## Esempio

`getListItem([10, 2, 3], 1)`

Restituisce &quot;2&quot;

`getListItem(["A", "B", "C"], 2)`
Restituisce &quot;C&quot;

Esempi con un campo evento &quot;event.appVersion&quot; con valore: &quot;20.45.2.3434&quot;

`split(@event{event.appVersion}, "\\.")`

Restituisce `["20", "45", "2", "3434"]`

`getListItem(split(@event{event.appVersion}, "\\."), 0)`

Restituisce &quot;20&quot;
