---
solution: Journey Optimizer
product: journey optimizer
title: Note sulle versioni 2022
description: Note sulle versioni 2022 di Journey Optimizer
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
hidefromtoc: true
hide: true
exl-id: 0997a640-3f89-4460-ba93-ea21a9d4efc5
source-git-commit: b8d56578aae90383092978446cb3614a4a033f80
workflow-type: tm+mt
source-wordcount: '3599'
ht-degree: 100%

---

# Note sulle versioni 2022 {#release-notes-2022}

In questa pagina sono elencate tutte le funzioni e i miglioramenti di [!DNL Journey Optimizer] rilasciati nel 2022.



## Versione di ottobre 2022 {#oct-2022-release}

<!--

### New capability{#oct-2022-features}

<table>
<thead>
<tr>
<th><strong>Direct Mail Channel (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add direct mail messages in your campaigns and journeys. Direct mail is an offline channel that allows you to personalize and generate the files required by direct mail providers to send mail to your customers.</p>
<p>When you prepare a direct mail delivery, Journey Optimizer generates a file including all the targeted profiles and the chosen contact information (postal address for example). You will then be able to send this file to your direct mail provider who will take care of the actual sending.</p>
</td>
</tr>
</tbody>
</table>

-->

### Miglioramenti {#oct-2022-improvements}

**Percorsi**

* È stata aggiunta l’opzione **Forza il reingresso in caso di ricorrenza** nei parametri di pianificazione per le attività Leggi pubblico ricorrenti. Questa opzione ti consente di far passare automaticamente tutti i profili ancora presenti nel percorso all’esecuzione successiva. Quando questa opzione è disattivata, i profili devono completare il percorso prima di poter entrare nuovamente in un’altra occorrenza. [Ulteriori informazioni](../building-journeys/read-audience.md#configuring-segment-trigger-activity)

**Amministrazione**

* È stato aggiunto un messaggio all’interfaccia utente per avvisare che le configurazioni di sottodominio, sottodominio della pagina di destinazione, record PTR e pool IP sono comuni a tutte le sandbox e quindi qualsiasi modifica a una di queste configurazioni influirà anche sulle sandbox di produzione.
* I passaggi per caricare l’elenco di soppressione come file CSV dall’interfaccia utente sono stati modificati. [Ulteriori informazioni](../configuration/manage-suppression-list.md#download-suppression-list)

**Campagne**

* Ora puoi archiviare le campagne completate e interrotte. [Ulteriori informazioni](../campaigns/manage-campaigns.md#archive)


## Versione di settembre 2022{#sept-2022-release}

### Nuove funzionalità{#sept-2022-features}

<table>
<thead>
<tr>
<th><strong>Contenuti dinamici e nuovo generatore di regole condizionali</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi creare contenuti dinamici per adattare il contenuto dei messaggi in base alle regole condizionali.</p> 
<p>Le regole condizionali vengono create utilizzando un generatore di regole visive nell’editor di espressioni, in cui puoi memorizzarle per un ulteriore riutilizzo in tutti i percorsi e le campagne.</p>
<img src="assets/do-not-localize/dynamic-content.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../personalization/get-started-dynamic-content.md">documentazione dettagliata</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Campagne attivate da API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Oltre alle campagne pianificate esistenti, ora puoi creare campagne attivate da API in Journey Optimizer e richiamarle da un sistema esterno utilizzando le API.</p>
<p>Questo ti consente di soddisfare varie esigenze operative e di messaggistica transazionale, tra cui reimpostazioni di password e token OTP.</p>
<img src="assets/do-not-localize/api-triggered.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../campaigns/api-triggered-campaigns.md">documentazione dettagliata</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Controllo dell’accesso ai dati</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Tramite il controllo dell’accesso basato sugli attributi, gli amministratori possono controllare l’accesso a oggetti specifici in base a determinati attributi. Questi attributi possono essere metadati aggiunti a un oggetto, ad esempio le etichette. A partire da questa versione, gli amministratori possono inoltre definire ruoli utente con accesso solo a campi e/o oggetti specifici e ai dati corrispondenti a tali campi e/o oggetti.</p>
<p> Il controllo degli accessi basato su attributi è attualmente limitato ad alcuni utenti e verrà esteso a tutti gli ambienti con una versione futura.</p>
<img src="assets/do-not-localize/olac.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../administration/object-based-access.md">documentazione dettagliata</a>.
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Governance dei dati e privacy</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con il framework di governance per l’etichettatura e l’applicazione dell’utilizzo dati (DULE), Journey Optimizer ora può sfruttare i criteri di governance di Adobe Experience Platform per impedire che campi sensibili vengano esportati in sistemi di terze parti tramite azioni personalizzate. Se il sistema identifica un campo con restrizioni nei parametri delle azioni personalizzate, viene visualizzato un errore che impedisce la pubblicazione del percorso.</p>
<p>L’utilizzo dell’etichettatura e l’applicazione dell’utilizzo dati (DULE) è attualmente limitato a clienti selezionati e verrà implementato in tutti gli ambienti in una versione futura.</p>
<p>Per ulteriori informazioni, consulta la <a href="../action/action-privacy.md">documentazione dettagliata</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Applicazione automatica del consenso (criteri di consenso)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform consente di adottare e applicare facilmente i criteri di marketing per rispettare le preferenze di consenso dei clienti. I criteri di consenso sono definiti in Adobe Experience Platform. In Journey Optimizer puoi applicare questi criteri di consenso alle azioni personalizzate. Ad esempio, puoi definire i criteri di consenso per escludere i clienti che non hanno acconsentito a ricevere comunicazioni e-mail, push o SMS.
<p>L’applicazione automatica del consenso è attualmente disponibile solo per le organizzazioni che hanno acquistato l’offerta aggiuntiva Healthcare Shield.</p>
<p>Per ulteriori informazioni, consulta la <a href="../action/consent.md">documentazione dettagliata</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Gestione autorizzazioni</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer supporta la definizione dei ruoli utente e dei criteri di accesso per gestire le autorizzazioni per funzioni e oggetti. Mediante le <strong>Autorizzazioni di Adobe Experience Cloud</strong>, puoi creare e gestire i ruoli, nonché assegnare le autorizzazioni per le risorse desiderate per tali ruoli. Le autorizzazioni ti consentono inoltre di gestire le etichette, le sandbox e gli utenti associati a un ruolo specifico.</p>
<p> L’utilizzo delle autorizzazioni è attualmente limitato a clienti selezionati e verrà esteso a tutti gli ambienti in una versione futura.</p>
<p>Per ulteriori informazioni, consulta la <a href="../administration/attribute-based-access.md">documentazione dettagliata</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Avvisi e monitoraggio</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In qualità di utente di Journey Optimizer, ora puoi accedere agli avvisi di sistema tramite l’interfaccia utente per ricevere notifiche quando i percorsi non funzionano come previsto. Puoi visualizzare gli avvisi disponibili e abbonarti. Il primo avviso disponibile con questa versione ti avviserà se un’attività di Leggi pubblico non ha elaborato alcun profilo durante l’arco temporale definito. Ora che questo flusso di lavoro è disponibile, verranno introdotte ulteriori funzioni che possano sfruttarlo.</p>
<!--p>For more information, refer to the <a href="../reports/alerts.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Data Hygiene</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform provides a suite of data hygiene capabilities that allow you manage your stored data through programmatic deletions of consumer records and datasets. This capability is now available for Adobe Journey Optimizer. </p>
<p>You can manage your data stores to ensure that information is used as expected, is updated when incorrect data needs fixing, and is deleted when organizational policies deem it necessary.</p>
<p><strong>Caution</strong> - Data Hygiene capabilities are currently only available for organizations that have purchased the Healthcare Shield add-on offering.</p>
<p>For more information, refer to the <a href="../building-journeys/read-audience.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->

### Miglioramenti{#sept-2022-improvements}

**Percorsi**

* Il **Set di dati di entità** è ora disponibile come set di dati predefinito in Adobe Journey Optimizer. Questo set di dati di ricerca include metadati per arricchire le informazioni di tracciamento e feedback sui set di dati. Questo ti aiuterà a migliorare i rapporti e le query con dati più comprensibili. [Ulteriori informazioni](../data/datasets-query-examples.md#entity-dataset)
* È stata aggiunto un nuovo guardrail ai percorsi unitari (che iniziano con un evento o una qualificazione del pubblico) per evitare che i percorsi vengano attivati erroneamente più volte per lo stesso evento. Per impostazione predefinita, il reingresso del profilo viene ora bloccato temporaneamente per 5 minuti. [Ulteriori informazioni](../start/guardrails.md#events-g)

**Amministrazione**

* Quando si attiva o si disattiva l’elenco Consentiti, ora viene visualizzato una nuova avvertenza per specificare gli effetti di ogni azione. [Ulteriori informazioni](../configuration/allow-list.md#enable-allow-list)
* È stata aggiornata l’interfaccia utente per creare configurazioni dei canali e pool IP, gestire l’elenco di soppressione e l’elenco Consentiti e configurare il canale SMS.
* Ora, durante la creazione della prima configurazione dei canali per un determinato sottodominio, il tempo di elaborazione richiederà da 10 minuti a 10 giorni e solo fino a 3 ore per le superfici successive che utilizzano quello stesso sottodominio. [Ulteriori informazioni](../configuration/channel-surfaces.md#create-channel-surface)
* È stata aggiornata l’interfaccia utente per la creazione dei predefiniti per pagina di destinazione e dei sottodomini della pagina di destinazione. [Ulteriori informazioni](../landing-pages/lp-subdomains.md)

**Controlli di audit**

* Con Journey Optimizer puoi identificare le azioni eseguite dagli utenti nel sistema su vari servizi e funzionalità come campagne, percorsi, messaggi, pagine di destinazione, ecc. Le risorse del registro di controllo ora includono modifiche su varie altre azioni e vengono registrate automaticamente al verificarsi dell’attività. Ulteriori informazioni sono disponibili in [questa pagina](../privacy/audit-logs.md).

**Supporto per l’archiviazione**

* Il nuovo **Set di dati di entità** include un campo Modello che consente di esportare il formato e la struttura dei messaggi inviati su tutti i canali a scopo di archiviazione. [Ulteriori informazioni](../configuration/archiving-support.md)

**Pagine di destinazione**

* Ora puoi utilizzare dati contestuali provenienti da un’altra pagina all’interno della stessa pagina di destinazione. Ad esempio, se colleghi una casella di controllo a un elenco di iscrizioni nella pagina di destinazione principale, puoi utilizzare tale elenco di iscrizioni nella pagina secondaria di ringraziamento. [Ulteriori informazioni](../landing-pages/lp-content.md#use-primary-page-context)

<!--* When configuring the primary page, you can now create additional data to enable storing information when the landing page is being submitted. [Learn more](../landing-pages/lp-content.md#use-additional-data)-->

<!--* You can now use information that was submitted on a landing page to send communications to your customers. For example, if a user subscribes to a given subscription list, you can leverage that information to send an email recommending other subscription lists to that user.-->

### Altre modifiche{#sept-2022-other}

* La modalità Burst di un percorso è stata sostituita dalla modalità Consegna rapida di una campagna. [Ulteriori informazioni](../push/create-push.md#rapid-delivery)
* Per migliorare le prestazioni, i gruppi di campo di evento esperienza non possono più essere utilizzati in percorsi che iniziano con un’attività Leggi pubblico, Qualificazione del pubblico o Evento di business. Questo cambiamento è applicabile solo ai nuovi percorsi. Quelli esistenti manterranno il comportamento corrente. [Ulteriori informazioni](../start/guardrails.md#expression-editor)
* È stato rimosso il limite di 1 ora per i percorsi con Leggi pubblico pianificati. Questi percorsi ora possono essere eseguiti senza ritardi.




## Versione di agosto 2022 {#aug-2022-release}

### Nuove funzionalità

<table>
<thead>
<tr>
<th><strong>Creare e gestire campagne in Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Utilizza le campagne Journey Optimizer per distribuire contenuti una tantum a un pubblico specifico utilizzando vari canali. Quando si utilizzano i percorsi, le azioni sono progettate per essere eseguite in sequenza. Con le campagne, le azioni vengono eseguite simultaneamente, immediatamente o in base a una pianificazione specifica. </p>
<img src="assets/do-not-localize/campaigns.gif"/>
<p>Scopri come creare una campagna nella <a href="../campaigns/get-started-with-campaigns.md">documentazione dettagliata</a> e nel <a href="https://video.tv.adobe.com/v/3412404?captions=ita">video sulle funzioni</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Inviare SMS agli utenti (disponibilità generale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi creare, personalizzare e inviare SMS in Journey Optimizer tramite un’integrazione con <b>Sinch</b> o <b>Twilio</b>.</p>
<img src="assets/do-not-localize/SMS.gif"/>
<p>Per informazioni su come creare e inviare un SMS, consulta la <a href="../sms/create-sms.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>New Dynamic Expression Builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create conditional content blocks across different authoring services to personalize your content.</p>
<p>In addition to the Personalization Expression Library, the Expression Editor provides a new Conditional Rule Builder to help you design and save your content blocks.</p>
<p>For more information, refer to the <a href="../building-journeys/read-audience.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->


### Miglioramenti

**Generazione rapporti**

* La tabella e il grafico dei criteri di consenso sono ora disponibili nei rapporti globali del Percorso. Questi widget consentono di tenere traccia dei profili esclusi dai criteri nelle azioni personalizzate. [Ulteriori informazioni](../reports/journey-global-report-cja.md#journey-global)

  Per poter accedere ai widget più recenti, è necessario reimpostare le diverse dashboard di reporting. Per ulteriori informazioni sulla personalizzazione delle dashboard, consulta la [documentazione dettagliata](../reports/report-gs-cja.md).

**Amministrazione**

* È ora possibile aggiornare il numero di telefono principale da utilizzare per il canale SMS. [Ulteriori informazioni](../configuration/primary-email-addresses.md)


## Versione di luglio 2022 {#july-2022-release}

### Nuove funzionalità

<table>
<thead>
<tr>
<th><strong>Nuovo flusso di messaggistica in linea</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer fornisce un nuovo flusso per la creazione dei messaggi nei Percorsi. La messaggistica in linea consente agli utenti di risparmiare tempo e semplifica il processo del flusso di lavoro per creare e inviare un’e-mail, una notifica push o un SMS in Journey Optimizer. Rimuovendo i messaggi come passaggio separato e rendendoli modificabili in linea nell’ambito di un’azione nell’area di lavoro del Percorso, si riducono i clic e le schermate necessari per progettare e modificare i contenuti.</p>
<img src="assets/do-not-localize/inline.gif"/>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Controllo degli accessi basato su attributi (disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile identificare i campi dello schema con etichette che definiscono gli ambiti di utilizzo organizzativi o dei dati. Gli amministratori possono utilizzare l’interfaccia Autorizzazioni per definire i criteri di accesso che coprono i campi dello schema XDM per controllare l’accesso consentito a utenti o gruppi di utenti (utenti interni, esterni o di terze parti) e gestire l’accesso a tipi specifici di dati (ad esempio Dati personali sensibili/SPD).</p>
<p>Il controllo degli accessi basato su attributi è attualmente limitato ad alcuni utenti e verrà esteso a tutti gli ambienti con una versione futura.</p>
<p>Per ulteriori informazioni, consulta la <a href="../administration/attribute-based-access.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Lavori decisionali in batch</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile eseguire lavori decisionali in batch direttamente dall’interfaccia utente; non è quindi più necessario ricorrere a uno sviluppatore per eseguire processi API in batch, riducendo il tempo necessario per il marketing. Questa nuova interfaccia consente di creare nuovi lavori e gestire quelli correnti o passati.</p>
<img src="assets/do-not-localize/batch.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../offers/batch-delivery.md">documentazione dettagliata.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Utilizza automaticamente l’offerta più performante nelle decisioni (disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Nella gestione delle decisioni, ora puoi utilizzare sistemi di modelli di ottimizzazione personalizzati. Questo nuovo tipo di modello consente di ottimizzare e personalizzare le offerte in base alle loro prestazioni e ai tipi di pubblico.</p>
<p>L’utilizzo di modelli di ottimizzazione personalizzati basati su IA è attualmente limitato ad alcuni utenti e verrà esteso a tutti gli ambienti con una versione futura.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../offers/ranking/personalized-optimization-model.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti

**Percorsi**

* **Cessazione di un percorso** - Nell’area di lavoro del percorso, l’attività **Fine** è stata rimossa dalla palette. I tag di fine vengono ora aggiunti per impostazione predefinita alla fine di ciascun percorso e non possono essere rimossi. Questo miglioramento consente una migliore generazione di rapporti su dove un cliente ha abbandonato il percorso, senza che sia necessaria alcuna azione da parte del professionista del percorso. Fai riferimento alla [documentazione](../building-journeys/end-journey.md) e al [video sulle funzioni](https://video.tv.adobe.com/v/345376){target="_blank"}.


* L’opzione **Fuso orario del profilo** è ora deselezionata per impostazione predefinita nelle proprietà del percorso. [Ulteriori informazioni](../building-journeys/timezone-management.md#timezone-from-profiles)

**Messaggi**

* I predefiniti per messaggi ora sono le **configurazioni dei canali**. [Ulteriori informazioni](../configuration/channel-surfaces.md)

**Amministrazione**

* **Modifica record PTR**: ora, quando si aggiorna un record PTR, il tempo di elaborazione richiederà solo un massimo di 3 ore. [Ulteriori informazioni](../configuration/ptr-records.md#processing)

* **Interfaccia utente per l’elenco Consentiti**: è ora possibile utilizzare l’interfaccia utente di Journey Optimizer per aggiungere nuovi indirizzi e-mail o domini all’elenco Consentiti. [Ulteriori informazioni](../configuration/allow-list.md)

* **Aggiornamento della logica per l’elenco Consentiti**: ora la logica dell’elenco Consentiti si applica non appena la funzione è abilitata, anche se l’elenco è vuoto. [Ulteriori informazioni](../configuration/allow-list.md#logic)

* **Parametri di tracciamento URL** - Ora puoi utilizzare l’editor espressioni per configurare i parametri di tracciamento URL nelle superfici e-mail (ossia i predefiniti per messaggi). [Ulteriori informazioni](../email/email-settings.md#url-tracking)

**Gestione delle decisioni**

* **Dimensione pubblico**: ora nell’interfaccia utente viene visualizzato un nuovo componente per la stima delle dimensioni pubblico durante la creazione di una regola di decisione, quando si seleziona un pubblico o una regola per impostare un’idoneità all’offerta, oppure quando si aggiunge un pubblico o una regola a un ambito di decisione.


## Versione di giugno 2022 {#june-2022-release}

### Nuove funzionalità

<table>
<thead>
<tr>
<th><strong>Inviare SMS agli utenti (disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi creare, personalizzare e inviare SMS in Journey Optimizer tramite un’integrazione con <b>Sinch</b> o <b>Twilio</b>.</p>
<!--img src="assets/do-not-localize/SMS.gif"/-->
<p>Il canale SMS è attualmente disponibile solo per un set di organizzazioni (disponibilità limitata). Per ulteriori informazioni, contatta il tuo rappresentante Adobe.</p>
<p>Per informazioni su come creare e inviare un SMS, consulta la <a href="../sms/create-sms.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>L’integrazione con Adobe Stock consente di trovare più rapidamente immagini di forte impatto</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Il plug-in per l’integrazione di Adobe Stock e E-mail designer di Adobe Journey Optimizer offre ai clienti un modo semplice di cercare le immagini da utilizzare nella creazione dei messaggi, acquistarne la licenza e salvarle. </br> La nuova opzione <b>Trova foto Stock simili</b> consente inoltre di individuare foto Stock simili alle tue immagini per contenuto, colore e composizione. </p>
<p>Per ulteriori informazioni, consulta la <a href="../integrations/stock.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Utilizza E-mail Ccn in tutte le e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora è possibile utilizzare la funzionalità E-mail Ccn (copia carbone nascosta) per memorizzare le e-mail inviate da Adobe Journey Optimizer. Se abiliti questa opzione nei tuoi predefiniti e-mail, ogni e-mail verrà inviata anche come copiata nascosta all’indirizzo in Ccn.</p>
<p>Per ulteriori informazioni, consulta la <a href="../configuration/archiving-support.md#bcc-email">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--<table>
<thead>
<tr>
<th><strong>Automatically use the best performing offer in your decisions</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use personalized optimization model systems in Decision Management. This new type of model allows you to optimize and personalize offers based on audiences and offer performance.</p>
<p>The use of personalized optimization AI models is currently restricted to selected users, and will be deployed to all environments in a future release.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>For more information, refer to the <a href="../offers/ranking/personalized-optimization-model.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Copiare oggetti da una sandbox a un’altra</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi ricreare le esperienze da una sandbox Journey Optimizer a un’altra, ad esempio da una sandbox non di produzione a una di produzione. Questa nuova funzionalità consente di copiare da un ambiente all’altro un intero percorso, compresi tutti gli oggetti da cui dipende la sua esecuzione corretta. Oltre ai percorsi, puoi anche copiare altri componenti quali offerte, messaggi, schemi, set di dati, origini dati, eventi e azioni.</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/copy-to-sandbox.md">documentazione dettagliata</a>.
</td>
</tr>
</tbody>
</table>




### Miglioramenti

**Gestione delle decisioni**

* **Supporto di file HTML e JSON**: ora è possibile trascinare file HTML e JSON esterni dalla libreria di risorse Adobe Experience Cloud nel contenuto della rappresentazione dell’offerta. [Ulteriori informazioni](../offers/offer-library/add-representations.md#html-json)


**E-mail**

* **Salva come modello**: ora è possibile salvare un contenuto e-mail come modello e riutilizzarlo per creare altri messaggi. [Ulteriori informazioni](../content-management/content-templates.md#video-templates)


**Amministrazione**

* **Parametri URL di tracciamento anteprima**: quando configuri un predefinito di messaggio, se definisci i parametri di tracciamento URL ora viene visualizzata un’anteprima dinamica dell’URL di tracciamento risultante. [Ulteriori informazioni](../email/email-settings.md#url-tracking)

* **Modifica del predefinito per messaggi**: ora al momento dell’aggiornamento di un predefinito per messaggi, il tempo di elaborazione può richiedere solo fino a 3 ore. [Ulteriori informazioni](../configuration/channel-surfaces.md#edit-channel-surface)

* **Modifica del pool IP**: ora quando si aggiorna un pool IP il tempo di elaborazione può richiedere solo fino a 3 ore. [Ulteriori informazioni](../configuration/ip-pools.md#edit-ip-pool)




## Versione di maggio 2022 {#may-2022-release}

### Nuove funzionalità

<table>
<thead>
<tr>
<th><strong>Regole di frequenza dei messaggi </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi impostare regole di business cross-channel che escluderanno automaticamente i profili sollecitati eccessivamente da messaggi e azioni.</p>
<p>Per ulteriori informazioni, consulta la <a href="../conflict-prioritization/rule-sets.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Gestione delle decisioni: modello di ottimizzazione automatica basato su classificazione IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Nella gestione delle decisioni, ora è possibile utilizzare sistemi formati su modelli. Questa nuova funzionalità classifica le offerte da visualizzare per un determinato profilo.</p>
<p>Per ulteriori informazioni, consulta la <a href="../offers/offer-activities/configure-offer-selection.md#use-ranking-strategy">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Attribute-based Access Control (ABAC)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Permission management in Journey Optimizer has been extended to data access. You can now manage data access for specific teams or groups of users (i.e. internal, external, 3rd parties) ​and manage access to specific types of data (i.e. Sensitive Personal Data/SPD).</p>
<p>This capability is available for a limited set of customers.</p>
<p>For more information, refer to the <a href="../landing-pages/create-lp.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Registri di audit di Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora è possibile monitorare le azioni eseguite dagli utenti sulle risorse di Adobe Journey Optimizer.</p>
<p>Per ulteriori informazioni, consulta la <a href="../privacy/audit-logs.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti

**Personalizzazione**

* **Nuova funzione helper per nascondere i caratteri**: la funzione helper `mask` consente di sostituire una parte di stringa con caratteri “X”. [Ulteriori informazioni](../personalization/functions/string.md#mask)

**Pagine di destinazione**

* **Pagine di destinazione senza modulo**: ora è possibile creare e pubblicare una pagina di destinazione che non contiene un modulo e che non richiede alcuna azione da parte dei visitatori.
* **Modelli di pagina di destinazione**: ora è possibile salvare una pagina di destinazione come modello e riutilizzarla durante la creazione di altre pagine di destinazione. [Ulteriori informazioni](../landing-pages/lp-templates.md)
* **Torna alla pagina principale**: ora è possibile aggiungere un collegamento alla pagina principale da qualsiasi pagina secondaria all’interno della stessa pagina di destinazione.
* **Supporto di JavaScript personalizzato**: ora è possibile aggiungere codice JavaScript personalizzato al contenuto della pagina di destinazione per applicare uno stile avanzato o aggiungere comportamenti personalizzati alle pagine di destinazione.    [Ulteriori informazioni](../landing-pages/lp-custom-js.md)

**Percorsi**

* **Leggi pubblico**: i percorsi Leggi pubblico una tantum passano ora allo stato Completato 30 giorni dopo l’esecuzione del percorso. Per i tipi di pubblico con lettura pianificata, devono invece trascorrere 30 giorni dall’esecuzione dell’ultima occorrenza. [Ulteriori informazioni](../building-journeys/read-audience.md)
* **Editor espressioni**: è stata aggiunta la funzione [limit](../building-journeys/functions/list-functions.md#limit) per consentire di limitare il numero di elementi di un elenco. La funzione [sort](../building-journeys/functions/list-functions.md#sort) consente ora di ordinare un oggetto elenco. È stato aggiunto anche il supporto di listObject alle funzioni [disctinct](../building-journeys/functions/list-functions.md#distinct) e [distinctWithNull](../building-journeys/functions/list-functions.md#distinctWithNull).

**Amministrazione**

* **Aggiornamento della dashboard di utilizzo della licenza**: la dashboard Utilizzo licenze disponibile nell’interfaccia utente di [!DNL Adobe Journey Optimizer] ora riflette il valore preciso per la ricchezza media dei profili prevista **Con licenza**. Osserverai un calo nella rappresentazione di questa metrica, che indica che il limite di licenza è ora correttamente segnalato. [Ulteriori informazioni](../audience/license-usage.md)


## Versione di aprile 2022 {#april-2022-release}

### Miglioramenti

**Pagine di destinazione**

* **Nuova opzione per le caselle di controllo di consenso/rinuncia** - È ora possibile inserire una singola casella di controllo di consenso/rinuncia nelle pagine di destinazione di iscrizione. Gli utenti devono selezionare la casella di controllo per il consenso (opt-in) e deselezionarla per la rinuncia (opt-out). [Ulteriori informazioni](../landing-pages/design-lp.md#design-lp)

* **Campi delle pagine di destinazione precompilati** - È ora possibile consentire agli utenti di precompilare i campi della pagina di destinazione con le informazioni del profilo. [Ulteriori informazioni](../landing-pages/create-lp.md#configure-primary-page)

**Gestione delle decisioni**

* **API Decisioning in Edge** - L’API Decisioning di Edge può consegnare ed eseguire il rendering di offerte personalizzate gestite mediante la funzionalità di gestione delle decisioni. Puoi creare le offerte e altri oggetti correlati utilizzando l’interfaccia utente o le API di gestione delle decisioni. [Ulteriori informazioni](../offers/api-reference/offer-delivery-api/edge-decisioning-api.md)

**Amministrazione**

* **Durata invio PTR** - Le modifiche PTR ora diventano effettive dopo alcune ore. [Ulteriori informazioni](../configuration/ptr-records.md#processing)

**Progettazione e-mail**

* Per progettare il contenuto delle e-mail in Journey Optimizer sono ora disponibili **20 nuovi modelli e-mail**.

**Interfaccia utente**

* **Aiuto contestuale nell’interfaccia utente di Journey Optimizer** - Sono stati aggiunti collegamenti di aiuto contestuali verso diverse pagine della documentazione di Journey Optimizer. Quando disponibile, fai clic sull’icona “i” per visualizzare una breve descrizione della funzionalità corrente e accedere ai relativi articoli.

**Integrazione con Adobe Campaign Standard**

In qualità di cliente Adobe Campaign Standard, ora puoi inviare e-mail, notifiche push e SMS utilizzando Journey Optimizer. Utilizza le nuove azioni incorporate per sfruttare le funzionalità di messaggistica transazionale di Campaign Standard in Journey Optimizer. [Ulteriori informazioni](../action/acs-action.md)

<!--
### Fixes

* Fixed an issue which caused tracking reports not to be available as the `JourneyActionId` was not properly populated. PLATIR-19854, CJM-26006
* Fixed an error on business events which could block the journey publication. CJM-25931
* Fixed an issue which could prevent images in Email Designer templates from being displayed. PLATIR-18176, CJM-25008
-->

## Versione di marzo 2022 {#march-2022-release}

### Miglioramenti

**Percorsi**

* Per evitare di includere campi non necessari nello schema di profilo unificato, lo schema Evento delle fasi del percorso non è più abilitato per i profili per impostazione predefinita. Se necessario, puoi attivarlo. [Ulteriori informazioni](../reports/sharing-overview.md)
* I nuovi eventi delle fasi relativi ai processi di esportazione vengono ora inviati da Journey Optimizer a Adobe Experience Platform. Nella documentazione sono stati aggiunti esempi di query. [Ulteriori informazioni](../reports/query-examples.md)

**Gestione delle decisioni**

* Ora puoi specificare se il limite di offerte viene applicato a tutti gli utenti o a un profilo specifico, e a tutti i posizionamenti o a singoli posizionamenti. [Ulteriori informazioni](../offers/offer-library/add-constraints.md#capping)
* API Batch Decisioning consente alle organizzazioni di utilizzare la funzionalità di gestione delle decisioni per tutti i profili presenti in un dato pubblico in una chiamata. Il contenuto dell’offerta per ogni profilo presente nel pubblico viene inserito in un set di dati AEP, dove è disponibile per flussi di lavoro in batch personalizzati. [Ulteriori informazioni](../offers/api-reference/offer-delivery-api/batch-decisioning-api.md)

**Amministrazione**

* Ora puoi abilitare o disabilitare il collegamento di annullamento dell’iscrizione nell’intestazione delle e-mail a livello di predefinito del messaggio e impostare un URL di annullamento dell’iscrizione personalizzato a livello di messaggio. [Ulteriori informazioni](../configuration/channel-surfaces.md#list-unsubscribe)
* L’elenco Consentiti ora può essere abilitato e disabilitato tramite l’interfaccia [!DNL Journey Optimizer] sulle sandbox di produzione e di non produzione. [Ulteriori informazioni](../configuration/allow-list.md#enable-allow-list)

**Personalizzazione**

* Ora puoi salvare più di 40 espressioni di personalizzazione nella libreria. [Ulteriori informazioni](../personalization/use-expression-fragments.md)

## Versione di febbraio 2022 {#feb-2022-release}

### Nuove funzionalità

<table>
<thead>
<tr>
<th><strong>Pagine di destinazione di iscrizione</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile creare e progettare pagine di destinazione in Journey Optimizer e indirizzare gli utenti a moduli online in cui possono acconsentire o rinunciare alla ricezione delle comunicazioni o iscriversi a un servizio specifico, ad esempio una newsletter.</p>
<p>Per ulteriori informazioni, consulta la <a href="../landing-pages/create-lp.md">documentazione dettagliata</a> e alcuni <a href="../landing-pages/lp-use-cases.md">esempi di casi d’uso</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nuova libreria di espressioni di personalizzazione</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer fornisce ora una libreria in cui è possibile accedere a espressioni di personalizzazione predefinite. Queste espressioni sono configurate dagli utenti amministratore.</p>
<p>Per ulteriori informazioni, consulta la <a href="../personalization/use-expression-fragments.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>API Developer Site and Suppression API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer provide RESTful APIs that allow you to programmatically perform key operations in your applications.
Developer SDK for Journey Optimizer is now available with the Suppression API (beta).</p>
<p>With this API, you can control your outgoing messages using suppression and allow lists.
The suppression list helps you with honoring the ISPs' feedback to preserve sending IP reputation. The allow list helps you ensure that you send only to those email addresses which are in the allowed list, and typically to ensure that you do not send mails to customers from your development sandbox.</p>
<p>See <a href="https://developer.adobe.com/journey-optimizer-apis/">Adobe Journey Optimizer APIs</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Trasmettere le informazioni per tenere traccia dei messaggi con i parametri di tracciamento UTM</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Nel contenuto del messaggio di Journey Optimizer, ora puoi aggiungere parametri UTM ai collegamenti: possono fornire dati aggiuntivi su quel collegamento e aiutarti a identificare dove e perché una persona ha fatto clic sul collegamento.</p>
<p>Per ulteriori informazioni, consulta la <a href="../configuration/channel-surfaces.md#configure-email-settings">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti

**Percorsi**

* Per ottimizzare le prestazioni, tutti i percorsi in modalità di test che non sono stati attivati per una settimana torneranno allo stato Bozza. [Ulteriori informazioni](../building-journeys/testing-the-journey.md#important_notes)
* L’integrazione tra Journey Optimizer e Adobe Campaign v7/v8 è stata ottimizzata per migliorarne le prestazioni. La configurazione predefinita del limite è stata modificata in 4000 chiamate/5 minuti. [Ulteriori informazioni](../action/acc-action.md#important-notes)

**Generazione rapporti**

* È ora possibile filtrare le consegne in base al loro stato:
   * Dall’elenco Esecuzione messaggi, ora puoi escludere le bozze dall’elenco delle consegne.
   * Dai rapporti Live/Global puoi scegliere di escludere gli eventi di test.

* Ora puoi accedere ai rapporti relativi ai dati di ottimizzazione del tempo di invio: il numero di persone che hanno ricevuto messaggi immediatamente e il numero di persone a cui il messaggio è stato inviato con un&#39;ottimizzazione di 1 ora, 2 ore ecc.

<!--* decision management reports are now available in Journey Optimizer. You can access the following metrics: Offers sent - Offers' impression rate - Offers' click rate - Breakdown report on Offers' sent.-->

**Gestione delle decisioni**

* Le classificazioni e la classificazione IA sono ora raggruppate in un’unica scheda.

## Versione di gennaio 2022 {#january-2022-release}

### Nuove funzionalità

<table>
<thead>
<tr>
<th><strong>Percorsi: ottimizzare l’incremento graduale dell’IP con le condizioni per un limite dei profili</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Durante la configurazione di un’attività <strong>Condizione</strong> in un percorso, ora puoi definire un limite di profili. Questo nuovo tipo di condizione consente di impostare un numero massimo di profili per un percorso. Una volta raggiunto tale limite, i profili partecipanti seguono un percorso alternativo. Questo consente di incrementare gradualmente il volume delle consegne (incremento graduale dell’IP). Ad esempio, puoi incrementare gradualmente le consegne per un dominio suddividendo l’esecuzione su più giorni: invia 1000 messaggi il primo giorno, 2000 il secondo giorno e così via.</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/condition-activity.md#profile_cap">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Percorsi: miglioramento delle attività Leggi pubblico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Alle attività <strong>Leggi pubblico</strong> ricorrenti è stata aggiunta l’opzione <strong>Lettura incrementale</strong>. Questa opzione consente di rivolgersi solo ai singoli utenti che sono entrati a far parte del pubblico dopo l’ultima esecuzione del percorso. La prima esecuzione si rivolge sempre a tutti i membri del pubblico.</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/read-audience.md#configuring-segment-trigger-activity">documentazione dettagliata</a>.
</td>
</tr>
</tbody>
</table>

### Miglioramenti

**Percorsi**

* Ora è possibile collegare gli eventi dei passaggi di Journey Optimizer ad altri set di dati in [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=it). Il campo **profileID** nello schema incorporato Evento passaggio percorso è ora definito come campo di identità. [Ulteriori informazioni](../reports/sharing-overview.md#integration-cja)

**Gestione delle decisioni**

* Quando aggiorni un’offerta, un’offerta di fallback, una raccolta di offerte o una decisione di offerta a cui viene fatto riferimento direttamente o indirettamente in un messaggio pubblicato, gli aggiornamenti vengono ora rispecchiati automaticamente nel messaggio corrispondente, senza doverlo ripubblicare. [Ulteriori informazioni](../offers/offers-e2e.md#insert-decision-in-email)

* Quando si effettua una simulazione per capire quali offerte verranno consegnate per un determinato profilo di test, ora è possibile modificare le impostazioni predefinite della simulazione e visualizzare il codice corrispondente alle simulazioni, utile per la risoluzione dei problemi. [Ulteriori informazioni](../offers/offer-activities/simulation.md#define-simulation-settings)

**Amministrazione**

* Gli amministratori ora possono modificare i record PTR con un sottodominio configurato tramite CNAME. [Ulteriori informazioni](../configuration/ptr-records.md#edit-ptr-subdomains-cname)

**Personalizzazione**

* **Aggiungi ai preferiti**: per rendere più efficienti le attività di personalizzazione, è stato introdotto il concetto di salvataggio dei preferiti. L’aggiunta di attributi diversi al menu dei preferiti consente di accedere rapidamente agli elementi utilizzati con maggiore frequenza. [Ulteriori informazioni](../personalization/personalize.md#fav)
