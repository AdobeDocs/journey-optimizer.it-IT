---
solution: Journey Optimizer
product: journey optimizer
title: Operatori
description: Scopri gli operatori nelle espressioni avanzate
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: espressione, sintassi, operatori, editor, percorso
exl-id: 706e2e02-9bd9-46e7-a73d-dda3c9ae4ba8
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 5%

---

# Operatori {#operators}

Esistono due tipi di operatori: operatori unari e operatori binari. Sono disponibili operatori unari di sinistra e operatori unari di destra.

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

* Quando si utilizza una moltiplicazione (`*`), entrambi i campi dell&#39;operazione devono avere lo stesso tipo, intero o decimale. Esempio:
   * l’esempio seguente è corretto: `3.0 * 4.0`
   * `3 * 4.0` genererà un errore

## Logico  {#logical}

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

### non

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

Nullo significa che l’espressione non ha un valore valutato.

Esempio:

```json
@{BarBeacon.location} is null
```

### non è nullo

```json
<expression> is not null
```

Il risultato è booleano.

Nullo significa che l’espressione non ha un valore valutato.

Esempio:

```json
@{BarBeacon.location} is not null
```

### ha valore null

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
>Per &lt;expression1> e &lt;expression2> non esiste alcun controllo del tipo di dati.

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
Per &lt;expression1> e &lt;expression2> non esiste alcun controllo del tipo di dati.

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

&lt;expression2> non deve essere uguale a 0 (restituisce 0).

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

## Math {#math}

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

Restituisce &quot;l’ora corrente è 2019-09-23T09:30:06,693Z&quot;

```json
(now()) + " is the current time"
```

Restituisce &quot;2019-09-23T09:30:06.693Z è l&#39;ora corrente&quot;

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
(toDateTime("2011-12-03T15:15:30Z")) + (toDuration("PT15M"))  
```

Restituisce un _dateTime_ 03/12/2011:30:30Z

```json
(toDateTimeOnly("2011-12-03T15:15:30")) + (toDuration("PT15M"))
```

Restituisce un _dateTimeOnly_ 03/12/2011:30:30

```json
(now()) + (toDuration("PT1H"))
```

Restituisce un _dateTime_ (con fuso orario UTC) un’ora dopo rispetto all’ora corrente

```json
(toDuration("PT1H")) + (toDuration("PT1H"))
```

Restituisce un _durata_ PT2H
