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
source-git-commit: 2d3430eaa8c15ade3fddcc4883a29efdb059bfa9
workflow-type: tm+mt
source-wordcount: 3733
ht-degree: 25%

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
<p>Ora puoi impostare il percorso su Simulazione. Questa modalità ti consente di convalidare la logica utilizzando utenti simulati. Si tratta di profili temporanei creati appositamente per la simulazione, che consentono di eseguire liberamente i test senza dover gestire profili di test persistenti in Adobe Experience Platform. </p>
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
<p>Precedentemente disponibile in Disponibilità limitata, questa funzionalità è ora generalmente disponibile per tutti i clienti. I frammenti di percorso supportano anche <strong>Strumenti sandbox</strong>, che consentono di creare pacchetti ed esportare frammenti tra sandbox diverse.</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/journey-fragments.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 9 giugno 2026</p>
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
<p>L'attività <strong>Ottimizza</strong> ora supporta <strong>Regole di targeting</strong> che consentono di definire criteri specifici che i clienti devono soddisfare per qualificarsi per un particolare percorso di percorso, in base a segmenti di pubblico o attributi di profilo.</p>
<p>A differenza della sperimentazione, in cui i clienti vengono assegnati in modo casuale ai percorsi, il targeting utilizza una logica deterministica per garantire che il pubblico o il profilo cliente appropriato venga indirizzato al percorso previsto.</p>
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
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/expression/expression-agent.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 3 giugno 2026</p> 
</td>
</tr>
</tbody>
</table>

* **Interrompere direttamente un percorso in pausa** - È ora possibile interrompere un percorso direttamente dallo stato **In pausa**. In precedenza, era necessario riprendere un percorso in pausa in **Live** prima di poterlo arrestare. [Ulteriori informazioni](../building-journeys/journey-pause.md#stop-close-paused)

  Data di disponibilità: 18-22 giugno 2026

* **Supporto di identificatori supplementari per tipi di pubblico esterni** - Gli identificatori supplementari nei percorsi sono ora supportati per i tipi di pubblico esterni, inclusi i tipi di pubblico importati da un file CSV e quelli creati con la composizione di pubblico federato. Puoi designare qualsiasi attributo non di identità o di identità non di persona del pubblico come ID supplementare; non è richiesta alcuna etichettatura schema. [Ulteriori informazioni](../building-journeys/supplemental-identifier.md)

  Data di disponibilità: 11 giugno 2026

* **Interruzione automatica per percorsi di pubblico lettura non ricorrenti** - I **percorsi di pubblico lettura** non ricorrenti passano ora automaticamente allo stato **Interrotto** una volta terminato l&#39;ultimo profilo attivo. In precedenza, questi percorsi rimanevano **Live** fino alla scadenza del timeout globale di 91 giorni, anche quando non vi scorrevano più profili. Con questo miglioramento, lo stato del percorso riflette lo stato di esecuzione effettivo non appena viene completato, mantenendo accurato l’inventario del percorso senza interventi manuali.

  Si noti che questo comportamento non si applica ai percorsi che includono nodi che causano periodi di attesa, ad esempio nodi Attendi, nodi Reazione o transizioni attivate da eventi. Questi percorsi rimangono soggetti al normale timeout globale di 91 giorni. [Ulteriori informazioni](../building-journeys/end-journey.md#auto-stop-non-recurring)

  Data di disponibilità: 9 giugno 2026

* **Autenticazione personalizzata basata sui certificati nelle azioni personalizzate** - Le azioni personalizzate ora supportano l’autenticazione personalizzata basata su certificato. Aggiungendo `subType: "certificateCredential"` a una configurazione di autorizzazione personalizzata, Journey Optimizer utilizza il certificato gestito di Adobe per firmare un’asserzione client JWT e scambiarla con un token di accesso, senza richiedere alcun segreto client. Progettato per le API aziendali che applicano la verifica dell’identità basata su certificato, come Microsoft Entra ID. [Ulteriori informazioni](../datasource/external-data-sources.md#certificate-credential)

  Data di disponibilità: 4 giugno 2026

* **Limite percorso live aumentato e nuovi guardrail** - È ora possibile avere fino a **200 percorsi attivi**, aumentato rispetto al limite precedente di 100. [Ulteriori informazioni](../start/guardrails.md#journeys-guardrails-journeys)

  Data di disponibilità: 18 giugno 2026. Questa funzionalità verrà gradualmente implementata in tutte le aree geografiche nei prossimi giorni.

+++ In arrivo — **Le informazioni di seguito sono soggette a modifiche.**

* **Date di inizio e di fine nell&#39;intestazione del percorso** - Quando le date di inizio e/o di fine sono configurate in un percorso attivo, ora sono visualizzate nell&#39;**intestazione percorso** accanto al badge di stato attivo. L’etichetta visualizzata si adatta a seconda che ogni data sia imminente o già passata.

+++

### Campagne orchestrate {#june-26-oc}

In questa versione, le campagne orchestrate sono dotate delle seguenti funzionalità e miglioramenti.

+++ In arrivo — **Le informazioni di seguito sono soggette a modifiche.**

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
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.</p>
<p> Data di disponibilità: 30 giugno 2026</p>
</td>
</tr>
</tbody>
</table>

* **Personalizzazione basata su loop per dati relazionali** - L&#39;editor di personalizzazione ora supporta un blocco di loop che esegue iterazioni sulle raccolte relazionali, ad esempio ordini, account o prenotazioni, ed esegue il rendering di un blocco di contenuto per record all&#39;interno di un&#39;unica e-mail o SMS. Le raccolte vengono configurate tramite il selettore dati utilizzando token di personalizzazione, senza che sia necessaria la scrittura di espressioni. [Ulteriori informazioni](../orchestrated/add-personalization.md#enrichment-collections)

  Data di disponibilità: fine di giugno 2026

* **Personalizzazione dei dettagli del mittente e-mail per destinatario e campagna** - Le campagne orchestrate ora supportano la personalizzazione di **campi di intestazione e-mail**, inclusi Nome mittente, Indirizzo mittente e Risposta, utilizzando gli attributi del profilo o i dati relazionali. Questo consente ai dettagli del mittente di riflettere l’advisor, la posizione o la filiale pertinente per ciascun destinatario, anziché instradare tutti gli invii tramite un unico indirizzo aziendale. I valori dell’intestazione possono essere impostati a livello di canale e sostituiti per campagna utilizzando dati contestuali per un controllo più preciso.

+++

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

+++ In arrivo — **Le informazioni di seguito sono soggette a modifiche.**

* **Attributi degli elementi dinamici** - Gli attributi personalizzati degli elementi di decisione possono ora essere personalizzati al momento della consegna utilizzando dati di profilo, contestuali e di pubblico. Questo elimina la necessità di mantenere offerte duplicate per varianti di contenuto minori, consentendo agli addetti al marketing di gestire meno elementi decisionali e più flessibili.

  Data di disponibilità: 22 giugno 2026

+++

### Gestione dei contenuti {#june-26-content}

In questa versione sono state aggiunte le seguenti funzionalità e miglioramenti alla gestione dei contenuti.

<table>
<thead>
<tr>
<th><strong>Simula varianti di contenuto: generazione di varianti di esperienza e IA aggiornate</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sono ora disponibili due aggiornamenti per il flusso di lavoro <strong>Simula contenuto</strong>:</p>
<ul>
<li><strong>Nuovo percorso predefinito</strong>. Facendo clic su <strong>Simula contenuto</strong>, ora viene aperta l'esperienza <strong>Simula varianti di contenuto</strong> per impostazione predefinita. Da una singola schermata, puoi aggiungere input di esempio manualmente o da un file CSV/JSON, riutilizzare gli utenti simulati, visualizzare in anteprima il rendering e inviare bozze. Per visualizzare l'anteprima con i profili di test di Adobe Experience Platform, inviare bozze con i dati del profilo di test o controllare il rendering della casella in entrata e i rapporti di posta indesiderata, fai clic su <strong>Simula contenuto</strong>, quindi seleziona <strong>Simula contenuto (profili AEP)</strong> dal menu a discesa.</li>
<li><strong>Varianti di contenuto generate dall'intelligenza artificiale</strong>: nell'esperienza <strong>Simula varianti di contenuto</strong>, fai clic su <strong>Genera</strong> per utilizzare l'intelligenza artificiale per creare automaticamente varianti di contenuto. Il sistema analizza il messaggio, rileva i campi di personalizzazione e i rami condizionali e inserisce valori realistici in modo da poter convalidare il rendering senza creare manualmente ogni variante.</li>
</ul>
<p>Per ulteriori informazioni, consulta la <a href="../test-approve/simulate-sample-input.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 9 giugno 2026</p>
</td>
</tr>
</tbody>
</table>


+++ In arrivo — **Le informazioni di seguito sono soggette a modifiche.**

<table>
<thead>
<tr>
<th><strong>Simula varianti di contenuto: generazione di varianti di esperienza e IA aggiornate</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sono ora disponibili due aggiornamenti per il flusso di lavoro <strong>Simula contenuto</strong>:</p>
<ul>
<li><strong>Nuovo percorso predefinito</strong>. Facendo clic su <strong>Simula contenuto</strong>, ora viene aperta l'esperienza <strong>Simula varianti di contenuto</strong> per impostazione predefinita. Da una singola schermata, puoi aggiungere input di esempio manualmente o da un file CSV/JSON, riutilizzare gli utenti simulati, visualizzare in anteprima il rendering e inviare bozze. Per visualizzare l'anteprima con i profili di test di Adobe Experience Platform, inviare bozze con i dati del profilo di test o controllare il rendering della casella in entrata e i rapporti di posta indesiderata, fai clic su <strong>Simula contenuto</strong>, quindi seleziona <strong>Simula contenuto (profili AEP)</strong> dal menu a discesa.</li>
<li><strong>Varianti di contenuto generate dall'intelligenza artificiale</strong>: nell'esperienza <strong>Simula varianti di contenuto</strong>, fai clic su <strong>Genera</strong> per utilizzare l'intelligenza artificiale per creare automaticamente varianti di contenuto. Il sistema analizza il messaggio, rileva i campi di personalizzazione e i rami condizionali e inserisce valori realistici in modo da poter convalidare il rendering senza creare manualmente ogni variante.</li>
</ul>
<p>Per ulteriori informazioni, consulta la <a href="../test-approve/simulate-sample-input.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 9 giugno 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Miglioramenti ai frammenti di contenuto Adobe Experience Manager in Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Questa versione apporta diversi miglioramenti per rendere <strong>i frammenti di contenuto di Adobe Experience Manager</strong> più utilizzabili, più governabili e più pronti per la produzione nei flussi di lavoro di authoring di Journey Optimizer:</p>
<ul>
<li>Journey Optimizer ora supporta il recupero di frammenti di contenuto da più configurazioni di Adobe Experience Manager, inclusi i livelli di pubblicazione di authoring, pubblicazione e autenticazione.</li>
<li>Una volta selezionato un frammento, il relativo contesto viene mantenuto per tutto il messaggio, consentendo agli autori di riutilizzare i campi del frammento in blocchi di contenuto senza effettuare una nuova selezione.</li>
<li>In Journey Optimizer è stata introdotta una nuova pagina di elenco dei frammenti di contenuto dedicati per migliorare la gestione del ciclo di vita; gli utenti possono identificare frammenti non sincronizzati e attivare sincronizzazioni manuali per restare al corrente.</li>
<li>Il supporto per le impostazioni internazionali e le varianti ora consente agli addetti al marketing di lavorare con versioni alternative dello stesso frammento di contenuto in modo più mirato.</li>
<li>Ora puoi accedere in modo flessibile ai contenuti Adobe Experience Manager da Adobe Journey Optimizer. Questa versione introduce la possibilità di <strong>cambiare l'archivio di origine</strong> per i frammenti di contenuto utilizzati nei percorsi e nelle campagne.</li>
<li>Ora compatibile con <b>Managed Services</b>, puoi visualizzare, accedere e utilizzare i frammenti di contenuto di Adobe Experience Manager direttamente in Journey Optimizer per la personalizzazione. È sufficiente aggiungere l’URL dell’archivio Adobe Experience Manager Managed Services nelle impostazioni di configurazione come configurazione unica.</li>
</ul>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integrazione dell’assistente AI con Adobe Experience Manager Asset Essentials</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L'Assistente AI ora recupera automaticamente <b>immagini approvate dal brand</b> direttamente dal tuo Adobe Experience Manager Assets durante la generazione di e-mail, pagine Web e notifiche push. Questo elimina la necessità di cercare manualmente in Assets o di affidarsi a fallback generici di intelligenza artificiale, garantendo che ogni elemento visivo sia perfettamente accurato e conforme al marchio.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Assistente AI per i miglioramenti nella generazione dei contenuti</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Questa versione migliora l'esperienza di generazione dei contenuti di <strong>AI Assistant</strong> grazie a una maggiore capacità di modifica delle immagini, a un'estrazione del marchio più affidabile e al supporto dell'autenticità dei contenuti nel flusso delle immagini:</p>
<ul>
<li><strong>La modifica di immagini AI</strong> è ora disponibile nel flusso di generazione delle immagini, incluso il supporto per modelli di terze parti di Firefly, per consentire di perfezionare le immagini di origine senza uscire dall'assistente.</li>
<li><strong>L'estrazione del segnale del marchio</strong> offre risultati di qualità superiore. Quando le pagine selezionate non ricevono un segnale sufficiente, i fallback migliorati ora popolano colori, composizione tipografica, linee guida per la scrittura e altri attributi del marchio.</li>
<li><strong>L'estrazione del marchio basata sul Web</strong> è più affidabile. Una migliore gestione del timeout impedisce a pagine lente, popup e banner di cookie di bloccare l’estrazione.</li>
<li><strong>L'autenticità dei contenuti (CAI)</strong> è ora supportata nel flusso di immagini. Questa versione risolve anche i problemi di caricamento delle immagini di riferimento e migliora la gestione delle immagini senza un manifesto C2PA esistente.</li>
</ul>
</td>
</tr>
</tbody>
</table>

+++


### Canale e-mail {#june-26-email}

In questa versione sono stati aggiunti i seguenti miglioramenti al canale e-mail.

* **Crittografia dei parametri URL**: ora è possibile crittografare i parametri URL nei collegamenti alle pagine di destinazione e di tracciamento aggiunti ai messaggi e-mail. In questo modo viene fornito un ulteriore livello di sicurezza per i dati dei parametri sensibili. Precedentemente rilasciata in disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale). [Ulteriori informazioni](../personalization/url-parameter-encryption.md)

  Data di disponibilità: 1° giugno 2026

* **Nuove autorizzazioni per il registro delle chiavi**: sono ora necessarie due nuove autorizzazioni per accedere e gestire le chiavi necessarie per la crittografia dei parametri URL: **Gestisci registro chiavi** e **Visualizza registro chiavi**. [Ulteriori informazioni](../administration/high-low-permissions.md#administration-permissions)

  Data di disponibilità: 1° giugno 2026

<table>
<thead>
<tr>
<th><strong>Testo formattato nei campi modificabili per i frammenti</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi aggiungere testo RTF a frammenti personalizzabili utilizzati nel contenuto delle e-mail.</p>
<p>Ad esempio, quando utilizzi il componente Testo come campo modificabile nel Designer e-mail, puoi formattare direttamente il contenuto (ad esempio, grassetto e corsivo) e inserire collegamenti ipertestuali.</p>
<p><img src="assets/do-not-localize/rich-text-editable-fields.gif"></p>
<p>Per ulteriori informazioni, consulta la <a href="../content-management/customizable-fragments.md#rich-text-visual">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: fine giugno 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Verifica del contenuto nel Designer e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ora include la convalida tecnica automatizzata direttamente nel Designer e-mail, che consente di individuare i problemi di HTML e CSS prima dell’invio.</p>
<p>Controlla gli elementi non supportati come i tag <code>&lt;script&gt;</code> e <code>&lt;base&gt;</code>, i div vuoti che possono interrompere il layout in Microsoft Outlook, i tag meta refresh di HTML e le soglie di dimensione CSS o HTML che attivano gli errori di rendering in Gmail.</p>
<p>I risultati vengono visualizzati come errori, avvisi o avvisi informativi direttamente nel pannello di authoring, con dettagli contestuali e correzioni con un solo clic, se disponibili, in modo che i problemi possano essere risolti senza uscire dall’editor.</p>
<p><img src="assets/do-not-localize/content-check.gif"></p>
<p>Per ulteriori informazioni, consulta la <a href="../email/content-check.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 18 giugno 2026</p>
</td>
</tr>
</tbody>
</table>

* **Convertitore immagine/HTML avanzato** - È ora disponibile una nuova versione della funzionalità di conversione da immagine a HTML, che offre una maggiore precisione nella generazione di HTML. Questo aggiornamento sfrutta modelli LLM di livello superiore per fornire un output HTML più preciso e affidabile dagli input delle immagini.

  Data di disponibilità: 18 giugno 2026

+++ In arrivo — **Le informazioni di seguito sono soggette a modifiche.**

<table>
<thead>
<tr>
<th><strong>Abilita riduzione dimensioni e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ora include un’opzione per ridurre le dimensioni del HTML dell’e-mail eliminando spazi vuoti inutili, commenti e codice ridondante, senza influire sul rendering dell’e-mail.</p>
<p>In questo modo è possibile migliorare il recapito dei messaggi evitando soglie di dimensione utilizzate da alcuni provider di posta elettronica per contrassegnare o rifiutare i messaggi e ridurre i tempi di caricamento per i destinatari.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Moduli nel Designer e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>E-mail Designer ora include una libreria di moduli di layout pronti all’uso, come intestazioni, schede dei prodotti, blocchi di informazioni e piè di pagina, che puoi trascinare direttamente nell’area di lavoro delle e-mail.</p>
<p>Ogni modulo è preconfigurato con proprietà modificabili (immagine, titolo, testo, pulsante, collegamenti) e può essere completamente personalizzato tramite l’interfaccia di WYSIWYG, velocizzando la creazione delle e-mail senza richiedere di creare strutture da zero.</p>
<p>Data di disponibilità: 22 giugno 2026</p>
</td>
</tr>
</tbody>
</table>

+++

### Contenuti e integrazioni {#june-26-integration}

In questa versione sono disponibili le seguenti funzionalità e miglioramenti per la gestione dei contenuti e le integrazioni.

<table>
<thead>
<tr>
<th><strong>Miglioramenti ai frammenti di contenuto Adobe Experience Manager in Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Questa versione apporta diversi miglioramenti per rendere <strong>i frammenti di contenuto di Adobe Experience Manager</strong> più utilizzabili, più governabili e più pronti per la produzione nei flussi di lavoro di authoring di Journey Optimizer:</p>
<ul>
<li>Journey Optimizer ora supporta il recupero di frammenti di contenuto da più configurazioni di Adobe Experience Manager, inclusi i livelli di pubblicazione di authoring, pubblicazione e autenticazione.</li>
<li>Una volta selezionato un frammento, il relativo contesto viene mantenuto per tutto il messaggio, consentendo agli autori di riutilizzare i campi del frammento in blocchi di contenuto senza effettuare una nuova selezione.</li>
<li>In Journey Optimizer è stata introdotta una nuova pagina di elenco dei frammenti di contenuto dedicati per migliorare la gestione del ciclo di vita; gli utenti possono identificare frammenti non sincronizzati e attivare sincronizzazioni manuali per restare al corrente.</li>
<li>Il supporto per le impostazioni internazionali e le varianti ora consente agli addetti al marketing di lavorare con versioni alternative dello stesso frammento di contenuto in modo più mirato.</li>
<li>Ora puoi accedere in modo flessibile ai contenuti Adobe Experience Manager da Adobe Journey Optimizer. Questa versione introduce la possibilità di <strong>cambiare l'archivio di origine</strong> per i frammenti di contenuto utilizzati nei percorsi e nelle campagne.</li>
<li>Ora compatibile con <b>Managed Services</b>, puoi visualizzare, accedere e utilizzare i frammenti di contenuto di Adobe Experience Manager direttamente in Journey Optimizer per la personalizzazione. È sufficiente aggiungere l’URL dell’archivio Adobe Experience Manager Managed Services nelle impostazioni di configurazione come configurazione unica.</li>
</ul>
<p>Per ulteriori informazioni, consulta la <a href="../integrations/aem-fragments-gs.md">documentazione dettagliata</a>.</p>
<p>Data di disponibilità: 18 giugno 2026</p>
</td>
</tr>
</tbody>
</table>

+++ In arrivo — **Le informazioni di seguito sono soggette a modifiche.**

<table>
<thead>
<tr>
<th><strong>Integrazione dell’assistente AI con Adobe Experience Manager Asset Essentials</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L'Assistente AI ora recupera automaticamente <b>immagini approvate dal brand</b> direttamente dal tuo Adobe Experience Manager Assets durante la generazione di e-mail, pagine Web e notifiche push. Questo elimina la necessità di cercare manualmente in Assets o di affidarsi a fallback generici di intelligenza artificiale, garantendo che ogni elemento visivo sia perfettamente accurato e conforme al marchio.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Assistente AI per i miglioramenti nella generazione dei contenuti</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Questa versione migliora l'esperienza di generazione dei contenuti di <strong>AI Assistant</strong> grazie a una maggiore capacità di modifica delle immagini, a un'estrazione del marchio più affidabile e al supporto dell'autenticità dei contenuti nel flusso delle immagini:</p>
<ul>
<li><strong>La modifica di immagini AI</strong> è ora disponibile nel flusso di generazione delle immagini, incluso il supporto per modelli di terze parti di Firefly, per consentire di perfezionare le immagini di origine senza uscire dall'assistente.</li>
<li><strong>L'estrazione del segnale del marchio</strong> offre risultati di qualità superiore. Quando le pagine selezionate non ricevono un segnale sufficiente, i fallback migliorati ora popolano colori, composizione tipografica, linee guida per la scrittura e altri attributi del marchio.</li>
<li><strong>L'estrazione del marchio basata sul Web</strong> è più affidabile. Una migliore gestione del timeout impedisce a pagine lente, popup e banner di cookie di bloccare l’estrazione.</li>
<li><strong>L'autenticità dei contenuti (CAI)</strong> è ora supportata nel flusso di immagini. Questa versione risolve anche i problemi di caricamento delle immagini di riferimento e migliora la gestione delle immagini senza un manifesto C2PA esistente.</li>
</ul>
</td>
</tr>
</tbody>
</table>

+++

### Generazione di rapporti {#june-26-reporting}

+++ In arrivo — **Le informazioni di seguito sono soggette a modifiche**

* **Clic stimati per rapporti e-mail e SMS** — È ora disponibile una nuova metrica **Clic stimati** in Percorsi, campagne e rapporti canale per e-mail e SMS. Questa metrica esclude il traffico identificato generato da bot e interazioni non umane (NHI) per fornire una visione più chiara dell’effettivo coinvolgimento dei clienti. La metrica Clic esistente rimane disponibile e continua a segnalare i clic totali.

* **Nuove metriche di clic stimate per la generazione di rapporti e-mail e SMS** - Per fornire una visualizzazione più accurata del reale coinvolgimento dei clienti, sono ora disponibili nuove metriche stimate per Percorsi, campagne e rapporti sui canali. Queste metriche aiutano a filtrare le interazioni non umane (NHI) e i clic dei bot dai dati di reporting:

   * CTR stimato: clic stimati relativi al totale delle consegne.
   * CTOR stimato solo per e-mail: clic stimati relativi alle aperture stimate.

  Data di disponibilità: fine giugno 2026

+++

### Amministrazione {#june-26-administration}

In questa versione sono stati aggiunti i seguenti miglioramenti per l’amministrazione e la gestione dei dati.

* [!BADGE Importante]{type=Informative} **Il set di dati dell&#39;evento di feedback dei messaggi di AJO passa all&#39;acquisizione in batch** - Il **set di dati dell&#39;evento di feedback dei messaggi di AJO** sta passando dall&#39;acquisizione in streaming all&#39;acquisizione in batch. Di conseguenza, per questo set di dati è prevista una latenza massima di 2 ore. Se hai creato rapporti in Customer Journey Analytics o eseguito query utilizzando questo set di dati, tenere conto di questa latenza aumentata in futuro. [Ulteriori informazioni](../data/datasets-query-examples.md#message-feedback-event-dataset)

  Data di disponibilità: 10 giugno 2026

* **Avvisi del cliente per eventi del ciclo di vita della campagna** - I nuovi avvisi di sistema ora ti segnalano gli eventi chiave del ciclo di vita per le campagne Azione e quelle attivate dall’API. Abbonati a livello di sandbox. [Ulteriori informazioni](../reports/alerts.md)

  Data di disponibilità: 1° giugno 2026


+++ In arrivo — **Le informazioni di seguito sono soggette a modifiche**

* **Inserimento di IP nella whitelist di Web Application Firewall (WAF)** - Adobe Journey Optimizer ora supporta la whitelist IP di Web Application Firewall (WAF) per le pagine di destinazione, consentendo alle organizzazioni di applicare che tutte le richieste in ingresso vengano instradate esclusivamente tramite l&#39;infrastruttura WAF configurata. Con questo miglioramento, i clienti possono configurare Journey Optimizer per rifiutare qualsiasi richiesta diretta che aggiri il livello WAF, garantendo che i criteri di sicurezza definiti in strumenti come Imperva vengano applicati in modo coerente. Questa funzionalità rafforza la postura di sicurezza per le aziende con requisiti di accesso alla rete rigorosi, fornendo loro il controllo completo sul flusso di traffico verso le pagine di destinazione ospitate da AJO.

  Data di disponibilità: fine giugno 2026

+++


### Messaggistica mobile (SMS, MMS, RCS e LINE) {#june-26-mobile}

In questa versione sono disponibili i seguenti miglioramenti alla messaggistica mobile.

* **Clic univoci per rapporti SMS** - È stato introdotto un nuovo modulo **Clic univoci** per i rapporti SMS, che porta lo stesso livello di tracciamento granulare delle prestazioni degli SMS attualmente disponibile per i rapporti e-mail.

* **SMS - Visualizza metriche di utilizzo** - Per i clienti che acquistano SMS direttamente tramite Adobe Journey Optimizer, è stata introdotta una nuova **dashboard di utilizzo SMS**. Ora puoi visualizzare e tenere traccia degli ultimi 90 giorni di metriche di invio dei messaggi, suddivisi per messaggi MO (Mobile Originated) e MT (Mobile Terminated). Questi dati sono disponibili anche per il download tramite CSV, fornendo una maggiore visibilità e un maggiore controllo sulla spesa SMS. [Ulteriori informazioni](../mobile/sms-usage-report.md)

* **Clic stimati per rapporto SMS** - È ora disponibile una nuova metrica Clic stimati in Percorsi, campagne e rapporti Canale per e-mail e SMS. Questa metrica esclude il traffico identificato generato da bot e interazioni non umane (NHI) per fornire una visione più chiara dell’effettivo coinvolgimento dei clienti. La metrica Clic esistente rimane disponibile e continua a segnalare i clic totali.

+++ In arrivo — **Le informazioni di seguito sono soggette a modifiche.**

* **Canale LINE - Modifiche all&#39;authoring** - L&#39;interfaccia utente del canale LINE è stata aggiornata con funzionalità avanzate di authoring dei messaggi. Questa versione introduce il supporto per **formati di messaggi multipli**, inclusi Testo, Immagine, Imagemap, Carosello e Flex (Editor JSON), insieme alle anteprime dei dispositivi in tempo reale. Gli utenti possono ora gestire messaggi raggruppati con un massimo di cinque messaggi ordinati (con controlli di aggiunta, rimozione e riordinamento) e sfruttare l’editor di personalizzazione integrato per messaggi convalidati e dinamici.

+++

### Miglioramenti a livello di usabilità {#june-26-usability}

+++ In arrivo — **Le informazioni di seguito sono soggette a modifiche.**

* **Cartelle per Percorsi e campagne** - È ora possibile organizzare i percorsi e le campagne in **cartelle** per migliorare la navigazione e la gestione nell&#39;interfaccia.

+++

<!--
+++ Coming soon — **Information below is subject to change.**

* **Override the default execution field in campaigns** - Previously available at the journey level, you can now override the default execution field set globally for your Email, SMS and WhatsApp deliveries in the campaign parameters.

  Availability date: Early June, 2026

+++
-->
