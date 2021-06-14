---
title: Mappa la libreria delle funzioni
description: Mappa la libreria delle funzioni
feature: Personalizzazione
topic: Personalizzazione
role: Data Engineer
level: Experienced
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 7%

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
