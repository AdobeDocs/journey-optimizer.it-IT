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
source-git-commit: d7ea623e1da2675abcd4bd596cd02ef8133c8b3c
workflow-type: tm+mt
source-wordcount: '4947'
ht-degree: 68%
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

**Novità di CX Enterprise Coworker di questo mese**

Questa versione apporta diverse competenze e funzioni migliorate di [Coworker](../start/ai-features.md#cx-coworker), elencate di seguito per la visibilità. Ciascuna è descritta anche nella relativa sezione sottostante.

* [Plug-in per contenuto canale CE](#sep-26-content-management): nuovo plug-in che riunisce in Coworker le competenze relative a copia, immagine ed e-mail di Campaign, dalla descrizione della campagna alla copia pronta per la produzione e a HTML.
* [Strumenti MCP per la gestione dei contenuti](#sep-26-content-management) - Rileva e gestisci modelli di contenuto, frammenti, pagine di destinazione e contenuti di messaggi in linea tramite messaggi in linguaggio naturale in Coworker.
* [Simulazione del percorso](#sep-26-journeys): automatizza la convalida del percorso end-to-end e interpreta i risultati direttamente in Coworker.
* [Confronta le versioni del percorso](#sep-26-journeys): ottieni un confronto strutturato e dettagliato tra due versioni qualsiasi di un percorso tramite la chat di Coworker.
* [Analisi delle anomalie del Percorso](#sep-26-journeys) - Rilevamento di picchi, cadute o linee piatte imprevisti nei conteggi di entrata, uscita o invio di messaggi di un percorso, con diagnostica della root cause.
* [Abilità di decisioning Explainer](#sep-26-decisioning) - Chiedi al tuo collega perché è stata mostrata o meno un&#39;offerta specifica a un profilo o a un segmento e ottieni una traccia completa delle esclusioni di idoneità, classificazione e regole.
* [Regole e abilità di classificazione](#sep-26-decisioning) - Crea, spiega, simula e ottimizza le regole di idoneità Decisioning e le formule di classificazione in linguaggio naturale, senza scrivere o convalidare manualmente la sintassi PQL.

+++ Disponibile a breve: **le informazioni riportate di seguito sono soggette a modifiche.**

* [Creazione del percorso dalla barra di Coworker](#sep-26-journeys): genera percorsi con l’IA direttamente dalla barra a destra in Coworker, che sostituisce la precedente esperienza dell’Assistente IA.
* [Competenza per consigli sulla fedeltà](#sep-26-loyalty): richiedi opportunità di sfida direttamente nell’interfaccia conversazionale di Coworker e trasformale in sfide live senza uscire dalla chat.
* [Competenza analisi della pulizia](#sep-26-journeys): scansiona percorsi in bozza e attivi per rilevare configurazioni interrotte, errori silenziosi e risorse obsolete o inutilizzate, con correzioni consigliate.
* [Competenza analisi delle prestazioni aziendali](#sep-26-journeys): analizza le prestazioni del percorso e ottieni consigli concreti sull’ottimizzazione, in modo sicuro dalla chat.

+++

>[!ENDSHADEBOX]

### Gestione dei contenuti {#sep-26-content-management}

In questa versione, è disponibile la seguente funzionalità per la gestione dei contenuti.

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
<th><strong>Strumenti MCP per la gestione dei contenuti in CX Coworker</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>CX Coworker dispone ora di un nuovo set di <strong>strumenti MCP per la gestione dei contenuti</strong>, che consente di individuare e gestire le risorse di contenuti Journey Optimizer tramite prompt in linguaggio naturale. Chiedi di elencare o recuperare modelli di contenuto, frammenti, pagine di destinazione e contenuti di messaggi in linea con il percorso o la campagna. Può anche creare contenuti, aggiornare modelli e creare, aggiornare, clonare e pubblicare frammenti, nonché aggiornare il contenuto delle azioni del canale in linea direttamente nel percorso e nella campagna.</p>
<p>Per ulteriori informazioni, consulta la <a href="../content-management/content-management-coworker-skills.md#content-management">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 3 settembre 2026</p>
</td>
</tr>
</tbody>
</table>

* **Casella di controllo del consenso obbligatorio per le pagine di destinazione**: ora puoi rendere obbligatoria una casella di controllo nel componente del modulo della pagina di destinazione, richiedendo ai visitatori di selezionarla (ad esempio, per dare il consenso) prima di poter inviare il modulo. [Ulteriori informazioni](../landing-pages/lp-content.md#use-form-component)

  Data di disponibilità: 4 settembre 2026

* **Parole chiave riservate aggiuntive nella sintassi di personalizzazione**: l’elenco delle parole chiave riservate in PQL (Profile Query Language) è stato ampliato per includere parole chiave generali, unità di tempo e operatori booleani/logici. Se lo schema XDM contiene un nome campo che corrisponde a una di queste parole chiave, racchiudilo tra apici per farvi riferimento in un’espressione di personalizzazione. [Ulteriori informazioni](../personalization/personalization-syntax.md#reserved-keywords)

  Data di disponibilità: 1 settembre 2026

+++ Disponibile a breve: **le informazioni riportate di seguito sono soggette a modifiche.**

* **Convalida URL in Simula contenuto** - Quando visualizzi l&#39;anteprima del contenuto, Journey Optimizer ora controlla automaticamente i collegamenti Web in esso contenuti e contrassegna gli URL interrotti, non sicuri o non raggiungibili prima dell&#39;invio. Questa funzionalità è in disponibilità limitata per una parte della clientela.

+++

### Fedeltà {#sep-26-loyalty}

<table>
<thead>
<tr>
<th><strong>Aggiornamenti alla mappatura eventi fedeltà</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La creazione o la modifica di una mappatura eventi ora utilizza un nuovo **generatore di mappatura visiva**: seleziona uno schema, scegli i campi da un selettore di campi ricercabili, mappa ogni campo su un campo evento fedeltà con stato di connessione per riga e visualizza in anteprima l’espressione JSONata generata automaticamente, con l’opzione di passare alla modifica manuale di JSONata in qualsiasi momento.</p><p>Inoltre, le “Definizioni degli eventi” nell’amministratore Fedeltà sono state rinominate “Mappature eventi”, con una vista a elenco aggiornata che mostra il nome dello schema dell’evento Esperienza leggibile dall’utente.</p>
<p>Per ulteriori informazioni, consulta la <a href="../loyalty-challenges/loyalty-admin.md#event-mappings">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 22 settembre 2026</p>
</td>
</tr>
</tbody>
</table>

* **Sfide fedeltà “per sempre”**: le sfide fedeltà possono ora essere eseguite a tempo indeterminato. Imposta **Fine sfida** su **Nessuna data di fine** durante la configurazione della pianificazione e la sfida non avrà mai scadenza. [Ulteriori informazioni](../loyalty-challenges/create-challenges.md#schedule)

  Data di disponibilità: 1 settembre 2026

* **Fedeltà disponibile per la clientela Healthcare Shield e Privacy and Security Shield**: Journey Optimizer Loyalty è ora disponibile per la clientela Healthcare Shield e Privacy and Security Shield. [Ulteriori informazioni](../loyalty-challenges/get-started.md)

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

* **Sfide del dominio nell’editor di personalizzazione della scheda contenuto**: l’editor di personalizzazione della scheda contenuto ora supporta **Sfide** come dominio, consentendoti l’accesso ai metadati della sfida durante l’authoring di personalizzazione della scheda contenuto. In questo modo è più facile creare contenuti personalizzati per ogni fase di una sfida, ovvero lancio, in corso e fine, senza codice personalizzato.

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
<th><strong>Simulazione del percorso in Coworker</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La <strong>competenza simulazione del percorso</strong> in Coworker automatizza la convalida end-to-end del percorso e consente di interpretare facilmente i risultati. Questa funzione attualmente supporta solo il flusso di simulazione rapida e non sostituisce completamente l’esperienza di simulazione manuale di Journey Optimizer.</p>
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
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe. Per informazioni dettagliate sul ciclo di rilascio e sulle fasi di disponibilità, consulta <a href="releases.md">Ciclo di rilascio di Journey Optimizer</a>.</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/journey-properties.md#performance-management">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 1 settembre 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Genera espressioni con l’IA nei percorsi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’editor di espressioni avanzate del percorso ora integra la generazione di espressioni basate sull’IA: descrivi l’espressione che desideri creare in linguaggio naturale e l’editor genererà codice pronto all’uso da applicare immediatamente o da perfezionare tramite prompt di follow-up.</p>
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

* **Funzione decisioni nella simulazione del percorso**: la sperimentazione del percorso, come parte dell’attività **Ottimizza**, è ora supportata nella simulazione. L’indirizzamento viene gestito dalla funzione Decisioni ed è casuale e non deterministico per ciascun utente simulato.

  [Ulteriori informazioni](../building-journeys/simulate-journey-gs.md)

  Data di disponibilità: 15 settembre 2026

* **Avviso di rilevamento anomalie del nuovo percorso**: un nuovo avviso di sistema ti avvisa quando il traffico giornaliero di un percorso attivo si discosta dalla propria linea di base cronologica o scende inaspettatamente a zero, per entrate nel percorso, uscite dal percorso e invii di eventi. Questo avviso è attualmente disponibile solo nelle sandbox di produzione.

  [Ulteriori informazioni](../reports/alerts.md)

  Data di disponibilità: 15 settembre 2026

* **Funzione Decisioni nella simulazione del percorso**: è ora possibile simulare percorsi che si basano sulla Funzione decisioni, con il supporto per i seguenti elementi:

  * I nodi di decisione sul contenuto sono ora supportati nella simulazione.
  * Il metodo della regola di targeting dell’attività Ottimizza è ora supportato nella simulazione.
  * Le azioni con contenuti basati sulle decisioni di Adobe Journey Optimizer (ad esempio e-mail che utilizzano un criterio di decisione) sono ora supportate nella simulazione.
  * I criteri di decisione che utilizzano l’idoneità e la classificazione delle offerte basandosi su regola, pubblico, priorità o formula sono completamente supportati. Classificazione tramite modello di IA: è supportata anche la personalizzazione, anche se le offerte restituite possono variare tra le esecuzioni.

  [Ulteriori informazioni](../building-journeys/simulate-journey-gs.md)

  Data di disponibilità: 8 settembre 2026

* **Competenza Analizza anomalie del percorso**: CX Coworker è ora in grado di rilevare picchi, cali o azzeramenti imprevisti nei conteggi di entrata, uscita o invii di messaggi di un percorso rispetto alle linee di base cronologiche utilizzando la competenza **Analizza anomalie del percorso**. Una volta confermata un’anomalia reale, la competenza esegue una diagnostica di sola lettura per individuare una probabile causa principale e i relativi consigli. [Ulteriori informazioni](../building-journeys/journeys-coworker-skills.md#journey-analyze)

  Data di disponibilità: 2 settembre 2026

* **Nuova funzione dateDiff nell’editor di espressioni del percorso**: l’editor di espressioni del percorso include ora la funzione `dateDiff`, che calcola la differenza tra due date, espressa in numero di giorni. Questa funzione è utile per una logica basata sul tempo, ad esempio per creare scadenze, calcolare la durata del ciclo di vita del cliente o creare timer di conti alla rovescia nelle condizioni del percorso.  [Ulteriori informazioni](../building-journeys/functions/date-functions.md#dateDiff)

  Data di disponibilità: 1 settembre 2026

+++ Disponibile a breve: **le informazioni riportate di seguito sono soggette a modifiche.**

<table>
<thead>
<tr>
<th><strong>Schede di consigli di IA per gli avvisi sul percorso</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Nella pagina Home di Journey Optimizer viene ora visualizzata una <strong>scheda di consigli forniti dall’IA</strong> quando viene attivato un avviso sul percorso per <strong>azioni personalizzate del percorso non riuscite</strong> e <strong>anomalie rilevate nel percorso</strong>. Selezionando la scheda si apre il percorso con la barra destra già compilata con l’analisi eseguita.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Attività del percorso di disattivazione delle attività in entrata</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Una nuova attività di <strong>disattivazione dell’attività in entrata</strong> nell’area di lavoro del percorso consente di rimuovere un profilo da un massimo di cinque attività o esperienze in entrata direttamente da un percorso, separando la mancata idoneità in entrata dall’uscita dal percorso per un’orchestrazione più avanzata cross-channel.</p>
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
<th><strong>Creazione del percorso dalla barra di Coworker</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La <strong>creazione del percorso con l’IA</strong> è ora disponibile direttamente dalla barra laterale destra di Coworker, sostituendo la precedente esperienza di Assistente IA con un punto di ingresso integrato e rinominato per la generazione di percorsi.</p>
</td>
</tr>
</tbody>
</table>

* **Abilità di analisi dell&#39;igiene** - CX Coworker ora può analizzare i percorsi attivi e in bozza per individuare configurazioni interrotte, errori silenziosi e risorse in declino o inutilizzate, ad esempio percorsi bozza non aggiornati, origini dati orfane ed errori persistenti di azioni personalizzate, oltre a trovare direttamente in chat le correzioni consigliate. <!-- Documentation link: TBD -->

* **Supporto di ID supplementari nella simulazione del percorso**: l’**ID supplementare** è ora supportato nella simulazione del percorso, consentendo di testare scenari utente complessi sia per i percorsi di pubblico di lettura che per quelli attivati da eventi.

* **Soppressione di eventi nei passaggi di esecuzioni di prova per rapporti personalizzati**: nell’ambito dell’ottimizzazione degli eventi dei passaggi, durante le esecuzioni di prova dei percorsi Journey Optimizer ora non genera più alcuni eventi di passaggi che non vengono inclusi nei rapporti. Questo influisce solo sui rapporti personalizzati basati su questi tipi di eventi di passaggio delle esecuzioni di prova. Per i rapporti interessati da questa modifica, riattiva l’esecuzione di prova per rigenerare i dati.

* **Timeout del ripristino automatico degli eventi nelle proprietà del percorso**: le proprietà del percorso ora includono l’impostazione **Imposta timeout di ripristino dell’evento**: per impostazione predefinita, gli eventi del percorso interessati vengono nuovamente riprodotti in automatico fino a 72 ore dopo un’interruzione del servizio, senza che sia necessaria alcuna azione. È possibile attivare questa impostazione per controllare la finestra di ripetizione (0-72 ore) per i percorsi sensibili al tempo. Anche il campo **Timeout o errore** esistente è stato rinominato in **Azione personalizzata/Timeout origine dati** per evitare confusione tra le due impostazioni.

* **Eventi di passaggio ridotti per le attività attendi ed eventi** - Gli eventi di passaggio non vengono più generati per le attività **attendi** e **evento** quando il profilo non è stato effettivamente elaborato in tale attività.

+++

### Campagne {#sep-26-campaigns}

+++ Disponibile a breve: **le informazioni riportate di seguito sono soggette a modifiche.**

* **Cartelle per campagne di azione**: ora puoi organizzare le campagne di azione in cartelle per migliorarne la navigazione e la gestione all’interno dell’interfaccia.

* **Sostituzione dei campi di esecuzione predefiniti nelle campagne di azione**: precedentemente disponibili a livello di percorso, ora puoi sostituire i campi di esecuzione predefiniti configurati a livello globale per le consegne tramite e-mail, SMS e WhatsApp nei parametri delle campagne di azione.

+++


### Canali {#sep-26-channels}

In questa versione sono stati aggiunti i miglioramenti e le funzionalità seguenti per i canali.

* **Limite aumentato di delega dei sottodomini** - A seconda del contratto di licenza, ora puoi richiedere fino a 3000 sottodomini (in precedenza limitati a 100) contattando il tuo rappresentante Adobe. Questa funzionalità è in disponibilità limitata per una parte della clientela. [Ulteriori informazioni](../configuration/delegate-subdomain.md#guardrails)

  Data di disponibilità: 25 settembre 2026

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
<p>I <strong>canali in uscita personalizzati</strong> consentono agli amministratori di portare qualsiasi canale di messaggistica in uscita basato su HTTP, come WeChat, Kakao Talk, Messenger o un provider proprietario, direttamente in Journey Optimizer tramite un generatore di canali senza codice. Una volta configurati, i canali personalizzati sono disponibili in tutte le campagne, i percorsi e le campagne orchestrate, con lo stesso set completo di funzionalità dei canali nativi: personalizzazione con l’editor di espressioni, sperimentazione dei contenuti, anteprima e bozza, reporting predefinito e applicazione delle norme in materia di consenso e governance.</p>
<p>Con questa versione, i canali in uscita personalizzati acquisiscono anche diverse nuove funzionalità:</p>
<ul>
<li>Utilizza la funzione Decisioni di Journey Optimizer nel payload del canale personalizzato tramite l’editor di personalizzazione, come nelle esperienze basate su codice.</li>
<li>Applica le regole di business ai canali personalizzati, proprio come puoi già fare già con i canali nativi.</li>
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
<th><strong>Attività live per aggiornamenti live di Android</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ora amplia le funzionalità di personalizzazione per dispositivi mobili in tempo reale estendendo il <strong>supporto di attività live ad Android</strong>. Puoi fornire aggiornamenti sull’avanzamento in tempo reale direttamente agli utenti, ad esempio quelli relativi al tracciamento degli ordini, agli stati dei voli, agli eventi live e ai punteggi sportivi in tempo reale.</p>
<p>Oltre a supportare le attività live di iOS, Journey Optimizer ora gestisce i token push temporanei per gli aggiornamenti live di Android sulle diverse configurazioni della piattaforma. Supporta sia i flussi di aggiornamento broadcast che quelli transazionali utilizzando campagne attivate da API e API headless.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Miglioramenti ai modelli di notifiche push di Android</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le notifiche push di Android venivano sottoposte in precedenza a rendering con un layout singolo e fisso: le immagini venivano sempre ritagliate al centro e il corpo del testo lungo veniva troncato. Questa versione introduce un selettore di modelli al momento dell’authoring, consentendo agli addetti al marketing di controllare il layout delle notifiche push di Android.</p>
<p>Sono disponibili i seguenti miglioramenti:</p>
<ul>
<li><b>Selezione layout</b>: nuovo selettore del layout delle notifiche push (standard/espanso) durante la creazione di un messaggio push Android.</li>
<li><b>Layout standard con “Mostra immagine intera”</b>: scegli ritaglia per riempire e ridimensiona per adattare.</li>
<li><b>Layout espanso</b>: testo del corpo su più righe senza troncamento e miniatura opzionale con icona grande.</li>
<li><b>Corpo compresso (layout espanso)</b>: imposta un corpo di testo separato e più breve per lo stato compresso.</li>
</ul>
</td>
</tr>
</tbody>
</table>

* **Flessibilità di autenticazione BYOP degli SMS personalizzati**: ora è possibile configurare le **intestazioni di autenticazione personalizzate** durante la connessione della configurazione OAuth del provider SMS, tra cui la posizione del token nei messaggi in uscita e la formattazione della richiesta del token.

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
<th><strong>Attività OR-join per campagne orchestrate</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’<strong>attività Unisci</strong> nelle campagne orchestrate ora supporta entrambe le condizioni di unione E e OPPURE. Con la logica OR, un profilo che completa un singolo ramo a monte, anziché tutti, continua lungo un singolo percorso condiviso a valle. Questo rende possibile modellare direttamente sull’area di lavoro pattern come “se A o B o C, quindi fai questo” senza duplicare i passaggi a valle tra rami separati.</p>
</td>
</tr>
</tbody>
</table>

* **Canale LINE per campagne orchestrate**: LINE è ora disponibile come canale nativo in uscita nelle campagne orchestrate, insieme a e-mail, SMS e push. Puoi creare e inviare messaggi LINE direttamente dall’area di lavoro della campagna, con testo, sticker, immagini, video, dati sulla posizione e messaggi Flex, per casi d’uso promozionali, transazionali e di coinvolgimento continuo in mercati in cui prevale il canale LINE, come il Giappone e l’APAC. Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora in disponibilità generale.

* **Monitoraggio dell’orchestrazione della campagna**: è ora disponibile una nuova interfaccia per il tracciamento dello stato di acquisizione e dell’aggiornamento dei dati dell’archivio relazionale utilizzati dalla segmentazione della campagna orchestrata. Ciò ti offre una visibilità diretta sullo stato dei dati che alimentano i tipi di pubblico batch. Una nuova scheda orchestrazione della campagna nella dashboard di monitoraggio di Adobe Experience Platform evidenzia lo stato dei flussi di dati dell’archivio relazionale (record acquisiti/aggiornati/eliminati/non riusciti/ignorati), con grafici di dettaglio e un raggruppamento per flusso di dati/set di dati che include la derivazione.

* **API di monitoraggio per nuove campagne orchestrate**: sono ora disponibili nuove **specifiche API** per le campagne orchestrate, che consentono di creare, gestire e attivare in modo programmatico campagne orchestrate, favorendo una maggiore integrazione con sistemi esterni e pipeline di automazione.

+++

### Canale e-mail {#sep-26-email-channel}

In questa versione, il canale e-mail sarà arricchito dalle seguenti funzionalità.

+++ Disponibile a breve: **le informazioni riportate di seguito sono soggette a modifiche.**

<table>
<thead>
<tr>
<th><strong>Sostituire le impostazioni di configurazione del canale e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Durante la creazione di percorsi e campagne, ora puoi sostituire i parametri delle e-mail derivati dalla configurazione del canale selezionata direttamente a livello di percorso o di azione della campagna.</p>
<p>Ciò ti consente di personalizzare i campi dell’intestazione dell’e-mail (<strong>Nome del mittente</strong>, <strong>Prefisso dell’e-mail del mittente</strong>, <strong>Nome del mittente per le risposte</strong> e <strong>E-mail per le risposte</strong>), l’indirizzo di esecuzione e i valori di annullamento dell’iscrizione all’elenco, utilizzando gli attributi del profilo o i dati contestuali per un controllo più preciso. Questo fa sì che i dettagli del mittente riflettano l’esperto, la posizione o il ramo relativa a ciascun destinatario, anziché instradare tutti gli invii tramite un unico indirizzo aziendale.</p>
</td>
</tr>
</tbody>
</table>

* **Sostituzione elenco di soppressione a livello di azione e-mail** - Journey Optimizer ora consente di sovrascrivere il comportamento dell&#39;elenco di soppressione direttamente a livello di azione e-mail in percorsi e campagne. Questo offre ai team maggiore flessibilità per le comunicazioni operative o per le comunicazioni critiche in termini di conformità che richiedono una configurazione di invio dedicata, preservando al contempo i controlli degli elenchi di soppressione globali esistenti per tutti gli altri invii. Questo miglioramento consente alle organizzazioni di gestire gli scenari di eccezione con precisione senza modificare il proprio modello di governance di eliminazione più ampio.

+++

### E-mail designer {#sep-26-email-designer}

In questa versione sono stati aggiunti i miglioramenti e le funzionalità seguenti a E-mail designer.

<table>
<thead>
<tr>
<th><strong>Nuovo componente tabella in E-mail Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>E-mail Designer ora include un <strong>componente tabella</strong> incorporato, che consente di strutturare il contenuto in righe e colonne direttamente all’interno dell’e-mail. Trascina e rilascia il componente nell’area di lavoro, personalizza il numero di righe e colonne e definisci lo stile di ogni cella in modo indipendente per creare layout chiari e organizzati senza dover ricorrere a codice HTML personalizzato.</p>
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
<th><strong>Supporto della modalità scura per le varianti del tema delle e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>I temi delle e-mail ora supportano la modalità scura, in modo che ogni variante di colore possa essere riprodotta con un aspetto personalizzato per i destinatari che visualizzano il messaggio e-mail in un client abilitato per tale modalità.</p>
<p>Quando è attivata questa opzione, viene generata automaticamente una palette scura predefinita per ogni variante che puoi personalizzare ulteriormente con una palette diversa o con colori personalizzati. La personalizzazione è indipendente dalla progettazione della modalità chiara, quindi le modifiche apportate in una modalità non influiscono sull’altra.</p>
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
<th><strong>Importare modelli Dynamic Media direttamente dai file PSD in E-mail designer</strong><br/></th>
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

### Onboarding {#sep-26-onboarding}

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
<p>La transizione da un’altra piattaforma di marketing ad Adobe Journey Optimizer è più semplice grazie a funzionalità guidate che ti consentono di spostare in Journey Optimizer i contenuti e i percorsi e-mail già esistenti. Un’<strong>area di lavoro dedicata</strong> ti consente di riutilizzare ciò che hai già a disposizione, invece di ricreare tutto da zero.</p>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
</td>
</tr>
</tbody>
</table>

+++

### Generazione di rapporti {#sep-26-reporting}

In questa versione è disponibile la funzionalità seguente per il reporting.

<table>
<thead>
<tr>
<th><strong>Nuovi grafici di monitoraggio in entrata nella gestione dei dati</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile monitorare l’integrità dei dati in entrata direttamente da <strong>Gestione dati &gt; Monitoraggio &gt; Edge</strong>, con sei nuovi grafici che includono gli eventi relativi a velocità effettiva, latenza e proposta:</p>
<ul>
<li><strong>Velocità effettiva in entrata di AJO</strong>: velocità effettiva in entrata complessiva (record al secondo) nel tempo.</li>
<li><strong>Suddivisione della velocità effettiva in entrata di AJO</strong>: velocità effettiva in entrata suddivisa per posizione.</li>
<li><strong>Latenza in entrata di AJO</strong>: latenza della richiesta in entrata (in millisecondi), suddivisa per la distribuzione dei valori (P50, P90 e altro).</li>
<li><strong>Velocità effettiva degli eventi di proposta in entrata di AJO</strong>: velocità effettiva degli eventi di proposta (segnali di tracciamento generati quando un utente interagisce, visualizza o attiva offerte personalizzate) nel tempo.</li>
<li><strong>Velocità effettiva degli eventi di proposta in entrata di AJO per canale</strong>: velocità efffettiva degli eventi di proposta suddivisa per canale in entrata (CBE, in-app, schede di contenuto).</li>
<li><strong>Velocità effettiva di eventi di proposta in entrata di AJO per tipo di evento</strong>: velocità effettiva di eventi di proposta suddivisa per tipo di evento (ignorato, eliminato, visualizzato, attivato, interagito, inviato).</li>
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
<th><strong>Supporto della funzione Decisioni nel canale web</strong><br/></th>
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
<p>Per ulteriori informazioni, consulta la <a href="../experience-decisioning/experience-decisioning-coworker-skills.md#decisioning-explainer">documentazione dettagliata</a>.</p>
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

* **Supporto per i profili Adobe Experience Platform nella simulazione della formula di regole e classificazioni**: durante la simulazione di una formula di una regola o classificazione, è ora possibile selezionare un profilo Adobe Experience Platform per riempire automaticamente gli attributi di una variante di dati di test, anziché immetterli manualmente. [Ulteriori informazioni](../experience-decisioning/ranking/ranking-formulas.md#simulate-ranking-formula)

  Data di disponibilità: 22 settembre 2026

### Tipi di pubblico {#sep-26-audiences}

Il seguente promemoria si applica ai tipi di pubblico di questa versione.

* **Prossima modifica relativa ai tipi di pubblico per l’arricchimento della composizione del pubblico**: durante la versione di ottobre (prevista per la fine del mese), Journey Optimizer interromperà i percorsi e le campagne che utilizzano o fanno riferimento a un pubblico per la composizione del pubblico il cui set di dati di origine sia privo di un **descrittore di identità primaria**. Da quel momento in poi, nei percorsi e nelle campagne sono supportati solo i tipi di pubblico di composizione del pubblico generati con un descrittore di identità principale. Se hai bisogno che questi percorsi o campagne rimangano attivi, contatta il tuo rappresentante Adobe: il nostro team di prodotto può aiutarti ad effettuare la migrazione. <!-- Documentation link: TBD -->

### Amministrazione {#sep-26-administration}

In questa versione il promemoria seguente si applica all’amministrazione.

* **Guardrail TTL (time-to-live) del set di dati: sandbox esistenti**: il guardrail TTL (time-to-live) per i set di dati generati dal sistema Journey Optimizer (90 giorni nell’archivio dei profili, 13 mesi nel data lake) verrà applicato alle organizzazioni e alle sandbox della clientela esistente a partire dal 1 ottobre 2026.

### Miglioramenti dell’usabilità {#sep-26-usability}

* **Scollegamento e unione di rami nella nuova area di lavoro del percorso**: ora è possibile scollegare un ramo dal resto del percorso senza eliminarlo e riunirlo in un secondo momento in un punto diverso, selezionando un’attività idonea direttamente nell’area di lavoro o selezionandola da un elenco di rami scollegati o già utilizzati. [Ulteriori informazioni](../building-journeys/using-the-journey-designer.md#join-and-detach-branches)

  Data di disponibilità: 1 settembre 2026

+++ Disponibile a breve: **le informazioni riportate di seguito sono soggette a modifiche.**

* **Miglioramenti di usabilità nell’esperienza di simulazione dei contenuti**: la nuova esperienza di simulazione dei contenuti ora consente di denominare e organizzare le varianti per facilitare il confronto, la copia o l’eliminazione dei dettagli delle varianti direttamente da ogni scheda; visualizzare i percorsi degli attributi completi e la configurazione del canale per scheda su richiesta; e caricare profili CSV, JSON o JSONL personalizzati con un pulsante di caricamento più prominente.

* **Calendario unificato per campagne, percorsi e campagne orchestrate**: la vista calendario per percorsi e campagne ora non è più disponibile in inventari separati, ma in un menu unificato, accessibile dalla barra laterale sinistra, che mostra entrambi in un’unica vista combinata.

+++
