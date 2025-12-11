---
title: Introduzione alle funzioni helper
description: Libreria di funzioni Journey Optimizer Helper
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 9b0b0d8e-a819-4d2e-a241-f3c4d104eab9
source-git-commit: cdf9eadc36d7e7b3538690a7a165bc39eccc40b5
workflow-type: tm+mt
source-wordcount: '2458'
ht-degree: 2%

---

# Introduzione alle funzioni helper{#functions}

Le funzioni di supporto consentono di trasformare e manipolare i dati all’interno dei contenuti personalizzati. Puoi utilizzarli per eseguire calcoli, formattare dati, applicare condizioni ed eseguire varie operazioni per creare esperienze dinamiche e personalizzate per i clienti.

Queste funzioni sfruttano il linguaggio di modelli [!DNL Journey Optimizer]. Scopri le linee guida sulla sintassi di personalizzazione in [questa pagina](../personalization-syntax.md).

➡️ [Scopri come utilizzare le funzioni di assistenza in questo video](#video)

## Accedere alle funzioni di assistenza

Le funzioni helper sono disponibili dal menu delle funzioni dell’editor di personalizzazione:

![](../assets/access-helper-functions.png)

Le funzioni sono organizzate in tre categorie per facilitarne la navigazione:

* **[Funzioni](#functions-helper)** - Operazioni di trasformazione e manipolazione dei dati
* **[Helpers](#helper-helper)** - Logica condizionale e funzioni di utilità
* **[Operatori](#operators-helper)** - Operatori logici e di confronto

**Per utilizzare una funzione helper:**

1. Seleziona una categoria per visualizzarne le sottocategorie e le funzioni disponibili
1. Fai clic sull&#39;icona `>` per espandere le sottocategorie
1. Fai clic sull&#39;icona `+` accanto a una funzione per aggiungerla al codice di personalizzazione
1. Fare clic sull&#39;icona `...` per visualizzare la descrizione della funzione o aggiungerla ai preferiti. [Ulteriori informazioni](../personalize.md#fav)

>[!NOTE]
>
>Le funzioni e le funzionalità disponibili nell&#39;editor di personalizzazione sono diverse da quelle disponibili nell&#39;editor di espressioni avanzate di [Percorso](../../building-journeys/expression/expressionadvanced.md). La funzione `now()` è ad esempio disponibile solo nelle espressioni di percorso. [Ulteriori informazioni](../../email/code-content.md#date-time-limitations)

## Funzioni{#functions-helper}

### Funzioni di aggregazione e array

<table>
    <tr>
        <td><a href="aggregation.md#average">Medio</a></td><td>Questa funzione restituisce la media aritmetica di tutti i valori selezionati all’interno dell’array.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count">Count</a></td><td>Questa funzione restituisce il numero di elementi all’interno dell’array specificato</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count-only-null">Count Only Null</a></td><td>Questa funzione conta il numero di valori Null nell’elenco.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count-with-null">Conteggio con valori Null</a></td><td>Questa funzione conta tutti gli elementi dell’elenco, compresi i valori nulli</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct">Distinct</a></td><td>Questa funzione ottiene valori da un array o da un elenco con valori duplicati rimossi</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct-count-with-null">Conteggio valori univoci con valori Null</a></td><td>Questa funzione conta il numero di valori diversi, inclusi i valori Null.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#head">Primo elemento</a></td><td>Questa funzione restituisce il primo elemento di un array o di un elenco.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#first-n">Primo n nell’array</a></td><td>Questa funzione restituisce i primi elementi "N" di un array, se ordinati in ordine crescente in base alla data espressione numerica</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#in">In entrata</a></td><td>Questa funzione viene utilizzata per determinare se un elemento è membro di un array o di un elenco</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#includes">Include</a></td><td>Questa funzione determina se un array o un elenco contiene un dato elemento</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#intersects">Intersects</a></td><td>Questa funzione determina se due array o elenchi hanno almeno un membro comune</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#last-n">Ultimo n nell’array</a></td><td>Questa funzione restituisce gli ultimi elementi "N" di un array, se ordinati in ordine crescente in base alla data espressione numerica</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#max">Massimo</a></td><td>Questa funzione restituisce il più grande di tutti i valori selezionati all’interno di un array.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#min">Minimo</a></td><td>Questa funzione restituisce il più piccolo di tutti i valori selezionati all’interno dell’array.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#notin">Non in</a></td><td>Questa funzione determina se un elemento non è un membro di un array o di un elenco</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#subset">Sottoinsieme di</a></td><td>Questa funzione determina se un array specifico (array A) è un sottoinsieme di un altro array (array B), ovvero se tutti gli elementi nell’array A sono elementi dell’array B</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#sum">Sum</a></td><td>Questa funzione restituisce la somma di tutti i valori selezionati all’interno dell’array.</td>
    </tr>
    <tr>
    <td><a href="arrays-list.md#superset">Soprainsieme di</a></td><td>Questa funzione determina se un array specifico (array A) è un superset di un altro array (array B), ovvero se l’array A contiene tutti gli elementi dell’array B</td>
    </tr>
</table>

### Funzioni data/ora{#date-functions}

<table>
    <tr>
        <td><a href="dates.md#add-days">Aggiungi giorni</a></td><td>Questa funzione regola una data specificata di un numero specificato di giorni, utilizzando valori positivi per incrementare e valori negativi per diminuire.</td>
    </tr>
    <tr>
        <td><a href="dates.md#add-hours">Aggiungi ore</a></td><td>Questa funzione regola una data specificata di un numero specificato di ore, utilizzando valori positivi per incrementare e valori negativi per diminuire.</td>
    </tr>
    <tr>
        <td><a href="dates.md#add-minutes">Aggiungi minuti</a></td><td>Questa funzione regola una data specificata di un numero specificato di minuti, utilizzando valori positivi per incrementare e valori negativi per diminuire.</td>
    </tr>
    <tr>
        <td><a href="dates.md#add-months">Aggiungi mesi</a></td><td>Questa funzione regola una data specificata di un numero specificato di mesi, utilizzando valori positivi per incrementare e valori negativi per diminuire.</td>
    </tr>
    <tr>
        <td><a href="dates.md#add-seconds">Aggiungi secondi</a></td><td>Questa funzione regola una data specificata di un numero specificato di secondi, utilizzando valori positivi per incrementare e valori negativi per diminuire.</td>
    </tr>
    <tr>
        <td><a href="dates.md#add-years">Aggiungi anni</a></td><td>Questa funzione adegua una data specificata di un numero specificato di anni, utilizzando valori positivi per incrementare e valori negativi per diminuire.</td>
    </tr>
    <tr>
        <td><a href="dates.md#age">Età</a></td><td>Questa funzione recupera l’età da una data specificata.</td>
    </tr>
    <tr>
        <td><a href="dates.md#age-days">Età in giorni</a></td><td>Questa funzione calcola l’età di una data specificata in giorni, ovvero il numero di giorni trascorsi tra la data specificata e la data corrente, negativo per le date future e positivo per le date passate.</td>
    </tr>
    <tr>
        <td><a href="dates.md#age-months">Età in mesi</a></td><td>Questa funzione calcola l’età di una data specificata in mesi, ovvero il numero di mesi trascorsi tra la data specificata e la data corrente, negativo per le date future e positivo per le date passate.</td>
    </tr>
    <tr>
        <td><a href="dates.md#compare-dates">Confronta date</a></td><td>Questa funzione confronta la prima data di input con l’altra. Restituisce 0 se data1 è uguale a data2, -1 se data1 precede data2 e 1 se data1 segue data2.</td>
    </tr>
    <tr>
        <td><a href="dates.md#convert-zoned-date-time">Converti DataOraZona</a></td><td>Questa funzione converte una data/ora in un determinato fuso orario.</td>
    </tr>
    <tr>
        <td><a href="dates.md#current">Ora corrente in millisecondi</a></td><td>Questa funzione recupera il tempo corrente in millisecondi epoca.</td>
    </tr>
    <tr>
        <td><a href="dates.md#date-diff">Differenza data</a></td><td>Questa funzione recupera la differenza tra due date in numero di giorni.</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-month">Giorno del mese</a></td><td>Questa funzione restituisce il numero che rappresenta il giorno del mese.</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-week">Giorno della settimana</a></td><td>Questa funzione recupera il giorno della settimana.</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-year">Giorno dell’anno</a></td><td>Questa funzione recupera il giorno dell’anno.</td>
    </tr>
    <tr>
        <td><a href="dates.md#diff-seconds">Differenza In Secondi</a></td><td>Questa funzione restituisce la differenza tra due date in termini di secondi.</td>
    </tr>
    <tr>
        <td><a href="dates.md#extract-hours">Estrai ore</a></td><td>Questa funzione estrae il componente Ora da una data marca temporale.</td>
    </tr>
    <tr>
        <td><a href="dates.md#extract-minutes">Estrai minuti</a></td><td>Questa funzione estrae il componente minuto da una data marca temporale.</td>
    </tr>
    <tr>
        <td><a href="dates.md#extract-months">Estrai mesi</a></td><td>Questa funzione estrae il componente mese da una data marca temporale.</td>
    </tr>
    <tr>
        <td><a href="dates.md#extract-seconds">Estrai secondi</a></td><td>Questa funzione estrae il secondo componente da una data marca temporale.</td>
    </tr>
    <tr>
        <td><a href="dates.md#format-date">Formato data</a></td><td>Questa funzione formatta un valore di data e ora.</td>
    </tr>
    <tr>
        <td><a href="dates.md#format-date-locale">Formattare la data con il supporto delle impostazioni internazionali</a></td><td>Questa funzione formatta un valore di data e ora nella corrispondente rappresentazione sensibile alla lingua, ovvero nelle impostazioni internazionali desiderate.</td>
    </tr>
    <tr>
        <td><a href="dates.md#get-current-zoned-date-time">Ottieni CurrentZonedDateTime</a></td><td>Questa funzione restituisce la data e l’ora correnti con le informazioni sul fuso orario.</td>
    </tr>
    <tr>
        <td><a href="dates.md#hours-difference">Differenza ore</a></td><td>Questa funzione restituisce la differenza tra due date in termini di ore.</td>
    </tr>
    <tr>
        <td><a href="dates.md#diff-minutes">Differenza minuti</a></td><td>Questa funzione restituisce la differenza tra due date in termini di minuti.</td>
    </tr>
    <tr>
        <td><a href="dates.md#months-difference">Differenza mesi</a></td><td>Questa funzione restituisce la differenza tra due date in termini di mesi.</td>
    </tr>
    <tr>
        <td><a href="dates.md#set-days">Imposta giorni</a></td><td>Questa funzione imposta il giorno del mese per la data/ora specificata.</td>
    </tr>
    <tr>
        <td><a href="dates.md#set-hours">Imposta ore</a></td><td>Questa funzione imposta l’ora della data/ora.</td>
    </tr>
    <tr>
        <td><a href="dates.md#to-date-time">A Data/Ora</a></td><td>Questa funzione converte la stringa in data. In caso di input non valido, restituisce la data epoca come output.</td>
    </tr>
    <tr>
        <td><a href="dates.md#to-utc">A UTC</a></td><td>Questa funzione converte un datetime in UTC.</td>
    </tr>
    <tr>
        <td><a href="dates.md#truncate-day">Tronca all'inizio del giorno</a></td><td>Questa funzione modifica una data/ora specificata impostandola sull’inizio del giorno con l’ora impostata su 00:00.</td>
    </tr>
    <tr>
        <td><a href="dates.md#truncate-quarter">truncateToStartOfQuarter</a></td><td>Questa funzione tronca una data/ora al primo giorno del trimestre (ad esempio 1 gennaio, 1 aprile, 1 luglio, 1 ottobre) alle 00:00.
</td>
    </tr>
    <tr>
        <td><a href="dates.md#truncate-week">truncateToStartOfWeek</a></td><td>Questa funzione modifica una data/ora impostandola sull’inizio della settimana (lunedì alle 00:00).</td>
    </tr>
    <tr>
        <td><a href="dates.md#truncate-year">truncateToStartOfYear</a></td><td>Questa funzione modifica una data/ora specificata troncandola al primo giorno dell’anno (1° gennaio) alle 00:00.</td>
    </tr>
    <tr>
        <td><a href="dates.md#week-of-year">Settimana dell’anno</a></td><td>Questa funzione restituisce la settimana dell’anno.</td>
    </tr>
    <tr>
        <td><a href="dates.md#diff-years">Differenza anni</a></td><td>Questa funzione restituisce la differenza tra due date in termini di anni.</td>
    </tr>
</table>

### Funzioni mappa {#map-functions}

<table>
    <tr>
        <td><a href="maps.md#get">Ottenere</a></td><td>Questa funzione viene utilizzata per recuperare il valore di una mappa per una determinata chiave</td>
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
        <td><a href="math.md#round-down">Arrotonda per difetto</a></td><td>Questa funzione arrotonda un numero per difetto</td>
    </tr>
    <tr>
        <td><a href="math.md#round-up">Arrotonda per eccesso</a></td><td>Questa funzione arrotonda un numero per eccesso</td>
    </tr>
    <tr>
    <td><a href="math.md#to-hex-string">Alla stringa esadecimale</a></td><td>Converte qualsiasi numero nella relativa stringa esadecimale.</td>
    </tr>
    <tr>
    <td><a href="math.md#to-int">ToInt</a></td><td>Converte uno qualsiasi di questi tipi (number, double, int, long, float, short, byte, boolean, string) in un numero intero.</td>
    </tr>
    <tr>
        <td><a href="math.md#to-percentage">A percentuale</a></td><td>Questa funzione converte un numero in percentuale.</td>
    </tr>
    <tr>
        <td><a href="math.md#to-precision">Per la precisione</a></td><td>Questa funzione converte un numero con la precisione richiesta.</td>
    </tr>
    <tr>
        <td><a href="math.md#to-string">A stringa</a></td><td>Questa funzione converte qualsiasi numero nella sua rappresentazione di stringa. </td>
    </tr>
</table>

### Funzioni oggetto {#object-functions}

<table>
    <tr>
        <td><a href="objects.md#isNotNull">Non è nullo</a></td><td>Questa funzione viene utilizzata per determinare se esiste un riferimento a un oggetto</td>
    </tr>
    <tr>
        <td><a href="objects.md#isNull">È nullo</a></td><td>Questa funzione viene utilizzata per determinare se un riferimento a un oggetto non esiste</td>
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
        <td><a href="string.md#concat">Concat</a></td><td>Questa funzione viene utilizzata per combinare due stringhe in una</td>
    </tr>
    <tr>
        <td><a href="string.md#contains">Contiene</a></td><td>Questa funzione viene utilizzata per determinare se una stringa contiene una sottostringa specificata</td>
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
        <td><a href="string.md#encode64">Codifica 64</a></td><td>Questa funzione viene utilizzata per codificare una stringa</td>
    </tr>
    <tr>
        <td><a href="string.md#endsWith">Termina con</a></td><td>Questa funzione viene utilizzata per determinare se una stringa termina con una sottostringa specificata</td>
    </tr>
        </tr>
    <tr>
        <td><a href="string.md#equals">È uguale a</a></td><td>Questa funzione viene utilizzata per determinare se una stringa non inizia con una sottostringa specificata, con distinzione tra maiuscole e minuscole</td>
    </tr>
    <tr>
        <td><a href="string.md#equalsIgnoreCase">Ignora maiuscole/minuscole uguale a</a></td><td>Questa funzione viene utilizzata per determinare se una stringa non inizia con una sottostringa specificata, senza distinzione tra maiuscole e minuscole</td>
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
        <td><a href="string.md#is-not-empty">Non è vuoto</a></td><td>Questa funzione restituisce true se la stringa nel parametro non è vuota.</td>
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
        <td><a href="string.md#like">Simile a</a></td><td>Questa funzione viene utilizzata per determinare se una stringa corrisponde a un pattern specificato</td>
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
        <td><a href="string.md#not-equal-with-ignore-case">Non uguale con ignora maiuscole/minuscole</a></td><td>Questa funzione confronta due stringhe ignorando le maiuscole/minuscole.</td>
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
        <td><a href="string.md#sha256">SHA256</a></td><td>Questa funzione calcola e restituisce l’hash sha256 di una stringa.</td>
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
        <td><a href="string.md#sub-string">Sottostringa</a></td><td>Questa funzione restituisce la sottostringa dell’espressione stringa tra l’indice iniziale e l’indice finale.</td>
    </tr>
    <tr>
        <td><a href="string.md#titleCase">Tutte iniziali maiuscole</a></td><td>Questa funzione viene utilizzata per rendere maiuscole le prime lettere di ogni parola di una stringa</td>
    </tr>
    <tr>
        <td><a href="string.md#to-bool">To Bool</a></td><td>Questa funzione converte un valore di argomento in un valore booleano, a seconda del tipo.</td>
    </tr>
    <tr>
        <td><a href="string.md#to-date-time">A Data/Ora</a></td><td>Questa funzione viene utilizzata per convertire una stringa in data. In caso di input non valido, restituisce la data epoca come output.</td>
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
        <td><a href="string.md#url-decode">Decodifica URL</a></td><td>Questa funzione viene utilizzata per decodificare una stringa con codifica URL.</td>
    </tr>
    <tr>
        <td><a href="string.md#url-encode">Codifica URL</a></td><td>Questa funzione viene utilizzata per la codifica URL di una stringa.</td>
    </tr>
</table>


## Helper{#helper-helper}

Gli helper sono dettagliati in [questa pagina](helpers.md).


<table>
    <tr>
        <td><a href="helpers.md#default">Valore di fallback predefinito</a></td><td>Questa funzione viene utilizzata per eseguire il rendering di una variabile con il valore predefinito</td>
    </tr>
    <tr>
        <td><a href="helpers.md#each">Ogni</a></td><td>Questa funzione viene utilizzata per eseguire iterazioni su un array</td>
    </tr>
    <tr>
        <td><a href="helpers.md#execution-metadata">Metadati di esecuzione</a></td><td>Questo helper acquisisce metadati personalizzati chiave-valore durante il rendering dei messaggi in modo che possano essere memorizzati nell’oggetto metadati di esecuzione runtime</td>
    </tr>
    <tr>
        <td><a href="helpers.md#if-function">Se</a></td><td>Questa funzione viene utilizzata per definire un blocco condizionale. Se la valutazione dell’espressione restituisce true, viene eseguito il rendering del blocco.</td>
    </tr>
    <tr>
        <td><a href="helpers.md#let">Let</a></td><td>Questa funzione consente di memorizzare un’espressione come variabile da utilizzare successivamente in una query</td>
    </tr>
   <tr>
        <td><a href="helpers.md#unless">A meno che</a></td><td>Questa funzione viene utilizzata per definire un blocco condizionale. Se la valutazione dell’espressione restituisce false, viene eseguito il rendering del blocco</td>
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
        <td><a href="arithmetic-functions.md#add">Addizione</a></td><td>Questo operatore viene utilizzato per trovare la somma di due espressioni di argomento</td>
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

Le funzioni di confronto vengono utilizzate per confrontare espressioni e valori diversi, restituendo di conseguenza true o false.

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
        <td><a href="operators.md#notequal">Non è uguale a</a></td><td>Questo operatore controlla se l’espressione data non è uguale al valore dato</td>
    </tr>
</table>

## Video dimostrativo{#video}

Scopri come trasformare i valori di personalizzazione utilizzando le funzioni di assistenza alla personalizzazione e studia diversi casi d’uso per le funzioni di supporto.

>[!VIDEO](https://video.tv.adobe.com/v/3416645?captions=ita&quality=12)
