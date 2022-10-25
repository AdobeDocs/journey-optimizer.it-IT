---
title: Guida introduttiva alle funzioni Helper
description: Libreria funzioni Journey Optimizer Helper
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 9b0b0d8e-a819-4d2e-a241-f3c4d104eab9
source-git-commit: 315c3e8c04b2e3944d0d5b2befb205acbe0ef7c9
workflow-type: tm+mt
source-wordcount: '1738'
ht-degree: 3%

---

# Guida introduttiva alle funzioni Helper{#functions}

Utilizzo [!DNL Journey Optimizer] modello del linguaggio per eseguire operazioni sui dati, ad esempio calcoli, formattazione dei dati o conversioni, condizioni e manipolarli nel contesto della personalizzazione. Scopri le linee guida per la sintassi di personalizzazione in [questa pagina](../personalization-syntax.md).

➡️ [Scopri come utilizzare le funzioni helper in questo video](#video)

Il linguaggio modello viene sfruttato nelle funzioni helper disponibili nell’elenco a discesa di personalizzazione dell’editor espressioni, come segue:

![](../assets/access-helper-functions.png)

In [!DNL Journey Optimizer] Editor espressioni, funzioni helper sono raggruppate in tre categorie: [Funzioni](#functions-helper), [Helper](#helper-helper) e [Operatori](#operators-helper).

Seleziona una categoria per accedere a sottocategorie e funzioni.

Accedere alle sottocategorie facendo clic sul pulsante `>` icona. Seleziona una funzione facendo clic sul pulsante `+` icona: la funzione viene aggiunta automaticamente alla schermata di personalizzazione.

Fai clic sul pulsante `...` per visualizzare la descrizione della funzione e aggiungerla ai preferiti. [Ulteriori informazioni](../personalize.md#fav)

## Funzioni{#functions-helper}

### Funzioni di aggregazione e array

<table>
    <tr>
        <td><a href="aggregation.md#average">Medio</a></td><td>Questa funzione restituisce la media aritmetica di tutti i valori selezionati all'interno della matrice</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count">Conteggio</a></td><td>Questa funzione restituisce il numero di elementi all'interno della matrice specificata</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count-only-null">Solo conteggio Null</a></td><td>Questa funzione conta il numero di valori nulli nell'elenco.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count-with-null">Conteggio con Null</a></td><td>Questa funzione conta tutti gli elementi dell'elenco, inclusi i valori nulli</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct">Distinto</a></td><td>Questa funzione ottiene valori da una matrice o da un elenco con valori duplicati rimossi</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct-count-with-null">Conteggio Distinto Con Null</a></td><td>Questa funzione conta il numero di valori diversi, inclusi i valori nulli</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#head">Primo elemento</a></td><td>Questa funzione restituisce il primo elemento di un array o di un elenco</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#first-n">Primo n nell'array</a></td><td>Questa funzione restituisce i primi elementi `N` in un array, se ordinati in ordine crescente in base all'espressione numerica specificata</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#in">In</a></td><td>Questa funzione consente di determinare se un elemento è membro di una matrice o di un elenco</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#includes">Include</a></td><td>Questa funzione determina se una matrice o un elenco contiene un elemento specificato</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#intersects">Intersecazioni</a></td><td>Questa funzione determina se due array o elenchi hanno almeno un membro comune</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#last-n">Ultimo n nella matrice</a></td><td>Questa funzione restituisce gli ultimi elementi `N` in un array, se ordinati in ordine crescente in base all'espressione numerica specificata</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#max">Massimo</a></td><td>Questa funzione restituisce il più grande di tutti i valori selezionati all'interno di una matrice</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#min">Minimo</a></td><td>Questa funzione restituisce il valore più piccolo tra tutti i valori selezionati all'interno della matrice</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#notin">Non in</a></td><td>Questa funzione determina se un elemento non è membro di una matrice o di un elenco</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#subset">Sottoinsieme di</a></td><td>Questa funzione determina se un array specifico (array A) è un sottoinsieme di un altro array (array B), ossia se tutti gli elementi dell'array A sono elementi dell'array B</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#sum">Somma</a></td><td>Questa funzione restituisce la somma di tutti i valori selezionati all'interno della matrice</td>
    </tr>
    <tr>
    <td><a href="arrays-list.md#superset">Superset di</a></td><td>Questa funzione determina se un array specifico (array A) è un superset di un altro array (array B), ovvero se l'array A contiene tutti gli elementi dell'array B</td>
    </tr>
</table>

### Funzioni di data e ora{#date-functions}

<table>
    <tr>
        <td><a href="dates.md#age">Età</a></td><td>Questa funzione recupera l'età da una data specificata</td>
    </tr>
    <tr>
        <td><a href="dates.md#current">Tempo corrente in millisecondi</a></td><td>Questa funzione recupera l'ora corrente in millisecondi epoch</td>
    </tr>
    <tr>
        <td><a href="dates.md#date-diff">Differenza tra date</a></td><td>Questa funzione recupera la differenza tra due date in numero di giorni</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-week">Giorno della settimana</a></td><td>Questa funzione recupera il giorno della settimana</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-year">Giorno dell’anno</a></td><td>Questa funzione recupera il giorno dell'anno</td>
    </tr>
    <tr>
        <td><a href="dates.md#format-date">Data del formato</a></td><td>Questa funzione formatta un valore di ora della data</td>
    </tr>
    <tr>
        <td><a href="dates.md#set-days">Imposta giorni</a></td><td>Questa funzione imposta il giorno del mese per la data-ora specificata</td>
    </tr>
    <tr>
        <td><a href="dates.md#set-hours">Imposta ore</a></td><td>Questa funzione imposta l'ora della data-ora</td>
    </tr>
    <tr>
        <td><a href="dates.md#to-utc">A UTC</a></td><td>Questa funzione converte un datetime in UTC</td>
    </tr>
    <tr>
        <td><a href="dates.md#week-of-year">Settimana dell’anno</a></td><td>Questa funzione restituisce la settimana dell'anno</td>
    </tr>
</table>
</table>

### Funzioni mappa {#map-functions}

<table>
    <tr>
        <td><a href="maps.md#get">Ottenere</a></td><td>Questa funzione viene utilizzata per recuperare il valore di una mappa per una determinata chiave</td>
    </tr>
    <tr>
        <td><a href="maps.md#keys">Chiavi</a></td><td>Questa funzione viene utilizzata per recuperare tutte le chiavi di una determinata mappa</td>
    </tr>
    <tr>
        <td><a href="maps.md#values">Valori</a></td><td>Questa funzione recupera tutti i valori di una data mappa</td>
    </tr>
</table>

### Funzioni matematiche {#math-functions}

<table>
    <tr>
        <td><a href="objects.md#absolute">Assoluto</a></td><td>Questa funzione converte un numero che è valore assoluto</td>
    </tr>
    <tr>
        <td><a href="objects.md#random">Random</a></td><td>Questa funzione restituisce un valore casuale compreso tra 0 e 1</td>
    </tr>
    <tr>
        <td><a href="objects.md#round-down">Round down</a></td><td>Questa funzione consente di arrotondare un numero</td>
    </tr>
    <tr>
        <td><a href="objects.md#round-up">Arrotondamento</a></td><td>Questa funzione arrotonda un numero</td>
    </tr>
    <tr>
        <td><a href="objects.md#to-percentage">A percentuale</a></td><td>Questa funzione converte un numero in percentuale</td>
    </tr>
    <tr>
        <td><a href="objects.md#to-precision">Precisione</a></td><td>Questa funzione converte un numero in una precisione richiesta</td>
    </tr>
</table>

### Funzioni oggetto {#object-functions}

<table>
    <tr>
        <td><a href="objects.md#isNotNull">Non è Null</a></td><td>Questa funzione viene utilizzata per determinare se esiste un riferimento a un oggetto</td>
    </tr>
    <tr>
        <td><a href="objects.md#isNull">È nullo</a></td><td>Questa funzione viene utilizzata per determinare se non esiste un riferimento a un oggetto</td>
    </tr>
</table>

### Funzioni stringa {#string-functions}

<table>
    <tr>
        <td><a href="string.md#camelCase">Cammello</a></td><td>Questa funzione viene utilizzata per capitalizzare la prima lettera di ogni parola di una stringa</td>
    </tr>
    <tr>
        <td><a href="string.md#concat">Concat</a></td><td>Questa funzione viene utilizzata per combinare due stringhe in una</td>
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
        <td><a href="string.md#encode64">Codifica 64</a></td><td>Questa funzione viene utilizzata per codificare o decodificare una stringa</td>
    </tr>
    <tr>
        <td><a href="string.md#endsWith">Termina con</a></td><td>Questa funzione viene utilizzata per determinare se una stringa termina con una sottostringa specificata</td>
    </tr>
        </tr>
    <tr>
        <td><a href="string.md#equals">È uguale a</a></td><td>Questa funzione viene utilizzata per determinare se una stringa non inizia con una sottostringa specificata, con distinzione tra maiuscole e minuscole</td>
    </tr>
    <tr>
        <td><a href="string.md#equalsIgnoreCase">Uguale a Ignore Case</a></td><td>Questa funzione consente di determinare se una stringa non inizia con una sottostringa specificata, senza distinzione tra maiuscole e minuscole</td>
    </tr>
    <tr>
        <td><a href="string.md#extractEmailDomain">Estrai dominio e-mail</a></td><td>Questa funzione viene utilizzata per estrarre il dominio di un indirizzo e-mail</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-host">Ottieni host url</a></td><td>Questa funzione viene utilizzata per ottenere l'host url.</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-path">Ottieni percorso URL</a></td><td>Questa funzione viene utilizzata per ottenere il percorso url</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-protocol">Ottieni protocollo url</a></td><td>Questa funzione viene utilizzata per ottenere il protocollo url</td>
    </tr>
    <tr>
        <td><a href="string.md#index-of">Indice</a></td><td>Questa funzione restituisce la posizione (nel primo argomento) della prima occorrenza del secondo parametro. Restituisce -1 se non è presente alcuna corrispondenza</td>
    </tr>
    <tr>
        <td><a href="string.md#isEmpty">IsEmpty</a></td><td>Questa funzione viene utilizzata per verificare se una stringa o un'espressione è vuota.</td>
    </tr>
    <tr>
        <td><a href="string.md#is-not-empty">Non è vuoto</a></td><td>Questa funzione restituisce true se la stringa nel parametro non è vuota.</td>
    </tr>
    <tr>
        <td><a href="string.md#last-index-of">Ultimo Indice</a></td><td>Questa funzione restituisce la posizione (nel primo argomento) dell'ultima occorrenza del secondo parametro. Restituisce -1 se non è presente alcuna corrispondenza.</td>
    </tr>
    <tr>
        <td><a href="string.md#leftTrim">Taglio a sinistra</a></td><td>Questa funzione rimuove gli spazi bianchi dall'inizio di una stringa</td>
    </tr>
    <tr>
        <td><a href="string.md#length">Lunghezza</a></td><td>Questa funzione viene utilizzata per ottenere il numero di caratteri in una stringa o un'espressione</td>
    </tr>
    <tr>
        <td><a href="string.md#like">Simile</a></td><td>Questa funzione viene utilizzata per determinare se una stringa corrisponde a un pattern specificato</td>
    </tr>
    <tr>
        <td><a href="string.md#lower">Custodia minuscola</a></td><td>Questa funzione converte una stringa in lettere minuscole</td>
    </tr>
    <tr>
        <td><a href="string.md#mask">Maschera</a></td><td>Questa funzione viene utilizzata per sostituire una parte di una stringa con caratteri "X".</td>
    </tr>
    <tr>
        <td><a href="string.md#matches">Corrisponde</a></td><td>Questa funzione viene utilizzata per determinare se una stringa corrisponde a una specifica espressione regolare</td>
    </tr>
    <tr>
        <td><a href="string.md#md5">MD5</a></td><td>Questa funzione restituisce hash md5 della stringa di input.</td>
    </tr>
    <tr>
        <td><a href="string.md#notEqualTo">Non uguale a</a></td><td>Questa funzione viene utilizzata per determinare se una stringa non è uguale alla stringa specificata</td>
    </tr>
    <tr>
        <td><a href="string.md#not-equal-with-ignore-case">Non uguale a Ignora maiuscole/minuscole</a></td><td>Questa funzione confronta due stringhe ignorando le maiuscole/minuscole.</td>
    </tr>
    <tr>
        <td><a href="string.md#regexGroup">Gruppo di espressioni regolari</a></td><td>Questa funzione viene utilizzata per estrarre informazioni specifiche, in base all'espressione regolare fornita</td>
    </tr>
    <tr>
        <td><a href="string.md#replace">Sostituisci</a></td><td>Questa funzione sostituisce una stringa secondaria specificata in una stringa con un'altra sottostringa</td>
    </tr>
    <tr>
        <td><a href="string.md#replaceAll">Sostituisci tutto</a></td><td>Questa funzione sostituisce tutte le sottostringhe di un testo che corrisponde alla stringa "target" con la stringa letterale di "sostituzione" specificata</td>
    </tr>
    <tr>
        <td><a href="string.md#rightTrim">Taglio a destra</a></td><td>Questa funzione rimuove gli spazi bianchi dalla fine di una stringa </td>
    </tr>
    <tr>
        <td><a href="string.md#split">Dividere</a></td><td>Questa funzione viene utilizzata per dividere una stringa per un carattere specificato</td>
    </tr>
    <tr>
        <td><a href="string.md#startsWith">Inizia con</a></td><td>Questa funzione viene utilizzata per determinare se una stringa inizia con una sottostringa specificata</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-date">Stringa alla data</a></td><td>Questa funzione viene utilizzata per convertire la stringa in data. Restituisce la data epoch come output per input non valido.</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-integer">Stringa a numero intero</a></td><td>Questa funzione converte un valore stringa in un valore intero.</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-number">Stringa al numero</a></td><td>Questa funzione viene utilizzata per convertire una stringa in numero. Restituisce la stessa stringa dell'output per input non valido.</td>
    </tr>
    <tr>
        <td><a href="string.md#sub-string">Sottostringa</a></td><td>Questa funzione restituisce la sottostringa dell'espressione stringa tra l'indice begin e l'indice end.</td>
    </tr>
    <tr>
        <td><a href="string.md#titleCase">Caso del titolo</a></td><td>Questa funzione viene utilizzata per far maiuscola alle prime lettere di ogni parola di una stringa</td>
    </tr>
    <tr>
        <td><a href="string.md#to-bool">A Bool</a></td><td>Questa funzione converte un valore di argomento in un valore booleano, a seconda del tipo.</td>
    </tr>
    <tr>
        <td><a href="string.md#to-date-time">A ora</a></td><td>Questa funzione viene utilizzata per convertire la stringa in data. Restituisce la data epoch come output per input non valido.</td>
    </tr>
    <tr>
        <td><a href="string.md#to-date-time-only">Solo per data</a></td><td>Questa funzione converte un valore di argomento in un valore solo di data e ora. Restituisce la data epoch come output per input non valido.</td>
    </tr>
    <tr>
        <td><a href="string.md#trim">Trim (Taglia)</a></td><td>Questa funzione rimuove gli spazi bianchi dall'inizio e dalla fine di una stringa</td>
    </tr>
    <tr>
        <td><a href="string.md#upper">Custodia superiore</a></td><td>Questa funzione converte una stringa in lettere maiuscole</td>
    </tr>
    <tr>
        <td><a href="string.md#url-decode">decodifica URL</a></td><td>Questa funzione viene utilizzata per decodificare una stringa codificata in url.</td>
    </tr>
    <tr>
        <td><a href="string.md#url-encode">Codifica URL</a></td><td>Questa funzione viene utilizzata per codificare in url una stringa.</td>
    </tr>
</table>


## Assistenza{#helper-helper}

Gli aiutanti sono descritti in [questa pagina](helpers.md).


<table>
    <tr>
        <td><a href="helpers.md#default">Valore di fallback predefinito</a></td><td>Questa funzione consente di eseguire il rendering di una variabile con impostazione predefinita</td>
    </tr>
    <tr>
        <td><a href="helpers.md#each">Ogni</a></td><td>Questa funzione viene utilizzata per eseguire iterazioni su un array</td>
    </tr>
    <tr>
        <td><a href="helpers.md#if-function">Se</a></td><td>Questa funzione viene utilizzata per definire un blocco condizionale - se la valutazione dell’espressione restituisce true, viene eseguito il rendering del blocco</td>
    </tr>
    <tr>
        <td><a href="helpers.md#let">Lasciare</a></td><td>Questa funzione consente di memorizzare un’espressione come variabile da utilizzare successivamente in una query</td>
    </tr>
   <tr>
        <td><a href="helpers.md#unless">A meno che</a></td><td>Questa funzione viene utilizzata per definire un blocco condizionale - se la valutazione dell’espressione restituisce false, viene eseguito il rendering del blocco</td>
    </tr>
    <tr>
        <td><a href="helpers.md#with">Con</a></td><td>Questa funzione viene utilizzata per modificare il token di valutazione della parte modello</td>
    </tr>
</table>

## Operatori{#operators-helper}

### Funzioni aritmetiche {#arithmetic-helper}

Le funzioni aritmetiche vengono utilizzate per eseguire calcoli di base sui valori.

<table>
    <tr>
        <td><a href="arithmetic-functions.md#add">Aggiunta</a></td><td>Questo operatore viene utilizzato per trovare la somma di due espressioni di argomento</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#divide">Dividi</a></td><td>Questo operatore viene utilizzato per trovare il quoziente di due espressioni di argomento</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#multiply">Moltiplicazione</a></td><td>Questo operatore viene utilizzato per trovare il prodotto di due espressioni di argomento</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#remainder">Resto</a> </td><td>Questo operatore viene utilizzato per trovare il resto dopo aver diviso le due espressioni di argomento</td>
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

Le funzioni di confronto vengono utilizzate per confrontare espressioni e valori diversi e restituiscono true o false di conseguenza.

<table>
    <tr>
        <td><a href="operators.md#equals">È uguale a</a></td><td>Questa operazione controlla se i valori sono uguali</td>
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
        <td><a href="operators.md#notequal">Non è uguale a</a></td><td>Questo operatore controlla se un'espressione specificata non è uguale a un valore</td>
    </tr>
</table>

## Video introduttivo{#video}

Scopri come trasformare i valori di personalizzazione utilizzando le funzioni di assistenza alla personalizzazione e studia diversi casi d’uso per le funzioni di supporto.

>[!VIDEO](https://video.tv.adobe.com/v/334244?quality=12)
