---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Note sulla versione di Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 65d9eddd6ca99046cb711be80fe3eaa4791b14ad
workflow-type: tm+mt
source-wordcount: '2991'
ht-degree: 28%

---

# Note sulla versione {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novità"
>abstract="**Adobe Journey Optimizer** offre continuamente nuove funzioni, miglioramenti a quelle esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese."

[!DNL Adobe Journey Optimizer] segue un modello di distribuzione continua, che consente ad Adobe di fornire nuove funzioni, miglioramenti e correzioni su base continuativa. Questo approccio consente un rollout scalabile e graduale delle funzionalità per garantire prestazioni e stabilità in tutti gli ambienti.

A causa di questo modello, le note sulla versione vengono aggiornate prima del successivo rilascio mensile. Per informazioni dettagliate sul ciclo di rilascio e sulle fasi di disponibilità, consulta [Ciclo di rilascio di Journey Optimizer](releases.md).

[!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche sono disponibili nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.

## Note pre-release del 26 marzo {#march-26-rn}

**Le note pre-release riportate di seguito sono soggette a modifica senza preavviso fino alla data di disponibilità della versione**. I collegamenti, le schermate e la documentazione aggiornata vengono pubblicati nelle note sulla versione, alla data di rilascio.

Consulta anche [Note sulla versione preliminare di Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Data di rilascio**: 24-25 marzo 2026

### Nuove funzionalità {#march-26-features}



<table>
<thead>
<tr>
<th><strong>Messaggi transazionali nelle campagne orchestrate</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le campagne orchestrate ora supportano la <strong>messaggistica transazionale</strong>, che consente di attivare messaggi in tempo reale basati su eventi, ad esempio conferme di ordini, notifiche di prenotazione e aggiornamenti dell'account, direttamente all'interno del flusso di lavoro della campagna.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Attivare campagne orchestrate tramite API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi attivare una campagna orchestrata tramite API. Configura la campagna di Target come "Attivata da un segnale" e pubblicala. Quindi utilizza una chiamata API per attivare la campagna. La chiamata API può includere parametri che saranno disponibili come variabili nella campagna attivata.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Attività di test nelle campagne orchestrate</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Una nuova attività <strong>Test</strong> è ora disponibile nelle campagne orchestrate. Questa attività indirizza l’esecuzione del flusso di lavoro a rami diversi in base a condizioni definite, consentendo di convalidare la logica e le configurazioni della campagna prima di attivare le consegne live.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Crittografia dei parametri URL</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>I parametri URL nei collegamenti di tracciamento e nelle pagine di destinazione ora possono essere crittografati, fornendo un ulteriore livello di sicurezza per i dati sensibili dei parametri.</p>
<ul>
<li>Registra e gestisci le chiavi di crittografia in un registro <strong>Amministrazione</strong> dedicato.</li>
<li>Utilizza il nuovo helper per la crittografia nelle espressioni per crittografare i dati sensibili nei collegamenti di tracciamento e negli URL delle pagine di destinazione per i parametri di query che desideri proteggere al momento del rendering.</li>
</ul>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
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
<p>Utilizza il nuovo nodo Optimize per rivolgerti a tipi di pubblico specifici oppure esegui test A/B per determinare il percorso migliore per soddisfare i KPI incentrati sull’azienda.
Questo strumento consente di testare e variare e di personalizzare le comunicazioni, la sequenza e la tempistica per raggiungere al meglio la clientela.
</p>
<p>Precedentemente rilasciata in Disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (Disponibilità generale). <a href="../building-journeys/optimize.md">Ulteriori informazioni</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Supporto della ricerca di set di dati in percorsi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Una nuova attività in percorsi, Ricerca set di dati, consente di recuperare dinamicamente i dati dai set di dati dei record di Adobe Experience Platform durante il runtime. Sfruttando questa funzionalità, puoi accedere ai dati che potrebbero non trovarsi nel profilo o nel payload dell’evento, garantendo che le interazioni della clientela siano pertinenti e tempestive. Precedentemente rilasciata in Disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (Disponibilità generale). Per ulteriori informazioni, consulta la <a href="../building-journeys/dataset-lookup.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Attività azione canale nativa obsolete</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In seguito alla disponibilità generale dell'attività <strong>Azione</strong> nel febbraio 2026, le attività legacy del canale nativo (e-mail, push, SMS, in-app, web, esperienza basata su codice e scheda contenuto) nell'area di lavoro del percorso sono ora obsolete.</p>
<p>Ora puoi utilizzare una singola <strong>attività Azione</strong> per configurare tutte le azioni del canale, sostituendo la necessità di nodi specifici del canale separati.</p>
I percorsi esistenti che utilizzano le attività dei canali precedenti continueranno a funzionare senza la necessità di apportare modifiche o migrazioni.
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/journey-action.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Supporto per le decisioni nel canale e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile utilizzare <strong>Decisioning</strong> per personalizzare e ottimizzare il contenuto dei messaggi di posta elettronica. Sfrutta punteggi di priorità, formule o modelli di IA per visualizzare le offerte e i contenuti più rilevanti per ogni destinatario.</p>
<p>Precedentemente rilasciata in Disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (Disponibilità generale). Con questa versione di disponibilità generale, sono ora supportate le pagine mirror.</p>
<p>Per ulteriori informazioni, consulta la <a href="../experience-decisioning/create-decision-policy.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Conversione di immagini in modelli di contenuto e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora è possibile convertire le immagini in modelli di contenuto e-mail direttamente in Journey Optimizer. Utilizza l’analisi basata sull’intelligenza artificiale per generare automaticamente modelli HTML strutturati dai riferimenti visivi, riducendo in modo significativo i tempi di progettazione delle e-mail.</p>
<p>Precedentemente rilasciata in Disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (Disponibilità generale). <a href="../content-management/image-to-html.md">Ulteriori informazioni</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Casella in entrata</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Una nuova <strong>casella in entrata</strong> è una funzionalità mobile, disponibile con schede di contenuto, che consente ai clienti di creare una posizione centralizzata all'interno dell'app o del sito Web per visualizzare i messaggi inviati agli utenti. Questo estende la durata delle comunicazioni di marketing garantendo che i messaggi rimangano accessibili anche dopo essere stati chiusi.</p>
<p>Data di disponibilità: mercoledì 31 marzo 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Editor HTML avanzato per modelli e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La modalità HTML avanzata per i modelli di contenuto e-mail consente di modificare l’origine HTML del contenuto nel Designer e-mail, aggiungere espressioni avanzate (come condizioni) nell’origine e passare dalla vista HTML a quella desktop senza perdere le modifiche.</p>
<p>Questa funzionalità è disponibile solo nei modelli di contenuto per il canale e-mail. Attualmente è a disponibilità limitata. Per ottenere l’accesso, contatta il rappresentante Adobe.</p>
<p><img src="assets/do-not-localize/expert-mode.gif"/></p>
<p>Per ulteriori informazioni, consulta la <a href="../content-management/email-template-expert-mode.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: mercoledì 10 marzo 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integrazione di modelli Firefly personalizzati e modelli di generazione di immagini di terze parti</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Integrazione perfetta di modelli Firefly standard e personalizzati, insieme a modelli di immagini di terze parti approvati, per fornire maggiore flessibilità, controllo e allineamento del brand durante la generazione delle immagini.</p>
<p>Scegli il modello giusto per le tue esigenze:</p>
<ul><li> <strong>Adobe model</strong> (con tecnologia Firefly Image Model 4) per la generazione immediata di immagini senza installazione aggiuntiva</li><li> <strong>Modello partner</strong> (con tecnologia Gemini 2.5 Flash) per funzionalità specializzate</li><li><strong>Modelli personalizzati</strong> (modelli specifici del brand addestrati sulle tue risorse) per la generazione di prodotti sul brand che sono allineati con precisione alla tua identità del brand, allo stile e alle linee guida visive.</li></ul>
<p>Per ulteriori informazioni, consulta la <a href="../content-management/generative-models.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: martedì 2 marzo 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Attività live per iOS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Porta esperienze in tempo reale direttamente su Blocca Screens e Dynamic Island dei tuoi clienti con iOS Live Activity in Adobe Journey Optimizer. Consegna aggiornamenti live, dal tracciamento degli ordini e dello stato dei voli, ai conteggi degli eventi, ai punteggi live e all’avanzamento della consegna, senza richiedere agli utenti di aprire l’app. Tieni il pubblico informato e coinvolto al momento giusto, proprio dove si trova.</p>
<p>Precedentemente rilasciata in versione beta, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p>Per ulteriori informazioni, consulta la <a href="../mobile-live/get-started-mobile-live.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: mercoledì 3 marzo 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent: creazione di contenuti del canale</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con tecnologia <strong>Adobe Experience Platform Agent Orchestrator</strong>, <strong>Journey Agent</strong> è disponibile in Journey Optimizer e consente di analizzare i percorsi tramite un'interfaccia in linguaggio naturale. È inoltre possibile generare e gestire contenuti specifici per il canale direttamente in Journey Agent, creando contenuti per canali quali e-mail e push, applicando e visualizzando in anteprima modelli, perfezionando tono e stile tramite prompt e aprendo contenuti in <strong>Content Designer</strong> per la modifica nel contesto.</p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<p>Per ulteriori informazioni, consulta la <a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent.html">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: giovedì 4 marzo 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Monitoraggio del modello di IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ora consente di monitorare lo stato, lo stato di formazione e le prestazioni dei modelli di IA per il decisioning. Questo consente di verificare il successo della formazione, risolvere eventuali problemi e comprendere l’impatto sui risultati, al fine di selezionare le offerte migliori per ogni cliente che utilizza l’intelligenza artificiale. Questa funzionalità è disponibile solo per <strong>Decisioning</strong> (non per i modelli di gestione delle decisioni legacy).</p>
<p>Questa funzionalità è attualmente disponibile solo per i modelli di <strong>ottimizzazione personalizzata</strong> (non ottimizzazione automatica).</p>
<p><img src="assets/do-not-localize/ai-model-observability.gif"/></p>
<p>Per ulteriori informazioni, consulta la <a href="../experience-decisioning/ranking/ai-model-observability.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: martedì 9 marzo 2026</p>
</td>
</tr>
</tbody>
</table>


### Miglioramenti {#march-26-improv}

Di seguito sono elencati i miglioramenti inclusi in questa versione.


#### Generazione dei rapporti

* **Escludi clic bot per rapporti e-mail e SMS** - La generazione di rapporti e-mail e SMS ora filtra automaticamente i clic bot dalle metriche di clic, fornendo dati di coinvolgimento più precisi e impedendo al traffico automatizzato di gonfiare i valori delle prestazioni.

* **Ottimizzazione dell&#39;ora di invio: la posizione dei controlli aggiornata e il nuovo rapporto di incremento** - I controlli di ottimizzazione dell&#39;ora di invio (STO) sono stati spostati nel menu di configurazione Azione. Inoltre, è ora disponibile un nuovo rapporto lift nei rapporti Percorsi per misurare l’impatto dell’STO sulle metriche delle prestazioni della campagna.

#### E-mail designer

* **Designer e-mail visualizzato in Unified Shell** - Il Designer e-mail viene ora visualizzato nell&#39;esperienza di Unified Shell, fornendo un&#39;esperienza di navigazione e di intestazione coerente che è in linea con altre applicazioni Adobe.

* **Supporto della modalità testo nei frammenti** - Per supportare flussi di lavoro di posta elettronica basati su testo, ora puoi creare e gestire versioni testuali dei frammenti visivi per un utilizzo ottimale nella versione di testo normale delle e-mail che includono tale frammento.

  **Attenzione:** quando si utilizza un frammento creato prima della versione corrente, è possibile che la versione del testo del frammento non venga rappresentata correttamente, sia nel Designer e-mail che nell&#39;e-mail finale recapitata ai destinatari. Per ottenere risultati ottimali con i frammenti meno recenti, modifica, salva e ripubblica ogni frammento.

#### Funzione Decisioni

* **Feed di modifica del riferimento al frammento di espressione in Edge Decisioning** - Questo miglioramento consente di riflettere automaticamente le modifiche nei riferimenti ai frammenti in tutti gli elementi che fanno riferimento a frammenti, senza dover aggiornare nulla manualmente (ripubblicazione della campagna o del criterio decisionale).

* **Frammenti facoltativi negli elementi decisionali** - Quando si utilizzano frammenti negli elementi decisionali, è ora possibile rendere facoltativo un frammento in modo che, se temporaneamente non disponibile in Edge, venga ignorato e il rendering del percorso o della campagna continui invece di avere esito negativo.

#### Configurazione

* **Cartelle per percorsi e campagne** - È ora possibile organizzare i percorsi e le campagne in cartelle, consentendo una navigazione strutturata e una gestione più semplice per i team che lavorano con grandi volumi di contenuti. Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.

* **AJO Secondary Recipient Feedback Event Rename** - Il set di dati `AJO Email BCC Feedback Event` è stato rinominato in `AJO Secondary Recipient Feedback Event`. L’impatto varia a seconda della situazione:

   * **Utenti esistenti**: viene aggiornato solo il nome visualizzato. Il nome della tabella sottostante rimane invariato.
   * **Nuovi utenti e sandbox**: sia il nome visualizzato che il nome della tabella riflettono il nuovo nome.
   * **Utenti esistenti con nuove sandbox**: il nome visualizzato e il nome della tabella vengono aggiornati al nuovo nome.

  Data di disponibilità: martedì 2 marzo 2026

#### Campagne orchestrate

* **Variabili globali in Campagne orchestrate** - Le campagne orchestrate ora supportano variabili globali che possono essere definite una volta e riutilizzate in tutte le attività di un flusso di lavoro, semplificando la configurazione e garantendo la coerenza in valori dinamici, espressioni e personalizzazione dei contenuti.

* **Semplificazione delle dimensioni di destinazione nelle campagne orchestrate** - È ora possibile selezionare facilmente o dedurre automaticamente le dimensioni di destinazione e secondarie corrette nelle campagne orchestrate per un&#39;attivazione accurata ed efficiente del pubblico.

#### Percorsi

* **Invio ondata di messaggi in uscita in percorsi** - È ora possibile pianificare i messaggi provenienti da percorsi Journey Optimizer da recapitare in batch controllati nel tempo. [Ulteriori informazioni](../building-journeys/send-using-waves.md)

  Precedentemente rilasciata in Disponibilità limitata per l’utilizzo in percorsi, questa funzionalità è ora disponibile per tutti gli ambienti (Disponibilità generale).

  Data di disponibilità: martedì 16 marzo 2026

* **Sospendi e riprendi dettagli nei dettagli tecnici del percorso** - I **dettagli tecnici** del percorso ora includono ulteriori informazioni sulla pausa e sulla ripresa: la data e l&#39;ora dell&#39;ultima pausa e della ripresa, il nome visualizzato e l&#39;identificatore interno dell&#39;utente che ha eseguito ogni azione e un set completo di impostazioni di percorso in pausa come il comportamento della pausa, la durata massima della pausa e lo stato di ripresa automatica. [Ulteriori informazioni](../building-journeys/journey-properties.md)

  Data di disponibilità: martedì 2 marzo 2026


## Note sulla versione di febbraio 2026 {#feb-26-01-rn}

Le sezioni [Nuove funzionalità](#feb-26-01-features) e [Miglioramenti](#feb-26-01-improv) riguardano le funzionalità già disponibili. <!--The [Coming soon](#coming-soon) section lists features and improvements scheduled for release later in February.-->

<!--**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.-->

<!--**Release date**: February 17-18, 2026-->

### Nuove funzionalità {#feb-26-01-features}


<table>
<thead>
<tr>
<th><strong>arbitrato di percorso</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile utilizzare <strong>formule di classificazione</strong> per aumentare automaticamente i punteggi di priorità del percorso in base agli attributi del profilo cliente e ai fattori contestuali, in modo che i clienti immettano i percorsi più rilevanti.</p>
<p><img src="assets/do-not-localize/journey-arbitration-formulas.gif"/></p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<p>Per ulteriori informazioni, consulta la <a href="../conflict-prioritization/journey-ranking-formulas.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: mercoledì 24 febbraio 2026</p>
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
<p>Journey Optimizer supporta una nuova <strong>attività Azione</strong> generica che consente di configurare sia le azioni singole che i gruppi di azioni in entrata con più azioni, semplificando la configurazione delle azioni nell'area di lavoro del percorso. In particolare, questa nuova funzione consente:</p>
<ul>
<li>una configurazione semplificata dell’azione nativa nell’area di lavoro del percorso;</li>
<li>la capacità di creare gruppi di azioni in entrata con più azioni;</li>
<li>la possibilità di aggiungere l’ottimizzazione a qualsiasi azione del canale incorporata;</li>
<li>Possibilità di aggiungere sia opzioni di sperimentazione che opzioni multilingue a qualsiasi azione.</li>
</ul>
<p><img src="assets/do-not-localize/action-activity.gif"/></p>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/journey-action.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: sabato 20 febbraio 2026</p>
<p><strong>Nota:</strong> tutti i canali nativi sono ora accessibili tramite l'attività del percorso di azioni. Le attività dei canali nativi legacy diventeranno obsolete con la versione di marzo. I percorsi esistenti che includono azioni legacy continueranno a funzionare così come sono, non è richiesta alcuna migrazione.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Invio ondata di messaggi in uscita</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi pianificare i messaggi provenienti da campagne o percorsi Journey Optimizer da consegnare in batch controllati nel tempo.</p>
<p>L’invio ondata offre i seguenti vantaggi:</p>
<ul>
<li>Migliore recapito messaggi: Spread invia nel tempo per contribuire a mantenere una solida reputazione del mittente e ridurre il rischio di essere segnalati come spam.</li>
<li>Controllo del carico: evita di sopraffare i sistemi a valle (ad esempio call center e pagine di destinazione) limitando il numero di messaggi che vengono inviati contemporaneamente.</li>
<li>Casi d’uso complessi e sensibili al tempo: adatti a tipi di pubblico di grandi dimensioni o quando è necessario controllare la tempistica (ad esempio capacità del call center, offerte incrementali o con limiti di tempo).</li>
</ul>
<p><img src="assets/do-not-localize/waves.gif"/></p>
<p>In <strong>campagne</strong>, questa funzionalità è disponibile per tutti gli ambienti (disponibilità generale). Per ulteriori informazioni, consulta la <a href="../campaigns/send-using-waves.md">documentazione dettagliata</a>.</p>

<p>In <strong>percorsi</strong>, questa funzionalità è disponibile solo per un set di organizzazioni (disponibilità limitata). Per ottenere l'accesso, contatta il tuo rappresentante Adobe. Per ulteriori informazioni, consulta la <a href="../building-journeys/send-using-waves.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: venerdì 19 febbraio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Migrare i sottodomini alla delega personalizzata</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi migrare i sottodomini utilizzando la modalità di delega CNAME alla delega personalizzata direttamente dall’interfaccia, in modo da soddisfare criteri di sicurezza più severi in linea con le linee guida della tua azienda senza ricreare le configurazioni del canale.</p>
<p><img src="assets/do-not-localize/subdomain-migration.gif"/></p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<p>Per ulteriori informazioni, consulta la <a href="../configuration/custom-subdomain-migration.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: venerdì 19 febbraio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canale per notifiche push web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer ora supporta <strong>notifiche push web</strong>, espandendo il canale push oltre i dispositivi mobili. Puoi inviare facilmente le notifiche ai <strong>browser di dispositivi mobili e desktop</strong>, per raggiungere la clientela direttamente sui dispositivi senza richiedere un’app. Questo miglioramento consente di coinvolgere gli utenti con messaggi tempestivi e personalizzati in tempo reale, sfruttando gli stessi flussi di lavoro di authoring e le stesse funzionalità di targeting già disponibili per le notifiche push per dispositivi mobili.</p>
<p><img src="assets/do-not-localize/web-push.gif"/></p>
<p>Precedentemente rilasciata in Beta, questa funzionalità sarà disponibile per tutti gli ambienti (disponibilità generale).</p>
<p>Per ulteriori informazioni, consulta la <a href="../push/push-configuration-web.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: sabato 13 febbraio 2026</p>
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
<p>Una nuova <strong>attività Content Decision</strong> è ora disponibile nell'area di lavoro del percorso per l'integrazione di offerte personalizzate direttamente nei percorsi di clienti. Questa attività ti consente di fornire contenuti basati su decisioni e di fare riferimento a tali offerte in tutto il percorso, in condizioni per la creazione di diramazioni basate sull’idoneità, in azioni personalizzate per il passaggio dei dati delle offerte a sistemi esterni e in altre attività per la creazione di esperienze cliente completamente personalizzate.</p>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p><img src="assets/do-not-localize/content-decision.gif"/></p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/content-decision.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: mercoledì 10 febbraio 2026</p>
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
<p>Le API per gli strumenti di migrazione sono ora disponibili per migrare a livello di programmazione le entità <strong>Gestione decisioni</strong> in <strong>Decisioning</strong>, con:</p>
<ul>
<li>Ambiti di migrazione flessibili (a livello di sandbox, offerta o decisione)</li>
<li>Automazione di analisi e convalida delle dipendenze</li>
<li>Supporto del rollback per le migrazioni completate</li>
<li>Rapporti dettagliati sulla migrazione con mappature degli oggetti</li>
</ul>
<p>Per ulteriori informazioni, consulta la <a href="../experience-decisioning/decisioning-migration-api.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 3 febbraio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Monitoraggio delle azioni personalizzate</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Approfondisci insight sullo stato e sulle prestazioni degli endpoint di azione personalizzati con un nuovo dashboard di monitoraggio e dati arricchiti sugli eventi dei passaggi del percorso. Tieni traccia correttamente di chiamate, errori, velocità effettiva, tempi di risposta e tempi di attesa delle code per comprendere rapidamente quando, dove e perché si verificano anomalie.</p>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p>Per ulteriori informazioni, consulta la <a href="../action/reporting.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 3 febbraio 2026</p>
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
<p>Ora puoi personalizzare e ottimizzare il contenuto dei messaggi SMS con Decisioning. Utilizzando punteggi di priorità, formule o modelli di IA, puoi così presentare a ogni cliente i contenuti più adatti.</p>
<p>Per ulteriori informazioni, consulta la <a href="../experience-decisioning/create-decision.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 2 febbraio 2026</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti {#feb-26-01-improv}

Di seguito sono elencati i miglioramenti inclusi in questa versione.

#### Configurazione

* **Utilizzo degli eventi di esperienza nelle espressioni di percorso** - A partire dal 1° aprile 2026, l&#39;utilizzo degli attributi degli eventi di esperienza nelle espressioni di percorso non sarà più supportato per le organizzazioni che non hanno utilizzato questa funzionalità negli ultimi 90 giorni. Questa funzionalità non è più disponibile per le nuove organizzazioni di clienti dall’8 luglio 2025. Per alternative, consulta [Ricerca eventi esperienza in percorsi](../building-journeys/exp-event-lookup.md).

#### Gestione dei contenuti

<!--
* **Update brands with new color tab** - Brand guidelines help ensure your brand is presented consistently across all touchpoints. The new <strong>Colors</strong> section defines the standards for your brand's color system, outlining how colors are selected, organized, and applied across experiences. It ensures consistent use of primary, secondary, accent, and neutral colors to support a cohesive, accessible, and recognizable brand identity. [Read more](../content-management/brands.md)
-->

* **Utilizza i temi per convertire le immagini in modelli e-mail**. Quando converti un&#39;immagine in un modello e-mail in Journey Optimizer, ora puoi utilizzare un tema come input in modo che il HTML generato segua i parametri del tuo marchio. Lo stile, ad esempio il colore di sfondo, il colore dei pulsanti, i tipi di carattere, l&#39;interlinea, i margini e la spaziatura interna, viene applicato automaticamente, riducendo il lavoro di progettazione manuale e distribuendo un modello pronto per l&#39;uso con modifiche minime. [Ulteriori informazioni](../content-management/image-to-html.md)

  Data di disponibilità: 17 febbraio 2026.

<!--* **Text mode for fragments** - You can now create and manage text versions of your fragments, supporting workflows that rely on plain text content and providing the same flexibility as in email content. [Read more](../content-management/create-fragments.md)-->

#### E-mail designer

* **Rientro testo** - È ora possibile applicare un rientro a sinistra personalizzabile alla prima riga di paragrafi nei componenti di testo direttamente dal pannello delle proprietà. <!--The new **Indentation** control lets you define indentation in pixels or percentage via a numeric input or slider, with live preview on the canvas. -->Ciò migliora la leggibilità dei contenuti lunghi, ad esempio editoriali e articoli. [Ulteriori informazioni](../email/get-started-email-style.md)

  Data di disponibilità: 18 febbraio 2026.

#### Funzione Decisioni

* **Supporto in entrata di Edge per l&#39;utilizzo dei dati di Adobe Experience Platform in Decisioning**. L&#39;utilizzo dei dati di Adobe Experience Platform in Decisioning ora supporta casi d&#39;uso in entrata Edge, oltre alle azioni e-mail e personalizzate nei percorsi. [Ulteriori informazioni](../experience-decisioning/aep-data-exd.md)

  Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.


* **Allega frammenti agli elementi decisionali**: Journey Optimizer ora consente di allegare agli elementi decisionali frammenti che possono essere utilizzati nelle campagne di esperienza basata su codice tramite i criteri di decisione. [Ulteriori informazioni](../experience-decisioning/fragments-decision-policies.md)

  Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).

  Data di disponibilità: 12 febbraio 2026.

#### Personalizzazione

* **Helper metadati esecuzione** - La funzione helper `executionMetadata` è ora disponibile per tutti i clienti Journey Optimizer. Utilizzala per aggiungere dinamicamente informazioni contestuali a qualsiasi azione nativa e acquisirle in un set di dati per l’esportazione in sistemi esterni. [Ulteriori informazioni](../personalization/functions/helpers.md#execution-metadata)

  Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).

  Data di disponibilità: 20 febbraio 2026.

#### SMS

* **Webhook SMS** - I webhook sono ora supportati in tutti i provider SMS. Puoi configurare ogni webhook in base allo scopo previsto: i webhook in entrata per acquisire i messaggi in arrivo e i webhook di feedback per ricevere le conferme di consegna, gli aggiornamenti di stato e altri eventi relativi ai messaggi. [Ulteriori informazioni](../sms/sms-webhook.md)

  Data di disponibilità: 2 febbraio 2026.

<!--## Coming soon {#coming-soon}

The features and improvements below are planned for release later in February. Release dates and scope may change without prior notice.

### Improvements {#coming-soon-improv}

* **Decisioning preview in Code-based Experience channel** - You can now preview decision items when configuring Decisioning with the Code-based Experience channel. Preview is available directly in the authoring interface before going live.

  Availability date: February 18, 2026
-->

