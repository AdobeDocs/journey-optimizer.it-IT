---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
feature: Release Notes
topic: Content Management
description: Note sulla versione di Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 3ab4e6a7ff6c7e0ec97ee2021eb8b38e321b138c
workflow-type: tm+mt
source-wordcount: '1657'
ht-degree: 89%

---

# Note sulla versione {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novità"
>abstract="**Adobe Journey Optimizer** offre continuamente nuove funzioni, miglioramenti a quelle esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese."

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Tutte le modifiche sono consolidate nell’ultima settimana di ogni mese nelle presenti note sulla versione. [!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.

## Aggiornamenti di ottobre 2024 {#24-10-rn}

Prossima **data di rilascio**: 28-30 ottobre 2024

Le [funzionalità](#24-10-features) e [miglioramenti](#24-10-improvements) elencati di seguito sono stati rilasciati questo mese.

### Nuove funzionalità {#24-10-features}

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
<p>Data di disponibilità: 21 ottobre 2024</p>
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
<p>Il reporting di Journey Optimizer è ora generalmente disponibile (GA) e viene fornito con una migliore interoperabilità con funzionalità di Customer Journey Analytics, standardizzando il reporting su entrambe le piattaforme e migliorando la coerenza e l’affidabilità dei dati. Questa integrazione diretta tra Journey Optimizer e Customer Journey Analytics fornisce una visione più chiara delle metriche delle prestazioni e consente agli utenti di prendere decisioni più informate.</p>
<p>Con la disponibilità generale, vengono introdotte quattro nuove funzioni: la possibilità di creare metriche semplici, creare e pubblicare tipi di pubblico, porre domande ad hoc tramite Insight Builder e pianificare l’invio automatico via e-mail dei rapporti ai destinatari chiave.</p>
<p>Per ulteriori informazioni, consulta la <a href="../reports/report-cja-manage.md">documentazione dettagliata</a>.</p>
<img src="assets/do-not-localize/ajo-cja.gif">
<p>Data di disponibilità: 16 ottobre 2024</p>
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
<p>Data di rilascio: 1 ottobre 2024</p>
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
<p>Data di rilascio: 1 ottobre 2024</p>
</tr>
</tbody>
</table>

>[!IMPORTANT]
>
>L’esperienza di reporting corrente verrà ritirata a gennaio 2025. Dopo questa data, la nuova esperienza di reporting diventerà lo standard. Consigliamo di acquisire familiarità con le nuove funzioni e funzionalità per garantire una transizione semplice.
>
> [Scopri come iniziare a utilizzare la nuova interfaccia di reporting di Journey Optimizer](../reports/report-gs-cja.md)

### Miglioramenti {#24-10-improvements}

**Percorsi** - Data di disponibilità: 3 ottobre 2024

* **Parametri nelle azioni personalizzate**: i parametri NULL e facoltativi sono ora supportati nelle azioni personalizzate. [Ulteriori informazioni](../action/about-custom-action-configuration.md#define-the-message-parameters)

**Governance dei dati e criteri di consenso** - Data di disponibilità: 7 ottobre 2024

* L’applicazione dei **criteri di governance dei dati** ora avviene su tutti i canali in Journey Optimizer. Per coloro che hanno creato criteri in Adobe Experience Platform, questi vengono applicati alle azioni di marketing come parte dell’impostazione delle configurazioni dei canali. Durante la creazione dei contenuti tramite una configurazione, il sistema verifica tutti i campi di personalizzazione per individuare eventuali violazioni della governance dei dati. Se viene rilevata una violazione, non sarà possibile pubblicare un percorso o una campagna. [Ulteriori informazioni](../action/action-privacy.md)

* I **criteri di consenso personalizzati** ora si applicano a tutti i canali Journey Optimizer. Al momento dell’applicazione prima dell’invio di un messaggio o della consegna di un’esperienza in entrata, il sistema controlla che l’utente abbia dato il consenso all’utilizzo dei campi di personalizzazione nel contenuto che riceverà. Se non viene fornito alcun consenso, l’esperienza non sarà visualizzata. [Ulteriori informazioni](../action/consent.md)

  >[!NOTE]
  >
  >I criteri di consenso sono attualmente disponibili solo per le organizzazioni che hanno acquistato le offerte aggiuntive **Healthcare Shield** e **Privacy and Security Shield**.

**Tipi di pubblico** - Data di disponibilità: 8 ottobre 2024

* Quando esegui il targeting di un pubblico di un file CSV, ora puoi utilizzare gli attributi del file nell’editor di personalizzazione e nel generatore di regole per percorsi e campagne. [Ulteriori informazioni](../audience/about-audiences.md)

* L’utilizzo di tipi di pubblico e attributi da aggiornamenti personalizzati (file CSV) non è al momento disponibile per l’utilizzo con Healthcare Shield o Privacy and Security Shield.

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
<p>Per ulteriori informazioni, consulta la <a href="../content-card/get-started-content-card.md">documentazione dettagliata</a>.</p>
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
<p>I criteri di approvazione sono attualmente disponibili solo per alcune organizzazioni (disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
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
<th><strong>Accelerazione dei contenuti dell’Assistente IA </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Dopo aver creato e personalizzato il messaggio, porta il contenuto al livello successivo con l’Assistente AI Content Accelerator in Journey Optimizer. Ora puoi utilizzare l’Assistente AI per ottimizzare l’impatto del messaggio sperimentando diversi titoli principali e immagini. Ogni variante viene gestita come un trattamento univoco, per misurare e confrontare quale titolo genera effettivamente più clic.</p>
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


![Newsletter](../assets/do-not-localize/nl-icon.png) Iscriviti subito alla [newsletter trimestrale Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} e ricevi gli ultimi aggiornamenti dei prodotti, storie interessanti, casi d’uso, suggerimenti e altro ancora direttamente nella tua casella in entrata ogni trimestre.