---
solution: Journey Optimizer
product: journey optimizer
title: Note pre-release per Journey Optimizer
description: Note pre-release di Adobe Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 1f53a578e91cd26e0e062c20b371a344ad709a8f
workflow-type: tm+mt
source-wordcount: '1030'
ht-degree: 47%

---

# Note pre-release {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nell’ultima settimana di ogni mese, tutte le modifiche vengono consolidate nelle [note sulla versione](release-notes.md).


## Note preliminari al 25 agosto {#25-8-rn}

**Le note precedenti al rilascio sono soggette a modifiche senza preavviso fino alla data di disponibilità del rilascio**. I collegamenti, le schermate e la documentazione aggiornata vengono pubblicati nelle note sulla versione, alla data di rilascio.

Consulta anche [Note pre-release di Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Data di rilascio**: 19 agosto 2025


### Nuove funzionalità {#Aug-25-8-features}

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
<p><!--img src="assets/do-not-localize/PauseResume.gif"/>--></p>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p><!--For more information, refer to the <a href="../building-journeys/journey-pause.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Vista calendario</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Negli elenchi dei percorsi e delle campagne è ora disponibile una vista calendario. Consente di visualizzare tutte le attivazioni dei percorsi e delle campagne nei rispettivi elenchi.</p>
<p>Precedentemente rilasciata in versione a disponibilità limitata, questa funzione è ora disponibile per tutti gli ambienti. Con questa versione in disponibilità generale, la funzione include:</p>
<ul>
<li>Miglioramenti della progettazione per la navigazione nelle date,</li>
<li>Possibilità di visualizzare le bozze delle campagne se hai impostato una data di inizio e una data di fine</li>
<li>Nuova impostazione per nascondere e visualizzare gli elementi del calendario in esecuzione per un periodo di tempo prolungato.</li>
</ul>
<p><!--img src="assets/do-not-localize/calendar.gif"/>--></p>
<p><!--For more information, refer to the <a href="../building-journeys/journey-ui.md#journeys-calendar">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Modalità scura in E-mail designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>E-mail designer di Journey Optimizer ora offre la possibilità di passare alla visualizzazione in modalità scura, in cui è possibile definire anche impostazioni personalizzate specifiche da mostrare solo per i destinatari che leggono le e-mail in modalità scura.</p>
<p>Si noti quanto segue:</p>
<ul>
<li>Il rendering finale in modalità scura può variare e dipende dal client e-mail del destinatario.</li>
<li>Non tutti i client e-mail supportano la modalità scura personalizzata. Inoltre, alcuni client e-mail applicano soltanto la propria modalità scura predefinita per tutte le e-mail ricevute. In entrambi i casi, non è possibile eseguire il rendering delle impostazioni personalizzate definite in E-mail designer.</li>
</ul>
<P>Questa funzionalità è disponibile attualmente in versione beta e solo per la clientela beta. Per partecipare al programma Beta, contatta il tuo rappresentante Adobe.</p>
<p><!--img src="assets/do-not-localize/dark-mode.gif"/>--></p>
<p><!--For more information, refer to the <a href="../email/dark-mode.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Utilizzare i dati di Adobe Experience Platform per la personalizzazione</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sfrutta i dati da Adobe Experience Platform nell’editor di personalizzazione per personalizzare i contenuti. A questo scopo, i set di dati necessari per la personalizzazione della ricerca devono prima essere abilitati tramite una chiamata API. Al termine, è possibile utilizzare i relativi dati per personalizzare il contenuto in [!DNL Journey Optimizer].</p>
<p>Precedentemente rilasciata in versione a disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti. Con questa versione con disponibilità generale sono stati introdotti i seguenti miglioramenti:</p>
<ul>
<li>Supporto dei canali in entrata,</li>
<li>La funzione helper "datasetLookup" può ora essere utilizzata all’interno di frammenti di espressione e visivi per personalizzare il contenuto utilizzando i dati dei set di dati di Adobe Experience Platform,</li>
<li>Un’opzione nel set di dati ora consente di abilitare i set di dati per la personalizzazione di ricerca, senza dover eseguire una chiamata API.</li>
</ul>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Utilizzare la funzione Decisioni nel canale e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi aggiungere i criteri di decisione in percorsi e campagne e-mail. I criteri di decisione sono contenitori per le offerte che sfruttano il motore di Decisione per restituire in modo dinamico il contenuto migliore da consegnare per ogni membro del pubblico.</p>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Moduli personalizzati per pagine di destinazione</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ora consente di creare moduli personalizzati e di sfruttarli nelle pagine di destinazione per acquisire gli attributi di profilo nel set di dati definito per ciascun modulo.</p>
<p>Questa funzionalità è disponibile attualmente in versione beta e solo per la clientela beta. Per partecipare al programma Beta, contatta il tuo rappresentante Adobe.</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Ottimizzazione del percorso</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ora ti offre gli strumenti per ottimizzare i tuoi percorsi sfruttando i framework di intelligenza artificiale e sperimentazione e garantendo al contempo l’usabilità fluida e la differenziazione tra le funzionalità di condizione e ottimizzazione.</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>


### Miglioramenti {#Aug-25-8-improv}

Di seguito sono elencati i miglioramenti inclusi in questa versione.

- **Amministrazione**
   - **Avvisi di monitoraggio della configurazione del canale** - È ora possibile abbonarsi per ricevere gli avvisi di sistema, tramite e-mail o nel centro notifiche di Journey Optimizer, nel caso in cui si verifichi un errore di configurazione del canale o se manca un record DNS.

- **Campagne**
   - **Controllo del tasso nelle campagne in uscita** - È ora possibile abilitare il controllo del tasso di limitazione per le campagne in uscita (e-mail, SMS, notifiche push), consentendo di evitare il sovraccarico sui sistemi a valle, come le pagine di destinazione o le piattaforme di assistenza clienti.
   - **Pianificazione delle campagne azione** - Le pianificazioni giornaliere, settimanali e mensili della campagna sono state aggiornate per migliorarne la granularità. Ad esempio, ora puoi impostare il numero di settimane/mesi tra le pianificazioni, definire il giorno in cui eseguire e decidere di interrompersi dopo un numero specifico di occorrenze o in una data specifica.

- **Canale - Push**
   - **Data di scadenza notifica push** - È ora possibile specificare una data di scadenza per ogni notifica push, che impedisce l&#39;invio di messaggi sensibili al tempo (ad esempio Black Friday Sale) dopo una determinata data, evitando in tal modo di fornire ai clienti esperienze scadenti.

- **Canale - E-mail**
   - **Allegati PDF alle e-mail** - È ora possibile allegare file PDF statici ai messaggi e-mail inviati con Journey Optimizer.

- **Configurazione**
   - **Supporto di domini dinamici** - Journey Optimizer ora supporta la personalizzazione negli URL di tracciamento per i domini predefiniti elencati a livello di configurazione del canale.
   - **Supporto di attributi personalizzati con URL per l&#39;annullamento dell&#39;iscrizione con un solo clic**. Con Journey Optimizer, se gestisci il consenso al di fuori di Adobe, puoi impostare un endpoint personalizzato esterno definendo un collegamento per l&#39;annullamento dell&#39;iscrizione con un solo clic nella configurazione dell&#39;e-mail. Quando i destinatari fanno clic sul collegamento di annullamento dell’abbonamento, Journey Optimizer aggiunge alcuni parametri predefiniti specifici del profilo all’evento di aggiornamento del consenso.

     Per personalizzare ulteriormente il collegamento di annullamento dell’iscrizione con un solo clic, ora puoi definire gli attributi personalizzati che verranno aggiunti all’evento di consenso.

- **Percorsi**
   - **Attività azione nei percorsi** - Journey Optimizer supporta una nuova attività Azione generica che consente di configurare azioni in uscita a canale singolo e multicanale, semplificando la configurazione delle azioni nell&#39;area di lavoro del percorso. Con questa nuova attività, puoi anche aggiungere l’ottimizzazione del targeting, esperimenti e varianti di linguaggio multilingue a qualsiasi azione di canale incorporata.
   - **Operazioni di Percorso in serie** - Dall&#39;elenco dei tuoi percorsi, ora puoi selezionare più elementi. Una volta selezionata, puoi sospendere o riprendere fino a 10 percorsi alla volta.