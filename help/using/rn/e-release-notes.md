---
solution: Journey Optimizer
product: journey optimizer
title: Note pre-release per Journey Optimizer
description: Note pre-release di Adobe Journey Optimizer
feature: Release Notes
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
source-git-commit: 9915d814778a8d18cf4a691e8e2d351c2ac7c405
workflow-type: tm+mt
source-wordcount: 1599
ht-degree: 7%

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

<!--
* **Supplemental identifier support for external audiences** - Supplemental identifiers in journeys are now supported for external audiences, including audiences imported from a CSV file and audiences created with Federated Audience Composition. You can designate any non-identity attribute or non-person identity attribute from the audience as the supplemental ID, no schema labeling is required.
-->

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
</td>
</tr>
</tbody>
</table>

* **Personalizzazione basata su loop per dati relazionali in campagne orchestrate** - L&#39;editor di personalizzazione ora supporta un **blocco di loop** che esegue iterazioni su raccolte relazionali, ad esempio ordini, account o prenotazioni, ed esegue il rendering di un blocco di contenuto per record all&#39;interno di una singola e-mail o SMS. Le raccolte vengono configurate tramite il selettore dati utilizzando token di personalizzazione, senza che sia necessaria la scrittura di espressioni.

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

### Canali {#june-26-channels}

In questa versione è stata introdotta la seguente funzionalità.

<table>
<thead>
<tr>
<th><strong>Canali in uscita personalizzati</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ora introduce <strong>Canali personalizzati</strong>, una nuova funzionalità che consente agli amministratori di portare qualsiasi canale di messaggistica in uscita basato su HTTP, come WeChat, Kakao Talk, Messenger o un provider proprietario, direttamente in Journey Optimizer tramite un generatore di canali senza codice.</p>
<p>Una volta configurati, i canali personalizzati sono disponibili tra campagne, percorsi e campagne orchestrate, con le stesse funzionalità complete dei canali nativi: personalizzazione con editor di espressioni, sperimentazione dei contenuti, anteprima e bozza, reporting preconfigurato e applicazione del consenso e della governance. Questo risolve il vuoto precedentemente affrontato dalle azioni personalizzate, limitate ai percorsi e prive di authoring di contenuti dedicato.</p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
</td>
</tr>
</tbody>
</table>

### E-mail {#june-26-email}

In questa versione, il canale e-mail sarà arricchito dalle seguenti funzionalità e miglioramenti.

<!--
<table>
<thead>
<tr>
<th><strong>Advanced Components</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The Email Designer now includes a library of ready-to-use layout components — such as Headers, Product Cards (1, 2, or 3 columns), Information blocks, and Footers — that you can drag and drop directly into your email canvas. Each component comes pre-configured with editable properties (image, title, text, button, links) and can be fully customized through the WYSIWYG interface, speeding up email creation without requiring you to build structures from scratch.</p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>Verifica del contenuto nel Designer e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ora consente agli utenti di convalidare la qualità del contenuto dell'<strong>e-mail</strong>, inclusa la leggibilità, l'efficacia e la coerenza del contenuto, direttamente nell'interfaccia di E-mail Designer.</p>
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
</td>
</tr>
</tbody>
</table>

* **Testo formattato in campi modificabili per frammenti** - È ora possibile aggiungere testo formattato a frammenti personalizzabili utilizzati nel contenuto delle e-mail. Ad esempio, quando utilizzi il componente Testo come campo modificabile nel Designer e-mail, puoi formattare direttamente il contenuto (ad esempio, grassetto e corsivo) e inserire collegamenti ipertestuali.

<!--
* **Text mode support in fragments** - To support text-based email workflows, you can now create and manage text versions of your visual fragments for optimal use in the plain text version of emails that include that fragment. When using a fragment that was created before the current release, the fragment text version may be incorrectly rendered — both in the Email Designer and in the final email delivered to your recipients. For best results with older fragments, edit, save and republish each fragment.
-->

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

### Campagne {#june-26-campaigns}

In questa versione sono disponibili i seguenti miglioramenti per le campagne.

* **Escludi il campo di esecuzione predefinito nelle campagne**. Precedentemente disponibile a livello di percorso, ora puoi sovrascrivere il **campo di esecuzione predefinito** impostato globalmente per le consegne e-mail, SMS e WhatsApp nei parametri della campagna.

### Generazione di rapporti {#june-26-reporting}

In questa versione sono stati apportati i seguenti miglioramenti alla generazione di rapporti.

* **Metriche di clic stimate per la generazione di rapporti e-mail e SMS** - **Clic stimati** è ora disponibile in Percorsi, campagne e rapporti sul canale. Questa metrica riflette i clic totali dopo l’esclusione del traffico identificato proveniente da bot e non umani (NHI), fornendo un quadro più chiaro dell’effettivo coinvolgimento dei clienti.

+++ In arrivo — **Le informazioni di seguito sono soggette a modifiche.**

* **Nuove metriche di clic stimate per la generazione di rapporti e-mail e SMS** - Per fornire una visualizzazione più accurata del reale coinvolgimento dei clienti, sono ora disponibili nuove metriche stimate per Percorsi, campagne e rapporti sui canali. Queste metriche aiutano a filtrare le interazioni non umane (NHI) e i clic dei bot dai dati di reporting:

   * CTR stimato: clic stimati relativi al totale delle consegne.
   * CTOR stimato solo per e-mail: clic stimati relativi alle aperture stimate.

  Data di disponibilità: fine giugno 2026

+++

### Configurazione {#june-26-configuration}

In questa versione sono stati introdotti i seguenti miglioramenti alla configurazione e all’amministrazione di.

* **Set di dati da streaming a modalità batch** - Il set di dati dell&#39;evento di feedback dei messaggi di AJO sta passando dallo streaming alla **modalità di acquisizione batch**. Questa modifica assicura che l’acquisizione dei dati non superi i limiti di acquisizione dello streaming. Se utilizzi questo set di dati nei rapporti di Customer Journey Analytics o esegui query su di esso, prevedi un aumento della latenza dei dati fino a 2 ore.

### Miglioramenti a livello di usabilità {#june-26-usability}

In questa versione sono disponibili i seguenti miglioramenti a livello di usabilità.

* **Cartelle per Percorsi e campagne** - È ora possibile organizzare i percorsi e le campagne in **cartelle** per migliorare la navigazione e la gestione nell&#39;interfaccia.
