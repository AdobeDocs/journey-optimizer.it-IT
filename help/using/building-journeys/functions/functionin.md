---
product: journey optimizer
title: in
description: Scopri la funzione in
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: in, funzione, espressione, percorso
exl-id: 629b7aa3-8904-453b-ba3c-c6a333b13c81
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 18%

---

# in {#in}

Controlla se il primo valore dell&#39;argomento si trova nell&#39;elenco. Il controllo viene eseguito tramite un valore Equal per ogni valore di argomento. Restituisce true se il valore dell&#39;argomento viene trovato, false in caso contrario.

Il tipo di `<expression>` deve corrispondere agli elementi dell’elenco. I tipi di elementi dell’elenco, come promemoria, devono corrispondere tra loro.

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
| DateTime | DateTime |
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
