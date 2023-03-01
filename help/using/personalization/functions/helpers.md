---
title: Assistenza
description: Assistenza
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: b08dc0f8-c85f-4aca-85eb-92dc76b0e588
source-git-commit: 22752a30fef53808fa9deb80a2053d5bc22abc95
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 4%

---

# Assistenza {#gs-helpers}

## Valore di fallback predefinito{#default-value}

Il `Default Fallback Value` helper viene utilizzato per restituire un valore di fallback predefinito se un attributo è vuoto o nullo. Questo meccanismo funziona per gli attributi del profilo e gli eventi di Percorso.

**Sintassi**

```sql
Hello {%=profile.personalEmail.name.firstName ?: "there" %}!
```

In questo esempio, il valore `there` viene visualizzato se `firstName` l&#39;attributo di questo profilo è vuoto o nullo.

## Condizioni{#if-function}

Il `if` helper viene utilizzato per definire un blocco condizionale.
Se la valutazione dell’espressione restituisce true, il blocco viene renderizzato, altrimenti viene saltato.

**Sintassi**

```sql
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

Dopo il `if` helper, puoi immettere un `else` per specificare un blocco di codice da eseguire, se la stessa condizione è false.
Il `elseif` L&#39;istruzione specificherà una nuova condizione da verificare se la prima istruzione restituisce false.


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

1. **Eseguire il rendering di diversi collegamenti store in base alle espressioni condizionali**

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

1. **Contenuto condizionale basato sull’iscrizione al segmento**

   ```sql
   {%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
   Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
   {%else%} if 'profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"'%}
   Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
   {%/if%}
   ```

>[!NOTE]
>
>Per ulteriori informazioni sulla segmentazione e sul servizio di segmentazione, consulta questa pagina [sezione](../../segment/about-segments.md).


## A meno che{#unless}

Il `unless` helper viene utilizzato per definire un blocco condizionale. In opposizione alla proposta `if`  helper, se la valutazione dell’espressione restituisce false, viene eseguito il rendering del blocco.

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

Il `each` helper viene utilizzato per eseguire iterazioni su un array.
La sintassi dell’helper è ```{{#each ArrayName}}``` Contenuto {{/each}}
È possibile fare riferimento ai singoli elementi array utilizzando la parola chiave **questo** all&#39;interno del blocco. È possibile eseguire il rendering dell’indice dell’elemento dell’array utilizzando {{@index}}.

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

## Con{#with}

Il `with` helper viene utilizzato per modificare il token di valutazione della parte modello.

**Sintassi**

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

Il `with` helper è utile anche per definire una variabile di scelta rapida.

**Esempio**

Da utilizzare con per l’aliasing di nomi di variabili lunghi a nomi più brevi:

```sql
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```

## Let{#let}

Il `let` consente di memorizzare un’espressione come variabile da utilizzare successivamente in una query.

**Sintassi**

```sql
{% let variable = expression %} {{variable}}
```

**Esempio**

L&#39;esempio seguente consente di calcolare tutte le somme dei totali dei prodotti con la transazione in USD se la somma è maggiore di 100 $ e minore di 1000 $.

```sql
{% let variable = expression %} {{variable}}
```
