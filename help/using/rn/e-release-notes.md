---
solution: Journey Optimizer
product: journey optimizer
title: Note pre-release per Journey Optimizer
description: Note pre-release di Adobe Journey Optimizer
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
hide: true
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2:
  - id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794
  - id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0
  - id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: d606b40759f8415c40329e6a18aea3870bbe99ee
workflow-type: tm+mt
source-wordcount: 1839
ht-degree: 20%

---


# Note pre-release {#e-release-notes}

Adobe Journey Optimizer offre continuamente nuove funzioni, miglioramenti a quelle esistenti e correzioni di bug. Nell’ultima settimana di ogni mese, tutte le modifiche vengono consolidate nelle [note sulla versione](release-notes.md).

## Note pre-release di agosto 2026 {#august-26-rn}

**Le note pre-release riportate di seguito sono soggette a modifica senza preavviso fino alla data di disponibilità della versione**. I collegamenti, le schermate e la documentazione aggiornata vengono pubblicati una volta che le modifiche saranno disponibili in produzione. Anche se la maggior parte delle modifiche viene consegnata nella data di rilascio, alcune potrebbero essere implementate in un secondo momento.

Consulta anche [Note pre-release di Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Data di rilascio**: 18-19 agosto 2026

### Formazione iniziale {#august-26-onboarding}

In questa versione verrà introdotta la seguente funzionalità per l’onboarding.

<table>
<thead>
<tr>
<th><strong>Funzionalità guidate per l’onboarding di e-mail e percorsi (disponibilità generale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La transizione da un’altra piattaforma di marketing a Adobe Journey Optimizer è più semplice grazie a funzionalità guidate che consentono di spostare in Journey Optimizer i contenuti e i percorsi e-mail esistenti. Un’area di lavoro dedicata ti consente di riutilizzare ciò che hai invece di ricostruire da zero.</p>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15330">DOCAC-15330</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### Percorsi {#august-26-journeys}

In questa versione sono stati aggiunti i miglioramenti e le funzioni seguenti ai percorsi.

<table>
<thead>
<tr>
<th><strong>Blocco a livello di percorso</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile configurare un gruppo di sospensione per i percorsi direttamente dalle proprietà del percorso. Un blocco è una percentuale configurabile del pubblico di destinazione che viene escluso dall’accesso al percorso e non riceve alcuna comunicazione. Confrontando i profili di sospensione con i profili attivi nella generazione rapporti di Customer Journey Analytics, puoi misurare l’incremento incrementale (il vero impatto) fornito dal percorso.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15162">DOCAC-15162</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Aggiungi nuova funzione dateDiff nell&#39;editor espressioni di percorso**. L&#39;editor espressioni di percorso include ora la funzione `dateDiff`, che calcola la differenza tra due date in un numero di giorni. Questa funzione è utile per una logica basata sul tempo, ad esempio per creare scadenze, calcolare la durata del ciclo di vita del cliente o creare timer di conto alla rovescia in condizioni di percorso. <a href="https://jira.corp.adobe.com/browse/DOCAC-15293">15293</a> DOCAC <!-- Documentation link: TBD -->

* **Date di inizio e di fine nell&#39;intestazione del percorso** - Quando le date di inizio e/o di fine sono configurate in un percorso, ora vengono visualizzate nell&#39;intestazione del percorso accanto al badge di stato. L’etichetta visualizzata si adatta a seconda che ogni data sia imminente o già passata. <a href="https://jira.corp.adobe.com/browse/DOCAC-14702">14702</a> DOCAC <!-- Documentation link: TBD -->

### Campagne {#august-26-camp}

In questa versione sono disponibili le seguenti funzionalità e miglioramenti per le campagne.

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
<p>Questa funzionalità è attualmente disponibile in versione beta privata per un set limitato di organizzazioni. Per ulteriori informazioni, contatta il rappresentante Adobe.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15166">DOCAC-15166</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Cartelle per campagne** - È ora possibile organizzare le campagne in cartelle per migliorare la navigazione e la gestione nell&#39;interfaccia. <a href="https://jira.corp.adobe.com/browse/DOCAC-15098">15098</a> DOCAC <!-- Documentation link: TBD -->

* **Punteggio di allineamento del brand nella dashboard di Campaign**: ora puoi valutare il punteggio di allineamento del brand direttamente all’interno della dashboard di Campaign, per garantire che il contenuto rimanga in linea con il brand. Questo consente di verificare le linee guida all’istante, senza il bisogno di aprire il designer contenuti. <a href="https://jira.corp.adobe.com/browse/DOCAC-14516">14516</a> DOCAC <!-- Documentation link: TBD -->

* **Sostituisci il campo di esecuzione predefinito nelle campagne** - Precedentemente disponibile a livello di percorso, ora puoi sostituire nei parametri della campagna il campo di esecuzione predefinito impostato a livello globale per le consegne e-mail, SMS e WhatsApp. <a href="https://jira.corp.adobe.com/browse/DOCAC-14718">14718</a> DOCAC <!-- Documentation link: TBD -->

### Campagne orchestrate {#august-26-oc}

In questa versione sono state aggiunte alle campagne orchestrate le funzioni e i miglioramenti seguenti.

<table>
<thead>
<tr>
<th><strong>Supporto per le ore non interattive</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi applicare le ore non interattive. Le ore tranquille ti consentono di definire esclusioni basate sul tempo per impedire l’invio di messaggi durante periodi specifici, aiutandoti a rispettare le preferenze dei clienti e i requisiti di conformità in tutti i casi di utilizzo dell’orchestrazione delle campagne.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14054">DOCAC-14054</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Supporto del canale LINE (disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi aggiungere azioni LINE direttamente nelle campagne. Questa nuova attività ti consente di creare e distribuire contenuti altamente personalizzati, tra cui testo, adesivi, immagini, video, dati sulla posizione e messaggi Flex avanzati, per coinvolgere i tuoi clienti in modo semplice sulla piattaforma LINE. Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14905">DOCAC-14905</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Possibilità di gestire le dimensioni di destinazione del profilo** - È ora possibile eliminare un Dimension di destinazione del profilo o modificare e scambiare lo spazio dei nomi delle identità configurato, fornendo un maggiore controllo e flessibilità sulle impostazioni dei dati. <a href="https://jira.corp.adobe.com/browse/DOCAC-15018">15018</a> DOCAC <!-- Documentation link: TBD -->

* **Nuove API pubbliche** - Sono ora disponibili nuove specifiche API. Queste API consentono di creare, gestire e attivare in modo programmatico campagne orchestrate, consentendo una più profonda integrazione con sistemi esterni e pipeline di automazione. <a href="https://jira.corp.adobe.com/browse/DOCAC-14308">14308</a> DOCAC <!-- Documentation link: TBD -->

* **Personalizzazione dei dettagli del mittente e-mail per destinatario e campagna** - Le campagne orchestrate ora supportano la personalizzazione dei campi dell&#39;intestazione e-mail, inclusi Nome mittente, Indirizzo mittente e Risposta, utilizzando gli attributi del profilo o i dati relazionali. Questo consente ai dettagli del mittente di riflettere l’esperto, la posizione o la filiale relativa a ciascun destinatario, anziché instradare tutti gli invii tramite un unico indirizzo aziendale. I valori dell’intestazione possono essere impostati a livello di canale e sostituiti per campagna utilizzando dati contestuali per un controllo più preciso. <a href="https://jira.corp.adobe.com/browse/DOCAC-13761">13761</a> DOCAC <!-- Documentation link: TBD -->

* **Semplificazione della dimensione di destinazione** - La dimensione di targeting attiva viene ora visualizzata nell&#39;area di lavoro del flusso di lavoro, per consentirti di vedere quale dimensione viene utilizzata da un&#39;attività di canale. Il flusso di segmentazione tra più entità è più semplice in quanto non è più necessaria un’attività &quot;Modifica dimensione&quot; separata. Inoltre, ora puoi scegliere esplicitamente se i messaggi vengono inviati a livello di profilo o a un livello di dimensione secondario. <a href="https://jira.corp.adobe.com/browse/DOCAC-13554">13554</a> DOCAC <!-- Documentation link: TBD -->

* **Invio graduale** - È ora possibile pianificare la consegna dei messaggi in uscita in batch controllati nel tempo. Ideale per campagne di grandi volumi o che richiedono molto tempo, l’invio di ondate supporta anche una migliore recapito messaggi e contribuisce a mantenere una solida reputazione del mittente riducendo il rischio di essere segnalati come spam. <a href="https://jira.corp.adobe.com/browse/DOCAC-13990">13990</a> DOCAC <!-- Documentation link: TBD -->

### Canali {#august-26-channels}

In questa versione sono disponibili le seguenti funzionalità e miglioramenti per i canali.

<table>
<thead>
<tr>
<th><strong>Supporto per le decisioni nel canale web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Decisioning è ora disponibile per il canale web. Puoi utilizzare i criteri di decisione direttamente nell’editor visivo web per fornire le offerte più rilevanti a ogni visitatore.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-11548">DOCAC-11548</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Allegati PDF personalizzati in e-mail attivate da API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ora supporta l’associazione di fino a cinque PDF specifici per destinatario per e-mail nelle campagne attivate da API. I file PDF vengono recuperati in modo sicuro dalla Data Landing Zone e allegati al momento dell’invio, con la posizione di ciascun file passata direttamente nel payload API. Questo consente ai sistemi di generazione dei documenti esistenti a monte di rimanere operativi, con la gestione della distribuzione da parte di Journey Optimizer.</p>
<p>I casi d’uso supportati includono fatture, estratti conto, biglietti, contratti, etichette di spedizione e documenti simili che variano a seconda del destinatario. Gli allegati PDF personalizzati sono disponibili solo nelle campagne attivate da API e non sono supportati nei percorsi o nelle campagne orchestrate.</p>
<p>Volumi e dimensioni di allegati più grandi sono supportati tramite il componente aggiuntivo per allegati di PDF; per informazioni, contatta il rappresentante Adobe.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15186">DOCAC-15186</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Canale LINE - Modifiche all’authoring**: l’interfaccia utente del canale LINE è stata aggiornata con funzionalità avanzate di authoring dei messaggi. Questa versione introduce il supporto per più formati di messaggi, tra cui Testo, Immagine, Imagemap, Carosello e Flex (Editor JSON), insieme alle anteprime dei dispositivi in tempo reale. Gli utenti possono ora gestire messaggi raggruppati fino a un massimo di cinque messaggi ordinati (con controlli di aggiunta, rimozione e riordinamento) e sfruttare l’editor di personalizzazione integrato per la messaggistica convalidata e dinamica. <a href="https://jira.corp.adobe.com/browse/DOCAC-14869">14869</a> DOCAC <!-- Documentation link: TBD -->

* **Componente aggiuntivo Prestazioni per velocità effettiva - Push** - È disponibile una nuova modalità di messaggistica transazionale a velocità effettiva elevata nelle campagne attivate dall&#39;API. Questa modalità è progettata per la messaggistica transazionale in tempo reale su larga scala e supporta fino a 5.000 transazioni al secondo con maggiore disponibilità. Precedentemente disponibile solo per il canale e-mail, questa funzionalità è ora disponibile anche per il canale push, per le organizzazioni che hanno acquistato il componente aggiuntivo Messaggistica transazionale ad alta velocità di Adobe. Per ulteriori informazioni, contatta il tuo rappresentante Adobe. <a href="https://jira.corp.adobe.com/browse/DOCAC-14717">14717</a> DOCAC <!-- Documentation link: TBD -->

### Funzione Decisioni {#august-26-decisioning}

In questa versione, il seguente miglioramento sta per essere adottato nelle decisioni.

* **Limitazione di frequenza a livello di posizionamento in Decisioning** - Le regole di limitazione di frequenza in Decisioning possono ora essere definite in base ai singoli posizionamenti, fornendo un controllo più preciso sulla frequenza con cui un&#39;offerta viene visualizzata in una determinata superficie. Sono disponibili due modalità: la quota limite specifica per il posizionamento, che definisce un limite applicabile solo quando l’offerta viene visualizzata in un posizionamento selezionato, e la quota limite per posizionamento, che applica un limite in modo indipendente su ogni posizionamento in cui viene visualizzata l’offerta, in modo che ogni posizionamento mantenga il proprio contatore di quota limite. Tieni presente che il limite relativo al posizionamento non si applica alle offerte con limite massimo basate su regole basate sui dati di Adobe Experience Platform. <a href="https://jira.corp.adobe.com/browse/DOCAC-14980">14980</a> DOCAC <!-- Documentation link: TBD -->

### E-mail designer {#august-26-email}

In questa versione, e-mail Designer presenta il seguente miglioramento.

* **Nuovo componente tabella in E-mail Designer** - Il Designer e-mail ora include un componente tabella incorporato, che consente di strutturare il contenuto in righe e colonne direttamente all&#39;interno dell&#39;e-mail. Trascina e rilascia il componente nell’area di lavoro, personalizza il numero di righe e colonne e applica uno stile indipendente a ogni cella per creare layout chiari e organizzati senza affidarsi a HTML personalizzati. <a href="https://jira.corp.adobe.com/browse/DOCAC-15093">15093</a> DOCAC <!-- Documentation link: TBD -->

### Amministrazione {#august-26-administration}

In questa versione è disponibile il seguente miglioramento per la somministrazione.

* **Processo OTP del ciclo di feedback per sottodomini personalizzati** - Il processo di configurazione del sottodominio personalizzato Feedback Loop (FBL) è stato migliorato inserendo la password monouso (OTP) dell&#39;hub mittente di Yahoo direttamente nell&#39;interfaccia utente del prodotto. Ora gli utenti possono recuperare e visualizzare automaticamente l’OTP generato durante la verifica della proprietà del dominio dell’hub del mittente Yahoo. <a href="https://jira.corp.adobe.com/browse/DOCAC-14815">14815</a> DOCAC <!-- Documentation link: TBD -->

### Miglioramenti dell’usabilità {#august-26-usability}

In questa versione sono stati introdotti i seguenti miglioramenti per la fruibilità.

* **Nuova esperienza di simulazione del contenuto per le varianti di contenuto** - Il flusso di lavoro **Simula contenuto** introduce un&#39;esperienza riprogettata: tutte le varianti ora vengono riprodotte insieme in un&#39;unica griglia scorrevole (layout affiancati, sovrapposti o a capo), sostituendo la visualizzazione una variante alla volta. Una singola barra delle azioni inferiore consolida la navigazione tra le varianti di test, lo zoom, la commutazione del riquadro di visualizzazione (desktop/mobile), la commutazione delle impostazioni locali, l’aggiunta di input di esempio, la generazione di varianti con IA, il prelievo e il salvataggio di utenti simulati e l’importazione o l’esportazione di varianti. Rimuovendo la barra a sinistra e comprimendo i livelli di intestazione aggiuntivi, le anteprime avranno molto più spazio. L&#39;opzione **Passa all&#39;esperienza classica** nella barra delle azioni inferiore consente di ripristinare l&#39;esperienza precedente in qualsiasi momento. <a href="https://jira.corp.adobe.com/browse/DOCAC-15285">15285</a> DOCAC <!-- Documentation link: TBD -->

* **Operazioni di massa nell&#39;inventario dei percorsi** - È ora possibile eseguire nuove azioni di massa direttamente dall&#39;elenco dell&#39;inventario dei percorsi, rendendo più rapida la gestione di più percorsi contemporaneamente. Seleziona diversi percorsi e applica una delle seguenti nuove azioni in un singolo passaggio: **aggiungi al pacchetto**, **elimina**, **sposta nella cartella**, **modifica tag** o **gestisci accesso**. Questo riduce la necessità di ripetere la stessa azione un percorso alla volta, semplificando la gestione dei percorsi per i team che lavorano con un numero elevato di percorsi. <a href="https://jira.corp.adobe.com/browse/DOCAC-15358">15358</a> DOCAC <!-- Documentation link: TBD -->

<!--
## June '26 pre-release notes {#june-26-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published once changes are live in production. While most changes are delivered on the release date, a few may roll out later — refer to the Availability Date listed for each entry for details.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/it/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: June 16-17, 2026

### Journeys {#june-26-journeys}

The following capabilities and improvements are coming to journeys in this release.

* **Increased live journey limit and new guardrails** - You can now have up to **200 active journeys**, increased from the previous limit of 100.



### Orchestrated campaigns {#june-26-oc}

The following capabilities and improvements are coming to orchestrated campaigns in this release.

-->
