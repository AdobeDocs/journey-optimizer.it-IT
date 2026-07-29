---
solution: Journey Optimizer
product: journey optimizer
title: Note pre-release per Journey Optimizer
description: Note pre-release di Adobe Journey Optimizer
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
hide: true
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2: id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: af90368835866c2779e36a98f8aa8cb7a39d8ad4
workflow-type: tm+mt
source-wordcount: 1630
ht-degree: 15%

---


# Note pre-release {#e-release-notes}

Adobe Journey Optimizer offre continuamente nuove funzioni, miglioramenti a quelle esistenti e correzioni di bug. Nell’ultima settimana di ogni mese, tutte le modifiche vengono consolidate nelle [note sulla versione](release-notes.md).

<!--
## June '26 pre-release notes {#june-26-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published once changes are live in production. While most changes are delivered on the release date, a few may roll out later — refer to the Availability Date listed for each entry for details.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: June 16-17, 2026

### Journeys {#june-26-journeys}

The following capabilities and improvements are coming to journeys in this release.

<table>
<thead>
<tr>
<th><strong>Channel optimization (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add multiple outbound channels (Email, Push, SMS) to a single journey action and let Journey Optimizer automatically deliver through the best channel for each customer. Three optimization modes are available: manual ranking, customer profile preference (XDM attribute), and AI model-based ranking using propensity scores. When the top-ranked channel is unavailable, the system falls back to the next available channel.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../building-journeys/channel-optimization.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>

* **Increased live journey limit and new guardrails** - You can now have up to **200 active journeys**, increased from the previous limit of 100.



### Orchestrated campaigns {#june-26-oc}

The following capabilities and improvements are coming to orchestrated campaigns in this release.

-->

## Note pre-release del 26 luglio {#july-26-rn}

**Le note pre-release riportate di seguito sono soggette a modifica senza preavviso fino alla data di disponibilità della versione**. I collegamenti, le schermate e la documentazione aggiornata vengono pubblicati una volta che le modifiche saranno disponibili in produzione. Anche se la maggior parte delle modifiche viene consegnata nella data di rilascio, alcune potrebbero essere implementate in un secondo momento.

Consulta anche [Note pre-release di Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Data di rilascio**: 28-29 luglio 2026

<!--

### Onboarding {#july-26-onboarding}

Journey Optimizer introduces the Onboarding Assistant, a new capability in this release.

<table>
<thead>
<tr>
<th><strong>Onboarding Assistant</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Transitioning to Adobe Journey Optimizer from another marketing platform is easier with guided capabilities that help you move existing email content and journeys into Journey Optimizer. A dedicated workspace lets you reuse what you have instead of rebuilding from scratch.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<GIF placeholder: to be added>
<Documentation link: TBD>
</td>
</tr>
</tbody>
</table>

-->

### Percorsi {#july-26-journeys}

Il seguente miglioramento è stato aggiunto ai percorsi in questa versione.

* **Tipi di pubblico esterni nella simulazione del Percorso** - La simulazione del Percorso ora supporta i tipi di pubblico esterni. Quando simuli percorsi che eseguono il targeting di tipi di pubblico CSV o Federated Audience Composition, puoi simulare gli attributi di arricchimento di tali tipi di pubblico direttamente tramite il modulo di interfaccia utente o un’importazione JSON. L’interfaccia utente mostra in modo dinamico solo gli attributi di arricchimento specifici utilizzati nella logica di percorso, consentendo la convalida precisa dei rami decisionali e delle regole di personalizzazione prima della pubblicazione. <!-- Documentation link: TBD -->

### Campagne {#july-26-campaigns}

In questa versione sono state aggiunte alle campagne le funzionalità e i miglioramenti seguenti.

<table>
<thead>
<tr>
<th><strong>Allegati PDF personalizzati in e-mail attivate da API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ora supporta l’associazione di fino a cinque PDF specifici per destinatario per e-mail nelle campagne attivate da API. I file PDF vengono recuperati in modo sicuro dall’archiviazione di Azure o AWS e allegati al momento dell’invio, con la posizione di ciascun file passata direttamente nel payload API. Questo consente ai sistemi di generazione dei documenti esistenti a monte di rimanere operativi, con la gestione della distribuzione da parte di Journey Optimizer.</p>
<p>I casi d’uso supportati includono fatture, estratti conto, biglietti, contratti, etichette di spedizione e documenti simili che variano a seconda del destinatario. Gli allegati PDF personalizzati sono disponibili solo nelle campagne attivate da API e non sono supportati nei percorsi o in altri tipi di campagne (azione, orchestrato).</p>
<p>Volumi e dimensioni di allegati più grandi sono supportati tramite il componente aggiuntivo per allegati di PDF; per informazioni, contatta il rappresentante Adobe.</p>
<p></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Simulazione dell’esperienza in entrata nelle campagne di azione</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi simulare azioni del canale in entrata nelle campagne Azione prima di andare "live". Utilizza la modalità di simulazione per verificare la configurazione con utenti simulati e visualizzare in anteprima l’esperienza di cui è stato eseguito il rendering, inclusi un URL generato e un codice QR, in modo da poter convalidare regole, decisioni e rendering end-to-end dei contenuti.</p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Cartelle per campagne** - È ora possibile organizzare le campagne in cartelle per migliorare la navigazione e la gestione nell&#39;interfaccia. Questa funzionalità è disponibile solo per campagne attivate da API e azioni. <!-- Documentation link: TBD -->

* **Escludi il campo di esecuzione predefinito nelle campagne**. Precedentemente disponibile a livello di percorso, ora puoi sovrascrivere il campo di esecuzione predefinito impostato a livello globale per le consegne e-mail, SMS e WhatsApp nei parametri della campagna. <!-- Documentation link: TBD -->

* **Punteggio di allineamento del brand nella dashboard di Campaign**: ora puoi valutare il punteggio di allineamento del brand direttamente all’interno della dashboard di Campaign, per garantire che il contenuto rimanga in linea con il brand. Questo consente di verificare le linee guida immediatamente senza dover aprire la finestra di progettazione del contenuto. <!-- Documentation link: TBD -->

### Campagne orchestrate {#july-26-oc}

In questa versione sono stati aggiunti i seguenti miglioramenti alle campagne orchestrate.

* **Autorizzazione per la visualizzazione delle transizioni di una campagna orchestrata** - Aggiunta nuova autorizzazione **Visualizza transizioni campagna orchestrate** per sostituire l&#39;opzione legacy **Visualizza file in campagne orchestrate**. Questa modifica ti consente di nascondere i risultati dell’anteprima nelle transizioni della campagna per supportare la conformità con le informazioni che consentono l’identificazione personale.

<!--
* **Send messages in waves** - You can now schedule outbound messages from orchestrated campaigns to be delivered in controlled batches over time. Ideal for high-volume or time-sensitive campaigns, wave sending also supports better deliverability and helps maintain a strong sender reputation by reducing the risk of being flagged as spam.
-->

<!--
### Optimization {#july-26-optimization}

<table>
<thead>
<tr>
<th><strong>Channel optimization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now configure a journey or campaign action to include multiple outbound channels (Email, Push, SMS) and let Journey Optimizer automatically deliver through the best channel for each customer. Three optimization modes are available:</p>
<ul>
<li>Manual ranking: specify your preferred channel order.</li>
<li>Customer preference: use the customer's preferred channel from their profile (Experience Data Model Consents & Preferences attribute).</li>
<li>AI model-based ranking: use machine learning propensity scores to infer the most effective channel per customer.</li>
</ul>
<p>When the top-ranked channel is unavailable (not opted-in, frequency-capped, or not configured), the system falls back to the next available channel.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
</td>
</tr>
</tbody>
</table>
-->

<!--
<table>
<thead>
<tr>
<th><strong>Quiet Hours support for orchestrated campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now apply quiet hours to Orchestrated campaigns. Quiet hours let you define time-based exclusions to prevent messages from being sent during specific periods, helping you respect customer preferences and compliance requirements across campaign orchestration use cases.</p>
<Documentation link: TBD>
</td>
</tr>
</tbody>
</table>

* **Ability to Manage Profile Target Dimensions** - You can now delete a Profile Target Dimension or edit and swap its configured identity namespace, providing greater control and flexibility over your data setups.

* **Support for Line** - You can now add LINE actions directly into your Orchestrated campaigns. This new activity allows you to build and deliver highly personalized content, including text, stickers, images, videos, location data, and rich Flex Messages, to engage your customers seamlessly on the LINE platform. This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.

* **New Orchestrated campaigns public APIs** - New API specifications are now available for Orchestrated campaigns. These APIs allow you to programmatically create, manage, and trigger orchestrated campaigns, enabling deeper integration with external systems and automation pipelines.

* **Personalize email sender details per recipient and campaign** - Orchestrated campaigns now support personalization of email header fields, including From name, From address, and Reply-To, using profile attributes or relational data. This allows sender details to reflect the relevant advisor, location, or branch for each recipient, rather than routing all sends through a single corporate address. Header values can be set at the channel level and overridden per campaign using contextual data for more precise control. Documentation link: TBD

* **Target dimension simplification in Orchestrated campaigns** - The active targeting dimension is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.

-->

### Canali {#july-26-channels}

In questa versione sono state aggiunte le seguenti funzionalità e miglioramenti ai canali.

<table>
<thead>
<tr>
<th><strong>Canale in uscita personalizzato</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer introduce ora i canali personalizzati, una nuova funzionalità che consente agli amministratori di portare qualsiasi canale di messaggistica in uscita basato su HTTP, come WeChat, Kakao Talk, Messenger o un provider proprietario, direttamente in Journey Optimizer tramite un Channel Builder senza codice.</p >
<p>Una volta configurati, i canali personalizzati sono disponibili tra campagne, percorsi e campagne orchestrate, con le stesse funzionalità complete dei canali nativi: personalizzazione con editor di espressioni, sperimentazione dei contenuti, anteprima e bozza, reporting preconfigurato e applicazione del consenso e della governance.</p>
<p>Questo risolve un vuoto precedentemente affrontato dalle azioni personalizzate, limitate solo ai percorsi e prive di funzionalità di canale dedicate.</p>
<p>I canali in uscita personalizzati sono attualmente disponibili come Disponibilità limitata. Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Canale WhatsApp: supporto modelli di flusso WhatsApp** - È ora possibile inviare modelli di flusso WhatsApp in Adobe Journey Optimizer per fornire esperienze interattive multischermo come sondaggi e acquisizione di lead. Le risposte vengono acquisite al momento dell’invio e memorizzate come payload JSON non elaborati nel nuovo set di dati evento di tracciamento del canale di Journey Optimizer. <!-- Documentation link: TBD -->

* **Componente aggiuntivo Prestazioni per velocità effettiva - Push** - È disponibile una nuova modalità di messaggistica transazionale a velocità effettiva elevata nelle campagne attivate dall&#39;API. Questa modalità è progettata per la messaggistica transazionale in tempo reale su larga scala e supporta fino a 5.000 transazioni al secondo con maggiore disponibilità. Precedentemente disponibile solo per il canale e-mail, questa funzionalità è ora disponibile anche per il canale push, per le organizzazioni che hanno acquistato il componente aggiuntivo Messaggistica transazionale ad alta velocità di Adobe. Per ulteriori informazioni, contatta il rappresentante Adobe. <!-- Documentation link: TBD -->

* **Integrazioni provider personalizzato migliorate - Dispositivi mobili** - Le integrazioni provider personalizzato offrono ora maggiore flessibilità con messaggi chiave e aggiornamenti di intestazione:

  * Personalizzazione intestazione: ora puoi modificare il valore predefinito dell’intestazione Content-Type e aggiungere fino a 10 parametri di intestazione personalizzati.

  * Supporto del payload SMS: è stato aggiunto il supporto per le funzioni helper di Adobe Journey Optimizer all’interno del payload SMS, incluso encode64.

### Funzione Decisioni {#july-26-decisioning}

In questa versione sono stati aggiunti i seguenti miglioramenti a Decisioning.

* **Personalization a livello di offerta** - Gli attributi personalizzati dell&#39;elemento di decisione possono ora essere personalizzati al momento della consegna utilizzando dati di profilo, contestuali e di pubblico. Questo elimina la necessità di mantenere offerte duplicate per varianti di contenuto minori, consentendo agli addetti al marketing di gestire meno elementi decisionali e più flessibili. <!-- Documentation link: TBD -->

<!--
* **Placement-level frequency capping in Decisioning** - Frequency capping rules in Decisioning can now be scoped to individual placements, giving you finer control over how often an offer is shown in a given surface. Two modes are available: placement-specific capping (define a cap that applies only when the offer is displayed in a selected placement) and per-placement capping (apply a cap independently across every placement where the offer appears, so each placement maintains its own capping counter). Documentation link: TBD
-->

### Gestione dei contenuti {#july-26-content}

In questa versione sono stati aggiunti i seguenti miglioramenti alla gestione dei contenuti.

* Supporto di **Frammenti di espressione in `<head>` di modelli e-mail** - I frammenti di espressione possono ora essere utilizzati in `<head>` di modelli e-mail. Questo consente di centralizzare lo stile o qualsiasi codice personalizzato in un singolo frammento e riutilizzarlo in più modelli. Quando un frammento viene aggiornato e ripubblicato, tutte le e-mail create da modelli che vi fanno riferimento ereditano automaticamente il codice più recente, eliminando la necessità di aggiornare manualmente ogni e-mail singolarmente. <!-- Documentation link: TBD -->

* **&quot;Assistente IA&quot; rinominato in &quot;Genera contenuto&quot;** - L&#39;Assistente IA è stato rinominato in &quot;Genera contenuto&quot; in Adobe Journey Optimizer. Questo aggiornamento è limitato alla denominazione e alla terminologia; non sono state introdotte modifiche funzionali. Le etichette di navigazione, i pulsanti, i menu e le finestre di dialogo per la generazione di contenuti, la generazione di immagini, le espressioni di personalizzazione e la sperimentazione di contenuti sono stati rinominati da &quot;Assistente IA&quot; a &quot;Genera contenuto&quot;. <!-- Documentation link: TBD -->

* **Origine immagini flessibile per la generazione di contenuti AI** - La generazione di contenuti in Journey Optimizer ora genera immagini approvate dal marchio direttamente da Adobe Experience Manager Assets Essentials e versioni successive. Il bilanciamento è controllato da tre modalità: Assets (Digital Asset Management, di origine predefinita), Balanced (Digital Asset Management-first, AI riempie i vuoti) e Creative (AI-first). In questo modo ogni elemento visivo sarà accurato, conforme al marchio e pronto per la produzione per percorsi e campagne. <!-- Documentation link: TBD -->

* **Miglioramenti multilingue** - Le impostazioni della lingua possono ora essere duplicate da un&#39;impostazione attiva esistente, pertanto non è più necessario ricreare completamente una configurazione per apportare modifiche. È inoltre possibile copiare una condizione da una lingua a un&#39;altra durante la creazione di Impostazioni lingua, semplificando la configurazione di siti con molte lingue.

<!--
### Integrations {#july-26-integrations}

The following improvements have been added to integrations in this release.

* **Real-time countdown timers for Adobe Experience Manager Dynamic Media integration** - Marketers can now build countdown timers as Dynamic Media templates in Adobe Experience Manager and pull them directly into Journey Optimizer. Timers render live at the moment of open, so every recipient sees an accurate countdown, not a static image. Configure dates, styling, and fallback values right within the Journey Optimizer editor to power flash sales and limited-time offers. [Documentation link: TBD]
-->

### Personalizzazione {#july-26-personalization}

In questa versione sono stati aggiunti i seguenti miglioramenti alla personalizzazione.

* **Gestione dei domini per la personalizzazione URL completa/di base** - È ora possibile creare e gestire i domini approvati per la personalizzazione URL completa e di base direttamente dalle impostazioni di amministrazione in Adobe Journey Optimizer, senza dover contattare il supporto Adobe. <!-- Documentation link: TBD -->

<!-- Documentation link: TBD -->

### E-mail designer {#july-26-email}

In questa versione è stata aggiunta la seguente funzionalità al canale e-mail.

<table>
<thead>
<tr>
<th><strong>Moduli in E-mail designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>E-mail designer ora include una libreria di moduli di layout pronti all’uso, ad esempio intestazioni, schede di prodotto, blocchi di informazioni e piè di pagina, che puoi trascinare direttamente nell’area di lavoro dell’e-mail.</p>
<p>Ogni modulo è preconfigurato con proprietà modificabili (immagine, titolo, testo, pulsante, collegamenti) e può essere completamente personalizzato tramite l’interfaccia WYSIWYG, velocizzando la creazione delle e-mail senza richiedere di creare strutture da zero.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>


### Amministrazione {#july-26-administration}

In questa versione sono state aggiunte le seguenti funzionalità di amministrazione.

<table>
<thead>
<tr>
<th><strong>Inserimento di IP nella whitelist di Web Application Firewall</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer ora supporta l’inserimento di IP nella whitelist di Web Application Firewall per le pagine di destinazione, consentendo alle organizzazioni di applicare che tutte le richieste in ingresso vengano instradate esclusivamente tramite l’infrastruttura configurata di Web Application Firewall. Con questo miglioramento, i clienti possono configurare Journey Optimizer per rifiutare qualsiasi richiesta diretta che aggiri il livello di firewall dell’applicazione web, garantendo che i criteri di sicurezza definiti in strumenti come Imperva vengano applicati in modo coerente.</p>
<p>Questa funzionalità rafforza la postura di sicurezza per le aziende con requisiti di accesso alla rete rigorosi, offrendo loro il pieno controllo del flusso di traffico verso le pagine di destinazione ospitate da Journey Optimizer.</p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### Miglioramenti dell’usabilità {#july-26-usability}

In questa versione sono disponibili i seguenti miglioramenti a livello di usabilità.

* **Scelte rapide per l&#39;avvio dei canali SMS, Push, In-App e Codebase nei modelli di contenuto** - Il pulsante **Altre azioni** nell&#39;elenco dei modelli di contenuto ora fornisce ulteriori scelte rapide specifiche per il canale. Per i modelli SMS, modifica rapidamente il messaggio o controlla il numero di caratteri o i segmenti. Per i modelli push, modifica il titolo, il corpo o il contenuto multimediale. Per i modelli in-app, modifica l’intestazione del messaggio, il corpo del messaggio o l’URL del file multimediale. Per i modelli di canale Codebase, modifica direttamente il codice. Queste scelte rapide estendono le scelte rapide per l’avvio rapido del canale e-mail già disponibili. <!-- Documentation link: TBD -->

* **Nuova esperienza di simulazione del contenuto per il test del contenuto** - Il flusso di lavoro **Simula contenuto** introduce un&#39;esperienza riprogettata: tutte le varianti ora vengono riprodotte insieme in un&#39;unica griglia scorrevole (layout affiancati, sovrapposti o a capo), sostituendo la visualizzazione una variante alla volta. Una singola barra delle azioni inferiore consolida la navigazione tra le varianti di test, lo zoom, la commutazione del riquadro di visualizzazione (desktop/mobile), la commutazione delle impostazioni locali, l’aggiunta di input di esempio, la generazione di varianti con IA, il prelievo e il salvataggio di utenti simulati e l’importazione o l’esportazione di varianti. Rimuovendo la barra a sinistra e comprimendo i livelli di intestazione aggiuntivi, le anteprime avranno molto più spazio. L&#39;opzione **Passa all&#39;esperienza classica** nella barra delle azioni inferiore consente di ripristinare l&#39;esperienza precedente in qualsiasi momento. <!-- Documentation link: TBD -->
