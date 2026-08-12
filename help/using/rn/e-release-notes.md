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
source-git-commit: 56c4e711aa1acaf7fcf7977c974736d2e7e7d999
workflow-type: tm+mt
source-wordcount: 1277
ht-degree: 15%

---


# Note pre-release {#e-release-notes}

Adobe Journey Optimizer offre continuamente nuove funzioni, miglioramenti a quelle esistenti e correzioni di bug. Nell’ultima settimana di ogni mese, tutte le modifiche vengono consolidate nelle [note sulla versione](release-notes.md).

## Note pre-release di agosto 2026 {#august-26-rn}

**Le note pre-release riportate di seguito sono soggette a modifica senza preavviso fino alla data di disponibilità della versione**. I collegamenti, le schermate e la documentazione aggiornata vengono pubblicati una volta che le modifiche saranno disponibili in produzione. Anche se la maggior parte delle modifiche viene consegnata nella data di rilascio, alcune potrebbero essere implementate in un secondo momento.

Consulta anche [Note pre-release di Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Data di rilascio**: 18-19 agosto 2026

<!--
### Onboarding {#august-26-onboarding}

The following capability is coming to onboarding in this release.

<table>
<thead>
<tr>
<th><strong>Guided capabilities for onboarding emails and journeys (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Transitioning to Adobe Journey Optimizer from another marketing platform is easier with guided capabilities that help you move existing email content and journeys into Journey Optimizer. A dedicated workspace lets you reuse what you have instead of rebuilding from scratch.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<GIF placeholder: to be added>
<Documentation link: TBD>
</td>
</tr>
</tbody>
</table>

-->

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
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Aggiungi nuova funzione dateDiff nell&#39;editor espressioni di percorso**. L&#39;editor espressioni di percorso include ora la funzione `dateDiff`, che calcola la differenza tra due date in un numero di giorni. Questa funzione è utile per una logica basata sul tempo, ad esempio per creare scadenze, calcolare la durata del ciclo di vita del cliente o creare timer di conto alla rovescia in condizioni di percorso. <!-- Documentation link: TBD -->

* **Date di inizio e di fine nell&#39;intestazione del percorso** - Quando le date di inizio e/o di fine sono configurate in un percorso, ora vengono visualizzate nell&#39;intestazione del percorso accanto al badge di stato. L’etichetta visualizzata si adatta a seconda che ogni data sia imminente o già passata. <!-- Documentation link: TBD -->

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
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Riprogettazione del flusso di authoring di Action Campaign** - Il flusso di authoring di Adobe Journey Optimizer Action Campaign è stato riprogettato per offrire un&#39;esperienza utente decisamente più intuitiva, efficiente e fluida.

* **Cartelle per le campagne d&#39;azione** - È ora possibile organizzare le campagne d&#39;azione in cartelle per migliorare la navigazione e la gestione nell&#39;interfaccia. <!-- Documentation link: TBD -->

<!--* **Brand alignment score in Action Campaign dashboard** - You can now assess your brand alignment score directly within your Action Campaign dashboard to ensure content stays on-brand. This allows you to verify guidelines at a glance without having to open the content designer.  Documentation link: TBD -->

* **Sostituisci il campo di esecuzione predefinito in Campagne azione**. Precedentemente disponibile a livello di percorso, ora puoi sovrascrivere il campo di esecuzione predefinito impostato a livello globale per le consegne e-mail, SMS e WhatsApp nei parametri di Campagna azione. <!-- Documentation link: TBD -->

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
<p>Con il rilascio della funzione Canali in uscita personalizzati, ora puoi aggiungere azioni LINE direttamente nelle campagne. Questa nuova attività ti consente di creare e distribuire contenuti altamente personalizzati, tra cui testo, adesivi, immagini, video, dati sulla posizione e messaggi Flex avanzati, per coinvolgere i tuoi clienti in modo semplice sulla piattaforma LINE. Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Possibilità di gestire le dimensioni di destinazione del profilo** - È ora possibile eliminare un Dimension di destinazione del profilo o modificare e scambiare lo spazio dei nomi delle identità configurato, fornendo un maggiore controllo e flessibilità sulle impostazioni dei dati. <!-- Documentation link: TBD -->

* **Nuove API pubbliche** - Sono ora disponibili nuove specifiche API. Queste API consentono di creare, gestire e attivare in modo programmatico campagne orchestrate, consentendo una più profonda integrazione con sistemi esterni e pipeline di automazione. <!-- Documentation link: TBD -->

* **Personalizzazione dei dettagli del mittente e-mail per destinatario e campagna** - Le campagne orchestrate ora supportano la personalizzazione dei campi di intestazione e-mail, inclusi Nome mittente, Prefisso e-mail mittente, Nome destinatario risposta e E-mail di risposta, nonché l&#39;indirizzo di esecuzione, utilizzando gli attributi del profilo o i dati relazionali. Questo consente ai dettagli del mittente di riflettere l’esperto, la posizione o la filiale relativa a ciascun destinatario, anziché instradare tutti gli invii tramite un unico indirizzo aziendale. I valori dell’intestazione possono essere impostati a livello di canale e sostituiti per campagna utilizzando dati contestuali per un controllo più preciso. <!-- Documentation link: TBD -->

* **Semplificazione della dimensione di destinazione** - La dimensione di targeting attiva viene ora visualizzata nell&#39;area di lavoro del flusso di lavoro, per consentirti di vedere quale dimensione viene utilizzata da un&#39;attività di canale. Il flusso di segmentazione tra più entità è più semplice in quanto non è più necessaria un’attività &quot;Modifica dimensione&quot; separata. Inoltre, ora puoi scegliere esplicitamente se i messaggi vengono inviati a livello di profilo o a un livello di dimensione secondario. <!-- Documentation link: TBD -->

* **Invio graduale** - È ora possibile pianificare la consegna dei messaggi in uscita in batch controllati nel tempo. Ideale per campagne di grandi volumi o che richiedono molto tempo, l’invio di ondate supporta anche una migliore recapito messaggi e contribuisce a mantenere una solida reputazione del mittente riducendo il rischio di essere segnalati come spam. <!-- Documentation link: TBD -->

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
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>


* **Componente aggiuntivo Prestazioni per velocità effettiva - Push** - È disponibile una nuova modalità di messaggistica transazionale a velocità effettiva elevata nelle campagne attivate dall&#39;API. Questa modalità è progettata per la messaggistica transazionale in tempo reale su larga scala e supporta fino a 5.000 transazioni al secondo con maggiore disponibilità. Precedentemente disponibile solo per il canale e-mail, questa funzionalità è ora disponibile anche per il canale push, per le organizzazioni che hanno acquistato il componente aggiuntivo Messaggistica transazionale ad alta velocità di Adobe. Per ulteriori informazioni, contatta il rappresentante Adobe. <!-- Documentation link: TBD -->

### Funzione Decisioni {#august-26-decisioning}

In questa versione, il seguente miglioramento sta per essere adottato nelle decisioni.

* **Limitazione di frequenza a livello di posizionamento in Decisioning** - Le regole di limitazione di frequenza in Decisioning possono ora essere definite in base ai singoli posizionamenti, fornendo un controllo più preciso sulla frequenza con cui un&#39;offerta viene visualizzata in una determinata superficie. Sono disponibili due modalità: la quota limite specifica per il posizionamento, che definisce un limite applicabile solo quando l’offerta viene visualizzata in un posizionamento selezionato, e la quota limite per posizionamento, che applica un limite in modo indipendente su ogni posizionamento in cui viene visualizzata l’offerta, in modo che ogni posizionamento mantenga il proprio contatore di quota limite. Tieni presente che il limite relativo al posizionamento non si applica alle offerte con limite massimo basate su regole basate sui dati di Adobe Experience Platform. <!-- Documentation link: TBD -->

* **Pagine mirror in frammenti visivi** - È ora possibile inserire pagine mirror in un frammento visivo. Gli attributi Decisioning vengono visualizzati correttamente sul collegamento della pagina speculare, anche quando il frammento viene utilizzato in una campagna e-mail che sfrutta Decisioning. Per poter visualizzare gli attributi decisionali, prima di pubblicare il frammento è necessario aggiungere la pagina speculare al frammento visivo. <!-- Documentation link: TBD -->

### E-mail designer {#august-26-email}

In questa versione, e-mail Designer presenta il seguente miglioramento.

* **Nuovo componente tabella in E-mail Designer** - Il Designer e-mail ora include un componente tabella incorporato, che consente di strutturare il contenuto in righe e colonne direttamente all&#39;interno dell&#39;e-mail. Trascina e rilascia il componente nell&#39;area di lavoro, personalizza il numero di righe e colonne e applica uno stile a ogni cella in modo indipendente per creare layout chiari e organizzati senza affidarsi a HTML personalizzato. <!-- Documentation link: TBD -->

### Amministrazione {#august-26-administration}

In questa versione è disponibile il seguente miglioramento per la somministrazione.

* **Processo OTP del ciclo di feedback per sottodomini personalizzati** - Il processo di configurazione del sottodominio personalizzato Feedback Loop (FBL) è stato migliorato inserendo la password monouso (OTP) dell&#39;hub mittente di Yahoo direttamente nell&#39;interfaccia utente del prodotto. Ora gli utenti possono recuperare e visualizzare automaticamente l’OTP generato durante la verifica della proprietà del dominio dell’hub del mittente Yahoo. <!-- Documentation link: TBD -->

<!--

## June '26 pre-release notes {#june-26-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published once changes are live in production. While most changes are delivered on the release date, a few may roll out later — refer to the Availability Date listed for each entry for details.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: June 16-17, 2026

### Journeys {#june-26-journeys}

The following capabilities and improvements are coming to journeys in this release.

* **Increased live journey limit and new guardrails** - You can now have up to **200 active journeys**, increased from the previous limit of 100.



### Orchestrated campaigns {#june-26-oc}

The following capabilities and improvements are coming to orchestrated campaigns in this release.

-->


