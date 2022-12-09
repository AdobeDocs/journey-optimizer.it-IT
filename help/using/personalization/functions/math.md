---
title: Libreria funzioni matematiche
description: Libreria funzioni matematiche
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---

# Funzioni matematiche {#math}

Scopri come utilizzare le funzioni Math nell’editor espressioni.

## Assoluto {#absolute}

La `absolute` La funzione viene utilizzata per convertire un numero il cui valore è assoluto.

**Formato**

```sql
{%= absolute(int) %}: int
```

## Casuale {#random}

La `random` viene utilizzato per restituire un valore casuale compreso tra 0 e 1.

**Formato**

```sql
{%= random() %}: double
```

## Round down {#round-down}

La `roundDown` viene utilizzata per arrotondare un numero.

**Formato**

```sql
{%= roundDown(double) %}: double
```

## Arrotondamento {#round-up}

La `Count only null` viene utilizzata per arrotondare un numero.

**Formato**

```sql
{%= roundUp(double) %}: double
```

## In percentuale {#to-percentage}

La `toPercentage` viene utilizzata per convertire un numero in percentuale.

**Formato**

```sql
{%= toPercentage(double) %}: string
```

## Precisione {#to-precision}

La `toPrecision` viene utilizzata per convertire un numero in precisione richiesta.

**Formato**

```sql
{%= toPrecision(double,int) %}: string
```
