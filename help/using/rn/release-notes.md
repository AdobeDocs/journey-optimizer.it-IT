---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
feature: Release Notes
topic: Content Management
description: Note sulla versione di Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: d93b7ce225294257f49caee6ac08cfb575611a93
workflow-type: tm+mt
source-wordcount: '1122'
ht-degree: 45%

---

# Note sulla versione {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novità"
>abstract="**Adobe Journey Optimizer** offre continuamente nuove funzioni, miglioramenti a quelle esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese."

[!DNL Adobe Journey Optimizer] segue un modello di distribuzione continua, che consente ad Adobe di fornire nuove funzioni, miglioramenti e correzioni su base continuativa. Questo approccio consente un rollout scalabile e graduale delle funzionalità per garantire prestazioni e stabilità in tutti gli ambienti.

A causa di questo modello, le note sulla versione vengono aggiornate tra le versioni mensili.  Una sezione dedicata agli [aggiornamenti più recenti](#updates-rn) evidenzia nuove funzionalità e miglioramenti man mano che vengono implementati in produzione, in modo da essere sempre informati di tutte le modifiche in tempo reale. <!--For full details about the release cycle and availability phases, see [Journey Optimizer release cycle](#releases.md).-->

[!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche sono disponibili nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.

## Note sulla versione di ottobre 2025 {#oct-25-10-rn}

**Data di rilascio**: giovedì 22 ottobre 2025

### Nuove funzionalità {#oct-25-10-features}

<table>
<thead>
<tr>
<th><strong>Ore/Esclusioni basate sul tempo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le ore di pausa consentono di definire esclusioni basate sul tempo per i canali E-mail, SMS, Push e WhatsApp. Assicura che non vengano inviati messaggi in specifici periodi di tempo, aiutandoti a rispettare le preferenze dei clienti e i requisiti di conformità.</p>
<p>Puoi applicare ore non interattive tramite set di regole, che possono essere assegnate a singole azioni in campagne o percorsi per un controllo preciso.</p>
<p>Le regole di orario non interattivo sono attualmente disponibili solo per un set di organizzazioni (disponibilità limitata). Per essere aggiunti alla lista d’attesa, contatta il tuo rappresentante Adobe.</p>
<img src="assets/do-not-localize/quiet-hour.gif">
<p>Per ulteriori informazioni, consulta la <a href="../conflict-prioritization/quiet-hours.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: giovedì 22 ottobre 2025</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Custom action monitoring and reporting</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>This capability provides better visibility into journey health and execution, including lifecycle status and performance alerts. You can now quickly understand when, where, and why an anomalous situation is occurring in a custom action.</p>
<img src="assets/do-not-localize/FILE.gif">
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p>
<p>Availability date: October 22, 2025</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>RCS Basic Messaging</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>With the new RCS Basic add-on offering, you can now deliver basic Rich Communication Services (RCS) messaging in Journey Optimizer, enabling the following enhanced messaging capabilities subject to provider and geographical support:</p>
<ul>
<li><strong>Branded and verified sender support:</strong> Send messages using verified business profiles with branding elements (logo, sender name, etc.).</li>
<li><strong>Message delivery insights:</strong> Receive detailed delivery reports including message status updates (e.g., sent, delivered, read).</li>
<li><strong>Link tracking:</strong> Embed and track URLs within RCS messages for engagement analytics.</li>
<li><strong>Fallback to SMS:</strong> Automatic fallback to SMS when the recipient's device does not support RCS or is temporarily unreachable via RCS.</li>
<li><strong>Basic message composition:</strong> Send basic text-based RCS messages.</li>
</ul>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Direct mail channel in Orchestrated campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Direct mail channel is now available in orchestrated campaigns. The Direct mail activity facilitates direct mail sending within your Orchestrated campaign, for both one-time and recurring messages. It serves to automate the process of generating the extraction file required by direct mail providers. You can combine channel activities into the Orchestrated campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Direct Mail channel in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Previously limited to Campaigns, Direct Mail channel is now available on the journey canvas, enabling you to incorporate Direct Mail into your journeys. Direct Mail can now be used in both batch and 1:1 journey scenarios, with support for file extraction configuration and time-based frequency settings.</p>
<p> Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>New API to retrieve Action Campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new Journey Optimizer API is now available, enabling you to programmatically retrieve and inspect campaign-related data such as details, versions, and configurations.</p>
<p>For more information, refer to the <a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/">detailed documentation</a>.</p>
<p>Availability date: October 22, 2025</p>
</td>
</tr>
</tbody>
</table-->

<!--<table>
<thead>
<tr>
<th><strong>New source connectors for loyalty apps</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>New source connectors are now available in Adobe Experience Platform for the Talon.One, Capillary and Kobie loyalty Apps. These connectors let you seamlessly stream loyalty data into Adobe Experience Platform and leverage these data in Journey Optimizer.</p>
<p>For more information, refer to the <a href="../start/get-started-sources.md">detailed documentation</a>.</p>
<p>Availability date: October 22, 2025</p>
</td>
</tr>
</tbody>
</table>-->

<!--table>
<thead>
<tr>
<th><strong>Decisioning support in email channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add Decision policies into email journeys and campaigns. Decision policies are containers for your offers that leverage the Decisioning engine to dynamically return the best content to deliver for each audience member.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<img src="assets/do-not-localize/FILE.gif">
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p>
<p>Availability date: October 22, 2025</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Messaggistica ad alta velocità per campagne e-mail attivate da API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Una nuova modalità di messaggistica transazionale ad alta velocità è disponibile nelle campagne attivate dall’API. Questa modalità è progettata per la messaggistica transazionale in tempo reale su larga scala e supporta fino a 5.000 transazioni al secondo con maggiore disponibilità. Questa modalità supporta anche i messaggi transazionali senza fare riferimento o creare profili cliente, ad esempio pagamento come ospite, conferma di un ordine, reimpostazioni della password, notifiche di sicurezza e altre notifiche di servizio/operative.</p>
<p>Questa funzionalità è disponibile solo per il canale e-mail, per le organizzazioni che hanno acquistato il componente aggiuntivo Adobe High Throughput Transactional Messaging. Per ulteriori informazioni, contatta il tuo rappresentante Adobe.</p>
<p>Per ulteriori informazioni, consulta la <a href="../campaigns/api-triggered-high-throughput.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: giovedì 22 ottobre 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Regole di targeting riutilizzabili</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Per risparmiare tempo e fatica, Journey Optimizer ora consente di creare regole riutilizzabili da un menu dell’interfaccia utente dedicato e di sfruttarle durante la creazione del targeting, come parte dell’ottimizzazione dei contenuti in una campagna o in un percorso, nell’attività Ottimizza percorso.</p>
<p>Le regole di targeting sono attualmente a disponibilità limitata. Per ottenere l’accesso, contatta il rappresentante Adobe. Questa funzionalità è disponibile solo per le organizzazioni che hanno acquistato il componente aggiuntivo Decisioning. Verrà introdotto progressivamente per tutti i clienti.</p>
<img src="assets/do-not-localize/targeting-rules.gif">
<p>Per ulteriori informazioni, consulta la <a href="../experience-decisioning/rules.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: giovedì 22 ottobre 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Avvisi nuovi Percorsi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sono disponibili nuovi avvisi preconfigurati per monitorare l’esecuzione del percorso:</p>
<ul><li><a href="../reports/alerts.md#alert-discard-rate">Frequenza eliminazioni profilo superata</a>: rapporto tra eliminazioni di profili e profili immessi negli ultimi 5 minuti ha superato la soglia</li>
<li><a href="../reports/alerts.md#alert-custom-action-error-rate">Frequenza errori azione personalizzata superata</a>: rapporto tra errori azione personalizzata e chiamate HTTP riuscite negli ultimi 5 minuti ha superato la soglia</li>
<li><a href="../reports/alerts.md#alert-profile-error-rate">Frequenza errori profilo superata</a>: rapporto tra profili in errore e profili immessi negli ultimi 5 minuti ha superato la soglia.</li></ul> <p>Puoi modificare i valori di soglia e iscriverti agli avvisi a livello di singolo percorso invece che globalmente.</p>
<p>Per ulteriori informazioni, consulta la <a href="../reports/alerts.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: mercoledì 14 ottobre 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Helper metadati esecuzione</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Nell’editor di personalizzazione è disponibile una nuova funzione helper "executionMetadata". Consente di aggiungere informazioni contestuali a qualsiasi azione nativa e di acquisirle in un set di dati per l’esportazione in sistemi esterni.</p>
<p>Questa funzionalità è in disponibilità limitata. Per ottenere l’accesso, contatta il rappresentante Adobe.</p>
<img src="assets/do-not-localize/execution-metadata.gif">
<p>Per ulteriori informazioni, consulta la <a href="../personalization/functions/helpers.md#execution-metadata">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: martedì 13 ottobre 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Experimentation Accelerator con agente di sperimentazione</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer Experimentation Accelerator ora include l’agente di sperimentazione, uno strumento di conversazione basato sull’intelligenza artificiale che consente di interagire con esperimenti, informazioni approfondite e opportunità. Migliora l’esperienza di Journey Optimizer Experimentation Accelerator, aiutandoti a eseguire gli esperimenti in modo più efficiente, scoprire cosa funziona e scoprire dove ottimizzarla successivamente.</p>
<p>Per ulteriori informazioni, consulta la <a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-experiment.html?lang=it" target="_blank">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: sabato 10 ottobre 2025</p>
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
<li>Per ulteriori dimensioni o volumi, puoi acquistare il componente aggiuntivo per gli allegati PDF. Per ulteriori informazioni, contatta il tuo rappresentante Adobe.</li>
</ul>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p><img src="assets/do-not-localize/pdf-attachments.gif"/></p>
<p>Per ulteriori informazioni, consulta la <a href="../email/pdf-attachments.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 30 settembre 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>API pubblica per recuperare i percorsi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora disponibile una nuova API di Journey Optimizer per recuperare i percorsi e i relativi oggetti associati, come campagne e superfici.</p>
<p>Per ulteriori informazioni, consulta la <a href="https://developer.adobe.com/journey-optimizer-apis/references/journeys-retrieve/">documentazione dettagliata</a></p>
<p>Data di disponibilità: 25 settembre 2025</p>
</td>
</tr>
</tbody>
</table>

<!--
## Latest updates {#updates-rn}

New capabilities and improvements released in the past weeks are listed below, with their availability date. They will be grouped with the next release notes content at the end of the month. See also the latest [release notes below](#latest-rn).
-->

### Miglioramenti {#updates-improvements}

<!--Availability date: October 22, 2025-->

**Campo di esecuzione per canale WhatsApp**

Oltre a E-mail e SMS, puoi sapere come aggiornare il campo di esecuzione predefinito per le consegne WhatsApp a livello di sandbox. È inoltre possibile ignorare il campo di esecuzione impostato a livello globale modificandolo nei parametri avanzati dell’attività di percorso WhatsApp o nella configurazione del canale WhatsApp. [Ulteriori informazioni](../configuration/primary-email-addresses.md)

Data di disponibilità: giovedì 22 ottobre 2025

**Supporto di attributi personalizzati per l’indirizzo Mailto (annulla iscrizione)**

Con Journey Optimizer, se il consenso è gestito al fuori di Adobe, puoi impostare endpoint personalizzati esterni definendo un collegamento per l’annullamento dell’iscrizione con un solo clic e un indirizzo e-mail di annullamento dell’iscrizione personalizzato nella configurazione dell’e-mail. Quando i destinatari fanno clic sul collegamento di annullamento dell’iscrizione, Journey Optimizer aggiunge alcuni parametri predefiniti specifici del profilo all’evento di aggiornamento del consenso.

Per personalizzare ulteriormente gli endpoint personalizzati, ora è possibile definire gli attributi personalizzati che verranno aggiunti all’evento di consenso. [Ulteriori informazioni](../email/list-unsubscribe.md#custom-attributes)

>[!AVAILABILITY]
>
>Questa funzionalità è già disponibile per l’**[!UICONTROL URL di annullamento dell’iscrizione con un solo clic]** da agosto 2025 ed è ora disponibile per l’opzione **[!UICONTROL Mailto (annulla iscrizione)]** in disponibilità limitata. Per ottenere l’accesso, contatta il rappresentante Adobe.

Data di disponibilità: 6 ottobre 2025

### Disponibile a breve {#oct-25-10-soon}

Nei prossimi giorni, saranno rilasciati i seguenti miglioramenti e funzionalità. **Le informazioni sono soggette a modifiche**. I collegamenti, le schermate e la documentazione aggiornati verranno condivisi una volta che tali aggiornamenti saranno disponibili in produzione.

#### Nuove funzionalità {#oct-25-10-soon-features}

<table>
<thead>
<tr>
<th><strong>Temi in E-mail designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi applicare rapidamente temi preapprovati per garantire la coerenza del brand in tutte le e-mail, velocizzare il processo di creazione delle campagne e creare e-mail di alta qualità in modo indipendente, riducendo al contempo la dipendenza dai team di design.</p>
<p>Precedentemente rilasciata nella versione beta, questa funzionalità è ora disponibile per un set di organizzazioni (disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<!--img src="assets/do-not-localize/themes.gif">
<p>For more information, refer to the <a href="../email/apply-email-themes.md">detailed documentation</a>.</p>
<p>Availability date: November 4, 2025</p-->
</td>
</tr>
</tbody>
</table>

#### Miglioramenti {#oct-25-10-soon-improvements}

**Decisioning nelle e-mail tramite modelli AI**

Ora puoi utilizzare i modelli AI per ottimizzare il contenuto migliore nell’e-mail tramite l’utilizzo di Decisioning. Ad esempio, questa funzionalità ti consente di offrire il contenuto migliore in base a eventi personalizzati come Acquisti, Clic su pulsanti, Aggiungi al carrello e così via.

<!--
<table>
<thead>
<tr>
<th><strong>New Web Push notifications channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer now supports Web Push notifications, expanding the push channel beyond mobile. You can seamlessly deliver notifications to both mobile and desktop browsers, enabling you to reach customers directly on their devices without requiring an app.</p>
<p>This enhancement allows you to engage users with timely, personalized messages in real time, leveraging the same authoring workflows and targeting capabilities already available for mobile push.</p>
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Custom action monitoring and reporting</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Custom action monitoring and reporting is now available. This capability provides better visibility into journey health and execution, including lifecycle status and performance alerts. You can now quickly understand when, where, and why an anomalous situation is occurring in a custom action.</p>
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p>
</td>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>New source connectors for loyalty apps</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>New source connectors are now available in Adobe Experience Platform for the Talon.One, Capillary, and Kobie loyalty apps. These connectors let you seamlessly stream loyalty data into Adobe Experience Platform and leverage these data in Journey Optimizer.</p>
</td>
</tr>
</tbody>
</table>


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
<p>This capability is available in Limited Availability. Contact your Adobe representative to gain access.</p>
<p><img src="assets/do-not-localize/forms.gif"/></p>
<p>For more information, refer to the <a href="../landing-pages/lp-forms.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p>
</td>
</tr>
</tbody>
</table>
-->
