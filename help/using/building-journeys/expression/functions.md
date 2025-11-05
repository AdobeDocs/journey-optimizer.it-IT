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
source-git-commit: d58319d687d113ce680c415524fdea0400cb38f0
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
| Conversione | [toBool](../functions/conversion-functions.md#toBool) |
| Conversione | [toDateOnly](../functions/conversion-functions.md#toDateOnly) |
| Conversione | [toDateTime](../functions/conversion-functions.md#toDateTime) |
| Conversione | [toDateTimeOnly](../functions/conversion-functions.md#toDateTimeOnly) |
| Conversione | [toDecimal](../functions/conversion-functions.md#toDecimal) |
| Conversione | [toDuration](../functions/conversion-functions.md#toDuration) |
| Conversione | [toInteger](../functions/conversion-functions.md#toInteger) |
| Conversione | [toString](../functions/conversion-functions.md#toString) |
| Data | [currentTimeInMillis](../functions/date-functions.md#currentTimeInMillis) |
| Data | [inLastDays](../functions/date-functions.md#inLastDays) |
| Data | [inLastHours](../functions/date-functions.md#inLastHours) |
| Data | [inLastMonths](../functions/date-functions.md#inLastMonths) |
| Data | [inLastYears](../functions/date-functions.md#inLastYears) |
| Data | [inNextDays](../functions/date-functions.md#inNextDays) |
| Data | [inNextHours](../functions/date-functions.md#inNextHours) |
| Data | [inNextMonths](../functions/date-functions.md#inNextMonths) |
| Data | [inNextYears](../functions/date-functions.md#inNextYears) |
| Data | [now](../functions/date-functions.md#now) |
| Data | [nowWithDelta](../functions/date-functions.md#nowWithDelta) |
| Data | [setHours](../functions/date-functions.md#setHours) |
| Data | [setDays](../functions/date-functions.md#setDays) |
| Data | [updateTimeZone](../functions/date-functions.md#updateTimeZone) |
| Elenco | [distinct](../functions/list-functions.md#distinct) |
| Elenco | [distinctWithNull](../functions/list-functions.md#distinctWithNull) |
| Elenco | [filtro](../functions/list-functions.md#filter) |
| Elenco | [getListItem](../functions/list-functions.md#getListItem) |
| Elenco | [in](../functions/list-functions.md#in) |
| Elenco | [intersezione](../functions/list-functions.md#intersect) |
| Elenco | [limite](../functions/list-functions.md#limit) |
| Elenco | [listSize](../functions/list-functions.md#listSize) |
| Elenco | [serializeList](../functions/list-functions.md#serializeList) |
| Elenco | [sort](../functions/list-functions.md#sort) |
| Matematica | [random](../functions/functionrandom.md) |
| Matematica | [round](../functions/functionround.md) |
| Stringa | [concat](../functions/string-functions.md#concat) |
| Stringa | [contain](../functions/string-functions.md#contain) |
| Stringa | [containIgnoreCase](../functions/string-functions.md#containIgnoreCase) |
| Stringa | [endWith](../functions/string-functions.md#endWith) |
| Stringa | [endWithIgnoreCase](../functions/string-functions.md#endWithIgnoreCase) |
| Stringa | [equalIgnoreCase](../functions/string-functions.md#equalIgnoreCase) |
| Stringa | [indexOf](../functions/string-functions.md#indexOf) |
| Stringa | [isEmpty](../functions/string-functions.md#isEmpty) |
| Stringa | [isNotEmpty](../functions/string-functions.md#isNotEmpty) |
| Stringa | [lastIndexOf](../functions/string-functions.md#lastIndexOf) |
| Stringa | [length](../functions/string-functions.md#length) |
| Stringa | [Lower](../functions/string-functions.md#lower) |
| Stringa | [matchRegExp](../functions/string-functions.md#matchRegExp) |
| Stringa | [notEqualIgnoreCase](../functions/string-functions.md#notEqualIgnoreCase) |
| Stringa | [replace](../functions/string-functions.md#replace) |
| Stringa | [replaceAll](../functions/string-functions.md#replaceAll) |
| Stringa | [split](../functions/string-functions.md#split) |
| Stringa | [startWith](../functions/string-functions.md#startWith) |
| Stringa | [startWithIgnoreCase](../functions/string-functions.md#startWithIgnoreCase) |
| Stringa | [substr](../functions/string-functions.md#substr) |
| Stringa | [trim](../functions/string-functions.md#trim) |
| Stringa | [upper](../functions/string-functions.md#upper) |
| Stringa | [uuid](../functions/string-functions.md#uuid) |
