---
solution: Journey Optimizer
product: journey optimizer
title: Configurare le sfide relative alla fedeltà
description: Scopri come configurare i provider di premi, le definizioni di eventi, l'inventario dei prodotti, le esclusioni e le impostazioni a livello di organizzazione per le sfide di fidelizzazione in Adobe [!DNL Journey Optimizer].
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="Beta privata" type="Informative"
mini-toc-levels: 1
exl-id: f8a3b2c1-4d5e-6f7a-8b9c-0d1e2f3a4b5c
source-git-commit: 0104f7b79145d7defee673fc6c9cd7d86fef3201
workflow-type: tm+mt
source-wordcount: '1636'
ht-degree: 1%

---

# Configurare le sfide relative alla fedeltà {#loyalty-admin}

<!-- Unpublished draft: Loyalty Admin UI documentation is not validated for Experience League. This page uses hide: true until review. -->

>[!BEGINSHADEBOX]

**Sommario**

[Introduzione alle sfide di fedeltà](get-started.md)

+++Creare e gestire le sfide

* [Accesso e gestione di sfide e attività](access-loyalty-challenges.md)
* [Creare le sfide](create-challenges.md)
* [Creare le attività](create-tasks.md)
* [Monitorare le prestazioni della sfida fedeltà](loyalty-reporting.md)

+++

**Configura e integra**

* **Configura le sfide fedeltà** ◀︎ **Sei qui**
* [Dati e set di dati sulla fedeltà](loyalty-data-and-datasets.md)
* [Riferimento API per le sfide di fedeltà](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Questa funzionalità è attualmente in **versione beta privata**. Per informazioni dettagliate sul ciclo di rilascio e sulle fasi di disponibilità in [!DNL Journey Optimizer], vedere [ciclo di rilascio](../rn/releases.md).

## Panoramica {#access-loyalty-admin}

La configurazione delle sfide di fidelizzazione collega [!DNL Journey Optimizer] ai sistemi di fidelizzazione esterni impostando l&#39;evasione dei premi, la mappatura degli eventi, l&#39;inventario dei prodotti e le esclusioni prima che gli addetti al marketing creino le sfide.

>[!NOTE]
>
>La configurazione delle sfide di fidelizzazione richiede l&#39;accesso dell&#39;amministratore all&#39;istanza [!DNL Journey Optimizer], oltre alle autorizzazioni necessarie per le sfide di fidelizzazione. Per ottenere l’accesso, contatta il tuo amministratore Adobe.

Per aprire l&#39;interfaccia di configurazione, passa a **[!UICONTROL Fedeltà]** e seleziona **[!UICONTROL Amministratore fedele]**. L’interfaccia è organizzata in schede:

* **Impostazioni globali** - Selezionare lo spazio dei nomi dell&#39;identità Experience Platform per il programma. [Scopri come configurare le impostazioni globali](#global-settings)
* **Provider di premi**: collega le API che soddisfano i premi quando i clienti avanzano o completano le sfide. [Scopri come configurare i provider di premi](#reward-providers)
* **Definizioni evento** — Mappa gli eventi esperienza in arrivo alle attività utilizzate nelle **[!UICONTROL attività evento personalizzato]**. [Scopri come configurare le definizioni degli eventi](#event-definitions)
* **Inventario prodotti**: carica i mapping da elemento a gruppo da utilizzare nelle regole di idoneità dell&#39;attività. [Scopri come configurare l&#39;inventario dei prodotti](#product-inventory)
* **Esclusioni**: consente di caricare esclusioni di gruppi e elementi a livello di organizzazione per la configurazione dell&#39;attività. [Scopri come configurare le esclusioni](#exclusions)

## Impostazioni globali {#global-settings}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_global_settings"
>title="Impostazioni globali"
>abstract="Le impostazioni globali definiscono la configurazione a livello di organizzazione per le sfide di fidelizzazione, incluso lo spazio dei nomi delle identità utilizzato per identificare i membri tra eventi e sfide."

Apri la scheda **[!UICONTROL Impostazioni globali]** e seleziona lo spazio dei nomi [Identity](https://experienceleague.adobe.com/it/docs/experience-platform/identity/features/namespaces) di Adobe Experience Platform per le sfide di fidelizzazione nel menu a discesa **[!UICONTROL Spazio dei nomi]**. Questo spazio dei nomi deve corrispondere al modo in cui i profili dei membri vengono identificati nei dati.

![](assets/admin-global-settings.png)

➡️ [Scopri come utilizzare gli spazi dei nomi delle identità](https://experienceleague.adobe.com/it/docs/experience-platform/identity/features/namespaces){target="_blank"}

## Provider di premi {#reward-providers}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_reward_providers"
>title="Provider di premi"
>abstract="Un provider di premi definisce il sistema esterno che [!DNL Journey Optimizer] chiama per soddisfare i premi quando i clienti completano le sfide. Configurare l&#39;endpoint del provider, le definizioni dei premi, le impostazioni proxy e l&#39;autenticazione per ogni integrazione."

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_reward_providers_connection"
>title="Connessione provider di premi"
>abstract="Configurare la modalità di connessione di [!DNL Journey Optimizer] all&#39;API di ricompensa: nome provider, descrizione, URL endpoint e intestazioni HTTP necessari per le chiamate di evasione."

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_reward_providers_details"
>title="Definizioni dei premi"
>abstract="Le definizioni dei premi specificano ogni tipo di premio che questo provider può emettere (ad esempio, punti o stelle) e il payload [!DNL Journey Optimizer] invia quando i premi vengono soddisfatti."

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_reward_providers_proxy"
>title="Proxy premio"
>abstract="Facoltativamente, instradare le chiamate di evasione tramite un server proxy invece di inviarle direttamente all’endpoint API di ricompensa. Configurare host, porta, credenziali e se il proxy è abilitato. Il valore delle credenziali è in genere simile al seguente: `{ "userName": "test", "password": "xxxx" }`"

Un **provider di premi** indica a [!DNL Journey Optimizer] dove inviare le chiamate di evasione quando viene registrato l&#39;avanzamento della richiesta di verifica o viene completata una richiesta di verifica. Ad esempio, un’API che attribuisce punti fedeltà o stelle a un account membro.

Per creare un provider di premi, eseguire la procedura seguente:

1. Apri la scheda **[!UICONTROL Provider di premi]** e seleziona **[!UICONTROL Crea provider di premi]**.

   ![](assets/admin-reward.png)

1. Immetti un **[!UICONTROL Nome]** e una **[!UICONTROL Descrizione]**.

1. Nel campo **[!UICONTROL URL]**, immetti l&#39;endpoint API che riceve le richieste di evasione.

1. Aggiungi **[!UICONTROL Intestazioni]** in base alle esigenze della tua API (ad esempio, chiavi API o tipi di contenuto).

1. Configura le risorse associate al tuo provider di premi. Espandi ciascuna sezione seguente per i dettagli del campo:

   +++Definizioni dei premi

   Aggiungi una voce per tipo di premio supportato dal provider (ad esempio punti programma, stelle o credito monetario). Per ogni definizione:

   * Immetti un **[!UICONTROL Nome]** e una **[!UICONTROL Descrizione]**.
   * Specificare se la definizione è **[!UICONTROL Abilitata]**.
   * Attiva **[!UICONTROL Predefinito]** per contrassegnare una definizione come predefinita per questo provider.
   * Definisci il **payload** inviato con le chiamate di evasione.

   ![](assets/admin-reward-definition.png)

   +++

   +++Proxy premio

   Indirizza le chiamate di evasione tramite un server intermedio invece di inviarle direttamente all’endpoint. Nelle schermate del provider di premi e **[!UICONTROL Crea proxy]**, utilizza il campo **[!UICONTROL Credenziali]** per l&#39;autenticazione proxy.

   * Immetti un **[!UICONTROL Nome]** e una **[!UICONTROL Descrizione]**.
   * Immettere **[!UICONTROL Host]** e **[!UICONTROL Porta]**.
   * Specificare se il proxy è **[!UICONTROL abilitato]**.
   * In **[!UICONTROL Credenziali]**, immettere il nome utente e la password proxy come JSON. Il valore delle credenziali è in genere simile al seguente:

     ```json
     { "userName": "test", "password": "xxxx" }
     ```

   ![](assets/admin-reward-proxies.png)

   +++

   +++Generatore di token di autenticazione

   Da utilizzare quando l’API richiede un token Bearer o un’autenticazione simile.

   * Immetti un **[!UICONTROL Nome]** e una **[!UICONTROL Descrizione]**.
   * In **[!UICONTROL Tipo di autenticazione]** immettere il tipo di autenticazione, ad esempio Bearer.
   * Seleziona il metodo HTTP (ad esempio, POST).
   * Immetti l&#39;URL dell&#39;endpoint del token e la **[!UICONTROL chiave token]** nella risposta (ad esempio, `access_token`).
   * Specificare se il generatore di token di autenticazione è **[!UICONTROL Abilitato]**.
   * Aggiungi le intestazioni richieste dall’endpoint token.

   [!DNL Journey Optimizer] utilizza questa configurazione per ottenere un nuovo token prima di ogni chiamata all&#39;API di ricompensa.

   ![](assets/admin-reward-auth.png)

   +++

1. Selezionare **[!UICONTROL Crea provider di premi]**. Il provider e tutte le risorse configurate vengono salvati insieme.

Dopo il salvataggio, il provider viene visualizzato nell&#39;elenco dei provider di premi. Gli addetti al marketing possono selezionarlo durante la configurazione dei premi per la sfida. [Scopri come configurare i premi per le sfide](create-challenges.md#rewards)

Per modificare un provider di premi, aprire la scheda **[!UICONTROL Provider di premi]**, selezionare il provider e aggiornare i campi in uso. Le modifiche alle definizioni dei premi, ai proxy e ai generatori di token di autenticazione vengono salvate automaticamente quando vengono aggiornate.

>[!NOTE]
>
>**[!UICONTROL Acquisisci i tuoi dati]**: le sfide ti consentono di ottenere premi grazie alla tua integrazione dei dati. I provider di premi configurati in questo punto non sono applicabili a queste sfide. [Scopri come creare le sfide per i tuoi dati](create-challenges.md#create-the-challenge)

## Definizioni degli eventi {#event-definitions}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_event_definitions"
>title="Definizioni degli eventi"
>abstract="Le definizioni degli eventi indicano a [!DNL Journey Optimizer] come identificare e interpretare i dati degli eventi in arrivo dalle origini esterne. Ogni definizione mappa un tipo di evento specifico, ad esempio un acquisto o un check-in, in modo che il sistema possa tenere traccia dell’avanzamento del cliente verso le attività di verifica."

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_event_schema"
>title="Schema evento e trasformatore"
>abstract="Quando l&#39;organizzazione invia eventi in un formato JSON personalizzato, utilizza **[!UICONTROL Schema]** per convalidare il payload e **[!UICONTROL Trasformatore]** (ad esempio, un&#39;espressione JSONata) per mappare i campi nel formato previsto da Sfide di fedeltà."

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_event_identification"
>title="Identificazione evento"
>abstract="Specificare il modo in cui [!DNL Journey Optimizer] riconosce l&#39;evento nei payload in ingresso utilizzando un percorso di identificatore, valori di identificatore, un ID di schema XDM o una combinazione di questi campi."

**[!UICONTROL Le definizioni degli eventi]** indicano a [!DNL Journey Optimizer] quali eventi di esperienza Adobe Experience Platform in ingresso elaborare. Ad esempio, un acquisto o il check-in in un hotel. Gli addetti al marketing fanno riferimento a queste definizioni quando creano **[!UICONTROL attività evento personalizzato]**. Gli eventi che non corrispondono ad alcuna definizione vengono ignorati.

Quando l&#39;organizzazione invia eventi nel proprio formato JSON, **[!UICONTROL Schema]** e **[!UICONTROL Trasformatore]** consentono a [!DNL Journey Optimizer] di convalidare il payload, analizzarlo e decidere se tenere traccia dell&#39;attività.

Per creare una definizione di evento, effettua le seguenti operazioni:

1. Apri la scheda **[!UICONTROL Definizioni evento]** e crea una nuova definizione.

   ![](assets/admin-event-definition.png)

1. Immetti un **[!UICONTROL Nome]** per l&#39;evento (ad esempio, `Coffee purchase`). Gli addetti al marketing visualizzano questo nome durante la configurazione di un&#39;attività **[!UICONTROL Evento personalizzato]**.

1. Specificare il modo in cui [!DNL Journey Optimizer] riconosce l&#39;evento nei payload in ingresso. Fornisci un **[!UICONTROL percorso identificatore]**, un **[!UICONTROL ID schema XDM]** o entrambi:

   * **[!UICONTROL Percorso identificatore]** — Percorso di un campo nel payload (ad esempio, `data.memberId`). Utilizzalo quando abbini gli eventi in base ai valori nel payload.
   * **[!UICONTROL Valori identificatore]** — Valori nel percorso dell&#39;identificatore che devono essere presenti affinché la definizione corrisponda.
   * **[!UICONTROL ID schema XDM]** — ID dello schema XDM di Experience Platform per questo tipo di evento. Da utilizzare quando gli eventi vengono acquisiti in base a uno schema noto.

1. Se necessario, incolla le stringhe in **[!UICONTROL Schema]** e **[!UICONTROL Trasformatore]**:

   * **[!UICONTROL Schema]** — Stringa di convalida per il payload in ingresso.
   * **[!UICONTROL Trasformatore]**: espressione di trasformazione (ad esempio, JSONata) che mappa il payload nel formato previsto da Sfide di fedeltà.

1. Salva la definizione dell’evento. Viene visualizzato nell&#39;elenco **[!UICONTROL Definizioni evento]** ed è disponibile quando gli addetti al marketing creano **[!UICONTROL attività evento personalizzato]**. [Scopri come creare le attività](create-tasks.md#choose-activity)

## Inventario prodotti {#product-inventory}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_product_inventory"
>title="Inventario prodotti"
>abstract="Carica un file CSV che mappa gli identificatori degli elementi ai gruppi di prodotti. Gli addetti al marketing possono fare riferimento a questi gruppi durante la configurazione degli articoli idonei per le attività di acquisto e spesa senza immettere alcun ID articolo."

La scheda **[!UICONTROL Inventario prodotti]** raggruppa gli elementi del catalogo in modo che gli addetti al marketing possano eseguirne il targeting nelle attività senza immettere ogni ID elemento. Carica un **file CSV** che associa ogni identificatore di elemento a uno o più **gruppi di prodotti** (lo stesso elemento può appartenere a più gruppi). I gruppi importati sono disponibili durante la configurazione dell’idoneità delle attività. [Scopri come creare le attività](create-tasks.md)

Per caricare un file di inventario dei prodotti, effettua le seguenti operazioni:

1. Prepara un file CSV che associa ogni identificatore di elemento a uno o più gruppi di prodotti. Espandi la sezione seguente per visualizzare un esempio.

   +++Esempio di CSV dell’inventario dei prodotti

   ![](assets/admin-inventory-csv.png)

   +++

1. Apri la scheda **[!UICONTROL Inventario prodotti]**.

1. Seleziona **[!UICONTROL Carica]** e scegli il tuo file CSV.

   ![](assets/admin-inventory-upload.png)

1. Esaminare i dati importati nell&#39;elenco di inventario. L’elenco mostra una riga per elemento. La colonna **[!UICONTROL Gruppi inclusi in]** mostra ogni gruppo di prodotti per l&#39;elemento come pillola o più pillole quando l&#39;elemento appartiene a più gruppi.

   ![](assets/admin-inventory-imported.png)

1. Per visualizzare tutti gli elementi di un gruppo di prodotti, seleziona la pillola del gruppo nella colonna **[!UICONTROL Gruppi inclusi in]** su qualsiasi riga. Nella vista Dettagli gruppo sono elencati tutti gli elementi del gruppo.

   ![](assets/admin-inventory-group.png)

1. Apri **[!UICONTROL Cronologia caricamento]** per visualizzare i caricamenti CSV precedenti.

## Esclusioni {#exclusions}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_exclusions"
>title="Esclusioni"
>abstract="Carica un file CSV che definisce gli elementi di catalogo e i gruppi esclusi a livello di programma. I gruppi di esclusione importati vengono visualizzati quando gli addetti al marketing configurano elementi ed esclusioni idonei per le attività."

La scheda **[!UICONTROL Esclusioni]** definisce gli elementi e i gruppi di catalogo esclusi a livello di programma, pertanto gli addetti al marketing non devono elencare le stesse esclusioni per ogni attività. Carica un **file CSV** che associa ogni identificatore di elemento a uno o più **gruppi di esclusione** (lo stesso elemento può appartenere a più gruppi).

Dopo l&#39;importazione, gli elementi e i gruppi esclusi vengono visualizzati nel generatore di attività quando gli addetti al marketing configurano **[!UICONTROL Elementi ed esclusioni idonei]**. [Scopri come definire elementi ed esclusioni idonei per le attività](create-tasks.md#eligible-items-exclusions)

Per caricare le esclusioni, effettua le seguenti operazioni:

1. Prepara un file CSV che associa ogni identificatore di elemento a uno o più gruppi di esclusione. Espandi la sezione seguente per visualizzare un esempio.

   +++Esempio di CSV delle esclusioni

   ![](assets/admin-exclusions-csv.png)

   +++

1. Apri la scheda **[!UICONTROL Esclusioni]**.

1. Seleziona **[!UICONTROL Carica]** e scegli il tuo file CSV.

   ![](assets/admin-exclusions-upload.png)

1. Esamina i dati importati nell’elenco delle esclusioni. L’elenco mostra una riga per elemento. La colonna **[!UICONTROL Gruppi inclusi in]** mostra ogni gruppo di esclusione per l&#39;elemento come pillola o più pillole quando l&#39;elemento appartiene a più gruppi.

<!-- SCREENSHOT: Exclusions list after CSV upload -->

1. Per visualizzare tutti gli elementi di un gruppo di esclusione, seleziona la pillola del gruppo nella colonna **[!UICONTROL Gruppi inclusi in]** su qualsiasi riga. Nella vista Dettagli gruppo sono elencati tutti gli elementi del gruppo.

<!-- SCREENSHOT: Exclusion group details -->

1. Apri **[!UICONTROL Cronologia caricamento]** per visualizzare i caricamenti CSV precedenti.
