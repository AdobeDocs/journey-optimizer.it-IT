---
product: journey optimizer
title: updateTimeZone
description: Scopri la funzione updateTimeZone
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: updateTimeZone, funzione, espressione, percorso
exl-id: 1bf4662e-55d0-4631-af93-1430ec7ed7e2
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 10%

---

# updateTimeZone {#updateTimeZone}

Restituisce una nuova data e ora, con un nuovo fuso orario nello stesso istante.

## Categoria

Data

## Sintassi della funzione

`updateTimeZone(<parameters>)`

## Parametri

* id fuso orario: stringa
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
