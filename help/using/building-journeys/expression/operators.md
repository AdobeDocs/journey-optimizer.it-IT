---
solution: Journey Optimizer
product: journey optimizer
title: Operatori
description: Informazioni sugli operatori nelle espressioni avanzate
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: espressione, sintassi, operatori, editor, percorso
exl-id: 706e2e02-9bd9-46e7-a73d-dda3c9ae4ba8
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 6%

---

# Operatori {#operators}

Esistono due tipi di operatori: operatori unari e operatori binari. Ci sono operatori unari a sinistra e operatori unari a destra.

```json
// left-hand unary operators
// <operator> <operand> 
// operand is an expression
not (@{LobbyBeacon.endUserIDs._experience.emailid.id}=="example@adobe.com")

// right-hand unary operators
// <operator> <operand> 
// operand is an expression
@{LobbyBeacon.endUserIDs._experience.emailid.id} is not null

// binary operators
// <operand1> <operator> <operand2>
// operand is an expression
(@{LobbyBeacon.endUserIDs._experience.emailid.id}=="example1@adobe.com") or (@{LobbyBeacon.endUserIDs._experience.emailid.id}=="example2@adobe.com") 
```

## Note importanti{#important-notes}

* Quando si utilizza una moltiplicazione (`*`), entrambi i campi operazione devono avere lo stesso tipo, intero o decimale. Esempio :
   * l&#39;esempio seguente è corretto: `3.0 * 4.0`
   * `3 * 4.0` porterà a un errore

## Logica  {#logical}

### e

```json
<expression1> and <expression2>
```

Entrambi &lt;expression1> e &lt;expression2> deve essere booleano. Il risultato è booleano.

Esempio:

```json
3.14 > 2 and 3.15 < 1
```

### oppure

```json
<expression1> or <expression2>
```

Entrambi &lt;expression1> e &lt;expression2> deve essere booleano. Il risultato è booleano.

Esempio:

```json
3.14 > 2 or 3.15 < 1
```

### not

```json
not <expression>
```

&lt;expression> deve essere booleano. Il risultato è booleano.

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

Il valore null indica che l&#39;espressione non ha alcun valore valutato.

Esempio:

```json
@{BarBeacon.location} is null
```

### non è null

```json
<expression> is not null
```

Il risultato è booleano.

Il valore null indica che l&#39;espressione non ha alcun valore valutato.

Esempio:

```json
@{BarBeacon.location} is not null
```

### ha null

```json
<expression> has null
```

&lt;expression> deve essere un elenco. Il risultato è booleano.

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
Per &lt;expression1> e &lt;expression2> non è disponibile alcun controllo del tipo di dati.

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

È possibile confrontare sia un numero intero che un decimale con un numero intero o decimale.

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

È possibile confrontare sia un numero intero che un decimale con un numero intero o decimale.

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

È possibile confrontare sia un numero intero che un decimale con un numero intero o decimale.

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

È possibile confrontare sia un numero intero che un decimale con un numero intero o decimale.

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

Entrambe le espressioni devono essere numeriche (integer o decimali).

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

Entrambe le espressioni devono essere numeriche (integer o decimali).

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

Entrambe le espressioni devono essere numeriche (integer o decimali).

Il risultato è anche numerico.

&lt;expression2> deve essere diverso da 0 (restituisce 0).

Esempio:

```json
4 / 2
```

Restituisce 2

### *

```json
<expression1> * <expression2>
```

Entrambe le espressioni devono essere numeriche (integer o decimali).

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

Entrambe le espressioni devono essere numeriche (integer o decimali).

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

Il tipo di espressione è integer o decimale.

Esempio:

```json
@ is numeric
```

### è un numero intero

```json
<expression> is integer
```

Il tipo di espressione è integer.

Esempio:

```json
@ is integer
```

### è decimale

```json
<expression> is decimal
```

Il tipo di espressione è decimale.

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

Conconcatena due espressioni.

Un&#39;espressione deve essere una stringa concatenata.

Esempio:

```json
"the current time is " + (now())
```

Restituisce &quot;l&#39;ora corrente è 2019-09-23T09:30:06,693Z&quot;

```json
(now()) + " is the current time"
```

Restituisce &quot;2019-09-23T09:30:06.693Z è l&#39;ora attuale&quot;

```json
"a" + "b" + "c" + 1234
```

Restituisce &quot;abc1234&quot;.

## Data {#date}

### +

```json
<expression> + <duration>
```

Aggiungi una durata a un dateTime, a un dateTimeOnly o a una durata.

Esempio:

```json
(toDateTime("2011-12-03T15:15:30Z")) + (toDuration("PT15M"))  
```

Restituisce un valore _dateTime_ 2011-12-03T15:30:30 Z

```json
(toDateTimeOnly("2011-12-03T15:15:30")) + (toDuration("PT15M"))
```

Restituisce un valore _dateTimeOnly_ 2011-12-03T15:30:30

```json
(now()) + (toDuration("PT1H"))
```

Restituisce un valore _dateTime_ (con fuso orario UTC) un&#39;ora dopo dall&#39;ora corrente

```json
(toDuration("PT1H")) + (toDuration("PT1H"))
```

Restituisce un valore _durata_ PT2H
