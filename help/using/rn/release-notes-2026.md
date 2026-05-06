---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione 2026
description: Note sulla versione di Journey Optimizer 2026
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 65ca94cf-8e17-4a25-90f3-238083f81477
source-git-commit: 70a9be0c253bbed319510058f7f249f5919bf7b8
workflow-type: tm+mt
source-wordcount: '4254'
ht-degree: 46%

---

# Note sulla versione 2026 {#release-notes-2026}

In questa pagina sono elencate tutte le funzionalità e i miglioramenti di [!DNL Journey Optimizer] rilasciati nel 2026.

## Note sulla versione di marzo 2026 {#march-26-rn}

Le sezioni [Nuove funzionalità](#march-26-features) e [Miglioramenti](#march-26-improv) riguardano le funzionalità già disponibili. <!--The [Coming soon](#coming-soon) section lists features and improvements scheduled for release later in March.-->

<!--
**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform pre-release notes](https://experienceleague.adobe.com/it/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.
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
<p>Abilita l’integrazione diretta con modelli Firefly standard e personalizzati, nonché con modelli di immagini di terze parti approvati, per usufruire di maggiore flessibilità, controllo e allineamento al brand durante la generazione delle immagini.</p>
<p>Scegli il modello giusto per le tue esigenze:</p>
<ul><li> <strong>Modello Adobe</strong> (basato su Firefly Image Model 4) per la generazione immediata di immagini senza configurazione aggiuntiva</li><li> <strong>Modello partner</strong> (basato su Gemini 2.5 Flash) per funzionalità specializzate</li><li><strong>Modelli personalizzati</strong> (modelli specifici del brand basati sulle tue risorse) per la generazione di prodotti in linea con il brand che sono allineati con precisione all’identità del brand, allo stile e alle linee guida visive.</li></ul>
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
<p>Per ulteriori informazioni, consulta la <a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent.html?lang=it" target="_blank">documentazione dettagliata</a>.</p>
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


## Note sulla versione di febbraio 2026 {#feb-26-01-rn}

### Nuove funzionalità {#feb-26-01-features}


<table>
<thead>
<tr>
<th><strong>arbitrato di percorso</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile utilizzare <strong>formule di classificazione</strong> per aumentare automaticamente i punteggi di priorità del percorso in base agli attributi del profilo cliente e ai fattori contestuali, in modo che i clienti immettano i percorsi più rilevanti.</p>
<p><img src="assets/do-not-localize/journey-arbitration-formulas.gif"/></p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<p>Per ulteriori informazioni, consulta la <a href="../conflict-prioritization/journey-ranking-formulas.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 24 febbraio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Attività di azione nei percorsi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer supporta una nuova <strong>attività Azione</strong> generica che consente di configurare sia le azioni singole che i gruppi di azioni in entrata con più azioni, semplificando la configurazione delle azioni nell'area di lavoro del percorso. In particolare, questa nuova funzione consente:</p>
<ul>
<li>una configurazione semplificata dell’azione nativa nell’area di lavoro del percorso;</li>
<li>la capacità di creare gruppi di azioni in entrata con più azioni;</li>
<li>la possibilità di aggiungere l’ottimizzazione a qualsiasi azione del canale incorporata;</li>
<li>Possibilità di aggiungere sia opzioni di sperimentazione che opzioni multilingue a qualsiasi azione.</li>
</ul>
<p><img src="assets/do-not-localize/action-activity.gif"/></p>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/journey-action.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 20 febbraio 2026</p>
<p><strong>Nota:</strong> tutti i canali nativi sono ora accessibili tramite l'attività del percorso di azioni. Le attività dei canali nativi legacy diventeranno obsolete con la versione di marzo. I percorsi esistenti che includono azioni legacy continueranno a funzionare così come sono, non è richiesta alcuna migrazione.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Invio ondata di messaggi in uscita</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi pianificare i messaggi provenienti da campagne o percorsi Journey Optimizer da consegnare in batch controllati nel tempo.</p>
<p>L’invio ondata offre i seguenti vantaggi:</p>
<ul>
<li>Migliore recapito messaggi: Spread invia nel tempo per contribuire a mantenere una solida reputazione del mittente e ridurre il rischio di essere segnalati come spam.</li>
<li>Controllo del carico: evita di sopraffare i sistemi a valle (ad esempio call center e pagine di destinazione) limitando il numero di messaggi che vengono inviati contemporaneamente.</li>
<li>Casi d’uso complessi e sensibili al tempo: adatti a tipi di pubblico di grandi dimensioni o quando è necessario controllare la tempistica (ad esempio capacità del call center, offerte incrementali o con limiti di tempo).</li>
</ul>
<p><img src="assets/do-not-localize/waves.gif"/></p>
<p>In <strong>campagne</strong>, questa funzionalità è disponibile per tutti gli ambienti (disponibilità generale). Per ulteriori informazioni, consulta la <a href="../campaigns/send-using-waves.md">documentazione dettagliata</a>.</p>

<p>In <strong>percorsi</strong>, questa funzionalità è disponibile solo per un set di organizzazioni (disponibilità limitata). Per ottenere l'accesso, contatta il tuo rappresentante Adobe. Per ulteriori informazioni, consulta la <a href="../building-journeys/send-using-waves.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 19 febbraio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Migrare i sottodomini alla delega personalizzata</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi migrare i sottodomini utilizzando la modalità di delega CNAME alla delega personalizzata direttamente dall’interfaccia, in modo da soddisfare criteri di sicurezza più severi in linea con le linee guida della tua azienda senza ricreare le configurazioni del canale.</p>
<p><img src="assets/do-not-localize/subdomain-migration.gif"/></p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<p>Per ulteriori informazioni, consulta la <a href="../configuration/custom-subdomain-migration.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 19 febbraio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canale per notifiche push web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer ora supporta <strong>notifiche push web</strong>, espandendo il canale push oltre i dispositivi mobili. Puoi inviare facilmente le notifiche ai <strong>browser di dispositivi mobili e desktop</strong>, per raggiungere la clientela direttamente sui dispositivi senza richiedere un’app. Questo miglioramento consente di coinvolgere gli utenti con messaggi tempestivi e personalizzati in tempo reale, sfruttando gli stessi flussi di lavoro di authoring e le stesse funzionalità di targeting già disponibili per le notifiche push per dispositivi mobili.</p>
<p><img src="assets/do-not-localize/web-push.gif"/></p>
<p>Precedentemente rilasciata in Beta, questa funzionalità sarà disponibile per tutti gli ambienti (disponibilità generale).</p>
<p>Per ulteriori informazioni, consulta la <a href="../push/push-configuration-web.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 13 febbraio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Attività di decisione sui contenuti</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Una nuova <strong>attività Content Decision</strong> è ora disponibile nell'area di lavoro del percorso per l'integrazione di offerte personalizzate direttamente nei percorsi di clienti. Questa attività ti consente di fornire contenuti basati su decisioni e di fare riferimento a tali offerte in tutto il percorso, in condizioni per la creazione di diramazioni basate sull’idoneità, in azioni personalizzate per il passaggio dei dati delle offerte a sistemi esterni e in altre attività per la creazione di esperienze cliente completamente personalizzate.</p>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p><img src="assets/do-not-localize/content-decision.gif"/></p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/content-decision.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 10 febbraio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>API per strumenti di migrazione self-service</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le API per gli strumenti di migrazione sono ora disponibili per migrare a livello di programmazione le entità <strong>Gestione decisioni</strong> in <strong>Decisioning</strong>, con:</p>
<ul>
<li>Ambiti di migrazione flessibili (a livello di sandbox, offerta o decisione)</li>
<li>Automazione di analisi e convalida delle dipendenze</li>
<li>Supporto del rollback per le migrazioni completate</li>
<li>Rapporti dettagliati sulla migrazione con mappature degli oggetti</li>
</ul>
<p>Per ulteriori informazioni, consulta la <a href="../experience-decisioning/decisioning-migration-api.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 3 febbraio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Monitoraggio delle azioni personalizzate</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Approfondisci insight sullo stato e sulle prestazioni degli endpoint di azione personalizzati con un nuovo dashboard di monitoraggio e dati arricchiti sugli eventi dei passaggi del percorso. Tieni traccia correttamente di chiamate, errori, velocità effettiva, tempi di risposta e tempi di attesa delle code per comprendere rapidamente quando, dove e perché si verificano anomalie.</p>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p>Per ulteriori informazioni, consulta la <a href="../action/reporting.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 3 febbraio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Supporto per le decisioni nel canale SMS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi personalizzare e ottimizzare il contenuto dei messaggi SMS con Decisioning. Utilizzando punteggi di priorità, formule o modelli di IA, puoi così presentare a ogni cliente i contenuti più adatti.</p>
<p>Per ulteriori informazioni, consulta la <a href="../experience-decisioning/create-decision.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 2 febbraio 2026</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti {#feb-26-01-improv}

Di seguito sono elencati i miglioramenti inclusi in questa versione.

#### Configurazione

* **Utilizzo degli eventi di esperienza nelle espressioni di percorso** - A partire dal 1° aprile 2026, l&#39;utilizzo degli attributi degli eventi di esperienza nelle espressioni di percorso non sarà più supportato per le organizzazioni che non hanno utilizzato questa funzionalità negli ultimi 90 giorni. Questa funzionalità non è più disponibile per le nuove organizzazioni di clienti dall’8 luglio 2025. Per alternative, consulta [Ricerca eventi esperienza in percorsi](../building-journeys/exp-event-lookup.md).

#### Gestione dei contenuti

<!--
* **Update brands with new color tab** - Brand guidelines help ensure your brand is presented consistently across all touchpoints. The new <strong>Colors</strong> section defines the standards for your brand's color system, outlining how colors are selected, organized, and applied across experiences. It ensures consistent use of primary, secondary, accent, and neutral colors to support a cohesive, accessible, and recognizable brand identity. [Read more](../content-management/brands.md)
-->

* **Utilizza i temi per convertire le immagini in modelli e-mail**. Quando converti un&#39;immagine in un modello e-mail in Journey Optimizer, ora puoi utilizzare un tema come input in modo che il HTML generato segua i parametri del tuo marchio. Lo stile, ad esempio il colore di sfondo, il colore dei pulsanti, i tipi di carattere, l&#39;interlinea, i margini e la spaziatura interna, viene applicato automaticamente, riducendo il lavoro di progettazione manuale e distribuendo un modello pronto per l&#39;uso con modifiche minime. [Ulteriori informazioni](../content-management/image-to-html.md)

  Data di disponibilità: 17 febbraio 2026.

<!--* **Text mode for fragments** - You can now create and manage text versions of your fragments, supporting workflows that rely on plain text content and providing the same flexibility as in email content. [Read more](../content-management/create-fragments.md)-->

#### E-mail designer

* **Rientro testo** - È ora possibile applicare un rientro a sinistra personalizzabile alla prima riga di paragrafi nei componenti di testo direttamente dal pannello delle proprietà. <!--The new **Indentation** control lets you define indentation in pixels or percentage via a numeric input or slider, with live preview on the canvas. -->Ciò migliora la leggibilità dei contenuti lunghi, ad esempio editoriali e articoli. [Ulteriori informazioni](../email/get-started-email-style.md)

  Data di disponibilità: 18 febbraio 2026.

#### Funzione Decisioni

* **Supporto in entrata di Edge per l&#39;utilizzo dei dati di Adobe Experience Platform in Decisioning**. L&#39;utilizzo dei dati di Adobe Experience Platform in Decisioning ora supporta casi d&#39;uso in entrata Edge, oltre alle azioni e-mail e personalizzate nei percorsi. [Ulteriori informazioni](../experience-decisioning/aep-data-exd.md)

  Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.

* **Anteprima Decisioning nel canale di esperienza basato su codice** - È ora possibile visualizzare in anteprima gli elementi decisionali durante la configurazione di Decisioning con il canale di esperienza basato su codice. L’anteprima è disponibile direttamente nell’interfaccia di authoring prima della pubblicazione. [Ulteriori informazioni](../code-based/test-code-based.md#preview-code-based)

  Data di disponibilità: 18 febbraio 2026

<!--
THIS WAS FINALLY NOT RELEASED IN FEBRUARY

* **Attach fragments to decision items** - Journey Optimizer now provides the ability to attach fragments to decision items which can be leveraged in code-based experience campaigns through decision policies. [Read more](../experience-decisioning/fragments-decision-policies.md)

  Previously released in Limited Availability, this capability is now available to all environments (General Availability).

  Availability date: February 12, 2026.
-->

#### Personalizzazione

* **Helper metadati esecuzione** - La funzione helper `executionMetadata` è ora disponibile per tutti i clienti Journey Optimizer. Utilizzala per aggiungere dinamicamente informazioni contestuali a qualsiasi azione nativa e acquisirle in un set di dati per l’esportazione in sistemi esterni. [Ulteriori informazioni](../personalization/functions/helpers.md#execution-metadata)

  Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).

  Data di disponibilità: 20 febbraio 2026.

#### SMS

* **Webhook SMS** - I webhook sono ora supportati in tutti i provider SMS. Puoi configurare ogni webhook in base allo scopo previsto: i webhook in entrata per acquisire i messaggi in arrivo e i webhook di feedback per ricevere le conferme di consegna, gli aggiornamenti di stato e altri eventi relativi ai messaggi. [Ulteriori informazioni](../sms/sms-webhook.md)

  Data di disponibilità: 2 febbraio 2026.



## Note sulla versione di gennaio 2026 {#jan-26-rn}

<!--**Release date**: January 27-28, 2026-->

### Nuove funzionalità {#jan-26-01-features}


<table>
<thead>
<tr>
<th><strong>Supporto per le decisioni nel canale push</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi personalizzare e ottimizzare il contenuto delle <strong>notifiche push</strong> con <strong>decisioni</strong>. Utilizzando punteggi di priorità, formule o modelli di IA, puoi così presentare a ogni cliente i contenuti più adatti.</p>
<p>Experience Decisioning con notifiche push richiede una versione specifica del SDK mobile. Prima di implementare questa funzione, controlla le <a href="https://developer.adobe.com/client-sdks/home/release-notes" target="_blank">note sulla versione</a> per identificare la versione richiesta e assicurarti di aver effettuato l'aggiornamento di conseguenza. Puoi anche visualizzare tutte le versioni di SDK disponibili per la tua piattaforma in <a href="https://developer.adobe.com/client-sdks/home/current-sdk-versions" target="_blank">questa sezione</a>.</p>
<p>Per ulteriori informazioni, consulta la <a href="../experience-decisioning/create-decision.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 30 gennaio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canale direct mail nei percorsi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Precedentemente limitato alle campagne, il canale <strong>direct mail</strong> è ora disponibile nell’area di lavoro dei percorsi e consente di incorporare direct mail nei percorsi. Direct mail può ora essere utilizzato sia in <strong>batch che in scenari di percorso 1:1</strong>, con il supporto per la configurazione dell’estrazione dei file e le impostazioni di frequenza temporale.</p>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p><img src="assets/do-not-localize/dm-journey.gif"/></p>
<p>Per ulteriori informazioni, consulta la <a href="../direct-mail/get-started-direct-mail.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: venerdì 29 gennaio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Ore di silenzio (esclusioni basate sul tempo)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le <strong>ore di silenzio</strong> consentono di definire esclusioni basate sul tempo per i canali E-mail, SMS, Push e WhatsApp. Garantiscono che non vengano inviati messaggi in specifici periodi di tempo, aiutandoti a rispettare le preferenze dei clienti e i requisiti di conformità. Puoi applicare ore di silenzio tramite <strong>set di regole</strong>, che possono essere assegnate a singole azioni in campagne o percorsi per un controllo preciso.</p>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzione è ora disponibile per tutti gli ambienti. Con questo rilascio in disponibilità generale, la funzione ora consente di mettere in coda un’azione di una campagna fino al termine delle ore di silenzio, nonché di visualizzare in anteprima la regola Ore di silenzio attivata.</p>
<p><img src="assets/do-not-localize/quiet-hour-ga.gif"/></p>
<p>Per ulteriori informazioni, consulta la <a href="../conflict-prioritization/quiet-hours.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: venerdì 29 gennaio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Esportazione dei messaggi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora disponibile una nuova funzionalità di <strong>esportazione dei messaggi</strong> per i canali e-mail e SMS. Questa funzione consente di esportare automaticamente il contenuto dei messaggi inviati in un set di dati Experience Platform dedicato, per le seguenti esigenze:</p>
<ul>
<li>Soddisfare i requisiti di conformità alle normative (ad esempio HIPAA)</li>
<li>Archiviare i messaggi per richieste legali e di assistenza clienti</li>
<li>Mantenere copie dei contenuti personalizzati inviati a singoli utenti</li>
</ul>
<p>I record vengono conservati nel set di dati di esportazione dei messaggi di AJO per 7 giorni di calendario dall’acquisizione. Durante questo periodo di conservazione, puoi esportarli nel tuo archivio tramite le destinazioni Experience Platform. La funzione è abilitata a livello di configurazione dei canali e ti permette di <strong>definire in modo granulare</strong> quali messaggi esportare.</p>
<p>Questa funzionalità è disponibile solo per i canali e-mail e SMS, per le organizzazioni che hanno acquistato il componente aggiuntivo per l’esportazione dei messaggi. Per ulteriori informazioni, contatta il tuo rappresentante Adobe.</p>
<p><img src="assets/do-not-localize/message-export.gif"/></p>
<p>Per ulteriori informazioni, consulta la <a href="../configuration/message-export.md#message-export">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 28 gennaio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canale direct mail nelle campagne orchestrate</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Il canale direct mail è ora disponibile nelle campagne orchestrate. L’<strong>attività Direct mail</strong> facilita l’invio con direct mail all’interno della campagna orchestrata, per messaggi singoli o ricorrenti. Consente di automatizzare il processo di generazione del <strong>file di estrazione</strong> richiesto dai provider di servizi di direct mail. Puoi combinare le attività del canale nell’area di lavoro della campagna orchestrata per creare campagne cross-channel in grado di attivare azioni basate sui dati e sul comportamento della clientela.</p>
<p><img src="assets/do-not-localize/dm-oc.gif"/></p>
<p>Per ulteriori informazioni, consulta la <a href="../orchestrated/activities/channels.md#channel">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 28 gennaio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Agente Journey - Crea un percorso</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’agente Journey ora offre funzionalità di creazione che consentono agli utenti di Journey Optimizer di creare e configurare percorsi di marketing tramite un’interfaccia basata su <strong>linguaggio naturale</strong>. Con queste nuove competenze, i professionisti possono creare rapidamente percorsi semplicemente descrivendone i requisiti tramite <strong>prompt conversazionali</strong>. Questa innovazione semplifica il processo di creazione del percorso e consente ai marketer di concentrarsi sulla strategia anziché sulla configurazione tecnica.</p>
<p>Per ulteriori informazioni, consulta la <a href="../start/ai-features.md#journey-agent">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 12 gennaio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>API di recupero di campagne con azioni</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora disponibile una nuova API di Journey Optimizer che consente di recuperare e ispezionare in modo programmatico i <strong>dati relativi alla campagna</strong>, ad esempio dettagli, versioni e configurazioni.</p>
<p>Per ulteriori informazioni, consulta la <a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve" target="_blank">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 24 novembre 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Temi di E-mail designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi applicare rapidamente <strong>temi preapprovati</strong> per garantire la <strong>coerenza del brand</strong> in tutte le e-mail, velocizzare il processo di creazione delle campagne e produrre e-mail di alta qualità in modo indipendente, riducendo al contempo la dipendenza dai team di progettazione grafica.</p>
<p><img src="assets/do-not-localize/themes.gif"/></p>
<p>Precedentemente rilasciata nella versione Beta, questa funzionalità è ora disponibile per un set di organizzazioni (disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<p>Per ulteriori informazioni, consulta la <a href="../email/apply-email-themes.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 5 novembre 2025</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti {#jan-26-01-improv}

#### IA

* **Controlli di qualità dei contenuti con l’Assistente IA**: oltre all’allineamento al brand, ora puoi valutare la <strong>qualità dei contenuti</strong> complessiva per individuare potenziali problemi di <strong>leggibilità</strong>, coesione ed efficacia, indipendentemente dalle linee guida del brand. Questi controlli automatizzati consentono di individuare messaggi poco chiari, toni incoerenti o lacune strutturali. [Ulteriori informazioni](../content-management/brands-score.md#validate-quality).

  [Guarda il video su questa funzione](https://video.tv.adobe.com/v/3470544/?learn=on).

#### Percorsi

* **Combinare azioni con messaggi native e di Adobe Campaign**: Journey Optimizer ora consente di combinare, nello stesso percorso, azioni con messaggii di <strong>Adobe Campaign v7/v8</strong> con le <strong>azioni di canale native</strong> . [Ulteriori informazioni](../building-journeys/using-adobe-campaign-v7-v8.md)

  Data di disponibilità: mercoledì 27 gennaio 2026.

* **Payload di risposta in caso di errore per azioni personalizzate**: ora puoi facoltativamente definire un <strong>payload di risposta in caso di errore</strong> per le azioni personalizzate. Se una chiamata non riesce, il payload di errore viene esposto nel contesto del percorso (sotto il nodo errorResponse dell’azione) ed è disponibile nel <strong>ramo timeout/errore</strong>, insieme a `jo_status_code`, per un migliore supporto della logica di fallback e del debug. [Ulteriori informazioni](../action/about-custom-action-configuration.md#define-the-message-parameters)

  Data di disponibilità: mercoledì 27 gennaio 2026.

* **Convalida della dimensione del payload Journey nei percorsi**: Journey Optimizer ora convalida la <strong>dimensione del payload</strong> per garantire prestazioni e stabilità del sistema ottimali. Durante la creazione o la pubblicazione di percorsi, vengono visualizzati messaggi chiari di <strong>avvertenze ed errori</strong> se la dimensione del payload si avvicina o supera i limiti consigliati, con istruzioni da mettere subito in pratica per ottimizzare la configurazione dei percorsi. Questa convalida proattiva consente di individuare per tempo potenziali problemi e di mantenere ottimali le prestazioni del percorso. [Ulteriori informazioni](../start/guardrails.md#journey-payload-size)

  Data di disponibilità: mercoledì 27 gennaio 2026.


* **Avvisi sui percorsi**: sono disponibili nuovi <strong>avvisi preconfigurati</strong> per i percorsi.
   * <strong>Tasso di profili rimossi superato</strong>: il rapporto tra i profili rimossi e i profili in ingresso negli ultimi 5 minuti ha superato la soglia consentita.
   * <strong>Tasso di errore nelle azioni personalizzate superato</strong>: il rapporto tra gli errori nelle azioni personalizzate e le chiamate HTTP riuscite negli ultimi 5 minuti ha superato la soglia consentita.
   * <strong>Tasso di profili con errori superato</strong>: il rapporto tra profili con errori e profili in ingresso negli ultimi 5 minuti ha superato la soglia la consentita.

  Per ulteriori informazioni, consulta la [documentazione dettagliata](../reports/alerts.md).

  Data di disponibilità: 14 ottobre 2025.

#### Campagne orchestrate

* **Ereditarietà delle etichette di utilizzo dati per i tipi di pubblico**: le etichette applicate in Adobe Experience Platform ora vengono riportate in automatico quando un <strong>pubblico</strong> viene salvato in campagne orchestrate, in modo da ridurre l’assegnazione manuale dei <strong>tag DULE</strong>. [Ulteriori informazioni](../orchestrated/activities/save-audience.md)

* **Filtri preimpostati con parametri**: puoi ora creare <strong>filtri preimpostati</strong> con <strong>parametri</strong> nelle campagne orchestrate per regole riutilizzabili e modificabili. [Ulteriori informazioni](../orchestrated/predefined-filters.md)

* **Selezionare gli attributi e copiare i valori di distribuzione**: ora puoi <strong>selezionare o copiare i valori</strong> direttamente dalla vista <strong>Distribuzione dei valori</strong> nelle campagne orchestrate. [Ulteriori informazioni](../orchestrated/build-query.md)

* **Conferma del messaggio prima dell’invio**: ora è abilitato per impostazione predefinita un <strong>passaggio di conferma</strong> prima dell’invio di campagne orchestrate, per ridurre il rischio di invio accidentale. [Ulteriori informazioni](../orchestrated/activities/channels.md#confirm-message-sending)

* **Filtri di retargeting preimpostati**: per agevolare il retargeting per diversi casi d’uso di campagne orchestrate, questa versione introduce nuovi <strong>filtri di feedback sulla campagna</strong>. Questi filtri consentono di rivolgersi direttamente a un pubblico in base al <strong>coinvolgimento nei messaggi</strong> (ad esempio: inviato, solo aperto, aperto o cliccato, oppure aperto e cliccato) e di selezionare la campagna specifica o in transizione di cui desideri eseguire il retargeting. [Ulteriori informazioni](../orchestrated/retarget.md)

* **Supporto per il controllo della frequenza**: le campagne orchestrate ora supportano il <strong>controllo della frequenza</strong> per regolare la cadenza delle consegne e rispettare eventuali <strong>vincoli di volumi</strong>. [Ulteriori informazioni](../orchestrated/activities/channels.md#rate-control)

* **Pulsante di riavvio**: le campagne orchestrate ora includono un <strong>pulsante di riavvio</strong> per <strong>riavviare rapidamente le esecuzioni</strong>, se necessario, prima di pubblicare la campagna. [Ulteriori informazioni](../orchestrated/start-monitor-campaigns.md)

* **Supporto per metadati generati dall’utente**: la <strong>funzione helper executionMetadata</strong>, ora disponibile nell’editor di personalizzazione per le campagne orchestrate, consente di allegare informazioni contestuali a qualsiasi azione nativa e di memorizzarle in un set di dati per l’esportazione in sistemi esterni. [Ulteriori informazioni](../personalization/functions/helpers.md#execution-metadata)

  Data di disponibilità: mercoledì 27 gennaio 2026.

* **Ripristina stato bozza delle campagne live** - Ora puoi ripristinare lo stato bozza delle campagne orchestrate live quando si verificano errori di esecuzione o quando devi modificare le campagne pianificate prima che inizino l&#39;esecuzione. Questa opzione è disponibile fino all’invio del primo messaggio. [Ulteriori informazioni](../orchestrated/start-monitor-campaigns.md#back-to-draft)

#### Campagne

* **Pianificare le campagne utilizzando il fuso orario del profilo**: nella pianificazione delle campagne, ora puoi specificare che la consegna dei messaggi avvenga secondo il <strong>fuso orario</strong> di ciascun profilo. [Ulteriori informazioni](../campaigns/campaign-schedule.md)

  **Nota**: questo miglioramento è disponibile solo per un set di organizzazioni (disponibilità limitata).

  Data di disponibilità: mercoledì 27 gennaio 2026.

#### Autorizzazioni

* **Impedire l’autoapprovazione per percorsi e campagne**: durante la creazione o l’impostazione dei <strong>criteri di approvazione</strong>, grazie a una nuova opzione puoi impedire a chi crea un percorso o una campagna di <strong>approvare i propri oggetti</strong>. [Ulteriori informazioni](../test-approve/approval-policies.md)

  Data di disponibilità: mercoledì 27 gennaio 2026.
