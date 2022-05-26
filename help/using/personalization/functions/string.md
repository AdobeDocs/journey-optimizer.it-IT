---
title: Libreria di funzioni stringa
description: Libreria di funzioni stringa
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 8674ef9e-261b-49d9-800e-367f9f7ef979
source-git-commit: b9ebacf410f268e19bbaf1d43ee98f5376d0913f
workflow-type: tm+mt
source-wordcount: '1237'
ht-degree: 7%

---

# Funzioni stringa {#string}

Scopri come utilizzare le funzioni String nell’editor espressioni.

## Cammello {#camelCase}

La `camelCase` la funzione maiuscola la prima lettera di ogni parola di una stringa.

**Formato**

```sql
{%= camelCase(string)%}
```

**Esempio**

La funzione seguente capitalizza la prima lettera di parola nell&#39;indirizzo della strada del profilo.

```sql
{%= camelCase(profile.homeAddress.street) %}
```

## Concat {#concate}

La `concat` la funzione combina due stringhe in una.

**Formato**

```sql
{%= concat(string,string) %}
```

**Esempio**

La funzione seguente combina la città del profilo e il paese in un’unica stringa.

```sql
{%= concat(profile.homeAddress.city,profile.homeAddress.country) %}
```

## Contains {#contains}

La `contains` viene utilizzata per determinare se una stringa contiene una sottostringa specificata.

**Formato**

```sql
{%= contains(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `STRING_1` | Stringa da cui eseguire il controllo. |
| `STRING_2` | Stringa da cercare all’interno della prima stringa. |
| `CASE_SENSITIVE` | Un parametro facoltativo per determinare se il controllo è sensibile a maiuscole e minuscole. Valori possibili: true (predefinito) / false. |

**Esempi**

* La funzione seguente controlla se il nome del profilo contiene la lettera A (in lettere maiuscole o minuscole). In questo caso, restituisce &quot;true&quot;, altrimenti restituisce &quot;false&quot;.

   ```sql
   {%= contains(profile.person.name.firstName, "A", false) %}
   ```

* La seguente query determina, con distinzione tra maiuscole e minuscole, se l’indirizzo e-mail della persona contiene la stringa &quot;2010@gm&quot;.

   ```sql
   {%= contains(profile.person.emailAddress,"2010@gm") %}
   ```

## Non contiene{#doesNotContain}

La `doesNotContain` viene utilizzata per determinare se una stringa non contiene una sottostringa specificata.

**Formato**

```sql
{%= doesNotContain(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `STRING_1` | Stringa da cui eseguire il controllo. |
| `STRING_2` | Stringa da cercare all’interno della prima stringa. |
| `CASE_SENSITIVE` | Un parametro facoltativo per determinare se il controllo è sensibile a maiuscole e minuscole. Valori possibili: true (predefinito) / false. |

**Esempio**

La seguente query determina, con distinzione tra maiuscole e minuscole, se l’indirizzo e-mail della persona non contiene la stringa &quot;2010@gm&quot;.

```sql
{%= doesNotContain(profile.person.emailAddress,"2010@gm")%}
```


## Non termina con{#doesNotEndWith}

La `doesNotEndWith` viene utilizzata per determinare se una stringa non termina con una sottostringa specificata.

**Formato**

```sql
{%= doesNotEndWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa da cui eseguire il controllo. |
| `{STRING_2}` | Stringa da cercare all’interno della prima stringa. |
| `{CASE_SENSITIVE}` | Un parametro facoltativo per determinare se il controllo è sensibile a maiuscole e minuscole. Valori possibili: true (predefinito) / false. |

**Esempio**

La seguente query determina, con distinzione tra maiuscole e minuscole, se l’indirizzo e-mail della persona non termina con &quot;.com&quot;.

```sql
doesNotEndWith(person.emailAddress,".com")
```

## Non inizia con{#doesNotStartWith}

La `doesNotStartWith` viene utilizzata per determinare se una stringa non inizia con una sottostringa specificata.

**Formato**

```sql
{%= doesNotStartWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa da cui eseguire il controllo. |
| `{STRING_2}` | Stringa da cercare all’interno della prima stringa. |
| `{CASE_SENSITIVE}` | Un parametro facoltativo per determinare se il controllo è sensibile a maiuscole e minuscole. Valori possibili: true (predefinito) / false. |

**Esempio**

La seguente query determina, con distinzione tra maiuscole e minuscole, se il nome della persona non inizia con &quot;Joe&quot;.

```sql
{%= doesNotStartWith(person.name,"Joe")%}
```

## Codifica 64{#encode64}

La `encode64` viene utilizzata per codificare una stringa per conservare le informazioni personali (PI) se devono essere incluse, ad esempio, in un URL.

**Formato**

```sql
{%= encode64(string) %}
```

## Termina con{#endsWith}

La `endsWith` viene utilizzata per determinare se una stringa termina con una sottostringa specificata.

**Formato**

```sql
{%= endsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa da cui eseguire il controllo. |
| `{STRING_2}` | Stringa da cercare all’interno della prima stringa. |
| `{CASE_SENSITIVE}` | Un parametro facoltativo per determinare se il controllo è sensibile a maiuscole e minuscole. Valori possibili: true (predefinito) / false. |

**Esempio**

La seguente query determina, con distinzione tra maiuscole e minuscole, se l’indirizzo e-mail della persona termina con &quot;.com&quot;.

```sql
{%= endsWith(person.emailAddress,".com") %}
```


## È uguale a{#equals}

La `equals` viene utilizzata per determinare se una stringa è uguale alla stringa specificata, con distinzione tra maiuscole e minuscole.

**Formato**

```sql
{%= equals(STRING_1, STRING_2) %}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa da cui eseguire il controllo. |
| `{STRING_2}` | Stringa da confrontare con la prima stringa. |

**Esempio**

La seguente query determina, con distinzione tra maiuscole e minuscole, se il nome della persona è &quot;John&quot;.

```sql
{%=equals(profile.person.name,"John") %}
```

## Uguale a Ignore Case{#equalsIgnoreCase}

La `equalsIgnoreCase` viene utilizzata per determinare se una stringa è uguale alla stringa specificata, senza distinzione tra maiuscole e minuscole.

**Formato**

```sql
{%= equalsIgnoreCase(STRING_1, STRING_2) %}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa da cui eseguire il controllo. |
| `{STRING_2}` | Stringa da confrontare con la prima stringa. |

**Esempio**

La seguente query determina, senza distinzione tra maiuscole e minuscole, se il nome della persona è &quot;John&quot;.

```sql
{%= equalsIgnoreCase(profile.person.name,"John") %}
```

## Estrai dominio e-mail {#extractEmailDomain}

La `extractEmailDomain` viene utilizzata per estrarre il dominio di un indirizzo e-mail.

**Formato**

```sql
{%= extractEmailDomain(string) %}
```

**Esempio**

La seguente query estrae il dominio e-mail dell’indirizzo e-mail personale.

```sql
{%= extractEmailDomain(profile.personalEmail.address) %}
```

## È vuoto {#isEmpty}

La `isEmpty` viene utilizzata per determinare se una stringa è vuota.

**Formato**

```sql
{%= isEmpty(string) %}
```

**Esempio**

La funzione seguente restituisce &quot;true&quot; se il numero di telefono cellulare del profilo è vuoto. Altrimenti, restituirà &quot;false&quot;.

```sql
{%= isEmpty(profile.mobilePhone.number) %}
```

## Taglio a sinistra {#leftTrim}

La `leftTrim` viene utilizzata per rimuovere gli spazi vuoti dall&#39;inizio di una stringa.

**Formato**

```sql
{%= leftTrim(string) %}
```

## Length {#length}

La `length` viene utilizzato per ottenere il numero di caratteri in una stringa o un&#39;espressione.

**Formato**

```sql
{%= length(string) %}
```

**Esempio**

La funzione seguente restituisce la lunghezza del nome della città del profilo.

```sql
{%= length(profile.homeAddress.city) %}
```

## Simile{#like}

La `like` viene utilizzata per determinare se una stringa corrisponde a un pattern specificato.

**Formato**

```sql
{%= like(STRING_1, STRING_2) %}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa da cui eseguire il controllo. |
| `{STRING_2}` | Espressione da confrontare con la prima stringa. Sono disponibili due caratteri speciali supportati per la creazione di un’espressione: `%` e `_`. <ul><li>`%` viene utilizzato per rappresentare zero o più caratteri.</li><li>`_` viene utilizzato per rappresentare esattamente un carattere.</li></ul> |

**Esempio**

La seguente query recupera tutte le città in cui i profili vivono contenenti il pattern &quot;es&quot;.

```sql
{%= like(profile.homeAddress.city, "%es%")%}
```

## Custodia minuscola{#lower}

La `lowerCase` converte una stringa in lettere minuscole.

**Sintassi**

```sql
{%= lowerCase(string) %}
```

**Esempio**

Questa funzione converte il nome del profilo in lettere minuscole.

```sql
{%= lowerCase(profile.person.name.firstName) %}
```

## Corrisponde{#matches}

La `matches` viene utilizzata per determinare se una stringa corrisponde a una specifica espressione regolare. Fai riferimento a [presente documento](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) per ulteriori informazioni sui pattern di corrispondenza nelle espressioni regolari.

**Formato**

```sql
{%= matches(STRING_1, STRING_2) %}
```

**Esempio**

La seguente query determina, senza distinzione tra maiuscole e minuscole, se il nome della persona inizia con &quot;John&quot;.

```sql
{%= matches(person.name.,"(?i)^John") %}
```

## Maschera (#mask)

La `Mask` viene utilizzata per sostituire una parte di una stringa con caratteri &quot;X&quot;.

**Formato**

```sql
{%= mask(string,integer,integer) %}
```

**Esempio**

La seguente query sostituisce la stringa &quot;123456789&quot; con caratteri &quot;X&quot;, ad eccezione dei primi e degli ultimi 2 caratteri.

```sql
{%= mask("123456789",1,2) %}
```

La query restituisce `1XXXXXX89`.

## Non uguale a{#notEqualTo}

La `notEqualTo` viene utilizzata per determinare se una stringa non è uguale alla stringa specificata.

**Formato**

```sql
{%= notEqualTo(STRING_1, STRING_2) %}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa da cui eseguire il controllo. |
| `{STRING_2}` | Stringa da confrontare con la prima stringa. |

**Esempio**

La seguente query determina, con distinzione tra maiuscole e minuscole, se il nome della persona non è &quot;John&quot;.

```sql
{%= notEqualTo(profile.person.name,"John") %}
```

## Gruppo di espressioni regolari{#regexGroup}

La `Group` viene utilizzata per estrarre informazioni specifiche, in base all&#39;espressione regolare fornita.

**Formato**

```sql
{%= regexGroup(STRING, EXPRESSION, GROUP) %}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING}` | Stringa da cui eseguire il controllo. |
| `{EXPRESSION}` | L&#39;espressione regolare da abbinare alla prima stringa. |
| `{GROUP}` | Gruppo di espressioni con cui confrontarsi. |

**Esempio**

La seguente query viene utilizzata per estrarre il nome di dominio da un indirizzo e-mail.

```sql
{%= regexGroup(emailAddress,"@(\w+)", 1) %}
```

## Sostituisci {#replace}

La `replace` viene utilizzata per sostituire una stringa secondaria specificata in una stringa con un&#39;altra sottostringa.

**Formato**

```sql
{%= replace(string,string,string) %}
```

**Esempio**

La seguente funzione .

```sql

```


## Sostituisci tutto{#replaceAll}

La `replaceAll` viene utilizzata per sostituire tutte le sottostringhe di un testo che corrisponde alla stringa &quot;target&quot; con la stringa letterale di &quot;sostituzione&quot; specificata. La sostituzione procede dall’inizio della stringa alla fine, ad esempio sostituendo &quot;aa&quot; con &quot;b&quot; nella stringa &quot;aaa&quot; si otterrà &quot;ba&quot; invece di &quot;ab&quot;.

**Formato**

```sql
{%= replaceAll(string,string,string) %}
```


## Taglio a destra {#rightTrim}

La `rightTrim` viene utilizzata per rimuovere gli spazi bianchi dall&#39;estremità di una stringa.


**Formato**

```sql
{%= rightTrim(string) %}
```

## Dividere {#split}

La `split` viene utilizzata per dividere una stringa in base a un carattere specificato.

**Formato**

```sql
{%= split(string,string) %}
```

<!--
**Example**

The following function .

```sql

```

-->

## Inizia con{#startsWith}

La `startsWith` viene utilizzata per determinare se una stringa inizia con una sottostringa specificata.

**Formato**

```sql
{%= startsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa da cui eseguire il controllo. |
| `{STRING_2}` | Stringa da cercare all’interno della prima stringa. |
| `{CASE_SENSITIVE}` | Un parametro facoltativo per determinare se il controllo è sensibile a maiuscole e minuscole. Per impostazione predefinita, è impostato su true. |

**Esempio**

La seguente query determina, con distinzione tra maiuscole e minuscole, se il nome della persona inizia con &quot;Joe&quot;.

```sql
{%= startsWith(person.name,"Joe") %}
```

## Caso del titolo{#titleCase}

La **titleCase** viene utilizzata per utilizzare le lettere iniziali di ogni parola di una stringa.

**Sintassi**

```sql
{%= titleCase(string) %}
```

**Esempio**

Se la persona vive a Washington High Street, questa funzione restituirà Washington High Street.

```sql
{%= titleCase(profile.person.location.Street) %}
```

## Rifila{#trim}

La **trim** rimuove tutti gli spazi bianchi dall&#39;inizio e alla fine di una stringa.

**Sintassi**

```sql
{%= trim(string) %}
```

## Caso superiore{#upper}

La **UpCase** converte una stringa in lettere maiuscole.

**Sintassi**

```sql
{%= upperCase(string) %}
```

**Esempio**

Questa funzione converte il cognome del profilo in lettere maiuscole.

```sql
{%= upperCase(profile.person.name.lastName) %}
```
