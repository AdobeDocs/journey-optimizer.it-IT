---
solution: Journey Optimizer
product: journey optimizer
title: Note pre-release per Journey Optimizer
description: Note pre-release di Adobe Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 1b21dc3355ebbfe16dd145de929a87eeb26db826
workflow-type: tm+mt
source-wordcount: '1553'
ht-degree: 25%

---

# Note pre-release {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nell’ultima settimana di ogni mese, tutte le modifiche vengono consolidate nelle [note sulla versione](release-notes.md).

## Note pre-release di febbraio 2026 {#feb-26-01-rn}

**Le note pre-release riportate di seguito sono soggette a modifica senza preavviso fino alla data di disponibilità della versione**. I collegamenti, le schermate e la documentazione aggiornata vengono pubblicati nelle note sulla versione, alla data di rilascio.

Consulta anche [Note pre-release di Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Data di rilascio**: mercoledì 17 febbraio 2026

### Nuove funzionalità {#feb-26-01-features}

<table>
<thead>
<tr>
<th><strong>Invio ondata di messaggi in uscita</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Puoi pianificare i messaggi in uscita da <strong>campagne</strong> o <strong>percorsi</strong> per essere recapitati in <strong>batch</strong> controllati nel tempo.</p>
<p>L’invio ondata offre i seguenti vantaggi:</p>
<ul>
<li>Migliore <strong>recapito messaggi</strong> - Il servizio Spread invia nel tempo per contribuire a mantenere una solida reputazione del <strong>mittente</strong> e ridurre il rischio di essere segnalati come spam.</li>
<li><strong>Controllo del carico</strong> - Evita di sovraccaricare i sistemi a valle (ad esempio call center, pagine di destinazione) limitando il numero di messaggi inviati contemporaneamente.</li>
<li>Casi d’uso complessi e sensibili al tempo: adatti a tipi di pubblico di grandi dimensioni o quando è necessario controllare la tempistica (ad esempio capacità del call center, offerte incrementali o con limiti di tempo).</li>
</ul>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-11533">Collegamento all’attività DOCAC su JIRA</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>arbitrato di percorso</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile utilizzare <strong>formule</strong> e <strong>modelli di IA</strong> per aumentare automaticamente i <strong>punteggi di priorità dei percorsi</strong> in base agli attributi del profilo cliente e ai fattori contestuali, in modo che i clienti immettano i percorsi più rilevanti.</p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (<strong>Disponibilità limitata</strong>). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13976">Collegamento all’attività DOCAC su JIRA</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent: creazione di contenuti per il canale</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con tecnologia <strong>Adobe Experience Platform Agent Orchestrator</strong>, <strong>Journey Agent</strong> è disponibile in Journey Optimizer e consente di analizzare i percorsi tramite un'interfaccia <strong>in linguaggio naturale</strong>. È inoltre possibile generare e gestire contenuti specifici per il canale direttamente in Journey Agent, creando contenuti per canali quali e-mail e push, applicando e visualizzando in anteprima modelli, perfezionando tono e stile tramite prompt e aprendo contenuti in <strong>Content Designer</strong> per la modifica nel contesto.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13980">Collegamento all’attività DOCAC su JIRA</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Attività mobili live</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Le attività live</strong> forniscono <strong>aggiornamenti in tempo reale</strong> ed esperienze interattive nelle app mobili, consentendo agli utenti di rimanere informati sugli eventi in corso o sulle attività direttamente sullo schermo del proprio dispositivo. Questa funzione migliora il coinvolgimento fornendo informazioni in tempo reale, come tracciamento dell’avanzamento, aggiornamenti degli eventi o contenuti interattivi, senza richiedere agli utenti di aprire l’app.</p>
<p>Precedentemente rilasciata in versione beta, questa funzionalità è ora disponibile per tutti gli ambienti (<strong>Disponibilità generale</strong>).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13588">Collegamento all’attività DOCAC su JIRA</a></p>
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
<p>Journey Optimizer supporta una nuova attività <strong>Action</strong> generica che consente di configurare sia le azioni singole che i gruppi di azioni in entrata <strong>con più azioni</strong>, semplificando la configurazione delle azioni nell'area di lavoro <strong>percorsi</strong>. In particolare, questa nuova funzione consente:</p>
<ul>
<li>una configurazione semplificata dell’azione nativa nell’area di lavoro del percorso;</li>
<li>la capacità di creare gruppi di azioni in entrata con più azioni;</li>
<li>Possibilità di aggiungere <strong>ottimizzazione</strong> a qualsiasi azione del canale incorporata.</li>
<li>Possibilità di aggiungere entrambe le opzioni <strong>sperimentazione</strong> e <strong>multilingue</strong> a qualsiasi azione.</li>
</ul>
<p>Questa funzionalità è ora disponibile per tutti gli ambienti (<strong>Disponibilità generale</strong>).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13290">Collegamento all’attività DOCAC su JIRA</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canale di notifiche web push</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer ora supporta le <strong>notifiche web push</strong>, estendendo il canale push oltre i dispositivi mobili. Puoi inviare facilmente le notifiche ai browser di dispositivi mobili e desktop, per raggiungere ogni cliente direttamente sul dispositivi che utilizza, senza ricorrere a un’app. Questo miglioramento consente di coinvolgere gli utenti con messaggi tempestivi e personalizzati in tempo reale, sfruttando gli stessi <strong>flussi di lavoro per l'authoring</strong> e le stesse <strong>funzionalità di targeting</strong> già disponibili per il push mobile.</p>
<p>Precedentemente rilasciata in versione beta, questa funzionalità è ora disponibile per tutti gli ambienti (<strong>Disponibilità generale</strong>).</p>
<p>Data di disponibilità: venerdì 12 febbraio 2026</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13581">Collegamento all’attività DOCAC su JIRA</a></p>
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
<p>Una nuova <strong>attività Content Decision</strong> è ora disponibile nell'<strong>area di lavoro percorsi</strong> per l'integrazione di <strong>offerte personalizzate</strong> direttamente nei percorsi di clienti. Questa attività ti consente di fornire contenuti basati su decisioni e di fare riferimento a tali offerte in tutto il percorso, in condizioni per la creazione di diramazioni basate sull’idoneità, in azioni personalizzate per il passaggio dei dati delle offerte a sistemi esterni e in altre attività per la creazione di esperienze cliente completamente personalizzate.</p>
<p>Precedentemente rilasciata in Disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (<strong>Disponibilità generale</strong>).</p>
<p><img src="assets/do-not-localize/content-decision.gif"/></p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/content-decision.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: giovedì 11 febbraio 2026</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-12902">Collegamento all’attività DOCAC su JIRA</a></p>
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
<p><strong>Le API per gli strumenti di migrazione</strong> sono ora disponibili per migrare a livello di programmazione <strong>Entità di gestione delle decisioni</strong> in <strong>Decisioning</strong>, con:</p>
<ul>
<li>Ambiti di migrazione flessibili (<strong>sandbox</strong>, <strong>offer</strong> o <strong>decision</strong> livello)</li>
<li><strong>analisi delle dipendenze</strong> e convalida automatizzate</li>
<li><strong>Supporto rollback</strong> per le migrazioni completate</li>
<li>Rapporti dettagliati sulla migrazione con mappature degli oggetti</li>
</ul>
<p>Per ulteriori informazioni, consulta la <a href="../experience-decisioning/decisioning-migration-api.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 3 febbraio 2026</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13837">Collegamento all’attività DOCAC su JIRA</a></p>
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
<p>Approfondisci insight sullo stato e sulle prestazioni dei <strong>endpoint di azioni personalizzati</strong> con un nuovo <strong>dashboard di monitoraggio</strong> e dati di <strong>evento del passaggio di percorso</strong> arricchiti. Tieni traccia correttamente di chiamate, errori, velocità effettiva, tempi di risposta e tempi di attesa delle code per comprendere rapidamente quando, dove e perché si verificano anomalie.</p>
<p>Precedentemente rilasciata in Disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (<strong>Disponibilità generale</strong>).</p>
<p>Per ulteriori informazioni, consulta la <a href="../action/reporting.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 3 febbraio 2026</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13981">Collegamento all’attività DOCAC su JIRA</a></p>
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
<p>Ora puoi personalizzare e ottimizzare il contenuto dei <strong>messaggi SMS</strong> con <strong>Decisioning</strong>. Utilizza <strong>Punteggi di priorità</strong>, <strong>Formule</strong> o <strong>Modelli AI</strong> per mostrare ai tuoi clienti il contenuto migliore.</p>
<p>Per ulteriori informazioni, consulta la <a href="../experience-decisioning/create-decision.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 2 febbraio 2026</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13426">Collegamento all’attività DOCAC su JIRA</a></p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti {#feb-26-01-improv}

Di seguito sono elencati i miglioramenti inclusi in questa versione.

#### Configurazione

* **Ritiro ricerca eventi esperienza** - A partire dal 1° aprile 2026, la <strong>ricerca eventi esperienza</strong> nell&#39;editor espressioni di condizione percorso verrà ritirata per le organizzazioni che non hanno utilizzato la ricerca eventi esperienza negli ultimi 90 giorni. Questa funzionalità non è più disponibile per le nuove organizzazioni di clienti dall’8 luglio 2025. Per alternative, consulta [Ricerca eventi esperienza in percorsi](../building-journeys/exp-event-lookup.md).

  <a href="https://jira.corp.adobe.com/browse/DOCAC-14136">Collegamento all&#39;attività JIRA DOCAC</a>

* **Cambio del metodo di delega del sottodominio** - È ora possibile passare da un metodo di <strong>delega del sottodominio</strong> a un altro. Questo consente di migrare i domini utilizzando la modalità di delega <strong>CNAME</strong> al metodo di delega <strong>personalizzata</strong> per rispettare i criteri di sicurezza della tua azienda.

  <a href="https://jira.corp.adobe.com/browse/DOCAC-13610">Collegamento all&#39;attività JIRA DOCAC</a>

#### E-mail designer

* **Utilizza un tema del brand per convertire un&#39;immagine in un modello e-mail**. Quando converti un&#39;immagine in un modello e-mail in Journey Optimizer, ora puoi utilizzare un <strong>tema</strong> come input in modo che il HTML generato segua i tuoi <strong>parametri del brand</strong>. Lo stile, ad esempio il colore di sfondo, il colore dei pulsanti, i tipi di carattere, l&#39;interlinea, i margini e la spaziatura interna, viene applicato automaticamente, riducendo il lavoro di progettazione manuale e distribuendo un modello pronto per l&#39;uso con modifiche minime.

  <a href="https://jira.corp.adobe.com/browse/DOCAC-14105">Collegamento all&#39;attività JIRA DOCAC</a>

* **Aggiorna i marchi con la nuova scheda colore** - <strong>Linee guida per i marchi</strong> per garantire che il tuo marchio venga presentato in modo coerente in tutti i punti di contatto. Nella nuova <strong>sezione Colori</strong> puoi definire gli standard del sistema di colori del brand, delineando il modo in cui i colori vengono selezionati, organizzati e applicati in tutte le esperienze. Questa seione promuove un utilizzo coerente dei colori primari, secondari, di accento e neutri per supportare un’identità del brand coesa, accessibile e riconoscibile.

  <a href="https://jira.corp.adobe.com/browse/DOCAC-13811">Collegamento all&#39;attività JIRA DOCAC</a>

#### IA

* **Integrazione di modelli Firefly personalizzati e di modelli di generazione di immagini di terze parti** - Integrazione perfetta di <strong>modelli Firefly</strong> standard e personalizzati, insieme a <strong>modelli di immagini di terze parti</strong> approvati (ad esempio, NanoBanana), per fornire maggiore flessibilità, controllo e allineamento del brand durante la generazione di immagini. Questo consente di selezionare il modello migliore per ogni caso d’uso: Firefly standard per esigenze generali, Firefly personalizzato per la generazione on-brand o modelli di terze parti approvati per scenari specializzati o sperimentali.

  <a href="https://jira.corp.adobe.com/browse/DOCAC-13918">Collegamento all&#39;attività JIRA DOCAC</a>

* **Supporto del modello 3P di Firefly per la generazione di immagini di terze parti**. È ora possibile utilizzare <strong>modelli di generazione di immagini di terze parti</strong> (ad esempio OpenAI e Gemini) insieme a Firefly per la creazione di immagini in Journey Optimizer. Questo offre maggiore flessibilità nella scelta del modello corretto per ogni caso d&#39;uso e nell&#39;integrazione dei provider esterni approvati tramite il <strong>gateway Firefly 3P</strong>.

  <a href="https://jira.corp.adobe.com/browse/DOCAC-14145">Collegamento all&#39;attività JIRA DOCAC</a>

#### Campagne

* **Cartelle per percorsi e campagne** - È ora possibile organizzare <strong>percorsi</strong> e <strong>campagne</strong> in <strong>cartelle</strong> per migliorare la navigazione e la gestione nell&#39;interfaccia.

  <a href="https://jira.corp.adobe.com/browse/DOCAC-14038">Collegamento all&#39;attività JIRA DOCAC</a>

#### Decisioni per le esperienze

* **Anteprima Experience Decisioning nel canale esperienza basato su codice** - È ora possibile visualizzare in anteprima <strong>elementi decisionali</strong> durante la configurazione di <strong>Experience Decisioning</strong> con il canale <strong>Esperienza basata su codice</strong>. L’anteprima è disponibile direttamente nell’interfaccia di authoring prima della pubblicazione.

  <a href="https://jira.corp.adobe.com/browse/DOCAC-14082">Collegamento all&#39;attività JIRA DOCAC</a>

* **Osservabilità del modello di IA per la classificazione delle offerte** - Journey Optimizer ora consente di monitorare <strong>integrità</strong>, <strong>stato di apprendimento</strong> e <strong>prestazioni</strong> dei <strong>modelli di IA</strong> in Decisioning, in modo da verificare il successo della formazione, risolvere gli errori e comprendere l&#39;impatto sui risultati. Questa funzionalità è disponibile solo per i modelli di ottimizzazione personalizzati (non per l’ottimizzazione automatica).

  <a href="https://jira.corp.adobe.com/browse/DOCAC-14040">Collegamento all&#39;attività JIRA DOCAC</a>

* **Allega frammenti agli elementi decisionali** - Journey Optimizer ora consente di allegare <strong>frammenti</strong> a <strong>elementi decisionali</strong> che possono essere utilizzati nelle campagne di esperienza basate su codice tramite <strong>criteri decisionali</strong>.

  **Nota**: questo miglioramento è ora disponibile per tutti gli ambienti (<strong>Disponibilità generale</strong>).

  Data di disponibilità: 12 febbraio 2026.

  <a href="https://jira.corp.adobe.com/browse/DOCAC-13418">Collegamento all&#39;attività JIRA DOCAC</a>

#### Percorsi

* **Più azioni in entrata nei percorsi**. Per semplificare l&#39;orchestrazione del percorso, è ora possibile definire più <strong>azioni in entrata</strong> in un singolo percorso. Precedentemente disponibile nelle campagne, questa funzionalità consente di distribuire più <strong>esperienze basate su codice</strong>, <strong>messaggi in-app</strong>, <strong>schede di contenuto</strong> o <strong>azioni Web</strong> in posizioni diverse contemporaneamente, ogni azione contenente contenuti specifici.

  **Nota**: questo miglioramento è ora disponibile per tutti gli ambienti (<strong>Disponibilità generale</strong>).

  <a href="https://jira.corp.adobe.com/browse/DOCAC-13453">Collegamento all&#39;attività JIRA DOCAC</a>

* **Webhook SMS**: i <strong>webhook</strong> sono ora supportati per tutti i provider SMS. Puoi configurare ogni webhook in base allo scopo previsto: <strong>Webhook in entrata</strong> per acquisire i messaggi in arrivo e <strong>Webhook di feedback</strong> per ricevere conferme di recapito, aggiornamenti dello stato e altri eventi relativi ai messaggi. [Ulteriori informazioni](../sms/sms-webhook.md)

  Data di disponibilità: 2 febbraio 2026.

  <a href="https://jira.corp.adobe.com/browse/DOCAC-13978">Collegamento all&#39;attività JIRA DOCAC</a>

<!--
## January '26 pre-release notes {#jan-26-01-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/it/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: January 27, 2026

### New capabilities {#jan-26-01-features}

<table>
<thead>
<tr>
<th><strong>Action activity in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer supports a new generic <strong>Action activity</strong> that enables you to configure both single actions and <strong>multi-action inbound action groups</strong>, allowing for streamlined action configuration within the journey canvas. In particular, this new feature allows for:</p>
<ul>
<li>A simplified native action configuration within the journey canvas.</li>
<li>The capacity to create multi-action inbound action groups.</li>
<li>The ability to add optimization to any built-in channel action.</li>
<li>The ability to add both experimentation and multi-lingual options to any action.</li>
</ul>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13290">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-111916">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Custom action monitoring</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Gain deeper insight into the health and performance of your custom action endpoints with a new <strong>monitoring dashboard</strong> and enriched journey step event data. Track successful calls, errors, throughput, response times, and queue wait times to quickly understand when, where, and why anomalies occur.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13981">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-126869">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Quiet Hours / Time Based Exclusions</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Quiet hours let you define <strong>time-based exclusions</strong> for Email, SMS, Push, and WhatsApp channels. They ensure that no messages are sent during specific periods of time, helping you respect customer preferences and compliance requirements. You can apply quiet hours through <strong>rule sets</strong>, which can be assigned to individual actions in campaigns or journeys for precise control.</p>
<p>Previously released in Limited Availability, this feature is now available to all environments. With this General Availability release, the feature now includes the ability for customer to queue a campaign action until the completion of Quiet Hours, and the ability to preview the activated Quiet Hours rule.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13986">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-63912">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Direct Mail channel in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Previously limited to Campaigns, the <strong>Direct Mail channel</strong> is now available on the <strong>journey canvas</strong>, enabling you to incorporate Direct Mail into your journeys. Direct Mail can now be used in both batch and 1:1 journey scenarios, with support for file extraction configuration and time-based frequency settings.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13543">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-38399">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Web Push notifications channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer now supports <strong>Web Push notifications</strong>, expanding the push channel beyond mobile. You can seamlessly deliver notifications to both mobile and desktop browsers, enabling you to reach customers directly on their devices without requiring an app. This enhancement allows you to engage users with timely, personalized messages in real time, leveraging the same authoring workflows and targeting capabilities already available for mobile push.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13581">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-37866">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Decisioning support in Push and SMS channels</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add <strong>Decision policies</strong> into push and SMS journeys and campaigns. Decision policies are containers for your offers that leverage the Decisioning engine to dynamically return the best content to deliver for each audience member.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13426">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/DOCAC-13425">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-55817">Link to PRODUCT JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-55818">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Direct mail channel in Orchestrated campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Direct mail channel is now available in orchestrated campaigns. The <strong>Direct mail activity</strong> facilitates direct mail sending within your Orchestrated campaign, for both one-time and recurring messages. It serves to automate the process of generating the <strong>extraction file</strong> required by direct mail providers. You can combine channel activities into the Orchestrated campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13379">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-82584">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>New source connectors for loyalty apps</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>New <strong>source connectors</strong> are now available in Adobe Experience Platform for the Talon.One, Capillary and Kobie loyalty Apps. These connectors let you seamlessly stream loyalty data into Adobe Experience Platform and leverage these data in Journey Optimizer.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13372">Link to DOCAC JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Message Export</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new <strong>Message Export</strong> capability is now available for email and SMS channels. This feature allows you to automatically export sent message content to a dedicated Experience Platform dataset, enabling you to:</p>
<ul>
<li>Meet regulatory compliance requirements (such as HIPAA)</li>
<li>Archive messages for legal claims and customer care inquiries</li>
<li>Retain copies of personalized content sent to individuals</li>
</ul>
<p>Records are retained in the AJO Message Export Dataset for <strong>7 calendar days from ingestion</strong>. During this retention period, you can export the data to your own storage via Experience Platform destinations. The feature is enabled at the channel configuration level, giving you granular control over which messages are exported.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-12915">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-105313">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent - Create a Journey</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Create Agent enables Journey Optimizer users to build and configure marketing journeys using a natural language interface. With Journey Create Agent, practitioners can quickly create journeys by describing their requirements in conversational prompts. The agent streamlines journey creation, allowing marketers to focus on strategy rather than technical configuration.</p>
<p><a href="https://experienceleague.adobe.com/it/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent#journey-create-agent-skill-overview-and-user-guide" target="_blank">Learn more</a></p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13747">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-95142">Link to PRODUCT JIRA task</a></p>
<p>Availability date: January 12, 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>New API to retrieve Action Campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new <strong>Journey Optimizer API</strong> is now available, enabling you to programmatically retrieve and inspect campaign-related data such as details, versions, and configurations.</p>
<p>For more information, refer to the <a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/">detailed documentation</a>.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13506">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-96195">Link to PRODUCT JIRA task</a></p>
<p>Availability date: November 24, 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>New journey alerts</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Three new <strong>journey alerts</strong> are now available to help you monitor and track journey lifecycle events and custom action performance:</p>
<ul>
<li><strong>Journey Published</strong>: Receive notifications when a journey is published by a practitioner in the journey canvas.</li>
<li><strong>Journey Finished</strong>: Get alerts when a journey has finished, with specific definitions based on journey type (Read Audience or Event-triggered).</li>
<li><strong>Custom Action Capping Triggered</strong>: Be notified when capping is activated on a custom action endpoint.</li>
</ul>
<p>These alerts can be subscribed to at the organization level or for specific journeys.</p>
<p>For more information, refer to the <a href="../reports/alerts.md#journey-alerts">detailed documentation</a>.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13465">Link to DOCAC JIRA task</a></p>
<p>Availability date: November 5, 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Themes in the Email Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now quickly apply <strong>pre-approved themes</strong> to ensure brand consistency across all emails, speed up your campaign creation process, and independently produce high-quality emails while reducing dependency on design teams.</p>
<p>Previously released in beta version, this capability is now available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<img src="assets/do-not-localize/themes.gif">
<p>For more information, refer to the <a href="../email/apply-email-themes.md">detailed documentation</a>.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-12941">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/NEO-88838">Link to PRODUCT JIRA task</a></p>
<p>Availability date: November 5, 2025</p>
</td>
</tr>
</tbody>
</table>

### Improvements {#jan-26-01-improv}

Improvements coming with this release are listed below.

#### AI

* **AI Assistant Content Quality Checks** - In addition to brand alignment, you can now evaluate overall <strong>content quality</strong> to uncover potential issues with readability, cohesiveness, and effectiveness, independent of your brand guidelines. These automated checks help identify unclear messaging, inconsistent tone, or structural gaps.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13917">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-103238">Link to PRODUCT JIRA task</a>
* **Update brands with new color tab** - Brand guidelines help ensure your brand is presented consistently across all touchpoints. The new <strong>Colors section</strong> defines the standards for your brand's color system, outlining how colors are selected, organized, and applied across experiences. It ensures consistent use of primary, secondary, accent, and neutral colors to support a cohesive, accessible, and recognizable brand identity.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13811">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-121183">Link to PRODUCT JIRA task</a>

#### Campaigns

* **Schedule Campaign using Profile Time Zone** - Campaign scheduling can now use each profile's <strong>time zone</strong> to deliver messages at the intended local time.

  **Note**: This improvement is only available for a set of organizations (Limited Availability).
  <a href="https://jira.corp.adobe.com/browse/DOCAC-11534">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-43782">Link to PRODUCT JIRA task</a>

#### Channels

* **SMS Webhooks: Phase II** - Description to be provided.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13978">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-93914">Link to PRODUCT JIRA task</a>

#### Email Designer

* **In-place corrections in the Email designer** - <strong>AI-powered automatic content suggestions</strong> are now available in the Email Designer when violations are detected during content validation. If content is flagged as misaligned with brand guidelines or fails quality criteria, the system proactively generates corrected alternatives that can be reviewed and applied inline, improving compliance and accelerating production.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13979">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-95365">Link to PRODUCT JIRA task</a>

#### Experience Decisioning

* **Self-service migration tooling APIs** - A new set of <strong>migration tooling APIs</strong> is available to migrate Offer management entities to Experience Decisioning. The tooling enables seamless migration between sandboxes with dependency resolution and rollback capabilities.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13837">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-109695">Link to PRODUCT JIRA task</a>

* **Attach fragments to decision items** - Journey Optimizer now provides the ability to attach <strong>fragments</strong> to decision items which can be leveraged in code-based experience campaigns through decision policies.

  **Note**: Previously released in Limited Availability, this improvement is now available to all environments (General Availability).
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13418">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-110282">Link to PRODUCT JIRA task</a>

#### Journeys

* **Leverage a failure response payload in journey Custom Actions** - You can now define an optional <strong>error response payload</strong> for custom actions. When a call fails, the error payload is exposed in the journey context and is available in the timeout/error branch to support richer fallback logic and debugging.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13977">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-113125">Link to PRODUCT JIRA task</a>

* **Combine native and Adobe Campaign message actions** - Journey Optimizer now lets you combine Adobe Campaign v7/v8 message actions with native channel actions in the same journey.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13974">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-113103">Link to PRODUCT JIRA task</a>

* **Journey payload size validation in journeys** - Journey Optimizer now provides <strong>payload size validation</strong> to help ensure optimal performance and system stability. When building or publishing journeys, you receive clear warnings and errors if payload sizes approach or exceed recommended limits, along with actionable guidance to optimize your journey configuration. This proactive validation helps you identify potential issues early and maintain journey performance.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13840">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-122236">Link to PRODUCT JIRA task</a>

* **Multiple inbound actions in journeys** - To simplify your journey orchestration, you can now define <strong>multiple inbound actions</strong> in a single journey. Previously available in campaigns, this capability enables you to deliver multiple code-based experiences, In-app messages, Content Cards or web actions to different locations at the same time, each action containing a specific content.

  **Note**: Previously released in Limited Availability, this improvement is now available to all environments (General Availability).
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13453">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-111916">Link to PRODUCT JIRA task</a>

#### Orchestrated campaigns

* **Select attributes and copy distribution values** - You can now select or copy values directly from the distribution of values view in orchestrated campaigns.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13973">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-105244">Link to PRODUCT JIRA task</a>

* **Data usage label inheritance for audiences** - <strong>Data usage labels</strong> applied in Adobe Experience Platform now automatically carry over when saving audiences in orchestrated campaigns, reducing manual DULE tagging.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13972">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-120769">Link to PRODUCT JIRA task</a>

* **Predefined retargeting filters** - To support easier retargeting for orchestrated campaign use cases, this release introduces new <strong>retargeting filters</strong>. These filters let you directly target audiences based on message engagement, such as sent, opened only, opened or clicked, or opened and clicked, and select the specific campaign or in-transition campaign you want to retarget.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13971">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-116701">Link to PRODUCT JIRA task</a>

* **Predefined filters with parameters** - You can now create <strong>filters with parameters</strong> in orchestrated campaigns for reusable, editable rules.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13970">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-115431">Link to PRODUCT JIRA task</a>

* **Message confirmation before send** - A <strong>confirmation step</strong> is now enabled by default before sending orchestrated campaigns to reduce accidental sends.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13927">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-87219">Link to PRODUCT JIRA task</a>

* **User-generated metadata support** - The <strong>executionMetadata helper function</strong> is now available in the personalization editor for Orchestrated Campaigns, enabling you to attach contextual information to any native action and store it in a dataset for export to external systems.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13923">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-112697">Link to PRODUCT JIRA task</a>

* **Restart button** - Orchestrated campaigns now include a <strong>restart button</strong> so you can quickly re-launch runs when needed before publishing the campaign.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13920">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-106020">Link to PRODUCT JIRA task</a>

* **Rate control support** - Orchestrated campaigns now support <strong>rate control</strong> to help you pace deliveries and align with volume constraints.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13764">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-113254">Link to PRODUCT JIRA task</a>

#### Permissions

* **Prevent self-approval for journeys and campaigns** - You can now require that creators cannot approve their own journeys or campaigns, improving <strong>separation of duties</strong> in approval workflows.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13472">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-99957">Link to PRODUCT JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-95676">Link to PRODUCT JIRA task</a>

## Coming soon {#jan-26-01-coming-soon}

In the next few days, the following capabilities and enhancements are scheduled for release. **Information is subject to change**. Updated links, screens, and documentation will be shared once these updates are live in production.

<table>
<thead>
<tr>
<th><strong>Content generation within Journey Agent</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Powered by Adobe Experience Platform Agent Orchestrator, <strong>Journey Agent</strong> is available in Journey Optimizer and enables you to analyze journeys through a natural language interface. You can now also generate and manage channel-specific content directly in Journey Agent, creating content for channels such as email and push, applying and previewing templates, refining tone and style through prompts, and opening content in Content Designer for in-context editing.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13980">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-111882">Link to PRODUCT JIRA task</a></p>
<p>Availability date: February 2, 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Content decision activity</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now include <strong>personalized offers</strong> in your journeys through a dedicated Content decision activity in the journey canvas, and use them in journey activities, including conditions and custom actions.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-12902">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-99223">Link to PRODUCT JIRA task</a></p>
<p>Availability date: February 3, 2026</p>
</td>
</tr>
</tbody>
</table>
-->
