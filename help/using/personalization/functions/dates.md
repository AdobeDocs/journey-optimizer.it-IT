---
title: Libreria di funzioni Data e ora
description: Libreria di funzioni Data e ora
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: edc040de-dfb3-4ebc-91b4-239e10c2260b
TQID: https://experienceleague.adobe.com/J-aZtYitBu8T4oSwTwKNNDeA-7tA4l8Wi5YZ1WLcT3E
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2: []
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 1762
ht-degree: 5%

---

# Funzioni data/ora{#date-time}

Le funzioni di data e ora vengono utilizzate per eseguire operazioni di data e ora sui valori all&#39;interno di Journey Optimizer.

>[!NOTE]
>
>Funzione `now()` non disponibile nell&#39;editor di personalizzazione. Utilizzare `getCurrentZonedDateTime()` o `currentTimeInMillis()` per i valori di data/ora correnti. [Ulteriori informazioni](../../email/code-content.md#date-time-limitations)

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

+++Esempio — Giorni rimanenti fino a un evento

La seguente operazione restituisce il numero di giorni tra la data odierna e una data futura memorizzata nel profilo (ad esempio, una data di fine abbonamento o una data evento):

```sql
{%= dateDiff(getCurrentZonedDateTime(), stringToDate(profile.events.subscriptionEndDate)) %}
```

+++

+++Esempio reale — Conto alla rovescia nella riga dell’oggetto

Utilizza `dateDiff` per creare un conto alla rovescia dinamico per le righe dell&#39;oggetto o il contenuto dell&#39;e-mail:

```handlebars
{% let daysLeft = dateDiff(getCurrentZonedDateTime(), stringToDate(profile.loyalty.expiryDate)) %}
{%#if daysLeft > 0%}
Your points expire in {{daysLeft}} day{%#if daysLeft > 1%}s{%/if%} — use them before they're gone!
{%else%}
Your points have expired.
{%/if%}
```

Output (esempio): `Your points expire in 7 days — use them before they're gone!`

+++

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

La funzione `dayOfWeek` viene utilizzata per recuperare il giorno della settimana. Restituisce un numero intero compreso tra 1 (lunedì) e 7 (domenica) in base allo standard ISO-8601.

**Sintassi**

```sql
{%= dayOfWeek(datetime) %}
```

+++Esempio — Rileva i fine settimana nel contenuto personalizzato

Utilizza questa funzione all’interno di e-mail o contenuti per adattare la messaggistica in base alla giornata. L&#39;operatore di confronto in PQL è `=` (singolo è uguale a, non `==`):

```handlebars
{%#if dayOfWeek(getCurrentZonedDateTime()) = 6 or dayOfWeek(getCurrentZonedDateTime()) = 7%}
We're closed on weekends — your request will be processed on the next business day.
{%else%}
Our team will get back to you within 24 hours.
{%/if%}
```

| Day | Valore restituito |
|-----|----------------|
| Lunedì | 1 |
| Martedì | 2 |
| Mercoledì | 3 |
| Giovedì | 4 |
| Venerdì | 5 |
| Sabato | 6 |
| Domenica | 7 |

+++

>[!NOTE]
>
>`dayOfWeek()` è progettato per la **personalizzazione del contenuto** (ad esempio, adattando il testo del corpo dell&#39;e-mail in base al giorno). Se devi **instradare i profili in modo diverso in un percorso** in base al giorno della settimana (ad esempio saltare i fine settimana per un&#39;attività Attendi), utilizza l&#39;opzione integrata **Condizione temporale → Giorno della settimana** disponibile direttamente nell&#39;attività Condizione percorso. [Ulteriori informazioni](../../building-journeys/condition-activity.md#date_condition)

## Giorno dell’anno{#day-year}

La funzione `dayOfYear` viene utilizzata per recuperare il giorno dell&#39;anno.

**Sintassi**

```sql
{%= dayOfYear(datetime) %}
```

+++Esempio

* Input: `{%= dayOfYear(stringToDate("2024-03-15T00:00:00Z")) %}`
* Output: `75`

+++

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

+++Esempio reale - Visualizza solo ora corrente come HH:MM

Combina `extractHours` e `extractMinutes` per eseguire il rendering solo della porzione di tempo senza data, giorno o anno:

```handlebars
{% let h = extractHours(getCurrentZonedDateTime()) %}
{% let m = extractMinutes(getCurrentZonedDateTime()) %}
Your appointment is confirmed for {{h}}:{%#if m < 10%}0{%/if%}{{m}}.
```

Output (esempio): `Your appointment is confirmed for 14:05.`

La protezione con zero iniziale (`{%#if m < 10%}0{%/if%}`) garantisce che i minuti al di sotto di 10 vengano visualizzati come due cifre (ad esempio `09` invece di `9`).

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

Dove il primo parametro è l’attributo data-ora e il secondo valore è il modo in cui desideri che la data venga convertita e visualizzata.

>[!NOTE]
>
> La funzione `formatDate` richiede come input un tipo di campo data-ora **&#x200B;**, non una stringa. Se il campo è memorizzato come tipo di stringa nello schema XDM, devi prima convertirlo in data e ora utilizzando una funzione di conversione come `stringToDate()` o `toDateTime()`. Vedi gli esempi di seguito.
>
> Se un modello di data non è valido, la data tornerà al formato standard ISO.
>
> Puoi utilizzare le funzioni di formattazione della data Java riepilogate nella [documentazione di Oracle](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}

**Esempi**

+++Formattazione di un campo data-ora

L&#39;operazione seguente formatta un campo data-ora nel formato MM/GG/AA.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY") %}
```

+++

+++Conversione di una stringa in data

Se il campo è memorizzato come stringa, è necessario convertirlo in una data/ora utilizzando `stringToDate()` prima di formattarlo.

```sql
{%= formatDate(stringToDate(profile.person.birthDayAndMonth), "MM/DD/YY") %}
```

+++

+++Formato data completo con nome giorno

L&#39;operazione seguente restituisce un formato di data completo con il nome del giorno, il nome del mese, il giorno e l&#39;anno.

```sql
{%= formatDate(profile.person.birthDateTime, "EEEE MMMM dd yyyy") %}
```

Output: `Wednesday January 01 2020`

+++

+++Data dinamica basata sull’ora del sistema

È possibile formattare l&#39;ora di sistema corrente per generare date dinamiche. L&#39;operazione seguente restituisce la data corrente in formato MM/gg/AAAA.

```sql
{%= formatDate(getCurrentZonedDateTime(), "MM/dd/YYYY") %}
```

Output (del 30 gennaio 2026): `01/30/2026`

+++

+++Formato del giorno della settimana

È possibile estrarre il giorno della settimana in formato breve.

```sql
{%= formatDate(getCurrentZonedDateTime(), "EEE") %}
```

Output: `Sun` (per domenica), `Mon` (per lunedì), `Tue` (per martedì), ecc.

Per l&#39;output in minuscolo, combinare con la funzione `lowerCase`:

```sql
{%= lowerCase(formatDate(getCurrentZonedDateTime(), "EEE")) %}
```

Output: `sun`, `mon`, `tue`, ecc.

+++

+++Formattazione di una marca temporale da un evento contestuale

Quando si utilizza una marca temporale da un attributo di contesto di evento di percorso, si applicano due requisiti:

* **Racchiudi il timestamp con`toDateTime()`**. I timestamp dell&#39;evento di contesto non vengono riconosciuti automaticamente come valori data-ora da `formatDate()`.
* **Racchiudi gli ID evento numerici nei backtick**. Se l&#39;ID evento è un numero (ad esempio, `1697323153`), deve essere preceduta da un carattere di escape con backtick nel percorso dell&#39;espressione. In caso contrario, l&#39;editor genera un errore di sintassi PQL.
* **Utilizzare la sintassi `{% let %}` o `{%= %}`**. È possibile assegnare il risultato a una variabile con `{% let %}` ed eseguirne il rendering con `{{varName}}` oppure utilizzare direttamente la sintassi `{%= %}` in linea.

```handlebars
{% let appointmentDate = formatDate(toDateTime(context.journey.events.`1697323153`.timestamp), "dd/MM/yyyy HH:mm") %}
{{appointmentDate}}
```

Output (esempio): `18/03/2026 14:30`

+++

>[!CAUTION]
>
>**Errore comune: &quot;input non corrispondente &#39;(&#39; previsto \&lt;EOF\>&quot;**
>
>Questo errore di sintassi PQL si verifica quando si utilizza `formatDate()` con un timestamp evento di contesto in linea (`{%= formatDate(...) %}`). Le cause più comuni sono un ID evento numerico non racchiuso tra apici retroversi (`` ` ``) o un campo marca temporale passato direttamente a `formatDate()` senza prima racchiuderlo in `toDateTime()`. Per risolvere entrambi i problemi, utilizzare il modello di assegnazione `{% let %}` illustrato nell&#39;esempio precedente.

### Caratteri pattern {#pattern-characters}

Alcune lettere di serie possono avere un aspetto simile ma rappresentare concetti diversi.

| Pattern | Significato | Esempio (per `2023-12-31T10:15:30Z`) |
|---------|---------|--------------------------------------|
| `y` | Anno solare (anno standard) | `2023` |
| `Y` | Anno basato sulla settimana (ISO 8601). Può variare in base ai limiti dell&#39;anno. | `2024` (dal 31 dicembre 2023 cade nella prima settimana del 2024) |
| `M` | Mese dell&#39;anno (1-12 o testo simile a `Jan`, `January`) | `12` o `Dec` |
| `m` | Minuto dell&#39;ora (0-59) | `15` |
| `d` | Giorno del mese (1-31) | `31` |
| `D` | Giorno dell’anno (1-366) | `365` |

### Formattare la data con il supporto delle impostazioni internazionali{#format-date-locale}

La funzione `formatDate` può essere utilizzata per formattare un valore di data e ora nella corrispondente rappresentazione sensibile alla lingua, ovvero in una lingua desiderata. Il formato deve essere un pattern Java DateTimeFormat valido.

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

+++Esempio

Impostare il giorno del mese al 1° giorno:

* Input: `{%= setDays(stringToDate("2024-11-15T17:19:51Z"), 1) %}`
* Output: `2024-11-01T17:19:51Z`

+++

## Imposta ore{#set-hours}

La funzione `setHours` viene utilizzata per impostare l&#39;ora della data/ora.

**Sintassi**

```sql
{%= setHours(datetime, hour) %}
```

+++Esempio — Impostare una data/ora su un&#39;ora specifica

* Input: `{%= setHours(stringToDate("2024-11-01T17:19:51Z"), 0) %}`
* Output: `2024-11-01T00:19:51Z`

+++

+++Esempio reale: X giorni prima di una data di fine dinamica

Per eseguire il targeting di un profilo X giorni prima di una data memorizzata nel profilo (ad esempio, scadenza abbonamento), utilizzare `addDays` con un valore negativo:

```sql
{%= addDays(stringToDate(profile.subscription.endDate), -7) %}
```

Per normalizzare anche l&#39;ora a un&#39;ora fissa (ad esempio le 9), combinare con `setHours`:

```sql
{%= setHours(addDays(stringToDate(profile.subscription.endDate), -7), 9) %}
```

+++

## A data/ora {#to-date-time}

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

+++Esempio

* Input: `{%= weekOfYear(stringToDate("2024-11-01T17:19:51Z")) %}`
* Output: `44`

+++

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
