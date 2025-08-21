---
solution: Journey Optimizer
product: journey optimizer
title: Note pre-release per Journey Optimizer
description: Note pre-release di Adobe Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 75c3db704853b8d2d8920ddd0086681d1fb02a93
workflow-type: ht
source-wordcount: '1033'
ht-degree: 100%

---

# Note pre-release {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nell’ultima settimana di ogni mese, tutte le modifiche vengono consolidate nelle [note sulla versione](release-notes.md).


## Note pre-release di agosto 2025 {#25-8-rn}

**Le note pre-release riportate di seguito sono soggette a modifica senza preavviso fino alla data di disponibilità della versione**. I collegamenti, le schermate e la documentazione aggiornata vengono pubblicati nelle note sulla versione, alla data di rilascio.

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
<li>Miglioramenti della progettazione per la navigazione tra date.</li>
<li>Possibilità di visualizzare le campagne di bozza se hai impostato una data di inizio e una data di fine</li>
<li>Nuova impostazione per nascondere e visualizzare gli elementi del calendario in esecuzione per molto tempo.</li>
</ul>
<p><!--img src="assets/do-not-localize/calendar.gif"/>--></p>
<p><!--For more information, refer to the <a href="../building-journeys/journey-ui.md#journeys-calendar">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Dark mode in the Email Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The Journey Optimizer Email Designer now offers the ability to switch to dark mode view, where you can additionally define specific custom settings that will display only for recipients reading their emails in dark mode.</p>
<p>Note the following:</p>
<ul>
<li>The dark mode final rendering may vary and depends on the recipient's email client.</li>
<li>Not all email clients support custom dark mode. Moreover, some email clients only apply their own default dark mode for all emails that are received. In both cases, the custom settings that you defined in the Email Designer cannot be rendered.</li>
</ul>
<P>This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.</p>
<p><img src="assets/do-not-localize/dark-mode.gif"/></p>
<p>For more information, refer to the <a href="../email/dark-mode.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table-->

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
<li>Supporto dei canali in entrata.</li>
<li>La funzione helper “datasetLookup” può ora essere utilizzata all’interno di frammenti di espressione e visivi per personalizzare il contenuto utilizzando i dati dei set di dati di Adobe Experience Platform,</li>
<li>Un’opzione nel set di dati ora consente di abilitare i set di dati per la personalizzazione della ricerca, senza dover eseguire una chiamata API.</li>
</ul>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Use Decisioning in email channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add Decision policies into email journeys and campaigns. Decision policies are containers for your offers that leverage the Decisioning engine to dynamically return the best content to deliver for each audience member.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p><img src="assets/do-not-localize/FILE.gif"/></p>
<p><For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Ottimizzazione del percorso</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ora offre gli strumenti per ottimizzare i tuoi percorsi sfruttando i framework di sperimentazione e l’intelligenza artificiale, garantendo al contempo un’usabilità fluida e la differenziazione tra le funzionalità di condizione e ottimizzazione.</p>
<p>Questa funzionalità è in disponibilità limitata. Per ottenere l’accesso, contatta il rappresentante Adobe.</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Attività di azione nei percorsi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer supporta una nuova attività Azione generica che consente di configurare sia azioni singole che gruppi di azioni multiple in uscita, semplificandone la configurazione nell’area di lavoro del percorso. In particolare, questa nuova funzione consente:</p>
<ul>
<li>Una configurazione semplificata dell’azione nativa nell’area di lavoro del percorso.</li>
<li>La capacità di creare nodi in entrata con più azioni.</li>
<li>La possibilità di aggiungere l’ottimizzazione a qualsiasi azione del canale incorporata.</li>
<li>La possibilità di aggiungere sia opzioni di sperimentazione che opzioni multilingue a qualsiasi azione.</li>
</ul>
<p>Questa funzionalità è in disponibilità limitata. Per ottenere l’accesso, contatta il rappresentante Adobe.</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Moduli personalizzati della pagina di destinazione</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ora consente di creare moduli personalizzati e di sfruttarli nelle pagine di destinazione per acquisire gli attributi di profilo nel set di dati definito per ciascun modulo.</p>
<p>Questa funzionalità è in disponibilità limitata. Per ottenere l’accesso, contatta il rappresentante Adobe.</p>
<p><!--This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.--></p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>


### Miglioramenti {#Aug-25-8-improv}

Di seguito sono elencati i miglioramenti inclusi in questa versione.

* **Amministrazione**

   * **Avvisi di monitoraggio della configurazione dei canali**: in caso di errore nella configurazione di un canale o di record DNS mancante, ora è possibile iscriversi per ricevere avvisi di sistema, tramite e-mail o nel centro notifiche di Journey Optimizer.

* **Campagne**

   * **Controllo della frequenza nelle campagne in uscita**: ora è possibile abilitare il controllo della limitazione di frequenza per le campagne in uscita (e-mail, SMS, notifiche push), consentendo di evitare il sovraccarico sui sistemi a valle, come le pagine di destinazione o le piattaforme di assistenza clienti.

   * **Pianificazione delle campagne di azione**: i moduli di pianificazione giornaliera, settimanale e mensile delle campagne sono stati aggiornati per migliorarne la granularità. Ad esempio, ora puoi impostare il numero di settimane/mesi tra le pianificazioni, definire il giorno in cui eseguire le campagne e decidere di interromperle dopo un numero specifico di occorrenze o in una data specifica.

   * **Campagne programmate per azioni transazionali**: le campagne programmate per azioni transazionali sono ora disponibili per l’invio di comunicazioni transazionali batch e basate sul pubblico tramite canali e-mail, SMS e push.

* **Canale - Push**

   * **Data di scadenza notifica push**: ora è possibile specificare una data di scadenza per ogni notifica push, impedendo l’invio di messaggi urgenti (come quelli delle offerte del Black Friday) dopo una determinata data, evitando quindi di fornire esperienze scadenti alla clientela.

* **Canale - E-mail**

   * **Allegati PDF alle e-mail**: ora è possibile allegare file PDF statici ai messaggi e-mail inviati con Journey Optimizer.

* **Canale - SMS**

   * **Rinuncia parziale**: se abilitata, l’opzione **Rinuncia parziale** rileva i messaggi in entrata più simili alle parole chiave di rinuncia definite (ad esempio, “CANCIL”) e invia automaticamente una risposta di conferma per verificare l’intenzione dell’utente di annullare l’iscrizione. Se l’utente conferma tramite il prompt definito, l’iscrizione viene annullata.

     Tenere presente che **Rinuncia parziale** è disponibile solo con Sinch e Infobip.

   * **Verifica connessione SMS**: ora è possibile testare e verificare facilmente le credenziali API SMS all’interno di Adobe Journey Optimizer inviando un messaggio di esempio a un dispositivo designato.

* **Configurazione**

   * **Supporto di domini dinamici**: Journey Optimizer ora supporta la personalizzazione negli URL di tracciamento per i domini predefiniti elencati a livello di configurazione dei canali.

   * **Supporto di attributi personalizzati con URL di annullamento dell’iscrizione con un solo clic**: con Journey Optimizer, se il consenso è gestito al fuori di Adobe, è possibile impostare un endpoint personalizzato esterno definendo un collegamento per l’annullamento dell’iscrizione con un solo clic nella configurazione dell’e-mail. Quando i destinatari fanno clic sul collegamento di annullamento dell’iscrizione, Journey Optimizer aggiunge alcuni parametri predefiniti specifici del profilo all’evento di aggiornamento del consenso.

     Per personalizzare ulteriormente il collegamento di annullamento dell’iscrizione con un solo clic, ora è possibile definire gli attributi personalizzati che verranno aggiunti all’evento di consenso.

* **Funzione Decisioni**

   * **Allega frammenti agli elementi decisionali**: Journey Optimizer ora consente di allegare frammenti agli elementi decisionali che possono essere utilizzati nelle campagne di esperienza basata su codice tramite i criteri di decisione.

* **Percorsi**

   * **Operazioni del percorso in blocco**: dall’elenco dei tuoi percorsi, ora puoi selezionare più elementi. Una volta selezionati, puoi sospendere o riprendere fino a 10 percorsi alla volta.
