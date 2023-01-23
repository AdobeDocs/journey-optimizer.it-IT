---
product: journey optimizer
title: nowWithDelta
description: Scopri la funzione nowWithDelta
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: nowWithDelta, funzione, espressione, percorso
exl-id: cb1eb221-8532-4637-ac6c-8e058463ac94
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 7%

---

# nowWithDelta {#nowWithDelta}

Restituisce il datetime corrente, incluso un offset. Se viene specificato un ID del fuso orario, viene applicato l&#39;offset del fuso orario. Per ulteriori informazioni sui tipi di dati, consulta [questa pagina](../expression/data-types.md).

## Categoria

Data

## Sintassi della funzione

`nowWithDelta(<parameters>)`

## Parametri

| Parametro | Descrizione |
|--- |--- |
| delta | valore intero positivo o negativo |
| parte della data | anni, mesi, giorni, ore, minuti o secondi come stringa |
| id fuso orario | rappresentazione stringa del valore del fuso orario. Per ulteriori informazioni, consulta [Tipi di dati](../expression/data-types.md). L&#39;ID del fuso orario deve essere una costante stringa. Non può essere un riferimento di campo né un&#39;espressione. |

## Firme e tipo restituito

`nowWithDelta(<delta>,<date part>`

`nowWithDelta(<delta>,<date part>,"<timeZone id>")`

Restituisce un valore dateTime.

## Esempi

`nowWithDelta(-2, "hours")`

`nowWithDelta(-2, "hours", "Europe/Paris")`

Restituisce un dataTime esattamente 2 ore fa.
