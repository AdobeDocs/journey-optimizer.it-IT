---
title: Libreria di funzioni per gli operatori
description: Libreria di funzioni per gli operatori
feature: Personalizzazione
topic: Personalizzazione
role: Data Engineer
level: Experienced
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 12%

---

# Operatori {#operators}

![](../../assets/do-not-localize/badge.png)

## Funzioni booleane

Le funzioni booleane vengono utilizzate per eseguire la logica booleana su elementi diversi.

### E{#and}

La funzione `and` viene utilizzata per creare una congiunzione logica.

**Formato**

```sql
{%= query1 and query2 %}
```

**Esempio**

L&#39;operazione successiva prevede il rimpatrio di tutte le persone con il paese d&#39;origine come la Francia e l&#39;anno di nascita del 1985.

```sql
{%= profile.homeAddress.country = "France" and profile.person.birthYear = 1985 %}
```

### Oppure{#or}

La funzione `or` viene utilizzata per creare una disgiunzione logica.

**Formato**

```sql
{%= query1 or query2 %}
```

**Esempio**

L&#39;operazione successiva prevede il rimpatrio di tutte le persone con il paese d&#39;origine come la Francia o l&#39;anno di nascita del 1985.

```sql
{%= profile.homeAddress.country = "France" or profile.person.birthYear = 1985 %}
```

<!--
## Not{#not}

The `not` (or `!`) function is used to create a logical negation.

**Format**

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





## Funzioni di confronto

Le funzioni di confronto vengono utilizzate per confrontare espressioni e valori diversi e restituiscono true o false di conseguenza.

### È uguale a{#equals}

La funzione `=` (equals) controlla se un valore o un&#39;espressione è uguale a un altro valore o espressione.

**Formato**

```sql
{%= expression = value %}
```

**Esempio**

L&#39;operazione seguente controlla se il paese di origine è la Francia.

```sql
{%= profile.homeAddress.country = "France" %}
```

### Non uguale{#notequal}

La funzione `!=` (non uguale) controlla se un valore o un&#39;espressione è **non** uguale a un altro valore o espressione.

**Formato**

```sql
{%= expression != value %}
```

**Esempio**

L&#39;operazione seguente controlla se il paese di origine non è la Francia.

```sql
{%= profile.homeAddress.country != "France" %}
```

### Maggiore di{#greaterthan}

La funzione `>` (maggiore di) viene utilizzata per verificare se il primo valore è maggiore del secondo valore.

**Formato**

```sql
{%= expression1 > expression2 %}
```

**Esempio**

La seguente operazione definisce le persone nate rigorosamente dopo il 1970.

```sql
{%= profile.person.birthYear > 1970 %}
```

### Maggiore o uguale a{#greaterthanorequal}

La funzione `>=` (maggiore o uguale a) viene utilizzata per verificare se il primo valore è maggiore o uguale al secondo valore.

**Formato**

```sql
{%= expression1 >= expression2 %}
```

**Esempio**

L&#39;operazione seguente definisce le persone nate nel 1970 o dopo tale data.

```sql
{%= profile.person.birthYear >= 1970 %}
```

### Minore di{#lessthan}

La funzione di confronto `<` (minore di) viene utilizzata per verificare se il primo valore è minore del secondo valore.

**Formato**

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

**Formato**

```sql
{%= expression1 <= expression2 %}
```

**Esempio**

L&#39;operazione seguente definisce le persone nate nel 2000 o prima.

```sql
{%= profile.person.birthYear <= 2000 %}
```

**Operazioni con numeri**

