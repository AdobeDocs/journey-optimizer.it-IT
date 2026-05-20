---
solution: Journey Optimizer
product: journey optimizer
title: Configurare il programma fedeltà
description: Scopri come configurare i provider di premi, le definizioni degli eventi e le impostazioni dell’organizzazione per il programma fedeltà in Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="Beta privata" type="Informative"
mini-toc-levels: 1
exl-id: f8a3b2c1-4d5e-6f7a-8b9c-0d1e2f3a4b5c
source-git-commit: aea783bd8f2351d4a5d8aa6b84c24a713a6c0306
workflow-type: tm+mt
source-wordcount: '1221'
ht-degree: 2%

---

# Configurare il programma fedeltà {#loyalty-admin}

>[!BEGINSHADEBOX]

**Documentazione sulle sfide di fedeltà:**

* [Introduzione alle sfide di fedeltà](get-started.md)
* [Accesso e gestione di sfide e attività](access-loyalty-challenges.md)
* [Creare le sfide](create-challenges.md)
* [Creare le attività](create-tasks.md)
* [Monitorare le prestazioni della sfida fedeltà](loyalty-reporting.md)
* **Configura il programma fedeltà** ◀︎ **Sei qui**
* [Riferimento API per le sfide di fedeltà](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Questa funzionalità è attualmente in **versione beta privata**. Per informazioni dettagliate sul ciclo di rilascio e sulle fasi di disponibilità, consulta [Ciclo di rilascio di Journey Optimizer](../rn/releases.md).

Nella sezione **[!UICONTROL Amministratore fedeltà]** puoi configurare la modalità di connessione di Journey Optimizer al backend del programma fedeltà. Gli addetti al marketing utilizzano **[!UICONTROL Sfide di fidelizzazione (Beta)]** per progettare sfide, attività, contenuti e messaggi. L&#39;amministratore della fidelizzazione è una configurazione separata e monouso per la gestione dei premi e la mappatura degli eventi.

Quando un cliente completa una sfida (o raggiunge un traguardo di ricompensa), Journey Optimizer chiama il provider di ricompense configurato qui per consegnare punti o altri premi. Le impostazioni **[!UICONTROL Contenuto]**, **[!UICONTROL Messaggistica]** e **[!UICONTROL Pubblico]** della sfida non sono interessate dalla configurazione dell&#39;amministratore della fedeltà.

## Accedi all’amministrazione per la fedeltà {#access-loyalty-admin}

Per aprire Amministratore fedeltà, accedi a Journey Optimizer e seleziona **[!UICONTROL Amministratore fedeltà]** nel menu di navigazione a sinistra.

<!-- SCREENSHOT: Loyalty Admin entry in the left navigation -->

L’interfaccia di amministrazione è organizzata in schede. A seconda dell&#39;organizzazione, è possibile che vengano visualizzate **[!UICONTROL Impostazioni globali]**, **[!UICONTROL Provider di premi]**, **[!UICONTROL Definizioni eventi]** e **[!UICONTROL Inventario prodotti]**.

## Impostazioni globali {#global-settings}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_global_settings"
>title="Impostazioni globali"
>abstract="Seleziona lo spazio dei nomi dell’identità Adobe Experience Platform per il programma fedeltà e copia l’ID configurazione. Queste impostazioni a livello di organizzazione sono necessarie prima che i fornitori di premi possano soddisfare correttamente i premi."

Utilizza **[!UICONTROL Impostazioni globali]** per configurare le opzioni a livello di organizzazione per le sfide di fedeltà.

1. Apri la scheda **[!UICONTROL Impostazioni globali]**.

1. Nel menu a discesa **[!UICONTROL Spazio dei nomi]**, seleziona lo [spazio dei nomi delle identità](https://experienceleague.adobe.com/it/docs/experience-platform/identity/features/namespaces) da Adobe Experience Platform utilizzato dal programma fedeltà. Seleziona **[!UICONTROL Salva]** per aggiornare lo spazio dei nomi nella configurazione delle sfide di fedeltà della tua organizzazione.

1. Copiare l&#39;**[!UICONTROL ID configurazione]** se è necessario condividerlo con il team di implementazione o i sistemi esterni.

<!-- SCREENSHOT: Global settings tab showing namespace drop-down, Save, and Configuration ID -->

## Provider di premi {#reward-providers}

Un **provider di premi** indica a Journey Optimizer dove inviare chiamate di evasione quando viene registrato l&#39;avanzamento della sfida o quando viene completata una sfida, ad esempio un&#39;API che attribuisce punti fedeltà o stelle a un account membro.

Un fornitore di premi include:

* Dettagli della connessione di base (nome, descrizione, URL API, intestazioni)
* **[!UICONTROL Definizioni premi]** — tipi di premio che questo provider può assegnare (ad esempio, stelle o miglia)
* **[!UICONTROL Ricompensa proxy]** (facoltativo): instradare le chiamate tramite un proxy anziché direttamente all&#39;endpoint
* **[!UICONTROL Generatori di token di autenticazione]**: in che modo Journey Optimizer ottiene i token di accesso prima di richiamare l&#39;API

### Creare un provider di premi {#create-reward-provider}

Per registrare un nuovo provider di premi e le relative risorse, eseguire la procedura seguente.

1. Apri la scheda **[!UICONTROL Provider di premi]** e inizia a creare un provider.

1. Immetti un **[!UICONTROL Nome]** e una **[!UICONTROL Descrizione]**, quindi l&#39;**[!UICONTROL URL API]** a cui vengono inviate le richieste di evasione.

1. Aggiungi **[!UICONTROL Intestazioni]** in base alle esigenze della tua API (ad esempio, chiavi API o tipi di contenuto). Puoi aggiungere o rimuovere righe di intestazione nell’interfaccia utente.

1. Configura **[!UICONTROL Definizioni premi]**:

   * Definisci ogni tipo di premio supportato dal provider, ad esempio punti programma o stelle.
   * È possibile contrassegnare una definizione come **predefinita** per tale provider.
   * Specifica il **payload** inviato con chiamate di evasione per ogni definizione.

1. Facoltativamente, configurare un proxy **[!UICONTROL Ricompensa]**:

   * **[!UICONTROL Host]**, **[!UICONTROL Porta]** e credenziali
   * **[!UICONTROL Nome]**, **[!UICONTROL Descrizione]** e se il proxy è **abilitato**

1. Configura un **[!UICONTROL generatore di token di autenticazione]** se l&#39;API richiede un token prima di ogni chiamata:

   * URL endpoint token e metodo HTTP (ad esempio, **POST** per flussi in stile OAuth)
   * **[!UICONTROL Chiave token]** nella risposta (ad esempio, `access_token`)
   * Intestazioni richieste dall’endpoint token

   Journey Optimizer richiede un token da questa configurazione prima di chiamare l&#39;API di ricompensa, pertanto le chiamate utilizzano le credenziali correnti.

1. Selezionare **[!UICONTROL Crea provider di premi]**. Il provider e le relative risorse secondarie (definizioni, proxy e generatore di token) vengono creati insieme.

<!-- SCREENSHOT: Reward provider creation form with definitions, proxy, and auth token sections -->

Dopo la creazione, il provider viene visualizzato nell&#39;elenco dei provider di premi. Gli addetti al marketing selezionano questo provider durante [la configurazione dei premi per la sfida](create-challenges.md#rewards).

### Modificare un provider di premi {#edit-reward-provider}

1. Apri la scheda **[!UICONTROL Provider di premi]** e seleziona un provider.

1. Aggiorna il nome, la descrizione, l’URL o le intestazioni del provider in base alle esigenze.

1. Per modificare le **[!UICONTROL definizioni dei premi]**, **[!UICONTROL proxy dei premi]** o **[!UICONTROL generatori di token di autenticazione]**, aprire la sezione corrispondente e modificare i campi. Le modifiche a queste risorse secondarie vengono salvate quando vengono aggiornate.

<!-- SCREENSHOT: Reward provider detail view with child resource sections -->

>[!NOTE]
>
>Per **[!UICONTROL problemi relativi all&#39;immissione di dati]** in cui le attività e i premi derivano interamente dall&#39;integrazione dei dati, i provider di premi configurati in questo punto potrebbero non essere applicabili. [Ulteriori informazioni sulle sfide relative ai dati](create-challenges.md#create-the-challenge).

## Definizioni degli eventi {#event-definitions}

**[!UICONTROL Definizioni di eventi]** mappa gli eventi di esperienza in arrivo nel formato del tuo marchio alle attività che le sfide di fidelizzazione possono utilizzare, in particolare **[!UICONTROL Attività evento personalizzato]**. Quando i dati arrivano dai canali, Journey Optimizer utilizza queste definizioni per decidere se un evento è rilevante e come interpretarlo. Gli eventi che non corrispondono ad alcuna definizione vengono ignorati.

### Creare una definizione di evento {#create-event-definition}

1. Apri la scheda **[!UICONTROL Definizioni evento]** e crea una nuova definizione.

1. Immetti un **[!UICONTROL Nome]** per l&#39;evento (ad esempio, `Coffee purchase`). Questo nome è ciò che gli addetti al marketing selezionano quando configurano un&#39;attività **[!UICONTROL Evento personalizzato]**.

1. Specificare come identificare l&#39;evento nei payload in ingresso:

   * **[!UICONTROL Percorso identificatore]** — Percorso JSON del campo che identifica l&#39;evento o il membro (ad esempio, `data.memberId`)
   * **[!UICONTROL Valori identificatore]** — valori che devono essere presenti affinché la definizione corrisponda

1. Facoltativamente, specifica un **[!UICONTROL ID schema XDM]** e/o utilizza i campi **[!UICONTROL Schema]** e **[!UICONTROL Trasformatore]** per incollare lo schema e le stringhe di trasformazione utilizzati dal team per analizzare e convalidare il JSON in ingresso prima dell&#39;elaborazione.

   Puoi fornire un ID schema XDM, un percorso di identificazione o entrambi, a seconda di come sono strutturati i tuoi eventi.

1. Salva la definizione dell’evento.

<!-- SCREENSHOT: Event definition form with identifier path, values, and schema fields -->

La maggior parte delle organizzazioni crea più definizioni di evento, una per attività di cui desidera tenere traccia (ad esempio, acquisto, check-in o visita del sito). [Scopri come utilizzare le attività evento personalizzate nelle sfide](create-tasks.md#choose-activity).

## Inventario prodotti {#product-inventory}

La scheda **[!UICONTROL Inventario prodotti]** ti consente di caricare un file CSV per mappare gli identificatori di prodotti o elementi (ad esempio, ID MPG) ai gruppi di prodotti utilizzati per l&#39;idoneità delle attività. Questo supporta scenari in cui le attività fanno riferimento a prodotti raggruppati anziché a singoli SKU digitati manualmente.

1. Apri la scheda **[!UICONTROL Inventario prodotti]**.

1. Carica il file di mappatura trascinandolo nell’area di caricamento o sfogliandolo per selezionarlo.

1. Esaminare le mappature importate nell&#39;elenco di inventario. Seleziona un gruppo di prodotti per visualizzare tutti gli articoli del gruppo. Utilizza la ricerca per trovare gli elementi in base al nome o all’ID.

1. Utilizza **[!UICONTROL Cronologia caricamento]** per visualizzare i caricamenti precedenti.

<!-- SCREENSHOT: Product inventory list after CSV upload -->

>[!NOTE]
>
>**[!UICONTROL Le esclusioni globali]** per l&#39;inventario dei prodotti sono pianificate per una versione futura e non sono documentate qui.

## Rapporto tra amministrazione fidelizzazione e sfide {#how-admin-relates-to-challenges}

| Area | Configurato in Amministratore fedeltà | Configurato in Sfide fedeltà |
|------|----------------------------|----------------------------------|
| API per l’adempimento dei premi | Sì — i fornitori di premi | No - seleziona solo provider e importi |
| Mappatura di eventi per attività personalizzate | Sì — Definizioni degli eventi | No — seleziona il nome dell&#39;evento nelle attività evento personalizzate |
| Mappature dei gruppi di prodotti | Sì - inventario prodotti | No: utilizza i gruppi durante l&#39;authoring di attività di acquisto/spesa |
| Struttura della sfida, contenuto, pubblico | No | Sì |

Ordine di impostazione tipico:

1. Configura **[!UICONTROL Impostazioni globali]** e almeno un **[!UICONTROL Provider di premi]** in Amministratore fedeltà.
1. È possibile aggiungere **[!UICONTROL Definizioni evento]** e **[!UICONTROL Inventario prodotto]** se il programma utilizza eventi personalizzati o gruppi di prodotti basati su CSV.
1. Crea [attività](create-tasks.md) e [sfide](create-challenges.md) in **[!UICONTROL Sfide fedeltà (Beta)]**, selezionando il provider di premi e le definizioni configurate.

Adobe Journey Optimizer invia chiamate di evasione al provider quando i clienti ottengono premi; la piattaforma fedeltà è responsabile dell&#39;accredito dell&#39;account del membro.

## Prerequisiti {#prerequisites}

L’Amministratore per la fedeltà è destinato a un piccolo gruppo di amministratori dell’organizzazione. Oltre alle autorizzazioni necessarie per [Sfide fedeltà](get-started.md#prerequisites), è necessario disporre dell&#39;accesso per configurare le impostazioni fedeltà a livello di organizzazione.

Contatta l&#39;amministratore se **[!UICONTROL Amministratore fedeltà]** non viene visualizzato nel menu di navigazione a sinistra o se non riesci a salvare le impostazioni globali o i provider di premi.
