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
feature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2:
  - id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794
  - id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0
  - id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 5592f564456edf86e04dc9849c947402126cf161
workflow-type: tm+mt
source-wordcount: 2234
ht-degree: 85%

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

## Aggiornamenti di settembre 2026 {#sep-26-updates}

### Percorsi {#sep-26-journeys}

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

* **Nuova funzione dateDiff nell&#39;editor espressioni di percorso**. L&#39;editor espressioni di percorso include ora la funzione `dateDiff`, che calcola la differenza tra due date in un numero di giorni. Questa funzione è utile per una logica basata sul tempo, ad esempio per creare scadenze, calcolare la durata del ciclo di vita del cliente o creare timer di conto alla rovescia in condizioni di percorso.  [Ulteriori informazioni](../building-journeys/functions/date-functions.md#dateDiff)

  Data di disponibilità: 1 settembre 2026

### Campagne {#sep-26-campaigns}

+++ Disponibile a breve: **le informazioni riportate di seguito sono soggette a modifiche.**

<table>
<thead>
<tr>
<th><strong>Simulazione dell’esperienza in entrata nelle campagne di azione</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi simulare le azioni del canale in entrata nelle campagne di azione prima della pubblicazione. Utilizza la modalità di simulazione per testare la configurazione con utenti simulati e visualizzare in anteprima l’esperienza di cui è stato eseguito il rendering, inclusi un URL generato e un codice QR, in modo da poter convalidare regole, decisioni e rendering end-to-end dei contenuti.</p>
<p>Questa funzionalità è attualmente disponibile in versione Private Beta per un numero limitato di organizzazioni. Per ulteriori informazioni, contatta il tuo rappresentante Adobe.</p>
<p>Data di disponibilità: 4 settembre 2026</p>
</td>
</tr>
</tbody>
</table>

* **Cartelle per le campagne d&#39;azione** - È ora possibile organizzare le campagne d&#39;azione in cartelle per migliorare la navigazione e la gestione nell&#39;interfaccia.

* **Riprogettazione del flusso di authoring della campagna di azione**: il flusso di authoring della campagna di azione di Adobe Journey Optimizer è stato riprogettato per offrire un’esperienza utente decisamente più intuitiva, efficiente e fluida.

* **Sostituisci i campi di esecuzione predefiniti nelle campagne Azione**. Precedentemente disponibili a livello di percorso, ora puoi sovrascrivere i campi di esecuzione predefiniti configurati a livello globale per le consegne e-mail, SMS e WhatsApp nei parametri della campagna Azione.

+++

## Note sulla versione di agosto 2026 {#aug-26-updates}

### Gestione dei contenuti

In questa versione sono stati introdotti i seguenti miglioramenti e funzionalità per la gestione dei contenuti.

<table>
<thead>
<tr>
<th><strong>Origine immagine flessibile per la generazione di contenuti IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora, la generazione dei contenuti in Journey Optimizer utilizza direttamente immagini approvate dal brand provenienti da Adobe Experience Manager Assets Essentials e versioni successive. Il bilanciamento è controllato da tre modalità: Bilanciata (priorità alla gestione delle risorse digitali, con l’IA che colma le lacune; modalità predefinita), Risorse (originate dalla gestione delle risorse digitali) e Creativa (IA).</p>
<p><img src="../content-management/assets/image-mode-3.png"></p>
<p>Per ulteriori informazioni, consulta la <a href="../content-management/generative-uc.md#image-mode">documentazione dettagliata</a>.</p>
<p> Data di disponibilità: 5 agosto 2026</p>
</td>
</tr>
</tbody>
</table>

* **Avviso sulle dimensioni delle varianti di contenuto**: in Journey Optimizer viene ora visualizzato un avviso di limite non permanente quando una variante di contenuto supera la soglia di dimensioni consigliata: 1200 KB per modelli e messaggi, 700 KB per frammenti e 1000 KB per pagine di destinazione. Il salvataggio e la pubblicazione non bloccati. [Ulteriori informazioni](../start/guardrails.md#content-authoring)

  Data di disponibilità: 25 agosto 2026

* **Limiti di conteggio dei frammenti nel contenuto**: Journey Optimizer ora convalida il numero di frammenti univoci utilizzati all’interno di una parte di contenuto, ovvero fino a 60 per variante e fino a 120 per tutte le varianti di un singolo messaggio. Gli avvisi vengono visualizzati al 75% di ogni limite; la pubblicazione viene bloccata una volta raggiunto il limite permanente. [Ulteriori informazioni](../start/guardrails.md#fragments-guardrails)

  Data di disponibilità: 25 agosto 2026

### Percorsi {#aug-26-journeys}


* **Date di inizio e di fine nell’intestazione del percorso**: quando le date di inizio e/o di fine sono configurate in un percorso, ora vengono visualizzate nell’intestazione del percorso accanto al badge dello stato. L’etichetta visualizzata si adatta a seconda che ogni data sia imminente o già passata. [Ulteriori informazioni](../building-journeys/journey-properties.md#dates)

  Data di disponibilità: 20 agosto 2026

* **Nuove funzioni per gli elenchi nell’editor di espressioni avanzato** - Nell’editor delle espressioni avanzato sono disponibili due nuove funzioni: `mergeLists` combina due elenchi, con o senza deduplicazione e `differenceLists` restituisce gli elementi di un elenco che non sono presenti nell’altro. [Ulteriori informazioni](../building-journeys/functions/list-functions.md)

  Data di disponibilità: 13 agosto 2026

* **Ottimizzazione dei tempi di invio nell&#39;attività Attendi** - Ottimizzazione dei tempi di invio è ora disponibile nell’attività Attendi, consentendo all’IA di Adobe di determinare il tempo ottimale per proseguire con qualsiasi attività a valle. [Ulteriori informazioni](../building-journeys/wait-activity.md#sto-wait)

  Data di disponibilità: 13 agosto 2026

### Campagne {#aug-26-campaigns}

In questa versione sono stati aggiunti i seguenti miglioramenti e funzionalità alle campagne.

<table>
<thead>
<tr>
<th><strong>Allegati PDF personalizzati in e-mail attivate da API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ora supporta fino a <b>cinque allegati PDF</b> totali per e-mail nelle campagne attivate da API, inclusi PDF statici e specifici dei destinatari. I file PDF specifici dei destinatari vengono recuperati in modo sicuro dall’area di destinazione dei dati e allegati al momento dell’invio, con la posizione di ciascun file passata direttamente nel payload API. Questo consente ai sistemi di generazione dei documenti esistenti a monte di rimanere operativi, con la gestione della consegna da parte di Journey Optimizer.</p>
<p>I casi d’uso supportati includono fatture, istruzioni, ticket, contratti, etichette di spedizione e documenti simili che variano a seconda del destinatario. Gli allegati PDF personalizzati sono disponibili solo per campagne e-mail attivate da API transazionali e non sono supportati in percorsi o campagne orchestrate.</p>
<p>Volumi e dimensioni di allegati più grandi sono supportati tramite il componente aggiuntivo per allegati PDF; per informazioni, contatta il rappresentante Adobe.</p>
<p>Per ulteriori informazioni, consulta la <a href="../email/pdf-attachments.md#personalized-attachments">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 12 agosto 2026</p>
</td>
</tr>
</tbody>
</table>

* **Abbonamenti agli avvisi sul ciclo di vita per campagna**: ora puoi abbonarti agli avvisi sul ciclo di vita della campagna supportati per una singola campagna, oltre all’abbonamento esistente a livello di sandbox. Questo ti consente di monitorare singole campagne ad alta priorità senza ricevere lo stesso avviso per ogni campagna nella sandbox. [Ulteriori informazioni](../reports/alerts.md#subscribe-alerts)

  Data di disponibilità: 13 agosto 2026

### Campagne orchestrate {#august-26-oc}

In questa versione sono stati aggiunti i miglioramenti e le funzionalità seguenti alle campagne orchestrate.

<table>
<thead>
<tr>
<th><strong>Supporto ore di silenzio</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi applicare le ore di silenzio. Le ore di silenzio ti consentono di definire esclusioni basate sul tempo per impedire l’invio di messaggi durante periodi specifici, aiutandoti a rispettare le preferenze del cliente e i requisiti di conformità in tutti i casi d’uso dell’orchestrazione delle campagne.</p>
<p>Per ulteriori informazioni, consulta la <a href="../conflict-prioritization/quiet-hours.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 18 agosto 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Inviare utilizzando gli scaglioni</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi pianificare la consegna di messaggi in uscita in batch controllati nel tempo. Ideale per campagne con volumi elevati o che richiedono molto tempo, l’invio in scaglioni supporta anche una recapitabilità migliore e contribuisce a mantenere una solida reputazione del mittente riducendo il rischio di essere segnalato come spam. </p>
<p>Per ulteriori informazioni, consulta la <a href="../delivery/send-using-waves.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 18 agosto 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Supporto del canale LINE (disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi aggiungere azioni LINE alle campagne orchestrate. Questa nuova attività ti consente di creare e consegnare contenuti altamente personalizzati, inclusi testo, adesivi, immagini, video, dati sulla posizione e messaggi Flex avanzati, per coinvolgere la clientela in modo semplice sulla piattaforma LINE. Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<p>Per ulteriori informazioni, consulta la <a href="../orchestrated/activities/channels.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 12 agosto 2026</p>
</td>
</tr>
</tbody>
</table>

* **Possibilità di gestire le dimensioni target del profilo**: ora puoi eliminare una dimensione target del profilo o modificare e scambiare lo spazio dei nomi identità configurato, fornendo un maggiore controllo e flessibilità sulle configurazioni dei dati. [Ulteriori informazioni](../orchestrated/target-dimension.md)

  Data di disponibilità: 18 agosto 2026

<!-- * **New public APIs** - New API specifications are now available. These APIs allow you to programmatically create, manage, and trigger orchestrated campaigns, enabling deeper integration with external systems and automation pipelines. Documentation link: TBD -->

* **Personalizzazione dei dettagli del mittente e-mail per destinatario e campagna (disponibilità limitata)**: le campagne orchestrate ora supportano la personalizzazione dei campi dell’intestazione e-mail, inclusi Nome mittente, Prefisso e-mail mittente, Nome “Rispondi a” e E-mail di risposta, nonché l’indirizzo di esecuzione, utilizzando gli attributi del profilo o i dati relazionali. Questo consente ai dettagli del mittente di indicare l’esperto, la posizione o la filiale relativa a ciascun destinatario, anziché instradare tutti gli invii tramite un unico indirizzo aziendale. I valori dell’intestazione possono essere impostati a livello di canale e sostituiti per campagna utilizzando dati contestuali per un controllo più preciso. [Ulteriori informazioni](../orchestrated/activities/channels.md#configuration)

  Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata).

  Data di disponibilità: 18 agosto 2026

* **Semplificazione della dimensione target**: la dimensione targeting attiva viene ora visualizzata nell’area di lavoro del flusso di lavoro, che illustra quale dimensione viene utilizzata da un’attività di canale. Il flusso di segmentazione di più entità è più semplice in quanto non è più necessaria un’attività &quot;Modifica dimensione&quot; separata. Inoltre, ora puoi scegliere esplicitamente se i messaggi vengono inviati a livello di profilo o a un livello di dimensione secondario. [Ulteriori informazioni](../orchestrated/activities/channels.md#add)

  Data di disponibilità: 18 agosto 2026

### Fedeltà {#aug-26-loyalty}

<table>
<thead>
<tr>
<th><strong>Abilità di Approfondimenti fedeltà</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer presenta <strong>Loyalty Insights</strong>, una nuova abilità di CX Coworker per porre domande sulle prestazioni delle sfide e altri dati del programma fedeltà acquisiti nei gruppi di campi Fedeltà in Adobe Experience Platform.</p>
<p>Per ulteriori informazioni, consulta la <a href="../start/ajo-coworker-skills.md#loyalty-skills">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 31 agosto 2026</p>
</td>
</tr>
</tbody>
</table>

### Canali {#august-26-channels}

* **Metadati di esecuzione attività live (executionMetadata)**: le campagne di attività live (transazionali e di marketing) attivate da API ora supportano un campo executionMetadata facoltativo su ogni destinatario. Questo consente di allegare a un’esecuzione dati valore/chiave personalizzata, come un ID ordine, un livello fedeltà o un codice di area geografica. [Ulteriori informazioni](../mobile-live/create-mobile-live.md#metadata)

  Data di disponibilità: 19 agosto 2026

* **Componente aggiuntivo con prestazioni per velocità effettiva - push**: nelle campagne attivate da API è disponibile una nuova modalità di messaggistica transazionale di velocità effettiva elevata. Questa modalità è progettata per la messaggistica transazionale in tempo reale su larga scala e supporta fino a 5.000 transazioni al secondo con maggiore disponibilità. Precedentemente disponibile solo per il canale e-mail, questa funzionalità è ora disponibile per il canale push, per le organizzazioni che hanno acquistato l’offerta con componente aggiuntivo per messaggistica transazionale con velocità effettiva elevata di Adobe. Per ulteriori informazioni, contatta il tuo rappresentante Adobe. [Ulteriori informazioni](../campaigns/api-triggered-high-throughput.md)

  Data di disponibilità: 11 agosto 2026

### Configurazione {#august-26-configuration}

* **Supporto multi-SAN nella generazione CSR per la configurazione del sottodominio personalizzato** - Durante la configurazione o la migrazione di un sottodominio personalizzato tramite il metodo di delega personalizzata, la richiesta di firma del certificato (CSR, Certificate Signing Request) viene ora generata automaticamente con `data.{subdomain}` e `cdn.{subdomain}` come nomi alternativi soggetti (SAN, Subject Alternative Names). In precedenza, la CSR generata includeva solo `data.{subdomain}`, richiedendo l&#39;aggiunta manuale di `cdn.{subdomain}` prima dell&#39;invio all&#39;autorità di certificazione. [Ulteriori informazioni](../configuration/custom-subdomain-migration.md#send-csr-to-ca)

  Data di disponibilità: 20 agosto 2026

### Funzione Decisioni {#decisioning-august}

* **Quota limite a livello di posizionamento nella funzione Decisioni**: le regole riguardandi la limitazione della funzione Decisioni possono ora essere definite in base ai singoli posizionamenti, assicurando un controllo più preciso sulla frequenza con cui un’offerta viene visualizzata in una determinata superficie. Sono disponibili due modalità: **capping specifico per posizionamento**, che definisce un limite applicabile solo quando l’offerta viene visualizzata in un posizionamento selezionato, e **capping per posizionamento**, che applica un limite in modo indipendente in ogni posizionamento in cui viene visualizzata l’offerta, in modo che ogni posizionamento mantenga il proprio contatore di limiti. Tieni presente che il limite relativo al posizionamento non si applica alle offerte con limite massimo basate su regole basate sui dati di Adobe Experience Platform. [Ulteriori informazioni](../experience-decisioning/items.md#capping)

  Data di disponibilità: 24 agosto 2026

* **Pagine mirror nei frammenti visivi**: ora puoi inserire pagine mirror in un frammento visivo. Gli attributi della funzione Decisioni eseguono il rendering correttamente sul collegamento della pagina mirror, anche quando il frammento viene utilizzato in una campagna e-mail che sfrutta la funzione Decisioni. Per poter visualizzare gli attributi della funzione Decisioni, prima di pubblicare il frammento è necessario aggiungere la pagina mirror al frammento visivo. [Ulteriori informazioni](../email/message-tracking.md#decisioning-mirror-page)

  Data di disponibilità: 11 agosto 2026

### Miglioramenti dell’usabilità {#august-26-usability}

* **Selezione multipla nella nuova area di lavoro del percorso**: la nuova esperienza dell’area di lavoro del percorso introduce una selezione semplificata a più nodi: tieni premuto Maiusc e trascina per selezionare più nodi contemporaneamente, anziché selezionarli singolarmente. Questo consente di eseguire in modo efficiente su più nodi azioni in blocco, come copiare, eliminare o salvare come frammento di percorso. [Ulteriori informazioni](../building-journeys/using-the-journey-designer.md#canvas-capabilities)

  Data di disponibilità: 17 agosto 2026

* **Operazioni in blocco nell’inventario del percorso**: ora puoi eseguire nuove azioni in blocco direttamente dall’elenco dell’inventario del percorso, rendendo più rapida la gestione di più percorsi contemporaneamente. Seleziona diversi percorsi e applica una delle seguenti nuove azioni in un singolo passaggio: **aggiungi al pacchetto**, **elimina**, **sposta nella cartella**, **modifica tag** o **gestisci accesso**. Questo riduce la necessità di ripetere la stessa azione un percorso alla volta, semplificando la gestione del percorso per i team che lavorano con un numero elevato di percorsi. [Ulteriori informazioni](../building-journeys/journey-ui.md)

  Data di disponibilità: 12 agosto 2026

* **Nuova esperienza di simulazione dei contenuti per testare il contenuto** - Il flusso di lavoro **Simula contenuto** introduce un’esperienza riprogettata: in tutte le varianti ora viene eseguito il rendering in un’unica griglia scorrevole (layout affiancati, sovrapposti o con ritorno a capo), sostituendo la visualizzazione una variante alla volta. Una singola barra delle azioni inferiore consolida la navigazione tra le varianti di test, lo zoom, il cambio del riquadro di visualizzazione (desktop/dispositivi mobili), il cambio della lingua, l’aggiunta di input di esempio, la generazione di varianti con IA, la scelta e il salvataggio di utenti simulati e l’importazione o l’esportazione di varianti. Rimuovendo la barra a sinistra e comprimendo i livelli di intestazione aggiuntivi, le anteprime avranno molto più spazio. L’opzione **Passa all’esperienza classica** nella barra delle azioni inferiore consente di ripristinare l’esperienza precedente in qualsiasi momento. [Ulteriori informazioni](../test-approve/simulate-content-variations.md)

  Data di disponibilità: 11 agosto 2026


