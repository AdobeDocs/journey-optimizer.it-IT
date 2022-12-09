---
product: journey optimizer
title: intersecare
description: Scopri l’intersezione della funzione
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: e236efa9-91a8-4f08-94c6-45f1e060bb2f
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---

# intersecare{#intersect}

Restituisce i valori comuni nei due elenchi di input. Se uno dei due elenchi è nullo, restituisce un elenco vuoto.

## Categoria

Elenco

## Sintassi della funzione

`intersect(<parameters>)`

## Parametri

| Parametro | Tipo |
|-----------|------------------|
| elenco 1 | elenco |
| elenco 2 | elenco |

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
