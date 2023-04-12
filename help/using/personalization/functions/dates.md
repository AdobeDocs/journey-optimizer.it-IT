---
title: Libreria funzioni Data Time
description: Libreria funzioni Data Time
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: edc040de-dfb3-4ebc-91b4-239e10c2260b
source-git-commit: 2444d8fbe3a86feb0497d754b4f57f234fa29e49
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 4%

---

# Funzioni di data e ora{#date-time}

Le funzioni di data e ora vengono utilizzate per eseguire operazioni di data e ora sui valori all’interno di Journey Optimizer.

## Età{#age}

La `age` viene utilizzata per recuperare l’età da una data specificata.

**Sintassi**

```sql
 {%= age(datetime) %}
```

<!--
**Example**

The following operation gets the value of the identity map for the key `example@example.com`.

```sql
 {%= age(datetime) %}
```
-->

## Tempo corrente in millisecondi{#current-time}

La `currentTimeInMillis` viene utilizzata per recuperare il tempo corrente in millisecondi epoch.

**Sintassi**

```sql
{%= currentTimeInMillis() %}
```

<!--
**Example**

The following operation gets all the keys for the map `identityMap`.

```sql
{%= keys(identityMap) %}
```
-->

## Differenza tra date{#date-diff}

La `dateDiff` viene utilizzata per recuperare la differenza tra due date in numero di giorni.

**Sintassi**

```sql
{%= dateDiff(datetime,datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->


## Giorno della settimana{#day-week}

La `dayOfWeek` viene utilizzata per recuperare il giorno della settimana.

**Sintassi**

```sql
{%= dayOfWeek(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## Giorno dell’anno{#day-year}

La `dayOfYear` viene utilizzata per recuperare il giorno dell’anno.

**Sintassi**

```sql
{%= dayOfYear(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## Data del formato{#format-date}

La `formatDate` viene utilizzata per formattare un valore di ora della data. Il formato deve essere un pattern Java DateTimeFormat valido.

**Sintassi**

```sql
{%= formatDate(datetime, format) %}
```

Se la prima stringa è l’attributo data e il secondo valore è il modo in cui si desidera convertire e visualizzare la data.

>[!NOTE]
>
> Se un pattern di data non è valido, la data si basa sul formato standard ISO.
>
> È possibile utilizzare le funzioni di formattazione della data Java come riepilogato in [Documentazione di Oracle](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}

**Esempio**

L’operazione seguente restituisce la data nel seguente formato: MM/GG/AA.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/DD/YY") %}
```

## Data del formato con supporto delle impostazioni internazionali{#format-date-locale}

La `formatDate` viene utilizzata per formattare un valore di data e ora nella corrispondente rappresentazione sensibile alla lingua, cioè in un’impostazione internazionale desiderata. Il formato deve essere un pattern Java DateTimeFormat valido.

**Sintassi**

```sql
{%= formatDate(datetime, format, locale) %}
```

Se la prima stringa è l&#39;attributo data, il secondo valore indica il modo in cui si desidera convertire e visualizzare la data e il terzo valore rappresenta le impostazioni internazionali in formato stringa.

>[!NOTE]
>
> Se un pattern di data non è valido, la data si basa sul formato standard ISO.
>
> È possibile utilizzare le funzioni di formattazione della data Java come riepilogato in [Documentazione di Oracle](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html).
>
> È possibile utilizzare la formattazione e le impostazioni internazionali valide come riepilogato in [Documentazione di Oracle](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) e [Impostazioni internazionali supportate](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html).


**Esempio**

L’operazione seguente restituisce la data nel seguente formato: MM/GG/AA e locale FRANCE.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/DD/YY", "fr_FR") %}
```

## Imposta giorni{#set-days}

La `setDays` viene utilizzata per impostare il giorno del mese per la data-ora specificata.

**Sintassi**

```sql
{%= setDays(datetime, day) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## Imposta ore{#set-hours}

La `setHours` viene utilizzata per impostare l&#39;ora della data-ora.

**Sintassi**

```sql
{%= setHours(datetime, hour) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->


## A UTC{#to-utc}

La `toUTC` viene utilizzata per convertire un datetime in UTC.


**Sintassi**

```sql
{%= toUTC(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->


## Settimana dell’anno UTC{#week-of-year}

La `weekOfYear` viene utilizzata per recuperare la settimana dell’anno.

**Sintassi**

```sql
{%= weekOfYear(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->