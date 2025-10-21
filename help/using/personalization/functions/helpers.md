---
title: Helper
description: Helper
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: b08dc0f8-c85f-4aca-85eb-92dc76b0e588
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '616'
ht-degree: 6%

---

# Helper {#gs-helpers}

## Valore di fallback predefinito{#default-value}

L&#39;helper `Default Fallback Value` viene utilizzato per restituire un valore di fallback predefinito se un attributo è vuoto o nullo. Questo meccanismo funziona per gli attributi del profilo e gli eventi di Percorso.

**Sintassi**

```sql
Hello {%=profile.personalEmail.name.firstName ?: "there" %}!
```

In questo esempio, il valore `there` viene visualizzato se l&#39;attributo `firstName` di questo profilo è vuoto o nullo.

## Condizioni{#if-function}

L&#39;helper `if` viene utilizzato per definire un blocco condizionale.
Se la valutazione dell’espressione restituisce true, il blocco viene renderizzato, altrimenti viene saltato.

**Sintassi**

```sql
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

Dopo l&#39;helper `if`, è possibile immettere un&#39;istruzione `else` per specificare un blocco di codice da eseguire, se la stessa condizione è false.
L&#39;istruzione `elseif` specificherà una nuova condizione da verificare se la prima istruzione restituisce false.


**Formato**

```sql
{
    {
        {%#if condition1%} element_1 
        {%else if condition2%} element_2 
        {%else%} default_element 
        {%/if%}
    }
}
```

**Esempi**

1. **Eseguire il rendering di collegamenti archivio diversi in base alle espressioni condizionali**

   ```sql
   {%#if profile.homeAddress.countryCode = "FR"%}
   <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
   {%else%}
   <a href="https://www.somedomain.com/en">Checkout our catalogue</a>
   {%/if%}
   ```

1. **Determinare l&#39;estensione dell&#39;indirizzo di posta elettronica**

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **Aggiungere un collegamento condizionale**

   La seguente operazione aggiungerà un collegamento al sito Web &quot;www.adobe.com/academia&#39;&quot; solo per i profili con indirizzi e-mail &quot;edu&quot;, al sito Web &quot;www.adobe.com/org&#39;&quot; per i profili con indirizzi e-mail &quot;org&quot; e all’URL predefinito &quot;www.adobe.com/users&#39;&quot; per tutti gli altri profili:

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **Contenuto condizionale basato sull&#39;appartenenza al pubblico**

   ```sql
   {%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
   Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
   {%else if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"%}
   Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
   {%/if%}
   ```

>[!NOTE]
>
>Per ulteriori informazioni sui tipi di pubblico e sul servizio di segmentazione, consulta [questa sezione](../../audience/about-audiences.md).


## A meno che{#unless}

L&#39;helper `unless` viene utilizzato per definire un blocco condizionale. In opposizione all&#39;helper `if`, se la valutazione dell&#39;espressione restituisce false, viene eseguito il rendering del blocco.

**Sintassi**

```sql
{%#unless unlessCondition%} element_1 {%else%} default_element {%/unless%}
```

**Esempio**

Esegui il rendering di alcuni contenuti in base all’estensione dell’indirizzo e-mail:

```sql
{%#unless endsWith(profile.personalEmail.address, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content
{%/unless%}
```

## Ogni{#each}

L&#39;helper `each` viene utilizzato per eseguire l&#39;iterazione su un array.
La sintassi dell&#39;helper è ```{{#each ArrayName}}``` YourContent `{{/each}}`
È possibile fare riferimento ai singoli elementi array utilizzando la parola chiave **this** all&#39;interno del blocco. È possibile eseguire il rendering dell&#39;indice dell&#39;elemento dell&#39;array utilizzando `{{@index}}`.

**Sintassi**

```sql
{{#each profile.productsInCart}}
    <li>{{this.name}}</li>
{{/each}}
```

**Esempio**

```sql
{{#each profile.homeAddress.city}}
  {{@index}} : {{this}}<br>
{{/each}}
```

**Esempio**

Esegui il rendering di un elenco di prodotti che questo utente ha nel carrello:

```sql
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
{{/each}}
```

## Con{#with}

L&#39;helper `with` viene utilizzato per modificare il token di valutazione della parte modello.

**Sintassi**

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

L&#39;helper `with` è utile anche per definire una variabile di collegamento.

**Esempio**

Da utilizzare con per l’aliasing di nomi di variabili lunghi a nomi più brevi:

```sql
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```

## Let{#let}

La funzione `let` consente di archiviare un&#39;espressione come variabile da utilizzare successivamente in una query.

**Sintassi**

```sql
{% let variable = expression %} {{variable}}
```

**Esempio**

L&#39;esempio seguente consente di calcolare la somma totale dei prezzi dei prodotti nel carrello con prezzi compresi tra 100 e 1000.

```sql
{% let sum = 0%}
    {{#each profile.productsInCart as |p|}}
        {%#if p.price>100 and p.price<1000%}
            {%let sum = sum + p.price %}
        {%/if%}
    {{/each}}
{{sum}}
```

## Metadati di esecuzione {#execution-metadata}

>[!AVAILABILITY]
>
>Questa funzionalità è in disponibilità limitata. Per ottenere l’accesso, contatta il rappresentante Adobe.

L&#39;helper `executionMetadata` consente di acquisire e archiviare in modo dinamico coppie chiave-valore personalizzate nel contesto di esecuzione del messaggio.

**Sintassi**

```
{{executionMetadata key="your_key" value="your_value"}}
```

In questa sintassi, `key` fa riferimento al nome dei metadati e `value` sono i metadati da mantenere.

**Caso d’uso**

Con questa funzione, puoi aggiungere informazioni contestuali a qualsiasi azione nativa delle campagne o dei percorsi. Questo consente di esportare i dati contestuali di consegna in tempo reale verso sistemi esterni per vari scopi come il tracciamento, l’analisi, la personalizzazione e l’elaborazione a valle.

>[!NOTE]
>
>La funzione dei metadati di esecuzione non è supportata da [azioni personalizzate](../../action/action.md).

Ad esempio, puoi utilizzare l’helper dei metadati di esecuzione per aggiungere un ID specifico a ciascuna consegna inviata a ciascun profilo. Queste informazioni vengono generate durante il runtime e i metadati di esecuzione arricchiti possono quindi essere esportati per la riconciliazione a valle con una piattaforma di reporting esterna.

**Come funziona**

Seleziona qualsiasi elemento dal contenuto del canale all&#39;interno di una campagna o di un percorso e, utilizzando l&#39;editor di personalizzazione, aggiungi l&#39;helper `executionMetadata` a questo elemento.

>[!NOTE]
>
>La funzione Execution Metadata non è visibile quando viene visualizzato il contenuto stesso.


In fase di esecuzione, il valore dei metadati viene aggiunto al set di dati **[!UICONTROL Message Feedback Event]** esistente con la seguente aggiunta di schema:

```
"_experience": {
  "customerJourneyManagement": {
    "messageExecution": {
      "metadata": {
        "your_key": "your_value"
      }
    }
  }
}
```

>[!NOTE]
>
>Ulteriori informazioni sui set di dati in [questa sezione](../../data/get-started-datasets.md).

**Limitazione**

Esiste un limite massimo di 2 kb per le coppie chiave-valore per azione.

Se viene superato il limite di 2 KB, il messaggio viene comunque recapitato, ma è possibile troncare qualsiasi coppia di valori chiave.

**Esempio**

```
{{executionMetadata key="firstName" value=profile.person.name.firstName}}
```

In questo esempio, supponendo `profile.person.name.firstName` = &quot;Alex&quot;, l&#39;entità risultante è:

```
{
  "key": "firstName",
  "value": "Alex"
}
```

