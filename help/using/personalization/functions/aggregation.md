---
title: Libreria di funzioni di aggregazione
description: Libreria di funzioni di aggregazione
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: a029f716-ea1e-4d79-82b7-59770f05161b
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 8%

---

# Funzioni di aggregazione {#aggregation}

Le funzioni di aggregazione vengono utilizzate per raggruppare più valori per formare un singolo valore di riepilogo.

## Medio{#average}

La `average` restituisce la media aritmetica di tutti i valori selezionati all&#39;interno dell&#39;array.

**Sintassi**

```sql
{%= average(array) %}
```

**Esempio**

L&#39;operazione seguente restituisce il prezzo medio di tutti gli ordini.

```sql
{%=average(orders.order.price)%}
```

## Conteggio{#count}

La `count` restituisce il numero di elementi all&#39;interno della matrice specificata.

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

La `max` restituisce il valore più grande tra tutti i valori selezionati all&#39;interno dell&#39;array.

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

La `min` restituisce il valore più piccolo tra tutti i valori selezionati all&#39;interno della matrice.

**Sintassi**

```sql
{%= min(array) %}
```

**Esempio**

L&#39;operazione seguente restituisce il prezzo più basso di tutti gli ordini.

```sql
{%=min(orders.order.price) %}
```

## Somma{#sum}

La `sum` restituisce la somma di tutti i valori selezionati all&#39;interno della matrice.

**Sintassi**

```sql
{%= sum(array) %}
```

**Esempio**

L&#39;operazione seguente restituisce la somma di tutti i prezzi degli ordini.

```sql
{%=sum(orders.order.price)%}
```
