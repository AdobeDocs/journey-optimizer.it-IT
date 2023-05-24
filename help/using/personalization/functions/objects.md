---
title: Libreria funzioni oggetti
description: Libreria funzioni oggetti
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 6ce70e32-aac3-4a2c-bfeb-c370521853ca
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 7%

---

# Funzioni oggetto {#objects}

## È nullo{#isNull}

Il `isNull` determina se un riferimento a un oggetto non esiste.

**Sintassi**

```sql
{%= isNull(object) %}
```

**Esempio**

L&#39;operazione seguente verifica se l&#39;indirizzo dell&#39;abitazione della persona non esiste.

```sql
{%= isNull(person.homeAddress) %}
```

## Non è nullo{#isNotNull}

Il `isNotNull` determina se esiste un riferimento a un oggetto.

**Sintassi**

```sql
{%= isNotNull(object) %}
```

**Esempio**

L&#39;operazione seguente verifica se l&#39;indirizzo dell&#39;abitazione della persona esiste.

```sql
{%= isNotNull(person.homeAddress) %}
```
