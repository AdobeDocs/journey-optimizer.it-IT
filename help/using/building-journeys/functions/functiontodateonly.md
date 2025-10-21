---
product: journey optimizer
title: toDateOnly
description: Scopri la funzione toDateOnly
feature: Journeys
role: Developer
level: Experienced
keywords: toDateOnly, funzione, espressione, percorso
exl-id: 1929644f-8b51-4f95-aea5-627fc1dd115d
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 10%

---

# toDateOnly{#toDateOnly}

Converte un argomento in un valore di tipo dateOnly. Per ulteriori informazioni sui tipi di dati, consulta questa [sezione](../expression/data-types.md).

## Categoria

Conversione

## Sintassi della funzione

`toDateOnly(<parameters>)`

## Parametri

| Parametro | Tipo |
|-----------|------------------|
| Rappresentazione stringa di una data come &quot;AAAA-MM-GG&quot; (formato XDM). Supporta anche il formato ISO-8601: viene considerata solo la parte **full-date** (consultare [RFC 3339, sezione 5.6](https://www.rfc-editor.org/rfc/rfc3339#section-5.6) | stringa |
| data e ora | dateTime |
| data e ora senza fuso orario | dateTimeOnly |
| valore intero di un’epoca in millisecondi | intero |

## Firme e tipi restituiti

`toDateOnly(<dateTime>)`

`toDateOnly(<dateTimeOnly>)`

`toDateOnly(<string>)`

`toDateOnly(<integer>, <integer>, <integer>)`

Restituisce un valore di tipo dateOnly.

## Esempi

`toDateOnly("2023-08-18")`

`toDateOnly("2023-08-18T00:00:00.000Z")`

`toDateOnly("2023-08-18T00:00:00")`

tutti restituiscono un oggetto dateOnly che rappresenta il 18 agosto 2023.

`toDateOnly(#{ExperiencePlatform.ProfileFieldGroup.person.birthDate})`

Restituisce un valore dateOnly.
