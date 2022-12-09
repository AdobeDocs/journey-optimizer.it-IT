---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione 2022
description: Note sulla versione di Journey Optimizer 2022
exl-id: 0997a640-3f89-4460-ba93-ea21a9d4efc5
source-git-commit: c6498633fdfdc9442203a3bf980f1b12bd1c6a6b
workflow-type: tm+mt
source-wordcount: '3479'
ht-degree: 0%

---

# Note sulla versione 2022 {#release-notes-2022}

In questa pagina sono elencate tutte le funzioni e i miglioramenti per [!DNL Journey Optimizer] rilasciato nel 2022.


## Versione di settembre 2022{#sept-2022-release}

### Nuove funzionalità{#sept-2022-features}

<table>
<thead>
<tr>
<th><strong>Contenuto dinamico e nuovo generatore di regole condizionali</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi creare contenuti dinamici per adattare il contenuto dei messaggi in base a regole condizionali.</p> 
<p>Le regole condizionali vengono create utilizzando un generatore di regole visive nell’editor espressioni, in cui puoi memorizzarle per un ulteriore riutilizzo nei percorsi e nelle campagne.</p>
<img src="assets/do-not-localize/dynamic-content.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../personalization/get-started-dynamic-content.md">documentazione dettagliata</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Campagne attivate dall’API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Oltre alle campagne pianificate esistenti, ora puoi creare campagne attivate dall’API in Journey Optimizer e richiamarle da un sistema esterno utilizzando le API.</p>
<p>Questo ti consente di soddisfare varie esigenze operative e di messaggistica transazionale, come reimpostazioni di password, token OTP e altri.</p>
<img src="assets/do-not-localize/api-triggered.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../campaigns/api-triggered-campaigns.md">documentazione dettagliata</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Controllo dell'accesso ai dati</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Attraverso il controllo dell’accesso basato sugli attributi, gli amministratori possono controllare l’accesso a oggetti specifici in base a determinati attributi. Questi attributi possono essere metadati aggiunti a un oggetto, ad esempio etichette. A partire da questa versione, gli amministratori possono anche definire ruoli utente con accesso solo a campi e/o oggetti specifici e ai dati corrispondenti a tali campi e/o oggetti.</p>
<p> L’utilizzo del controllo degli accessi basato su attributi è attualmente limitato a clienti selezionati e verrà distribuito a tutti gli ambienti in una versione futura.</p>
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
<p>Con il framework di governance DULE (Data Usage Labeling and Enforcement, etichettatura e applicazione dell’uso dei dati), ora Journey Optimizer può sfruttare i criteri di governance di Adobe Experience Platform per impedire che campi sensibili vengano esportati in sistemi di terze parti tramite azioni personalizzate. Se il sistema identifica un campo con restrizioni nei parametri delle azioni personalizzate, viene visualizzato un errore che impedisce la pubblicazione del percorso.</p>
<p>L’utilizzo di DULE (Data Usage Labeling and Enforcement, etichettatura e applicazione dell’uso dei dati) è attualmente limitato a clienti selezionati e verrà implementato in tutti gli ambienti in una versione futura.</p>
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
<p>Adobe Experience Platform ti consente di adottare e applicare facilmente le politiche di marketing per rispettare le preferenze di consenso dei tuoi clienti. I criteri di consenso sono definiti in Adobe Experience Platform. In Journey Optimizer puoi applicare questi criteri di consenso alle azioni personalizzate. Ad esempio, puoi definire i criteri di consenso per escludere i clienti che non hanno acconsentito a ricevere comunicazioni e-mail, push o SMS.
<p>L'applicazione automatica del consenso è attualmente disponibile solo per le organizzazioni che hanno acquistato l'offerta aggiuntiva Healthcare Shield.</p>
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
<p>Journey Optimizer supporta la definizione dei ruoli utente e dei criteri di accesso per gestire le autorizzazioni per funzioni e oggetti. Attraverso <strong>Autorizzazioni di Adobe Experience Cloud</strong>, puoi creare e gestire i ruoli e assegnare le autorizzazioni di risorse desiderate per questi ruoli. Le autorizzazioni ti consentono inoltre di gestire le etichette, le sandbox e gli utenti associati a un ruolo specifico.</p>
<p> L’utilizzo delle autorizzazioni è attualmente limitato a clienti selezionati e verrà distribuito a tutti gli ambienti in una versione futura.</p>
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
<p>In qualità di utente di Journey Optimizer, ora puoi accedere agli avvisi di sistema tramite l’interfaccia utente per ricevere notifiche quando i percorsi non funzionano come previsto. Puoi visualizzare gli avvisi disponibili e abbonarti. Il primo avviso disponibile con questa versione ti avviserà se un’attività Leggi segmento non ha elaborato alcun profilo durante l’intervallo di tempo definito. Ora che questo flusso di lavoro viene sbloccato, ne verrà fatto di più.</p>
<p>Per ulteriori informazioni, consulta la <a href="../reports/alerts.md">documentazione dettagliata</a>.
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
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->

### Miglioramenti{#sept-2022-improvements}

**Percorsi**

* La **Set di dati di entità** è ora disponibile come set di dati predefinito in Adobe Journey Optimizer. Questo set di dati di ricerca include metadati per arricchire le informazioni sui set di dati di tracciamento e feedback. Questo ti aiuterà a migliorare i tuoi rapporti e le tue query con dati più comprensibili. [Ulteriori informazioni](../data/datasets-query-examples.md#entity-dataset)
* È stata aggiunta una nuova guardrail ai percorsi unitari (a partire da un evento o da una qualifica di segmento) per evitare che i percorsi vengano erroneamente attivati più volte per lo stesso evento. Per impostazione predefinita, il rientro del profilo viene bloccato temporaneamente per 5 minuti. [Ulteriori informazioni](../start/guardrails.md#events-g)

**Amministrazione**

* Quando si attiva o si disattiva l’elenco Consentiti, ora viene visualizzato un nuovo avviso per descrivere in dettaglio gli impatti di ogni azione. [Ulteriori informazioni](../configuration/allow-list.md#enable-allow-list)
* È stata aggiornata l’interfaccia utente per la creazione di superfici dei canali, la creazione di pool IP, la gestione dell’elenco di soppressione e dell’elenco consentiti e la configurazione del canale SMS.
* Ora, quando si crea la superficie del primo canale per un determinato sottodominio, il tempo di elaborazione richiederà da 10 a 10 giorni e solo fino a 3 ore per le superfici successive che utilizzano quel sottodominio. [Ulteriori informazioni](../configuration/channel-surfaces.md#create-channel-surface)
* È stata aggiornata l’interfaccia utente per la creazione dei predefiniti pagina di destinazione e dei sottodomini della pagina di destinazione. [Ulteriori informazioni](../landing-pages/lp-subdomains.md)

**Controlli di audit**

* Con Journey Optimizer puoi identificare le azioni eseguite dagli utenti nel sistema su vari servizi e funzionalità come campagne, percorsi, messaggi, pagine di destinazione, ecc. Le risorse del registro di controllo ora includono modifiche su varie altre azioni e vengono registrate automaticamente al verificarsi dell’attività. Ulteriori informazioni [in questa pagina](../privacy/audit-logs.md).

**Supporto per l&#39;archiviazione**

* Il nuovo **Set di dati di entità** include un campo Modello che consente di esportare il formato e la struttura dei messaggi inviati su tutti i canali a scopo di archiviazione. [Ulteriori informazioni](../configuration/archiving-support.md)

**Pagine di destinazione**

* Ora puoi utilizzare dati contestuali provenienti da un’altra pagina all’interno della stessa pagina di destinazione. Ad esempio, se colleghi una casella di controllo a un elenco di sottoscrizioni nella pagina di destinazione principale, puoi utilizzare tale elenco nella pagina secondaria &quot;grazie&quot;. [Ulteriori informazioni](../landing-pages/lp-content.md#use-primary-page-context)

<!--* When configuring the primary page, you can now create additional data to enable storing information when the landing page is being submitted. [Learn more](../landing-pages/lp-content.md#use-additional-data)-->

<!--* You can now use information that was submitted on a landing page to send communications to your customers. For example, if a user subscribes to a given subscription list, you can leverage that information to send an email recommending other subscription lists to that user.-->

### Altre modifiche{#sept-2022-other}

* La modalità Journey Burst è stata sostituita dalla modalità di consegna rapida di Campaign. [Ulteriori informazioni](../campaigns/create-campaign.md#rapid-delivery)
* Per migliorare le prestazioni, non è più possibile utilizzare i gruppi di campi evento Experience nei percorsi che iniziano con un segmento Read , una qualifica Segment o un’attività dell’evento aziendale. Questa modifica si applica solo ai nuovi percorsi. Quelli esistenti manterranno il comportamento corrente. [Ulteriori informazioni](../start/guardrails.md#expression-editor)
* È stato rimosso il limite di 1 ora per i percorsi pianificati dei segmenti di lettura. Questi percorsi possono ora essere eseguiti senza ritardi.




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
<p>Utilizza le campagne di Journey Optimizer per distribuire contenuti una tantum a un segmento specifico utilizzando vari canali. Quando utilizzi i percorsi, le azioni sono progettate per essere eseguite in sequenza. Con le campagne, le azioni vengono eseguite simultaneamente, immediatamente o in base a una pianificazione specifica. </p>
<img src="assets/do-not-localize/campaigns.gif"/>
<p>Scopri come creare una campagna nel <a href="../campaigns/get-started-with-campaigns.md">documentazione dettagliata</a> e <a href="https://video.tv.adobe.com/v/346680">video sulle funzioni</a>.
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
<p>Ora puoi creare, personalizzare e inviare SMS in Journey Optimizer tramite un’integrazione con <b>Singola</b> o <b>Twilio</b>.</p>
<img src="assets/do-not-localize/SMS.gif"/>
<p>Scopri come creare e inviare un SMS in questo <a href="../sms/create-sms.md">documentazione dettagliata</a>.</p>
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
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->


### Miglioramenti

**Reporting**

* La tabella e il grafico dei criteri di consenso sono ora disponibili nei rapporti globali di Journey. Questi widget ti consentono di tenere traccia dei profili esclusi dai criteri nelle azioni personalizzate. [Ulteriori informazioni](../reports/journey-global-report.md#journey-global)

   Per poter accedere ai widget più recenti, è necessario reimpostare le diverse dashboard di reporting. Per ulteriori informazioni sulla personalizzazione del dashboard, consulta [la documentazione dettagliata](../reports/global-report.md).

**Amministrazione**

* È ora possibile aggiornare il numero di telefono principale da utilizzare per il canale SMS. [Ulteriori informazioni](../configuration/primary-email-addresses.md)


## Versione di luglio 2022 {#july-2022-release}

### Nuove funzionalità

<table>
<thead>
<tr>
<th><strong>Nuovo flusso di messaggi in-line</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer fornisce un nuovo flusso per la creazione dei messaggi in Journey. La messaggistica in-line consentirà agli utenti di risparmiare tempo significativo e semplificherà il processo del flusso di lavoro per creare e inviare un’e-mail, una notifica push o un SMS in Journey Optimizer. Rimuovendo i messaggi come passaggio separato e rendendoli modificabili in linea come parte di un’azione su Journey Canvas, gli utenti dovranno fare clic su un numero inferiore di pulsanti e navigare in un numero inferiore di schermate per progettare e modificare il contenuto.</p>
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
<p>È ora possibile identificare i campi dello schema con le etichette che definiscono gli ambiti di utilizzo organizzativi o dei dati. Gli amministratori possono utilizzare l’interfaccia Autorizzazioni per definire i criteri di accesso che coprono i campi dello schema XDM e gestire meglio l’accesso dato a utenti o gruppi di utenti (utenti interni, esterni o di terze parti) e gestire l’accesso a tipi specifici di dati (ad esempio Dati personali sensibili/SPD).</p>
<p>L'utilizzo del controllo di accesso basato su attributi è attualmente limitato agli utenti selezionati e verrà distribuito a tutti gli ambienti in una versione futura.</p>
<p>Per ulteriori informazioni, consulta la <a href="../administration/attribute-based-access.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Processi decisionali in batch</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile eseguire processi di decisione batch dall'interfaccia utente, in modo che non sia necessario uno sviluppatore per eseguire processi api batch e posso ridurre il tempo necessario per il marketing. Questa nuova interfaccia ti consente di creare lavori e gestire i lavori correnti/passati.</p>
<img src="assets/do-not-localize/batch.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../offers/batch-delivery.md">documentazione dettagliata.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Utilizza automaticamente l'offerta più performante nelle tue decisioni (disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile utilizzare sistemi di modelli di ottimizzazione personalizzati nella gestione delle decisioni. Questo nuovo tipo di modello ti consente di ottimizzare e personalizzare le offerte in base ai segmenti e alle prestazioni delle offerte.</p>
<p>L’utilizzo di modelli AI di ottimizzazione personalizzati è attualmente limitato agli utenti selezionati e verrà distribuito a tutti gli ambienti in una versione futura.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../offers/ranking/personalized-optimization-model.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti

**Percorsi**

* **Terminazione di un percorso** - Nell’area di lavoro del percorso, il **Fine** l’attività è stata rimossa dalla palette. I tag finali vengono ora aggiunti per impostazione predefinita alla fine di ciascun percorso e non possono essere rimossi. Questo miglioramento consente di registrare meglio dove un cliente ha abbandonato il percorso, senza che sia necessaria alcuna azione da parte del professionista del percorso. Fai riferimento a [documentazione](../building-journeys/end-journey.md) e [video sulle funzioni](https://video.tv.adobe.com/v/345376){target=&quot;_blank&quot;}.


* La **Fuso orario del profilo** l’opzione è ora deselezionata per impostazione predefinita nelle proprietà del percorso. [Ulteriori informazioni](../building-journeys/timezone-management.md#timezone-from-profiles)

**Messaggi**

* I predefiniti per messaggi sono ora **superfici del canale**. [Ulteriori informazioni](../configuration/channel-surfaces.md)

**Amministrazione**

* **Edizione record PTR** - Ora, quando si aggiorna un record PTR, il tempo di elaborazione richiederà solo 3 ore. [Ulteriori informazioni](../configuration/ptr-records.md#processing)

* **Interfaccia utente dell’elenco consentita** - È ora possibile utilizzare l’interfaccia utente di Journey Optimizer per aggiungere nuovi indirizzi e-mail o domini all’elenco consentiti. [Ulteriori informazioni](../configuration/allow-list.md)

* **Aggiornamento logico elenco consentito** - Ora la logica di elenco consentita si applica non appena la funzione è abilitata, anche se l’elenco è vuoto. [Ulteriori informazioni](../configuration/allow-list.md#logic)

* **Parametri di tracciamento URL** - È ora possibile utilizzare l’editor espressioni per configurare i parametri di tracciamento URL nelle superfici dell’e-mail (ad es. predefiniti). [Ulteriori informazioni](../email/email-settings.md#url-tracking)

**Gestione delle decisioni**

* **Dimensione del pubblico** - Ora nell’interfaccia utente viene visualizzato un nuovo componente per la stima delle dimensioni del pubblico durante la creazione di una regola decisionale, durante la selezione di un segmento o di una regola per impostare un’idoneità per l’offerta o quando si aggiunge un segmento o una regola a un ambito decisionale.


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
<p>Ora puoi creare, personalizzare e inviare SMS in Journey Optimizer tramite un’integrazione con <b>Singola</b> o <b>Twilio</b>.</p>
<!--img src="assets/do-not-localize/SMS.gif"/-->
<p>Il canale SMS è attualmente disponibile solo per un set di organizzazioni (disponibilità limitata). Per ulteriori informazioni, contatta il tuo rappresentante Adobe.</p>
<p>Scopri come creare e inviare un SMS in questo <a href="../sms/create-sms.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Maggiore impatto sull’immagine grazie all’integrazione con Adobe Stock</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Il plug-in per l’integrazione di Adobe Stock e Adobe Journey Optimizer E-mail Designer offre ai clienti un modo semplice di navigare, concedere in licenza e salvare le immagini da utilizzare nella creazione dei messaggi. </br> Il nuovo <b>Trova foto simili</b> consente inoltre di individuare le foto Stock che corrispondono al contenuto, al colore e alla composizione delle immagini. </p>
<!--img src="assets/do-not-localize/stock-rn.gif"/-->
<p>Per ulteriori informazioni, consulta la <a href="../email/stock.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Utilizza indirizzi Ccn e-mail in tutte le e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile utilizzare la funzionalità CCN (copia per conoscenza nascosta) dell’e-mail per memorizzare le e-mail inviate da Adobe Journey Optimizer. Abilita questa opzione nei tuoi predefiniti e-mail in modo che ogni e-mail inviata venga copiata in modalità cieca nell’indirizzo CCN.</p>
<!--img src="assets/do-not-localize/bcc-rn.gif"/-->
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
<p>You can now use personalized optimization model systems in Decision Management. This new type of model allows you to optimize and personalize offers based on segments and offer performance.</p>
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
<th><strong>Copiare oggetti tra le sandbox</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi ricreare le esperienze da una sandbox di Journey Optimizer a un'altra, ad esempio da una sandbox non di produzione a una sandbox di produzione. Questa nuova funzionalità copia un intero percorso, inclusi gli oggetti da cui dipende l’esecuzione corretta del percorso, da un ambiente all’altro. Oltre ai percorsi, puoi anche copiare altri componenti come Offerte, Messaggi, Schemi, Set di dati, Origini dati, Eventi e Azioni.</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/copy-to-sandbox.md">documentazione dettagliata</a>.
</td>
</tr>
</tbody>
</table>




### Miglioramenti

**Gestione delle decisioni**

* **Supporto di file HTML e JSON** - È ora possibile trascinare file HTML e JSON esterni dalla libreria delle risorse di Adobe Experience Cloud nel contenuto della rappresentazione dell’offerta. [Ulteriori informazioni](../offers/offer-library/add-representations.md#html-json)


**E-mail**

* **Salva come modello** - È ora possibile salvare un contenuto e-mail come modello e riutilizzarlo durante la creazione di altri messaggi. [Ulteriori informazioni](../email/email-templates.md)


**Amministrazione**

* **Parametri URL di tracciamento anteprima** - Quando configuri un predefinito di messaggio, se definisci i parametri di tracciamento URL, ora viene visualizzata un’anteprima dinamica dell’URL di tracciamento risultante. [Ulteriori informazioni](../email/email-settings.md#url-tracking)

* **Modifica del predefinito del messaggio** - Al momento dell’aggiornamento di un predefinito per messaggi, il tempo di elaborazione può richiedere solo 3 ore. [Ulteriori informazioni](../configuration/channel-surfaces.md#edit-channel-surface)

* **edizione pool IP** - Ora, quando si aggiorna un pool IP, il tempo di elaborazione può richiedere solo 3 ore. [Ulteriori informazioni](../configuration/ip-pools.md#edit-ip-pool)




## Versione di maggio 2022 {#may-2022-release}

### Nuove funzionalità

<table>
<thead>
<tr>
<th><strong>Regole di frequenza dei messaggi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi impostare regole di business cross-channel che escluderanno automaticamente i profili sollecitati eccessivamente da messaggi e azioni.</p>
<!--img src="assets/do-not-localize/frequency-rn.gif"/-->
<p>Per ulteriori informazioni, consulta la <a href="../configuration/frequency-rules.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Gestione delle decisioni - Modello di ottimizzazione automatica di AI Ranking</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile utilizzare sistemi basati su modelli in Gestione delle decisioni. Questa nuova funzionalità classifica le offerte da visualizzare per un determinato profilo.</p>
<!--img src="assets/do-not-localize/optimization.gif"/-->
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
<p>È ora possibile monitorare le azioni eseguite dagli utenti sulle risorse di Adobe Journey Optimizer.</p>
<!--img src="assets/do-not-localize/audit-rn.gif"/-->
<p>Per ulteriori informazioni, consulta la <a href="../privacy/audit-logs.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti

**Personalizzazione**

* **Nuova funzione helper per per nascondere i caratteri** - `mask` la funzione helper ti consente di sostituire una parte di una stringa con caratteri &quot;X&quot;. [Ulteriori informazioni](../personalization/functions/string.md#mask)

**Pagine di destinazione**

* **Pagine di destinazione senza modulo** - È ora possibile creare e pubblicare una pagina di destinazione che non contiene un modulo e che non richiede alcuna azione da parte dei visitatori.
* **Modelli di pagina di destinazione** - È ora possibile salvare una pagina di destinazione come modello e riutilizzarla durante la creazione di altre pagine di destinazione. [Ulteriori informazioni](../landing-pages/lp-templates.md)
* **Torna alla pagina principale** - È ora possibile aggiungere un collegamento alla pagina principale da qualsiasi pagina secondaria all’interno della stessa pagina di destinazione.
* **Supporto JavaScript personalizzato** - È ora possibile aggiungere JavaScript personalizzati al contenuto della pagina di destinazione per eseguire uno stile avanzato o aggiungere comportamenti personalizzati alle pagine di destinazione.    [Ulteriori informazioni](../landing-pages/lp-custom-js.md)

**Percorsi**

* **Leggi segmento** - I percorsi dei segmenti di sola lettura ora passano allo stato Completato 30 giorni dopo l’esecuzione del percorso. Per i segmenti di lettura pianificati, trascorrono 30 giorni dall’esecuzione dell’ultima occorrenza. [Ulteriori informazioni](../building-journeys/read-segment.md)
* **Editor espressioni** - [limite](../building-journeys/functions/functionlimit.md) è stata aggiunta la funzione per consentire di limitare il numero di elementi di un elenco. La [sort](../building-journeys/functions/functionsort.md) consente ora di ordinare un oggetto elenco. È stato aggiunto anche il supporto di listObject al [disctinct](../building-journeys/functions/functiondistinct.md) e [distinctWithNull](../building-journeys/functions/functiondistinctwithnull.md) funzioni.

**Amministrazione**

* **Aggiornamento del dashboard di utilizzo della licenza** - Il dashboard di utilizzo della licenza disponibile in [!DNL Adobe Journey Optimizer] l&#39;interfaccia utente ora riflette il valore esatto per **Concesso in licenza** Ricchezza media del profilo. Vedrai un calo di questa rappresentazione metrica, il che significa che il limite di licenza è ora correttamente segnalato. [Ulteriori informazioni](../segment/license-usage.md)


## Versione di aprile 2022 {#april-2022-release}

### Miglioramenti

**Pagine di destinazione**

* **Nuova opzione per le caselle di controllo di consenso/rinuncia** - È ora possibile inserire una singola casella di controllo per l’opt-in/opt-out nelle pagine di destinazione dell’abbonamento. Gli utenti devono selezionare la casella di controllo per il consenso (opt-in) e deselezionarla per rimuovere il loro consenso (opt-out). [Ulteriori informazioni](../landing-pages/design-lp.md#define-lp-specific-content)

* **Campi delle pagine di destinazione precompilati** - È ora possibile consentire agli utenti di precompilare i campi della pagina di destinazione con le informazioni sul profilo. [Ulteriori informazioni](../landing-pages/create-lp.md#configure-primary-page)

**Gestione delle decisioni**

* **Decisioning API in Edge** - L’API Edge Decisioning può distribuire ed eseguire il rendering di offerte personalizzate gestite nella gestione delle decisioni. Puoi creare le offerte e altri oggetti correlati utilizzando l’interfaccia utente o le API per la gestione delle decisioni. [Ulteriori informazioni](../offers/api-reference/offer-delivery-api/edge-decisioning-api.md)

**Amministrazione**

* **Durata invio PTR** - La durata di validità dell&#39;editing PTR è ora di alcune ore. [Ulteriori informazioni](../configuration/ptr-records.md#processing)

**Progettazione e-mail**

* **20 nuovi modelli e-mail** sono ora disponibili per progettare il contenuto delle e-mail in Journey Optimizer.

**Interfaccia utente**

* **Aiuto contestuale nell’interfaccia utente di Journey Optimizer** - Sono stati aggiunti collegamenti di aiuto contestuali a più pagine in Journey Optimizer. Quando disponibile, fai clic sull’icona &quot;i&quot; per visualizzare una descrizione rapida della funzionalità corrente e accedere agli articoli correlati.

**Integrazione con Adobe Campaign Standard**

In qualità di cliente di Adobe Campaign Standard, ora puoi inviare e-mail, notifiche push e SMS utilizzando Journey Optimizer. Utilizza le nuove azioni integrate per sfruttare le funzionalità di messaggistica transazionale di Campaign Standard in Journey Optimizer.  [Ulteriori informazioni](../action/acs-action.md)

<!--
### Fixes

* Fixed an issue which caused tracking reports not to be available as the `JourneyActionId` was not properly populated. PLATIR-19854, CJM-26006
* Fixed an error on business events which could block the journey publication. CJM-25931
* Fixed an issue which could prevent images in Email Designer templates from being displayed. PLATIR-18176, CJM-25008
-->

## Versione di marzo 2022 {#march-2022-release}

### Miglioramenti

**Percorsi**

* Per evitare di includere campi non necessari nello schema di profilo unificato, lo schema Evento passaggio del percorso non è più abilitato per impostazione predefinita per i profili. Se necessario, puoi attivarlo. [Ulteriori informazioni](../reports/sharing-overview.md)
* I nuovi eventi dei passaggi relativi ai processi di esportazione ora vengono inviati da Journey Optimizer ad Adobe Experience Platform. Nella documentazione sono stati aggiunti esempi di query. [Ulteriori informazioni](../reports/query-examples.md)

**Gestione delle decisioni**

* Ora puoi specificare se il limite di offerta viene applicato a tutti gli utenti o a un profilo specifico e a tutti i posizionamenti o per posizionamento. [Ulteriori informazioni](../offers/offer-library/add-constraints.md#capping)
* L’API Batch Decisioning consente alle organizzazioni di utilizzare la funzionalità di gestione delle decisioni per tutti i profili in un dato segmento in una chiamata. Il contenuto dell’offerta per ogni profilo del segmento viene inserito in un set di dati AEP dove è disponibile per flussi di lavoro batch personalizzati. [Ulteriori informazioni](../offers/api-reference/offer-delivery-api/batch-decisioning-api.md)

**Amministrazione**

* Ora puoi abilitare/disabilitare il collegamento di annullamento all’abbonamento in/dall’intestazione dell’e-mail a livello di predefinito del messaggio e impostare un URL di annullamento dell’abbonamento personalizzato a livello di messaggio. [Ulteriori informazioni](../configuration/channel-surfaces.md#list-unsubscribe)
* L’elenco Consentiti può ora essere abilitato e disabilitato tramite [!DNL Journey Optimizer] interfaccia sulle sandbox di produzione e non di produzione. [Ulteriori informazioni](../configuration/allow-list.md#enable-allow-list)

**Personalizzazione**

* Ora puoi salvare più di 40 espressioni di personalizzazione nella libreria . [Ulteriori informazioni](../personalization/personalization-library.md)

## Versione di febbraio 2022 {#feb-2022-release}

### Nuove funzionalità

<table>
<thead>
<tr>
<th><strong>Pagine di destinazione dell’abbonamento</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile creare e progettare pagine di destinazione in Journey Optimizer e indirizzare gli utenti a moduli online in cui possono acconsentire o rinunciare alla ricezione delle comunicazioni o abbonarsi a un servizio specifico, ad esempio una newsletter.</p>
<p>Per ulteriori informazioni, consulta la <a href="../landing-pages/create-lp.md">documentazione dettagliata</a> e correlati <a href="../landing-pages/lp-use-cases.md">caso d’uso del campione</a>.</p>
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
<p>Per ulteriori informazioni, consulta la <a href="../personalization/personalization-library.md">documentazione dettagliata</a>.</p>
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
The suppression list helps you with honoring the ISPs' feedback to preserve sending IP reputation. The allow list helps you ensure that you send only to those email addresses which are in the allowed list, and typically to ensure that you don't send mails to customers from your development sandbox.</p>
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
<p>Nel contenuto del messaggio di Journey Optimizer puoi ora aggiungere parametri UTM ai collegamenti: possono fornire dati aggiuntivi su quel collegamento e aiutarti a identificare dove e perché una persona ha fatto clic sul collegamento.</p>
<p>Per ulteriori informazioni, consulta la <a href="../configuration/channel-surfaces.md#configure-email-settings">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti

**Percorsi**

* Per ottimizzare le prestazioni, tutti i percorsi in modalità di test che non sono stati attivati per una settimana torneranno allo stato Bozza. [Leggi tutto](../building-journeys/testing-the-journey.md#important_notes)
* L’integrazione tra Journey Optimizer e Adobe Campaign Classic è stata ottimizzata per migliorare le prestazioni. La configurazione predefinita del limite è stata modificata in 4000 chiamate/5 minuti.    [Leggi tutto](../action/acc-action.md#important-notes)

**Reporting**

* È ora possibile filtrare le consegne in base al loro stato:
   * Dall’elenco Esecuzione messaggi, ora puoi escludere le bozze dall’elenco delle consegne.
   * Dai rapporti Live/Global puoi scegliere di escludere gli eventi di test.

* È ora possibile accedere ai rapporti relativi ai dati di ottimizzazione del tempo di invio: il numero di persone che hanno inviato messaggi immediatamente e il numero di persone che sono state inviate con un&#39;ottimizzazione di 1 ora, 2 ore di ottimizzazione, ecc.

<!--* decision management reports are now available in Journey Optimizer. You can access the following metrics: Offers sent - Offers' impression rate - Offers' click rate - Breakdown report on Offers' sent.-->

**Gestione delle decisioni**

* Le classificazioni e la classificazione AI sono ora raggruppate in un’unica scheda.

## Versione di gennaio 2022 {#january-2022-release}

### Nuove funzionalità

<table>
<thead>
<tr>
<th><strong>Percorsi: ottimizza la crescita IP con le condizioni del limite del profilo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Durante la configurazione di un <strong>Condizione</strong> in un percorso, ora puoi definire un limite del profilo. Questo nuovo tipo di condizione ti consente di impostare un numero massimo di profili per un percorso di percorso. Una volta raggiunto questo limite, i profili che entrano hanno un percorso alternativo. Questo ti consente di aumentare il volume delle consegne (IP ramp verso l’alto). Ad esempio, puoi aumentare le consegne su un dominio suddividendo l’esecuzione: inviare 1000 messaggi il giorno 1, 2000 il giorno 2, ecc.</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/condition-activity.md#profile_cap">documentazione dettagliata</a> e correlati <a href="../building-journeys/ramp-up-deliveries-uc.md">caso d’uso del campione</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Viaggi - Miglioramento del segmento di lettura</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La <strong>Lettura incrementale</strong> è stata aggiunta l’opzione a ricorrente <strong>Leggi segmento</strong> attività. Questa opzione ti consente di eseguire il targeting solo dei singoli utenti che sono entrati nel segmento dall’ultima esecuzione del percorso. La prima esecuzione esegue sempre il targeting di tutti i membri del segmento.</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">documentazione dettagliata</a>.
</td>
</tr>
</tbody>
</table>

### Miglioramenti

**Percorsi**

* Gli eventi di passaggio di Journey Optimizer possono ora essere collegati ad altri set di dati in [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html). La **profileID** nello schema predefinito del passaggio del percorso Evento , ora è definito come un campo di identità. [Ulteriori informazioni](../reports/sharing-overview.md#integration-cja)

**Gestione delle decisioni**

* Quando aggiorni un’offerta, un’offerta di fallback, una raccolta di offerte o una decisione di offerta a cui viene fatto riferimento direttamente o indirettamente in un messaggio pubblicato, gli aggiornamenti vengono ora rispecchiati automaticamente nel messaggio corrispondente, senza dover ripubblicarlo. [Ulteriori informazioni](../offers/offers-e2e.md#insert-decision-in-email)

* Quando si simulano le offerte che verranno consegnate per un determinato profilo di test, ora è possibile modificare le impostazioni di simulazione predefinite e visualizzare il codice corrispondente alle simulazioni che possono essere utilizzate per la risoluzione dei problemi. [Ulteriori informazioni](../offers/offer-activities/simulation.md#define-simulation-settings)

**Amministrazione**

* Gli amministratori possono ora modificare i record PTR con un sottodominio configurato CNAME. [Ulteriori informazioni](../configuration/ptr-records.md#edit-ptr-subdomains-cname)

**Personalizzazione**

* **Aggiungi ai preferiti** - Per migliorare l’efficienza quando si lavora con la personalizzazione, abbiamo introdotto il concetto di risparmio dei preferiti. L’aggiunta di attributi diversi al menu dei preferiti consente di accedere rapidamente agli elementi utilizzati con maggiore frequenza. [Ulteriori informazioni](../personalization/personalize.md#fav)
