---
solution: Journey Optimizer
product: journey optimizer
title: Note preliminari sulla versione
description: Note preliminari sulla versione di Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 20f5dc6eab5695b485f4569ad098922a130d4b56
workflow-type: ht
source-wordcount: '1022'
ht-degree: 100%

---

# Note preliminari sulla versione {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nell’ultima settimana di ogni mese, tutte le modifiche vengono consolidate nelle [note sulla versione](release-notes.md).

**Le note preliminari sulla versione riportate di seguito sono soggette a modifiche senza preavviso fino alla data di disponibilità della versione**. I collegamenti, le schermate e la documentazione aggiornata vengono pubblicati nelle [note sulla versione](release-notes.md), alla data di rilascio.


## Note preliminari sulla versione di giugno 2025 {#25-6-rn}


**Le note preliminari sulla versione riportate di seguito sono soggette a modifica senza preavviso fino alla data di disponibilità della versione**. I collegamenti, le schermate e la documentazione aggiornata sono pubblicati alla data di rilascio.

**Data di rilascio**: 18 giugno 2025


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
<p>La messaggistica RCS (Rich Communication Services) è ora supportata in Journey Optimizer, consentendo le seguenti funzionalità di messaggistica avanzate, soggette al supporto di provider e operatore mobile.</p>
<ul>
<li>Supporto per mittente brandizzato e verificato: invia messaggi utilizzando profili aziendali verificati con elementi di branding (logo, nome del mittente, ecc.).</li>
<li>Informazioni approfondite sulla consegna dei messaggi: puoi ricevere rapporti di consegna dettagliati, inclusi gli aggiornamenti sullo stato del messaggio (ad esempio inviato, consegnato, letto).</li>
<li>Tracciamento dei collegamenti: incorpora e tieni traccia degli URL nei messaggi RCS per l’analisi del coinvolgimento.</li>
<li>Fallback su SMS: fallback automatico su SMS quando il dispositivo del profilo non supporta la RCS o è temporaneamente non raggiungibile tramite RCS.</li>
<li>Composizione di base dei messaggi: invia messaggi RCS basati su testo con elementi avanzati e file multimediali facoltativi, a seconda del supporto del provider.</li>
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
<th><strong>Campi modulo nei contenuti di esperienze basate su codice</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora è possibile definire campi modificabili specifici nei modelli di contenuto JSON o HTML, consentendo agli utenti non tecnici di modificare facilmente il contenuto di una visualizzazione modulo, nell’authoring del canale dell’esperienza basato su codice, senza il bisogno di manipolare alcun codice.<br />Inoltre, durante la definizione dei modelli di contenuto dell’esperienza basati su codice, è ora possibile inserire criteri di decisione nel modello, aumentando la riutilizzabilità e la facilità d’uso.</p>
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
<p>Oltre alla delega completa e al metodo CNAME, ora è disponibile un nuovo metodo di configurazione del sottodominio: il metodo di delega personalizzata consente di controllare e gestire completamente tutti gli aspetti del DNS necessari per la consegna, il rendering e il tracciamento dei messaggi.</p>
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
<p>Ora è possibile includere e utilizzare offerte personalizzate all’interno dei percorsi e delle attività relative tramite un’attività dedicata di Content Decisioning nell’area di lavoro del percorso, comprese condizioni e azioni personalizzate.</p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (disponibilità limitata) e verrà introdotta a livello globale in una versione futura.</p>
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
<th><strong>Prova del percorso</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La prova del percorso è una modalità speciale di pubblicazione di un percorso in Adobe Journey Optimizer che consente ai professionisti del percorso di poterne effettuare un test, utilizzando dati di produzione reali e senza la necessità di contattare la clientela reale o aggiornare le informazioni di profilo. Questa funzione aiuta i professionisti del percorso ad acquisire maggiore sicurezza rispetto alla progettazione di un percorso e al targeting del pubblico, prima della pubblicazione effettiva.</p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (disponibilità limitata) e verrà introdotta a livello globale in una versione futura.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Mettere in pausa e riprendere i percorsi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile mettere in pausa e riprendere i percorsi. Questa funzionalità offre ai professionisti del percorso maggiore controllo e flessibilità, consentendo di sospendere temporaneamente i percorsi live senza compromettere l’esperienza cliente. Quando il percorso è in pausa, le comunicazioni non vengono inviate e i profili rimangono in stato di sospensione fino a quando il percorso non viene ripreso.</p>
<p>È possibile mettere in pausa e riprendere un singolo percorso, oppure eseguire operazioni di pausa e di ripresa in blocco su un gruppo di percorsi.</p>
<p>Inoltre, è possibile applicare filtri globali ai percorsi in pausa per escludere i profili in base ai rispettivi attributi.</p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (disponibilità limitata) e verrà introdotta a livello globale in una versione futura.</p>
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
<p>Per “scalare il vincitore della sperimentazione” si intende presentare automaticamente o manualmente la variante vincente di un esperimento a tutto il pubblico. Questa funzione assicura che, una volta identificata la variante dalle prestazioni migliori, sia possibile massimizzarne la portata e l’efficacia senza una costante supervisione manuale.</p>
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

* **Set di regole del canale**

   * **Intervallo di durata personalizzato** per la limitazione: nella schermata di configurazione dei set di regole del canale è ora disponibile il nuovo campo **Conteggio ripetizioni**, che consente di applicare regole di quota limite su più giorni, settimane o mesi, a seconda della durata specificata.

   * **Durata oraria**: ora è possibile applicare una limitazione su base oraria per i set di regole del canale.

* **Esperienze basate su codice**

   * L’aggiunta di un criterio di decisione è ora disponibile nei modelli di contenuto di esperienza basati su codice.

   * Dalla schermata del percorso dell’esperienza basato sul codice o dell’edizione della campagna, ora puoi aggiungere direttamente un criterio di decisione senza aprire l’editor di personalizzazione.

* **Supporto CSS personalizzato in E-mail Designer**

  Journey Optimizer ora consente di aggiungere CSS personalizzato al contenuto delle e-mail direttamente all’interno di E-mail Designer.

* **Nuova navigazione con schede per le campagne**

  Un nuovo pattern di navigazione consente un accesso più rapido alla creazione dei contenuti e supporta un’ulteriore espansione delle impostazioni nelle campagne.

* **Decisioning** - Data di disponibilità: 3 giugno 2025

  Ora è possibile copiare gli oggetti decisionali in sandbox diverse, semplificando i test e i flussi di lavoro di implementazione. [Ulteriori informazioni](../configuration/copy-objects-to-sandbox.md#decisioning)

* **Supporto degli attributi di elementi decisionali per le regole decisionali** - Data di disponibilità: 4 giugno 2025

  Ora puoi sfruttare gli attributi degli elementi decisionali per creare regole decisionali. [Ulteriori informazioni](../experience-decisioning/rules.md#create)

* **Aggiornamento API per l’esecuzione messaggi interattivi** - Data di disponibilità: 6 giugno 2025

  L’API per l’esecuzione dei messaggi interattivi ora consente di eliminare la pianificazione per l’esecuzione delle campagne successive. [Ulteriori informazioni](https://developer.adobe.com/journey-optimizer-apis/references/messaging/){target="_blank"}