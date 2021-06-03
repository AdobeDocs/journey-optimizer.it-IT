---
title: Libreria funzioni
description: Libreria funzioni
source-git-commit: cd1b07bbb4b247d1d8c0cc87be9e4bdad22377ed
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 6%

---

# Funzioni aritmetiche {#maths}

![](../../assets/do-not-localize/badge.png)

Le funzioni aritmetiche vengono utilizzate per eseguire calcoli di base sui valori.

## Add{#add}

La funzione `+` (addizione) viene utilizzata per trovare la somma di due espressioni di argomento.

**Formato**

```sql
{%= double + double %}
```

**Esempio**

L&#39;operazione seguente è pari al prezzo di due prodotti diversi.

```sql
{%= product1.price + product2.price %}
```

## Moltiplica{#multiply}

La funzione `*` (moltiplicazione) viene utilizzata per trovare il prodotto di due espressioni di argomento.

**Formato**

```sql
{%= double * double %}
```

**Esempio**

L&#39;operazione seguente individua il prodotto dell&#39;inventario e il prezzo di un prodotto per trovare il valore lordo del prodotto.

```sql
{%= product.inventory * product.price %}
```

## Sottrai{#substract}

La funzione `-` (sottrazione) viene utilizzata per trovare la differenza tra due espressioni di argomento.

**Formato**

```sql
{%= double - double %}
```

**Esempio**

L&#39;operazione seguente individua la differenza di prezzo tra due prodotti diversi.

```sql
{%= product1.price - product2.price %}
```

## Dividi{#divide}

La funzione `/` (divisione) viene utilizzata per trovare il quoziente di due espressioni di argomento.

**Formato**

```sql
{%= double / double %}
```

**Esempio**

L&#39;operazione seguente trova il quoziente tra il totale dei prodotti venduti e il totale del denaro guadagnato per vedere il costo medio per articolo.

```sql
{%= totalProduct.price / totalProduct.sold %}
```

## Resto{#remainder}

La funzione `%` (modulo/rest) viene utilizzata per trovare il resto dopo aver diviso le due espressioni di argomento.

**Formato**

```sql
{%= double % double %}
```

**Esempio**

L&#39;operazione seguente verifica se l&#39;età della persona è divisibile per cinque anni.

```sql
{%= person.age % 5 = 0 %}
```
