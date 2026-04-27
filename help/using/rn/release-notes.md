---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Note sulla versione di Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 89b884cf1feb7af9fe52b14b4ae706013ed70247
workflow-type: tm+mt
source-wordcount: '3965'
ht-degree: 16%

---

# Note sulla versione {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novità"
>abstract="**Adobe Journey Optimizer** offre continuamente nuove funzionalità, miglioramenti alle funzionalità esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese."

[!DNL Adobe Journey Optimizer] segue un modello di distribuzione continua, che consente ad Adobe di fornire nuove funzionalità, miglioramenti e correzioni su base continuativa. Questo approccio consente un rollout scalabile e graduale delle funzionalità per garantire prestazioni e stabilità in tutti gli ambienti.

A causa di questo modello, le note sulla versione vengono aggiornate prima del successivo rilascio mensile. Per informazioni dettagliate sul ciclo di rilascio e sulle fasi di disponibilità, consulta [Ciclo di rilascio di Journey Optimizer](releases.md).

[!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche sono disponibili nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.

## Note sulla versione precedente al 26 aprile {#april-26-rn}

**Le note pre-release riportate di seguito sono soggette a modifica senza preavviso fino alla data di disponibilità della versione**. I collegamenti, le schermate e la documentazione aggiornata vengono pubblicati nelle note sulla versione, alla data di rilascio.

Consulta anche [Note pre-release di Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

Nuove funzionalità e miglioramenti rilasciati all’inizio di aprile vengono annunciati con la data di disponibilità.

**Data di rilascio**: 28-29 aprile 2026

### Nuove funzionalità {#april-26-features}

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
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
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
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
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
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Collegamenti diretti nel Designer e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile aggiungere collegamenti diretti ai contenuti delle e-mail tramite un’opzione dedicata nel Designer e-mail. In questo modo gli utenti vengono indirizzati direttamente al contenuto in-app corretto invece di essere reindirizzati a browser o app store, mantenendo il contesto e il coinvolgimento.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Cartelle per percorsi e campagne</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi organizzare i percorsi e le campagne in <strong>cartelle</strong> per migliorare la navigazione e la gestione nell'interfaccia.</p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
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
<p>Adobe Journey Optimizer ora fornisce un server <strong>MCP (Model Context Protocol)</strong> che riunisce le operazioni di campagna, fedeltà, configurazione dei canali e sandbox direttamente in qualsiasi applicazione compatibile con MCP. Con questa integrazione, utenti tipo diversi possono collaborare intorno agli stessi dati di orchestrazione. Invece di scrivere query sull’API REST di Adobe Journey Optimizer o navigare tra più schermate dell’interfaccia utente, puoi descrivere l’intento conversando e consentire al LLM di richiamare gli strumenti MCP appropriati. Questa funzionalità è attualmente disponibile in Claude Web e Desktop.</p>
<p>Questa funzionalità è disponibile per tutti i clienti di Public Beta.</p>
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
</td>
</tr>
</tbody>
</table>

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
<p>[!DNL Adobe Journey Optimizer] ora include <strong>L'Assistente AI</strong> direttamente nell'editor di personalizzazione che converte i prompt in linguaggio naturale in espressioni di personalizzazione e logica condizionale valide, senza richiedere alcuna esperienza di sintassi. Descrivi la personalizzazione che desideri ottenere e AI genera codice pronto all’uso che puoi applicare immediatamente o perfezionare tramite prompt di follow-up.</p>
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

<!--
<table>
<thead>
<tr>
<th><strong>Optimize email text for AI inboxes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer now includes a new capability that ensures your emails are optimally structured for AI-powered inboxes such as Apple Intelligence and Google Gemini in Gmail.</p>
<p>As AI assistants increasingly control how recipients read and act on email, this feature helps you author content that performs well across downstream AI tasks including summarization, triage, prioritization, and intent extraction.</p>
<p><img src="assets/do-not-localize/text-optimizer.gif"></p>
<p>For more information, refer to <a href="../email/llm-email-optimizer.md">Optimize email text for AI inboxes</a>.</p>
<p>Availability date: April 3, 2026</p>
</td>
</tr>
</tbody>
</table>
-->

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

* **Punteggio di allineamento del brand nel dashboard di Campaign**: ora puoi valutare il punteggio di allineamento del brand direttamente nel dashboard di Campaign per garantire che il contenuto rimanga nel brand. Questo consente di verificare le linee guida immediatamente senza dover aprire la finestra di progettazione del contenuto.

* **Prompt Assistant Enhancement** - Prompt Assistant migliora la generazione di contenuti AI analizzando i prompt degli utenti in tempo reale e identificando le lacune in termini di chiarezza, completezza e contesto. Suggerisce riscritture migliorate e fornisce indicazioni fruibili per arricchire i prompt con dettagli chiave come pubblico, tono e intento. La funzione fa anche domande mirate di chiarimento per aiutare gli utenti a perfezionare i loro input prima della generazione. Questo consente di ottenere output più precisi, di alta qualità e con un numero inferiore di iterazioni. [Ulteriori informazioni](../content-management/ai-assistant-prompting-guide.md)

#### Funzione Decisioni

* **Allega frammenti agli elementi decisionali** - Journey Optimizer ora consente di allegare frammenti agli elementi decisionali che possono essere utilizzati nelle campagne e-mail e nell&#39;esperienza basata sul codice tramite i criteri decisionali. Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).

* **I frammenti temporaneamente non disponibili vengono ignorati** - Se un frammento è temporaneamente non disponibile in Edge, quando si utilizzano frammenti negli elementi decisionali, viene ignorato e il rendering del percorso o della campagna continua invece di avere esito negativo. [Ulteriori informazioni](../experience-decisioning/fragments-decision-policies.md#temporary-unavailable-fragments)

  Data di disponibilità: 14 aprile 2026

#### Push

* **Personalizza ID app nelle impostazioni del canale** - Nelle impostazioni di configurazione del canale push, ora puoi personalizzare il campo **ID app** in modo che ogni destinatario possa ricevere una notifica push dal brand appropriato in base alle informazioni del proprio profilo.

#### SMS

* **Conteggio caratteri** - In Adobe Journey Optimizer è ora possibile utilizzare il Conteggio caratteri per monitorare la lunghezza dei messaggi SMS in tempo reale. Consente di visualizzare quando un messaggio verrà suddiviso in più segmenti per gestire meglio la formattazione ed evitare aumenti imprevisti nei costi di invio. [Ulteriori informazioni](../sms/create-sms.md)

* **Rinuncia e consenso al numero di telefono e al mittente** - Per gli SMS, Journey Optimizer registra ora il consenso al marketing e la rinuncia al livello sia del numero di telefono del profilo che del codice breve.

  Questa funzionalità è attualmente disponibile solo per le configurazioni Sinch SMS. [Ulteriori informazioni](../sms/sms-configuration-sinch.md)

* **SMS in entrata in un set di dati personalizzato** - In **Credenziali API SMS**, instradare **SMS in entrata** in un **set di dati Experience Event personalizzato e abilitato al profilo** selezionato anziché solo il set di dati di tracciamento predefinito. [Ulteriori informazioni](../sms/sms-webhook.md)

* **Miglioramento dell&#39;interfaccia del webhook** - Durante la configurazione dei webhook SMS, l&#39;interfaccia utente include ora una guida di installazione integrata con esempi pratici, che semplificano l&#39;allineamento dei payload del provider e la risoluzione dei problemi senza uscire dal flusso di configurazione. [Ulteriori informazioni](../sms/sms-webhook.md)

#### WhatsApp

* **Pulsanti interattivi WhatsApp e tracciamento** - WhatsApp in Journey Optimizer ora supporta i pulsanti interattivi richiesti dai modelli e dai casi d&#39;uso, insieme al tracciamento delle interazioni integrato, in modo da poter misurare il coinvolgimento e analizzare le prestazioni insieme al reporting degli altri canali.

#### Integrazioni Adobe Experience Manager

* **Supporto variante frammento di contenuto Adobe Experience Manager** - È possibile selezionare **varianti frammento di contenuto** (ad esempio varianti di lingua o di canale) durante l&#39;inserimento di frammenti di contenuto Adobe Experience Manager, con una gestione migliorata per gli scenari locali e multilingue. [Ulteriori informazioni](../integrations/aem-fragments.md#aem-variations)

  Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.

  Data di disponibilità: 3 aprile 2026

* **Contesto del frammento di contenuto di Adobe Experience Manager durante l&#39;authoring** - La selezione del frammento di contenuto rimane attiva durante lo spostamento tra campi di testo e blocchi di contenuto, quindi puoi aggiungere altri campi di frammento senza riaprire **Apri AEM Content Advisor** ogni volta. [Ulteriori informazioni](../integrations/aem-fragments.md)

  Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.

  Data di disponibilità: 1 aprile 2026

#### Configurazione

* **Autorizzazioni specifiche per le chiavi di crittografia dei parametri URL**. Per accedere e gestire le chiavi per la crittografia dei parametri URL, sono state create nuove autorizzazioni. È ora necessario disporre delle autorizzazioni **Visualizza registro chiavi** e **Gestisci registro chiavi**.

#### Campagne orchestrate

* **Miglioramenti di Data Modeler** - Gli schemi relazionali orchestrati ora supportano chiavi composite che si estendono su più campi. Il caricamento di uno schema da un file DDL comporta anche l&#39;inserimento di enumerazioni e il caricamento da un file DDL o Excel crea automaticamente relazioni composite tra le tabelle. Nella vista relazione entità, i collegamenti compositi ora visualizzano l’intero set di coppie di campi tra le tabelle dopo il caricamento di un file.

* **Variabili globali in Campagne orchestrate** - Le campagne orchestrate ora supportano variabili globali che possono essere definite una volta e riutilizzate in tutte le attività di un flusso di lavoro, semplificando la configurazione e garantendo la coerenza in valori dinamici, espressioni e personalizzazione dei contenuti.

#### Progettazione e-mail

* **Editor HTML avanzato per contenuti e-mail** - La modalità HTML avanzata consente di modificare l&#39;origine HTML del contenuto nel Designer e-mail, aggiungere espressioni avanzate (ad esempio condizioni) nell&#39;origine e passare dalla visualizzazione HTML alla visualizzazione Desktop senza perdere le modifiche.

  Precedentemente disponibile solo per i modelli di contenuto e-mail, questa funzionalità è ora distribuita al contenuto di **e-mail** nel Designer e-mail (ad esempio, e-mail create in percorsi e campagne), oltre ai modelli di contenuto e-mail. Attualmente è in disponibilità limitata; per ottenere l’accesso, contatta il rappresentante Adobe. [Ulteriori informazioni](../email/email-expert-mode.md)

  Data di disponibilità: 9 aprile 2026

* **Assistente AI per le espressioni di personalizzazione in E-mail Designer**. In E-mail Designer, seleziona un componente e utilizza **Aggiungi espressione** nella barra degli strumenti contestuale per descrivere la personalizzazione necessaria in linguaggio semplice, rivedere l&#39;espressione generata e inserirla senza uscire dalla finestra di progettazione. [Ulteriori informazioni](../content-management/generative-personalization-expressions.md#generate-email-designer)

  Data di disponibilità: 15 aprile 2026

#### Ottimizzazione percorso percorso

* **Tipo di esperimento** - È ora possibile scegliere tra esperimento A/B (suddivisione fissa all&#39;inizio) o slot machine (suddivisione automatica con aggiornamenti settimanali del peso) durante la configurazione di un esperimento percorso. [Ulteriori informazioni](../building-journeys/path-experimentation.md)

  Data di disponibilità: 7 aprile 2026

* **Sperimentazione del percorso: ridimensiona il vincitore** - Ora puoi distribuire automaticamente o manualmente il percorso vincente di un esperimento al tuo pubblico completo. Una volta determinato il vincitore, puoi amplificarne la portata e l’efficacia senza monitorare costantemente l’esperimento. [Ulteriori informazioni](../building-journeys/path-experimentation.md#scale-winner)

  Questa funzionalità è disponibile solo in percorsi unitari (qualifiche attivate da eventi e pubblico). Non è disponibile per i percorsi Read audience.

  Data di disponibilità: 7 aprile 2026

* **Condizioni** - L&#39;attività [Ottimizza](../building-journeys/optimize.md) è il nuovo veicolo per la creazione di percorsi condizionali in percorsi. Sostituisce l&#39;attività **Condition** precedente, che è stata rimossa dall&#39;interfaccia utente. Tutta la logica condizionale viene mantenuta e ora viene gestita tramite le condizioni dell&#39;attività **Ottimizza**. [Ulteriori informazioni](../building-journeys/conditions.md)

  Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).

  Data di disponibilità: 7 aprile 2026


## Note sulla versione di marzo 2026 {#march-26-rn}

Le sezioni [Nuove funzionalità](#march-26-features) e [Miglioramenti](#march-26-improv) riguardano le funzionalità già disponibili. <!--The [Coming soon](#coming-soon) section lists features and improvements scheduled for release later in March.-->

<!--
**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.
-->

**Data di rilascio**: 24-25 marzo 2026

### Nuove funzionalità {#march-26-features}

<table>
<thead>
<tr>
<th><strong>Crittografia dei parametri URL</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>I parametri URL nei collegamenti delle pagine di destinazione e di tracciamento aggiunti ai messaggi e-mail ora possono essere crittografati, fornendo un ulteriore livello di sicurezza per i dati dei parametri sensibili.</p>
<ul>
<li>Registra e gestisci le chiavi di crittografia nel registro dedicato <strong>Amministrazione</strong>.</li>
<li>Utilizza la nuova funzione di assistenza "Encrypt" nelle espressioni per crittografare dati sensibili negli URL per i parametri di query che desideri proteggere al momento del rendering.</li>
</ul>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<p><img src="assets/do-not-localize/encrypt-helper.gif"></p>
<p>Per ulteriori informazioni, consulta la <a href="../personalization/url-parameter-encryption.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 31 marzo 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Conversione di immagini in modelli di contenuto e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora è possibile convertire le immagini in modelli di contenuto e-mail direttamente in Journey Optimizer. Utilizza l’analisi basata sull’intelligenza artificiale per generare automaticamente modelli HTML strutturati dai riferimenti visivi, riducendo in modo significativo i tempi di progettazione delle e-mail.</p>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p><img src="assets/do-not-localize/image-converter.gif"></p>
<p>Per ulteriori informazioni, consulta la <a href="../content-management/image-to-html.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 31 marzo 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Moduli personalizzati della pagina di destinazione</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con [!DNL Journey Optimizer] puoi acquisire gli attributi del profilo tramite le pagine di destinazione.</p>
<p>Crea, progetta e gestisci moduli personalizzati adatti alle tue esigenze sulla base di un set di dati specifico. Puoi quindi sfruttare questi moduli nelle pagine di destinazione per aggiungere gli attributi di profilo desiderati nel set di dati definito per ciascun modulo.</p>
<p>Precedentemente rilasciata in Disponibilità limitata per i clienti negli Stati Uniti e in Australia, questa funzionalità è ora disponibile per tutti gli ambienti (Disponibilità generale).</p>
<p><img src="assets/do-not-localize/forms.gif"/></p>
<p>Per ulteriori informazioni, consulta la <a href="../landing-pages/lp-forms.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 26 marzo 2026.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Attività di test nelle campagne orchestrate</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Una nuova attività <strong>Test</strong> è ora disponibile nelle campagne orchestrate. Questa attività indirizza l’esecuzione del flusso di lavoro a rami diversi in base a condizioni definite, consentendo di convalidare la logica e le configurazioni della campagna prima di attivare le consegne live.</p>
<p><img src="../orchestrated/assets/test-1.png"></p>
<p>Per ulteriori informazioni, consulta la <a href="../orchestrated/activities/test.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Supporto della ricerca di set di dati in percorsi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Una nuova attività <strong>Ricerca set di dati</strong> in percorsi consente di recuperare dinamicamente i dati dai set di dati dei record di Adobe Experience Platform in fase di esecuzione, consentendo l'accesso a informazioni che non fanno parte del payload del profilo o dell'evento, in modo che le interazioni dei clienti rimangano pertinenti e tempestive.</p>
<p>Precedentemente rilasciata in Disponibilità limitata a un set limitato di organizzazioni, l’attività di ricerca del set di dati in percorsi è ora disponibile per tutti i clienti autorizzati a [ricerca set di dati](../data/lookup-aep-data.md), pur rimanendo in Disponibilità limitata.</p>
<p><img src="../building-journeys/assets/aep-data-activity.png"></p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/dataset-lookup.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>L’attività Azione sostituisce le attività di percorso specifiche per il canale</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In seguito alla disponibilità generale dell'attività <strong>Azione</strong> nel febbraio 2026, le attività legacy del canale nativo (e-mail, push, SMS, in-app, web, esperienza basata su codice e scheda contenuto) nell'area di lavoro del percorso sono ora obsolete.</p>
<p>Ora devi utilizzare la singola attività Azione per configurare tutte le azioni del canale, sostituendo la necessità di nodi specifici del canale separati.</p>
<p>I percorsi esistenti che utilizzano attività di canale legacy continuano a funzionare senza la necessità di apportare modifiche o migrazioni.</p>
<p><img src="assets/do-not-localize/action-activity.gif"></p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/journey-action.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Editor HTML avanzato per modelli e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La modalità HTML avanzata per i modelli di contenuto e-mail consente di modificare l’origine HTML del contenuto nel Designer e-mail, aggiungere espressioni avanzate (come condizioni) nell’origine e passare dalla vista HTML a quella desktop senza perdere le modifiche.</p>
<p>Questa funzionalità è disponibile solo nei modelli di contenuto per il canale e-mail. Attualmente è in disponibilità limitata; per ottenere l’accesso, contatta il rappresentante Adobe.</p>
<p><img src="assets/do-not-localize/expert-mode.gif"/></p>
<p>Per ulteriori informazioni, consulta la <a href="../email/email-expert-mode.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 10 marzo 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integrazione di modelli Firefly personalizzati e modelli di generazione di immagini di terze parti</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Integrazione perfetta di modelli Firefly standard e personalizzati, insieme a modelli di immagini di terze parti approvati, per fornire maggiore flessibilità, controllo e allineamento del brand durante la generazione delle immagini.</p>
<p>Scegli il modello giusto per le tue esigenze:</p>
<ul><li> <strong>Adobe model</strong> (con tecnologia Firefly Image Model 4) per la generazione immediata di immagini senza installazione aggiuntiva</li><li> <strong>Modello partner</strong> (con tecnologia Gemini 2.5 Flash) per funzionalità specializzate</li><li><strong>Modelli personalizzati</strong> (modelli specifici del brand addestrati sulle tue risorse) per la generazione di prodotti sul brand che sono allineati con precisione alla tua identità del brand, allo stile e alle linee guida visive.</li></ul>
<p>Per ulteriori informazioni, consulta la <a href="../content-management/generative-models.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 2 marzo 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Attività live per iOS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Porta le esperienze in tempo reale direttamente su Blocca Screens e Dynamic Island dei tuoi clienti con <strong>iOS Live Activity</strong> in Adobe Journey Optimizer. Consegna aggiornamenti live, dal tracciamento degli ordini e dello stato dei voli, ai conteggi degli eventi, ai punteggi live e all’avanzamento della consegna, senza richiedere agli utenti di aprire l’app. Tieni il pubblico informato e coinvolto al momento giusto, proprio dove si trova.</p>
<p>Precedentemente rilasciata in versione beta, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p>Per ulteriori informazioni, consulta la <a href="../mobile-live/get-started-mobile-live.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 3 marzo 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent: creazione di contenuti del canale</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con tecnologia <strong>Adobe Experience Platform Agent Orchestrator</strong>, <strong>Journey Agent</strong> è disponibile in Journey Optimizer e consente di analizzare i percorsi tramite un'interfaccia in linguaggio naturale. È inoltre possibile generare e gestire contenuti specifici per il canale direttamente in Journey Agent, creando contenuti per canali quali e-mail e push, applicando e visualizzando in anteprima modelli, perfezionando tono e stile tramite prompt e aprendo contenuti in <strong>Content Designer</strong> per la modifica nel contesto.</p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<p>Per ulteriori informazioni, consulta la <a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent.html" target="_blank">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 4 marzo 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Monitoraggio del modello di IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ora consente di monitorare lo stato, lo stato di formazione e le prestazioni dei modelli di IA per il decisioning. Questo consente di verificare il successo della formazione, risolvere eventuali problemi e comprendere l’impatto sui risultati, al fine di selezionare le offerte migliori per ogni cliente che utilizza l’intelligenza artificiale. Questa funzionalità è disponibile solo per <strong>Decisioning</strong> (non per i modelli di gestione delle decisioni legacy).</p>
<p>Questa funzionalità è attualmente disponibile solo per i modelli di <strong>ottimizzazione personalizzata</strong> (non ottimizzazione automatica).</p>
<p><img src="assets/do-not-localize/ai-model-observability.gif"/></p>
<p>Per ulteriori informazioni, consulta la <a href="../experience-decisioning/ranking/ai-model-observability.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 9 marzo 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Attivare campagne orchestrate utilizzando un segnale</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile attivare le campagne orchestrate tramite un <strong>segnale API</strong>. Per configurare questa impostazione, configura la campagna di destinazione come <strong>Attivata da un segnale</strong>, pubblicala e attivala tramite una chiamata API. Tutti i parametri inclusi nella chiamata API sono disponibili come variabili all’interno della campagna in esecuzione. Tieni presente che le campagne orchestrate attivate dal segnale rimangono <strong>campagne batch</strong> e sono diverse dalle campagne attivate dall'API.</p>
<p><img src="assets/do-not-localize/oc-triggered.gif"></p>
<p>Per ulteriori informazioni, consulta la <a href="../orchestrated/trigger-orchestrated-campaign.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Categoria transazionale nelle campagne orchestrate</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Nelle campagne orchestrate, ora puoi impostare un'attività del canale sulla categoria <strong>Transazionale</strong>. Questo applica configurazioni del canale transazionale a tale attività ed è utile quando le regole aziendali non devono essere applicate o quando non è richiesto il consenso dei clienti.</p>
<p><img src="assets/do-not-localize/oc-transactional.gif"></p>
<p>Per ulteriori informazioni, consulta la <a href="../orchestrated/activities/channels.md#add">documentazione dettagliata</a>.</p>
<p>Nei prossimi giorni questa funzionalità verrà gradualmente implementata in tutte le aree geografiche.</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti {#march-26-improv}

Di seguito sono elencati i miglioramenti inclusi in questa versione.

#### Personalizzazione

* **Personalizzazione URL completo/di base** - Puoi personalizzare gli URL di destinazione utilizzando gli attributi del profilo (ad esempio, per il dominio o il percorso). Per abilitare questa funzionalità, fornisci ad Adobe l’elenco dei domini accettati. [Ulteriori informazioni](../personalization/personalization-build-expressions.md#where)

  Precedentemente rilasciata in Disponibilità limitata per l’utilizzo in percorsi, questa funzionalità è ora disponibile per tutti gli ambienti (Disponibilità generale).

  Data di disponibilità: 1 aprile 2026

#### Reporting

* **Ottimizzazione dell&#39;ora di invio: la posizione dei controlli aggiornata e il nuovo rapporto di incremento** - I controlli di ottimizzazione dell&#39;ora di invio (STO) sono stati spostati nel menu di configurazione Azione. Inoltre, è ora disponibile un nuovo rapporto lift nei rapporti Percorsi per misurare l’impatto dell’STO sulle metriche delle prestazioni della campagna. [Ulteriori informazioni](../reports/channel-report-cja.md#optimization-models)

  Data di disponibilità: 27 marzo 2026

<!--
* **Exclude bot clicks for email and SMS reporting** - Email and SMS reporting now automatically filters out bot clicks from click metrics, providing more accurate engagement data and preventing automated traffic from inflating your performance figures.

#### Email Designer

* **Email Designer displayed in Unified Shell** - The Email Designer is now displayed within the Unified Shell experience, providing a consistent navigation and header experience that aligns with other Adobe applications.

* **Text mode support in fragments** - To support text-based email workflows, you can now create and manage text versions of your visual fragments for optimal use in the plain text version of emails that include that fragment.

  **Caution:** When using a fragment that was created before the current release, the fragment text version may be incorrectly rendered—both in the Email Designer and in the final email delivered to your recipients. For best results with older fragments, edit, save and republish each fragment.
-->

#### Configurazione

<!--* **Folders for journeys and campaigns** - You can now organize your journeys and campaigns into folders, enabling structured navigation and easier management for teams working with large volumes of content. This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.-->

* **Rinnovo dei certificati di dominio AJO non riuscito** - È ora possibile abbonarsi per ricevere gli avvisi di sistema, tramite e-mail o nel centro notifiche Journey Optimizer, quando un certificato di dominio utilizzato per il recapito messaggi e-mail sta per scadere o è già scaduto. [Ulteriori informazioni](../reports/alerts.md#alert-certificates-renewal-unsuccessful)

  Data di disponibilità: 26 marzo 2026

* **AJO Secondary Recipient Feedback Event Rename** - Il set di dati `AJO Email BCC Feedback Event` è stato rinominato in `AJO Secondary Recipient Feedback Event`. L’impatto varia a seconda della situazione:

   * **Utenti esistenti**: viene aggiornato solo il nome visualizzato. Il nome della tabella sottostante rimane invariato.
   * **Nuovi utenti e sandbox**: sia il nome visualizzato che il nome della tabella riflettono il nuovo nome.
   * **Utenti esistenti con nuove sandbox**: il nome visualizzato e il nome della tabella vengono aggiornati al nuovo nome.

  >[!NOTE]
  >
  >I nuovi set di dati mostrano immediatamente il nuovo nome. Per i nomi dei set di dati precedenti, la retrocompilazione e la riconciliazione procedono gradualmente e il completamento potrebbe richiedere diverse settimane.

  Data di disponibilità: 2 marzo 2026


#### Percorsi

* **Azione Aggiorna profilo: supporto per più attributi di profilo** - L&#39;attività dell&#39;azione **Aggiorna profilo** ora supporta l&#39;aggiornamento di un massimo di cinque attributi di profilo in un singolo nodo. In precedenza, ogni azione poteva aggiornare un solo attributo alla volta, richiedendo a più nodi di aggiornare diversi attributi. Utilizza il nuovo pulsante **Aggiorna un altro campo** per aggiungere altre coppie campo/valore, riducendo la complessità dell&#39;area di lavoro e migliorando le prestazioni. [Ulteriori informazioni](../building-journeys/update-profiles.md)

* **Invio ondata di messaggi in uscita in percorsi** - È ora possibile pianificare i messaggi provenienti da percorsi Journey Optimizer da recapitare in batch controllati nel tempo. [Ulteriori informazioni](../building-journeys/send-using-waves.md)

  Precedentemente rilasciata in Disponibilità limitata per l’utilizzo in percorsi, questa funzionalità è ora disponibile per tutti gli ambienti (Disponibilità generale).

  Data di disponibilità: 16 marzo 2026

* **Sospendi e riprendi dettagli nei dettagli tecnici del percorso** - I **dettagli tecnici** del percorso ora includono ulteriori informazioni sulla pausa e sulla ripresa: la data e l&#39;ora dell&#39;ultima pausa e della ripresa, il nome visualizzato e l&#39;identificatore interno dell&#39;utente che ha eseguito ogni azione e un set completo di impostazioni di percorso in pausa come il comportamento della pausa, la durata massima della pausa e lo stato di ripresa automatica. [Ulteriori informazioni](../building-journeys/journey-properties.md)

  Data di disponibilità: 2 marzo 2026

#### Funzione Decisioni

* **Migrazione delle decisioni: attributi di offerta e di contesto**. La mappatura dell&#39;entità API di migrazione elenca ora **attributi di offerta** (`migratedofferattributes` nello schema Elemento di offerta personalizzato) e **attributi di contesto** (`migratedcontextattributes` nello schema Set di dati di migrazione). [Ulteriori informazioni](../experience-decisioning/decisioning-migration-api.md#entity-mapping)

  Data di disponibilità: 31 marzo 2026

<!--
## Coming soon {#coming-soon}

The features and improvements below are planned for release later in March/early April. Release dates and scope are **subject to change without prior notice**.


WAITING RELEASE DATE CONFIRMATION * **Target dimension simplification in Orchestrated Campaigns** - The active targeting dimension is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.


WAITING RELEASE DATE CONFIRMATION
* **Target dimension simplification in Orchestrated Campaigns** - The active targeting dimension is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.
-->
