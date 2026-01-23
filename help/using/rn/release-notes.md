---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Note sulla versione di Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 775811ef33441c3209eaedc6cd3bee8f686190e0
workflow-type: tm+mt
source-wordcount: '2087'
ht-degree: 29%

---

# Note sulla versione {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novità"
>abstract="**Adobe Journey Optimizer** offre continuamente nuove funzioni, miglioramenti a quelle esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese."

[!DNL Adobe Journey Optimizer] segue un modello di distribuzione continua, che consente ad Adobe di fornire nuove funzioni, miglioramenti e correzioni su base continuativa. Questo approccio consente un rollout scalabile e graduale delle funzionalità per garantire prestazioni e stabilità in tutti gli ambienti.

A causa di questo modello, le note sulla versione vengono aggiornate tra le versioni mensili. Per informazioni dettagliate sul ciclo di rilascio e sulle fasi di disponibilità, consulta [Ciclo di rilascio di Journey Optimizer](releases.md).

[!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche sono disponibili nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.

## Note pre-release di gennaio 2026 {#latest-rn}

**Data di rilascio**: mercoledì 27 gennaio 2026

**Le note pre-release riportate di seguito sono soggette a modifica senza preavviso fino alla data di disponibilità della versione**. I collegamenti, le schermate e la documentazione aggiornata vengono pubblicati nelle note sulla versione, alla data di rilascio.

Consulta anche [Note pre-release di Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

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
<p><strong>Nota</strong>: le ore non interattive non sono supportate per le campagne orchestrate.</p>
<p>Precedentemente rilasciata in Disponibilità limitata, questa funzione è ora disponibile per tutti gli ambienti. Con questa versione con disponibilità generale, la funzione ora include la possibilità per il cliente di mettere in coda un’azione della campagna fino al completamento delle Ore non interattive e la possibilità di visualizzare in anteprima la regola delle Ore non interattive.</p>
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
<p><strong>Nota</strong>: la notifica silenziosa non è ancora supportata per le notifiche Web Push.</p>
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
<p>È ora disponibile una nuova funzionalità <strong>Esportazione messaggi</strong> per i canali e-mail e SMS. Questa funzione consente di esportare automaticamente il contenuto dei messaggi inviati in un set di dati Experience Platform dedicato, consentendoti di:</p>
<ul>
<li>Soddisfare i requisiti di conformità alle normative (ad esempio HIPAA)</li>
<li>Archiviare i messaggi per richieste di rimborso legali e richieste di assistenza clienti</li>
<li>Mantieni copie dei contenuti personalizzati inviati a singoli utenti</li>
</ul>
<p>I record vengono conservati nel set di dati di esportazione dei messaggi di AJO per <strong>7 giorni di calendario dall'acquisizione</strong>. Durante questo periodo di conservazione, puoi esportare i dati nel tuo archivio tramite le destinazioni Experience Platform. La funzione è abilitata a livello di configurazione del canale, per fornire un controllo granulare sui messaggi esportati.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent - Creazione di un Percorso</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’agente di creazione percorsi consente agli utenti di Journey Optimizer di creare e configurare percorsi di marketing utilizzando un’interfaccia in linguaggio naturale. Con l’agente di creazione del Percorso, i professionisti possono creare rapidamente i percorsi descrivendo i loro requisiti nei prompt conversazionali. L’agente semplifica la creazione del percorso, consentendo agli addetti al marketing di concentrarsi sulla strategia anziché sulla configurazione tecnica.</p>
<p><a href="https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent#journey-create-agent-skill-overview-and-user-guide" target="_blank">Ulteriori informazioni</a></p>
<p>Data di disponibilità: martedì 12 gennaio 2026</p>
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
<p>Data di disponibilità: giovedì 5 novembre 2025</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti {#jan-26-01-improv}

Di seguito sono elencati i miglioramenti inclusi in questa versione.

#### AI

* **Controlli di qualità dei contenuti dell&#39;Assistente AI** - Oltre all&#39;allineamento del brand, ora puoi valutare la <strong>qualità complessiva dei contenuti</strong> per individuare potenziali problemi di leggibilità, coesione ed efficacia, indipendentemente dalle linee guida del brand. Questi controlli automatizzati consentono di identificare messaggi non chiari, toni incoerenti o lacune strutturali.

* **Aggiorna i marchi con la nuova scheda colore**: le linee guida per i marchi garantiscono che il tuo marchio venga presentato in modo coerente in tutti i punti di contatto. La nuova <strong>sezione Colori</strong> definisce gli standard per il sistema di colori del tuo marchio, delineando il modo in cui i colori vengono selezionati, organizzati e applicati tra le esperienze. Garantisce un uso coerente dei colori primari, secondari, di accento e neutri per supportare un&#39;identità del brand coesa, accessibile e riconoscibile.

#### Campagne

* **Pianifica campagna utilizzando il fuso orario del profilo** - La pianificazione delle campagne può ora utilizzare il <strong>fuso orario</strong> di ciascun profilo per recapitare i messaggi all&#39;ora locale prevista. La pianificazione tramite i fusi orari del profilo è disponibile per i canali E-mail, Push, SMS, WhatsApp e LINE.

  **Nota**: questo miglioramento è disponibile solo per un set di organizzazioni (disponibilità limitata).


#### E-mail Designer

* **Correzioni sul posto nella finestra di progettazione e-mail** - Durante la gestione del contenuto in base alle linee guida del brand, sono ora disponibili <strong>suggerimenti di contenuto automatici basati sull&#39;intelligenza artificiale</strong> quando vengono rilevate violazioni durante la convalida del contenuto. Se il contenuto viene segnalato come non allineato con le linee guida del marchio o non soddisfa i criteri di qualità, il sistema genera in modo proattivo alternative corrette che possono essere riviste e applicate in linea, migliorando la conformità e accelerando la produzione.

#### Experience Decisioning

* **API per strumenti di migrazione self-service** - È disponibile un nuovo set di <strong>API per strumenti di migrazione</strong> per migrare le entità di Gestione offerte in Experience Decisioning. Gli strumenti consentono una migrazione fluida tra sandbox con risoluzione delle dipendenze e funzionalità di rollback.

* **Allega frammenti agli elementi decisionali** - Journey Optimizer ora consente di allegare <strong>frammenti</strong> agli elementi decisionali che possono essere utilizzati nelle campagne di esperienza basate su codice tramite i criteri decisionali.

  **Nota**: rilasciato in precedenza in Disponibilità limitata, questo miglioramento è ora disponibile per tutti gli ambienti (Disponibilità generale).

#### Percorsi

* **Sfrutta un payload di risposta di errore nelle azioni personalizzate del percorso** - Ora puoi definire un <strong>payload di risposta di errore</strong> facoltativo per le azioni personalizzate. Quando una chiamata non riesce, il payload di errore viene esposto nel contesto del percorso ed è disponibile nel ramo timeout/errore per supportare logica di fallback e debug più completi.

* **Combina azioni messaggio native e Adobe Campaign** - Journey Optimizer ora consente di combinare azioni messaggio Adobe Campaign v7/v8 con azioni canale native nello stesso percorso.

* **Convalida dimensioni payload di Percorso in percorsi** - Journey Optimizer fornisce ora <strong>la convalida dimensioni payload</strong> per garantire prestazioni e stabilità del sistema ottimali. Quando crei o pubblichi percorsi, ricevi chiari avvisi ed errori se le dimensioni del payload si avvicinano o superano i limiti consigliati, insieme a indicazioni fruibili per ottimizzare la configurazione del percorso. Questa convalida proattiva consente di identificare tempestivamente i potenziali problemi e di mantenere le prestazioni del percorso.

* **Più azioni in entrata nei percorsi**. Per semplificare l&#39;orchestrazione del percorso, è ora possibile definire <strong>più azioni in entrata</strong> in un singolo percorso. Precedentemente disponibile nelle campagne, questa funzionalità consente di distribuire contemporaneamente verso posizioni diverse più esperienze basate su codice, messaggi in-app, schede di contenuto o azioni web, ciascuna con un contenuto specifico.

  **Nota**: rilasciato in precedenza in Disponibilità limitata, questo miglioramento è ora disponibile per tutti gli ambienti (Disponibilità generale).

#### Campagne orchestrate

* **Selezionare gli attributi e copiare i valori di distribuzione** - È ora possibile selezionare o copiare i valori direttamente dalla visualizzazione Distribuzione dei valori nelle campagne orchestrate.

* **Ereditarietà delle etichette di utilizzo dati per i tipi di pubblico** - <strong>Le etichette di utilizzo dati</strong> applicate in Adobe Experience Platform ora vengono riportate automaticamente durante il salvataggio dei tipi di pubblico in campagne orchestrate, riducendo l&#39;assegnazione manuale di tag DULE.

* **Filtri di retargeting predefiniti** - Per supportare il retargeting più semplice per i casi di utilizzo di campagne orchestrate, questa versione introduce nuovi <strong>filtri di retargeting</strong>. Questi filtri ti consentono di indirizzare direttamente i tipi di pubblico in base al coinvolgimento nei messaggi, ad esempio inviato, aperto o su cui è stato fatto clic, oppure aperto e su cui è stato fatto clic, e selezionare la campagna specifica o in transizione di cui desideri eseguire il retargeting.

* **Filtri predefiniti con parametri** - È ora possibile creare <strong>filtri con parametri</strong> in campagne orchestrate per regole riutilizzabili e modificabili.

* **Conferma del messaggio prima dell&#39;invio** - Un <strong>passaggio di conferma</strong> è ora abilitato per impostazione predefinita prima dell&#39;invio di campagne orchestrate per ridurre gli invii accidentali.

* **Supporto dei metadati generati dall&#39;utente**. La funzione <strong>executionMetadata helper</strong> è ora disponibile nell&#39;editor di personalizzazione per le campagne orchestrate e consente di allegare informazioni contestuali a qualsiasi azione nativa e di memorizzarle in un set di dati per l&#39;esportazione in sistemi esterni.

* **Pulsante di riavvio** - Le campagne orchestrate ora includono un <strong>pulsante di riavvio</strong> che consente di riavviare rapidamente le esecuzioni quando necessario prima di pubblicare la campagna.

* **Supporto per il controllo dei tassi** - Le campagne orchestrate ora supportano il <strong>controllo dei tassi</strong> per aiutarti a pianificare le consegne e allinearsi ai vincoli del volume.

#### Autorizzazioni

* **Impedisci l&#39;autoapprovazione per percorsi e campagne** - È ora possibile richiedere che i creatori non possano approvare i propri percorsi o campagne, migliorando <strong>la separazione dei compiti</strong> nei flussi di lavoro di approvazione.

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
<p>Questa funzionalità sarà disponibile per tutti gli ambienti (disponibilità generale).</p>
<p>Data di disponibilità: mercoledì 3 febbraio 2026</p>
</td>
</tr>
</tbody>
</table>
