---
title: Libreria funzioni
description: Libreria funzioni
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 7%

---

# Funzioni oggetto {#objects}

![](../../assets/do-not-localize/badge.png)

## È nullo

La funzione `isNull` determina se un riferimento a un oggetto non esiste.

**Formato**

```sql
isNull({OBJECT})
```

**Esempio**

La seguente query PQL controlla se l&#39;indirizzo di origine della persona non esiste.

```sql
isNull(person.homeAddress)
```

## Non è Null

La funzione `isNotNull` determina se esiste un riferimento a un oggetto.

**Formato**

```sql
isNotNull({OBJECT})
```

**Esempio**

La seguente query PQL controlla se l&#39;indirizzo di casa della persona esiste.

```sql
isNotNull(person.homeAddress)
```
