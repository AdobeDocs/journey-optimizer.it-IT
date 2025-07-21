---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
feature: Release Notes
topic: Content Management
description: Note sulla versione di Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 1bdba8c5c1a9238d351b159551f6d3924935b339
workflow-type: tm+mt
source-wordcount: '1307'
ht-degree: 95%

---

# Note sulla versione {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novità"
>abstract="**Adobe Journey Optimizer** offre continuamente nuove funzioni, miglioramenti a quelle esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese."

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese. [!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche sono disponibili nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.

## Ultimi aggiornamenti {#latest-updates}

### Inventari separati per le campagne

Le campagne di azione e le campagne attivate da API sono ora organizzate in inventari a schede diversi per facilitare la visualizzazione rapida di tutte le campagne di un particolare tipo.

### Modifica nelle condizioni di percorso {#ee-change@}

A partire dall’8 luglio, nelle nuove organizzazioni dei clienti, la creazione di espressioni utilizzando gli eventi di esperienza non è più supportata nell’editor di espressioni utilizzato nelle condizioni di percorso. Di conseguenza, gli eventi esperienza nell’[origine dati di Experience Platform](../datasource/adobe-experience-platform-data-source.md) non possono essere utilizzati per la creazione di espressioni. Si fa riferimento ad approcci alternativi e best practice per la creazione di espressioni/logiche con eventi esperienza [qui](../building-journeys/exp-event-lookup.md).

Il modo in cui viene effettuato l’accesso ai dati dell’evento di contesto del percorso nei percorsi unitari rimane invariato. Negli editor di espressioni e di personalizzazione, gli utenti possono continuare ad accedere ai dati trasmessi con l’evento del percorso iniziale.

Per ulteriori informazioni, consulta [queste Domande frequenti](../building-journeys/exp-event-lookup.md#faq-ee).


## Note sulla versione di giugno 2025 {#25-6-rn}

<!--
**Early release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published at the release date.-->

**Data di rilascio**: 18 giugno 2025

<!--See also [Adobe Experience Platform Pre Release Notes](https://experienceleague.adobe.com/it/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.-->

### Nuove funzionalità {#25-06-features}

Di seguito sono descritte le nuove funzionalità incluse in questa versione.

<table>
<thead>
<tr>
<th><strong>Set di dati di Adobe Experience Platform nella funzione Decisioni (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Precedentemente disponibili per la personalizzazione, i set di dati di Adobe Experience Platform ora possono essere sfruttati per la funzione decisioni. Questo consente di estendere la definizione degli attributi di decisione ai dati aggiuntivi nei set di dati per aggiornamenti in blocco che vengono modificati periodicamente senza dover aggiornare manualmente gli attributi uno alla volta. Ad esempio disponibilità, tempi di attesa e così via.</p>
<p>Questa funzionalità è disponibile per tutta la clientela come versione Beta pubblica. Se desideri accedervi, contatta il rappresentante del tuo account.</p>
<p>Per ulteriori informazioni, consulta la <a href="../experience-decisioning/aep-data-exd.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 20 giugno 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Messaggistica RCS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La messaggistica RCS (Rich Communication Services) è ora supportata in Journey Optimizer, consentendo le seguenti funzionalità di messaggistica avanzate, soggette al supporto di provider e operatore mobile.</p>
<ul>
<li>Supporto per mittente brandizzato e verificato: invia messaggi utilizzando profili aziendali verificati con elementi di branding (logo, nome del mittente, ecc.).</li>
<li>Informazioni approfondite sulla consegna dei messaggi: puoi ricevere rapporti di consegna dettagliati, inclusi gli aggiornamenti sullo stato del messaggio (ad esempio inviato, consegnato, letto).</li>
<li>Tracciamento dei collegamenti: incorpora e tieni traccia degli URL nei messaggi RCS per l’analisi del coinvolgimento.</li>
<li>Fallback su SMS: fallback automatico su SMS quando il dispositivo del profilo non supporta la RCS o è temporaneamente non raggiungibile tramite RCS.</li>
<li>Composizione di base dei messaggi: invia messaggi RCS basati su testo con elementi avanzati e file multimediali facoltativi, a seconda del supporto del provider.</li>
</ul>
<p>Per ulteriori informazioni, consulta la <a href="../sms/sms-configuration.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Campi modulo nei contenuti di esperienze basate su codice</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora è possibile definire campi modificabili specifici nei modelli di contenuto JSON o HTML, consentendo agli utenti non tecnici di modificare facilmente il contenuto di una visualizzazione modulo, nell’authoring del canale dell’esperienza basato su codice, senza il bisogno di manipolare alcun codice.<br />Inoltre, durante la definizione dei modelli di contenuto dell’esperienza basati su codice, è ora possibile inserire criteri di decisione nel modello, aumentando la riutilizzabilità e la facilità d’uso.</p>
<img src="assets/do-not-localize/form-fields.gif">
<p>Per ulteriori informazioni, consulta la <a href="../code-based/code-based-form-fields.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Custom delegation method for subdomains</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In addition to the full delegation and the CNAME method, a new subdomain configuration method is now available: the Custom delegation method, which enables you to fully own controlling and maintaining all aspects of DNS that are required for delivering, rendering and tracking messages.</p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>Attività di decisione sul contenuto nei percorsi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora è possibile includere e utilizzare offerte personalizzate all’interno dei percorsi e delle attività relative tramite un’attività dedicata di decisione sul contenuto nell’area di lavoro del percorso, comprese condizioni e azioni personalizzate.</p>
<img src="assets/do-not-localize/content-decision.gif">
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (disponibilità limitata) e verrà introdotta a livello globale in una versione futura.</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/content-decision.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Prova del percorso</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La prova del percorso è una modalità speciale di pubblicazione di un percorso in Adobe Journey Optimizer che consente ai professionisti del percorso di poterne effettuare un test, utilizzando dati di produzione reali e senza la necessità di contattare la clientela reale o aggiornare le informazioni di profilo. Questa funzione aiuta i professionisti del percorso ad acquisire maggiore sicurezza rispetto alla progettazione di un percorso e al targeting del pubblico, prima della pubblicazione effettiva.</p>
<img src="assets/do-not-localize/DryRun.gif">
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (disponibilità limitata) e verrà introdotta a livello globale in una versione futura.</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/journey-dry-run.md">documentazione dettagliata</a>.</p>

</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Mettere in pausa e riprendere i percorsi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile mettere in pausa e riprendere i percorsi. Questa funzionalità offre ai professionisti del percorso maggiore controllo e flessibilità, consentendo di sospendere temporaneamente i percorsi live senza compromettere l’esperienza cliente. Quando il percorso è in pausa, le comunicazioni non vengono inviate e i profili rimangono in stato di sospensione fino a quando il percorso non viene ripreso.</p>
<p>È possibile mettere in pausa e riprendere un singolo percorso, oppure eseguire operazioni di pausa e di ripresa in blocco su un gruppo di percorsi.</p>
<p>Inoltre, è possibile applicare filtri globali ai percorsi in pausa per escludere i profili in base ai rispettivi attributi.</p>
<img src="assets/do-not-localize/PauseResume.gif">
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (disponibilità limitata) e verrà introdotta a livello globale in una versione futura.</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/journey-pause.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Scalare il vincitore della sperimentazione</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Per “scalare il vincitore della sperimentazione” si intende presentare automaticamente o manualmente la variante vincente di un esperimento a tutto il pubblico. Questa funzione assicura che, una volta identificata la variante dalle prestazioni migliori, sia possibile massimizzarne la portata e l’efficacia senza una costante supervisione manuale.</p>
<p>Per ulteriori informazioni, consulta la <a href="../content-management/content-experiment.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 2 giugno 2025</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Conflitti e assegnazione delle priorità</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In Journey Optimizer, è essenziale gestire il volume e la tempistica delle campagne e dei percorsi per evitare di sopraffare la clientela con troppe interazioni. Journey Optimizer offre ora diversi strumenti per la gestione dei conflitti e l’assegnazione delle priorità. In precedenza disponibili solo per le organizzazioni con accesso alle funzionalità rilasciate con disponibilità limitata (LA), questi sono ora disponibili per tutti (GA, disponibilità generale).</p>
<p>Precedentemente rilasciata in versione a disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti. Con questa versione con disponibilità generale sono stati introdotti i seguenti miglioramenti:</p>
<ul>
<li>Supporto esteso: gli strumenti per la gestione dei conflitti ora supportano sia i percorsi unitari che i percorsi di qualificazione di un pubblico, oltre ai percorsi Leggi pubblico.</li>
<li>Risoluzione dei problemi migliorata: nel servizio query sono ora disponibili due nuovi campi evento del passaggio che consentono di analizzare il motivo per cui un profilo è stato rifiutato da un percorso o da una campagna.</li>
<li>Rapporti migliorati: i rapporti ora indicano la regola specifica che ha determinato l’esclusione di un profilo da un percorso o da una campagna, fornendo maggiore trasparenza e informazioni actionable.</li></ul>
<img src="assets/do-not-localize/gif-conflict.gif">
<p>Per ulteriori informazioni, consulta la <a href="../conflict-prioritization/gs-conflict-prioritization.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 3 giugno 2025</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti {#25-06-improv}

Di seguito sono elencati i miglioramenti inclusi in questa versione.

* **Set di regole del canale**

   * **Intervallo di durata personalizzato** per la limitazione: nella schermata di configurazione dei set di regole del canale è ora disponibile il nuovo campo **Ogni**, che consente di applicare regole di quota limite su più giorni, settimane o mesi, a seconda della durata specificata.

   * **Ripristina quota limite oraria**: ora è possibile applicare una limitazione su base oraria per i set di regole del canale. Questa funzionalità è disponibile solo per un set di organizzazioni (disponibilità limitata). Contatta l’assistenza clienti per l’attivazione.

   * **Durata giornaliera**: precedentemente disponibile in Disponibilità limitata, la quota limite “Giornaliera” nei set di regole del canale è ora disponibile per tutta la clientela.

  Per ulteriori informazioni, consulta la [documentazione dettagliata](../conflict-prioritization/channel-capping.md).

* **Esperienze basate su codice**

   * L’aggiunta di un criterio di decisione è ora disponibile nei modelli di contenuto di esperienza basata su codice, dove può essere utilizzato per sfruttare le offerte nei campi di modulo modificabili. [Ulteriori informazioni](../code-based/code-based-form-fields.md)

   * Dal percorso dell’esperienza basata su codice o dalla schermata di modifica della campagna, ora è possibile aggiungere direttamente un criterio di decisione senza aprire l’editor di personalizzazione. [Ulteriori informazioni](../code-based/create-code-based.md#edit-code)

* **Supporto CSS personalizzato in E-mail Designer**

  Journey Optimizer ora consente di aggiungere CSS personalizzato al contenuto delle e-mail direttamente all’interno di E-mail designer. [Ulteriori informazioni](../email/custom-css.md)

* **Nuova navigazione con schede per le campagne**

  Un nuovo pattern di navigazione consente un accesso più rapido all’authoring dei contenuti e supporta un’ulteriore espansione delle impostazioni nelle campagne. [Ulteriori informazioni](../campaigns/create-campaign.md)

* **Funzione Decisioni**

   * **Copia sandbox e funzione Decisioni** (data di disponibilità: 3 giugno 2025): è ora possibile copiare gli oggetti della funzione Decisioni tra sandbox, semplificando i flussi di lavoro di test e distribuzione. [Ulteriori informazioni](../configuration/copy-objects-to-sandbox.md#decisioning)

   * **Supporto dell’attributo degli elementi decisionali per le regole di decisione** (data di disponibilità: 4 giugno 2025): è ora possibile sfruttare gli attributi degli elementi decisionali per creare regole di decisione. [Ulteriori informazioni](../experience-decisioning/rules.md#create)

* **Aggiornamento API per l’esecuzione messaggi interattivi** - Data di disponibilità: 6 giugno 2025

  L’API per l’esecuzione dei messaggi interattivi ora consente di eliminare la pianificazione per l’esecuzione delle campagne successive. [Ulteriori informazioni](https://developer.adobe.com/journey-optimizer-apis/references/messaging/){target="_blank"}
