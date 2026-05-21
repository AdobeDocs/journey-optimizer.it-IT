---
solution: Journey Optimizer
product: journey optimizer
title: Configurare il programma fedeltà
description: Scopri come configurare i provider di premi, le definizioni degli eventi e le impostazioni a livello di organizzazione per il programma fedeltà in Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="Beta privata" type="Informative"
mini-toc-levels: 1
exl-id: f8a3b2c1-4d5e-6f7a-8b9c-0d1e2f3a4b5c
source-git-commit: a4ad533e54f3692eb0483138a8cfd1cee0e77ba1
workflow-type: tm+mt
source-wordcount: '1128'
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

Nella sezione **[!UICONTROL Amministratore fedeltà]** puoi configurare la modalità di connessione di Journey Optimizer ai sistemi fedeltà esterni. Gli addetti al marketing utilizzano **[!UICONTROL Sfide di fedeltà (Beta)]** per progettare sfide, attività, contenuti e messaggi. **[!UICONTROL Amministratore fidelizzazione]** è un&#39;area separata di sola amministrazione per l&#39;adempimento dei premi, la mappatura degli eventi e l&#39;inventario dei prodotti.

Quando un cliente completa una sfida o raggiunge un traguardo di ricompensa, Journey Optimizer chiama il provider di ricompense configurato per fornire punti o altri premi. La configurazione in **[!UICONTROL Amministrazione fedeltà]** non influisce sulle impostazioni **[!UICONTROL Contenuto]**, **[!UICONTROL Messaggistica]** o **[!UICONTROL Pubblico]**, che rimangono sotto il controllo dell&#39;addetto marketing.

## Confronto tra le configurazioni qui e quelle relative alle sfide di fedeltà {#scope}

| Area | Configurato in Amministratore fedeltà | Configurato in Sfide fedeltà |
|------|----------------------------|----------------------------------|
| API per l’adempimento dei premi | Sì — i fornitori di premi | No - seleziona solo provider e importi |
| Mappatura di eventi per attività personalizzate | Sì — Definizioni degli eventi | No — seleziona il nome dell&#39;evento nelle attività evento personalizzate |
| Mappature dei gruppi di prodotti | Sì - inventario prodotti | No: utilizza i gruppi durante l&#39;authoring di attività di acquisto/spesa |
| Struttura della sfida, contenuto, pubblico | No | Sì |

Adobe Journey Optimizer invia chiamate di evasione al provider di premi quando i clienti ottengono premi. La tua piattaforma fedeltà è responsabile dell’accredito dell’account dell’utente.

## Prerequisiti {#prerequisites}

**[!UICONTROL Amministratore fedeltà]** è destinato a un numero limitato di amministratori per organizzazione. Oltre alle autorizzazioni necessarie per [Sfide fedeltà](get-started.md#prerequisites), è necessario disporre dell&#39;accesso a livello di amministratore per l&#39;istanza di Journey Optimizer. Contatta il tuo amministratore Adobe per richiedere l’accesso.

## Accedi all’amministrazione per la fedeltà {#access-loyalty-admin}

Per aprire **[!UICONTROL Amministratore fidelizzazione]**, selezionalo dalla navigazione a sinistra in Journey Optimizer.

<!-- SCREENSHOT: Loyalty Admin entry in the left navigation -->

**[!UICONTROL L&#39;amministratore fedeltà]** è organizzato in schede: **[!UICONTROL Impostazioni globali]**, **[!UICONTROL Provider premi]**, **[!UICONTROL Definizioni eventi]** e **[!UICONTROL Inventario prodotti]**. Le schede disponibili dipendono dalle autorizzazioni della tua organizzazione e dalla configurazione delle funzioni.

## Impostazioni globali {#global-settings}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_global_settings"
>title="Impostazioni globali"
>abstract="Seleziona lo spazio dei nomi dell’identità Adobe Experience Platform per il programma fedeltà e copia l’ID configurazione. Queste impostazioni a livello di organizzazione sono necessarie prima che i fornitori di premi possano soddisfare correttamente i premi."

Utilizza **[!UICONTROL Impostazioni globali]** per configurare le opzioni a livello di organizzazione per le sfide di fedeltà.

1. Apri la scheda **[!UICONTROL Impostazioni globali]**.

1. Nell&#39;elenco a discesa **[!UICONTROL Spazio dei nomi]**, seleziona lo spazio dei nomi [identità](https://experienceleague.adobe.com/it/docs/experience-platform/identity/features/namespaces) utilizzato dal programma fedeltà.

1. Seleziona **[!UICONTROL Salva]** per applicare lo spazio dei nomi alla configurazione delle sfide fedeltà.

1. Copia l&#39;**[!UICONTROL ID configurazione]** quando devi condividerlo con il team di implementazione o con sistemi esterni, ad esempio durante la configurazione della consegna di eventi in entrata.

<!-- SCREENSHOT: Global settings tab showing namespace drop-down, Save, and Configuration ID -->

## Provider di premi {#reward-providers}

Un **provider di premi** indica a Journey Optimizer dove inviare chiamate di evasione quando viene registrato l&#39;avanzamento della sfida o quando viene completata una sfida, ad esempio un&#39;API che attribuisce punti fedeltà o stelle a un account membro.

La configurazione di un fornitore di premi include:

* Dettagli della connessione di base (nome, descrizione, URL API, intestazioni)
* **[!UICONTROL Definizioni premio]**: i tipi di premio che questo provider può assegnare (ad esempio, stelle o miglia)
* **[!UICONTROL Ricompensa i proxy]** (facoltativo): un proxy intermedio attraverso il quale vengono instradate le chiamate invece che direttamente l&#39;endpoint
* **[!UICONTROL Generatori di token di autenticazione]**: il meccanismo utilizzato da Journey Optimizer per ottenere i token di accesso prima di richiamare l&#39;API

### Creare un provider di premi {#create-reward-provider}

1. Apri la scheda **[!UICONTROL Provider di premi]** e seleziona **[!UICONTROL Crea provider di premi]**.

1. Immetti un **[!UICONTROL Nome]**, **[!UICONTROL Descrizione]** e l&#39;URL **[!UICONTROL API]** che riceve le richieste di evasione.

1. Aggiungi **[!UICONTROL Intestazioni]** in base alle esigenze della tua API (ad esempio, chiavi API o tipi di contenuto).

1. Configura **[!UICONTROL Definizioni premi]**: una voce per tipo di premio supportato dal provider, ad esempio punti programma o stelle. Per ogni definizione:

   * Specifica il **payload** inviato con le chiamate di evasione.
   * È possibile contrassegnare una definizione come **predefinita** per questo provider.

1. Facoltativamente, configura un **[!UICONTROL Proxy premio]** per instradare le chiamate di evasione tramite un server intermedio:

   * **[!UICONTROL Nome]**, **[!UICONTROL Descrizione]** e se il proxy è **abilitato**
   * **[!UICONTROL Host]**, **[!UICONTROL Porta]** e credenziali

1. Configura un **[!UICONTROL generatore di token di autenticazione]** se l&#39;API richiede un token Bearer per l&#39;autenticazione:

   * URL endpoint token e metodo HTTP (ad esempio, **POST** per flussi in stile OAuth)
   * **[!UICONTROL Chiave token]** nella risposta (ad esempio, `access_token`)
   * Intestazioni richieste dall’endpoint token

   Journey Optimizer utilizza questa configurazione per ottenere un nuovo token prima di richiamare l’API di ricompensa.

1. Selezionare **[!UICONTROL Crea provider di premi]**. Il provider e tutte le risorse figlio configurate vengono salvati insieme.

<!-- SCREENSHOT: Reward provider creation form with definitions, proxy, and auth token sections -->

Dopo il salvataggio, il provider viene visualizzato nell&#39;elenco dei provider di premi. Gli addetti al marketing selezionano questo provider durante [la configurazione dei premi per la sfida](create-challenges.md#rewards).

Per modificare un provider di premi esistente, aprire la scheda **[!UICONTROL Provider di premi]**, selezionare il provider e aggiornare i campi in uso. Le modifiche alle risorse secondarie (definizioni di premi, proxy, generatori di token di autenticazione) vengono salvate quando vengono aggiornate.

<!-- SCREENSHOT: Reward provider detail view with child resource sections -->

>[!NOTE]
>
>**[!UICONTROL Acquisisci i tuoi dati]**: le sfide ti consentono di ottenere premi grazie alla tua integrazione dei dati. I fornitori di premi configurati in questo punto non si applicano a tali sfide. [Ulteriori informazioni sulle sfide relative ai dati](create-challenges.md#create-the-challenge).

## Definizioni degli eventi (facoltativo) {#event-definitions}

**[!UICONTROL Definizioni di eventi]** mappa gli eventi esperienza dei sistemi, in qualsiasi formato JSON o XDM utilizzato dal tuo marchio, sulle attività su cui le sfide di fidelizzazione possono agire, in particolare **[!UICONTROL Attività evento personalizzato]**. Quando arrivano gli eventi, Journey Optimizer utilizza queste definizioni per decidere se elaborarli. Gli eventi che non corrispondono ad alcuna definizione vengono ignorati.

### Creare una definizione di evento {#create-event-definition}

1. Apri la scheda **[!UICONTROL Definizioni evento]** e crea una nuova definizione.

1. Immetti un **[!UICONTROL Nome]** per l&#39;evento (ad esempio, `Coffee purchase`). Questo è il nome visualizzato dagli addetti al marketing durante la configurazione di un&#39;attività **[!UICONTROL Evento personalizzato]**.

1. Specificare come identificare l&#39;evento nei payload in ingresso:

   * **[!UICONTROL Percorso identificatore]** — Percorso JSON del campo che identifica l&#39;evento o il membro (ad esempio, `data.memberId`)
   * **[!UICONTROL Valori identificatore]** — valori che devono essere presenti affinché la definizione corrisponda

1. Facoltativamente, specifica un **[!UICONTROL ID schema XDM]** se i payload dell&#39;evento sono conformi a uno schema Experience Platform.

1. Facoltativamente, utilizza i campi **[!UICONTROL Schema]** e **[!UICONTROL Trasformatore]** per fornire schemi personalizzati e stringhe di trasformazione per l&#39;analisi e la convalida del JSON in ingresso.

   Puoi fornire un ID schema XDM, un percorso di identificazione o entrambi, a seconda di come sono strutturati i tuoi eventi.

1. Salva la definizione dell’evento.

<!-- SCREENSHOT: Event definition form with identifier path, values, and schema fields -->

La maggior parte delle organizzazioni crea più definizioni di evento, una per attività di cui desidera tenere traccia (ad esempio, acquisto, check-in o visita del sito). [Scopri come utilizzare le attività evento personalizzate nelle sfide](create-tasks.md#choose-activity).

## Inventario dei prodotti (facoltativo) {#product-inventory}

Utilizza la scheda **[!UICONTROL Inventario prodotti]** per caricare un file CSV che mappa gli identificatori di prodotti o elementi (ad esempio, ID MPG) ai gruppi di prodotti. Gli addetti al marketing possono quindi fare riferimento a questi gruppi nelle regole di idoneità delle attività anziché digitare singoli SKU.

1. Apri la scheda **[!UICONTROL Inventario prodotti]**.

1. Carica il file di mappatura.

1. Esaminare le mappature importate nell&#39;elenco di inventario. Seleziona un gruppo di prodotti per visualizzare tutti gli elementi del gruppo oppure utilizza la ricerca per trovare gli elementi per nome o ID.

1. Utilizza **[!UICONTROL Cronologia caricamento]** per visualizzare i caricamenti precedenti.

<!-- SCREENSHOT: Product inventory list after CSV upload -->

>[!NOTE]
>
>**[!UICONTROL Le esclusioni globali]** per l&#39;inventario dei prodotti sono pianificate per una versione futura e non sono documentate qui.
