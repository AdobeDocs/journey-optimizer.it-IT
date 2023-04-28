---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
description: Note sulla versione di Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: e0c8aaf114e1e60a49a721c894d14b0cc6b9f764
workflow-type: tm+mt
source-wordcount: '1860'
ht-degree: 82%

---

# Note sulla versione {#release-notes}

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese.

Le note sulle versioni precedenti sono disponibili in [questa pagina](release-notes-2022.md). Per ulteriori modifiche, puoi consultare anche la pagina dedicata agli [ultimi aggiornamenti della documentazione](documentation-updates.md).

[!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Iscriviti subito alla [newsletter trimestrale Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} e ricevi gli ultimi aggiornamenti dei prodotti, storie interessanti, casi d’uso, suggerimenti e altro ancora direttamente nella tua casella in entrata ogni trimestre.


## Note sulla versione di aprile 2023 {#apr-rn-2023}

<!--Information below is subject to change without prior notice until the release availability date. Updated documentation will be published at the release date, and direct links will be added in this page.

**Release date**: April 27, 2023-->

### Nuove funzionalità{#apr-2023-features}

<table>
<thead>
<tr>
<th><strong>Canale web (disponibilità generale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer sta espandendo le sue funzionalità cross-channel aggiungendo il supporto per il canale web. Ora puoi creare, modificare e visualizzare in anteprima le esperienze web come qualsiasi altro canale, tramite un’interfaccia visiva intelligente e intuitiva per personalizzare la user experience. Al momento, in Journey Optimizer puoi creare solo esperienze web nelle campagne.</p>
<img src="assets/do-not-localize/web-authoring.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../web/get-started-web.md">documentazione dettagliata</a>.</p>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Flusso di lavoro di avvio rapido per l’onboarding mobile (beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora disponibile il nuovo flusso di lavoro di avvio rapido per l’onboarding mobile. Utilizza questa nuova funzione di prodotto per configurare rapidamente l’SDK Mobile per iniziare a raccogliere e convalidare i dati degli eventi mobili e a inviare notifiche push mobili con Adobe Journey Optimizer. Questa funzionalità è accessibile tramite la home page di Data Collection come versione beta pubblica.</p>
<img src="../push/assets/mobile-wf-home.png"/>
<p>Per ulteriori informazioni, consulta la <a href="../push/mobile-onboarding-wf.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>New Journey dashboard (beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p> The Journey dashboard is now split in two tabs:</p>
<ul><li>Use the <strong>Overview</strong> tab to access a new dashboard which displays key metrics related to your journeys.</li>
<li>Use the <strong>Browse</strong> tab to access the list of all journeys.</li></ul>
<p>This capability is accessible in all journeys as a public beta.</p>
<img src="assets/do-not-localize/journey-dashboard.gif"/>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Personalized Optimization AI ranking model (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Personalized Optimization AI ranking models are now generally available in Decision Management. This new type of model allows you to optimize and personalize offers based on segments and offer performance.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>For more information, refer to the <a href="../offers/ranking/personalized-optimization-model.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->

### Miglioramenti {#april-2023-improvements}

**Percorsi**

* L’area di lavoro del percorso ora visualizza l’ID attività sulle attività dei messaggi e sui tag di fine. Questo migliora il reporting e il retargeting.
* È stato migliorato il layout del riquadro di configurazione, visualizzato in azioni, origini dati, eventi e percorsi.
* Sono state aggiunte nuove protezioni ai percorsi:
   * Il numero di attività in un percorso è ora limitato a 50. [Ulteriori informazioni](../start/guardrails.md#journeys-guardrails-journeys)
   * Numero di **percorsi vivi** in un’organizzazione ora è limitato a 100 per sandbox. I percorsi in modalità di prova non vengono presi in considerazione. [Ulteriori informazioni](../start/guardrails.md#journeys-guardrails-journeys)

* Quando si aggiunge un [E-mail](../email/create-email.md), [SMS](../sms/create-sms.md) o [Push](../push/create-push.md) in un percorso, la superficie viene ora preriempita, per impostazione predefinita, con l&#39;ultima superficie utilizzata per quel canale, nel percorso corrente.
* È ora possibile definire parametri di query statici o dinamici nelle azioni personalizzate. [Ulteriori informazioni](../action/about-custom-action-configuration.md#url-configuration)

**Generazione rapporti**

* Ora puoi esportare i rapporti di Journey Optimizer come PDF. [Ulteriori informazioni](../reports/global-report.md#export-reports)

**Progettazione contenuti**

* Adobe Journey Optimizer Content Designer è stato aggiornato e l’accesso a stili e componenti di progettazione è ora più semplice. Questa nuova versione offre una migliore esperienza utente e include prestazioni più elevate, compatibilità parziale in modalità scura e il supporto di nuovi standard di accessibilità.



## Note sulla versione di marzo 2023 {#mar-2023}

### Nuove funzionalità{#mar-2023-features}

<table>
<thead>
<tr>
<th><strong>Canale in-app (disponibilità generale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi inviare messaggi in-app personalizzati agli utenti dell’app all’interno di una campagna. Utilizza Journey Optimizer per progettare notifiche e personalizzare il layout, la visualizzazione, il testo e i pulsanti del messaggio per creare un’esperienza semplice.</p>
<img src="assets/do-not-localize/in-app.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../in-app/get-started-in-app.md">documentazione dettagliata</a>.</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Tracciamento dei clic SMS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con il tracciamento dei clic SMS, puoi monitorare le prestazioni degli URL abbreviati, identificare chi vi ha fatto clic e utilizzare questi dati per effettuare il retargeting di tali clienti con le campagne successive.</p>
<img src="assets/do-not-localize/sms-tracking.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../sms/create-sms.md#sms-content">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Utilizzare i tag nei percorsi (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In qualità di utente business di Journey Optimizer, adesso puoi organizzare gli oggetti aziendali utilizzando i tag. I tag rappresentano un modo rapido e semplice di classificare gli oggetti per migliorare la ricerca. Questa funzione è attualmente in versione beta e disponibile solo nei Percorsi.</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/tags.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>



### Miglioramenti {#mar-2023-improvements}

**Percorsi**

* La nuova **API di limitazione** consente di impostare un limite al numero di eventi inviati al secondo, evitando picchi di traffico eccessivi sui sistemi esterni o sulle API. Al raggiungimento del limite impostato, tutte le chiamate API successive vengono messe in coda ed elaborate il prima possibile, nell’ordine in cui sono state ricevute. Questa funzione supporta una sola configurazione di limitazione per tutte le sandbox. [Ulteriori informazioni](../configuration/external-systems.md)
* L’area di lavoro del percorso è stata ottimizzata per un’esperienza utente più semplice e migliorata. Alla fine di ogni percorso nell’area di lavoro, i segnaposto vuoti sono stati rimossi. Ora puoi semplicemente aggiungere le attività trascinandole alla fine di un percorso.
* Nell’area di lavoro del percorso, l’etichetta del tag **Fine** non viene più impostata automaticamente con il nome dell’attività precedente. Se necessario, gli utenti possono aggiungere manualmente un’etichetta personalizzata.
* Il timeout predefinito e la durata dell’errore nelle proprietà del percorso sono stati modificati da 5 a 30 secondi. [Ulteriori informazioni](../configuration/external-systems.md#timeout)
* Il tasso di limitazione predefinito nelle attività del segmento di lettura è stato modificato da 20.000 a 5.000 messaggi al secondo. [Ulteriori informazioni](../building-journeys/read-segment.md#configuring-segment-trigger-activity)
* È stata aggiunta una guardrail alla modalità di test per ascoltare solo gli eventi inviati tramite l’interfaccia. Gli eventi inviati tramite uno strumento esterno non vengono presi in considerazione. [Ulteriori informazioni](../building-journeys/testing-the-journey.md)


<!-- 
* When adding an Email, SMS or Push action in a journey, the surface is now pre-filled, by default, with the last used surface for that channel.
* A new type of system alert has been introduced. You can now get notified when a custom action fails. [Learn more](../reports/alerts.md)
* Timeout and error management has been improved in journeys. Timeout and error paths are now always added on the canvas. A new toolbar button is available to show/hide these paths. [Learn more](../building-journeys/journey-gs.md#timeout_and_error)
* The Journey dashboard is now split in two tabs:
    * Use the **Overview** tab to access a new dashboard which displays key metrics related to your journeys.
    * Use the **Browse** tab to access list of all journeys.
-->

**Gestione delle decisioni**

* Per evitare potenziale confusione con il recente rilascio della funzione dei tag in Adobe Experience Platform, i tag di Gestione delle decisioni sono stati rinominati in “Qualificatori di raccolta”.

   Tieni presente che anche se il termine “tag” non viene più utilizzato nell’interfaccia utente di Gestione delle decisioni, lo è ancora nei servizi back-end come API e set di dati.

* Ora puoi reimpostare il contatore del limite di offerta su base giornaliera, settimanale o mensile. [Ulteriori informazioni](../offers/offer-library/add-constraints.md#capping)

* Puoi anche scegliere quale evento di Adobe Experience Platform deve essere considerato come limite di offer decisioning. [Ulteriori informazioni](../offers/offer-library/add-constraints.md#capping)

* Nella schermata di creazione dei posizionamenti sono stati aggiunti ulteriori parametri. Questi consentono di controllare se un’offerta può essere duplicata in più posizionamenti e di specificare se il contenuto e i metadati dell’offerta devono essere inclusi nella risposta API. [Ulteriori informazioni](../offers/offer-library/creating-placements.md)

**Personalizzazione**

* Ora puoi includere nell’Editor espressioni il testo di fallback predefinito per gli attributi di profilo basati su stringhe. Questi valori verranno visualizzati se gli attributi selezionati non restituiscono alcun risultato. [Ulteriori informazioni](../personalization/personalization-build-expressions.md#add)

**Generazione rapporti**

* La funzionalità dei widget di reporting è stata migliorata con la possibilità di personalizzare la visualizzazione dei dati da parte degli utenti. Con questo miglioramento, gli utenti possono ora scegliere tra più opzioni di visualizzazione, tra cui grafico, tabella e grafici ad anello.

   Per poter accedere ai widget più recenti, è necessario reimpostare le diverse dashboard di reporting. Per ulteriori informazioni sulla personalizzazione delle dashboard, consulta la [documentazione dettagliata](../reports/global-report.md#modify-dashboard).

## Note sulla versione di febbraio 2023 {#feb-2023}

### Nuove funzionalità{#feb-2023-features}

<table>
<thead>
<tr>
<th><strong>Canale in-app (beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi inviare messaggi in-app personalizzati agli utenti dell’app all’interno di una campagna. Utilizza Journey Optimizer per progettare notifiche e personalizzare il layout, la visualizzazione, il testo e i pulsanti del messaggio per creare un’esperienza semplice.</p>
<p><strong>Attenzione</strong>: al momento questa funzione è disponibile nella versione beta e solo per utenti beta. Per partecipare al programma beta, contatta l’Assistenza clienti Adobe.</p>
<img src="assets/do-not-localize/in-app.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../in-app/get-started-in-app.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Esporta i set di dati Journey Optimizer nelle destinazioni di archiviazione cloud (beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile stabilire una connessione in tempo reale con le posizioni di archiviazione cloud per esportare il contenuto dei set di dati. Le destinazioni disponibili sono: archiviazione cloud Amazon S3, BLOB di Azure, Azure Data Lake Gen 2, area di destinazione dei dati, archiviazione cloud Google, SFTP.</p>
<p><strong>Attenzione</strong>: questa funzione è attualmente in versione beta ed è disponibile per tutti gli utenti di Adobe Journey Optimizer. Collabora con il tuo rappresentante Adobe per accedere alle destinazioni se non hai già accesso.</p>
<img src="assets/do-not-localize/gif-destinations.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../data/export-datasets.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--

<table>
<thead>
<tr>
<th><strong>Performance Measurement in campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now measure the performance of your campaigns across inbound and outbound through dedicated reports. Adobe Journey Optimizer reports can retrieve additional metrics to use in the <strong>Objective</strong> tab of your campaign reports. </p>
<img src="assets/do-not-localize/performance_report.gif"/>
<p>For more information, refer to the <a href="../privacy/data-hygiene.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>

+++ Learn more about Performance Measurement

The **[!UICONTROL Objective]** tab of your Campaign report allows you to better fine-tune your deliveries' reports by targeting one specific metric. With this feature, you can effectively track and analyze your campaign's performance and make informed decisions to improve your results.

The **[!UICONTROL Objectives]** listed are linked to **[!UICONTROL Datasets]** that define a connection to a system in order to retrieve additional information. A list of pre-configured **[!UICONTROL Objectives]** is available, but you can also customize your report by adding new **[!UICONTROL Datasets]** and defining your own objectives. 

By selecting the desired Objectives, the **[!UICONTROL Performance overview]** and **[!UICONTROL Campaign objective]** widgets provide a comprehensive and insightful summary of your delivery performance, allowing you to closely monitor and evaluate the success of your campaign.

With the **[!UICONTROL Campaign objective]** widget, you can also choose to compare your primary objective against another performance metric.

Note that each widget can be resized and deleted as needed.
+++




<table>
<thead>
<tr>
<th><strong>Use Tags in your Journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>As a Journey Optimizer practitioner, you can now organize your business objects using tags. Tags are a quick and easy way of classifying objects to improve search. Tags are currently only available for Journeys.</p>
</td>
</tr>
</tbody>
</table>

-->

### Miglioramenti {#feb-2023-improvements}

**Percorsi**

* Il campo **Periodo di attesa per il rientro** è stato aggiunto alle proprietà del percorso. Questo campo ti consente di definire il tempo di attesa prima di consentire a un profilo di accedere nuovamente al percorso in percorsi unitari (a partire da un evento o una qualifica di segmento). In questo modo si evita che i percorsi vengano attivati erroneamente più volte per lo stesso evento. Per impostazione predefinita, il campo è impostato su 5 minuti. [Ulteriori informazioni](../building-journeys/journey-gs.md#entrance)

* Sono stati apportati miglioramenti per le **date di inizio e di fine percorso**. Se non hai specificato una data di inizio, ora viene aggiunta automaticamente al momento della pubblicazione. Per i percorsi **Leggi segmento**, ora puoi aggiungere una data di fine. Questo consente ai profili di uscire automaticamente quando viene raggiunta la data. [Ulteriori informazioni](../building-journeys/journey-gs.md#dates)

<!--

* The Journey canvas has been enhanced for a simpler and improved user experience. At the end of each path in the canvas, the empty placeholders have been removed. You can now simply add your activities by dragging them anywhere between nodes. [Learn more](../building-journeys/using-the-journey-designer.md)

* Timeout and error management has been improved in journeys. Timeout and error paths are now always added on the canvas. A new toolbar button is available to show/hide these paths. [Learn more](../building-journeys/journey-gs.md#timeout_and_error)

* A new type of system alert has been introduced. You can now get notified when a custom action fails. [Learn more](../reports/alerts.md)

* The Journey dashboard is now split in two tabs:
    * Use the **Overview** tab to access a new dashboard which displays key metrics related to your journeys.
    * Use the **Browse** tab to access list of all journeys.
-->


**Amministrazione**

* **Elenco Consentiti**: è ora possibile scaricare l’elenco Consentiti come file .csv. [Ulteriori informazioni](../configuration/allow-list.md#download-allowed-list)

* **Superficie e-mail**: è stato aggiunto un controllo aggiuntivo alle impostazioni dell’area e-mail. Se il record MX per il sottodominio utilizzato in **Risposta all’indirizzo (e-mail)** o **Indirizzo e-mail CCN** non è configurato correttamente, non è più possibile creare la superficie e-mail. È necessario configurarla o utilizzarne un’altra [Ulteriori informazioni](../email/email-settings.md#reply-to-email)

* **Superficie e-mail**: nella sezione **Parametri di tracciamento URL** delle impostazioni della superficie dell’e-mail, il limite per ogni campo **Valore** è stato aggiornato da 255 caratteri a 5 KB per la compatibilità con il tracciamento di Adobe Analytics. [Ulteriori informazioni](../email/email-settings.md#url-tracking)

**Gestione delle decisioni**

* **Posizionamenti**: nella schermata di creazione dei posizionamenti sono stati aggiunti ulteriori parametri. Questi consentono di controllare se un’offerta può essere duplicata in più posizionamenti e di specificare se il contenuto e i metadati dell’offerta devono essere inclusi nella risposta API. [Ulteriori informazioni](../offers/offer-library/creating-placements.md)

* **Personalizzazione URL**: quando aggiungi URL come contenuto alle rappresentazioni delle offerte, ora puoi personalizzare tali URL utilizzando l’editor espressioni. [Ulteriori informazioni](../offers/offer-library/add-representations.md)

## Note sulla versione di gennaio 2023{#jan-2023-release}

### Nuove funzionalità{#jan-2023-features}

<table>
<thead>
<tr>
<th><strong>Igiene dei dati</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform offre una suite di funzionalità di igiene dei dati che ti consentono di gestire i dati archiviati tramite l’eliminazione programmatica di record e set di dati del consumatore. Questa funzionalità è ora disponibile per Adobe Journey Optimizer. </p>
<p>Puoi gestire gli archivi dati per garantire che le informazioni vengano utilizzate come previsto, che vengano aggiornate quando è necessario correggere dati non corretti e che vengano eliminate quando i criteri organizzativi lo ritengono necessario.</p>
<p><strong>Attenzione</strong>: le funzionalità di igiene dei dati sono attualmente disponibili solo per le organizzazioni che hanno acquistato le offerte aggiuntive <strong>Healthcare Shield</strong> e <strong>Privacy and Security Shield</strong>.</p><p>Per ulteriori informazioni, consulta la <a href="../privacy/data-hygiene.md">documentazione dettagliata</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Modelli di contenuto e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile creare modelli di contenuto autonomi da sfruttare tra percorsi e campagne per riutilizzarli rapidamente.</p> 
</p>
<img src="assets/do-not-localize/content-template.gif"/>
<p>Scopri come creare, modificare e utilizzare modelli di contenuto in <a href="https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/email-channel/content-templates.html?lang=it">questo video</a>. Per ulteriori informazioni, consulta la <a href="../email/content-templates.md">documentazione dettagliata</a>.
</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti {#jan-2023-improvements}

**Percorsi**

* Quando si aggiunge una **Qualificazione del segmento** o **Leggi segmento** in un percorso, lo spazio dei nomi viene ora precompilato, per impostazione predefinita, con l’ultimo spazio dei nomi utilizzato. Fai riferimento alle sezioni [Qualificazione del segmento](../building-journeys/segment-qualification-events.md#about-segment-qualification) e [Leggi segmento](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* Nell’area di lavoro del percorso, nella barra degli strumenti è disponibile un nuovo pulsante che consente di scaricare una schermata del percorso.

**E-mail Designer**

* Ora puoi esportare il contenuto delle e-mail dal menu **Esporta HTML**. I file esportati sono disponibili in un file di archivio (.ZIP).

**Amministrazione**

* Una nuova sottosezione fornisce consigli sulla creazione dell’indirizzo **Rispondi a (e-mail)** per garantire una corretta gestione delle risposte. [Ulteriori informazioni](../email/email-settings.md#reply-to-email)

* Durante la creazione o la modifica dei **Pool IP**, i record PTR associati vengono ora visualizzati nell’elenco IP e, al passaggio del mouse, sugli indirizzi IP selezionati. [Ulteriori informazioni](../configuration/ip-pools.md#create-ip-pool)

* Dopo aver selezionato un pool IP in una superficie del canale, le informazioni del record PTR sono ora visibili quando si passa il mouse sugli indirizzi IP. [Ulteriori informazioni](../email/email-settings.md#subdomains-and-ip-pools)

* È stata aggiornata l’interfaccia utente per la modifica dei [Record PTR](../configuration/ptr-records.md#edit-ptr-record) e dei [campi esecuzione](../configuration/primary-email-addresses.md).

* È stata migliorata l’interfaccia utente per la creazione e la modifica dei sottodomini. [Ulteriori informazioni](../configuration/delegate-subdomain.md)

* La schermata Elenco di soppressione dei **Caricamenti recenti** è stata aggiornata. [Ulteriori informazioni](../configuration/manage-suppression-list.md#recent-uploads)

**Campagne**

* Una richiesta cURL di esempio che consente l’esecuzione di campagne attivate da API viene ora generata automaticamente e resa disponibile nella schermata della campagna. [Ulteriori informazioni](../campaigns/api-triggered-campaigns.md)


**Personalizzazione**

* Sono disponibili nuove funzioni assistenza: formatCurrency, charCodeAt, stringToDate, toString, formatNumber e toHexString. Inoltre, la funzione toDateTimeOnly ora accetta tipi di campi stringa, data, long e int. [Ulteriori informazioni](../personalization/functions/functions.md)
