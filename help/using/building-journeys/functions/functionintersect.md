---
product: journey optimizer
title: intersect
description: Scopri l’intersezione della funzione
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: interseca, funzione, espressione, percorso
exl-id: e236efa9-91a8-4f08-94c6-45f1e060bb2f
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 12%

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

Restituisce [&quot;sport&quot;, &quot;notizie&quot;]

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
    ["sports", "news", "documentary"]
)
```

Restituisce elementi comuni tra gli attributi del profilo e un elenco di categorie specificato.

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
        @{myEvent.sport_interests}
)
```

Restituisce elementi comuni tra gli attributi del profilo e il campo evento specificato.
