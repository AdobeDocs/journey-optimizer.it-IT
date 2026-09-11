---
solution: Journey Optimizer
product: journey optimizer
title: Note pre-release per Journey Optimizer
description: Note pre-release di Adobe Journey Optimizer
hide: true
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: bb359667-ec7d-4d4b-8663-5850fc219d32
subfeature_v2: id: a7b2bfc5-be71-4740-b371-76fa6be8df02
source-git-commit: c8585d3a3d3d9f1c1f13cb52dbc1dfc62bb52468
workflow-type: tm+mt
source-wordcount: 1958
ht-degree: 19%

---


# Note pre-release {#e-release-notes}

Adobe Journey Optimizer offre continuamente nuove funzioni, miglioramenti a quelle esistenti e correzioni di bug. Nell’ultima settimana di ogni mese, tutte le modifiche vengono consolidate nelle [note sulla versione](release-notes.md).

## Note pre-release di settembre 2026 {#sep-26-rn}

**Le note pre-release riportate di seguito sono soggette a modifica senza preavviso fino alla data di disponibilità della versione**. I collegamenti, le schermate e la documentazione aggiornata vengono pubblicati una volta che le modifiche saranno disponibili in produzione. Anche se la maggior parte delle modifiche viene consegnata alla data di rilascio, alcune potrebbero essere implementate in un secondo momento. Per ulteriori informazioni, fai riferimento alla data di disponibilità elencata per ciascuna voce.

Consulta anche [Note pre-release di Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Data di rilascio**: 21-22 settembre 2026

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
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Abilità per i consigli sulla fedeltà di CX Coworker** - Gli addetti al marketing possono ora richiedere **opportunità di sfida** direttamente nell&#39;interfaccia conversazionale di CX Coworker, ottenendo idee fondate sulle sfide basate sulle tendenze reali dei programmi di fidelizzazione e trasformandole in sfide live senza uscire dalla chat. <!-- Documentation link: TBD -->

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
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

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
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Sperimentazione del percorso di decisione nella simulazione del Percorso** - **Sperimentazione percorso**, parte dell&#39;attività Ottimizza in Decisioning, è ora supportata nella simulazione del Percorso. <!-- Documentation link: TBD -->

* **Supporto di ID supplementari nella simulazione di Percorso** - **L&#39;ID supplementare** è ora supportato nella simulazione di Percorso, consentendo di testare scenari utente complessi sia per i percorsi di pubblico di lettura che per quelli attivati da eventi. <!-- Documentation link: TBD -->

* **Logica di attesa per valutazione del pubblico in batch perfezionata** - Nell&#39;attività **Read audience**, l&#39;opzione &quot;Trigger dopo valutazione del pubblico in batch&quot; in percorsi attende ora una nuova valutazione del pubblico solo quando è già in corso una segmentazione in batch e il batch da attivare è diverso da quello utilizzato nell&#39;esecuzione precedente, evitando inutili ritardi per percorsi che non devono attendere. <!-- Documentation link: TBD -->

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
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canale di destinazione in percorsi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer ora include un nuovo <strong>nodo Destinazioni</strong> nell'area di lavoro del percorso, consentendo ai clienti congiunti di Adobe Experience Platform Real-Time CDP e Journey Optimizer di aggiungere o rimuovere profili da tipi di pubblico esterni di media a pagamento, come Facebook e Google, direttamente all'interno di un percorso.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Flessibilità di autenticazione BYOP SMS personalizzato** - È ora possibile configurare **intestazioni di autenticazione personalizzate** durante la connessione della configurazione OAuth del provider SMS, tra cui la posizione del token nei messaggi in uscita e la formattazione della richiesta del token. <!-- Documentation link: TBD -->

### Campagne orchestrate {#sep-26-oc}

In questa versione sono state aggiunte alle campagne orchestrate le funzioni e i miglioramenti seguenti.

<table>
<thead>
<tr>
<th><strong>Attività di unione OR</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L'attività AND-join è stata aggiornata a un'attività <strong>Join generica</strong>, che consente di scegliere tra le condizioni AND e OR join.</p>
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
<p>Le campagne orchestrate ora supportano <strong>avvisi in tempo reale</strong>, incluse le notifiche critiche quando una campagna non riesce, viene eseguita più a lungo di una soglia definita o viene restituito un errore a livello di attività, in modo che gli addetti al marketing possano rilevare e risolvere i problemi senza attendere il completamento di una campagna.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Supporto per LINE** - È ora possibile aggiungere **azioni LINE** direttamente nelle campagne orchestrate. Questa nuova attività ti consente di creare e consegnare contenuti altamente personalizzati, inclusi testo, adesivi, immagini, video, dati sulla posizione e messaggi Flex avanzati, per coinvolgere la clientela in modo semplice sulla piattaforma LINE. Precedentemente rilasciata in Disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (Disponibilità generale). <!-- Documentation link: TBD -->

* **API di monitoraggio per nuove campagne orchestrate** - Sono ora disponibili nuove **specifiche API** per le campagne orchestrate, che consentono di creare, gestire e attivare in modo programmatico campagne orchestrate, consentendo una maggiore integrazione con sistemi esterni e pipeline di automazione. <!-- Documentation link: TBD -->

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
</td>
</tr>
</tbody>
</table>

* **Cartelle per le campagne** - È ora possibile organizzare le campagne in **cartelle** per migliorare la navigazione e la gestione nell&#39;interfaccia. <!-- Documentation link: TBD -->

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
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Generazione delle regole di decisioning da CX Coworker** - L&#39;esperienza **Generazione delle regole di decisioning assistito da AI**, precedentemente disponibile tramite la barra destra, è ora accessibile tramite CX Coworker, che sostituisce la barra destra come metodo per creare regole con AI. <!-- Documentation link: TBD -->

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
<p>Poiché questa anteprima nell’editor si basa su un filtro CSS e non è perfetta per i pixel, si consiglia di inviare una bozza per verificare l’esatto rendering nei client e-mail abilitati per la modalità scura.</p>
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
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Tipi di carattere di fallback per i tipi di carattere personalizzati nei temi e-mail** - È ora possibile definire un tipo di carattere di fallback per qualsiasi tipo di carattere personalizzato (Web) applicato tramite i temi e-mail. Se il client e-mail di un abbonato non supporta il font personalizzato, Adobe Journey Optimizer visualizza automaticamente il font di fallback specificato invece di lasciare la scelta sul font predefinito del client e-mail. In questo modo la tipografia delle e-mail è più vicina alle linee guida del brand e riduce le incoerenze nel rendering dei font tra i client e-mail. <!-- Documentation link: TBD -->

### Amministrazione {#sep-26-administration}

In questa versione è disponibile il seguente miglioramento per la somministrazione.

* **Processo OTP del ciclo di feedback per i sottodomini personalizzati** - Il processo di configurazione del sottodominio personalizzato del ciclo di feedback (FBL) è stato migliorato presentando l&#39;hub mittente di Yahoo **One-Time Password (OTP)** direttamente nell&#39;interfaccia utente del prodotto. Ora gli utenti possono recuperare e visualizzare automaticamente l’OTP generato durante la verifica della proprietà del dominio dell’hub del mittente Yahoo. <!-- Documentation link: TBD -->

### Miglioramenti dell’usabilità {#sep-26-usability}

* **Miglioramenti di usabilità nell&#39;esperienza di simulazione dei contenuti** - La nuova esperienza di simulazione dei contenuti ora consente di denominare e organizzare le varianti per facilitare il confronto, copiare o eliminare i dettagli delle varianti direttamente da ogni scheda, visualizzare i percorsi degli attributi completi e la configurazione del canale per scheda su richiesta e caricare profili CSV, JSON o JSONL personalizzati da un pulsante di caricamento più prominente.


