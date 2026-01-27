---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Note sulla versione di Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 33bb27ff4181e196d05f320c5b958628a6bd6bf6
workflow-type: tm+mt
source-wordcount: '1707'
ht-degree: 17%

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
<th><strong>Ore non interattive (esclusioni basate sul tempo)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le ore di pausa consentono di definire <strong>esclusioni basate sul tempo</strong> per i canali e-mail, SMS, push e WhatsApp. Assicura che non vengano inviati messaggi in periodi specifici, aiutandoti a rispettare le preferenze dei clienti e i requisiti di conformità. Puoi applicare le ore non interattive tramite <strong>set di regole</strong>, che possono essere assegnate a singole azioni in campagne o percorsi per un controllo preciso.</p>
<p>Precedentemente rilasciata in Disponibilità limitata, questa funzione è ora disponibile per tutti gli ambienti (Disponibilità generale). Con questa versione con disponibilità generale, la funzione ora include la possibilità per i clienti di mettere in coda un’azione della campagna fino al completamento delle Ore non interattive e la possibilità di visualizzare in anteprima la regola delle Ore non interattive.</p>
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
<p>Adobe Journey Optimizer ora supporta <strong>notifiche Web push</strong>, espandendo il canale push oltre i dispositivi mobili. Puoi inviare notifiche sia ai browser mobili che a quelli desktop, per raggiungere i clienti direttamente sui loro dispositivi senza richiedere un’app. Questo miglioramento consente di coinvolgere gli utenti con messaggi tempestivi e personalizzati in tempo reale, sfruttando gli stessi flussi di lavoro di authoring e le stesse funzionalità di targeting già disponibili per il push mobile.</p>
<p>Precedentemente rilasciata in versione Beta, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
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
<p>Precedentemente limitato alle campagne, il <strong>canale direct mailing</strong> è ora disponibile nell'area di lavoro del percorso e consente di incorporare Direct mailing nei percorsi. La direct mailing può ora essere utilizzata sia in scenari batch che in scenari di percorso 1:1, con il supporto per la configurazione dell'estrazione dei file e le impostazioni di frequenza basate sul tempo.</p>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canale direct mailing in campagne orchestrate</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Il canale direct mailing è ora disponibile nelle campagne orchestrate. L'<strong>attività Direct Mail</strong> facilita l'invio di direct mailing all'interno della campagna orchestrata sia per messaggi occasionali che ricorrenti. Automatizza la generazione del <strong>file di estrazione</strong> richiesto dai provider di direct mailing. Puoi combinare le attività del canale nell’area di lavoro della campagna orchestrata per creare campagne cross-channel che attivano azioni basate sul comportamento dei clienti e sui dati.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Supporto per le decisioni nel canale SMS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile aggiungere <strong>Criteri di decisione</strong> ai percorsi e alle campagne SMS. I criteri di decisione sono contenitori per le offerte che sfruttano il motore di Decisione per restituire in modo dinamico il contenuto migliore da consegnare per ogni membro del pubblico.</p>
<p>Questa funzionalità è disponibile in Disponibilità limitata per un set di organizzazioni. Contatta il tuo rappresentante Adobe.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>API per strumenti di migrazione self-service</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Le API per strumenti di migrazione</strong> sono ora disponibili per migrare a livello di programmazione le entità di gestione delle decisioni in Decisioning, con:</p>
<ul>
<li>Ambiti di migrazione flessibili (livello sandbox, offerta o decisione)</li>
<li>Analisi e convalida delle dipendenze automatizzate</li>
<li>Supporto del rollback per le migrazioni completate</li>
<li>Rapporti dettagliati sulla migrazione con mappature oggetto</li>
</ul>
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
<th><strong>Journey Agent - Creazione di un Percorso</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Agent ora offre funzionalità di creazione che consentono agli utenti di Journey Optimizer di creare e configurare percorsi di marketing tramite un'interfaccia <strong>in linguaggio naturale</strong>. I professionisti possono creare rapidamente percorsi descrivendo i propri requisiti nei prompt conversazionali. Ciò semplifica il processo di creazione del percorso, consentendo agli addetti al marketing di concentrarsi sulla strategia anziché sulla configurazione tecnica.</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti {#jan-26-01-improv}

Di seguito sono elencati i miglioramenti inclusi in questa versione.

#### AI

* **Controlli di qualità dei contenuti dell&#39;Assistente AI** - Oltre all&#39;allineamento del brand, ora puoi valutare la <strong>qualità complessiva dei contenuti</strong> per individuare potenziali problemi di leggibilità, coesione ed efficacia, indipendentemente dalle linee guida del brand. Questi controlli automatizzati consentono di identificare messaggi non chiari, toni incoerenti o lacune strutturali.

* **Aggiorna i marchi con la nuova scheda colore**: le linee guida per i marchi garantiscono che il tuo marchio venga presentato in modo coerente in tutti i punti di contatto. La nuova <strong>sezione Colori</strong> definisce gli standard per il sistema di colori del tuo marchio, delineando il modo in cui i colori vengono selezionati, organizzati e applicati tra le esperienze. Garantisce un uso coerente dei colori primari, secondari, di accento e neutri per supportare un&#39;identità del brand coesa, accessibile e riconoscibile.

#### Canali

* **Hook Web SMS** - <strong>Gli hook Web</strong> sono ora supportati in tutti i provider SMS. Puoi configurare ogni web hook in base allo scopo previsto: i web hook in entrata per acquisire i messaggi in entrata e i web hook di feedback per ricevere le conferme di consegna, gli aggiornamenti di stato e altri eventi relativi ai messaggi.

#### Campagne

* **Pianifica campagna utilizzando il fuso orario del profilo** - La pianificazione delle campagne può ora utilizzare il <strong>fuso orario</strong> di ciascun profilo per recapitare i messaggi all&#39;ora locale prevista.

  **Nota**: questo miglioramento è disponibile solo per un set di organizzazioni (disponibilità limitata).


#### Experience Decisioning

* **Allega frammenti agli elementi decisionali** - Journey Optimizer ora consente di allegare <strong>frammenti</strong> agli elementi decisionali, che possono essere utilizzati nelle campagne di esperienza basate su codice tramite i criteri decisionali.

  **Nota**: rilasciato in precedenza in Disponibilità limitata, questo miglioramento è ora disponibile per tutti gli ambienti (Disponibilità generale).

#### Percorsi

* **Sfrutta un payload di risposta di errore nelle azioni personalizzate del percorso** - Ora puoi definire un <strong>payload di risposta di errore</strong> facoltativo per le azioni personalizzate. Quando una chiamata non riesce, il payload di errore viene esposto nel contesto del percorso ed è disponibile nel ramo timeout/errore, insieme a `jo_status_code`, per supportare logica di fallback e debug più completi.

* **Combina azioni messaggio native e Adobe Campaign** - Journey Optimizer ora consente di combinare azioni messaggio Adobe Campaign v7/v8 con azioni canale native nello stesso percorso.

* **Convalida delle dimensioni del payload di Percorso in percorsi** - Journey Optimizer ora convalida le dimensioni del payload di percorso per garantire prestazioni e stabilità ottimali. Quando crei o pubblichi percorsi, ricevi chiari avvisi ed errori se le dimensioni del payload si avvicinano o superano i limiti consigliati, insieme a indicazioni fruibili per ottimizzare la configurazione del percorso. Questa convalida proattiva consente di identificare tempestivamente i potenziali problemi e di mantenere le prestazioni del percorso.

#### Campagne orchestrate

* **Selezionare gli attributi e copiare i valori di distribuzione** - È ora possibile selezionare o copiare i valori direttamente dalla visualizzazione Distribuzione dei valori nelle campagne orchestrate.

* **Ereditarietà delle etichette di utilizzo dei dati per i tipi di pubblico** - Le etichette applicate in Adobe Experience Platform ora vengono riportate automaticamente durante il salvataggio dei tipi di pubblico in campagne orchestrate, riducendo l&#39;assegnazione manuale di tag DULE.

* **Filtri di retargeting predefiniti** - Per supportare il retargeting più semplice per i casi di utilizzo di campagne orchestrate, questa versione introduce nuovi <strong>filtri di feedback campagna</strong>. Questi filtri ti consentono di indirizzare direttamente i tipi di pubblico in base al coinvolgimento nei messaggi, ad esempio inviato, aperto o su cui è stato fatto clic, oppure aperto e su cui è stato fatto clic, e selezionare la campagna specifica o in transizione di cui desideri eseguire il retargeting.

* **Filtri predefiniti con parametri** - È ora possibile creare filtri predefiniti con <strong>parametri</strong> in campagne orchestrate per regole riutilizzabili e modificabili.

* **Conferma del messaggio prima dell&#39;invio** - Un <strong>passaggio di conferma</strong> è ora abilitato per impostazione predefinita prima dell&#39;invio di campagne orchestrate per ridurre gli invii accidentali.

* **Supporto metadati generato dall&#39;utente**. La funzione helper <strong>executeMetadata</strong> è ora disponibile nell&#39;editor di personalizzazione per le campagne orchestrate, consentendo di allegare informazioni contestuali a qualsiasi azione nativa e di memorizzarle in un set di dati per l&#39;esportazione in sistemi esterni.

* **Pulsante di riavvio** - Le campagne orchestrate ora includono un <strong>pulsante di riavvio</strong> che consente di riavviare rapidamente le esecuzioni quando necessario prima di pubblicare la campagna.

* **Supporto per il controllo dei tassi** - Le campagne orchestrate ora supportano il <strong>controllo dei tassi</strong> per aiutarti a pianificare le consegne e allinearsi ai vincoli del volume.

#### Autorizzazioni

* **Impedisci l&#39;autoapprovazione per percorsi e campagne** - È stata aggiunta un&#39;opzione durante la creazione o l&#39;impostazione dei criteri di approvazione per impedire ai creatori di percorsi o campagne di approvare i propri oggetti.

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
<p>Con tecnologia Adobe Experience Platform Agent Orchestrator, <strong>Journey Agent</strong> è disponibile in Journey Optimizer e consente di analizzare i percorsi tramite un'interfaccia in linguaggio naturale. Ora puoi generare e gestire contenuti specifici per il canale direttamente in Journey Agent, creando contenuti per canali quali e-mail e push, applicando e visualizzando in anteprima modelli, perfezionando tono e stile tramite prompt e aprendo contenuti in <strong>Content Designer</strong> per la modifica nel contesto.</p>
<p>Data di disponibilità: martedì 2 febbraio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Supporto per le decisioni nel canale push</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi personalizzare e ottimizzare il contenuto dei messaggi push con <strong>Decisioning</strong>. Utilizza <strong>Punteggi di priorità</strong>, Formule o Modelli di intelligenza artificiale per mostrare il contenuto migliore ai tuoi clienti.</p>
<p>Data di disponibilità: mercoledì 3 febbraio 2026</p>
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
<p>I record vengono conservati nel set di dati di esportazione dei messaggi di AJO per 7 giorni di calendario dall’acquisizione. Durante questo periodo di conservazione, puoi esportare i dati nel tuo archivio tramite le destinazioni Experience Platform. La funzione è abilitata a livello di configurazione del canale, per fornire un controllo granulare sui messaggi esportati.</p>
<p>Questa funzionalità è disponibile solo per il canale e-mail e SMS, per le organizzazioni che hanno acquistato l’offerta del componente aggiuntivo Esportazione messaggi. Per ulteriori informazioni, contatta il tuo rappresentante Adobe.</p>
<p>Data di disponibilità: giovedì 28 gennaio 2026</p>
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
<p>Una nuova <strong>attività Content Decision</strong> è ora disponibile nell'area di lavoro del percorso per l'integrazione di offerte personalizzate direttamente nei percorsi di clienti. Questa attività ti consente di fornire contenuti basati su decisioni e di fare riferimento a tali offerte in tutto il percorso, in condizioni per la creazione di diramazioni basate sull’idoneità, in azioni personalizzate per la trasmissione dei dati delle offerte a sistemi esterni e in altre attività per la creazione di esperienze cliente completamente personalizzate.</p>
<p>Questa funzionalità sarà disponibile per tutti gli ambienti (disponibilità generale).</p>
<p>Data di disponibilità: mercoledì 3 febbraio 2026</p>
</td>
</tr>
</tbody>
</table>
