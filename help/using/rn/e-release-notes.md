---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
description: Note preliminari sulla versione di Journey Optimizer
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: d945e22af664876bf5f5403e7e466a1e383e9501
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 19%

---

# Note preliminari sulla versione {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nell’ultima settimana di ogni mese, tutte le modifiche vengono consolidate nelle [note sulla versione](release-notes.md).

Le note preliminari sulla versione riportate di seguito sono soggette a modifiche senza preavviso fino alla data di disponibilità della versione. I collegamenti, le schermate e la documentazione aggiornata vengono pubblicati nelle [note sulla versione](release-notes.md), alla data di rilascio.

## Note preliminari sulla versione di febbraio 2024 {#e-2024}

**Data di rilascio**: 20-21 febbraio 2024

### Nuove funzionalità{#e-features}

Questa versione include le nuove funzionalità elencate di seguito.


<table>
<thead>
<tr>
<th><strong>Messaggistica Web in-app</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi utilizzare la nuova funzionalità di messaggistica Web in-app per visualizzare contenuti personalizzati direttamente sui siti web tramite messaggi di sovrapposizione modale. Questa funzione consente di interagire in modo efficace con i visitatori web, migliorando l’interazione, la fidelizzazione e i tassi di conversione degli utenti.<br/><br/></p>
<!--img src="assets/do-not-localize/computed-attributes.gif"-->
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Regole aziendali (beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi creare regole di limitazione della frequenza che si applicano ai canali SMS e Direct Mail. Inoltre, puoi impostare regole di quota limite per tipo di comunicazione.<br/><br/></p>
<!--img src="assets/do-not-localize/computed-attributes.gif"-->
</tr>
</tbody>
</table>



### Miglioramenti {#e-improvements}

Questa versione include i miglioramenti elencati di seguito.

**Tipi di pubblico**

* **Elenchi seed** - Le varianti sono ora supportate quando si utilizza **elenchi seed**. Come ogni profilo del pubblico di destinazione, gli indirizzi di seed ricevono una copia di tutte le varianti dello stesso messaggio (come i diversi trattamenti di un esperimento di contenuto).

Precedentemente disponibili come versione beta, i seguenti miglioramenti sono ora disponibili per tutti gli utenti:

* Ora puoi eseguire il targeting **pubblico caricato da un file CSV** in percorsi e campagne. [Ulteriori informazioni](../audience/about-audiences.md#segments-in-journey-optimizer)
* Ora puoi eseguire il targeting **tipi di pubblico creati tramite la composizione del pubblico** e sfruttano gli attributi di arricchimento nei Percorsi. [Ulteriori informazioni](../building-journeys/read-audience.md)

**Percorsi**

* **Filtrare i percorsi** - È ora possibile utilizzare **date personalizzate per filtrare i percorsi** magazzino, oltre ai filtri di data predefiniti esistenti. Questo consente di perfezionare l’elenco visualizzando percorsi pubblicati in una data specifica, all’interno di un mese specifico, durante un anno intero o entro intervalli di tempo specifici.
* **Azioni personalizzate** - È ora possibile aggiornare l’intestazione &quot;content-type&quot; in **azioni personalizzate**.
* **Configurazione** : l’attributo identityMap in stepEvents ora è precompilato. L’identità primaria è definita come &quot;primary = true&quot;.
* **Interfaccia utente** - La barra superiore, nelle schermate di percorso, è stata riorganizzata per offrire un’esperienza migliore. Tra i diversi aggiornamenti, l’icona &quot;matita&quot; che consente di accedere alle proprietà del percorso è ora visualizzata a sinistra della barra superiore, accanto al nome del percorso.


**Canale SMS**

* **Parole chiave di consenso/rinuncia** - Durante la configurazione del canale SMS, ora puoi personalizzare la **Parole chiave di consenso e rinuncia** in base alle tue preferenze. Journey Optimizer attiva la risposta in base a queste parole chiave specificate.

**Campagne**

* **Campagne attivate da API** - Le informazioni sono state aggiunte nel **richiesta cURL** sezione di **Campagne attivate da API** che sono in **Bozza** per specificare che la richiesta cURL di esempio è visibile solo dopo la pubblicazione e l’esecuzione della campagna.

**Gestione delle decisioni**

* **Regole di limitazione** - È ora possibile aggiungere **più regole di limite** per un&#39;offerta. Ciò ti consente di aumentare il livello di controllo sulla modalità di invio delle offerte.

**Modelli di contenuto**

* **Miniatura** - A **visualizzazione miniature** è ora disponibile per modelli di contenuto e frammenti per migliorare l’accesso visivo.
* **Canali** - I modelli di contenuto sono ora disponibili per **tutti i canali**, ad eccezione del Web.