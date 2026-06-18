---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione alla gestione dei dati in Journey Optimizer
description: Scopri come i dati fluiscono in e da Adobe Journey Optimizer, compresi i concetti chiave, i passaggi di configurazione e i guardrail.
feature: Data Management
role: Developer, Admin, User
level: Beginner, Intermediate
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
TQID: https://experienceleague.adobe.com/Dq8mzkfuxvcoAPI1vjq9lFHjz4Z5j9s42-kfMy59PeI
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: aeebb91a-f216-4d5f-8da1-3a7e6f696ed0
subfeature_v2: id: a1cdc218-59b7-4eef-b5cf-2a7ad74b3371id: d6e5c7fd-c1d6-4137-98cd-138ccde6752fid: cf3fbcd7-c075-4ae4-8de5-96e736ab2ea3id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: cc72dcf1-72e1-48cc-b434-e7c27d62d67cid: d095671a-1355-40aa-8b5f-06c33c68080bid: ebde5b41-29c9-4f5e-9ef6-1197e85409e3id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: cbcb1cb0abbb8d4c6ea173c4deff071d0081da4e
workflow-type: tm+mt
source-wordcount: 2650
ht-degree: 98%

---

# Introduzione alla gestione dei dati {#about-data}

>[!BEGINSHADEBOX]

**In questa pagina:** ottieni una panoramica pratica del flusso di dati in entrata e in uscita da Adobe Journey Optimizer, inclusi schemi, set di dati, identità, profili e origini dati, in modo che il tuo team possa completare i passaggi di preparazione ai dati prima di creare percorsi e campagne.

>[!ENDSHADEBOX]

I dati costituiscono la base di ogni percorso, decisione e messaggio consegnato con [!DNL Adobe Journey Optimizer].

Questa pagina offre un punto di partenza pratico per comprendere:

* I blocchi predefiniti di dati di base utilizzati da Journey Optimizer (schemi, set di dati, identità, profili)
* Come Journey Optimizer utilizza i dati di Adobe Experience Platform
* Quali passaggi di configurazione dei dati deve completare il team prima di creare percorsi e campagne
* Come procedere per la configurazione dettagliata e le best practice

Utilizza questa guida insieme ai data engineer, amministratori e marketer in modo che tutti possano condividere una visione comune del modo in cui i dati fluiscono da e verso Journey Optimizer.

>[!TIP]
>La gestione dati in Journey Optimizer è per te una novità? Guarda il [tutorial di presentazione Configurazione dei dati](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/data-management/set-up-data-overview){target="_blank"} per una guida pratica e intuitiva su schemi, set di dati e origini.

## Come Journey Optimizer utilizza i dati di Adobe Experience Platform {#aep-data}

[!DNL Adobe Journey Optimizer] è basato su [!DNL Adobe Experience Platform]. Non mantiene un archivio dati separato e isolato. Utilizza invece la stessa base dati delle altre applicazioni [!DNL CX Enterprise].

Gli schemi e i set di dati risiedono in Adobe Experience Platform. Le identità e il [Profilo cliente in tempo reale](../audience/get-started-profiles.md) sono gestiti da Identity Service e dal servizio Profilo. Journey Optimizer legge i dati dei profili e degli eventi da Adobe Experience Platform per valutare le condizioni dei percorsi, personalizzare i messaggi e selezionare le offerte. Scrive i dati di interazione, tra cui gli eventi di invio, apertura, clic e mancato recapito e gli eventi dei passaggi del percorso, all’interno dei set di dati di Experience Platform. Può inoltre cercare set di dati aggiuntivi durante il runtime senza copiare tali dati nel profilo.

>[!TIP]
>Considera Adobe Experience Platform come un livello dati centrale e Journey Optimizer come un’applicazione che orchestra percorsi e messaggi utilizzando la base dati condivisa.

➡️ [Ulteriori informazioni sull’architettura di Journey Optimizer](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/get-started/essentials/understanding-ajo#architecture-details){target="_blank"}

## Concetti chiave sui dati in Journey Optimizer {#key-concepts}

Quando utilizzi i dati in Journey Optimizer, incontrerai diversi concetti correlati. La tabella seguente offre una rapida panoramica; le sezioni che seguono spiegano ogni concetto in modo più dettagliato.

| Concetto | Che cos’è | Uso principale in Journey Optimizer |
|---|---|---|
| Schema XDM | Regole che rappresentano, convalidano e formattano i dati (create da una classe + gruppi di campi) | Modellare attributi di profilo ed eventi comportamentali |
| Set di dati | Tabella di archiviazione per i dati conformi a uno schema | Conservare i dati di profilo, evento e generati dal sistema |
| Connettore di origine | Trasmette o invia in batch i dati da sistemi esterni in AEP | Acquisire dati CRM, di analisi e web |
| Origine dati | Espone AEP o campi esterni all’interno di percorsi | Alimentare le condizioni dei percorsi e la personalizzazione dei messaggi |
| Identità | Identificatore che rappresenta in modo univoco un singolo cliente | Unire i profili tra i canali |
| Set di dati di ricerca | Riferimento durante il runtime ai dati di AEP senza archiviazione nel profilo | Arricchire i messaggi con dati di riferimento live |

### Schema (schema XDM) {#schema}

Uno schema è un set di regole che rappresentano, convalidano e formattano i dati. È composto da una **classe** (che definisce il comportamento di base: record o serie temporale) e da **gruppi di campi** facoltativi (che aggiungono campi specifici). Gli schemi vengono definiti utilizzando gli standard Experience Data Model (XDM) e risiedono in Adobe Experience Platform.

XDM esiste per risolvere un problema reale: lo stesso concetto, (un cliente, un acquisto, un prodotto) è denominato e strutturato in modo diverso nei vari sistemi di origine. XDM fornisce un linguaggio condiviso che unifica questi concetti in un’unica definizione, indipendentemente da dove hanno origine i dati. Questo consente a Journey Optimizer di utilizzare in modo coerente i dati del tuo CRM, sito web, app mobile e data warehouse allo stesso tempo.

In Journey Optimizer, in genere vengono utilizzati gli schemi **Profilo individuale XDM** per gli attributi del cliente (nome, preferenze, consenso) e gli schemi **ExperienceEvent XDM** per gli eventi comportamentali (acquisti, visualizzazioni di pagina, iscrizioni).

➡️ [Ulteriori informazioni sugli schemi](get-started-schemas.md)

### Set di dati {#dataset}

Un set di dati è un costrutto di archiviazione e gestione per dati conformi a uno schema; puoi considerarlo come una tabella con un set definito di colonne e righe. Tutti i dati utilizzati da Journey Optimizer vengono memorizzati nei set di dati di Adobe Experience Platform. Possono essere set di dati di profilo (che contribuiscono al Profilo cliente in tempo reale), set di dati di eventi (che archiviano i dati comportamentali per percorsi e analisi) o set di dati di sistema creati automaticamente da Journey Optimizer per il tracciamento, il feedback e gli eventi relativi ai passaggi di un percorso.

➡️ [Ulteriori informazioni sui set di dati](get-started-datasets.md)

### Connettore di origine {#source-connector}

Un connettore di origine (noto anche come **origine**) consente di acquisire dati da più sistemi, come Adobe Analytics, Adobe Experience Platform Web SDK, l’archiviazione cloud (S3, Azure Blob) o i database CRM, in Adobe Experience Platform. Oltre all’acquisizione non elaborata, i connettori consentono la strutturazione, l’etichettatura e il miglioramento dei dati utilizzando i servizi Experience Platform, inclusa la mappatura dei campi per gli schemi XDM e l’etichettatura per la governance dei dati.

➡️ [Ulteriori informazioni sui connettori di origine](../start/get-started-sources.md)

### Origine dati (Journey Optimizer) {#data-source}

Un’origine dati in Journey Optimizer definisce quali campi di Adobe Experience Platform (o API esterne) vengono esposti all’interno di percorsi e messaggi. Configurate nell’interfaccia utente di Journey Optimizer, le origini dati includono solitamente l’origine dati integrata di Adobe Experience Platform (che espone gli attributi del Profilo cliente in tempo reale) e le origini dati esterne o personalizzate facoltative, richiamate durante l’esecuzione del percorso per un ulteriore arricchimento. Vengono utilizzate per le condizioni del percorso, le azioni personalizzate e la personalizzazione dei messaggi.

➡️ [Ulteriori informazioni sulle origini dati](../datasource/about-data-sources.md)

>[!NOTE]
>Il [glossario di Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/landing/glossary){target="_blank"} definisce l’“Origine dati” in modo generico come l’origine dei dati (un CRM, un’app mobile, ecc.). In Journey Optimizer, l’**origine dati** ha un significato specifico: una configurazione dell’interfaccia utente che controlla quali campi vengono esposti all’interno di percorsi e messaggi.

### Identità e profilo cliente in tempo reale {#identity}

Un’identità è un identificatore che rappresenta in modo univoco un singolo cliente, ad esempio un ID cookie, un ID dispositivo, un indirizzo e-mail o un ID CRM. Le identità sono organizzate in spazi dei nomi (E-mail, ECID, CRMID) e identità multiple di una stessa persona vengono unite in un grafo identità unificato. Profilo cliente in tempo reale utilizza tale grafo per mantenere una visione completa di ogni singolo cliente combinando dati provenienti da più canali, inclusi quelli online, offline, CRM e origini di terze parti.

Un concetto chiave per i principianti è il modello **frammento di profilo**. Ogni volta che un cliente interagisce con il tuo brand su un dispositivo o canale specifico (il tuo sito web, l’app mobile o un negozio), tale interazione viene registrata come un frammento di profilo: una vista parziale di tale cliente basata su quel punto di contatto specifico. Il Profilo cliente in tempo reale unisce continuamente questi frammenti in base a valori di identità condivisi, creando un profilo completo e aggiornato. Journey Optimizer legge da questo profilo assemblato per valutare le condizioni, selezionare le offerte e personalizzare i messaggi in tempo reale.

➡️ [Ulteriori informazioni sulle identità in Journey Optimizer](../audience/get-started-identity.md)

### Set di dati di ricerca {#lookup-dataset}

Un set di dati di ricerca consente a Journey Optimizer di recuperare dati di riferimento o transazionali durante la fase di esecuzione da un set di dati Adobe Experience Platform, senza archiviare tali dati nel profilo cliente in tempo reale. Questo è utile per i dati di riferimento che cambiano frequentemente (prezzi, inventario, orari del negozio) o per i dati transazionali necessari al momento dell’invio del messaggio, ma che non appartengono al profilo. Journey Optimizer esegue la ricerca durante l’esecuzione dei percorsi o dei messaggi in base a una chiave, ad esempio un ID prodotto.

➡️ [Ulteriori informazioni sui set di dati di ricerca](lookup-aep-data.md)

## Elenco di controllo per la preparazione dei dati {#checklist}

Prima che i marketer inizino a creare percorsi e campagne, la tua organizzazione deve completare una serie di passaggi per la preparazione dei dati. Questo garantisce che Journey Optimizer possa utilizzare dati corretti, al momento giusto e in modo conforme.

>[!NOTE]
>I passaggi seguenti coinvolgono più ruoli: data engineer, amministratori e marketer. Utilizza questo elenco di controllo come piano condiviso per preparare il tuo ambiente. I passaggi 1-4 vengono completati in Adobe Experience Platform; i passaggi 5-6 vengono configurati in Journey Optimizer.

I sei passaggi seguenti ti guideranno attraverso l’intero processo di configurazione dei dati, dalla configurazione dell’identità alla verifica del corretto flusso dei dati in Journey Optimizer:

1. Definire la strategia di identità
1. Progettare schemi per dati di profilo ed eventi
1. Creare set di dati abilitati per il profilo
1. Acquisire i dati dalle origini
1. Configurare le origini dati in Journey Optimizer
1. Verificare tracciamento, feedback e i set di dati di percorso

+++ Definire la strategia di identità

Scegli un’identità principale per i clienti (ad esempio ECID, e-mail o CRMID) e configura gli spazi dei nomi corrispondenti in Adobe Experience Platform Identity Service. Assicurati che i campi di identità siano presenti negli schemi abilitati per il profilo e conferma che i profili siano uniti correttamente nel grafo delle identità.

➡️ [Ulteriori informazioni sulle identità in Journey Optimizer](../audience/get-started-identity.md)

+++

+++ Progettare schemi per dati di profilo ed eventi

Crea schemi di **Profilo individuale XDM** per acquisire gli attributi del cliente come nome e informazioni di contatto, preferenze e interessi, fase del ciclo di vita o stato del consenso. Crea schemi **XDM ExperienceEvent** per acquisire dati comportamentali e transazionali come eventi web e app, acquisti e interazioni offline. Contrassegna i campi corretti come identità e attributi di profilo, se appropriato.

➡️ [Ulteriori informazioni sugli schemi](get-started-schemas.md)

+++

+++ Creare set di dati abilitati per il profilo

In Adobe Experience Platform, crea set di dati basati sugli schemi XDM e abilita il Profilo su tutti i set di dati che dovrebbero contribuire al Profilo cliente in tempo reale. Conferma che i set di dati generati dal sistema e creati da Journey Optimizer siano visibili nell’area di lavoro Set di dati.

➡️ [Ulteriori informazioni sui set di dati](get-started-datasets.md)

+++

+++ Acquisire i dati dalle origini

Configura i connettori di origine per i sistemi aziendali, ad esempio Adobe Analytics, Adobe Experience Platform Web SDK o le piattaforme CRM e POS, e mappa i campi in ingresso sugli schemi XDM. Verifica che i dati arrivino nei set di dati corretti e vengano visualizzati nel Profilo cliente in tempo reale, dove previsto.

➡️ [Ulteriori informazioni sui connettori di origine](../start/get-started-sources.md)

➡️ [Tutorial: creare set di dati e acquisire dati](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/data-management/create-datasets-and-ingest-data){target="_blank"}

+++

+++ Configurare le origini dati in Journey Optimizer

Le origini dati sono un concetto specifico di Journey Optimizer: non si trovano dove risiedono i dati, ma dove dichiari i campi che Journey Optimizer è autorizzata a leggere durante l’esecuzione dei percorsi e dei messaggi. Prima che un percorso possa valutare una condizione come “Il cliente è un membro fidelizzato?” o personalizzare un messaggio con un nome, i campi del profilo pertinenti devono essere esposti tramite una configurazione dell’origine dati.

Journey Optimizer include un’[origine dati di Adobe Experience Platform](../datasource/adobe-experience-platform-data-source.md) incorporata che fornisce l’accesso diretto agli attributi del Profilo cliente in tempo reale. Questo copre la stragrande maggioranza dei casi d’uso: lettura degli attributi del profilo per la personalizzazione o controllo dei campi relativi a consenso e preferenze. Inoltre puoi configurare [origini dati esterne](../datasource/external-data-sources.md) per chiamare API di terze parti in fase di runtime del percorso, ad esempio per recuperare un punteggio fedeltà in tempo reale, un consiglio di prodotto o un livello di inventario del negozio non memorizzato in Adobe Experience Platform.

>[!NOTE]
>L’accesso diretto ai dati degli eventi esperienza tramite l’origine dati incorporata di Adobe Experience Platform è diventato obsoleto e verrà progressivamente disabilitato. [Ulteriori informazioni](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/orchestrate-journeys/journey-use-cases/exp-event-lookup){target="_blank"}.

La configurazione delle origini dati è un’attività amministrativa che sblocca l’intero livello dati per autori di percorso e marketer. Una volta esposto tramite un’origine dati, un campo diventa disponibile nel generatore di condizioni di percorso, negli editor di personalizzazione dei messaggi e nelle regole di Offer Decisioning, senza richiedere alcun lavoro tecnico aggiuntivo in fase di creazione del percorso.

➡️ [Ulteriori informazioni sulla configurazione dell’origine dati](../datasource/about-data-sources.md)

+++

+++ Verificare tracciamento, feedback e i set di dati di percorso

Conferma che i set di dati generati dal sistema di Journey Optimizer siano disponibili nell’area di lavoro Set di dati. Esegui percorsi di test e campagne, quindi utilizza Editor di query per verificare che gli eventi di invio, apertura, clic e mancato recapito vengano registrati e che gli eventi e gli stati dei passaggi dei percorsi siano acquisiti correttamente. Utilizza questi set di dati per il monitoraggio continuo, la risoluzione dei problemi e l’ottimizzazione dei percorsi.

➡️ [Ulteriori informazioni sulle query in Journey Optimizer](get-started-queries.md)

+++

## Guardrail e considerazioni sulla progettazione dei dati {#guardrails}

Alcuni guardrail e limitazioni di prodotto possono influenzare il modo in cui progetti il modello di dati e i percorsi. Rivedi questi elementi in anticipo per evitare di rielaborarli in seguito.

>[!IMPORTANT]
>Per le informazioni più recenti, consulta sempre la pagina [Guardrail e limitazioni di Journey Optimizer](../start/guardrails.md). I riepiloghi che seguono evidenziano alcuni elementi chiave, ma potrebbero evolvere nel tempo.

### Set di dati di sistema e TTL di Journey Optimizer {#datasets-ttl}

Journey Optimizer crea diversi set di dati generati dal sistema per il tracciamento, il feedback e gli eventi dei passaggi del percorso. A partire da febbraio 2025, in alcuni di questi set di dati viene introdotto un guardrail time-to-live (TTL), che potrebbe influenzare la durata di conservazione dei dati per l’analisi e la risoluzione dei problemi.

➡️ [Ulteriori informazioni sui guardrail TTL del set di dati](datasets-ttl.md)

### Segmentazione in streaming ed eventi Journey Optimizer {#streaming-segmentation}

A partire dal 1° novembre 2024, la segmentazione in streaming non supporterà più eventi di invio e apertura dai set di dati di feedback e tracciamento di Journey Optimizer. Per casi d’uso come la quota limite e la gestione dell’eccesso, utilizza le [Regole di business](../conflict-prioritization/rule-sets.md) invece di segmenti di streaming basati su eventi di invio/apertura.

➡️ [Ulteriori informazioni sui set di dati](get-started-datasets.md)

### Funzione Decisioni e ricerca del set di dati {#lookup-guardrails}

La ricerca del set di dati è ideale per la modifica frequente di attributi (inventario, prezzi, meteo) o dati che non devono essere memorizzati nel Profilo cliente in tempo reale. Prima di progettare la strategia di ricerca, rivedi i guardrail specifici del prodotto, come i limiti di dimensione dei set di dati e i limiti di query nella relativa documentazione.

➡️ [Ulteriori informazioni sui set di dati di ricerca](lookup-aep-data.md)

## Esempio: preparazione dei dati per un percorso di benvenuto {#example}

L’esempio seguente mostra come i concetti di questa pagina collaborano in uno scenario semplice.

1. Un data engineer crea uno [schema Profilo individuale XDM](get-started-schemas.md) per gli attributi del cliente (nome, e-mail, livello fedeltà, consenso) e uno schema XDM ExperienceEvent per gli eventi di registrazione web.
1. [I set di dati abilitati per il profilo](get-started-datasets.md) vengono creati per ogni schema: uno per gli attributi CRM e uno per gli eventi di registrazione.
1. I team web e per dispositivi mobili trasmettono gli eventi di registrazione tramite Adobe Experience Platform Web SDK; i dati CRM vengono acquisiti tramite un [connettore di origine](../start/get-started-sources.md).
1. Un amministratore configura l’[origine dati Adobe Experience Platform](../datasource/adobe-experience-platform-data-source.md) in Journey Optimizer ed espone campi come `profile.person.name.firstName`, `profile.personalEmail.address` e `profile.loyaltyTier`.
1. Un marketer [crea un percorso di benvenuto](../building-journeys/journey-gs.md) che ascolta un evento di registrazione e utilizza tali attributi di profilo per [personalizzare l’e-mail di benvenuto](../personalization/personalize.md). Journey Optimizer scrive gli eventi di invio e apertura nei set di dati di tracciamento e registra l’avanzamento del percorso nei set di dati evento dei passaggi del percorso.
1. Uno sviluppatore utilizza [Editor di query](get-started-queries.md) per verificare che gli eventi scorrano correttamente e analizza le prestazioni (aperture, clic, tempo di invio). Il team regola il percorso e il contenuto in base a queste informazioni.

Questo flusso illustra il modo in cui schemi, set di dati, origini, origini dati e query collaborano in un caso d’uso completo e intuitivo.

## Risorse correlate {#related-resources}

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

**Introduzione agli schemi**

Scopri come creare schemi XDM in Adobe Experience Platform, scegliere le classi e i gruppi di campi appropriati e modellare gli attributi del profilo e gli eventi comportamentali.

[Ulteriori informazioni](get-started-schemas.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg)

**Utilizzare i set di dati**

Scopri come creare set di dati abilitati per profili ed eventi, monitorare l’acquisizione dei dati ed esplorare i set di dati generati dal sistema e creati automaticamente da Journey Optimizer per il tracciamento, il feedback e gli eventi dei passaggi del percorso.

[Ulteriori informazioni](get-started-datasets.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

**Configurare le origini dati**

Istruzioni dettagliate sulla configurazione dell’origine dati integrata di Adobe Experience Platform e delle origini dati esterne facoltative per esporre i campi del profilo e le risposte API esterne all’interno dei percorsi.

[Ulteriori informazioni](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg)

**Utilizzare i dati di Adobe Experience Platform (ricerca)**

Scopri come arricchire i messaggi in fase di runtime con dati di riferimento o transazionali provenienti dai set di dati di AEP, senza memorizzarli nel profilo cliente in tempo reale.

[Ulteriori informazioni](lookup-aep-data.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

**Introduzione alle query**

Utilizza Query Service per analizzare i set di dati di Journey Optimizer, verificare che gli eventi fluiscano correttamente e creare query di reporting sui dati di invio, apertura, clic e mancato recapito.

[Ulteriori informazioni](get-started-queries.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

**Introduzione ai profili**

Scopri come funziona il Profilo cliente in tempo reale in Journey Optimizer e come sfogliare, ispezionare e convalidare i singoli profili dei clienti nell’interfaccia utente di Platform.

[Ulteriori informazioni](../audience/get-started-profiles.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

**Tutorial di presentazione Configurazione dei dati**

Una descrizione dettagliata con video intuitivo sulla configurazione dei dati in Journey Optimizer, che include schemi, set di dati e origini end-to-end.

[Guarda il tutorial](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/data-management/set-up-data-overview){target="_blank"}
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

**Tutorial per creare set di dati e acquisire dati**

Un tutorial pratico che mostra come creare set di dati in Adobe Experience Platform e acquisire dati utilizzando i connettori di origine, con istruzioni dettagliate che puoi seguire nella tua sandbox.

[Guarda il tutorial](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/data-management/create-datasets-and-ingest-data){target="_blank"}
:::

::::
