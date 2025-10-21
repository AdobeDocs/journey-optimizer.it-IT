---
title: Libreria di funzioni di aggregazione
description: Libreria di funzioni di aggregazione
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: a029f716-ea1e-4d79-82b7-59770f05161b
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 9%

---

# Funzioni di aggregazione {#aggregation}

Le funzioni di aggregazione vengono utilizzate per raggruppare più valori in modo da formare un unico valore di riepilogo.

## Medio{#average}

La funzione `average` restituisce la media aritmetica di tutti i valori selezionati all&#39;interno dell&#39;array.

**Sintassi**

```sql
{%= average(array) %}
```

**Esempio**

L&#39;operazione seguente restituisce il prezzo medio di tutti gli ordini.

```sql
{%=average(orders.order.price)%}
```

## Count{#count}

La funzione `count` restituisce il numero di elementi all&#39;interno dell&#39;array specificato.

**Sintassi**

```sql
{%= count(array) %}
```

**Esempio**

L&#39;operazione seguente restituisce il numero di ordini nell&#39;array.

```sql
{%= count(orders) %}
```

## Massimo{#max}

La funzione `max` restituisce il più grande di tutti i valori selezionati all&#39;interno dell&#39;array.

**Sintassi**

```sql
{%= max(array) %}
```

**Esempio**

L&#39;operazione seguente restituisce il prezzo più alto di tutti gli ordini.

```sql
{%=max(orders.order.price)%}
```

## Minimo{#min}

La funzione `min` restituisce il più piccolo di tutti i valori selezionati all&#39;interno dell&#39;array.

**Sintassi**

```sql
{%= min(array) %}
```

**Esempio**

L&#39;operazione seguente restituisce il prezzo più basso di tutti gli ordini.

```sql
{%=min(orders.order.price) %}
```

## Sum{#sum}

La funzione `sum` restituisce la somma di tutti i valori selezionati all&#39;interno dell&#39;array.

**Sintassi**

```sql
{%= sum(array) %}
```

**Esempio**

L&#39;operazione seguente restituisce la somma di tutti i prezzi degli ordini.

```sql
{%=sum(orders.order.price)%}
```
