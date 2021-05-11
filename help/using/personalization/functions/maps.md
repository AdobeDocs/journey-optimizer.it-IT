---
title: Libreria funzioni
description: Libreria funzioni
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 5%

---

# Funzioni Mappe {#maps}

![](../../assets/do-not-localize/badge.png)

[!DNL Profile Query Language] (PQL) offre funzioni che facilitano l’interazione con le mappe.

## Get

La funzione `get` viene utilizzata per recuperare il valore di una mappa per una determinata chiave.

**Formato**

```sql
get({MAP},{STRING})
```

**Esempio**

La seguente query PQL ottiene il valore della mappa di identità per la chiave `example@example.com`.

```sql
get(identityMap,"example@example.com")
```

## Chiavi

La funzione `keys` viene utilizzata per recuperare tutte le chiavi di una determinata mappa.

**Formato**

```sql
keys({MAP})
```

**Esempio**

La seguente query PQL ottiene tutte le chiavi per la mappa `identityMap`.

```sql
keys(identityMap)
```

## Valori

La funzione `values` viene utilizzata per recuperare tutti i valori di una determinata mappa.

**Formato**

```sql
values({MAP})
```

**Esempio**

La seguente query PQL ottiene tutti i valori per la mappa `identityMap`.

```sql
values(identityMap)
```
