---
title: Libreria funzioni
description: Libreria funzioni
source-git-commit: 8c58dd667ea59a17833bbe3482b1a233ac2e28fe
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 7%

---

# Funzioni oggetto {#objects}

![](../../assets/do-not-localize/badge.png)

## È nullo{#isNull}

La funzione `isNull` determina se un riferimento a un oggetto non esiste.

**Formato**

```sql
{%= isNull(object) %}
```

**Esempio**

L&#39;operazione seguente verifica se l&#39;indirizzo di origine della persona non esiste.

```sql
{%= isNull(person.homeAddress) %}
```

## Non è Null{#isNotNull}

La funzione `isNotNull` determina se esiste un riferimento a un oggetto.

**Formato**

```sql
{%= isNotNull(object) %}
```

**Esempio**

L&#39;operazione seguente controlla se l&#39;indirizzo di origine della persona esiste.

```sql
{%= isNotNull(person.homeAddress) %}
```
