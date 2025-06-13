---
solution: Journey Optimizer
product: journey optimizer
title: Note preliminari sulla versione
description: Note preliminari sulla versione di Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 8188749c47be0a3d91b9857d170bceb4747a3400
workflow-type: tm+mt
source-wordcount: '1017'
ht-degree: 33%

---

# Note preliminari sulla versione {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nell’ultima settimana di ogni mese, tutte le modifiche vengono consolidate nelle [note sulla versione](release-notes.md).

**Le note preliminari sulla versione riportate di seguito sono soggette a modifiche senza preavviso fino alla data di disponibilità della versione**. I collegamenti, le schermate e la documentazione aggiornata vengono pubblicati nelle [note sulla versione](release-notes.md), alla data di rilascio.


## Note preliminari sulla versione del 25 giugno {#25-6-rn}


**Le note preliminari sulla versione riportate di seguito sono soggette a modifica senza preavviso fino alla data di disponibilità della versione**. I collegamenti, le schermate e la documentazione aggiornata sono pubblicati alla data di rilascio.

**Data di rilascio**: giovedì 18 giugno 2025


### Nuove funzionalità {#25-06-features}

Di seguito sono descritte le nuove funzionalità incluse in questa versione.




<table>
<thead>
<tr>
<th><strong>Messaggistica RCS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La messaggistica RCS (Rich Communication Services) è ora supportata in Journey Optimizer, consentendo le seguenti funzionalità di messaggistica avanzate soggette al supporto di provider e gestori:</p>
<ul>
<li>Supporto per mittenti con marchio e verificati: invia messaggi utilizzando profili aziendali verificati con elementi di branding (logo, nome del mittente, ecc.).</li>
<li>Informazioni sulla consegna dei messaggi: puoi ricevere rapporti di consegna dettagliati, inclusi gli aggiornamenti sullo stato del messaggio (ad esempio inviato, consegnato, letto).</li>
<li>Tracciamento dei collegamenti: incorpora e tieni traccia degli URL nei messaggi RCS per l’analisi del coinvolgimento.</li>
<li>Fallback a SMS: fallback automatico a SMS quando il dispositivo del profilo non supporta RCS o è temporaneamente non raggiungibile tramite RCS.</li>
<li>Composizione di base dei messaggi: invia messaggi RCS basati su testo con file multimediali facoltativi ed elementi avanzati, a seconda del supporto del provider.</li>
</ul>
<!--p>For more information, refer to the <a href="../sms/sms-configuration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>True Multi-Tenant Unitary Delivery</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>No description provided.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Campi modulo nel contenuto dell’esperienza basata su codice</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi definire campi modificabili specifici nei modelli di contenuto JSON o HTML, che consentono agli utenti non tecnici di modificare facilmente il contenuto in una visualizzazione modulo nell’authoring del canale di esperienza basato sul codice, senza dover manipolare alcun codice. Inoltre, quando definisci i modelli di contenuto dell’esperienza basati su codice ora puoi inserire criteri di decisione nel modello, aumentando la riutilizzabilità e la facilità d’uso.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Metodo di delega personalizzato per sottodomini</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Oltre alla delega completa e al metodo CNAME, ora è disponibile un nuovo metodo di configurazione del sottodominio: il metodo di delega personalizzata, che consente di gestire e controllare tutti gli aspetti del DNS necessari per la consegna, il rendering e il tracciamento dei messaggi.</p>
<p>Precedentemente rilasciata in versione a disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Attività Content Decisioning nei percorsi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi includere offerte personalizzate nei tuoi percorsi tramite un’attività Content Decisioning dedicata nell’area di lavoro del percorso e utilizzarle nelle attività del percorso, incluse condizioni e azioni personalizzate.</p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (disponibilità limitata) e verrà implementata a livello globale in una versione futura.</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Experience Decisioning in email channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>No description provided.</p>
</td>
</tr>
</tbody>
</table-->



<table>
<thead>
<tr>
<th><strong>Esecuzione di prova del percorso</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Percorsi Dry run è una speciale modalità di pubblicazione del percorso in Adobe Journey Optimizer che consente ai professionisti del percorso di testare un percorso utilizzando dati di produzione reali senza contattare clienti reali o aggiornare le informazioni del profilo. Questa funzione aiuta i professionisti del percorso ad acquisire fiducia nella progettazione del percorso e nel targeting del pubblico prima di pubblicarlo in diretta.</p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (disponibilità limitata) e verrà implementata a livello globale in una versione futura.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Sospendi e riprendi percorsi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile sospendere e riprendere i percorsi. Questa funzionalità offre ai professionisti del percorso maggiore controllo e flessibilità, consentendo la sospensione temporanea dei percorsi live senza interrompere la customer experience. Quando è in pausa, non vengono inviate comunicazioni e i profili rimangono in stato di sospensione fino alla ripresa del percorso.</p>
<p>È possibile sospendere e riprendere un solo percorso oppure eseguire le operazioni di pausa collettiva e ripresa di un gruppo di percorsi.</p>
<p>Inoltre, puoi applicare filtri globali ai percorsi in pausa per escludere i profili in base ai loro attributi.</p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (disponibilità limitata) e verrà implementata a livello globale in una versione futura.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Scalare il vincitore della sperimentazione</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Scalabilità del vincitore della sperimentazione consente di distribuire automaticamente o manualmente la variante vincente di un esperimento al pubblico completo. Questa funzione assicura che, una volta identificata la variante dalle prestazioni migliori, sia possibile massimizzarne la portata e l’efficacia senza una costante supervisione manuale.</p>
<p>Per ulteriori informazioni, consulta la <a href="../content-management/content-experiment.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 2 giugno 2025</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Conflitti e assegnazione delle priorità</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In Journey Optimizer, è essenziale gestire il volume e la tempistica delle campagne e dei percorsi per evitare di sopraffare la clientela con troppe interazioni. Journey Optimizer offre ora diversi strumenti per la gestione dei conflitti e l’assegnazione delle priorità. In precedenza disponibili solo per le organizzazioni con accesso alle funzionalità rilasciate con disponibilità limitata (LA), questi sono ora disponibili per tutti (GA, disponibilità generale).</p>
<p>Precedentemente rilasciata in versione a disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti. Con questa versione con disponibilità generale sono stati introdotti i seguenti miglioramenti:</p>
<ul>
<li>Supporto esteso: gli strumenti per la gestione dei conflitti ora supportano sia i percorsi unitari che i percorsi di qualificazione di un pubblico, oltre ai percorsi Leggi pubblico.</li>
<li>Risoluzione dei problemi migliorata: nel servizio query sono ora disponibili due nuovi campi evento del passaggio che consentono di analizzare il motivo per cui un profilo è stato rifiutato da un percorso o da una campagna.</li>
<li>Rapporti migliorati: i rapporti ora indicano la regola specifica che ha determinato l’esclusione di un profilo da un percorso o da una campagna, fornendo maggiore trasparenza e informazioni actionable.</li></ul>
<img src="assets/do-not-localize/gif-conflict.gif">
<p>Per ulteriori informazioni, consulta la <a href="../conflict-prioritization/gs-conflict-prioritization.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 3 giugno 2025</p>
</td>
</tr>
</tbody>
</table>


### Miglioramenti {#25-06-improv}

Di seguito sono elencati i miglioramenti inclusi in questa versione.

* **Set di regole canale**

   * **Intervallo di durata personalizzato** per il limite - Nella schermata di configurazione dei set di regole di canale è ora disponibile un nuovo campo **Conteggio ripetizioni** che consente di applicare le regole del limite di frequenza su più giorni, settimane o mesi, a seconda della durata specificata.

   * **Durata oraria** - È ora possibile applicare il limite su base oraria per i set di regole del canale.

* **Esperienze basate su codice**

  I criteri di decisione sono ora disponibili nei modelli di contenuto di esperienza basati su codice e nella barra a destra dell’editor di codice.

* **E-mail Designer**

   * **Supporto CSS personalizzato** - Journey Optimizer ora consente di aggiungere CSS personalizzato al contenuto delle e-mail direttamente all&#39;interno di E-mail Designer.
   * **Supporto modalità scura** - La finestra di progettazione e-mail di Journey Optimizer offre ora la possibilità di passare alla modalità scura in cui è possibile definire impostazioni specifiche.


* **Decisioning** - Data di disponibilità: 3 giugno 2025

  Ora è possibile copiare gli oggetti decisionali in sandbox diverse, semplificando i test e i flussi di lavoro di implementazione. [Ulteriori informazioni](../configuration/copy-objects-to-sandbox.md#decisioning)

* **Supporto degli attributi degli elementi di decisione per le regole di decisione** - Data di disponibilità: 4 giugno 2025

  Ora puoi sfruttare gli attributi degli elementi di decisione per creare regole di decisione. [Ulteriori informazioni](../experience-decisioning/rules.md#create)

* **Aggiornamento API di esecuzione messaggi interattivi** - Data di disponibilità: 6 giugno 2025

  L’API di esecuzione interattiva dei messaggi ora consente di eliminare la pianificazione della prossima esecuzione delle campagne. [Ulteriori informazioni](https://developer.adobe.com/journey-optimizer-apis/references/messaging/){target="_blank"}