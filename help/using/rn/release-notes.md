---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
description: Note sulla versione di Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '1101'
ht-degree: 90%

---

# Note sulla versione {#release-notes}

Questa pagina elenca tutte le nuove funzionalità e i miglioramenti introdotti in [!DNL Journey Optimizer]. Per ulteriori modifiche, puoi consultare anche la pagina dedicata agli [ultimi aggiornamenti della documentazione](documentation-updates.md).

[!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Scopri di più su queste modifiche nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target=&quot;_blank&quot;}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Iscriviti alla [newsletter trimestrale di Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} e ricevi gli ultimi aggiornamenti dei prodotti, storie interessanti, casi d’uso, suggerimenti e altro ancora direttamente nella tua casella in entrata ogni trimestre.


## Ottobre 2022 {#oct-2022-release}

### Miglioramenti{#oct-2022-improvements}

**Percorsi**

* La **Forza il rientro sulla ricorrenza** è stata aggiunta un’opzione nei parametri ricorrenti di pianificazione dei segmenti di lettura. Questa opzione ti consente di far uscire automaticamente tutti i profili ancora presenti nel percorso all’esecuzione successiva. Quando l’opzione è disattivata, i profili devono terminare il percorso prima di poter reimmettere in un’altra occorrenza. [Ulteriori informazioni](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

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
<p>Le regole condizionali vengono create utilizzando un generatore di regole visive nell’editor espressioni, in cui puoi memorizzarle per un ulteriore riutilizzo in tutti i percorsi e le campagne.</p>
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
<p>In qualità di utente Journey Optimizer, ora puoi accedere agli avvisi di sistema tramite l’interfaccia utente per ricevere notifiche quando i percorsi non funzionano come previsto. Puoi visualizzare gli avvisi disponibili e abbonarti. Il primo avviso disponibile con questa versione ti avviserà se un’attività di lettura del segmento non ha elaborato alcun profilo durante l’intervallo di tempo definito. Ora che questo flusso di lavoro è disponibile, verranno introdotte ulteriori funzioni che possano sfruttarlo.</p>
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

* Il **Set di dati di entità** è ora disponibile come set di dati predefinito in Adobe Journey Optimizer. Questo set di dati di ricerca include metadati per arricchire le informazioni di tracciamento e feedback sui set di dati. Questo ti aiuterà a migliorare i rapporti e le query con dati più comprensibili. [Ulteriori informazioni](../start/datasets-query-examples.md#entity-dataset)
* È stata aggiunto un nuovo guardrail ai percorsi unitari (che iniziano con un evento o una qualificazione di segmento) per evitare che i percorsi vengano erroneamente attivati più volte per lo stesso evento. Per impostazione predefinita, il rientro nel profilo viene ora bloccato temporaneamente per 5 minuti. [Ulteriori informazioni](../start/guardrails.md#events-g)

**Amministrazione**

* Quando si attiva o si disattiva l’elenco Consentiti, ora viene visualizzato una nuova avvertenza per specificare gli effetti di ogni azione. [Ulteriori informazioni](../configuration/allow-list.md#enable-allow-list)
* È stata aggiornata l’interfaccia utente per creare superfici di canale e pool IP, gestire gli elenchi di soppressione e Consentiti e configurare il canale SMS.
* Ora, quando si crea la prima superficie di canale per un determinato sottodominio, il tempo di elaborazione richiederà 10 minuti anziché 10 giorni e solo fino a 3 ore per le superfici successive che utilizzano quello stesso sottodominio. [Ulteriori informazioni](../configuration/channel-surfaces.md#create-channel-surface)

<!--* Now when downloading the suppression list as a CSV file, you can choose the file that was previously generated, or generate a new file.-->
* È stata aggiornata l’interfaccia utente per la creazione dei predefiniti per pagina di destinazione e dei sottodomini della pagina di destinazione. [Ulteriori informazioni](../configuration/lp-subdomains.md)

**Controlli di audit**

* Con Journey Optimizer puoi identificare le azioni eseguite dagli utenti nel sistema su vari servizi e funzionalità come campagne, percorsi, messaggi, pagine di destinazione, ecc. Le risorse del registro di controllo ora includono modifiche su varie altre azioni e vengono registrate automaticamente al verificarsi dell’attività. Per ulteriori informazioni, consulta [questa pagina](../privacy/audit-logs.md).

**Supporto per l’archiviazione**

* Il nuovo **Set di dati di entità** include un campo Modello che consente di esportare il formato e la struttura dei messaggi inviati su tutti i canali a scopo di archiviazione. [Ulteriori informazioni](../configuration/archiving-support.md)

**Pagine di destinazione**

* Ora puoi utilizzare dati contestuali provenienti da un’altra pagina all’interno della stessa pagina di destinazione. Ad esempio, se colleghi una casella di controllo a un elenco di iscrizioni nella pagina di destinazione principale, puoi utilizzare tale elenco di iscrizioni nella pagina secondaria di ringraziamento. [Ulteriori informazioni](../landing-pages/lp-content.md#use-primary-page-context)

<!--* When configuring the primary page, you can now create additional data to enable storing information when the landing page is being submitted. [Learn more](../landing-pages/lp-content.md#use-additional-data)-->

<!--* You can now use information that was submitted on a landing page to send communications to your customers. For example, if a user subscribes to a given subscription list, you can leverage that information to send an email recommending other subscription lists to that user.-->

### Altre modifiche{#sept-2022-other}

* La modalità Burst di un percorso è stata sostituita dalla modalità Consegna rapida di una campagna. [Ulteriori informazioni](../campaigns/create-campaign.md#rapid-delivery)
* Per migliorare le prestazioni, i gruppi di campo evento di un’esperienza non possono più essere utilizzati nei percorsi che iniziano con un’attività Leggi segmento, Qualificazione del segmento o Evento di business. Questo cambiamento è applicabile solo ai nuovi percorsi. Quelli esistenti manterranno il comportamento corrente. [Ulteriori informazioni](../start/guardrails.md#expression-editor)
* È stato rimosso il limite di 1 ora per i percorsi con Leggi segmento pianificati. Questi percorsi ora possono essere eseguiti senza ritardi.

