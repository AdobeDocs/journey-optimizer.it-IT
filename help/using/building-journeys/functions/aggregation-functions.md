---
product: journey optimizer
title: Funzioni di aggregazione
description: Informazioni sulle funzioni di aggregazione
feature: Journeys
role: Developer
level: Experienced
keywords: aggregazione, funzioni, espressione, percorso, media, conteggio, max, min, sum
version: Journey Orchestration
source-git-commit: af1babe501a5b2c6a67730396a8f5e2c5d85e60a
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 8%

---

# Funzioni di aggregazione {#aggregation-functions}

Le funzioni di aggregazione vengono utilizzate per eseguire calcoli su un insieme di valori e restituire un singolo valore. Queste funzioni sono particolarmente utili quando si lavora con elenchi e array nelle espressioni di percorso.

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

**Nota:** Il parametro `<listObject>` non è supportato in questa funzione.

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

## countWithNull {#countWithNull}

Conta tutti gli elementi dell’elenco, inclusi i valori Null.

**Nota:** Il parametro `<listObject>` non è supportato in questa funzione.

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

**Nota:** Il parametro `<listObject>` non è supportato in questa funzione.

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
