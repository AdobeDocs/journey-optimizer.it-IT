---
product: journey optimizer
title: Funzioni di conversione
description: Scopri le funzioni di conversione
feature: Journeys
role: Developer
level: Experienced
keywords: conversione, funzioni, espressione, percorso, tipo, cast
version: Journey Orchestration
source-git-commit: 7d75abf6b428becc8b535a63421e85cca417daac
workflow-type: tm+mt
source-wordcount: '940'
ht-degree: 6%

---

# Funzioni di conversione {#conversion-functions}

Le funzioni di conversione consentono di trasformare i dati da un tipo all’altro all’interno delle espressioni di percorso. Queste funzioni sono essenziali per garantire la compatibilità dei dati e una corretta gestione del tipo quando si lavora con origini dati e operazioni diverse.

Utilizza le funzioni di conversione quando devi:

* Convertire i valori stringa in tipi numerici, booleani o di data
* Trasformazione di data e ora tra formati e rappresentazioni diversi
* Cast valori numerici tra tipi integer e decimal
* Garantire la compatibilità dei tipi per confronti e operazioni
* Elabora dati provenienti da origini esterne che possono avere formati di tipo diversi

Ogni funzione di conversione gestisce in automatico regole e casi edge specifici del tipo, rendendo la trasformazione dei dati più affidabile e prevedibile nelle espressioni di percorso.

## toBool {#toBool}

Converte un valore di argomento in un valore booleano, a seconda del tipo.

* Da stringa: prova a convertire il valore stringa come booleano; da &quot;true&quot; se il valore stringa è &quot;true&quot;; in caso contrario false
* Dal valore numerico: true se il valore numerico non è uguale a 0, false in caso contrario

+++Sintassi

`toBool(<parameter>)`

+++

+++Parametri

* decimale
* booleano
* stringa
* intero

+++

+++Firme e tipi restituiti

`toBool(<decimal>)`

`toBool(<boolean>)`

`toBool(<string>)`

`toBool(<integer>)`

Restituisce un valore booleano.

+++

+++Esempi

`toBool("true")`

`toBool(1)`

Restituisce true.

`toBool("this is not a boolean")`

Restituisce false.

+++

## toDateOnly {#toDateOnly}

Converte un argomento in un valore di tipo dateOnly. Per ulteriori informazioni sui tipi di dati, consulta questa [sezione](../expression/data-types.md).

+++Sintassi

`toDateOnly(<parameters>)`

+++

+++Parametri

| Parametro | Tipo |
|-----------|------------------|
| Rappresentazione stringa di una data come &quot;AAAA-MM-GG&quot; (formato XDM). Supporta anche il formato ISO-8601: viene considerata solo la parte **full-date** (consultare [RFC 3339, sezione 5.6](https://www.rfc-editor.org/rfc/rfc3339#section-5.6) | stringa |
| data e ora | dateTime |
| data e ora senza fuso orario | dateTimeOnly |
| valore intero di un’epoca in millisecondi | intero |

+++

+++Firme e tipi restituiti

`toDateOnly(<dateTime>)`

`toDateOnly(<dateTimeOnly>)`

`toDateOnly(<string>)`

`toDateOnly(<integer>, <integer>, <integer>)`

Restituisce un valore di tipo dateOnly.

+++

+++Esempi

`toDateOnly("2023-08-18")`

`toDateOnly("2023-08-18T00:00:00.000Z")`

`toDateOnly("2023-08-18T00:00:00")`

tutti restituiscono un oggetto dateOnly che rappresenta il 18 agosto 2023.

`toDateOnly(#{ExperiencePlatform.ProfileFieldGroup.person.birthDate})`

Restituisce un valore dateOnly.

+++

## toDateTime {#toDateTime}

Converte i parametri in un valore di data e ora, a seconda del tipo.

+++Sintassi

`toDateTime(<parameters>)`

+++

+++Parametri

| Parametro | Tipo |
|-----------|------------------|
| data e ora nel formato ISO-8601 | stringa |
| id fuso orario | stringa |
| data e ora senza fuso orario | dateTimeOnly |
| valore intero di un’epoca in millisecondi | intero |

+++

+++Firme e tipi restituiti

`toDateTime(<string>)`

`toDateTime(<stringified time zone id>, <dateTimeOnly>)`

`toDateTime(<integer>)`

Restituisce un valore **dateTime**.

+++

+++Esempi

`toDateTime ("2023-08-18T23:17:59.123Z")`

Restituisce 2023-08-18T23:17:59.123Z

`toDateTime(toDateTimeOnly("UTC", "2023-08-18T23:17:59.123"))`

Restituisce 2023-08-18T23:17:59.123Z

`toDateTime(1560762190189)`

Restituisce 2023-06-17T09:03:10.189Z

+++

>[!NOTE]
>
>L’ID del fuso orario deve essere una costante stringa. Non può essere un riferimento di campo né un&#39;espressione. Per ulteriori informazioni sui tipi di dati, consultare [questa pagina](../expression/data-types.md).

## toDateTimeOnly {#toDateTimeOnly}

Converte un valore di argomento in un valore di sola data e ora.

+++Sintassi

`toDateTimeOnly(<parameters>)`

+++

+++Parametri

| Parametro | Tipo |
|-----------|------------------|
| data e ora in formato ISO-8601 o &quot;AAAA-MM-GG&quot; (formato data XDM) | stringa |
| data e ora | dateTime |

+++

+++Firme e tipi restituiti

`toDateTimeOnly(<dateTime>)`

`toDateTimeOnly(<string>)`

Restituisce un valore datetime senza considerare il fuso orario.

+++

+++Esempi

`toDateTimeOnly ("2023-08-18")`

restituisce un valore dateTime che rappresenta 2023-08-18T00:00:00.000

`toDateTimeOnly(now())`

+++

## toDecimal {#toDecimal}

Converte un valore di argomento in un valore decimale, a seconda del tipo.

+++Sintassi

`toDecimal(<parameter>)`

+++

+++Parametri

| Parametro | Descrizione |
|--- |--- |
| stringa | converte il valore stringa come decimale |
| dateTime | converte la data in millisecondi (millisecondi epoca) |
| booleano | converte il valore booleano come 1 se true, 0 se false |
| intero | converte in un decimale (ad esempio.: 1 diventa 1,0) |

+++

+++Firme e tipi restituiti

`toDecimal(<integer>)`

`toDecimal(<decimal>)`

`toDecimal(<string>)`

`toDecimal(<boolean>)`

Restituisce un decimale.

+++

+++Esempi

`toDecimal("4.0")`

Restituisce 4,0.

+++

## toDuration {#toDuration}

Converte un valore di argomento in una durata. Per ulteriori informazioni sui tipi di dati, consultare [questa pagina](../expression/data-types.md).

+++Sintassi

`toDuration(<parameter>)`

+++

+++Parametri

| Parametro | Descrizione |
|--- |--- |
| stringa | formati basati sul formato di durata ISO-8601 PnDTnHnMn.nS con giorni considerati esattamente 24 ore |
| intero | numero di millisecondi |

Espressione stringa: i formati accettati sono basati sul formato di durata ISO-8601 PnDTnHnMn.nS con giorni considerati esattamente 24 ore.

La stringa inizia con un segno facoltativo, indicato dal simbolo ASCII negativo o positivo. Se negativo, l&#39;intero periodo viene ignorato. La lettera ASCII &quot;P&quot; è successiva in maiuscolo o in minuscolo. Ci sono poi quattro sezioni, ciascuna composta da un numero e un suffisso. Le sezioni hanno suffissi in ASCII di &quot;D&quot;, &quot;H&quot;, &quot;M&quot; e &quot;S&quot; per giorni, ore, minuti e secondi, accettati in maiuscolo o minuscolo. I suffissi devono essere disposti in ordine. La lettera ASCII &quot;T&quot; deve precedere la prima occorrenza, se presente, di un&#39;ora, un minuto o una seconda sezione. Deve essere presente almeno una delle quattro sezioni e, se &quot;T&quot; è presente, deve esserci almeno una sezione dopo la &quot;T&quot;. La parte numerica di ogni sezione deve essere costituita da una o più cifre ASCII. Il numero può essere preceduto dal simbolo ASCII negativo o positivo. Il numero di giorni, ore e minuti deve essere analizzato in lungo. Il numero di secondi deve essere analizzato insieme alla frazione facoltativa. Il punto decimale può essere un punto o una virgola. La parte frazionaria può avere da zero a 9 cifre.

+++

+++Firme e tipo restituito

`toDuration(<string>)`

`toDuration(<integer>)`

Restituisce una durata.

+++

+++Esempi

`toDuration("PT10H")`

Restituisce una durata di 10 ore.

`toDuration("PT4S")`

Restituisce una durata di 4 secondi.

`toDuration(4000)`

Restituisce una durata di 4 secondi.

+++

## toInteger {#toInteger}

Converte un valore di argomento in un numero intero.

+++Sintassi

`toInteger(<parameter>)`

+++

+++Parametri

| Parametro | Descrizione |
|--- |--- |
| stringa | converte il valore stringa come numero intero |
| dateTime | converte la data in millisecondi (millisecondi epoca) |
| decimale | converte in numero intero rimuovendo la parte decimale (ad esempio: 1,5 diventa 1) |
| booleano | converte il valore booleano come 1 se true, 0 se false |

+++

+++Firme e tipo restituito

`toInteger(<dateTime>)`

`toInteger(<decimal>)`

`toInteger(<integer>)`

`toInteger(<string>)`

`toInteger(<boolean>)`

Restituisce un numero intero.

+++

+++Esempi

`toInteger("4")`

Restituisce 4.

+++

## toString {#toString}

Converte un valore di argomento in un valore stringa, a seconda del tipo. Per ulteriori informazioni sui tipi di dati, consultare [questa pagina](../expression/data-types.md).

+++Sintassi

`toString(<parameter>)`

+++

+++Parametri

| Parametro | Descrizione |
|--- |--- |
| dateTime | converte la data nel formato data UTC |
| dateTimeOnly | converte la data nel formato data UTC |
| durata | convertire nel numero di millisecondi corrispondente come stringa |
| intero | converte in rappresentazione stringa del valore (1 diventa &quot;1&quot;) |
| decimale | converte in rappresentazione stringa del valore (1,5 diventa &quot;1,5&quot;) |
| booleano | converti il valore booleano come &#39;true&#39; se true, &#39;false&#39; se false |

+++

+++Firme e tipo restituito

`toString(<dateTimeOnly>)`

`toString(<dateTime>)`

`toString(<duration>)`

`toString(<boolean>)`

`toString(<integer>)`

`toString(<decimal>)`

Restituisce una stringa.

+++

+++Esempi

`toString(4)`

Restituisce &quot;4&quot;.

`toString(#{ExperiencePlatform.test_date.person.birthDate}))`

Restituisce la rappresentazione in forma di stringa del campo dataOnly specificato (campo Data XDM), ad esempio &quot;2023-08-18&quot;.

`toString(toDuration(1520))`

Restituisce &quot;PT1.52S&quot;.

+++

