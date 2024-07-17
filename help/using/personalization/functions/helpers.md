---
title: Helper
description: Helper
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: b08dc0f8-c85f-4aca-85eb-92dc76b0e588
source-git-commit: 7e7ff2f6451947d4d52efb2963d940ba3f50819f
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 5%

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
   {%else%} if 'profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"'%}
   Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
   {%/if%}
   ```

>[!NOTE]
>
>Per ulteriori informazioni sui tipi di pubblico e sul servizio di segmentazione, consulta questa [sezione](../../audience/about-audiences.md).


## Unless{#unless}

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
Some edu specific content Content
{%/unless%}
```

## Each{#each}

L&#39;helper `each` viene utilizzato per eseguire l&#39;iterazione su un array.
La sintassi dell&#39;helper è ```{{#each ArrayName}}``` YourContent {{/each}}
È possibile fare riferimento ai singoli elementi array utilizzando la parola chiave **this** all&#39;interno del blocco. È possibile eseguire il rendering dell&#39;indice dell&#39;elemento dell&#39;array utilizzando {{@index}}.

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

Esegui il rendering di un elenco di prodotti che questo utente ha nel carrello:

```sql
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
   </br>
{{/each}}
```

## With{#with}

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
