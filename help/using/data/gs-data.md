---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione alla gestione dei dati in Journey Optimizer
description: Scopri come i dati fluiscono in e da Adobe Journey Optimizer, compresi i concetti chiave, i passaggi di configurazione e le protezioni.
feature: Data Management
role: Developer, Admin, User
level: Beginner, Intermediate
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
source-git-commit: 7094cb2717f36042fa0aec1c6442f8d00c593823
workflow-type: tm+mt
source-wordcount: '2442'
ht-degree: 1%

---


# Introduzione alla gestione dei dati {#about-data}

I dati sono alla base di ogni percorso, decisione e messaggio consegnato con [!DNL Adobe Journey Optimizer].

Questa pagina offre un punto di partenza pratico per comprendere:

* I blocchi predefiniti di dati di base utilizzati da Journey Optimizer (schemi, set di dati, identità, profili)
* Utilizzo dei dati di Adobe Experience Platform in Journey Optimizer
* Quali passaggi di configurazione dei dati deve completare il team prima di creare percorsi e campagne
* Come procedere per la configurazione dettagliata e le best practice

Utilizza questa guida insieme ai tuoi data engineer, amministratori e addetti al marketing in modo che tutti possano condividere un’immagine comune del modo in cui i dati scorrono da e verso Journey Optimizer.

>[!TIP]
>Ti avvicini ora alla gestione dati in Journey Optimizer? Guarda il [tutorial sulla configurazione della panoramica dei dati](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/data-management/set-up-data-overview){target="_blank"} per una guida pratica e intuitiva di schemi, set di dati e origini.

## Utilizzo dei dati di Adobe Experience Platform in Journey Optimizer {#aep-data}

[!DNL Adobe Journey Optimizer] è basato su [!DNL Adobe Experience Platform]. Non mantiene un archivio dati separato e isolato. Invece, utilizza la stessa base di dati delle altre applicazioni Experience Cloud.

Gli schemi e i set di dati risiedono in Adobe Experience Platform. Le identità e il [Profilo cliente in tempo reale](../audience/get-started-profiles.md) sono gestiti dal servizio identità e dal servizio profili. Journey Optimizer legge i dati dei profili e degli eventi da Adobe Experience Platform per valutare le condizioni del percorso, personalizzare i messaggi e selezionare le offerte. Scrive di nuovo i dati di interazione, come gli eventi di invio, apertura, clic e mancato recapito e gli eventi dei passaggi del percorso, nei set di dati di Experience Platform. Può anche cercare set di dati aggiuntivi in fase di esecuzione senza copiare tali dati nel profilo.

>[!TIP]
>Considera Adobe Experience Platform come il tuo livello dati centrale e Journey Optimizer come un’applicazione che orchestra percorsi e messaggi utilizzando la base dati condivisa.

➡️ [Ulteriori informazioni sull&#39;architettura di Journey Optimizer](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/get-started/essentials/understanding-ajo#architecture-details){target="_blank"}

## Concetti chiave dei dati in Journey Optimizer {#key-concepts}

Quando lavori con i dati in Journey Optimizer, incontrerai diversi concetti correlati. La tabella seguente offre una rapida panoramica; le sezioni che seguono spiegano ogni concetto in modo più dettagliato.

| Concetto | Che cos’è | Uso principale in Journey Optimizer |
|---|---|---|
| Schema XDM | Regole che rappresentano, convalidano e formattano i dati (create da una classe + gruppi di campi) | Attributi del profilo del modello ed eventi comportamentali |
| Set di dati | Tabella di archiviazione per i dati conformi a uno schema | Conserva i dati di profilo, evento e generati dal sistema |
| Connettore Source | Trasmette o batch i dati da sistemi esterni in AEP | Acquisire dati CRM, analitici e web |
| Origine dati | Espone AEP o campi esterni all’interno di percorsi | Condizioni del percorso di alimentazione e personalizzazione dei messaggi |
| Identità | Identificatore che rappresenta in modo univoco un singolo cliente | Unire i profili tra i canali |
| Cerca set di dati | Riferimento runtime ai dati di AEP senza archiviazione profilo | Arricchire i messaggi con dati di riferimento live |

### Schema (schema XDM) {#schema}

Uno schema è un insieme di regole che rappresentano, convalidano e formattano i dati. È composto da una **classe** (che definisce il comportamento di base: record o serie temporale) e da **gruppi di campi** facoltativi (che aggiungono campi specifici). Gli schemi vengono definiti utilizzando gli standard Experience Data Model (XDM) e risiedono in Adobe Experience Platform.

XDM esiste per risolvere un problema reale: lo stesso concetto — un cliente, un acquisto, un prodotto — è denominato e strutturato in modo diverso tra i sistemi di origine. XDM fornisce un linguaggio condiviso che unifica questi concetti in un’unica definizione, indipendentemente da dove hanno origine i dati. Questo consente a Journey Optimizer di lavorare in modo coerente con i dati del tuo CRM, del tuo sito web, della tua app mobile e del tuo data warehouse allo stesso tempo.

In Journey Optimizer, in genere si utilizzano gli schemi **Profilo individuale XDM** per gli attributi del cliente (nome, preferenze, consenso) e gli schemi **ExperienceEvent XDM** per gli eventi comportamentali (acquisti, visualizzazioni di pagina, iscrizioni).

➡️ [Ulteriori informazioni sugli schemi](get-started-schemas.md)

### Set di dati {#dataset}

Un set di dati è un costrutto di archiviazione e gestione per dati conformi a uno schema, ovvero una tabella con un set definito di colonne e righe. Tutti i dati utilizzati da Journey Optimizer vengono memorizzati nei set di dati di Adobe Experience Platform. Possono essere set di dati di profilo (che contribuiscono a Real-Time Customer Profile), set di dati di eventi (che memorizzano i dati comportamentali per percorsi e analisi) o set di dati di sistema creati automaticamente da Journey Optimizer per il tracciamento, il feedback e gli eventi delle fasi del percorso.

➡️ [Ulteriori informazioni sui set di dati](get-started-datasets.md)

### Connettore Source {#source-connector}

Un connettore di origine (noto anche come **sorgente**) consente di acquisire dati da più sistemi, come Adobe Analytics, Adobe Experience Platform Web SDK, l&#39;archiviazione cloud (S3, Azure Blob) o i database CRM, in Adobe Experience Platform. Oltre all’acquisizione raw, i connettori consentono la strutturazione, l’etichettatura e il miglioramento dei dati utilizzando i servizi Experience Platform, inclusa la mappatura dei campi per gli schemi XDM e l’etichettatura per la governance dei dati.

➡️ [Ulteriori informazioni sui connettori di origine](../start/get-started-sources.md)

### Origine dati (Journey Optimizer) {#data-source}

Un’origine dati in Journey Optimizer definisce quali campi di Adobe Experience Platform (o API esterne) sono esposti all’interno di percorsi e messaggi. Configurate nell’interfaccia utente di Journey Optimizer, le origini dati in genere includono l’origine dati integrata di Adobe Experience Platform (che espone gli attributi del profilo cliente in tempo reale) e le origini dati esterne o personalizzate facoltative chiamate in fase di esecuzione del percorso per un ulteriore arricchimento. Vengono utilizzati per le condizioni di percorso, le azioni personalizzate e la personalizzazione dei messaggi.

➡️ [Ulteriori informazioni sulle origini dati](../datasource/about-data-sources.md)

>[!NOTE]
>Il [glossario di Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/landing/glossary){target="_blank"} definisce genericamente &quot;origine dati&quot; come l&#39;origine dei dati (CRM, app mobile, ecc.). In Journey Optimizer, l&#39;**origine dati** ha un significato specifico: una configurazione dell&#39;interfaccia utente che controlla quali campi sono esposti all&#39;interno di percorsi e messaggi.

### Identità e profilo cliente in tempo reale {#identity}

Un’identità è un identificatore che rappresenta in modo univoco un singolo cliente, ad esempio un ID cookie, un ID dispositivo, un indirizzo e-mail o un ID CRM. Le identità sono organizzate in namespace (E-mail, ECID, CRMID) e più identità per la stessa persona sono unite in un grafico di identità unificato. Real-Time Customer Profile utilizza tale grafico per mantenere una visualizzazione olistica di ogni singolo cliente combinando dati provenienti da più canali, inclusi online, offline, CRM e origini di terze parti.

Un concetto chiave per i principianti è il modello **frammento di profilo**. Ogni volta che un cliente interagisce con il tuo marchio su un dispositivo o canale specifico (il tuo sito web, l’app mobile o uno store), tale interazione viene registrata come frammento di profilo: una visualizzazione parziale del cliente in base a quel punto di contatto specifico. Real-Time Customer Profile unisce continuamente questi frammenti in base a valori di identità condivisi, creando un profilo completo e aggiornato. Journey Optimizer legge da questo profilo assemblato per valutare le condizioni, selezionare le offerte e personalizzare i messaggi in tempo reale.

➡️ [Ulteriori informazioni sulle identità in Journey Optimizer](../audience/get-started-identity.md)

### Cerca set di dati {#lookup-dataset}

Un set di dati di ricerca consente a Journey Optimizer di recuperare dati di riferimento o transazionali in fase di esecuzione da un set di dati Adobe Experience Platform, senza archiviarli nel profilo cliente in tempo reale. Questo è utile per modificare frequentemente i dati di riferimento (prezzi, inventario, ore di immagazzinamento) o i dati transazionali necessari al momento del messaggio ma che non appartengono al profilo. Journey Optimizer esegue la ricerca durante l’esecuzione del percorso o del messaggio in base a una chiave, ad esempio un ID prodotto.

➡️ [Ulteriori informazioni sui set di dati di ricerca](lookup-aep-data.md)

## Elenco di controllo per la preparazione dei dati {#checklist}

Prima che gli esperti di marketing inizino a creare percorsi e campagne, la tua organizzazione deve completare una serie di passaggi di preparazione ai dati. In questo modo Journey Optimizer è in grado di utilizzare i dati corretti, al momento giusto e in modo conforme.

>[!NOTE]
>I passaggi seguenti coinvolgono più ruoli: data engineer, amministratori e addetti al marketing. Utilizza questo elenco di controllo come piano condiviso per preparare il tuo ambiente. I passaggi 1-4 sono completati in Adobe Experience Platform; i passaggi 5-6 sono configurati in Journey Optimizer.

I sei passaggi seguenti descrivono l’intero processo di configurazione dei dati, dalla configurazione dell’identità alla verifica del corretto flusso dei dati in Journey Optimizer:

1. Definire la strategia di identità
1. Progettare schemi per dati di profilo ed eventi
1. Creare set di dati abilitati per il profilo
1. Acquisire dati dalle origini
1. Configurare le origini dati in Journey Optimizer
1. Verifica il tracciamento, il feedback e i set di dati di percorso

+++ Definire la strategia di identità

Scegli un’identità primaria per i clienti (ad esempio ECID, e-mail o CRMID) e configura i namespace corrispondenti nel servizio Adobe Experience Platform Identity. Assicurati che i campi di identità siano presenti negli schemi abilitati per il profilo e verifica che i profili siano uniti correttamente nel grafo delle identità.

➡️ [Ulteriori informazioni sulle identità in Journey Optimizer](../audience/get-started-identity.md)

+++

+++ Progettare schemi per dati di profilo ed eventi

Crea schemi di **Profilo individuale XDM** per acquisire gli attributi del cliente come nome e informazioni di contatto, preferenze e interessi, fase del ciclo di vita o stato del consenso. Crea schemi **XDM ExperienceEvent** per acquisire dati comportamentali e transazionali come eventi web e app, acquisti e interazioni offline. Se necessario, contrassegna i campi corretti come identità e attributi di profilo.

➡️ [Ulteriori informazioni sugli schemi](get-started-schemas.md)

+++

+++ Creare set di dati abilitati per il profilo

In Adobe Experience Platform, crea set di dati basati sugli schemi XDM e abilita Profilo su qualsiasi set di dati che dovrebbe contribuire a Real-Time Customer Profile. Conferma che i set di dati generati dal sistema e creati da Journey Optimizer siano visibili nell’area di lavoro Set di dati.

➡️ [Ulteriori informazioni sui set di dati](get-started-datasets.md)

+++

+++ Acquisire dati dalle origini

Configura i connettori di origine per i sistemi aziendali, ad esempio Adobe Analytics, Adobe Experience Platform Web SDK o le piattaforme CRM e POS, e mappa i campi in ingresso sugli schemi XDM. Verifica che i dati arrivino nei set di dati corretti e vengano visualizzati nel Profilo cliente in tempo reale, dove previsto.

➡️ [Ulteriori informazioni sui connettori di origine](../start/get-started-sources.md)

➡️ [Tutorial: crea set di dati e acquisisci dati](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/data-management/create-datasets-and-ingest-data){target="_blank"}

+++

+++ Configurare le origini dati in Journey Optimizer

Le origini dati sono un concetto specifico di Journey Optimizer: non si trovano dove risiedono i dati, ma dove si dichiarano i campi che Journey Optimizer è autorizzata a leggere durante l’esecuzione del percorso e del messaggio. Prima che un percorso possa valutare una condizione come &quot;il cliente è un membro fedeltà?&quot; Per personalizzare un messaggio con un nome, i campi del profilo pertinenti devono essere esposti tramite una configurazione dell’origine dati.

Journey Optimizer include un&#39;origine dati integrata di [Adobe Experience Platform](../datasource/adobe-experience-platform-data-source.md) che consente l&#39;accesso diretto agli attributi del profilo cliente in tempo reale. Questo copre la stragrande maggioranza dei casi d’uso: lettura degli attributi del profilo per la personalizzazione o controllo dei campi di consenso e preferenza. È inoltre possibile configurare [origini dati esterne](../datasource/external-data-sources.md) per chiamare API di terze parti in fase di esecuzione del percorso, ad esempio per recuperare un punteggio di fedeltà in tempo reale, un consiglio di prodotto o un livello di inventario dello store non memorizzato in Adobe Experience Platform.

>[!NOTE]
>L’accesso diretto ai dati dell’evento esperienza tramite l’origine dati integrata di Adobe Experience Platform è diventato obsoleto e viene progressivamente disabilitato. [Ulteriori informazioni](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/orchestrate-journeys/journey-use-cases/exp-event-lookup){target="_blank"}.

La configurazione delle origini dati è un’attività amministrativa che sblocca l’intero livello dati per gli autori di percorso e gli esperti di marketing. Una volta esposto tramite un’origine dati, un campo diventa disponibile nel generatore di condizioni di percorso, negli editor di personalizzazione dei messaggi e nelle regole di Offer Decisioning, senza richiedere alcun lavoro tecnico aggiuntivo in fase di creazione del percorso.

➡️ [Ulteriori informazioni sulla configurazione origine dati](../datasource/about-data-sources.md)

+++

+++ Verifica il tracciamento, il feedback e i set di dati di percorso

Conferma che i set di dati generati dal sistema di Journey Optimizer siano disponibili nell’area di lavoro Set di dati. Esegui percorsi di test e campagne, quindi utilizza Query Editor per verificare che gli eventi di invio, apertura, clic e mancato recapito siano registrati e che gli eventi e gli stati dei passaggi di percorso siano acquisiti correttamente. Utilizza questi set di dati per il monitoraggio continuo, la risoluzione dei problemi e l’ottimizzazione del percorso.

➡️ [Ulteriori informazioni sulle query in Journey Optimizer](get-started-queries.md)

+++

## Guardrail e considerazioni sulla progettazione dei dati {#guardrails}

Alcuni guardrail e limitazioni del prodotto possono influenzare il modo in cui progettate il modello di dati e i percorsi. Esamina questi elementi in anticipo per evitare di rielaborarli in seguito.

>[!IMPORTANT]
>Per informazioni aggiornate, consulta sempre la pagina [Guardrail e limitazioni di Journey Optimizer](../start/guardrails.md). I riepiloghi che seguono evidenziano alcuni elementi chiave, ma potrebbero evolvere nel tempo.

### Set di dati di sistema e TTL di Journey Optimizer {#datasets-ttl}

Journey Optimizer crea diversi set di dati generati dal sistema per il tracciamento, il feedback e gli eventi dei passaggi del percorso. A partire da febbraio 2025, in alcuni di questi set di dati viene introdotto un guardrail time-to-live (TTL), che potrebbe influenzare la durata di conservazione dei dati per l’analisi e la risoluzione dei problemi.

➡️ [Ulteriori informazioni sui guardrail TTL del set di dati](datasets-ttl.md)

### Segmentazione in streaming ed eventi Journey Optimizer {#streaming-segmentation}

A partire dal 1° novembre 2024, la segmentazione in streaming non supporta più eventi di invio e apertura dai set di dati di tracciamento e feedback di Journey Optimizer. Per casi d&#39;uso come il limite di frequenza e la gestione dell&#39;eccesso, utilizza [Regole aziendali](../conflict-prioritization/rule-sets.md) invece di segmenti di streaming basati su eventi di invio/apertura.

➡️ [Ulteriori informazioni sui set di dati](get-started-datasets.md)

### Ricerca e decisioning del set di dati {#lookup-guardrails}

La ricerca del set di dati è ideale per la modifica frequente di attributi (inventario, prezzi, meteo) o dati che non devono essere memorizzati nel Profilo cliente in tempo reale. Prima di progettare la strategia di ricerca, consulta i guardrail specifici del prodotto, come i limiti di dimensione dei set di dati e i limiti di query nella relativa documentazione.

➡️ [Ulteriori informazioni sui set di dati di ricerca](lookup-aep-data.md)

## Esempio: preparazione dei dati per un percorso di benvenuto {#example}

L&#39;esempio seguente mostra come i concetti di questa pagina funzionano insieme in uno scenario semplice.

1. Un tecnico dati crea uno schema [Profilo individuale XDM](get-started-schemas.md) per gli attributi del cliente (nome, e-mail, livello fedeltà, consenso) e uno schema XDM ExperienceEvent per gli eventi di abbonamento web.
1. [I set di dati abilitati per il profilo](get-started-datasets.md) vengono creati per ogni schema: uno per gli attributi di gestione delle relazioni con i clienti e uno per gli eventi di registrazione.
1. I team Web e mobili trasmettono gli eventi di registrazione tramite Adobe Experience Platform Web SDK; i dati CRM vengono acquisiti tramite un [connettore di origine](../start/get-started-sources.md).
1. Un amministratore configura l&#39;origine dati [Adobe Experience Platform](../datasource/adobe-experience-platform-data-source.md) in Journey Optimizer ed espone campi come `profile.person.name.firstName`, `profile.personalEmail.address` e `profile.loyaltyTier`.
1. Un addetto marketing [crea un percorso di benvenuto](../building-journeys/journey-gs.md) che ascolta un evento di registrazione e utilizza gli attributi del profilo per [personalizzare l&#39;e-mail di benvenuto](../personalization/personalize.md). Journey Optimizer scrive gli eventi di invio e apertura nei set di dati di tracciamento e registra l’avanzamento del percorso nei set di dati evento delle fasi del percorso.
1. Uno sviluppatore utilizza [Query Editor](get-started-queries.md) per verificare che gli eventi scorrano correttamente e analizza le prestazioni (aperture, clic, tempo di invio). Il team regola il percorso e il contenuto in base a queste informazioni.

Questo flusso illustra il modo in cui schemi, set di dati, origini, origini dati e query interagiscono in un caso d’uso completo e intuitivo.

## Risorse correlate {#related-resources}

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=it)

**Introduzione agli schemi**

Scopri come creare schemi XDM in Adobe Experience Platform, scegliere le classi e i gruppi di campi giusti e modellare gli attributi del profilo e gli eventi comportamentali.

[Ulteriori informazioni](get-started-schemas.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg?lang=it)

**Utilizzare i set di dati**

Scopri come creare set di dati abilitati per profili ed eventi, monitorare l’acquisizione dei dati ed esplorare i set di dati generati dal sistema e creati automaticamente da Journey Optimizer per il tracciamento, il feedback e gli eventi dei passaggi del percorso.

[Ulteriori informazioni](get-started-datasets.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=it)

**Configurare origini dati**

Linee guida dettagliate sulla configurazione dell’origine dati integrata di Adobe Experience Platform e delle origini dati esterne facoltative per esporre i campi del profilo e le risposte API esterne all’interno dei percorsi.

[Ulteriori informazioni](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=it)

**Usa dati di Adobe Experience Platform (ricerca)**

Scopri come arricchire i messaggi in fase di esecuzione con dati di riferimento o transazionali dai set di dati di AEP, senza archiviarli nel profilo cliente in tempo reale.

[Ulteriori informazioni](lookup-aep-data.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=it)

**Introduzione alle query**

Utilizza Query Service per analizzare i set di dati di Journey Optimizer, verificare che gli eventi scorrano correttamente e creare query di reporting sui dati di invio, apertura, clic e mancato recapito.

[Ulteriori informazioni](get-started-queries.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=it)

**Introduzione ai profili**

Scopri come funziona Real-Time Customer Profile in Journey Optimizer e come sfogliare, esaminare e convalidare i singoli profili dei clienti nell’interfaccia utente di Platform.

[Ulteriori informazioni](../audience/get-started-profiles.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=it)

**Tutorial sulla configurazione della panoramica dei dati**

Un video per principianti sulla configurazione dei dati in Journey Optimizer, che tratta schemi, set di dati e origini end-to-end.

[Guarda l&#39;esercitazione](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/data-management/set-up-data-overview){target="_blank"}
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=it)

**Crea set di dati e acquisisci tutorial dati**

Un tutorial pratico che mostra come creare set di dati in Adobe Experience Platform e acquisire dati utilizzando i connettori di origine, con istruzioni dettagliate che puoi seguire nella tua sandbox.

[Guarda l&#39;esercitazione](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/data-management/create-datasets-and-ingest-data){target="_blank"}
:::

::::
