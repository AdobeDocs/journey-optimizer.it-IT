---
product: journey optimizer
title: Funzioni stringa
description: Informazioni sulle funzioni stringa
feature: Journeys
role: Developer
level: Experienced
keywords: stringa, funzioni, espressione, percorso, testo, manipolazione
version: Journey Orchestration
source-git-commit: bb47ca4957129a4d05aa3d7286409eef0cb62143
workflow-type: tm+mt
source-wordcount: '1127'
ht-degree: 15%

---

# Funzioni stringa {#string-functions}

Le funzioni stringa consentono di manipolare e utilizzare valori di testo all&#39;interno delle espressioni di percorso. Queste funzioni sono essenziali per l’elaborazione, la convalida, la trasformazione e l’analisi del testo nei percorsi del cliente.

Utilizza le funzioni stringa quando devi:

* Concatena e combina più valori di testo ([concat](#concat))
* Cerca pattern o sottostringhe di testo specifiche ([contain](#contain), [containIgnoreCase](#containIgnoreCase), [indexOf](#indexOf), [lastIndexOf](#lastIndexOf), [matchRegExp](#matchRegExp))
* Confronta le stringhe con corrispondenza con distinzione tra maiuscole e minuscole o senza distinzione tra maiuscole e minuscole ([equalIgnoreCase](#equalIgnoreCase), [notEqualIgnoreCase](#notEqualIgnoreCase))
* Controlla se la stringa inizia e termina ([startWith](#startWith), [startWithIgnoreCase](#startWithIgnoreCase), [endWith](#endWith), [endWithIgnoreCase](#endWithIgnoreCase))
* Estrai parti di testo utilizzando operazioni di sottostringa ([substr](#substr))
* Trasforma il testo in maiuscolo o minuscolo ([upper](#upper), [lower](#lower), [trim](#trim))
* Verifica se le stringhe sono vuote o contengono valori specifici ([isEmpty](#isEmpty), [isNotEmpty](#isNotEmpty))
* Sostituisci modelli di testo con nuovi valori ([replace](#replace), [replaceAll](#replaceAll))
* Dividi le stringhe in matrici per ulteriore elaborazione ([split](#split))
* Ottieni la lunghezza della stringa ([lunghezza](#length)) o genera identificatori univoci ([uuid](#uuid))

Le funzioni stringa forniscono funzionalità complete di manipolazione del testo, consentendo un’elaborazione sofisticata dei dati e una logica condizionale basata sul contenuto di testo nelle espressioni di percorso.

## concatena {#concat}

Concatena due parametri di stringa o un elenco di stringhe.

+++Sintassi

`concat(<parameters>)`

+++

+++Parametri

| Parametro | Tipo |
|-----------|------------------|
| Elenco | listString |
| stringa | stringa |

+++

+++Firma e tipo restituito

`concat(<string>,<string>)`

`concat(<listString>)`

Restituisce una stringa.

+++

+++Esempi

`concat("Hello","World")`

Restituisce &quot;HelloWorld&quot;.

`concat(["Hello"," ","World"])`

Restituisce &quot;Hello World&quot;.

+++

## contain {#contain}

Controlla se la seconda stringa di argomento è contenuta nella prima stringa di argomento.

+++Sintassi

`contain(<parameters>)`

+++

+++Parametri

* stringa

+++

+++Firma e tipo restituito

`contain(<string>,<string>)`

Restituisce un valore booleano.

+++

+++Esempi

`contain("rowing is great", "great")`

Restituisce true.

+++

## containIgnoreCase {#containIgnoreCase}

Controlla se la seconda stringa di argomento è contenuta nella prima stringa di argomento, senza tenere conto della distinzione tra maiuscole e minuscole.

+++Sintassi

`containIgnoreCase(<parameters>)`

+++

+++Parametri

| Parametro | Tipo |
|-----------|------------------|
| stringa | stringa |
| stringa cercata | stringa |

+++

+++Firma e tipo restituito

`containIgnoreCase(<string>,<string>)`

Restituisce un valore booleano.

+++

+++Esempi

`containIgnoreCase("rowing is great", "GREAT")`

Restituisce true.

+++

## endWith {#endWith}

Restituisce true se il secondo parametro è un suffisso del primo.

+++Sintassi

`endWith(<parameters>)`

+++

+++Parametri

| Parametro | Tipo |
|-----------|------------------|
| stringa | stringa |
| suffisso | stringa |

+++

+++Firma e tipo restituito

`endWith(<string>,<string>)`

Restituisce un valore booleano.

+++

+++Esempi

`endWith("Hello World", "World")`

Restituisce true.

`endWith("Hello World", "Hello")`

Restituisce false.

+++

## endWithIgnoreCase {#endWithIgnoreCase}

Controlla se la stringa del primo argomento termina con una stringa specifica (stringa del secondo argomento), senza tenere conto delle maiuscole/minuscole.

+++Sintassi

`endWithIgnoreCase(<parameters>)`

+++

+++Parametri

| Parametro | Tipo |
|-----------|------------------|
| stringa | stringa |
| suffisso | stringa |

+++

+++Firma e tipo restituito

`endWithIgnoreCase(<string>,<string>)`

Restituisce un valore booleano.

+++

+++Esempi

`endWithIgnoreCase("rowing is great", "AT")`

Restituisce true.

+++

## equalIgnoreCase {#equalIgnoreCase}

Confronta la prima stringa di argomento con la seconda stringa di argomento, ignorando le considerazioni relative alle maiuscole/minuscole.

+++Sintassi

`equalIgnoreCase(<parameters>)`

+++

+++Parametri

* stringa

+++

+++Firma e tipo restituito

`equalIgnoreCase(<string>,<string>)`

Restituisce un valore booleano.

+++

+++Esempi

`equalIgnoreCase("rowing is great", "rowing is GREAT")`

Restituisce true.

+++

## indexOf {#indexOf}

Restituisce la posizione della prima occorrenza del secondo parametro nel primo argomento. Restituisce -1 se non viene trovata alcuna corrispondenza.

+++Sintassi

`indexOf(<parameters>)`

+++

+++Parametri

| Parametro | Tipo |
|-----------|------------------|
| stringa | Stringa |
| valore specificato | Stringa |

+++

+++Firma e tipo restituito

`indexOf(<string>,<string>)`

Restituisce un numero intero.

+++

+++Esempi

`indexOf("Hello", "l")`

Restituisce 2.

Spiegazione:

In &quot;Hello&quot;, la prima occorrenza di &quot;l&quot; è nella posizione 2.

+++

## IsEmpty {#isEmpty}

Restituisce true se la stringa nel parametro non contiene alcun carattere.

+++Sintassi

`isEmpty(<parameters>)`

+++

+++Parametri

* stringa

+++

+++Firma e tipo restituito

`isEmpty(<string>)`

Restituisce un valore booleano.

+++

+++Esempi

`isEmpty("")`

Restituisce true.

`isEmpty("Hello World")`

Restituisce false.

+++

## isNotEmpty {#isNotEmpty}

Restituisce true se la stringa nel parametro non è vuota.

+++Sintassi

`isNotEmpty(<parameters>)`

+++

+++Parametri

* stringa

+++

+++Firma e tipo restituito

`isNotEmpty(<string>)`

Restituisce un valore booleano.

+++

+++Esempi

`isNotEmpty("")`

Restituisce false.

`isNotEmpty("hello")`

Restituisce true.

+++

## lastIndexOf {#lastIndexOf}

Restituisce la posizione (nel primo argomento) dell&#39;ultima occorrenza del secondo parametro. Restituisce -1 se non viene trovata alcuna corrispondenza.

+++Sintassi

`lastIndexOf(<parameters>)`

+++

+++Parametro

| Parametro | Tipo |
|-----------|------------------|
| stringa | Stringa |
| valore specificato | Stringa |

+++

+++Firma e tipo restituito

`lastIndexOf(<string>,<string>)`

Restituisce un numero intero.

+++

+++Esempi

`lastIndexOf("Hello", "l")`

Restituisce 3.

Spiegazione:

In &quot;Hello&quot;, l&#39;ultima occorrenza di &quot;l&quot; è nella posizione 3.

+++

## lunghezza {#length}

Restituisce il numero di caratteri dell’espressione stringa nel parametro.

+++Sintassi

`length(<parameters>)`

+++

+++Parametro

* stringa

+++

+++Firma e tipo restituito

`length(<string>)`

Restituisce un numero intero.

+++

+++Esempi

`length("Hello World")`

Restituisce 11.

+++

## lower {#lower}

Restituisce una versione in minuscolo del parametro.

+++Sintassi

`lower(<parameter>)`

+++

+++Parametro

* stringa

+++

+++Firma e tipo restituito

`lower(<string>)`

Restituisce una stringa.

+++

+++Esempi

`lower("A")`

Restituisce &quot;a&quot;.

+++

## matchRegExp {#matchRegExp}

Restituisce true se la stringa nel primo parametro corrisponde all&#39;espressione regolare nel secondo parametro. Per ulteriori informazioni, vedere [questa pagina](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html).

+++Sintassi

`matchRegExp(<parameters>)`

+++

+++Parametri

| Parametro | Tipo |
|--- |--- |
| stringa | stringa |
| regexp | stringa |

+++

+++Firma e tipo restituito

`matchRegExp(<string>,<string>)`

Restituisce un valore booleano.

+++

+++Esempi

`matchRegExp("12345", "\\d+")`

Restituisce true.

+++

## notEqualIgnoreCase {#notEqualIgnoreCase}

Verificare se la prima stringa di argomento con la seconda stringa di argomento è diversa, ignorando le considerazioni relative alle maiuscole e minuscole.

+++Sintassi

`notEqualIgnoreCase(<parameters>)`

+++

+++Parametri

* stringa

+++

+++Firma e tipo restituito

`notEqualIgnoreCase(<string>,<string>)`

Restituisce un valore booleano.

+++

+++Esempi

`notEqualIgnoreCase(@event{iOSPushPermissionAllowed.device.model}, "iPad")`

+++

## replace {#replace}

Sostituisce la prima occorrenza corrispondente alla stringa di destinazione con la stringa di sostituzione nella stringa di base.

La sostituzione procede dall&#39;inizio della stringa alla fine, ad esempio, sostituendo &quot;aa&quot; con &quot;b&quot; nella stringa &quot;aaa&quot; si otterrà &quot;ba&quot; invece di &quot;ab&quot;.

+++Sintassi

`replace(<parameters>)`

+++

+++Parametri

| Parametro | Tipo |
|-----------|--------------|
| base | stringa |
| destinazione | stringa (RegExp) |
| sostituzione | stringa |

+++

+++Firma e tipo restituito

`replace(<base>,<target>,<replacement>)`

Restituisce una stringa.

+++

+++Esempi

`replace("Hello World", "l", "x")`

Restituisce &quot;Hexlo World&quot;.

**Esempio con RegExp:**

Poiché il parametro di destinazione è un RegExp, a seconda della stringa che si desidera sostituire, potrebbe essere necessario eseguire l&#39;escape di alcuni caratteri. Ecco un esempio:

* stringa da valutare: `|OFFER_A|OFFER_B`
* fornito da un attributo di profilo `#{ExperiencePlatform.myFieldGroup.profile.myOffers}`
* Stringa da sostituire: `|OFFER_A`
* Stringa sostituita da: `''`
* Aggiungere `\\` prima del carattere `|`.

L’espressione è:

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|OFFER_A', '')`

La stringa restituita è: `|OFFER_B`

Puoi anche creare la stringa da sostituire da un dato attributo:

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|' + #{ExperiencePlatform.myFieldGroup.profile.myOfferCode}, '')`

+++

## replaceAll {#replaceAll}

Sostituisce tutte le occorrenze che corrispondono alla stringa di destinazione con la stringa di sostituzione nella stringa di base.

La sostituzione procede dall&#39;inizio della stringa alla fine, ad esempio, sostituendo &quot;aa&quot; con &quot;b&quot; nella stringa &quot;aaa&quot; si otterrà &quot;ba&quot; invece di &quot;ab&quot;.

+++Sintassi

`replaceAll(<parameters>)`

+++

+++Parametri

| Parametro | Tipo |
|-----------|--------------|
| base | stringa |
| destinazione | stringa (RegExp) |
| sostituzione | stringa |

+++

+++Firma e tipo restituito

`replaceAll(<baseString>,<sourceString>,<replacementString>)`

Restituisce una stringa.

+++

+++Esempi

`replaceAll("Hello World", "l", "x")`

Restituisce &quot;Hexxo Worxd&quot;.

Poiché il parametro di destinazione è un RegExp, a seconda della stringa che si desidera sostituire, potrebbe essere necessario eseguire l&#39;escape di alcuni caratteri. Consulta l&#39;esempio nella funzione [replace](#replace).

+++

## split {#split}

Divide la prima stringa di argomento con una stringa di separatore (seconda stringa di argomento, che può essere un&#39;espressione regolare) per produrre un elenco di stringhe (token).

+++Sintassi

`split(<parameters>)`

+++

+++Parametri

| Parametro | Tipo |
|-----------|------------------|
| stringa di input | stringa |
| stringa separatore | stringa |

+++

+++Firme e tipo restituito

`split(<input string>, <separator string>)`

Restituisce un valore listString.

+++

+++Esempi

`split("A_B_C", "_")`

Restituisce `["A","B","C"]`

Esempio con un campo evento &quot;event.appVersion&quot; con valore: &quot;20.45.2.3434&quot;

`split(@event{event.appVersion}, "\\.")`

Restituisce `["20", "45", "2", "3434"]`

+++

## startWith {#startWith}

Restituisce true se il secondo parametro è un prefisso del primo.

+++Sintassi

`startWith(<parameters>)`

+++

+++Parametri

| Parametro | Tipo |
|-------------|--------|
| stringa | stringa |
| prefisso | stringa |

+++

+++Firma e tipo restituito

`startWith(<string>,<string>)`

Restituisce un valore booleano.

+++

+++Esempi

`startWith("Hello World", "Hello")`

Restituisce true.

`startWith("Hello World", "World")`

Restituisce false.

+++

## startWithIgnoreCase {#startWithIgnoreCase}

Restituisce true se il secondo parametro è un prefisso del primo senza considerare la distinzione tra maiuscole e minuscole.

+++Sintassi

`startWithIgnoreCase(<parameters>)`

+++

+++Parametri

| Parametro | Tipo |
|-------------|--------|
| stringa | stringa |
| prefisso | stringa |

+++

+++Firma e tipo restituito

`startWithIgnoreCase(<string>,<string>)`

Restituisce un valore booleano.

+++

+++Esempi

`startWithIgnoreCase("rowing is great", "RO")`

Restituisce true.

+++

## substr {#substr}

Restituisce la sottostringa dell&#39;espressione stringa tra l&#39;indice iniziale e l&#39;indice finale. Se l&#39;indice finale non è definito, si trova tra l&#39;indice iniziale e la fine.

+++Sintassi

`substr(<parameters>)`

+++

+++Parametri

| Parametro | tipo |
|-------------|----------|
| stringa | stringa |
| beginIndex | intero |
| endIndex | intero |

+++

+++Firma e tipo restituito

`substr(<string>,<beginIndex>)`

`substr(<string>,<beginIndex>,<endIndex>)`

Restituisce una stringa.

+++

+++Esempi

`substr("Hello World",6)`

Restituisce &quot;World&quot;.

`substr("Hello World", 0, 5)`

Restituisce &quot;Hello&quot;.

+++

## trim {#trim}

Rimuove gli spazi iniziali e finali.

+++Sintassi

`trim(<parameters>)`

+++

+++Parametro

| Parametro | Tipo |
|-----------|------------------|
| stringa | stringa |

+++

+++Firma e tipo restituito

`trim(<string>)`

Restituisce una stringa.

+++

+++Esempi

`trim(" Hello ")`

Restituisce &quot;Hello&quot;.

+++

## upper {#upper}

Restituisce una versione in maiuscolo del parametro.

+++Sintassi

`upper(<parameters>)`

+++

+++Firma e tipo restituito

`upper(<string>)`

Restituisce una stringa.

+++

+++Esempi

`upper("b")`

Restituisce &quot;B&quot;.

+++

## uuid {#uuid}

Genera un UUID (Universal Unique IDentifier) casuale.

+++Sintassi

`uuid()`

+++

+++Parametri 

Questa funzione non richiede parametri.

+++

+++Firma e tipo restituito

`uuid()`

Restituisce una stringa.

+++

+++Esempi

`uuid()`

Restituisce &quot;79e70b7f-8a85-400b-97a1-9f9826121553&quot;.

+++

