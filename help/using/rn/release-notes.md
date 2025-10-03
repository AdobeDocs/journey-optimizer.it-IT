---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
feature: Release Notes
topic: Content Management
description: Note sulla versione di Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 0d32f1f79314694a34e1e996ed405a4484dc863d
workflow-type: tm+mt
source-wordcount: '1726'
ht-degree: 90%

---

# Note sulla versione {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novità"
>abstract="**Adobe Journey Optimizer** offre continuamente nuove funzioni, miglioramenti a quelle esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese."

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese. [!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche sono disponibili nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.

## Note sulla versione di settembre 2025 {#25-9-rn}

**Data di rilascio**: 23-24 settembre 2025

### Nuove funzionalità {#sept-25-9-features}

<!-- table>
<thead>
<tr>
<th><strong>Public API to retrieve journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new Journey Optimizer API is now available to retrieve journeys and their associated objects such as campaigns and surfaces.</p>
<p>For more information, refer to the <a href="https://developer.adobe.com/journey-optimizer-apis/references/journeys-retrieve/">detailed documentation</a></p>
<p>Availability date: Sept 25, 2025</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Journey Optimizer Experimentation Accelerator</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer Experimentation Accelerator è un prodotto di intelligenza artificiale progettato migliorare ulteriormente la sperimentazione. Creato per gli utenti di Adobe Journey Optimizer e Adobe Target, unifica la gestione degli esperimenti, fornisce informazioni e opportunità basate sull’intelligenza artificiale e introduce un nuovo agente di sperimentazione.</p>
<p>Potrai scoprire:</p>
<ul>
<li><strong>Inventario unificato degli esperimenti:</strong> visualizza, filtra e gestisci rapidamente tutti gli esperimenti da Adobe Journey Optimizer e Adobe Target in un’unica area di lavoro centrale.</li>
<li><strong>Insight e opportunità sull’esperimento IA:</strong> supera la semplice lettura dei dati con insight e consigli basati sull’intelligenza artificiale generativa. Ciascun esperimento ora evidenzia opportunità utilizzabili, corredate da motivazioni a supporto, in modo che i team possano decidere con maggiore sicurezza cosa testare successivamente.</li>
<li><strong>Supporto Multi-Armed Bandit (MAB) in Journey Optimizer:</strong> massimizza l’impatto riducendo il traffico sprecato con esperimenti Multi-Armed Bandit. Invece di suddividere i tipi di pubblico in modo uniforme, il MAB assegna automaticamente più visitatori alle varianti con le prestazioni migliori in tempo reale, in modo da poter fornire esperienze di maggior valore a una clientela più elevata e continuando ad apprendere al tempo stesso che cosa funziona.</li></ul>
<p><img src="assets/do-not-localize/experimentation-accelerator.gif"/></p>
<p>Per ulteriori informazioni, consulta la <a href="../content-management/experiment-accelerator.md">documentazione dettagliata</a></p>
<p>Data di disponibilità: 23 settembre 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>L’Agente Journey è ora disponibile.</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Basato su <a href="https://experienceleague.adobe.com/it/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator" target="_blank">Adobe Experience Platform Agent Orchestrator</a>, l’Agente Journey è disponibile in Journey Optimizer. Consente di analizzare i percorsi attraverso un’interfaccia in linguaggio naturale. L’agente rileverà i conflitti di pubblico o di pianificazione e gli abbandoni del profilo in un percorso per aiutarti a risolverli. Presto, potrai creare percorsi con supporto agentico.</p>
<p>Per ulteriori informazioni, consulta la <a href="https://experienceleague.adobe.com/it/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent-analyze" target="_blank">documentazione dettagliata</a></p>
<p>Data di disponibilità: 24 settembre 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Modalità scura in E-mail designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>E-mail designer di Journey Optimizer ora offre la possibilità di passare alla visualizzazione in modalità scura, in cui è possibile definire anche impostazioni personalizzate specifiche da mostrare solo per i destinatari che leggono le e-mail in modalità scura.</p>
<p>Si noti quanto segue:</p>
<ul>
<li>Il rendering finale in modalità scura può variare e dipende dal client e-mail del destinatario.</li>
<li>Non tutti i client e-mail supportano la modalità scura personalizzata. Inoltre, alcuni client e-mail applicano soltanto la propria modalità scura predefinita per tutte le e-mail ricevute. In entrambi i casi, non è possibile eseguire il rendering delle impostazioni personalizzate definite in E-mail designer.</li>
</ul>
<p><img src="assets/do-not-localize/dark-mode.gif"/></p>
<p>Per ulteriori informazioni, consulta la <a href="../email/dark-mode.md">documentazione dettagliata</a></p>
 <p>Data di disponibilità: 16 settembre 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Ottimizzazione del percorso</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Utilizza la nuova funzione Ottimizza nodo per eseguire il targeting di tipi di pubblico specifici oppure esegui test A/B per determinare il percorso migliore per soddisfare i KPI incentrati sull’azienda.</p>
<p>Questo strumento consente di testare e variare e di personalizzare le comunicazioni, la sequenza e la tempistica per raggiungere al meglio la clientela.</p>
<p>Questa funzionalità è in disponibilità limitata. Per ottenere l’accesso, contatta il rappresentante Adobe.</p>
<p><img src="assets/do-not-localize/optimize.gif"/></p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/optimize.md">documentazione dettagliata</a></p>
<p>Data di disponibilità: 4 settembre 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Metodo di delega personalizzato per sottodomini</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Oltre alla delega completa e al metodo CNAME, ora è disponibile un nuovo metodo di configurazione del sottodominio: il metodo di delega personalizzata consente di controllare e gestire completamente tutti gli aspetti del DNS necessari per la consegna, il rendering e il tracciamento dei messaggi.</p>
<p>Questa funzionalità è in disponibilità limitata. Per ottenere l’accesso, contatta il rappresentante Adobe.</p>
<p><img src="assets/do-not-localize/custom-delegation.gif"/></p>
<p>Per ulteriori informazioni, consulta la <a href="../configuration/delegate-custom-subdomain.md">documentazione dettagliata</a></p>
<p>Data di disponibilità: 4 settembre 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Utilizza i dati di Adobe Experience Platform per la personalizzazione e la funzione Decisioni</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Precedentemente rilasciata in versione Beta pubblica, questa funzionalità è ora disponibile per tutti gli ambienti. Con questa versione, sono stati introdotti i seguenti miglioramenti:</p>
<ul><li>Supporto per la personalizzazione della ricerca di set di dati nei canali in entrata.</li>
<li>È ora possibile utilizzare la funzione helper “datasetLookup” nei frammenti di espressione. Per il momento, questa funzionalità è disponibile per una parte limitata della clientela. Per potervi accedere, contatta il tuo rappresentante Adobe.</li>
<li>Un’opzione nell’interfaccia per la gestione del set di dati ora consente di abilitare i set di dati basati su record per la personalizzazione della ricerca, senza dover eseguire una chiamata API.</li>
<li>Il monitoraggio è stato migliorato per tenere traccia dello stato di acquisizione dei dati e sapere quando i set di dati sono pronti per la ricerca.</li>
<li>Le linee guida e i guardrail di utilizzo sono stati aggiornati per garantire prestazioni e affidabilità ottimali.</li>
<li>Ora è possibile sfruttare i set di dati di Adobe Experience Platform nelle regole di limitazione della funzione Decisioni.</li></ul></p>
<p>Per ulteriori informazioni, consulta la <a href="../data/lookup-aep-data.md">documentazione dettagliata</a></p>
<p>Data di disponibilità: 1 settembre 2025</p>
</td>
</tr>
</tbody>
</table>


### Miglioramenti {#sept-25-9-improvements}

* **Supporto webhook per campagne attivate da API**\
  Le campagne attivate da API ora supportano i webhook. Configura un URL del webhook per ricevere aggiornamenti di stato in tempo reale per ogni messaggio, migliorando l’osservabilità e abilitando il monitoraggio e l’automazione senza soluzione di continuità. [Ulteriori informazioni](../configuration/feedback-webhooks.md)

  Data di disponibilità: 29 settembre 2025

* **Supporto mTLS per il canale SMS**
Durante la configurazione di un provider SMS personalizzato, ora puoi abilitare l’autenticazione TLS reciproca (mTLS), che richiede sia al client che al server di confermare reciprocamente la propria identità prima che venga stabilita una connessione sicura. [Ulteriori informazioni](../sms/sms-configuration-custom.md) - Data di disponibilità: 23 settembre 2025

* **Schemi basati su modelli**\
  Gli schemi basati su modelli possono ora essere utilizzati per supportare le esigenze di modellazione relazionale nelle campagne orchestrate. [Ulteriori informazioni](../orchestrated/gs-schemas.md) - Data di disponibilità: 23 settembre 2025

* **Supporto per la ricerca di set di dati in percorsi**\
  Una nuova attività nei percorsi, **Ricerca set di dati**, consente di recuperare dinamicamente i dati dai set di dati dei record di Adobe Experience Platform durante il runtime. Sfruttando questa funzionalità, puoi accedere ai dati che potrebbero non trovarsi nel profilo o nel payload dell’evento, garantendo che le interazioni della clientela siano pertinenti e tempestive. [Ulteriori informazioni](../building-journeys/dataset-lookup.md) - Data di disponibilità: 23 settembre 2025

  Questa attività è disponibile solo per un set di organizzazioni (disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.

* **Supporto del reindirizzamento nelle azioni personalizzate del percorso**\
  I reindirizzamenti (302) sono ora supportati nelle azioni personalizzate del percorso. - Data di disponibilità: 23 settembre 2025

* **Avvisi di monitoraggio della configurazione dei canali**: nel caso si verifichi un errore di configurazione dei canali e-mail utilizzando il tipo di delega dei sottodomini personalizzato, ora è possibile iscriversi per ricevere avvisi di sistema, tramite e-mail o nel centro notifiche di Journey Optimizer. [Ulteriori informazioni](../reports/alerts.md#alert-channel-config-failure) - Data di disponibilità: 23 settembre 2025

* **Richieste di annullamento dell’iscrizione con un solo clic**: sono stati introdotti miglioramenti che rafforzano ulteriormente la gestione delle richieste di annullamento dell’iscrizione con un solo clic configurate in Gestito da Adobe, garantendo un’elaborazione affidabile e coerente. - Data di disponibilità: 23 settembre 2025

* **I parametri del corpo JSON nidificati sono ora supportati nell’autenticazione personalizzata**\
  Durante la configurazione dell’autenticazione personalizzata per un’azione personalizzata, sono ora supportati gli oggetti JSON nidificati (ad esempio, oggetti secondari all’interno di `bodyParams`). [Ulteriori informazioni](../datasource/external-data-sources.md#custom-authentication-mode) - Data di disponibilità: 18 settembre 2025

* **Ripristina quota limite oraria**: ora è possibile applicare una limitazione su base oraria per i set di regole del canale. Precedentemente disponibile in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti e consente di scegliere 1 ora (in precedenza 3 ore). [Ulteriori informazioni](../conflict-prioritization/channel-capping.md) - Data di disponibilità: 17 settembre 2025

* **Simulazione delle varianti di contenuto per tutti i canali in entrata**\
  Precedentemente disponibile solo per i canali di notifica e-mail, SMS e push, la simulazione delle varianti di contenuto ora si applica anche a tutti i canali in entrata. [Ulteriori informazioni](../test-approve/simulate-sample-input.md) - Data di disponibilità: 17 settembre 2025

* **Espressioni per le regole di limitazione della funzione Decisioni**: è ora possibile creare espressioni personalizzate per definire la soglia di una regola di limitazione per un elemento decisionale. [Ulteriori informazioni](../experience-decisioning/items.md#capping) - Data di disponibilità: 16 settembre 2025

* **Supporto di domini dinamici**: Journey Optimizer ora supporta la personalizzazione dell’URL completa/di base per i domini predefiniti accettati da Adobe. [Ulteriori informazioni](../personalization/personalization-build-expressions.md#where) - Data di disponibilità: 12 settembre 2025

  Questa funzionalità è in disponibilità limitata per una parte della clientela.

* **Webhook** - Questa versione introduce i seguenti miglioramenti per i webhook durante la configurazione di un provider SMS personalizzato:

   * Ora puoi definire lo scopo del webhook, in entrata o Feedback, a seconda del tipo di dati che desideri acquisire. [Ulteriori informazioni](../sms/sms-configuration-custom.md#webhook) - Data di disponibilità: 23 settembre 2025

   * L&#39;interfaccia per la configurazione delle parole chiave è stata migliorata per semplificarne la configurazione. [Ulteriori informazioni](../sms/sms-configuration-custom.md#webhook) - Data di disponibilità: 23 settembre 2025

* **SMS**

   * Durante la configurazione di un provider SMS personalizzato, è ora possibile definire una parola chiave **Default** utilizzata quando un SMS in arrivo contiene una parola chiave non riconosciuta. Puoi anche creare **Parole chiave personalizzate** per azioni specifiche. [Ulteriori informazioni](../sms/sms-configuration-custom.md) - Data di disponibilità: 23 settembre 2025

   * È ora possibile accedere alle risposte non definite di parole chiave in entrata inviate tramite un messaggio SMS, inclusi errori di battitura, parole o frasi non esplicitamente definite nella configurazione. Vengono archiviati nel set di dati **AJO Email Tracking Experience Event**, in **InboundMessage** per 13 mesi. Disponibile solo con il provider Sinch, Infobip e SMS personalizzato. - Data di disponibilità: 23 settembre 2025

<!--
* **Approval policy permissions**
  Added an option when creating or setting Approval Policy to prevent Journey/Campaign creators from approving their own objects. [Read more](../test-approve/approval-policies.md) - Availability date: Sept 23, 2025 
-->

### Disponibile a breve {#sept-25-9-soon}

Nei prossimi giorni, saranno rilasciati i seguenti miglioramenti e funzionalità. **Le informazioni sono soggette a modifiche**. I collegamenti, le schermate e la documentazione aggiornati verranno condivisi una volta che tali aggiornamenti saranno disponibili in produzione.

<!--table>
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
</table-->

<!--table>
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
</table-->

<!--table>
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
</table-->


<table>
<thead>
<tr>
<th><strong>Moduli personalizzati della pagina di destinazione</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con [!DNL Journey Optimizer] è ora possibile acquisire gli attributi di profilo tramite le pagine di destinazione.</p>
<p>Crea, progetta e gestisci moduli personalizzati adatti alle tue esigenze sulla base di un set di dati specifico. Puoi quindi sfruttare questi moduli nelle pagine di destinazione per aggiungere gli attributi di profilo desiderati nel set di dati definito per ciascun modulo.</p>
<p>Questa funzionalità è in disponibilità limitata. Per ottenere l’accesso, contatta il rappresentante Adobe.</p>
<p><img src="assets/do-not-localize/forms.gif"/></p>
<!--p>For more information, refer to the <a href="../landing-pages/lp-forms.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p-->
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
<!--p>For more information, refer to the <a href="../email/pdf-attachments.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p-->
</td>
</tr>
</tbody>
</table>



* **Avvisi su nuovi percorsi**\
  Sono disponibili nuovi avvisi preconfigurati per i percorsi:

   * Superamento del tasso di eliminazione dei profili: il rapporto tra i profili eliminati e i profili in ingresso negli ultimi 5 minuti che ha superato la soglia.
   * Superamento del tasso di errore delle azioni personalizzate: il rapporto tra gli errori delle azioni personalizzate e le chiamate HTTP riuscite negli ultimi 5 minuti che ha superato la soglia.
   * Superamento del tasso di errore dei profili: il rapporto tra i profili in errore e i profili in ingresso negli ultimi 5 minuti che ha superato la soglia.
<!--
  * [Profile Discard Rate Exceeded](../reports/alerts.md#profile-discard-rate-exceeded): Ratio of profile discards to entered profiles over the last 5 mins exceeded threshold.  
  * [Custom Action Error Rate Exceeded](../reports/alerts.md#custom-action-error-rate-exceeded): Ratio of custom action errors to successful HTTP calls over the last 5 mins exceeded threshold.  
  * [Profile Error Rate Exceeded](../reports/alerts.md#profile-error-rate-exceeded): Ratio of profiles-in-error to entered profiles over the last 5 mins exceeded threshold.-->

Puoi modificare i valori di soglia e iscriverti agli avvisi a livello di singolo percorso invece che globalmente.

<!-- Availability date: Sept XX, 2025-->


* **Supporto di attributi personalizzati con URL per l’annullamento dell’iscrizione con un solo clic**\
  Con Journey Optimizer, se il consenso è gestito al fuori di Adobe, puoi impostare un endpoint personalizzato esterno definendo un collegamento per l’annullamento dell’iscrizione con un solo clic nella configurazione dell’e-mail. Quando i destinatari fanno clic sul collegamento di annullamento dell’iscrizione, Journey Optimizer aggiunge alcuni parametri predefiniti specifici del profilo all’evento di aggiornamento del consenso.

  Per personalizzare ulteriormente l’indirizzo e-mail di annullamento dell’iscrizione con un solo clic, puoi definire gli attributi personalizzati che verranno aggiunti all’evento del consenso. Questa funzionalità è già disponibile per il collegamento personalizzato per l’annullamento dell’iscrizione con un solo clic a partire dalla versione del 25 agosto.

  <!-- Availability date: Sept XX, 2025-->
