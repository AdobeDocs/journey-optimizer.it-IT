---
solution: Journey Optimizer
product: journey optimizer
title: Note pre-release per Journey Optimizer
description: Note pre-release di Adobe Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 3d9316e3a42696c4e944ec23b0300e56b07142c2
workflow-type: tm+mt
source-wordcount: '2342'
ht-degree: 23%

---

# Note pre-release {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nell’ultima settimana di ogni mese, tutte le modifiche vengono consolidate nelle [note sulla versione](release-notes.md).


## Note pre-release di gennaio 2026 {#jan-26-01-rn}

**Le note pre-release riportate di seguito sono soggette a modifica senza preavviso fino alla data di disponibilità della versione**. I collegamenti, le schermate e la documentazione aggiornata vengono pubblicati nelle note sulla versione, alla data di rilascio.

Consulta anche [Note pre-release di Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Data di rilascio**: martedì 26 gennaio 2026

### Nuove funzionalità {#jan-26-01-features}

<table>
<thead>
<tr>
<th><strong>Attività di azione nei percorsi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer supporta una nuova attività <strong>Action</strong> generica che consente di configurare sia le azioni singole che i gruppi di azioni in entrata <strong>con più azioni</strong>, semplificando la configurazione delle azioni nell'area di lavoro del percorso. In particolare, questa nuova funzione consente:</p>
<ul>
<li>una configurazione semplificata dell’azione nativa nell’area di lavoro del percorso;</li>
<li>la capacità di creare gruppi di azioni in entrata con più azioni;</li>
<li>la possibilità di aggiungere l’ottimizzazione a qualsiasi azione del canale incorporata;</li>
<li>la possibilità di aggiungere sia opzioni di sperimentazione che opzioni multilingue a qualsiasi azione.</li>
</ul>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13290">COLLEGAMENTO ALL'ATTIVITÀ DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-111916">COLLEGAMENTO ALL'ATTIVITÀ PRODUCT JIRA</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Monitoraggio delle azioni personalizzato</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Approfondisci insight sullo stato e sulle prestazioni degli endpoint di azione personalizzati con un nuovo <strong>dashboard di monitoraggio</strong> e dati arricchiti dell'evento del passaggio di percorso. Tieni traccia di chiamate, errori, velocità effettiva, tempi di risposta e tempi di attesa delle code per capire rapidamente quando, dove e perché si verificano anomalie.</p>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13981">COLLEGAMENTO ALL'ATTIVITÀ DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-126869">COLLEGAMENTO ALL'ATTIVITÀ PRODUCT JIRA</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Ore di silenzio/Esclusioni basate sul tempo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le ore di pausa consentono di definire <strong>esclusioni basate sul tempo</strong> per i canali e-mail, SMS, push e WhatsApp. Assicura che non vengano inviati messaggi in specifici periodi di tempo, aiutandoti a rispettare le preferenze dei clienti e i requisiti di conformità. Puoi applicare le ore non interattive tramite <strong>set di regole</strong>, che possono essere assegnate a singole azioni in campagne o percorsi per un controllo preciso.</p>
<p>Precedentemente rilasciata in Disponibilità limitata, questa funzione è ora disponibile per tutti gli ambienti. Con questa versione con disponibilità generale, la funzione ora include la possibilità per il cliente di mettere in coda un’azione della campagna fino al completamento delle Ore non interattive e la possibilità di visualizzare in anteprima la regola delle Ore non interattive.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13986">COLLEGAMENTO ALL'ATTIVITÀ DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-63912">COLLEGAMENTO ALL'ATTIVITÀ PRODUCT JIRA</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canale direct mailing in percorsi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Precedentemente limitato alle campagne, il <strong>canale Direct Mail</strong> è ora disponibile nell'<strong>area di lavoro percorsi</strong>, consentendoti di incorporare Direct Mail nei tuoi percorsi. La direct mailing può ora essere utilizzata sia in scenari batch che in scenari di percorso 1:1, con il supporto per la configurazione dell'estrazione dei file e le impostazioni di frequenza basate sul tempo.</p>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13543">COLLEGAMENTO ALL'ATTIVITÀ DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-38399">COLLEGAMENTO ALL'ATTIVITÀ PRODUCT JIRA</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canale notifiche push web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer ora supporta <strong>notifiche Web push</strong>, espandendo il canale push oltre i dispositivi mobili. Puoi inviare facilmente le notifiche ai browser mobili e desktop, per raggiungere i clienti direttamente sui loro dispositivi senza richiedere un’app. Questo miglioramento consente di coinvolgere gli utenti con messaggi tempestivi e personalizzati in tempo reale, sfruttando gli stessi flussi di lavoro di authoring e le stesse funzionalità di targeting già disponibili per le notifiche push dei dispositivi mobili.</p>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13581">COLLEGAMENTO ALL'ATTIVITÀ DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-37866">COLLEGAMENTO ALL'ATTIVITÀ PRODUCT JIRA</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Supporto per le decisioni nei canali push e SMS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile aggiungere <strong>Criteri di decisione</strong> in percorsi e campagne push e SMS. I criteri di decisione sono contenitori per le offerte che sfruttano il motore di Decisione per restituire in modo dinamico il contenuto migliore da consegnare per ogni membro del pubblico.</p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13426">COLLEGAMENTO ALL'ATTIVITÀ DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/DOCAC-13425">COLLEGAMENTO ALL'ATTIVITÀ DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-55817">COLLEGAMENTO ALL'ATTIVITÀ PRODUCT JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-55818">COLLEGAMENTO ALL'ATTIVITÀ PRODUCT JIRA</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canale direct mail nelle campagne orchestrate</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Il canale direct mailing è ora disponibile nelle campagne orchestrate. L'<strong>attività Direct Mail</strong> facilita l'invio di direct mailing all'interno della campagna orchestrata, sia per messaggi occasionali che ricorrenti. Consente di automatizzare il processo di generazione del <strong>file di estrazione</strong> richiesto dai provider di direct mailing. È possibile combinare le attività del canale nell’area di lavoro della campagna orchestrata per creare campagne cross-channel in grado di attivare azioni basate sui dati e sul comportamento della clientela.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13379">COLLEGAMENTO ALL'ATTIVITÀ DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-82584">COLLEGAMENTO ALL'ATTIVITÀ PRODUCT JIRA</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nuovi connettori di origini per le app fedeltà</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>I nuovi <strong>connettori di origine</strong> sono ora disponibili in Adobe Experience Platform per le app fedeltà Talon.One, Capillary e Kobie. Questi connettori consentono di trasferire in streaming i dati relativi alla fedeltà in Adobe Experience Platform e di sfruttarli in Journey Optimizer.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13372">COLLEGA A ATTIVITÀ DOCAC JIRA</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Esportazione messaggio</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile <strong>esportare le consegne inviate</strong> in un set di dati specifico, a scopo di archiviazione e conformità. Questa capacità è disponibile non solo per la posta elettronica, ma anche per altri canali come gli SMS. La conservazione dei dati per il set di dati di esportazione del messaggio è ora <strong>7 giorni</strong>.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-12915">COLLEGAMENTO ALL'ATTIVITÀ DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-105313">COLLEGAMENTO ALL'ATTIVITÀ PRODUCT JIRA</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nuova API per recuperare le campagne Azione</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora disponibile una nuova <strong>API Journey Optimizer</strong> che consente di recuperare ed esaminare a livello di programmazione i dati relativi alla campagna, ad esempio dettagli, versioni e configurazioni.</p>
<p>Per ulteriori informazioni, consulta la <a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/">documentazione dettagliata</a>.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13506">COLLEGAMENTO ALL'ATTIVITÀ DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-96195">COLLEGAMENTO ALL'ATTIVITÀ PRODUCT JIRA</a></p>
<p>Data di disponibilità: martedì 24 novembre 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Avvisi su nuovi percorsi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sono ora disponibili tre nuovi <strong>avvisi di percorso</strong> per aiutarti a monitorare e tenere traccia degli eventi del ciclo di vita del percorso e delle prestazioni delle azioni personalizzate:</p>
<ul>
<li><strong>Percorso pubblicato</strong>: ricevi notifiche quando un percorso viene pubblicato da un professionista nell’area di lavoro del percorso.</li>
<li><strong>Percorso completato</strong>: ricevi avvisi al termine di un percorso, con definizioni specifiche basate sul tipo di percorso (Leggi pubblico o Attivato da eventi).</li>
<li><strong>Limitazione azione personalizzata attivata</strong>: ricevi una notifica quando il limite viene attivato su un endpoint dell’azione personalizzata.</li>
</ul>
<p>È possibile iscriversi a questi avvisi a livello organizzativo o per singoli percorsi.</p>
<p>Per ulteriori informazioni, consulta la <a href="../reports/alerts.md#journey-alerts">documentazione dettagliata</a>.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13465">COLLEGA A ATTIVITÀ DOCAC JIRA</a></p>
<p>Data di disponibilità: giovedì 5 novembre 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Temi in E-mail designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi applicare rapidamente <strong>temi approvati in precedenza</strong> per garantire la coerenza del brand in tutte le e-mail, velocizzare il processo di creazione delle campagne e produrre in modo indipendente e-mail di alta qualità, riducendo al contempo la dipendenza dai team di progettazione.</p>
<p>Precedentemente rilasciata nella versione Beta, questa funzionalità è ora disponibile per un set di organizzazioni (disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<img src="assets/do-not-localize/themes.gif">
<p>Per ulteriori informazioni, consulta la <a href="../email/apply-email-themes.md">documentazione dettagliata</a>.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-12941">COLLEGAMENTO ALL'ATTIVITÀ DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/NEO-88838">COLLEGAMENTO ALL'ATTIVITÀ PRODUCT JIRA</a></p>
<p>Data di disponibilità: giovedì 5 novembre 2025</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti {#jan-26-01-improv}

Di seguito sono elencati i miglioramenti inclusi in questa versione.

#### AI

* **Controlli di qualità dei contenuti dell&#39;Assistente AI** - Oltre all&#39;allineamento del brand, ora puoi valutare la <strong>qualità complessiva dei contenuti</strong> per individuare potenziali problemi di leggibilità, coesione ed efficacia, indipendentemente dalle linee guida del brand. Questi controlli automatizzati consentono di identificare messaggi non chiari, toni incoerenti o lacune strutturali.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13917">COLLEGAMENTO ALL&#39;ATTIVITÀ DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-103238">COLLEGAMENTO ALL&#39;ATTIVITÀ PRODUCT JIRA</a>
* **Aggiorna i marchi con la nuova scheda colore**: le linee guida per i marchi garantiscono che il tuo marchio venga presentato in modo coerente in tutti i punti di contatto. La nuova <strong>sezione Colori</strong> definisce gli standard per il sistema di colori del tuo marchio, delineando il modo in cui i colori vengono selezionati, organizzati e applicati tra le esperienze. Garantisce un uso coerente dei colori primari, secondari, di accento e neutri per supportare un&#39;identità del brand coesa, accessibile e riconoscibile.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13811">COLLEGAMENTO ALL&#39;ATTIVITÀ DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-121183">COLLEGAMENTO ALL&#39;ATTIVITÀ PRODUCT JIRA</a>

#### Campagne

* **Pianifica campagna utilizzando il fuso orario del profilo** - La pianificazione delle campagne può ora utilizzare il <strong>fuso orario</strong> di ciascun profilo per recapitare i messaggi all&#39;ora locale prevista.

  **Nota**: questo miglioramento è disponibile solo per un set di organizzazioni (disponibilità limitata).
  <a href="https://jira.corp.adobe.com/browse/DOCAC-11534">COLLEGAMENTO ALL&#39;ATTIVITÀ DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-43782">COLLEGAMENTO ALL&#39;ATTIVITÀ PRODUCT JIRA</a>

#### Canali

* **Webhook SMS: fase II** - Descrizione da fornire.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13978">COLLEGAMENTO ALL&#39;ATTIVITÀ DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-93914">COLLEGAMENTO ALL&#39;ATTIVITÀ PRODUCT JIRA</a>

* **Offerta di vendita WhatsApp** - Descrizione da fornire.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13669">COLLEGAMENTO ALL&#39;ATTIVITÀ DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-86420">COLLEGAMENTO ALL&#39;ATTIVITÀ PRODUCT JIRA</a>

#### E-mail Designer

* **Correzioni sul posto in E-mail designer** - <strong>Sono ora disponibili suggerimenti di contenuto automatico basati su IA</strong> in E-mail Designer quando vengono rilevate violazioni durante la convalida del contenuto. Se il contenuto viene segnalato come non allineato con le linee guida del marchio o non soddisfa i criteri di qualità, il sistema genera in modo proattivo alternative corrette che possono essere riviste e applicate in linea, migliorando la conformità e accelerando la produzione.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13979">COLLEGAMENTO ALL&#39;ATTIVITÀ DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-95365">COLLEGAMENTO ALL&#39;ATTIVITÀ PRODUCT JIRA</a>

#### Experience Decisioning

* **Arbitrato di Percorso** - È ora possibile utilizzare <strong>formule e modelli di IA</strong> per aumentare automaticamente i punteggi di priorità del percorso in base agli attributi del profilo cliente e ai fattori contestuali, in modo che i clienti entrino nei percorsi più rilevanti.

  **Nota**: questo miglioramento è disponibile solo per un set di organizzazioni (disponibilità limitata).
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13976">COLLEGAMENTO ALL&#39;ATTIVITÀ DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-78932">COLLEGAMENTO ALL&#39;ATTIVITÀ PRODUCT JIRA</a>

* **documentazione degli strumenti sandbox exd - aggiornamento** - Descrizione da fornire.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13596">COLLEGAMENTO ALL&#39;ATTIVITÀ DOCAC JIRA</a>

* **API per strumenti di migrazione self-service** - È disponibile un nuovo set di <strong>API per strumenti di migrazione</strong> per migrare le entità di Gestione offerte in Experience Decisioning. Gli strumenti consentono una migrazione fluida tra sandbox con risoluzione delle dipendenze e funzionalità di rollback.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13837">COLLEGAMENTO ALL&#39;ATTIVITÀ DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-109695">COLLEGAMENTO ALL&#39;ATTIVITÀ PRODUCT JIRA</a>

* **Allega frammenti agli elementi decisionali** - Journey Optimizer ora consente di allegare <strong>frammenti</strong> agli elementi decisionali che possono essere utilizzati nelle campagne di esperienza basate su codice tramite i criteri decisionali.

  **Nota**: rilasciato in precedenza in Disponibilità limitata, questo miglioramento è ora disponibile per tutti gli ambienti (Disponibilità generale).
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13418">COLLEGAMENTO ALL&#39;ATTIVITÀ DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-110282">COLLEGAMENTO ALL&#39;ATTIVITÀ PRODUCT JIRA</a>

#### Percorsi

* **Sfrutta un payload di risposta di errore nelle azioni personalizzate del percorso** - Ora puoi definire un <strong>payload di risposta di errore</strong> facoltativo per le azioni personalizzate. Quando una chiamata non riesce, il payload di errore viene esposto nel contesto del percorso ed è disponibile nel ramo timeout/errore per supportare logica di fallback e debug più completi.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13977">COLLEGAMENTO ALL&#39;ATTIVITÀ DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-113125">COLLEGAMENTO ALL&#39;ATTIVITÀ PRODUCT JIRA</a>

* **Combina azioni messaggio native e Adobe Campaign** - Journey Optimizer ora consente di combinare azioni messaggio Adobe Campaign v7/v8 con azioni canale native nello stesso percorso.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13974">COLLEGAMENTO ALL&#39;ATTIVITÀ DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-113103">COLLEGAMENTO ALL&#39;ATTIVITÀ PRODUCT JIRA</a>

* **Convalida dimensioni payload di Percorso in percorsi** - Journey Optimizer fornisce ora <strong>la convalida dimensioni payload</strong> per garantire prestazioni e stabilità del sistema ottimali. Quando crei o pubblichi percorsi, ricevi chiari avvisi ed errori se le dimensioni del payload si avvicinano o superano i limiti consigliati, insieme a indicazioni fruibili per ottimizzare la configurazione del percorso. Questa convalida proattiva consente di identificare tempestivamente i potenziali problemi e di mantenere le prestazioni del percorso.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13840">COLLEGAMENTO ALL&#39;ATTIVITÀ DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-122236">COLLEGAMENTO ALL&#39;ATTIVITÀ PRODUCT JIRA</a>

* **Più azioni in entrata nei percorsi**. Per semplificare l&#39;orchestrazione del percorso, è ora possibile definire <strong>più azioni in entrata</strong> in un singolo percorso. Precedentemente disponibile nelle campagne, questa funzionalità consente di distribuire contemporaneamente verso posizioni diverse più esperienze basate su codice, messaggi in-app, schede di contenuto o azioni web, ciascuna con un contenuto specifico.

  **Nota**: rilasciato in precedenza in Disponibilità limitata, questo miglioramento è ora disponibile per tutti gli ambienti (Disponibilità generale).
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13453">COLLEGAMENTO ALL&#39;ATTIVITÀ DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-111916">COLLEGAMENTO ALL&#39;ATTIVITÀ PRODUCT JIRA</a>

#### Campagne orchestrate

* **Selezionare gli attributi e copiare i valori di distribuzione** - È ora possibile selezionare o copiare i valori direttamente dalla visualizzazione Distribuzione dei valori nelle campagne orchestrate.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13973">COLLEGAMENTO ALL&#39;ATTIVITÀ DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-105244">COLLEGAMENTO ALL&#39;ATTIVITÀ PRODUCT JIRA</a>

* **Ereditarietà delle etichette di utilizzo dati per i tipi di pubblico** - <strong>Le etichette di utilizzo dati</strong> applicate in Adobe Experience Platform ora vengono riportate automaticamente durante il salvataggio dei tipi di pubblico in campagne orchestrate, riducendo l&#39;assegnazione manuale di tag DULE.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13972">COLLEGAMENTO ALL&#39;ATTIVITÀ DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-120769">COLLEGAMENTO ALL&#39;ATTIVITÀ PRODUCT JIRA</a>

* **Filtri di retargeting predefiniti** - Per supportare il retargeting più semplice per i casi di utilizzo di campagne orchestrate, questa versione introduce nuovi <strong>filtri di retargeting</strong>. Questi filtri ti consentono di indirizzare direttamente i tipi di pubblico in base al coinvolgimento nei messaggi, ad esempio inviato, aperto o su cui è stato fatto clic, oppure aperto e su cui è stato fatto clic, e selezionare la campagna specifica o in transizione di cui desideri eseguire il retargeting.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13971">COLLEGAMENTO ALL&#39;ATTIVITÀ DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-116701">COLLEGAMENTO ALL&#39;ATTIVITÀ PRODUCT JIRA</a>

* **Filtri predefiniti con parametri** - È ora possibile creare <strong>filtri con parametri</strong> in campagne orchestrate per regole riutilizzabili e modificabili.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13970">COLLEGAMENTO ALL&#39;ATTIVITÀ DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-115431">COLLEGAMENTO ALL&#39;ATTIVITÀ PRODUCT JIRA</a>

* **Conferma del messaggio prima dell&#39;invio** - Un <strong>passaggio di conferma</strong> è ora abilitato per impostazione predefinita prima dell&#39;invio di campagne orchestrate per ridurre gli invii accidentali.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13927">COLLEGAMENTO ALL&#39;ATTIVITÀ DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-87219">COLLEGAMENTO ALL&#39;ATTIVITÀ PRODUCT JIRA</a>

* **Supporto dei metadati generati dall&#39;utente**. La funzione <strong>executionMetadata helper</strong> è ora disponibile nell&#39;editor di personalizzazione per le campagne orchestrate e consente di allegare informazioni contestuali a qualsiasi azione nativa e di memorizzarle in un set di dati per l&#39;esportazione in sistemi esterni.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13923">COLLEGAMENTO ALL&#39;ATTIVITÀ DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-112697">COLLEGAMENTO ALL&#39;ATTIVITÀ PRODUCT JIRA</a>

* **Pulsante di riavvio** - Le campagne orchestrate ora includono un <strong>pulsante di riavvio</strong> che consente di riavviare rapidamente le esecuzioni quando necessario prima di pubblicare la campagna.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13920">COLLEGAMENTO ALL&#39;ATTIVITÀ DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-106020">COLLEGAMENTO ALL&#39;ATTIVITÀ PRODUCT JIRA</a>

* **Supporto per il controllo dei tassi** - Le campagne orchestrate ora supportano il <strong>controllo dei tassi</strong> per aiutarti a pianificare le consegne e allinearsi ai vincoli del volume.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13764">COLLEGAMENTO ALL&#39;ATTIVITÀ DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-113254">COLLEGAMENTO ALL&#39;ATTIVITÀ PRODUCT JIRA</a>

#### Autorizzazioni

* **Impedisci l&#39;autoapprovazione per percorsi e campagne** - È ora possibile richiedere che i creatori non possano approvare i propri percorsi o campagne, migliorando <strong>la separazione dei compiti</strong> nei flussi di lavoro di approvazione.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13472">COLLEGAMENTO ALL&#39;ATTIVITÀ DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-99957">COLLEGAMENTO ALL&#39;ATTIVITÀ PRODUCT JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-95676">COLLEGAMENTO ALL&#39;ATTIVITÀ PRODUCT JIRA</a>

## Disponibile a breve {#jan-26-01-coming-soon}

Nei prossimi giorni, saranno rilasciati i seguenti miglioramenti e funzionalità. **Le informazioni sono soggette a modifiche**. I collegamenti, le schermate e la documentazione aggiornati verranno condivisi una volta che tali aggiornamenti saranno disponibili in produzione.

<table>
<thead>
<tr>
<th><strong>Generazione di contenuti in Journey Agent</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con tecnologia Adobe Experience Platform Agent Orchestrator, <strong>Journey Agent</strong> è disponibile in Journey Optimizer e consente di analizzare i percorsi tramite un'interfaccia in linguaggio naturale. Ora puoi anche generare e gestire contenuti specifici per il canale direttamente in Journey Agent, creando contenuti per canali quali e-mail e push, applicando e visualizzando in anteprima modelli, perfezionando tono e stile attraverso i prompt e aprendo contenuti in Content Designer per la modifica nel contesto.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13980">COLLEGAMENTO ALL'ATTIVITÀ DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-111882">COLLEGAMENTO ALL'ATTIVITÀ PRODUCT JIRA</a></p>
<p>Data di disponibilità: martedì 2 febbraio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Attività di decisione sui contenuti</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi includere <strong>offerte personalizzate</strong> nei tuoi percorsi tramite un'attività di decisione Contenuto dedicata nell'area di lavoro del percorso e utilizzarle nelle attività del percorso, incluse condizioni e azioni personalizzate.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-12902">COLLEGAMENTO ALL'ATTIVITÀ DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-99223">COLLEGAMENTO ALL'ATTIVITÀ PRODUCT JIRA</a></p>
<p>Data di disponibilità: martedì 2 febbraio 2026</p>
</td>
</tr>
</tbody>
</table>
