---
solution: Journey Optimizer
product: journey optimizer
title: Note pre-release per Journey Optimizer
description: Note pre-release di Adobe Journey Optimizer
feature: Release Notes
hide: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2:
  - id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794
  - id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0
  - id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: 3902d92e0306ea23fa877dca64165b14c4e3f9dd
workflow-type: tm+mt
source-wordcount: 1960
ht-degree: 10%

---


# Note pre-release {#e-release-notes}

Adobe Journey Optimizer offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nell’ultima settimana di ogni mese, tutte le modifiche vengono consolidate nelle [note sulla versione](release-notes.md).

## Note pre-release del 26 giugno {#june-26-rn}

**Le note pre-release riportate di seguito sono soggette a modifica senza preavviso fino alla data di disponibilità della versione**. I collegamenti, le schermate e la documentazione aggiornata vengono pubblicati una volta che le modifiche sono live in produzione. Anche se la maggior parte delle modifiche viene consegnata alla data di rilascio, alcune possono essere implementate in un secondo momento. Per ulteriori informazioni, fare riferimento alla Data di disponibilità elencata per ciascuna voce.

Consulta anche [Note pre-release di Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Data di rilascio**: 16-17 giugno 2026


### Percorsi {#june-26-journeys}

In questa versione, i percorsi apporteranno le seguenti funzionalità e miglioramenti.

<table>
<thead>
<tr>
<th><strong>Ottimizzazione del percorso del percorso - Targeting</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Utilizza il nuovo <strong>Ottimizza nodo</strong> per eseguire il targeting di tipi di pubblico specifici per determinare il percorso migliore per soddisfare i KPI incentrati sull'azienda.</p>
<p>Questo strumento ti consente di sviluppare campagne di marketing più efficaci con una maggiore probabilità di risonanza a livello 1:1, di migliorare le attività di personalizzazione del marketing per i clienti e di migliorare i KPI critici di coinvolgimento dei clienti, come conversioni e ricavi.</p>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14720">Collegamento all’attività DOCAC su JIRA</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Arbitrato percorso - Formule</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile utilizzare <strong>formule</strong> per aumentare automaticamente i <strong>punteggi di priorità dei percorsi</strong> in base agli attributi del profilo cliente e ai fattori contestuali, garantendo ai clienti l'accesso ai percorsi più rilevanti.</p>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14719">Collegamento all’attività DOCAC su JIRA</a></p>
</td>
</tr>
</tbody>
</table>

* **Limite percorso live aumentato e nuovi guardrail** - È ora possibile avere fino a **200 percorsi attivi**, aumentato rispetto al limite precedente di 100.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14826">Collegamento all&#39;attività JIRA DOCAC</a>

* **Date di inizio e di fine nell&#39;intestazione del percorso** - Quando le date di inizio e/o di fine sono configurate in un percorso attivo, ora sono visualizzate nell&#39;**intestazione percorso** accanto al badge di stato attivo. L’etichetta visualizzata si adatta a seconda che ogni data sia imminente o già passata.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14702">Collegamento all&#39;attività JIRA DOCAC</a>

* **Interrompere o chiudere direttamente un percorso in pausa** - È ora possibile **interrompere un percorso o chiuderlo ai nuovi ingressi** direttamente dallo stato **In pausa**. In precedenza, un percorso in pausa doveva essere ripreso in Live prima di poter essere interrotto o chiuso.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14229">Collegamento all&#39;attività JIRA DOCAC</a>

### Campagne orchestrate {#june-26-oc}

In questa versione, le campagne orchestrate sono dotate delle seguenti funzionalità e miglioramenti.

<table>
<thead>
<tr>
<th><strong>Attività di caricamento file nelle campagne orchestrate</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le campagne orchestrate ora supportano il caricamento di un <strong>file CSV o TXT</strong> direttamente nell'area di lavoro della campagna come pubblico di destinazione, senza prima acquisire il file in Adobe Experience Platform. I dati del file vengono utilizzati in fase di esecuzione e non vengono mantenuti come set di dati di Adobe Experience Platform. Durante l’impostazione del file, puoi definire le mappature di colonna, i tipi di dati, la gestione dei valori NULL e i criteri di errore per colonna. In questo modo sono supportate campagne di invio ad hoc o di elenco partner in cui non è possibile creare una pipeline di acquisizione completa.</p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14704">Collegamento all’attività DOCAC su JIRA</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Supporto di Quiet Hours per campagne orchestrate</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile applicare <strong>ore non interattive</strong> alle campagne orchestrate. Le ore non interattive consentono di definire <strong>esclusioni basate sul tempo</strong> per impedire l'invio di messaggi durante periodi specifici, aiutandoti a rispettare le preferenze dei clienti e i requisiti di conformità in tutti i casi di utilizzo dell'orchestrazione delle campagne.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14054">Collegamento all’attività DOCAC su JIRA</a></p>
</td>
</tr>
</tbody>
</table>

* **Personalizzazione basata su loop per dati relazionali in campagne orchestrate** - L&#39;editor di personalizzazione ora supporta un **blocco di loop** che esegue iterazioni su raccolte relazionali, ad esempio ordini, account o prenotazioni, ed esegue il rendering di un blocco di contenuto per record all&#39;interno di una singola e-mail o SMS. Le raccolte vengono configurate tramite il selettore dati utilizzando token di personalizzazione, senza che sia necessaria la scrittura di espressioni.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14703">Collegamento all&#39;attività JIRA DOCAC</a>

* **Personalizzazione dei dettagli del mittente e-mail per destinatario e campagna** - Le campagne orchestrate ora supportano la personalizzazione di **campi di intestazione e-mail**, inclusi Nome mittente, Indirizzo mittente e Risposta, utilizzando gli attributi del profilo o i dati relazionali. Questo consente ai dettagli del mittente di riflettere l’advisor, la posizione o la filiale pertinente per ciascun destinatario, anziché instradare tutti gli invii tramite un unico indirizzo aziendale. I valori dell’intestazione possono essere impostati a livello di canale e sostituiti per campagna utilizzando dati contestuali per un controllo più preciso.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13761">Collegamento all&#39;attività JIRA DOCAC</a>

* **Semplificazione della dimensione di destinazione nelle campagne orchestrate** - La **dimensione di targeting** attiva è ora visualizzata nell&#39;area di lavoro del flusso di lavoro, per consentirti di vedere quale dimensione viene utilizzata da un&#39;attività di canale. Il flusso di segmentazione tra più entità è più semplice in quanto non è più necessaria un’attività &quot;Modifica dimensione&quot; separata. Inoltre, ora puoi scegliere esplicitamente se i messaggi vengono inviati a livello di profilo o a un livello di dimensione secondario.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13554">Collegamento all&#39;attività JIRA DOCAC</a>

* **Escludi il campo di esecuzione predefinito nelle campagne**. Precedentemente disponibile a livello di percorso, ora puoi sovrascrivere il **campo di esecuzione predefinito** impostato globalmente per le consegne e-mail, SMS e WhatsApp nei parametri della campagna.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14718">Collegamento all&#39;attività JIRA DOCAC</a>

### Funzione Decisioni {#june-26-decisioning}

In questa versione, la seguente funzionalità sta per essere decisa.

<table>
<thead>
<tr>
<th><strong>Sfruttare il frammento di contenuto di Adobe Experience Manager in Decisioning</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile mappare <strong>frammenti di contenuto di Adobe Experience Manager</strong> in <strong>elementi decisionali</strong> in Decisioning e sfruttarli all'interno dei criteri decisionali per consegnare il frammento giusto al cliente giusto al momento giusto.</p>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14885">Collegamento all’attività DOCAC su JIRA</a></p>
</td>
</tr>
</tbody>
</table>

### Canale e-mail {#june-26-email}

In questa versione, il canale e-mail sarà arricchito dalle seguenti funzionalità e miglioramenti.

<table>
<thead>
<tr>
<th><strong>Componenti avanzati - Layout (componenti avanzati)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>E-mail Designer ora include una <strong>libreria di componenti layout pronti all'uso</strong>, come intestazioni, schede prodotto (1, 2 o 3 colonne), blocchi di informazioni e piè di pagina, che puoi trascinare direttamente nell'area di lavoro della posta elettronica. Ogni componente è preconfigurato con proprietà modificabili (immagine, titolo, testo, pulsante, collegamenti) e può essere completamente personalizzato tramite l’interfaccia di WYSIWYG, velocizzando la creazione delle e-mail senza richiedere di creare strutture da zero.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14877">Collegamento all’attività DOCAC su JIRA</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Archiviazione del contenuto e-mail Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ora consente agli utenti di convalidare la qualità del contenuto dell'<strong>e-mail</strong>, inclusa la leggibilità, l'efficacia e la coerenza del contenuto, direttamente nell'interfaccia di E-mail Designer.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14870">Collegamento all’attività DOCAC su JIRA</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Abilita riduzione dimensioni e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Questa nuova opzione consente di <strong>ridurre le dimensioni di HTML</strong> in un'e-mail eliminando spazi vuoti, commenti e codice ridondante non necessari, senza modificare l'aspetto dell'e-mail. Questo consente di migliorare il recapito dei messaggi (alcuni provider di posta elettronica rifiutano o contrassegnano le e-mail di dimensioni eccessive) e può velocizzare il tempo di caricamento dei destinatari.</p>
<p>Data di disponibilità: 10 giugno 2026</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14777">Collegamento all’attività DOCAC su JIRA</a></p>
</td>
</tr>
</tbody>
</table>

* **Supporto della modalità testo nei frammenti** - Per supportare flussi di lavoro di posta elettronica basati su testo, ora puoi creare e gestire **versioni di testo** dei tuoi frammenti visivi per un utilizzo ottimale nella versione di testo normale delle e-mail che includono tale frammento. Quando si utilizza un frammento creato prima della versione corrente, è possibile che il rendering della versione del testo del frammento non sia corretto, sia nel Designer e-mail che nell’e-mail finale inviata ai destinatari. Per ottenere risultati ottimali con i frammenti meno recenti, modifica, salva e ripubblica ogni frammento.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14204">Collegamento all&#39;attività JIRA DOCAC</a>

* **Sono stati aggiornati i benchmark della velocità effettiva di invio in batch con scenari rivolti al cliente** - I **benchmark della velocità effettiva di invio in batch di Adobe Journey Optimizer** sono stati aggiornati per riflettere le prestazioni a livello di produzione in più scenari di personalizzazione, dagli invii di base ai contenuti dinamici complessi con logica condizionale. Le metriche aggiornate sono ora disponibili nella documentazione del prodotto per consentire ai clienti di pianificare con precisione i volumi di messaggistica.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14816">Collegamento all&#39;attività JIRA DOCAC</a>

* **Processo OTP del ciclo di feedback per sottodomini personalizzati** - Il processo di configurazione del sottodominio personalizzato del ciclo di feedback (FBL) è stato migliorato presentando l&#39;hub mittente di Yahoo **One-Time Password (OTP)** direttamente nell&#39;interfaccia utente del prodotto. Ora gli utenti possono recuperare e visualizzare automaticamente l’OTP generato durante la verifica della proprietà del dominio dell’hub del mittente Yahoo.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14815">Collegamento all&#39;attività JIRA DOCAC</a>

### Messaggistica mobile (SMS, MMS, RCS e LINE) {#june-26-mobile}

In questa versione sono disponibili i seguenti miglioramenti alla messaggistica mobile.

* **Clic univoci per rapporti SMS** - È stato introdotto un nuovo modulo **Clic univoci** per i rapporti SMS, che porta lo stesso livello di tracciamento granulare delle prestazioni degli SMS attualmente disponibile per i rapporti e-mail.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14895">Collegamento all&#39;attività JIRA DOCAC</a>

* **Canale LINE - Modifiche all&#39;authoring** - L&#39;interfaccia utente del canale LINE è stata aggiornata con funzionalità avanzate di authoring dei messaggi. Questa versione introduce il supporto per **formati di messaggi multipli**, inclusi Text, Image, Imagemap, Carosello e Flex (editor JSON), oltre alle anteprime dei dispositivi in tempo reale. Gli utenti possono ora gestire messaggi raggruppati con un massimo di cinque messaggi ordinati (con controlli di aggiunta, rimozione e riordinamento) e sfruttare l’editor di personalizzazione integrato per messaggi convalidati e dinamici.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14869">Collegamento all&#39;attività JIRA DOCAC</a>

* **Rivendita Journey Optimizer - Visualizza metriche di utilizzo** - Per i clienti che acquistano SMS direttamente tramite Adobe Journey Optimizer, è stata introdotta una nuova **dashboard di utilizzo SMS**. Ora puoi visualizzare e tenere traccia degli ultimi 90 giorni di metriche di invio dei messaggi, suddivisi per messaggi MO (Mobile Originated) e MT (Mobile Terminated). Questi dati sono disponibili anche per il download tramite CSV, fornendo una maggiore visibilità e un maggiore controllo sulla spesa SMS.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14345">Collegamento all&#39;attività JIRA DOCAC</a>

### Contenuti e integrazioni {#june-26-content}

In questa versione sono disponibili le seguenti funzionalità e miglioramenti per la gestione dei contenuti e le integrazioni.

<table>
<thead>
<tr>
<th><strong>Frammenti di contenuto con Adobe Experience Manager</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Questa versione apporta diversi miglioramenti per rendere <strong>i frammenti di contenuto di Adobe Experience Manager</strong> più utilizzabili, più governabili e più pronti per la produzione nei flussi di lavoro di authoring di Journey Optimizer:</p>
<ul>
<li>Journey Optimizer ora supporta il recupero di frammenti di contenuto da più configurazioni di Adobe Experience Manager, inclusi i livelli di pubblicazione di authoring, pubblicazione e autenticazione.</li>
<li>Una volta selezionato un frammento, il relativo contesto viene mantenuto per tutto il messaggio, consentendo agli autori di riutilizzare i campi del frammento in blocchi di contenuto senza effettuare una nuova selezione.</li>
<li>In Journey Optimizer è stata introdotta una nuova pagina di elenco dei frammenti di contenuto dedicati per migliorare la gestione del ciclo di vita; gli utenti possono identificare frammenti non sincronizzati e attivare sincronizzazioni manuali per restare al corrente.</li>
<li>Il supporto per le impostazioni internazionali e le varianti ora consente agli addetti al marketing di lavorare con versioni alternative dello stesso frammento di contenuto in modo più mirato.</li>
</ul>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14686">Collegamento all’attività DOCAC su JIRA</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Configurazione archivio Adobe Experience Manager</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi accedere in modo flessibile ai contenuti Adobe Experience Manager da Adobe Journey Optimizer. Questa versione introduce la possibilità di <strong>cambiare l'archivio di origine</strong> per i frammenti di contenuto utilizzati nei percorsi e nelle campagne.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14684">Collegamento all’attività DOCAC su JIRA</a></p>
</td>
</tr>
</tbody>
</table>

* Integrazione di **Frammenti di contenuto nativi di Adobe Experience Manager (Managed Services)** - Ora compatibile con **Managed Services**, puoi visualizzare, accedere e utilizzare frammenti di contenuto di Adobe Experience Manager direttamente in Journey Optimizer per la personalizzazione. È sufficiente aggiungere l’URL dell’archivio Adobe Experience Manager Managed Services nelle impostazioni di configurazione come configurazione unica.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14821">Collegamento all&#39;attività JIRA DOCAC</a>

* Integrazione dell&#39;assistente **AI con Adobe Experience Manager Asset Essentials** - L&#39;Assistente AI ora recupera automaticamente **immagini approvate dal marchio** direttamente dal tuo Adobe Experience Manager Assets durante la generazione di e-mail, pagine Web e notifiche push. Questo elimina la necessità di cercare manualmente in Assets o di affidarsi a fallback generici di intelligenza artificiale, garantendo che ogni elemento visivo sia perfettamente accurato e conforme al marchio.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14761">Collegamento all&#39;attività JIRA DOCAC</a>

### Canali personalizzati {#june-26-channels}

In questa versione, la seguente funzionalità sarà disponibile nei canali.

<table>
<thead>
<tr>
<th><strong>Canale in uscita personalizzato</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ora introduce <strong>Canali personalizzati</strong>, una nuova funzionalità che consente agli amministratori di portare qualsiasi canale di messaggistica in uscita basato su HTTP, come WeChat, Kakao Talk, Messenger o un provider proprietario, direttamente in AJO tramite un <strong>Channel Builder senza codice</strong>. Una volta configurati, i canali personalizzati sono disponibili per campagne, Percorsi e campagne orchestrate, con le stesse funzionalità complete dei canali nativi: personalizzazione con editor di espressioni, sperimentazione dei contenuti, anteprima e bozze, reporting preconfigurato e applicazione del consenso e della governance. In questo modo è stato colmato il divario precedentemente affrontato dalle azioni personalizzate, limitate ai Percorsi e prive di authoring di contenuti dedicati.</p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-11381">Collegamento all’attività DOCAC su JIRA</a></p>
</td>
</tr>
</tbody>
</table>

### Generazione di rapporti {#june-26-reporting}

In questa versione sono stati apportati i seguenti miglioramenti alla generazione di rapporti.

* **Escludi clic bot per rapporti e-mail e SMS** - Per fornire una visualizzazione più accurata del reale coinvolgimento dei clienti, sono ora disponibili nuove metriche stimate per Percorsi, campagne e rapporti sui canali. Queste metriche aiutano a filtrare le interazioni non umane (NHI) e i clic dei bot dai dati di reporting:
   * Clic stimati: numero totale di clic conteggiati dopo la rimozione del traffico identificati da bot e non umani.
   * CTR stimato: clic stimati relativi al totale delle consegne.
   * CTOR stimato solo per e-mail: clic stimati relativi alle aperture stimate.

  <a href="https://jira.corp.adobe.com/browse/DOCAC-14354">Collegamento all&#39;attività JIRA DOCAC</a>

### Configurazione {#june-26-configuration}

In questa versione sono stati introdotti i seguenti miglioramenti alla configurazione e all’amministrazione di.

* **Inserimento di IP nella whitelist di Web Application Firewall (WAF) per le pagine di destinazione di AJO** - Adobe Journey Optimizer ora supporta **Inserimento di IP nella whitelist di Web Application Firewall (WAF)** per le pagine di destinazione, consentendo alle organizzazioni di applicare che tutte le richieste in ingresso vengano instradate esclusivamente tramite l&#39;infrastruttura WAF configurata. Con questo miglioramento, i clienti possono configurare AJO per rifiutare qualsiasi richiesta diretta che aggiri il livello WAF, garantendo che i criteri di sicurezza definiti in strumenti come Imperva vengano applicati in modo coerente. Questa funzionalità rafforza la postura di sicurezza per le aziende con requisiti di accesso alla rete rigorosi, fornendo loro il controllo completo sul flusso di traffico verso le pagine di destinazione ospitate da AJO.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14814">Collegamento all&#39;attività JIRA DOCAC</a>

* **Set di dati da streaming a modalità batch** - Il set di dati dell&#39;evento di feedback dei messaggi di AJO sta passando dallo streaming alla **modalità di acquisizione batch**. Questa modifica assicura che l’acquisizione dei dati non superi i limiti di acquisizione dello streaming. Se utilizzi questo set di dati nei rapporti di Customer Journey Analytics o esegui query su di esso, prevedi un aumento della latenza dei dati fino a 2 ore.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14771">Collegamento all&#39;attività JIRA DOCAC</a>

### Miglioramenti a livello di usabilità {#june-26-usability}

In questa versione sono disponibili i seguenti miglioramenti a livello di usabilità.

* **Cartelle per Percorsi e campagne** - È ora possibile organizzare i percorsi e le campagne in **cartelle** per migliorare la navigazione e la gestione nell&#39;interfaccia.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14038">Collegamento all&#39;attività JIRA DOCAC</a>

