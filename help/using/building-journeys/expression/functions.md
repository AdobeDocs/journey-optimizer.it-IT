---
solution: Journey Optimizer
product: journey optimizer
title: Funzioni
description: Informazioni sulle funzioni
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 5b978eef-7d3e-41fe-bb08-0cf37c3b125d
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---

# Funzioni {#functions}

Una funzione può avere firme diverse (un diverso insieme di parametri ordinati). Una firma di funzione può avere espressioni 0-N come parametri ordinati.

`<function name>`(`<expression as param 1>`, `<expression as param 2>`, ...`<expression as param N>`)

Ogni funzione ha un tipo restituito specifico.

Elenco delle funzioni supportate.

## Funzioni principali

| Categoria | Funzione |
|-------------|-----------------------|
| Adobe Experience Platform | [inSegment](../functions/functioninsegment.md) |
| Aggregazione | [avg](../functions/functionavg.md) |
| Aggregazione | [count](../functions/functioncount.md) |
| Aggregazione | [countOnlyNull](../functions/functioncountonlynull.md) |
| Aggregazione | [countWithNull](../functions/functioncountwithnull.md) |
| Aggregazione | [distinctCount](../functions/functiondistinctcount.md) |
| Aggregazione | [distinctCountWithNull](../functions/functiondistinctcountwithnull.md) |
| Aggregazione | [max](../functions/functionmax.md) |
| Aggregazione | [min](../functions/functionmin.md) |
| Aggregazione | [sum](../functions/functionsum.md) |
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
| Elenco | [distinto](../functions/functiondistinct.md) |
| Elenco | [distinctWithNull](../functions/functiondistinctwithnull.md) |
| Elenco | [filter](../functions/functionfilter.md) |
| Elenco | [getListItem](../functions/functiongetlistitem.md) |
| Elenco | [in](../functions/functionin.md) |
| Elenco | [intersecare](../functions/functionintersect.md) |
| Elenco | [listSize](../functions/functionlimit.md) |
| Elenco | [listSize](../functions/functionlistsize.md) |
| Elenco | [serializeList](../functions/functionserializelist.md) |
| Elenco | [sort](../functions/functionsort.md) |
| Matematica | [casuale](../functions/functionrandom.md) |
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
| Stringa | [startWith](../functions/functionstartwith.md) |
| Stringa | [startWithIgnoreCase](../functions/functionstartwithignorecase.md) |
| Stringa | [substr](../functions/functionsubstr.md) |
| Stringa | [trim](../functions/functiontrim.md) |
| Stringa | [superiore](../functions/functionupper.md) |
| Stringa | [uuid](../functions/functionuuid.md) |
