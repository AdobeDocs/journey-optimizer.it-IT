---
title: Libreria funzioni operatori
description: Libreria funzioni operatori
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 75b0b380-d9a6-418e-b9f6-e64de385ba8d
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 11%

---

# Operatori {#operators}

## Funzioni booleane {#boolean-functions}

Le funzioni booleane vengono utilizzate per eseguire la logica booleana su elementi diversi.

### E{#and}

La funzione `and` viene utilizzata per creare una congiunzione logica.

**Sintassi**

```sql
{%= query1 and query2 %}
```

**Esempio**

L&#39;operazione seguente restituirà tutte le persone con paese di origine come la Francia e anno di nascita del 1985.

```sql
{%= profile.homeAddress.country = "France" and profile.person.birthYear = 1985 %}
```

### Oppure{#or}

La funzione `or` viene utilizzata per creare una disgiunzione logica.

**Sintassi**

```sql
{%= query1 or query2 %}
```

**Esempio**

L&#39;operazione seguente restituirà tutte le persone con il paese di origine come Francia o anno di nascita del 1985.

```sql
{%= profile.homeAddress.country = "France" or profile.person.birthYear = 1985 %}
```

<!--
## Not{#not}

The `not` (or `!`) function is used to create a logical negation.

**Syntax**

```sql
not ({QUERY})
!({QUERY})
```

**Example**

The following operation will return all people who do not have their home country as Canada.

```sql
not (homeAddress.countryISO = "CA")
```
-->

## Funzioni di confronto {#comparison-functions}

Le funzioni di confronto vengono utilizzate per confrontare espressioni e valori diversi, restituendo di conseguenza true o false.

### È uguale a{#equals}

La funzione `=` (è uguale a) controlla se un valore o un&#39;espressione è uguale a un altro valore o espressione.

**Sintassi**

```sql
{%= expression = value %}
```

**Esempio**

L&#39;operazione seguente verifica se il paese di residenza è la Francia.

```sql
{%= profile.homeAddress.country = "France" %}
```

### Non uguale{#notequal}

La funzione `!=` (diverso da) controlla se un valore o un&#39;espressione è **diverso** uguale a un altro valore o espressione.

**Sintassi**

```sql
{%= expression != value %}
```

**Esempio**

L&#39;operazione seguente verifica se l&#39;indirizzo del paese di origine non è la Francia.

```sql
{%= profile.homeAddress.country != "France" %}
```

### Maggiore di{#greaterthan}

La funzione `>` (maggiore di) viene utilizzata per verificare se il primo valore è maggiore del secondo valore.

**Sintassi**

```sql
{%= expression1 > expression2 %}
```

**Esempio**

L&#39;operazione seguente definisce le persone nate rigorosamente dopo il 1970.

```sql
{%= profile.person.birthYear > 1970 %}
```

### Maggiore o uguale a{#greaterthanorequal}

La funzione `>=` (maggiore o uguale a) viene utilizzata per verificare se il primo valore è maggiore o uguale al secondo valore.

**Sintassi**

```sql
{%= expression1 >= expression2 %}
```

**Esempio**

L&#39;operazione seguente definisce le persone nate nel 1970 o dopo di esso.

```sql
{%= profile.person.birthYear >= 1970 %}
```

### Minore di{#lessthan}

La funzione di confronto `<` (minore di) viene utilizzata per verificare se il primo valore è minore del secondo valore.

**Sintassi**

```sql
{%= expression1 < expression2 %}
```

**Esempio**

L&#39;operazione seguente definisce le persone nate prima del 2000.

```sql
{%= profile.person.birthYear < 2000 %}
```

### Minore o uguale a{#lessthanorequal}

La funzione di confronto `<=` (minore o uguale a) viene utilizzata per verificare se il primo valore è minore o uguale al secondo valore.

**Sintassi**

```sql
{%= expression1 <= expression2 %}
```

**Esempio**

L&#39;operazione seguente definisce le persone nate nel 2000 o prima.

```sql
{%= profile.person.birthYear <= 2000 %}
```

**Operazioni con numeri**
