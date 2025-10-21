---
product: journey optimizer
title: replaceAll
description: Scopri la funzione replaceAll
feature: Journeys
role: Developer
level: Experienced
keywords: replaceAll, funzione, espressione, percorso
exl-id: 5543e123-a5f4-4153-8709-97eeb9be83ba
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 10%

---

# replaceAll {#replaceAll}

Sostituisce tutte le occorrenze che corrispondono alla stringa di destinazione con la stringa di sostituzione nella stringa di base.

La sostituzione procede dall&#39;inizio della stringa alla fine, ad esempio, sostituendo &quot;aa&quot; con &quot;b&quot; nella stringa &quot;aaa&quot; si otterrà &quot;ba&quot; invece di &quot;ab&quot;.

## Categoria

Stringa

## Sintassi della funzione

`replaceAll(<parameters>)`

## Parametri

| Parametro | Tipo |
|-----------|--------------|
| base | stringa |
| destinazione | stringa (RegExp) |
| sostituzione | stringa |

## Firma e tipo restituito

`replaceAll(<baseString>,<sourceString>,<replacementString>)`

Restituisce una stringa.

## Esempio{#example}

`replaceAll("Hello World", "l", "x")`

Restituisce &quot;Hexxo Worxd&quot;.

Poiché il parametro di destinazione è un RegExp, a seconda della stringa che si desidera sostituire, potrebbe essere necessario eseguire l&#39;escape di alcuni caratteri. Fai riferimento all&#39;esempio in [questa pagina](../functions/functionreplace.md#example_2).
