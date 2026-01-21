---
solution: Journey Optimizer
product: journey optimizer
title: Note pre-release per Journey Optimizer
description: Note pre-release di Adobe Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 86bd616a9331c5225c78ccf52c5d26a063fa8654
workflow-type: tm+mt
source-wordcount: '2080'
ht-degree: 31%

---

# Note pre-release {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nell’ultima settimana di ogni mese, tutte le modifiche vengono consolidate nelle [note sulla versione](release-notes.md).


## Gennaio &#39;26 pre-note sulla versione {#jan-26-01-rn}

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
<p>Journey Optimizer supporta una nuova attività<strong> Azione generica </strong>che consente di configurare sia azioni singole che <strong>gruppi di azioni</strong> in ingresso con più azioni, consentendo una configurazione semplificata delle azioni all'interno dell'area di lavoro del percorso. In particolare, questa nuova funzione consente:</p>
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
<p>Ottieni informazione approfondita più approfondite sullo stato e sulle prestazioni dei tuoi endpoint di azione personalizzati con un nuovo <strong>dashboard</strong> di monitoraggio e dati avanzati sugli eventi delle fasi del percorso. Tieni traccia delle chiamate riuscite, degli errori, della velocità effettiva, dei tempi di risposta e dei tempi di attesa coda per capire rapidamente quando, dove e perché si verificano anomalie.</p>
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
<p>Le ore di silenzio consentono di definire <strong>esclusioni</strong> basate sul tempo per i canali e-mail, SMS, push e WhatsApp. Garantiscono che nessun messaggio venga inviato durante specifici periodi di tempo, aiutandoti a rispettare le preferenze dei clienti e i requisiti di conformità. È possibile applicare ore di silenzio attraverso <strong>regola set</strong>, che possono essere assegnati a singole azioni in campagne o percorsi per un controllo preciso.</p>
<p>Precedentemente rilasciata in Disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti. Con questa versione di disponibilità generale, la funzionalità include ora la possibilità per il cliente di coda un'azione della campagna fino al completamento delle ore silenziose e la possibilità di visualizzare in anteprima la regola delle ore silenziose attivate.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canale Direct Mail nei percorsi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Precedentemente limitato alle campagne, il <strong>canale</strong> Direct Mail è ora disponibile nell'area di lavoro<strong> del viaggio, consentendoti di incorporare Direct </strong>Mail nei tuoi percorsi. Direct Mail può ora essere utilizzato sia in batch che in scenari di percorso 1:1, con supporto per la configurazione dell'estrazione dei file e le impostazioni di frequenza basate sul tempo.</p>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canale notifiche push Web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Systems Journey Optimizer ora supporta <strong>le notifiche</strong> push Web, espandendo il canale push oltre i dispositivi mobili. Puoi inviare senza problemi notifiche ai browser sia mobili che desktop, consentendoti di raggiungere i clienti direttamente sui loro dispositivi senza richiedere un'app. Questo miglioramento consente di coinvolgere gli utenti con messaggi tempestivi e personalizzati in tempo reale, sfruttando gli stessi flussi di lavoro di authoring e le stesse funzionalità di targeting già disponibili per le notifiche push dei dispositivi mobili.</p>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Messaggistica di base RCS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con la nuova <strong>offerta di componenti aggiuntivi</strong> RCS Basic, è ora possibile fornire servizi RCS (Rich Communication Services) di base messaggistica si trovano nel Journey Optimizer, consentendo le seguenti funzionalità di messaggistica avanzate soggette al supporto del provider e dell'operatore:</p>
<ul>
<li>Supporto per mittente brandizzato e verificato: invia messaggi utilizzando profili aziendali verificati con elementi di branding (logo, nome del mittente, ecc.).</li>
<li>Informazioni approfondite sulla consegna dei messaggi: puoi ricevere rapporti di consegna dettagliati, inclusi gli aggiornamenti sullo stato del messaggio (ad esempio inviato, consegnato, letto).</li>
<li>Tracciamento dei collegamenti: incorpora e tieni traccia degli URL nei messaggi RCS per l’analisi del coinvolgimento.</li>
<li>Fallback su SMS: fallback automatico su SMS quando il dispositivo del profilo non supporta la RCS o è temporaneamente non raggiungibile tramite RCS.</li>
<li>Composizione di base dei messaggi: invia messaggi RCS di base basati su testo.</li>
</ul>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Supporto decisionale nei canali Push e SMS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi aggiungere <strong>criteri decisionali</strong> nei percorsi e nelle campagne push e SMS. I criteri di decisione sono contenitori per le offerte che sfruttano il motore di Decisione per restituire in modo dinamico il contenuto migliore da consegnare per ogni membro del pubblico.</p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canale di direct mail nelle campagne orchestrate</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Il canale di direct mail è ora disponibile nelle campagne orchestrate. L'attività <strong></strong> di Direct mail facilita l'invio di direct mail all'interno della campagna orchestrata, sia per i messaggi una tantum che per quelli ricorrenti. Serve ad automatizzare il processo di generazione <strong>del file</strong> di estrazione richiesto dai provider di direct mail. È possibile combinare le attività del canale nell’area di lavoro della campagna orchestrata per creare campagne cross-channel in grado di attivare azioni basate sui dati e sul comportamento della clientela.</p>
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
<p>Con Journey Optimizer, ora puoi acquisire <strong>gli attributi del</strong> profilo attraverso le pagine di destinazione. Crea, progetta e gestire <strong>moduli</strong> personalizzati su misura per le tue esigenze basati su un set di dati specifico. Puoi quindi sfruttare questi moduli nelle pagine di destinazione per aggiungere gli attributi di profilo desiderati nel set di dati definito per ciascun modulo.</p>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
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
<p><strong>Nuovo connettori</strong> sorgente sono ora disponibili in Adobe Experience Platform per le app fedeltà Talon.One, Capillary e Kobie. Questi connettori consentono di trasferire in streaming i dati relativi alla fedeltà in Adobe Experience Platform e di sfruttarli in Journey Optimizer.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Esportazione Invia messaggio</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora è possibile <strong>esportare le</strong> consegne inviate in un set di dati specifico, per scopi di archiviazione e conformità. Questa capacità è disponibile non solo per la posta elettronica, ma anche per altri canali come gli SMS. La conservazione dei dati per il set di dati di esportazione dei messaggi è ora <strong>di 7 giorni</strong>.</p>
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
<p>È ora disponibile una nuova <strong>API</strong> Journey Optimizer, che consente di recuperare e ispezionare a livello di codice i dati relativi alla campagna come dettagli, versioni e configurazioni.</p>
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
<p>Sono ora disponibili tre nuovi <strong>avvisi relativi al percorso che consentono di monitorare e tenere traccia degli eventi del ciclo di</strong> vita del viaggio e delle prestazioni delle azioni personalizzate:</p>
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
<p>Ora puoi applicare <strong>rapidamente temi</strong> pre-approvati per garantire la coerenza del brand su tutte le e-mail, accelerare il processo di creazione delle campagne e produrre autonomamente e-mail di alta qualità, riducendo al contempo la dipendenza dai team di progettazione.</p>
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

#### Intelligenza artificiale

* **Controlli** di qualità dei contenuti dell&#39;assistente AI - Oltre all&#39;allineamento marchio, ora puoi valutare la qualità<strong> complessiva </strong>del contenuto per scoprire potenziali problemi con leggibilità, coesione ed efficacia, indipendentemente dalle tue linee guida marchio. Questi controlli automatici aiutano a identificare messaggistica poco chiari, tono incoerente o lacune strutturali.
* **Aggiorna i marchi con nuove scheda** colore: le linee guida del marchio aiutano a garantire che i tuoi marchio siano presentati in modo coerente su tutti i punti di contatto. La nuova <strong>sezione</strong> Colori definisce gli standard per il sistema di colori del tuo marchio, delineando il modo in cui i colori vengono selezionati, organizzati e applicati tra le esperienze. Garantisce un uso coerente di colori primari, secondari, accentati e neutri per supportare un identità del brand coeso, accessibile e riconoscibile.

#### Campagne

* **Pianificare Campaign utilizzando il fuso** orario del profilo: Campaign pianificazione può ora utilizzare il fuso<strong> orario di </strong>ciascun profilo per recapitare i messaggi all&#39;ora locale prevista.

  **Nota**: questo miglioramento è disponibile solo per un gruppo di organizzazioni (disponibilità limitata).

#### Canali

* **Webhook SMS: Fase II** - Descrizione da fornire.

* **Offerta** di rivendita WhatsApp - Descrizione da fornire.

#### E-mail Designer

* **Correzioni sul posto in Email Designer** - <strong>I suggerimenti</strong> di contenuto automatici basati sull&#39;intelligenza artificiale sono ora disponibili in Email Designer quando vengono rilevate violazioni durante contenuto convalida. Se contenuto viene contrassegnato come disallineato con le linee guida marchio o non soddisfa i criteri di qualità, il sistema genera in modo proattivo alternative corrette che possono essere riviste e applicate in linea, migliorando la conformità e accelerando la produzione.

#### Esperienza decisionale

* **Arbitrato** del percorso - Ora puoi utilizzare <strong>formule e modelli</strong> di intelligenza artificiale per aumentare automaticamente i punteggi di priorità del percorso in base agli attributi del profilo del cliente e ai fattori contestuali, garantendo che i clienti inseriscano i percorsi più pertinenti.

  **Nota**: questo miglioramento è disponibile solo per un gruppo di organizzazioni (disponibilità limitata).

* **Documentazione sugli strumenti sandbox EXD - Aggiornamento** - Descrizione da fornire.

* **API** degli strumenti di migrazione self-service: è disponibile un nuovo set di API degli strumenti di migrazione per migrare le entità di gestione dell&#39;offerta <strong></strong> a Experience Decisioning. Gli strumenti consentono una migrazione senza soluzione di continuità tra le sandbox con risoluzione delle dipendenze e funzionalità di rollback.

* **Allegare frammenti agli elementi decisionali** - Journey Optimizer offre ora la possibilità di allegare <strong>frammenti</strong> agli elementi decisionali che possono essere sfruttati nelle campagne di esperienza basate su codice tramite criteri decisionali.

  **Nota**: precedentemente rilasciato in Disponibilità limitata, questo miglioramento è ora disponibile per tutti gli ambienti (Disponibilità generale).

#### Percorsi

* **Sfrutta un payload di risposta di errore nel percorso Azioni** personalizzate: ora è possibile definire un payload<strong> facoltativo </strong>di risposta di errore per le azioni personalizzate. Quando una chiamata non riesce, il payload di errore viene esposto nel contesto del percorso ed è disponibile nel ramo timeout/errore per supportare una logica di fallback e un debug più avanzati.

* **Combinare azioni** di messaggi nativo e Adobe Campaign - Journey Optimizer ora ti consente di combinare le azioni dei messaggi Adobe Campaign v7/v8 con le azioni del canale nativo nello stesso percorso.

* **Dimensioni del carico utile del viaggio convalida nei percorsi** - Journey Optimizer ora fornisce <strong>convalida</strong> delle dimensioni del carico utile per garantire prestazioni ottimali e stabilità del sistema. Quando crei o pubblichi percorsi, ricevi avvisi ed errori chiari se le dimensioni del carico utile si avvicinano o superano i limiti consigliati, insieme a indicazioni utili per ottimizzare la configurazione del percorso. Questo convalida proattivo ti aiuta a identificare tempestivamente potenziali problemi e a mantenere le prestazioni del percorso.

* **Più azioni in entrata nei percorsi: per semplificare l&#39;orchestrazione** del percorso, è ora possibile definire <strong>più azioni</strong> in entrata in un unico percorso. Precedentemente disponibile nelle campagne, questa funzionalità consente di distribuire contemporaneamente verso posizioni diverse più esperienze basate su codice, messaggi in-app, schede di contenuto o azioni web, ciascuna con un contenuto specifico.

  **Nota**: precedentemente rilasciato in Disponibilità limitata, questo miglioramento è ora disponibile per tutti gli ambienti (Disponibilità generale).

#### Campagne orchestrate

* **Selezionare gli attributi e copiare i valori** di distribuzione: ora è possibile selezionare o copiare i valori direttamente dalla visualizzazione della distribuzione dei valori nelle campagne orchestrate.

* **Ereditarietà delle etichette di utilizzo dei dati per i tipi di pubblico:** le<strong> etichette</strong> di utilizzo dei dati applicate in Adobe Experience Platform ora vengono trasferite automaticamente quando si salvano le audience nelle campagne orchestrate, riducendo il assegnazione tag DULE manuale.

* **Filtri** di retargeting predefiniti: per facilitare il retargeting per i casi d&#39;uso delle campagne orchestrate, questa versione introduce nuovi <strong>filtri</strong> di retargeting. Questi filtri ti consentono di destinazione direttamente i tipi di pubblico in base al coinvolgimento del messaggio, ad esempio inviato, aperto solo, aperto o cliccato o aperto e cliccato e selezionare la campagna specifica o la campagna in-transizione di cui desideri eseguire il retargeting.

* **Filtri predefiniti con parametri** : è ora possibile creare <strong>filtri con parametri</strong> in campagne orchestrate per regole riutilizzabili e modificabili.

* **Invia messaggio conferma prima dell&#39;invio** - Un <strong>passaggio</strong> di conferma è ora abilitato per impostazione predefinita prima dell&#39;invio di campagne orchestrate per ridurre gli invii accidentali.

* **Supporto** metadati generato dall&#39;utente - La <strong>funzione</strong> di supporto executionMetadata è ora disponibile nel editor personalizzazione per campagne orchestrate, consentendo di allegare informazioni contestuali a qualsiasi azione nativo e di store in un set di dati per l&#39;esportazione in sistemi esterni.

* **Riavvia pulsante** - Le campagne orchestrate ora includono un <strong>pulsante</strong> di riavvio in modo da poter rapidamente lanciare le esecuzioni quando necessario prima di pubblicare la campagna.

* **Supporto per il controllo** delle tariffe - Le campagne orchestrate ora supportano <strong>il controllo</strong> delle tariffe per aiutarti a velocizzare le consegne e allinearti ai vincoli di volume.

#### Autorizzazioni

* **Impedisci l&#39;autoapprovazione per percorsi e campagne** : ora puoi richiedere che i creator non possano approvare i propri percorsi o campagne, migliorando <strong>la separazione dei compiti</strong> nei flussi di lavoro di approvazione.

## Disponibile a breve {#jan-26-01-coming-soon}

Nei prossimi giorni, saranno rilasciati i seguenti miglioramenti e funzionalità. **Le informazioni sono soggette a modifiche**. I collegamenti, le schermate e la documentazione aggiornati verranno condivisi una volta che tali aggiornamenti saranno disponibili in produzione.

<table>
<thead>
<tr>
<th><strong>Generazione di contenuti all'interno di Journey Agent</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Basato su Adobe Experience Platform Agent Orchestrator, <strong>Journey Agent</strong> è disponibile in Journey Optimizer e consente di analizzare i percorsi attraverso un'interfaccia in linguaggio naturale. Ora puoi anche generare e gestire contenuto specifici del canale direttamente in Journey Agent, creando contenuto per canali come e-mail e push, applicando e visualizzando in anteprima i modelli, perfezionando il tono e lo stile tramite prompt e aprendo contenuto in Content Designer per la modifica in contesto.</p>
<p>Data di disponibilità: martedì 2 febbraio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Attività decisionale sui contenuti</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi includere <strong>offerte</strong> personalizzate nei tuoi percorsi attraverso un'attività decisionale dedicata ai contenuti nell'area di lavoro del percorso e usarle nelle attività del percorso, incluse condizioni e azioni personalizzate.</p>
<p>Data di disponibilità: martedì 2 febbraio 2026</p>
</td>
</tr>
</tbody>
</table>
