---
title: Note sulla versione
description: Note sulla versione di Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: cdaa6def25adcb63318c272efbfc6d7c4212a9dc
workflow-type: tm+mt
source-wordcount: '961'
ht-degree: 19%

---

# Note sulla versione {#release-notes}

Questa pagina elenca tutte le nuove funzionalità e i miglioramenti introdotti in [!DNL Journey Optimizer]. Per ulteriori modifiche, puoi consultare anche la pagina dedicata agli [ultimi aggiornamenti della documentazione](documentation-updates.md).

[!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Scopri di più su queste modifiche nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target=&quot;_blank&quot;}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Iscriviti alla [newsletter trimestrale di Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} e ricevi gli ultimi aggiornamenti dei prodotti, storie interessanti, casi d’uso, suggerimenti e altro ancora direttamente nella tua casella in entrata ogni trimestre.

## Versione di settembre 2022{#sept-2022-release}

### Nuove funzionalità{#sept-2022-features}


<!--
<table>
<thead>
<tr>
<th><strong>Dynamic content & new conditional rule builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create dynamic content to adapt the content of your messages based on conditional rules.</p> 
<p>Conditional rules are created using a visual rule builder within the Expression Editor, where you can store them for further reuse across your journeys and campaigns.</p>
<img src="assets/do-not-localize/dynamic-content.gif"/>
<p>For more information, refer to the <a href="../personalization/get-started-dynamic-content.md">detailed documentation</a>.
</td>
</tr>
</tbody>
</table>
-->

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
<p>Con il framework di governance DULE (Data Usage Labeling and Enforcement, etichettatura e applicazione dell’uso dei dati), Journey Optimizer ora può sfruttare i criteri di governance di Adobe Experience Platform per impedire che campi sensibili vengano esportati in sistemi di terze parti tramite azioni personalizzate. Se il sistema identifica un campo con restrizioni nei parametri delle azioni personalizzate, viene visualizzato un errore che impedisce la pubblicazione del percorso.</p>
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
<p>Adobe Experience Platform consente di adottare e applicare facilmente le politiche di marketing per rispettare le preferenze di consenso dei clienti. I criteri di consenso sono definiti in Adobe Experience Platform. In Journey Optimizer puoi applicare questi criteri di consenso alle azioni personalizzate. Ad esempio, puoi definire i criteri di consenso per escludere i clienti che non hanno acconsentito a ricevere comunicazioni e-mail, push o SMS.
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
<p>Journey Optimizer supporta la definizione dei ruoli utente e dei criteri di accesso per gestire le autorizzazioni per funzioni e oggetti. Attraverso <strong>Autorizzazioni Adobe Experience Cloud</strong>, puoi creare e gestire i ruoli e assegnare le autorizzazioni di risorse desiderate per questi ruoli. Le autorizzazioni ti consentono inoltre di gestire le etichette, le sandbox e gli utenti associati a un ruolo specifico.</p>
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
<p>In qualità di utente Journey Optimizer, ora puoi accedere agli avvisi di sistema tramite l’interfaccia utente per ricevere notifiche quando i percorsi non funzionano come previsto. Puoi visualizzare gli avvisi disponibili e abbonarti. Il primo avviso disponibile con questa versione ti avviserà se un’attività Leggi segmento non ha elaborato alcun profilo durante l’intervallo di tempo definito. Ora che il flusso di lavoro viene sbloccato, ne verrà fatto di più.</p>
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

* La **Set di dati di entità** è ora disponibile come set di dati predefinito in Adobe Journey Optimizer. Questo set di dati di ricerca include metadati per arricchire le informazioni sui set di dati di tracciamento e feedback. Questo ti aiuterà a migliorare i tuoi rapporti e le tue query con dati più comprensibili. [Ulteriori informazioni](../start/datasets-query-examples.md#entity-dataset)
* È stata aggiunta una nuova guardrail ai percorsi unitari (a partire da un evento o da una qualifica di segmento) per evitare che i percorsi vengano erroneamente attivati più volte per lo stesso evento. Per impostazione predefinita, il rientro del profilo viene bloccato temporaneamente per 5 minuti. [Ulteriori informazioni](../start/guardrails.md#events-g)

**Amministrazione**

* Quando si abilita o disabilita l’elenco Consentiti, ora viene visualizzato un nuovo avviso per descrivere in dettaglio gli impatti di ogni azione. [Ulteriori informazioni](../configuration/allow-list.md#enable-allow-list)
* È stata aggiornata l’interfaccia utente per la creazione di superfici dei canali, la creazione di pool IP, la gestione dell’elenco di soppressione e dell’elenco Consentiti e la configurazione del canale SMS.
<!--* Now when creating the first channel surface for a given subdomain, the processing time will take 10 minutes to 10 days, and only up to 3 hours for subsequent surfaces using that subdomain. Learn more
* Now when downloading the suppression list as a CSV file, you can choose the file that was previously generated, or generate a new file.
* The user interface for creating landing page presets and landing page subdomains has been improved. Learn more -->

**Controlli di audit**

* Con Journey Optimizer, puoi identificare le azioni eseguite dagli utenti nel sistema su vari servizi e funzionalità come campagne, percorsi, messaggi, pagine di destinazione, ecc. Le risorse del registro di controllo ora includono modifiche su varie altre azioni e vengono registrate automaticamente al verificarsi dell’attività. Per ulteriori informazioni, consulta [questa pagina](../privacy/audit-logs.md).

**Supporto per l&#39;archiviazione**

* Il nuovo **Set di dati di entità** include un campo Modello che consente di esportare il formato e la struttura dei messaggi inviati su tutti i canali a scopo di archiviazione. [Ulteriori informazioni](../configuration/archiving-support.md)

**Pagine di destinazione**

* Ora puoi utilizzare dati contestuali provenienti da un’altra pagina all’interno della stessa pagina di destinazione. Ad esempio, se colleghi una casella di controllo a un elenco di sottoscrizioni nella pagina di destinazione principale, puoi utilizzare tale elenco nella pagina secondaria &quot;grazie&quot;. [Ulteriori informazioni](../landing-pages/lp-content.md#use-primary-page-context)

* Durante la configurazione della pagina principale, è ora possibile creare dati aggiuntivi per abilitare la memorizzazione delle informazioni durante l’invio della pagina di destinazione. [Ulteriori informazioni](../landing-pages/lp-content.md#use-additional-data)

<!--* You can now use information that was submitted on a landing page to send communications to your customers. For example, if a user subscribes to a given subscription list, you can leverage that information to send an email recommending other subscription lists to that user.-->

### Altre modifiche{#sept-2022-other}

* La modalità Burst di percorso è stata sostituita dalla modalità di consegna rapida di Campaign. Per saperne di più
* Per migliorare le prestazioni, i gruppi di campi evento Experience non possono più essere utilizzati nei percorsi che iniziano con un segmento Read , una qualifica Segment o un’attività dell’evento aziendale. Questa modifica si applica solo ai nuovi percorsi. Quelli esistenti manterranno il comportamento corrente. [Ulteriori informazioni](../start/guardrails.md#expression-editor)
* È stato rimosso il limite di 1 ora per i percorsi di segmenti di lettura pianificati. Questi percorsi ora possono essere eseguiti senza ritardi.

