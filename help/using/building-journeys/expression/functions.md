---
solution: Journey Optimizer
product: journey optimizer
title: Funzioni
description: Informazioni sulle funzioni
feature: Journeys
role: Developer
level: Experienced
keywords: funzione, espressioni, editor, percorso
exl-id: 5b978eef-7d3e-41fe-bb08-0cf37c3b125d
version: Journey Orchestration
source-git-commit: af1babe501a5b2c6a67730396a8f5e2c5d85e60a
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 69%

---

# Funzioni {#functions}

Una funzione può avere firme diverse (un diverso set di parametri ordinati). Una firma di funzione può avere espressioni 0-N come parametri ordinati.

`<function name>`(`<expression as param 1>`, `<expression as param 2>`, ... ,`<expression as param N>`)

Ogni funzione ha un tipo restituito specifico.

Elenco delle funzioni supportate.

## Funzioni principali

| Categoria | Funzione |
|-------------|-----------------------|
| Adobe Experience Platform | [inAudience](../functions/functioninaudience.md) |
| Aggregazione | [avg](../functions/aggregation-functions.md#avg) |
| Aggregazione | [count](../functions/aggregation-functions.md#count) |
| Aggregazione | [countOnlyNull](../functions/aggregation-functions.md#countOnlyNull) |
| Aggregazione | [countWithNull](../functions/aggregation-functions.md#countWithNull) |
| Aggregazione | [distinctCount](../functions/aggregation-functions.md#distinctCount) |
| Aggregazione | [distinctCountWithNull](../functions/aggregation-functions.md#distinctCountWithNull) |
| Aggregazione | [max](../functions/aggregation-functions.md#max) |
| Aggregazione | [min](../functions/aggregation-functions.md#min) |
| Aggregazione | [sum](../functions/aggregation-functions.md#sum) |
| Conversione | [toBool](../functions/functiontobool.md) |
| Conversione | [toDateOnly](../functions/functiontodateonly.md) |
| Conversione | [toDateTime](../functions/functiontodatetime.md) |
| Conversione | [toDateTimeOnly](../functions/functiontodatetimeonly.md) |
| Conversione | [toDecimal](../functions/functiontodecimal.md) |
| Conversione | [toDuration](../functions/functiontoduration.md) |
| Conversione | [toInteger](../functions/functiontointeger.md) |
| Conversione | [toString](../functions/functiontostring.md) |
| Data | [currentTimeInMillis](../functions/functioncurrenttimeinmillis.md) |
| Data | [inLastDays](../functions/functioninlastdays.md) |
| Data | [inLastHours](../functions/functioninlasthours.md) |
| Data | [inLastMonths](../functions/functioninlastmonths.md) |
| Data | [inLastYears](../functions/functioninlastyears.md) |
| Data | [inNextDays](../functions/functioninnextdays.md) |
| Data | [inNextHours](../functions/functioninnexthours.md) |
| Data | [inNextMonths](../functions/functioninnextmonths.md) |
| Data | [inNextYears](../functions/functioninnextyears.md) |
| Data | [now](../functions/functionnow.md) |
| Data | [nowWithDelta](../functions/functionnowwithdelta.md) |
| Data | [setHours](../functions/functionsethours.md) |
| Data | [setDays](../functions/functionsetdays.md) |
| Data | [updateTimeZone](../functions/functionupdatetimezone.md) |
| Elenco | [distinct](../functions/functiondistinct.md) |
| Elenco | [distinctWithNull](../functions/functiondistinctwithnull.md) |
| Elenco | [filtro](../functions/functionfilter.md) |
| Elenco | [getListItem](../functions/functiongetlistitem.md) |
| Elenco | [in](../functions/functionin.md) |
| Elenco | [intersezione](../functions/functionintersect.md) |
| Elenco | [limite](../functions/functionlimit.md) |
| Elenco | [listSize](../functions/functionlistsize.md) |
| Elenco | [serializeList](../functions/functionserializelist.md) |
| Elenco | [sort](../functions/functionsort.md) |
| Matematica | [random](../functions/functionrandom.md) |
| Matematica | [round](../functions/functionround.md) |
| Stringa | [concat](../functions/functionconcat.md) |
| Stringa | [contain](../functions/functioncontain.md) |
| Stringa | [containIgnoreCase](../functions/functioncontainwithignorecase.md) |
| Stringa | [endWith](../functions/functionendwith.md) |
| Stringa | [endWithIgnoreCase](../functions/functionendwithignorecase.md) |
| Stringa | [equalIgnoreCase](../functions/functionequalignorecase.md) |
| Stringa | [indexOf](../functions/functionindexof.md) |
| Stringa | [isEmpty](../functions/functionisempty.md) |
| Stringa | [isNotEmpty](../functions/functionisnotempty.md) |
| Stringa | [lastIndexOf](../functions/functionlastindexof.md) |
| Stringa | [length](../functions/functionlength.md) |
| Stringa | [Lower](../functions/functionlower.md) |
| Stringa | [matchRegExp](../functions/functionmatchregexp.md) |
| Stringa | [notEqualIgnoreCase](../functions/functionnotequalignorecase.md) |
| Stringa | [replace](../functions/functionreplace.md) |
| Stringa | [replaceAll](../functions/functionreplaceall.md) |
| Stringa | [split](../functions/functionsplit.md) |
| Stringa | [startWith](../functions/functionstartwith.md) |
| Stringa | [startWithIgnoreCase](../functions/functionstartwithignorecase.md) |
| Stringa | [substr](../functions/functionsubstr.md) |
| Stringa | [trim](../functions/functiontrim.md) |
| Stringa | [upper](../functions/functionupper.md) |
| Stringa | [uuid](../functions/functionuuid.md) |
