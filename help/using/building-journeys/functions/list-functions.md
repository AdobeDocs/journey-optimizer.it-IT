---
product: journey optimizer
title: Elencare funzioni
description: Informazioni sulle funzioni elenco
feature: Journeys
role: Developer
level: Experienced
keywords: elenco, funzioni, espressione, percorso, matrice, raccolta
version: Journey Orchestration
source-git-commit: 0331f8fe2439d41c08ad88a6d0bd95dd150bab90
workflow-type: tm+mt
source-wordcount: '1144'
ht-degree: 9%

---

# Elencare funzioni {#list-functions}

Le funzioni elenco consentono di manipolare e utilizzare insiemi di valori all’interno delle espressioni di percorso. Queste funzioni sono essenziali per filtrare, ordinare, trasformare e analizzare array ed elenchi nei percorsi dei clienti.

Utilizza le funzioni elenco quando devi:

* Filtrare ed estrarre elementi specifici dalle raccolte in base a criteri
* Ordinare e organizzare gli elementi dell’elenco in ordine crescente o decrescente
* Rimuovi i duplicati e ottieni valori univoci dagli elenchi
* Verifica se i valori esistono nelle raccolte
* Limita il numero di elementi restituiti da un elenco
* Trasformare gli elenchi in diversi formati o tipi di dati
* Eseguire operazioni sui set come la ricerca di elementi comuni tra gli elenchi

Le funzioni elenco forniscono potenti strumenti per l’utilizzo di strutture di dati complesse, consentendo una sofisticata manipolazione dei dati e una logica condizionale basata sui contenuti della raccolta.

## distinct {#distinct}

Restituisce i valori o gli oggetti distinti di un elenco specifico. Le voci Null vengono ignorate.

+++Sintassi

`distinct(<parameters>)`

+++

+++Parametri

| Parametro | Tipo | Descrizione |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly o listObject | Elenco da elaborare. Per listObject, deve essere un riferimento di campo. |
| keyAttributeName | stringa | Questo parametro è facoltativo e solo per listObject. Se il parametro non viene fornito, un oggetto viene considerato duplicato se tutti gli attributi hanno gli stessi valori. In caso contrario, un oggetto viene considerato duplicato se l’attributo specificato ha lo stesso valore. |

+++

+++Firme e tipi restituiti

`distinct(<listInteger>)`

Restituisce un elenco di numeri interi.

`distinct(<listDecimal>)`

Restituisce un elenco di decimali.

`distinct(<listString>)`

Restituisce un elenco di stringhe.

`distinct(<listDateTimeOnly>)`

Restituisce un elenco di date senza considerare il fuso orario.

`distinct(<listDateTime>)`

Restituisce un elenco di date.

`distinct(<listDateOnly>)`

Restituisce un elenco di date.

`distinct(<listBoolean>)`

Restituisce un elenco di booleani.

`distinct(<listDuration>)`

Restituisce un elenco di durate.

`distinct(<listObject>)`

`distinct(<listObject>,<string>)`

Restituisce un elenco di oggetti.

+++

+++Esempi

`distinct([10,2,10,null])`

Restituisce `[10, 2]`.

+++

## distinctWithNull {#distinctWithNull}

Restituisce i valori o gli oggetti distinti di un elenco specifico. Se l&#39;elenco include almeno una voce Null, nell&#39;elenco restituito sarà presente una voce Null.

+++Sintassi

`distinctWithNull(<parameters>)`

+++

+++Parametri

| Parametro | Tipo | Descrizione |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly | Elenco da elaborare. |

+++

+++Firme e tipi restituiti

`distinctWithNull(<listInteger>)`

Restituisce un elenco di numeri interi.

`distinctWithNull(<listDecimal>)`

Restituisce un elenco di decimali.

`distinctWithNull(<listString>)`

Restituisce un elenco di stringhe.

`distinctWithNull(<listDateTimeOnly>)`

Restituisce un elenco di date senza considerare il fuso orario.

`distinctWithNull(<listDateTime>)`

Restituisce un elenco di date.

`distinctWithNull(<listDateOnly>)`

Restituisce un elenco di date.

`distinctWithNull(<listBoolean>)`

Restituisce un elenco di booleani.

`distinctWithNull(<listDuration>)`

Restituisce un elenco di durate.

+++

+++Esempi

`distinctWithNull([10,2,10,null])`

Restituisce [10, 2, null]

+++

**Nota:** Il parametro `<listObject>` non è supportato in questa funzione.

## filter {#filter}

Restituisce un oggetto listObject con oggetti il cui attributo chiave corrisponde a uno dei valori chiave specificati.

+++Sintassi

`filter(<parameters>)`

+++

+++Parametri

| Parametro | Tipo | Descrizione |
|-----------|------------------|------------------|
| listToFilter | listObject | elenco di oggetti da filtrare. Deve essere un riferimento di campo. |
| keyAttributeName | stringa | nome attributo negli oggetti dell’elenco specificato, utilizzato come chiave per il filtro |
| keyValueList | list | array di valori chiave per il filtro |

+++

+++Firme e tipi restituiti

`filter(listObject, string, listString)`

`filter(listObject, string, listInteger)`

`filter(listObject, string, listDecimal)`

`filter(listObject, string, listDateTime)`

`filter(listObject, string, listDateTimeOnly)`

`filter(listObject, string, listDateOnly)`

`filter(listObject, string, listDuration)`

`filter(listObject, string, listBoolean)`

Restituisce un oggetto listObject.

+++

+++Esempi

Ecco un esempio di payload passato in un evento in ingresso &quot;myevent&quot;:

```json
"productListItems": [{
   "id": "product1",
   "name": "the product 1",
   "price": 20
},{
   "id": "product2",
   "name": "the product 2",
   "price": 30
},{
   "id": "product3",
   "name": "the product 3",
   "price": 50
}]
```

È possibile utilizzare la seguente espressione:

```json
filter(
 @event{myevent.productListItems},
 "id", 
 ["product2", "product3", "product4"]
)
```

Restituisce un oggetto listObject contenente i due oggetti con &quot;product2&quot; e &quot;product3&quot; come id.

+++

## getListItem {#getListItem}

Restituisce l&#39;elemento dell&#39;elenco in corrispondenza dell&#39;indice specificato.

+++Sintassi

`getListItem(<parameters>)`

+++

+++Parametri

| Parametro | Tipo |
|-----------|------------------|
| list | listString |
| list | listBoolean |
| list | listInteger |
| list | listDecimal |
| list | listDuration |
| list | listDateTime |
| list | listDateTimeOnly |
| list | listDateOnly |
| index | intero |

+++

+++Firme e tipo restituito

`getListItem(<listInteger>,<index>)`

Restituisce un numero intero.

`getListItem(<listDecimal>,<index>)`

Restituisce un valore decimale.

`getListItem(<listString>,<index>)`

Restituisce una stringa.

`getListItem(<listDateTimeOnly>,<index>)`

Restituisce un valore datetime senza considerare il fuso orario.

`getListItem(<listDateTime>,<index>)`

Restituisce un valore datetime.

`getListItem(<listDateOnly>,<index>)`

Restituisce un elenco di date.

`getListItem(<listBoolean>,<index>)`

Restituisce un valore booleano.

`getListItem(<listDuration>,<index>)`

Restituisce una durata.

+++

+++Esempi

`getListItem([10, 2, 3], 1)`

Restituisce &quot;2&quot;

`getListItem(["A", "B", "C"], 2)`

Restituisce &quot;C&quot;

Esempi con un campo evento &quot;event.appVersion&quot; con valore: &quot;20.45.2.3434&quot;

`split(@event{event.appVersion}, "\\.")`

Restituisce `["20", "45", "2", "3434"]`

`getListItem(split(@event{event.appVersion}, "\\."), 0)`

Restituisce &quot;20&quot;

+++

## in {#in}

Controlla se il primo valore di argomento è presente nell&#39;elenco. Il controllo viene eseguito tramite un valore Uguale su ciascun argomento. Restituisce true se viene trovato il valore dell’argomento, in caso contrario false.

Il tipo di `<expression>` deve corrispondere agli elementi dell&#39;elenco. I tipi di elementi dell&#39;elenco, come promemoria, devono corrispondere tra loro.

+++Sintassi

`in(<parameters>)`

+++

+++Parametri

| Parametro | Tipo |
|-----------|------------------|
| Stringa | Stringa |
| Booleano | Booleano |
| Intero | Intero |
| Decimale | Decimale |
| Durata | Durata |
| Data e ora | Data e ora |
| DateTimeOnly | DateTimeOnly |
| Elenco | listString |
| Elenco | listBoolean |
| Elenco | listInteger |
| Elenco | listDecimal |
| Elenco | listDuration |
| Elenco | listDateTime |
| Elenco | listDateTimeOnly |
| Elenco | listDateOnly |

+++

+++Firma e tipo restituito

`in(<integer>,<listInteger>)`

`in(<decimal>,<listDecimal>)`

`in(<string>,<listString>)`

`in(<boolean>,<listBoolean>)`

`in(<dateTimeOnly>,<listDateTimeOnly>)`

`in(<dateTime>,<listDateTime>)`

`in(<dateOnly>,<listDateOnly>)`

`in(<duration>,<listDuration>)`

Restituisce un valore booleano.

+++

+++Esempi

`in(4,[4,5,3,4])`

Restituisce true.

`in(8,[4,5,3,4])`

Restituisce false.

`in(#{ExperiencePlatform.ProfileFieldGroup.profile.person.gender}, ["male"])`

+++

## intersect {#intersect}

Restituisce i valori comuni nei due elenchi di input. Se uno dei due elenchi è nullo, restituisce un elenco vuoto.

+++Sintassi

`intersect(<parameters>)`

+++

+++Parametri

| Parametro | Tipo |
|-----------|------------------|
| elenco 1 | list |
| elenco 2 | list |

+++

+++Firme e tipi restituiti

`intersect(listString,listString)`: listString

`intersect(listDecimal,listDecimal)`: listDecimal

`intersect(listInteger,listInteger)`: listInteger

`intersect(listDateTime,listDateTime)`: listDateTime

`intersect(listDateTimeOnly,listDateTimeOnly)`: listDateTimeOnly

`intersect(listDateOnly,listDateOnly)`: listDateOnly

`intersect(listDuration,listDuration)`: listDuration

`intersect(listBoolean,listBoolean)`: listBoolean

Restituisce un elenco.

+++

+++Esempi

```json
intersect(
    ["sports", "news", "documentary"],
    ["sports", "movies", "documentary"]
)
```

Restituisce [&quot;sport&quot;, &quot;news&quot;]

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
    ["sports", "documentary"]
)
```

Restituisce elementi comuni tra gli attributi del profilo e un elenco specifico di categorie.

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
        @event{myEvent.sport_interests}
)
```

Restituisce elementi comuni tra gli attributi del profilo e il campo evento specificato.

+++

## limit {#limit}

Restituisce il primo o l&#39;ultimo N elemento di un elenco.

+++Sintassi

`limit(<parameters>)`

+++

+++Parametri

| Parametro | Tipo | Descrizione |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly o listObject | Elenco da considerare. Per listObject, deve essere un riferimento di campo. |
| numberOfItems | intero | Numero di elementi da restituire dall&#39;elenco specificato. |
| firstOrLastItems | booleano | Questo parametro è facoltativo (true per impostazione predefinita). true restituisce i primi elementi. false restituisce gli ultimi elementi. |

+++

+++Firma e tipo restituito

`limit(<listString>,<integer>)`

`limit(<listString>,<integer>,<boolean>)`

Restituisce un elenco di stringhe.

`limit(<listInteger>,<integer>)`

`limit(<listInteger>,<integer>,<boolean>)`

Restituisce un elenco di numeri interi.

`limit(<listDecimal>,<integer>)`

`limit(<listDecimal>,<integer>,<boolean>)`

Restituisce un elenco di decimali.

`limit(<listBoolean>,<integer>)`

`limit(<listBoolean>,<integer>,<boolean>)`

Restituisce un elenco di booleani.

`limit(<listDateOnly>,<integer>)`

`limit(<listDateOnly>,<integer>,<boolean>)`

Restituisce un elenco di date.

`limit(<listDateTimeOnly>,<integer>)`

`limit(<listDateTimeOnly>,<integer>,<boolean>)`

Restituisce un elenco di date senza considerare il fuso orario.

`limit(<listDateTime>,integer>)`

`limit(<listDateTime>,<integer>,<boolean>)`

Restituisce un elenco di date.

`limit(<listDuration>,<integer>)`

`limit(<listDuration>,<integer>,<boolean>)`

Restituisce un elenco di durate.

`limit(<listObject>,<integer>)`

`limit(<listObject>,<integer>,<boolean>)`

Restituisce un elenco di oggetti.

+++

+++Esempi

`limit(["A", "B", "C", "D", "E"], 3)`

Restituisce `["A","B","C"]`.

`limit(["A", "B", "C", "D", "E"], 3, false)`

Restituisce `["C","D","E"]`.

+++

## listSize {#listSize}

Conta il numero di elementi nell&#39;elenco.

+++Sintassi

`listSize(<parameters>)`

+++

+++Parametri

| Parametro | Tipo | Descrizione |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly o listObject | Elenco da elaborare. Per listObject, deve essere un riferimento di campo. Un listObject non può contenere un oggetto null. |

+++

+++Firme e tipo restituito

`listSize(<listInteger>)`

`listSize(<listDecimal>)`

`listSize(<listString>)`

`listSize(<listBoolean>)`

`listSize(<listDateTimeOnly>)`

`listSize(<listDateTime>)`

`listSize(<listDateOnly>)`

`listSize(<listDuration>)`

Restituisce un numero intero.

`listSize(<listObject>)`

+++

+++Esempi

`listSize([10,2,3])`

Restituisce 3.

`listSize(@event{my_event.productListItems})`

Restituisce il numero di oggetti nella matrice di oggetti specificata (tipo listObject).

+++

## serializeList {#serializeList}

Converte un elenco specifico (qualsiasi tipo eccetto listObject) in una stringa.

+++Sintassi

`serializeList(<parameters>)`

+++

+++Parametri

| Parametro | Tipo | Descrizione |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly | Elenco da convertire in stringa. |
| separatore | stringa | Separatore tra ciascun elemento elenco nella stringa di output. |
| addQuotes | booleano | Questo parametro indica se ogni elemento nella stringa di output deve includere virgolette (true) o meno (false). |

+++

+++Firma e tipo restituito

`serializeList(<listInteger>,<string>,<boolean>)`

`serializeList(<listDecimal>,<string>,<boolean>)`

`serializeList(<listString>,<string>,<boolean>)`

`serializeList(<listBoolean>,<string>,<boolean>)`

`serializeList(<listDateTimeOnly>,<string>,<boolean>)`

`serializeList(<listDateTime>,<string>,<boolean>)`

`serializeList(<listDateOnly>,<string>,<boolean>)`

`serializeList(<listDuration>,<string>,<boolean>)`

Restituisce una stringa.

+++

+++Esempi

`serializeList(["Hello","World"], " ", false)`

Restituisce &quot;Hello World&quot;.

`serializeList(["Hello", "World"], ",", true)`

Restituisce &quot;&quot;Hello&quot;,&quot;World&quot;&quot;.

+++

## ordina {#sort}

Ordina un elenco di valori o oggetti nell&#39;ordine naturale.

+++Sintassi

`sort(<parameters>)`

+++

+++Parametri

| Parametro | Tipo | Descrizione |
|-----------|------------------|------------------|
| listToSort | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly o listObject | Elenco da ordinare. Per listObject, deve essere un riferimento di campo. |
| keyAttributeName | stringa | Questo parametro è solo per listObject. Il nome dell’attributo negli oggetti dell’elenco specificato viene utilizzato come chiave per l’ordinamento. |
| ordinamentoOrdine | booleano | Crescente (true) o Decrescente (false) |

+++

+++Firma e tipo restituito

`sort(<listInteger>,<boolean>)`

Restituisce un elenco di numeri interi.

`sort(<listDecimal>,<boolean>)`

Restituisce un elenco di decimali.

`sort(<listString>,<boolean>)`

Restituisce un elenco di stringhe.

`sort(<listDateTimeOnly>,<boolean>)`

Restituisce un elenco di date senza considerare il fuso orario.

`sort(<listDateTime>,<boolean>)`

Restituisce un elenco di date.

`sort(<listDateOnly>,<boolean>)`

Restituisce un elenco di date.

`sort(<listBoolean>,<boolean>)`

Restituisce un elenco di booleani.

`sort(<listObject>,<string>,<boolean>)`

Restituisce un elenco di oggetti.

+++

+++Esempi

`sort(["A", "C", "B"], true)`

Restituisce `["A","B","C"]`.

`sort([1, 3, 2], false)`

Restituisce `[3, 2, 1]`.

`sort(@event{my_event.productListItems}, "SKU", true)`

Restituisce l&#39;oggetto listObject ordinato in base all&#39;attributo SKU (ordine crescente)

+++

