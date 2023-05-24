---
product: journey optimizer
title: sort
description: Scopri l’ordinamento delle funzioni
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: sort, function, expression, percorsi
exl-id: 607e1424-4165-48ae-b896-cce2d18f7dcc
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 8%

---

# sort {#sort}

Ordina un elenco di valori o oggetti nell&#39;ordine naturale.

>[!NOTE]
>
>Se l’elenco di destinazione è un listObject, questa funzione può essere utilizzata solo nelle espressioni di azione personalizzate.

## Categoria

Elenco

## Sintassi della funzione

`sort(<parameters>)`

## Parametri

| Parametro | Tipo | Descrizione |
|-----------|------------------|------------------|
| listToSort | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly o listObject | Elenco da ordinare. Per listObject, deve essere un riferimento di campo. |
| keyAttributeName | string | Questo parametro è solo per listObject. Il nome dell’attributo negli oggetti dell’elenco specificato viene utilizzato come chiave per l’ordinamento. |
| ordinamentoOrdine | booleano | Crescente (true) o Decrescente (false) |

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

