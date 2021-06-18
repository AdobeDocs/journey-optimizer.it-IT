---
title: Libreria di funzioni di aggregazione
description: Libreria di funzioni di aggregazione
feature: Personalizzazione
topic: Personalizzazione
role: Data Engineer
level: Experienced
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 9%

---

# Funzioni di aggregazione {#aggregation}

Le funzioni di aggregazione vengono utilizzate per raggruppare più valori per formare un singolo valore di riepilogo.

## Conteggio{#count}

La funzione `count` restituisce il numero di elementi all&#39;interno della matrice specificata.

**Formato**

```sql
{%= count(array) %}
```

**Esempio**

L&#39;operazione seguente restituisce il numero di ordini nell&#39;array.

```sql
{%= count(orders) %}
```

## Somma{#sum}

La funzione `sum` restituisce la somma di tutti i valori selezionati all&#39;interno della matrice.

**Formato**

```sql
{%= sum(array) %}
```

**Esempio**

L&#39;operazione seguente restituisce la somma di tutti i prezzi degli ordini.

```sql
{%=sum(orders.order.price)%}
```

## Medio{#average}

La funzione `average` restituisce la media aritmetica di tutti i valori selezionati all&#39;interno della matrice.

**Formato**

```sql
{%= average(array) %}
```

**Esempio**

L&#39;operazione seguente restituisce il prezzo medio di tutti gli ordini.

```sql
{%=average(orders.order.price)%}
```

## Minimo{#min}

La funzione `min` restituisce il valore più piccolo tra tutti i valori selezionati all&#39;interno dell&#39;array.

**Formato**

```sql
{%= min(array) %}
```

**Esempio**

L&#39;operazione seguente restituisce il prezzo più basso di tutti gli ordini.

```sql
{%=min(orders.order.price)%}
```

## Massimo{#max}

La funzione `max` restituisce il valore più grande tra tutti i valori selezionati all&#39;interno dell&#39;array.

**Formato**

```sql
{%= max(array) %}
```

**Esempio**

L&#39;operazione seguente restituisce il prezzo più alto di tutti gli ordini.

```sql
{%=max(orders.order.price)%}
```
