---
title: Mappa la libreria delle funzioni
description: Mappa la libreria delle funzioni
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: de6a8da2-55cf-4105-ba93-40c556732626
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 6%

---

# Funzioni Mappe{#maps}

Utilizza le funzioni Mappa nella personalizzazione per semplificare l’interazione con le mappe.

## Ottenere{#get}

La `get` viene utilizzata per recuperare il valore di una mappa per una determinata chiave.

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

La `keys` viene utilizzata per recuperare tutte le chiavi di una determinata mappa.

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

La `values` viene utilizzata per recuperare tutti i valori di una data mappa.

**Sintassi**

```sql
{%= values(map) %}
```

**Esempio**

L&#39;operazione seguente ottiene tutti i valori per la mappa `identityMap`.

```sql
{%= values(identityMap) %}
```
