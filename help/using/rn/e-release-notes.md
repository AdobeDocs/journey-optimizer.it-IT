---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
description: Note preliminari sulla versione di Journey Optimizer
feature: Release Notes
topic: Content Management
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 61447b6400b65e29a9187790e74be47b09764c4a
workflow-type: tm+mt
source-wordcount: '1967'
ht-degree: 98%

---

# Note preliminari sulla versione {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nell’ultima settimana di ogni mese, tutte le modifiche vengono consolidate nelle [note sulla versione](release-notes.md).

**Le note preliminari sulla versione riportate di seguito sono soggette a modifiche senza preavviso fino alla data di disponibilità della versione**. I collegamenti, le schermate e la documentazione aggiornata vengono pubblicati nelle [note sulla versione](release-notes.md), alla data di rilascio.

## Note preliminari sulla versione di ottobre 2024 {#e-2024}

**Data di rilascio**: 29-30 ottobre 2024

### Nuove funzionalità {#e-features}

Questa versione include le nuove funzionalità elencate di seguito.

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
<!--p>For more information, refer to the <a href="../content-management/gs-generative.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/ai-content.gif"/-->
</td>
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
<p>Precedentemente disponibile per un set di organizzazioni (LA), i criteri di approvazione sono ora disponibili per tutti gli utenti (GA).</p>
<p>Per ulteriori informazioni, consulta la <a href="../test-approve/gs-approval.md">documentazione dettagliata</a>.</p>
<img src="assets/do-not-localize/approval.gif"/>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Personalizzazione della configurazione e-mail (disponibilità generale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi definire sottodomini dinamici e parametri di intestazione personalizzati durante la creazione di configurazioni per il canale e-mail, per maggiore flessibilità e controllo sulle impostazioni e-mail.</p><p>L’utilizzo di una configurazione personalizzata in una campagna o in un percorso consente di visualizzare in anteprima il contenuto delle e-mail per verificare la presenza di potenziali errori con le impostazioni dinamiche definite.</p>
<p>Precedentemente disponibile per un set di organizzazioni (LA), la personalizzazione della configurazione e-mail è ora disponibile per tutti gli utenti (GA).</p>
<p>Per ulteriori informazioni, consulta la <a href="../email/surface-personalization.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Testare il contenuto utilizzando dati di input di esempio (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ora consente di testare diverse varianti del contenuto delle e-mail visualizzandolo in anteprima e inviando bozze utilizzando dati di input di esempio caricati da un file CSV o aggiunti manualmente. Tutti gli attributi dei profili utilizzati nel contenuto per la personalizzazione vengono rilevati automaticamente dal sistema e possono essere utilizzati per i test per creare più varianti.</p>
<p>Questa funzionalità è attualmente disponibile solo come versione Beta.</p>
<!--<p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p>-->
</td>
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
<p>In Journey Optimizer, gestire il volume e la tempistica delle campagne e dei percorsi è essenziale per evitare di sopraffare i clienti con troppe interazioni. Journey Optimizer offre ora diversi strumenti per la gestione dei conflitti e la definizione delle priorità.</p><p><ul><li><b>Quota limite percorsi</b>: ora è possibile creare set di regole da applicare ai tuoi percorsi, in modo da limitare il numero di percorsi per un profilo per giorno, settimana o mese, nonché controllare il numero di percorsi simultanei in esecuzione contemporaneamente.</li>
<li><b>Punteggio di priorità</b>: ora è possibile assegnare un punteggio di priorità, compreso tra 0 e 100, a una campagna o a un percorso. Un numero più alto indica una priorità più alta. Quando due campagne o azioni del percorso utilizzano la stessa configurazione dei canali, Journey Optimizer selezionerà quella con il punteggio di priorità più alto. Se le campagne hanno lo stesso punteggio, verrà scelta la campagna modificata meno di recente.</li>
<li><b>Visualizza conflitti potenziali</b>: un nuovo pulsante “Visualizza conflitti potenziali” nei percorsi e nelle campagne ora consente di identificare la sovrapposizione con altri percorsi o campagne, ad esempio la data di inizio, il pubblico di destinazione o la configurazione dei canali selezionata.</li>
<li><b>Journey Arbitration</b> (Arbitrato del percorso): questa nuova funzionalità consente di assegnare la priorità ai percorsi più importanti per i clienti. È possibile creare una regola per eliminare l’ingresso in un percorso con priorità inferiore quando un cliente si qualifica per un imminente percorso con priorità maggiore.</li></ul></p>
<!--<p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p>-->
<p>Le funzionalità di gestione dei conflitti e delle priorità sono disponibili in Disponibilità limitata per un gruppo selezionato di clienti. Tenere presente che queste funzioni verranno gradualmente implementate per più utenti in futuro. Se lo desideri, puoi rivolgerti al team del tuo account per l’inserimento nella lista d’attesa per queste funzioni.</p>

</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Modalità di modifica non visiva per il Designer web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In alternativa al Designer web di Journey Optimizer, ora è possibile aggiungere modifiche al sito web utilizzando un editor non visivo. Questo consente di inserire le modifiche manualmente senza aprire le pagine nell’editor visivo.
La modalità di modifica non visiva è utile se non è possibile installare estensioni del browser come Adobe Experience Cloud Visual Helper, necessarie per caricare le pagine nel Designer web.</p>
<!--p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p-->
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
<p>Precedentemente disponibile per un set di organizzazioni (LA), gli esperimenti nei percorsi sono ora disponibili per tutti gli utenti (GA).</p>
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
<p>La funzione Decisioni, precedentemente disponibile per un set di organizzazioni (LA) e nota come Decisioni per le esperienze, è ora disponibile per tutti gli utenti (GA). La funzione Decisioni semplifica la personalizzazione proponendo un catalogo centralizzato di offerte di marketing note come “elementi decisionali” e un motore decisionale sofisticato. Questo motore sfrutta le regole e i criteri di classificazione per selezionare e presentare a ogni persona gli elementi decisionali più rilevanti. Questi elementi decisionali sono integrati direttamente in un’ampia gamma di superfici in entrata tramite il canale di esperienza basato su codice.</p>

<p>Per il momento, la funzione Decisioni non è disponibile per le organizzazioni che hanno acquistato le offerte aggiuntive Healthcare Shield e Privacy and Security Shield di Adobe.</p>

<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Set di regole (disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora è possibile creare regole granulari per la quota limite e applicarle ai messaggi o ai percorsi tramite set di regole. Questa nuova funzionalità consente di controllare la frequenza con cui i tipi di pubblico ricevono un messaggio, impostando regole cross-channel che escludono automaticamente da messaggi e azioni i profili sollecitati eccessivamente.</p><p>Consente inoltre di limitare il numero di percorsi al giorno, alla settimana o al mese e di controllare il numero di percorsi simultanei in esecuzione contemporaneamente.</p>
<p>I set di regole sono accessibili in Disponibilità limitata per un gruppo selezionato di clienti. Tenere presente che queste funzioni verranno gradualmente implementate per più utenti in futuro. Se lo desideri, puoi rivolgerti al team del tuo account per l’inserimento nella lista d’attesa per questa funzione.</p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
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
<p>Grazie alla disponibilità generale, i contenuti multilingue sono ora accessibili su tutti i canali. </p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
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
<li>Accelerare i flussi di lavoro dei professionisti per i clienti di Journey Optimizer che utilizzano Da Vinci per l’authoring e AJO per l’ottimizzazione e la consegna</li>
<li>Ottimizzare i modelli Da Vinci con dati Adobe.</li></ul></p>
<!--p>For more information, refer to the <a href="../code-based/get-started-code-based.md">detailed documentation</a>.</p-->
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
<p>Disponibile dal 16 ottobre 2024</p>
<p>La funzione di reporting di Journey Optimizer, ora in disponibilità generale (GA), include una migliorata interoperabilità con le funzionalità di Customer Journey Analytics, per standardizzare il reporting su entrambe le piattaforme e migliorare la coerenza e l’affidabilità dei dati. Questa integrazione ottimizzata tra Journey Optimizer e Customer Journey Analytics consente una visione più chiara delle metriche delle prestazioni, in modo che gli utenti possano prendere decisioni più informate.</p>
<p>Con la disponibilità generale, vengono introdotte quattro nuove funzioni: la possibilità di creare metriche semplici, creare e pubblicare tipi di pubblico, porre domande ad hoc tramite Insight Builder e pianificare l’invio automatico via e-mail dei rapporti ai destinatari chiave.</p>
<p>Per ulteriori informazioni, consulta la <a href="../reports/report-cja-manage.md">documentazione dettagliata</a>.</p>
<img src="assets/do-not-localize/ajo-cja.gif">
<p>Importante: l’esperienza di reporting corrente verrà ritirata a partire da gennaio 2025. Dopo questa data, la nuova esperienza di reporting diventerà lo standard. Consigliamo di acquisire familiarità con le nuove funzioni e funzionalità per garantire una transizione semplice. <a href="../reports/report-gs-cja.md">Scopri come iniziare a utilizzare la nuova interfaccia di reporting di Journey Optimizer</a></p>
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
<p>Disponibile dal 1 ottobre 2024</p>
<p>Con il canale di esperienza basato su codice, Adobe Journey Optimizer consente di eseguire personalizzazioni e test avanzati per qualsiasi proprietà in entrata, facilitando la consegna diretta di esperienze personalizzate in diversi punti di contatto come app web, app mobili, app desktop, console video, dispositivi connessi per TV, smart TV, chioschi, sportelli bancomat, dispositivi IoT e altro ancora. Il canale di esperienza basata su codice è ora disponibile nell’area di lavoro del percorso.</p>
<p>Per ulteriori informazioni, consulta la <a href="../code-based/create-code-based.md">documentazione dettagliata</a>.</p>
<img src="../assets/do-not-localize/code-based-journey.gif"/>
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
<p>Disponibile dal 1 ottobre 2024</p>
<p>Con il canale web, Adobe Journey Optimizer ti consente di personalizzare l’esperienza web che fornisci alla clientela tramite percorsi web in entrata. Il canale web è ora disponibile nell’area di lavoro del percorso.</p>
<p>Per ulteriori informazioni, consulta la <a href="../web/create-web.md">documentazione dettagliata</a>.</p>
<img src="../assets/do-not-localize/web-journey.gif"/>
</tr>
</tbody>
</table>

### Miglioramenti {#e-improvements}

Questa versione include i miglioramenti elencati di seguito.

**Canale SMS**

>[!AVAILABILITY]
>
>I seguenti miglioramenti sono disponibili solo con i provider Sinch e Infobip.

Sono stati introdotti miglioramenti agli SMS per ottimizzare le funzionalità di messaggistica:

* È possibile definire e gestire parole chiave univoche per le campagne e i percorsi SMS, consentendo una comunicazione più personalizzata ed efficiente.

* È possibile creare e inviare un messaggio SMS predefinito quando una parola chiave non viene riconosciuta.

* Ora è possibile modificare o eliminare una configurazione dei canali API SMS.

<!--**Journeys**-->

<!--* **Path experiment in journeys** - With the journey path experiment, you can now define and track key metrics for your journey paths, allowing you to measure the impact of your activities and to provide clearer insights into your performance. -->

<!--* **Max number of Live journeys** - Journey Optimizer now has a guardrail of 500 live journeys on production sandboxes, instead of 100. The number of live journeys is visible in the journey canvas. (DOCAC-10977) -->

**Set di dati**

* **Guardrail time-to-live (TTL)**: a partire dal 1° novembre 2024, un guardrail time-to-live verrà introdotto nei set di dati generati dal sistema Journey Optimizer in nuove sandbox e nuove organizzazioni come segue:

   * 90 giorni per i dati nell’archivio dei profili
   * 13 mesi per i dati nel data lake

  In una fase successiva, questa modifica verrà implementata nelle sandbox della clientela esistente.

  Inoltre, dal 1° novembre la segmentazione in streaming non supporterà più l’utilizzo di eventi di invio e apertura dai set di dati di tracciamento e feedback. Da quel momento, questa modifica verrà applicata a tutte le sandbox e organizzazioni della clientela. [Ulteriori informazioni](../data/datasets-ttl.md)

* **Parametri nelle azioni personalizzate** (data di disponibilità 3 ottobre 2024): i parametri NULL e facoltativi sono ora supportati nelle azioni personalizzate. [Ulteriori informazioni](../action/about-custom-action-configuration.md#define-the-message-parameters)

**Generazione rapporti**

* È ora disponibile il reporting di **Decisioning**, che offre informazioni essenziali su come i visitatori interagiscono con le esperienze.

**Governance dei dati e criteri di consenso** - Data di disponibilità: 7 ottobre 2024

* L’applicazione dei **criteri di governance dei dati** ora avviene su tutti i canali in Journey Optimizer. Per coloro che hanno creato criteri in Adobe Experience Platform, questi vengono applicati alle azioni di marketing come parte dell’impostazione delle configurazioni dei canali. Durante la creazione dei contenuti tramite una configurazione, il sistema verifica tutti i campi di personalizzazione per individuare eventuali violazioni della governance dei dati. Se viene rilevata una violazione, non sarà possibile pubblicare un percorso o una campagna. [Ulteriori informazioni](../action/action-privacy.md)

* I **criteri di consenso personalizzati** ora si applicano a tutti i canali Journey Optimizer. Al momento dell’applicazione prima dell’invio di un messaggio o della consegna di un’esperienza in entrata, il sistema controlla che l’utente abbia dato il consenso all’utilizzo dei campi di personalizzazione nel contenuto che riceverà. Se non viene fornito alcun consenso, l’esperienza non sarà visualizzata. [Ulteriori informazioni](../action/consent.md)

  >[!NOTE]
  >
  >I criteri di consenso sono attualmente disponibili solo per le organizzazioni che hanno acquistato le offerte aggiuntive **Healthcare Shield** e **Privacy and Security Shield**.

**Tipi di pubblico** - Data di disponibilità: 8 ottobre 2024

* Quando esegui il targeting di un pubblico di un file CSV, ora puoi utilizzare gli attributi del file nell’editor di personalizzazione e nel generatore di regole per percorsi e campagne. [Ulteriori informazioni](../audience/about-audiences.md)

* L’utilizzo di tipi di pubblico e attributi da aggiornamenti personalizzati (file CSV) non è al momento disponibile per l’utilizzo con Healthcare Shield o Privacy and Security Shield.

**Canale basato su codice**

* Sono ora disponibili modelli di contenuto. È possibile accelerare la creazione delle esperienze basate sul codice partendo da un modello di contenuto creato dagli sviluppatori. L’utilizzo di un modello di contenuto consente ai marketer di modificare solo alcuni valori o campi, invece di comporre l’intero payload di contenuto HTML o JSON.

**Funzione decisioni**

Gli utenti di [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=it) possono ora scegliere modelli personalizzati per l’ottimizzazione durante la configurazione di un modello di intelligenza artificiale nella funzione Decisioni (precedentemente nota come Decisioni per le esperienze). Questo consente, ad esempio, di ottimizzare una tabella “acquisti” personalizzata, anziché i vincoli definiti come il tasso di clickthrough.
