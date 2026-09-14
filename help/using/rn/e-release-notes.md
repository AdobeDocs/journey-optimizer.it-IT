---
solution: Journey Optimizer
product: journey optimizer
title: Note pre-release per Journey Optimizer
description: Note pre-release di Adobe Journey Optimizer
hide: true
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
    internal-label: Administration
subfeature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
    internal-label: Journey Optimizer release notes
source-git-commit: b52a13ced7828d3e484508caf24b1e4716df087e
workflow-type: tm+mt
source-wordcount: '3422'
ht-degree: 10%
---

# Note pre-release {#e-release-notes}

Adobe Journey Optimizer offre continuamente nuove funzioni, miglioramenti a quelle esistenti e correzioni di bug. Nell’ultima settimana di ogni mese, tutte le modifiche vengono consolidate nelle [note sulla versione](release-notes.md).

## Note pre-release di settembre 2026 {#sep-26-rn}

**Le note pre-release riportate di seguito sono soggette a modifica senza preavviso fino alla data di disponibilità della versione**. I collegamenti, le schermate e la documentazione aggiornata vengono pubblicati una volta che le modifiche saranno disponibili in produzione. Anche se la maggior parte delle modifiche viene consegnata alla data di rilascio, alcune potrebbero essere implementate in un secondo momento. Per ulteriori informazioni, fai riferimento alla data di disponibilità elencata per ciascuna voce.

Consulta anche [Note pre-release di Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Data di rilascio**: 22-23 settembre 2026

### Gestione dei contenuti {#sep-26-content-management}

In questa versione, la seguente funzionalità verrà implementata per la gestione dei contenuti.

<table>
<thead>
<tr>
<th><strong>Plug-in per la copia dei messaggi e la progettazione delle e-mail in CX Collaborator</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In CX Coworker sono ora disponibili due nuovi plug-in per semplificare i <strong>flussi di lavoro di messaggistica ed e-mail</strong> dalla strategia alla distribuzione:</p>
<p><strong>Plug-in per la copia dei messaggi</strong>:</p>
<ul>
<li>Acquisisce i resoconti delle campagne e definisce le mappe di messaggistica, gli archi narrativi e i ruoli dei canali.</li>
<li>Crea una matrice di contenuti multidimensionale personalizzata per canali, punti di contatto, lingue, tipi di pubblico e varianti.</li>
<li>Produce una nuova copia e sfrutta Adobe Firefly per generare, ritagliare e adattare gli elementi visivi delle campagne.</li>
<li>Consente la valutazione diretta dei contenuti e sincronizza direttamente le risorse approvate con Journey Optimizer, Adobe Campaign V8 e Marketo.</li>
</ul>
<p><strong>Plug-in di progettazione e-mail</strong>:</p>
<ul>
<li>Converte gli obiettivi di marketing, le schermate di riferimento o i collegamenti di progettazione Figma in piani di layout personalizzati e e-mail HTML pronte per la produzione.</li>
<li>Gestisce le risorse riutilizzabili del brand, i token di progettazione e i modelli e-mail strutturali.</li>
<li>I controlli hanno assemblato il codice e-mail per la conformità aziendale, la qualità del design visivo e gli standard di accessibilità WCAG 2.1 AA.</li>
<li>Esporta HTML approvato direttamente in Adobe Journey Optimizer e Adobe Campaign.</li>
</ul>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15642" target="_blank">DOCAC-15642</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### Fedeltà {#sep-26-loyalty}

In questa versione, le seguenti funzionalità e miglioramenti sono disponibili per la fidelizzazione.

<table>
<thead>
<tr>
<th><strong>Opportunità di sfida</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Il menu Prestazioni fedeltà ora include una <strong>scheda Opportunità</strong>, che mette in evidenza tendenze e lacune rilevate dall'intelligenza artificiale, come l'attrito per progressione del livello o l'abbandono di attività di sfida, ciascuna con un impatto previsto e un'azione "Crea con intelligenza artificiale" con un solo clic per generare una sfida che la soddisfi.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15563" target="_blank">DOCAC-15563</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Aggiornamenti alla mappatura degli eventi di fedeltà</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La creazione o la modifica di una mappatura degli eventi ora utilizza un nuovo **generatore di mappature visive**: seleziona uno schema, scegli i campi da un selettore di campi ricercabili, mappa ogni campo su un campo evento fedeltà con stato di connessione per riga e visualizza in anteprima l’espressione JSONata generata automaticamente, con l’opzione di passare alla modifica manuale di JSONata in qualsiasi momento.</p><p>Inoltre, le "Definizioni degli eventi" nell’amministratore Fedeltà sono state rinominate "Mappature eventi", con una vista a elenco aggiornata che mostra il nome dello schema dell’evento Esperienza leggibile dall’utente.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15661" target="_blank">DOCAC-15661</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Abilità per i consigli sulla fedeltà di CX Coworker** - Gli addetti al marketing possono ora richiedere **opportunità di sfida** direttamente nell&#39;interfaccia conversazionale di CX Coworker, ottenendo idee fondate sulle sfide basate sulle tendenze reali dei programmi di fidelizzazione e trasformandole in sfide live senza uscire dalla chat. <a href="https://jira.corp.adobe.com/browse/DOCAC-15565" target="_blank">15565</a> DOCAC <!-- Documentation link: TBD -->

* **Sfide del dominio nell&#39;editor di personalizzazione della scheda di contenuto** - L&#39;editor di personalizzazione della scheda di contenuto ora supporta **Sfide** come dominio, consentendo l&#39;accesso ai metadati della richiesta di verifica durante l&#39;authoring della personalizzazione della scheda di contenuto. In questo modo è più facile creare contenuti personalizzati per ogni fase di una sfida, ovvero lancio, in corso e fine, senza codice personalizzato. <a href="https://jira.corp.adobe.com/browse/DOCAC-15681" target="_blank">15681</a> DOCAC <!-- Documentation link: TBD -->

### Formazione iniziale {#sep-26-onboarding}

In questa versione verrà introdotta la seguente funzionalità per l’onboarding.

<table>
<thead>
<tr>
<th><strong>Funzionalità guidate per l’onboarding di e-mail e percorsi (disponibilità generale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La transizione da un’altra piattaforma di marketing a Adobe Journey Optimizer è più semplice grazie a funzionalità guidate che ti consentono di spostare in Journey Optimizer i contenuti e i percorsi e-mail già esistenti. Un'area di lavoro <strong>dedicata</strong> ti consente di riutilizzare ciò che hai invece di ricompilare da zero.</p>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15330" target="_blank">DOCAC-15330</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### Percorsi {#sep-26-journeys}

In questa versione sono stati aggiunti i miglioramenti e le funzioni seguenti ai percorsi.

<table>
<thead>
<tr>
<th><strong>Simulazione del percorso in CX Collaborator (MCP &amp; Chat)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L'abilità <strong>Simulazione Percorso</strong> in CX Coworker automatizza la convalida end-to-end del percorso e consente di interpretare facilmente i risultati. Questa funzione attualmente supporta solo il flusso di simulazione rapida e non sostituisce completamente l’esperienza di simulazione manuale di Journey Optimizer.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15374" target="_blank">DOCAC-15374</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Sperimentazione del percorso di decisione nella simulazione del Percorso** - **Sperimentazione percorso**, parte dell&#39;attività Ottimizza in Decisioning, è ora supportata nella simulazione del Percorso. <a href="https://jira.corp.adobe.com/browse/DOCAC-15641" target="_blank">15641</a> DOCAC <!-- Documentation link: TBD -->

* **Supporto di ID supplementari nella simulazione di Percorso** - **L&#39;ID supplementare** è ora supportato nella simulazione di Percorso, consentendo di testare scenari utente complessi sia per i percorsi di pubblico di lettura che per quelli attivati da eventi. <a href="https://jira.corp.adobe.com/browse/DOCAC-15448" target="_blank">15448</a> DOCAC <!-- Documentation link: TBD -->

<table>
<thead>
<tr>
<th><strong>Creazione di percorsi dalla barra di CX Customerorker</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La creazione di <strong>Percorsi con IA</strong> è ora disponibile direttamente dalla barra laterale destra di CX Coworker, sostituendo la precedente esperienza di AI Assistant con un punto di ingresso integrato e con marchio diverso per la generazione di percorsi.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14898" target="_blank">DOCAC-14898</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Attività in entrata Attività del percorso di disattivazione</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Una nuova attività <strong>Inbound Activity Deactivation</strong> nell'area di lavoro del percorso consente di rimuovere un profilo da un massimo di cinque attività o esperienze in entrata direttamente da un percorso, separando l'interdizione in entrata dall'uscita dal percorso per un'orchestrazione cross-channel più avanzata.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15686" target="_blank">DOCAC-15686</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Logica di attesa per valutazione del pubblico in batch perfezionata** - Nell&#39;attività **Read audience**, l&#39;opzione &quot;Trigger dopo valutazione del pubblico in batch&quot; in percorsi ora attende sempre il completamento di una segmentazione in batch in corso, assicurando che il percorso utilizzi i dati di esecuzione invece di tornare a uno snapshot precedente. Se non è in corso alcuna segmentazione batch, il percorso utilizza immediatamente l’ultima istantanea disponibile, a meno che tale istantanea non sia lo stesso batch utilizzato nell’esecuzione precedente, nel qual caso il percorso attende, fino alla finestra configurata, un batch più recente e ignora l’esecuzione di quel giorno se nessuna arriva in tempo. <a href="https://jira.corp.adobe.com/browse/DOCAC-15465" target="_blank">15465</a> DOCAC <!-- Documentation link: TBD -->

* **Confronta le versioni di percorso con CX Coworker** - Oggi, la revisione di ciò che è cambiato tra due versioni di un percorso richiede il confronto manuale all&#39;interno di Journey Optimizer nodo per nodo - non esiste alcuna differenza strutturata, il che rende i controlli di revisione delle modifiche, audit e pre-pubblicazione lenti e soggetti a errori, soprattutto quando i percorsi diventano più complessi. Questa funzionalità consente a un cliente o a un agente di IA di confrontare due versioni qualsiasi di un percorso tramite CX Coworker Chat e di recuperare una versione completamente fedele, **differenze strutturate** - nodi aggiunti/rimossi/modificati/spostati con dettagli a livello di campo, connessioni modificate, modifiche delle proprietà a livello di percorso e conteggi di rollup - senza aprire Journey Optimizer. <a href="https://jira.corp.adobe.com/browse/DOCAC-15297" target="_blank">15297</a> DOCAC <!-- Documentation link: TBD -->

* **Anteprima del contenuto nell&#39;area di lavoro del percorso** - La revisione del contenuto del canale richiede oggi l&#39;apertura di ogni nodo singolarmente, uno alla volta - lenta e soggetta a errori in percorsi con molti nodi di canale, soprattutto dove la personalizzazione significa controllare più trattamenti o varianti per nodo. **Anteprima contenuto** rimuove tale attrito presentando una miniatura di contenuto per ogni nodo di canale direttamente nell&#39;area di lavoro, con una finestra modale a schermo intero per esaminare e passare da un trattamento all&#39;altro e da una variante all&#39;altra. <a href="https://jira.corp.adobe.com/browse/DOCAC-15456" target="_blank">15456</a> DOCAC <!-- Documentation link: TBD -->

* **Avviso di rilevamento anomalie del nuovo Percorso** - Un nuovo avviso di sistema ora avvisa quando il traffico giornaliero di un percorso attivo si scosta dalla propria linea di base cronologica o scende a zero in modo imprevisto tra le entrate del Percorso, le uscite dal Percorso e gli invii di eventi. Questo avviso è attualmente disponibile solo nelle sandbox di produzione. <a href="https://jira.corp.adobe.com/browse/DOCAC-15545" target="_blank">15545</a> DOCAC <!-- Documentation link: TBD -->

* **Eventi di passaggio ridotti per le attività attendi ed eventi** - Gli eventi di passaggio non vengono più generati per le attività **attendi** e **evento** quando il profilo non è stato effettivamente elaborato in tale attività. <!-- DRAFT: pending DOCAC sub-task under DOCAC-15691, see CJM-165835 --> <!-- Documentation link: TBD -->

* **Eliminazione step-event esecuzione di prova per rapporti personalizzati** - Nell&#39;ambito dell&#39;ottimizzazione step-event, Journey Optimizer ora interrompe la generazione di alcuni eventi di passaggio non segnalabili durante le esecuzioni di Percorso. Questo influisce solo sui rapporti personalizzati basati su questi tipi di eventi step a esecuzione ininterrotta. Se siete interessati, riattivate l&#39;esecuzione di prova per rigenerare i dati. <a href="https://jira.corp.adobe.com/browse/DOCAC-15691" target="_blank">15691</a> DOCAC <!-- Documentation link: TBD -->

* **Abilità di Coworker per l&#39;analisi dell&#39;igiene** - Una nuova abilità di **Analisi dell&#39;igiene** in CX Coworker esegue la scansione dei percorsi attivi e in bozza per individuare configurazioni non funzionanti, errori silenziosi e risorse inutilizzate o in decomposizione, come percorsi di bozza non aggiornati, origini dati orfane, errori persistenti di azione personalizzata e tassi di esclusione del consenso elevati, e visualizza le correzioni consigliate direttamente dalla chat. <a href="https://jira.corp.adobe.com/browse/DOCAC-15689" target="_blank">15689</a> DOCAC <!-- Documentation link: TBD -->

* **Competenza di collaboratore per l&#39;analisi delle prestazioni aziendali** - Una nuova abilità di **Analisi delle prestazioni aziendali** in CX Coworker analizza le prestazioni dei percorsi, spiega le aree di prestazioni inferiori e consiglia ottimizzazioni concrete, come attese di ricoinvolgimento, escalation dei canali, ottimizzazione dell&#39;ora di invio, esperimenti A/B, quota limite di frequenza o utilizzo del fuso orario del profilo, in base all&#39;obiettivo di ogni percorso. <a href="https://jira.corp.adobe.com/browse/DOCAC-15688" target="_blank">15688</a> DOCAC <!-- Documentation link: TBD -->

* **Timeout del ripristino automatico degli eventi nelle proprietà del Percorso** - Le proprietà del Percorso ora includono un&#39;impostazione **Imposta timeout ripristino evento**: per impostazione predefinita, gli eventi di percorso interessati vengono riprodotti automaticamente fino a 72 ore dopo un&#39;interruzione del servizio senza che sia necessaria alcuna azione. È possibile attivare questa impostazione per controllare la finestra di ripetizione (0-72 ore) per i percorsi sensibili al tempo. Anche il campo **Timeout o errore** esistente è stato rinominato in **Azione personalizzata/Timeout azione IDS** per evitare confusione tra le due impostazioni. <a href="https://jira.corp.adobe.com/browse/DOCAC-15685" target="_blank">15685</a> DOCAC <!-- Documentation link: TBD -->

### Canali {#sep-26-channels}

In questa versione sono disponibili le seguenti funzionalità e miglioramenti per i canali.

<table>
<thead>
<tr>
<th><strong>Attività live per Android Live Updates</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ora amplia le funzionalità di personalizzazione mobile in tempo reale estendendo il supporto di <strong>Attività live ad Android</strong>. Puoi fornire aggiornamenti sull’avanzamento in tempo reale direttamente agli utenti, ad esempio tracciamento degli ordini, stati dei voli, aggiornamenti degli eventi live e punteggi sportivi in tempo reale.</p>
<p>Oltre a supportare le attività di iOS Live, Journey Optimizer ora gestisce i token push temporanei per Android Live Updates sulle diverse configurazioni della piattaforma. Supporta sia i flussi di aggiornamento broadcast che quelli transazionali utilizzando campagne attivate da API e API headless.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15510" target="_blank">DOCAC-15510</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canale in uscita personalizzato (disponibilità generale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Canali in uscita personalizzati</strong> consentono agli amministratori di portare qualsiasi canale di messaggistica in uscita basato su HTTP, ad esempio WeChat, Kakao Talk, Messenger o un provider proprietario, direttamente in Journey Optimizer tramite un Channel Builder senza codice. Una volta configurati, i canali personalizzati sono disponibili in tutte le campagne, i percorsi e le campagne orchestrate, con lo stesso set completo di funzionalità dei canali nativi: personalizzazione con l’editor di espressioni, sperimentazione dei contenuti, anteprima e bozza, reporting predefinito e applicazione delle norme in materia di consenso e governance.</p>
<p>Con questa versione, i canali in uscita personalizzati acquisiscono anche diverse nuove funzionalità:</p>
<ul>
<li>Utilizza Journey Optimizer Decisioning nel payload del canale personalizzato tramite Personalization Editor, come nelle esperienze basate su codice.</li>
<li>Applica le regole business ai canali personalizzati nello stesso modo in cui già puoi farlo sui canali nativi.</li>
<li>Seleziona i canali personalizzati nell’elenco dei canali per le campagne attivate da API, operazione che in precedenza non era possibile.</li>
<li>Definisci un webhook di reporting per un canale personalizzato e collegalo a una configurazione di canale, in modo da arricchire i rapporti di Journey Optimizer con eventi di interazione.</li>
</ul>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14037" target="_blank">DOCAC-14037</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Sostituisci impostazioni di configurazione del canale e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Durante la creazione di percorsi e campagne, ora puoi ignorare i parametri e-mail derivati dalla configurazione del canale selezionata direttamente a livello di percorso o di azione della campagna.</p>
<p>Ciò ti consente di personalizzare i campi dell'intestazione e-mail (<strong>Dal nome</strong>, <strong>Dal prefisso e-mail</strong>, <strong>Rispondi al nome</strong> e <strong>Rispondi all'e-mail</strong>), l'indirizzo di esecuzione e i valori di annullamento iscrizione all'elenco, utilizzando gli attributi del profilo o i dati contestuali per un controllo più preciso. In particolare, questo consente ai dettagli del mittente di riflettere l’advisor, la posizione o la filiale pertinente per ciascun destinatario, anziché instradare tutti gli invii tramite un unico indirizzo aziendale.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14718" target="_blank">DOCAC-14718</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Flessibilità di autenticazione BYOP SMS personalizzato** - È ora possibile configurare **intestazioni di autenticazione personalizzate** durante la connessione della configurazione OAuth del provider SMS, tra cui la posizione del token nei messaggi in uscita e la formattazione della richiesta del token. <a href="https://jira.corp.adobe.com/browse/DOCAC-15638" target="_blank">15638</a> DOCAC <!-- Documentation link: TBD -->

### Campagne orchestrate {#sep-26-oc}

In questa versione sono state aggiunte alle campagne orchestrate le funzioni e i miglioramenti seguenti.

<table>
<thead>
<tr>
<th><strong>O partecipa all’attività per campagne orchestrate</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L'attività <strong>Join</strong> nelle campagne orchestrate ora supporta sia le condizioni di join AND che OR. Con la logica OR, un profilo che completa un singolo ramo a monte, anziché tutti, continua lungo un singolo percorso a valle condiviso. Questo rende possibile modellare "se A o B o C, quindi fai questo" pattern direttamente sull’area di lavoro senza duplicare i passaggi a valle tra rami separati.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15020" target="_blank">DOCAC-15020</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Avvisi per campagne orchestrate</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le campagne orchestrate ora supportano <strong>avvisi automatizzati</strong> tramite lo stesso framework di avvisi utilizzato nei percorsi e nelle campagne. Gli avvisi vengono attivati quando l’esecuzione di una campagna ha esito negativo, si interrompe o richiede conferma e ogni avviso include ciò che è successo, quando, dove e un collegamento diretto alla vista monitoraggio, suddiviso in categorie in base alla gravità in modo che i team possano definire la priorità senza controlli manuali dell’interfaccia utente.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14886" target="_blank">DOCAC-14886</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Canale LINE per campagne orchestrate** - LINE è ora disponibile come canale nativo in uscita nelle campagne orchestrate, insieme a e-mail, SMS e push. Puoi creare e inviare messaggi LINE direttamente dall’area di lavoro della campagna, inclusi testo, adesivi, immagini, video, dati sulla posizione e messaggi Flex, supportando casi di utilizzo promozionali, transazionali e di coinvolgimento continuo in mercati dominanti LINE come il Giappone e APAC. Precedentemente rilasciata in Disponibilità limitata, questa funzionalità è ora generalmente disponibile. <a href="https://jira.corp.adobe.com/browse/DOCAC-15102" target="_blank">15102</a> DOCAC <!-- Documentation link: TBD -->

* **API di monitoraggio per nuove campagne orchestrate** - Sono ora disponibili nuove **specifiche API** per le campagne orchestrate, che consentono di creare, gestire e attivare in modo programmatico campagne orchestrate, consentendo una maggiore integrazione con sistemi esterni e pipeline di automazione. <a href="https://jira.corp.adobe.com/browse/DOCAC-14308" target="_blank">14308</a> DOCAC <!-- Documentation link: TBD -->

* **Miglioramenti dell&#39;interfaccia utente Direct Join** - Quando si aggiunge un attributo da una raccolta correlata, è ora possibile scegliere tra tre modalità di unione, una nuova impostazione predefinita che segnala il potenziale impatto sulle prestazioni dei prodotti cartesiani, oltre alle modalità Aggregate e Advanced esistenti, per semplificare la comprensione dei compromessi della query prima di generarla. <a href="https://jira.corp.adobe.com/browse/DOCAC-15675" target="_blank">15675</a> DOCAC <!-- Documentation link: TBD -->

* **Contenuto condizionale con dati relazionali in campagne orchestrate** - Durante la creazione di contenuto condizionale in E-mail Designer per campagne orchestrate, ora è possibile creare condizioni direttamente su **dati relazionali**, ad esempio record correlati associati a un profilo, non solo attributi di profilo standard. In questo modo si colma un vuoto rispetto alla versione originale, consentendo agli addetti al marketing di creare visivamente queste condizioni senza bisogno di assistenza tecnica. <a href="https://jira.corp.adobe.com/browse/DOCAC-15679" target="_blank">15679</a> DOCAC <!-- Documentation link: TBD -->

### Campagne {#sep-26-campaigns}

In questa versione sono disponibili le seguenti funzionalità e miglioramenti per le campagne.

<table>
<thead>
<tr>
<th><strong>Simulazione dell’esperienza in entrata nelle campagne d’azione (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi simulare le azioni del canale in entrata nelle campagne di azione prima della pubblicazione. Utilizza la modalità di simulazione per testare la configurazione con utenti simulati e visualizzare in anteprima l’esperienza di cui è stato eseguito il rendering, inclusi un URL generato e un codice QR, in modo da poter convalidare regole, decisioni e rendering end-to-end dei contenuti.</p>
<p>Questa funzionalità è attualmente disponibile in versione Private Beta per un numero limitato di organizzazioni. Per ulteriori informazioni, contatta il tuo rappresentante Adobe.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15166" target="_blank">DOCAC-15166</a></p>
</td>
</tr>
</tbody>
</table>

* **Cartelle per le campagne** - È ora possibile organizzare le campagne in **cartelle** per migliorare la navigazione e la gestione nell&#39;interfaccia. <a href="https://jira.corp.adobe.com/browse/DOCAC-15098" target="_blank">15098</a> DOCAC <!-- Documentation link: TBD -->

### Decisioni {#sep-26-decisioning}

In questa versione sono stati aggiunti i miglioramenti e le funzioni seguenti per la funzione Decisioni.

<table>
<thead>
<tr>
<th><strong>Supporto per le decisioni nel canale web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La funzione Decisioni è ora disponibile per il canale web. Puoi utilizzare i criteri di decisione direttamente nell’editor visivo per il web per fornire le offerte più rilevanti a chi visita il sito.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-11548" target="_blank">DOCAC-11548</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Generazione di regole di decisioning da CX Coworker** - L&#39;esperienza **Generazione di regole di decisioning assistite da AI**, precedentemente disponibile tramite la barra corretta, è ora accessibile tramite CX Coworker, che sostituisce la barra corretta come metodo per creare regole con AI. <a href="https://jira.corp.adobe.com/browse/DOCAC-15290" target="_blank">15290</a> DOCAC <!-- Documentation link: TBD -->

### Direct mail {#sep-26-direct-mail}

In questa versione, le funzionalità e i miglioramenti seguenti verranno introdotti in Direct Mail.

* **Dividi automaticamente i file di grandi dimensioni** - I file di Direct Mail possono ora essere suddivisi in più parti automaticamente quando superano i 20 GB circa o manualmente scegliendo una dimensione di file di destinazione nella configurazione di indirizzamento dei file. Un file manifesto JSON facoltativo descrive tutte le parti generate. <a href="https://jira.corp.adobe.com/browse/DOCAC-15677" target="_blank">15677</a> DOCAC <!-- Documentation link: TBD -->

* **Limite di pubblico aumentato** - Il limite di pubblico del canale Direct Mail è stato aumentato da 3 milioni a 100 milioni di profili, consentendo di indirizzare tipi di pubblico molto più grandi senza riscontrare errori di creazione dei file. <a href="https://jira.corp.adobe.com/browse/DOCAC-15676" target="_blank">15676</a> DOCAC <!-- Documentation link: TBD -->

### E-mail designer {#sep-26-email-designer}

In questa versione, e-mail Designer presenta le seguenti funzionalità e miglioramenti.

<table>
<thead>
<tr>
<th><strong>Stile indipendente in modalità scura per le varianti del tema e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>I temi e-mail ora supportano lo stile indipendente per la modalità scura. Nel generatore di temi è possibile attivare la modalità scura per una determinata variante per generare un foglio di stile dedicato in modalità scura che viene modificato separatamente dagli stili in modalità chiara. Le modifiche apportate in una modalità non sovrascrivono più l'altra. Nell’editor e-mail e modelli, una nuova opzione di anteprima accanto alle opzioni di visualizzazione per desktop e dispositivi mobili consente di visualizzare l’anteprima del contenuto in modalità scura.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15663" target="_blank">DOCAC-15663</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Importare modelli Dynamic Media direttamente dai file PSD nel Designer e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Il componente Dynamic Media di E-mail Designer ora consente di importare un file Photoshop (PSD) direttamente come nuovo modello, oltre a sfogliare i modelli Dynamic Media esistenti. Trascina e rilascia un file PSD nel componente, quindi Adobe Journey Optimizer lo converte automaticamente in un modello Dynamic Media memorizzato in Dynamic Media: non è necessaria alcuna conversione manuale o round trip through Adobe Experience Manager. Una volta importato, puoi modificare il modello utilizzando l’editor Dynamic Media integrato, la stessa esperienza utilizzata per il contenuto Adobe Express nel Designer e-mail.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15664" target="_blank">DOCAC-15664</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nuovo componente tabella in E-mail Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>E-mail Designer ora include un <strong>componente tabella</strong> incorporato, che consente di strutturare il contenuto in righe e colonne direttamente all'interno dell'e-mail. Trascina e rilascia il componente nell’area di lavoro, personalizza il numero di righe e colonne e applica uno stile indipendente a ogni cella per creare layout chiari e organizzati senza affidarsi a HTML personalizzati.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15093" target="_blank">DOCAC-15093</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Tipi di carattere di fallback per i tipi di carattere personalizzati nei temi e-mail** - È ora possibile definire un tipo di carattere di fallback per qualsiasi tipo di carattere personalizzato (Web) applicato tramite i temi e-mail. Se il client e-mail di un abbonato non supporta il font personalizzato, Adobe Journey Optimizer visualizza automaticamente il font di fallback specificato invece di lasciare la scelta sul font predefinito del client e-mail. In questo modo la tipografia delle e-mail è più vicina alle linee guida del brand e riduce le incoerenze nel rendering dei font tra i client e-mail. <a href="https://jira.corp.adobe.com/browse/DOCAC-15662" target="_blank">15662</a> DOCAC <!-- Documentation link: TBD -->

### Generazione di rapporti {#sep-26-reporting}

In questa versione verrà presentata la seguente funzionalità per la generazione di rapporti.

<table>
<thead>
<tr>
<th><strong>Nuovi grafici di monitoraggio in entrata in Gestione dati</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile monitorare l'integrità dei dati in entrata direttamente da <strong>Gestione dati &gt; Monitoraggio &gt; Edge</strong>, con sei nuovi grafici che includono gli eventi relativi a velocità effettiva, latenza e proposta:</p>
<ul>
<li><strong>Throughput in entrata AJO</strong>: throughput in entrata complessivo (record al secondo) nel tempo.</li>
<li><strong>Analisi stratificata velocità effettiva in entrata di AJO</strong>: velocità effettiva in entrata suddivisa per posizione.</li>
<li><strong>Latenza in entrata AJO</strong> — latenza richiesta in entrata (in millisecondi), suddivisa per la distribuzione dei valori (P50, P90 e altro).</li>
<li><strong>Throughput eventi proposte in entrata di AJO</strong>: throughput degli eventi di proposta (segnali di tracciamento generati quando un utente interagisce, visualizza o attiva offerte personalizzate) nel tempo.</li>
<li><strong>Throughput degli eventi delle proposte in entrata di AJO per canale</strong> — throughput degli eventi delle proposte suddiviso per canale in entrata (CBE, in-app, schede di contenuto).</li>
<li><strong>Throughput eventi proposte in entrata AJO per tipo di evento</strong> — throughput eventi proposte suddiviso per tipo di evento (ignorato, soppresso, visualizzato, attivato, interagito, inviato).</li>
</ul>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15680" target="_blank">DOCAC-15680</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### Amministrazione {#sep-26-administration}

Il seguente promemoria si applica all’amministrazione in questa versione.

* **Guardrail TTL (Time-to-live) del set di dati: sandbox esistenti**. Il guardrail TTL (time-to-live) per i set di dati generati dal sistema Journey Optimizer (90 giorni nell&#39;archivio dei profili, 13 mesi nel data lake) verrà applicato alle sandbox e alle organizzazioni dei clienti esistenti a partire dal 1° ottobre 2026. <a href="https://jira.corp.adobe.com/browse/DOCAC-15239" target="_blank">15239</a> DOCAC <!-- Documentation link: TBD -->

* **Prossima modifica ai tipi di pubblico per l&#39;arricchimento della composizione del pubblico** - Durante la versione di ottobre (fine ottobre), Journey Optimizer interromperà i percorsi che utilizzano o fanno riferimento a un pubblico per la composizione del pubblico il cui set di dati di origine non ha un **descrittore di identità primario**. Da quel momento in poi, solo i tipi di pubblico di Composizione del pubblico generati con un descrittore di identità principale sono supportati nei percorsi. Se hai bisogno che questi percorsi rimangano attivi, contatta il tuo rappresentante Adobe: il nostro team di prodotto può aiutarti a migrare. <a href="https://jira.corp.adobe.com/browse/DOCAC-15690" target="_blank">15690</a> DOCAC <!-- Documentation link: TBD -->

### Miglioramenti dell’usabilità {#sep-26-usability}

* **Miglioramenti di usabilità nell&#39;esperienza di simulazione dei contenuti** - La nuova esperienza di simulazione dei contenuti ora consente di denominare e organizzare le varianti per facilitare il confronto, copiare o eliminare i dettagli delle varianti direttamente da ogni scheda, visualizzare i percorsi degli attributi completi e la configurazione del canale per scheda su richiesta e caricare profili CSV, JSON o JSONL personalizzati da un pulsante di caricamento più prominente. <a href="https://jira.corp.adobe.com/browse/DOCAC-15570" target="_blank">15570</a> DOCAC

* **Calendario unificato per campagne, Percorsi e campagne orchestrate** - La visualizzazione calendario per percorsi e campagne ora si sposta da inventari separati in un menu unificato accessibile dalla barra a sinistra che mostra entrambi in un&#39;unica visualizzazione combinata. <a href="https://jira.corp.adobe.com/browse/DOCAC-15571" target="_blank">15571</a> DOCAC <!-- Documentation link: TBD -->


