---
solution: Journey Optimizer
product: journey optimizer
title: Modificare le espressioni
description: Scopri come modificare le espressioni.
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: bf0a905f-00af-4ed7-9e4f-bf8cb0af9ea9
source-git-commit: 3f92dc721648f822687b8efc302c40989b72b145
workflow-type: tm+mt
source-wordcount: '2150'
ht-degree: 97%

---


# Modificare le espressioni {#edit-expressions}

+++ Sommario

| Ti diamo il benvenuto nelle campagne orchestrate | Avviare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](gs-orchestrated-campaigns.md)<br/><br/>Creazione e gestione di schemi e set di dati relazionali:</br> <ul><li>[Introduzione a schemi e set di dati](gs-schemas.md)</li><li>[Schema manuale](manual-schema.md)</li><li>[Schema di caricamento file](file-upload-schema.md)</li><li>[Acquisire dati](ingest-data.md)</li></ul>[Accedere e gestire campagne orchestrate](access-manage-orchestrated-campaigns.md)<br/><br/>[Passaggi chiave per creare una campagna orchestrata](gs-campaign-creation.md) | [Creare e pianificare la campagna](create-orchestrated-campaign.md)<br/><br/>[Orchestrare le attività](orchestrate-activities.md)<br/><br/>[Avviare e monitorare la campagna](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | [Utilizzare il generatore di regole](orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](build-query.md)<br/><br/><b>[Modificare le espressioni](edit-expressions.md)</b><br/><br/>[Retargeting](retarget.md) | [Introduzione alle attività](activities/about-activities.md)<br/><br/>Attività:<br/>[AND-join](activities/and-join.md) - [Crea pubblico](activities/build-audience.md) - [Modifica dimensione](activities/change-dimension.md) - [Attività canale](activities/channels.md) - [Combina](activities/combine.md) - [Deduplica](activities/deduplication.md) - [Arricchimento](activities/enrichment.md) - [Fork](activities/fork.md) - [Riconciliazione](activities/reconciliation.md) - [Salva pubblico](activities/save-audience.md) - [Dividi](activities/split.md) - [Attendi](activities/wait.md) |

{style="table-layout:fixed"}

+++
<br/>

>[!BEGINSHADEBOX]

Il contenuto di questa pagina non è definitivo e potrebbe essere soggetto a modifiche.

>[!ENDSHADEBOX]

>[!NOTE]
>
>La sezione seguente fornisce informazioni su come utilizzare l’editor di espressioni per creare regole. Tieni presente che la sintassi utilizzata per creare le regole è diversa da quella utilizzata per aggiungere la personalizzazione.

## Utilizzare l’editor di espressioni {#edit}

La modifica di un’espressione comporta l’immissione manuale di condizioni per formare una regola. Questa modalità ti permette di utilizzare funzioni avanzate, che ti consentono di gestire i valori utilizzati per eseguire query specifiche, come la gestione di date, stringhe, campi numerici e ordinamento.

L’editor di espressioni è disponibile dal pulsante **[!UICONTROL Modifica espressione]** del generatore di regole, disponibile per i campi **[!UICONTROL Attributo]** e **[!UICONTROL Valore]** durante la configurazione di una condizione personalizzata.

| Accedere dal campo **Attributo** | Accedere dal campo **Valore** |
| --- | --- |
| ![Editor di espressioni per il campo Attributo](assets/rule-builder-expression-access-attribute.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} | ![Editor di espressioni per il campo Valore](assets/rule-builder-expression-access-value.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |

L’editor di espressioni mostra:

* Un **campo di input (1)** in cui è definita l’espressione.
* Un elenco dei **campi (2)** disponibili che possono essere utilizzati nell’espressione e che corrispondono alla dimensione targeting della query.
* **Funzioni helper (3)**, ordinate per categoria.

Modifica l’espressione immettendo un’espressione direttamente nel campo di input. Per aggiungere un campo o una funzione helper, posiziona il cursore nell’espressione nel punto in cui desideri aggiungerla e fai clic sul pulsante +.

![Interfaccia dell’editor di espressioni](assets/rule-builder-expression-editor.png){zoomable="yes"}

## Funzioni Helper

Lo strumento di modifica delle query ti consente di utilizzare funzioni avanzate per eseguire filtri complessi a seconda dei risultati desiderati e dei tipi di dati gestiti. Sono disponibili le seguenti funzioni:

### Aggregato

Le funzioni di aggregazione eseguono calcoli su un set di valori.

<table>
<tbody>
<tr>
<td><strong>Nome</strong></td>
<td><strong>Descrizione</strong></td>
<td><strong>Sintassi</strong></td>
</tr>
<tr>
<td><strong>Avg</strong></td>
<td>Restituisce la media di una colonna di tipo numerico</td>
<td>Avg(&lt;valore&gt;)</td>
</tr>
<tr>
<td><strong>Count</strong></td>
<td>Conta i valori non nulli in una colonna</td>
<td>Count(&lt;valore&gt;)</td>
</tr>
<tr>
<td><strong>CountAll</strong></td>
<td>Conta i valori restituiti (tutti i campi)</td>
<td>CountAll()</td>
</tr>
<tr>
<td><strong>Countdistinct</strong></td>
<td>Conta i valori distinti non nulli in una colonna</td>
<td>Countdistinct(&lt;valore&gt;)</td>
</tr>
<tr>
<td><strong>Max</strong></td>
<td>Restituisce il valore massimo in una colonna di tipo numerico, stringa o data</td>
<td>Max(&lt;valore&gt;)</td>
</tr>
<tr>
<td><strong>Min</strong></td>
<td>Restituisce il valore minimo in una colonna di tipo numerico, stringa o data</td>
<td>Min(&lt;valore&gt;)</td>
</tr>
<tr>
<td><strong>StdDev</strong></td>
<td>Restituisce la deviazione standard in una colonna numerica, stringa o data</td>
<td>StdDev(&lt;valore&gt;)</td>
</tr>
<tr>
<td><strong>StringAgg</strong></td>
<td>Restituisce la concatenazione dei valori di una colonna di tipo stringa, separati dal carattere nel secondo argomento</td>
<td>StringAgg(&lt;Valore&gt;, &lt;Stringa&gt;)</td>
</tr>
<tr>
<td><strong>Sum</strong></td>
<td>Restituisce la somma dei valori in una colonna di tipo numerico, stringa o data</td>
<td>Sum(&lt;valore&gt;)</td>
</tr>
</tbody>
</table>

### Date

Le funzioni data gestiscono i valori di data o ora.

<table>
<tbody>
<tr>
<td><strong>Nome</strong></td>
<td><strong>Descrizione</strong></td>
<td><strong>Sintassi</strong></td>
</tr>
<tr>
<td><strong>AddDays</strong></td>
<td>Aggiunge un numero di giorni a una data</td>
<td>AddDays(&lt;data&gt;, &lt;numero&gt;)</td>
</tr>
<tr>
<td><strong>AddHours</strong></td>
<td>Aggiunge un numero di ore a una data</td>
<td>AddHours(&lt;data&gt;, &lt;numero&gt;)</td>
</tr>
<tr>
<td><strong>AddMinutes</strong></td>
<td>Aggiunge un numero di minuti a una data</td>
<td>AddMinutes(&lt;data&gt;, &lt;numero&gt;)</td>
</tr>
<tr>
<td><strong>AddMonths</strong></td>
<td>Aggiunge un numero di mesi a una data</td>
<td>AddMonths(&lt;data&gt;, &lt;numero&gt;)</td>
</tr>
<tr>
<td><strong>AddSeconds</strong></td>
<td>Aggiunge un numero di secondi a una data</td>
<td>AddSeconds(&lt;data&gt;, &lt;numero&gt;)</td>
</tr>
<tr>
<td><strong>AddYears</strong></td>
<td>Aggiunge un numero di anni a una data</td>
<td>AddYears(&lt;data&gt;, &lt;numero&gt;)</td>
</tr>
<tr>
<td><strong>ConvertNTZ</strong></td>
<td>Converte la marca temporale NTZ (marca temporale senza fuso orario) in TZ (marca temporale con fuso orario) applicando la sessione definita TZ</td>
<td>ConvertNTZ (&lt;data+ora&gt;)</td>
</tr>
<tr>
<td><strong>DateCmp</strong></td>
<td>Confronta due date</td>
<td>DateCmp(&lt;data, data&gt;)</td>
</tr>
<tr>
<td><strong>DateOnly</strong></td>
<td>Restituisce solo la data (con l’ora su 00:00)</td>
<td>DateOnly(&lt;data&gt;)</td>
</tr>
<tr>
<td><strong>Day</strong></td>
<td>Restituisce il numero che rappresenta il giorno della data</td>
<td>Day(&lt;data&gt;)</td>
</tr>
<tr>
<td><strong>DayOfYear</strong></td>
<td>Restituisce il numero del giorno dell’anno della data</td>
<td>DayOfYear(&lt;data&gt;)</td>
</tr>
<tr>
<td><strong>DaysAgo</strong></td>
<td>Restituisce la data corrispondente alla data corrente meno n giorni</td>
<td>DaysAgo(&lt;numero&gt;)</td>
</tr>
<tr>
<td><strong>DaysAgoInt</strong></td>
<td>Restituisce la data corrispondente (numero intero aaaammgg) alla data corrente meno n giorni</td>
<td>DaysAgoInt(&lt;numero&gt;)</td>
</tr>
<tr>
<td><strong>DaysDiff</strong></td>
<td>Restituisce il numero di giorni tra due date</td>
<td>DaysDiff(&lt;data di fine&gt;, &lt;data di inizio&gt;)</td>
</tr>
<tr>
<td><strong>DaysOld</strong></td>
<td>Restituisce l’età in giorni di una data</td>
<td>DaysOld(&lt;data&gt;)</td>
</tr>
<tr>
<td><strong>GetDate</strong></td>
<td>Restituisce la data di sistema corrente del server</td>
<td>GetDate()</td>
</tr>
<tr>
<td><strong>Hour</strong></td>
<td>Restituisce l’ora della data</td>
<td>Hour(&lt;data&gt;)</td>
</tr>
<tr>
<td><strong>HoursDiff</strong></td>
<td>Restituisce il numero di ore tra due date</td>
<td>HoursDiff(&lt;data di fine&gt;, &lt;data di inizio&gt;)</td>
</tr>
<tr>
<td><strong>Minuti</strong></td>
<td>Restituisce i minuti della data</td>
<td>Minute(&lt;data&gt;)</td>
</tr>
<tr>
<td><strong>MinutesDiff</strong></td>
<td>Restituisce il numero di minuti tra due date</td>
<td>MinutesDiff(&lt;data di fine&gt;, &lt;data di inizio&gt;)</td>
</tr>
<tr>
<td><strong>Month</strong></td>
<td>Restituisce il numero che rappresenta il mese della data</td>
<td>Month(&lt;data&gt;)</td>
</tr>
<tr>
<td><strong>MonthsAgo</strong></td>
<td>Restituisce la data corrispondente alla data corrente meno n mesi</td>
<td>MonthsAgo(&lt;numero&gt;)</td>
</tr>
<tr>
<td><strong>MonthsDiff</strong></td>
<td>Restituisce il numero di mesi tra due date</td>
<td>MonthsDiff(&lt;data di fine&gt;, &lt;data di inizio&gt;)</td>
</tr>
<tr>
<td><strong>MonthsOld</strong></td>
<td>Restituisce l’età in mesi di una data</td>
<td>MonthsOld(&lt;data&gt;)</td>
</tr>
<tr>
<td><strong>Oldest</strong></td>
<td>Restituisce la data meno recente in un intervallo</td>
<td>Oldest(&lt;data, data&gt;)</td>
</tr>
<tr>
<td><strong>Second</strong></td>
<td>Restituisce i secondi della data</td>
<td>Second(&lt;data&gt;)</td>
</tr>
<tr>
<td><strong>SecondsDiff</strong></td>
<td>Restituisce il numero di secondi tra due date</td>
<td>SecondsDiff(&lt;data di fine&gt;, &lt;data di inizio&gt;)</td>
</tr>
<tr>
<td><strong>SubDays</strong></td>
<td>Sottrae un numero di giorni da una data</td>
<td>SubDays(&lt;data&gt;, &lt;numero&gt;)</td>
</tr>
<tr>
<td><strong>SubHours</strong></td>
<td>Sottrae un numero di ore da una data</td>
<td>SubHours(&lt;data&gt;, &lt;numero&gt;)</td>
</tr>
<tr>
<td><strong>SubMinutes</strong></td>
<td>Sottrae un numero di minuti da una data</td>
<td>SubMinutes(&lt;data&gt;, &lt;numero&gt;)</td>
</tr>
<tr>
<td><strong>SubMonths</strong></td>
<td>Sottrae un numero di mesi da una data</td>
<td>SubMonths(&lt;data&gt;, &lt;numero&gt;)</td>
</tr>
<tr>
<td><strong>SubSeconds</strong></td>
<td>Sottrae un numero di secondi da una data</td>
<td>SubSeconds(&lt;data&gt;, &lt;numero&gt;)</td>
</tr>
<tr>
<td><strong>SubYears</strong></td>
<td>Sottrae un numero di anni da una data</td>
<td>SubYears(&lt;data&gt;, &lt;numero&gt;)</td>
</tr>
<tr>
<td><strong>ToDate</strong></td>
<td>Converte una data + ora in una data</td>
<td>ToDate(&lt;data + ora&gt;)</td>
</tr>
<tr>
<td><strong>ToDateTime</strong></td>
<td>Converte una stringa in una data + ora</td>
<td>ToDateTime(&lt;stringa&gt;)</td>
</tr>
<tr>
<td><strong>ToTimestamp</strong></td>
<td>Converte una stringa in una marca temporale</td>
<td>ToTimestamp(&lt;stringa&gt;)</td>
</tr>
<tr>
<td><strong>ToTimeZone</strong></td>
<td>Converte data + ora in fuso orario</td>
<td>ToTimeZone(&lt;data&gt;, &lt;time zone&gt;)</td>
</tr>
<tr>
<td><strong>TruncDate</strong></td>
<td>Arrotonda una data + ora al secondo più vicino</td>
<td>TruncDate(@lastModified, &lt;numero di secondi&gt;)</td>
</tr>
<tr>
<td><strong>TruncDateTZ</strong></td>
<td>Arrotonda una data + ora a una determinata precisione, espressa in secondi</td>
<td>TruncDateTZ(&lt;data&gt;, &lt;numero di secondi&gt;, &lt;time zone&gt;)</td>
</tr>
<tr>
<td><strong>TruncQuarter</strong></td>
<td>Arrotonda una data al trimestre</td>
<td>TruncQuarter(&lt;data&gt;)</td>
</tr>
<tr>
<td><strong>TruncTime</strong></td>
<td>Arrotonda la parte dell’ora al secondo più vicino</td>
<td>TruncTime(&lt;data&gt;, &lt;numero di secondi&gt;)</td>
</tr>
<tr>
<td><strong>TruncWeek</strong></td>
<td>Arrotonda una data alla settimana</td>
<td>TruncWeek(&lt;data&gt;)</td>
</tr>
<tr>
<td><strong>TruncYear</strong></td>
<td>Arrotonda una data + ora al 1° gennaio dell’anno</td>
<td>TruncYear(&lt;data&gt;)</td>
</tr>
<tr>
<td><strong>WeekDay</strong></td>
<td>Restituisce un numero che rappresenta il giorno della settimana della data (0=lunedì, 6=domenica)</td>
<td>WeekDay(&lt;data&gt;)</td>
</tr>
<tr>
<td><strong>Year</strong></td>
<td>Restituisce il numero che rappresenta l’anno della data</td>
<td>Year(&lt;data&gt;)</td>
</tr>
<tr>
<td><strong>YearAndMonth</strong></td>
<td>Restituisce il numero che rappresenta l’anno e il mese della data</td>
<td>YearAndMonth(&lt;data&gt;)</td>
</tr>
<tr>
<td><strong>YearsAgo</strong></td>
<td>Restituisce il numero di anni tra una data specificata e la data corrente</td>
<td>YearsAgo(&lt;data&gt;)</td>
</tr>
<tr>
<td><strong>YearsDiff</strong></td>
<td>Restituisce il numero di anni tra due date</td>
<td>YearsDiff(&lt;data di fine&gt;, &lt;data di inizio&gt;)</td>
</tr>
<tr>
<td><strong>YearsOld</strong></td>
<td>Restituisce l’età in anni di una data</td>
<td>YearsOld(&lt;data&gt;)</td>
</tr>
</tbody>
</table>

>[!NOTE]
>
>Tieni presente che la funzione **DateOnly** tiene conto del fuso orario del server, non di quello dell’operatore.


### Geomarketing

Le funzioni di geomarketing vengono utilizzate per manipolare i valori geografici.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Nome</strong><br /> </td> 
   <td> <strong>Descrizione</strong><br /> </td> 
   <td> <strong>Sintassi</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Distance</strong><br /> </td> 
   <td> Restituisce la distanza tra due punti definiti da longitudine e latitudine espressa in gradi.<br /> </td> 
   <td> Distance(&lt;Longitudine A&gt;, &lt;Latitudine A&gt;, &lt;Longitudine B&gt;, &lt;Latitudine B&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### Numerico

Le funzioni numeriche vengono utilizzate per convertire il testo in numeri.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Nome</strong><br /> </td> 
   <td> <strong>Descrizione</strong><br /> </td> 
   <td> <strong>Sintassi</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Abs</strong><br /> </td> 
   <td> Restituisce il valore assoluto di un numero<br /> </td> 
   <td> Abs(&lt;numero&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Ceil</strong><br /> </td> 
   <td> Restituisce il numero intero più piccolo maggiore o uguale a un numero<br /> </td> 
   <td> Ceil(&lt;numero&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Floor</strong><br /> </td> 
   <td> Restituisce il numero intero maggiore o uguale a un numero<br /> </td> 
   <td> Floor(&lt;numero&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Greatest</strong><br /> </td> 
   <td> Restituisce il numero maggiore tra due numeri<br /> </td> 
   <td> Greatest(&lt;numero 1&gt;, &lt;numero 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Least</strong><br /> </td> 
   <td> Restituisce il minore tra due numeri<br /> </td> 
   <td> Least(&lt;numero 1&gt;, &lt;numero 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Mod</strong><br /> </td> 
   <td> Restituisce il resto della divisione del numero intero da n1 per n2<br /> </td> 
   <td> Mod(&lt;numero 1&gt;, &lt;numero 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Percent</strong><br /> </td> 
   <td> Restituisce il rapporto tra due numeri espresso come percentuale<br /> </td> 
   <td> Percent(&lt;numero 1&gt;, &lt;numero 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Random</strong><br /> </td> 
   <td> Restituisce il valore casuale<br /> </td> 
   <td> Random()<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Round</strong><br /> </td> 
   <td> Arrotonda un numero a n decimali<br /> </td> 
   <td> Round(&lt;numero&gt;, &lt;numero di decimali&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Sign</strong><br /> </td> 
   <td> Restituisce il segno del numero<br /> </td> 
   <td> Sign(&lt;numero&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToDouble</strong><br /> </td> 
   <td> Converte un numero intero in un numero in virgola mobile<br /> </td> 
   <td> ToDouble(&lt;numero&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToInt64</strong><br /> </td> 
   <td> Converte un numero in virgola mobile in un numero intero a 64 bit<br /> </td> 
   <td> ToInt64(&lt;numero&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToInteger</strong><br /> </td> 
   <td> Converte un numero in virgola mobile in un numero intero<br /> </td> 
   <td> ToInteger(&lt;numero&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Trunc</strong><br /> </td> 
   <td> Tronca n1 a n2 decimali<br /> </td> 
   <td> Trunc(&lt;n1&gt;, &lt;n2&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### Altre

Questa tabella contiene le altre funzioni disponibili.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Nome</strong><br /> </td> 
   <td> <strong>Descrizione</strong><br /> </td> 
   <td> <strong>Sintassi</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AESEncrypt</strong><br /> </td> 
   <td> Stringa di crittografia fornita nell’argomento<br /> </td> 
   <td> AESEncrypt(&lt;valore&gt;)<br /> </td> 
  </tr>
  <tr> 
   <td> <strong>Case</strong><br /> </td> 
   <td> Restituisce il valore 1 se la condizione è vera. In caso contrario, restituisce il valore 2.<br /> </td> 
   <td> Case(When(&lt;condizione&gt;, &lt;valore 1&gt;), Else(&lt;valore 2&gt;))<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ClearBit</strong><br /> </td> 
   <td> Elimina il contrassegno nel valore<br /> </td> 
   <td> ClearBit(&lt;identificatore&gt;, &lt;contrassegno&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Coalesce</strong><br /> </td> 
   <td> Restituisce il valore 2 se il valore 1 è zero o nullo, altrimenti restituisce il valore 1<br /> </td> 
   <td> Coalesce(&lt;valore 1&gt;, &lt;valore 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Decode</strong><br /> </td> 
   <td> Restituisce il valore 3 se il valore 1 = al valore 2. In caso contrario, restituisce il valore 4.<br /> </td> 
   <td> Decode(&lt;valore 1&gt;, &lt;valore 2&gt;, &lt;valore 3&gt;, &lt;valore 4&gt;)<br /> </td>  
  </tr>

<tr> 
   <td> <strong>Else</strong><br /> </td> 
   <td> Restituisce il valore 1 (può essere utilizzato solo come parametro della funzione Case)<br /> </td> 
   <td> Else(&lt;valore 1&gt;, &lt;valore 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>GetEmailDomain</strong><br /> </td> 
   <td> Estrae il dominio da un indirizzo e-mail<br /> </td> 
   <td> GetEmailDomain(&lt;valore&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>GetMirrorURL</strong><br /> </td> 
   <td> Recupera l’URL del server della pagina mirror<br /> </td> 
   <td> GetMirrorURL(&lt;valore&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Iif</strong><br /> </td> 
   <td> Restituisce il valore 1 se l’espressione è vera. In caso contrario, restituisce il valore 2<br /> </td> 
   <td> Iif(&lt;condizione&gt;, &lt;valore 1&gt;, &lt;valore 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>IsBitSet</strong><br /> </td> 
   <td> Indica se il contrassegno si trova nel valore<br /> </td> 
   <td> IsBitSet(&lt;identificatore&gt;, &lt;contrassegno&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>IsEmptyString</strong><br /> </td> 
   <td> Restituisce il valore 2 se la stringa è vuota, altrimenti restituisce il valore 3<br /> </td> 
   <td> IsEmptyString(&lt;valore 1&gt;, &lt;valore 2&gt;, &lt;valore 3&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>NewUUID</strong><br /> </td> 
   <td> Restituisce un ID univoco<br /> </td> 
   <td> NewUUID()<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>NoNull</strong><br /> </td> 
   <td> Restituisce la stringa vuota se l’argomento è NULL<br /> </td> 
   <td> NoNull(&lt;valore&gt;)<br /> </td>   
  </tr> 
  <tr> 
   <td> <strong>RowId</strong><br /> </td> 
   <td> Restituisce il numero di riga<br /> </td> 
   <td> RowId<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>SetBit</strong><br /> </td> 
   <td> Forza il contrassegno nel valore<br /> </td> 
   <td> SetBit(&lt;identificatore&gt;, &lt;contrassegno&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToBoolean</strong><br /> </td> 
   <td> Converte un numero in booleano<br /> </td> 
   <td> ToBoolean(&lt;numero&gt;)<br /> </td>   
  </tr> 
  <tr> 
   <td> <strong>When</strong><br /> </td> 
   <td> Restituisce il valore 1 se l’espressione è vera. In caso contrario, restituisce il valore 2 (può essere utilizzato solo come parametro della funzione Case)<br /> </td> 
   <td> When(&lt;condizione&gt;, &lt;valore 1&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### Stringa

Le funzioni di stringa vengono utilizzate per manipolare un insieme di stringhe.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Nome</strong><br /> </td> 
   <td> <strong>Descrizione</strong><br /> </td> 
   <td> <strong>Sintassi</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AllNonNull2</strong><br /> </td> 
   <td> Indica se tutti i parametri non sono nulli e non sono vuoti<br /> </td> 
   <td> AllNonNull2(&lt;stringa&gt;, &lt;stringa&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>AllNonNull3</strong><br /> </td> 
   <td> Indica se tutti i parametri non sono nulli e non sono vuoti<br /> </td> 
   <td> AllNonNull3(&lt;stringa&gt;, &lt;stringa&gt;, &lt;stringa&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Ascii</strong><br /> </td> 
   <td> Restituisce il valore ASCII del primo carattere della stringa<br /> </td> 
   <td> Ascii(&lt;stringa&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Char</strong><br /> </td> 
   <td> Restituisce il carattere corrispondente al codice ASCII “n”<br /> </td> 
   <td> Char(&lt;numero&gt;)<br /></td>  
  </tr> 
  <tr> 
   <td> <strong>Charindex</strong><br /> </td> 
   <td> Restituisce la posizione della stringa 2 nella stringa 1.<br /> </td> 
   <td> Charindex(&lt;stringa&gt;, &lt;stringa&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>dataLength</strong><br /> </td> 
   <td> Restituisce la dimensione in byte della stringa<br /> </td> 
   <td> dataLength(&lt;stringa&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>GetLine</strong><br /> </td> 
   <td> Restituisce l’ennesima riga (da 1 a n) della stringa<br /> </td> 
   <td> GetLine(&lt;stringa&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>IfEquals</strong><br /> </td> 
   <td> Restituisce il terzo parametro se i primi due parametri sono uguali. In caso contrario, restituisce l’ultimo parametro<br /> </td> 
   <td> IfEquals(&lt;stringa&gt;, &lt;stringa&gt;, &lt;stringa&gt;, &lt;stringa&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>IsMemoNull</strong><br /> </td> 
   <td> Indica se il promemoria passato come parametro è nullo<br /> </td> 
   <td> IsMemoNull(&lt;promemoria&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>JuxtWords</strong><br /> </td> 
   <td> Concatena le stringhe passate come parametri. Se necessario, aggiunge spazi tra le stringhe.<br /> </td> 
   <td> JuxtWords(&lt;stringa&gt;, &lt;stringa&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>JuxtWords3</strong><br /> </td> 
   <td> Concatena le stringhe passate come parametri. Se necessario, aggiunge spazi tra le stringhe<br /> </td> 
   <td> JuxtWords3(&lt;stringa&gt;, &lt;stringa&gt;, &lt;stringa&gt;)<br /></td>  
  </tr> 
  <tr> 
   <td> <strong>Left</strong><br /> </td> 
   <td> Restituisce i primi n caratteri della stringa<br /> </td> 
   <td> Left(&lt;stringa&gt;, &lt;numero&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Length</strong><br /> </td> 
   <td> Restituisce la lunghezza della stringa<br /> </td> 
   <td> Length(&lt;stringa&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Line</strong><br /> </td> 
   <td> Estrae la riga n dalla stringa<br /> </td> 
   <td> Line(&lt;stringa&gt;, &lt;numero&gt;)<br /></td> 
  </tr>
  <tr> 
   <td> <strong>Lower</strong><br /> </td> 
   <td> Restituisce la stringa in caratteri minuscoli<br /> </td> 
   <td> Lower(&lt;stringa&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>LPad</strong><br /> </td> 
   <td> Restituisce la stringa completata a sinistra<br /> </td> 
   <td> LPad(&lt;stringa&gt;, &lt;numero&gt;, &lt;carattere&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Ltrim</strong><br /> </td> 
   <td> Rimuove gli spazi a sinistra della stringa<br /> </td> 
   <td> Ltrim(&lt;stringa&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Md5Digest</strong><br /> </td> 
   <td> Restituisce una rappresentazione esadecimale della chiave MD5 di una stringa<br /> </td> 
   <td> Md5Digest(&lt;stringa&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>MemoContains</strong><br /> </td> 
   <td> Specifica se il promemoria contiene la stringa passata come parametro<br /> </td> 
   <td> MemoContains(&lt;promemoria&gt;, &lt;stringa&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>NodeValue</strong><br /> </td> 
   <td> Estrae il valore di un campo XML dal relativo XPath e dai dati del campo<br /> </td> 
   <td> NodeValue (&lt;stringa&gt;, &lt;stringa&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Replace</strong><br /> </td> 
   <td> Sostituisce tutte le occorrenze di un valore di stringa specificato con un altro valore di stringa.<br /> </td> 
   <td> Replace(&lt;Stringa&gt;,&lt;Stringa&gt;,&lt;Stringa&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Right</strong><br /> </td> 
   <td> Restituisce gli ultimi n caratteri della stringa<br /> </td> 
   <td> Right(&lt;stringa&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>RPad</strong><br /> </td> 
   <td> Restituisce la stringa completata a destra<br /> </td> 
   <td> RPad(&lt;stringa&gt;, &lt;numero&gt;, &lt;carattere&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Rtrim</strong><br /> </td> 
   <td> Rimuove gli spazi a destra della stringa<br /> </td> 
   <td> Rtrim(&lt;stringa&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sha256Digest</strong><br /> </td> 
   <td> Rappresentazione esadecimale della chiave SHA256 di una stringa.<br /> </td> 
   <td> Sha256Digest(&lt;Stringa&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sha512Digest</strong><br /> </td> 
   <td> Rappresentazione esadecimale della chiave SHA512 di una stringa.<br /> </td> 
   <td> Sha512Digest(&lt;Stringa&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Smart</strong><br /> </td> 
   <td> Restituisce la stringa con la prima lettera di ciascuna parola in maiuscolo<br /> </td> 
   <td> Smart(&lt;stringa&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Substring</strong><br /> </td> 
   <td> Estrae la stringa secondaria a partire dal carattere n1 della stringa e con una lunghezza n2<br /> </td> 
   <td> Substring(&lt;stringa&gt;, &lt;offset&gt;, &lt;lunghezza&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToString</strong><br /> </td> 
   <td> Converte il numero in una stringa<br /> </td> 
   <td> ToString(&lt;numero&gt;, &lt;numero&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Upper</strong><br /> </td> 
   <td> Restituisce la stringa in caratteri maiuscoli<br /> </td> 
   <td> Upper(&lt;stringa&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>VirtualLink</strong><br /> </td> 
   <td> Restituisce la chiave esterna di un collegamento passato come parametro se gli altri due parametri sono uguali<br /> </td> 
   <td> VirtualLink(&lt;numero&gt;, &lt;numero&gt;, &lt;numero&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>VirtualLinkStr</strong><br /> </td> 
   <td> Restituisce la chiave esterna (testo) di un collegamento passato come parametro se gli altri due parametri sono uguali<br /> </td> 
   <td> VirtualLinkStr(&lt;stringa&gt;, &lt;numero&gt;, &lt;numero&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### Finestra

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Nome</strong><br /> </td> 
   <td> <strong>Descrizione</strong><br /> </td> 
   <td> <strong>Sintassi</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>_Over__</strong><br /> </td> 
   <td> Esegue la chiamata alla funzione SQL immessa come primo parametro, su Partizione o Ordina per i campi immessi come secondo parametro<br /> </td> 
   <td> _Over_ (&lt;Valore&gt;, &lt;Valore&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Desc</strong><br /> </td> 
   <td> Applica un ordinamento decrescente<br /> </td> 
   <td> Desc(&lt;valore 1&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>OrderBy</strong><br /> </td> 
   <td> Ordina il risultato all’interno della partizione<br /> </td> 
   <td> OrderBy(&lt;valore 1&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>PartitionBy</strong><br /> </td> 
   <td> Partiziona il risultato di una query su una tabella<br /> </td> 
   <td> PartitionBy(&lt;valore 1&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>RowNum</strong><br /> </td> 
   <td> Genera un numero di riga basato sulla partizione della tabella e su una sequenza di ordinamento.<br /> </td> 
   <td> RowNum(PartitionBy(&lt;valore 1&gt;), OrderBy(&lt;valore 1&gt;))<br /> </td> 
  </tr> 
 </tbody> 
</table>
