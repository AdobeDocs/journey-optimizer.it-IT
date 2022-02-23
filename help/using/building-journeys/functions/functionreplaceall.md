---
product: adobe campaign
title: replaceAll
description: Scopri la funzione replaceAll
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 5543e123-a5f4-4153-8709-97eeb9be83ba
source-git-commit: 87b8056d26fe91a71e92ca346a9811c609d41128
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 10%

---

# replaceAll {#replaceAll}

Sostituisce tutte le occorrenze corrispondenti alla stringa di destinazione con la stringa di sostituzione nella stringa di base.

La sostituzione procede dall’inizio della stringa alla fine, ad esempio sostituendo &quot;aa&quot; con &quot;b&quot; nella stringa &quot;aaa&quot; si otterrà &quot;ba&quot; invece di &quot;ab&quot;.

## Categoria

Stringa

## Sintassi della funzione

`replaceAll(<parameters>)`

## Parametri

| Parametro | Tipo |
|-----------|--------------|
| base | stringa |
| target | string (RegExp) |
| sostituzione | stringa |

## Firma e tipo restituito

`replaceAll(<baseString>,<sourceString>,<replacementString>)`

Restituisce una stringa.

## Esempio{#example}

`replaceAll("Hello World", "l", "x")`

Restituisce &quot;Hexxo Worxd&quot;.

Poiché il parametro di destinazione è un RegExp, a seconda della stringa che desideri sostituire, potrebbe essere necessario applicare l’escape di alcuni caratteri. Fai riferimento all’esempio in [questa pagina](../functions/functionreplace.md#example_2).
