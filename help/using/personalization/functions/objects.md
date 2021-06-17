---
title: Libreria di funzioni per oggetti
description: Libreria di funzioni per oggetti
feature: Personalizzazione
topic: Personalizzazione
role: Data Engineer
level: Experienced
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 10%

---

# Funzioni oggetto {#objects}

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
