---
title: Libreria funzioni
description: Libreria funzioni
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 9%

---

# Operatori {#operators}

![](../../assets/do-not-localize/badge.png)

## E

La funzione `and` viene utilizzata per creare una congiunzione logica.

**Formato**

```sql
{QUERY} and {QUERY}
```

**Esempio**

La seguente query PQL restituirà tutte le persone con il paese di origine come Canada e l&#39;anno di nascita del 1985.

```sql
homeAddress.countryISO = "CA" and person.birthYear = 1985
```

## Oppure

La funzione `or` viene utilizzata per creare una disgiunzione logica.

**Formato**

```sql
{QUERY} or {QUERY}
```

**Esempio**

La seguente query PQL restituirà tutte le persone con il paese di origine come Canada o l&#39;anno di nascita del 1985.

```sql
homeAddress.countryISO = "CA" or person.birthYear = 1985
```

## Non

La funzione `not` (o `!`) viene utilizzata per creare una negazione logica.

**Formato**

```sql
not ({QUERY})
!({QUERY})
```

**Esempio**

La seguente query PQL restituirà tutte le persone che non hanno il proprio paese di origine come Canada.

```sql
not (homeAddress.countryISO = "CA")
```

## Se

La funzione `if` viene utilizzata per risolvere un&#39;espressione a seconda che una condizione specificata sia vera o meno.

**Formato**

```sql
if ({TEST_EXPRESSION}, {TRUE_EXPRESSION}, {FALSE_EXPRESSION})
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{TEST_EXPRESSION}` | Espressione booleana in fase di test. |
| `{TRUE_EXPRESSION}` | L&#39;espressione il cui valore verrà utilizzato se `{TEST_EXPRESSION}` è true. |
| `{FALSE_EXPRESSION}` | L&#39;espressione il cui valore verrà utilizzato se `{TEST_EXPRESSION}` è false. |

**Esempio**

La seguente query PQL imposta il valore come `1` se il paese di origine è Canada e `2` se il paese di origine non è Canada.

```sql
if (homeAddress.countryISO = "CA", 1, 2)
```

## È uguale a

La funzione `=` (equals) controlla se un valore o un&#39;espressione è uguale a un altro valore o espressione.

**Formato**

```sql
{EXPRESSION} = {VALUE}
```

**Esempio**

La seguente query PQL controlla se il paese dell&#39;indirizzo di origine è in Canada.

```sql
homeAddress.countryISO = "CA"
```

## Non uguale

La funzione `!=` (non uguale) controlla se un valore o un&#39;espressione è **non** uguale a un altro valore o espressione.

**Formato**

```sql
{EXPRESSION} != {VALUE}
```

**Esempio**

La seguente query PQL controlla se il paese dell&#39;indirizzo di origine non è in Canada.

```sql
homeAddress.countryISO != "CA"
```

## Maggiore di

La funzione `>` (maggiore di) viene utilizzata per verificare se il primo valore è maggiore del secondo valore.

**Formato**

```sql
{EXPRESSION} > {EXPRESSION} 
```

**Esempio**

La seguente query PQL definisce le persone i cui compleanni non rientrano in gennaio o febbraio.

```sql
person.birthMonth > 2
```

## Maggiore o uguale a

La funzione `>=` (maggiore o uguale a) viene utilizzata per verificare se il primo valore è maggiore o uguale al secondo valore.

**Formato**

```sql
{EXPRESSION} >= {EXPRESSION} 
```

**Esempio**

La seguente query PQL definisce le persone i cui compleanni non rientrano in gennaio o febbraio.

```sql
person.birthMonth >= 3
```

## Minore di

La funzione di confronto `<` (minore di) viene utilizzata per verificare se il primo valore è minore del secondo valore.

**Formato**

```sql
{EXPRESSION} < {EXPRESSION} 
```

**Esempio**

La seguente query PQL definisce le persone il cui compleanno è a gennaio.

```sql
person.birthMonth < 2
```

## Minore o uguale a

La funzione di confronto `<=` (minore o uguale a) viene utilizzata per verificare se il primo valore è minore o uguale al secondo valore.

**Formato**

```sql
{EXPRESSION} <= {EXPRESSION} 
```

**Esempio**

La seguente query PQL definisce le persone il cui compleanno è in gennaio o febbraio.

```sql
person.birthMonth <= 2
```

## Add

La funzione `+` (addizione) viene utilizzata per trovare la somma di due espressioni di argomento.

**Formato**

```sql
{NUMBER} + {NUMBER}
```

**Esempio**

La seguente query PQL somma il prezzo di due prodotti diversi.

```sql
product1.price + product2.price
```

## Moltiplica

La funzione `*` (moltiplicazione) viene utilizzata per trovare il prodotto di due espressioni di argomento.

**Formato**

```sql
{NUMBER} * {NUMBER}
```

**Esempio**

La seguente query PQL individua il prodotto dell&#39;inventario e il prezzo di un prodotto per trovare il valore lordo del prodotto.

```sql
product.inventory * product.price
```

## Sottrai

La funzione `-` (sottrazione) viene utilizzata per trovare la differenza tra due espressioni di argomento.

**Formato**

```sql
{NUMBER} - {NUMBER}
```

**Esempio**

La seguente query PQL trova la differenza di prezzo tra due prodotti diversi.

```sql
product1.price - product2.price
```

## Dividi

La funzione `/` (divisione) viene utilizzata per trovare il quoziente di due espressioni di argomento.

**Formato**

```sql
{NUMBER} / {NUMBER}
```

**Esempio**

La seguente query PQL trova il quoziente tra il totale dei prodotti venduti e il totale del denaro guadagnato per vedere il costo medio per articolo.

```sql
totalProduct.price / totalProduct.sold
```

## Resto

La funzione `%` (modulo/rest) viene utilizzata per trovare il resto dopo aver diviso le due espressioni di argomento.

**Formato**

```sql
{NUMBER} % {NUMBER}
```

**Esempio**

La seguente query PQL controlla se l&#39;età della persona è divisibile per cinque anni.

```sql
person.age % 5 = 0
```
