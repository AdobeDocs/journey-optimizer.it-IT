---
title: Libreria funzioni aritmetiche
description: Libreria funzioni aritmetiche
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 21ef8f50-8389-4675-a8e5-0438a3eee592
TQID: https://experienceleague.adobe.com/vQcfLG40Xhz4-ebm--J875oU4o-6BXC0SvNq24OOyTk
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 180
ht-degree: 7%

---

# Funzioni aritmetiche {#maths}

Le funzioni aritmetiche vengono utilizzate per eseguire calcoli di base sui valori.

## Add{#add}

La funzione `+` (addizione) viene utilizzata per trovare la somma di due espressioni di argomento.

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

La funzione `*` (moltiplicazione) viene utilizzata per trovare il prodotto di due espressioni di argomento.

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

La funzione `-` (sottrazione) viene utilizzata per trovare la differenza tra due espressioni di argomento.

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

La funzione `/` (divisione) viene utilizzata per trovare il quoziente di due espressioni di argomento.

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

La funzione `%` (modulo/resto) viene utilizzata per trovare il resto dopo aver diviso le due espressioni di argomento.

**Sintassi**

```sql
{%= double % double %}
```

**Esempio**

L’operazione seguente verifica se l’età della persona è divisibile di cinque.

```sql
{%= person.age % 5 = 0 %}
```
