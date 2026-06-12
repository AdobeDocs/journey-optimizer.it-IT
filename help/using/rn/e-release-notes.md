---
solution: Journey Optimizer
product: journey optimizer
title: Note pre-release per Journey Optimizer
description: Note pre-release di Adobe Journey Optimizer
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2: id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: b7088f7f9a21839bde56b71ccacd6c62d4e004ff
workflow-type: tm+mt
source-wordcount: 2008
ht-degree: 5%

---


# Note pre-release {#e-release-notes}

Adobe Journey Optimizer offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nell’ultima settimana di ogni mese, tutte le modifiche vengono consolidate nelle [note sulla versione](release-notes.md).

## Note pre-release del 26 giugno {#june-26-rn}

**Le note pre-release riportate di seguito sono soggette a modifica senza preavviso fino alla data di disponibilità della versione**. I collegamenti, le schermate e la documentazione aggiornata vengono pubblicati una volta che le modifiche sono live in produzione. Anche se la maggior parte delle modifiche viene consegnata alla data di rilascio, alcune possono essere implementate in un secondo momento. Per ulteriori informazioni, fare riferimento alla Data di disponibilità elencata per ciascuna voce.

Consulta anche [Note pre-release di Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Data di rilascio**: 16-17 giugno 2026

### Percorsi {#june-26-journeys}

In questa versione, i percorsi apporteranno le seguenti funzionalità e miglioramenti.

* **Limite percorso live aumentato e nuovi guardrail** - È ora possibile avere fino a **200 percorsi attivi**, aumentato rispetto al limite precedente di 100.

* **Date di inizio e di fine nell&#39;intestazione del percorso** - Quando le date di inizio e/o di fine sono configurate in un percorso attivo, ora sono visualizzate nell&#39;**intestazione percorso** accanto al badge di stato attivo. L’etichetta visualizzata si adatta a seconda che ogni data sia imminente o già passata.

* **Interrompere o chiudere direttamente un percorso in pausa** - È ora possibile **interrompere un percorso o chiuderlo ai nuovi ingressi** direttamente dallo stato **In pausa**. In precedenza, un percorso in pausa doveva essere ripreso in Live prima di poter essere interrotto o chiuso.

### Campagne orchestrate {#june-26-oc}

In questa versione, le campagne orchestrate sono dotate delle seguenti funzionalità e miglioramenti.

<table>
<thead>
<tr>
<th><strong>Targeting basato su file nelle campagne orchestrate</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le campagne orchestrate ora supportano il caricamento di un <strong>file CSV o TXT</strong> direttamente nell'area di lavoro della campagna come pubblico di destinazione, senza prima acquisire il file in Adobe Experience Platform. I dati del file vengono utilizzati in fase di esecuzione e non vengono mantenuti come set di dati di Adobe Experience Platform. Durante l’impostazione del file, puoi definire le mappature di colonna, i tipi di dati, la gestione dei valori NULL e i criteri di errore per colonna. Le righe che non superano la convalida vengono rifiutate e registrate prima dell’esecuzione della campagna, mantenendo il pubblico pulito senza la pre-elaborazione manuale. Questa funzione è particolarmente adatta per campagne di invio ad hoc o di elenco di partner in cui non è pratico creare una pipeline di acquisizione completa.</p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
</td>
</tr>
</tbody>
</table>

* **Personalizzazione basata su loop per dati relazionali in campagne orchestrate** - L&#39;editor di personalizzazione ora supporta un **blocco di loop** che esegue iterazioni su raccolte relazionali, ad esempio ordini, account o prenotazioni, ed esegue il rendering di un blocco di contenuto per record all&#39;interno di una singola e-mail o SMS. Le raccolte vengono configurate tramite il selettore dati utilizzando token di personalizzazione, senza che sia necessaria la scrittura di espressioni. Puoi visualizzare in anteprima il modo in cui i blocchi con ciclo continuo eseguono il rendering rispetto ai dati di esempio prima che la campagna venga pubblicata, inclusa la gestione di raccolte vuote.

* **Personalizzazione dei dettagli del mittente e-mail per destinatario e campagna** - Le campagne orchestrate ora supportano la personalizzazione di **campi di intestazione e-mail**, inclusi Nome mittente, Indirizzo mittente e Risposta, utilizzando gli attributi del profilo o i dati relazionali. Questo consente ai dettagli del mittente di riflettere l’advisor, la posizione o la filiale pertinente per ciascun destinatario, anziché instradare tutti gli invii tramite un unico indirizzo aziendale. I valori dell’intestazione possono essere impostati a livello di canale e sostituiti per campagna utilizzando dati contestuali per un controllo più preciso.

<!--
* **Target dimension simplification in Orchestrated campaigns** - The active **targeting dimension** is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.
-->

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
</td>
</tr>
</tbody>
</table>

* **Attributi di offerta dinamici** - Gli attributi di offerta in Decisioning possono ora essere personalizzati al momento della consegna utilizzando dati di profilo, contestuali e di pubblico. Questo elimina la necessità di mantenere offerte duplicate per varianti di contenuto minori, consentendo agli addetti al marketing di gestire meno elementi decisionali e più flessibili.

* **Limitazione di frequenza a livello di posizionamento in Decisioning** - Le regole di limitazione di frequenza in Decisioning possono ora essere definite in base ai singoli posizionamenti, fornendo un controllo più preciso sulla frequenza con cui un&#39;offerta viene visualizzata in una determinata superficie. Sono disponibili due modalità:

   * Limitazione specifica del posizionamento: definisci un limite applicabile solo quando l’offerta viene visualizzata in un posizionamento selezionato.
   * Limitazione per posizionamento: applica un tappo in modo indipendente su ogni posizionamento in cui viene visualizzata l’offerta, in modo che ogni posizionamento mantenga il proprio contatore di limitazione.

### E-mail {#june-26-email}

In questa versione, il canale e-mail sarà arricchito dalle seguenti funzionalità e miglioramenti.

<table>
<thead>
<tr>
<th><strong>Controlli di qualità del contenuto nel Designer e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ora include il punteggio di qualità del contenuto direttamente nel Designer e-mail, che analizza l’e-mail in tre dimensioni prima del lancio: controllo ortografico, grammaticale e punteggiatura; leggibilità e tono, inclusi i flag per le frasi lunghe, la voce passiva e il gergo; ed efficacia dell’oggetto e del CTA, valutati per chiarezza, urgenza e struttura. Ogni controllo fa emergere suggerimenti actionable, consentendo ai team di rilevare e risolvere i problemi senza uscire dall’interfaccia di authoring.</p>
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
<p>Journey Optimizer ora include un’opzione per ridurre le dimensioni del HTML dell’e-mail eliminando spazi vuoti inutili, commenti e codice ridondante, senza influire sul rendering dell’e-mail. In questo modo è possibile migliorare il recapito dei messaggi evitando soglie di dimensione utilizzate da alcuni provider di posta elettronica per contrassegnare o rifiutare i messaggi e ridurre i tempi di caricamento per i destinatari.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Testo formattato nei campi modificabili per i frammenti</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi aggiungere testo RTF a frammenti personalizzabili utilizzati nel contenuto delle e-mail. Ad esempio, quando utilizzi il componente Testo come campo modificabile nel Designer e-mail, puoi formattare direttamente il contenuto (ad esempio, grassetto e corsivo) e inserire collegamenti ipertestuali.</p>
</td>
</tr>
</tbody>
</table>

* **Convertitore immagine/HTML avanzato** - È ora disponibile una nuova versione della funzionalità di conversione da immagine a HTML, che offre una maggiore precisione nella generazione di HTML. Questo aggiornamento sfrutta modelli LLM di livello superiore per fornire un output HTML più preciso e affidabile dagli input delle immagini.

+++ In arrivo — **Le informazioni di seguito sono soggette a modifiche**

<table>
<thead>
<tr>
<th><strong>Moduli nel Designer e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>E-mail Designer ora include una libreria di moduli di layout pronti all’uso, come intestazioni, schede dei prodotti, blocchi di informazioni e piè di pagina, che puoi trascinare direttamente nell’area di lavoro delle e-mail.</p>
<p>Ogni modulo è preconfigurato con proprietà modificabili (immagine, titolo, testo, pulsante, collegamenti) e può essere completamente personalizzato tramite l’interfaccia di WYSIWYG, velocizzando la creazione delle e-mail senza richiedere di creare strutture da zero.</p>
<p>Data di disponibilità: 22 giugno 2026</p>
</td>
</tr>
</tbody>
</table>

+++

### Messaggistica mobile (SMS, MMS, RCS e LINE) {#june-26-mobile}

In questa versione sono disponibili i seguenti miglioramenti alla messaggistica mobile.

* **Clic univoci per rapporti SMS** - È stato introdotto un nuovo modulo **Clic univoci** per i rapporti SMS, che porta lo stesso livello di tracciamento granulare delle prestazioni degli SMS attualmente disponibile per i rapporti e-mail.

* **Canale LINE - Modifiche all&#39;authoring** - L&#39;interfaccia utente del canale LINE è stata aggiornata con funzionalità avanzate di authoring dei messaggi. Questa versione introduce il supporto per **formati di messaggi multipli**, inclusi Testo, Immagine, Imagemap, Carosello e Flex (Editor JSON), insieme alle anteprime dei dispositivi in tempo reale. Gli utenti possono ora gestire messaggi raggruppati con un massimo di cinque messaggi ordinati (con controlli di aggiunta, rimozione e riordinamento) e sfruttare l’editor di personalizzazione integrato per messaggi convalidati e dinamici.

* **SMS - Visualizza metriche di utilizzo** - Per i clienti che acquistano SMS direttamente tramite Adobe Journey Optimizer, è stata introdotta una nuova **dashboard di utilizzo SMS**. Ora puoi visualizzare e tenere traccia degli ultimi 90 giorni di metriche di invio dei messaggi, suddivisi per messaggi MO (Mobile Originated) e MT (Mobile Terminated). Questi dati sono disponibili anche per il download tramite CSV, fornendo una maggiore visibilità e un maggiore controllo sulla spesa SMS.

### Contenuti e integrazioni {#june-26-content}

In questa versione sono disponibili le seguenti funzionalità e miglioramenti per la gestione dei contenuti e le integrazioni.

<table>
<thead>
<tr>
<th><strong>Miglioramenti ai frammenti di contenuto Adobe Experience Manager in Journey Optimizer</strong><br/></th>
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
<li>Ora puoi accedere in modo flessibile ai contenuti Adobe Experience Manager da Adobe Journey Optimizer. Questa versione introduce la possibilità di <strong>cambiare l'archivio di origine</strong> per i frammenti di contenuto utilizzati nei percorsi e nelle campagne.</li>
<li>Ora compatibile con <b>Managed Services</b>, puoi visualizzare, accedere e utilizzare i frammenti di contenuto di Adobe Experience Manager direttamente in Journey Optimizer per la personalizzazione. È sufficiente aggiungere l’URL dell’archivio Adobe Experience Manager Managed Services nelle impostazioni di configurazione come configurazione unica.</li>
</ul>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integrazione dell’assistente AI con Adobe Experience Manager Asset Essentials</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L'Assistente AI ora recupera automaticamente <b>immagini approvate dal brand</b> direttamente dal tuo Adobe Experience Manager Assets durante la generazione di e-mail, pagine Web e notifiche push. Questo elimina la necessità di cercare manualmente in Assets o di affidarsi a fallback generici di intelligenza artificiale, garantendo che ogni elemento visivo sia perfettamente accurato e conforme al marchio.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Assistente AI per i miglioramenti nella generazione dei contenuti</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Questa versione migliora l'esperienza di generazione dei contenuti di <strong>AI Assistant</strong> grazie a una maggiore capacità di modifica delle immagini, a un'estrazione del marchio più affidabile e al supporto dell'autenticità dei contenuti nel flusso delle immagini:</p>
<ul>
<li><strong>La modifica di immagini AI</strong> è ora disponibile nel flusso di generazione delle immagini, incluso il supporto per modelli di terze parti di Firefly, per consentire di perfezionare le immagini di origine senza uscire dall'assistente.</li>
<li><strong>L'estrazione del segnale del marchio</strong> offre risultati di qualità superiore. Quando le pagine selezionate non ricevono un segnale sufficiente, i fallback migliorati ora popolano colori, composizione tipografica, linee guida per la scrittura e altri attributi del marchio.</li>
<li><strong>L'estrazione del marchio basata sul Web</strong> è più affidabile. Una migliore gestione del timeout impedisce a pagine lente, popup e banner di cookie di bloccare l’estrazione.</li>
<li><strong>L'autenticità dei contenuti (CAI)</strong> è ora supportata nel flusso di immagini. Questa versione risolve anche i problemi di caricamento delle immagini di riferimento e migliora la gestione delle immagini senza un manifesto C2PA esistente.</li>
</ul>
</td>
</tr>
</tbody>
</table>

<!--
### Campaigns {#june-26-campaigns}

The following improvement is coming to campaigns in this release.

* **Override the default execution field in campaigns** - Previously available at the journey level, you can now override the default **execution field** set globally for your Email, SMS and WhatsApp deliveries in the campaign parameters.
-->

### Generazione di rapporti {#june-26-reporting}

In questa versione sono stati apportati i seguenti miglioramenti alla generazione di rapporti.

* **Clic stimati per rapporti e-mail e SMS** — È ora disponibile una nuova metrica **Clic stimati** in Percorsi, campagne e rapporti canale per e-mail e SMS. Questa metrica esclude il traffico identificato generato da bot e interazioni non umane (NHI) per fornire una visione più chiara dell’effettivo coinvolgimento dei clienti. La metrica Clic esistente rimane disponibile e continua a segnalare i clic totali.

+++ In arrivo — **Le informazioni di seguito sono soggette a modifiche**

* **Nuove metriche di clic stimate per la generazione di rapporti e-mail e SMS** - Per fornire una visualizzazione più accurata del reale coinvolgimento dei clienti, sono ora disponibili nuove metriche stimate per Percorsi, campagne e rapporti sui canali. Queste metriche aiutano a filtrare le interazioni non umane (NHI) e i clic dei bot dai dati di reporting:

   * CTR stimato: clic stimati relativi al totale delle consegne.
   * CTOR stimato solo per e-mail: clic stimati relativi alle aperture stimate.

  Data di disponibilità: fine giugno 2026

+++

### Configurazione {#june-26-configuration}

In questa versione sono stati introdotti i seguenti miglioramenti alla configurazione e all’amministrazione di.

* **Set di dati da streaming a modalità batch** - Il set di dati dell&#39;evento di feedback dei messaggi di AJO sta passando dallo streaming alla **modalità di acquisizione batch**. Questa modifica assicura che l’acquisizione dei dati non superi i limiti di acquisizione dello streaming. Se utilizzi questo set di dati nei rapporti di Customer Journey Analytics o esegui query su di esso, prevedi un aumento della latenza dei dati fino a 2 ore.

+++ In arrivo — **Le informazioni di seguito sono soggette a modifiche**

* **Inserimento di IP nella whitelist di Web Application Firewall (WAF)** - Adobe Journey Optimizer ora supporta la whitelist IP di Web Application Firewall (WAF) per le pagine di destinazione, consentendo alle organizzazioni di applicare che tutte le richieste in ingresso vengano instradate esclusivamente tramite l&#39;infrastruttura WAF configurata. Con questo miglioramento, i clienti possono configurare Journey Optimizer per rifiutare qualsiasi richiesta diretta che aggiri il livello WAF, garantendo che i criteri di sicurezza definiti in strumenti come Imperva vengano applicati in modo coerente. Questa funzionalità rafforza la postura di sicurezza per le aziende con requisiti di accesso alla rete rigorosi, fornendo loro il controllo completo sul flusso di traffico verso le pagine di destinazione ospitate da AJO.

  Data di disponibilità: fine giugno 2026

+++

### Miglioramenti a livello di usabilità {#june-26-usability}

In questa versione sono disponibili i seguenti miglioramenti a livello di usabilità.

* **Cartelle per Percorsi e campagne** - È ora possibile organizzare i percorsi e le campagne in **cartelle** per migliorare la navigazione e la gestione nell&#39;interfaccia.
