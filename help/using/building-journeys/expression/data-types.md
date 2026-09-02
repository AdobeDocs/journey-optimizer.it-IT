---
solution: Journey Optimizer
product: journey optimizer
title: Tipi di dati
description: Informazioni sui tipi di dati nelle espressioni avanzate
feature: Journeys
role: Developer
level: Experienced
keywords: espressione, dati, tipo di dati, percorso
exl-id: fdfc3287-d733-45fb-ad11-b4238398820a
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/0UKY3G4hyMnSkzh8wlMx-yQ1yymKjs6FuIBdGo1SJqc
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1124
ht-degree: 3%

---

# Tipi di dati {#data-types}

Tecnicamente, una costante contiene sempre un tipo di dati. Nell’espressione letterale, specifichiamo solo il valore. Il tipo di dati può essere dedotto dal valore (ad esempio stringa, numero intero, decimale e così via). Per casi specifici come la data e l’ora, utilizziamo funzioni dedicate per la rappresentazione.

Le sezioni seguenti forniscono informazioni sulle diverse espressioni dei tipi di dati e sulla loro rappresentazione.

## stringa {#string}

**Descrizione**

Sequenza comune di caratteri. Non dispone di dimensioni specifiche, ad eccezione di quelle implicite provenienti dall’ambiente, come la quantità di memoria disponibile.

Formato JSON: String

Formato di serializzazione: UTF-8

**Rappresentazione letterale**

```json
"<value>"
```

```json
'<value>'
```

**Esempio**

```json
"hello world"
```

```json
'hello world'
```

## intero {#integer}

**Descrizione**

Valore intero compreso tra -2^63 e 2^63-1.

Formato JSON: numero

**Rappresentazione letterale**

```json
<integer value>
```

**Esempio**

```json
42
```

## decimale {#decimal}

**Descrizione**

Numero decimale. Rappresenta un valore mobile:

* massimo valore positivo finito di tipo double, (2-2^-52)x2^1023
* valore normale positivo più piccolo di tipo double, 2-1022
* valore positivo più piccolo diverso da zero di tipo double, 2 p-1074

Formato JSON: numero

Formato di serializzazione: utilizzando &#39;.&#39; come separatore decimale.

**Rappresentazione letterale**

```json
<integer value>.<integer value>
```

**Esempio**

```json
3.14
```

## booleano {#boolean}

**Descrizione**

Valore booleano scritto in minuscolo: true o false

Formato JSON: booleano

**Rappresentazione letterale**

```json
true
```

```json
false
```

**Esempio**

```json
true
```

## dateOnly {#date-only}

**Descrizione**

Rappresenta solo una data senza un fuso orario, visualizzato come anno-mese-giorno.

È una descrizione della data, utilizzata per i compleanni.

Formato JSON: String.

Il formato è: AAAA-MM-GG (ISO-8601), ad esempio: &quot;2021-03-11&quot;.

Può essere incapsulato in una funzione toDateOnly.

Utilizza DateTimeFormatter ISO_LOCAL_DATE_TIME per deserializzare e serializzare il valore. [Ulteriori informazioni](https://datatracker.ietf.org/doc/html/rfc3339#section-5.6)

**Rappresentazione letterale**

```json
date("<dateOnly in ISO-8601 format>")  
```

**Esempio**

```json
date("2021-02-19")
```

## dateTimeOnly {#date-time-only}

**Descrizione**

Rappresenta una data/ora senza fuso orario, visualizzata come anno-mese-giorno-ora-minuto-secondo-millisecondo.

Formato JSON: String.

Non memorizza né rappresenta un fuso orario. Si tratta invece di una descrizione della data, utilizzata per i compleanni, combinata con l&#39;ora locale visualizzata su un orologio da parete.

Non può rappresentare un istante sulla linea temporale senza informazioni aggiuntive, ad esempio uno scostamento o un fuso orario.

Può essere incapsulato in una funzione toDateTimeOnly.

Formato di serializzazione: formato data/ora offset esteso ISO-8601.

Utilizza DateTimeFormatter ISO_LOCAL_DATE_TIME per deserializzare e serializzare il valore. [Ulteriori informazioni](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html#ISO_LOCAL_DATE_TIME"){_blank}.

**Rappresentazione letterale**

```json
date("<dateTimeOnly in ISO-8601 format>")  
```

**Esempi**

```json
date("2024-02-19T00.00.000")
date("2024-02-19T00.00")
```

## dateTime {#date-time}

**Descrizione**

Costante di data e ora che considera anche il fuso orario. Rappresenta una data-ora con uno scostamento da UTC.

Può essere vista come un istante di tempo con le informazioni aggiuntive dell&#39;offset. È un modo per rappresentare un &quot;momento&quot; specifico in un certo luogo del mondo.

Formato JSON: String.

Può essere incapsulato in una funzione toDateTime.

Formato di serializzazione: formato data/ora offset esteso ISO-8601.

Utilizza DateTimeFormatter ISO_OFFSET_DATE_TIME per deserializzare e serializzare il valore. [Ulteriori informazioni](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html#ISO_OFFSET_DATE_TIME){_blank}.

Puoi anche trasmettere un numero intero che passa un valore epoca. [Ulteriori informazioni](https://www.epochconverter.com){_blank}.

Il fuso orario può essere specificato da uno scostamento o da un codice del fuso orario (ad esempio: Europa/Parigi, Z - che significa UTC).

**Rappresentazione letterale**

```json
toDateTime("<dateTime in ISO-8601 format>")
```

```json
date("<dateTime in ISO-8601 format>")
```

```json
toDateTime(<integer value of an epoch in milliseconds>)
```

**Esempi**

```json
date("2024-02-19T00.00.000Z")
```

```json
toDateTime("1977-04-22T06:00:00Z")
```

```json
toDateTime("2023-12-03T15:15:30Z")
```

```json
toDateTime("2023-12-03T15:15:30.123Z")
```

```json
toDateTime("2023-12-03T15:15:30.123+02:00")
```

```json
toDateTime("2023-12-03T15:15:30.123-00:20")
```

```json
toDateTime(1560762190189)
```

## durata {#duration}

**Descrizione**

Rappresenta un periodo di tempo basato sul tempo, ad esempio &quot;34,5 secondi&quot;. Modella una quantità o una quantità di tempo in termini di millisecondi.

Le unità temporali supportate sono: millisecondi, secondi, minuti, ore, giorni in cui un giorno equivale a 24 ore. Anni e mesi non sono supportati in quanto non rappresentano un periodo di tempo fisso.

Formato JSON: String.

Deve essere incapsulato in una funzione toDuration.

Formato di serializzazione: per deserializzare un ID di fuso orario, viene utilizzata la funzione java java.time.

Duration.parse: i formati accettati sono basati sul formato di durata ISO-8601 PnDTnHnMn.nS con giorni considerati esattamente 24 ore. [Ulteriori informazioni](https://docs.oracle.com/javase/8/docs/api/java/time/Duration.html#parse-java.lang.CharSequence-){_blank}.

**Rappresentazione letterale**

```json
toDuration("<duration in ISO-8601 format>")
```

```json
toDuration(<duration in milliseconds>)
```

**Esempio**

```json
toDuration("PT5S") -- parses as 5 seconds
```

```json
toDuration(500) -- parses as 500ms
```

```json
toDuration("PT20.345S") -- parses as "20.345 seconds"
```

```json
toDuration("PT15M") -- parses as "15 minutes" (where a minute is 60 seconds)
```

```json
toDuration("PT10H")  -- parses as "10 hours" (where an hour is 3600 seconds)
```

```json
toDuration("P2D") -- parses as "2 days" (where a day is 24 hours or 86400 seconds)
```

```json
toDuration("P2DT3H4M") -- parses as "2 days, 3 hours and 4 minutes"
```

```json
toDuration("P-6H3M") -- parses as "-6 hours and +3 minutes"
```

```json
toDuration("-P6H3M") -- parses as "-6 hours and -3 minutes"
```

```json
toDuration("-P-6H+3M") -- parses as "+6 hours and -3 minutes"
```

## list {#list}

**Descrizione**

Elenco di espressioni separate da virgole che utilizzano parentesi quadre come delimitatori.

Il polimorfismo non è supportato, pertanto tutte le espressioni contenute nell&#39;elenco devono avere lo stesso tipo.

**Rappresentazione letterale**

```json
[<expression>, <expression>, ... ]
```

**Esempio**

```json
["value1","value2"]
```

```json
[3,5]
```

```json
[toDuration(500),toDuration(800)]
```

+++ Guida di riferimento della Knowledge Base di AI

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

* **TL;DR:** In questa pagina vengono descritti tutti i tipi di dati supportati nell&#39;editor di espressioni avanzate di Percorso, ovvero stringa, numero intero, decimale, booleano, dateOnly, dateTimeOnly, dateTime, duration ed list, con i relativi formati JSON, regole di serializzazione e sintassi di rappresentazione letterale.

**Intenti:**

* Identificare la sintassi letterale corretta per ogni tipo di dati durante la scrittura di espressioni di percorso
* Comprendere la differenza tra i tipi `dateOnly`, `dateTimeOnly` e `dateTime` e quando utilizzarli
* Rappresenta un valore di durata utilizzando il formato ISO-8601 o millisecondi con la funzione `toDuration()`
* Creare un&#39;espressione elenco con sintassi per parentesi quadre da utilizzare nelle operazioni di raccolta
* Utilizzare le funzioni di conversione (`toDateTime`, `toDateTimeOnly`, `toDuration`, `toDateOnly`) per creare costanti tipizzate

**Glossario:**

* **dateOnly**: una data senza fuso orario o ora, formattata come AAAA-MM-GG; adatta per compleanni o date di calendario *(specifico per prodotto)*
* **dateTimeOnly**: una data e un&#39;ora senza informazioni sul fuso orario; non può rappresentare un istante specifico senza un offset *(specifico per prodotto)*
* **dateTime**: una costante data-ora che include un offset UTC, che rappresenta un istante specifico; può anche essere creata da un numero intero epoca *(specifico per prodotto)*
* **durata**: quantità basata sul tempo modellata in millisecondi; utilizza il formato `PnDTnHnMn.nS` ISO-8601; anni e mesi non sono supportati *(specifici del prodotto)*
* **elenco**: raccolta di espressioni dello stesso tipo, separate da virgole, delimitate da parentesi quadre *(specifiche del prodotto)*

**Guardrail:**

* La durata supporta solo millisecondi, secondi, minuti, ore e giorni; anni e mesi non sono supportati in quanto non rappresentano quantità fisse di tempo
* Un valore `duration` deve essere racchiuso in `toDuration()`, non può essere espresso come valore letterale non elaborato
* Tutte le espressioni in un `list` devono avere lo stesso tipo — polimorfismo non supportato
* `dateTimeOnly` non può rappresentare un istante in tempo senza uno scostamento o un fuso orario aggiuntivo

**Terminologia:**

* Nome canonico: Tipi di dati — Acronimo: none — Varianti: tipi di dati espressione, tipi di dati percorso
* Sinonimi: &quot;dateTime&quot; = &quot;date-time with timezone&quot;; &quot;dateTimeOnly&quot; = &quot;local date-time&quot;
* Non confondere: `dateOnly` (nessuna ora) ≠ `dateTimeOnly` (data + ora, nessun fuso orario) ≠ `dateTime` (data + ora + fuso orario/offset)

**Domande frequenti:**

* **Q: Qual è la differenza tra `dateTimeOnly` e `dateTime`?** — `dateTimeOnly` non ha fuso orario o scostamento e non può rappresentare un istante preciso; `dateTime` include uno scostamento UTC e rappresenta un momento specifico nel tempo.
* **Q: come si esprime una durata di 2 giorni e 3 ore?** — Utilizza `toDuration("P2DT3H")`.
* **Q: è possibile combinare numeri interi e stringhe in un&#39;espressione elenco?** — No; tutte le espressioni di un elenco devono essere dello stesso tipo.
* **D: come si crea `dateTime` da un timestamp epoca in millisecondi?** — Utilizzare `toDateTime(<epoch in milliseconds>)`, ad esempio `toDateTime(1560762190189)`.
* **Q: `true` o `True` è il valore letterale booleano corretto?** — Utilizzare `true` o `false` in minuscolo; le varianti in maiuscolo non sono valide.

+++
