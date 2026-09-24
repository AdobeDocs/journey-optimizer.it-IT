---
solution: Journey Optimizer
product: journey optimizer
title: Aggiornamenti alla documentazione
description: Scopri gli ultimi aggiornamenti della documentazione per Adobe Journey Optimizer, incluse nuove pagine, riorganizzazioni e chiarimenti.
keywords: aggiornamenti documentazione, note sulla versione, journey optimizer, registro modifiche
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 83c8f206-bce3-4cc8-94a3-575ec1d999bc
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
    internal-label: Administration
subfeature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
    internal-label: Journey Optimizer release notes
source-git-commit: 4e9ccef9fabcfeb9271e8f560ff11286caa4786c
workflow-type: tm+mt
source-wordcount: '7258'
ht-degree: 81%
---

# Aggiornamenti alla documentazione {#latest-updates}

In questa pagina sono elencate tutte le ultime modifiche apportate alla documentazione di [!DNL Journey Optimizer], oltre agli aggiornamenti relativi alle funzioni e ai miglioramenti alle note di rilascio mensili.

## Settembre 2026 {#september-2026}

* I guardrail di `inAudience` ora includono la soluzione alternativa per le sandbox con più di 5.000 tipi di pubblico, in cui i tipi di pubblico meno recenti possono essere rifiutati durante la creazione del percorso perché la convalida controlla solo i 5.000 tipi di pubblico aggiornati più di recente. [Ulteriori informazioni](../building-journeys/functions/functioninaudience.md#guardrails)

* Le linee guida per le pagine mirror delle e-mail sono state espanse: la documentazione ora spiega che gli URL delle pagine mirror non possono essere recuperati tramite un’API pubblica o un set di dati, consiglia di esportare i messaggi o archiviare i dati in formato Ccn per mantenere il contenuto inviato e chiarisce che i collegamenti alle pagine mirror sono inattivi nelle bozze e nelle simulazioni. [Ulteriori informazioni](../email/message-tracking.md#mirror-page)

* È ora disponibile una nuova pagina di **demo interattiva** per le sfide di fidelizzazione, con collegamento a una demo self-guide e cliccabile che copre il flusso di creazione delle sfide dell&#39;addetto al marketing (tra cui Porti i tuoi dati e le dashboard di approfondimenti), l&#39;esperienza del cliente finale e la gestione delle sfide di fidelizzazione in CX Coworker. [Ulteriori informazioni](../loyalty-challenges/loyalty-challenges-demo.md)

* La pagina **Personalizza sfondo e-mail** è stata espansa e migliorata. Ora documenta l&#39;elenco a discesa **Posizionamento immagine** completo per le immagini di sfondo e aggiunge nuove best practice per i colori e le immagini di sfondo, tra cui un consiglio per testare le immagini di sfondo tra client e-mail reali anziché affidarsi esclusivamente all&#39;anteprima di E-mail Designer. [Ulteriori informazioni](../email/backgrounds.md)

* La pagina **Progetta contenuto da zero con E-mail Designer** è stata riorganizzata e chiarita: distingue la struttura **[!UICONTROL n:n colonna]** dalle strutture dei predefiniti fissi, i documenti in cui il conteggio delle colonne di una struttura può essere aumentato senza perdere il contenuto esistente, spiega il comportamento di stacking delle colonne su dispositivi mobili e aggiunge un nuovo passaggio sull&#39;utilizzo di **[!UICONTROL Moduli]** per la creazione rapida di e-mail. [Ulteriori informazioni](../email/content-from-scratch.md)

* La pagina **Progetta il percorso** ora include una sezione completa di tutorial sulla nuova esperienza dell&#39;area di lavoro, che illustra come aggiungere attività, utilizzare le icone della barra degli strumenti, selezionare più attività per azioni in blocco, copiare e incollare attività e unire o scollegare rami. [Ulteriori informazioni](../building-journeys/using-the-journey-designer.md#canvas-capabilities)

* Sono state aggiunte nuove linee guida per la verifica della consegna delle azioni personalizzate: la pagina **Esempi di query per set di dati** spiega ora come scegliere tra l’evento di feedback dei messaggi, il tracciamento delle e-mail e i set di dati dell’evento del passaggio di Percorso a seconda del tipo di azione e documenta come risolvere l’errore &quot;Tabella non predisposta per il set di dati&quot;. Le pagine **Panoramica degli eventi dei passaggi del Percorso** e **Risoluzione dei problemi di esecuzione del percorso live** sono state aggiornate di conseguenza, chiarendo che una chiamata di azione personalizzata riuscita conferma solo che Journey Optimizer ha eseguito l&#39;azione e non che il sistema esterno ha recapitato un messaggio. [Ulteriori informazioni](../data/datasets-query-examples.md#choose-the-correct-dataset)

* Le informazioni su CX Coworker sono state aggiunte alla pagina **Utilizzare l&#39;intelligenza artificiale**, in cui sono descritti CX Coworker, il modo in cui si relaziona all&#39;Assistente all&#39;intelligenza artificiale e i riferimenti alla documentazione ufficiale di Coworker. Sono state aggiunte pagine dedicate alle abilità in ogni guida alle funzionalità: [CX Coworker skills for groups](../building-journeys/journeys-coworker-skills.md), [CX Coworker skills for loyalty](../loyalty-challenges/loyalty-coworker-skills.md) e [CX Coworker content management tools](../content-management/content-management-coworker-skills.md). [Ulteriori informazioni](../start/ai-features.md#cx-coworker)

* Una nuova abilità **Analizza anomalie Percorso** è stata documentata in **Analisi Percorso** nella pagina CX Coworker. Rileva picchi, cadute o linee piatte imprevisti all’entrata, all’uscita o all’invio di un percorso rispetto alle linee di base storiche ed esegue una diagnostica di sola lettura per individuare una probabile causa principale. [Ulteriori informazioni](../building-journeys/journeys-coworker-skills.md#journey-analyze)

* Le pagine **Guardrail e limitazioni** e **Proprietà Percorso** sono state aggiornate per documentare il limite del payload di percorso predefinito come **2 MB (2.000.000 byte)**, chiarire che il valore riflette la definizione del percorso serializzato anziché il solo conteggio delle attività e spiegare le soglie di avviso del 90% e di blocco del 100%. [Ulteriori informazioni](../start/guardrails.md#journey-payload-size) e [ulteriori informazioni](../building-journeys/journey-properties.md#journey-payload-size)

* La pagina **Guardrail e limitazioni** è stata corretta per riflettere il fatto che i frammenti visivi di dimensioni superiori a 100 KB o i frammenti di espressione di dimensioni superiori a 200 KB non possono più causare problemi di troncamento nella consegna delle e-mail: ora si applica un singolo guardrail con dimensioni di frammento pari a 700 KB. [Ulteriori informazioni](../start/guardrails.md#fragments-guardrails)

* La pagina **Crea attività live** è stata corretta: il campo `executionMetadata` è disponibile solo per le campagne **Transazionali** attivate da API, non per le campagne Marketing attivate da API come indicato in precedenza. [Ulteriori informazioni](../mobile-live/create-mobile-live.md#metadata)

* La documentazione dell&#39;**AJO Message Feedback Event Dataset** è stata espansa per chiarire che copre il feedback sulla consegna dei messaggi su tutti i canali (e-mail, SMS/RCS/MMS, Direct Mail), non solo e-mail e push, e ora include una **sezione Classify test and non-test execution** che spiega come interpretare il campo `isTestExecution`, inclusi `NULL` o valori mancanti. [Ulteriori informazioni](../data/datasets-query-examples.md#classify-test-executions)

* È stata documentata una nuova funzionalità **Gestione dei contenuti** per CX Coworker, basata su 15 strumenti MCP di lettura/scrittura che consentono di individuare, creare, aggiornare, clonare e pubblicare modelli di contenuto, frammenti, pagine di destinazione e contenuti di messaggi in linea di percorso/campagna utilizzando prompt in linguaggio naturale. [Ulteriori informazioni](../content-management/content-management-coworker-skills.md#content-management)

* Nella documentazione di **Aggiungi contenuto alla pagina di destinazione** è ora descritta un&#39;opzione **Rendi obbligatorio il campo modulo** per le caselle di controllo del consenso: se abilitata, il modulo non può essere inviato a meno che la casella di controllo non sia selezionata e sia applicata sia sul lato client che sul lato server. [Ulteriori informazioni](../landing-pages/lp-content.md#use-form-component)

* La pagina **Introduzione alla simulazione di Percorso** è stata aggiornata per documentare che i nodi Content Decision e il metodo della regola di targeting dell&#39;attività **Ottimizza** sono ora supportati in Simulazione (precedentemente indicata come blocco), con una nuova tabella **Comportamento delle decisioni** che descrive in dettaglio il modo in cui vengono valutati l&#39;idoneità delle offerte, le regole di idoneità e i tipi di pubblico e i metodi di classificazione durante l&#39;esecuzione di una simulazione. [Ulteriori informazioni](../building-journeys/simulate-journey-gs.md#limitations)

* La pagina **Converti immagini in modelli di contenuto e-mail** è stata corretta per rimuovere un requisito di autorizzazioni non accurato: l&#39;autorizzazione **Gestisci modelli di contenuto** non è necessaria per accedere e creare modelli con l&#39;immagine al convertitore HTML. È necessaria solo l&#39;autorizzazione **Genera contenuto**. [Ulteriori informazioni](../content-management/image-to-html.md#access-image-to-html)

* La pagina **Sistemi esterni (azioni personalizzate)** è stata corretta: l&#39;interruttore di circuito per gli endpoint di azione personalizzati lenti ora si attiva quando più del 20% delle chiamate in una finestra di 120 secondi supera **5 secondi** (in precedenza erano documentati 10 secondi). [Ulteriori informazioni](../configuration/external-systems.md#response-time)

* La pagina **Configura la configurazione del canale** include ora una nota che chiarisce che lo schema utilizzato per la dimensione secondaria deve avere una chiave primaria e che le chiavi primarie composite non sono supportate. [Ulteriori informazioni](../orchestrated/channel-config.md)

* Le pagine **Dati e set di dati fedeltà** e **Introduzione alle origini** sono stati aggiornati per includere LAVA come connettore di fedeltà e premi supportato, insieme a Talon.One, Capillary e Kobie. [Ulteriori informazioni](../loyalty-challenges/loyalty-data-and-datasets.md)

## agosto 2026 {#august-2026}

* La pagina **Aggiungi frammenti visivi alle e-mail** ora chiarisce che un frammento con contenuto dinamico e uno stato predefinito vuoto viene visualizzato vuoto in E-mail Designer — simula con un profilo corrispondente per visualizzare in anteprima il contenuto. [Ulteriori informazioni](../email/use-visual-fragments.md#fragment-dynamic-content)

* La pagina **Traccia i messaggi** è stata aggiornata per chiarire che i caratteri URL non supportati (ad esempio, gli apostrofi) devono essere codificati in percentuale e che la mancata codifica può interrompere i collegamenti tracciati e i parametri di tracciamento URL. [Ulteriori informazioni](../email/message-tracking.md#insert-links)

* La pagina **Invia con scaglioni** è stata aggiornata per documentare che l&#39;ultimo scaglione in un percorso di pubblico di lettura deve essere pianificato entro **6 giorni e 18 ore** dall&#39;inizio del percorso. Il superamento di questa finestra attiva un errore di convalida e impedisce al percorso di entrare in modalità di test o di andare &quot;live&quot;. [Ulteriori informazioni](../delivery/send-using-waves.md#limitations-guardrails)

* È stata aggiunta una nuova sezione **Elimina eventi di feedback** alla pagina **Raccolta dati di gestione delle decisioni**, che documenta come utilizzare il flag `dryRun` per eliminare gli eventi di decisione durante il test e impedire l&#39;acquisizione di feedback per i contatori di reporting e quota limite. [Ulteriori informazioni](../offers/data-collection/data-collection.md#suppress-feedback)

* È ora disponibile una nuova pagina **Scegli un metodo di convalida**. Vengono confrontati la simulazione del Percorso, la modalità di test e l&#39;esecuzione di prova del Percorso, ovvero i dati utilizzati da ciascun utente, se invia messaggi reali, errori comuni da evitare e una guida decisionale per scegliere il metodo corretto in ogni fase della creazione di un percorso. [Ulteriori informazioni](../building-journeys/choose-validation-method.md)

* La pagina **Guardrail e limitazioni** è stata aggiornata per chiarire l’attività di qualificazione del pubblico e i guardrail degli eventi: la formulazione ora fa riferimento in modo coerente alle **attività** di qualificazione del pubblico (anziché i nodi), anche quando vengono utilizzati come criteri di uscita, ed entrambi i guardrail ora coprono esplicitamente percorsi **live, chiusi, in pausa, in modalità di test e di prova**. [Ulteriori informazioni](../start/guardrails.md#audience-qualif-g)

* È stata aggiunta una nota alla sezione **Testare l’ottimizzazione dimensioni HTML** per chiarire che le dimensioni della bozza riflettono le dimensioni del modello HTML (Handlebars al valore minimo), non le dimensioni finali dell’e-mail consegnata, che possono essere maggiori una volta risolte le espressioni dinamiche al momento della consegna. [Ulteriori informazioni](../email/create-email.md#optimize-html-proof)

* È stata aggiunta una nuova sezione **Limitazioni del browser web per dispositivi mobili** alla pagina **Introduzione alla progettazione delle e-mail**, che documenta il motivo per cui è possibile eseguire il rendering delle e-mail in modo diverso in Gmail o Outlook quando si accede tramite un browser su un dispositivo mobile, insieme a un suggerimento per la soluzione alternativa. [Ulteriori informazioni](../email/get-started-email-design.md#mobile-web-limitations)

* È stata aggiunta una nuova sezione **Considerazioni sul rendering di Outlook** alla pagina **Introduzione alla progettazione delle e-mail**, in cui sono elencate le particolarità comuni di Outlook da tenere in considerazione durante la progettazione: numeri pari per spaziature e larghezze, larghezze delle tabelle basate su pixel, attributi di larghezza delle immagini per HTML, testo alternativo, bordi su celle della tabella e angoli arrotondati. [Ulteriori informazioni](../email/get-started-email-design.md#outlook-tips)

* La pagina **Guardrail TTL (time-to-live) dei set di dati** è stata aggiornata con una tabella di **set di dati interessati** significativamente espansa, che ora include tutti i set di dati generati dal sistema di Journey Optimizer (inclusi alcuni non elencati in precedenza, ad esempio il servizio di consenso AJO, il profilo di messaggistica interattiva, il profilo push e i set di dati di esportazione dei messaggi) insieme a una nuova colonna **Disponibilità** che indica se ogni set di dati è incluso per impostazione predefinita o richiede un componente aggiuntivo o una licenza specifici. Anche la pagina **Guardrail e limitazioni** è stata aggiornata per riflettere la data di applicazione confermata per questo guardrail: la modifica verrà applicata su **sandbox del cliente esistenti** a partire dal **1 ottobre 2026**. [Ulteriori informazioni](../data/datasets-ttl.md#datasets)

* Alla documentazione del contenuto generativo è stata aggiunta la nuova sezione **Utilizza la modalità impostazioni immagine**. Spiega le modalità **Bilanciata**, **DAM** e **Creativa** disponibili nelle **[!UICONTROL Impostazioni immagine]**, che controllano se le immagini delle origini di contenuto generate dall’IA dalla libreria Gestione delle risorse digitali, le generano con l’IA o le combinano. [Ulteriori informazioni](../content-management/generative-uc.md#image-mode)

* La descrizione delle **Destinazioni** in **Navigazione a sinistra > Sezioni principali** è stata aggiornata per notare che le organizzazioni con [!DNL Real-Time CDP] o [!DNL Adobe Journey Optimizer] possono anche attivare tipi di pubblico per destinazioni di personalizzazione idonee, come [!DNL Adobe Target], dal catalogo delle destinazioni di Experience Platform. [Ulteriori informazioni](../start/user-interface.md#main-sections)

* Sono stati aggiunti video descrittivi alla documentazione sulle sfide di fedeltà per creare le sfide, impostare i fornitori di premi e monitorare le prestazioni delle sfide. [Guarda i video della sfida](../loyalty-challenges/create-challenges.md#video), [guarda il video del provider di premi](../loyalty-challenges/reward-definition-guide.md#video) e [guarda il video del reporting](../loyalty-challenges/loyalty-reporting.md#video).

## luglio 2026 {#july-2026}

* È stata aggiunta una nuova sezione **Impostazioni di consegna** alla navigazione della documentazione. Raggruppa le funzioni relative alla consegna che si applicano a percorsi, campagne e campagne orchestrate: **Invia in scaglioni**, **Ottimizzazione dell’ora di invio** e **Ottimizzazione del canale** sono state tutte spostate dalla sezione Percorsi.

* Le pagine separate della documentazione **Invia in scaglioni** per percorsi e campagne di azione sono state unite in una singola pagina, che ora include anche le campagne orchestrate. [Ulteriori informazioni](../delivery/send-using-waves.md)

* È stato aggiunto un suggerimento che punta all’articolo della community Experience League su **come scollegare e ricongiungersi ai nodi** nella nuova area di lavoro del percorso alla pagina **Progettazione del percorso**. [Ulteriori informazioni](../building-journeys/using-the-journey-designer.md)

* La sezione del componente **Griglia** è stata aggiunta alla pagina **Componenti di contenuto E-mail designer**. Consente di organizzare il contenuto in una griglia strutturata di righe e colonne, in cui ogni cella può contenere altri componenti di contenuto. [Ulteriori informazioni](../email/content-components.md#grid)

* La sezione del componente **Griglia** è stata aggiunta alla pagina **Utilizza i componenti di contenuto di E-mail Designer**. Il componente Griglia consente di organizzare il contenuto in una griglia strutturata di righe e colonne, in cui ogni cella può contenere altri componenti di contenuto. [Ulteriori informazioni](../email/content-components.md#grid)

* La documentazione dell’**API di migrazione della funzione Decisioni** è stata aggiornata con la precisazione che la sandbox di destinazione **può essere la stessa della sandbox di origine**. Il processo di migrazione gestisce questo scenario e garantisce l’integrità dei dati, indipendentemente dal fatto che gli oggetti vengano migrati all’interno della stessa sandbox o a una diversa. [Ulteriori informazioni](../experience-decisioning/decisioning-migration-api.md#target-sandbox-preparation)

* La documentazione dell&#39;API **Decisioning Migration** è stata migliorata con indicazioni complete sulla migrazione degli oggetti di gestione delle decisioni in Decisioning. Le nuove sezioni includono: riferimento di mappatura entità con 10 convenzioni di denominazione, copertura nell’ambito rispetto a quella esterna all’ambito, confronti dettagliati tra modelli di richiesta/risposta, tre modelli di implementazione (lato client, lato server, ibrido) con gestione dei cookie, requisiti di tracciamento degli eventi con 5 esempi JSON di eventi, prerequisiti per la migrazione tra sandbox, un processo di migrazione in 5 fasi end-to-end e domande frequenti sulla migrazione. [Ulteriori informazioni](../experience-decisioning/decisioning-migration-api.md)

* È ora disponibile una nuova pagina delle **competenze CX Coworker**. Fornisce una documentazione completa di tutte le competenze di percorso disponibili in Journey Optimizer, incluse creazione di percorsi, creazione di contenuti per i canali, gestione delle sfide fedeltà e analisi di percorso, con casi d’uso, prompt di esempio e best practice per ogni competenza. [Ulteriori informazioni](../start/ai-features.md#cx-coworker)

* La documentazione della funzione **A precisione** è stata aggiornata per chiarire che `toPrecision` si comporta come JavaScript `toFixed()`: restituisce una stringa con un numero fisso di posizioni decimali, inclusa la spaziatura zero quando necessario. [Ulteriori informazioni](../personalization/functions/math.md#to-precision)

* La pagina **Terminare un percorso** è stata aggiornata per chiarire il tempo di interruzione automatica per i percorsi Leggi pubblico non ricorrenti: un buffer di sicurezza di circa **96 ore (~4 giorni)** dopo l’esecuzione pianificata (intervallo di inattività di 24 ore + tolleranza di 72 ore per le ore di silenzio), durante il quale il percorso può rimanere nello stato **Live** prima di passare a **Interrotto** poco dopo la scadenza del buffer. La pagina ora chiarisce anche che i percorsi basati su scaglioni (a più scaglioni) e i percorsi che utilizzano l’ottimizzazione dell’ora di invio, sono esclusi da questa interruzione automatica e seguono invece il timeout standard di percorso di 91 giorni. [Ulteriori informazioni](../building-journeys/end-journey.md#auto-stop-non-recurring)

* La pagina **Creare campagne di preparazione IP** è stata aggiornata per chiarire che le regole di targeting possono essere applicate alle campagne di preparazione IP e per documentare il comportamento di valutazione: l’iscrizione del pubblico è fissa all’attivazione dell’esecuzione (segmentazione in batch giornaliera), mentre gli attributi del profilo vengono letti al momento dell’esecuzione dai dati in batch acquisiti più di recente. [Ulteriori informazioni](../configuration/ip-warmup-campaign.md)

* È stato aggiunto un avviso alla pagina **Modificare record PTR** per informare la clientela che quando si aggiunge un nuovo record DNS di inoltro alla loro piattaforma, il record DNS di inoltro per il vecchio sottodominio non deve essere rimosso fino al completamento dello spostamento, poiché in questo modo la modifica non riuscirà. [Ulteriori informazioni](../configuration/ptr-records.md#edit-ptr-subdomains-cname)

* Le pagine **Invia in scaglioni** sono state aggiornate per chiarire il comportamento di rivalutazione del pubblico in più scaglioni: l’iscrizione al pubblico è fissa al momento dell’attivazione (istantanea), ma gli attributi del profilo e il consenso vengono valutati durante l’elaborazione di ogni scaglione. Ciò significa che le rinunce che si verificano tra uno scaglione e l’altro vengono rispettate. Ulteriori informazioni nella [sezione Domande frequenti](../delivery/send-using-waves.md#faq).

* La pagina **Governance dei dati** è stata aggiornata per chiarire che l’applicazione dei criteri DULE si applica solo ai **campi attributo profilo**. I campi basati su eventi (attributi di contesto come i campi evento del percorso) non sono supportati: le etichette applicate a tali campi nell’interfaccia utente non limitano l’utilizzo dei dati. [Ulteriori informazioni](../action/action-privacy.md)

* La documentazione **Ottimizzazione dell’ora di invio** è stata aggiornata per riflettere il nuovo limite **[!UICONTROL Invia entro prossimo]** di **2-100 ore** (in precedenza 1-168) e per documentare le aree geografiche dell&#39;hub di AEP supportate per questa funzionalità. [Ulteriori informazioni](../building-journeys/send-time-optimization.md#use-send-time-optimization)


* Le pagine relative al **Modello di ottimizzazione personalizzato** sono state aggiornate per riflettere gli ultimi miglioramenti apportati al modello; in esse vengono illustrati il funzionamento del modello ensemble, i requisiti relativi ai set di dati, i casi d’uso, le ipotesi chiave e il comportamento in fase di avvio a freddo. Ulteriori informazioni sono disponibili nelle sezioni [Decisioni per le esperienze](../experience-decisioning/ranking/personalized-optimization-model.md) e [Offer Decisioning](../offers/ranking/personalized-optimization-model.md).

* È stata aggiunta una nota alla pagina **Formule di ranking per l’arbitrato del percorso** per specificare che le formule di ranking sono disponibili solo per le organizzazioni che hanno acquistato il componente aggiuntivo **Decisioning**. [Ulteriori informazioni](../conflict-prioritization/journey-ranking-formulas.md)

* È ora disponibile una nuova pagina di **Frammenti dinamici**. Descrive come utilizzare la risoluzione dei frammenti dinamici in [!DNL Journey Optimizer] per selezionare il frammento pubblicato da inserire in un messaggio in fase di esecuzione, in base agli attributi di profilo, alle ricerche di set di dati o ai dati contestuali trasferiti al momento dell’invio. [Ulteriori informazioni](../content-management/dynamic-fragments.md)

## Giugno 2026 {#june-2026}

* La pagina **Controllare e inviare un messaggio di direct mail** è stata aggiornata per chiarire il tempo di esportazione e il comportamento di raggruppamento di direct mail, inclusa la pianificazione fissa dell’esportazione ogni 4 ore (UTC), il motivo per cui è possibile generare più file in una sola giornata, quando l’attività **[!UICONTROL Aggiorna profilo]** viene eseguita nei percorsi e i consigli per gli scenari in cui viene generato un solo file al giorno. [Ulteriori informazioni](../direct-mail/test-send-direct-mail.md#dm-export-timing)

* Ora è disponibile una nuova pagina **Tipi di percorso: scegli quello giusto**. Vengono confrontati tutti i punti di ingresso del percorso (Leggi pubblico, Qualificazione del pubblico, Evento unitario ed Evento di business) con le guide alle decisioni e una matrice di compatibilità delle funzioni per aiutarti a scegliere il tipo giusto per il tuo caso d’uso. [Ulteriori informazioni](../building-journeys/journey-types-selection.md)

* Ora è disponibile una nuova pagina **Percorsi o campagne**. Confronta i percorsi, le campagne di azione e le campagne attivate da API in base allo stile di esecuzione, al modello dati e al caso d’uso, tra cui l’attivazione del canale in entrata per la personalizzazione edge a bassa latenza, la consegna in entrata su più superfici e indicazioni su quando utilizzare le campagne orchestrate (composizione del pubblico ad hoc, dati federati). [Ulteriori informazioni](../start/journeys-vs-campaigns.md)

* La pagina **Modalità a velocità effettiva elevata** è stata aggiornata per riflettere l’ampliamento della disponibilità geografica: la funzione è ora disponibile in tutte le aree geografiche ad eccezione della Svizzera per le organizzazioni che dispongono della licenza del componente aggiuntivo per la messaggistica transazionale a velocità effettiva elevata. [Ulteriori informazioni](../campaigns/api-triggered-high-throughput.md)

* È stata aggiunta una nuova sezione **Profili coinvolgibili e utilizzo delle licenze** alla pagina **Introduzione ai profili** come unica source of truth per questo concetto, con riferimenti mirati aggiunti nelle sezioni Tipi di pubblico, Campagne e Decisioning. [Ulteriori informazioni](../audience/get-started-profiles.md#engageable-profiles)

* La documentazione dell&#39;attività **Dividi** è stata aggiornata per documentare il campo **[!UICONTROL Codice segmento]** disponibile nelle impostazioni di ogni sottoinsieme, che consente di assegnare un identificatore univoco a ogni segmento di pubblico a scopo di tracciamento e reporting. [Ulteriori informazioni](../orchestrated/activities/split.md)

* La pagina **Configurare una dimensione targeting** è stata aggiornata per documentare i due tipi di dimensione targeting disponibili nelle campagne orchestrate: la **dimensione targeting di profilo** incorporata (nessuna configurazione richiesta) e le **dimensioni targeting personalizzate** basate su schemi relazionali. [Ulteriori informazioni](../orchestrated/target-dimension.md)

* La documentazione **Sfruttare i temi in un frammento** è stata resa più chiara per documentare esplicitamente il limite di compatibilità a 5 temi (incluso il vincolo del tema predefinito di Adobe) e per spiegare che l’inserimento di frammenti è bloccato quando il tema dell’e-mail non è uno dei temi associati al frammento. [Ulteriori informazioni](../email/apply-email-themes.md#leverage-themes-fragment)

* Le pagine **Introduzione ai set di dati** e **Introduzione agli schemi** sono state aggiornate con indicazioni sull’abilitazione dei set di dati e degli schemi per il profilo cliente in tempo reale, tra cui considerazioni chiave, la distinzione tra la disabilitazione di un set di dati e dello schema sottostante, nonché i collegamenti alla documentazione contenente la pianificazione e le best practice di Adobe Experience Platform. [Ulteriori informazioni sui set di dati](../data/get-started-datasets.md) e [Ulteriori informazioni sugli schemi](../data/get-started-schemas.md)

* È ora disponibile un nuovo hub di onboarding **Introduzione ad Adobe Journey Optimizer**. I nuovi utenti, se hanno già eseguito l’onboarding, possono scegliere il percorso in base al ruolo, esplorare le nozioni di base o passare ad aree quotidiane, senza dover sapere dove cercare. [Ulteriori informazioni](../../rp_landing_pages/get-started-landing-page.md)

* Una nuova pagina **Iniziare dall&#39;obiettivo** ti consente di iniziare da ciò che desideri ottenere, anziché dal nome di una funzionalità. Gli obiettivi di business vengono mappati alla funzionalità di [!DNL Journey Optimizer] consigliata in termini di configurazione, percorsi, campagne, personalizzazione, decisioni e reporting. [Ulteriori informazioni](../start/ajo-use-case-guide.md)

* La guida al ruolo **Introduzione per gli sviluppatori** è stata aggiornata con introduzioni più chiare per ogni sezione e schede **Collaborazione tra ruoli** migliorate che fanno riferimento a percorsi e rimandano alle pagine chiave relative all’implementazione. [Ulteriori informazioni](../start/path/developer.md)

* Alla documentazione relativa alla **Sperimentazione del percorso** è stata aggiunta una nuova sottosezione **Assegnazione del percorso al reingresso del percorso**. Si precisa che l’assegnazione del percorso è permanente per un profilo in caso di ingressi multipli alla stessa versione del percorso, ma solo all’interno di quella versione del percorso. Le assegnazioni vengono reimpostate quando viene pubblicata una nuova versione del percorso e ogni attività di sperimentazione in un percorso applica un’assegnazione casuale indipendente. [Ulteriori informazioni](../building-journeys/path-experimentation.md#path-assignment)
* I riferimenti ad **Adobe Experience Cloud** sono stati allineati con il brand **[!DNL Adobe CX Enterprise]** nella documentazione di [!DNL Journey Optimizer].

* La documentazione della funzione di data **`nowWithDelta()`** è stata aggiornata per chiarire il comportamento di fine mese: quando il mese target ha un numero di giorni inferiore al giorno del mese corrente, il risultato viene normalizzato all’ultimo giorno valido di quel mese. [Ulteriori informazioni](../building-journeys/functions/date-functions.md#nowWithDelta)

* La pagina **Introduzione alla recapitabilità** è stata aggiornata con una nuova sottosezione **Provider senza FBL per destinatario**. Elenca i principali provider di cassette postali che non restituiscono reclami di posta indesiderata per destinatario (Gmail/Google Workspace, Apple iCloud e Corporate Microsoft 365/Exchange Online) e spiega perché per i destinatari che utilizzano questi servizi è prevista l’assenza di una voce nell’elenco di soppressione. [Ulteriori informazioni](../reports/deliverability.md#providers-no-fbl)

* **Decisioni per le esperienze è ora disponibile per il canale direct mail.** Una nuova pagina **Decisioning batch in direct mail** descrive come utilizzare il motore decisionale per personalizzare i file di estrazione della direct mailing o per esportare i profili e i relativi risultati decisionali da utilizzare nei sistemi a valle. **Direct mail** è stato aggiunto come canale supportato nella documentazione di Decisioning (Guida introduttiva, Creare un criterio di decisione, Utilizzare i criteri di decisione nei messaggi, Introduzione ai criteri di decisione), inclusa la possibilità di restituire più elementi decisionali per profilo tramite il campo **[!UICONTROL Numero di elementi]**. [Ulteriori informazioni](../experience-decisioning/batch-decisioning-direct-mail.md)

* La documentazione **Frammenti di percorso** non è più contrassegnata come disponibilità limitata. La pagina ora include una nota che disambigua i frammenti di percorso dal contenuto **[!UICONTROL Frammenti]** e **Frammenti di contenuto AEM** (con collegamento incrociato da tutte e tre le pagine) e i documenti supportano **Strumenti sandbox**, **Registri di controllo** e **assegnazione tag**. Sono stati aggiunti anche frammenti di percorso alla pagina **Introduzione ai percorsi**. [Ulteriori informazioni](../building-journeys/journey-fragments.md)

* La documentazione **Origini dati esterne** e **Azione personalizzata** è stata aggiornata per l’autenticazione personalizzata. Il campo `tokenInResponse` ora consente di specificare se il `access_token` o il `id_token` viene utilizzato come credenziale di autenticazione quando un endpoint restituisce entrambi. Per l’autenticazione personalizzata basata su certificato, i campi `subType` e `aud` sono ora obbligatori, l’endpoint del token `method` deve essere `POST` e i riferimenti a “Azure Entra ID” sono stati corretti in “Microsoft Entra ID”. [Ulteriori informazioni](../datasource/external-data-sources.md#certificate-credential)

* La pagina **Introduzione a Decisioning** è stata aggiornata con un grafico di processo che riepiloga il flusso di lavoro Decisioning end-to-end, dalla gestione degli elementi decisionali e la configurazione delle strategie di selezione all’incorporamento dei criteri decisionali in un percorso o in una campagna. [Ulteriori informazioni](../experience-decisioning/gs-experience-decisioning.md#process)

* Nella documentazione **Intestazioni mittente** è ora possibile specificare che **[!UICONTROL Nome mittente]** e **[!UICONTROL E-mail mittente]** devono essere entrambi impostati o lasciati vuoti, altrimenti non è possibile pubblicare percorsi e campagne. [Ulteriori informazioni](../email/header-parameters.md#sender-header)

## Maggio 2026 {#may-2026}

* Le limitazioni e le best practice relative all’utilizzo di contenuto dinamico in frammenti visivi sono state unite in un’unica sezione **Gestire il contenuto condizionale in frammenti** per migliorarne la leggibilità. [Ulteriori informazioni](../email/use-visual-fragments.md#fragment-dynamic-content)

* Sono state aggiunte due nuove autorizzazioni di alto livello: **Gestisci registro chiavi**, che consente agli utenti di visualizzare, creare, ruotare e revocare le chiavi nel registro delle chiavi e **Visualizza registro chiavi**, che consente agli utenti di visualizzare l’elenco del registro e i dettagli delle chiavi. [Ulteriori informazioni](../administration/high-low-permissions.md#administration-permissions)

* Nella documentazione di **Utilizzare i criteri di decisione nei messaggi** è ora descritto come visualizzare la struttura completa di un criterio di decisione dal riepilogo della campagna e copiare un riepilogo tecnico JSON negli appunti per la risoluzione dei problemi. [Ulteriori informazioni](../experience-decisioning/use-decision-policy.md#decision-policy-summary)

* La pagina legacy [Modelli di ottimizzazione automatica](../offers/ranking/auto-optimization-model.md) di **gestione delle decisioni** è stata riscritta per allinearla alla documentazione aggiornata della funzione Decisioni, inclusi i requisiti e le limitazioni, la panoramica dell’apprendimento di rafforzamento, l’ottimizzazione del bilanciamento con l’apprendimento e i dettagli del campionamento di Thompson. [Ulteriori informazioni](../offers/ranking/auto-optimization-model.md)

* La pagina **Note sulla versione** è stata ristrutturata con un layout basato su argomenti. Le modifiche ora sono raggruppate per area di prodotto invece che per tipo di modifica, con una nuova sezione dedicata denominata **Miglioramenti a livello di usabilità**. Le voci disponibili a breve vengono visualizzate come pannelli a soffietto all’interno di ciascun argomento. [Ulteriori informazioni](release-notes.md)

* La pagina **Guardrail e limitazioni delle campagne orchestrate** documenta ora il limite di **attività di canale** per campagna orchestrata. [Ulteriori informazioni](../orchestrated/guardrails.md#activities-limitations)

* La documentazione **Copiare oggetti Journey Optimizer tra sandbox** ora include una nota importante per le **campagne orchestrate**: dopo l’importazione, è necessario duplicare la campagna nella sandbox di destinazione e utilizzare il duplicato per l’esecuzione, affinché il reporting acquisisca correttamente i feedback e i dati di tracciamento. [Ulteriori informazioni](../configuration/copy-objects-to-sandbox.md#copy-to-sandbox)

* La pagina **Terminologia chiave** è stata completamente rinnovata: sono stati aggiunti sei nuovi termini, introdotta una nuova sezione **Termini relativi a conflitti e all’assegnazione delle priorità** e aggiunta una nuova guida alla disambiguazione **Quando i termini sembrano simili** per quattro coppie di termini comunemente confuse. I termini specifici di Adobe Experience Platform sono stati rimossi e sostituiti con una nota collegata al glossario di Adobe Experience Platform. [Ulteriori informazioni](../start/terminology.md)

* La documentazione relativa ai **deep link** è stata ampliata con una nuova sezione **Creazione di deep link** che descrive le due opzioni disponibili per l’e-mail (interfaccia utente di E-mail designer e codice dell’editor di personalizzazione) e la sintassi della funzione URL per gli SMS. La pagina **Creare un messaggio SMS** ora include un passaggio di deep link nel flusso di authoring dei contenuti. [Ulteriori informazioni](../email/deeplinks.md)

* Il riferimento all’helper per l’**URL** è stato aggiornato con una sezione dedicata nella documentazione della personalizzazione. [Ulteriori informazioni](../personalization/functions/helpers.md#url)

* È stata aggiunta una limitazione alla documentazione dell’helper per i **metadati di esecuzione**: la funzione non è supportata nei canali in entrata (Web, esperienza basata su codice, messaggio in-app, schede di contenuto). [Ulteriori informazioni](../personalization/functions/helpers.md#execution-metadata)

* È stata aggiunta una nuova pagina **Ricette di personalizzazione** in cui sono disponibili pattern di personalizzazione pronti all’uso per i casi d’uso più comuni in [!DNL Journey Optimizer]. Vengono illustrate le ricette relative a data e ora (formattazione della data corrente, conto alla rovescia per la scadenza, calcolo dei giorni rimanenti, visualizzazione solo dell’ora e rilevamento di fine settimana e giorni feriali), le ricette di stringhe (utilizzo di `replaceAll` con assegnazione variabile) e le ricette di fallback condizionali (fallback di campi vuoti con `isEmpty`). [Ulteriori informazioni](../personalization/personalization-recipes.md)

* La documentazione relativa alla **sintassi della personalizzazione** è stata aggiornata con un’introduzione ampliata che chiarisce la differenza tra le sintassi Handlebars (`{{...}}`) e PQL (`{%= ... %}`), incluse una tabella di utilizzo, istruzioni sull’escape delle virgolette doppie letterali e una nuova sezione **Regole di sintassi PQL per le chiavi di attributo speciali** che include parole chiave riservate, chiavi di attributo con trattini e ID eventi numerici. È stata corretta anche la nota sull’escape backtick: è possibile fare riferimento direttamente ai nomi di campo con trattini nei blocchi `{{...}}`, solo la sintassi con i backtick non funziona in quel contesto. [Ulteriori informazioni](../personalization/personalization-syntax.md)

* La documentazione delle **funzioni di data e ora** è stata arricchita con nuovi esempi reali: un pattern per il conto alla rovescia per `dateDiff`, una condizione per la distinzione tra fine settimana e giorno feriale per `dayOfWeek` (con una nota sull’utilizzo dell’attività di condizione del percorso per l’indirizzamento dei casi d’uso) e un pattern per la sola visualizzazione dell’ora che combina `extractHours` e `extractMinutes` con una protezione dello zero iniziale. [Ulteriori informazioni](../personalization/functions/dates.md)

* La documentazione delle **funzioni stringa** è stata aggiornata con un nuovo esempio per `replaceAll` che mostra come assegnare il risultato a una variabile `{% let %}` per il riutilizzo in più espressioni nello stesso modello. [Ulteriori informazioni](../personalization/functions/string.md#replace-all)

* La documentazione delle **funzioni di array** è stata aggiornata con una nuova sezione **Eseguire l’iterazione di un array** che documenta l’helper di blocco Handlebars `{{#each}}`, inclusa una nota che chiarisce che `{{#each}}` è supportato solo nell’editor di personalizzazione e non può essere utilizzato all’interno di attività di condizione del percorso. [Ulteriori informazioni](../personalization/functions/arrays-list.md#each-loop)

* La pagina **Introduzione ai set di dati** è stata aggiornata con una nuova voce **In entrata** nella sezione dei set di dati di sistema che documenta il _Set di dati evento di attività in entrata di AJO_. È stata aggiunta una nota per chiarire che un profilo deve avere almeno un messaggio inviato da [!DNL Journey Optimizer] prima che i messaggi in arrivo vengano acquisiti in questo set di dati. [Ulteriori informazioni](../data/get-started-datasets.md#system-datasets)

* La documentazione relativa all’**esportazione del contenuto del messaggio** è stata ampliata con **Domande frequenti sull’esportazione dei messaggi** (contenuti personalizzati, immagini e file multimediali, collegamenti tracciati, PII, conservazione, casi d’uso, ecc.) e con **esempi di JSON esportati** per SMS ed e-mail. [Ulteriori informazioni](../configuration/message-export.md)

* Una nuova pagina **Schema di esportazione dei messaggi di AJO** documenta ogni campo del set di dati di esportazione dei messaggi di AJO, con i tipi di dati e la gerarchia per il payload di e-mail e SMS esportati. [Ulteriori informazioni](../configuration/message-export-schema.md)

* È stata aggiunta la nuova pagina **Personalizzare gli URL nelle e-mail** che consolida le indicazioni sulla personalizzazione dinamica di URL, sulla personalizzazione completa/di base di URL, sulla personalizzazione dei parametri di tracciamento di URL e sui guardrail principali. [Ulteriori informazioni](../email/url-personalization.md)

* Nella pagina con gli esempi di query è stata aggiunta una nuova sezione **Query per le regole di business** che fornisce una query data lake per controllare tutte le eliminazioni dei profili dovute alle esclusioni delle quote limite per un percorso specifico dopo una data specifica. La query include il campo `eventCodeReason` per identificare se i profili sono stati esclusi perché è stato raggiunto un limite (`CAP_REACHED`) o a causa di una priorità inferiore (`LOWER_PRIORITY`). [Ulteriori informazioni](../reports/query-examples.md#business-rules-queries)

* La documentazione sulle **proprietà del percorso** è stata aggiornata per documentare il nuovo indicatore della **dimensione corrente del payload del percorso** nel pannello delle proprietà del percorso. Questo campo di sola lettura mostra la dimensione corrente del payload del percorso rispetto al limite configurato (ad esempio 1,5 MB su 2 MB), consentendo di monitorare la complessità del percorso prima della pubblicazione e di evitare errori di pubblicazione correlati alle dimensioni. [Ulteriori informazioni](../building-journeys/journey-properties.md#journey-payload-size)

## Aprile 2026 {#april-2026}

* La documentazione dell’attività **Cambia dimensione** è stata aggiornata per chiarire che, mentre l’attività utilizza un’unione esterna e mantiene tutti i record al passaggio di modifica della dimensione, i record senza un profilo corrispondente nella nuova dimensione targeting vengono silenziosamente esclusi al momento della consegna dei messaggi. [Ulteriori informazioni](../orchestrated/activities/change-dimension.md)

* Sono stati migliorati i guardrail nella documentazione **Aggiungere un campo CC alle e-mail**. Ora specificano che l’indirizzo CC non viene controllato in base al consenso o alla soppressione, e che le aperture e i click-through dalle e-mail inviate all’indirizzo CC vengono presi in considerazione nei click e nelle aperture totali dall’analisi di invio. [Ulteriori informazioni](../configuration/cc-email-field.md)

* La documentazione delle **attività di canale** è stata aggiornata con una nuova sezione **Messaggi di marketing e messaggi transazionali** che spiega le differenze comportamentali tra le due categorie di canale: requisiti di consenso, applicazione della regola di business, tipo di configurazione dei canali e casi d’uso consigliati. [Ulteriori informazioni](../orchestrated/activities/channels.md#marketing-vs-transactional)

* La documentazione dell’**attività Fork** è stata arricchita con una nuova sezione **Esempi** che illustra come utilizzare l’attività Fork per dividere un pubblico tra due rami e-mail paralleli, uno di marketing e uno transazionale, in una singola esecuzione della campagna. [Ulteriori informazioni](../orchestrated/activities/fork.md#fork-examples)

* La documentazione dell’**attività Crea pubblico** è stata arricchita con un nuovo esempio che mostra come filtrare i profili in base a un attributo del piano di iscrizione utilizzando il generatore di regole. [Ulteriori informazioni](../orchestrated/activities/build-audience.md#build-audience-examples)

* La pagina **Introduzione alle campagne orchestrate** documenta il pattern di livello di base **Crea pubblico → Fork → Canale A + Canale B** in **Cosa include una campagna orchestrata?**, con riferimenti incrociati alle pagine relative all’attività Fork e ai messaggi di marketing e transazionali. [Ulteriori informazioni](../orchestrated/gs-orchestrated-campaigns.md#gs-ms-campaign-inside)

* La pagina **Modificare il contenuto dell’e-mail con l’editor HTML avanzato** è stata spostata dalla sezione Gestione dei contenuti alla sezione **E-mail** della documentazione. Nella pagina è ora documentato che l’editor HTML avanzato è disponibile in E-mail designer per i messaggi e-mail e per i modelli di contenuto e-mail. [Ulteriori informazioni](../email/email-expert-mode.md)

* La documentazione **Avvia e monitora le campagne orchestrate** è stata aggiornata con una nuova sezione che descrive nel dettaglio la sequenza di esecuzione interna al momento della pubblicazione, insieme a una tabella di stato del ciclo di vita della campagna, un elenco di controllo pre-pubblicazione e un avviso di conferma dell’invio per le campagne non ricorrenti. [Ulteriori informazioni](../orchestrated/start-monitor-campaigns.md#publication-sequence)

* La documentazione dell’attività **Salva pubblico** è stata aggiornata con una nota che chiarisce che le attività Salva pubblico vengono sempre eseguite prima di quelle dei messaggi al momento della pubblicazione. [Ulteriori informazioni](../orchestrated/activities/save-audience.md)

* Sono state aggiunte tre nuove domande e risposte alle **Domande frequenti sulle campagne orchestrate**: cosa accade internamente al momento della pubblicazione, un elenco di controllo in 7 punti sui motivi per cui i messaggi potrebbero non essere inviati dopo la pubblicazione e come la ricerca delle istantanee dei profili differisce dalla risoluzione dei profili in tempo reale. [Ulteriori informazioni](../orchestrated/orchestrated-campaigns-faq.md)

* È stata aggiunta una nuova sezione **[Eventi eliminati a causa di un’istanza di percorso bloccata](../building-journeys/troubleshooting-execution.md#max-instance-stack-events-reached)** alla documentazione sulla risoluzione dei problemi del percorso, che spiega il motivo dell’eliminazione di `maxInstanceStackEventsReached`, quando si verifica e come attenuarlo. Anche le pagine dell’elenco dei campi evento dei passaggi e dei guardrail sono state aggiornate di conseguenza.

* La documentazione su come **Sfrutta i frammenti nei criteri di decisione** ora include note di guardrail per il canale **E-mail**: la funzione **[!UICONTROL Simula contenuto]** non mostra i frammenti di espressione dall’elemento di decisione, mentre la funzione **[!UICONTROL Invia bozza]** e le campagne attivate lo fanno. Nella pagina viene inoltre indicato che non è possibile assegnare **[!UICONTROL frammenti visivi]** a un elemento di decisione. In questo contesto sono supportati solo **frammenti di espressione**. [Ulteriori informazioni](../experience-decisioning/fragments-decision-policies.md)

## Marzo 2026 {#march-2026}

* La documentazione relativa alla **visualizzazione in anteprima di esperienze basate su codice con Decisioni per le esperienze** ora chiarisce che **[!UICONTROL Simula contenuto]** è solo l’anteprima del contenuto. I dati contestuali provenienti dalle richieste live di Edge non vengono simulati nell’anteprima di authoring. [Ulteriori informazioni](../code-based/test-code-based.md#preview-code-based)

* La documentazione di **Utilizza i dati di Adobe Experience Platform** è stata aggiornata: i guardrail non indicano più che le ricerche dei set di dati non possono essere concatenate, in modo da riflettere il comportamento corrente del prodotto. [Ulteriori informazioni](../data/lookup-aep-data.md)

* La documentazione dell’attività **Aggiorna profilo** è stata aggiornata per documentare il supporto relativo all’aggiornamento di un massimo di cinque attributi profilo in una singola azione. [Ulteriori informazioni](../building-journeys/update-profiles.md)

* L’attività **Leggi pubblico** e la documentazione di **Proprietà del percorso** sono state aggiornate per chiarire il ciclo di vita di 91 percorsi relativo ai percorsi ricorrenti sempre attivi. La sezione di pianificazione ora conferma esplicitamente che i percorsi ricorrenti senza data di fine rimangono live oltre i 91 giorni e le domande frequenti sul timeout globale sono state espanse per distinguere il TTL del profilo di 91 giorni dalla finestra di reporting di 91 giorni. [Ulteriori informazioni](../building-journeys/read-audience.md#schedule)

* La documentazione dell’attività **Ricerca set di dati** è stata aggiornata per chiarire che la chiave di ricerca deve essere configurata in modalità avanzata affinché la sintassi `@datasetLookup{}` funzioni nelle attività delle condizioni a valle. È stata aggiunta una sezione di risoluzione dei problemi con indicazioni sulla risoluzione dell’errore “Ricerca set di dati non trovata”. [Ulteriori informazioni](../building-journeys/dataset-lookup.md#troubleshooting)

* La documentazione delle **funzioni data e ora** è stata aggiornata con un nuovo esempio che mostra come formattare una marca temporale da un attributo evento di contesto, incluso il requisito `toDateTime()`, la sintassi backtick per gli ID evento numerici e un callout di errore comune per l’errore “input non corrispondente” di PQL. [Ulteriori informazioni](../personalization/functions/dates.md#format-date)

* La documentazione sulle **limitazioni e guardrail delle campagne orchestrate** e **Introduzione ai connettori di origine** è stata aggiornata per chiarire che, per la funzione Modifica acquisizione dei dati basata su file, il campo `_change_request_type` è obbligatorio e i relativi valori devono essere in minuscolo `u` (upsert) o `d` (elimina), non in maiuscolo. [Ulteriori informazioni](../orchestrated/guardrails.md)

* La documentazione di **Aggiungi collegamenti e tiene traccia dei messaggi** è stata aggiornata con indicazioni sulla modalità di generazione degli identificatori di tracciamento (urlID): un urlID univoco viene assegnato solo quando sia l’URL che l’etichetta sono univoci. Per tenere traccia dello stesso URL in più e-mail (o più volte all’interno della stessa e-mail), gli utenti devono utilizzare un’etichetta univoca per ogni URL simile; in caso contrario, [!DNL Journey Optimizer] non è in grado di determinare quale collegamento sia stato cliccato. [Ulteriori informazioni](../email/message-tracking.md#track-across-multiple-emails)

* La documentazione **Crea profili di test** è stata aggiornata con una nota importante sui requisiti del descrittore di identità: quando un set di dati viene eliminato e ricreato, lo schema deve mantenere il descrittore di identità corretto nel campo di identità primaria. Senza di esso, i profili acquisiti non verranno contrassegnati come `testProfile = true` anche se l’acquisizione viene completata correttamente. È stato aggiunto un elenco di controllo per la risoluzione dei problemi. [Ulteriori informazioni](../audience/creating-test-profiles.md)

* La documentazione dell’attività **Leggi pubblico** è stata aggiornata per chiarire che un’attività **Evento di business** è un’eccezione alla regola per cui Leggi pubblico deve essere la prima attività di un percorso. È stata aggiunta anche una nota che fa riferimento all’attività **Ottimizza** come alternativa avanzata per il controllo del targeting del pubblico. [Ulteriori informazioni](../building-journeys/read-audience.md)

* **Invia a scaglioni** nei percorsi ora è generalmente disponibile. Il flag Disponibilità limitata è stato rimosso dalla documentazione. [Ulteriori informazioni](../delivery/send-using-waves.md)

* La documentazione dell’attività **Salta** è stata arricchita con una nuova sezione sulle strategie di progettazione, **percorsi secondari ridotti**, che spiega come suddividere flussi complessi end-to-end in percorsi secondari più piccoli e mirati, collegati tramite l’attività Salta. [Ulteriori informazioni](../building-journeys/jump.md#jump-strategy)

* La documentazione di **Tag** è stata aggiornata con indicazioni sull’utilizzo di categorie di tag in alternativa a convenzioni di denominazione complesse. Una nuova sezione spiega come configurare categorie di tag per la gestione del percorso scalabile. [Ulteriori informazioni](../building-journeys/tags.md)

* La documentazione di **Informazioni sulle origini dati** ora include una nuova sezione che consente ai professionisti di scegliere tra tre strategie di accesso ai dati: accesso ai dati esterni tramite azioni personalizzate, utilizzo di un set di dati non abilitato per Profilo o utilizzo di un set di dati abilitato per il profilo. Ogni opzione è descritta con compromessi e casi d’uso consigliati. [Ulteriori informazioni](../datasource/about-data-sources.md#data-access-strategy)

* La documentazione di **Progettazione notifiche push** è stata aggiornata con una nota che chiarisce il comportamento dei collegamenti universali su iOS: se l’URL di notifica è registrato come collegamento universale, l’app associata si aprirà indipendentemente dall’azione URL web scelta. Sono state aggiunte indicazioni su come forzare l’apertura di un browser. [Ulteriori informazioni](../push/design-push.md)

* La nuova pagina **Monitora i modelli IA** è ora disponibile nella documentazione della funzione Decisioni. Spiega come tenere traccia dello stato, dello stato di formazione e delle prestazioni dei modelli di ottimizzazione personalizzati direttamente in [!DNL Journey Optimizer]. [Ulteriori informazioni](../experience-decisioning/ranking/ai-model-observability.md)

* L’**editor HTML avanzato** (modalità esperto) per i modelli e-mail è ora disponibile in disponibilità limitata. La pagina della documentazione è ora accessibile pubblicamente. Questa funzionalità consente di visualizzare e modificare l’origine non elaborata HTML dei modelli di contenuto e-mail direttamente da E-mail designer. [Ulteriori informazioni](../email/email-expert-mode.md)

* La documentazione relativa al **tracciamento URL** e alla **risoluzione dei problemi del percorso** è stata aggiornata per documentare il comportamento di `context.system.source.actionId` in percorsi chiusi. Percorsi chiusi o non ripubblicati possono produrre segnaposti `{}` vuoti negli URL di tracciamento. Sono state aggiunte indicazioni su come risolvere il problema ripubblicando il percorso o rimuovendo il parametro interessato. [Ulteriori informazioni](../email/url-tracking.md)

* La documentazione dell’**origine dati di Adobe Experience Platform** è stata aggiornata con una nota che specifica che, nella configurazione dell’origine dati, sono supportati solo gli schemi basati sui profili individuali XDM. [Ulteriori informazioni](../datasource/adobe-experience-platform-data-source.md)

* La documentazione dei **guardrail TTL (Time-to-live) dei set di dati** è stata migliorata con una nuova voce di domande frequenti per identificare chiaramente quali set di dati sono soggetti a TTL. TTL si applica esclusivamente ai set di dati di serie temporali; i set di dati di tipo record come quelli di entità, di classificazione e gli archivi di oggetti decisionali non sono soggetti a TTL e non saranno influenzati dal rollout del guardrail. [Ulteriori informazioni](../data/datasets-ttl.md)

* Le **Proprietà percorso** e **Metti in pausa un percorso** sono state aggiornate per documentare i nuovi campi Pausa e Riprendi ora disponibili nei dettagli tecnici del percorso. Il pulsante **Copia dettagli tecnici** ora include `lastPausedAt`, `lastPausedBy`, `lastPausedById`, `lastResumedAt`, `lastResumedBy` e `lastResumedById`, oltre al blocco `pausedJourneySettings` esistente. È stata aggiunta anche una nuova sezione alla pagina **Metti in pausa un percorso** che spiega come visualizzare le marche temporali di pausa e ripresa direttamente dalle proprietà del percorso. [Ulteriori informazioni](../building-journeys/journey-properties.md)

## Febbraio 2026 {#february-2026}

* È ora disponibile una nuova pagina per la gestione delle decisioni. Questa elenca tutti gli operatori, gli helper e le funzioni supportate durante la personalizzazione del contenuto delle offerte (rappresentazioni) con l’editor di personalizzazione. Utilizza questo elenco per evitare errori di runtime. Quando si personalizzano i contenuti in Offer Decisioning, sono supportate solo le funzioni documentate. [Ulteriori informazioni](../offers/offer-library/personalization-editor-supported-functions.md)

* La documentazione di **Crea criteri di decisione** e **Utilizza criteri di decisione nei messaggi** è stata aggiornata per e-mail: una nota ora spiega che quando la stessa offerta può essere selezionata da più di un criterio di decisione nel corpo dell’e-mail, il motore deduplica le offerte (ogni posizionamento riceve un’offerta diversa). Per visualizzare la stessa offerta in più posizionamenti (ad esempio, intestazione e piè di pagina), utilizza **Riutilizza output di decisione**. [Ulteriori informazioni](../experience-decisioning/create-decision-policy.md)

* La pagina Elementi di decisione è stata aggiornata con informazioni sul canale push e sul limite di eventi personalizzati. [Ulteriori informazioni](../experience-decisioning/items.md#capping)

* La documentazione di **Ricerca evento esperienza nei percorsi** è stata aggiornata con la timeline obsoleta: a partire dal 1° aprile 2026, le organizzazioni che non hanno utilizzato attributi di evento esperienza nelle espressioni di percorso negli ultimi 90 giorni non avranno più accesso a questa funzionalità. Le domande frequenti ora si concentrano sulla timeline previdenziale e su chi è interessato, e la pagina dello schema dell’evento esperienza è stata allineata con un collegamento diretto ad approcci alternativi. [Ulteriori informazioni](../building-journeys/exp-event-lookup.md)

* La documentazione della **funzione Decisioni** è stata aggiornata per la **ricerca set di dati** con dati di Adobe Experience Platform: il guardrail dei canali supportato ora indica che la ricerca set di dati funziona per tutti i canali in cui è disponibile la funzione Decisioni (esperienza basata su codice, e-mail, push, SMS e attività di decisione sui contenuti nei percorsi). Le note sulla versione beta pubblica e sulla disponibilità limitata sono state rimosse dalle pagine dedicate alle regole di decisione, alle formule di ranking e agli elementi decisionali. [Ulteriori informazioni](../experience-decisioning/aep-data-exd.md)

* La pagina di integrazione dei sistemi esterni è stata aggiornata con i collegamenti alle origini dati e alle azioni personalizzati e chiarisce che il proxy di uscita fornisce un IP statico per le chiamate in uscita da **azioni personalizzate** ai sistemi esterni. [Ulteriori informazioni](../configuration/external-systems.md)

* La documentazione sull’esecuzione di prova del percorso è stata chiarita: per gli attributi di evento del passaggio `inDryRun` e `dryRunID` viene ora indicato che restituiscono `true`/ID istanza in modalità di esecuzione di prova e `null` per percorsi test o live. Le indicazioni per escludere gli eventi del passaggio di esecuzione in prova nelle query di reporting sono state aggiornate di conseguenza. [Ulteriori informazioni](../building-journeys/journey-dry-run.md)

* **Web push** ora è generalmente disponibile. La documentazione delle notifiche push è stata ristrutturata e aggiornata di conseguenza (introduzione, progettazione, invio, creazione). [Ulteriori informazioni](../push/get-started-push.md)

* La pagina Configurazione di web push è ora disponibile nella documentazione. [Ulteriori informazioni](../push/push-configuration-web.md)

* La documentazione sull’utilizzo dei frammenti nella funzione Decisioni è stata aggiornata: sono state aggiunte note nelle sezioni Frammenti e funzione Decisioni ed è stata aggiornata la pagina Frammenti nei criteri di decisione. [Ulteriori informazioni](../experience-decisioning/fragments-decision-policies.md)

* La documentazione del webhook SMS è stata aggiornata: il contenuto del webhook Twilio è stato rimosso. [Ulteriori informazioni](../mobile/mobile-webhook.md)

* La documentazione di **Converti immagini in modelli di contenuto** è stata migliorata con guardrail e consigli espansi, casi d’uso comuni e indicazioni più chiare per convertire le progettazioni di immagini in modelli di contenuto HTML modificabili. Essa menziona anche il fatto che ora puoi utilizzare un tema come input per la conversione. [Ulteriori informazioni](../content-management/image-to-html.md)

* La documentazione API di migrazione della funzione Decisioni è stata aggiornata. [Ulteriori informazioni](../experience-decisioning/decisioning-migration-api.md)

* L’attività **Decisione sui contenuti** ora è generalmente disponibile. La pagina dell’attività Decisione sui contenuti è stata aggiornata con una sezione sui dati di Decisioning disponibile negli eventi del passaggio. [Ulteriori informazioni](../building-journeys/content-decision.md)

* Nella sezione Sfide di fedeltà sono stati aggiunti collegamenti alla documentazione API delle sfide di fidelizzazione (introduzione, crea sfide, crea attività, accedi alle sfide di fidelizzazione). [Ulteriori informazioni](../loyalty-challenges/get-started.md)

* Le informazioni sui canali supportati nella documentazione relativa alla procedura guidata di creazione della campagna sono state corrette. Le pagine Domande frequenti nell’Introduzione ai canali e alle campagne orchestrate sono state aggiornate di conseguenza. [Ulteriori informazioni](../campaigns/get-started-with-campaigns.md)

* La documentazione sulle autorizzazioni è stata corretta per quanto riguarda le autorizzazioni **Gestione percorso** e **Approva**. [Ulteriori informazioni](../administration/ootb-permissions.md)

* La documentazione sulle integrazioni di AEM (Adobe Experience Manager) è stata aggiornata con la denominazione rivista (contenuto dinamico AEM e frammenti AEM). [Ulteriori informazioni](../integrations/aem-fragments.md)

* È stato aggiunto un nuovo motivo di esclusione all’elenco esclusioni: **UnsubscribeLinkNotValid** (codice di errore 050081). Questa esclusione viene generata quando la lunghezza dell’oggetto mailTo per l’annullamento dell’iscrizione a mailing list supera il limite RFC di 998 caratteri. [Ulteriori informazioni](../reports/exclusion-list.md)

* La documentazione della funzione helper formatDate è stata migliorata con una nota con cui la funzione richiede un tipo di campo data-ora (non una stringa) e con più esempi: formattazione di un campo data-ora, conversione di una stringa in data per prima, data completa con nome del giorno, data dinamica dall’ora di sistema e formato giorno della settimana con output in minuscolo. [Ulteriori informazioni](../personalization/functions/dates.md#format-date)

* La documentazione e-mail relativa alla versione di testo è stata migliorata con indicazioni complete sui casi d’uso, inclusi i criteri decisionali per l’utilizzo del testo normale personalizzato rispetto alla sincronizzazione automatica, esempi pratici con scenari reali e una sezione Domande frequenti con domande comuni. [Ulteriori informazioni](../email/text-version-email.md#when-to-use)

* La documentazione sui temi di E-mail designer è stata aggiornata con informazioni sulle limitazioni relative al supporto dei caratteri web e sull’importanza dei caratteri di fallback. [Ulteriori informazioni](../email/apply-email-themes.md#themes-guardrails)

* È stata aggiunta una limitazione alla documentazione dell’helper per i metadati di esecuzione per chiarire che i metadati non vengono acquisiti per i profili esclusi dall’azione. [Ulteriori informazioni](../personalization/functions/helpers.md#execution-metadata)

* La documentazione sugli esempi di implementazione basati su codice è stata aggiornata per includere il campo token in propositionAction per un tracciamento e un’attribuzione accurati in Decisioning. [Ulteriori informazioni](../code-based/code-based-implementation-samples.md#client-side-how)

* È stata aggiunta una nota alla documentazione relativa al tracciamento degli URL e di annullamento iscrizione alla mailing list per chiarire che l’ordine dei parametri di tracciamento aggiunti agli URL è casuale e non può essere controllato. [Ulteriori informazioni](../email/url-tracking.md)

## Gennaio 2026 {#january-2026}

* La documentazione della dashboard Utilizzo licenze è stata chiarita con indicazioni aggiornate su **Profili coinvolgibili**, inclusi i dettagli sulla definizione e le indicazioni per la risoluzione dei problemi. [Ulteriori informazioni](../audience/license-usage.md#what-is-engageable-profile)

* È stata aggiunta una nota alla documentazione sui temi di E-mail designer per chiarire le limitazioni relative al supporto dei caratteri web. [Ulteriori informazioni](../email/apply-email-themes.md#themes-guardrails)

* È stata aggiunta una nuova sezione guardrail per documentare la convalida della dimensione del payload del percorso, comprese le soglie per avvertenze ed errori e indicazioni su come ottimizzare i percorsi. [Ulteriori informazioni](../start/guardrails.md#journey-payload-size)

* La documentazione sui guardrail per la funzione Decisioni è stata aggiornata per includere i limiti di dimensione degli elementi decisionali (1 KB per gli elementi che includono attributi, con un massimo di 30 attributi). [Ulteriori informazioni](../experience-decisioning/decisioning-guardrails.md)

* È stata aggiunta una nota alla documentazione sulla creazione dei criteri di decisione per informare gli utenti che, una volta creato un criterio di decisione, eventuali modifiche possono richiedere fino a 15 minuti per essere propagate in tutte le aree geografiche dei dati e fino a 30 minuti per il Canada. [Ulteriori informazioni](../experience-decisioning/create-decision-policy.md#review)

* È stata aggiunta una nota alla documentazione sui frammenti per avvisare che, quando sia l’etichetta che l’URL del pulsante sono resi modificabili in un frammento, il set di dati di tracciamento registra il valore dell’URL invece del valore dell’etichetta. [Ulteriori informazioni](../content-management/customizable-fragments.md#visual)

* È ora disponibile una nuova pagina che descrive i vantaggi della migrazione dalla gestione delle decisioni alla funzione Decisioni, con informazioni sulle API per gli strumenti di migrazione in arrivo. [Ulteriori informazioni](../experience-decisioning/migrate-to-decisioning.md)

* È stato aggiunto un guardrail per chiarire che i set di dati di ricerca sono disponibili per l’attivazione in entrata basata su Edge solo nell’area geografica in cui risiede la sandbox del set di dati. [Ulteriori informazioni](../data/lookup-aep-data.md#guidelines)

* È stata aggiunta una nuova sezione alla documentazione sulla configurazione del canale delle campagne orchestrate, in cui viene spiegato come utilizzare gli attributi contestuali (come ID campagna, nome e dettagli delle azioni) nei parametri di tracciamento URL a scopo di analisi e reporting. [Ulteriori informazioni](../orchestrated/channel-config.md#url-tracking)

* La documentazione sull’ottimizzazione dei contenuti è stata ristrutturata per migliorarne la chiarezza. La pagina di ottimizzazione principale è stata divisa in quattro specifiche pagine secondarie: una pagina di introduzione, una pagina dedicata al targeting, una alla sperimentazione e un’altra alla combinazione di entrambi questi approcci. [Ulteriori informazioni](../content-management/gs-message-optimization.md)

* Le note in merito alla disponibilità limitata sono state rimosse da tre avvisi di percorso (Percorso pubblicato, Percorso completato e Limitazione azione personalizzata attivata), in quanto queste funzioni sono ora state rilasciate in disponibilità generale. [Ulteriori informazioni](../reports/alerts.md)

* La pagina di destinazione Test, convalida e approvazione è stata migliorata con nuove sezioni che includono una panoramica delle funzionalità di test, risposte alle domande più comuni, struttura decisionale con collegamenti di navigazione e terminologia migliorata con collegamenti alla documentazione. [Ulteriori informazioni](../../rp_landing_pages/test-landing-page.md)

* È stata aggiunta una nuova sezione alla documentazione sulla sintassi di personalizzazione per chiarire come utilizzare parole chiave riservate in espressioni di personalizzazione. Se utilizzate come nomi dei campi nello schema XDM, alcune parole chiave PQL come `next`, `last` e `this` devono essere sottoposte a escaping, racchiudendole tra apici inversi (backtick). [Ulteriori informazioni](../personalization/personalization-syntax.md#reserved-keywords)

* Le pagine [Introduzione alle campagne](../campaigns/get-started-with-campaigns.md) e [Gestione campagne](../campaigns/manage-campaigns.md) sono state ristrutturate con un’architettura delle informazioni migliorata, che include un flusso di lavoro completo con guide specifiche per tipo, confronti migliorati tra tipi di campagna e tabella di stato consolidata.

* La pagina di destinazione Percorsi è stata rinnovata per facilitare l’onboarding con un nuovo flusso di lavoro in 6 passaggi, confronti migliorati tra tipi di percorso e una navigazione migliorata all’interno della documentazione. [Ulteriori informazioni](../building-journeys/journey.md)

* È stata aggiunta una sezione dettagliata per aiutare gli utenti a generare chiavi private OpenSSH con codifica base64 per l’autenticazione SFTP durante la configurazione dell’indirizzamento dei file per direct mail per evitare errori di connessione. [Ulteriori informazioni](../direct-mail/direct-mail-configuration.md#ssh-key-generation)

* È stata aggiunta una nota alla documentazione sulla delega del sottodominio per informare gli utenti di consentire la propagazione DNS per 24-48 ore prima di tentare la delega a Adobe. [Ulteriori informazioni](../configuration/delegate-subdomain.md#set-up-subdomain)
