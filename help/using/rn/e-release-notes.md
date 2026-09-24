---
solution: Journey Optimizer
product: journey optimizer
title: Note pre-release per Journey Optimizer
description: Note pre-release di Adobe Journey Optimizer
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
source-git-commit: 8a0943c7362859a4431f35b6b6163b2d947fff43
workflow-type: tm+mt
source-wordcount: '1874'
ht-degree: 10%
---

# Note pre-release {#e-release-notes}

Adobe Journey Optimizer offre continuamente nuove funzioni, miglioramenti a quelle esistenti e correzioni di bug. Nell’ultima settimana di ogni mese, tutte le modifiche vengono consolidate nelle [note sulla versione](release-notes.md).

## Note pre-release di settembre 2026 {#sep-26-rn}

**Le note pre-release riportate di seguito sono soggette a modifica senza preavviso fino alla data di disponibilità della versione**. I collegamenti, le schermate e la documentazione aggiornata vengono pubblicati una volta che le modifiche saranno disponibili in produzione. Anche se la maggior parte delle modifiche viene consegnata alla data di rilascio, alcune potrebbero essere implementate in un secondo momento. Per ulteriori informazioni, fai riferimento alla data di disponibilità elencata per ciascuna voce.

Consulta anche [Note pre-release di Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Data di rilascio**: 22-23 settembre 2026

>[!BEGINSHADEBOX]

**Novità di CX Enterprise Coworker questo mese**

Questa versione include diverse funzionalità e abilità [Collaboratore](../start/ai-features.md#cx-coworker) nuove e migliorate, elencate qui per la visibilità. Ognuna di esse è descritta anche nella sezione pertinente riportata di seguito.

* [Plug-in per contenuto canale CE](#sep-26-content-management): nuovo plug-in che riunisce in Coworker le competenze relative a copia, immagine ed e-mail di Campaign, dalla descrizione della campagna alla copia pronta per la produzione e a HTML.
* [Abilità per consigli sulla fedeltà](#sep-26-loyalty) - Richiedi opportunità di verifica direttamente nell&#39;interfaccia conversazionale di Coworker e trasformale in una sfida dal vivo senza uscire dalla chat.
* [Simulazione Percorso](#sep-26-journeys) - Automatizza la convalida del percorso end-to-end e interpreta i risultati direttamente in Coworker.
* Creazione di [Percorsi dalla barra di Coworker](#sep-26-journeys): genera percorsi con IA direttamente dalla barra di Coworker a destra, sostituendo la precedente esperienza di Assistente IA.
* [Confronta versioni di percorso](#sep-26-journeys) - Ottieni un diff strutturato e a piena fedeltà tra due versioni di un percorso tramite Chat con collaboratori.
* [Abilità di analisi dell&#39;igiene](#sep-26-journeys) - Analizza i percorsi attivi e in bozza per individuare configurazioni non funzionanti, errori silenziosi e risorse inutilizzate o in declino, con correzioni consigliate.
* [Competenza nell&#39;analisi delle prestazioni aziendali](#sep-26-journeys) - Analizza le prestazioni del percorso e ottieni consigli concreti sull&#39;ottimizzazione direttamente dalla chat.

>[!ENDSHADEBOX]

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

* **Sfide del dominio nell&#39;editor di personalizzazione della scheda di contenuto** - L&#39;editor di personalizzazione della scheda di contenuto ora supporta **Sfide** come dominio, consentendo l&#39;accesso ai metadati della richiesta di verifica durante l&#39;authoring della personalizzazione della scheda di contenuto. In questo modo è più facile creare contenuti personalizzati per ogni fase di una sfida, ovvero lancio, in corso e fine, senza codice personalizzato.

<!--
### Onboarding {#sep-26-onboarding}

The following capability is coming to onboarding in this release.

<table>
<thead>
<tr>
<th><strong>Guided capabilities for onboarding emails and journeys (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Transitioning to Adobe Journey Optimizer from another marketing platform is easier with guided capabilities that help you move existing email content and journeys into Journey Optimizer. A <strong>dedicated workspace</strong> lets you reuse what you have instead of rebuilding from scratch.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
</td>
</tr>
</tbody>
</table>

-->

### Percorsi {#sep-26-journeys}

In questa versione sono stati aggiunti i miglioramenti e le funzioni seguenti ai percorsi.

<table>
<thead>
<tr>
<th><strong>Creazione di percorsi dalla barra di Collaboratore</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La creazione di <strong>Percorsi con IA</strong> è ora disponibile direttamente dalla barra laterale destra di Coworker, sostituendo la precedente esperienza di AI Assistant con un punto di ingresso integrato e modificato per la generazione di percorsi.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Schede di consigli AI per gli avvisi di percorso</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Nella home page di Journey Optimizer viene ora visualizzata una <strong>scheda di consigli AI</strong> quando viene attivato un avviso di percorso che copre <strong>l'errore di un'azione personalizzata di Percorso</strong> e <strong>gli avvisi di Percorso per anomalie</strong>. Selezionando la scheda si apre il percorso con la barra destra precompilata con l’analisi già eseguita.</p>
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
</td>
</tr>
</tbody>
</table>

* **Supporto Jump per i percorsi di qualificazione del pubblico** - I Percorsi che iniziano con **Qualificazione del pubblico** possono ora utilizzare un&#39;attività **Jump** per accedere a un percorso iniziale basato su eventi; il passaggio a un percorso basato su Qualificazione del pubblico non è supportato.

* **Confrontare le versioni di percorso con Coworker** - Oggi, la revisione di ciò che è cambiato tra due versioni di un percorso richiede il confronto manuale all&#39;interno di Journey Optimizer nodo per nodo - non esiste una differenza strutturata, il che rende i controlli di revisione delle modifiche, audit e pre-pubblicazione lenti e soggetti a errori, soprattutto quando i percorsi diventano più complessi. Questa funzionalità consente a un cliente o a un agente di IA di confrontare due versioni qualsiasi di un percorso tramite Chat di Coworker e di recuperare una **differenze strutturate**, ovvero nodi aggiunti/rimossi/modificati/spostati con dettagli a livello di campo, connessioni modificate, modifiche alle proprietà a livello di percorso e conteggi di rollup, senza aprire Journey Optimizer.

* **Eventi di passaggio ridotti per le attività attendi ed eventi** - Gli eventi di passaggio non vengono più generati per le attività **attendi** e **evento** quando il profilo non è stato effettivamente elaborato in tale attività. <!-- DRAFT: pending DOCAC sub-task under DOCAC-15691, see CJM-165835 -->
<!-- Documentation link: TBD -->

* **Eliminazione step-event esecuzione di prova per rapporti personalizzati** - Nell&#39;ambito dell&#39;ottimizzazione step-event, Journey Optimizer ora interrompe la generazione di alcuni eventi di passaggio non segnalabili durante le esecuzioni di Percorso. Questo influisce solo sui rapporti personalizzati basati su questi tipi di eventi step a esecuzione ininterrotta. Se siete interessati, riattivate l&#39;esecuzione di prova per rigenerare i dati.

* **Abilità di Coworker per analisi dell&#39;igiene** - Una nuova abilità di analisi dell&#39;igiene in Coworker analizza i percorsi attivi e di bozza per individuare configurazioni non funzionanti, errori silenziosi e risorse inutilizzate o in declino, ad esempio percorsi di bozza non aggiornati, origini dati orfane ed errori persistenti di azioni personalizzate, e visualizza le correzioni consigliate direttamente dalla chat. <!-- Documentation link: TBD -->

* **Competenza di Coworker per l&#39;analisi delle prestazioni aziendali** - Una nuova abilità di **Analisi delle prestazioni aziendali** in Coworker analizza le prestazioni dei percorsi, spiega le aree di prestazioni inferiori e consiglia ottimizzazioni concrete, come attese di ricoinvolgimento, escalation dei canali e ottimizzazione del tempo di invio.  <!-- Documentation link: TBD -->

* **Timeout del ripristino automatico degli eventi nelle proprietà del Percorso** - Le proprietà del Percorso ora includono un&#39;impostazione **Imposta timeout ripristino evento**: per impostazione predefinita, gli eventi di percorso interessati vengono riprodotti automaticamente fino a 72 ore dopo un&#39;interruzione del servizio senza che sia necessaria alcuna azione. È possibile attivare questa impostazione per controllare la finestra di ripetizione (0-72 ore) per i percorsi sensibili al tempo. Anche il campo **Timeout o errore** esistente è stato rinominato in **Azione personalizzata/Timeout azione IDS** per evitare confusione tra le due impostazioni.

### Canali {#sep-26-channels}

In questa versione sono disponibili le seguenti funzionalità e miglioramenti per i canali.

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
</td>
</tr>
</tbody>
</table>

* **Direct mailing - Dividi automaticamente i file di grandi dimensioni** - I file Direct mailing ora possono essere suddivisi in più parti automaticamente quando superano i 20 GB circa, oppure manualmente scegliendo una dimensione di file di destinazione nella configurazione di indirizzamento dei file.

* **Direct mailing - Limite di pubblico aumentato** - Il limite di pubblico del canale Direct mailing è stato aumentato da 3 milioni a 100 milioni di profili, consentendoti di rivolgerti a un pubblico molto più ampio senza riscontrare errori di creazione dei file.

### Canale e-mail {#sep-26-email-channel}

In questa versione, il canale e-mail sarà arricchito dalle seguenti funzionalità.

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
</td>
</tr>
</tbody>
</table>

* **Sostituzione elenco di soppressione a livello di azione e-mail** - Journey Optimizer ora consente di sovrascrivere il comportamento dell&#39;elenco di soppressione direttamente a livello di azione e-mail in percorsi e campagne. Questo offre ai team maggiore flessibilità per le comunicazioni operative o per le comunicazioni critiche in termini di conformità che richiedono una configurazione di invio dedicata, preservando al contempo i controlli degli elenchi di soppressione globali esistenti per tutti gli altri invii. Questo miglioramento consente alle organizzazioni di gestire gli scenari di eccezione con precisione senza modificare il proprio modello di governance di eliminazione più ampio.

* **Convalida della sintassi URL nell&#39;authoring delle e-mail** - Journey Optimizer ora convalida gli URL in una fase precedente del flusso e fornisce indicazioni più chiare quando viene rilevata una sintassi non valida. In questo modo gli autori possono individuare i problemi prima della finalizzazione, ridurre gli errori di pubblicazione e migliorare l’affidabilità della consegna.

### E-mail designer {#sep-26-email-designer}

In questa versione, e-mail Designer presenta le seguenti funzionalità e miglioramenti.

<table>
<thead>
<tr>
<th><strong>Supporto della modalità scura per le varianti del tema e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>I temi e-mail ora supportano la modalità scura, in modo che ogni variante di colore possa essere riprodotta con un aspetto personalizzato per i destinatari che visualizzano il messaggio e-mail in un client abilitato alla modalità scura.</p>
<p>Quando questa opzione è attivata, viene generata automaticamente una tavolozza scura predefinita per ogni variante e puoi personalizzarla ulteriormente con una tavolozza diversa o con colori personalizzati, indipendentemente dalla progettazione della modalità chiara, in modo che le modifiche apportate in una modalità non influiscano sull'altra.</p>
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
</td>
</tr>
</tbody>
</table>

* **Tipi di carattere di fallback per i tipi di carattere personalizzati nei temi e-mail** - È ora possibile definire un tipo di carattere di fallback per qualsiasi tipo di carattere personalizzato (Web) applicato tramite i temi e-mail. Se il client e-mail di un abbonato non supporta il font personalizzato, Adobe Journey Optimizer visualizza automaticamente il font di fallback specificato invece di lasciare la scelta sul font predefinito del client e-mail. In questo modo la tipografia delle e-mail è più vicina alle linee guida del brand e riduce le incoerenze nel rendering dei font tra i client e-mail.

### Campagne orchestrate {#sep-26-oc}

In questa versione sono state aggiunte alle campagne orchestrate le funzioni e i miglioramenti seguenti.


* **API di monitoraggio per nuove campagne orchestrate** - Sono ora disponibili nuove **specifiche API** per le campagne orchestrate, che consentono di creare, gestire e attivare in modo programmatico campagne orchestrate, consentendo una maggiore integrazione con sistemi esterni e pipeline di automazione.


### Miglioramenti dell’usabilità {#sep-26-usability}

* **Miglioramenti di usabilità nell&#39;esperienza di simulazione dei contenuti** - La nuova esperienza di simulazione dei contenuti ora consente di denominare e organizzare le varianti per facilitare il confronto, copiare o eliminare i dettagli delle varianti direttamente da ogni scheda, visualizzare i percorsi degli attributi completi e la configurazione del canale per scheda su richiesta e caricare profili CSV, JSON o JSONL personalizzati da un pulsante di caricamento più prominente.

* **Calendario unificato per campagne, Percorsi e campagne orchestrate** - La visualizzazione calendario per percorsi e campagne ora si sposta da inventari separati in un menu unificato accessibile dalla barra a sinistra che mostra entrambi in un&#39;unica visualizzazione combinata.

