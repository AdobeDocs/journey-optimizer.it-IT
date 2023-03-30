---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
description: Note sulla versione di Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 15b3b783f0a679e207a104d6333e96c92a02efb1
workflow-type: tm+mt
source-wordcount: '1346'
ht-degree: 79%

---

# Note sulla versione {#release-notes}

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese.

Le note sulle versioni precedenti sono disponibili in [questa pagina](release-notes-2022.md). Per ulteriori modifiche, puoi consultare anche la pagina dedicata agli [ultimi aggiornamenti della documentazione](documentation-updates.md).

[!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Iscriviti subito alla [newsletter trimestrale Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} e ricevi gli ultimi aggiornamenti dei prodotti, storie interessanti, casi d’uso, suggerimenti e altro ancora direttamente nella tua casella in entrata ogni trimestre.


## Note sulla versione di marzo 2023 {#mar-2023}

Le informazioni riportate di seguito sono soggette a modifiche senza preavviso fino alla data di disponibilità del rilascio. La documentazione aggiornata verrà pubblicata alla data di rilascio e in questa pagina verranno aggiunti collegamenti diretti.


### Nuove funzionalità{#mar-2023-features}

<!--
<table>
<thead>
<tr>
<th><strong>In-app channel (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now send personalized In-app messages to your app users within a campaign. Use Journey Optimizer to design notifications and customize the message layout, display, text, and buttons to create a seamless experience.</p>
<img src="assets/do-not-localize/in-app.gif"/>
<p>For more information, refer to the <a href="../in-app/get-started-in-app.md">detailed documentation</a>.</p>
</tr>
</tbody>
</table>
-->

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
<th><strong>Utilizzare i tag nei Percorsi (Beta)</strong><br/></th>
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

* Il nuovo **API di limitazione** consente di impostare un limite al numero di eventi inviati al secondo, evitando picchi di traffico eccessivi sui sistemi esterni o sulle API. Al raggiungimento del limite impostato, tutte le chiamate API successive vengono messe in coda ed elaborate il prima possibile, nell’ordine in cui sono state ricevute. Questa funzione supporta una sola configurazione di limitazione per tutte le sandbox. [Ulteriori informazioni](../configuration/external-systems.md)
* L’area di lavoro del Percorso è stata migliorata per un’esperienza utente più semplice e migliorata. Alla fine di ogni percorso nell&#39;area di lavoro, i portapacchi vuoti sono stati rimossi. Ora puoi semplicemente aggiungere le tue attività trascinandole alla fine di un percorso.
* Nell’area di lavoro del percorso, l’etichetta della **Fine** non viene più impostato automaticamente con il nome dell’attività precedente. Se necessario, gli utenti possono aggiungere manualmente un’etichetta personalizzata.
* Il timeout predefinito e la durata dell’errore nelle proprietà del percorso sono stati modificati da 5 a 30 secondi. [Ulteriori informazioni](../configuration/external-systems.md#timeout)
* Il tasso di limitazione predefinito nelle attività del segmento di lettura è stato modificato da 20.000 a 5.000 messaggi al secondo. [Ulteriori informazioni](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

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

<!--* Additional parameters have been added in placements creation screen. They allow you to control whether an offer can be duplicated across multiple placements, and to specify if the offer's content and metadata should be included in the API response. [Learn more](../offers/offer-library/creating-placements.md)-->

**Personalizzazione**

* Ora puoi includere nell’editor espressioni il testo di fallback predefinito per gli attributi di profilo basati su stringhe. Questi valori verranno visualizzati se gli attributi selezionati non restituiscono alcun risultato. [Ulteriori informazioni](../personalization/personalization-build-expressions.md#add)

<!--
**Reporting**

* The reporting widget functionality has been improved with the ability to customize how users view their data. With this improvement, users can now choose between multiple visualization options, including graph, table, and donut charts.

    To have access to the latest widgets, please note that you will have to reset the different reporting dashboards. For more information on dashboard customization, refer to the [detailed documentation](../reports/global-report.md#modify-dashboard).
-->

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

<!--
* **Placements** - Additional parameters have been added in placements creation screen. They allow you to control whether an offer can be duplicated across multiple placements, and to specify if the offer's content and metadata should be included in the API response. [Learn more](../offers/offer-library/creating-placements.md)
-->

* **Personalizzazione URL**: quando aggiungi URL come contenuto alle rappresentazioni delle offerte, ora puoi personalizzare tali URL utilizzando l’editor espressioni. [Ulteriori informazioni](../offers/offer-library/add-representations.md)

## Versione di gennaio 2023 {#jan-2023-release}

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
