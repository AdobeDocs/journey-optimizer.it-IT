---
product: journey optimizer
title: limit
description: Scopri il limite di funzioni
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: limite, funzione, espressione, percorso
exl-id: 7fa1e393-2912-4392-b759-e54d08d5635a
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 8%

---

# limit {#limit}

Restituisce il primo o l’ultimo N elementi di un elenco.

>[!NOTE]
>
>Se l’elenco di destinazione è un listObject, è possibile utilizzare questa funzione solo nelle espressioni di azione personalizzate.

## Categoria

Elenco

## Sintassi della funzione

`limit(<parameters>)`

## Parametri

| Parametro | Tipo | Descrizione |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly o listObject | Elenco da ordinare. Per listObject, deve essere un riferimento di campo. |
| numberOfItems | numero intero | Numero di elementi da restituire dall’elenco specificato. |
| firstOrLastItems | booleano | Questo parametro è facoltativo (true per impostazione predefinita). true restituisce i primi elementi. false restituisce gli ultimi elementi. |

## Firma e tipo restituito

`limit(<listString>,<integer>)`
`limit(<listString>,<integer>,<boolean>)`

Restituisce un elenco di stringhe.

`limit(<listInteger>,<integer>)`
`limit(<listInteger>,<integer>,<boolean>)`

Restituisce un elenco di numeri interi.

`limit(<listDecimal>,<integer>)`
`limit(<listDecimal>,<integer>,<boolean>)`

Restituisce un elenco di decimali.

`limit(<listBoolean>,<integer>)`
`limit(<listBoolean>,<integer>,<boolean>)`

Restituisce un elenco di booleani.

`limit(<listDateOnly>,<integer>)`
`limit(<listDateOnly>,<integer>,<boolean>)`

Restituisce un elenco di date.

`limit(<listDateTimeOnly>,<integer>)`
`limit(<listDateTimeOnly>,<integer>,<boolean>)`

Restituisce un elenco di date senza considerare il fuso orario.

`limit(<listDateTime>,integer>)`
`limit(<listDateTime>,<integer>,<boolean>)`

Restituisce un elenco di date.

`limit(<listDuration>,<integer>)`
`limit(<listDuration>,<integer>,<boolean>)`

Restituisce un elenco di durate.

`limit(<listObject>,<integer>)`
`limit(<listObject>,<integer>,<boolean>)`

Restituisce un elenco di oggetti.

## Esempio

`limit(["A", "B", "C", "D", "E"], 3)`

Restituisce `["A","B","C"]`.

`limit(["A", "B", "C", "D", "E"], 3, false)`

Restituisce `["C","D","E"]`.
