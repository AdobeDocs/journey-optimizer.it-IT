---
product: journey optimizer
title: sort
description: Scopri l’ordinamento delle funzioni
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 607e1424-4165-48ae-b896-cce2d18f7dcc
source-git-commit: 0b19af568b33d29f4b35deeab6def17919cfe824
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 8%

---

# sort {#sort}

Ordina un elenco di valori o oggetti nell’ordine naturale.

>[!NOTE]
>
>Se l’elenco di destinazione è un listObject, è possibile utilizzare questa funzione solo nelle espressioni di azione personalizzate.

## Categoria

Elenco

## Sintassi della funzione

`sort(<parameters>)`

## Parametri

| Parametro | Tipo | Descrizione |
|-----------|------------------|------------------|
| listToSort | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly o listObject | Elenco da ordinare. Per listObject, deve essere un riferimento di campo. |
| keyAttributeName | stringa | Questo parametro è solo per listObject. Il nome dell’attributo negli oggetti dell’elenco specificato viene utilizzato come chiave per l’ordinamento. |
| sortOrder | booleano | Crescente (true) o decrescente (false) |

## Firma e tipo restituito

`sort(<listInteger>,<boolean>)`

Restituisce un elenco di numeri interi.

`sort(<listDecimal>,<boolean>)`

Restituisce un elenco di decimali.

`sort(<listString>,<boolean>)`

Restituisce un elenco di stringhe.

`sort(<listDateTimeOnly>,<boolean>)`

Restituisce un elenco di date senza considerare il fuso orario.

`sort(<listDateTime>,<boolean>)`

Restituisce un elenco di date.

`sort(<listDateOnly>,<boolean>)`

Restituisce un elenco di date.

`sort(<listBoolean>,<boolean>)`

Restituisce un elenco di booleani.

`sort(<listObject>,<string>,<boolean>)`

Restituisce un elenco di oggetti.

## Esempio

`sort(["A", "C", "B"], true)`

Restituisce `["A","B","C"]`.

`sort([1, 3, 2], false)`

Restituisce `[3, 2, 1]`.

