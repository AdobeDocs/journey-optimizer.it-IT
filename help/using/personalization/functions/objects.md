---
title: Libreria di funzioni per oggetti
description: Libreria di funzioni per oggetti
feature: Personalizzazione
topic: Personalizzazione
role: Data Engineer
level: Experienced
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 10%

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
