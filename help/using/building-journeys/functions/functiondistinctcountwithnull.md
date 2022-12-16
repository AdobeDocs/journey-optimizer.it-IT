---
product: journey optimizer
title: distinctCountWithNull
description: Scopri la funzione distinctCountWithNull
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 2c3f629f-2220-44a4-9b0c-8aa602301098
source-git-commit: 0b19af568b33d29f4b35deeab6def17919cfe824
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 24%

---

# distinctCountWithNull {#distinctCountWithNull}

Conta il numero di valori diversi, inclusi i valori nulli.

>[!NOTE]
>
>Se l’elenco di destinazione è un listObject, è possibile utilizzare questa funzione solo nelle espressioni di azione personalizzate.

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
