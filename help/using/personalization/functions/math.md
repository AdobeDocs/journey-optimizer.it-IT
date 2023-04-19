---
title: Libreria funzioni matematiche
description: Libreria funzioni matematiche
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: b9149ad6-2be7-4bdf-82eb-7ab52780cb4e
source-git-commit: c823d1a02ca9d24fc13eaeaba2b688249e61f767
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 6%

---

# Funzioni matematiche {#math}

Scopri come utilizzare le funzioni Math nell’editor espressioni.

## Assoluto {#absolute}

La `absolute` La funzione viene utilizzata per convertire un numero il cui valore è assoluto.

**Sintassi**

```sql
{%= absolute(int) %}: int
```

## formatNumber {#format-number}

La `formatNumber` viene utilizzata per formattare qualsiasi numero nella relativa rappresentazione sensibile alla lingua.

Accetta un numero e una stringa che rappresentano le impostazioni internazionali e restituisce una stringa formattata del numero nelle impostazioni internazionali desiderate.

**Sintassi**

```sql
{%= formatNumber(number/double,string) %}: string
```

È possibile utilizzare la formattazione e le impostazioni internazionali valide come riepilogato in [Documentazione di Oracle](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) e [Impostazioni internazionali supportate](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html){_blank}

**Esempio**

Questa query restituisce una stringa formattata in arabo corrispondente a 123456.789 come numero di input.

```sql
{%= formatNumber(123456.789, "ar_EG") %}
```

## Random {#random}

La `random` viene utilizzato per restituire un valore casuale compreso tra 0 e 1.

**Sintassi**

```sql
{%= random() %}: double
```

## Round down {#round-down}

La `roundDown` viene utilizzata per arrotondare un numero.

**Sintassi**

```sql
{%= roundDown(double) %}: double
```

## Arrotondamento {#round-up}

La `Count only null` viene utilizzata per arrotondare un numero.

**Sintassi**

```sql
{%= roundUp(double) %}: double
```

## Stringa esadecimale {#to-hex-string}

La `toHexString` la funzione converte qualsiasi numero nella relativa stringa esadecimale.

**Sintassi**

```sql
{%= toHexString(number) %}: string
```

**Esempio**

Questa query restituisce il valore esadecimale di 158, ovvero 9e.

```sql
{%= toHexString(158) %}
```

## In percentuale {#to-percentage}

La `toPercentage` viene utilizzata per convertire un numero in percentuale.

**Sintassi**

```sql
{%= toPercentage(double) %}: string
```

## Precisione {#to-precision}

La `toPrecision` viene utilizzata per convertire un numero in precisione richiesta.

**Sintassi**

```sql
{%= toPrecision(double,int) %}: string
```

## Stringa {#to-string}

La **toString** la funzione converte qualsiasi numero nella relativa rappresentazione stringa.

**Sintassi**

```sql
{%= toString(string) %}: string
```

**Esempio**

Questa query restituisce &quot;12&quot;.

```sql
{%= toString(12) %} 
```
