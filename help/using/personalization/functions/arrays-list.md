---
title: Libreria di funzioni di array
description: Libreria di funzioni di array
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: dfe611fb-9c50-473c-9eb7-b983e1e6f01e
source-git-commit: 91f221781f1655066ec0f6b1c3f2c1faefd09d69
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 6%

---

# Funzioni array ed elenco {#arrays}

Utilizza queste funzioni per semplificare l’interazione con array, elenchi e stringhe.

## Conteggio solo null {#count-only-null}

La `countOnlyNull` viene utilizzato per contare il numero di valori nulli in un elenco.

**Formato**

```sql
{%= countOnlyNull(array) %}
```

**Esempio**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

Restituisce 3.

## Conteggio con Null {#count-with-null}

La `countWithNull` viene utilizzata per contare tutti gli elementi di un elenco, inclusi i valori nulli.

**Formato**

```sql
{%= countWithNull(array) %}
```

**Esempio**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

Restituisce 6.

## Distinto{#distinct}

La `distinct` viene utilizzata per ottenere i valori da una matrice o da un elenco con i valori duplicati rimossi.

**Formato**

```sql
{%= distinct(array) %}
```

**Esempio**

L&#39;operazione seguente specifica le persone che hanno effettuato ordini in più store.

```sql
{%= distinct(person.orders.storeId).count() > 1 %}
```

## Conteggio Distinto Con Null {#distinct-count-with-null}

La `distinctCountWithNull` viene utilizzata per contare il numero di valori diversi in un elenco, inclusi i valori nulli.

**Formato**

```sql
{%= distinctCountWithNull(array) %}
```

**Esempio**

```sql
{%= distinctCountWithNull([10,2,10,null]) %}
```

Restituisce 3.

## Primo elemento{#head}

La `head` viene utilizzata per restituire il primo elemento di una matrice o di un elenco.

**Formato**

```sql
{%= head(array) %}
```

**Esempio**

L&#39;operazione seguente restituisce il primo dei primi cinque ordini con il prezzo più alto. Ulteriori informazioni sulle `topN` si trova nella [first `n` in matrice](#first-n) sezione .

```sql
{%= head(topN(orders,price, 5)) %}
```

## Primo `n` in matrice {#first-n}

La `topN` viene utilizzata per restituire il primo `N` elementi in una matrice, se ordinati in ordine crescente in base all&#39;espressione numerica specificata.

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

L&#39;operazione seguente restituisce i primi cinque ordini con il prezzo più basso.

```sql
{%= topN(orders,price, 5) %}
```

## In{#in}

La `in` viene utilizzata per determinare se un elemento è membro di una matrice o di un elenco.

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

La `includes` viene utilizzata per determinare se una matrice o un elenco contiene un elemento specificato.

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

La `intersects` viene utilizzata per determinare se due array o elenchi hanno almeno un membro comune.

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

## Ultimo `n` in matrice{#last-n}

La `bottomN` viene utilizzata per restituire l&#39;ultima `N` elementi in una matrice, se ordinati in ordine crescente in base all&#39;espressione numerica specificata.

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

L&#39;operazione seguente restituisce gli ultimi cinque ordini con il prezzo più alto.

```sql
{%= bottomN(orders,price, 5) %}
```

## Non in{#notin}

La `notIn` viene utilizzata per determinare se un elemento non è membro di una matrice o di un elenco.

>[!NOTE]
>
>La `notIn` Funzione *anche* assicura che nessuno dei due valori sia uguale a null. Pertanto, i risultati non sono una negazione esatta del `in` funzione .

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

La `subsetOf` viene utilizzata per determinare se un array specifico (array A) è un sottoinsieme di un altro array (array B). In altre parole, tutti gli elementi dell&#39;array A sono elementi dell&#39;array B.

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

La `supersetOf` viene utilizzata per determinare se un array specifico (array A) è un superset di un altro array (array B). In altre parole, l&#39;array A contiene tutti gli elementi dell&#39;array B.

**Formato**

```sql
{%= supersetOf(array1, array2) %}
```

**Esempio**

L&#39;operazione seguente definisce le persone che hanno mangiato sushi e pizza almeno una volta.

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"] %}
```
