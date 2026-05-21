---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Note sulla versione di Adobe Journey Optimizer
hide: true
source-git-commit: 6f67786674f995422a5add1600d7f0dbfe915067
workflow-type: tm+mt
source-wordcount: '2835'
ht-degree: 18%

---


<!-- DRAFT — Topic-based layout exploration. All content is identical to release-notes.md (May '26). The only change is the grouping axis: topic > type. -->

# Note sulla versione {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novità"
>abstract="**Adobe Journey Optimizer** offre in modo continuo nuove funzionalità, miglioramenti a quelle esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese."

[!DNL Adobe Journey Optimizer] segue un modello di distribuzione continua, che consente ad Adobe di fornire nuove funzionalità, miglioramenti e correzioni su base regolare. Questo approccio consente un rollout scalabile e graduale delle funzionalità per garantire prestazioni e stabilità in tutti gli ambienti. A causa di questo modello, le note sulla versione vengono aggiornate prima del successivo rilascio mensile. Per informazioni dettagliate sul ciclo di rilascio e sulle fasi di disponibilità, consulta [Ciclo di rilascio di Journey Optimizer](releases.md).

[!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche sono disponibili nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.

>[!NOTE]
>
>Le funzionalità elencate in queste note sulla versione includono una **Data di disponibilità** che indica quando ogni modifica diventa accessibile nell&#39;ambiente. Le voci contrassegnate con **In arrivo** sono pianificate per il rilascio nei prossimi giorni o settimane. Le informazioni contenute in queste sezioni sono soggette a modifiche.

## Note sulla versione di maggio 2026 {#may-26-rn}

### Percorsi {#may-26-journeys}

In questa versione sono state aggiunte le seguenti funzionalità e miglioramenti ai percorsi. Ulteriori modifiche sono previste nei prossimi giorni o settimane. Vedere la sezione [In arrivo](#may-26-journeys-coming-soon) di seguito.

<table>
<thead>
<tr>
<th><strong>Frammenti di percorso (disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile creare <strong>frammenti di Percorso</strong> in Adobe Journey Optimizer. I frammenti di percorso sono set riutilizzabili di nodi di percorso che è possibile compilare una volta e rilasciare in qualsiasi percorso della sandbox. Che si tratti di un controllo di idoneità, di una logica di indirizzamento dei canali preferita o di una sequenza di benvenuto, i frammenti consentono ai team di spostarsi più rapidamente e rimanere coerenti, senza dover ogni volta ricostruire la stessa logica da zero.</p>
<p>Una volta creati, i frammenti vengono memorizzati in un <strong>Inventario frammenti</strong> dedicato e possono essere inseriti in qualsiasi percorso utilizzando l'attività <strong>Frammenti Percorso</strong>.</p>
<!--<p><img src="assets/do-not-localize/journey-fragments.gif"></p>-->
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/journey-fragments.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 13 maggio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Simulazione percorso (disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi impostare un percorso su <strong>Simulazione</strong>. Questa modalità consente di convalidare una logica utilizzando gli <strong>utenti simulati</strong>. Si tratta di profili temporanei creati appositamente per la simulazione, che consentono di eseguire liberamente i test senza dover gestire profili di test persistenti in Adobe Experience Platform.</p>
<p>Questa funzionalità è disponibile per tutta la clientela come disponibilità limitata con funzionalità essenziali.</p>
<p><img src="assets/do-not-localize/simulate-user.gif"></p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/simulate-journey.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 5 maggio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Ottimizzazione del percorso del percorso - Targeting (disponibilità generale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Utilizza il nuovo nodo <strong>Ottimizza</strong> per eseguire il targeting di tipi di pubblico specifici per determinare il percorso migliore per soddisfare i KPI incentrati sul business.</p>
<p>Questo strumento ti consente di sviluppare campagne di marketing più efficaci con una maggiore probabilità di risonanza a livello 1:1, di migliorare le attività di personalizzazione del marketing per i clienti e di migliorare i KPI critici di coinvolgimento dei clienti, come conversioni e ricavi.</p>
<p>Precedentemente disponibile in Disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti.</p>
<p>Data di disponibilità: 21 maggio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Arbitrato percorso - formule di classificazione (disponibilità generale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile utilizzare le formule per aumentare automaticamente i punteggi di priorità del percorso in base agli attributi del profilo cliente e ai fattori contestuali, in modo che i clienti possano accedere ai percorsi più rilevanti.</p>
<p>Precedentemente disponibile in Disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti.</p>
<p>Data di disponibilità: 21 maggio 2026</p>
</td>
</tr>
</tbody>
</table>

#### Disponibile a breve {#may-26-journeys-coming-soon}

Le seguenti funzionalità di percorso sono previste nei prossimi giorni o settimane. **Le informazioni seguenti sono soggette a modifiche.**

<table>
<thead>
<tr>
<th><strong>Assistente AI per espressioni di Percorso (Beta pubblico)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’Assistente IA ora funziona nell’editor di espressioni avanzate di percorso per convertire i prompt in linguaggio naturale in espressioni e logiche condizionali valide. Descrivi l’espressione che desideri creare e l’Assistente AI genera codice pronto all’uso che puoi applicare immediatamente o perfezionare tramite prompt di follow-up.</p>
<p>Questa funzionalità è disponibile per tutti i clienti come Beta pubblico.</p>
<!--<p><img src="assets/do-not-localize/expression-assistant.gif"></p>-->
<p>Data di disponibilità: 22 maggio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Simulazione percorso (disponibilità generale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Precedentemente rilasciata in Disponibilità limitata, la simulazione del Percorso è ora disponibile per tutti gli ambienti. Con questa versione di disponibilità generale, ora puoi utilizzare Journey Agent per generare utenti ed eventi simulati direttamente nel menu Simulazione.</p>
<p>Data di disponibilità: 1 giugno 2026</p>
</td>
</tr>
</tbody>
</table>

* **Completamento automatico per percorsi di pubblico di lettura non ricorrenti** - I **percorsi di pubblico di lettura** non ricorrenti passano ora automaticamente allo stato **Interrotto** una volta terminato l&#39;ultimo profilo attivo. In precedenza, questi percorsi rimanevano **Live** fino alla scadenza del timeout globale di 91 giorni, anche quando non vi scorrevano più profili. Con questo miglioramento, lo stato del percorso riflette lo stato di esecuzione effettivo non appena viene completato, mantenendo accurato l’inventario del percorso senza interventi manuali.

  Si noti che questo comportamento non si applica ai percorsi che includono nodi che causano periodi di attesa, ad esempio nodi di attesa, nodi di reazione o transizioni attivate da eventi. Questi percorsi rimangono soggetti al timeout globale standard di 91 giorni.

  Data di disponibilità: 21 maggio 2026

* **Autenticazione personalizzata basata su certificato nelle azioni personalizzate**. Le azioni personalizzate ora supportano l&#39;autenticazione personalizzata basata su certificato. Aggiungendo `subType: "certificateCredential"` a una configurazione di autorizzazione personalizzata, Journey Optimizer utilizza il certificato gestito di Adobe per firmare un&#39;asserzione client JWT e scambiarla per un token di accesso, senza richiedere segreto client. Progettato per le API aziendali che applicano la verifica dell’identità basata su certificato, come Azure Entra ID.

  Data di disponibilità: 21 maggio 2026

* **Personalizzazione basata su loop per dati relazionali** - L&#39;editor di personalizzazione ora supporta un blocco di loop che esegue iterazioni sulle raccolte relazionali, ad esempio ordini, account o prenotazioni, ed esegue il rendering di un blocco di contenuto per record all&#39;interno di un&#39;unica e-mail o SMS. Le raccolte vengono configurate tramite il selettore dati utilizzando token di personalizzazione, senza che sia necessaria la scrittura di espressioni.

  Data di disponibilità: 1 giugno 2026

* **Supporto di identificatori supplementari per tipi di pubblico esterni** - Gli identificatori supplementari nei percorsi sono ora supportati per i tipi di pubblico esterni, inclusi i tipi di pubblico importati da un file CSV e i tipi di pubblico creati con Federated Audience Composition. Puoi designare qualsiasi attributo di identità non di identità o di identità non di persona dal pubblico come ID supplementare, senza richiedere alcuna etichettatura schema.

  Data di disponibilità: 1 giugno 2026

### Campagne orchestrate {#may-26-oc}

In questa versione sono state aggiunte alle campagne orchestrate le funzionalità e i miglioramenti seguenti. Ulteriori modifiche sono previste nei prossimi giorni o settimane. Vedere la sezione [In arrivo](#may-26-oc-coming-soon) di seguito.

<table>
<thead>
<tr>
<th><strong>Campagne orchestrate concatenate</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile collegare le campagne orchestrate attivando una campagna orchestrata direttamente dall'<strong>attività finale</strong> di un'altra campagna orchestrata.</p>
<p>Questo consente di suddividere una logica di orchestrazione complessa in flussi più piccoli e riutilizzabili che possono essere chiamati da più campagne principali anziché ricostruiti ogni volta. Il payload passato in fase di runtime è disponibile per la segmentazione e la personalizzazione nella campagna a valle, in modo che ogni campagna collegata possa comportarsi in base al contesto ricevuto.</p>
<p><img src="assets/do-not-localize/oc-trigger.gif"></p>
<p>Per ulteriori informazioni, consulta la <a href="../orchestrated/trigger-orchestrated-campaign.md#signal-end">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 20 maggio 2026</p>
</td>
</tr>
</tbody>
</table>

* **Aggiungi collegamenti nell&#39;attività di arricchimento** - La funzionalità Aggiungi collegamento è ora disponibile nell&#39;attività di arricchimento per le campagne orchestrate. Ciò consente di creare una relazione diretta tra i dati della tabella di lavoro e le tabelle di database esistenti.

  Data di disponibilità: 20 maggio 2026

#### Disponibile a breve {#may-26-oc-coming-soon}

La seguente funzionalità di campagna orchestrata è prevista nei prossimi giorni o settimane. **Le informazioni seguenti sono soggette a modifiche.**

<table>
<thead>
<tr>
<th><strong>Targeting basato su file per campagne orchestrate (disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le campagne orchestrate ora supportano il caricamento di un file CSV o TXT direttamente nell’area di lavoro della campagna come pubblico di destinazione, senza prima acquisire il file in Adobe Experience Platform. I dati del file vengono utilizzati in fase di esecuzione e non vengono mantenuti come set di dati di Adobe Experience Platform. Durante l’impostazione del file, puoi definire le mappature di colonna, i tipi di dati, la gestione dei valori NULL e i criteri di errore per colonna. In questo modo sono supportate campagne di invio ad hoc o di elenco partner in cui non è possibile creare una pipeline di acquisizione completa.</p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<p>Data di disponibilità: 1 giugno 2026</p>
</td>
</tr>
</tbody>
</table>

### Campagne {#may-26-campaigns}

#### Disponibile a breve {#may-26-campaigns-coming-soon}

I seguenti miglioramenti della campagna sono attesi nei prossimi giorni o settimane. **Le informazioni seguenti sono soggette a modifiche.**

* **Avvisi del cliente per eventi del ciclo di vita della campagna** - I nuovi avvisi di sistema ora ti segnalano gli eventi chiave del ciclo di vita per le campagne attivate da API e da Azione. Iscriviti a livello di sandbox.

  Data di disponibilità: 1 giugno 2026

* **Escludi il campo di esecuzione predefinito nelle campagne**. Precedentemente disponibile a livello di percorso, ora puoi sovrascrivere il campo di esecuzione predefinito impostato a livello globale per le consegne e-mail, SMS e WhatsApp nei parametri della campagna.

  Data di disponibilità: 1 giugno 2026

### Funzione Decisioni {#may-26-decisioning}

In questa versione sono state aggiunte le seguenti funzionalità e miglioramenti a Decisioning. Ulteriori modifiche sono previste nei prossimi giorni o settimane. Vedere la sezione [In arrivo](#may-26-decisioning-coming-soon) di seguito.

<table>
<thead>
<tr>
<th><strong>Regole di decisione e ottimizzazione IA della formula di classificazione</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>[!DNL Adobe Journey Optimizer] ora utilizza l’intelligenza artificiale per rilevare le regole di decisioning e le formule di classificazione che possono essere semplificate. Nell’inventario, un indicatore rosso viene visualizzato su qualsiasi regola per la quale l’IA ha identificato un’opportunità di ottimizzazione. Facendo clic sull’indicatore, l’espressione originale viene visualizzata insieme alla versione suggerita dall’intelligenza artificiale. Da lì, puoi scaricare un file per rivedere il modo in cui i profili simulati vengono valutati da ogni versione e confermare che si comportano in modo identico, quindi sostituire l’espressione con quella ottimizzata.</p>
<p><img src="assets/do-not-localize/rule-ai.gif"></p>
<p>Per ulteriori informazioni, consulta la <a href="../start/ai-features.md#decisioning-optimization">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 5 maggio 2026</p>
</td>
</tr>
</tbody>
</table>

* **API del flusso di lavoro di migrazione Decisioning** - Il contratto API per la creazione di flussi di lavoro di analisi delle dipendenze e migrazione è stato aggiornato: passa **`request-level`** come **parametro query** nell&#39;URL della richiesta (`sandbox`, `offer` o `decision`). Il livello di richiesta non deve più essere inviato nel corpo del codice JSON. [Ulteriori informazioni](../experience-decisioning/decisioning-migration-api.md)

  Data di disponibilità: 6 maggio 2026

* **Frammenti di contenuto Adobe Experience Manager in Decisioning** - È ora possibile mappare i frammenti di contenuto Adobe Experience Manager agli elementi decisionali in Decisioning e sfruttarli all’interno dei criteri decisionali per fornire il frammento giusto al cliente giusto al momento giusto. [Ulteriori informazioni](../integrations/aem-fragments.md#aem-decisioning)

  Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.

  Data di disponibilità: 20 maggio 2026

#### Disponibile a breve {#may-26-decisioning-coming-soon}

La funzionalità Decisioning seguente è prevista per i prossimi giorni o settimane. **Le informazioni seguenti sono soggette a modifiche.**

<table>
<thead>
<tr>
<th><strong>Supporto per le decisioni nel canale Direct Mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi aggiungere i criteri di decisione ai percorsi e alle campagne di Direct Mail. I criteri di decisione sono contenitori per le offerte che sfruttano il motore di decisione per restituire in modo dinamico il contenuto migliore per ogni membro del pubblico. Direct Mail decisioning supporta anche casi di utilizzo di decisioni in batch, consentendo di esportare gli elementi di offerta corrispondenti per ogni profilo in un determinato pubblico Adobe Experience Platform.</p>
<!--<p><img src="assets/do-not-localize/exd-dm.gif"></p>-->
<p>Data di disponibilità: 1 giugno 2026</p>
</td>
</tr>
</tbody>
</table>

### Canale e-mail {#may-26-email}

In questa versione sono state aggiunte le seguenti funzionalità e miglioramenti al canale e-mail. Ulteriori modifiche sono previste nei prossimi giorni o settimane. Vedere la sezione [In arrivo](#may-26-email-coming-soon) di seguito.

<table>
<thead>
<tr>
<th><strong>Collegamenti diretti in E-mail designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi aggiungere collegamenti diretti ai contenuti delle e-mail tramite un’opzione dedicata in E-mail designer. Ciò garantisce che gli utenti vengano indirizzati direttamente verso i contenuti in-app corretti, anziché essere reindirizzati ai browser o agli app store, preservando il contesto e il coinvolgimento.</p>
<p><img src="assets/do-not-localize/deeplinks.gif"></p>
<p>Per ulteriori informazioni, consulta la <a href="../email/deeplinks.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 12 maggio 2026</p>
</td>
</tr>
</tbody>
</table>

#### Disponibile a breve {#may-26-email-coming-soon}

I seguenti miglioramenti del canale e-mail sono attesi nei prossimi giorni o settimane. **Le informazioni seguenti sono soggette a modifiche.**

* **Personalizzazione dei dettagli del mittente e-mail per destinatario e campagna** - Le campagne orchestrate ora supportano la personalizzazione dei campi dell&#39;intestazione e-mail, inclusi Nome mittente, Indirizzo mittente e Risposta, utilizzando gli attributi del profilo o i dati relazionali. Questo consente ai dettagli del mittente di riflettere l’advisor, la posizione o la filiale pertinente per ciascun destinatario, anziché instradare tutti gli invii tramite un unico indirizzo aziendale.

  I valori dell’intestazione possono essere impostati a livello di canale e sostituiti per campagna utilizzando dati contestuali per un controllo più preciso.

  Data di disponibilità: 1 giugno 2026

* **Testo formattato in campi frammento modificabili** - È ora possibile aggiungere testo formattato a frammenti personalizzabili utilizzati nel contenuto dell&#39;e-mail. Ad esempio, quando utilizzi il componente Testo come campo modificabile nel Designer e-mail, puoi formattare direttamente il contenuto (ad esempio, grassetto e corsivo) e inserire collegamenti ipertestuali.

  Data di disponibilità: 1 giugno 2026

* **Limita l&#39;interruzione dell&#39;ereditarietà nei frammenti** - Durante la creazione o la modifica di un frammento, ora puoi scegliere se modificarlo quando viene utilizzato nelle e-mail. Il blocco di un frammento ne garantisce la sincronizzazione ovunque appaia, impedendo modifiche locali che potrebbero violare gli standard del marchio o i requisiti di conformità. Questa impostazione può essere aggiornata in un secondo momento e può essere applicata a utilizzi futuri.

  Data di disponibilità: 21 maggio 2026

### Messaggistica mobile (SMS, MMS e RCS) {#may-26-mobile}

In questa versione sono state aggiunte le seguenti funzionalità e miglioramenti alla messaggistica mobile.

<table>
<thead>
<tr>
<th><strong>Nuovo canale di messaggi mobile e messaggistica RCS avanzata</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>SMS, MMS e RCS ora sono unificati in un'unica azione <strong>Mobile Message</strong> in Adobe Journey Optimizer, semplificando la gestione di tutti i tipi di messaggi mobili da un'unica posizione. Come parte di questo aggiornamento, ora è possibile creare messaggi RCS per rich media, incluse immagini, caroselli e azioni suggerite, direttamente in Journey Optimizer tramite una nuova esperienza di authoring nativa.</p>
<p>Per ulteriori informazioni, consulta la <a href="../mobile/get-started-mobile.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 20 maggio 2026</p>
</td>
</tr>
</tbody>
</table>

* **Conteggio caratteri** - È ora possibile utilizzare il conteggio caratteri per monitorare la lunghezza dei messaggi SMS in tempo reale. Consente di visualizzare quando un messaggio verrà suddiviso in più segmenti per gestire meglio la formattazione ed evitare aumenti imprevisti nei costi di invio. [Ulteriori informazioni](../mobile/create-mobile-message.md)

* **SMS in entrata verso un set di dati personalizzato**: nelle **credenziali API SMS**, indirizza gli **SMS in entrata** verso un **set di dati dell’evento esperienza personalizzato e abilitato per i profili** selezionato, anziché solo verso il set di dati di tracciamento predefinito. [Ulteriori informazioni](../mobile/mobile-webhook.md)

* **Miglioramento dell’interfaccia del webhook**: durante la configurazione dei webhook SMS, l’interfaccia utente include ora una guida di configurazione integrata con esempi pratici, che semplifica l’allineamento dei payload dei provider e la risoluzione dei problemi senza bisogno di uscire dal flusso di configurazione. [Ulteriori informazioni](../mobile/mobile-webhook.md)

### Canale WhatsApp {#may-26-whatsapp}

In questa versione sono stati aggiunti i seguenti miglioramenti al canale WhatsApp.

* **Supporto e monitoraggio dei pulsanti WhatsApp** - I modelli WhatsApp ora supportano **Risposta rapida**, **Call to action - URL** e **Call to action - telefono**, **Copia codice** non supportati. Journey Optimizer invia i pulsanti supportati e tiene traccia delle interazioni insieme al reporting degli altri canali.

* **Dati contestuali del canale WhatsApp** - Journey Optimizer ora acquisisce dati di interazione aggiuntivi restituiti dal canale WhatsApp e li memorizza nel **Set di dati AJO EmailTrackingExperienceEvent** nel gruppo di campi `whatsAppChannelContext`.

  +++ Campi acquisiti per la creazione e l’analisi del coinvolgimento del pubblico WhatsApp

   * **`messageType`** - Tipo di messaggio WhatsApp (ad esempio `templateBased`, `response`)
   * **`inboundMessage`** - Contenuto risposta in entrata (ad esempio `stop`, `start`, `subscribe`)
   * **`inboundNumber`** - ID mittente in cui è stato ricevuto il messaggio in entrata
   * **`channelType`** - Categoria canale (`Utility`, `Marketing` o `Promotional`)
   * **`profileNumber`** - Numero di telefono da cui è stato ricevuto il messaggio in entrata
   * **`origTimestamp`** - Timestamp originale da Meta / WhatsApp
   * **`status`** - Stato della consegna, inclusi feedback del provider standardizzato (`sent`, `delivered`, `bounce`, `error`, `delay`, `duplicate`, `denylist`, `exclude` o `unknown`) e messaggio di stato del provider non elaborato
   * **`reactionEvent`** - Contenuto della risposta dell&#39;utente: emoji per le reazioni o testo del messaggio per le risposte a un messaggio specifico
   * **`reactionMessageID`** - ID del messaggio originale a cui viene inviata la risposta
   * **`reactionActionName`** - Tipo di azione di risposta (`react`, `unreact` o `reply`)
   * **`interactiveSelectedTitle`** - Titolo selezionato dall&#39;utente da un messaggio interattivo WhatsApp
   * **`interactiveType`** - Tipo di messaggio interattivo (`list reply`, `button reply` o `button`)
   * **`interactiveSelectedDescription`** - Descrizione dell&#39;opzione interattiva WhatsApp selezionata
   * **`interactiveSelectedID`** - ID dell&#39;opzione selezionata da WhatsApp

  +++

### Contenuti e integrazioni {#may-26-content}

In questa versione sono state aggiunte le seguenti funzionalità e miglioramenti per la gestione dei contenuti e le integrazioni.

<table>
<thead>
<tr>
<th><strong>Selettore Contenuto verificato</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ora utilizza il selettore <strong>Contenuto verificato</strong>, una finestra modale unificata per la selezione sia di Experience Manager Assets che di frammenti di contenuto. Il nuovo selettore include:</p>
<ul>
<li><strong>Esplorazione, ricerca e filtro</strong> in tutte le risorse e i frammenti.</li>
<li><strong>Ricerca semantica AI</strong>: descrive ciò di cui hai bisogno in linguaggio semplice, ad esempio "caffè in montagna", per far emergere risorse contestualmente rilevanti in base al significato e al contenuto, non solo corrispondenze testuali. Sono supportate anche le query multilingue.</li>
<li><strong>Caricamento breve</strong>: carica un documento di marketing per rendere automaticamente visibili le risorse che sono allineate al contesto della campagna in base al contenuto e ai requisiti.</li>
<li><strong>Rappresentazioni Dynamic Media</strong>: seleziona e applica le rappresentazioni immagine per le risorse dinamiche senza uscire dal selettore.</li>
</ul>
<p>Per ulteriori informazioni, consulta la <a href="../integrations/aem-content-advisor.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 19 maggio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integrazioni (disponibilità generale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La funzione <b>Integrazioni</b> consente di connettere origini dati di terze parti direttamente ad Adobe Journey Optimizer. Semplificando il modo in cui estrai i dati esterni e i <b>contenuti componibili</b>, questa funzione rende più facile consegnare messaggi personalizzati e dinamici su tutti i canali.</p>
<p>Precedentemente rilasciata in Beta, questa funzionalità è ora disponibile per tutti gli ambienti.</p>
<p>Per ulteriori informazioni, consulta la <a href="../integrations/integrations.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 4 maggio 2026</p>
</td>
</tr>
</tbody>
</table>

* **Accesso all&#39;archivio tra più organizzazioni nel selettore Assets** - È ora possibile selezionare facilmente le risorse dagli archivi tra più organizzazioni direttamente nel selettore risorse di Adobe Experience Manager.

### Amministrazione {#may-26-admin}

#### Disponibile a breve {#may-26-admin-coming-soon}

I seguenti miglioramenti della somministrazione sono attesi nei prossimi giorni o settimane. **Le informazioni seguenti sono soggette a modifiche.**

* **Cartelle per percorsi e campagne** - È ora possibile organizzare i percorsi e le campagne in cartelle per migliorare la navigazione e la gestione nell&#39;interfaccia.

  Data di disponibilità: 21 maggio 2026

* **Il set di dati dell&#39;evento di feedback del messaggio sta passando all&#39;acquisizione in batch** - `AJO Message Feedback Event Dataset` sta passando dallo streaming alla modalità di acquisizione in batch. Questa modifica assicura che l’acquisizione dei dati non superi i limiti di acquisizione dello streaming. Se utilizzi questo set di dati nei rapporti di Customer Journey Analytics o esegui query su di esso, prevedi un aumento della latenza dei dati fino a 2 ore.

  Data di disponibilità: 1 giugno 2026

### Generazione dei rapporti {#may-26-reporting}

#### Disponibile a breve {#may-26-reporting-coming-soon}

Nei prossimi giorni o settimane sono previsti i seguenti miglioramenti per quanto riguarda la generazione di rapporti. **Le informazioni seguenti sono soggette a modifiche.**

* **Escludi clic bot per rapporti e-mail e SMS** - Sono ora disponibili nuove metriche stimate per aiutare a filtrare le interazioni non umane (bot) dai rapporti e-mail e SMS. Questi includono click stimati, tassi di click-through (CTR) e tassi di click-to-open (CTOR), che forniscono una visione più accurata del coinvolgimento reale dei clienti. Le metriche esistenti rimangono invariate e possono essere utilizzate insieme al reporting corrente per migliorare l’analisi.

  Data di disponibilità: 1 giugno 2026
