---
product: adobe campaign
title: replaceAll
description: Scopri la funzione replaceAll
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 16%

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
| target | stringa |
| sostituzione | stringa |

## Firma e tipo restituito

`replaceAll(<baseString>,<sourceString>,<replacementString>)`

Restituisce una stringa.

## Esempio

`replaceAll("Hello World", "l", "x")`

Restituisce &quot;Hexxo Worxd&quot;.
