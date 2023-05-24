---
product: journey optimizer
title: distinctCountWithNull
description: Scopri la funzione distinctCountWithNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinctCountWithNull, funzione, espressione, percorso
exl-id: 2c3f629f-2220-44a4-9b0c-8aa602301098
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 22%

---

# distinctCountWithNull {#distinctCountWithNull}

Conta il numero di valori diversi, inclusi i valori Null.

>[!NOTE]
>
>Se l’elenco di destinazione è un listObject, questa funzione può essere utilizzata solo nelle espressioni di azione personalizzate.

## Categoria

Aggregazione

## Sintassi della funzione

`distinctCountWithNull(<listAny>)`

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

## Firma e tipo restituito

`distinctCountWithNull(<listAny>)`

Restituisce un numero intero.

## Esempio

`distinctCountWithNull([10,2,10,null])`

Restituisce 3.
