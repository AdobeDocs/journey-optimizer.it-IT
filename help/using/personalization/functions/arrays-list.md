---
title: Libreria di funzioni di array
description: Libreria di funzioni di array
feature: Personalizzazione
topic: Personalizzazione
role: Data Engineer
level: Experienced
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 5%

---

# Array e funzioni elenco {#arrays}

![](../../assets/do-not-localize/badge.png)

Utilizza queste funzioni per semplificare l’interazione con array, elenchi e stringhe.

## Distinto{#distinct}

La funzione `distinct` viene utilizzata per ottenere valori da una matrice o da un elenco con valori duplicati rimossi.

**Formato**

```sql
{%= distinct(array) %}
```

**Esempio**

L&#39;operazione seguente specifica le persone che hanno effettuato ordini in più store.

```sql
{%= distinct(person.orders.storeId).count() > 1 %}
```

## Primo elemento{#head}

La funzione `head` viene utilizzata per restituire il primo elemento della matrice o dell&#39;elenco.

**Formato**

```sql
{%= head({array}) %}
```

**Esempio**

L&#39;operazione seguente restituisce il primo dei primi cinque ordini con il prezzo più alto. Ulteriori informazioni sulla funzione `topN` sono disponibili nella sezione [first `n` in array](#first-n) .

```sql
{%= head(topN(orders,price, 5)) %}
```

## Primo `n` nella matrice {#first-n}

La funzione `topN` viene utilizzata per restituire i primi `N` elementi di un array, se ordinati in ordine crescente in base all&#39;espressione numerica specificata.

**Formato**

```sql
{%= topN(array, value, amount) %}
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{ARRAY}` | Matrice o elenco da ordinare. |
| `{VALUE}` | Proprietà in cui ordinare la matrice o l&#39;elenco. |
| `{AMOUNT}` | Numero di elementi da restituire. |

**Esempio**

L&#39;operazione seguente restituisce i primi cinque ordini con il prezzo più alto.

```sql
{%= topN(orders,price, 5) %}
```

## In{#in}

La funzione `in` viene utilizzata per determinare se un elemento è membro di una matrice o di un elenco.

**Formato**

```sql
{%= in(value, array) %}
```

**Esempio**

L&#39;operazione seguente definisce le persone con compleanni a marzo, giugno o settembre.

```sql
{%= in (person.birthMonth, [3, 6, 9]) %}
```

## Include{#includes}

La funzione `includes` viene utilizzata per determinare se una matrice o un elenco contiene un elemento specificato.

**Formato**

```sql
{%= includes(array,item) %}
```

**Esempio**

L’operazione seguente definisce le persone il cui colore preferito include il rosso.

```sql
{%= includes(person.favoriteColors,"red") %}
```

## Intersecazioni{#intersects}

La funzione `intersects` viene utilizzata per determinare se due array o elenchi hanno almeno un membro comune.

**Formato**

```sql
{%= intersects(array1, array2) %}
```

**Esempio**

L’operazione seguente definisce le persone i cui colori preferiti includono almeno uno di rosso, blu o verde.

```sql
{%= intersects(person.favoriteColors,["red", "blue", "green"]) %}
```


<!-- ## Intersection{#intersection}

The `intersection` function is used to determine the common members of two arrays or lists.

**Format**

```sql
intersection({ARRAY},{ARRAY})
```

**Example**

The following operation defines if person 1 and person 2 both have favorite colors of red, blue, and green.

```sql
intersection(person1.favoriteColors,person2.favoriteColors) = ["red", "blue", "green"]
```
-->

## Ultimo `n` nell&#39;array{#last-n}

La funzione `bottomN` viene utilizzata per restituire gli ultimi `N` elementi di un array, se ordinati in ordine crescente in base all&#39;espressione numerica specificata.

**Formato**

```sql
{%= bottomN(array, value, amount) %}
```

| Argomento | Descrizione |
| --------- | ----------- | 
| `{ARRAY}` | Matrice o elenco da ordinare. |
| `{VALUE}` | Proprietà in cui ordinare la matrice o l&#39;elenco. |
| `{AMOUNT}` | Numero di elementi da restituire. |

**Esempio**

L&#39;operazione seguente restituisce i primi cinque ordini con il prezzo più basso.

```sql
{%= bottomN(orders,price, 5) %}
```


## Non in{#notin}

La funzione `notIn` viene utilizzata per determinare se un elemento non è membro di una matrice o di un elenco.

>[!NOTE]
>
>La funzione `notIn` *anche* assicura che nessuno dei due valori sia uguale a null. Pertanto, i risultati non sono una negazione esatta della funzione `in`.

**Formato**

```sql
{%= notIn(value, array) %}
```

**Esempio**

L&#39;operazione seguente definisce le persone con compleanni che non sono in marzo, giugno o settembre.

```sql
{%= notIn(person.birthMonth ,[3, 6, 9]) %}
```


## Sottoinsieme di{#subset}

La funzione `subsetOf` viene utilizzata per determinare se un array specifico (array A) è un sottoinsieme di un altro array (array B). In altre parole, tutti gli elementi dell&#39;array A sono elementi dell&#39;array B.

**Formato**

```sql
{%= subsetOf(array1, array2) %}
```

**Esempio**

L’operazione seguente definisce le persone che hanno visitato tutte le loro città preferite.

```sql
{%= subsetOf(person.favoriteCities,person.visitedCities) %}
```

## Superset di{#superset}

La funzione `supersetOf` viene utilizzata per determinare se un array specifico (array A) è un superset di un altro array (array B). In altre parole, l&#39;array A contiene tutti gli elementi dell&#39;array B.

**Formato**

```sql
{%= supersetOf(array1, array2) %}
```

**Esempio**

L&#39;operazione seguente definisce le persone che hanno mangiato sushi e pizza almeno una volta.

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"] %}
```







