---
product: journey optimizer
title: toDateTime
description: Scopri la funzione toDateTime
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: toDateTime, funzione, espressione, percorso
exl-id: 2b487e60-593e-4bf7-9639-f469ba0f5cdc
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 10%

---

# toDateTime {#toDateTime}

Converte i parametri in un valore di data e ora, a seconda del tipo.

## Categoria

Conversione

## Sintassi della funzione

`toDateTime(<parameters>)`

## Elemento “parameters”

| Parametro | Tipo |
|-----------|------------------|
| data e ora nel formato ISO-8601 | stringa |
| id fuso orario | stringa |
| data e ora senza fuso orario | dateTimeOnly |
| valore intero di un’epoca in millisecondi | intero |

>[!NOTE]
>
>L’ID del fuso orario deve essere una costante stringa. Non può essere un riferimento di campo né un&#39;espressione. Per ulteriori informazioni sui tipi di dati, consultare [questa pagina](../expression/data-types.md).

## Firme e tipi restituiti

`toDateTime(<string>)`

`toDateTime(<stringified time zone id>, <dateTimeOnly>)`

`toDateTime(<integer>)`

Restituisce un valore **dateTime**.

<!--`toDateTime(<year>,<month>,<dayOfMonth>,<hour>,<minute>,<second>)`

Returns a date time with default time zone UTC.

`toDateTime(<year>,<month>,<dayOfMonth>)`
`toDateTime(<stringified timeZone>,<year>,<month>,<dayOfMonth>)`
`toDateTime(<timeZone>,<year>,<month>,<dayOfMonth>)`

Return a datetime where hour, minute and second set to 0.

`toDateTime(<stringified timeZone>,<year>,<month>,<dayOfMonth>,<hour>,<minute>,<second>)`
`toDateTime(<string>)`
`toDateTime(<string>,<integer>)`
`toDateTime(<stringified timeZone>,<dateTimeOnly)`

`toDateTime(<timeZone>,<integer>)`

Return a datetime.

-->

## Esempi

`toDateTime ("2023-08-18T23:17:59.123Z")`

Restituisce 2023-08-18T23:17:59.123Z

`toDateTime(toDateTimeOnly("UTC", "2023-08-18T23:17:59.123"))`

Restituisce 2023-08-18T23:17:59.123Z

`toDateTime(1560762190189)`

Restituisce 2023-06-17T09:03:10.189Z

<!--`toDateTime ("2016-08-18T23:17:59.123", "UTC")`

Returns 2016-08-18T23:17:59.123Z.

`toDateTime("Z",2016,8,18,23,17,59)`

Returns 2016-08-18T23:17:59.000Z.

`toDateTime("Z",2016,8,18)`

Returns 2016-08-18T00:00:00.000Z.-->
