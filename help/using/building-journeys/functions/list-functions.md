---
product: journey optimizer
title: Funzioni elenco
description: Informazioni sulle funzioni elenco
feature: Journeys
role: Developer
level: Experienced
keywords: elenco, funzioni, espressione, percorso, matrice, raccolta
version: Journey Orchestration
exl-id: b17245ba-4ffa-4f5b-914e-4c0972e9c7c4
TQID: https://experienceleague.adobe.com/XWWixhfBVKw-kdgO4WPWrtiIqA8sFt0ql0IVZ-2QsUI
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: d00e9f03-e50b-4162-b143-0c0817c937c2
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1642
ht-degree: 6%

---

# Funzioni elenco {#list-functions}

Le funzioni elenco consentono di manipolare e utilizzare insiemi di valori all’interno delle espressioni di percorso. Queste funzioni sono essenziali per filtrare, ordinare, trasformare e analizzare array ed elenchi nei percorsi dei clienti.

Utilizza le funzioni elenco quando devi:

* Filtra ed estrai elementi specifici dalle raccolte in base ai criteri ([filter](#filter), [getListItem](#getListItem))
* Ordina e organizza gli elementi elenco in ordine crescente o decrescente ([ordina](#sort))
* Rimuovi i duplicati e ottieni valori univoci dagli elenchi ([distinct](#distinct), [distinctWithNull](#distinctWithNull))
* Verifica se i valori esistono nelle raccolte ([in](#in))
* Limita il numero di elementi restituiti da un elenco ([limit](#limit))
* Ottenere le dimensioni di un elenco ([listSize](#listSize)) o trasformare gli elenchi in formati diversi ([serializeList](#serializeList))
* Eseguire operazioni sui set come la ricerca di elementi comuni tra elenchi ([intersect](#intersect))

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

+++ Guida di riferimento della Knowledge Base di AI

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

* **TL;DR:** In questa pagina sono documentate tutte le funzioni di elenco disponibili nelle espressioni di percorso di AJO, con informazioni su come filtrare, ordinare, deduplicare, controllare l&#39;appartenenza, limitare, serializzare e trovare intersezioni di elenchi e array.

**Intenti:**
* Rimuovere i valori duplicati da un elenco utilizzando `distinct` (ignorando i valori Null) o `distinctWithNull` (mantenendo i valori Null)
* Filtrare un listObject per restituire solo oggetti che corrispondono a valori chiave specifici utilizzando `filter`
* Recuperare un elemento in un indice specifico da un elenco utilizzando `getListItem`
* Verificare se esiste un valore in un elenco utilizzando `in`
* Trovare elementi comuni tra due elenchi utilizzando `intersect`
* Restituire il primo o l&#39;ultimo N elementi di un elenco utilizzando `limit`
* Contare il numero totale di elementi in un elenco utilizzando `listSize`
* Convertire un elenco in una stringa delimitata utilizzando `serializeList`
* Ordinare un elenco in ordine crescente o decrescente utilizzando `sort`

**Glossario:**
* **listObject**: un elenco di oggetti complessi che devono essere un riferimento di campo; non può contenere oggetti Null *(specifici del prodotto)*
* **keyAttributeName**: parametro di stringa facoltativo utilizzato con `distinct`, `filter` e `sort` per identificare l&#39;attributo di oggetto da utilizzare per la deduplicazione, il filtraggio o l&#39;ordinamento di *(specifico per prodotto)*
* **intersect**: un&#39;operazione set restituisce solo gli elementi presenti in entrambi gli elenchi di input

**Guardrail:**
* `distinctWithNull` non supporta il tipo di parametro `<listObject>`
* `filter` richiede che il parametro listObject sia un riferimento di campo, non un valore letterale in linea
* `listSize` in un listObject richiede che l&#39;elenco sia un riferimento di campo; un listObject non può contenere oggetti null
* `serializeList` non supporta il tipo `listObject`

**Terminologia:**
* Nome canonico: Funzioni elenco — Acronimo: none — Varianti: funzioni raccolta, funzioni matrice
* Sinonimi: &quot;listSize&quot; = &quot;count list elements&quot;; &quot;serializeList&quot; = &quot;join list to string&quot;
* Non confondere: &quot;distinct&quot; (ignora i valori Null) ≠ &quot;distinctWithNull&quot; (mantiene null come valore distinto)
* Non confondere: &quot;limit&quot; con il terzo parametro `true` (restituisce i primi N elementi) ≠ &quot;limit&quot; con `false` (restituisce gli ultimi N elementi)
* Non confondere: &quot;intersect&quot; (elementi comuni tra due elenchi) ≠ &quot;filter&quot; (elementi che corrispondono a valori chiave specifici)

**Domande frequenti:**
* **D: come è possibile ottenere i primi 3 elementi di un elenco?** — Utilizzare `limit(myList, 3)` o `limit(myList, 3, true)`; per impostazione predefinita vengono restituiti i primi elementi.
* **D: come è possibile ottenere gli ultimi 3 elementi di un elenco?** — Utilizza `limit(myList, 3, false)`.
* **Q: Qual è la differenza tra `distinct` e `distinctWithNull`?** — `distinct` ignora i valori Null e li esclude dal risultato; `distinctWithNull` tratta i valori Null come valori distinti e include una voce Null se sono presenti valori Null.
* **Q: è possibile filtrare un elenco di stringhe con `filter`?** — No, `filter` funziona solo su `listObject`; per gli elenchi scalari utilizza `in` o `distinct` per la deduplicazione.
* **D: come posso verificare se un valore è presente in un elenco?** — Utilizzare `in(value, myList)`, che restituisce true se il valore si trova nell&#39;elenco.
* **Q: è possibile ordinare un listObject in base a un attributo specifico?** — Sì, utilizza `sort(@event{...}, "attributeName", true)` dove il secondo parametro è il nome dell&#39;attributo e il terzo è la direzione di ordinamento (true = ascending).

+++
