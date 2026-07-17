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
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2: id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: d00e9f03-e50b-4162-b143-0c0817c937c2id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 423db08a3c4c5a8d9540fa0c8e03e28ca36ca299
workflow-type: tm+mt
source-wordcount: 3064
ht-degree: 74%

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

## Aggiornamenti del 26 luglio {#july-26-updates}

### Nuove funzionalità {#july-26-new-capabilities}

<table>
<thead>
<tr>
<th><strong>Verifica dei contenuti in E-mail designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ora include la convalida tecnica automatizzata direttamente in E-mail designer, che consente di individuare i problemi di HTML e CSS prima dell’invio.</p>
<p>I controlli coprono gli elementi non supportati, ad esempio i tag <code>&lt;script&gt;</code> e <code>&lt;base&gt;</code>, i div vuoti che possono compromettere il layout in Microsoft Outlook, i tag HTML meta refresh e le soglie di dimensioni CSS o HTML che causano errori di rendering in Gmail.</p>
<p>I risultati vengono visualizzati come errori, avvertenze o avvisi informativi direttamente nel pannello di authoring, con dettagli contestuali e correzioni con un solo clic, se disponibili, in modo che i problemi possano essere risolti senza uscire dall’editor.</p>
<p>Precedentemente disponibile in disponibilità limitata, questa funzionalità è ora disponibile per tutta la clientela.</p>
<p><img src="assets/do-not-localize/content-check.gif"></p>
<p>Per ulteriori informazioni, consulta la <a href="../email/content-check.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 16 luglio 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Targeting basato su file nelle campagne orchestrate</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le campagne orchestrate ora supportano il caricamento di un <strong>file CSV o TXT</strong> direttamente nell'area di lavoro della campagna come pubblico di destinazione, senza prima acquisire il file in Adobe Experience Platform. I dati del file vengono utilizzati in fase di esecuzione e non vengono mantenuti come set di dati di Adobe Experience Platform. Durante l’impostazione del file, puoi definire le mappature di colonna, i tipi di dati, la gestione dei valori NULL e i criteri di errore per colonna. Le righe che non superano la convalida vengono rifiutate e registrate prima dell’esecuzione della campagna, mantenendo il pubblico pulito senza la pre-elaborazione manuale. Questa funzione è particolarmente adatta per campagne di invio ad hoc o di elenco di partner in cui non è pratico creare una pipeline di acquisizione completa.</p>
<p>Per ulteriori informazioni, consulta la <a href="../orchestrated/activities/load-file.md">documentazione dettagliata</a>.</p>
<p> Data di disponibilità: 6 luglio 2026</p>
</td>
</tr>
</tbody>
</table>

### Miglioramenti {#july-26-improvements}

* **Nuovi strumenti del server AJO MCP** - Il server MCP [!DNL Adobe Journey Optimizer] espone ora cinque ulteriori **strumenti di configurazione del canale** di sola lettura, consentendo di eseguire query sulle configurazioni del canale, sulle risorse di supporto e sulle azioni di marketing direttamente dall&#39;assistente AI. È ora possibile utilizzare **Elenca configurazioni canale** (su tutti i canali AJO), **Ottieni configurazione canale**, **Elenca risorse configurazione**, **Ottieni risorsa configurazione** e **Elenca azioni marketing**. [Ulteriori informazioni](../integrations/ajo-mcp.md#mcp-tools)

  Data di disponibilità: 9 luglio 2026


### Miglioramenti dell’usabilità {#july-26-usability}

I seguenti miglioramenti a livello di usabilità sono stati rilasciati a luglio 2026.

#### Gestione dei contenuti

* **Scelte rapide per l&#39;avvio nell&#39;inventario dei frammenti** - È ora possibile accedere rapidamente alle azioni comuni dall&#39;elenco dei frammenti utilizzando il pulsante **[!UICONTROL Altre azioni]**. Le scelte rapide disponibili includono la modifica del frammento, l’apertura dei relativi dettagli e l’eliminazione della versione bozza. [Ulteriori informazioni](../content-management/manage-fragments.md#quick-launch-fragments)

  ![](../content-management/assets/fragment-quick-launch.png)

* **Scelte rapide per l&#39;avvio nell&#39;inventario dei modelli** - Il pulsante **[!UICONTROL Altre azioni]** nell&#39;elenco dei modelli di contenuto consente ora di accedere rapidamente alle azioni più comuni: modifica dei dettagli dei modelli, simulazione del contenuto ed eliminazione di un modello. Per i modelli e-mail, con collegamenti aggiuntivi puoi modificare l’oggetto e il corpo dell’e-mail, visualizzare o inviare una bozza, eseguire un rapporto sulla posta indesiderata ed eseguire il rendering dell’e-mail. [Ulteriori informazioni](../content-management/access-content-templates.md#quick-launch-templates)

  ![](../content-management/assets/content-template-quick-launch.png)

#### Percorsi

È stata introdotta una **nuova interfaccia utente** per l&#39;area di lavoro di percorso, che offre prestazioni migliori per i percorsi di grandi dimensioni, layout automatico per una migliore leggibilità e un&#39;esperienza di authoring guidata.

![](../building-journeys/assets/journey-new-canvas.png)

Per passare alla nuova interfaccia utente, fai clic sul pulsante **[!UICONTROL Nuova esperienza]**. Questa impostazione viene salvata a livello di percorso, pertanto per impostazione predefinita il percorso viene riaperto nella nuova esperienza. Per ripristinare, fai clic su **[!UICONTROL Esperienza precedente]**. [Ulteriori informazioni](../building-journeys/using-the-journey-designer.md#canvas-capabilities)

![](../building-journeys/assets/journey-new-experience-switch.png)

Data di disponibilità: 16 luglio 2026


## Note sulla versione di giugno 2026 {#june-26-rn}

### Percorsi {#june-26-journeys}

In questa versione sono stati aggiunti i seguenti miglioramenti ai percorsi e le seguenti funzioni. Ulteriori modifiche sono previste nei prossimi giorni o settimane.


<table>
<thead>
<tr>
<th><strong>Simulazione del percorso (disponibilità generale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi impostare il percorso su Simulazione. Questa modalità consente di convalidare la logica utilizzando utenti simulati. Si tratta di profili temporanei creati appositamente per la simulazione, che consentono di eseguire liberamente i test senza dover gestire profili di test persistenti in Adobe Experience Platform. </p>
<p>Precedentemente rilasciata in disponibilità limitata, la Simulazione del percorso è ora disponibile per tutti gli ambienti. Con questa versione in disponibilità generale, ora puoi utilizzare l’Agente Journey per generare utenti ed eventi simulati direttamente nel menu Simulazione.</p>
<p><img src="assets/do-not-localize/journey-simulation.gif"></p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/simulate-journey-gs.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 9 giugno 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Frammenti di percorso (disponibilità generale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi creare <strong>frammenti del percorso</strong> in Adobe Journey Optimizer. I frammenti del percorso sono set riutilizzabili di nodi di percorso che puoi creare una volta e inserire in qualsiasi percorso all’interno della sandbox. Che si tratti di un controllo di idoneità, di una logica di indirizzamento dei canali preferita o di una sequenza di benvenuto, i frammenti consentono ai team di spostarsi più rapidamente e rimanere coerenti, senza dover ricostruire ogni volta la stessa logica da zero.</p>
<p>Una volta creati, i frammenti vengono conservati in un apposito <strong>Inventario dei frammenti</strong> e possono essere inseriti in qualsiasi percorso utilizzando l’attività <strong>Frammenti del percorso</strong>.</p>
<p>Precedentemente disponibile in disponibilità limitata, questa funzionalità è ora disponibile per tutta la clientela. I frammenti di percorso supportano anche <strong>Strumenti sandbox</strong>, che consentono di creare pacchetti ed esportare frammenti tra sandbox diverse.</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/journey-fragments.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 9 giugno 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Ottimizzazione del percorso - Targeting (disponibilità generale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’<strong>attività Ottimizza</strong> ora supporta <strong>Regole di targeting</strong> che consentono di definire criteri specifici che i clienti devono soddisfare per qualificarsi per un determinato percorso, in base ai segmenti di pubblico o agli attributi di profilo.</p>
<p>A differenza della sperimentazione, in cui la clientela viene assegnata in modo casuale ai percorsi, il targeting utilizza una logica deterministica per garantire che il pubblico o il profilo cliente appropriato venga indirizzato al percorso previsto.</p>
<p>Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p><img src="assets/do-not-localize/optimize.gif"></p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/path-targeting.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 8 giugno 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Assistente IA per espressioni del percorso (Beta pubblica)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’Assistente IA ora funziona nell’editor di espressioni avanzato del percorso per convertire i prompt in linguaggio naturale in espressioni valide e logica condizionale. Descrivi l’espressione che desideri creare e l’Assistente IA genererà un codice pronto all’uso che potrai applicare immediatamente o perfezionare tramite i prompt di follow-up.</p>
<p>Questa funzionalità è disponibile per tutta la clientela come versione Beta pubblica.</p>
<p><img src="assets/do-not-localize/expression-assistant.gif"></p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/expression/generate-expression.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 3 giugno 2026</p> 
</td>
</tr>
</tbody>
</table>


* [!BADGE Obsolescenza]{type=Negative} **I tipi di pubblico batch sono stati dichiarati obsoleti nel nodo Qualificazione del pubblico**. A partire dal **agosto 2026**, Journey Optimizer bloccherà la pubblicazione per qualsiasi percorso utilizzando un pubblico batch in un nodo **Qualificazione del pubblico**. Nell’area di lavoro del percorso è già presente un avviso di convalida. I percorsi live esistenti non vengono interessati. I percorsi nuovi, in bozza e duplicati che includono questa configurazione devono essere aggiornati prima di agosto 2026. Utilizza un pubblico in streaming nel nodo Qualificazione del pubblico o passa a un&#39;attività **Read Audience**. [Scopri come eseguire la migrazione dei percorsi](../building-journeys/aq-batch-audiences-migration.md)

* **Interrompere direttamente un percorso in pausa** - È ora possibile interrompere un percorso direttamente dallo stato **In pausa**. In precedenza, era necessario riprendere un percorso in pausa in **Live** prima di poterlo arrestare. [Ulteriori informazioni](../building-journeys/journey-pause.md#stop-close-paused)

  Data di disponibilità: 18-22 giugno 2026

* **Supporto di identificatori supplementari per tipi di pubblico esterni**: gli identificatori supplementari nei percorsi sono ora supportati per i tipi di pubblico esterni, inclusi quelli importati da un file CSV e quelli creati con la composizione di pubblico federato. Puoi designare qualsiasi attributo non di identità o di identità non di persona del pubblico come ID supplementare; non è richiesta alcuna etichettatura schema. [Ulteriori informazioni](../building-journeys/supplemental-identifier.md)

  Data di disponibilità: 11 giugno 2026

* **Interruzione automatica per percorsi Leggi pubblico non ricorrenti**: i percorsi **Leggi pubblico** non ricorrenti eseguono ora una transizione in automatico allo stato **Interrotto** una volta terminato l’ultimo profilo attivo. In precedenza, questi percorsi rimanevano **Live** fino alla scadenza del timeout globale di 91 giorni, anche quando non vi scorrevano più profili. Con questo miglioramento, lo stato del percorso riflette lo stato di esecuzione effettivo non appena viene completato, mantenendo accurato l’inventario del percorso senza interventi manuali.

  Si noti che questo comportamento non si applica ai percorsi che includono nodi che causano periodi di attesa, ad esempio nodi Attendi, nodi Reazione o transizioni attivate da eventi. Questi percorsi rimangono soggetti al normale timeout globale di 91 giorni. [Ulteriori informazioni](../building-journeys/end-journey.md#auto-stop-non-recurring)

  Data di disponibilità: 9 giugno 2026

* **Autenticazione personalizzata basata sui certificati nelle azioni personalizzate** - Le azioni personalizzate ora supportano l’autenticazione personalizzata basata su certificato. Aggiungendo `subType: "certificateCredential"` a una configurazione di autorizzazione personalizzata, Journey Optimizer utilizza il certificato gestito di Adobe per firmare un’asserzione client JWT e scambiarla con un token di accesso, senza richiedere alcun segreto client. Progettato per le API aziendali che applicano la verifica dell’identità basata sui certificati, ad esempio Microsoft Entra ID. [Ulteriori informazioni](../datasource/external-data-sources.md#certificate-credential)

  Data di disponibilità: 4 giugno 2026

* **Limite percorso live aumentato e nuovi guardrail**: è ora possibile avere fino a **200 percorsi attivi**, limite aumentato rispetto al precedente di 100. [Ulteriori informazioni](../start/guardrails.md#journeys-guardrails-journeys)

  Data di disponibilità: 18 giugno 2026. Questa funzionalità verrà gradualmente implementata in tutte le aree geografiche nei prossimi giorni.


+++ Disponibile a breve: **le informazioni riportate di seguito sono soggette a modifiche.**

* **Date di inizio e di fine nell’intestazione del percorso**: quando le date di inizio e/o di fine sono configurate in un percorso attivo, ora vengono visualizzate nell’**intestazione del percorso** accanto al badge di stato live. L’etichetta visualizzata si adatta a seconda che ogni data sia imminente o già passata.

+++

### Campagne orchestrate {#june-26-oc}

In questa versione sono state aggiunte alle campagne orchestrate le funzioni e i miglioramenti seguenti.

* **Personalizzazione basata su loop per dati relazionali** - L&#39;editor di personalizzazione ora supporta un blocco di loop che esegue iterazioni sulle raccolte relazionali, ad esempio ordini, account o prenotazioni, ed esegue il rendering di un blocco di contenuto per record all&#39;interno di un&#39;unica e-mail o SMS. Le raccolte vengono configurate tramite il selettore dati utilizzando token di personalizzazione, senza che sia necessaria la scrittura di espressioni. [Ulteriori informazioni](../orchestrated/add-personalization.md#enrichment-collections)

  Data di disponibilità: 26 giugno 2026

### Funzione Decisioni {#june-26-decisioning}

In questa versione sono state aggiunte alla funzione Decisioni le funzionalità e i miglioramenti seguenti.

<table>
<thead>
<tr>
<th><strong>Supporto della funzione Decisioni nel canale direct mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi aggiungere i criteri di decisione in percorsi e campagne direct mail. I criteri di decisione sono contenitori per le offerte che sfruttano il motore della funzione Decisioni per restituire in modo dinamico il contenuto migliore per ogni membro del pubblico. La funzione Decisioni di direct mail supporta anche casi d’uso di decisioni in batch, consentendo di esportare gli elementi di offerta corrispondenti per ogni profilo in un determinato pubblico di Adobe Experience Platform. </p>
<p><img src="assets/do-not-localize/exd-dm.gif"></p>
<p>Per ulteriori informazioni, consulta la <a href="../experience-decisioning/use-decision-policy.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 3 giugno 2026</p>
</td>
</tr>
</tbody>
</table>

* **Sfruttare i frammenti di contenuto di Adobe Experience Manager in Decisioning** - È ora possibile mappare i frammenti di contenuto di Adobe Experience Manager agli elementi decisionali in Decisioning e sfruttarli all&#39;interno dei criteri decisionali per fornire il frammento giusto al cliente giusto al momento giusto. Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale). [Ulteriori informazioni](../experience-decisioning/fragments-decision-policies.md)

  Data di disponibilità: 18 giugno 2026

### Gestione dei contenuti {#june-26-content}

In questa versione sono state aggiunte le seguenti funzionalità e miglioramenti alla gestione dei contenuti.

<table>
<thead>
<tr>
<th><strong>Simulare varianti di contenuto: generazione di varianti IA e di esperienza aggiornate</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sono ora disponibili due aggiornamenti per il flusso di lavoro <strong>Simula contenuto</strong>:</p>
<ul>
<li><strong>Nuovo percorso predefinito</strong>: facendo clic su <strong>Simula contenuto</strong>, ora viene aperta l’esperienza <strong>Simula varianti di contenuto</strong> per impostazione predefinita. Da una singola schermata, puoi aggiungere input di esempio manualmente o da un file CSV/JSON, riutilizzare gli utenti simulati, visualizzare in anteprima il rendering e inviare bozze. Per visualizzare in anteprima con i profili di test di Adobe Experience Platform, inviare bozze con i dati del profilo di test o controllare il rendering della casella in entrata e i rapporti di posta indesiderata, fai clic su <strong>Simula contenuto</strong>, quindi seleziona <strong>Simula contenuto (profili AEP)</strong> dal menu a discesa.</li>
<li><strong>Varianti di contenuto generate dall’IA</strong>: nell’esperienza <strong>Simula varianti di contenuto</strong>, fai clic su <strong>Genera</strong> per utilizzare l’IA per creare automaticamente varianti di contenuto. Il sistema analizza il messaggio, rileva i campi di personalizzazione e i rami condizionali e inserisce valori realistici in modo da poter convalidare il rendering senza creare manualmente ogni variante.</li>
</ul>
<p>Per ulteriori informazioni, consulta la <a href="../test-approve/simulate-sample-input.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 9 giugno 2026</p>
</td>
</tr>
</tbody>
</table>


### Canale e-mail {#june-26-email}

In questa versione sono stati aggiunti i seguenti miglioramenti al canale e-mail.

* **Crittografia dei parametri URL**: ora è possibile crittografare i parametri URL nei collegamenti alle pagine di destinazione e di tracciamento aggiunti ai messaggi e-mail. In questo modo viene fornito un ulteriore livello di sicurezza per i dati dei parametri sensibili. Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale). [Ulteriori informazioni](../personalization/url-parameter-encryption.md)

  Data di disponibilità: 1° giugno 2026

* **Nuove autorizzazioni per il registro delle chiavi**: sono ora necessarie due nuove autorizzazioni per accedere e gestire le chiavi necessarie per la crittografia dei parametri URL: **Gestisci registro chiavi** e **Visualizza registro chiavi**. [Ulteriori informazioni](../administration/high-low-permissions.md#administration-permissions)

  Data di disponibilità: 1° giugno 2026

<table>
<thead>
<tr>
<th><strong>Ottimizzazione delle dimensioni delle e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ora include un’opzione per ridurre le dimensioni dell’e-mail HTML eliminando spazi vuoti non necessari, commenti e codice ridondante, senza influire sul rendering dell’e-mail.</p>
<p>In questo modo è possibile migliorare la recapitabilità dei messaggi evitando soglie di dimensione utilizzate da alcuni provider di posta elettronica per contrassegnare o rifiutare i messaggi e ridurre i tempi di caricamento per i destinatari.</p>
<p><img src="assets/do-not-localize/email-size-optimization.gif"></p>
<p>Per ulteriori informazioni, consulta la <a href="../email/create-email.md#optimize-html-size">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 26 giugno 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Rich text nei campi modificabili per i frammenti</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi aggiungere Rich text a frammenti personalizzabili utilizzati nel contenuto delle e-mail.</p>
<p>Ad esempio, quando utilizzi il componente Testo come campo modificabile in E-mail designer, puoi formattare direttamente il contenuto (ad esempio, grassetto e corsivo) e inserire collegamenti ipertestuali.</p>
<p><img src="assets/do-not-localize/rich-text-editable-fields.gif"></p>
<p>Per ulteriori informazioni, consulta la <a href="../content-management/customizable-fragments.md#rich-text-visual">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 19 giugno 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Verifica dei contenuti in E-mail designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ora include la convalida tecnica automatizzata direttamente in E-mail designer, che consente di individuare i problemi di HTML e CSS prima dell’invio.</p>
<p>I controlli coprono gli elementi non supportati, ad esempio i tag <code>&lt;script&gt;</code> e <code>&lt;base&gt;</code>, i div vuoti che possono compromettere il layout in Microsoft Outlook, i tag HTML meta refresh e le soglie di dimensioni CSS o HTML che causano errori di rendering in Gmail.</p>
<p>I risultati vengono visualizzati come errori, avvertenze o avvisi informativi direttamente nel pannello di authoring, con dettagli contestuali e correzioni con un solo clic, se disponibili, in modo che i problemi possano essere risolti senza uscire dall’editor.</p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<p><img src="assets/do-not-localize/content-check.gif"></p>
<p>Per ulteriori informazioni, consulta la <a href="../email/content-check.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 18 giugno 2026</p>
</td>
</tr>
</tbody>
</table>

* **Convertitore HTML/immagine avanzato**: è ora disponibile una nuova versione della funzione di conversione da immagine a HTML, che offre una precisione migliorata nella generazione di HTML. Questo aggiornamento sfrutta modelli LLM di livello superiore per fornire un output HTML più preciso e affidabile dagli input delle immagini.

  Data di disponibilità: 18 giugno 2026

### Contenuti e integrazioni {#june-26-integration}

In questa versione sono stati aggiunti i miglioramenti e le funzionalità seguenti per la gestione dei contenuti e le integrazioni.

<table>
<thead>
<tr>
<th><strong>Miglioramenti ai frammenti di contenuto Adobe Experience Manager in Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Questa versione apporta diversi miglioramenti per rendere i <strong>frammenti di contenuto di Adobe Experience Manager</strong> più utilizzabili, più governabili e più pronti per la produzione nei flussi di lavoro di authoring di Journey Optimizer:</p>
<ul>
<li>Journey Optimizer ora supporta il recupero di frammenti di contenuto da più configurazioni di Adobe Experience Manager, inclusi i livelli di pubblicazione autenticata, di pubblicazione e di authoring.</li>
<li>Una volta selezionato un frammento, il relativo contesto viene mantenuto per tutto il messaggio, consentendo agli autori di riutilizzare i campi del frammento in blocchi di contenuto senza effettuare una nuova selezione.</li>
<li>In Journey Optimizer è stata introdotta una nuova pagina di elenco dei frammenti di contenuto dedicati per migliorare la gestione del ciclo di vita; gli utenti possono identificare frammenti non sincronizzati e attivare sincronizzazioni manuali per rimanere aggiornati.</li>
<li>Il supporto per le impostazioni locali e le varianti ora consente ai marketer di utilizzare versioni alternative dello stesso frammento di contenuto in modo più mirato.</li>
<li>Ora puoi accedere in modo flessibile ai contenuti Adobe Experience Manager da Adobe Journey Optimizer. Questa versione introduce la possibilità di <strong>passare all’archivio di origine</strong> per i frammenti di contenuto utilizzati nei percorsi e nelle campagne.</li>
<li>Ora compatibile con <b>Managed Services</b>, puoi visualizzare, accedere e utilizzare i frammenti di contenuto di Adobe Experience Manager direttamente in Journey Optimizer per la personalizzazione. È sufficiente aggiungere l’URL dell’archivio Adobe Experience Manager Managed Services nelle impostazioni di configurazione come configurazione unica.</li>
</ul>
<p>Per ulteriori informazioni, consulta la <a href="../integrations/aem-fragments-gs.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 18 giugno 2026</p>
</td>
</tr>
</tbody>
</table>

<!--
+++ Coming soon — **Information below is subject to change.**

<table>
<thead>
<tr>
<th><strong>AI assistant integration with Adobe Experience Manager Asset Essentials</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The AI Assistant now automatically fetches <b>brand-approved images</b> directly from your Adobe Experience Manager Assets when generating Emails, Web pages, and Push notifications. This eliminates the need to manually search the Assets or rely on generic AI fallbacks, ensuring every visual is perfectly accurate and brand-compliant.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>AI Assistant for content generation enhancements</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>This release improves the <strong>AI Assistant</strong> content generation experience with stronger image editing, more reliable brand extraction, and content authenticity support in the image flow:</p>
<ul>
<li><strong>AI image editing</strong> is now available in the image generation flow, including Firefly third-party model support, so you can refine source images without leaving the assistant.</li>
<li><strong>Brand signal extraction</strong> delivers higher-quality results. When selected pages lack sufficient signal, improved fallbacks now populate colors, typography, writing guidelines, and other brand attributes.</li>
<li><strong>Web-based brand extraction</strong> is more reliable. Improved timeout handling helps prevent slow pages, popups, and cookie banners from blocking extraction.</li>
<li><strong>Content authenticity (CAI)</strong> is now supported in the image flow. This release also fixes reference image upload issues and improves handling for images without an existing C2PA manifest.</li>
</ul>
</td>
</tr>
</tbody>
</table>

+++
-->

### Generazione di rapporti {#june-26-reporting}

In questa versione sono stati aggiunti i seguenti miglioramenti al reporting.

* **Nuove metriche di clic stimate per il reporting delle e-mail** - Per fornire una visualizzazione più accurata del coinvolgimento reale dei clienti, sono ora disponibili nuove metriche stimate per Percorsi, campagne e rapporti sui canali.

  * **CTR stimato** (tasso di click-through): calcolato come numero di clic stimato rispetto al numero totale di messaggi consegnati.

  * **CTOR stimato** (tasso di clic per apertura): calcolato come clic stimati rispetto al numero totale di aperture stimate.

  Data di disponibilità: 25 giugno 2026

### Amministrazione {#june-26-administration}

In questa versione sono stati aggiunti i seguenti miglioramenti per l’amministrazione e la gestione dei dati.

* [!BADGE Importante]{type=Informative} **Il set di dati evento di feedback del messaggio AJO sta passando all’acquisizione in batch**: il **set di dati evento di feedback del messaggio AJO** sta passando dall’acquisizione in streaming a quella in batch. Di conseguenza, per questo set di dati è prevista una latenza massima fino a 2 ore. Se hai creato rapporti in Customer Journey Analytics o eseguito query utilizzando questo set di dati, tieni conto di questo aumento della latenza in futuro. [Ulteriori informazioni](../data/datasets-query-examples.md#message-feedback-event-dataset)

  Data di disponibilità: 10 giugno 2026

* **Avvisi del cliente per eventi del ciclo di vita della campagna** - I nuovi avvisi di sistema ora ti segnalano gli eventi chiave del ciclo di vita per le campagne Azione e quelle attivate dall’API. Abbonati a livello di sandbox. [Ulteriori informazioni](../reports/alerts.md)

  Data di disponibilità: 1° giugno 2026

<!--
+++ Coming soon — **Information below is subject to change**

* **Web Application Firewall (WAF) IP whitelisting** - Adobe Journey Optimizer now supports Web Application Firewall (WAF) IP whitelisting for landing pages, enabling organizations to enforce that all incoming requests are routed exclusively through their configured WAF infrastructure. With this enhancement, customers can configure Journey Optimizer to reject any direct requests that bypass the WAF layer, ensuring that security policies defined in tools such as Imperva are consistently applied. This capability strengthens the security posture for enterprises with strict network access requirements, giving them full control over the traffic flow to their AJO-hosted landing pages.
  
  Availability date: Late June, 2026

+++
-->

### Messaggistica per dispositivi mobili (SMS, MMS, RCS e LINE) {#june-26-mobile}

In questa versione sono disponibili i seguenti miglioramenti alla messaggistica per dispositivi mobili.

* **Clic univoci per rapporti SMS**: è stato introdotto un nuovo modulo **Clic univoci** nei rapporti SMS, che offre lo stesso livello di tracciamento granulare delle prestazioni per gli SMS, attualmente disponibile per i rapporti e-mail.

* **SMS - Visualizzazione delle metriche di utilizzo**:-per la clientela che acquista SMS direttamente tramite Adobe Journey Optimizer, è stata introdotta una nuova **dashboard di utilizzo degli SMS**. Ora puoi visualizzare e tenere traccia degli ultimi 90 giorni di metriche di invio dei messaggi, suddivisi per messaggi MO (Mobile Originated) e MT (Mobile Terminated). Questi dati sono disponibili anche per il download tramite CSV, fornendo una maggiore visibilità e un maggiore controllo sulla spesa SMS. [Ulteriori informazioni](../mobile/sms-usage-report.md)

* **Clic stimati per rapporto SMS** - È ora disponibile una nuova metrica Clic stimati in Percorsi, campagne e rapporti Canale per e-mail e SMS. Questa metrica esclude il traffico identificato come generato da bot e interazioni non umane (NHI) per fornire una visione più chiara del coinvolgimento cliente effettivo. La metrica Clic esistenti rimane disponibile e continua a segnalare i clic totali.

+++ Disponibile a breve: **le informazioni riportate di seguito sono soggette a modifiche.**

* **Canale LINE - Modifiche all’authoring**: l’interfaccia utente del canale LINE è stata aggiornata con funzionalità avanzate di authoring dei messaggi. Questa versione introduce il supporto per **formati di messaggi multipli**, inclusi Testo, Immagine, Imagemap, Carosello e Flex (Editor JSON), insieme alle anteprime del dispositivo in tempo reale. Gli utenti possono ora gestire messaggi raggruppati fino a un massimo di cinque messaggi ordinati (con controlli di aggiunta, rimozione e riordinamento) e sfruttare l’editor di personalizzazione integrato per la messaggistica convalidata e dinamica.

+++

### Miglioramenti dell’usabilità {#june-26-usability}

* **Cartelle per Percorsi** - È ora possibile organizzare i percorsi in **cartelle** per migliorare la navigazione e la gestione nell&#39;interfaccia. [Ulteriori informazioni](../building-journeys/journey-ui.md#journeys-folders)

  Data di disponibilità: 30 giugno 2026

<!--
+++ Coming soon — **Information below is subject to change.**

* **Override the default execution field in campaigns** - Previously available at the journey level, you can now override the default execution field set globally for your Email, SMS and WhatsApp deliveries in the campaign parameters.

  Availability date: Early June, 2026

+++
-->
