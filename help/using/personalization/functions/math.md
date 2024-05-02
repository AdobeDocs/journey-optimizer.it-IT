---
title: Libreria di funzioni matematiche
description: Libreria di funzioni matematiche
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: b9149ad6-2be7-4bdf-82eb-7ab52780cb4e
source-git-commit: 0571a11eabffeb5e318bebe341a8df18da7db598
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 6%

---

# Funzioni matematiche {#math}

Scopri come utilizzare le funzioni matematiche nell’editor di espressioni.

## Assoluto {#absolute}

Il `absolute` funzione viene utilizzata per convertire un numero in valore assoluto.

**Sintassi**

```sql
{%= absolute(int) %}: int
```

## formatNumber {#format-number}

Il `formatNumber` La funzione viene utilizzata per formattare qualsiasi numero nella relativa rappresentazione sensibile alla lingua.

Accetta un numero e una stringa che rappresenta la lingua e restituisce una stringa formattata del numero nella lingua desiderata.

**Sintassi**

```sql
{%= formatNumber(number/double,string) %}: string
```

È possibile utilizzare la formattazione e le lingue valide come riepilogato in [Documentazione di Oracle](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) e [Impostazioni internazionali supportate](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html){_blank}

**Esempio**

Questa query restituisce come numero di input una stringa formattata in arabo corrispondente a 123456,789.

```sql
{%= formatNumber(123456.789, "ar_EG") %}
```

## Casuale {#random}

Il `random` viene utilizzata per restituire un valore casuale compreso tra 0 e 1.

**Sintassi**

```sql
{%= random() %}: double
```

## Arrotonda per difetto {#round-down}

Il `roundDown` viene utilizzata per arrotondare un numero per difetto.

**Sintassi**

```sql
{%= roundDown(double) %}: double
```

## Arrotonda per eccesso {#round-up}

Il `Count only null` funzione viene utilizzato per arrotondare un numero.

**Sintassi**

```sql
{%= roundUp(double) %}: double
```

## Alla stringa esadecimale {#to-hex-string}

Il `toHexString` funzione converte qualsiasi numero nella relativa stringa esadecimale.

**Sintassi**

```sql
{%= toHexString(number) %}: string
```

**Esempio**

Questa query restituisce il valore esadecimale 158, ovvero 9e.

```sql
{%= toHexString(158) %}
```

## A Intero {#to-int}

Il `toInt` La funzione viene utilizzata per convertire uno qualsiasi di questi tipi (number, double, int, long, float, short, byte, boolean, string) in un numero intero.

**Sintassi**

```sql
{%= toInt(<valueToConvert>) %}: integer
```

**Esempio**

Questa query restituisce il valore intero 42,6, ovvero 42.

```sql
{%= toInt(42.6) %}: integer
```

## A percentuale {#to-percentage}

Il `toPercentage` viene utilizzata per convertire un numero in percentuale.

**Sintassi**

```sql
{%= toPercentage(double) %}: string
```

## Alla precisione {#to-precision}

Il `toPrecision` viene utilizzata per convertire un numero con la precisione richiesta.

**Sintassi**

```sql
{%= toPrecision(double,int) %}: string
```

## A stringa {#to-string}

Il **toString** funzione converte qualsiasi numero nella sua rappresentazione di stringa.

**Sintassi**

```sql
{%= toString(string) %}: string
```

**Esempio**

Questa query restituisce &quot;12&quot;.

```sql
{%= toString(12) %} 
```
