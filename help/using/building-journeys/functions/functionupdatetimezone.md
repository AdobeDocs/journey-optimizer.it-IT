---
product: adobe campaign
title: updateTimeZone
description: Scopri la funzione updateTimeZone
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 4695c88b4372a0f2a804bef268ae6f2d39eb2f0b
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 7%

---

# updateTimeZone {#updateTimeZone}

Restituisce una nuova data e un nuovo fuso orario nello stesso istante.

## Categoria

Data

## Sintassi della funzione

`updateTimeZone(<parameters>)`

## Parametri

* id fuso orario: string
* dateTime

## Firma e tipo restituito

`updateTimeZone(<dateTime>,<timeZone id>)`

Restituisce un valore datetime.

## Esempi

`updateTimeZone( toDateTime("2019-08-28T08:15:30.123-07:00"), "Europe/Paris"))`

Restituisce 2019-08-28T17:15:30.123+02:00.

<!--`updateTimeZone( toDateTime("2019-08-28T08:15:30.123-07:00"), toTimeZone("Europe/Paris")))`
Returns "2019-08-28T17:15:30.123+02:00".-->

`updateTimeZone(@{MyExpEvent.timestamp}, "Australia/Sydney")`

Se il valore del campo timestamp è `2021-11-16T16:55:12.939318+01:00`, quindi la funzione restituisce `2021-11-17T02:55:12.942115+11:00`.
