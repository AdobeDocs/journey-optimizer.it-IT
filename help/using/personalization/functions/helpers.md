---
title: Helper
description: Helper
feature: Personalizzazione
topic: Personalizzazione
role: Data Engineer
level: Experienced
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 4%

---


# Helper {#gs-helpers}

## Condizioni{#if-function}

L’ `if` helper viene utilizzato per definire un blocco condizionale.
Se la valutazione dell’espressione restituisce true, il blocco viene sottoposto a rendering in caso contrario viene ignorato.

**Sintassi**

```sql
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

In seguito all&#39;helper `if`, è possibile immettere un&#39;istruzione `else` per specificare un blocco di codice da eseguire, se la stessa condizione è falsa.
L’istruzione `elseif` specifica una nuova condizione per eseguire il test se la prima istruzione restituisce false.


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

1. **Eseguire il rendering di diversi collegamenti all’archivio in base a espressioni condizionali**

   ```sql
   {%#if profile.homeAddress.countryCode = "FR"%}
   <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
   {%else%}
   <a href="https://www.somedomain.com/en">Checkout our catalogue</a>
   {%/if%}
   ```

1. **Determinare l’estensione dell’indirizzo e-mail**

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

   La seguente operazione aggiunge un collegamento al sito web &quot;www.adobe.com/academia&#39;&quot; per i profili con indirizzi e-mail solo &#39;.edu&#39;, al sito web &quot;www.adobe.com/org&#39; per i profili con indirizzi e-mail &#39;.org&quot; e all’URL predefinito &quot;www.adobe.com/users&#39;&quot; per tutti gli altri profili:

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **Contenuto condizionale in base all’appartenenza al segmento**

   ```sql
   {%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
   Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
   {%else%} if 'profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"'%}
   Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
   {%/if%}
   ```

1. **Determinare se un profilo è già un membro**

   ```sql
   {%#if profile.segmentMembership.get(segments.`123e4567-e89b-12d3-a456-426614174000`.id)%}
       You're a member!
   {%else%}
       You should be a member! Sign up now!
   {%/if%}
   ```

>[!NOTE]
>
>Per ulteriori informazioni sul servizio di segmentazione e segmentazione, consulta questa [sezione](../../segment/about-segments.md).


## A meno che{#unless}

L’ `unless` helper viene utilizzato per definire un blocco condizionale. In opposizione all&#39;helper `if`, se la valutazione dell&#39;espressione restituisce false, viene eseguito il rendering del blocco.

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
Some edu specific content Content
{%/unless%}
```

## Ogni{#each}

L&#39;helper `each` viene utilizzato per eseguire iterazioni su un array.
La sintassi dell&#39;helper è ```{{#each ArrayName}}``` YourContent {{/each}}
Possiamo fare riferimento ai singoli elementi dell&#39;array utilizzando la parola chiave **this** all&#39;interno del blocco. È possibile eseguire il rendering dell&#39;indice dell&#39;elemento dell&#39;array utilizzando {{@index}}.

**Sintassi**

```sql
{{#each profile.productsInCart}}
    <li>{{this.name}}</li>
    </br>
{{/each}}
```

**Esempio**

```sql
{{#each profile.homeAddress.city}}
  {{@index}} : {{this}}<br>
{{/each}}
```

**Esempio**

Esegui il rendering di un elenco di prodotti di cui dispone questo utente nel carrello:

```sql
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
   </br>
{{/each}}
```

## Con{#with}

L’ `with` helper viene utilizzato per modificare il token di valutazione della parte modello.

**Sintassi**

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

L’ `with` helper è utile per definire anche una variabile di scelta rapida.

**Esempio**

Utilizzare con per assegnare i nomi di variabili lunghe a nomi più brevi:

```sql
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```

## Lasciare{#let}

La funzione `let` consente di memorizzare un’espressione come variabile da utilizzare successivamente in una query.

**Sintassi**

```sql
{% let variable = expression %} {{variable}}
```

**Esempio**

L&#39;esempio seguente consente a tutte le somme dei totali di prodotto con la transazione in USD se la somma è maggiore di $100 e inferiore a $1000.

```sql
{% let variable = expression %} {{variable}}
```
