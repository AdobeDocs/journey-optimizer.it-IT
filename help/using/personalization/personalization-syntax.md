---
solution: Journey Optimizer
product: journey optimizer
title: Sintassi di personalizzazione
description: Scopri come utilizzare la sintassi di personalizzazione.
feature: Personalization
topic: Personalization
role: Developer
level: Intermediate
keywords: espressione, editor, sintassi, personalizzazione
exl-id: 5a562066-ece0-4a78-92a7-52bf3c3b2eea
TQID: https://experienceleague.adobe.com/kZEw2lITdt8SMWMe-UT2vPzdoiAjB2vbItmK9zt-WJo
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2:
  - id: ac5d9310-7772-40fb-9d78-864562e1bfd6
  - id: e51e8901-97d9-4f7d-a835-503025a90e32
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 1299
ht-degree: 3%

---

# Sintassi di personalizzazione {#personalization-syntax}

Personalization in [!DNL Journey Optimizer] utilizza due sintassi complementari che funzionano insieme nella stessa espressione:

* **Handlebars** (`{{...}}`): utilizzato per eseguire il rendering degli attributi di profilo, eseguire il loop su array e chiamare gli helper di blocco. Consulta la [documentazione HandlebarsJS](https://handlebarsjs.com/) per un riferimento completo.
* **Profile Query Language (PQL)** (`{%= ... %}`): utilizzato per chiamare funzioni incorporate (ad esempio `upperCase()`, `formatDate()`, `dateDiff()`) e valutare espressioni condizionali.

Per evitare errori di runtime, è fondamentale capire in quale contesto ci si trova. Ad esempio, una chiamata di funzione PQL inserita all&#39;interno di `{{...}}` avrà esito negativo perché Handlebars tenta di risolverla come helper anziché valutarla come espressione di PQL.

**Esempi:**

| Caso d’uso | Sintassi |
|----------|--------|
| Eseguire il rendering di un attributo di profilo | `{{profile.person.name.firstName}}` |
| Chiamare una funzione PQL | `{%= upperCase(profile.person.name.firstName) %}` |
| Blocco condizionale | `{%#if profile.loyalty.tier = "gold"%}...{%/if%}` |
| Eseguire il ciclo su un array | `{{#each profile.orders}}...{{/each}}` |

La struttura degli attributi è definita in uno schema XDM di Adobe Experience Platform. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target="_blank"}.

>[!TIP]
>
>Per le espressioni pronte all&#39;uso che applicano queste sintassi a scenari reali, ad esempio formattazione delle date, conteggi, fallback condizionali e altro ancora, vedere la pagina **[Composizioni di Personalization](personalization-recipes.md)**.

## Regole generali di sintassi {#general-rules}

* Gli identificatori possono essere qualsiasi carattere Unicode ad eccezione dei seguenti caratteri speciali, che sono riservati per la sintassi Handlebars:

  ```
  Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
  ```

* La sintassi fa distinzione tra maiuscole e minuscole.

* Le parole **true**, **false**, **null** e **undefined** sono consentite solo nella prima parte di un&#39;espressione di percorso.

* In Handlebars, i valori restituiti da {{expression}} sono **con escape HTML**. Se l&#39;espressione contiene `&`, l&#39;output con escape HTML restituito verrà generato come `&amp;`. Se non vuoi che Handlebars sfugga a un valore, utilizza il &quot;triplo-stash&quot;.

  Si supponga che il valore del campo `profile.person.name` sia &quot;Mark &amp; Mary&quot;. La sintassi `{{profile.person.name}}` visualizzerà `Mark &amp; Mary`, mentre `{{{profile.person.name}}}` visualizzerà `Mark & Mary`.

* Per quanto riguarda gli argomenti delle funzioni letterali, il parser del linguaggio del modello non supporta una singola barra rovesciata senza escape (`\`). Questo carattere deve essere preceduto da una barra rovesciata (`\`). Esempio:

  `{%= regexGroup("abc@xyz.com","@(\\w+)", 1)%}`

* Per includere **virgolette doppie letterali** in un valore stringa (ad esempio, durante la generazione dell&#39;output JSON), esegui l&#39;escape con una barra rovesciata (`\"`):

  ```handlebars
  { "message": "Hello \"{{profile.person.name.firstName}}\"" }
  ```

  Output: `{ "message": "Hello \"John\"" }`

  In alternativa, utilizza il triplo-stash `{{{ }}}` per generare HTML senza escape quando il valore stesso contiene caratteri speciali che non desideri siano codificati in HTML.

## Parole chiave riservate {#reserved-keywords}

Alcune parole chiave sono riservate in Profile Query Language (PQL) e non possono essere utilizzate direttamente come nomi di campi o variabili nelle espressioni di personalizzazione. Se lo schema XDM contiene campi con nomi che corrispondono a parole chiave riservate, è necessario eseguirne l&#39;escape utilizzando apici inversi (`` ` ``) per farvi riferimento nelle espressioni.

**Le parole chiave riservate includono:**

* `next`
* `last`
* `this`

**Esempio:**

Se lo schema del profilo dispone di un campo denominato `next`, è necessario racchiuderlo in apici:

```
{{profile.person.`next`.name}}
```

Se non vengono utilizzati i backtick, l’editor di personalizzazione non riuscirà a eseguire la convalida e restituirà un errore.

>[!NOTE]
>
>L&#39;escape backtick per le parole chiave riservate si applica sia ai percorsi Handlebars `{{...}}` che alle espressioni PQL `{%= ... %}`, poiché queste parole chiave sono riservate al livello di risoluzione del percorso. Questa funzione è diversa dai nomi di campo sillabati, in cui l’escape con apice inverso è supportato solo all’interno di espressioni PQL. Vedi [Chiavi attributo con sillabazione](#hyphenated-keys).

## Regole di sintassi PQL per chiavi di attributi speciali {#pql-special-keys}

Oltre alle parole chiave riservate, due casi aggiuntivi richiedono l’escape backtick nelle espressioni PQL.

### Chiavi attributo sillabate {#hyphenated-keys}

Se lo schema XDM contiene nomi di campo con trattini (ad esempio `my-field`, `event-type`) o nomi che iniziano con o contengono numeri, racchiudi la chiave tra i segni di sospensione all&#39;interno delle espressioni PQL:

```sql
{%= profile.events.`order-total` > 100 %}
```

>[!NOTE]
>
>L&#39;escape di tipo Backtick è supportato solo all&#39;interno di espressioni PQL (`{%= ... %}`). Non è supportato nell&#39;interpolazione Handlebars (`{{...}}`). Tuttavia, è possibile fare riferimento direttamente ai nomi dei campi sillabati nei blocchi `{{...}}` (ad esempio `{{profile.my-custom-field}}`); solo la sintassi backtick non riesce.

Senza apici retroversi in un’espressione PQL, il trattino viene interpretato come un operatore di sottrazione e causa un errore di sintassi PQL.

### ID evento numerici negli attributi di contesto {#numeric-event-ids}

Quando si fa riferimento agli attributi dell&#39;evento di contesto in cui l&#39;ID evento è un numero (ad esempio `1697323153`), racchiuderlo in apici. Questo vale anche all&#39;interno di funzioni come `formatDate()`:

```handlebars
{% let ts = formatDate(toDateTime(context.journey.events.`1697323153`.timestamp), "dd/MM/yyyy") %}
{{ts}}
```

## Tipo coercizione {#type-coercion}

PQL è fortemente tipizzato. Quando si confrontano o si trasmettono valori, entrambi i lati devono essere dello stesso tipo. Casi comuni:

| Scenario | Soluzione |
|----------|----------|
| Valore numerico memorizzato come stringa | Usa `stringToNumber()` prima di aritmetica o confronto: `{%= stringToNumber(profile.loyalty.pointsBalance) > 500 %}` |
| Intero memorizzato come stringa | Usa `string_to_integer()` o `stringToNumber()` prima dell&#39;aritmetica |
| Booleano memorizzato come stringa | Usa `toBool()` per convertire: `{%= toBool(profile.consents.email.val) = true %}` |

## Spazi dei nomi disponibili {#namespaces}

* **Profilo**

  Questo spazio dei nomi consente di fare riferimento a tutti gli attributi definiti nello schema del profilo descritto nella [documentazione di Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target="_blank"}.

  Gli attributi devono essere definiti nello schema prima di essere referenziati in un blocco di personalizzazione [!DNL Journey Optimizer].

  Per ulteriori informazioni su come sfruttare gli attributi del profilo nelle condizioni, consulta [questa sezione](functions/helpers.md#if-function).

  +++Riferimenti di esempio

   * `{{profile.person.name.fullName}}`
   * `{{profile.person.name.firstName}}`
   * `{{profile.person.gender}}`
   * `{{profile.personalEmail.address}}`
   * `{{profile.mobilePhone.number}}`
   * `{{profile.homeAddress.city}}`
   * `{{profile.faxPhone.number}}`

  +++

* **Pubblico**

  Per ulteriori informazioni sul servizio di segmentazione, consulta [questa documentazione](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=it){target="_blank"}.

* **Offerte**

  Questo spazio dei nomi consente di fare riferimento alle decisioni sulle offerte esistenti.

  Per fare riferimento a un’offerta è necessario dichiarare un percorso con le diverse informazioni che definiscono un’offerta. Questo percorso ha la seguente struttura:

  `offers.Type.[Placement Id].[Activity Id].Attribute`

  dove:

   * `offers` identifica l&#39;espressione di percorso appartenente allo spazio dei nomi dell&#39;offerta
   * `Type` determina il tipo di rappresentazione dell&#39;offerta. I valori possibili sono: `image`, `html` e `text`
   * `Placement Id` e `Activity Id` sono identificatori di posizionamento e attività
   * `Attributes` sono attributi specifici dell&#39;offerta che dipendono dal tipo di offerta. Esempio: `deliveryUrl` per le immagini

  Per ulteriori informazioni sull&#39;API Decisions e sulle rappresentazioni di offerte, consulta [questa pagina](../offers/api-reference/offer-delivery-api/decisioning-api.md)

  Tutti i riferimenti vengono convalidati in base allo schema delle offerte con un meccanismo di convalida descritto in [questa pagina](../personalization/personalization-build-expressions.md)

  +++Riferimenti di esempio

   * Posizione in cui è ospitata l’immagine:

     `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl`

   * URL di destinazione quando fai clic sull’immagine:

     `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl`

   * Contenuto del testo dell’offerta proveniente dal motore decisionale:

     `offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

   * Contenuto HTML dell’offerta proveniente dal motore decisionale:

     `offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

  +++

## Helper {#helpers-all}

Un helper Handlebars è un semplice identificatore che può essere seguito da parametri. Ogni parametro è un&#39;espressione Handlebars. È possibile accedere a questi helper da qualsiasi contesto in un modello.

Questi helper di blocco sono identificati da un `#` che precede il nome dell&#39;helper e richiedono un `/` di chiusura corrispondente, con lo stesso nome.

I blocchi sono espressioni con un blocco di apertura (`{{# }}`) e chiusura (`{{/}}`).

Per ulteriori informazioni sulle funzioni di supporto, consultare [questa sezione](functions/helpers.md).

## Tipi letterali {#literal-types}

[!DNL Adobe Journey Optimizer] supporta i seguenti tipi letterali:

| Letterale | Definizione |
| ------- | ---------- |
| Stringa | Tipo di dati costituito da caratteri racchiusi tra virgolette doppie. <br>Esempi: `"prospect"`, `"jobs"`, `"articles"` |
| Booleano | Tipo di dati true o false. |
| Intero | Tipo di dati che rappresenta un numero intero. Può essere positivo, negativo o zero. <br>Esempi: `-201`, `0`, `412` |
| Array | Tipo di dati composto da un gruppo di altri valori letterali. Utilizza parentesi quadre per raggruppare e virgole per delimitare tra valori diversi. <br> **Nota:** non è possibile accedere direttamente alle proprietà degli elementi all&#39;interno di un array. <br> Esempi: `[1, 4, 7]`, `["US", "FR"]` |

>[!CAUTION]
>
>L&#39;utilizzo della variabile **xEvent** non è disponibile nelle espressioni di personalizzazione. Qualsiasi riferimento a xEvent provocherà errori di convalida.

## Best practice {#best-practices}

Rivedi queste regole di sintassi prima di creare espressioni di personalizzazione. La maggior parte degli errori di runtime deriva dalla combinazione di Handlebars e contesti di PQL.

**Utilizzare la sintassi del blocco condizionale corretta**

Usa sempre `{%#if%}` / `{%else if%}` / `{%else%}` / `{%/if%}`. Sintassi `{% if %}` / `{% elseif %}` / `{% endif %}` non supportata.

```handlebars
{%#if profile.loyalty.tier = "gold"%}
Gold member content
{%else if profile.loyalty.tier = "silver"%}
Silver member content
{%else%}
Default content
{%/if%}
```

**Non chiamare funzioni PQL all&#39;interno di `{{...}}` blocchi Handlebars**

`{{...}}` risolve solo le variabili Handlebars e gli helper, ma non valuta PQL. Il wrapping di una funzione PQL come `upperCase()` in `{{...}}` causa un errore di tipo &quot;Impossibile trovare l&#39;helper&quot;. Utilizza invece `{%= ... %}`:

| Non corretto | Corretto |
|-----------|---------|
| `{{upperCase(cleanName)}}` | `{%= upperCase(cleanName) %}` |

**Utilizzare un alias loop denominato quando si combina `{{#each}}` con`{%#if%}`**

`this.field` è risolto dal renderer Handlebars ma non dal valutatore PQL all&#39;interno di una condizione `{%#if%}`. Definire un alias denominato con `as |item|` in modo che entrambi i contesti possano risolvere il campo:

```handlebars
{{#each profile.orders as |order|}}
  {%#if order.status = "pending"%}
  Order {{order.id}} is pending.
  {%/if%}
{{/each}}
```

**Assegnare i risultati della funzione PQL a una variabile prima di eseguire un ciclo**

Impossibile chiamare le FDU di PQL come `topN` direttamente in `{{#each}}`. Valutali prima con `{% let %}`, quindi esegui un&#39;iterazione sul risultato:

```handlebars
{% let topOrders = topN(profile.orders, price, 3) %}
{{#each topOrders}}
  {{this.name}} — {{this.price}}&euro;
{{/each}}
```

**Utilizza `{% let %}` per evitare di ripetere le chiamate di funzione**

Se un valore calcolato è necessario più di una volta, memorizzalo in una variabile. Ciò migliora la leggibilità e impedisce le valutazioni ridondanti:

```handlebars
{% let cleanName = replaceAll(profile.person.name.firstName, "[^a-zA-Z]", "") %}
Hi {{cleanName}}, your code is: WELCOME-{%= upperCase(cleanName) %}
```

**Utilizza l&#39;ordine corretto degli argomenti per`dateDiff`**

`dateDiff(start, end)` prende prima la data precedente. Per calcolare i giorni rimanenti fino a una data futura, passare la data corrente come primo argomento:

```handlebars
{% let daysLeft = dateDiff(getCurrentZonedDateTime(), stringToDate(profile.loyalty.expiryDate)) %}
```

**Utilizzare `=` per i confronti di uguaglianza in PQL, non`==`**

PQL utilizza un singolo operatore `=` per l&#39;uguaglianza. L&#39;utilizzo di `==` genera un errore di sintassi.

**Usa i contrassegni per i nomi dei campi sillabati, solo nelle espressioni PQL**

Se il nome di un campo dello schema XDM contiene un trattino (ad esempio `order-total`), racchiudilo tra apici per evitare che il trattino venga analizzato come operatore di sottrazione. Questo è supportato solo all&#39;interno di `{%= ... %}` espressioni PQL, non nei blocchi Handlebars `{{...}}`:

```sql
{%= profile.events.`order-total` > 100 %}
```

Per le espressioni pronte all&#39;uso che puoi copiare direttamente nel contenuto, consulta [Composizioni di Personalization](personalization-recipes.md).
