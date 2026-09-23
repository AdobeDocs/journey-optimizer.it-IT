---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Note sulla versione di Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
TQID: https://experienceleague.adobe.com/YJKQFYUi8Kw7yZZKm8blcM-1G9uYsqcsEsopH0hOMhA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
    internal-label: Administration
subfeature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
    internal-label: Journey Optimizer release notes
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
    internal-label: Customer journeys
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 4f3312974e2533c97954e887b4371de6fc80595a
workflow-type: tm+mt
source-wordcount: '2079'
ht-degree: 21%
---
# Note sulla versione {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novità"
>abstract="**Adobe Journey Optimizer** offre in modo continuo nuove funzionalità, miglioramenti a quelle esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese."

[!DNL Adobe Journey Optimizer] segue un modello di distribuzione continua, che consente ad Adobe di fornire nuove funzionalità, miglioramenti e correzioni su base regolare. Questo approccio consente un rollout scalabile e graduale delle funzionalità per garantire prestazioni e stabilità in tutti gli ambienti. A causa di questo modello, le note sulla versione vengono aggiornate prima del successivo rilascio mensile. Per informazioni dettagliate sul ciclo di rilascio e sulle fasi di disponibilità, consulta [Ciclo di rilascio di Journey Optimizer](releases.md).

[!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche sono disponibili nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.

>[!NOTE]
>
>Le funzionalità elencate in queste note sulla versione includono una **Data di disponibilità** che indica quando ciascuna modifica diventa accessibile nel tuo ambiente. Le voci nei pannelli a soffietto **Disponibile a breve** sono previste nei prossimi giorni o settimane. Le informazioni in queste sezioni sono soggette a modifiche.

## Note sulla versione di settembre 2026 {#sep-26-updates}

### Gestione dei contenuti {#sep-26-content-management}

<table>
<thead>
<tr>
<th><strong>Strumenti MCP per la gestione dei contenuti in CX Collaborator</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>CX Coworker dispone ora di un nuovo set di <strong>strumenti MCP per la gestione dei contenuti</strong>, che consente di individuare e gestire le risorse di contenuti Journey Optimizer tramite prompt in linguaggio naturale. Chiedi di elencare o recuperare modelli di contenuto, frammenti, pagine di destinazione e contenuti di messaggi in linea di percorso/campagna. Può anche creare contenuti, aggiornare modelli e creare, aggiornare, clonare e pubblicare frammenti, nonché aggiornare il contenuto delle azioni del canale in linea direttamente nel percorso e nella campagna.</p>
<p>Per ulteriori informazioni, consulta la <a href="../content-management/content-management-coworker-skills.md#content-management">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 3 settembre 2026</p>
</td>
</tr>
</tbody>
</table>

* **Casella di controllo Consenso obbligatorio per le pagine di destinazione** - È ora possibile rendere obbligatoria una casella di controllo nel componente del modulo della pagina di destinazione, richiedendo ai visitatori di selezionarla (ad esempio, per dare il consenso) prima di poter inviare il modulo. [Ulteriori informazioni](../landing-pages/lp-content.md#use-form-component)

  Data di disponibilità: 4 settembre 2026

* **Altre parole chiave riservate nella sintassi di personalizzazione** - L&#39;elenco delle parole chiave riservate in Profile Query Language (PQL) è stato espanso per includere parole chiave generali, unità di tempo e operatori booleani/logici. Se lo schema XDM contiene un nome di campo che corrisponde a una di queste parole chiave, racchiudilo in apici per farvi riferimento in un’espressione di personalizzazione. [Ulteriori informazioni](../personalization/personalization-syntax.md#reserved-keywords)

  Data di disponibilità: 1 settembre 2026

### Fedeltà {#sep-26-loyalty}

<table>
<thead>
<tr>
<th><strong>Aggiornamenti alla mappatura degli eventi di fedeltà</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La creazione o la modifica di una mappatura degli eventi ora utilizza un nuovo **generatore di mappature visive**: seleziona uno schema, scegli i campi da un selettore di campi ricercabili, mappa ogni campo su un campo evento fedeltà con stato di connessione per riga e visualizza in anteprima l’espressione JSONata generata automaticamente, con l’opzione di passare alla modifica manuale di JSONata in qualsiasi momento.</p><p>Inoltre, le "Definizioni degli eventi" nell’amministratore Fedeltà sono state rinominate "Mappature eventi", con una vista a elenco aggiornata che mostra il nome dello schema dell’evento Esperienza leggibile dall’utente.</p>
<p>Per ulteriori informazioni, consulta la <a href="../loyalty-challenges/loyalty-admin.md#event-mappings">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 22 settembre 2026</p>
</td>
</tr>
</tbody>
</table>

* **Sfide di fedeltà &quot;per sempre&quot;** - Le sfide di fedeltà possono ora essere eseguite a tempo indeterminato. Imposta **Fine richiesta** su **Nessuna data di fine** durante la configurazione della pianificazione e la richiesta non scade mai. [Ulteriori informazioni](../loyalty-challenges/create-challenges.md#schedule)

  Data di disponibilità: 1 settembre 2026

* **Fedeltà disponibile per i clienti Healthcare Shield e Privacy and Security Shield** - Journey Optimizer Loyalty è ora disponibile per i clienti Healthcare Shield e Privacy and Security Shield. [Ulteriori informazioni](../loyalty-challenges/get-started.md)

  Data di disponibilità: 15 settembre 2026

+++ Disponibile a breve: **le informazioni riportate di seguito sono soggette a modifiche.**

* **Scadenze per il completamento della richiesta di fidelizzazione per membro** - Le sfide di fidelizzazione supportano ora le scadenze di completamento per membro: scegli &quot;Entro un numero di giorni dopo il consenso&quot; in Requisiti di completamento in modo che la scadenza di ogni membro venga calcolata dalla propria data di consenso anziché da una data di fine fissa a livello di programma. Se sono impostate sia una data di fine della sfida che questa finestra di consenso, la scadenza di ogni membro è quella che arriva per prima. <!-- Documentation link: TBD -->

+++

### Percorsi {#sep-26-journeys}

<table>
<thead>
<tr>
<th><strong>Simulazione percorso in Collaboratore</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L'abilità <strong>Simulazione Percorso</strong> in Coworker automatizza la convalida end-to-end del percorso e consente di interpretare facilmente i risultati. Questa funzione attualmente supporta solo il flusso di simulazione rapida e non sostituisce completamente l’esperienza di simulazione manuale di Journey Optimizer.</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/journeys-coworker-skills.md#journey-simulation">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 23 settembre 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Holdout a livello di percorso (disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi configurare un gruppo di holdout per i tuoi percorsi direttamente dalle proprietà del percorso. Un holdout è una percentuale configurabile del pubblico target che viene escluso dall’ingresso nel percorso e non riceve alcuna comunicazione. Confrontando i profili di holdout con quelli attivi nel reporting di Customer Journey Analytics, puoi misurare l’incremento (il vero impatto) fornito dal percorso.</p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe. Per informazioni dettagliate sul ciclo di rilascio e sulle fasi di disponibilità, consulta <a href="releases.md">Ciclo di rilascio di Journey Optimizer</a>.</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/journey-properties.md#performance-management">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 1 settembre 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Generare espressioni con IA nei percorsi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’editor di espressioni avanzate di percorso ora integra la generazione di espressioni basate sull’intelligenza artificiale: descrivi l’espressione da creare in linguaggio naturale e l’editor genera codice pronto all’uso che puoi applicare immediatamente o perfezionare tramite prompt di follow-up.</p>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/expression/generate-expression.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 1 settembre 2026</p>
</td>
</tr>
</tbody>
</table>


* **Supporto per le attività Salta nei percorsi di qualificazione del pubblico** - È ora possibile utilizzare le attività Salta nei percorsi che iniziano con un nodo di qualificazione del pubblico per passare ai percorsi basati su eventi. Questa funzionalità viene gradualmente implementata nelle organizzazioni. Se non lo vedi nel tuo ambiente, è possibile che tu stia ancora utilizzando i tipi di pubblico in batch nelle Qualifiche del pubblico. [Ulteriori informazioni](../building-journeys/jump.md)

  Data di disponibilità: 22 settembre 2026.

* **Attiva dopo la valutazione del pubblico in batch** - Per i percorsi ricorrenti che eseguono il targeting di tipi di pubblico in batch, puoi configurare una finestra di attesa di un massimo di 6 ore per una nuova valutazione in batch prima che il percorso venga eseguito. Se è in corso una valutazione, il percorso la attende per il completamento; se l’ultima istantanea è stata utilizzata dall’esecuzione precedente, attende un batch più recente. Se non è disponibile alcun nuovo pubblico entro la fine della finestra di attesa, tale occorrenza viene ignorata. [Ulteriori informazioni](../building-journeys/read-audience.md)

  Data di disponibilità: 18 settembre 2026

* **Decisioning nella simulazione del Percorso** - La sperimentazione del percorso, come parte dell&#39;attività **Ottimizza**, è ora supportata nella simulazione. L’instradamento viene gestito tramite Decisioning ed è casuale e non deterministico per ciascun utente simulato.

  [Ulteriori informazioni](../building-journeys/simulate-journey-gs.md)

  Data di disponibilità: 15 settembre 2026

* **Avviso di rilevamento anomalie del nuovo Percorso** - Un nuovo avviso di sistema ora avvisa quando il traffico giornaliero di un percorso attivo si scosta dalla propria linea di base cronologica o scende a zero in modo imprevisto tra le entrate del Percorso, le uscite dal Percorso e gli invii di eventi. Questo avviso è attualmente disponibile solo nelle sandbox di produzione.

  [Ulteriori informazioni](../reports/alerts.md)

  Data di disponibilità: 15 settembre 2026

* **Decisioning nella simulazione di Percorso** - È ora possibile simulare percorsi che si basano su Decisioning, con i seguenti elementi appena supportati:

  * I nodi di Content Decision sono ora supportati in Simulazione.
  * Il metodo della regola di targeting dell’attività Optimize è ora supportato in Simulazione.
  * Le azioni con contenuti decisionati da Adobe Journey Optimizer (ad esempio, e-mail che utilizzano un criterio di decisione) ora sono supportate nella simulazione.
  * I criteri di decisione che utilizzano l’idoneità per le offerte e la classificazione per regola, pubblico, priorità o formula sono completamente supportati. Classifica per modello di intelligenza artificiale: è supportato anche Personalization, anche se le offerte restituite possono variare tra le esecuzioni.

  [Ulteriori informazioni](../building-journeys/simulate-journey-gs.md)

  Data di disponibilità: 8 settembre 2026

* **Abilità Analizza anomalie Percorso** - CX Coworker è ora in grado di rilevare picchi, cadute o linee piatte imprevisti nei conteggi di entrata, uscita o invio di messaggi di un percorso rispetto alle linee di base storiche utilizzando l&#39;abilità **Analizza anomalie Percorso**. Una volta confermata una reale anomalia, l’abilità esegue una diagnostica di sola lettura per individuare una probabile causa principale e fornire consigli. [Ulteriori informazioni](../building-journeys/journeys-coworker-skills.md#journey-analyze)

  Data di disponibilità: 2 settembre 2026

* **Nuova funzione dateDiff nell&#39;editor espressioni di percorso**. L&#39;editor espressioni di percorso include ora la funzione `dateDiff`, che calcola la differenza tra due date in un numero di giorni. Questa funzione è utile per una logica basata sul tempo, ad esempio per creare scadenze, calcolare la durata del ciclo di vita del cliente o creare timer di conto alla rovescia in condizioni di percorso.  [Ulteriori informazioni](../building-journeys/functions/date-functions.md#dateDiff)

  Data di disponibilità: 1 settembre 2026

+++ Disponibile a breve: **le informazioni riportate di seguito sono soggette a modifiche.**

<table>
<thead>
<tr>
<th><strong>Anteprima del contenuto nell’area di lavoro del percorso</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La revisione del contenuto dei canali richiede oggi l’apertura di ogni attività singolarmente, una alla volta: lenta e soggetta a errori in percorsi con molte attività dei canali, soprattutto dove la personalizzazione significa controllare più trattamenti o varianti per attività. <strong>Anteprima contenuto</strong> rimuove tale attrito presentando una miniatura di contenuto per ogni attività di canale direttamente nell'area di lavoro, con una finestra modale a schermo intero per esaminare e passare da un trattamento all'altro e da una variante all'altra.</p>
<p>Data prevista di disponibilità: 28 settembre 2026</p>
</td>
</tr>
</tbody>
</table>

* **Abilità di analisi dell&#39;igiene** - CX Coworker ora può analizzare i percorsi attivi e in bozza per individuare configurazioni interrotte, errori silenziosi e risorse in declino o inutilizzate, ad esempio percorsi bozza non aggiornati, origini dati orfane ed errori persistenti di azioni personalizzate, oltre a trovare direttamente in chat le correzioni consigliate. <!-- Documentation link: TBD -->

+++

### Campagne {#sep-26-campaigns}

+++ Disponibile a breve: **le informazioni riportate di seguito sono soggette a modifiche.**

* **Cartelle per le campagne d&#39;azione** - È ora possibile organizzare le campagne d&#39;azione in cartelle per migliorare la navigazione e la gestione nell&#39;interfaccia.

* **Sostituisci i campi di esecuzione predefiniti nelle campagne Azione**. Precedentemente disponibili a livello di percorso, ora puoi sovrascrivere i campi di esecuzione predefiniti configurati a livello globale per le consegne e-mail, SMS e WhatsApp nei parametri della campagna Azione.

+++

### Campagne orchestrate {#sep-26-orchestrated-campaigns}

<table>
<thead>
<tr>
<th><strong>Avvisi per campagne orchestrate</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le campagne orchestrate ora supportano <strong>avvisi automatizzati</strong> tramite lo stesso framework di avvisi utilizzato nei percorsi e nelle campagne. Gli avvisi vengono attivati quando l’esecuzione di una campagna non riesce, si verifica un timeout e ogni avviso include ciò che è successo, quando, dove e un collegamento diretto all’area di lavoro per verificare ulteriori dettagli nei registri.</p>
<p>Per ulteriori informazioni, consulta la <a href="../orchestrated/start-monitor-campaigns.md#alerting">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 22 settembre 2026</p>
</td>
</tr>
</tbody>
</table>

* **Contenuto condizionale con dati relazionali in campagne orchestrate** - Durante la creazione di contenuto condizionale in E-mail Designer per campagne orchestrate, ora è possibile creare condizioni direttamente sui dati relazionali, ad esempio i record correlati associati a un profilo, non solo sugli attributi di profilo standard. [Ulteriori informazioni](../orchestrated/activities/channels.md#add-personalization)

  Data di disponibilità: 22 settembre 2026

### Formazione iniziale {#sep-26-onboarding}

In questa versione è disponibile il seguente miglioramento per l’onboarding.

<table>
<thead>
<tr>
<th><strong>Funzionalità guidate per e-mail e percorsi di onboarding</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le funzionalità guidate per l’onboarding di e-mail e percorsi includono ora i seguenti miglioramenti:</p>
<ul>
<li>Durante la migrazione di un'e-mail, [!DNL Journey Optimizer] identifica i blocchi di contenuto a cui fa riferimento l'e-mail e li espone come elementi di azione, in modo da poter eseguire la migrazione dei blocchi di contenuto insieme all'e-mail.</li>
<li>L’interfaccia è stata migliorata per rendere più intuitivo l’onboarding guidato.</li></ul>
<p>Per ulteriori informazioni, consulta la <a href="../start/onboarding-hub.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 2 settembre 2026</p>
</td>
</tr>
</tbody>
</table>

### Personalizzazione {#sep-26-personalization}

* **Correggi la sintassi con AI**: quando viene rilevato un errore di convalida della sintassi PQL, l&#39;editor di Personalization fornisce ora un&#39;opzione &quot;Correggi con AI&quot; per aiutare a risolvere il problema direttamente dall&#39;editor.

  Data di disponibilità: 22 settembre 2026

### Funzione Decisioni {#sep-26-decisioning}

<table>
<thead>
<tr>
<th><strong>Supporto per le decisioni nel canale web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>La funzione Decisioni è ora disponibile per il canale web. Puoi utilizzare i criteri di decisione direttamente nell’editor visivo per il web per fornire le offerte più rilevanti a chi visita il sito.</p>
<p>Per ulteriori informazioni, consulta la <a href="../experience-decisioning/use-decision-policy.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 22 settembre 2026</p>
</td>
</tr>
</tbody>
</table>

* **Supporto per i profili Adobe Experience Platform nella simulazione della formula di regole e classificazioni** - Durante la simulazione di una regola o di una formula di classificazione, è ora possibile selezionare un profilo Adobe Experience Platform per riempire automaticamente gli attributi di una variante di dati di test, anziché immetterli manualmente. [Ulteriori informazioni](../experience-decisioning/ranking/ranking-formulas.md#simulate-ranking-formula)

  Data di disponibilità: 22 settembre 2026

### Tipi di pubblico {#sep-26-audiences}

Il seguente promemoria si applica ai tipi di pubblico di questa versione.

* **Prossima modifica ai tipi di pubblico per l&#39;arricchimento della composizione del pubblico** - Durante la versione di ottobre (fine ottobre), Journey Optimizer interromperà i percorsi e le campagne che utilizzano o fanno riferimento a un pubblico per la composizione del pubblico il cui set di dati di origine non ha un **descrittore di identità primario**. Da quel momento in poi, solo i tipi di pubblico di Composizione del pubblico generati con un descrittore di identità principale sono supportati nei percorsi e nelle campagne. Se hai bisogno che questi percorsi o campagne rimangano attivi, contatta il tuo rappresentante Adobe: il nostro team di prodotto può aiutarti a migrare. <!-- Documentation link: TBD -->

### Amministrazione {#sep-26-administration}

Il seguente promemoria si applica all’amministrazione in questa versione.

* **Guardrail TTL (Time-to-live) del set di dati: sandbox esistenti**. Il guardrail TTL (time-to-live) per i set di dati generati dal sistema Journey Optimizer (90 giorni nell&#39;archivio dei profili, 13 mesi nel data lake) verrà applicato alle sandbox e alle organizzazioni dei clienti esistenti a partire dal 1° ottobre 2026.

### Miglioramenti dell’usabilità {#sep-26-usability}

* **Panoramica di IA negli avvisi di convalida dei frammenti** - La finestra di dialogo degli avvisi di convalida dei frammenti ora include una panoramica di IA che riepiloga e spiega i problemi di convalida (ad esempio espressioni non corrette, campi di profilo mancanti e JSON non valido) in modo che gli utenti possano risolvere più rapidamente i problemi.

  Data di disponibilità: 22 settembre 2026

* **È più semplice scollegare e unire rami nella nuova area di lavoro del percorso**. È ora possibile scollegare un ramo dal resto del percorso senza eliminarlo e unirlo di nuovo in un secondo momento in un punto diverso, selezionando un&#39;attività idonea direttamente nell&#39;area di lavoro o selezionandola da un elenco di rami disconnessi o già utilizzati. [Ulteriori informazioni](../building-journeys/using-the-journey-designer.md#join-and-detach-branches)

  Data di disponibilità: 1 settembre 2026

