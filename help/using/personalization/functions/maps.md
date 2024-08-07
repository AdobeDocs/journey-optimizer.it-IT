---
title: Libreria funzioni mappe
description: Libreria funzioni mappe
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: de6a8da2-55cf-4105-ba93-40c556732626
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 8%

---

# Funzioni mappe{#maps}

Utilizza le funzioni Mappa nella personalizzazione per semplificare l’interazione con le mappe.

## Ottieni{#get}

La funzione `get` viene utilizzata per recuperare il valore di una mappa per una determinata chiave.

**Sintassi**

```sql
{%= get(map, string) %}
```

**Esempio**

L&#39;operazione seguente ottiene il valore della mappa di identità per la chiave `example@example.com`.

```sql
{%= get(identityMap,"example@example.com") %}
```

## Chiavi{#keys}

La funzione `keys` viene utilizzata per recuperare tutte le chiavi per una determinata mappa.

**Sintassi**

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

**Sintassi**

```sql
{%= values(map) %}
```

**Esempio**

L&#39;operazione seguente ottiene tutti i valori per la mappa `identityMap`.

```sql
{%= values(identityMap) %}
```
