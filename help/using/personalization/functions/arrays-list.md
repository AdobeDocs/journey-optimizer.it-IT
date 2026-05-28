---
title: Libreria funzioni array
description: Libreria funzioni array
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: dfe611fb-9c50-473c-9eb7-b983e1e6f01e
TQID: https://experienceleague.adobe.com/CUiT5GFH9o4q-oOSWuKC8ZyLbRbH9lj88M92LhMIX9E
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
feature_v2: id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2: []
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 742
ht-degree: 4%

---

# Funzioni array ed elenco {#arrays}

Utilizzare queste funzioni per semplificare l&#39;interazione con array, elenchi e stringhe.

## Conteggio solo nulle {#count-only-null}

La funzione `countOnlyNull` viene utilizzata per contare il numero di valori Null in un elenco.

**Sintassi**

```sql
{%= countOnlyNull(array) %}
```

**Esempio**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

Restituisce 3.

## Conteggio con valori Null {#count-with-null}

La funzione `countWithNull` viene utilizzata per contare tutti gli elementi di un elenco, inclusi i valori Null.

**Sintassi**

```sql
{%= countWithNull(array) %}
```

**Esempio**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

Restituisce 6.

## Distinct{#distinct}

La funzione `distinct` viene utilizzata per ottenere valori da un array o da un elenco con valori duplicati rimossi.

**Sintassi**

```sql
{%= distinct(array) %}
```

**Esempio**

L&#39;operazione seguente specifica gli utenti che hanno effettuato ordini in più di un negozio.

```sql
{%= distinct(person.orders.storeId).count() > 1 %}
```

## Conteggio distinto con valore null {#distinct-count-with-null}

La funzione `distinctCountWithNull` viene utilizzata per contare il numero di valori diversi in un elenco, inclusi i valori Null.

**Sintassi**

```sql
{%= distinctCountWithNull(array) %}
```

**Esempio**

```sql
{%= distinctCountWithNull([10,2,10,null]) %}
```

Restituisce 3.

## Primo elemento{#head}

La funzione `head` viene utilizzata per restituire il primo elemento di un array o di un elenco.

**Sintassi**

```sql
{%= head(array) %}
```

**Esempio**

L&#39;operazione seguente restituisce il primo dei primi cinque ordini con il prezzo più alto. Ulteriori informazioni sulla funzione `topN` sono disponibili nella sezione [first `n` in array](#first-n).

```sql
{%= head(topN(orders,price, 5)) %}
```

## Ordinare e ottenere il primo N nell’array {#first-n}

La funzione `topN` ordina una matrice in ordine decrescente in base all&#39;espressione numerica specificata e restituisce i primi `N` elementi. Se la dimensione dell&#39;array è inferiore a `N`, restituisce l&#39;intero array ordinato.

Questa funzione
**Sintassi**

```sql
{%= topN(array, value, amount) %}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{ARRAY}` | Matrice o elenco da ordinare. |
| `{VALUE}` | Proprietà in cui ordinare l&#39;array o l&#39;elenco. |
| `{AMOUNT}` | Il numero di elementi da restituire. |

**Esempio**

L&#39;operazione seguente restituisce i primi cinque ordini con il prezzo più basso.

```sql
{%= topN(orders,price, 5) %}
```

## In entrata{#in}

La funzione `in` viene utilizzata per determinare se un elemento è membro di un array o di un elenco.

**Sintassi**

```sql
{%= in(value, array) %}
```

**Esempio**

L’operazione seguente definisce le persone il cui compleanno cade in marzo, giugno o settembre.

```sql
{%= in (person.birthMonth, [3, 6, 9]) %}
```

## Include{#includes}

La funzione `includes` viene utilizzata per determinare se un array o un elenco contiene un dato elemento.

**Sintassi**

```sql
{%= includes(array,item) %}
```

**Esempio**

L&#39;operazione seguente definisce le persone il cui colore preferito include il rosso.

```sql
{%= includes(person.favoriteColors,"red") %}
```

## Intersects{#intersects}

La funzione `intersects` viene utilizzata per determinare se due array o elenchi hanno almeno un membro comune.

**Sintassi**

```sql
{%= intersects(array1, array2) %}
```

**Esempio**

L&#39;operazione seguente definisce le persone i cui colori preferiti includono almeno uno rosso, blu o verde.

```sql
{%= intersects(person.favoriteColors,["red", "blue", "green"]) %}
```


<!--
## Intersection{#intersection}

The `intersection` function is used to determine the common members of two arrays or lists.

**Syntax**

```sql
intersection({ARRAY},{ARRAY})
```

**Example**

The following operation defines if person 1 and person 2 both have favorite colors of red, blue, and green.

```sql
intersection(person1.favoriteColors,person2.favoriteColors) = ["red", "blue", "green"]
```
-->

## Ordina e ottieni l’ultimo N nell’array {#last-n}

La funzione `bottomN` ordina una matrice in ordine crescente in base all&#39;espressione numerica specificata e restituisce i primi `N` elementi. Se la dimensione dell&#39;array è inferiore a `N`, restituisce l&#39;intero array ordinato.

**Sintassi**

```sql
{%= bottomN(array, value, amount) %}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{ARRAY}` | Matrice o elenco da ordinare. |
| `{VALUE}` | Proprietà in cui ordinare l&#39;array o l&#39;elenco. |
| `{AMOUNT}` | Il numero di elementi da restituire. |

**Esempio**

L&#39;operazione seguente restituisce gli ultimi cinque ordini con il prezzo più alto.

```sql
{%= bottomN(orders,price, 5) %}
```

## Non in{#notin}

La funzione `notIn` viene utilizzata per determinare se un elemento non è un membro di un array o di un elenco.

>[!NOTE]
>
>La funzione `notIn` *also* assicura che nessuno dei due valori sia uguale a null. Pertanto, i risultati non sono una negazione esatta della funzione `in`.

**Sintassi**

```sql
{%= notIn(value, array) %}
```

**Esempio**

L’operazione seguente definisce le persone il cui compleanno non è in marzo, giugno o settembre.

```sql
{%= notIn(person.birthMonth ,[3, 6, 9]) %}
```


## Sottoinsieme di{#subset}

La funzione `subsetOf` viene utilizzata per determinare se un array specifico (array A) è un sottoinsieme di un altro array (array B). In altre parole, che tutti gli elementi nell&#39;array A sono elementi dell&#39;array B.

**Sintassi**

```sql
{%= subsetOf(array1, array2) %}
```

**Esempio**

L&#39;operazione seguente definisce le persone che hanno visitato tutte le loro città preferite.

```sql
{%= subsetOf(person.favoriteCities,person.visitedCities) %}
```

## Soprainsieme di{#superset}

La funzione `supersetOf` viene utilizzata per determinare se un array specifico (array A) è un superset di un altro array (array B). In altre parole, l’array A contiene tutti gli elementi dell’array B.

**Sintassi**

```sql
{%= supersetOf(array1, array2) %}
```

**Esempio**

L’operazione seguente definisce le persone che hanno mangiato sushi e pizza almeno una volta.

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"]) %}
```

## Iterazione su un array {#each-loop}

Utilizza Handlebars `{{#each}}` block helper per eseguire il loop su un array ed eseguire il rendering del contenuto per ogni elemento in **contenuto personalizzato** (e-mail, SMS, push).

>[!NOTE]
>
>`{{#each}}` è disponibile solo nell&#39;**editor di personalizzazione** (contenuto e-mail, SMS, contenuto push). **non** è supportato nell&#39;attività condizione percorso. Per filtrare o associare gli elementi di un array all&#39;interno di una condizione di percorso, utilizzare [funzioni di gestione della raccolta](../../building-journeys/expression/collection-management-functions.md).

**Sintassi**

```handlebars
{{#each arrayAttribute}}
  {{this}}
{{/each}}
```

+++Esempio — Elenca tutti gli elementi di un array

```handlebars
{{#each profile.purchases.items}}
  - {{this.name}}: {{this.price}}€
{{/each}}
```

Output (esempio):

```
- Running shoes: 89€
- Water bottle: 15€
- Gym bag: 45€
```

+++

+++Esempio — accedere all&#39;indice del ciclo

Utilizza `@index` per accedere alla posizione del ciclo corrente (basata su 0):

```handlebars
{{#each profile.preferences.languages}}
  {{@index}}: {{this}}
{{/each}}
```

Output (esempio):

```
0: English
1: French
2: Spanish
```

+++

+++Esempio — Rendering condizionale all&#39;interno di un loop

Utilizza il blocco `{%#if%}` in `{{#each}}` per eseguire il rendering del contenuto solo quando viene soddisfatta una condizione:

>[!NOTE]
>
>`{% if %}` / `{% endif %}` non sono supportati. Utilizza invece `{%#if%}` / `{%/if%}`. Inoltre, `this.<field>` non funziona all&#39;interno di espressioni di condizione di PQL. Fare riferimento al campo direttamente utilizzando il nome attributo (ad esempio `order.status`).

```handlebars
{{#each profile.orders as |order|}}
  {%#if order.status = "pending"%}
  Your order {{order.id}} is still pending.
  {%/if%}
{{/each}}
```

Si tratta del modello consigliato per simulare un &quot;break on condition&quot;: solo gli elementi che corrispondono alla condizione producono output.

+++
