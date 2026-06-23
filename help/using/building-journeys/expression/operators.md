---
solution: Journey Optimizer
product: journey optimizer
title: Operatori
description: Scopri gli operatori nelle espressioni avanzate
feature: Journeys
role: Developer
level: Experienced
keywords: espressione, sintassi, operatori, editor, percorso
exl-id: 706e2e02-9bd9-46e7-a73d-dda3c9ae4ba8
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/sK2GNHkkiJ4M5V99Uucc-b68iESNW7kCNBjHVNT-dMs
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1001
ht-degree: 3%

---

# Operatori {#operators}

Esistono due tipi di operatori: operatori unari e operatori binari. Sono disponibili operatori unari di sinistra e operatori unari di destra.

```json
// left-hand unary operators
// <operator> <operand> 
// operand is an expression
not (@event{LobbyBeacon.endUserIDs._experience.emailid.id}=="example@adobe.com")

// right-hand unary operators
// <operator> <operand> 
// operand is an expression
@event{LobbyBeacon.endUserIDs._experience.emailid.id} is not null

// binary operators
// <operand1> <operator> <operand2>
// operand is an expression
(@event{LobbyBeacon.endUserIDs._experience.emailid.id}=="example1@adobe.com") or (@event{LobbyBeacon.endUserIDs._experience.emailid.id}=="example2@adobe.com") 
```

## Note importanti{#important-notes}

* Quando si utilizza una moltiplicazione (`*`), entrambi i campi dell&#39;operazione devono avere lo stesso tipo, intero o decimale. Esempio:
   * l&#39;esempio seguente è corretto: `3.0 * 4.0`
   * `3 * 4.0` genererà un errore

* Quando si utilizza l&#39;operatore `+`, l&#39;espressione deve essere racchiusa tra parentesi. Esempio:
   * `toDateTimeOnly(toDateTime((currentTimeInMillis()) + 1))` è corretto
   * `toDateTimeOnly(toDateTime(currentTimeInMillis() + 1))` genererà un errore

## Logico  {#logical}

### e

```json
<expression1> and <expression2>
```

Sia &lt;espressione1> che &lt;espressione2> devono essere booleani. Il risultato è booleano.

Esempio:

```json
3.14 > 2 and 3.15 < 1
```

### oppure

```json
<expression1> or <expression2>
```

Sia &lt;espressione1> che &lt;espressione2> devono essere booleani. Il risultato è booleano.

Esempio:

```json
3.14 > 2 or 3.15 < 1
```

### non

```json
not <expression>
```

&lt;espressione> deve essere booleano. Il risultato è booleano.

Esempio:

```json
not 3.15 < 1
```

## Confronto {#comparison}

### è nullo

```json
<expression> is null
```

Il risultato è booleano.

Nullo significa che l’espressione non ha un valore valutato.

Esempio:

```json
@event{BarBeacon.location} is null
```

### non è nullo

```json
<expression> is not null
```

Il risultato è booleano.

Nullo significa che l’espressione non ha un valore valutato.

Esempio:

```json
@event{BarBeacon.location} is not null
```

### ha valore null

```json
<expression> has null
```

&lt;espressione> deve essere un elenco. Il risultato è booleano.

Utile per identificare che un elenco contiene almeno un valore null.

Esempio:

```json
["foo", "bar", null] has null
```

Restituisce true

```json
["foo", "bar", ""] has null
```

Restituisce false perché &quot;&quot; non è considerato nullo.

### ==

```json
<expression1> == <expression2>
```

>[!NOTE]
>
>Per &lt;expression1> e &lt;expression2> non è disponibile alcun controllo del tipo di dati.

Esempio:

```json
3.14 == 42
```

```json
"foo" == "bar"
```

### !=

```json
<expression1> != <expression2>
```

>[!NOTE]
>
>Per &lt;expression1> e &lt;expression2> non è disponibile alcun controllo del tipo di dati.

Il risultato è booleano.

Esempio:

```json
3.14 != 42
```

```json
"foo" != "bar"
```

### >

```json
<expression1> > <expression2>
```

Datetime può essere confrontato con Datetime.

Datetimeonly può essere confrontato con Datetimeonly.

Sia il numero intero che il numero decimale possono essere confrontati con il numero intero o il numero decimale.

Qualsiasi altra combinazione è vietata.

Il risultato è booleano.

Esempio:

```json
3.14 > 42
```

### >=

```json
<expression1> >= <expression2>
```

Datetime può essere confrontato con Datetime.

Datetimeonly può essere confrontato con Datetimeonly.

Sia il numero intero che il numero decimale possono essere confrontati con il numero intero o il numero decimale.

Qualsiasi altra combinazione è vietata.

Il risultato è booleano.

Esempio:

```json
42 >= 3.14
```

### &lt;

```json
<expression1> < <expression2>
```

Datetime può essere confrontato con Datetime.

Datetimeonly può essere confrontato con Datetimeonly.

Sia il numero intero che il numero decimale possono essere confrontati con il numero intero o il numero decimale.

Qualsiasi altra combinazione è vietata.

Il risultato è booleano.

Esempio:

```json
42 < 3.14
```

### &lt;=

```json
<expression1> <= <expression2>
```

Datetime può essere confrontato con Datetime.

Datetimeonly può essere confrontato con Datetimeonly.

Sia il numero intero che il numero decimale possono essere confrontati con il numero intero o il numero decimale.

Qualsiasi altra combinazione è vietata.

Il risultato è booleano.

Esempio:

```json
42 <= 3.14
```

## Aritmetica {#arithmetic}

### +

```json
<expression1> + <expression2>
```

Entrambe le espressioni devono essere numeriche (numero intero o decimale).

Il risultato è anche numerico.

Esempio:

```json
1 + 2
```

Restituisce 3

### -

```json
<expression1> - <expression2>
```

Entrambe le espressioni devono essere numeriche (numero intero o decimale).

Il risultato è anche numerico.

Esempio:

```json
2 - 1 
```

Restituisce 1

### /

```json
<expression1> / <expression2>
```

Entrambe le espressioni devono essere numeriche (numero intero o decimale).

Il risultato è anche numerico.

&lt;espressione2> non deve essere uguale a 0 (restituisce 0).

Esempio:

```json
4 / 2
```

Restituisce 2

### *

```json
<expression1> * <expression2>
```

Entrambe le espressioni devono essere numeriche (numero intero o decimale).

Il risultato è anche numerico.

Esempio:

```json
3 * 4
```

Restituisce 12

### %

```json
<expression1> % <expression2>
```

Entrambe le espressioni devono essere numeriche (numero intero o decimale).

Il risultato è anche numerico.

Esempio:

```json
3 % 2
```

Restituisce 1.

## Matematica {#math}

### è numerico

```json
<expression> is numeric
```

Il tipo dell&#39;espressione è numero intero o decimale.

Esempio:

```json
@ is numeric
```

### è un numero intero

```json
<expression> is integer
```

Il tipo dell&#39;espressione è un numero intero.

Esempio:

```json
@ is integer
```

### è decimale

```json
<expression> is decimal
```

Il tipo dell&#39;espressione è decimal.

Esempio:

```json
@ is decimal
```

## Stringa {#string}

### +

```json
<string> + <expression>
```

```json
<expression> + <string>
```

Concatena due espressioni.

Un&#39;espressione deve essere una stringa concatenata.

Esempio:

```json
"the current time is " + (now())
```

Restituisce &quot;l’ora corrente è 2023-09-23T09:30:06.693Z&quot;

```json
(now()) + " is the current time"
```

Restituisce &quot;2023-09-23T09:30:06.693Z è l’ora corrente&quot;

```json
"a" + "b" + "c" + 1234
```

Restituisce &quot;abc1234&quot;.

## Data {#date}

### +

```json
<expression> + <duration>
```

Aggiungere una durata a un valore dateTime, dateTimeOnly o duration.

Esempio:

```json
(toDateTime("2023-12-03T15:15:30Z")) + (toDuration("PT15M"))  
```

Restituisce un valore _dateTime_ 2023-12-03T15:30:30Z

```json
(toDateTimeOnly("2023-12-03T15:15:30")) + (toDuration("PT15M"))
```

Restituisce un valore _dateTimeOnly_ 2023-12-03T15:30:30

```json
(now()) + (toDuration("PT1H"))
```

Restituisce un valore _dateTime_ (con fuso orario UTC) un&#39;ora dopo rispetto all&#39;ora corrente

```json
(toDuration("PT1H")) + (toDuration("PT1H"))
```

Restituisce un valore _duration_ PT2H

+++ Guida di riferimento della Knowledge Base di AI

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

* **TL;DR:** Questa pagina è un riferimento completo degli operatori disponibili nell&#39;editor di espressioni avanzate del Percorso, che include analisi logiche (`and`, `or`, `not`), confronti (`==`, `!=`, `>`, `>=`, `<`, `<=`, `is null`, `is not null`, `has null`), aritmetiche (`+`, `-`, `/`, `*`, `%`), controllo del tipo di corrispondenza (`is numeric`, `is integer`, `is decimal`), concatenazione di stringhe e operatori aritmetici di data.

**Intenti:**

* Combinare condizioni booleane utilizzando gli operatori logici `and`, `or` e `not`
* Verificare se il valore di un campo o di un&#39;espressione è null o non null utilizzando `is null` / `is not null`
* Rilevare valori Null in un elenco utilizzando l&#39;operatore `has null`
* Confronta valori numerici, datetime e datetimeonly utilizzando `>`, `>=`, `<`, `<=`, `==` e `!=`
* Eseguire l&#39;aritmetica sui valori numerici utilizzando `+`, `-`, `/`, `*` e `%`
* Aggiungere una durata a un valore dateTime, dateTimeOnly o duration utilizzando l&#39;operatore `+`

**Glossario:**

* **Operatore unario**: operatore applicato a un singolo operando; può essere mano sinistra (esempio: `not`) o mano destra (esempio: `is null`) *(specifico per prodotto)*
* **Operatore binario**: operatore applicato tra due operandi (ad esempio `and`, `==`, `+`) *(specifico per prodotto)*
* **ha null**: operatore unario destro che restituisce true se un elenco contiene almeno un elemento null *(specifico per prodotto)*
* **è numerico / è intero / è decimale**: operatori di verifica dei tipi che restituiscono un valore booleano basato sul sottotipo numerico dell&#39;espressione *(specifico per prodotto)*

**Guardrail:**

* Quando si utilizza la moltiplicazione (`*`), entrambi gli operandi devono essere dello stesso tipo numerico (intero o entrambi i decimali). La combinazione dei tipi causa un errore
* Quando si utilizza l&#39;operatore `+` per l&#39;aritmetica delle date, l&#39;espressione deve essere racchiusa tra parentesi per evitare errori di analisi
* Gli operatori di confronto (`>`, `>=`, `<`, `<=`) sono validi solo tra tipi compatibili: Datetime con Datetime, DatetimeOnly con DatetimeOnly o numeric con numeric. Qualsiasi altra combinazione non è consentita
* Una stringa vuota `""` non è considerata nulla — `has null` restituisce false per un elenco contenente `""`
* Gli operatori `==` e `!=` non eseguono alcun controllo del tipo di dati tra operandi

**Terminologia:**

* Nome canonico: Operators — Acronym: none — variants: expression operators, percorsi operators
* Sinonimi: `and` = &quot;AND logico&quot;; `or` = &quot;OR logico&quot;; `not` = &quot;NOT logico&quot;; `%` = &quot;modulo&quot;
* Non confondere: `is null` (l&#39;espressione non ha un valore valutato) ≠ `== null` (sintassi non valida); `has null` (l&#39;elenco contiene null) ≠ `is null` (l&#39;espressione stessa è null)

**Domande frequenti:**

* **Q: è possibile moltiplicare direttamente un numero intero per un numero decimale?** — No; entrambi gli operandi di `*` devono essere dello stesso tipo. Utilizzare `3.0 * 4.0` (entrambi decimali) o `3 * 4` (entrambi interi).
* **Q: come si aggiungono 15 minuti a un dateTime?** — Utilizza `(toDateTime("...")) + (toDuration("PT15M"))`.
* **Q: Qual è la differenza tra `is null` e `has null`?** — `is null` controlla se una singola espressione non ha un valore valutato; `has null` controlla se un elenco contiene almeno un elemento null.
* **Q: `"" has null` restituisce true?** — No; una stringa vuota non è considerata nulla, pertanto il risultato è falso.
* **Q: perché `3 * 4.0` causa un errore?** — L&#39;operatore `*` richiede che entrambi gli operandi siano dello stesso tipo numerico. La combinazione di numeri interi e decimali non è consentita.

+++
