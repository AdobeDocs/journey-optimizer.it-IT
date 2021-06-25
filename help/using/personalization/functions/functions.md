---
title: Libreria funzioni helper
description: Libreria funzioni Journey Optimizer Helper
feature: Personalizzazione
topic: Personalizzazione
role: Data Engineer
level: Experienced
source-git-commit: 94f3fb815fdeec9853351be9bc41b0579cfc6c5b
workflow-type: tm+mt
source-wordcount: '1181'
ht-degree: 2%

---


# Libreria funzioni helper{#functionsL}

Utilizza il linguaggio dei modelli [!DNL Journey Optimizer] per eseguire operazioni sui dati, ad esempio calcoli, formattazione dei dati o conversioni, condizioni e manipolarli nel contesto della personalizzazione. Scopri le linee guida sulla sintassi di personalizzazione in [questa pagina](../personalization-syntax.md).

[!DNL :arrow_forward:] [Scopri come utilizzare le funzioni helper nel video](#video)

Il linguaggio modello viene sfruttato nelle funzioni di supporto disponibili nell’elenco a discesa di personalizzazione dell’editor espressioni, come segue:

![](../assets/access-helper-functions.png)



Nell’ [!DNL Journey Optimizer] editor espressioni, le funzioni helper sono raggruppate in tre categorie: [Funzioni](#functions-helper), [Helpers](#helper-helper) e [Operatori](#operators-helper).

## Funzioni{#functions-helper}

**Funzioni array**

<table>
    <tr>
        <td><a href="aggregation.md#average">Medio</a></td><td>Questa funzione restituisce la media aritmetica di tutti i valori selezionati all'interno della matrice</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#in">In</a></td><td>Questa funzione consente di determinare se un elemento è membro di una matrice o di un elenco</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#min">Minimo</a></td><td>Questa funzione restituisce il valore più piccolo tra tutti i valori selezionati all'interno della matrice</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count">Conteggio</a></td><td>Questa funzione restituisce il numero di elementi all'interno della matrice specificata</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#includes">Include</a></td><td>Questa funzione determina se una matrice o un elenco contiene un elemento specificato</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#notin">Non in</a></td><td>Questa funzione determina se un elemento non è membro di una matrice o di un elenco</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct">Distinto</a></td><td>Questa funzione ottiene valori da una matrice o da un elenco con valori duplicati rimossi</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#intersects">Intersecazioni</a></td><td>Questa funzione determina se due array o elenchi hanno almeno un membro comune</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#subset">Sottoinsieme di</a></td><td>Questa funzione determina se un array specifico (array A) è un sottoinsieme di un altro array (array B), ossia se tutti gli elementi dell'array A sono elementi dell'array B</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#head">Primo elemento</a></td><td>Questa funzione restituisce il primo elemento di un array o di un elenco</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#last-n">Ultimo n nella matrice</a></td><td>Questa funzione restituisce gli ultimi elementi `N` in un array, se ordinati in ordine crescente in base all'espressione numerica specificata</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#sum">Somma</a></td><td>Questa funzione restituisce la somma di tutti i valori selezionati all'interno della matrice</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#first-n">Primo n nell'array</a></td><td>Questa funzione restituisce i primi elementi `N` in un array, se ordinati in ordine crescente in base all'espressione numerica specificata</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#max">Massimo</a></td><td>Questa funzione restituisce il valore più alto tra tutti i valori selezionati all'interno di una matrice</td>
    </tr>
    <tr>
    <td><a href="arrays-list.md#superset">Superset di</a></td><td>Questa funzione termina se un array specifico (array A) è un superset di un altro array (array B), ovvero se l'array A contiene tutti gli elementi dell'array B</td>
    </tr>
</table>


**Funzioni mappa**

<table>
    <tr>
        <td><a href="maps.md#get">Get</a></td><td>Questa funzione viene utilizzata per recuperare il valore di una mappa per una determinata chiave</td>
    </tr>
    <tr>
        <td><a href="maps.md#keys">Chiavi</a></td><td>Questa funzione viene utilizzata per recuperare tutte le chiavi di una determinata mappa</td>
    </tr>
    <tr>
        <td><a href="maps.md#values">Valori</a></td><td>Questa funzione recupera tutti i valori di una data mappa</td>
    </tr>
</table>

**Funzioni oggetto**

<table>
    <tr>
        <td><a href="objects.md#isNotNull">Non è Null</a></td><td>Questa funzione viene utilizzata per determinare se esiste un riferimento a un oggetto</td>
    </tr>
    <tr>
        <td><a href="objects.md#isNull">È nullo</a></td><td>Questa funzione viene utilizzata per determinare se non esiste un riferimento a un oggetto</td>
    </tr>
</table>

**Funzioni stringa**

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
        <td><a href="string.md#isEmpty">IsEmpty</a></td><td>Questa funzione viene utilizzata per verificare se una stringa o un'espressione è vuota.</td>
    </tr>
    <tr>
        <td><a href="string.md#leftTrim">Taglio a sinistra</a></td><td>Questa funzione rimuove gli spazi bianchi dall'inizio di una stringa</td>
    </tr>
    <tr>
        <td><a href="string.md#length">Length</a></td><td>Questa funzione viene utilizzata per ottenere il numero di caratteri in una stringa o un'espressione</td>
    </tr>
    <tr>
        <td><a href="string.md#like">Simile</a></td><td>Questa funzione viene utilizzata per determinare se una stringa corrisponde a un pattern specificato</td>
    </tr>
    <tr>
        <td><a href="string.md#lower">Custodia minuscola</a></td><td>Questa funzione converte una stringa in lettere minuscole</td>
    </tr>
    <tr>
        <td><a href="string.md#matches">Corrisponde</a></td><td>Questa funzione viene utilizzata per determinare se una stringa corrisponde a una specifica espressione regolare</td>
    </tr>
    <tr>
        <td><a href="string.md#notEqualTo">Non è uguale a</a></td><td>Questa funzione viene utilizzata per determinare se una stringa non è uguale alla stringa specificata</td>
    </tr>
    <tr>
        <td><a href="string.md#regexGroup">Gruppo di espressioni regolari</a></td><td>Questa funzione viene utilizzata per estrarre informazioni specifiche, in base all'espressione regolare fornita</td>
    </tr>
    <tr>
        <td><a href="string.md#replace">Replace</a></td><td>Questa funzione sostituisce una stringa secondaria specificata in una stringa con un'altra sottostringa</td>
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
        <td><a href="string.md#titleCase">Caso del titolo</a></td><td>Questa funzione viene utilizzata per far maiuscola alle prime lettere di ogni parola di una stringa</td>
    </tr>
    <tr>
        <td><a href="string.md#trim">Rifila</a></td><td>Questa funzione rimuove gli spazi bianchi dall'inizio e dalla fine di una stringa</td>
    </tr>
    <tr>
        <td><a href="string.md#upper">Custodia superiore</a></td><td>Questa funzione converte una stringa in lettere maiuscole</td>
    </tr>
</table>


## Assistenza{#helper-helper}

Gli helper sono descritti in [questa pagina](helpers.md).


<table>
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


### Funzioni booleane

Le funzioni booleane vengono utilizzate per eseguire la logica booleana su elementi diversi.

<table>
    <tr>
        <td><a href="operators.md#and">E</a></td><td>Questo operatore crea una congiunzione logica</td>
    </tr>
    <tr>
        <td><a href="operators.md#not">Se</a></td><td>Questo operatore risolve un'espressione a seconda che una condizione specificata sia vera</td>
    </tr>
    <tr>
        <td><a href="operators.md#not">Non</a></td><td>Questo operatore crea una negazione logica</td>
    </tr>
    <tr>
        <td><a href="operators.md#or">Oppure</a></td><td>Questo operatore crea una disgiunzione logica</td>
    </tr>
</table>


### Funzioni di confronto

Le funzioni di confronto vengono utilizzate per confrontare espressioni e valori diversi e restituiscono true o false di conseguenza.

<table>
    <tr>
        <td><a href="operators.md#and">Uguale</a></td><td>Questa operazione controlla se i valori sono uguali</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthan">Maggiore di</a></td><td>Questo operatore controlla se il primo valore è maggiore del secondo valore</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthanorequal">Maggiore o uguale a</a></td><td>Questo operatore controlla se il primo valore è maggiore o uguale al secondo valore</td>
    </tr>
    <tr>
        <td><a href="operators.md#notequal">Non è uguale a</a></td><td>Questo operatore controlla se un'espressione specificata non è uguale a un valore</td>
    </tr>
    <tr>
        <td><a href="operators.md#lessthanorequal">Minore o uguale a</a> </td><td>Questo operatore controlla se il primo valore è minore o uguale al secondo valore</td>
    </tr>
</table>

## Video introduttivo{#video}

Scopri come trasformare i valori di personalizzazione utilizzando le funzioni di supporto della personalizzazione e comprendere diversi casi d’uso per le funzioni di supporto.

>[!VIDEO](https://video.tv.adobe.com/v/334244?quality=12)