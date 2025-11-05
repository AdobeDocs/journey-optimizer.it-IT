---
solution: Journey Optimizer
product: journey optimizer
title: Funzioni
description: Informazioni sulle funzioni nelle espressioni di percorso
feature: Journeys
role: Developer
level: Experienced
keywords: funzione, espressioni, editor, percorso, dati, manipolazione
exl-id: 5b978eef-7d3e-41fe-bb08-0cf37c3b125d
version: Journey Orchestration
source-git-commit: 99053c6c1327818645adc4ab9a5d3dd30eb96b87
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 9%

---

# Funzioni {#functions}

Le funzioni sono gli elementi costitutivi delle espressioni di percorso dinamico in Adobe Journey Optimizer. Consentono di trasformare, calcolare, convalidare e manipolare i dati in tempo reale per creare esperienze cliente personalizzate. Con oltre 60 funzioni organizzate in categorie intuitive, puoi creare condizioni sofisticate, eseguire calcoli complessi e prendere decisioni basate sui dati in ogni fase del percorso del cliente.

## Informazioni sulle funzioni

Le funzioni nelle espressioni di percorso seguono un pattern di sintassi coerente:

`<function name>`(`<expression as param 1>`, `<expression as param 2>`, ... ,`<expression as param N>`)

**Caratteristiche chiave:**

* **Firme multiple**: una funzione può avere firme diverse (set diversi di parametri ordinati) per soddisfare vari casi d&#39;uso
* **Restituzioni specifiche per tipo**: ogni funzione ha un tipo restituito specifico (stringa, numero intero, booleano, data, elenco, ecc.)
* **Parametri da zero a N**: le funzioni possono accettare espressioni 0-N come parametri ordinati, fornendo flessibilità nel modo in cui utilizzarle

## Perché utilizzare le funzioni?

Le funzioni consentono di:

* **Creazione di condizioni dinamiche** - Percorsi di percorso di diramazione basati sulla valutazione dei dati in tempo reale
* **Personalizzazione su larga scala** - Personalizzazione di contenuti ed esperienze tramite dati sui clienti e informazioni sul comportamento
* **Automatizzare le decisioni** - Creare una logica intelligente senza intervento manuale
* **Trasforma dati** - Converti, formatta e modifica tipi di dati per garantire la compatibilità
* **Eseguire calcoli** - Eseguire operazioni matematiche e analisi statistiche
* **Convalida input** - Verifica la qualità e la completezza dei dati prima di intraprendere azioni

## Funzioni per categoria

Sfoglia le funzioni organizzate in base al loro scopo principale per trovare rapidamente lo strumento giusto per le tue esigenze.

### Adobe Experience Platform {#aep-functions}

**Segmentazione del pubblico e targeting**

Valuta l’iscrizione al pubblico per creare percorsi di percorso personalizzati in base ai segmenti di clienti definiti in Adobe Experience Platform.

| Funzione | Descrizione |
|----------|-------------|
| [inAudience](../functions/functioninaudience.md) | Verifica se un singolo appartiene a un pubblico specifico |

[Visualizza → dettagli funzione Adobe Experience Platform](../functions/functioninaudience.md)

### Funzioni di aggregazione {#aggregation-functions}

**Calcoli statistici e riepilogo dei dati**

Esegui calcoli su insiemi di valori per derivare informazioni approfondite quali medie, conteggi, somme e valori min/max. Essenziale per un processo decisionale basato sui dati.

| Funzione | Descrizione |
|----------|-------------|
| [avg](../functions/aggregation-functions.md#avg) | Calcola valore medio |
| [count](../functions/aggregation-functions.md#count) | Numero di elementi non nulli |
| [countOnlyNull](../functions/aggregation-functions.md#countOnlyNull) | Conta solo valori Null |
| [countWithNull](../functions/aggregation-functions.md#countWithNull) | Conteggio di tutti gli elementi inclusi i valori Null |
| [distinctCount](../functions/aggregation-functions.md#distinctCount) | Conteggio valori univoci non nulli |
| [distinctCountWithNull](../functions/aggregation-functions.md#distinctCountWithNull) | Conta valori univoci inclusi i valori Null |
| [max](../functions/aggregation-functions.md#max) | Trova valore massimo |
| [min](../functions/aggregation-functions.md#min) | Trova valore minimo |
| [sum](../functions/aggregation-functions.md#sum) | Calcola somma totale |

[Visualizza tutte le funzioni di aggregazione →](../functions/aggregation-functions.md)

### Funzioni di conversione {#conversion-functions}

**Trasformazione tipo dati**

Converti i dati tra tipi diversi (stringa, numero intero, decimale, booleano, data, durata) per garantire la compatibilità tra le operazioni e le origini dati.

| Funzione | Descrizione |
|----------|-------------|
| [toBool](../functions/conversion-functions.md#toBool) | Converti in booleano |
| [toDateOnly](../functions/conversion-functions.md#toDateOnly) | Converti solo in data (nessuna ora) |
| [toDateTime](../functions/conversion-functions.md#toDateTime) | Converti in data con ora |
| [toDateTimeOnly](../functions/conversion-functions.md#toDateTimeOnly) | Converti in data e ora senza fuso orario |
| [toDecimal](../functions/conversion-functions.md#toDecimal) | Converti in numero decimale |
| [toDuration](../functions/conversion-functions.md#toDuration) | Converti in durata |
| [toInteger](../functions/conversion-functions.md#toInteger) | Converti in numero intero |
| [toString](../functions/conversion-functions.md#toString) | Converti in stringa |

[Visualizza tutte le funzioni di conversione →](../functions/conversion-functions.md)

### Funzioni data {#date-functions}

**Manipolazione di data e ora**

Utilizza date, ore e fusi orari per creare condizioni basate sul tempo, pianificare azioni ed eseguire calcoli temporali.

| Funzione | Descrizione |
|----------|-------------|
| [currentTimeInMillis](../functions/date-functions.md#currentTimeInMillis) | Ottieni ora corrente in millisecondi |
| [inLastDays](../functions/date-functions.md#inLastDays) | Controlla se la data rientra negli ultimi N giorni |
| [inLastHours](../functions/date-functions.md#inLastHours) | Controlla se la data rientra nelle ultime N ore |
| [inLastMonths](../functions/date-functions.md#inLastMonths) | Controlla se la data rientra negli ultimi N mesi |
| [inLastYears](../functions/date-functions.md#inLastYears) | Controlla se la data rientra negli ultimi N anni |
| [inNextDays](../functions/date-functions.md#inNextDays) | Controlla se la data rientra nei N giorni successivi |
| [inNextHours](../functions/date-functions.md#inNextHours) | Controlla se la data rientra nelle N ore successive |
| [inNextMonths](../functions/date-functions.md#inNextMonths) | Controlla se la data rientra nei successivi N mesi |
| [inNextYears](../functions/date-functions.md#inNextYears) | Controlla se la data rientra nei prossimi N anni |
| [now](../functions/date-functions.md#now) | Ottieni data/ora corrente |
| [nowWithDelta](../functions/date-functions.md#nowWithDelta) | Ottieni ora corrente con offset |
| [setHours](../functions/date-functions.md#setHours) | Imposta ore specifiche in data/ora |
| [setDays](../functions/date-functions.md#setDays) | Imposta giorni specifici in data/ora |
| [updateTimeZone](../functions/date-functions.md#updateTimeZone) | Aggiorna il fuso orario di data e ora |

[Visualizza tutte le funzioni data →](../functions/date-functions.md)

### Elencare funzioni {#list-functions}

**Analisi e manipolazione della raccolta**

Filtrare, ordinare, trasformare e analizzare array ed elenchi per lavorare con strutture di dati complesse ed eseguire operazioni di impostazione.

| Funzione | Descrizione |
|----------|-------------|
| [distinct](../functions/list-functions.md#distinct) | Ottieni valori univoci (esclusi i valori Null) |
| [distinctWithNull](../functions/list-functions.md#distinctWithNull) | Ottieni valori univoci (include valori Null) |
| [filtro](../functions/list-functions.md#filter) | Filtra elenco in base a criteri |
| [getListItem](../functions/list-functions.md#getListItem) | Ottieni elemento in un indice specifico |
| [in](../functions/list-functions.md#in) | Controlla se il valore esiste nell’elenco |
| [intersezione](../functions/list-functions.md#intersect) | Trovare elementi comuni tra gli elenchi |
| [limite](../functions/list-functions.md#limit) | Limita il numero di elementi restituiti |
| [listSize](../functions/list-functions.md#listSize) | Ottieni dimensione elenco |
| [serializeList](../functions/list-functions.md#serializeList) | Converti elenco in stringa |
| [sort](../functions/list-functions.md#sort) | Ordinare gli elementi dell’elenco |

[Visualizza tutte le funzioni elenco →](../functions/list-functions.md)

### Funzioni matematiche {#math-functions}

**Operazioni matematiche**

Eseguire calcoli numerici e trasformazioni per l&#39;elaborazione dei dati e la logica di business.

| Funzione | Descrizione |
|----------|-------------|
| [random](../functions/math-functions.md#random) | Genera numero casuale (0-1) |
| [round](../functions/math-functions.md#round) | Arrotonda al numero intero più vicino |

[Visualizza tutte le funzioni matematiche →](../functions/math-functions.md)

### Funzioni stringa {#string-functions}

**Modifica e convalida del testo**

Elabora, trasforma, cerca e convalida i dati di testo per la creazione di contenuti dinamici e la logica condizionale.

| Funzione | Descrizione |
|----------|-------------|
| [concat](../functions/string-functions.md#concat) | Concatenare stringhe |
| [contain](../functions/string-functions.md#contain) | Controlla se la stringa contiene sottostringa |
| [containIgnoreCase](../functions/string-functions.md#containIgnoreCase) | Seleziona contiene (senza distinzione maiuscole/minuscole) |
| [endWith](../functions/string-functions.md#endWith) | Controlla se la stringa termina con il suffisso |
| [endWithIgnoreCase](../functions/string-functions.md#endWithIgnoreCase) | Seleziona termina con (senza distinzione maiuscole/minuscole) |
| [equalIgnoreCase](../functions/string-functions.md#equalIgnoreCase) | Confrontare le stringhe (senza distinzione maiuscole/minuscole) |
| [indexOf](../functions/string-functions.md#indexOf) | Trova prima posizione occorrenza |
| [isEmpty](../functions/string-functions.md#isEmpty) | Controlla se la stringa è vuota |
| [isNotEmpty](../functions/string-functions.md#isNotEmpty) | Controlla se la stringa non è vuota |
| [lastIndexOf](../functions/string-functions.md#lastIndexOf) | Trova ultima posizione occorrenza |
| [length](../functions/string-functions.md#length) | Ottieni lunghezza stringa |
| [Lower](../functions/string-functions.md#lower) | Converti in minuscolo |
| [matchRegExp](../functions/string-functions.md#matchRegExp) | Corrispondenza espressione regolare |
| [notEqualIgnoreCase](../functions/string-functions.md#notEqualIgnoreCase) | Seleziona diverso da (senza distinzione maiuscole/minuscole) |
| [replace](../functions/string-functions.md#replace) | Sostituisci prima occorrenza |
| [replaceAll](../functions/string-functions.md#replaceAll) | Sostituisci tutte le occorrenze |
| [split](../functions/string-functions.md#split) | Dividi stringa in matrice |
| [startWith](../functions/string-functions.md#startWith) | Controlla se la stringa inizia con il prefisso |
| [startWithIgnoreCase](../functions/string-functions.md#startWithIgnoreCase) | Seleziona inizia con (senza distinzione maiuscole/minuscole) |
| [substr](../functions/string-functions.md#substr) | Estrai sottostringa |
| [trim](../functions/string-functions.md#trim) | Rimuovi spazi iniziali/finali |
| [upper](../functions/string-functions.md#upper) | Converti in maiuscolo |
| [uuid](../functions/string-functions.md#uuid) | Genera UUID |

[Visualizza tutte le funzioni stringa →](../functions/string-functions.md)

## Passaggi successivi

Ora che conosci le funzioni disponibili, scopri:

* **[Editor espressioni avanzate](expressionadvanced.md)** - Scopri come creare espressioni complesse utilizzando l&#39;editor avanzato
* **[Sintassi espressione](generalities.md)** - Eseguire il master delle regole di sintassi per la scrittura di espressioni di percorso
* **[Operatori](operators.md)** - Individua gli operatori che puoi utilizzare con le funzioni per generare la logica
* **[Riferimenti campo](field-references.md)** - Comprendere come fare riferimento ai campi dati nelle espressioni
