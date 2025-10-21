---
product: journey optimizer
title: intersect
description: Scopri l’intersezione della funzione
feature: Journeys
role: Developer
level: Experienced
keywords: intersezione, funzione, espressione, percorso
exl-id: e236efa9-91a8-4f08-94c6-45f1e060bb2f
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 11%

---

# intersect{#intersect}

Restituisce i valori comuni nei due elenchi di input. Se uno dei due elenchi è nullo, restituisce un elenco vuoto.

## Categoria

Elenco

## Sintassi della funzione

`intersect(<parameters>)`

## Parametri

| Parametro | Tipo |
|-----------|------------------|
| elenco 1 | list |
| elenco 2 | list |

## Firme e tipi restituiti

`intersect(listString,listString)`: listString
`intersect(listDecimal,listDecimal)`: listDecimal
`intersect(listInteger,listInteger)`: listInteger
`intersect(listDateTime,listDateTime)`: listDateTime
`intersect(listDateTimeOnly,listDateTimeOnly)`: listDateTimeOnly
`intersect(listDateOnly,listDateOnly)`: listDateOnly
`intersect(listDuration,listDuration)`: listDuration
`intersect(listBoolean,listBoolean)`: listBoolean

Restituisce un elenco.

## Esempi

```json
intersect(
    ["sports", "news", "documentary"],
    ["sports", "movies", "documentary"]
)
```

Restituisce [&quot;sport&quot;, &quot;news&quot;]

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
    ["sports", "documentary"]
)
```

Restituisce elementi comuni tra gli attributi del profilo e un elenco specifico di categorie.

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
        @event{myEvent.sport_interests}
)
```

Restituisce elementi comuni tra gli attributi del profilo e il campo evento specificato.
