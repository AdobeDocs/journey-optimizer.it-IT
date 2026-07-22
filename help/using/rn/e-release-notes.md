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
source-git-commit: 2fdc3176a79289ef505f1a8c974810f97f048f6a
workflow-type: tm+mt
source-wordcount: 2470
ht-degree: 19%

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




### Orchestrated campaigns {#june-26-oc}

The following capabilities and improvements are coming to orchestrated campaigns in this release.

-->

## Note pre-release del 26 luglio {#july-26-rn}

**Le note pre-release riportate di seguito sono soggette a modifica senza preavviso fino alla data di disponibilità della versione**. I collegamenti, le schermate e la documentazione aggiornata vengono pubblicati una volta che le modifiche saranno disponibili in produzione. Anche se la maggior parte delle modifiche viene consegnata nella data di rilascio, alcune potrebbero essere implementate in un secondo momento.

Consulta anche [Note pre-release di Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Data di rilascio**: 28 luglio 2026

### Fedeltà {#july-26-loyalty}

Journey Optimizer introduce la fidelizzazione, una nuova funzionalità di questa versione.

<table>
<thead>
<tr>
<th><strong>Sfide di fedeltà</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le sfide della fedeltà trasformano le iniziative della fedeltà in esperienze coinvolgenti e gamified che motivano i clienti a intraprendere azioni di valore, come fare acquisti, scrivere recensioni, impegnarsi sui social media o fare riferimento ad amici.</p>
<p>Gli amministratori possono utilizzare il menu di amministrazione Fedeltà per collegare Journey Optimizer al tuo ecosistema di fidelizzazione, incluse le API di assegnazione dei premi, le definizioni degli eventi, l’inventario dei prodotti, le esclusioni e le impostazioni di identità. Gli addetti al marketing possono quindi progettare problematiche standard, in streaming o sequenziali, definire attività e premi, distribuire schede di contenuti e messaggi di branding e monitorare le prestazioni con dashboard di reporting integrate. Journey Optimizer genera i percorsi che orchestrano ogni sfida in background, in modo che i team possano concentrarsi sulla customer experience e sugli obiettivi aziendali.</p>
<!-- GIF placeholder: to be added -->
<p>Jira: <a href="https://jira.corp.adobe.com/browse/DOCAC-14019">DOCAC-14019</a></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### Formazione iniziale {#july-26-onboarding}

Journey Optimizer presenta Onboarding Hub, una nuova funzionalità disponibile in questa versione.

<table>
<thead>
<tr>
<th><strong>Hub di onboarding</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La transizione da un’altra piattaforma di marketing a Adobe Journey Optimizer è ora più semplice e veloce. Il nuovo hub di onboarding presenta un’area di lavoro di migrazione che consente di importare automaticamente il contenuto e i percorsi e-mail esistenti, evitando di doverli ricreare da zero.</p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<!-- GIF placeholder: to be added -->
<p>Jira: <a href="https://jira.corp.adobe.com/browse/DOCAC-15180">DOCAC-15180</a></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### Percorsi {#july-26-journeys}

In questa versione sono stati aggiunti i seguenti miglioramenti ai percorsi e le seguenti funzioni.

<table>
<thead>
<tr>
<th><strong>Ottimizzazione dei canali</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi configurare un’azione del percorso in modo da includere più canali in uscita (e-mail, push, SMS) e consentire a Journey Optimizer di distribuire automaticamente attraverso il canale migliore per ogni cliente. Sono disponibili tre modalità di ottimizzazione:</p>
<ul>
<li>Classificazione manuale: specifica l’ordine del canale preferito.</li>
<li>Preferenza del cliente: utilizza il canale preferito del cliente dal suo profilo (attributo Consensi e preferenze del modello di dati esperienza).</li>
<li>Classificazione basata su modello di intelligenza artificiale: utilizza i punteggi di propensione di apprendimento automatico per dedurre il canale più efficace per cliente.</li>
</ul>
<p>Quando il canale di livello più alto non è disponibile (non è prescelto, con limiti di frequenza o non è configurato), il sistema torna al canale successivo disponibile.</p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<p>Jira: <a href="https://jira.corp.adobe.com/browse/DOCAC-14900">DOCAC-14900</a></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Supporto di documenti di tipi di pubblico esterni (valori separati da virgole e Composizione di pubblico federato) nella simulazione di Percorso** - La simulazione di Percorso ora supporta i tipi di pubblico esterni. Durante la simulazione di percorsi che eseguono il targeting di valori separati da virgole o di tipi di pubblico con composizione di pubblico federato, puoi simulare gli attributi di arricchimento di tali tipi di pubblico direttamente tramite il modulo di interfaccia utente o un’importazione JSON. L’interfaccia utente mostra in modo dinamico solo gli attributi di arricchimento specifici utilizzati nella logica di percorso, consentendo la convalida precisa dei rami decisionali e delle regole di personalizzazione prima della pubblicazione. ([DOCAC-15074](https://jira.corp.adobe.com/browse/DOCAC-15074)) <!-- Documentation link: TBD -->

* **Date di inizio e di fine nell&#39;intestazione del percorso** - Quando le date di inizio e/o di fine sono configurate in un percorso attivo, ora vengono visualizzate nell&#39;intestazione del percorso accanto al badge di stato attivo. L’etichetta visualizzata si adatta a seconda che ogni data sia imminente o già passata. ([DOCAC-14702](https://jira.corp.adobe.com/browse/DOCAC-14702)) <!-- Documentation link: TBD -->

### Campagne orchestrate {#july-26-oc}

In questa versione sono state aggiunte alle campagne orchestrate le funzioni e i miglioramenti seguenti.

<table>
<thead>
<tr>
<th><strong>Supporto di Quiet Hours per campagne orchestrate</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi applicare ore non interattive alle campagne orchestrate. Le ore tranquille ti consentono di definire esclusioni basate sul tempo per impedire l’invio di messaggi durante periodi specifici, aiutandoti a rispettare le preferenze dei clienti e i requisiti di conformità in tutti i casi di utilizzo dell’orchestrazione delle campagne.</p>
<p>Jira: <a href="https://jira.corp.adobe.com/browse/DOCAC-14054">DOCAC-14054</a></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Campagne di azione modalità simulazione canali in entrata</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi simulare azioni del canale in entrata nelle campagne Azione prima di andare "live". Utilizza la modalità di simulazione per verificare la configurazione con utenti simulati e visualizzare in anteprima l’esperienza di cui è stato eseguito il rendering, inclusi un URL generato e un codice QR, in modo da poter convalidare regole, decisioni e rendering end-to-end dei contenuti.</p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<!-- GIF placeholder: to be added -->
<p>Jira: <a href="https://jira.corp.adobe.com/browse/DOCAC-15166">DOCAC-15166</a></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Possibilità di gestire le dimensioni di destinazione del profilo** - È ora possibile eliminare un Dimension di destinazione del profilo o modificare e scambiare lo spazio dei nomi delle identità configurato, fornendo un maggiore controllo e flessibilità sulle impostazioni dei dati. ([DOCAC-15018](https://jira.corp.adobe.com/browse/DOCAC-15018)) <!-- Documentation link: TBD -->

* **Autorizzazione per la visualizzazione delle transizioni di una campagna orchestrata** - Aggiunta nuova autorizzazione **Visualizza transizioni campagna orchestrate** per sostituire l&#39;opzione legacy **Visualizza file in campagne orchestrate**. Questa modifica ti consente di nascondere i risultati dell’anteprima nelle transizioni della campagna per supportare la conformità con le informazioni che consentono l’identificazione personale. ([DOCAC-14924](https://jira.corp.adobe.com/browse/DOCAC-14924)) <!-- Documentation link: TBD -->

* **Supporto per la riga** - È ora possibile aggiungere azioni LINE direttamente nelle campagne orchestrate. Questa nuova attività ti consente di creare e distribuire contenuti altamente personalizzati, tra cui testo, adesivi, immagini, video, dati sulla posizione e messaggi Flex avanzati, per coinvolgere i tuoi clienti in modo semplice sulla piattaforma LINE. Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe. ([DOCAC-14905](https://jira.corp.adobe.com/browse/DOCAC-14905)) <!-- Documentation link: TBD -->

* **API pubbliche di nuove campagne orchestrate** - Sono ora disponibili nuove specifiche API per le campagne orchestrate. Queste API consentono di creare, gestire e attivare in modo programmatico campagne orchestrate, consentendo una più profonda integrazione con sistemi esterni e pipeline di automazione. ([DOCAC-14308](https://jira.corp.adobe.com/browse/DOCAC-14308)) <!-- Documentation link: TBD -->

* **Personalizzazione dei dettagli del mittente e-mail per destinatario e campagna** - Le campagne orchestrate ora supportano la personalizzazione dei campi dell&#39;intestazione e-mail, inclusi Nome mittente, Indirizzo mittente e Risposta, utilizzando gli attributi del profilo o i dati relazionali. Questo consente ai dettagli del mittente di riflettere l’esperto, la posizione o la filiale relativa a ciascun destinatario, anziché instradare tutti gli invii tramite un unico indirizzo aziendale. I valori dell’intestazione possono essere impostati a livello di canale e sostituiti per campagna utilizzando dati contestuali per un controllo più preciso. ([DOCAC-13761](https://jira.corp.adobe.com/browse/DOCAC-13761)) <!-- Documentation link: TBD -->

* **Semplificazione della dimensione di destinazione nelle campagne orchestrate** - La dimensione di targeting attiva viene ora visualizzata nell&#39;area di lavoro del flusso di lavoro, per consentirti di vedere quale dimensione viene utilizzata da un&#39;attività di canale. Il flusso di segmentazione tra più entità è più semplice in quanto non è più necessaria un’attività &quot;Modifica dimensione&quot; separata. Inoltre, ora puoi scegliere esplicitamente se i messaggi vengono inviati a livello di profilo o a un livello di dimensione secondario. ([DOCAC-13554](https://jira.corp.adobe.com/browse/DOCAC-13554)) <!-- Documentation link: TBD -->

### Campagne {#july-26-campaigns}

In questa versione sono state aggiunte alle campagne le funzionalità e i miglioramenti seguenti.

<table>
<thead>
<tr>
<th><strong>Allegato PDF personalizzato per la messaggistica transazionale nelle campagne attivate dall’API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora è possibile allegare fino a cinque PDF dinamici e personalizzati per e-mail nelle campagne transazionali attivate da API, passando le posizioni dei file nel payload dell’API. In questo modo, settori quali l'aviazione possono inviare carte d'imbarco o conferme di viaggio, servizi finanziari per la consegna di fatture o rendiconti personalizzati e vendita al dettaglio per l'inclusione di ricezioni di ordini o etichette di restituzione, ognuno dei quali personalizzato per il destinatario al momento dell'invio.</p>
<p>Gli allegati PDF personalizzati e statici condividono la stessa quota; il superamento del limite di utilizzo corretto richiede il componente aggiuntivo allegato PDF. Questa funzione non è disponibile nelle campagne di percorso o di azione.</p>
<p>Jira: <a href="https://jira.corp.adobe.com/browse/DOCAC-15186">DOCAC-15186</a></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Cartelle per campagne** - È ora possibile organizzare le campagne in cartelle per migliorare la navigazione e la gestione nell&#39;interfaccia. ([DOCAC-15098](https://jira.corp.adobe.com/browse/DOCAC-15098)) <!-- Documentation link: TBD -->

* **Sostituisci il campo di esecuzione predefinito nelle campagne** - Precedentemente disponibile a livello di percorso, ora puoi sostituire nei parametri della campagna il campo di esecuzione predefinito impostato a livello globale per le consegne e-mail, SMS e WhatsApp. ([DOCAC-14718](https://jira.corp.adobe.com/browse/DOCAC-14718)) <!-- Documentation link: TBD -->

* **Punteggio di allineamento del brand nella dashboard di Campaign**: ora puoi valutare il punteggio di allineamento del brand direttamente all’interno della dashboard di Campaign, per garantire che il contenuto rimanga in linea con il brand. Questo consente di verificare le linee guida all’istante, senza il bisogno di aprire il designer contenuti. ([DOCAC-14516](https://jira.corp.adobe.com/browse/DOCAC-14516)) <!-- Documentation link: TBD -->

### Funzione Decisioni {#july-26-decisioning}

In questa versione sono stati aggiunti i seguenti miglioramenti a Decisioning.

* **Creazione di regole di decisione e formule di classificazione da un&#39;espressione in linguaggio naturale** - È ora possibile descrivere la regola di decisione o la formula di classificazione che si desidera creare in linguaggio semplice e consentire all&#39;Assistente IA di generarla automaticamente. Questa funzionalità è disponibile per i clienti che hanno accesso alle funzionalità di Adobe AI. ([DOCAC-15231](https://jira.corp.adobe.com/browse/DOCAC-15231)) <!-- Documentation link: TBD -->

* **Simulazione di regole di decisione e formule di classificazione** - È ora possibile simulare le regole di decisione e le formule di classificazione direttamente dall&#39;editor di regole o formule. Aggiungi varianti di test manuali o generale utilizzando l’intelligenza artificiale, quindi esegui l’espressione in base ai tuoi dati di test per convalidare l’idoneità e rivedere i risultati classificati, il tutto prima di distribuire in produzione. La generazione di varianti è disponibile per i clienti con accesso alle funzionalità di Adobe AI. ([DOCAC-15227](https://jira.corp.adobe.com/browse/DOCAC-15227)) <!-- Documentation link: TBD -->

* **Attributi di offerta dinamici** - Gli attributi personalizzati degli elementi di decisione possono ora essere personalizzati al momento della consegna utilizzando dati di profilo, contestuali e di pubblico. Questo elimina la necessità di mantenere offerte duplicate per varianti di contenuto minori, consentendo ai marketer di gestire meno elementi decisionali e più flessibili. ([DOCAC-14899](https://jira.corp.adobe.com/browse/DOCAC-14899)) <!-- Documentation link: TBD -->

### Gestione dei contenuti {#july-26-content}

In questa versione sono stati aggiunti i seguenti miglioramenti alla gestione dei contenuti.

* Supporto di **Frammenti di espressione in `<head>` di modelli e-mail** - I frammenti di espressione possono ora essere utilizzati in `<head>` di modelli e-mail. Questo consente di centralizzare lo stile o qualsiasi codice personalizzato in un singolo frammento e riutilizzarlo in più modelli. Quando un frammento viene aggiornato e ripubblicato, tutte le e-mail create da modelli che vi fanno riferimento ereditano automaticamente il codice più recente, eliminando la necessità di aggiornare manualmente ogni e-mail singolarmente. ([DOCAC-15257](https://jira.corp.adobe.com/browse/DOCAC-15257)) <!-- Documentation link: TBD -->

* **&quot;Assistente IA&quot; rinominato in &quot;Genera contenuto&quot;** - L&#39;Assistente IA è stato rinominato in &quot;Genera contenuto&quot; in Adobe Journey Optimizer. Questo aggiornamento è limitato alla denominazione e alla terminologia; non sono state introdotte modifiche funzionali. Le etichette di navigazione, i pulsanti, i menu e le finestre di dialogo per la generazione di contenuti, la generazione di immagini, le espressioni di personalizzazione e la sperimentazione di contenuti sono stati rinominati da &quot;Assistente IA&quot; a &quot;Genera contenuto&quot;. ([DOCAC-15230](https://jira.corp.adobe.com/browse/DOCAC-15230)) <!-- Documentation link: TBD -->

* **Origine immagini flessibile per la generazione di contenuti AI** - La generazione di contenuti in Journey Optimizer ora genera immagini approvate dal marchio direttamente da Adobe Experience Manager Assets Essentials e versioni successive. Il bilanciamento è controllato da tre modalità: Assets (Digital Asset Management, di origine predefinita), Balanced (Digital Asset Management-first, AI riempie i vuoti) e Creative (AI-first). In questo modo ogni elemento visivo sarà accurato, conforme al marchio e pronto per la produzione per percorsi e campagne. ([DOCAC-14761](https://jira.corp.adobe.com/browse/DOCAC-14761)) <!-- Documentation link: TBD -->

### Canale e-mail {#july-26-email}

In questa versione sono state aggiunte le seguenti funzionalità al canale e-mail.

<table>
<thead>
<tr>
<th><strong>Moduli in E-mail designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>E-mail designer ora include una libreria di moduli di layout pronti all’uso, ad esempio intestazioni, schede di prodotto, blocchi di informazioni e piè di pagina, che puoi trascinare direttamente nell’area di lavoro dell’e-mail. Ogni modulo è preconfigurato con proprietà modificabili (immagine, titolo, testo, pulsante, collegamenti) e può essere completamente personalizzato tramite l’interfaccia WYSIWYG, velocizzando la creazione delle e-mail senza richiedere di creare strutture da zero.</p>
<!-- GIF placeholder: to be added -->
<p>Jira: <a href="https://jira.corp.adobe.com/browse/DOCAC-14877">DOCAC-14877</a></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### Personalizzazione {#july-26-personalization}

In questa versione sono stati aggiunti i seguenti miglioramenti alla personalizzazione.

* **Gestione dei domini per la personalizzazione URL completa/di base** - È ora possibile creare e gestire i domini approvati per la personalizzazione URL completa e di base direttamente dalle impostazioni di amministrazione in Adobe Journey Optimizer, senza dover contattare il supporto Adobe. ([DOCAC-15187](https://jira.corp.adobe.com/browse/DOCAC-15187)) <!-- Documentation link: TBD -->

* **Nuove funzioni di supporto nelle espressioni di personalizzazione** - Nuove funzioni di supporto sono ora disponibili nelle espressioni di personalizzazione:

  * `appendQueryParams`: aggiunge un parametro di query a un URL o lo sostituisce se la chiave esiste già.
  * `dateBetween`: controlla se una data rientra in un intervallo di date di inizio e fine (incluso).
  * `equalsAnyIgnoreCase`: restituisce true quando una stringa corrisponde a qualsiasi valore specificato, ignorando la distinzione tra maiuscole e minuscole.
  * `getUrlFragment`: estrae la parte frammento di un URL (la parte dopo #).
  * `join`: concatena gli elementi array in una singola stringa utilizzando un separatore.
  * `decode64`: decodifica una stringa con codifica Base64. Se l&#39;input non è un valore Base64 valido, la stringa di input originale viene restituita invariata.

  Anche la funzione `concat` è stata migliorata e ora supporta due o più argomenti.

  Inoltre, sono ora disponibili le seguenti funzioni di migrazione dei modelli per facilitare la migrazione dei modelli esistenti a Journey Optimizer:

  * `ampCompare`: confronta due valori utilizzando l&#39;operatore di confronto specificato.
  * `ampSubstr`: restituisce una porzione di una stringa tra gli indici iniziale e finale specificati.
  * `compareTo`: confronta due stringhe lessicograficamente.

  ([DOCAC-15099](https://jira.corp.adobe.com/browse/DOCAC-15099)) <!-- Documentation link: TBD -->

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
<p>Journey Optimizer introduce ora i canali personalizzati, una nuova funzionalità che consente agli amministratori di portare qualsiasi canale di messaggistica in uscita basato su HTTP, come WeChat, Kakao Talk, Messenger o un provider proprietario, direttamente in Journey Optimizer tramite un Channel Builder senza codice. Una volta configurati, i canali personalizzati sono disponibili per campagne, Percorsi e campagne orchestrate, con le stesse funzionalità complete dei canali nativi: personalizzazione con editor di espressioni, sperimentazione dei contenuti, anteprima e bozze, reporting preconfigurato e applicazione del consenso e della governance. In questo modo è stato colmato il divario precedentemente affrontato dalle azioni personalizzate, limitate ai Percorsi e prive di authoring di contenuti dedicati.</p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<!-- GIF placeholder: to be added -->
<p>Jira: <a href="https://jira.corp.adobe.com/browse/DOCAC-11381">DOCAC-11381</a></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Canale WhatsApp: supporto modelli di flusso WhatsApp** - È ora possibile inviare modelli di flusso WhatsApp in Adobe Journey Optimizer per fornire esperienze interattive multischermo come sondaggi e acquisizione di lead. Le risposte vengono acquisite al momento dell’invio e memorizzate come payload JSON non elaborati nel nuovo set di dati evento di tracciamento del canale di Journey Optimizer. ([DOCAC-15223](https://jira.corp.adobe.com/browse/DOCAC-15223)) <!-- Documentation link: TBD -->

* **Componente aggiuntivo Prestazioni per velocità effettiva - Push** - È disponibile una nuova modalità di messaggistica transazionale a velocità effettiva elevata nelle campagne attivate dall&#39;API. Questa modalità è progettata per la messaggistica transazionale in tempo reale su larga scala e supporta fino a 5.000 transazioni al secondo con maggiore disponibilità. Precedentemente disponibile solo per il canale e-mail, questa funzionalità è ora disponibile anche per il canale push, per le organizzazioni che hanno acquistato il componente aggiuntivo Messaggistica transazionale ad alta velocità di Adobe. Per ulteriori informazioni, contatta il tuo rappresentante Adobe. ([DOCAC-14717](https://jira.corp.adobe.com/browse/DOCAC-14717)) <!-- Documentation link: TBD -->

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
<p>Jira: <a href="https://jira.corp.adobe.com/browse/DOCAC-14814">DOCAC-14814</a></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>
