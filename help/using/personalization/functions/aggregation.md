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
ht-degree: 7%

---

# Funzioni di aggregazione {#aggregation}

Le funzioni di aggregazione vengono utilizzate per raggruppare più valori in modo da formare un unico valore di riepilogo.

## Medio{#average}

Il `average` La funzione restituisce la media aritmetica di tutti i valori selezionati all’interno dell’array.

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

Il `count` La funzione restituisce il numero di elementi all’interno dell’array specificato.

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

Il `max` restituisce il più grande di tutti i valori selezionati all’interno dell’array.

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

Il `min` La funzione restituisce il più piccolo di tutti i valori selezionati all’interno dell’array.

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

Il `sum` restituisce la somma di tutti i valori selezionati all’interno dell’array.

**Sintassi**

```sql
{%= sum(array) %}
```

**Esempio**

L&#39;operazione seguente restituisce la somma di tutti i prezzi degli ordini.

```sql
{%=sum(orders.order.price)%}
```
