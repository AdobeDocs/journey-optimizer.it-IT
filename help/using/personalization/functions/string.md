---
title: Libreria funzioni
description: Libreria funzioni
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 7%

---

# Funzioni stringa {#string}

![](../../assets/do-not-localize/badge.png)


Funzioni di TBC CJM String

## Simile

La funzione `like` viene utilizzata per determinare se una stringa corrisponde a un pattern specificato.

**Formato**

```sql
like ({STRING_1},{STRING_2})
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa da cui eseguire il controllo. |
| `{STRING_2}` | Espressione da confrontare con la prima stringa. Sono disponibili due caratteri speciali supportati per la creazione di un’espressione: `%` e `_`. <ul><li>`%` viene utilizzato per rappresentare zero o più caratteri.</li><li>`_` viene utilizzato per rappresentare esattamente un carattere.</li></ul> |

**Esempio**

La seguente query recupera tutte le città contenenti il pattern &quot;es&quot;.

```sql
like (city ,"%es%")
```

## Inizia con

La funzione `startsWith` viene utilizzata per determinare se una stringa inizia con una sottostringa specificata.

**Formato**

```sql
startsWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa da cui eseguire il controllo. |
| `{STRING_2}` | Stringa da cercare all’interno della prima stringa. |
| `{BOOLEAN}` | Un parametro facoltativo per determinare se il controllo è sensibile a maiuscole e minuscole. Per impostazione predefinita, è impostato su true. |

**Esempio**

La seguente query determina, con distinzione tra maiuscole e minuscole, se il nome della persona inizia con &quot;Joe&quot;.

```sql
startsWith(person.name,"Joe")
```

## Non inizia con

La funzione `doesNotStartWith` viene utilizzata per determinare se una stringa non inizia con una sottostringa specificata.

**Formato**

```sql
doesNotStartWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa da cui eseguire il controllo. |
| `{STRING_2}` | Stringa da cercare all’interno della prima stringa. |
| `{BOOLEAN}` | Un parametro facoltativo per determinare se il controllo è sensibile a maiuscole e minuscole. Per impostazione predefinita, è impostato su true. |

**Esempio**

La seguente query determina, con distinzione tra maiuscole e minuscole, se il nome della persona non inizia con &quot;Joe&quot;.

```sql
doesNotStartWith(person.name,"Joe")
```

## Termina con

La funzione `endsWith` viene utilizzata per determinare se una stringa termina con una sottostringa specificata.

**Formato**

```sql
endsWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa da cui eseguire il controllo. |
| `{STRING_2}` | Stringa da cercare all’interno della prima stringa. |
| `{BOOLEAN}` | Un parametro facoltativo per determinare se il controllo è sensibile a maiuscole e minuscole. Per impostazione predefinita, è impostato su true. |

**Esempio**

La seguente query determina, con distinzione tra maiuscole e minuscole, se l’indirizzo e-mail della persona termina con &quot;.com&quot;.

```sql
endsWith(person.emailAddress,".com")
```

## Non termina con

La funzione `doesNotEndWith` viene utilizzata per determinare se una stringa non termina con una sottostringa specificata.

**Formato**

```sql
doesNotEndWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa da cui eseguire il controllo. |
| `{STRING_2}` | Stringa da cercare all’interno della prima stringa. |
| `{BOOLEAN}` | Un parametro facoltativo per determinare se il controllo è sensibile a maiuscole e minuscole. Per impostazione predefinita, è impostato su true. |

**Esempio**

La seguente query determina, con distinzione tra maiuscole e minuscole, se l’indirizzo e-mail della persona non termina con &quot;.com&quot;.

```sql
doesNotEndWith(person.emailAddress,".com")
```

## Contains

La funzione `contains` viene utilizzata per determinare se una stringa contiene una sottostringa specificata.

**Formato**

```sql
contains({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa da cui eseguire il controllo. |
| `{STRING_2}` | Stringa da cercare all’interno della prima stringa. |
| `{BOOLEAN}` | Un parametro facoltativo per determinare se il controllo è sensibile a maiuscole e minuscole. Per impostazione predefinita, è impostato su true. |

**Esempio**

La seguente query determina, con distinzione tra maiuscole e minuscole, se l’indirizzo e-mail della persona contiene la stringa &quot;2010@gm&quot;.

```sql
contains(person.emailAddress,"2010@gm")
```

## Non contiene

La funzione `doesNotContain` viene utilizzata per determinare se una stringa non contiene una sottostringa specificata.

**Formato**

```sql
doesNotContain({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa da cui eseguire il controllo. |
| `{STRING_2}` | Stringa da cercare all’interno della prima stringa. |
| `{BOOLEAN}` | Un parametro facoltativo per determinare se il controllo è sensibile a maiuscole e minuscole. Per impostazione predefinita, è impostato su true. |

**Esempio**

La seguente query determina, con distinzione tra maiuscole e minuscole, se l’indirizzo e-mail della persona non contiene la stringa &quot;2010@gm&quot;.

```sql
doesNotContain(person.emailAddress,"2010@gm")
```

## È uguale a

La funzione `equals` viene utilizzata per determinare se una stringa è uguale alla stringa specificata.

**Formato**

```sql
equals({STRING_1},{STRING_2})
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa da cui eseguire il controllo. |
| `{STRING_2}` | Stringa da confrontare con la prima stringa. |

**Esempio**

La seguente query determina, con distinzione tra maiuscole e minuscole, se il nome della persona è &quot;John&quot;.

```sql
equals(person.name,"John")
```

## Non uguale a

La funzione `notEqualTo` viene utilizzata per determinare se una stringa non è uguale alla stringa specificata.

**Formato**

```sql
notEqualTo({STRING_1},{STRING_2})
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa da cui eseguire il controllo. |
| `{STRING_2}` | Stringa da confrontare con la prima stringa. |

**Esempio**

La seguente query determina, con distinzione tra maiuscole e minuscole, se il nome della persona non è &quot;John&quot;.

```sql
notEqualTo(person.name,"John")
```

## Corrisponde

La funzione `matches` viene utilizzata per determinare se una stringa corrisponde a una specifica espressione regolare. Fare riferimento a [questo documento](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) per ulteriori informazioni sui pattern corrispondenti nelle espressioni regolari.

**Formato**

```sql
matches({STRING_1},STRING_2})
```

**Esempio**

La seguente query determina, senza distinzione tra maiuscole e minuscole, se il nome della persona inizia con &quot;John&quot;.

```sql
matches(person.name.,"(?i)^John")
```

## Gruppo di espressioni regolari

La funzione `regexGroup` viene utilizzata per estrarre informazioni specifiche, in base all&#39;espressione regolare fornita.

**Formato**

```sql
regexGroup({STRING},{EXPRESSION})
```

**Esempio**

La seguente query viene utilizzata per estrarre il nome di dominio da un indirizzo e-mail.

```sql
regexGroup(emailAddress,"@(\w+)", 1)
```
