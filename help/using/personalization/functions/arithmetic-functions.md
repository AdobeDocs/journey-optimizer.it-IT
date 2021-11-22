---
title: Libreria funzioni aritmetiche
description: Libreria funzioni aritmetiche
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 21ef8f50-8389-4675-a8e5-0438a3eee592
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 7%

---

# Funzioni aritmetiche {#maths}

Le funzioni aritmetiche vengono utilizzate per eseguire calcoli di base sui valori.

## Add{#add}

La `+` (aggiunta) viene utilizzata per trovare la somma di due espressioni di argomento.

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

La `*` (moltiplicazione) viene utilizzata per trovare il prodotto di due espressioni di argomento.

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

La `-` (sottrazione) viene utilizzata per trovare la differenza tra due espressioni di argomento.

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

La `/` (divisione) viene utilizzato per trovare il quoziente di due espressioni di argomento.

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

La `%` (modulo/rest) viene utilizzato per trovare il resto dopo aver diviso le due espressioni di argomento.

**Formato**

```sql
{%= double % double %}
```

**Esempio**

L&#39;operazione seguente verifica se l&#39;età della persona è divisibile per cinque anni.

```sql
{%= person.age % 5 = 0 %}
```
