---
title: Libreria funzioni
description: Libreria funzioni
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 7%

---

# Funzioni di aggregazione {#aggregation}

![](../../assets/do-not-localize/badge.png)

Le funzioni di aggregazione vengono utilizzate per raggruppare più valori all&#39;interno di array [!DNL Profile Query Language] (PQL) per formare un singolo valore di riepilogo.

## Conteggio

La funzione `count` restituisce il numero di elementi all&#39;interno della matrice specificata.

**Formato**

```sql
count({ARRAY})
```

**Esempio**

La seguente query PQL restituisce il numero di ordini nell&#39;array.

```sql
count(orders)
```

## Somma

La funzione `sum` restituisce la somma di tutti i valori selezionati all&#39;interno della matrice.

**Formato**

```sql
sum({ARRAY})
```

**Esempio**

La seguente query PQL restituisce la somma di tutti i prezzi degli ordini.

```sql
sum(orders.order.price)
```

## Medio

La funzione `average` restituisce la media aritmetica di tutti i valori selezionati all&#39;interno della matrice.

**Formato**

```sql
average({ARRAY})
```

**Esempio**

La seguente query PQL restituisce il prezzo medio di tutti gli ordini.

```sql
average(orders.order.price)
```

## Minimo

La funzione `min` restituisce il valore più piccolo tra tutti i valori selezionati all&#39;interno dell&#39;array.

**Formato**

```sql
min({ARRAY})
```

**Esempio**

La seguente query PQL restituisce il prezzo più basso di tutti gli ordini.

```sql
min(orders.order.price)
```

## Massimo

La funzione `max` restituisce il valore più grande tra tutti i valori selezionati all&#39;interno dell&#39;array.

**Formato**

```sql
max({ARRAY})
```

**Esempio**

La seguente query PQL restituisce il prezzo più alto di tutti gli ordini.

```sql
max(orders.order.price)
```
