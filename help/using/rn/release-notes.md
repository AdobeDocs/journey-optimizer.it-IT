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
source-git-commit: 0633e402cc52ee1cd6c4b7a74c4a57ee5ac33b39
workflow-type: tm+mt
source-wordcount: '4900'
ht-degree: 14%
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

>[!BEGINSHADEBOX]

**Novità di CX Enterprise Coworker questo mese**

Questa versione include diverse funzionalità e abilità [Collaboratore](../start/ai-features.md#cx-coworker) nuove e migliorate, elencate qui per la visibilità. Ognuna di esse è descritta anche nella sezione pertinente riportata di seguito.

* [Plug-in per contenuto canale CE](#sep-26-content-management): nuovo plug-in che riunisce in Coworker le competenze relative a copia, immagine ed e-mail di Campaign, dalla descrizione della campagna alla copia pronta per la produzione e a HTML.
* [Strumenti MCP per la gestione dei contenuti](#sep-26-content-management) - Rileva e gestisci modelli di contenuto, frammenti, pagine di destinazione e contenuti di messaggi in linea tramite messaggi in linguaggio naturale in Coworker.
* [Simulazione Percorso](#sep-26-journeys) - Automatizza la convalida del percorso end-to-end e interpreta i risultati direttamente in Coworker.
* [Confronta versioni di percorso](#sep-26-journeys) - Ottieni un diff strutturato e a piena fedeltà tra due versioni di un percorso tramite Chat con collaboratori.
* [Analisi delle anomalie del Percorso](#sep-26-journeys) - Rilevamento di picchi, cadute o linee piatte imprevisti nei conteggi di entrata, uscita o invio di messaggi di un percorso, con diagnostica della root cause.
* [Abilità di decisioning Explainer](#sep-26-decisioning) - Chiedi al tuo collega perché è stata mostrata o meno un&#39;offerta specifica a un profilo o a un segmento e ottieni una traccia completa delle esclusioni di idoneità, classificazione e regole.
* [Regole e abilità di classificazione](#sep-26-decisioning) - Crea, spiega, simula e ottimizza le regole di idoneità Decisioning e le formule di classificazione in linguaggio naturale, senza scrivere o convalidare manualmente la sintassi PQL.

+++ Disponibile a breve: **le informazioni riportate di seguito sono soggette a modifiche.**

* Creazione di [Percorsi dalla barra di Coworker](#sep-26-journeys): genera percorsi con IA direttamente dalla barra di Coworker a destra, sostituendo la precedente esperienza di Assistente IA.
* [Abilità per consigli sulla fedeltà](#sep-26-loyalty) - Richiedi opportunità di verifica direttamente nell&#39;interfaccia conversazionale di Coworker e trasformale in una sfida dal vivo senza uscire dalla chat.
* [Abilità di analisi dell&#39;igiene](#sep-26-journeys) - Analizza i percorsi attivi e in bozza per individuare configurazioni non funzionanti, errori silenziosi e risorse inutilizzate o in declino, con correzioni consigliate.
* [Competenza nell&#39;analisi delle prestazioni aziendali](#sep-26-journeys) - Analizza le prestazioni del percorso e ottieni consigli concreti sull&#39;ottimizzazione direttamente dalla chat.

+++

>[!ENDSHADEBOX]

### Gestione dei contenuti {#sep-26-content-management}

In questa versione, la seguente funzionalità verrà implementata per la gestione dei contenuti.

<table>
<thead>
<tr>
<th><strong>Plug-in Contenuto canale in Collaboratore</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In Coworker è ora disponibile un nuovo plug-in <strong>Contenuto canale</strong> che riunisce le abilità di copia, immagine e HTML e-mail per la campagna in un unico plug-in, dalla strategia alla distribuzione. Le seguenti abilità sono disponibili nel plug-in <b>Contenuto canale</b>:</p>
<ul>
<li><strong>Orchestrare l'authoring dei contenuti</strong>.</li>
<li><strong>Esplora strategia dei contenuti</strong></li>
<li><strong>Riepilogo contenuti</strong></li>
<li><strong>Generazione di contenuti</strong></li>
<li><strong>Verifica preparazione contenuto</strong></li>
<li><strong>Revisione e rigenerazione del contenuto</strong></li>
<li><strong>Genera immagine</strong></li>
<li><strong>Valuta progettazione contenuto</strong></li>
<li><strong>Salva contenuto canale</strong></li>
<li><strong>Crea e-mail da Figma</strong></li>
<li><strong>Ricerca marchio</strong> </li>
</ul>
<p>Per ulteriori informazioni, consulta la <a href="../content-management/content-management-coworker-skills.md#content-management#ce-channel-content">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 24 settembre 2026</p>
</td>
</tr>
</tbody>
</table>


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

+++ Disponibile a breve: **le informazioni riportate di seguito sono soggette a modifiche.**

* **Convalida URL in Simula contenuto** - Quando visualizzi l&#39;anteprima del contenuto, Journey Optimizer ora controlla automaticamente i collegamenti Web in esso contenuti e contrassegna gli URL interrotti, non sicuri o non raggiungibili prima dell&#39;invio. Questa funzionalità è in disponibilità limitata per una parte della clientela.

+++

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

<table>
<thead>
<tr>
<th><strong>Consigli sulle sfide</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Il menu Prestazioni fedeltà ora include schede **Opportunità** e **Tendenza**, che presentano tendenze e lacune rilevate dall’intelligenza artificiale, come l’attrito per progressione del livello o l’abbandono delle attività di sfida, ciascuna con un impatto previsto e un’azione "Crea con intelligenza artificiale" con un solo clic per generare una sfida che la soddisfi.</p><p>Inoltre, gli esperti di marketing possono richiedere **opportunità di sfida** direttamente nell’interfaccia conversazionale di Coworker, ottenendo idee basate su vere e proprie tendenze di programmi fedeltà e trasformandole in sfide live senza uscire dalla chat.</p>
</td>
</tr>
</tbody>
</table>

* **Scadenze per il completamento della richiesta di fidelizzazione per membro** - Le sfide di fidelizzazione supportano ora le scadenze di completamento per membro: scegli &quot;Entro un numero di giorni dopo il consenso&quot; in Requisiti di completamento in modo che la scadenza di ogni membro venga calcolata dalla propria data di consenso anziché da una data di fine fissa a livello di programma. Se sono impostate sia una data di fine della sfida che questa finestra di consenso, la scadenza di ogni membro è quella che arriva per prima. <!-- Documentation link: TBD -->

* **Sfide del dominio nell&#39;editor di personalizzazione della scheda di contenuto** - L&#39;editor di personalizzazione della scheda di contenuto ora supporta **Sfide** come dominio, consentendo l&#39;accesso ai metadati della richiesta di verifica durante l&#39;authoring della personalizzazione della scheda di contenuto. In questo modo è più facile creare contenuti personalizzati per ogni fase di una sfida, ovvero lancio, in corso e fine, senza codice personalizzato.

+++

### Percorsi {#sep-26-journeys}

<table>
<thead>
<tr>
<th><strong>Confronta versioni di percorso con Collaboratore</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Oggi, per rivedere ciò che è cambiato tra due versioni di un percorso è necessario confrontarle manualmente all'interno di Journey Optimizer nodo per nodo. Non esiste alcuna differenza strutturata, il che rende i controlli di revisione delle modifiche, di audit e pre-pubblicazione lenti e soggetti a errori, soprattutto in un momento in cui i percorsi diventano più complessi. Questa funzionalità consente a un cliente o a un agente di IA di confrontare due versioni qualsiasi di un percorso tramite Chat di Coworker e restituire una **diff strutturata** a piena fedeltà: nodi aggiunti/rimossi/modificati/spostati con dettagli a livello di campo, connessioni modificate, modifiche delle proprietà a livello di percorso e conteggi di rollup, senza aprire Journey Optimizer. </p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/journeys-coworker-skills.md#journey-analyze">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 24 settembre 2026</p>
</td>
</tr>
</tbody>
</table>

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
<th><strong>Schede di consigli AI per gli avvisi di percorso</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Nella home page di Journey Optimizer viene ora visualizzata una <strong>scheda di consigli AI</strong> quando viene attivato un avviso di percorso che copre <strong>l'errore di un'azione personalizzata di Percorso</strong> e <strong>gli avvisi di Percorso per anomalie</strong>. Selezionando la scheda si apre il percorso con la barra destra precompilata con l’analisi già eseguita.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Attività in entrata Attività del percorso di disattivazione</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Una nuova attività <strong>Inbound Activity Deactivation</strong> nell'area di lavoro del percorso consente di rimuovere un profilo da un massimo di cinque attività o esperienze in entrata direttamente da un percorso, separando l'interdizione in entrata dall'uscita dal percorso per un'orchestrazione cross-channel più avanzata.</p>
</td>
</tr>
</tbody>
</table>

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

<table>
<thead>
<tr>
<th><strong>Creazione di percorsi dalla barra di Collaboratore</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La creazione di <strong>Percorsi con IA</strong> è ora disponibile direttamente dalla barra laterale destra di Coworker, sostituendo la precedente esperienza di AI Assistant con un punto di ingresso integrato e modificato per la generazione di percorsi.</p>
</td>
</tr>
</tbody>
</table>

* **Abilità di analisi dell&#39;igiene** - CX Coworker ora può analizzare i percorsi attivi e in bozza per individuare configurazioni interrotte, errori silenziosi e risorse in declino o inutilizzate, ad esempio percorsi bozza non aggiornati, origini dati orfane ed errori persistenti di azioni personalizzate, oltre a trovare direttamente in chat le correzioni consigliate. <!-- Documentation link: TBD -->

* **Supporto di ID supplementari nella simulazione di Percorso** - **L&#39;ID supplementare** è ora supportato nella simulazione di Percorso, consentendo di testare scenari utente complessi sia per i percorsi di pubblico di lettura che per quelli attivati da eventi.

* **Eliminazione step-event esecuzione di prova per rapporti personalizzati** - Nell&#39;ambito dell&#39;ottimizzazione step-event, Journey Optimizer ora interrompe la generazione di alcuni eventi di passaggio non segnalabili durante le esecuzioni di Percorso. Questo influisce solo sui rapporti personalizzati basati su questi tipi di eventi step a esecuzione ininterrotta. Se siete interessati, riattivate l&#39;esecuzione di prova per rigenerare i dati.

* **Timeout del ripristino automatico degli eventi nelle proprietà del Percorso** - Le proprietà del Percorso ora includono un&#39;impostazione **Imposta timeout ripristino evento**: per impostazione predefinita, gli eventi di percorso interessati vengono riprodotti automaticamente fino a 72 ore dopo un&#39;interruzione del servizio senza che sia necessaria alcuna azione. È possibile attivare questa impostazione per controllare la finestra di ripetizione (0-72 ore) per i percorsi sensibili al tempo. Anche il campo **Timeout o errore** esistente è stato rinominato in **Azione personalizzata/Timeout origine dati** per evitare confusione tra le due impostazioni.

* **Eventi di passaggio ridotti per le attività attendi ed eventi** - Gli eventi di passaggio non vengono più generati per le attività **attendi** e **evento** quando il profilo non è stato effettivamente elaborato in tale attività.

+++

### Campagne {#sep-26-campaigns}

+++ Disponibile a breve: **le informazioni riportate di seguito sono soggette a modifiche.**

* **Cartelle per le campagne d&#39;azione** - È ora possibile organizzare le campagne d&#39;azione in cartelle per migliorare la navigazione e la gestione nell&#39;interfaccia.

* **Sostituisci i campi di esecuzione predefiniti nelle campagne Azione**. Precedentemente disponibili a livello di percorso, ora puoi sovrascrivere i campi di esecuzione predefiniti configurati a livello globale per le consegne e-mail, SMS e WhatsApp nei parametri della campagna Azione.

+++


### Canali {#sep-26-channels}

In questa versione sono disponibili le seguenti funzionalità e miglioramenti per i canali.

+++ Disponibile a breve: **le informazioni riportate di seguito sono soggette a modifiche.**

<table>
<thead>
<tr>
<th><strong>Canale in uscita personalizzato (disponibilità generale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Canali in uscita personalizzati</strong> consentono agli amministratori di portare qualsiasi canale di messaggistica in uscita basato su HTTP, ad esempio WeChat, Kakao Talk, Messenger o un provider proprietario, direttamente in Journey Optimizer tramite un Channel Builder senza codice. Una volta configurati, i canali personalizzati sono disponibili in tutte le campagne, i percorsi e le campagne orchestrate, con lo stesso set completo di funzionalità dei canali nativi: personalizzazione con l’editor di espressioni, sperimentazione dei contenuti, anteprima e bozza, reporting predefinito e applicazione delle norme in materia di consenso e governance.</p>
<p>Con questa versione, i canali in uscita personalizzati acquisiscono anche diverse nuove funzionalità:</p>
<ul>
<li>Utilizza Journey Optimizer Decisioning nel payload del canale personalizzato tramite Personalization Editor, come nelle esperienze basate su codice.</li>
<li>Applica le regole business ai canali personalizzati nello stesso modo in cui già puoi farlo sui canali nativi.</li>
<li>Seleziona i canali personalizzati nell’elenco dei canali per le campagne attivate da API, operazione che in precedenza non era possibile.</li>
<!--<li>Define a reporting webhook for a custom channel and attach it to a channel configuration, so you can enrich your Journey Optimizer reports with interaction events.</li>-->
</ul>
<p>Precedentemente disponibile in Disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (Disponibilità generale), con i miglioramenti descritti in precedenza.</p>
<p><img src="assets/do-not-localize/custom-channel.gif"></p>
<p>Per ulteriori informazioni, consulta la <a href="../custom-channel/get-started-custom-channel.md">documentazione dettagliata</a>.</p>

</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Attività live per Android Live Updates</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ora amplia le funzionalità di personalizzazione mobile in tempo reale estendendo il supporto di <strong>Attività live ad Android</strong>. Puoi fornire aggiornamenti sull’avanzamento in tempo reale direttamente agli utenti, ad esempio tracciamento degli ordini, stati dei voli, aggiornamenti degli eventi live e punteggi sportivi in tempo reale.</p>
<p>Oltre a supportare le attività di iOS Live, Journey Optimizer ora gestisce i token push temporanei per Android Live Updates sulle diverse configurazioni della piattaforma. Supporta sia i flussi di aggiornamento broadcast che quelli transazionali utilizzando campagne attivate da API e API headless.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Miglioramenti ai modelli di notifiche push in Android</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le notifiche push di Android venivano sottoposte in precedenza a rendering con un layout singolo e fisso: le immagini venivano sempre ritagliate al centro e il corpo del testo lungo veniva troncato. Questa versione introduce un selettore di modelli al momento dell’authoring, consentendo agli addetti al marketing di controllare il layout delle notifiche push di Android.</p>
<p>Sono disponibili i seguenti miglioramenti:</p>
<ul>
<li><b>Selezione layout</b>: nuovo selettore layout notifiche push (standard/espanso) durante la creazione di un messaggio push Android.</li>
<li><b>Layout standard con "Mostra intera immagine"</b>: scegliere ritagliata per riempire e ridimensionata per adattarla.</li>
<li><b>Layout espanso</b>: testo del corpo multiriga senza troncamento e miniatura opzionale con icona grande.</li>
<li><b>Corpo compresso (layout espanso)</b>: impostare un corpo di testo separato e più breve per lo stato compresso.</li>
</ul>
</td>
</tr>
</tbody>
</table>

* **Flessibilità di autenticazione BYOP SMS personalizzato** - È ora possibile configurare **intestazioni di autenticazione personalizzate** durante la connessione della configurazione OAuth del provider SMS, tra cui la posizione del token nei messaggi in uscita e la formattazione della richiesta del token.

* **Direct mailing - Dividi automaticamente i file di grandi dimensioni** - I file Direct mailing ora possono essere suddivisi in più parti automaticamente quando superano i 20 GB circa, oppure manualmente scegliendo una dimensione di file di destinazione nella configurazione di indirizzamento dei file.

* **Direct mailing - Limite di pubblico aumentato** - Il limite di pubblico del canale Direct mailing è stato aumentato da 3 milioni a 100 milioni di profili, consentendoti di rivolgerti a un pubblico molto più ampio senza riscontrare errori di creazione dei file.

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

* **Join diretti su raccolte in Campagne orchestrate** - Quando si aggiunge un attributo da una raccolta correlata, è ora possibile scegliere tra tre modalità di join, una nuova impostazione predefinita che segnala il potenziale impatto sulle prestazioni dei prodotti cartesiani, oltre alle modalità Aggregate e Avanzate esistenti, per semplificare la comprensione dei compromessi della query prima di generarla. [Ulteriori informazioni](../orchestrated/build-query.md#links)

  Data di disponibilità: 22 settembre 2026

+++ Disponibile a breve: **le informazioni riportate di seguito sono soggette a modifiche.**

<table>
<thead>
<tr>
<th><strong>O partecipa all’attività per campagne orchestrate</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L'attività <strong>Join</strong> nelle campagne orchestrate ora supporta sia le condizioni di join AND che OR. Con la logica OR, un profilo che completa un singolo ramo a monte, anziché tutti, continua lungo un singolo percorso a valle condiviso. Questo rende possibile modellare "se A o B o C, quindi fai questo" pattern direttamente sull’area di lavoro senza duplicare i passaggi a valle tra rami separati.</p>
</td>
</tr>
</tbody>
</table>

* **Canale LINE per campagne orchestrate** - LINE è ora disponibile come canale nativo in uscita nelle campagne orchestrate, insieme a e-mail, SMS e push. Puoi creare e inviare messaggi LINE direttamente dall’area di lavoro della campagna, inclusi testo, adesivi, immagini, video, dati sulla posizione e messaggi Flex, supportando casi di utilizzo promozionali, transazionali e di coinvolgimento continuo in mercati dominanti LINE come il Giappone e APAC. Precedentemente rilasciata in Disponibilità limitata, questa funzionalità è ora generalmente disponibile.

* **Monitoraggio di Campaign Orchestration**: è ora disponibile una nuova interfaccia utente per il tracciamento dello stato di acquisizione e dell&#39;aggiornamento dei dati dell&#39;archivio relazionale utilizzati dalla segmentazione orchestrata di Campaign. Ti dà visibilità diretta sullo stato dei dati che alimentano i tipi di pubblico in batch. Una nuova scheda Orchestrazione campagna nel dashboard di monitoraggio di Adobe Experience Platform evidenzia lo stato dei flussi di dati dell’archivio relazionale (record acquisiti/aggiornati/eliminati/non riusciti/ignorati), con grafici di drill-down e un raggruppamento per flusso di dati/set di dati che include la derivazione.

* **API di monitoraggio per nuove campagne orchestrate** - Sono ora disponibili nuove **specifiche API** per le campagne orchestrate, che consentono di creare, gestire e attivare in modo programmatico campagne orchestrate, consentendo una maggiore integrazione con sistemi esterni e pipeline di automazione.

+++

### Canale e-mail {#sep-26-email-channel}

In questa versione, il canale e-mail sarà arricchito dalle seguenti funzionalità.

+++ Disponibile a breve: **le informazioni riportate di seguito sono soggette a modifiche.**

<table>
<thead>
<tr>
<th><strong>Sostituisci impostazioni di configurazione del canale e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Durante la creazione di percorsi e campagne, ora puoi ignorare i parametri e-mail derivati dalla configurazione del canale selezionata direttamente a livello di percorso o di azione della campagna.</p>
<p>Ciò ti consente di personalizzare i campi dell'intestazione e-mail (<strong>Dal nome</strong>, <strong>Dal prefisso e-mail</strong>, <strong>Rispondi al nome</strong> e <strong>Rispondi all'e-mail</strong>), l'indirizzo di esecuzione e i valori di annullamento iscrizione all'elenco, utilizzando gli attributi del profilo o i dati contestuali per un controllo più preciso. In particolare, questo consente ai dettagli del mittente di riflettere l’advisor, la posizione o la filiale pertinente per ciascun destinatario, anziché instradare tutti gli invii tramite un unico indirizzo aziendale.</p>
</td>
</tr>
</tbody>
</table>

* **Sostituzione elenco di soppressione a livello di azione e-mail** - Journey Optimizer ora consente di sovrascrivere il comportamento dell&#39;elenco di soppressione direttamente a livello di azione e-mail in percorsi e campagne. Questo offre ai team maggiore flessibilità per le comunicazioni operative o per le comunicazioni critiche in termini di conformità che richiedono una configurazione di invio dedicata, preservando al contempo i controlli degli elenchi di soppressione globali esistenti per tutti gli altri invii. Questo miglioramento consente alle organizzazioni di gestire gli scenari di eccezione con precisione senza modificare il proprio modello di governance di eliminazione più ampio.

+++

### E-mail designer {#sep-26-email-designer}

In questa versione, e-mail Designer presenta le seguenti funzionalità e miglioramenti.

<table>
<thead>
<tr>
<th><strong>Nuovo componente tabella in E-mail Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>E-mail Designer ora include un <strong>componente tabella</strong> incorporato, che consente di strutturare il contenuto in righe e colonne direttamente all'interno dell'e-mail. Trascina e rilascia il componente nell’area di lavoro, personalizza il numero di righe e colonne e applica uno stile indipendente a ogni cella per creare layout chiari e organizzati senza affidarsi a HTML personalizzati.</p>
<p><img src="assets/do-not-localize/table-component.gif"></p>
<p>Per ulteriori informazioni, consulta la <a href="../email/content-components.md#table">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 24 settembre 2024.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Supporto della modalità scura per le varianti del tema e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>I temi e-mail ora supportano la modalità scura, in modo che ogni variante di colore possa essere riprodotta con un aspetto personalizzato per i destinatari che visualizzano il messaggio e-mail in un client abilitato alla modalità scura.</p>
<p>Quando questa opzione è attivata, viene generata automaticamente una tavolozza scura predefinita per ogni variante e puoi personalizzarla ulteriormente con una tavolozza diversa o con colori personalizzati, indipendentemente dalla progettazione della modalità chiara, in modo che le modifiche apportate in una modalità non influiscano sull'altra.</p>
<p><img src="../email/assets/theme-dark-mode-support.gif"></p>
<p>Per ulteriori informazioni, consulta la <a href="../email/apply-email-themes.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 24 settembre 2024.</p>
</td>
</tr>
</tbody>
</table>

+++ Disponibile a breve: **le informazioni riportate di seguito sono soggette a modifiche.**

<table>
<thead>
<tr>
<th><strong>Importare modelli Dynamic Media direttamente dai file PSD nel Designer e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Il componente Dynamic Media di E-mail Designer ora consente di importare un file Photoshop (PSD) direttamente come nuovo modello, oltre a sfogliare i modelli Dynamic Media esistenti. Trascina e rilascia un file PSD nel componente, Adobe Journey Optimizer lo converte automaticamente in un modello Dynamic Media. Non è necessaria alcuna conversione manuale o round trip through Adobe Experience Manager. Una volta importato, modifica il modello utilizzando l’editor Dynamic Media integrato.</p>
</td>
</tr>
</tbody>
</table>

+++

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
<p>Data di disponibilità: 23 settembre 2026</p>
</td>
</tr>
</tbody>
</table>

+++ Disponibile a breve: **le informazioni riportate di seguito sono soggette a modifiche.**

<table>
<thead>
<tr>
<th><strong>Funzionalità guidate per l’onboarding di e-mail e percorsi (disponibilità generale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La transizione da un’altra piattaforma di marketing a Adobe Journey Optimizer è più semplice grazie a funzionalità guidate che ti consentono di spostare in Journey Optimizer i contenuti e i percorsi e-mail già esistenti. Un'area di lavoro <strong>dedicata</strong> ti consente di riutilizzare ciò che hai invece di ricompilare da zero.</p>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
</td>
</tr>
</tbody>
</table>

+++

### Generazione di rapporti {#sep-26-reporting}

In questa versione verrà presentata la seguente funzionalità per la generazione di rapporti.

<table>
<thead>
<tr>
<th><strong>Nuovi grafici di monitoraggio in entrata in Gestione dati</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile monitorare l'integrità dei dati in entrata direttamente da <strong>Gestione dati &gt; Monitoraggio &gt; Edge</strong>, con sei nuovi grafici che includono gli eventi relativi a velocità effettiva, latenza e proposta:</p>
<ul>
<li><strong>Throughput in entrata AJO</strong>: throughput in entrata complessivo (record al secondo) nel tempo.</li>
<li><strong>Analisi stratificata velocità effettiva in entrata di AJO</strong>: velocità effettiva in entrata suddivisa per posizione.</li>
<li><strong>Latenza in entrata AJO</strong> — latenza richiesta in entrata (in millisecondi), suddivisa per la distribuzione dei valori (P50, P90 e altro).</li>
<li><strong>Throughput eventi proposte in entrata di AJO</strong>: throughput degli eventi di proposta (segnali di tracciamento generati quando un utente interagisce, visualizza o attiva offerte personalizzate) nel tempo.</li>
<li><strong>Throughput degli eventi delle proposte in entrata di AJO per canale</strong> — throughput degli eventi delle proposte suddiviso per canale in entrata (CBE, in-app, schede di contenuto).</li>
<li><strong>Throughput eventi proposte in entrata AJO per tipo di evento</strong> — throughput eventi proposte suddiviso per tipo di evento (ignorato, soppresso, visualizzato, attivato, interagito, inviato).</li>
</ul>
<p>Per ulteriori informazioni, consulta la <a href="../data/monitoring.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 24 settembre 2026</p>
</td>
</tr>
</tbody>
</table>

### Integrazioni {#sep-26-integrations}

In questa versione sono disponibili le seguenti funzionalità per le integrazioni.

+++ Disponibile a breve: **le informazioni riportate di seguito sono soggette a modifiche.**


* **Sostituzione token dinamica per frammenti Experience Manager** - I riferimenti ai frammenti di contenuto Experience Manager ora supportano un attributo **tokenSubstitution**. Se è impostato su `false`, la personalizzazione all&#39;interno dei campi del frammento si risolve direttamente, senza una mappa token nel riferimento. Il valore predefinito è `true`, che mantiene il comportamento esistente.

  Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.

* **Supporto dei frammenti di contenuto di AEM Managed Services in Decisioning** - Il supporto dei frammenti di contenuto di AEM Managed Services è ora disponibile in Decisioning durante la gestione degli elementi decisionali.


+++

### Personalizzazione {#sep-26-personalization}

* **Correggi la sintassi con AI**: quando si convalida un&#39;espressione, se viene rilevato un errore di sintassi PQL, l&#39;editor di Personalization fornisce un&#39;opzione &quot;Correggi con AI&quot; per aiutare a risolvere il problema direttamente dall&#39;editor. [Ulteriori informazioni](../personalization/personalization-build-expressions.md#validation-mechanisms).

  Data di disponibilità: 22 settembre 2026

### Funzione Decisioni {#sep-26-decisioning}

In questa versione sono disponibili le seguenti funzionalità e miglioramenti per il processo decisionale.

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

<table>
<thead>
<tr>
<th><strong>Esploratore delle decisioni in Collaboratore</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Una nuova abilità di <strong>Decisioning Explainer</strong> in CX Coworker consente di chiedere, in linguaggio naturale, perché è stata mostrata o meno un'offerta specifica a un profilo o a un segmento, l'idoneità al tracciamento, il limite, la classificazione e il pool di candidati coinvolti nella decisione.</p>
<p>Per ulteriori informazioni, consulta la <a href="../experience-decisioning/experience-decisioning-coworker-skills.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 16 settembre 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Regole e classificazione in Collaboratore</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Una nuova abilità <strong>Regole e classificazione</strong> in CX Coworker consente di creare, spiegare, simulare e ottimizzare le regole di idoneità e le formule di classificazione utilizzando il linguaggio naturale, senza scrivere o convalidare manualmente la sintassi PQL.</p>
<p>Per ulteriori informazioni, consulta la <a href="../experience-decisioning/experience-decisioning-coworker-skills.md#rules-ranking">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 16 settembre 2026</p>
</td>
</tr>
</tbody>
</table>

* **Frammenti di contenuto AEM in Decisioning disponibili per i clienti Managed Services** - In precedenza, i Frammenti di contenuto AEM in Decisioning erano disponibili solo per i clienti che utilizzavano l&#39;integrazione **Adobe Experience Manager as a Cloud Service**. Questa funzionalità è ora disponibile anche per i clienti che utilizzano **Adobe Experience Manager Managed Services**. [Ulteriori informazioni](../experience-decisioning/items.md#attributes)

  Data di disponibilità: 23 settembre 2026

* **Supporto per i profili Adobe Experience Platform nella simulazione della formula di regole e classificazioni** - Durante la simulazione di una regola o di una formula di classificazione, è ora possibile selezionare un profilo Adobe Experience Platform per riempire automaticamente gli attributi di una variante di dati di test, anziché immetterli manualmente. [Ulteriori informazioni](../experience-decisioning/ranking/ranking-formulas.md#simulate-ranking-formula)

  Data di disponibilità: 22 settembre 2026

### Tipi di pubblico {#sep-26-audiences}

Il seguente promemoria si applica ai tipi di pubblico di questa versione.

* **Prossima modifica ai tipi di pubblico per l&#39;arricchimento della composizione del pubblico** - Durante la versione di ottobre (fine ottobre), Journey Optimizer interromperà i percorsi e le campagne che utilizzano o fanno riferimento a un pubblico per la composizione del pubblico il cui set di dati di origine non ha un **descrittore di identità primario**. Da quel momento in poi, solo i tipi di pubblico di Composizione del pubblico generati con un descrittore di identità principale sono supportati nei percorsi e nelle campagne. Se hai bisogno che questi percorsi o campagne rimangano attivi, contatta il tuo rappresentante Adobe: il nostro team di prodotto può aiutarti a migrare. <!-- Documentation link: TBD -->

### Amministrazione {#sep-26-administration}

Il seguente promemoria si applica all’amministrazione in questa versione.

* **Guardrail TTL (Time-to-live) del set di dati: sandbox esistenti**. Il guardrail TTL (time-to-live) per i set di dati generati dal sistema Journey Optimizer (90 giorni nell&#39;archivio dei profili, 13 mesi nel data lake) verrà applicato alle sandbox e alle organizzazioni dei clienti esistenti a partire dal 1° ottobre 2026.

### Miglioramenti dell’usabilità {#sep-26-usability}

* **È più semplice scollegare e unire rami nella nuova area di lavoro del percorso**. È ora possibile scollegare un ramo dal resto del percorso senza eliminarlo e unirlo di nuovo in un secondo momento in un punto diverso, selezionando un&#39;attività idonea direttamente nell&#39;area di lavoro o selezionandola da un elenco di rami disconnessi o già utilizzati. [Ulteriori informazioni](../building-journeys/using-the-journey-designer.md#join-and-detach-branches)

  Data di disponibilità: 1 settembre 2026

+++ Disponibile a breve: **le informazioni riportate di seguito sono soggette a modifiche.**

* **Miglioramenti di usabilità nell&#39;esperienza di simulazione dei contenuti** - La nuova esperienza di simulazione dei contenuti ora consente di denominare e organizzare le varianti per facilitare il confronto, copiare o eliminare i dettagli delle varianti direttamente da ogni scheda, visualizzare i percorsi degli attributi completi e la configurazione del canale per scheda su richiesta e caricare profili CSV, JSON o JSONL personalizzati da un pulsante di caricamento più prominente.

* **Calendario unificato per campagne, Percorsi e campagne orchestrate** - La visualizzazione calendario per percorsi e campagne ora si sposta da inventari separati in un menu unificato accessibile dalla barra a sinistra che mostra entrambi in un&#39;unica visualizzazione combinata.

+++
