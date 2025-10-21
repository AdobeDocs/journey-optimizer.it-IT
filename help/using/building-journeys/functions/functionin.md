---
product: journey optimizer
title: in
description: Scopri la funzione in
feature: Journeys
role: Engineer
level: Experienced
keywords: in, funzione, espressione, percorso
exl-id: 629b7aa3-8904-453b-ba3c-c6a333b13c81
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 23%

---

# in {#in}

Controlla se il primo valore di argomento è presente nell&#39;elenco. Il controllo viene eseguito tramite un valore Uguale su ciascun argomento. Restituisce true se viene trovato il valore dell’argomento, in caso contrario false.

Il tipo di `<expression>` deve corrispondere agli elementi dell&#39;elenco. I tipi di elementi dell&#39;elenco, come promemoria, devono corrispondere tra loro.

## Categoria

Elenco

## Sintassi della funzione

`in(<parameters>)`

## Parametri

| Parametro | Tipo |
|-----------|------------------|
| Stringa | Stringa |
| Booleano | Booleano |
| Intero | Intero |
| Decimale | Decimale |
| Durata | Durata |
| Data e ora | Data e ora |
| DateTimeOnly | DateTimeOnly |
| Elenco | listString |
| Elenco | listBoolean |
| Elenco | listInteger |
| Elenco | listDecimal |
| Elenco | listDuration |
| Elenco | listDateTime |
| Elenco | listDateTimeOnly |
| Elenco | listDateOnly |

## Firma e tipo restituito

`in(<integer>,<listInteger>)`

`in(<decimal>,<listDecimal>)`

`in(<string>,<listString>)`

`in(<boolean>,<listBoolean>)`

`in(<dateTimeOnly>,<listDateTimeOnly>)`

`in(<dateTime>,<listDateTime>)`

`in(<dateOnly>,<listDateOnly>)`

`in(<duration>,<listDuration>)`

Restituisce un valore booleano.

## Esempio

`in(4,[4,5,3,4])`

Restituisce true.

`in(8,[4,5,3,4])`

Restituisce false.

`in(#{ExperiencePlatform.ProfileFieldGroup.profile.person.gender}, ["male"])`
