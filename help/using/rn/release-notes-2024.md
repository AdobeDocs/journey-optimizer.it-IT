---
solution: Journey Optimizer
product: journey optimizer
title: Note sulle versioni 2024
description: Note sulle versioni 2024 di Journey Optimizer
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: bae533c5-1bfc-48bf-9f8d-1145383c040c
source-git-commit: b8d56578aae90383092978446cb3614a4a033f80
workflow-type: ht
source-wordcount: '6783'
ht-degree: 100%

---

# Note sulle versioni 2024 {#release-notes-2024}

In questa pagina sono elencate tutte le funzioni e i miglioramenti di [!DNL Journey Optimizer] rilasciati nel 2024.

## Versione di ottobre 2024 {#24-10-rn}

**Data di rilascio**: 29-30 ottobre 2024

### Nuove funzionalità {#24-10-features}

Questa versione include le nuove funzionalità elencate di seguito:

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
<p>Disponibile dal 1° ottobre 2024</p>
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
<p>Disponibile dal 1° ottobre 2024</p>
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
<p>In Journey Optimizer, gestire il volume e la tempistica delle campagne e dei percorsi è essenziale per evitare di sopraffare la clientela con troppe interazioni. Journey Optimizer offre ora diversi strumenti per la gestione dei conflitti e la definizione delle priorità. <p>Per ulteriori informazioni, consulta la <a href="../conflict-prioritization/gs-conflict-prioritization.md">documentazione dettagliata</a>.</p></p><p><ul><li><b>Quota limite percorsi</b>: ora è possibile creare set di regole da applicare ai tuoi percorsi, in modo da limitare il numero di percorsi per un profilo per giorno, settimana o mese, nonché controllare il numero di percorsi simultanei in esecuzione contemporaneamente.</li>
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
<li>Accelerare i flussi di lavoro dei professionisti per la clientela di Journey Optimizer che utilizza Da Vinci per l’authoring e Adobe Journey Optimizer per l’ottimizzazione e la consegna</li>
<li>Ottimizzare i modelli Da Vinci con dati Adobe.</li></ul></p>
<p>Per ulteriori informazioni, consulta la <a href="https://movableink.com/adobe-and-movable-ink">documentazione di Movable Ink Da Vinci</a>.</p>
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


<table>
<thead>
<tr>
<th><strong>Funzione decisioni (disponibilità generale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La funzione Decisioni, precedentemente disponibile per un set di organizzazioni (LA) e nota come Decisioni per le esperienze, è ora disponibile per tutti gli utenti (GA), incluse le organizzazioni che hanno acquistato le offerte aggiuntive Adobe Healthcare Shield o Privacy and Security Shield.</p><p>La funzione Decisioni semplifica la personalizzazione proponendo un catalogo centralizzato di offerte di marketing note come “elementi decisionali” e un motore decisionale sofisticato. Questo motore sfrutta le regole e i criteri di classificazione per selezionare e presentare a ogni persona gli elementi decisionali più rilevanti. Questi elementi decisionali sono integrati direttamente in un’ampia gamma di superfici in entrata tramite il canale di esperienza basato su codice.</p>
<p>Per ulteriori informazioni, consulta la <a href="../experience-decisioning/gs-experience-decisioning.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

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
<p>Con la disponibilità generale, vengono introdotte quattro nuove funzioni: la possibilità di creare metriche semplici, creare e pubblicare tipi di pubblico, porre domande ad hoc tramite Insight Builder e pianificare l’invio automatico via e-mail dei rapporti ai destinatari chiave.</p>
<p>Per ulteriori informazioni, consulta la <a href="../reports/report-cja-manage.md">documentazione dettagliata</a>.</p>
<img src="assets/do-not-localize/ajo-cja.gif">
<p>Importante: l’esperienza di reporting corrente verrà ritirata a partire da gennaio 2025. Dopo questa data, la nuova esperienza di reporting diventerà lo standard. Consigliamo di acquisire familiarità con le nuove funzioni e funzionalità per garantire una transizione semplice. <a href="../reports/report-gs-cja.md">Scopri come iniziare a utilizzare la nuova interfaccia di reporting di Journey Optimizer</a></p>
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
<p>Journey Optimizer ora consente di testare diverse varianti di contenuto visualizzandolo in anteprima e inviando le bozze delle e-mail utilizzando dati di input di esempio caricati da un file o aggiunti manualmente. Tutti gli attributi dei profili utilizzati nel contenuto per la personalizzazione vengono rilevati automaticamente dal sistema e possono essere utilizzati per i test per creare più varianti.</p>
<p>Questa funzionalità è attualmente disponibile per tutta la clientela come versione beta pubblica, per i canali di notifica e-mail, SMS e push.</p>
<p>Per ulteriori informazioni, consulta la <a href="../test-approve/simulate-sample-input.md">documentazione dettagliata</a>.</p>
<img src="assets/do-not-localize/gif-simulate.gif">
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Utilizzare i dati di Adobe Experience Platform per la personalizzazione (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sfrutta i dati da Adobe Experience Platform nell’editor di personalizzazione per personalizzare i contenuti. A questo scopo, i set di dati necessari per la personalizzazione della ricerca devono prima essere abilitati tramite una chiamata API. Al termine, è possibile utilizzare i relativi dati per personalizzare il contenuto in [!DNL Journey Optimizer].</p>
<p>Questa funzionalità è accessibile a tutti i clienti come versione Beta pubblica.</p>
<p>Per ulteriori informazioni, consulta la <a href="../personalization/aep-data-perso.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti {#24-10-improvements}

Questa versione include i miglioramenti elencati di seguito.

**Canale SMS**

* Ora è possibile modificare o eliminare una configurazione dei canali API SMS. [Ulteriori informazioni](../sms/sms-configuration.md)

* I seguenti miglioramenti sono stati introdotti per migliorare le funzionalità di messaggistica SMS con Infobip e Sinch:

   * È possibile definire e gestire parole chiave univoche per le campagne e i percorsi SMS, consentendo una comunicazione più personalizzata ed efficiente.

   * È possibile creare e inviare un messaggio SMS predefinito quando una parola chiave non viene riconosciuta.

  Ulteriori informazioni su questi miglioramenti sono disponibili nella documentazione sulla configurazione di SMS per [Infobip](../sms/sms-configuration-infobip.md) e [Sinch](../sms/sms-configuration-sinch.md).


<!--**Journeys**-->

<!--* **Path experiment in journeys** - With the journey path experiment, you can now define and track key metrics for your journey paths, allowing you to measure the impact of your activities and to provide clearer insights into your performance. -->

<!--* **Max number of Live journeys** - Journey Optimizer now has a guardrail of 500 live journeys on production sandboxes, instead of 100. The number of live journeys is visible in the journey canvas. (DOCAC-10977) -->

**Canale web**

* **Modalità di modifica non visiva per il Designer web**: in alternativa al Designer web di Journey Optimizer, ora è possibile aggiungere modifiche al sito web utilizzando un editor non visivo. Questo consente di inserire le modifiche manualmente senza aprire le pagine nell’editor visivo. La modalità di modifica non visiva è utile se non è possibile installare estensioni del browser come Adobe Experience Cloud Visual Helper, necessarie per caricare le pagine nel Designer web. [Ulteriori informazioni](../web/web-non-visual-editor.md)


**Set di dati**

* **Eventi di invio e apertura**: a partire dal 1° novembre 2024, la segmentazione in streaming non supporterà più l’utilizzo di eventi di invio e apertura dal tracciamento e dai set di dati di feedback di Journey Optimizer. Questa modifica verrà applicata a tutte le sandbox e organizzazioni della clientela. [Ulteriori informazioni](../data/datasets-ttl.md#segmentation-update)

* **Impostazione time-to-live (TTL) del set di dati**: a partire da febbraio 2025, verrà introdotto un guardrail time-to-live (TTL) nei set di dati di Journey Optimizer generati dal sistema in nuove sandbox e nuove organizzazioni come segue:

   * 90 giorni per i dati nell’archivio dei profili
   * 13 mesi per i dati nel data lake

  In una fase successiva, questa modifica verrà implementata nelle sandbox della clientela esistente. [Ulteriori informazioni](../data/datasets-ttl.md#ttl-guardrail)

* **Parametri nelle azioni personalizzate**: la data di disponibilità è il 3 ottobre 2024. I parametri NULL e facoltativi sono ora supportati nelle azioni personalizzate. [Ulteriori informazioni](../action/about-custom-action-configuration.md#define-the-message-parameters)

**Generazione rapporti**

* È ora disponibile **il reporting della funzione decisioni** che offre informazioni essenziali su come i visitatori interagiscono con le esperienze. [Ulteriori informazioni](../reports/campaign-global-report-cja-code.md#decisioning-kpis)

**Governance dei dati e criteri di consenso** - Data di disponibilità: 7 ottobre 2024

* L’applicazione dei **criteri di governance dei dati** ora avviene su tutti i canali in Journey Optimizer. Per coloro che hanno creato criteri in Adobe Experience Platform, questi vengono applicati alle azioni di marketing come parte dell’impostazione delle configurazioni dei canali. Durante la creazione dei contenuti tramite una configurazione, il sistema verifica tutti i campi di personalizzazione per individuare eventuali violazioni della governance dei dati. Se viene rilevata una violazione, non sarà possibile pubblicare un percorso o una campagna. [Ulteriori informazioni](../action/action-privacy.md)

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

* Sono ora disponibili modelli di contenuto. È possibile accelerare la creazione delle esperienze basate sul codice partendo da un modello di contenuto creato dagli sviluppatori. L’utilizzo di un modello di contenuto consente ai marketer di modificare solo alcuni valori o campi, invece di comporre l’intero payload di contenuto HTML o JSON. [Ulteriori informazioni](../content-management/content-templates.md)

**Funzione decisioni**

* Gli utenti di [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=it) possono ora scegliere modelli personalizzati per l’ottimizzazione durante la configurazione di un modello di intelligenza artificiale nella funzione Decisioni (precedentemente nota come Decisioni per le esperienze). Questo consente, ad esempio, di ottimizzare una tabella “acquisti” personalizzata, anziché i vincoli definiti come il tasso di click-through. [Ulteriori informazioni](../experience-decisioning/ranking/ranking.md)

* Quando viene aggiunto un criterio di decisione a una campagna basata su codice con la funzione Decisioni, ora è possibile selezionare manualmente singoli elementi di decisione, oltre a strategie di selezione. Inoltre, ora è possibile selezionare più di un’offerta di fallback. Ciò garantisce che venga restituito un certo numero di elementi decisionali. [Ulteriori informazioni](../experience-decisioning/create-decision.md)



## Versione di settembre 2024 {#24-9-rn}

<!--
>[!CAUTION]
>
>**Early release notes below are subject to change without prior notice until the release date**. Links, screens and updated documentation are published at the release date.
>
-->

**Data di rilascio**: 24-26 settembre 2024

### Nuove funzionalità {#24-9-features}

Questa versione include le nuove funzionalità elencate di seguito.

<table>
<thead>
<tr>
<th><strong>Schede di contenuto per app per dispositivi mobili e siti web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le schede di contenuto sono una nuova funzione di messaggistica digitale di Adobe Journey Optimizer che offre contenuti personalizzati e coinvolgenti direttamente all’interno di app mobili e siti web. A differenza delle notifiche push tradizionali, le schede di contenuto si integrano perfettamente nell’interfaccia utente, offrendo aggiornamenti persistenti e non intrusivi che migliorano l’interazione e l’esperienza utente.</p>
<p>Questa funzione consente a marketer di presentare contenuti rich media rilevanti agli utenti, aumentando il coinvolgimento e garantendo la visualizzazione di messaggi importanti senza interromperne il percorso.</p>
<p>Per ulteriori informazioni, consulta la <a href="../../rp_landing_pages/content-card-landing-page.md">documentazione dettagliata</a>.</p>
<img src="assets/do-not-localize/content-card.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Approvazioni in percorsi e campagne (LA)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con i criteri di approvazione, ora puoi impostare un processo di approvazione in Journey Optimizer che consenta ai team di marketing di garantire che le campagne e i percorsi vengano rivisti e autorizzati dagli stakeholder prima della pubblicazione.</p>
<p>I criteri di approvazione sono attualmente disponibili solo per alcune organizzazioni (disponibilità limitata). Per ottenere l’accesso, contatta il tuo rappresentante Adobe.</p>
<p>Per ulteriori informazioni, consulta la <a href="../test-approve/gs-approval.md">documentazione dettagliata</a>.</p>
<img src="assets/do-not-localize/approval.gif"/>
</td>
</tr>
</tbody>
</table>

<!--<table>
<thead>
<tr>
<th><strong>Email Content Locking</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer now allows you to lock content in email templates, either by locking the entire template or specific structures and component. This allows you to prevent unintentional edits or deletions, giving you greater control over template customization, and improving the efficiency and reliability of your email campaigns.</p>
<p>For more information, refer to the <a href="../content-management/gs-generative.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/gif-content-locking.gif">
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Criteri di uscita globali nei percorsi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi definire i criteri di uscita a livello di percorso. Aggiungendo i criteri di uscita, fai in modo che i profili escano dal percorso non appena si verifica un evento (ad esempio, un acquisto) oppure se sono idonei per un pubblico. Questo impedirà all’utente di ricevere ulteriori comunicazioni dal percorso.</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/journey-properties.md#exit-criteria">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Assistente IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Dopo aver creato e personalizzato il messaggio, perfeziona ulteriormente il contenuto con l’Assistente IA in Journey Optimizer. Ora puoi utilizzare l’Assistente IA per ottimizzare l’impatto del messaggio sperimentando diversi titoli principali e immagini. Ogni variante viene gestita come un trattamento univoco, per misurare e confrontare quale titolo genera effettivamente più clic.</p>
<p>Immergiti in un’esperienza pratica con <a href="https://experienceleague.adobe.com/it/apps/journey-optimizer/ai-assistant-content-accelerator">la nostra anteprima della funzione live</a>, progettata per permetterti di esplorarla in prima persona e comprenderne appieno le funzionalità.</a>.</p>
<p>Per ulteriori informazioni, consulta la <a href="../content-management/gs-generative.md">documentazione dettagliata</a>.</p>
<img src="assets/do-not-localize/ai-content.gif"/>
<p>Data di disponibilità: 12 settembre 2024</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Configurazione guidata del canale</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La configurazione guidata del canale consente di automatizzare e convalidare la configurazione del canale in un’esperienza unificata, per velocizzare la fase iniziale di adozione di Journey Optimizer. Questa nuova configurazione guidata semplifica la configurazione rapida dei canali, affinché tutte le risorse necessarie siano installate e funzionanti in Experience Platform, Journey Optimizer e Raccolta dati. Questo consente ai team di marketing, di prodotto e di data engineering di iniziare rapidamente a creare campagne e percorsi.</p>
<p>Per ulteriori informazioni, consulta la <a href="../configuration/set-mobile-config.md">documentazione dettagliata</a>.</p>
<img src="assets/do-not-localize/guided-setup.gif"/>
<p>Data di disponibilità: 3 settembre 2024</p>
</br>
</td>
</tr>
</tbody>
</table>


### Miglioramenti {#24-9-improvements}

Questa versione include i miglioramenti elencati di seguito.

**Tipi di pubblico** - Data di disponibilità: 17 settembre 2024

**Utilizzo licenze**: la dashboard Utilizzo licenze mostra ora i profili anziché i tipi di pubblico che potrebbero essere coinvolti. [Ulteriori informazioni](../audience/license-usage.md)

**Gestione dei contenuti**

Ora puoi esportare modelli di contenuto e frammenti tra sandbox. [Ulteriori informazioni](../configuration/copy-objects-to-sandbox.md)

**Percorsi**

* **Miglioramenti al reporting in tempo reale**: il reporting in tempo reale fornisce informazioni approfondite sulle prestazioni dei percorsi nelle ultime 24 ore. È stato migliorato con l’aggiunta di nuove metriche (profili in entrata, in uscita e scartati e profili in errore) che consentono di comprendere più a fondo il comportamento e le prestazioni degli utenti direttamente dall’area di lavoro del percorso. [Ulteriori informazioni](../building-journeys/report-journey.md)


* (Data di disponibilità: 10 settembre) **Nuovi tentativi automatici per Leggi pubblico**: i nuovi tentativi vengono ora applicati per impostazione predefinita ai percorsi attivati dal pubblico (a partire da **Leggi pubblico** o **Evento business**) durante il recupero del processo di esportazione. Se si verifica un errore durante la creazione del processo di esportazione, verranno eseguiti nuovi tentativi ogni 10 minuti, per un massimo di 1 ora. Dopo i tentativi, verrà considerato come un errore. Questi tipi di percorsi possono quindi essere eseguiti fino a 1 ora dopo l’orario pianificato. [Ulteriori informazioni](../building-journeys/read-audience.md#retries)

**Canale e-mail**

* **Intestazione del messaggio nell’e-mail inviata e nella copia in Ccn**: è stata aggiunta una nuova intestazione a tutti i messaggi e-mail. Il valore di questa intestazione è univoco per ogni e-mail inviata e per la relativa copia in Ccn. Questa intestazione viene inoltre memorizzata nei set di dati del messaggio e del feedback Ccn, per consentire di riconciliare la copia Ccn e le informazioni dell’e-mail inviata corrispondente. [Ulteriori informazioni](../configuration/archiving-support.md#bcc-header)

* **Punteggio contenuti spam** (GA): ora puoi controllare il punteggio di contenuti spam nel **Rapporto spam** dedicato. Utilizzando SpamAssassin, Adobe Journey Optimizer può ora testare il contenuto delle e-mail e assegnargli un punteggio per indicare se gli ISP o i provider di caselle postali lo considereranno come contenuto indesiderato o meno. [Ulteriori informazioni](../content-management/spam-report.md)

**Canale SMS**

* **Modifica credenziali API**: è ora possibile modificare le impostazioni nelle credenziali API SMS, inclusi gli aggiornamenti alle parole chiave e alle risposte di consenso/rinuncia.

**API**

* **API di simulazione della campagna**: utilizza questa API per attivare il processo di bozza di una campagna. L’invio della bozza di una campagna è un processo asincrono, l’API restituirà un proofJobId che può essere utilizzato per controllare lo stato della bozza. [Ulteriori informazioni](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target="_blank"}

* (Data di disponibilità: 10 settembre) La [documentazione API di Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target="_blank"} è ora interattiva. Esplora gli endpoint API direttamente dalle pagine della documentazione per ottenere un feedback immediato e velocizzare l’implementazione tecnica.


  Tutte le pagine di riferimento API ora dispongono di una funzionalità **Provala** che puoi utilizzare per testare le chiamate API direttamente nella pagina del sito web della documentazione. [Ottieni le credenziali di autenticazione richieste](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"} e inizia a utilizzare la funzionalità per esplorare gli endpoint API.

  Utilizza questa nuova funzionalità per esplorare le richieste e le risposte dagli endpoint API, per ottenere feedback immediati e velocizzare l’implementazione tecnica.

  >[!CAUTION]
  >
  >Tieni presente che utilizzando la funzionalità API interattiva nelle pagine della documentazione, stai effettuando chiamate API reali agli endpoint. Tieni presente questo aspetto durante la sperimentazione con le sandbox di produzione.

**Configurazione**

* **Piani di preparazione IP**: questa funzionalità è ora disponibile per tutti i clienti, incluse le organizzazioni che hanno acquistato i componenti aggiuntivi Adobe **Healthcare Shield** o **Privacy and Security Shield**. [Ulteriori informazioni](../configuration/ip-warmup-gs.md)

<!--
![Newsletter](../assets/do-not-localize/nl-icon.png) Sign up for the [Adobe Journey Optimizer quarterly newsletter](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} today, and receive the latest product updates, exciting stories, use cases, tips and more delivered directly to your inbox every quarter.-->



## Versione di agosto 2024 {#8-2024}

**Data di rilascio**: 20-21 agosto 2024

### Nuove funzionalità {#8-features}

Questa versione include le nuove funzionalità elencate di seguito.

<!--
<table>
<thead>
<tr>
<th><strong>Content Cards (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Content cards are a new digital messaging feature in Adobe Journey Optimizer that delivers personalized and engaging content directly within mobile apps and websites. Unlike traditional push notifications, Content Cards integrate seamlessly into the user interface, offering persistent, non-intrusive updates that enhance user interaction and experience.</p>
<p>This feature enables marketers to present relevant, rich media content to users, driving higher engagement and ensuring important messages are seen without disrupting the user journey.</p>
</br>
<p>Content card are currently only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Configurazioni dei canali migliorate</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le funzionalità della superficie di canale corrente sono state migliorate per un approccio coerente su tutti i canali. Ora è possibile definire, gestire e riutilizzare queste configurazioni per qualsiasi canale, incluso il Web, la messaggistica in-app o l’esperienza basata su codice.</p>
<p><ul>
<li>Le superfici di canale ora sono state rinominate in <strong>Configurazioni di canale</strong></li>
<li>È possibile allegare una o più azioni di marketing per applicare il consenso e i criteri di governance dei dati</li>
<li>Il controllo dell’accesso a livello di oggetto (OLAC) è ora disponibile per ogni configurazione di canale, consentendo di decidere quali utenti possono creare o utilizzare configurazioni specifiche</li>
<li>Per alcuni canali, è possibile creare configurazioni di canale in grado di eseguire il targeting per più piattaforme. Ad esempio, potrebbe trattarsi di una configurazione di canale di messaggistica in-app in grado di eseguire il targeting per una pagina web, un’app iOS e un’app Android.</li>
</ul></p>
<p>Per ulteriori informazioni, consulta la <a href="../configuration/channel-surfaces.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Azione personalizzata Marketo Engage</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi integrare Adobe Journey Optimizer con Adobe Marketo Engage per creare i tuoi casi d’uso B2B. Una nuova azione personalizzata da un percorso consente di acquisire dati in Marketo.</p>
<p>Per ulteriori informazioni, consulta la <a href="../action/marketo-engage.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Variabili nei frammenti di contenuto</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le variabili globali dei frammenti aumentano la funzionalità dei frammenti esistenti per migliorare l’efficienza in termini di riutilizzo dei contenuti e casi d’uso di scripting. I frammenti possono ora utilizzare variabili di input e creare variabili di output utilizzabili nel contenuto delle campagne e dei percorsi. I frammenti ora possono utilizzare variabili di input, sia nei <a href="../personalization/use-expression-fragments.md">frammenti di espressione</a> che nei <a href="../email/use-visual-fragments.md">frammenti visivi</a>. Puoi utilizzare queste variabili per personalizzare il contenuto e i parametri dei messaggi nelle campagne e nei percorsi.</p>
<p>Per ulteriori informazioni, consulta la <a href="../personalization/use-expression-fragments.md">documentazione dettagliata</a>.</p>
</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Flusso di lavoro di preparazione IP</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Data di disponibilità: 13 agosto</p>
<p>Se invii un’e-mail con un nuovo indirizzo IP, ora puoi eseguire facilmente i flussi di lavoro di preparazione IP direttamente dall’interfaccia utente. Adobe Journey Optimizer offre un modo standardizzato ed efficiente di preparare gli indirizzi IP seguendo le best practice per una recapitabilità ottimale.</p>
<p>Per ulteriori informazioni, consulta la <a href="../configuration/ip-warmup-gs.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti {#8-improvements}

Questa versione include i miglioramenti elencati di seguito.

**Percorsi**

* Nell’attività **Condizione**, per impostazione predefinita, adesso la **[!UICONTROL Condizione temporale]** è impostata per ora, dalle 00:00 alle 12:00. [Ulteriori informazioni](../building-journeys/condition-activity.md#time_condition)
* Durante la creazione dei percorsi, gli avvisi vengono ora visualizzati da un pulsante **Avvisi**, per allinearsi agli altri avvisi e fornire un’esperienza utente coerente. [Ulteriori informazioni](../building-journeys/troubleshooting.md#activity-errors)
* Sono state migliorate le opzioni di zoom nella barra degli strumenti del percorso: la percentuale dello zoom è ora visibile ed è possibile reimpostare più facilmente il valore dello zoom.

**Canale push**

* Ora è possibile aggiungere le credenziali push dell’app mobile nelle impostazioni della configurazione dei canali di Adobe Journey Optimizer. Non è più necessario creare una superficie app nella raccolta dati di Adobe Experience Platform.

### Altre modifiche {#changes}

**Reporting**

* Sono stati aggiunti nuovi casi d’uso alla nuova esperienza di reporting:

   * Creazione di metriche calcolate personalizzate direttamente nei rapporti.
   * Creazione di un pubblico dai dati di reporting.
   * Utilizzo dello strumento di analisi esplorativa per creare facilmente tabelle e visualizzazioni da **[!UICONTROL Dimensioni]** e **[!UICONTROL Metriche]** selezionate.

  Per ulteriori informazioni, consulta la [documentazione dettagliata](../reports/report-cja-manage.md).



## Versione di luglio 2024 {#24-7-2024}

**Data di rilascio**: 30-31 luglio 2024

### Nuove funzionalità {#27-4-features}

Questa versione include le nuove funzionalità elencate di seguito.

<table>
<thead>
<tr>
<th><strong>Canale SMS con qualsiasi provider (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora, in Journey Optimizer, puoi configurare altri provider SMS oltre a quelli predefiniti Sinch, Infobip e Twilio.</p>
<img src="assets/do-not-localize/byo_sms.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../sms/sms-configuration-custom.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Composizione di pubblico federato (disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Composizione di pubblico federato è ora disponibile in Adobe Journey Optimizer. Consente alle aziende di comporre dati per un migliore utilizzo in vari casi d’uso. Con questo nuovo approccio, in qualità di utente di Adobe Real-Time Customer Data Platform e/o di Adobe Journey Optimizer, puoi federare i set di dati direttamente dal data warehouse esistente per arricchire i tipi di pubblico e gli attributi di Adobe Experience Platform in un unico sistema.</p>
<p>Per ulteriori informazioni, consulta la <a href="https://experienceleague.adobe.com/it/docs/federated-audience-composition/using/home"  target="_blank">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti {#27-4-improvements}

Questa versione include i miglioramenti elencati di seguito.

**Percorsi**

* (Data di disponibilità: 8 luglio) **Editor di espressioni avanzate nella configurazione degli eventi percorso**: ora puoi sfruttare l’editor di espressioni avanzate durante la configurazione di un evento, in modo da definire espressioni più complesse o utilizzare funzioni nella condizione ID evento. [Ulteriori informazioni](../event/about-creating.md#adv-exp-editor)



## Versione di giugno 2024 {#24-6-2024}

**Data di rilascio**: 18-19 giugno 2024

### Nuove funzionalità {#june-24-features}

Questa versione include le nuove funzionalità elencate di seguito.

<table>
<thead>
<tr>
<th><strong>Personalizzazione Frammenti di contenuto</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora è possibile definire in un frammento campi specifici che possono essere modificati quando il frammento viene aggiunto a una campagna o a un percorso. Questo consente di regolare le parti di contenuto al momento dell’utilizzo, fornendo flessibilità per sovrascrivere i valori predefiniti con dettagli specifici del contesto.</p>
<img src="../content-management/assets/do-not-localize/gif-fragments.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../content-management/customizable-fragments.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Reporting con Customer Journey Analytics (Disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La funzione di reporting di Journey Optimizer include una migliorata interoperabilità con le funzionalità di Customer Journey Analytics, per standardizzare il reporting su entrambe le piattaforme e migliorare la coerenza e l’affidabilità dei dati. Questa integrazione diretta tra Journey Optimizer e Customer Journey Analytics fornisce una visione più chiara delle metriche delle prestazioni e consente agli utenti di prendere decisioni più informate.</p>
<img src="assets/do-not-localize/ajo-cja.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../reports/report-gs-cja.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Assistente IA in Adobe Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Assistente IA è una funzione dell’interfaccia utente che consente di accedere ai concetti Adobe, comprenderli e ottenere informazioni operative per l’ambiente specifico. È disponibile in diversi prodotti Adobe Experience Cloud, tra cui Adobe Journey Optimizer.</p>
<p>Per ulteriori informazioni, consulta la <a href="../start/ai-assistant.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

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
<p>Il contenuto multilingue è attualmente disponibile solo per alcune organizzazioni (disponibilità limitata). Per ottenere l’accesso, contatta il tuo rappresentante Adobe.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Sperimentazione nei percorsi (disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Già disponibile nelle campagne, Adobe Journey Optimizer ora supporta gli esperimenti nei percorsi. Gli esperimenti sono test randomizzati: nel contesto dei test online significa che esponi alcuni utenti selezionati in modo casuale a una determinata variante di un messaggio e un altro gruppo di utenti selezionato in modo casuale a un’altra variante o trattamento. Dopo l’esposizione, puoi quindi misurare le metriche del risultato che ti interessano, ad esempio apertura di e-mail, iscrizioni o acquisti.</p>
<p>La sperimentazione nei percorsi è attualmente disponibile solo per alcune organizzazioni (disponibilità limitata). Per ottenere l’accesso, contatta il tuo rappresentante Adobe.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Extended personalization data - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now lookup and fetch data values within Adobe Experience Platform datasets, and use these values to build conditions in Adobe Journey Optimizer. You can leverage data from a lookup dataset when a relationship has been defined using an attribute inside of an array of objects. You can specify non-profile enabled datasets for lookup. Once enabled, you can use a profile attribute as a join key to the specified dataset to retrive further data for personalization.</p>
<p>This capability is currently available as a public beta.</p>
</td>
</tr>
</tbody>
</table-->

### Miglioramenti {#june24-improvements}

Questa versione include i miglioramenti elencati di seguito.

#### Gestione delle decisioni

* **Supporto di più regole nella gestione delle decisioni**: ora è possibile aggiungere fino a 10 regole di limitazione per una determinata offerta in Gestione delle decisioni. Ciò offre un maggiore controllo sulla modalità di invio delle offerte. [Ulteriori informazioni](../offers/offer-library/add-constraints.md#capping)

<!--* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->

#### Frammenti di contenuto

>[!AVAILABILITY]
>
>Questi miglioramenti verranno introdotti gradualmente nel corso di alcuni giorni dopo il rilascio iniziale. Alcuni utenti potranno accedervi subtio, mentre altri li troveranno nel proprio account con un leggero ritardo.

* È ora possibile modificare i frammenti e propagare le modifiche in tutti i percorsi live e le campagne in cui vengono utilizzati.
* Sono stati introdotti nuovi stati per i frammenti di contenuto: **Bozza**, **Live**, **Pubblicazione** e **Archiviato**.
* Per utilizzare un frammento in un percorso o in una campagna, ora è necessario che sia in stato **Live**. È stato aggiunto un nuovo passaggio al processo di creazione del frammento, che consente di pubblicarlo e renderlo disponibile per l’utilizzo in percorsi e campagne. Tenere presente che la pubblicazione del frammento richiede una nuova autorizzazione.

  **ATTENZIONE**: dato che gli stati **Bozza** e **Live** sono stati introdotti con la versione di giugno di Journey Optimizer, tutti i frammenti creati prima di questa versione presentano lo stato **Bozza** anche se vengono utilizzati in un percorso o in una campagna. Se apporti modifiche a questi frammenti, è necessario [pubblicarli](../content-management/create-fragments.md#publish) per renderli “live” e propagare le modifiche alle campagne e ai percorsi associati. È necessario creare anche una nuova versione di campagna/percorso e pubblicarla.

Per ulteriori informazioni, consulta la documentazione sui [frammenti di contenuto](../content-management/fragments.md).

#### Percorsi

* Il timeout globale dei percorsi è stato esteso a 91 giorni. [Ulteriori informazioni](../building-journeys/journey-properties.md#global_timeout)

  Questo nuovo timeout verrà applicato a tutti i nuovi percorsi creati. Per ulteriori informazioni, consulta la [sezione Domande frequenti](../building-journeys/journey-properties.md#timeout-faq). Queste modifiche verranno implementate gradualmente nel corso del mese di giugno.


* Adobe Journey Optimizer ora supporta le richieste di accesso/eliminazione della privacy e le richieste di gestione del ciclo di vita dei dati. [Ulteriori informazioni](../privacy/requests.md)
* È ora possibile ridimensionare le colonne nell’inventario del percorso.
  <!--* **Advanced expression editor in Event configuration** is now GA - You can now leverage the advanced expression editor while configuring an event, allowing you to define more complex expressions or use functions in the event id condition. This capability is released in Limited Availability for selected customers. [Read more](../event/about-creating.md)-->
* I **Criteri di unione** ora sono disponibili: i criteri di unione utilizzati da un percorso sono quindi visibili e coerenti in tutto il percorso. [Ulteriori informazioni](../building-journeys/journey-properties.md#merge-policies)


#### Campagne

* Durante la creazione di una campagna in Adobe Journey Optimizer, ora è possibile scegliere il tipo di campagna (pianificata o attivata) in una nuova finestra modale. [Ulteriori informazioni](../campaigns/create-campaign.md)

#### Canale e-mail

* **Annullamento iscrizione a mailing list**: a seguito dei recenti annunci Gmail e Yahoo per mittenti in blocco, Journey Optimizer supporta l’opzione Annullamento iscrizione a mailing list “post/1 clic”. Consulta le pagine seguenti: [Gestione della rinuncia e-mail](../email/email-opt-out.md#unsubscribe-header) e [Configurare le impostazioni e-mail](../email/email-settings.md#list-unsubscribe).

  **NOTA**: per qualsiasi nuova superficie di canale, l’opzione di intestazione per annullare l’iscrizione alla mailing list viene attivata per impostazione predefinita. Per le superfici esistenti, l’opzione URL di annullamento iscrizione con un solo clic nelle impostazioni della superficie di canale non è selezionata per impostazione predefinita. Se in precedenza utilizzavi un URL di rinuncia con un solo clic nel corpo dell’e-mail, questa impostazione è ancora valida. Se nelle impostazioni della superficie di canale, l’opzione URL di annullamento dell’iscrizione con un solo clic è selezionata, Adobe Journey Optimizer preferisce utilizzare l’URL per l’annullamento dell’iscrizione con un clic generato predefinito.

#### Canale SMS

* Ora è possibile aggiungere codici brevi univoci per ogni sandbox con una singola configurazione API, per rendere il processo più efficiente e lineare. [Ulteriori informazioni](../sms/sms-configuration.md)

* Dopo la creazione, il campo **Token API** sulla pagina **Dettagli delle credenziali API** ora è mascherato.

<!--* You can now modify existing SMS configurations.-->

#### Canale in-app

<!--* **Expression fragment** - Expression fragments are now available for the **In-app channel**. [Read more](../personalization/use-expression-fragments.md)-->

* Ora è possibile utilizzare il plug-in Edge Delivery per ottenere le informazioni necessarie per comprendere e risolvere i problemi relativi alle implementazioni in entrata. [Ulteriori informazioni sulla vista Edge Delivery](https://experienceleague.adobe.com/it/docs/experience-platform/assurance/view/edge-delivery){target="_blank"}


#### Canale direct mail

* Il canale direct mail è ora disponibile per tutta la clientela. [Ulteriori informazioni](../direct-mail/get-started-direct-mail.md)



## Versione di maggio 2024 {#may-2024}

**Data di rilascio**: 21-22 maggio 2024

### Nuove funzionalità {#e-features}

Questa versione include le nuove funzionalità elencate di seguito.

<table>
<thead>
<tr>
<th><strong>Decisioni per le esperienze: disponibilità limitata</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La funzione Decisioni per le esperienze semplifica la personalizzazione proponendo un catalogo centralizzato di offerte di marketing note come “elementi decisionali” e un motore decisionale sofisticato. Questo motore sfrutta le regole e i criteri di classificazione per selezionare e presentare a ogni persona gli elementi decisionali più rilevanti.</p>
<p>Gli elementi decisionali sono integrati direttamente in un’ampia gamma di configurazioni in entrata tramite il nuovo canale di esperienza basato su codice, ora accessibile nelle campagne Journey Optimizer. I criteri decisionali relativi alla funzione Decisioni per le esperienze sono disponibili per l’utilizzo solo in campagne di esperienza basate su codice.</p>
<p>La funzione Decisioni per le esperienze è attualmente disponibile solo per alcune organizzazioni (disponibilità limitata). Per ottenere l’accesso, contatta il tuo rappresentante Adobe.</p>
<img src="assets/do-not-localize/gif-exd.gif"/>
<p>Per ulteriori informazioni, consulta la <a href="../experience-decisioning/gs-experience-decisioning.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Personalizzazione della configurazione e-mail - Disponibilità limitata</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi definire sottodomini dinamici e parametri di intestazione personalizzati durante la creazione di configurazioni per il canale e-mail, per maggiore flessibilità e controllo sulle impostazioni e-mail.</p>
<p>La personalizzazione della configurazione e-mail è attualmente disponibile solo per un set di organizzazioni (disponibilità limitata). Per ottenere l’accesso, contatta il tuo rappresentante Adobe.</p>
<p>Per ulteriori informazioni, consulta la <a href="../email/surface-personalization.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>IP Warmup Workflow</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>If you are sending email on a brand new IP address, you can now easily perform IP warmup workflows directly from the user interface. Adobe Journey Optimizer offers a standardized and efficient way to warm up your IP adresses that follows the best practices for optimal deliverability.</p>
<p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Business rules - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create granular frequency capping rules, and apply them to different types of marketing communications through rule sets. This new capability lets you control how often your audiences receive a message by setting cross-channel rules, that automatically exclude over-solicited profiles from messages and actions.</p>
<p>Business rules capability is currently available as a beta. To join the beta program, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Extended personalization data - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now lookup and fetch data values within Adobe Experience Platform datasets, and use these values to build conditions in Adobe Journey Optimizer. You can leverage data from a lookup dataset when a relationship has been defined using an attribute inside of an array of objects. You can specify non-profile enabled datasets for lookup. Once enabled, you can use a profile attribute as a join key to the specified dataset to retrive further data for personalization.</p>
<p>This capability is currently available as a public beta.</p>
</td>
</tr>
</tbody>
</table-->

### Miglioramenti {#e-improvements}

Questa versione include i miglioramenti elencati di seguito.

**Decisioni per le esperienze**: disponibilità limitata

Dalla versione beta a quella con Disponibilità limitata, sono stati aggiunti i seguenti miglioramenti:

* **Decisioni per le esperienze + Esperienze basate su codice**: ora puoi sfruttare la funzione Decisioni per le esperienze per utilizzare gli elementi decisionali nelle campagne basate su codice. Nota: il canale di esperienza basato su codice e la funzione Decisioni per le esperienze non sono disponibili per le organizzazioni che hanno acquistato le offerte aggiuntive Healthcare Shield e Privacy and Security Shield di Adobe. [Ulteriori informazioni](../code-based/get-started-code-based.md)
* **Dati contestuali**: ora puoi sfruttare i dati contestuali provenienti da Adobe Experience Platform nelle regole di decisione e nelle formule di classificazione. [Ulteriori informazioni](../experience-decisioning/context-data.md)
* **Nuova autorizzazione**: è ora disponibile la nuova autorizzazione “Gestisci decisioni per le esperienze” per la risorsa Gestione delle decisioni. Questa consente di gestire i diritti relativi alla funzione Decisioni per le esperienze. [Ulteriori informazioni](../experience-decisioning/gs-experience-decisioning.md)
* **Regole di limitazione**: ora, in Decisione per le esperienze, è possibile aggiungere più regole di limitazione per un determinato elemento in Decisioni per le esperienze. Ciò offre un maggiore controllo sulla modalità di invio delle offerte. [Ulteriori informazioni](../experience-decisioning/items.md#capping)
* **Reporting**: ora puoi creare dashboard di reporting personalizzate delle campagne di Decisioni per le esperienze tramite [!DNL Customer Journey Analytics]. [Ulteriori informazioni](../experience-decisioning/cja-reporting.md)


<!--**Decision Management**

* **Multi-rule support** - You can now add up to 10 capping rules for a given offer in Decision Management. This allows you to increase the level of control over the way offers are sent.
* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->


**Canale e-mail**

<!--
* **List-unsubscribe** - Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. Refer to the following pages: [Email opt-out management](../email/email-opt-out.md#unsubscribe-header) and [Configure email settings](../email/email-settings.md#list-unsubscribe)
-->

* **Punteggio contenuto indesiderato** (beta): ora puoi controllare il punteggio del contenuto indesiderato in un rapporto relativo dedicato. Utilizzando SpamAssassin, Adobe Journey Optimizer può ora testare il contenuto delle e-mail e assegnargli un punteggio per indicare se gli ISP o i provider di caselle postali lo considereranno come contenuto indesiderato o meno. [Ulteriori informazioni](../content-management/spam-report.md)

  >[!AVAILABILITY]
  >
  >Questa funzionalità è disponibile attualmente in versione beta e solo per la clientela beta. Per partecipare al programma Beta, contatta il tuo rappresentante Adobe.

<!--
**Audiences**

* The use of audiences and attributes from audience composition and custom upload (CSV file) is now available for use with Healthcare Shield or Privacy and Security Shield.-->

<!--**Personalization**

* **Expression fragment** - Expression fragments are now available for the **In-app channel**. [Read more](../personalization/use-expression-fragments.md)-->

**Percorsi**

<!--* **Merge policies** (Limited Availability)- Merge policies used by a journey are now visible and consistent throughout the journey.-->
* **Supporto mTLS**: l’autenticazione mTLS è ora supportata nelle azioni personalizzate. Non è necessaria alcuna configurazione aggiuntiva nell’azione o nel percorso personalizzato per attivare mTLS; l’attivazione viene eseguita automaticamente quando viene rilevato un endpoint abilitato per mTLS. [Ulteriori informazioni](../action/about-custom-action-configuration.md#mtls-protocol-support)
* **Tabelle di ricerca negli eventi**: è ora possibile sfruttare i dati di un set di dati di ricerca quando una relazione è stata definita utilizzando un attributo all’interno di un array di oggetti. I valori di ricerca saranno disponibili nei percorsi (condizioni, azioni personalizzate, ecc.) e nella personalizzazione dei messaggi. [Ulteriori informazioni](../event/experience-event-schema.md#relationships_limitations)
* **Editor di espressioni avanzate nella configurazione dell’evento** (Disponibilità limitata): è ora possibile sfruttare l’editor di espressioni avanzate durante la configurazione di un evento, consentendoti di definire espressioni più complesse o utilizzare funzioni nella condizione per l’ID evento. Questa funzionalità viene rilasciata in Disponibilità limitata per clienti selezionati. [Ulteriori informazioni](../event/about-creating.md#adv-exp-editor)
* **Criteri di unione** (Disponibilità limitata): i criteri di unione utilizzati da un percorso sono ora visibili e coerenti in tutto il percorso. Questa funzionalità viene rilasciata in Disponibilità limitata per clienti selezionati. [Ulteriori informazioni](../building-journeys/journey-properties.md#merge-policies)

**Globalizzazione**

Come parte del nostro impegno continuo per offrire un’esperienza utente unificata, armonizziamo la terminologia utilizzata nei prodotti e nelle app di Adobe Experience Cloud. Questo influisce sul termine tedesco “Titel” che viene modificato in “Label” quando si riferisce al nome di un oggetto. Le modifiche verranno implementate progressivamente nell’interfaccia utente e nella documentazione.


## Versione di aprile 2024 {#apr-2024}

**Data di rilascio**: 2 maggio 2024

### Nuove funzionalità {#apr-features}

Questa versione include le nuove funzionalità elencate di seguito.

<table>
<thead>
<tr>
<th><strong>MMS (Multimedia Message Service): tutti i provider</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con il canale SMS, ora è possibile migliorare le comunicazioni inviando messaggi MMS (Multimedia Message Service), che consentono di condividere immagini, GIF o video con la clientela. Inizialmente disponibile solo con Sinch, la funzione MMS è ora disponibile anche con Infobip e Twilio.</p>
<img src="assets/do-not-localize/mms.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Designer del percorso e rapporti live migliorati</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Questa versione include un’interfaccia utente dell’area di lavoro migliorata per i percorsi e offre un’esperienza utente più intuitiva ed efficiente. Le attività sono più chiare e nell’area di lavoro del percorso è possibile ottenere più informazioni con meno clic.</p>
<img src="assets/new-canvas3.gif"/>
<p>Oltre al design migliorato dell’area di lavoro del percorso, è stata introdotta la possibilità di visualizzare le metriche di reporting delle ultime 24 ore direttamente nell’area di lavoro del percorso. </p>
<img src="assets/new-canvas6bis.png"/>
<p><strong>Nota</strong>: a partire dalla versione di aprile, queste modifiche verranno gradualmente implementate in tutti gli ambienti.</p>
<p>Per ulteriori informazioni, consulta la <a href="new-canvas.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<!-- table>
<thead>
<tr>
<th><strong>AI Assistant - Experience Variant Generation - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Once you have created and personalized your message, take your content to the next level with AI Assistant. You can now use AI Assistant to optimize your message's impact by experimenting with different main titles, and images. Each variant is managed as a unique Treatment, to measure and compare which title effectively generates more clicks.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Email Surface Personalization - Private beta </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now define dynamic subdomains and personalized header parameters when creating email channel configurations, for increased flexibility and control over your email settings.</p>
</td>
</tr>
</tbody>
</table-->

### Miglioramenti {#apr-improvements}

Questa versione include i miglioramenti elencati di seguito.

<!--
* **Expression Fragments supported for Web and In-App**: Expression fragments are now available for the Web and In-app channels. 
-->


<!--
* **DULE for AJO channel configuration**: It is now possible to apply a label on certain profile attributes to restrict their usage inside a channel configuration through marketing actions.
-->


<!--
* **List-Unsubscribe updates**: Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. 
-->

**Configurazione**

* Ora puoi selezionare un’azione di marketing al livello della configurazione dei canali. Se utilizzati in una configurazione, tutti i criteri di consenso associati a tale azione di marketing vengono usati per rispettare le preferenze della clientela. [Ulteriori informazioni](../action/consent.md#surface-marketing-actions)
* Per le configurazioni di canale è ora possibile utilizzare il controllo degli accessi a livello di oggetto. [Ulteriori informazioni](../configuration/channel-surfaces.md#create-channel-surface)
* Durante l’abilitazione dell’elenco di annullamenti dell’abbonamento in una configurazione di canale, ora puoi definire il livello di consenso per allinearlo a come gestisci il consenso da tutte le altre origini. [Ulteriori informazioni](../email/email-settings.md#list-unsubscribe)

**Gestione dei contenuti**

* Ora puoi simulare modelli di contenuto per tutti i canali. [Maggiori informazioni](../content-management/content-templates.md#video-templates)

**Personalizzazione**

* La nuova funzione helper **toInt** è disponibile nell’editor di espressioni. Ti consente di convertire uno qualsiasi di questi tipi (numero, doppio, int, lungo, mobile, corto, byte, booleano, stringa) in un numero intero. [Ulteriori informazioni](../personalization/functions/math.md#to-int)



## Versione di marzo 2024 {#mar-2024}

**Data di rilascio**: 19-20 marzo 2024

### Nuova funzionalità {#mar-features}

Questa versione include la nuova funzionalità descritta di seguito.

<table>
<thead>
<tr>
<th><strong>Esperienze basate su codice</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con il nuovo canale di esperienza basato su codice, Adobe Journey Optimizer consente di eseguire personalizzazioni e test avanzati per qualsiasi proprietà in entrata, facilitando la consegna diretta di esperienze personalizzate in diversi punti di contatto come app web, app mobili, app desktop, console video, dispositivi connessi per TV, smart TV, chioschi, sportelli bancomat, dispositivi IoT e altro ancora.</p>
<P>Le funzionalità principali includono:</p>
<ul><li> Personalizzazione universale: estende le esperienze personalizzate in tutti i punti di contatto, garantendo un percorso utenti coeso e personalizzato</li>
<li>Precisione granulare nella modifica: modifica contenuti specifici in singole posizioni all’interno delle app o delle pagine web</li>
<li>Implementazione versatile: supporto per metodi di implementazione lato server, basati su API o SDK per l’integrazione diretta con l’ambiente di sviluppo.</li></ul></p>
<p>Per ulteriori informazioni, consulta la <a href="../code-based/get-started-code-based.md">documentazione dettagliata</a>.</p>
<img src="assets/do-not-localize/code-based.gif"> 
</tr>
</tbody>
</table>

### Miglioramenti {#mar-improvements}

Questa versione include i miglioramenti elencati di seguito.

**Modelli di contenuto**

* **Miniature**: per i modelli di contenuto è ora disponibile la modalità **Vista a griglia**, in cui vengono visualizzate miniature dei modelli per agevolarne l’accesso visivo. Al momento sono supportati solo i modelli per e-mail HTML. [Ulteriori informazioni](../content-management/content-templates.md#template-thumbnails)

  >[!AVAILABILITY]
  >
  >Questa funzionalità viene rilasciata in Disponibilità limitata (LA) per un set limitato di clienti.

**Percorsi**

Sono stati aggiunti nuovi stati intermedi al ciclo di vita di authoring del percorso:

* Stato **Pubblicazione** tra gli stati **Bozza** e **Live**
* Stato **Interruzione** tra gli stati **Live** e **Interrotto**
* Stati **Attivazione modalità di test** o **Disattivazione modalità di test** tra gli stati **Bozza** e **Bozza (test)**

Quando un percorso si trova in uno stato intermedio, è di sola lettura. [Ulteriori informazioni](../building-journeys/journey-gs.md#filter)

## Versione di febbraio 2024 {#feb-2024}

**Data di rilascio**: 21-22 febbraio 2024

### Nuove funzionalità{#feb-features}

Questa versione include le nuove funzionalità elencate di seguito.


<table>
<thead>
<tr>
<th><strong>Messaggistica web in-app</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi utilizzare la nuova funzionalità di messaggistica web in-app per visualizzare contenuti personalizzati direttamente sui siti web tramite messaggi di sovrapposizione modale. Questa funzione consente di interagire in modo efficace con i visitatori web, migliorando l’interazione, la conservazione e i tassi di conversione degli utenti.<br/><br/></p>
<p>Per ulteriori informazioni, consulta la <a href="../in-app/create-in-app-web.md">documentazione dettagliata</a>.<br></br></p>
<img src="assets/do-not-localize/web_inapp.gif">
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Modelli di contenuto multicanale</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Oltre all’e-mail, ora sono disponibili modelli di contenuto per i seguenti canali: push, in-app, SMS e direct mail, ciascuno dei quali dispone di tipi di modello dedicati. Per l’e-mail, ora puoi selezionare il tipo di contenuto, che consente di salvare l’oggetto come parte del modello dell’e-mail. <br/><br/></p>
<p>Per ulteriori informazioni, consulta la <a href="../content-management/content-templates.md">documentazione dettagliata</a>.<br></br></p>
<img src="assets/do-not-localize/multi-chan-templates.gif"> 
</tr>
</tbody>
</table>


### Miglioramenti {#feb-improvements}

Questa versione include i miglioramenti elencati di seguito.

**Tipi di pubblico**

* **Elenchi seed**: quando si utilizzano gli **elenchi seed**, adesso sono supportate le varianti. Gli indirizzi seed ricevono una copia di tutte le varianti dello stesso messaggio (come i diversi trattamenti di un esperimento di contenuto). [Ulteriori informazioni](../configuration/seed-lists.md)

Precedentemente disponibili in versione beta, i seguenti miglioramenti sono ora disponibili per tutti gli utenti:

* Ora puoi eseguire il targeting dei **tipi di pubblico creati tramite la composizione del pubblico** e sfruttare gli attributi di arricchimento nei percorsi. [Ulteriori informazioni](../building-journeys/read-audience.md)

* Ora puoi eseguire il targeting di **tipi di pubblico caricati da un file CSV** nei percorsi e nelle campagne. [Ulteriori informazioni](../audience/about-audiences.md#about-segments)

  >[!AVAILABILITY]
  >
  >* L’utilizzo di tipi di pubblico e attributi dalla composizione del pubblico e dal caricamento personalizzato (file CSV) non è attualmente disponibile per l’utilizzo con Healthcare Shield o Privacy and Security Shield.
  >* Il miglioramento del **caricamento del pubblico da un file CSV** verrà introdotto gradualmente nel corso di alcuni giorni successivi alla versione iniziale. Mentre alcuni utenti hanno accesso immediato, altri potrebbero notare un ritardo prima che questo diventi disponibile nel loro ambiente.

**Percorsi**

* **Filtrare i percorsi**: è ora possibile utilizzare inventari di **date personalizzate per filtrare i percorsi**, oltre ai filtri di data predefiniti esistenti. Questo consente di perfezionare l’elenco visualizzando i percorsi creati o pubblicati in una data specifica, all’interno di un mese specifico, durante un anno intero o compresi in intervalli di tempo specifici. [Ulteriori informazioni](../building-journeys/journey-gs.md#filter)
* **Azioni personalizzate**: ora puoi aggiornare l’intestazione **content-type**. Questo nuovo **content-type** dovrebbe fare riferimento al contenuto JSON. [Ulteriori informazioni](../action/about-custom-action-configuration.md#url-configuration)
* **Configurazione**: l’attributo identityMap in stepEvents ora è precompilato. L’identità primaria è definita come “primary = true”. [Ulteriori informazioni](../reports/sharing-field-list.md)
* **Interfaccia utente**: la barra superiore, nelle schermate del percorso, è stata riorganizzata per offrire un’esperienza migliorata. Tra i diversi aggiornamenti, l’icona a forma di “matita” che consente di accedere alle proprietà del percorso è ora visualizzata a sinistra della barra superiore, accanto al nome del percorso. [Ulteriori informazioni](../building-journeys/journey-properties.md)

**Canale SMS**

* **Parole chiave di consenso/rinuncia**: durante la configurazione del canale SMS, ora puoi personalizzare le **parole chiave di consenso e rinuncia** in base alle tue preferenze. Journey Optimizer attiva la risposta in base a queste parole chiave specificate. [Ulteriori informazioni](../sms/sms-configuration.md)

**Campagne**

* **Campagne attivate da API**: è stato migliorato il codice cURL generato dopo l’attivazione di una campagna attivata da API. Ora include tutte le variabili di personalizzazione (profilo e contesto) utilizzate nel messaggio. [Ulteriori informazioni](../campaigns/api-triggered-campaigns.md#execute)

**Regole di frequenza**

* Oltre a e-mail e push, ora puoi creare regole di frequenza per i canali SMS e Direct Mail. Le regole di frequenza escludono automaticamente i profili sollecitati eccessivamente dai messaggi e dalle azioni quando viene raggiunta la quota limite. [Ulteriori informazioni](../conflict-prioritization/rule-sets.md)

<!--**Decision management**

* **Capping rules** - You can now add **multiple capping rules** for one offer. This allows you to increase the level of control over the way offers are sent.-->


## Versione di gennaio 2024 {#jan-2024}

**Data di rilascio**: 30-31 gennaio 2024

### Nuove funzionalità{#jan24-features}

Questa versione include le nuove funzionalità elencate di seguito.

<table>
<thead>
<tr>
<th><strong>Aggiornamenti del recapito dei messaggi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ora supporta la tecnologia di autenticazione DMARC.</p>
<p>A partire dal 1 febbraio 2024, Google e Yahoo richiedono di disporre di un record DMARC per qualsiasi dominio utilizzato per inviare loro e-mail. Assicurati di aver impostato il record DMARC per tutti i sottodomini che hai delegato o stai delegando ad Adobe in Journey Optimizer.</p>
<p>Per ulteriori informazioni, consulta la <a href="../configuration/dmarc-record-update.md">documentazione dettagliata</a>.</p>
<br/><img src="assets/do-not-localize/dmarc.gif"/>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Usare i playbook sui casi d’uso</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sfrutta un catalogo di playbook sui casi d’uso specifici del settore in Real-Time CDP e Journey Optimizer per risolvere casi d’uso comuni che è possibile eseguire utilizzando Adobe Experience Platform e Adobe Journey Optimizer.</p><p>Dopo aver scelto il playbook più adatto alle tue esigenze, puoi abilitarlo per generare le risorse necessarie per supportare il caso d’uso, ad esempio percorsi, messaggi, schemi o segmenti, e personalizzarle nel tuo schema per velocizzare il time-to-value.</p>
<p>Per ulteriori informazioni, consulta la <a href="../start/playbooks.md">documentazione dettagliata</a>.</p>
<br/><img src="assets/do-not-localize/playbooks.gif"/>
</tr>
</tbody>
</table>

### Miglioramenti {#jan24-improvements}

Questa versione include i miglioramenti elencati di seguito.

**Reporting**

* **Nuovi widget di raggruppamento basati su dominio**: sono stati aggiunti nuovi widget per migliorare i rapporti di Campaign e Journey. I widget **Motivi di mancato recapito per dominio**, **Inviato e consegnato da domini**, **Aperture e clic per dominio** e **Mancato recapito ed errori per dominio** forniscono un raggruppamento dettagliato a livello di dominio per le metriche chiave di consegna e tracciamento delle e-mail. [Ulteriori informazioni](../reports/channel-report-cja.md)

**Canale SMS**

* **Doppio consenso**: il flusso di lavoro do doppio consenso per SMS garantisce che gli utenti acconsentano esplicitamente alla ricezione di messaggi quando la richiesta viene avviata dal proprio dispositivo. Gli utenti avviano il processo di consenso inviando un messaggio SMS in entrata. Una volta confermato il consenso, viene inviato un messaggio di follow-up con la richiesta di verifica finale. Se un profilo utente non esiste, viene creato a conferma avvenuta correttamente. [Ulteriori informazioni](../sms/sms-configuration.md)

  Questa funzionalità è disponibile con i provider per SMS Sinch e Infobip.

**Percorsi**

* **Durata eventi di reazione** - La durata massima che puoi definire negli **eventi di reazione** è ora di 29 giorni anziché di 30. [Ulteriori informazioni](../building-journeys/reaction-events.md)

<!--* **Date filters** - You can now use custom dates to filter the journeys inventory, in addition to the existing predefined date filters. This allows you to refine the list by displaying journeys published on a specific date, within a particular month, throughout an entire year, or within specified time ranges. [Learn more](../building-journeys/journey-gs.md#filter)-->

* **Leggi pubblico**: l’attività **Leggi pubblico** ora si basa sul set di dati dello snapshot del profilo per i segmenti batch, che viene generato solo una volta al giorno dopo l’esecuzione del processo batch giornaliero pianificato, pertanto i dati verranno aggiornati fino all’ultimo processo batch giornaliero. [Ulteriori informazioni](../building-journeys/read-audience.md)

* **Gruppi di campi**: questa versione risolve un problema che in alcuni casi impediva il salvataggio dei gruppi di campi.

* Il supporto a `<listObject>` è stato modificato in più funzioni.

**Regole di frequenza**

* **Quota limite settimanale**: è ora possibile specificare il numero massimo di messaggi inviati a un profilo cliente in una settimana, oltre a quelli inviati in un mese. La quota limite si basa sul periodo di calendario selezionato e viene reimpostata all’inizio dell’intervallo di tempo corrispondente. [Ulteriori informazioni](../conflict-prioritization/rule-sets.md)

  >[!NOTE]
  >
  >Su richiesta, è disponibile anche l’opzione di quota limite giornaliera. Contatta il tuo rappresentante Adobe.

**Gestione delle decisioni**

* **Quota limite su Edge**: il contatore della quota limite ora è aggiornato e disponibile in una decisione API Edge Decisioning in meno di 3 secondi. [Ulteriori informazioni](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)
