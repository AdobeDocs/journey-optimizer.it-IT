---
solution: Journey Optimizer
product: journey optimizer
title: Configurare il programma fedeltà
description: Scopri come configurare provider di premi, definizioni di eventi, inventario dei prodotti, esclusioni e impostazioni a livello di organizzazione per il tuo programma fedeltà in Adobe [!DNL Journey Optimizer].
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="Beta privata" type="Informative"
mini-toc-levels: 1
exl-id: f8a3b2c1-4d5e-6f7a-8b9c-0d1e2f3a4b5c
source-git-commit: 3ed592e5a9a0671ddd09d648f7407a391cc9684f
workflow-type: tm+mt
source-wordcount: '1312'
ht-degree: 1%

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
>Questa funzionalità è attualmente in **versione beta privata**. Per informazioni dettagliate sul ciclo di rilascio e sulle fasi di disponibilità in [!DNL Journey Optimizer], vedere [ciclo di rilascio](../rn/releases.md).

## Panoramica {#access-loyalty-admin}

La configurazione del programma fedeltà connette [!DNL Journey Optimizer] ai sistemi fedeltà esterni impostando il rispetto dei premi, la mappatura degli eventi, l&#39;inventario dei prodotti e le esclusioni prima che gli addetti al marketing creino le sfide.

>[!NOTE]
>
>La configurazione del programma fedeltà richiede l&#39;accesso dell&#39;amministratore all&#39;istanza [!DNL Journey Optimizer], oltre alle autorizzazioni necessarie per le sfide di fedeltà. Per ottenere l’accesso, contatta il tuo amministratore Adobe.

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
>abstract="Seleziona lo spazio dei nomi dell’identità Adobe Experience Platform per il programma fedeltà."

Apri la scheda **[!UICONTROL Impostazioni globali]** e seleziona lo spazio dei nomi [Identity](https://experienceleague.adobe.com/it/docs/experience-platform/identity/features/namespaces) di Adobe Experience Platform per il programma fedeltà nel menu a discesa **[!UICONTROL Spazio dei nomi]**. Questo spazio dei nomi deve corrispondere al modo in cui i profili dei membri vengono identificati nei dati.

![](assets/admin-global-settings.png)

➡️ [Scopri come utilizzare gli spazi dei nomi delle identità](https://experienceleague.adobe.com/it/docs/experience-platform/identity/features/namespaces){target="_blank"}

## Provider di premi {#reward-providers}

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

   Indirizza le chiamate di evasione tramite un server intermedio invece di inviarle direttamente all’endpoint.

   * Immetti un **[!UICONTROL Nome]** e una **[!UICONTROL Descrizione]**.
   * Immettere **[!UICONTROL Host]** e **[!UICONTROL Porta]**.
   * Specificare se il proxy è **[!UICONTROL abilitato]**.
   * Aggiungi il proxy **[!UICONTROL Credenziali]**.

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

**[!UICONTROL Le definizioni degli eventi]** indicano a [!DNL Journey Optimizer] quali eventi di esperienza in ingresso elaborare. Ad esempio, un acquisto o il check-in in un hotel. Gli addetti al marketing fanno riferimento a queste definizioni in **[!UICONTROL attività evento personalizzato]**. Gli eventi che non corrispondono ad alcuna definizione vengono ignorati.

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

1. Salva la definizione dell’evento. Viene visualizzato nell&#39;elenco **[!UICONTROL Definizioni evento]** ed è disponibile quando gli addetti al marketing creano problemi. [Scopri come creare le sfide](create-challenges.md)

## Inventario prodotti {#product-inventory}

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
