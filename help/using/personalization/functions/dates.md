---
title: Libreria di funzioni Data e ora
description: Libreria di funzioni Data e ora
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: edc040de-dfb3-4ebc-91b4-239e10c2260b
source-git-commit: 3a4a58f8601c67e8e9a2b606a47c6b4bcc2dab05
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 7%

---

# Funzioni data/ora{#date-time}

Le funzioni di data e ora vengono utilizzate per eseguire operazioni di data e ora sui valori all&#39;interno di Journey Optimizer.

## Età{#age}

La funzione `age` viene utilizzata per recuperare l&#39;età da una data specificata.

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

## Ora corrente in millisecondi{#current-time}

La funzione `currentTimeInMillis` viene utilizzata per recuperare il tempo corrente in millisecondi epoca.

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

## Differenza data{#date-diff}

La funzione `dateDiff` viene utilizzata per recuperare la differenza tra due date in un numero di giorni.

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

La funzione `dayOfWeek` viene utilizzata per recuperare il giorno della settimana.

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

La funzione `dayOfYear` viene utilizzata per recuperare il giorno dell&#39;anno.

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

## Formato data{#format-date}

La funzione `formatDate` viene utilizzata per formattare un valore di data e ora. Il formato deve essere un pattern Java DateTimeFormat valido.

**Sintassi**

```sql
{%= formatDate(datetime, format) %}
```

Dove la prima stringa è l’attributo data e il secondo valore è il modo in cui desideri che la data venga convertita e visualizzata.

>[!NOTE]
>
> Se un modello di data non è valido, la data tornerà al formato standard ISO.
>
> Puoi utilizzare le funzioni di formattazione della data Java riepilogate nella [documentazione di Oracle](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}

**Esempio**

L&#39;operazione seguente restituisce la data nel formato seguente: MM/GG/AA.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY") %}
```

## Formattare la data con il supporto delle impostazioni internazionali{#format-date-locale}

La funzione `formatDate` viene utilizzata per formattare un valore di data e ora nella corrispondente rappresentazione sensibile alla lingua, ovvero in una lingua desiderata. Il formato deve essere un pattern Java DateTimeFormat valido.

**Sintassi**

```sql
{%= formatDate(datetime, format, locale) %}
```

Dove la prima stringa è l’attributo data, il secondo valore corrisponde al modo in cui la data deve essere convertita e visualizzata e il terzo valore rappresenta la lingua in formato stringa.

>[!NOTE]
>
> Se un modello di data non è valido, la data tornerà al formato standard ISO.
>
> È possibile utilizzare le funzioni di formattazione della data Java come riepilogato in [documentazione di Oracle](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html).
>
> Puoi utilizzare la formattazione e le impostazioni internazionali valide come riepilogato in [documentazione di Oracle](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) e [Impostazioni internazionali supportate](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html).


**Esempio**

L&#39;operazione seguente restituisce la data nel formato seguente: MM/GG/AA e impostazioni internazionali FRANCE.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/DD/YY", "fr_FR") %}
```

## Imposta giorni{#set-days}

La funzione `setDays` viene utilizzata per impostare il giorno del mese per la data/ora specificata.

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

La funzione `setHours` viene utilizzata per impostare l&#39;ora della data/ora.

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

La funzione `toUTC` viene utilizzata per convertire un datetime in UTC.


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

La funzione `weekOfYear` viene utilizzata per recuperare la settimana dell&#39;anno.

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