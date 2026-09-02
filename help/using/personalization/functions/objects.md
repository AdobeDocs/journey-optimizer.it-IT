---
title: Libreria funzioni oggetti
description: Libreria funzioni oggetti
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 6ce70e32-aac3-4a2c-bfeb-c370521853ca
TQID: https://experienceleague.adobe.com/EdvzBXdtv1Mm4yIZ8ehu4tx6uQBxnpcXTMVQIc1oQkI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2: []
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 57
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
