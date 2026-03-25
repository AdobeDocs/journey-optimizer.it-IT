---
solution: Journey Optimizer
product: journey optimizer
title: Note sulle versioni 2026
description: Note sulle versioni 2026 di Journey Optimizer
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 65ca94cf-8e17-4a25-90f3-238083f81477
source-git-commit: b6b74e357029f4924f9699c05af3a0fcd7fcefd6
workflow-type: tm+mt
source-wordcount: '2573'
ht-degree: 64%

---

# Note sulle versioni 2026 {#release-notes-2026}

In questa pagina sono elencate tutte le funzioni e i miglioramenti di [!DNL Journey Optimizer] rilasciati nel 2026.



## Note sulla versione di febbraio 2026 {#feb-26-01-rn}

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

* **Anteprima Decisioning nel canale di esperienza basato su codice** - È ora possibile visualizzare in anteprima gli elementi decisionali durante la configurazione di Decisioning con il canale di esperienza basato su codice. L’anteprima è disponibile direttamente nell’interfaccia di authoring prima della pubblicazione. [Ulteriori informazioni](../code-based/test-code-based.md#preview-code-based)

  Data di disponibilità: giovedì 18 febbraio 2026

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



## Note sulla versione di gennaio 2026 {#jan-26-rn}

<!--**Release date**: January 27-28, 2026-->

### Nuove funzionalità {#jan-26-01-features}


<table>
<thead>
<tr>
<th><strong>Supporto per le decisioni nel canale push</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi personalizzare e ottimizzare il contenuto delle <strong>notifiche push</strong> con <strong>decisioni</strong>. Utilizzando punteggi di priorità, formule o modelli di IA, puoi così presentare a ogni cliente i contenuti più adatti.</p>
<p>Experience Decisioning con notifiche push richiede una versione specifica del SDK mobile. Prima di implementare questa funzione, controlla le <a href="https://developer.adobe.com/client-sdks/home/release-notes/" target="_blank">note sulla versione</a> per identificare la versione richiesta e assicurarti di aver effettuato l'aggiornamento di conseguenza. Puoi anche visualizzare tutte le versioni di SDK disponibili per la tua piattaforma in <a href="https://developer.adobe.com/client-sdks/home/current-sdk-versions/" target="_blank">questa sezione</a>.</p>
<p>Per ulteriori informazioni, consulta la <a href="../experience-decisioning/create-decision.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 30 gennaio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canale direct mail nei percorsi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Precedentemente limitato alle campagne, il canale <strong>direct mail</strong> è ora disponibile nell’area di lavoro dei percorsi e consente di incorporare direct mail nei percorsi. Direct mail può ora essere utilizzato sia in <strong>batch che in scenari di percorso 1:1</strong>, con il supporto per la configurazione dell’estrazione dei file e le impostazioni di frequenza temporale.</p>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p><img src="assets/do-not-localize/dm-journey.gif"/></p>
<p>Per ulteriori informazioni, consulta la <a href="../direct-mail/get-started-direct-mail.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: venerdì 29 gennaio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Ore di silenzio (esclusioni basate sul tempo)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le <strong>ore di silenzio</strong> consentono di definire esclusioni basate sul tempo per i canali E-mail, SMS, Push e WhatsApp. Garantiscono che non vengano inviati messaggi in specifici periodi di tempo, aiutandoti a rispettare le preferenze dei clienti e i requisiti di conformità. Puoi applicare ore di silenzio tramite <strong>set di regole</strong>, che possono essere assegnate a singole azioni in campagne o percorsi per un controllo preciso.</p>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzione è ora disponibile per tutti gli ambienti. Con questo rilascio in disponibilità generale, la funzione ora consente di mettere in coda un’azione di una campagna fino al termine delle ore di silenzio, nonché di visualizzare in anteprima la regola Ore di silenzio attivata.</p>
<p><img src="assets/do-not-localize/quiet-hour-ga.gif"/></p>
<p>Per ulteriori informazioni, consulta la <a href="../conflict-prioritization/quiet-hours.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: venerdì 29 gennaio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Esportazione dei messaggi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora disponibile una nuova funzionalità di <strong>esportazione dei messaggi</strong> per i canali e-mail e SMS. Questa funzione consente di esportare automaticamente il contenuto dei messaggi inviati in un set di dati Experience Platform dedicato, per le seguenti esigenze:</p>
<ul>
<li>Soddisfare i requisiti di conformità alle normative (ad esempio HIPAA)</li>
<li>Archiviare i messaggi per richieste legali e di assistenza clienti</li>
<li>Mantenere copie dei contenuti personalizzati inviati a singoli utenti</li>
</ul>
<p>I record vengono conservati nel set di dati di esportazione dei messaggi di AJO per 7 giorni di calendario dall’acquisizione. Durante questo periodo di conservazione, puoi esportarli nel tuo archivio tramite le destinazioni Experience Platform. La funzione è abilitata a livello di configurazione dei canali e ti permette di <strong>definire in modo granulare</strong> quali messaggi esportare.</p>
<p>Questa funzionalità è disponibile solo per i canali e-mail e SMS, per le organizzazioni che hanno acquistato il componente aggiuntivo per l’esportazione dei messaggi. Per ulteriori informazioni, contatta il tuo rappresentante Adobe.</p>
<p><img src="assets/do-not-localize/message-export.gif"/></p>
<p>Per ulteriori informazioni, consulta la <a href="../configuration/message-export.md#message-export">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 28 gennaio 2026</p>
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
<p>Il canale direct mail è ora disponibile nelle campagne orchestrate. L’<strong>attività Direct mail</strong> facilita l’invio con direct mail all’interno della campagna orchestrata, per messaggi singoli o ricorrenti. Consente di automatizzare il processo di generazione del <strong>file di estrazione</strong> richiesto dai provider di servizi di direct mail. Puoi combinare le attività del canale nell’area di lavoro della campagna orchestrata per creare campagne cross-channel in grado di attivare azioni basate sui dati e sul comportamento della clientela.</p>
<p><img src="assets/do-not-localize/dm-oc.gif"/></p>
<p>Per ulteriori informazioni, consulta la <a href="../orchestrated/activities/channels.md#channel">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 28 gennaio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Agente Journey - Crea un percorso</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’agente Journey ora offre funzionalità di creazione che consentono agli utenti di Journey Optimizer di creare e configurare percorsi di marketing tramite un’interfaccia basata su <strong>linguaggio naturale</strong>. Con queste nuove competenze, i professionisti possono creare rapidamente percorsi semplicemente descrivendone i requisiti tramite <strong>prompt conversazionali</strong>. Questa innovazione semplifica il processo di creazione del percorso e consente ai marketer di concentrarsi sulla strategia anziché sulla configurazione tecnica.</p>
<p>Per ulteriori informazioni, consulta la <a href="../start/ai-features.md#journey-agent">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 12 gennaio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>API di recupero di campagne con azioni</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora disponibile una nuova API di Journey Optimizer che consente di recuperare e ispezionare in modo programmatico i <strong>dati relativi alla campagna</strong>, ad esempio dettagli, versioni e configurazioni.</p>
<p>Per ulteriori informazioni, consulta la <a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/" target="_blank">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 24 novembre 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Temi di E-mail designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi applicare rapidamente <strong>temi preapprovati</strong> per garantire la <strong>coerenza del brand</strong> in tutte le e-mail, velocizzare il processo di creazione delle campagne e produrre e-mail di alta qualità in modo indipendente, riducendo al contempo la dipendenza dai team di progettazione grafica.</p>
<p><img src="assets/do-not-localize/themes.gif"/></p>
<p>Precedentemente rilasciata nella versione Beta, questa funzionalità è ora disponibile per un set di organizzazioni (disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<p>Per ulteriori informazioni, consulta la <a href="../email/apply-email-themes.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 5 novembre 2025</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti {#jan-26-01-improv}

#### IA

* **Controlli di qualità dei contenuti con l’Assistente IA**: oltre all’allineamento al brand, ora puoi valutare la <strong>qualità dei contenuti</strong> complessiva per individuare potenziali problemi di <strong>leggibilità</strong>, coesione ed efficacia, indipendentemente dalle linee guida del brand. Questi controlli automatizzati consentono di individuare messaggi poco chiari, toni incoerenti o lacune strutturali. [Ulteriori informazioni](../content-management/brands-score.md#validate-quality).

  [Guarda il video su questa funzione](https://video.tv.adobe.com/v/3470554/?captions=ita&learn=on).

#### Percorsi

* **Combinare azioni con messaggi native e di Adobe Campaign**: Journey Optimizer ora consente di combinare, nello stesso percorso, azioni con messaggii di <strong>Adobe Campaign v7/v8</strong> con le <strong>azioni di canale native</strong> . [Ulteriori informazioni](../building-journeys/using-adobe-campaign-v7-v8.md)

  Data di disponibilità: mercoledì 27 gennaio 2026.

* **Payload di risposta in caso di errore per azioni personalizzate**: ora puoi facoltativamente definire un <strong>payload di risposta in caso di errore</strong> per le azioni personalizzate. Se una chiamata non riesce, il payload di errore viene esposto nel contesto del percorso (sotto il nodo errorResponse dell’azione) ed è disponibile nel <strong>ramo timeout/errore</strong>, insieme a `jo_status_code`, per un migliore supporto della logica di fallback e del debug. [Ulteriori informazioni](../action/about-custom-action-configuration.md#define-the-message-parameters)

  Data di disponibilità: mercoledì 27 gennaio 2026.

* **Convalida della dimensione del payload Journey nei percorsi**: Journey Optimizer ora convalida la <strong>dimensione del payload</strong> per garantire prestazioni e stabilità del sistema ottimali. Durante la creazione o la pubblicazione di percorsi, vengono visualizzati messaggi chiari di <strong>avvertenze ed errori</strong> se la dimensione del payload si avvicina o supera i limiti consigliati, con istruzioni da mettere subito in pratica per ottimizzare la configurazione dei percorsi. Questa convalida proattiva consente di individuare per tempo potenziali problemi e di mantenere ottimali le prestazioni del percorso. [Ulteriori informazioni](../start/guardrails.md#journey-payload-size)

  Data di disponibilità: mercoledì 27 gennaio 2026.


* **Avvisi sui percorsi**: sono disponibili nuovi <strong>avvisi preconfigurati</strong> per i percorsi.
   * <strong>Tasso di profili rimossi superato</strong>: il rapporto tra i profili rimossi e i profili in ingresso negli ultimi 5 minuti ha superato la soglia consentita.
   * <strong>Tasso di errore nelle azioni personalizzate superato</strong>: il rapporto tra gli errori nelle azioni personalizzate e le chiamate HTTP riuscite negli ultimi 5 minuti ha superato la soglia consentita.
   * <strong>Tasso di profili con errori superato</strong>: il rapporto tra profili con errori e profili in ingresso negli ultimi 5 minuti ha superato la soglia la consentita.

  Per ulteriori informazioni, consulta la [documentazione dettagliata](../reports/alerts.md).

  Data di disponibilità: 14 ottobre 2025.

#### Campagne orchestrate

* **Ereditarietà delle etichette di utilizzo dati per i tipi di pubblico**: le etichette applicate in Adobe Experience Platform ora vengono riportate in automatico quando un <strong>pubblico</strong> viene salvato in campagne orchestrate, in modo da ridurre l’assegnazione manuale dei <strong>tag DULE</strong>. [Ulteriori informazioni](../orchestrated/activities/save-audience.md)

* **Filtri preimpostati con parametri**: puoi ora creare <strong>filtri preimpostati</strong> con <strong>parametri</strong> nelle campagne orchestrate per regole riutilizzabili e modificabili. [Ulteriori informazioni](../orchestrated/predefined-filters.md)

* **Selezionare gli attributi e copiare i valori di distribuzione**: ora puoi <strong>selezionare o copiare i valori</strong> direttamente dalla vista <strong>Distribuzione dei valori</strong> nelle campagne orchestrate. [Ulteriori informazioni](../orchestrated/build-query.md)

* **Conferma del messaggio prima dell’invio**: ora è abilitato per impostazione predefinita un <strong>passaggio di conferma</strong> prima dell’invio di campagne orchestrate, per ridurre il rischio di invio accidentale. [Ulteriori informazioni](../orchestrated/activities/channels.md#confirm-message-sending)

* **Filtri di retargeting preimpostati**: per agevolare il retargeting per diversi casi d’uso di campagne orchestrate, questa versione introduce nuovi <strong>filtri di feedback sulla campagna</strong>. Questi filtri consentono di rivolgersi direttamente a un pubblico in base al <strong>coinvolgimento nei messaggi</strong> (ad esempio: inviato, solo aperto, aperto o cliccato, oppure aperto e cliccato) e di selezionare la campagna specifica o in transizione di cui desideri eseguire il retargeting. [Ulteriori informazioni](../orchestrated/retarget.md)

* **Supporto per il controllo della frequenza**: le campagne orchestrate ora supportano il <strong>controllo della frequenza</strong> per regolare la cadenza delle consegne e rispettare eventuali <strong>vincoli di volumi</strong>. [Ulteriori informazioni](../orchestrated/activities/channels.md#rate-control)

* **Pulsante di riavvio**: le campagne orchestrate ora includono un <strong>pulsante di riavvio</strong> per <strong>riavviare rapidamente le esecuzioni</strong>, se necessario, prima di pubblicare la campagna. [Ulteriori informazioni](../orchestrated/start-monitor-campaigns.md)

* **Supporto per metadati generati dall’utente**: la <strong>funzione helper executionMetadata</strong>, ora disponibile nell’editor di personalizzazione per le campagne orchestrate, consente di allegare informazioni contestuali a qualsiasi azione nativa e di memorizzarle in un set di dati per l’esportazione in sistemi esterni. [Ulteriori informazioni](../personalization/functions/helpers.md#execution-metadata)

  Data di disponibilità: mercoledì 27 gennaio 2026.

* **Ripristina stato bozza delle campagne live** - Ora puoi ripristinare lo stato bozza delle campagne orchestrate live quando si verificano errori di esecuzione o quando devi modificare le campagne pianificate prima che inizino l&#39;esecuzione. Questa opzione è disponibile fino all’invio del primo messaggio. [Ulteriori informazioni](../orchestrated/start-monitor-campaigns.md#back-to-draft)

#### Campagne

* **Pianifica campagna utilizzando il fuso orario del profilo** - La pianificazione delle campagne può ora utilizzare il <strong>fuso orario</strong> di ciascun profilo per recapitare i messaggi all&#39;ora locale prevista. [Ulteriori informazioni](../campaigns/campaign-schedule.md)

  **Nota**: questo miglioramento è disponibile solo per un set di organizzazioni (disponibilità limitata).

  Data di disponibilità: mercoledì 27 gennaio 2026.

#### Autorizzazioni

* **Impedire l’autoapprovazione per percorsi e campagne**: durante la creazione o l’impostazione dei <strong>criteri di approvazione</strong>, grazie a una nuova opzione puoi impedire a chi crea un percorso o una campagna di <strong>approvare i propri oggetti</strong>. [Ulteriori informazioni](../test-approve/approval-policies.md)

  Data di disponibilità: mercoledì 27 gennaio 2026.
