---
title: Libreria di funzioni per gli operatori
description: Libreria di funzioni per gli operatori
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 75b0b380-d9a6-418e-b9f6-e64de385ba8d
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 11%

---

# Operatori {#operators}

## Funzioni booleane

Le funzioni booleane vengono utilizzate per eseguire la logica booleana su elementi diversi.

### E{#and}

La `and` viene utilizzata per creare una congiunzione logica.

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

La `or` viene utilizzata per creare una disgiunzione logica.

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

La `=` (equals) controlla se un valore o un&#39;espressione è uguale a un altro valore o espressione.

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

La `!=` (diverso da uguale) controlla se un valore o un&#39;espressione è **not** uguale a un altro valore o espressione.

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

La `>` (maggiore di) viene utilizzato per verificare se il primo valore è maggiore del secondo valore.

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

La `>=` (maggiore o uguale a) viene utilizzato per verificare se il primo valore è maggiore o uguale al secondo valore.

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

La `<` (minore di) la funzione di confronto viene utilizzata per verificare se il primo valore è minore del secondo valore.

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

La `<=` (minore o uguale a) la funzione di confronto viene utilizzata per verificare se il primo valore è minore o uguale al secondo valore.

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
