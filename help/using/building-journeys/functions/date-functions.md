---
product: journey optimizer
title: Funzioni data
description: Scopri le funzioni data
feature: Journeys
role: Developer
level: Experienced
keywords: data, funzioni, espressione, percorso, ora
version: Journey Orchestration
source-git-commit: 42abfcc9711d87b2dc00df47e964dad07443f0ed
workflow-type: tm+mt
source-wordcount: '783'
ht-degree: 12%

---

# Funzioni data {#date-functions}

Le funzioni di data consentono di manipolare e utilizzare i valori di data e ora all&#39;interno delle espressioni di percorso. Queste funzioni sono essenziali per le condizioni basate sul tempo, la pianificazione e i calcoli temporali nei percorsi dei clienti.

Utilizza le funzioni data quando devi:

* Ottieni l’ora o la data corrente con una gestione specifica del fuso orario
* Verifica se una data rientra in un intervallo di tempo specifico (passato o futuro)
* Modifica dei componenti data e ora (ore, giorni, fusi orari)
* Eseguire calcoli e confronti basati sul tempo
* Conversione tra diversi formati e rappresentazioni temporali

Le funzioni di data forniscono un controllo preciso sulla logica temporale, consentendo di creare percorsi e condizioni di percorso sensibili al tempo che rispondono a specifici intervalli di tempo e pianificazioni.

## currentTimeInMillis {#currentTimeInMillis}

Restituisce il tempo corrente in millisecondi epoca.

+++Sintassi

`currentTimeInMillis()`

+++

+++Parametri

Questa funzione non utilizza parametri.

+++

+++Firme e tipo restituito

`currentTimeInMillis()`

Restituisce un numero intero.

+++

+++Esempi

`currentTimeInMillis()`

Restituisce &quot;1544712617131&quot;

+++

## inLastDays {#inLastDays}

Restituisce true se un dato dateTime è compreso tra now e now - delta days.

+++Sintassi

`inLastDays(<dateTime>,<delta>)`

+++

+++Parametri

| Parametro | Tipo |
|-----------|------------------|
| data e ora | dateTime |
| delta | intero |

+++

+++Firme e tipo restituito

`inLastDays(<dateTime>,<integer>)`

Restituisce un valore booleano.

+++

+++Esempi

`inLastDays(toDateTime('2023-12-12T01:11:00Z'), 4)`

Restituisce true.

+++

## inLastHours {#inLastHours}

Restituisce true se la data e l’ora specificate sono comprese tra now e now - delta hours.

+++Sintassi

`inLastHours(<dateTime>,<delta>)`

+++

+++Parametri

| Parametro | Tipo |
|-----------|------------------|
| data e ora | dateTime |
| delta | intero |

+++

+++Firme e tipo restituito

`inLastHours(<dateTime>,<integer>)`

Restituisce un valore booleano.

+++

+++Esempi

`inLastHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

Restituisce true.

`inLastHours(@event{MyEvent.timestamp}, 4)`

Restituisce true.

+++

## inLastMonths {#inLastMonths}

Restituisce true se una data o un&#39;ora specificata è compresa tra now e now - delta mesi.

+++Sintassi

`inLastMonths(<dateTime>,<delta>)`

+++

+++Parametri

| Parametro | Tipo |
|-----------|------------------|
| data e ora | dateTime |
| delta | intero |

+++

+++Firme e tipo restituito

`inLastMonths(<dateTime>,<integer>)`

Restituisce un valore booleano.

+++

+++Esempi

`inLastMonths(toDateTime('2023-12-12T01:11:00Z'), 4)`

Restituisce true.

+++

## inLastYears {#inLastYears}

Restituisce true se una data o un valore dateTime specificato è compreso tra now e now - delta years.

+++Sintassi

`inLastYears(<dateTime>,<delta>)`

+++

+++Parametri

| Parametro | Tipo |
|-----------|------------------|
| data e ora | dateTime |
| delta | intero |

+++

+++Firme e tipo restituito

`inLastYears(<dateTime>,<integer>)`

Restituisce un valore booleano.

+++

+++Esempi

`inLastYears(toDateTime('2023-12-12T01:11:00Z'), 4)`

Restituisce true.

+++

## inNextDays {#inNextDays}

Restituisce true se una data o un&#39;ora specificata è compresa tra now e now + delta giorni.

+++Sintassi

`inNextDays(<dateTime>,<delta>)`

+++

+++Parametri

| Parametro | Tipo |
|-----------|------------------|
| data e ora | dateTime |
| delta | intero |

+++

+++Firme e tipo restituito

`inNextDays(<dateTime>,<integer>)`

Restituisce un valore booleano.

+++

+++Esempi

`inNextDays(toDateTime('2023-12-12T01:11:00Z'), 4)`

Restituisce true.

+++

## inNextHours {#inNextHours}

Restituisce true se una data o un&#39;ora specificata è compresa tra now e now + delta ore.

+++Sintassi

`inNextHours(<dateTime>,<delta>)`

+++

+++Parametri

| Parametro | Tipo |
|-----------|------------------|
| data e ora | dateTime |
| delta | intero |

+++

+++Firme e tipo restituito

`inNextHours(<dateTime>,<integer>)`

Restituisce un valore booleano.

+++

+++Esempi

`inNextHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

Restituisce true.

+++

## inNextMonths {#inNextMonths}

Restituisce true se una data o un&#39;ora specificata è compresa tra now e now + delta mesi.

+++Sintassi

`inNextMonths(<dateTime>,<delta>)`

+++

+++Parametri

| Parametro | Tipo |
|-----------|------------------|
| data e ora | dateTime |
| delta | intero |

+++

+++Firme e tipo restituito

`inNextMonths(<dateTime>,<integer>)`

Restituisce un valore booleano.

+++

+++Esempi

`inNextMonths(toDateTime('2023-01-12T01:11:00Z'), 4)`

Restituisce true.

+++

## inNextYears {#inNextYears}

Restituisce true se una data o un&#39;ora specificata è compresa tra now e now + delta anni.

+++Sintassi

`inNextYears(<dateTime>,<delta>)`

+++

+++Parametri

| Parametro | Tipo |
|-----------|------------------|
| data e ora | dateTime |
| delta | intero |

+++

+++Firme e tipo restituito

`inNextYears(<dateTime>,<integer>)`

Restituisce un valore booleano.

+++

+++Esempi

`inNextYears(toDateTime('2021-12-12T01:11:00Z'), 4)`

Restituisce true.

+++

## now {#now}

Restituisce la data corrente in formato data e ora. Per ulteriori informazioni sui tipi di dati, consultare [questa pagina](../expression/data-types.md).

+++Sintassi

`now(<parameter>)`

+++

+++Parametri

| Parametro | Descrizione |
|--- |--- |
| stringa | Identificatore del fuso orario (facoltativo) |

+++

+++Firme e tipo restituito

`now()`

`now("<timeZone id>")`

Restituisce un valore dateTime.

+++

+++Esempi

`now()`

Restituisce 2023-06-03T06:30Z.

`toString(now())`

Restituisce &quot;2023-06-03T06:30Z&quot;

`now("Europe/Paris")`

Restituisce 2023-06-03T08:30+02:00.

+++

## nowWithDelta {#nowWithDelta}

Restituisce il valore datetime corrente comprensivo di un offset. Se viene specificato un ID di fuso orario, verrà applicato lo scostamento del fuso orario. Per ulteriori informazioni sui tipi di dati, consultare [questa pagina](../expression/data-types.md).

+++Sintassi

`nowWithDelta(<parameters>)`

+++

+++Parametri

| Parametro | Descrizione |
|--- |--- |
| delta | valore intero positivo o negativo |
| parte data | anni, mesi, giorni, ore, minuti o secondi come stringa |
| id fuso orario | rappresentazione stringa del valore del fuso orario. Per ulteriori informazioni, vedere [Tipi di dati](../expression/data-types.md). L’ID del fuso orario deve essere una costante stringa. Non può essere un riferimento di campo né un&#39;espressione. |

+++

+++Firme e tipo restituito

`nowWithDelta(<delta>,<date part>`

`nowWithDelta(<delta>,<date part>,"<timeZone id>")`

Restituisce un valore dateTime.

+++

+++Esempi

`nowWithDelta(-2, "hours")`

`nowWithDelta(-2, "hours", "Europe/Paris")`

Restituisce un valore dateTime esattamente 2 ore fa.

+++

## setHours {#setHours}

Imposta solo le ore di una data/ora o data/ora. Ad esempio, se desideri aspettare fino a un’ora specifica domani, puoi forzare l’ora.

+++Sintassi

`setHours(<parameter>)`

+++

+++Parametri

| Parametro | Tipo |
|--- |--- |
| data e ora | dateTime |
| data e ora senza considerare il fuso orario | dateTimeOnly |
| ore | intero |

+++

+++Firme e tipo restituito

`setHours(<dateTime>,<hours>)`

Restituisce un valore datetime.

`setHours(<dateTimeOnly>,<hours>)`

Restituisce un valore datetime senza considerare il fuso orario.

+++

+++Esempi

`setHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

Restituisce 2023-12-12T04:11:00Z.

`setHours(nowWithDelta(1, "days"), 20)`

Restituisce domani alle 20.00, dove XY corrisponde ai minuti al momento della valutazione dell&#39;ora corrente. :XY Se la valutazione viene eseguita alle 02:00, l&#39;ora restituita sarà le 20:00.:45:45

+++

## setDays {#setDays}

Imposta solo il giorno di un&#39;ora o di una data. Ad esempio, se desideri attendere fino a un determinato giorno del mese, puoi forzare il giorno.

+++Sintassi

`setDays(<parameter>)`

+++

+++Parametri

| Parametro | Tipo |
|--- |--- |
| data e ora | dateTime |
| data e ora senza considerare il fuso orario | dateTimeOnly |
| giorni | intero |

+++

+++Firme e tipo restituito

`setDays(<dateTime>,<days>)`

Restituisce un valore datetime.

`setDays(<dateTimeOnly>,<days>)`

Restituisce un valore datetime senza considerare il fuso orario.

+++

+++Esempi

`setDays(toDateTime('2023-12-12T01:11:00Z'), 25)`

Restituisce 2023-12-25T01:11:00Z.

`setDays(toDateTimeOnly(@event{MyEvent.registrationDate}), 1)`

+++

## updateTimeZone {#updateTimeZone}

Restituisce una nuova data e ora, con un nuovo fuso orario nello stesso istante.

+++Sintassi

`updateTimeZone(<parameters>)`

+++

+++Parametri

* id fuso orario: stringa
* dateTime

+++

+++Firma e tipo restituito

`updateTimeZone(<dateTime>,<timeZone id>)`

Restituisce un valore datetime.

+++

+++Esempi

`updateTimeZone( toDateTime("2023-08-28T08:15:30.123-07:00"), "Europe/Paris"))`

Restituisce 2023-08-28T17:15:30.123+02:00.

`updateTimeZone(@event{MyExpEvent.timestamp}, "Australia/Sydney")`

Se il valore del campo timestamp è `2021-11-16T16:55:12.939318+01:00`, la funzione restituisce `2021-11-17T02:55:12.942115+11:00`.

+++

