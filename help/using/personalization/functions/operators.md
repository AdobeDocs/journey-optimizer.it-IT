---
title: Libreria funzioni operatori
description: Libreria funzioni operatori
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 75b0b380-d9a6-418e-b9f6-e64de385ba8d
TQID: https://experienceleague.adobe.com/b4Tz4auDyWb-iaUYAie31DL5hlHh97n3rYm7EP-JjIw
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
feature_v2: id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2: []
source-git-commit: b08de542c4f952f82a503103c783e54196c6d5b6
workflow-type: tm+mt
source-wordcount: 461
ht-degree: 9%

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

## Funzioni di migrazione modelli {#template-migration-functions}

Le funzioni di migrazione dei modelli sono disponibili nell’editor di personalizzazione per facilitare la migrazione dei modelli esistenti a Journey Optimizer.

### Confronta tramite operatore{#amp-compare}

La funzione `ampCompare` confronta due valori utilizzando l&#39;operatore di confronto specificato.

**Sintassi**

```sql
{%= ampCompare(value1, value2, operator) %}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `value1` | Primo valore da confrontare. |
| `value2` | Secondo valore da confrontare. |
| `operator` | Intero che rappresenta l’operatore di confronto da utilizzare. |

**Esempio**

```sql
{%= ampCompare(profile.person.age, 18, 4) %}
```

### Intervallo sottostringa{#amp-substr}

La funzione `ampSubstr` restituisce una porzione di una stringa tra gli indici iniziale e finale specificati.

**Sintassi**

```sql
{%= ampSubstr(string, startIndex, endIndex) %}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `string` | Stringa di origine. |
| `startIndex` | Indice iniziale della sottostringa (numero intero). |
| `endIndex` | Indice finale della sottostringa (numero intero). |

**Esempio**

L&#39;espressione seguente restituisce i primi cinque caratteri della stringa &quot;Hello World&quot;.

```sql
{%= ampSubstr("Hello World", 0, 5) %}
```

Restituisce `Hello`.

### Confronta con{#compare-to}

La funzione `compareTo` confronta due stringhe lessicograficamente. Restituisce un numero intero negativo se la prima stringa precede la seconda, zero se è uguale o un numero intero positivo se la prima stringa è successiva alla seconda.

**Sintassi**

```sql
{%= compareTo(string1, string2) %}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `string1` | Prima stringa da confrontare. |
| `string2` | Seconda stringa da confrontare. |

**Esempio**

```sql
{%= compareTo("apple", "banana") %}
```
