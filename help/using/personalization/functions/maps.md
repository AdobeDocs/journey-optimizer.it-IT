---
title: Libreria funzioni
description: Libreria funzioni
source-git-commit: 8c58dd667ea59a17833bbe3482b1a233ac2e28fe
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 6%

---

# Funzioni Mappe{#maps}

![](../../assets/do-not-localize/badge.png)

[!DNL Profile Query Language] (PQL) offre funzioni che facilitano l’interazione con le mappe.

## Get{#get}

La funzione `get` viene utilizzata per recuperare il valore di una mappa per una determinata chiave.

**Formato**

```sql
{%= get(map, string) %}
```

**Esempio**

L&#39;operazione seguente ottiene il valore della mappa di identità per la chiave `example@example.com`.

```sql
{%= get(identityMap,"example@example.com") %}
```

## Chiavi{#keys}

La funzione `keys` viene utilizzata per recuperare tutte le chiavi di una determinata mappa.

**Formato**

```sql
{%= keys(map) %}
```

**Esempio**

L&#39;operazione seguente ottiene tutte le chiavi per la mappa `identityMap`.

```sql
{%= keys(identityMap) %}
```

## Valori{#values}

La funzione `values` viene utilizzata per recuperare tutti i valori di una determinata mappa.

**Formato**

```sql
{%= values(map) %}
```

**Esempio**

L&#39;operazione seguente ottiene tutti i valori della mappa `identityMap`.

```sql
{%= values(identityMap) %}
```
