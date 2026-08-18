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
source-git-commit: a0bba0ee8c2f7623d7cf7053b0c8dfc215b45fe0
workflow-type: tm+mt
source-wordcount: 744
ht-degree: 18%

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
<th><strong>Blocco a livello di percorso (disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile configurare un gruppo di sospensione per i percorsi direttamente dalle proprietà del percorso. Un blocco è una percentuale configurabile del pubblico di destinazione che viene escluso dall’accesso al percorso e non riceve alcuna comunicazione. Confrontando i profili di sospensione con i profili attivi nella generazione rapporti di Customer Journey Analytics, puoi misurare l’incremento incrementale (il vero impatto) fornito dal percorso.</p>
<p> Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Aggiungi nuova funzione dateDiff nell&#39;editor espressioni di percorso**. L&#39;editor espressioni di percorso include ora la funzione `dateDiff`, che calcola la differenza tra due date in un numero di giorni. Questa funzione è utile per una logica basata sul tempo, ad esempio per creare scadenze, calcolare la durata del ciclo di vita del cliente o creare timer di conto alla rovescia in condizioni di percorso. <!-- Documentation link: TBD -->

* **Date di inizio e di fine nell&#39;intestazione del percorso** - Quando le date di inizio e/o di fine sono configurate in un percorso, ora vengono visualizzate nell&#39;intestazione del percorso accanto al badge di stato. L’etichetta visualizzata si adatta a seconda che ogni data sia imminente o già passata. <!-- Documentation link: TBD -->

### Canali {#august-26-channels}

In questa versione sono disponibili i seguenti miglioramenti per Campaigns:

* **Metadati di esecuzione attività live (executionMetadata)** - Le campagne di attività live (transazionali e di marketing) attivate da API ora supportano un campo executionMetadata facoltativo su ogni destinatario. Questo consente di allegare a un’esecuzione dati chiave/valore personalizzati, come un ID ordine, un livello fedeltà o un codice di regione.

### Campagne {#august-26-camp}

In questa versione sono disponibili le seguenti funzionalità e miglioramenti.

<table>
<thead>
<tr>
<th><strong>Simulazione dell’esperienza in entrata nelle campagne d’azione</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi simulare le azioni del canale in entrata nelle campagne d’azione prima di andare "live". Utilizza la modalità di simulazione per verificare la configurazione con utenti simulati e visualizzare in anteprima l’esperienza di cui è stato eseguito il rendering, inclusi un URL generato e un codice QR, in modo da poter convalidare regole, decisioni e rendering end-to-end dei contenuti.</p>
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

* **Sostituisci i campi di esecuzione predefiniti nelle campagne Azione**. Precedentemente disponibili a livello di percorso, ora puoi sovrascrivere i campi di esecuzione predefiniti configurati a livello globale per le consegne e-mail, SMS e WhatsApp nei parametri della campagna Azione. <!-- Documentation link: TBD -->

### Funzione Decisioni {#august-26-decisioning}

In questa versione, le funzionalità e i miglioramenti riportati di seguito sono disponibili come elementi decisionali.

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

* **Limitazione di frequenza a livello di posizionamento in Decisioning** - Le regole di limitazione di frequenza in Decisioning possono ora essere definite in base ai singoli posizionamenti, fornendo un controllo più preciso sulla frequenza con cui un&#39;offerta viene visualizzata in una determinata superficie. Sono disponibili due modalità: la quota limite specifica per il posizionamento, che definisce un limite applicabile solo quando l’offerta viene visualizzata in un posizionamento selezionato, e la quota limite per posizionamento, che applica un limite in modo indipendente su ogni posizionamento in cui viene visualizzata l’offerta, in modo che ogni posizionamento mantenga il proprio contatore di quota limite. Tieni presente che il limite relativo al posizionamento non si applica alle offerte con limite massimo basate su regole basate sui dati di Adobe Experience Platform. <!-- Documentation link: TBD -->

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


