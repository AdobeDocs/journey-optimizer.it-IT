---
product: journey optimizer
title: Funzioni di aggregazione
description: Informazioni sulle funzioni di aggregazione
feature: Journeys
role: Developer
level: Experienced
keywords: aggregazione, funzioni, espressione, percorso, media, conteggio, max, min, sum
version: Journey Orchestration
exl-id: 871a5212-5b94-4a54-bf1d-276022be3c95
feature_v2: []
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1105
ht-degree: 5%

---

# Funzioni di aggregazione {#aggregation-functions}

Le funzioni di aggregazione eseguono calcoli su un insieme di valori e restituiscono un singolo risultato riepilogato. Queste funzioni consentono di analizzare i dati all&#39;interno delle espressioni di percorso calcolando le medie, trovando i valori minimi e massimi, contando gli elementi e sommando i valori numerici.

Utilizzare le funzioni di aggregazione quando è necessario:

* Calcola valori statistici da elenchi o matrici ([avg](#avg), [sum](#sum), [min](#min), [max](#max))
* Conta elementi nelle raccolte ([count](#count), [countOnlyNull](#countOnlyNull), [countWithNull](#countWithNull)), con opzioni per includere o escludere valori Null
* Determina valori univoci nei set di dati ([distinctCount](#distinctCount), [distinctCountWithNull](#distinctCountWithNull))
* Prendere decisioni basate sui dati in base a metriche calcolate

Le funzioni di aggregazione gestiscono automaticamente i valori Null in base al loro comportamento specifico, semplificando l&#39;utilizzo di dati reali che possono contenere valori mancanti o non definiti.


## avg {#avg}

Restituisce il valore medio tra un insieme di espressioni, sotto forma di elenco o di due espressioni. I valori Null vengono ignorati.

+++Sintassi

`avg(<parameter>)`

+++

+++Parametri

Tipi supportati:

* listInteger
* listDecimal
* decimale
* intero

+++

+++Firme e tipo restituito

`avg(<listInteger>)`

`avg(<listDecimal>)`

`avg(<decimal>,<decimal>)`

`avg(<decimal>,<integer>)`

`avg(<integer>,<decimal>)`

`avg(<integer>,<integer>)`

Restituisce un valore decimale.

+++

+++Esempi

`avg(@event{BarBeacon.inventory},5)`

`avg([10,3,8])`

Restituisce 7,0.

`avg(10.2, 3)`

Restituisce 6,6.

+++

## conteggio {#count}

Conta gli elementi dell’elenco senza tenere conto dei valori nulli.

+++Sintassi

`count(<listAny>)`

`count(<listObject>)`

+++

+++Parametri

| Parametro | Tipo | Descrizione |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly o listObject | Elenco da elaborare. Per listObject, deve essere un riferimento di campo. Un listObject non può contenere un oggetto null. |

+++

+++Firme e tipo restituito

`count(<listAny>)`

Restituisce un numero intero.

+++

+++Esempi

`count([10,2,10,null])`

Restituisce 3.

`count(@event{my_event.productListItems})`

Restituisce il numero di oggetti nella matrice di oggetti specificata (tipo listObject). Nota: listObject non può contenere un oggetto null

+++

## countOnlyNull {#countOnlyNull}

Conta il numero di valori Null nell&#39;elenco.

+++Sintassi

`countOnlyNull(<listAny>)`

+++

+++Parametri

| Parametro | Tipo |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

+++

+++Firme e tipo restituito

`countOnlyNull(<listAny>)`

Restituisce un numero intero.

+++

+++Esempi

`countOnlyNull([10,2,10,null])`

Restituisce 1.

+++

**Nota:** Il parametro `<listObject>` non è supportato in questa funzione.

## countWithNull {#countWithNull}

Conta tutti gli elementi dell’elenco, inclusi i valori Null.

+++Sintassi

`countWithNull(<listAny>)`

+++

+++Parametri

| Parametro | Tipo |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

+++

+++Firme e tipo restituito

`countWithNull(<listAny>)`

Restituisce un numero intero.

+++

+++Esempi

`countWithNull([10,2,10,null])`

Restituisce 4.

+++

**Nota:** Il parametro `<listObject>` non è supportato in questa funzione.

## distinctCount {#distinctCount}

Conta il numero di valori diversi ignorando i valori Null.

+++Sintassi

`distinctCount(<listAny>)`

+++

+++Parametri

| Parametro | Tipo | Descrizione |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly o listObject | Elenco da elaborare. Per listObject, deve essere un riferimento di campo. |
| keyAttributeName | stringa | Questo parametro è facoltativo e solo per listObject. Se il parametro non viene fornito, un oggetto viene considerato duplicato se tutti gli attributi hanno gli stessi valori. In caso contrario, un oggetto viene considerato duplicato se l’attributo specificato ha lo stesso valore. |

+++

+++Firme e tipo restituito

`distinctCount(<listAny>)`

Restituisce un numero intero.

`distinctCount(<listObject>)`

`distinctCount(<listObject>,<string>)`

Restituisce un elenco di oggetti.

+++

+++Esempi

`distinctCount([10,2,10,null])`

Restituisce 2.

`distinctCount(@event{my_event.productListItems})`

Restituisce il numero di oggetti strettamente distinti nella matrice di oggetti specificata (tipo listObject).

`distinctCount(@event{my_event.productListItems}, "SKU")`

Restituisce il numero di oggetti con un valore di attributo &quot;SKU&quot; distinto{}.

+++

## distinctCountWithNull {#distinctCountWithNull}

Conta il numero di valori diversi, inclusi i valori Null.

+++Sintassi

`distinctCountWithNull(<listAny>)`

+++

+++Parametri

| Parametro | Tipo |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

+++

+++Firme e tipo restituito

`distinctCountWithNull(<listAny>)`

Restituisce un numero intero.

+++

+++Esempi

`distinctCountWithNull([10,2,10,null])`

Restituisce 3.

+++

**Nota:** Il parametro `<listObject>` non è supportato in questa funzione.

## max {#max}

Restituisce il valore massimo in un insieme di espressioni, sotto forma di elenco o di due espressioni. I valori Null vengono ignorati.

+++Sintassi

`max(<parameter>)`

+++

+++Parametri

* listDuration
* listInteger
* listDecimal
* listDateTime
* listDateTimeOnly
* listDateOnly
* durata
* intero
* decimale
* dateTime
* dateTimeOnly

+++

+++Firme e tipi restituiti

`max(<listDuration>)`

Restituisce una durata.

`max(<listInteger>)`

Restituisce una durata.

`max(<listDateTimeOnly>)`

Restituisce un valore datetime senza considerare il fuso orario.

`max(<listDateTime>)`

Restituisce un valore datetime.

`max(<listDateOnly>)`

Restituisce una data.

`max(<listDecimal>)`

Restituisce un valore decimale.

`max(<decimal>,<decimal>)`

Restituisce un valore decimale.

`max(<duration>,<duration>)`

Restituisce una durata.

`max(<dateTime>,<dateTime>)`

Restituisce un valore datetime.

`max(<dateTimeOnly>,<dateTimeOnly>)`

Restituisce un valore datetime senza considerare il fuso orario.

`max(<integer>,<integer>)`

Restituisce un numero intero.

+++

+++Esempi

`max(@event{BarBeacon.inventory},5)`

`max([10,3,8])`

Restituisce 10.

`max([10,null,8])`

Restituisce 10.

+++

## min {#min}

Restituisce il valore minimo in un insieme di espressioni, sotto forma di elenco o di due espressioni. I valori Null vengono ignorati.

+++Sintassi

`min(<parameters>)`

+++

+++Parametri

* listDuration
* listInteger
* listDecimal
* listDateTime
* listDateTimeOnly
* listDateOnly
* durata
* intero
* decimale
* dateTime
* dateTimeOnly

+++

+++Firme e tipi restituiti

`min(<listDuration>)`

Restituisce una durata.

`min(<listInteger>)`

Restituisce una durata.

`min(<listDateTimeOnly>)`

Restituisce un valore datetime senza considerare il fuso orario.

`min(<listDateTime>)`

Restituisce un valore datetime.

`min(<listDateOnly>)`

Restituisce una data.

`min(<listDecimal>)`

Restituisce un valore decimale.

`min(<decimal>,<decimal>)`

Restituisce un valore decimale.

`min(<duration>,<duration>)`

Restituisce una durata.

`min(<dateTime>,<dateTime>)`

Restituisce un valore datetime.

`min(<dateTimeOnly>,<dateTimeOnly>)`

Restituisce un valore datetime senza considerare il fuso orario.

`min(<integer>,<integer>)`

Restituisce un numero intero.

+++

+++Esempi

`min(@event{BarBeacon.inventory},5)`

`min([10,3,8])`

Restituisce 3.

`min([10,null,8])`

Restituisce 8.

+++

## sum {#sum}

Restituisce la somma dei valori di un insieme di espressioni. I valori Null vengono ignorati.

+++Sintassi

`sum(<parameters>)`

+++

+++Parametri

* listInteger
* listDecimal
* durata
* intero
* decimale

+++

+++Firme e tipi restituiti

`sum(<listDecimal>)`

Restituisce un valore decimale.

`sum(<listInteger>)`

Restituisce un numero intero.

`sum(<integer>,<integer>)`

Restituisce un numero intero.

`sum(<decimal>,<decimal>)`

Restituisce un valore decimale.

+++

+++Esempi

`sum(@event{BarBeacon.inventory},5)`

`sum([10,3,8])`

Restituisce 21.

`sum([10.5,null,8.1])`

Restituisce 18,6.

+++

+++ Guida di riferimento della Knowledge Base di AI

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

* **TL;DR:** In questa pagina sono documentate tutte le funzioni di aggregazione disponibili nelle espressioni di percorso di AJO, con informazioni su come calcolare medie, somme, valori minimi e massimi, conteggi e conteggi distinti su elenchi e array.

**Intenti:**
* Calcola la media di un elenco di valori numerici utilizzando `avg`
* Sommare i valori numerici in un elenco o dai campi evento utilizzando `sum`
* Trovare il valore minimo o massimo in un elenco utilizzando `min` o `max`
* Conteggio di elementi non nulli, null-only o tutti gli elementi in un elenco tramite `count`, `countOnlyNull` o `countWithNull`
* Conta valori distinti in un elenco, con o senza valori Null, utilizzando `distinctCount` o `distinctCountWithNull`
* Filtrare oggetti univoci in un listObject in base a un attributo chiave specifico utilizzando `distinctCount` con un parametro chiave

**Glossario:**
* **listObject**: un elenco di oggetti complessi (riferimenti campo); non può contenere oggetti null *(specifici per prodotto)*
* **listAny**: elenco di qualsiasi tipo scalare supportato (string, boolean, integer, decimal, duration, dateTime, dateTimeOnly, dateOnly) *(specifico per prodotto)*
* **Valore Null**: elemento assente o non definito in un elenco. La maggior parte delle funzioni di aggregazione ignora i valori Null a meno che non vengano gestite esplicitamente dalla funzione (ad esempio, `countOnlyNull`, `countWithNull`, `distinctCountWithNull`)

**Guardrail:**
* `countOnlyNull`, `countWithNull` e `distinctCountWithNull` non supportano il tipo di parametro `<listObject>`
* `distinctCount` in un `listObject` richiede che l&#39;elenco sia un riferimento di campo, non un valore letterale in linea
* `count` su un `listObject` richiede che l&#39;elenco sia un riferimento di campo; un listObject non può contenere oggetti Null

**Terminologia:**
* Nome canonico: Funzioni di aggregazione — Acronimo: none — Varianti: funzioni di aggregazione, funzioni di raccolta
* Sinonimi: &quot;count&quot; = &quot;count elementi non null&quot;; &quot;countWithNull&quot; = &quot;count tutti gli elementi compresi i valori Null&quot;
* Non confondere: &quot;distinctCount&quot; (ignora i valori Null) ≠ &quot;distinctCountWithNull&quot; (include i valori Null come valore distinto)

**Domande frequenti:**
* **Q: `avg` include valori Null nel calcolo?** — No, `avg` ignora automaticamente i valori Null.
* **Q: Qual è la differenza tra `count` e `countWithNull`?** — `count` esclude i valori Null dal totale, mentre `countWithNull` conta ogni elemento, inclusi i valori Null.
* **Q: posso utilizzare `countOnlyNull` in un listObject?** — No, `<listObject>` non è supportato da `countOnlyNull`, `countWithNull` o `distinctCountWithNull`.
* **D: come posso contare oggetti distinti in un array in base a un attributo specifico?** — Utilizzare `distinctCount(@event{...}, "attributeName")` specificando il nome dell&#39;attributo chiave come secondo parametro.
* **D: che cosa restituisce `max` quando l&#39;elenco contiene valori Null?** — `max` ignora i valori Null e restituisce il valore massimo tra gli elementi non Null.

+++
