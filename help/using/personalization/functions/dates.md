---
title: Libreria di funzioni Data e ora
description: Libreria di funzioni Data e ora
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: edc040de-dfb3-4ebc-91b4-239e10c2260b
source-git-commit: 98202be781bec0b03a9a9f33e93f1b01b7830a37
workflow-type: tm+mt
source-wordcount: '1034'
ht-degree: 6%

---

# Funzioni data/ora{#date-time}

Le funzioni di data e ora vengono utilizzate per eseguire operazioni di data e ora sui valori all&#39;interno di Journey Optimizer.

## Aggiungi giorni {#add-days}

La funzione `addDays` regola una data specificata di un numero specificato di giorni, utilizzando valori positivi per l&#39;incremento e valori negativi per la riduzione.

**Sintassi**

```sql
{%= addDays(date, number) %}
```

+++Esempio

* Input: `{%= addDays(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* Output: `2024-11-11T17:19:51Z`

+++

## Aggiungi ore {#add-hours}

La funzione `addHours` regola una data specificata di un numero specificato di ore, utilizzando valori positivi per l&#39;incremento e valori negativi per la riduzione.

**Sintassi**

```sql
{%= addHours(date, number) %}
```

+++Esempio

* Input: `{%= addHours(stringToDate("2024-11-01T17:19:51Z"),1) %}`
* Output: `2024-11-01T18:19:51Z`

+++

## Aggiungi minuti {#add-minutes}

La funzione `addMinutes` regola una data specificata di un numero specificato di minuti, utilizzando valori positivi per l&#39;incremento e valori negativi per la riduzione.

**Sintassi**

```sql
{%= addMinutes(date, number) %}
```

+++Esempio

* Input: `{%= addMinutes(stringToDate("2024-11-01T17:59:51Z"),10) %}`
* Output: `2024-11-01T18:09:51Z`

+++

## Aggiungi mesi {#add-months}

La funzione `addMonths` regola una data specificata di un numero specificato di mesi, utilizzando valori positivi per l&#39;incremento e valori negativi per la riduzione.

**Sintassi**

```sql
{%= addMonths(date, number) %}
```

+++Esempio

* Input: `{%= addMonths(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* Output: `2025-01-01T17:19:51Z`

+++

## Aggiungi secondi {#add-seconds}

La funzione `addSeconds` regola una data specificata di un numero specificato di secondi, utilizzando valori positivi per l&#39;incremento e valori negativi per la riduzione.

**Sintassi**

```sql
{%= addSeconds(date, number) %}
```

+++Esempio

* Input: `{%= addSeconds(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* Output: `2024-11-01T17:20:01Z`

+++

## Aggiungi anni {#add-years}

La funzione `addYears` regola una data specificata di un numero specificato di anni, utilizzando valori positivi per l&#39;incremento e valori negativi per la riduzione.

**Sintassi**

```sql
{%= addYears(date, number) %}
```

+++Esempio

* Input: `{%= addYears(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* Output: `2026-11-01T17:19:51Z`

+++

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

## Età in giorni {#age-days}

La funzione `ageInDays` calcola l&#39;età di una data specificata in giorni, ovvero il numero di giorni trascorsi tra la data specificata e la data corrente, negativo per le date future e positivo per le date passate.

**Sintassi**

```sql
{%= ageInDays(date) %}
```

+++Esempio

currentDate = 2025-01-07T12:17:10.720122+05:30 (Asia/Calcutta)

* Input: `{%= ageInDays(stringToDate("2025-01-01T17:19:51Z"))%}`
* Output: `5`

+++

## Età in mesi {#age-months}

La funzione `ageInMonths` calcola l&#39;età di una data specificata in mesi, ovvero il numero di mesi trascorsi tra la data specificata e la data corrente, negativo per le date future e positivo per le date passate.

**Sintassi**

```sql
{%= ageInMonths(date) %}
```

+++Esempio

currentDate = 2025-01-07T12:22:46.993748+05:30(Asia/Calcutta)

* Input: `{%=ageInMonths(stringToDate("2024-01-01T00:00:00Z"))%}`
* Output: `12`

+++

## Confronta date {#compare-dates}

La funzione `compareDates` confronta la prima data di input con l&#39;altra. Restituisce 0 se data1 è uguale a data2, -1 se data1 precede data2 e 1 se data1 segue data2.

**Sintassi**

```sql
{%= compareDates(date1, date2) %}
```

+++Esempio

* Input: `{%=compareDates(stringToDate("2024-12-02T00:00:00Z"), stringToDate("2024-12-03T00:00:00Z"))%}`
* Output: `-1`

+++

## Converti DataOraZona {#convert-zoned-date-time}

La funzione `convertZonedDateTime` converte una data/ora in un determinato fuso orario.

**Sintassi**

```sql
{%= convertZonedDateTime(dateTime, timezone) %}
```

+++Esempio

* Input: `{%=convertZonedDateTime(stringToDate("2019-02-19T08:09:00Z"), "Asia/Tehran")%}`
* Output: `2019-02-19T11:39+03:30[Asia/Tehran]`

+++

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

## Giorno del mese {#day-month}

`dayOfMonth` restituisce il numero che rappresenta il giorno del mese.

**Sintassi**

```sql
{%= dayOfMonth(datetime) %}
```

+++Esempio

* Input: `{%= dayOfMonth(stringToDate("2024-11-05T17:19:51Z")) %}`
* Output: `5`

+++


## Giorno della settimana {#day-week}

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

## Differenza In Secondi {#diff-seconds}

La funzione `diffInSeconds` restituisce la differenza tra due date in secondi.

**Sintassi**

```sql
{%= diffInSeconds(endDate, startDate) %}
```

+++Esempio

* Input: `{%=diffInSeconds(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T17:19:01Z"))%}`
* Output: `50`

+++

## Estrai ore {#extract-hours}

La funzione `extractHours` estrae il componente Ora da un determinato timestamp.

**Sintassi**

```sql
{%= extractHours(date) %}
```

+++Esempio

* Input: `{%= extractHours(stringToDate("2024-11-01T17:19:51Z"))%}`
* Output: `17`

+++

## Estrai minuti {#extract-minutes}

La funzione `extractMinutes` estrae il componente del minuto da un determinato timestamp.

**Sintassi**

```sql
{%= extractMinutes(date) %}
```

+++Esempio

* Input: `{%= extractMinutes(stringToDate("2024-11-01T17:19:51Z"))%}`
* Output: `19`

+++

## Estrai mesi {#extract-months}

La funzione `extractMonth` estrae il componente mese da un determinato timestamp.

**Sintassi**

```sql
{%= extractMonths(date) %}
```

+++Esempio

* Input: `{%=extractMonth(stringToDate("2024-11-01T17:19:51Z"))%}`
* Output: `11`

+++

## Estrai secondi {#extract-seconds}

La funzione `extractSeconds` estrae il secondo componente da un determinato timestamp.

**Sintassi**

```sql
{%= extractSeconds(date) %}
```

+++Esempio

* Input: `{%=extractSeconds(stringToDate("2024-11-01T17:19:51Z"))%}`
* Output: `51`

+++

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
> Puoi utilizzare le funzioni di formattazione della data Java come riepilogato nella [documentazione di Oracle](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html).
>
> Puoi utilizzare la formattazione e le impostazioni internazionali valide come riepilogato in [Documentazione di Oracle](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) e [Impostazioni internazionali supportate](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html).

**Esempio**

L&#39;operazione seguente restituisce la data nel formato seguente: MM/gg/AA e impostazioni internazionali FRANCE.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY", "fr_FR") %}
```

## Ottieni CurrentZonedDateTime {#get-current-zoned-date-time}

La funzione `getCurrentZonedDateTime` restituisce la data e l&#39;ora correnti con le informazioni sul fuso orario.

**Sintassi**

```sql
{%= getCurrentZonedDateTime() %}
```

+++Esempio

* Input: `{%= getCurrentZonedDateTime() %}`
* Output: `2024-12-06T17:22:02.281067+05:30[Asia/Kolkata]`

+++

## Differenza ore {#hours-difference}

La funzione `diffInHours` restituisce la differenza tra due date in termini di ore.

**Sintassi**

```sql
{%= diffInHours(endDate, startDate) %}
```

+++Esempio

* Input: `{%= diffInHours(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T07:19:51Z"))%}`
* Output: `10`

+++

## Differenza minuti{#diff-minutes}

La funzione `diffInMinutes` viene utilizzata per restituire la differenza tra due date in termini di minuti.

**Sintassi**

```sql
{%= diffInMinutes(endDate, startDate) %}
```

+++Esempio

* Input: `{%= diffInMinutes(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T16:19:51Z"))%}`
* Output: `60`

+++

## Differenza mesi {#months-difference}

La funzione `diffInMonths` restituisce la differenza tra due date in termini di mesi.

**Sintassi**

```sql
{%= diffInMonths(endDate, startDate) %}
```

+++Esempio

* Input: `{%=diffInMonths(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-08-01T17:19:51Z"))%}`
* Output: `3`

+++

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

## A Data/Ora {#to-date-time}

La funzione `ToDateTime` converte la stringa in data. In caso di input non valido, restituisce la data epoca come output.

**Sintassi**

```sql
{%= toDateTime(string, string) %}
```

+++Esempio

* Input: `{%=toDateTime("2024-11-01T17:19:51Z")%}`
* Output: `2024-11-01T17:19:51Z`

+++

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

## Tronca all&#39;inizio del giorno {#truncate-day}

La funzione `truncateToStartOfDay` viene utilizzata per modificare una data/ora specificata impostandola sull&#39;inizio del giorno con l&#39;ora impostata su 00:00.

**Sintassi**

```sql
{%= truncateToStartOfDay(date) %}
```

+++Esempio

* Input: `{%= truncateToStartOfDay(stringToDate("2024-11-01T17:19:51Z")) %}`
* Output: `2024-11-01T00:00Z`

+++

## truncateToStartOfQuarter {#truncate-quarter}

La funzione `truncateToStartOfQuarter` viene utilizzata per troncare una data/ora al primo giorno del trimestre (ad esempio 1 gennaio, 1 aprile, 1 luglio, 1 ottobre) alle 00:00.

**Sintassi**

```sql
{%= truncateToStartOfQuarter(dateTime) %}
```

+++Esempio

* Input: `{%=truncateToStartOfQuarter(stringToDate("2024-11-01T17:19:51Z"))%}`
* Output: `2024-10-01T00:00Z`

+++

## truncateToStartOfWeek {#truncate-week}

La funzione `truncateToStartOfWeek` modifica una data/ora specificata impostandola all&#39;inizio della settimana (lunedì alle 00:00).

**Sintassi**

```sql
{%= truncateToStartOfWeek(dateTime) %}
```

+++Esempio

* Input: `{%= truncateToStartOfWeek(stringToDate("2024-11-19T17:19:51Z"))%} // tuesday`
* Output: `2024-11-18T00:00Z // monday`

+++

## truncateToStartOfYear {#truncate-year}

La funzione `truncateToStartOfYear` viene utilizzata per modificare una data/ora specificata troncandola al primo giorno dell&#39;anno (1 gennaio) alle 00:00.

**Sintassi**

```sql
{%= truncateToStartOfYear(dateTime) %}
```

+++Esempio

* Input: `{%=truncateToStartOfYear(stringToDate("2024-11-01T17:19:51Z"))%}`
* Output: `2024-01-01T00:00Z`

+++

## Settimana dell’anno {#week-of-year}

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

## Differenza anni {#diff-years}

La funzione `diffInYears` viene utilizzata per restituire la differenza tra due date in termini di anni.

**Sintassi**

```sql
{%= diffInYears(endDate, startDate) %}: int
```

+++Esempio

* Input: `{%=diffInYears(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2019-10-01T17:19:51Z"))%}`
* Output: `5`

+++
