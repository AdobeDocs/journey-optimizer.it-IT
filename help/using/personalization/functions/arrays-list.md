---
title: Libreria funzioni
description: Libreria funzioni
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '535'
ht-degree: 5%

---

# Array e funzioni elenco {#arrays}

![](../../assets/do-not-localize/badge.png)

[!DNL Profile Query Language] (PQL) offre funzioni che semplificano l’interazione con array, elenchi e stringhe.

## In

La funzione `in` viene utilizzata per determinare se un elemento è membro di una matrice o di un elenco.

**Formato**

```sql
in ({VALUE},{ARRAY})
```

**Esempio**

La seguente query PQL definisce le persone con i compleanni a marzo, giugno o settembre.

```sql
in (person.birthMonth, [3, 6, 9])
```

## Non in

La funzione `notIn` viene utilizzata per determinare se un elemento non è membro di una matrice o di un elenco.

>[!NOTE]
>
>La funzione `notIn` *anche* assicura che nessuno dei due valori sia uguale a null. Pertanto, i risultati non sono una negazione esatta della funzione `in`.

**Formato**

```sql
notIn ({VALUE},{ARRAY})
```

**Esempio**

La seguente query PQL definisce le persone con compleanni che non si trovano a marzo, giugno o settembre.

```sql
notIn (person.birthMonth ,[3, 6, 9])
```

## Intersecazioni

La funzione `intersects` viene utilizzata per determinare se due array o elenchi hanno almeno un membro comune.

**Formato**

```sql
intersects({ARRAY},{ARRAY})
```

**Esempio**

La seguente query PQL definisce le persone i cui colori preferiti includono almeno uno di rosso, blu o verde.

```sql
intersects(person.favoriteColors,["red", "blue", "green"])
```

## Intersection

La funzione `intersection` viene utilizzata per determinare i membri comuni di due array o elenchi.

**Formato**

```sql
intersection({ARRAY},{ARRAY})
```

**Esempio**

La seguente query PQL definisce se la persona 1 e la persona 2 hanno entrambi i colori preferiti di rosso, blu e verde.

```sql
intersection(person1.favoriteColors,person2.favoriteColors) = ["red", "blue", "green"]
```

## Sottoinsieme di

La funzione `subsetOf` viene utilizzata per determinare se un array specifico (array A) è un sottoinsieme di un altro array (array B). In altre parole, tutti gli elementi dell&#39;array A sono elementi dell&#39;array B.

**Formato**

```sql
subsetOf({ARRAY},{ARRAY})
```

**Esempio**

La seguente query PQL definisce le persone che hanno visitato tutte le loro città preferite.

```sql
subsetOf(person.favoriteCities,person.visitedCities)
```

## Superset di

La funzione `supersetOf` viene utilizzata per determinare se un array specifico (array A) è un superset di un altro array (array B). In altre parole, l&#39;array A contiene tutti gli elementi dell&#39;array B.

**Formato**

```sql
supersetOf({ARRAY},{ARRAY})
```

**Esempio**

La seguente query PQL definisce le persone che hanno mangiato sushi e pizza almeno una volta.

```sql
supersetOf(person.eatenFoods,["sushi", "pizza"])
```

## Include

La funzione `includes` viene utilizzata per determinare se una matrice o un elenco contiene un elemento specificato.

**Formato**

```sql
includes({ARRAY},{ITEM})
```

**Esempio**

La seguente query PQL definisce le persone il cui colore preferito include il rosso.

```sql
includes(person.favoriteColors,"red")
```

## Distinto

La funzione `distinct` viene utilizzata per rimuovere i valori duplicati da una matrice o da un elenco.

**Formato**

```sql
distinct({ARRAY})
```

**Esempio**

La seguente query PQL specifica le persone che hanno effettuato ordini in più di un archivio.

```sql
distinct(person.orders.storeId).count() > 1
```

## Primo `n` nella matrice {#first-n}

La funzione `topN` viene utilizzata per restituire i primi `N` elementi di un array, se ordinati in ordine crescente in base all&#39;espressione numerica specificata.

**Formato**

```sql
topN({ARRAY},{VALUE}, {AMOUNT})
```

| Argomento | Descrizione |
| --------- | ----------- |
| `{ARRAY}` | Matrice o elenco da ordinare. |
| `{VALUE}` | Proprietà in cui ordinare la matrice o l&#39;elenco. |
| `{AMOUNT}` | Numero di elementi da restituire. |

**Esempio**

La seguente query PQL restituisce i primi cinque ordini con il prezzo più alto.

```sql
topN(orders,price, 5)
```

## Ultimo `n` nella matrice

La funzione `bottomN` viene utilizzata per restituire gli ultimi `N` elementi di un array, se ordinati in ordine crescente in base all&#39;espressione numerica specificata.

**Formato**

```sql
bottomN({ARRAY},{VALUE}, {AMOUNT})
```

| Argomento | Descrizione |
| --------- | ----------- | 
| `{ARRAY}` | Matrice o elenco da ordinare. |
| `{VALUE}` | Proprietà in cui ordinare la matrice o l&#39;elenco. |
| `{AMOUNT}` | Numero di elementi da restituire. |

**Esempio**

La seguente query PQL restituisce i primi cinque ordini con il prezzo più basso.

```sql
bottomN(orders,price, 5)
```

## Primo elemento

La funzione `head` viene utilizzata per restituire il primo elemento della matrice o dell&#39;elenco.

**Formato**

```sql
head({ARRAY})
```

**Esempio**

La seguente query PQL restituisce il primo dei primi cinque ordini con il prezzo più alto. Ulteriori informazioni sulla funzione `topN` sono disponibili nella sezione [first `n` in array](#first-n) .

```sql
head(topN(orders,price, 5))
```
