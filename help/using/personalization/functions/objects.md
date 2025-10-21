---
title: Libreria funzioni oggetti
description: Libreria funzioni oggetti
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 6ce70e32-aac3-4a2c-bfeb-c370521853ca
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 7%

---

# Funzioni oggetto {#objects}

## È nullo{#isNull}

La funzione `isNull` determina se un riferimento a un oggetto non esiste.

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

La funzione `isNotNull` determina se esiste un riferimento a un oggetto.

**Sintassi**

```sql
{%= isNotNull(object) %}
```

**Esempio**

L&#39;operazione seguente verifica se l&#39;indirizzo dell&#39;abitazione della persona esiste.

```sql
{%= isNotNull(person.homeAddress) %}
```
