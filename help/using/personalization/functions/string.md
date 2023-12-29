---
title: Libreria funzioni stringa
description: Libreria funzioni stringa
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 8674ef9e-261b-49d9-800e-367f9f7ef979
source-git-commit: 118eddf540d1dfb3a30edb0b877189ca908944b1
workflow-type: tm+mt
source-wordcount: '1846'
ht-degree: 6%

---

# Funzioni stringa {#string}

Scopri come utilizzare le funzioni String nell’editor di espressioni.

## Camel Case {#camelCase}

Il `camelCase` La funzione maiuscola la prima lettera di ogni parola di una stringa.

**Sintassi**

```sql
{%= camelCase(string)%}
```

**Esempio**

La funzione seguente metterà in maiuscolo la prima lettera di parola nell’indirizzo stradale del profilo.

```sql
{%= camelCase(profile.homeAddress.street) %}
```

## Codice carattere in corrispondenza di {#char-code-at}

Il `charCodeAt` La funzione restituisce il valore ASCII di un carattere, come la funzione charCodeAt in JavaScript. Come argomenti di input sono necessari una stringa e un numero intero (che definisce la posizione del carattere) e viene restituito il valore ASCII corrispondente.

**Sintassi**

```sql
{%= charCodeAt(string,int) %}: int
```

**Esempio**

La funzione seguente restituisce il valore ASCII o i.e 111.

```sql
{%= charCodeAt("some", 1)%}
```

## Concat {#concate}

Il `concat` funzione combina due stringhe in una.

**Sintassi**

```sql
{%= concat(string,string) %}
```

**Esempio**

La funzione seguente combina il profilo città e paese in una singola stringa.

```sql
{%= concat(profile.homeAddress.city,profile.homeAddress.country) %}
```

## Contains {#contains}

Il `contains` La funzione viene utilizzata per determinare se una stringa contiene una sottostringa specificata.

**Sintassi**

```sql
{%= contains(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `STRING_1` | Stringa su cui eseguire il controllo. |
| `STRING_2` | Stringa da cercare nella prima stringa. |
| `CASE_SENSITIVE` | Un parametro opzionale per determinare se il controllo distingue tra maiuscole e minuscole. Valori possibili: true (predefinito) / false. |

**Esempi**

* La funzione seguente verifica se il nome del profilo contiene la lettera A (in maiuscolo o minuscolo). In questo caso, restituirà &quot;true&quot;, altrimenti restituirà &quot;false&quot;.

  ```sql
  {%= contains(profile.person.name.firstName, "A", false) %}
  ```

* La query seguente determina, con distinzione tra maiuscole e minuscole, se l’indirizzo e-mail della persona contiene la stringa &quot;2010@gm&quot;.

  ```sql
  {%= contains(profile.person.emailAddress,"2010@gm") %}
  ```

## Non contiene{#doesNotContain}

Il `doesNotContain` La funzione viene utilizzata per determinare se una stringa non contiene una sottostringa specificata.

**Sintassi**

```sql
{%= doesNotContain(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `STRING_1` | Stringa su cui eseguire il controllo. |
| `STRING_2` | Stringa da cercare nella prima stringa. |
| `CASE_SENSITIVE` | Un parametro opzionale per determinare se il controllo distingue tra maiuscole e minuscole. Valori possibili: true (predefinito) / false. |

**Esempio**

La query seguente determina, con distinzione tra maiuscole e minuscole, se l’indirizzo e-mail della persona non contiene la stringa &quot;2010@gm&quot;.

```sql
{%= doesNotContain(profile.person.emailAddress,"2010@gm")%}
```


## Non termina con{#doesNotEndWith}

Il `doesNotEndWith` La funzione viene utilizzata per determinare se una stringa non termina con una sottostringa specificata.

**Sintassi**

```sql
{%= doesNotEndWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa su cui eseguire il controllo. |
| `{STRING_2}` | Stringa da cercare nella prima stringa. |
| `{CASE_SENSITIVE}` | Un parametro opzionale per determinare se il controllo distingue tra maiuscole e minuscole. Valori possibili: true (predefinito) / false. |

**Esempio**

La query seguente determina, con distinzione tra maiuscole e minuscole, se l’indirizzo e-mail della persona non termina con &quot;.com&quot;.

```sql
doesNotEndWith(person.emailAddress,".com")
```

## Non inizia con{#doesNotStartWith}

Il `doesNotStartWith` La funzione viene utilizzata per determinare se una stringa non inizia con una sottostringa specificata.

**Sintassi**

```sql
{%= doesNotStartWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa su cui eseguire il controllo. |
| `{STRING_2}` | Stringa da cercare nella prima stringa. |
| `{CASE_SENSITIVE}` | Un parametro opzionale per determinare se il controllo distingue tra maiuscole e minuscole. Valori possibili: true (predefinito) / false. |

**Esempio**

La query seguente determina, con distinzione tra maiuscole e minuscole, se il nome della persona non inizia con &quot;Joe&quot;.

```sql
{%= doesNotStartWith(person.name,"Joe")%}
```

## Codifica 64{#encode64}

Il `encode64` La funzione viene utilizzata per codificare una stringa per conservare le informazioni personali (PI) se da includere, ad esempio, in un URL.

**Sintassi**

```sql
{%= encode64(string) %}
```

## Termina con{#endsWith}

Il `endsWith` viene utilizzata per determinare se una stringa termina con una sottostringa specificata.

**Sintassi**

```sql
{%= endsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa su cui eseguire il controllo. |
| `{STRING_2}` | Stringa da cercare nella prima stringa. |
| `{CASE_SENSITIVE}` | Un parametro opzionale per determinare se il controllo distingue tra maiuscole e minuscole. Valori possibili: true (predefinito) / false. |

**Esempio**

La query seguente determina, con distinzione tra maiuscole e minuscole, se l’indirizzo e-mail della persona termina con &quot;.com&quot;.

```sql
{%= endsWith(person.emailAddress,".com") %}
```


## È uguale a{#equals}

Il `equals` viene utilizzata per determinare se una stringa è uguale alla stringa specificata, con distinzione tra maiuscole e minuscole.

**Sintassi**

```sql
{%= equals(STRING_1, STRING_2) %}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa su cui eseguire il controllo. |
| `{STRING_2}` | Stringa da confrontare con la prima stringa. |

**Esempio**

La query seguente determina, con distinzione tra maiuscole e minuscole, se il nome della persona è &quot;John&quot;.

```sql
{%=equals(profile.person.name,"John") %}
```

## Ignora maiuscole/minuscole uguale a{#equalsIgnoreCase}

Il `equalsIgnoreCase` viene utilizzata per determinare se una stringa è uguale alla stringa specificata, senza distinzione tra maiuscole e minuscole.

**Sintassi**

```sql
{%= equalsIgnoreCase(STRING_1, STRING_2) %}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa su cui eseguire il controllo. |
| `{STRING_2}` | Stringa da confrontare con la prima stringa. |

**Esempio**

La query seguente determina se il nome della persona è &quot;John&quot; senza distinzione tra maiuscole e minuscole.

```sql
{%= equalsIgnoreCase(profile.person.name,"John") %}
```

## Estrai dominio e-mail {#extractEmailDomain}

Il `extractEmailDomain` viene utilizzata per estrarre il dominio di un indirizzo e-mail.

**Sintassi**

```sql
{%= extractEmailDomain(string) %}
```

**Esempio**

La query seguente estrae il dominio e-mail dell’indirizzo e-mail personale.

```sql
{%= extractEmailDomain(profile.personalEmail.address) %}
```

## Formato valuta {#format-currency}

Il `formatCurrency` La funzione viene utilizzata per convertire qualsiasi numero nella corrispondente rappresentazione della valuta sensibile alla lingua a seconda delle impostazioni locali passate come stringa nel secondo argomento.

**Sintassi**

```sql
{%= formatCurrency(number/double,string) %}: string
```

**Esempio**

Questa query restituisce £ 56,00

```sql
{%= formatCurrency(56L,"en_GB") %}
```

## Ottieni host URL {#get-url-host}

Il `getUrlHost` viene utilizzata per recuperare il nome host di un URL.

**Sintassi**

```sql
{%= getUrlHost(string) %}: string
```

**Esempio**

```sql
{%= getUrlHost("https://www.myurl.com/contact") %}
```

Restituisce &quot;www.myurl.com&quot;

## Ottieni percorso URL {#get-url-path}

Il `getUrlPath` La funzione viene utilizzata per recuperare il percorso dopo il nome di dominio di un URL.

**Sintassi**

```sql
{%= getUrlPath(string) %}: string
```

**Esempio**

```sql
{%= getUrlPath("https://www.myurl.com/contact.html") %}
```

Restituisce &quot;/contact.html&quot;

## Ottieni protocollo URL {#get-url-protocol}

Il `getUrlProtocol` viene utilizzata per recuperare il protocollo di un URL.

**Sintassi**

```sql
{%= getUrlProtocol(string) %}: string
```

**Esempio**

```sql
{%= getUrlProtocol("https://www.myurl.com/contact.html") %}
```

Restituisce &quot;http&quot;

## Indice di {#index-of}

Il `indexOf` viene utilizzata per restituire la posizione (nel primo argomento) della prima occorrenza del secondo parametro. Restituisce -1 se non viene trovata alcuna corrispondenza.

**Sintassi**

```sql
{%= indexOf(STRING_1, STRING_2) %}: integer
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa su cui eseguire il controllo. |
| `{STRING_2}` | Stringa da cercare nel primo parametro |

**Esempio**

```sql
{%= indexOf("hello world","world" ) %}
```

Restituisce 6.

## È vuoto {#isEmpty}

Il `isEmpty` viene utilizzata per determinare se una stringa è vuota.

**Sintassi**

```sql
{%= isEmpty(string) %}
```

**Esempio**

La funzione seguente restituisce &quot;true&quot; se il numero di telefono cellulare del profilo è vuoto. Altrimenti, restituirà &quot;false&quot;.

```sql
{%= isEmpty(profile.mobilePhone.number) %}
```

## Non è vuoto {#is-not-empty}

Il `isNotEmpty` viene utilizzata per determinare se una stringa non è vuota.

**Sintassi**

```sql
{= isNotEmpty(string) %}: boolean
```

**Esempio**

La funzione seguente restituisce &quot;true&quot; se il numero di telefono cellulare del profilo non è vuoto. Altrimenti, restituirà &quot;false&quot;.

```sql
{%= isNotEmpty(profile.mobilePhone.number) %}
```

## Ultimo indice di {#last-index-of}

Il `lastIndexOf` La funzione viene utilizzata per restituire la posizione (nel primo argomento) dell&#39;ultima occorrenza del secondo parametro. Restituisce -1 se non viene trovata alcuna corrispondenza.

**Sintassi**

```sql
{= lastIndexOf(STRING_1, STRING_2) %}: integer
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa su cui eseguire il controllo. |
| `{STRING_2}` | Stringa da cercare nel primo parametro |

**Esempio**

```sql
{%= lastIndexOf("hello world","o" ) %}
```

Restituisce 7.

## Taglia a sinistra {#leftTrim}

Il `leftTrim` La funzione viene utilizzata per rimuovere gli spazi bianchi dall’inizio di una stringa.

**Sintassi**

```sql
{%= leftTrim(string) %}
```

## Lunghezza {#length}

Il `length` La funzione viene utilizzata per ottenere il numero di caratteri in una stringa o in un’espressione.

**Sintassi**

```sql
{%= length(string) %}
```

**Esempio**

La funzione seguente restituisce la lunghezza del nome della città del profilo.

```sql
{%= length(profile.homeAddress.city) %}
```

## Mi piace{#like}

Il `like` viene utilizzata per determinare se una stringa corrisponde a un pattern specificato.

**Sintassi**

```sql
{%= like(STRING_1, STRING_2) %}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa su cui eseguire il controllo. |
| `{STRING_2}` | Espressione da confrontare con la prima stringa. Per creare un’espressione sono disponibili due caratteri speciali supportati: `%` e `_`. <ul><li>`%` viene utilizzato per rappresentare zero o più caratteri.</li><li>`_` viene utilizzato per rappresentare esattamente un carattere.</li></ul> |

**Esempio**

La query seguente recupera tutte le città in cui vivono i profili che contengono il pattern &quot;es&quot;.

```sql
{%= like(profile.homeAddress.city, "%es%")%}
```

## Minuscolo{#lower}

Il `lowerCase` funzione converte una stringa in lettere minuscole.

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

Il `matches` viene utilizzata per determinare se una stringa corrisponde a una specifica espressione regolare. Fare riferimento a [questo documento](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) per ulteriori informazioni sui pattern corrispondenti nelle espressioni regolari, vedere.

**Sintassi**

```sql
{%= matches(STRING_1, STRING_2) %}
```

**Esempio**

La query seguente determina, senza distinzione tra maiuscole e minuscole, se il nome della persona inizia con &quot;John&quot;.

```sql
{%= matches(person.name.,"(?i)^John") %}
```

## Maschera {#mask}

Il `Mask` La funzione viene utilizzata per sostituire una parte di stringa con caratteri &quot;X&quot;.

**Sintassi**

```sql
{%= mask(string,integer,integer) %}
```

**Esempio**

La query seguente sostituisce la stringa &quot;123456789&quot; con caratteri &quot;X&quot;, ad eccezione del primo e dell’ultimo secondo carattere.

```sql
{%= mask("123456789",1,2) %}
```

La query restituisce `1XXXXXX89`.

## MD5 {#md5}

Il `md5` La funzione viene utilizzata per calcolare e restituire l’hash md5 di una stringa.

**Sintassi**

```sql
{%= md5(string) %}: string
```

**Esempio**

```sql
{%= md5("hello world") %}
```

Restituisce &quot;5eb63bbbe01eeed093cb22bb8f5acdc3&quot;

## Diverso da{#notEqualTo}

Il `notEqualTo` viene utilizzata per determinare se una stringa non è uguale alla stringa specificata.

**Sintassi**

```sql
{%= notEqualTo(STRING_1, STRING_2) %}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa su cui eseguire il controllo. |
| `{STRING_2}` | Stringa da confrontare con la prima stringa. |

**Esempio**

La query seguente determina, con distinzione tra maiuscole e minuscole, se il nome della persona non è &quot;John&quot;.

```sql
{%= notEqualTo(profile.person.name,"John") %}
```

## Non uguale con ignora maiuscole/minuscole {#not-equal-with-ignore-case}

Il `notEqualWithIgnoreCase` viene utilizzata per confrontare due stringhe ignorando la distinzione tra maiuscole e minuscole.

**Sintassi**

```sql
{= notEqualWithIgnoreCase(STRING_1,STRING_2) %}: boolean
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa su cui eseguire il controllo. |
| `{STRING_2}` | Stringa da confrontare con la prima stringa. |

**Esempio**

La query seguente determina se il nome della persona non è &quot;John&quot;, senza distinzione tra maiuscole e minuscole.

```sql
{%= notEqualTo(profile.person.name,"john") %}
```

## Gruppo di espressioni regolari{#regexGroup}

Il `Group` La funzione viene utilizzata per estrarre informazioni specifiche, in base all’espressione regolare fornita.

**Sintassi**

```sql
{%= regexGroup(STRING, EXPRESSION, GROUP) %}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING}` | Stringa su cui eseguire il controllo. |
| `{EXPRESSION}` | Espressione regolare da confrontare con la prima stringa. |
| `{GROUP}` | Gruppo di espressioni con cui confrontare. |

**Esempio**

La query seguente viene utilizzata per estrarre il nome di dominio da un indirizzo e-mail.

```sql
{%= regexGroup(emailAddress,"@(\\w+)", 1) %}
```

## Sostituisci {#replace}

Il `replace` La funzione viene utilizzata per sostituire una determinata sottostringa in una stringa con un’altra sottostringa.

**Sintassi**

```sql
{%= replace(STRING_1,STRING_2,STRING_3) %}:string
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa in cui deve essere sostituita la sottostringa. |
| `{STRING_2}` | Sottostringa da sostituire. |
| `{STRING_3}` | La sottostringa di sostituzione. |

**Esempio**

```sql
{%= replace("Hello John, here is your monthly newsletter!","John","Mark") %}
```

Restituisce &quot;Ciao Mark, ecco la tua newsletter mensile!&quot;

## Sostituisci tutto{#replaceAll}

Il `replaceAll` La funzione viene utilizzata per sostituire tutte le sottostringhe di un testo che corrisponde all’espressione &quot;regex&quot; con la stringa letterale &quot;replace&quot; specificata. Regex gestisce in modo particolare &quot;\&quot; e &quot;+&quot; e tutte le espressioni regex seguono la strategia di escape PQL. La sostituzione procede dall&#39;inizio della stringa alla fine, ad esempio, sostituendo &quot;aa&quot; con &quot;b&quot; nella stringa &quot;aaa&quot; si otterrà &quot;ba&quot; invece di &quot;ab&quot;.

**Sintassi**

```sql
{%= replaceAll(string,string,string) %}
```

>[!NOTE]
>
> Se l&#39;espressione utilizzata come secondo argomento è un carattere regex speciale, utilizzare una doppia barra rovesciata (`//`).  I caratteri regex speciali sono: [., +, *, ?, ^, $, (, ), [,], {, }, |, \.]
> 
> Ulteriori informazioni in [Documentazione di Oracle](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html){_blank}.
>

## Taglia a destra {#rightTrim}

Il `rightTrim` La funzione viene utilizzata per rimuovere gli spazi bianchi dalla fine di una stringa.

**Sintassi**

```sql
{%= rightTrim(string) %}
```

## Split {#split}

Il `split` La funzione viene utilizzata per dividere una stringa per un determinato carattere.

**Sintassi**

```sql
{%= split(string,string) %}
```

## Inizia con{#startsWith}

Il `startsWith` viene utilizzata per determinare se una stringa inizia con una sottostringa specificata.

**Sintassi**

```sql
{%= startsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{STRING_1}` | Stringa su cui eseguire il controllo. |
| `{STRING_2}` | Stringa da cercare nella prima stringa. |
| `{CASE_SENSITIVE}` | Un parametro opzionale per determinare se il controllo distingue tra maiuscole e minuscole. Per impostazione predefinita, questo è impostato su true. |

**Esempio**

La query seguente determina, con distinzione tra maiuscole e minuscole, se il nome della persona inizia con &quot;Joe&quot;.

```sql
{%= startsWith(person.name,"Joe") %}
```

## Stringa a data {#string-to-date}

Il `stringToDate` funzione converte un valore stringa in un valore data-ora. Sono necessari due argomenti: la rappresentazione in forma di stringa di una data/ora e la rappresentazione in forma di stringa del formattatore.

**Sintassi**

```sql
{= stringToDate("date-time value","formatter" %}
```

**Esempio**

```sql
{= stringToDate("2023-01-10 23:13:26", "yyyy-MM-dd HH:mm:ss") %}
```

## Stringa a numero intero {#string-to-integer}

Il `string_to_integer` viene utilizzata per convertire un valore stringa in un valore intero.

**Sintassi**

```sql
{= string_to_integer(string) %}: int
```

## Stringa a numero {#string-to-number}

Il `stringToNumber` viene utilizzata per convertire una stringa in numero. In caso di input non valido, restituisce la stessa stringa come output.

**Sintassi**

```sql
{%= stringToNumber(string) %}: double
```

## Sottostringa {#sub-string}

Il `Count string` La funzione viene utilizzata per restituire la sottostringa dell&#39;espressione stringa tra l&#39;indice iniziale e l&#39;indice finale.
**Sintassi**

```sql
{= substr(string, integer, integer) %}: string
```

## Tutte iniziali maiuscole{#titleCase}

Il **titleCase** La funzione viene utilizzata per rendere maiuscole le prime lettere di ciascuna parola di una stringa.

**Sintassi**

```sql
{%= titleCase(string) %}
```

**Esempio**

Se la persona vive a Washington High Street, questa funzione restituirà Washington High Street.

```sql
{%= titleCase(profile.person.location.Street) %}
```

## To Bool {#to-bool}

Il `toBool` funzione viene utilizzata per convertire un valore di argomento in un valore booleano, a seconda del tipo.

**Sintassi**

```sql
{= toBool(string) %}: boolean
```

## A Data/Ora {#to-date-time}

Il `toDateTime` funzione viene utilizzata per convertire una stringa in data. In caso di input non valido, restituisce la data epoca come output.

**Sintassi**

```sql
{%= toDateTime(string, string) %}: date-time
```

## Solo a data/ora {#to-date-time-only}

Il `toDateTimeOnly` funzione viene utilizzata per convertire un valore di argomento in un valore di sola data e ora. In caso di input non valido, restituisce la data epoca come output. Questa funzione accetta tipi di campo stringa, data, long e int.

**Sintassi**

```sql
{%= toDateTimeOnly(string/date/long/int) %}: date-time
```

## Trim (Taglia) {#trim}

Il **trim** rimuove tutti gli spazi bianchi dall&#39;inizio e dalla fine di una stringa.

**Sintassi**

```sql
{%= trim(string) %}
```

## Maiuscolo{#upper}

Il **upperCase** funzione converte una stringa in lettere maiuscole.

**Sintassi**

```sql
{%= upperCase(string) %}
```

**Esempio**

Questa funzione converte il cognome del profilo in lettere maiuscole.

```sql
{%= upperCase(profile.person.name.lastName) %}
```

## Decodifica URL {#url-decode}

Il `urlDecode` viene utilizzata per decodificare una stringa con codifica url.

**Sintassi**

```sql
{%= urlDecode(string) %}: string
```

## Codifica URL {#url-encode}

Il `Count only null` La funzione viene utilizzata per codificare un URL in una stringa.

**Sintassi**

```sql
{%= urlEncode(string) %}: string
```
