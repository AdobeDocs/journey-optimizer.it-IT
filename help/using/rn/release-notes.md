---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Note sulla versione di Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 181d3d050177730f07454024e5d1a531724b4886
workflow-type: tm+mt
source-wordcount: '2294'
ht-degree: 19%

---

# Note sulla versione {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novità"
>abstract="**Adobe Journey Optimizer** offre continuamente nuove funzionalità, miglioramenti alle funzionalità esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese."

[!DNL Adobe Journey Optimizer] segue un modello di distribuzione continua, che consente ad Adobe di fornire nuove funzionalità, miglioramenti e correzioni su base continuativa. Questo approccio consente un rollout scalabile e graduale delle funzionalità per garantire prestazioni e stabilità in tutti gli ambienti.

A causa di questo modello, le note sulla versione vengono aggiornate prima del successivo rilascio mensile. Per informazioni dettagliate sul ciclo di rilascio e sulle fasi di disponibilità, consulta [Ciclo di rilascio di Journey Optimizer](releases.md).

[!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche sono disponibili nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.

## Aggiornamenti di maggio 2026 {#may-26-rn}

<table>
<thead>
<tr>
<th><strong>Simulazione percorso</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi impostare il percorso su <strong>Simulazione</strong>. Questa modalità ti consente di convalidare la logica utilizzando <strong>utenti simulati</strong>. Si tratta di profili temporanei creati appositamente per la simulazione, che consentono di eseguire liberamente i test senza dover gestire profili di test persistenti in Adobe Experience Platform.</p>
<p>Questa funzionalità è disponibile per tutti i clienti come disponibilità limitata con funzionalità essenziali.</p>
<p><img src="assets/do-not-localize/simulate-user.gif"></p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/simulate-journey.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 5 maggio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Regole di decisione e ottimizzazione IA della formula di classificazione</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>[!DNL Adobe Journey Optimizer] ora utilizza l’intelligenza artificiale per rilevare le regole di decisioning e le formule di classificazione che possono essere semplificate. Nell’inventario, un indicatore rosso viene visualizzato su qualsiasi regola per la quale l’IA ha identificato un’opportunità di ottimizzazione. Facendo clic sull’indicatore, l’espressione originale viene visualizzata insieme alla versione suggerita dall’intelligenza artificiale. Da lì, puoi scaricare un file per rivedere il modo in cui i profili simulati vengono valutati da ogni versione e confermare che si comportano in modo identico, quindi sostituire l’espressione con quella ottimizzata.</p>
<p>Per ulteriori informazioni, consulta la <a href="../start/ai-features.md#decisioning-optimization">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 5 maggio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integrazioni</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La funzionalità <b>Integrazioni</b> consente di connettere origini dati di terze parti direttamente a Adobe Journey Optimizer. Semplificando il modo in cui vengono estratti i dati esterni e <b>i contenuti componibili</b>, questa funzione consente di distribuire messaggi personalizzati e dinamici su tutti i canali.</p>
<p>Precedentemente rilasciata in versione Beta, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p>Per ulteriori informazioni, consulta la <a href="../integrations/integrations.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 4 maggio 2026</p>
</td>
</tr>
</tbody>
</table>



## Disponibile a breve {#coming-soon}

Le seguenti funzionalità e miglioramenti sono pianificati per il rilascio nei prossimi giorni. **Le informazioni sono soggette a modifiche**. I collegamenti, le schermate e la documentazione aggiornati verranno condivisi una volta che tali aggiornamenti saranno disponibili in produzione.

### Nuove funzionalità {#comming-soon-features}

<table>
<thead>
<tr>
<th><strong>Collegamenti diretti nel Designer e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile aggiungere collegamenti diretti ai contenuti delle e-mail tramite un’opzione dedicata nel Designer e-mail.</p><p>In questo modo gli utenti vengono indirizzati direttamente al contenuto in-app corretto invece di essere reindirizzati a browser o app store, mantenendo il contesto e il coinvolgimento.</p>
<!--<p><img src="assets/do-not-localize/forms.gif"></p>-->
<p>Per ulteriori informazioni, consulta la <a href="../email/message-tracking.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 7 maggio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Frammenti percorso</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile creare <strong>frammenti di Percorso</strong> in Adobe Journey Optimizer. I frammenti di percorso sono set riutilizzabili di nodi di percorso che è possibile compilare una volta e rilasciare in qualsiasi percorso della sandbox. Che si tratti di un controllo di idoneità, di una logica di indirizzamento dei canali preferita o di una sequenza di benvenuto, i frammenti consentono ai team di spostarsi più rapidamente e rimanere coerenti, senza dover ogni volta ricostruire la stessa logica da zero.</p>
<p>Una volta creati, i frammenti vengono memorizzati in un <strong>Inventario frammenti</strong> dedicato e possono essere inseriti in qualsiasi percorso utilizzando l'attività <strong>Frammenti Percorso</strong>.</p>
<!--<p><img src="assets/do-not-localize/journey-fragments.gif"></p>-->
<p>Questa funzionalità sarà disponibile solo per un set di organizzazioni (disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<!--p>For more information, refer to the <a href="../building-journeys/journey-fragments.md">detailed documentation</a>.</p-->
<p>Data di disponibilità: 12 maggio 2026</p>
</td>
</tr>
</tbody>
</table>



## Note sulla versione di aprile 2026 {#april-26-rn}

<!--
**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/it/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.
-->

Nuove funzionalità e miglioramenti rilasciati all’inizio di aprile vengono annunciati con la data di disponibilità.

**Data di rilascio**: 28-29 aprile 2026

### Nuove funzionalità {#april-26-features}

<table>
<thead>
<tr>
<th><strong>Attività di query incrementale nelle campagne orchestrate</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Le campagne orchestrate</strong> ora supportano un'attività <strong>Incremental query</strong> che esegue il targeting solo di profili o eventi nuovi idonei dall'ultima esecuzione.

In questo modo le campagne ricorrenti si concentrano sui nuovi tipi di pubblico (nuove iscrizioni, nuovi membri fedeltà e segmenti simili), riducendo al contempo i carichi di lavoro per le query ed evitando invii ridondanti nel tempo.</p>
<p>Per ulteriori informazioni, consulta la <a href="../orchestrated/activities/incremental-query.md#incremental-query-configuration">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 30 aprile 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Parametri del mittente nell’intestazione e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con Journey Optimizer, ora puoi inviare e-mail in cui l’entità trasmittente (Sender) è diversa dall’entità autore (From). I client e-mail che supportano questa impostazione in genere la visualizzano come "Sender on account of From" (Mittente per conto di Da) o mostrano un indicatore "via". Compila i campi facoltativi <strong>Intestazioni mittente</strong> nelle impostazioni del canale e-mail per configurare questa funzionalità.</p>
<p><img src="assets/do-not-localize/sender-headers.gif"></p>
<p>Per ulteriori informazioni, consulta la <a href="../email/header-parameters.md#sender-header">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Campo CC nelle impostazioni del canale e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi configurare un campo CC (copia per conoscenza) opzionale nelle impostazioni del canale e-mail. A differenza di Ccn, i destinatari CC sono visibili al destinatario principale, consentendo una comunicazione trasparente e una proprietà più chiara.</p>
<p>Ciò ti consente di copiare automaticamente le parti interessate corrette su ogni messaggio, ad esempio un responsabile delle relazioni o il proprietario dell’account, garantendo al contempo che il cliente sappia chi contattare per il follow-up.</p>
<p>Il campo CC supporta la personalizzazione, in modo che una singola configurazione possa instradare dinamicamente le copie in base ai dati del profilo, rendendole scalabili tra più casi d’uso senza necessità di ulteriori configurazioni.</p>
<p><img src="../configuration/assets/email-config-cc.png"></p>
<p>Per ulteriori informazioni, consulta la <a href="../configuration/cc-email-field.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Copiare campagne orchestrate tra sandbox diverse</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Gli strumenti sandbox ora supportano la creazione di pacchetti e la copia di campagne orchestrate da una sandbox all’altra. Questo elimina la necessità di ricreare manualmente le campagne in ogni ambiente. Quando una campagna viene inserita in un pacchetto, i suoi oggetti dipendenti principali, come i criteri di unione e i messaggi, vengono inclusi automaticamente, in modo che la campagna importata sia pronta per la configurazione e la convalida. Per proteggere gli ambienti di produzione, tutte le campagne importate vengono visualizzate come bozza nella sandbox di destinazione, assegnando ai team un passaggio di revisione e approvazione prima che venga pubblicata qualsiasi campagna.</p>
<p><img src="assets/do-not-localize/oc-sandbox.gif"></p>
<p>Per ulteriori informazioni, consulta la <a href="../configuration/copy-objects-to-sandbox.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integrazione dell’agente di IA per Journey Optimizer tramite MCP</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer ora fornisce un server <strong>MCP (Model Context Protocol)</strong> che riunisce le operazioni di campagna, configurazione del canale e sandbox direttamente in qualsiasi applicazione compatibile con MCP. Con questa integrazione, utenti tipo diversi possono collaborare intorno agli stessi dati di orchestrazione. Invece di scrivere query sull’API REST di Adobe Journey Optimizer o navigare tra più schermate dell’interfaccia utente, puoi descrivere l’intento conversando e consentire al LLM di richiamare gli strumenti MCP appropriati. Questa funzionalità è attualmente disponibile in Claude Web e Desktop.</p>
<p>Questa funzionalità è disponibile per tutti i clienti di Public Beta.</p>
<p>Per ulteriori informazioni, consulta la <a href="../integrations/ajo-mcp.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Arbitrato percorso - Modelli AI</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile utilizzare <strong>modelli AI</strong> nelle formule di classificazione per aumentare automaticamente i punteggi di priorità del percorso in base agli attributi del profilo cliente e ai fattori contestuali, garantendo ai clienti l'accesso ai percorsi più rilevanti.</p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<p><img src="assets/do-not-localize/journey-arbitration-ai-models.gif"></p>
<p>Per ulteriori informazioni, consulta la <a href="../conflict-prioritization/journey-ai-models.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integrazione Adobe Express</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L'<b>integrazione di Adobe Express</b> in Adobe Journey Optimizer consente di utilizzare gli strumenti di modifica di Adobe Express direttamente durante la creazione del contenuto, consentendo di ridimensionare, rimuovere gli sfondi, ritagliare e convertire le risorse in JPEG o PNG.
</p>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p><img src="assets/do-not-localize/express_resize.gif"></p>
<p>Per ulteriori informazioni, consulta la <a href="../integrations/express.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 23 aprile 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Ottimizzare le e-mail per le caselle in entrata AI</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer ora include una nuova funzionalità che garantisce che le e-mail siano strutturate in modo ottimale per le caselle in entrata basate sull’intelligenza artificiale, come Apple Intelligence e Google Gemini in Gmail.</p>
<p>Poiché gli assistenti AI controllano sempre di più il modo in cui i destinatari leggono e agiscono sulle e-mail, questa funzione consente di generare e creare contenuti con prestazioni ottimali per tutte le attività di IA a valle, tra cui riepilogo, valutazione, definizione delle priorità ed estrazione intento.</p>
<p><img src="assets/do-not-localize/optimize-for-ai.gif"></p>
<p>Per ulteriori informazioni, consulta <a href="../email/llm-email-optimizer.md">Ottimizzare l'e-mail per le caselle in entrata AI</a>.</p>
<p>Data di disponibilità: 17 aprile 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Assistente AI per le espressioni Personalization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>[!DNL Adobe Journey Optimizer] ora include <strong>L'Assistente AI</strong> direttamente nell'editor di personalizzazione e nel Designer di posta elettronica che converte i prompt in linguaggio naturale in espressioni di personalizzazione e logica condizionale valide, senza richiedere alcuna esperienza di sintassi. Descrivi la personalizzazione che desideri ottenere e AI genera codice pronto all’uso che puoi applicare immediatamente o perfezionare tramite prompt di follow-up.</p>
<p>L'assistente lavora anche al contrario. Seleziona un’espressione esistente e chiedi di spiegarne la logica, identificare i problemi o suggerire miglioramenti. Questo lo rende utile non solo per la creazione di nuove espressioni, ma anche per la revisione e il debug di quelle esistenti all’interno del team.</p>
<p><img src="assets/do-not-localize/assistant-perso.gif"></p>
<p>Per ulteriori informazioni, consultare <a href="../content-management/generative-personalization-expressions.md">Assistente AI per espressioni Personalization</a>.</p>
<p>Data di disponibilità: 13 aprile 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Sperimentazione del percorso del percorso</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Utilizza il nuovo nodo <strong>Ottimizza</strong> per eseguire test A/B o esperimenti di slot machine per determinare il percorso migliore per soddisfare i KPI incentrati sul business. Questo strumento consente di testare e variare e di personalizzare le comunicazioni, la sequenza e la tempistica per raggiungere al meglio la clientela.
</p>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p>Come parte della disponibilità generale, questa versione introduce la selezione del <strong>tipo di esperimento</strong> (A/B o slot machine) e <strong>Scala il vincitore</strong> per percorsi unitari.</p>
<p><img src="assets/do-not-localize/optimize-experiment.gif"></p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/path-experimentation.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 7 aprile 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Casella in entrata</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Posta in arrivo</strong> è una funzionalità mobile disponibile con schede contenuto che consente ai clienti di creare una posizione centralizzata all'interno dell'app o del sito Web per visualizzare i messaggi inviati agli utenti. Questo estende la durata delle comunicazioni di marketing garantendo che i messaggi rimangano accessibili anche dopo essere stati chiusi.</p>
<p><img src="assets/do-not-localize/inbox.gif"/></p>
<p>Per ulteriori informazioni, consulta la <a href="../inbox/inbox-gs.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 7 aprile 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Supporto per le decisioni nel canale e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile utilizzare <strong>Decisioning</strong> per personalizzare e ottimizzare il contenuto dei messaggi di posta elettronica. Sfrutta punteggi di priorità, formule o modelli di IA per visualizzare le offerte e i contenuti più rilevanti per ogni destinatario.</p>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale). Con questa versione di disponibilità generale, sono ora supportate le pagine mirror.</p>
<p><img src="assets/do-not-localize/exd-email.gif"></p>
<p>Per ulteriori informazioni, consulta la <a href="../experience-decisioning/create-decision-policy.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 6 aprile 2026</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti {#april-26-improv}

#### IA

<!--
* **Brand alignment score in Campaign dashboard** - You can now assess your brand alignment score directly within your Campaign dashboard to ensure content stays on-brand. This allows you to verify guidelines at a glance without having to open the content designer.
-->

* **Prompt Assistant Enhancement** - Prompt Assistant migliora la generazione di contenuti AI analizzando i prompt degli utenti in tempo reale e identificando le lacune in termini di chiarezza, completezza e contesto. Suggerisce riscritture migliorate e fornisce indicazioni fruibili per arricchire i prompt con dettagli chiave come pubblico, tono e intento. La funzione fa anche domande mirate di chiarimento per aiutare gli utenti a perfezionare i loro input prima della generazione. Questo consente di ottenere output più precisi, di alta qualità e con un numero inferiore di iterazioni. [Ulteriori informazioni](../content-management/ai-assistant-prompting-guide.md#prompt-assistant)

  Data di disponibilità: 5 maggio 2026

#### Push

* **Personalizza ID app nelle impostazioni del canale** - Nelle impostazioni di configurazione del canale push, ora puoi personalizzare il campo **ID app** in modo che ogni destinatario possa ricevere una notifica push dal brand appropriato in base alle informazioni del proprio profilo. [Ulteriori informazioni](../push/push-configuration.md#app-id-personalization)

#### Funzione Decisioni

* **Allega frammenti agli elementi decisionali** - Journey Optimizer ora consente di allegare frammenti agli elementi decisionali che possono essere utilizzati nelle campagne e-mail e nell&#39;esperienza basata sul codice tramite i criteri decisionali. [Ulteriori informazioni](../experience-decisioning/fragments-decision-policies.md)

  Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).

* **I frammenti temporaneamente non disponibili vengono ignorati** - Se un frammento è temporaneamente non disponibile in Edge, quando si utilizzano frammenti negli elementi decisionali, viene ignorato e il rendering del percorso o della campagna continua invece di avere esito negativo. [Ulteriori informazioni](../experience-decisioning/fragments-decision-policies.md#temporary-unavailable-fragments)

  Data di disponibilità: 14 aprile 2026

<!--
#### SMS

* **Character Count** - In Adobe Journey Optimizer, you can now use the Character Count to monitor the length of your SMS messages in real time. It helps you see when a message will be split into multiple segments to better manage formatting and avoid unexpected increases in sending costs. [Read more](../sms/create-sms.md)

* **Opt-out and consent at phone number and sender** - For SMS, Journey Optimizer now records marketing consent and opt-out at the level of both the profile's phone number and short code. 

  This capability is currently only available for Sinch SMS configurations. [Read more](../sms/sms-configuration-sinch.md)

* **SMS inbounds to a custom dataset** - In **SMS API credentials**, route **inbound SMS** to a **custom, profile-enabled Experience Event dataset** you select instead of only the default tracking dataset. [Read more](../sms/sms-webhook.md)

* **Webhook interface enhancement** - When configuring SMS webhooks, the user interface now includes a built-in setup guide with practical examples, making it easier to align provider payloads and troubleshoot issues without leaving the configuration flow. [Read more](../sms/sms-webhook.md)

#### WhatsApp

* **WhatsApp interactive buttons and tracking** - WhatsApp in Journey Optimizer now supports interactive buttons required by your templates and use cases, along with built-in interaction tracking so you can measure engagement and analyze performance alongside your other channel reporting.
-->

#### Integrazioni Adobe Experience Manager

* **Supporto variante frammento di contenuto Adobe Experience Manager** - È possibile selezionare **varianti frammento di contenuto** (ad esempio varianti di lingua o di canale) durante l&#39;inserimento di frammenti di contenuto Adobe Experience Manager, con una gestione migliorata per gli scenari locali e multilingue. [Ulteriori informazioni](../integrations/aem-fragments.md#aem-variations)

  Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).

* **Contesto del frammento di contenuto di Adobe Experience Manager durante l&#39;authoring** - La selezione del frammento di contenuto rimane attiva durante lo spostamento tra campi di testo e blocchi di contenuto, quindi puoi aggiungere altri campi di frammento senza riaprire **Apri AEM Content Advisor** ogni volta. [Ulteriori informazioni](../integrations/aem-fragments.md)

  Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).

#### Progettazione e-mail

* **Editor HTML avanzato per contenuti e-mail** - La modalità HTML avanzata consente di modificare l&#39;origine HTML del contenuto nel Designer e-mail, aggiungere espressioni avanzate (ad esempio condizioni) nell&#39;origine e passare dalla visualizzazione HTML alla visualizzazione Desktop senza perdere le modifiche.

  Precedentemente disponibile solo per i modelli di contenuto e-mail, questa funzionalità è ora distribuita al contenuto di **e-mail** nel Designer e-mail (ad esempio, e-mail create in percorsi e campagne), oltre ai modelli di contenuto e-mail. Attualmente è in disponibilità limitata; per ottenere l’accesso, contatta il rappresentante Adobe. [Ulteriori informazioni](../email/email-expert-mode.md)

  Data di disponibilità: 9 aprile 2026

#### Ottimizzazione percorso percorso

* **Tipo di esperimento** - È ora possibile scegliere tra esperimento A/B (suddivisione fissa all&#39;inizio) o slot machine (suddivisione automatica con aggiornamenti settimanali del peso) durante la configurazione di un esperimento percorso. [Ulteriori informazioni](../building-journeys/path-experimentation.md)

  Data di disponibilità: 7 aprile 2026

* **Sperimentazione del percorso: ridimensiona il vincitore** - Ora puoi distribuire automaticamente o manualmente il percorso vincente di un esperimento al tuo pubblico completo. Una volta determinato il vincitore, puoi amplificarne la portata e l’efficacia senza monitorare costantemente l’esperimento. [Ulteriori informazioni](../building-journeys/path-experimentation.md#scale-winner)

  Questa funzionalità è disponibile solo in percorsi unitari (qualifiche attivate da eventi e pubblico). Non è disponibile per i percorsi Read audience.

  Data di disponibilità: 7 aprile 2026

* **Condizioni** - L&#39;attività [Ottimizza](../building-journeys/optimize.md) è il nuovo veicolo per la creazione di percorsi condizionali in percorsi. Sostituisce l&#39;attività **Condition** precedente, che è stata rimossa dall&#39;interfaccia utente. Tutta la logica condizionale viene mantenuta e ora viene gestita tramite le condizioni dell&#39;attività **Ottimizza**. [Ulteriori informazioni](../building-journeys/conditions.md)

  Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).

  Data di disponibilità: 7 aprile 2026

#### Campagne orchestrate

* **Variabili globali in Campagne orchestrate** - Le campagne orchestrate ora supportano variabili globali che possono essere definite una volta e riutilizzate in tutte le attività di un flusso di lavoro, semplificando la configurazione e garantendo la coerenza in valori dinamici, espressioni e personalizzazione dei contenuti. [Ulteriori informazioni](../orchestrated/global-variables.md)
* **Miglioramenti di Data Modeler** - Gli schemi relazionali orchestrati ora supportano chiavi composite che si estendono su più campi. Il caricamento di uno schema da un file DDL comporta anche l&#39;inserimento di enumerazioni e il caricamento da un file DDL o Excel crea automaticamente relazioni composite tra le tabelle. Nella vista relazione entità, i collegamenti compositi ora visualizzano l’intero set di coppie di campi tra le tabelle dopo il caricamento di un file. [Ulteriori informazioni](../orchestrated/gs-schemas.md)
