---
title: Introduzione alle funzioni helper
description: Libreria di funzioni Journey Optimizer Helper
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 9b0b0d8e-a819-4d2e-a241-f3c4d104eab9
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '1872'
ht-degree: 22%

---

# Introduzione alle funzioni helper{#functions}

Utilizzare [!DNL Journey Optimizer] linguaggio di template per eseguire operazioni sui dati, ad esempio calcoli, formattazione o conversioni di dati, condizioni e manipolarli nel contesto della personalizzazione. Scopri le linee guida sulla sintassi di personalizzazione in [questa pagina](../personalization-syntax.md).



➡️ [Scopri come utilizzare le funzioni di assistenza in questo video](#video)

Il linguaggio dei modelli viene utilizzato nelle funzioni di supporto disponibili nell’elenco a discesa di personalizzazione dell’editor di personalizzazione, come segue:

![](../assets/access-helper-functions.png)

>[!NOTE]
>
>Le funzioni e le funzionalità disponibili nell’editor di personalizzazione sono diverse da quelle disponibili nella [Editor espressioni avanzate percorso](../../building-journeys/expression/expressionadvanced.md).

In [!DNL Journey Optimizer] nell’editor della personalizzazione, le funzioni di assistenza sono raggruppate in tre categorie: [Funzioni](#functions-helper), [Helper](#helper-helper) e [Operatori](#operators-helper).

Seleziona una categoria per accedere alle sottocategorie e alle funzioni.

Accedere alle sottocategorie facendo clic sul pulsante `>` icona. Seleziona una funzione facendo clic sul pulsante `+` icona: la funzione viene aggiunta automaticamente alla schermata di personalizzazione.

Fai clic su `...` per visualizzare la descrizione della funzione e aggiungerla ai preferiti. [Ulteriori informazioni](../personalize.md#fav)

## Funzioni{#functions-helper}

### Funzioni di aggregazione e array

<table>
    <tr>
        <td><a href="aggregation.md#average">Medio</a></td><td>Questa funzione restituisce la media aritmetica di tutti i valori selezionati all’interno dell’array.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count">Conteggio</a></td><td>Questa funzione restituisce il numero di elementi all’interno dell’array specificato</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count-only-null">Conteggio solo valori Null</a></td><td>Questa funzione conta il numero di valori Null nell’elenco.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count-with-null">Conteggio con valori Null</a></td><td>Questa funzione conta tutti gli elementi dell’elenco, compresi i valori nulli</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct">Diverso</a></td><td>Questa funzione ottiene valori da un array o da un elenco con valori duplicati rimossi</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct-count-with-null">Conteggio valori univoci con Null</a></td><td>Questa funzione conta il numero di valori diversi, inclusi i valori Null.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#head">Primo elemento</a></td><td>Questa funzione restituisce il primo elemento di un array o di un elenco.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#first-n">Primo/i n nell’array</a></td><td>Questa funzione restituisce i primi elementi "N" di un array, se ordinati in ordine crescente in base alla data espressione numerica</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#in">In entrata</a></td><td>Questa funzione viene utilizzata per determinare se un elemento è membro di un array o di un elenco</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#includes">Include</a></td><td>Questa funzione determina se un array o un elenco contiene un dato elemento</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#intersects">Interseca</a></td><td>Questa funzione determina se due array o elenchi hanno almeno un membro comune</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#last-n">Ultimo/i n nell’array</a></td><td>Questa funzione restituisce gli ultimi elementi "N" di un array, se ordinati in ordine crescente in base alla data espressione numerica</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#max">Massimo</a></td><td>Questa funzione restituisce il più grande di tutti i valori selezionati all’interno di un array.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#min">Minimo</a></td><td>Questa funzione restituisce il più piccolo di tutti i valori selezionati all’interno dell’array.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#notin">Non in entrata</a></td><td>Questa funzione determina se un elemento non è un membro di un array o di un elenco</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#subset">Sottoinsieme di</a></td><td>Questa funzione determina se un array specifico (array A) è un sottoinsieme di un altro array (array B), ovvero se tutti gli elementi nell’array A sono elementi dell’array B</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#sum">Somma</a></td><td>Questa funzione restituisce la somma di tutti i valori selezionati all’interno dell’array.</td>
    </tr>
    <tr>
    <td><a href="arrays-list.md#superset">Superset di</a></td><td>Questa funzione determina se un array specifico (array A) è un superset di un altro array (array B), ovvero se l’array A contiene tutti gli elementi dell’array B</td>
    </tr>
</table>

### Funzioni data/ora{#date-functions}

<table>
    <tr>
        <td><a href="dates.md#age">Età</a></td><td>Questa funzione recupera l’età da una data specificata</td>
    </tr>
    <tr>
        <td><a href="dates.md#current">Ora corrente in millisecondi</a></td><td>Questa funzione recupera l’ora corrente in millisecondi epoca</td>
    </tr>
    <tr>
        <td><a href="dates.md#date-diff">Differenza data</a></td><td>Questa funzione recupera la differenza tra due date in numero di giorni.</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-week">Giorno della settimana</a></td><td>Questa funzione recupera il giorno della settimana</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-year">Giorno dell’anno</a></td><td>Questa funzione recupera il giorno dell’anno</td>
    </tr>
    <tr>
        <td><a href="dates.md#format-date">Formato data</a></td><td>Questa funzione formatta un valore di data e ora</td>
    </tr>
    <tr>
        <td><a href="dates.md#format-date-locale">Formattare la data con il supporto delle impostazioni internazionali</a></td><td>Questa funzione formatta un valore di data e ora nella corrispondente rappresentazione sensibile alla lingua, ovvero nelle impostazioni internazionali desiderate.</td>
    </tr>
    <tr>
        <td><a href="dates.md#set-days">Imposta giorni</a></td><td>Questa funzione imposta il giorno del mese per la data/ora specificata</td>
    </tr>
    <tr>
        <td><a href="dates.md#set-hours">Imposta ore</a></td><td>Questa funzione imposta l’ora della data/ora</td>
    </tr>
    <tr>
        <td><a href="dates.md#to-utc">A UTC</a></td><td>Questa funzione converte un datetime in UTC.</td>
    </tr>
    <tr>
        <td><a href="dates.md#week-of-year">Settimana dell’anno</a></td><td>Questa funzione restituisce la settimana dell’anno.</td>
    </tr>
</table>
</table>

### Funzioni mappa {#map-functions}

<table>
    <tr>
        <td><a href="maps.md#get">Ottieni</a></td><td>Questa funzione viene utilizzata per recuperare il valore di una mappa per una determinata chiave</td>
    </tr>
    <tr>
        <td><a href="maps.md#keys">Chiavi</a></td><td>Questa funzione viene utilizzata per recuperare tutte le chiavi per una data mappa</td>
    </tr>
    <tr>
        <td><a href="maps.md#values">Valori</a></td><td>Questa funzione recupera tutti i valori di una data mappa</td>
    </tr>
</table>

### Funzioni matematiche {#math-functions}

<table>
    <tr>
        <td><a href="math.md#absolute">Assoluto</a></td><td>Questa funzione formatta qualsiasi numero nella sua rappresentazione sensibile alla lingua.</td>
    </tr>
    <tr>
        <td><a href="math.md#format-number">Formato numero</a></td><td>Questa funzione formatta qualsiasi numero nella sua rappresentazione sensibile alla lingua.</td>
    </tr>
    <tr>
        <td><a href="math.md#random">Casuale</a></td><td>Questa funzione restituisce un valore casuale compreso tra 0 e 1.</td>
    </tr>
    <tr>
        <td><a href="math.md#round-down">Arrotonda per difetto</a></td><td>Questa funzione arrotonda un numero per difetto.</td>
    </tr>
    <tr>
        <td><a href="math.md#round-up">Arrotonda per eccesso</a></td><td>Questa funzione arrotonda un numero per eccesso</td>
    </tr>
    <tr>
    <td><a href="math.md#to-hex-string">Alla stringa esadecimale</a></td><td>converte qualsiasi numero nella relativa stringa esadecimale.</td>
    </tr>
    <tr>
    <td><a href="math.md#to-int">ToInt</a></td><td>Converte uno qualsiasi di questi tipi (number, double, int, long, float, short, byte, boolean, string) in un numero intero.</td>
    </tr>
    <tr>
        <td><a href="math.md#to-percentage">A percentuale</a></td><td>Questa funzione converte un numero in percentuale.</td>
    </tr>
    <tr>
        <td><a href="math.md#to-precision">Per la precisione</a></td><td>Questa funzione converte un numero in base alla precisione richiesta.</td>
    </tr>
    <tr>
        <td><a href="math.md#to-string">A stringa</a></td><td>Questa funzione converte qualsiasi numero nella sua rappresentazione di stringa. </td>
    </tr>
</table>

### Funzioni oggetto {#object-functions}

<table>
    <tr>
        <td><a href="objects.md#isNotNull">Non è Null</a></td><td>Questa funzione viene utilizzata per determinare se esiste un riferimento a un oggetto</td>
    </tr>
    <tr>
        <td><a href="objects.md#isNull">È Null</a></td><td>Questa funzione viene utilizzata per determinare se un riferimento a un oggetto non esiste</td>
    </tr>
</table>

### Funzioni stringa {#string-functions}

<table>
    <tr>
        <td><a href="string.md#camelCase">Camel Case</a></td><td>Questa funzione viene utilizzata per scrivere in maiuscolo la prima lettera di ogni parola di una stringa</td>
    </tr>
    <tr>
        <td><a href="string.md#char-code-at">Codice carattere in corrispondenza di</a></td><td>Questa funzione restituisce il valore ASCII di un carattere, come la funzione charCodeAt in JavaScript</td>
    </tr>
    <tr>
        <td><a href="string.md#concat">Concatena</a></td><td>Questa funzione viene utilizzata per combinare due stringhe in una</td>
    </tr>
    <tr>
        <td><a href="string.md#contains">Contains</a></td><td>Questa funzione viene utilizzata per determinare se una stringa contiene una sottostringa specificata</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotContain">Non contiene</a></td><td>Questa funzione viene utilizzata per determinare se una stringa non contiene una sottostringa specificata</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotEndWith">Non termina con</a></td><td>Questa funzione viene utilizzata per determinare se una stringa non termina con una sottostringa specificata</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotStartWith">Non inizia con</a></td><td>Questa funzione viene utilizzata per determinare se una stringa non inizia con una sottostringa specificata</td>
    </tr>
    <tr>
        <td><a href="string.md#encode64">Codifica 64</a></td><td>Questa funzione viene utilizzata per codificare o decodificare una stringa.</td>
    </tr>
    <tr>
        <td><a href="string.md#endsWith">Termina con</a></td><td>Questa funzione viene utilizzata per determinare se una stringa termina con una sottostringa specificata</td>
    </tr>
        </tr>
    <tr>
        <td><a href="string.md#equals">Uguale a</a></td><td>Questa funzione viene utilizzata per determinare se una stringa non inizia con una sottostringa specificata, con distinzione tra maiuscole e minuscole</td>
    </tr>
    <tr>
        <td><a href="string.md#equalsIgnoreCase">Uguale a ignora distinzione tra maiuscole e minuscole</a></td><td>Questa funzione viene utilizzata per determinare se una stringa non inizia con una sottostringa specificata, senza distinzione tra maiuscole e minuscole</td>
    </tr>
    <tr>
        <td><a href="string.md#extractEmailDomain">Estrai dominio e-mail</a></td><td>Questa funzione viene utilizzata per estrarre il dominio di un indirizzo e-mail</td>
    </tr>
    <tr>
        <td><a href="string.md#format-currency">Formato valuta</a></td><td>Questa funzione converte qualsiasi numero nella corrispondente rappresentazione della valuta sensibile alla lingua, a seconda delle impostazioni locali passate come stringa nel secondo argomento.</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-host">Ottieni host URL</a></td><td>Questa funzione viene utilizzata per ottenere l’host URL.</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-path">Ottieni percorso URL</a></td><td>Questa funzione viene utilizzata per ottenere il percorso URL</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-protocol">Ottieni protocollo URL</a></td><td>Questa funzione viene utilizzata per ottenere il protocollo URL</td>
    </tr>
    <tr>
        <td><a href="string.md#index-of">Indice di</a></td><td>Questa funzione restituisce la posizione (nel primo argomento) della prima occorrenza del secondo parametro. Restituisce -1 se non viene trovata alcuna corrispondenza</td>
    </tr>
    <tr>
        <td><a href="string.md#isEmpty">IsEmpty</a></td><td>Questa funzione viene utilizzata per verificare se una stringa o un’espressione è vuota.</td>
    </tr>
    <tr>
        <td><a href="string.md#is-not-empty">Non è vuoto</a></td><td>Questa funzione restituisce true, se la stringa nel parametro non è vuota.</td>
    </tr>
    <tr>
        <td><a href="string.md#last-index-of">Ultimo indice di</a></td><td>Questa funzione restituisce la posizione (nel primo argomento) dell’ultima occorrenza del secondo parametro. Restituisce -1 se non viene trovata alcuna corrispondenza.</td>
    </tr>
    <tr>
        <td><a href="string.md#leftTrim">Taglia a sinistra</a></td><td>Questa funzione rimuove gli spazi bianchi dall’inizio di una stringa</td>
    </tr>
    <tr>
        <td><a href="string.md#length">Lunghezza</a></td><td>Questa funzione viene utilizzata per ottenere il numero di caratteri in una stringa o in un’espressione</td>
    </tr>
    <tr>
        <td><a href="string.md#like">Mi piace</a></td><td>Questa funzione viene utilizzata per determinare se una stringa corrisponde a un pattern specificato</td>
    </tr>
    <tr>
        <td><a href="string.md#lower">Minuscolo</a></td><td>Questa funzione converte una stringa in lettere minuscole.</td>
    </tr>
    <tr>
        <td><a href="string.md#mask">Maschera</a></td><td>Questa funzione viene utilizzata per sostituire una parte di stringa con caratteri "X".</td>
    </tr>
    <tr>
        <td><a href="string.md#matches">Corrisponde a</a></td><td>Questa funzione viene utilizzata per determinare se una stringa corrisponde a una specifica espressione regolare.</td>
    </tr>
    <tr>
        <td><a href="string.md#md5">MD5</a></td><td>Questa funzione restituisce l’hash MD5 della stringa di input.</td>
    </tr>
    <tr>
        <td><a href="string.md#notEqualTo">Non uguale a</a></td><td>Questa funzione viene utilizzata per determinare se una stringa non è uguale alla stringa specificata</td>
    </tr>
    <tr>
        <td><a href="string.md#not-equal-with-ignore-case">Non è uguale con ignora distinzione tra maiuscole e minuscole</a></td><td>Questa funzione confronta due stringhe ignorando la distinzione tra maiuscole e minuscole.</td>
    </tr>
    <tr>
        <td><a href="string.md#regexGroup">Gruppo di espressioni regolari</a></td><td>Questa funzione viene utilizzata per estrarre informazioni specifiche, in base all’espressione regolare fornita</td>
    </tr>
    <tr>
        <td><a href="string.md#replace">Sostituisci</a></td><td>Questa funzione sostituisce una determinata sottostringa in una stringa con un’altra sottostringa</td>
    </tr>
    <tr>
        <td><a href="string.md#replaceAll">Sostituisci tutto</a></td><td>Questa funzione sostituisce tutte le sottostringhe di un testo che corrisponde alla "destinazione" con la stringa letterale "replace" specificata</td>
    </tr>
    <tr>
        <td><a href="string.md#rightTrim">Taglia a destra</a></td><td>Questa funzione rimuove gli spazi bianchi dalla fine di una stringa. </td>
    </tr>
    <tr>
        <td><a href="string.md#split">Dividi</a></td><td>Questa funzione viene utilizzata per dividere una stringa per un determinato carattere</td>
    </tr>
    <tr>
        <td><a href="string.md#startsWith">Inizia con</a></td><td>Questa funzione viene utilizzata per determinare se una stringa inizia con una sottostringa specificata</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-date">Stringa a data</a></td><td>Questa funzione converte un valore stringa in un valore data-ora.</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-integer">Stringa a numero intero</a></td><td>Questa funzione converte un valore stringa in un valore intero.</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-number">Stringa a numero</a></td><td>Questa funzione viene utilizzata per convertire una stringa in numero. In caso di input non valido, restituisce la stessa stringa come output.</td>
    </tr>
    <tr>
        <td><a href="string.md#sub-string">Sottostringa</a></td><td>Questa funzione restituisce la sottostringa dell’espressione della stringa tra l’indice iniziale e l’indice finale.</td>
    </tr>
    <tr>
        <td><a href="string.md#titleCase">Tutte iniziali maiuscole</a></td><td>Questa funzione viene utilizzata per rendere maiuscole le prime lettere di ogni parola di una stringa</td>
    </tr>
    <tr>
        <td><a href="string.md#to-bool">A valore booleano</a></td><td>Questa funzione converte un valore di un argomento in un valore booleano, a seconda del tipo.</td>
    </tr>
    <tr>
        <td><a href="string.md#to-date-time">A data/ora</a></td><td>Questa funzione viene utilizzata per convertire una stringa in data. In caso di input non valido, restituisce la data epoca come output.</td>
    </tr>
    <tr>
        <td><a href="string.md#to-date-time-only">Solo a data/ora</a></td><td>Questa funzione converte un valore di argomento in un valore solo di data e ora. In caso di input non valido, restituisce la data epoca come output.</td>
    </tr>
    <tr>
        <td><a href="string.md#trim">Taglia</a></td><td>Questa funzione rimuove gli spazi bianchi dall’inizio e dalla fine di una stringa.</td>
    </tr>
    <tr>
        <td><a href="string.md#upper">Maiuscolo</a></td><td>Questa funzione converte una stringa in lettere maiuscole.</td>
    </tr>
    <tr>
        <td><a href="string.md#url-decode">Decodifica URL</a></td><td>Questa funzione viene utilizzata per decodificare una stringa codificato dell’URL.</td>
    </tr>
    <tr>
        <td><a href="string.md#url-encode">Codifica URL</a></td><td>Questa funzione viene utilizzata per la codifica URL di una stringa.</td>
    </tr>
</table>


## Helper{#helper-helper}

Gli helper sono descritti in [questa pagina](helpers.md).


<table>
    <tr>
        <td><a href="helpers.md#default">Valore di fallback predefinito</a></td><td>Questa funzione viene utilizzata per eseguire il rendering di una variabile con il valore predefinito</td>
    </tr>
    <tr>
        <td><a href="helpers.md#each">Each</a></td><td>Questa funzione viene utilizzata per eseguire iterazioni su un array</td>
    </tr>
    <tr>
        <td><a href="helpers.md#if-function">Se</a></td><td>Questa funzione viene utilizzata per definire un blocco condizionale. Se la valutazione dell’espressione restituisce true, viene eseguito il rendering del blocco.</td>
    </tr>
    <tr>
        <td><a href="helpers.md#let">Let</a></td><td>Questa funzione consente di memorizzare un’espressione come variabile da utilizzare successivamente in una query</td>
    </tr>
   <tr>
        <td><a href="helpers.md#unless">Unless</a></td><td>Questa funzione viene utilizzata per definire un blocco condizionale. Se la valutazione dell’espressione restituisce false, viene eseguito il rendering del blocco</td>
    </tr>
    <tr>
        <td><a href="helpers.md#with">With</a></td><td>Questa funzione viene utilizzata per modificare il token di valutazione della parte modello</td>
    </tr>
</table>

## Operatori{#operators-helper}

### Funzioni aritmetiche {#arithmetic-helper}

Le funzioni aritmetiche vengono utilizzate per eseguire calcoli di base sui valori.

<table>
    <tr>
        <td><a href="arithmetic-functions.md#add">Addizione</a></td><td>Questo operatore viene utilizzato per trovare la somma di due espressioni di argomento</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#divide">Dividi</a></td><td>Questo operatore viene utilizzato per trovare il quoziente di due espressioni di argomento</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#multiply">Moltiplicazione</a></td><td>Questo operatore viene utilizzato per trovare il prodotto di due espressioni di argomento</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#remainder">Rimanente</a> </td><td>Questo operatore viene utilizzato per trovare il resto dopo aver diviso le due espressioni di argomento</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#substract">Sottrazione</a> </td><td>Questo operatore trova la differenza tra due espressioni</td>
    </tr>
</table>


### Funzioni booleane {#boolean-functions}

Le funzioni booleane vengono utilizzate per eseguire la logica booleana su elementi diversi.

<table>
    <tr>
        <td><a href="operators.md#and">E</a></td><td>Questo operatore crea una congiunzione logica</td>
    </tr>
    <tr>
        <td><a href="operators.md#or">Oppure</a></td><td>Questo operatore crea una disgiunzione logica</td>
    </tr>
</table>


### Funzioni di confronto {#comparison-functions}

Le funzioni di confronto vengono utilizzate per confrontare espressioni e valori diversi, restituendo di conseguenza true o false.

<table>
    <tr>
        <td><a href="operators.md#equals">Uguale a</a></td><td>Questa operazione controlla se i valori sono uguali</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthan">Maggiore di</a></td><td>Questo operatore controlla se il primo valore è maggiore del secondo valore</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthanorequal">Maggiore o uguale a</a></td><td>Questo operatore controlla se il primo valore è maggiore o uguale al secondo valore</td>
    </tr>
    <tr>
        <td><a href="operators.md#lessthanorequal">Minore o uguale a</a> </td><td>Questo operatore controlla se il primo valore è minore o uguale al secondo valore</td>
    </tr>
    <tr>
        <td><a href="operators.md#notequal">Non è uguale a</a></td><td>Questo operatore controlla se l’espressione data non è uguale al valore dato</td>
    </tr>
</table>

## Video introduttivo{#video}

Scopri come trasformare i valori di personalizzazione utilizzando le funzioni di assistenza alla personalizzazione e studia diversi casi d’uso per le funzioni di supporto.

>[!VIDEO](https://video.tv.adobe.com/v/334244?quality=12)
