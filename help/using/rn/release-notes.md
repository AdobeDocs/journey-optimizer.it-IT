---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
feature: Release Notes
topic: Content Management
description: Note sulla versione di Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '1361'
ht-degree: 31%

---

# Note sulla versione {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novità"
>abstract="**Adobe Journey Optimizer** offre continuamente nuove funzioni, miglioramenti a quelle esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese."

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese. [!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche sono disponibili nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.


## Orchestrazione della campagna

**Data disponibilità**: 4 agosto 2025

Journey Optimizer ora include **Campaign Orchestration**, una nuova funzionalità appositamente creata per le campagne batch avviate dal marchio. Questa versione introduce un’area di lavoro di orchestrazione delle campagne e una modellazione dati migliorata, per consentire agli addetti al marketing di pianificare, eseguire il targeting e distribuire campagne personalizzate cross-channel.

![GIF di orchestrazione campagna](assets/do-not-localize/release.gif)

Include [Schemi relazionali e set di dati](#oc-relational) e [Campaign Canvas](#oc-canvas). Insieme, queste due innovazioni sbloccano un nuovo standard per l’orchestrazione di campagne batch in Journey Optimizer. Le funzionalità principali sono elencate di seguito.

### Funzionalità principali {#oc-capabilities}

* **Flussi di lavoro con più passaggi**

  Promuovi sofisticate campagne batch multicanale con la nuova area di lavoro appositamente creata per l’orchestrazione delle campagne.

* **Pubblico on demand**

  Segmentazione del pubblico on-demand per l’attivazione immediata.

* **Segmentazione di più entità**

  Crea tipi di pubblico utilizzando il contesto aziendale (dimensioni non basate sulle persone) come prodotti, store, rinnovi, prenotazioni e altro ancora.

* **Visibilità pre-invio**

  Rivedi, perfeziona e ottimizza i tipi di pubblico e le campagne prima del lancio e durante l’esecuzione delle campagne

### Area di lavoro della campagna {#oc-canvas}

Una nuova interfaccia di orchestrazione visiva creata appositamente per le campagne batch. Questa area di lavoro consente di:

* Pianificazione visiva dei flussi di campagne multicanale in più passaggi

* Supporto per tipi di pubblico on-demand creati da query relazionali

* Divisione avanzata del pubblico, attese e logica condizionale

* Conteggi precisi pre-invio dopo l’applicazione di regole business e filtri

### Schemi relazionali e set di dati {#oc-relational}

Adobe Experience Platform ora supporta entità relazionali (ad esempio prodotti, negozi, prenotazioni, contratti) collegate ai profili basati sulle persone. Ciò consente la segmentazione e la personalizzazione tra strutture di dati multidimensionali, consentendo casi d’uso come:

* Un messaggio per prenotazione, abbonamento o contratto

* Segmentazione basata su attributi di entità correlati (ad esempio, categoria di prodotto o ubicazione del negozio)

* Migliore indirizzabilità (ad esempio, invio a tutti i contatti noti associati a un’entità)

### Perché è importante

Questa versione offre agli addetti al marketing il controllo completo sul marketing in batch avviato dal brand e basato sul pubblico, combinando una modellazione flessibile dei dati con un’esperienza di orchestrazione personalizzata. È progettato specificamente per l’orchestrazione di campagne in batch da percorsi in tempo reale, offrendo al contempo personalizzazione e scalabilità avanzate.

### Ulteriori informazioni

Ulteriori informazioni sono disponibili nella [documentazione sull&#39;orchestrazione delle campagne](../orchestrated/gs-orchestrated-campaigns.md).

<!--
## August '25 pre release notes {#25-7-rn}

**Pre release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: August 19, 2025


### New capabilities {#Aug-25-8-features}

New capabilities coming with this release are detailed below.

### Improvements {#Aug-25-8-improv}

Improvements coming with this release are listed below.
-->


## Note sulla versione del 25 luglio {#25-7-rn}

**Data di rilascio**: mercoledì 29 luglio 2025

### Nuove funzionalità {#features-25-7}

Di seguito sono descritte le nuove funzionalità incluse in questa versione.

#### Funzioni

<table>
<thead>
<tr>
<th><strong>Canale WhatsApp</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ora supporta la messaggistica diretta WhatsApp, consentendo un’agevole integrazione nei percorsi e nelle campagne per migliorare la comunicazione e il coinvolgimento dei destinatari. Questo canale nativo offre integrazione predefinita di modelli WhatsApp, anteprima dei messaggi, personalizzazione, rapporti sulla consegna, webhook, gestione del consenso di consenso e rinuncia e altro ancora.</p>
<p>Precedentemente rilasciata in Beta, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p><img src="../whatsapp/assets/do-not-localize/WA-Animation.gif"/><p>
<p>Per ulteriori informazioni, consulta la <a href="../whatsapp/get-started-whatsapp.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Brand</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi creare e personalizzare i tuoi marchi per definire chiaramente la tua identità visiva e verbale nelle comunicazioni. Con il punteggio di Allineamento al marchio, puoi ricevere feedback in tempo reale su come il contenuto riflette il tono, lo stile e le linee guida del tuo marchio, consentendoti di rimanere costantemente nel marchio con ogni messaggio inviato.</p>
<p>Precedentemente rilasciata in Beta, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p><img src="assets/do-not-localize/brand-score.gif"/></p>
<p>Per ulteriori informazioni, consulta la <a href="../content-management/brands.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Utilizzare Decisioning nel canale e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi aggiungere i criteri di decisione in percorsi e campagne e-mail. I criteri di decisione sono contenitori per le offerte che sfruttano il motore di decisione per restituire in modo dinamico il contenuto migliore da consegnare per ogni membro del pubblico.</p>
<p>Questa funzionalità è disponibile in Disponibilità limitata. Per ottenere l’accesso, contatta il rappresentante Adobe.</p>
Per ulteriori informazioni, consulta la <a href="../experience-decisioning/create-decision.md">documentazione dettagliata</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canale LINE</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer ha ampliato le sue funzionalità cross-channel per includere il supporto per il canale LINE. Questo miglioramento consente di creare, modificare e visualizzare in anteprima le esperienze LINE, permettendo interazioni più personalizzate e coinvolgenti. Con LINE, puoi connetterti con più clientela, inviare contenuti rilevanti e migliorare il coinvolgimento.</p>
<p>In precedenza disponibile solo per richiesta, il canale LINE è ora disponibile per tutti gli utenti (disponibilità generale).</p>
<p>Per ulteriori informazioni, consulta la <a href="../line/get-started-line.md">documentazione dettagliata</a>.</p></td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Optimization in campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer now empowers you with the tools to deliver personalized and optimized content to your campaigns' audience, allowing you to run content experiments, create rule-based targeting, and use advanced combinations of both, to maximize the effectiveness of your campaigns.</p>
<p>With Optimization, you can:</p>
<ul>
<li>Test multiple content variations to identify the most effective messaging.</li>
<li>Deliver personalized content based on user attributes and contextual data.</li>
<li>Combine targeting and experimentation for advanced campaign strategies.</li>
<li>Filter out users that do not match variant criteria.</li>
<li>Ensure fallback mechanisms to maintain user engagement.</li>
</ul>
<P>Once the campaign is live, profiles are evaluated against the defined criteria, and based on matching criteria, they are delivered with the appropriate experience or content from the campaign.</p>
<p><img src="assets/do-not-localize/campaign-optimization.gif"/></p>
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table>
-->



<table>
<thead>
<tr>
<th><strong>Percorso esecuzione in prova</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La prova del percorso è una modalità speciale di pubblicazione di un percorso in Adobe Journey Optimizer che consente ai professionisti del percorso di poterne effettuare un test, utilizzando dati di produzione reali e senza la necessità di contattare la clientela reale o aggiornare le informazioni di profilo. Questa funzione aiuta i professionisti del percorso ad acquisire maggiore sicurezza rispetto alla progettazione di un percorso e al targeting del pubblico, prima della pubblicazione effettiva.</p>
<img src="assets/do-not-localize/DryRun.gif">
<p>Precedentemente rilasciata in versione a disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/journey-dry-run.md">documentazione dettagliata</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>ID supplementare per percorsi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi attivare i percorsi utilizzando un ID profilo insieme a un altro identificatore, ad esempio un ID ordine, un ID abbonamento o un ID prescrizione, affinché un profilo possa nello stesso percorso più volte allo stesso tempo. Questo consente scenari come la gestione di più ordini o abbonamenti in parallelo, con ogni istanza che segue il proprio iter lungo il percorso.</p>
<p>Precedentemente rilasciato a disponibilità limitata, l’uso di ID supplementari nei percorsi è ora disponibile per tutti gli ambienti. Con questa versione con disponibilità generale, la funzione ora include il supporto per percorsi Read audience.</p>
<p><img src="assets/do-not-localize/gif-supplemental.gif"/></p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/supplemental-identifier.md">documentazione dettagliata</a></p>
</td>
</tr>
</tbody>
</table>

### Avvisi interni al prodotto

È ora possibile abbonarsi a **avvisi e-mail e nel prodotto** per le versioni dei prodotti Journey Optimizer.

Per iscriversi:

* Passa a **Preferenze Adobe Experience Cloud**
* In **Notifiche**, individua **Nuove versioni di Journey Optimizer**
* Abilitare le notifiche in-app ed e-mail

![](assets/do-not-localize/pulse-notif.png){width="70%" align="left"}


### Modifica nelle condizioni di percorso {#ee-change@}

A partire dall’8 luglio, nelle nuove organizzazioni della clientela, la creazione di espressioni basate sugli eventi esperienza non è più supportata nell’editor di espressioni utilizzato nelle condizioni del percorso. Di conseguenza, gli eventi esperienza nell’[origine dati di Experience Platform](../datasource/adobe-experience-platform-data-source.md) non possono essere utilizzati per la creazione di espressioni. Si fa riferimento ad approcci alternativi e best practice per la creazione di espressioni/logiche con eventi esperienza [qui](../building-journeys/exp-event-lookup.md).

Il modo in cui viene effettuato l’accesso ai dati dell’evento di contesto del percorso nei percorsi unitari rimane invariato. Negli editor di espressioni e di personalizzazione, gli utenti possono continuare ad accedere ai dati trasmessi con l’evento del percorso iniziale.

Per ulteriori informazioni, consulta [queste Domande frequenti](../building-journeys/exp-event-lookup.md#faq-ee).

### Miglioramenti {#25-7-improv}

Di seguito sono elencati i miglioramenti inclusi in questa versione.

* **Campagne**

   * **Più azioni in entrata nelle campagne**. Per semplificare l&#39;orchestrazione delle campagne, è ora possibile definire più azioni in entrata in una singola campagna. Questa funzionalità consente di distribuire più esperienze basate su codice, messaggi in-app, schede di contenuto o azioni web a posizioni diverse contemporaneamente, ogni azione contenente un contenuto specifico.
  <!-- [Read more](../FILE.md) -->

   * **Riorganizzazione inventario campagne** - Le campagne pianificate e attivate da API sono ora suddivise in schede separate nell&#39;inventario delle campagne per facilitarne la navigazione e la gestione.

[Maggiori informazioni](../campaigns/modify-stop-campaign.md)

* **Gestione dati**
   * **Aggiornamento dei set di dati del sistema di gestione delle decisioni** - Le offerte personalizzate e di fallback eliminate sono ora contrassegnate come archiviate nei set di dati &quot;decision_object_repository_personalized_offers&quot; e &quot;decision_object_repository_fallback_offers&quot;. I record esistenti nel set di dati non vengono modificati.

[Maggiori informazioni](../offers/export-catalog/access-dataset.md)

* **Percorsi**
   * **Miglioramenti degli strumenti sandbox per Percorsi** - Quando si copiano percorsi in più sandbox utilizzando le funzionalità di esportazione e importazione dei pacchetti, sono ora disponibili anche le seguenti funzionalità:
      * Selezione di un evento esistente nella destinazione
      * Copiare su un evento indipendentemente da un percorso
      * Rilevamento delle relazioni tra gruppi di campi e origini dati, collegamento alla destinazione, se esistenti, creazione delle relazioni in caso contrario.

[Maggiori informazioni](../configuration/copy-objects-to-sandbox.md)

* **Canale - In-app**
   * **Coppie chiave/valore in-app** - Con i messaggi in-app, puoi definire coppie chiave-valore per includere variabili personalizzate nel payload del messaggio. Queste coppie chiave-valore ti consentono di trasmettere dati aggiuntivi in base alla configurazione e al caso d’uso specifici. [Ulteriori informazioni](../in-app/design-in-app.md)

* **Canale - Scheda Contenuto**

   * **Squalifica di una campagna basata su regole** - Durante la modifica di regole di consegna aggiuntive, l&#39;opzione Regole di consegna precedente è stata sostituita con tre tipi di regole distinti per controllare meglio la tempistica e la visibilità dei messaggi:
      * Mostra messaggio se: Condizioni che determinano quando viene visualizzata la scheda di contenuto.
      * Ignora messaggio se: condizioni che nascondono temporaneamente la scheda di contenuto. Può riapparire se vengono soddisfatte di nuovo le condizioni di visualizzazione.
      * Messaggio di esclusione se: condizioni che impediscono definitivamente la visualizzazione della scheda di contenuto.

[Maggiori informazioni](../content-card/design-content-card.md)

* **Funzione Decisioni**
   * **API per strumenti di migrazione** - Il team Journey Optimizer sta attualmente lavorando sulle API per strumenti di migrazione per migrare le entità di gestione delle decisioni in Decisioning. Questo strumento consente una migrazione senza soluzione di continuità tra sandbox con risoluzione delle dipendenze e funzionalità di rollback. Se ti interessa, contatta il tuo rappresentante Adobe.

* **Personalizzazione**
   * All’editor di personalizzazione è stata aggiunta la nuova funzione helper &quot;SHA256&quot;. Questa funzione viene utilizzata per calcolare e restituire l’hash sha256 di una stringa.

[Maggiori informazioni](../personalization/functions/string.md#sha256)
