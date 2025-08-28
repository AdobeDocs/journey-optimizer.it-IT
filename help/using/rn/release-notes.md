---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
feature: Release Notes
topic: Content Management
description: Note sulla versione di Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: ff3511e55eb56d8d5448df6d5de92dfd29ea8718
workflow-type: tm+mt
source-wordcount: '1702'
ht-degree: 72%

---

# Note sulla versione {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novità"
>abstract="**Adobe Journey Optimizer** offre continuamente nuove funzioni, miglioramenti a quelle esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese."

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese. [!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche sono disponibili nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.


## Note sulla versione di agosto 2025 {#25-8-rn}

**Data di rilascio**: 19 agosto 2025

### Nuove funzionalità {#Aug-25-8-features}

Di seguito sono descritte le nuove funzionalità incluse in questa versione.

<table>
<thead>
<tr>
<th><strong>Mettere in pausa e riprendere i percorsi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile mettere in pausa e riprendere i percorsi. Questa funzionalità offre ai professionisti del percorso maggiore controllo e flessibilità, consentendo di sospendere temporaneamente i percorsi live senza compromettere l’esperienza cliente. Quando il percorso è in pausa, le comunicazioni non vengono inviate e i profili rimangono in stato di sospensione fino a quando il percorso non viene ripreso.</p>
<p>È possibile mettere in pausa e riprendere un singolo percorso, oppure eseguire operazioni di pausa e di ripresa in blocco su un gruppo di percorsi.</p>
<p>Inoltre, è possibile applicare filtri globali ai percorsi in pausa per escludere i profili in base ai rispettivi attributi.</p>
<p><img src="assets/do-not-localize/PauseResume.gif"/></p>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/journey-pause.md">documentazione dettagliata</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Vista calendario</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Negli elenchi dei percorsi e delle campagne è ora disponibile una vista calendario. Consente di visualizzare tutte le attivazioni dei percorsi e delle campagne nei rispettivi elenchi.</p>
<p>Precedentemente rilasciata in versione a disponibilità limitata, questa funzione è ora disponibile per tutti gli ambienti. Con questa versione in disponibilità generale, la funzione include:</p>
<ul>
<li>Miglioramenti della progettazione per la navigazione tra date.</li>
<li>Possibilità di visualizzare le campagne di bozza se hai impostato una data di inizio e una data di fine</li>
<li>Nuova impostazione per nascondere e visualizzare gli elementi del calendario in esecuzione per molto tempo.</li>
</ul>
<p><img src="assets/do-not-localize/calendar.gif"/></p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/journey-ui.md#calendar">documentazione dettagliata</a></p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Dark mode in the Email Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The Journey Optimizer Email Designer now offers the ability to switch to dark mode view, where you can additionally define specific custom settings that will display only for recipients reading their emails in dark mode.</p>
<p>Note the following:</p>
<ul>
<li>The dark mode final rendering may vary and depends on the recipient's email client.</li>
<li>Not all email clients support custom dark mode. Moreover, some email clients only apply their own default dark mode for all emails that are received. In both cases, the custom settings that you defined in the Email Designer cannot be rendered.</li>
</ul>
<P>This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.</p>
<p><img src="assets/do-not-localize/dark-mode.gif"/></p>
<p>For more information, refer to the <a href="../email/dark-mode.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Use Adobe Experience Platform data for personalization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Leverage data from [!DNL Adobe Experience Platform] in the personalization editor to personalize your content and decision attributes. In particular, this allows you to extend the definition of your attributes to additional data in datasets for bulk updates that change periodically without having to manually update the attributes one at a time.</p>
<p>With this release, the following enhancements have been introduced:</p>
<ul>
<li>Support of inbound channels,</li>
<li>The "datasetLookup" helper function can now be used within expression and visual fragments to personalize content using data from Adobe Experience Platform datasets,</li>
<li>An option in the dataset now allows you to enable datasets for lookup personalization, without having to perform an API call.</li>
</ul>
<p>This capability is available in Limited Availability. Contact your Adobe representative to gain access.</p>
<p>For more information, refer to the <a href="../personalization/aep-data-perso.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Use Decisioning in email channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add Decision policies into email journeys and campaigns. Decision policies are containers for your offers that leverage the Decisioning engine to dynamically return the best content to deliver for each audience member.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p><img src="assets/do-not-localize/FILE.gif"/></p>
<p><For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Journey path optimization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Use the new Optimize node to target specific audiences or run A/B tests to determine the best path to meet your business-centric KPIs.</p>
<p>This tool allows you to test and vary, and customize communications, sequencing, and timing to best reach your customers.</p>
<p>This capability is available in Limited Availability. Contact your Adobe representative to gain access.</p>
<p><img src="assets/do-not-localize/optimize.gif"/></p>
<p>For more information, refer to the <a href="../building-journeys/optimize.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Attività di azione nei percorsi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer supporta una nuova attività Azione generica che consente di configurare sia azioni singole che gruppi di azioni multiple in uscita, semplificandone la configurazione nell’area di lavoro del percorso. In particolare, questa nuova funzione consente:</p>
<ul>
<li>Una configurazione semplificata dell’azione nativa nell’area di lavoro del percorso.</li>
<li>La capacità di creare gruppi di azioni in entrata con più azioni.</li>
<li>La possibilità di aggiungere l’ottimizzazione a qualsiasi azione del canale incorporata.</li>
<li>La possibilità di aggiungere sia opzioni di sperimentazione che opzioni multilingue a qualsiasi azione.</li>
</ul>
<p>Questa funzionalità è in disponibilità limitata. Per ottenere l’accesso, contatta il rappresentante Adobe.</p>
<p><img src="assets/do-not-localize/action-activity.gif"/></p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/journey-action.md">documentazione dettagliata</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Allegati PDF alle e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora è possibile allegare un file PDF statico a un messaggio e-mail inviato con Journey Optimizer.</p>
<ul>
<li>Puoi inviare fino a 6 messaggi con un allegato PDF per profilo all’anno.</li>
<li>La dimensione massima del file consentita per ciascun allegato è di 5 MB.</li>
<li>Per ulteriori dimensioni o volumi, è possibile acquistare un componente aggiuntivo per il pacchetto di allegati. Per ulteriori informazioni, contatta il tuo rappresentante Adobe.</li>
</ul>
<p>Questa funzionalità è in disponibilità limitata. Per ottenere l’accesso, contatta il rappresentante Adobe.</p>
<p><img src="assets/do-not-localize/pdf-attachments.gif"/></p>
<p>Per ulteriori informazioni, consulta la <a href="../email/pdf-attachments.md">documentazione dettagliata</a></p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Landing page custom forms</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>With [!DNL Journey Optimizer], you can now capture profile attributes though your landing pages.</p>
<p>Create, design and manage custom forms tailored to your needs based on a specific dataset. You can then leverage these forms in landing pages to add the profile attributes of your choice into the dataset defined for each form.</p>
<p>This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.</p>
<p><img src="assets/do-not-localize/forms.gif"/></p>
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>Ottimizzazione nelle campagne</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ora ti offre gli strumenti necessari per fornire al tuo pubblico contenuti personalizzati e ottimizzati, consentendoti di eseguire esperimenti sui contenuti, creare targeting basato su regole e utilizzare combinazioni avanzate di entrambe per massimizzare l’efficacia delle campagne e dei percorsi.</p>
<p>Con l'ottimizzazione è possibile:</p>
<ul>
<li>Testare più varianti di contenuto per identificare la messaggistica più efficace.</li>
<li>Distribuire contenuti personalizzati in base agli attributi utente e ai dati contestuali.</li>
<li>Combina targeting e sperimentazione per strategie avanzate.</li>
<li>Escludere gli utenti che non corrispondono ai criteri della variante.</li>
<li>Includere meccanismi di fallback per mantenere vivo il coinvolgimento dell’utente.</li>
</ul>
<P>Una volta che il percorso o la campagna è in esecuzione, i profili vengono valutati in base ai criteri definiti e, in base ai criteri di corrispondenza, vengono consegnati con l’esperienza o il contenuto appropriato.</p>
<p><img src="assets/do-not-localize/campaign-optimization.gif"/></p>
<p>Precedentemente rilasciata l’8 agosto solo nelle campagne, questa capacità è ora disponibile anche nei percorsi a partire dal 22 agosto.</p>
<p>Per ulteriori informazioni, consulta la <a href="../campaigns/campaigns-message-optimization.md">documentazione dettagliata</a></p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti {#Aug-25-8-improv}

Di seguito sono elencati i miglioramenti inclusi in questa versione.

* **Amministrazione**

   * **Avvisi di monitoraggio della configurazione del canale** - È ora possibile abbonarsi per ricevere gli avvisi di sistema, tramite e-mail o nel centro notifiche di Journey Optimizer, nel caso in cui manchi <!--a channel configuration failure happens or if -->un record DNS. [Ulteriori informazioni](../reports/alerts.md#alert-dns-record-missing)

* **Assistente IA**

   * **Generazione di contenuti in più lingue** - Il contenuto può essere generato in francese, spagnolo, tedesco, italiano, giapponese, svedese, olandese e norvegese. [Ulteriori informazioni](../content-management/generative-uc.md#languages)

     Data di disponibilità: 25 agosto


* **Campagne**

   * **Controllo del tasso nelle campagne in uscita** - È ora possibile abilitare il controllo del tasso per le campagne in uscita (e-mail, SMS, notifiche push), consentendo di evitare il sovraccarico sui sistemi a valle, come le pagine di destinazione o le piattaforme di assistenza clienti. [Ulteriori informazioni](../campaigns/campaign-schedule.md#rate-control)

   * **Pianificazione delle campagne di azione**: le pianificazioni giornaliere, settimanali e mensili della campagna sono state aggiornate per fornire un controllo più dettagliato sulle pianificazioni ricorrenti:

      * **Ricorrenza settimanale**: ora è possibile scegliere di ripetere la campagna ogni settimana o ogni due settimane e selezionare il giorno o i giorni della settimana in cui deve essere eseguita.

      * **Ricorrenza mensile**: ora è possibile scegliere di ripetere la campagna ogni mese o a mesi alterni e selezionare il giorno del mese in cui deve essere eseguita.

      * **Pianificazioni giornaliere, settimanali o mensili**: ora è possibile specificare se la pianificazione ricorrente deve terminare in una data specifica o dopo un determinato numero di occorrenze.

   * **Campagne programmate per azioni transazionali**: le campagne programmate per azioni transazionali sono ora disponibili per l’invio di comunicazioni transazionali batch e basate sul pubblico tramite canali e-mail, SMS e push.

* **Canale - Schede contenuto**

   * **Modelli di layout schede di contenuto** - Il canale della scheda di contenuto ora fornisce layout di messaggi OOTB che semplificheranno l&#39;esperienza di authoring. Questa versione include i modelli di layout Immagine piccola, Immagine grande e Solo immagine. [Ulteriori informazioni](../content-card/design-content-card.md)

* **Canale - Push**

   * **Data di scadenza notifica push**: ora è possibile specificare una data di scadenza per ogni notifica push, impedendo l’invio di messaggi urgenti (come quelli delle offerte del Black Friday) dopo una determinata data, evitando quindi di fornire esperienze scadenti alla clientela.

* **Canale - SMS**

   * **Rinuncia parziale**: se abilitata, l’opzione **Rinuncia parziale** rileva i messaggi in entrata più simili alle parole chiave di rinuncia definite (ad esempio, “CANCIL”) e invia automaticamente una risposta di conferma per verificare l’intenzione dell’utente di annullare l’iscrizione. Se l’utente conferma tramite il prompt definito, l’abbonamento viene annullato. [Ulteriori informazioni](../sms/sms-configuration-sinch.md)

     >[!NOTE]
     >
     >**La rinuncia fuzzy** è disponibile solo con Sinch e Infobip.

   * **Verifica connessione SMS** - Puoi testare e verificare facilmente le credenziali API SMS all&#39;interno di Adobe Journey Optimizer inviando un messaggio di esempio a un dispositivo designato. [Ulteriori informazioni](../sms/sms-configuration-sinch.md)

* **Configurazione**

  &lt;!—* **Supporto di domini dinamici** - Journey Optimizer ora supporta la personalizzazione URL completa/di base per i domini predefiniti accettati da Adobe. Questa funzionalità è disponibile in Disponibilità limitata per un set di clienti. [Ulteriori informazioni](../personalization/personalization-build-expressions.md#where)—Aggiornamento del 21 agosto: in attesa di eng. per confermare quando implementato su prod.—>

   * **Supporto di attributi personalizzati con URL di annullamento dell’iscrizione con un solo clic**: con Journey Optimizer, se il consenso è gestito al fuori di Adobe, è possibile impostare un endpoint personalizzato esterno definendo un collegamento per l’annullamento dell’iscrizione con un solo clic nella configurazione dell’e-mail. Quando i destinatari fanno clic sul collegamento di annullamento dell’iscrizione, Journey Optimizer aggiunge alcuni parametri predefiniti specifici del profilo all’evento di aggiornamento del consenso.

     Per personalizzare ulteriormente il collegamento di annullamento dell’iscrizione con un solo clic, ora puoi definire attributi personalizzati che verranno aggiunti anche all’evento di consenso. [Ulteriori informazioni](../email/list-unsubscribe.md#custom-attributes)

* **Set di dati**

   * **Archivio oggetti Experience Decisioning - Elementi offerta personalizzati** - Il set di dati di esportazione incorporato ora acquisisce tutti gli attributi dell&#39;offerta e lo stato del ciclo di vita, consentendo la personalizzazione completa e la generazione di rapporti. [Ulteriori informazioni](../data/export-datasets.md)

   * È stata introdotta la verifica della versione tramite il campo `etag` per migliorare la coerenza e tenere traccia delle modifiche per offrire elementi in modo più affidabile.

* **Funzione Decisioni**

   * **Allega frammenti agli elementi decisionali** - Journey Optimizer ora consente di allegare frammenti agli elementi decisionali che possono essere utilizzati nelle campagne di esperienza basate sul codice tramite i criteri decisionali. Questa funzionalità è disponibile in Disponibilità limitata per un set di clienti. [Ulteriori informazioni](../experience-decisioning/create-decision.md#fragments)

* **Percorsi**

   * **Operazioni del percorso in blocco**: dall’elenco dei tuoi percorsi, ora puoi selezionare più elementi. Una volta selezionati, puoi sospendere o riprendere fino a 10 percorsi alla volta.

   * **Supporto di reindirizzamento (302) nelle azioni personalizzate**: le azioni personalizzate possono ora gestire i reindirizzamenti HTTP 302 in base a una richiesta. Questo consente ai percorsi di integrarsi con le API che reindirizzano le richieste a URL localizzati o specifici di un’area geografica. I reindirizzamenti vengono seguiti automaticamente, garantendo che il contenuto corretto venga distribuito senza configurazioni aggiuntive.

   * **Più azioni in entrata nei percorsi**. Per semplificare l&#39;orchestrazione del percorso, è ora possibile definire più azioni in entrata in un singolo percorso. Precedentemente disponibile nelle campagne, questa funzionalità consente di distribuire più esperienze basate su codice, messaggi in-app, schede di contenuto o azioni web a posizioni diverse contemporaneamente, ogni azione contenente un contenuto specifico. [Ulteriori informazioni](../building-journeys/journey-action.md#multi-action)

## Orchestrazione della campagna

**Data di disponibilità**: 4 agosto 2025

Journey Optimizer ora include l’ **orchestrazione della campagna**, una nuova funzionalità appositamente creata per le campagne batch avviate dal brand. Questa versione introduce un’area di lavoro di orchestrazione della campagna e una modellazione dati migliorata, per consentire ai marketer di pianificare, eseguire il targeting e distribuire campagne cross-channel personalizzate.

>[!IMPORTANT]
>
>Per accedere all’orchestrazione della campagna, la licenza deve includere il pacchetto **Journey Optimizer - Campagne e Percorsi** o **Journey Optimizer - Campagne**. Contatta il tuo rappresentante Adobe per confermare la licenza e aggiornare, se necessario.

![GIF orchestrazione campagna](assets/do-not-localize/release.gif)

Include [Schemi relazionali e set di dati](#oc-relational) e [Area di lavoro della campagna](#oc-canvas). Insieme, queste due innovazioni sbloccano un nuovo standard per l’orchestrazione di campagne batch in Journey Optimizer. Le funzionalità principali sono elencate di seguito.

### Funzionalità principali {#oc-capabilities}

* **Flussi di lavoro con più passaggi**

  Promuovi sofisticate campagne batch multicanale con la nuova area di lavoro appositamente creata per l’orchestrazione delle campagne.

* **Tipi di pubblico on-demand**

  Segmentazione dei tipi di pubblico on-demand per l’attivazione immediata.

* **Segmentazione di più entità**

  Crea tipi di pubblico utilizzando il contesto aziendale (dimensioni non basate sulle persone) come prodotti, negozi, rinnovi, prenotazioni e altro ancora.

* **Visibilità pre-invio**

  Rivedi, perfeziona e ottimizza i tipi di pubblico e le campagne prima del lancio e durante l’esecuzione delle campagne

### Area di lavoro della campagna {#oc-canvas}

Una nuova interfaccia di orchestrazione visiva creata appositamente per le campagne batch. Questa area di lavoro consente:

* la pianificazione visiva dei flussi di campagne multicanale in più passaggi

* il supporto per tipi di pubblico on-demand creati da query relazionali

* la divisione avanzata del pubblico, attese e logica condizionale

* i conteggi precisi pre-invio dopo l’applicazione di regole di business e filtri

### Schemi relazionali e set di dati {#oc-relational}

Adobe Journey Optimizer ora supporta entità relazionali (ad esempio prodotti, negozi, prenotazioni, contratti) collegate ai profili basati sulle persone. Questo permette la segmentazione e la personalizzazione tra strutture di dati multidimensionali, consentendo casi d’uso come:

* Un messaggio per prenotazione, abbonamento o contratto

* La segmentazione basata su attributi di entità correlati (ad esempio, categoria di prodotto o ubicazione del negozio)

* Una migliore indirizzabilità (ad esempio, l’invio a tutti i contatti noti associati a un’entità)

### Perché è importante

Questa versione offre ai marketer il controllo completo sul marketing in batch avviato dal brand e basato sul pubblico, combinando una modellazione flessibile dei dati con un’esperienza di orchestrazione creata appositamente. È progettata specificamente per l’orchestrazione di campagne in batch da percorsi in tempo reale, offrendo al contempo personalizzazione e scalabilità avanzate.

### Ulteriori informazioni

Per ulteriori informazioni, consulta la [documentazione sull’orchestrazione della campagna](../orchestrated/gs-orchestrated-campaigns.md).


