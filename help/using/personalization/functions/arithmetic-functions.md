---
title: Libreria funzioni aritmetiche
description: Libreria funzioni aritmetiche
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 21ef8f50-8389-4675-a8e5-0438a3eee592
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 7%

---

# Funzioni aritmetiche {#maths}

Le funzioni aritmetiche vengono utilizzate per eseguire calcoli di base sui valori.

## Add{#add}

Il `+` (addizione) viene utilizzata per trovare la somma di due espressioni di argomento.

**Sintassi**

```sql
{%= double + double %}
```

**Esempio**

L&#39;operazione seguente somma il prezzo di due prodotti diversi.

```sql
{%= product1.price + product2.price %}
```

## Moltiplica{#multiply}

Il `*` (moltiplicazione) viene utilizzata per trovare il prodotto di due espressioni di argomento.

**Sintassi**

```sql
{%= double * double %}
```

**Esempio**

L&#39;operazione seguente individua il prodotto dell&#39;inventario e il prezzo di un prodotto per trovare il valore lordo del prodotto.

```sql
{%= product.inventory * product.price %}
```

## Sottrai{#substract}

Il `-` (sottrazione) viene utilizzata per trovare la differenza tra due espressioni di argomento.

**Sintassi**

```sql
{%= double - double %}
```

**Esempio**

L&#39;operazione seguente rileva la differenza di prezzo tra due prodotti diversi.

```sql
{%= product1.price - product2.price %}
```

## Dividi{#divide}

Il `/` (divisione) viene utilizzata per trovare il quoziente di due espressioni di argomento.

**Sintassi**

```sql
{%= double / double %}
```

**Esempio**

L&#39;operazione seguente consente di trovare il quoziente tra il totale dei prodotti venduti e il totale del denaro guadagnato per visualizzare il costo medio per articolo.

```sql
{%= totalProduct.price / totalProduct.sold %}
```

## Rimanente{#remainder}

Il `%` (modulo/resto) viene utilizzata per trovare il resto dopo aver diviso le due espressioni di argomento.

**Sintassi**

```sql
{%= double % double %}
```

**Esempio**

L’operazione seguente verifica se l’età della persona è divisibile di cinque.

```sql
{%= person.age % 5 = 0 %}
```
