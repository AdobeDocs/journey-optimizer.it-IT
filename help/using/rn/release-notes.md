---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
feature: Release Notes
topic: Content Management
description: Note sulla versione di Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 018ff365780c5064afd94c8f842ca0498fe06065
workflow-type: tm+mt
source-wordcount: '1960'
ht-degree: 78%

---

# Note sulla versione {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novità"
>abstract="**Adobe Journey Optimizer** offre continuamente nuove funzioni, miglioramenti a quelle esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese."

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese. [!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.

## Versione di ottobre 2024 {#24-10-rn}

**Data di rilascio**: 29-30 ottobre 2024

### Nuove funzionalità {#24-10-features}

Questa versione include le nuove funzionalità descritte di seguito:

<table>
<thead>
<tr>
<th><strong>Blocco dei contenuti e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ora consente di bloccare il contenuto nei modelli e-mail, bloccando l’intero modello o strutture e componenti specifici. Questo consente di evitare modifiche o eliminazioni non intenzionali, garantendo un maggiore controllo sulla personalizzazione dei modelli e migliorando l’efficienza e l’affidabilità delle campagne e-mail.</p>
<p>Per ulteriori informazioni, consulta la <a href="../content-management/content-locking.md">documentazione dettagliata</a>.</p>
<img src="assets/do-not-localize/gif-content-locking.gif">
<p>Disponibile dal 24 ottobre 2024</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Esperienze basate su codice nei percorsi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con il canale di esperienza basato su codice, Adobe Journey Optimizer consente di eseguire personalizzazioni e test avanzati per qualsiasi proprietà in entrata, facilitando la consegna diretta di esperienze personalizzate in diversi punti di contatto come app web, app mobili, app desktop, console video, dispositivi connessi per TV, smart TV, chioschi, sportelli bancomat, dispositivi IoT e altro ancora. Il canale di esperienza basata su codice è ora disponibile nell’area di lavoro del percorso.</p>
<p>Per ulteriori informazioni, consulta la <a href="../code-based/create-code-based.md">documentazione dettagliata</a>.</p>
<img src="../assets/do-not-localize/code-based-journey.gif"/>
<p>Disponibile dal 1 ottobre 2024</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Esperienze web nei percorsi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con il canale web, Adobe Journey Optimizer ti consente di personalizzare l’esperienza web che fornisci alla clientela tramite percorsi web in entrata. Il canale web è ora disponibile nell’area di lavoro del percorso.</p>
<p>Per ulteriori informazioni, consulta la <a href="../web/create-web.md">documentazione dettagliata</a>.</p>
<img src="../assets/do-not-localize/web-journey.gif"/>
<p>Disponibile dal 1 ottobre 2024</p>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Gestione dei conflitti e delle priorità (disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In Journey Optimizer, gestire il volume e la tempistica delle campagne e dei percorsi è essenziale per evitare di sopraffare i clienti con troppe interazioni. Journey Optimizer offre ora diversi strumenti per la gestione dei conflitti e la definizione delle priorità. <p>Per ulteriori informazioni, consulta la <a href="../conflict-prioritization/gs-conflict-prioritization.md">documentazione dettagliata</a>.</p></p><p><ul><li><b>Quota limite percorsi</b>: ora è possibile creare set di regole da applicare ai tuoi percorsi, in modo da limitare il numero di percorsi per un profilo per giorno, settimana o mese, nonché controllare il numero di percorsi simultanei in esecuzione contemporaneamente.</li>
<li><b>Punteggio di priorità</b>: ora è possibile assegnare un punteggio di priorità, compreso tra 0 e 100, a una campagna o a un percorso. Un numero più alto indica una priorità più alta. Quando due campagne o azioni del percorso utilizzano la stessa configurazione dei canali, Journey Optimizer selezionerà quella con il punteggio di priorità più alto. Se le campagne hanno lo stesso punteggio, verrà scelta la campagna modificata meno di recente.</li>
<li><b>Visualizza conflitti potenziali</b>: un nuovo pulsante “Visualizza conflitti potenziali” nei percorsi e nelle campagne ora consente di identificare la sovrapposizione con altri percorsi o campagne, ad esempio la data di inizio, il pubblico di destinazione o la configurazione dei canali selezionata.</li>
<li><b>Journey Arbitration</b> (Arbitrato del percorso): questa nuova funzionalità consente di assegnare la priorità ai percorsi più importanti per i clienti. È possibile creare una regola per eliminare l’ingresso in un percorso con priorità inferiore quando un cliente si qualifica per un imminente percorso con priorità maggiore.</li>
<li><b>Quota limite per tipo di comunicazione: </b>con i set di regole è ora possibile impostare regole granulari per tipo di comunicazione (ad esempio Vendite, Promozionali) per evitare di sovraccaricare i clienti con messaggi simili. Puoi controllare la frequenza su più canali, escludendo automaticamente i profili sollecitati eccessivamente per garantire una migliore esperienza cliente.</li></ul>

<img src="assets/do-not-localize/gif-conflict.gif">

<p>Le funzionalità di gestione dei conflitti e delle priorità sono disponibili in Disponibilità limitata per un gruppo selezionato di clienti. Tenere presente che queste funzioni verranno gradualmente implementate per più utenti in futuro. Se lo desideri, puoi rivolgerti al team del tuo account per l’inserimento nella lista d’attesa per queste funzioni.</p>

</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Integrazione di Movable Ink con Adobe Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile integrare Movable Ink Da Vinci e Adobe Journey Optimizer. Con questa nuova integrazione è possibile: </p>
<p><ul><li>Sfruttare le potenti funzionalità del prodotto Da Vinci di Movable Ink per assemblare e personalizzare le varianti e-mail per le campagne batch</li>
<li>Accelerare i flussi di lavoro dei professionisti per i clienti di Journey Optimizer che utilizzano Da Vinci per l’authoring e Adobe Journey Optimizer per l’ottimizzazione e la distribuzione</li>
<li>Ottimizzare i modelli Da Vinci con dati Adobe.</li></ul></p>
<p>Per ulteriori informazioni, consultare la <a href="https://movableink.com/adobe-and-movable-ink">documentazione di Mobile Ink Da Vinci</a>.</p>
</tr>
</tbody>
</table>

Precedentemente disponibili per un set di organizzazioni (LA), le seguenti funzionalità sono ora disponibili per tutti gli utenti (GA):

<table>
<thead>
<tr>
<th><strong>Personalizzazione della configurazione e-mail (disponibilità generale) </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Per una maggiore flessibilità e un maggiore controllo sulle impostazioni e-mail, puoi definire sottodomini dinamici e parametri di intestazione personalizzati durante la creazione delle configurazioni del canale e-mail.
</p>
<p>Per ulteriori informazioni, consulta la <a href="../email/surface-personalization.md">documentazione dettagliata</a>.</p>
<img src="assets/do-not-localize/surface-perso.gif"/>
<p>Disponibile dal 23 ottobre 2024</p>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Approvazioni in percorsi e campagne (disponibilità generale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con i criteri di approvazione, ora puoi impostare un processo di approvazione in Journey Optimizer che consenta ai team di marketing di garantire che le campagne e i percorsi vengano rivisti e autorizzati dagli stakeholder prima della pubblicazione.</p>
<p>Per ulteriori informazioni, consulta la <a href="../test-approve/gs-approval.md">documentazione dettagliata</a>.</p>
<img src="assets/do-not-localize/approval.gif"/>
<p>Disponibile dal 22 ottobre 2024</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Sperimentazione dei contenuti nei percorsi (disponibilità generale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Già disponibile nelle campagne, Adobe Journey Optimizer ora supporta gli esperimenti nei percorsi. Gli esperimenti sono test randomizzati: nel contesto dei test online significa che esponi alcuni utenti selezionati in modo casuale a una determinata variante di un messaggio e un altro gruppo di utenti selezionato in modo casuale a un’altra variante o trattamento. Dopo l’esposizione, puoi quindi misurare le metriche del risultato che ti interessano, ad esempio apertura di e-mail, iscrizioni o acquisti.</p>
<p>Per ulteriori informazioni, consulta la <a href="../content-management/content-experiment.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>


<!--<table>
<thead>
<tr>
<th><strong>Decisioning (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Decisioning, previously available for a set of organizations (LA) and known as Experience Decisioning, is now available to all users (GA), including organizations that have purchased the Adobe Healthcare Shield or Privacy and Security Shield add-on offerings.</p><p>Decisioning simplifies personalization by offering a centralized catalog of marketing offers known as 'decision items' and a sophisticated decision engine. This engine leverages rules and ranking criteria to select and present the most relevant decision items to each individual. These decision items are seamlessly integrated into a wide range of inbound surfaces through the code-based experience channel.</p>
<p>For more information, refer to the <a href="../experience-decisioning/gs-experience-decisioning.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Messaggi multilingue nei percorsi e nelle campagne (disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora è possibile creare contenuti multilingue all’interno di un’unica campagna o di un unico percorso in modo semplice. Con questa funzione, è possibile cambiare lingua durante la modifica della campagna o del percorso, semplificando l’intero processo di modifica e migliorando la capacità di gestire in modo efficiente i contenuti multilingue.</p>
<p>Per ulteriori informazioni, consulta la <a href="../content-management/multilingual-gs.md">documentazione dettagliata</a>.</p>
<img src="assets/do-not-localize/multilingual.gif">
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Esperienza di reporting aggiornata (disponibilità generale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La funzione di reporting di Journey Optimizer, ora in disponibilità generale (GA), include una migliorata interoperabilità con le funzionalità di Customer Journey Analytics, per standardizzare il reporting su entrambe le piattaforme e migliorare la coerenza e l’affidabilità dei dati. Questa integrazione ottimizzata tra Journey Optimizer e Customer Journey Analytics consente una visione più chiara delle metriche delle prestazioni, in modo che gli utenti possano prendere decisioni più informate.</p>
<p>Con la funzione Disponibilità generale vengono introdotte quattro nuove funzioni: la possibilità di creare metriche semplici, creare e pubblicare tipi di pubblico, porre domande ad hoc tramite Insight Builder e pianificare l’invio automatico via e-mail dei rapporti ai destinatari chiave.</p>
<p>Per ulteriori informazioni, consulta la <a href="../reports/report-cja-manage.md">documentazione dettagliata</a>.</p>
<img src="assets/do-not-localize/ajo-cja.gif">
<p>Importante: l’esperienza di reporting corrente verrà ritirata a gennaio 2025. Dopo questa data, la nuova esperienza di reporting diventerà lo standard. Consigliamo di acquisire familiarità con le nuove funzioni e funzionalità per garantire una transizione semplice. <a href="../reports/report-gs-cja.md">Scopri come iniziare a utilizzare la nuova interfaccia di reporting di Journey Optimizer</a></p>
<p>Disponibile dal 16 ottobre 2024</p>
</tr>
</tbody>
</table>

<!--The following capabilities are available to all customers in public beta:-->

<table>
<thead>
<tr>
<th><strong>Testare il contenuto utilizzando dati di input di esempio (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Percorsi optimizer ora consente di testare diverse varianti del contenuto visualizzandolo in anteprima e inviando bozze e-mail utilizzando dati di input di esempio caricati da un file o aggiunti manualmente. Tutti gli attributi dei profili utilizzati nel contenuto per la personalizzazione vengono rilevati automaticamente dal sistema e possono essere utilizzati per i test per creare più varianti.</p>
<p>Questa funzionalità è attualmente disponibile per tutti i clienti come versione beta pubblica, per i canali di notifica e-mail, SMS e push.</p>
<p>Per ulteriori informazioni, consulta la <a href="../test-approve/simulate-sample-input.md">documentazione dettagliata</a>.</p>
<img src="assets/do-not-localize/gif-simulate.gif">
</td>
</tr>
</tbody>
</table>


<!--<table>
<thead>
<tr>
<th><strong>Use Adobe Experience Platform data for personalization (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Leverage data from Adobe Experience Platform in the personalization editor to personalize your content. To do this, datasets needed for lookup personalization must first be enabled through an API call. Once done, you can use their data to personalize your content into [!DNL Journey Optimizer].</p>
<p>This capability is currently available to all customers as a public beta.</p>
<p>For more information, refer to the <a href="../personalization/lookup-aep-data.md"</a>.</p>
</td>
</tr>
</tbody>
</table>-->

### Miglioramenti {#24-10-improvements}

Questa versione include i miglioramenti elencati di seguito.

**Canale SMS**

* Ora puoi modificare o eliminare una configurazione del canale API SMS. [Ulteriori informazioni](../sms/sms-configuration.md)

* I seguenti miglioramenti sono stati introdotti per migliorare le funzionalità di messaggistica SMS con Infobip e Sinch:

   * È possibile definire e gestire parole chiave univoche per le campagne e i percorsi SMS, consentendo una comunicazione più personalizzata ed efficiente.

   * È possibile creare e inviare un messaggio SMS predefinito quando una parola chiave non viene riconosciuta.

  Ulteriori informazioni su questi miglioramenti sono disponibili nella documentazione sulla configurazione SMS per [Infobip](../sms/sms-configuration-infobip.md) e [Sinch](../sms/sms-configuration-sinch.md).


<!--**Journeys**-->

<!--* **Path experiment in journeys** - With the journey path experiment, you can now define and track key metrics for your journey paths, allowing you to measure the impact of your activities and to provide clearer insights into your performance. -->

&lt;!--* **Numero massimo di percorsi live**: Journey Optimizer ora dispone di un guardrail di 500 percorsi live sulle sandbox di produzione, anziché di 100. Il numero di percorsi live è visibile nell’area di lavoro del percorso. <!-- DOCAC-10977-->

**Canale web**

* **Modalità di modifica non visiva per la finestra di progettazione Web**. In alternativa alla finestra di progettazione Web di Journey Optimizer, è ora possibile aggiungere modifiche al sito Web utilizzando un editor non visivo. Consente di inserire le modifiche manualmente senza aprire le pagine nell’editor visivo. Questa modalità di modifica non visiva è utile se non è possibile installare estensioni del browser come Adobe Experience Cloud Visual Helper, necessaria per caricare le pagine nel web designer. [Ulteriori informazioni](../web/web-non-visual-editor.md)


**Set di dati**

* **Eventi di invio e apertura**: a partire dal 1° novembre 2024, la segmentazione in streaming non supporterà più l’utilizzo di eventi di invio e apertura dal tracciamento e dai set di dati di feedback di Journey Optimizer. Questa modifica verrà applicata a tutte le sandbox e organizzazioni della clientela. [Ulteriori informazioni](../data/datasets-ttl.md#segmentation-update)

* **Impostazione time-to-live (TTL) del set di dati**: a partire da febbraio 2025, verrà introdotto un guardrail time-to-live (TTL) nei set di dati di Journey Optimizer generati dal sistema in nuove sandbox e nuove organizzazioni come segue:

   * 90 giorni per i dati nell’archivio dei profili
   * 13 mesi per i dati nel data lake

  In una fase successiva, questa modifica verrà implementata nelle sandbox della clientela esistente. [Ulteriori informazioni](../data/datasets-ttl.md#ttl)

* **Parametri nelle azioni personalizzate** - Data di disponibilità: 3 ottobre 2024 - I parametri NULL e facoltativi sono ora supportati nelle azioni personalizzate. [Ulteriori informazioni](../action/about-custom-action-configuration.md#define-the-message-parameters)

**Generazione rapporti**

* È ora disponibile il reporting di **Decisioning**, che offre informazioni essenziali su come i visitatori interagiscono con le esperienze. [Ulteriori informazioni](../reports/campaign-global-report-cja-code.md#decisioning-kpis)

**Governance dei dati e criteri di consenso** - Data di disponibilità: 7 ottobre 2024

* L’applicazione dei **criteri di governance dei dati** ora avviene su tutti i canali in Journey Optimizer. Per i clienti che hanno creato criteri in Adobe Experience Platform, questi vengono applicati alle azioni di marketing come parte della configurazione delle configurazioni dei canali. Durante la creazione dei contenuti tramite una configurazione, il sistema verifica tutti i campi di personalizzazione per individuare eventuali violazioni della governance dei dati. Se viene rilevata una violazione, non sarà possibile pubblicare un percorso o una campagna. [Ulteriori informazioni](../action/action-privacy.md)

* I **criteri di consenso personalizzati** ora si applicano a tutti i canali Journey Optimizer. Al momento dell’applicazione prima dell’invio di un messaggio o della consegna di un’esperienza in entrata, il sistema controlla che l’utente abbia dato il consenso all’utilizzo dei campi di personalizzazione nel contenuto che riceverà. Se non viene fornito alcun consenso, l’esperienza non sarà visualizzata. [Ulteriori informazioni](../action/consent.md)

  >[!NOTE]
  >
  >I criteri di consenso sono attualmente disponibili solo per le organizzazioni che hanno acquistato le offerte aggiuntive **Healthcare Shield** e **Privacy and Security Shield**.

**Tipi di pubblico** - Data di disponibilità: 8 ottobre 2024

* Quando esegui il targeting di un pubblico di un file CSV, ora puoi utilizzare gli attributi del file nell’editor di personalizzazione e nel generatore di regole per percorsi e campagne. [Ulteriori informazioni](../audience/about-audiences.md)

* L’utilizzo di tipi di pubblico e attributi da aggiornamenti personalizzati (file CSV) non è al momento disponibile per l’utilizzo con Healthcare Shield o Privacy and Security Shield.

**Configurazione**: data di disponibilità: 23 ottobre 2024

* Durante l’utilizzo di una configurazione personalizzata in una campagna o in un percorso, ora è possibile visualizzare in anteprima il contenuto delle e-mail per verificare la presenza di potenziali errori con le impostazioni dinamiche definite. [Ulteriori informazioni](../email/surface-personalization.md#check-configuration)

**Canale basato su codice**

* Sono ora disponibili modelli di contenuto. È possibile accelerare la creazione delle esperienze basate sul codice partendo da un modello di contenuto creato dagli sviluppatori. L’utilizzo di un modello di contenuto consente all’addetto marketing di modificare solo alcuni valori o campi, invece di comporre l’intero payload di contenuto HTML o JSON. [Ulteriori informazioni](../content-management/content-templates.md)

**Funzione decisioni**

* Gli utenti di [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=it) possono ora scegliere modelli personalizzati per l’ottimizzazione durante la configurazione di un modello di intelligenza artificiale nella funzione Decisioni (precedentemente nota come Decisioni per le esperienze). Questo consente, ad esempio, di ottimizzare su una tabella &quot;acquisti&quot; personalizzata anziché vincoli definiti come il tasso di clickthrough. [Ulteriori informazioni](../experience-decisioning/ranking.md)

* Quando aggiungi un criterio di decisione a una campagna basata su codice con Decisioning, ora puoi selezionare manualmente singoli elementi decisionali, oltre a strategie di selezione. Inoltre, ora è possibile selezionare più di un’offerta di fallback. Ciò garantisce che venga restituito un certo numero di elementi decisionali. [Ulteriori informazioni](../experience-decisioning/create-decision.md)
