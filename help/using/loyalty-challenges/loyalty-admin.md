---
solution: Journey Optimizer
product: journey optimizer
title: Configurare il programma fedeltà
description: Scopri come configurare provider di premi, definizioni di eventi e impostazioni a livello di organizzazione per il tuo programma fedeltà in Adobe [!DNL Journey Optimizer].
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="Beta privata" type="Informative"
mini-toc-levels: 1
exl-id: f8a3b2c1-4d5e-6f7a-8b9c-0d1e2f3a4b5c
source-git-commit: 3d894653dd2ac1ddd10a8772da8d5cee21af9bca
workflow-type: tm+mt
source-wordcount: '1459'
ht-degree: 0%

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

Utilizza la configurazione del programma fedeltà in [!DNL Journey Optimizer] per connetterti ai sistemi fedeltà esterni. Gli addetti al marketing utilizzano **[!UICONTROL Sfide di fedeltà (Beta)]** per progettare sfide, attività, contenuti e messaggi. La configurazione del programma fedeltà è un&#39;area separata e riservata all&#39;amministratore per l&#39;adempimento dei premi, la mappatura degli eventi, l&#39;inventario dei prodotti e le esclusioni.

>[!NOTE]
>
>La configurazione del programma fedeltà è destinata agli amministratori. Oltre alle autorizzazioni necessarie per le sfide di fidelizzazione, è necessario disporre dell&#39;accesso a livello di amministratore all&#39;istanza [!DNL Journey Optimizer]. Contatta il tuo amministratore Adobe per richiedere l’accesso.

Per aprire l&#39;interfaccia di configurazione, passa a **[!UICONTROL Fedeltà]** e seleziona **[!UICONTROL Amministratore fedele]**. L’interfaccia è organizzata in schede:

* **Impostazioni globali** — Imposta lo spazio dei nomi dell&#39;identità di Experience Platform. [Scopri come configurare le impostazioni globali](#global-settings)
* **Provider di premi**: connetti le API esterne che soddisfano i premi, inclusi i tipi di premio, i proxy e l&#39;autenticazione. [Scopri come configurare i provider di premi](#reward-providers)
* **Definizioni evento** — Mappa gli eventi esperienza in arrivo alle attività utilizzabili nelle **[!UICONTROL attività evento personalizzato]**. [Scopri come configurare le definizioni degli eventi](#event-definitions)
* **Inventario prodotti**: carica i mapping da articolo a gruppo in modo da poter utilizzare i gruppi di prodotti nelle regole di idoneità dell&#39;attività. [Scopri come configurare l&#39;inventario dei prodotti](#product-inventory)
* **Esclusioni**: consente di caricare esclusioni di gruppi e elementi a livello di organizzazione applicabili quando gli addetti al marketing configurano attività. [Scopri come configurare le esclusioni](#exclusions)

## Impostazioni globali {#global-settings}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_global_settings"
>title="Impostazioni globali"
>abstract="Seleziona lo spazio dei nomi dell’identità Adobe Experience Platform per il programma fedeltà."

Apri la scheda **[!UICONTROL Impostazioni globali]**. Per il momento, la configurazione principale disponibile in questa scheda è la selezione dello spazio dei nomi dell&#39;identità di Adobe Experience Platform utilizzato dal programma fedeltà nel menu a discesa **[!UICONTROL Spazio dei nomi]**.

![](assets/admin-global-settings.png)

➡️ [Scopri come utilizzare gli spazi dei nomi delle identità](https://experienceleague.adobe.com/it/docs/experience-platform/identity/features/namespaces){target="_blank"}

## Provider di premi {#reward-providers}

Un **provider di premi** indica a [!DNL Journey Optimizer] dove inviare chiamate di evasione quando viene registrato l&#39;avanzamento della sfida o viene completata una sfida, ad esempio un&#39;API che attribuisce punti fedeltà o stelle a un account membro.
* **[!UICONTROL Definizioni premi]**: i tipi di premio che questo provider può assegnare (ad esempio, stelle o miglia).
* **[!UICONTROL Ricompensa i proxy]**: un proxy intermedio attraverso il quale vengono instradate le chiamate invece che direttamente l&#39;endpoint.
* **[!UICONTROL Generatori di token di autenticazione]**: il meccanismo utilizzato da [!DNL Journey Optimizer] per ottenere i token di accesso prima di richiamare l&#39;API.

Per creare un provider di premi, eseguire la procedura seguente:

1. Apri la scheda **[!UICONTROL Provider di premi]** e seleziona **[!UICONTROL Crea provider di premi]**.

   ![](assets/admin-reward.png)

1. Immetti un **[!UICONTROL Nome]** e una **[!UICONTROL Descrizione]**.

1. Nel campo **[!UICONTROL URL]**, immetti l&#39;URL API che riceve le richieste di evasione.

1. Aggiungi **[!UICONTROL Intestazioni]** in base alle esigenze della tua API (ad esempio, chiavi API o tipi di contenuto).

1. Configura le risorse seguenti associate al tuo provider di premi. Espandi ogni sezione per ulteriori informazioni:

   +++Definizioni dei premi

   Una voce per ogni premio supportato dal provider (ad esempio, punti programma o stelle, credito monetario). Per ogni definizione:

   * Immetti un nome e una descrizione.
   * Specificare se la definizione è **[!UICONTROL Abilitata]**.
   * Attiva l&#39;opzione **![!UICONTROL Default]** per contrassegnare una definizione come predefinita per questo provider.
   * Specifica il **payload** inviato con le chiamate di evasione.

   ![](assets/admin-reward-definition.png)

   +++

   +++Proxy premio

   Indirizza le chiamate di esecuzione tramite un server intermedio anziché direttamente all&#39;endpoint.

   * Immetti un nome e una descrizione.
   * Immettere le informazioni relative a **[!UICONTROL Host]**, **[!UICONTROL Porta]**.
   * Specificare se il proxy è **[!UICONTROL abilitato]**.
   * Aggiungi il proxy **[!UICONTROL Credenziali]**.

   ![](assets/admin-reward-proxies.png)

   +++

   +++Generatore di token di autenticazione

   Se l’API richiede un token Bearer per l’autenticazione.

   * Immettere un nome e una descrizione.
   * Nel campo Tipo di autenticazione immettere il tipo di autenticazione, ad esempio Bearer.
   * Seleziona il metodo HTTP da utilizzare (ad esempio, POST).
   * Immetti l’URL dell’endpoint del token. e aggiungi la **[!UICONTROL Chiave token]** nella risposta (ad esempio, `access_token`).
   * Specificare se il generatore di token di autenticazione è **[!UICONTROL Abilitato]**.
   * Se necessario, aggiungi le intestazioni richieste dall’endpoint token.

   [!DNL Journey Optimizer] utilizza questa configurazione per ottenere un nuovo token prima di chiamare la tua API di ricompensa.

   ![](assets/admin-reward-auth.png)

   +++

1. Selezionare **[!UICONTROL Crea provider di premi]**. Il provider e tutte le risorse configurate vengono salvati insieme.

Dopo il salvataggio, il provider viene visualizzato nell&#39;elenco dei provider di premi. Gli addetti al marketing possono selezionare questo provider durante la configurazione dei premi per la sfida. [Scopri come configurare i premi per le sfide](create-challenges.md#rewards)

Per modificare un provider di premi esistente, aprire la scheda **[!UICONTROL Provider di premi]**, selezionare il provider e aggiornare i campi in uso. Le modifiche alle risorse secondarie (definizioni di premi, proxy, generatori di token di autenticazione) vengono salvate quando vengono aggiornate.

>[!NOTE]
>
>**[!UICONTROL Acquisisci i tuoi dati]**: le sfide ti consentono di ottenere premi grazie alla tua integrazione dei dati. I fornitori di premi configurati in questo punto non si applicano a tali sfide. [Scopri come creare le sfide per i tuoi dati](create-challenges.md#create-the-challenge)

## Definizioni degli eventi {#event-definitions}

**[!UICONTROL Definizioni di eventi]** mappa gli eventi di esperienza dai sistemi (ad esempio, acquisto, check-in in hotel) alle attività su cui le sfide di fidelizzazione possono agire, in particolare **[!UICONTROL Attività evento personalizzato]**. Quando arrivano gli eventi, [!DNL Journey Optimizer] utilizza queste definizioni per decidere se elaborarle. Gli eventi che non corrispondono ad alcuna definizione vengono ignorati.

Per creare una definizione di evento, effettua le seguenti operazioni:

1. Apri la scheda **[!UICONTROL Definizioni evento]** e crea una nuova definizione.

   ![](assets/admin-event-definition.png)

1. Immetti un **[!UICONTROL Nome]** per l&#39;evento (ad esempio, `Coffee purchase`). Questo è il nome visualizzato dagli addetti al marketing durante la configurazione di un&#39;attività **[!UICONTROL Evento personalizzato]**.

1. Specificare il modo in cui [!DNL Journey Optimizer] riconosce l&#39;evento nei payload in ingresso. Fornisci un **[!UICONTROL percorso identificatore]**, un **[!UICONTROL ID schema XDM]** o entrambi:

   * **[!UICONTROL Percorso identificatore]**: percorso del campo che identifica l&#39;evento o il membro (ad esempio, `data.memberId`). Utilizzalo quando abbini gli eventi in base ai valori nel payload.
   * **[!UICONTROL Valori identificatore]** — Valori nel percorso dell&#39;identificatore che devono essere presenti affinché la definizione corrisponda.
   * **[!UICONTROL ID schema XDM]** — ID dello schema XDM di Experience Platform per questo tipo di evento. Da utilizzare quando gli eventi vengono acquisiti in base a uno schema noto.

1. Quando i brand inviano eventi nel proprio formato JSON, incolla le stringhe in **[!UICONTROL Schema]** e **[!UICONTROL Trasformatore]** in modo che [!DNL Journey Optimizer] possa identificare i dati, analizzarli e decidere se tenerne traccia.

   * **[!UICONTROL Schema]** — Stringa di convalida per il payload in ingresso.
   * **[!UICONTROL Trasformatore]**: espressione di trasformazione (ad esempio, JSONata) che mappa il payload nel formato previsto da Sfide di fedeltà.

1. Salva la definizione dell’evento. Viene visualizzato nell&#39;elenco **[!UICONTROL Definizioni evento]**. Ora è possibile utilizzarlo nelle sfide. [Scopri come creare le sfide](create-challenges.md)

## Inventario prodotti {#product-inventory}

La scheda **[!UICONTROL Inventario prodotti]** ti consente di raggruppare gli elementi del catalogo in modo da poterli indirizzare alle attività senza elencare ogni ID elemento. Carichi un **file CSV** che associa ogni identificatore di elemento a uno o più **gruppi di prodotti** (lo stesso elemento può essere visualizzato in più gruppi). Dopo l’importazione, tali gruppi sono disponibili quando si configura l’idoneità delle attività. [Scopri come creare le attività](create-tasks.md)

Per caricare un file di inventario dei prodotti, effettua le seguenti operazioni:

1. Prepara un file CSV che associa ogni identificatore di elemento a uno o più gruppi di prodotti. Espandi la sezione seguente per visualizzare un esempio.

   +++Esempio di CSV dell’inventario dei prodotti

   ![](assets/admin-inventory-csv.png)

   +++

1. Apri la scheda **[!UICONTROL Inventario prodotti]**.

1. Fai clic sul pulsante **[!UICONTROL Carica]** e seleziona il file CSV.

   ![](assets/admin-inventory-upload.png)

1. Esaminare il file importato nell&#39;elenco di inventario. L’elenco mostra una riga per elemento. Nella colonna **[!UICONTROL Gruppi inclusi in]** vengono visualizzati tutti i gruppi di prodotti a cui appartiene l&#39;elemento. Ogni gruppo appare come una pillola (diverse pillole se l&#39;articolo è in diversi gruppi).

   ![](assets/admin-inventory-imported.png)

1. Per visualizzare ogni elemento in un gruppo di prodotti, seleziona la pillola del gruppo nella colonna **[!UICONTROL Gruppi inclusi in]** su qualsiasi riga. Nella visualizzazione Dettagli gruppo sono elencati tutti gli elementi del gruppo, non solo l&#39;elemento nella riga selezionata.

   ![](assets/admin-inventory-group.png)

1. Utilizza **[!UICONTROL Cronologia caricamento]** per visualizzare i caricamenti precedenti di file CSV.

## Esclusioni {#exclusions}

La scheda **[!UICONTROL Esclusioni]** ti consente di definire gli elementi e i gruppi di catalogo esclusi nel programma fedeltà senza elencare tutti gli ID di elemento in ogni attività. Carica un **file CSV** che associa ogni identificatore di elemento a uno o più **gruppi di esclusione** (lo stesso elemento può essere visualizzato in più gruppi). Dopo l’importazione, tali elementi e gruppi sono disponibili nel generatore di attività: gli elementi esclusi vengono contrassegnati automaticamente e non possono essere inclusi in un’attività; i gruppi di esclusione possono essere aggiunti solo all’elenco di esclusione dell’attività, non a quello di inclusione. [Scopri come definire elementi ed esclusioni idonei per le attività](create-tasks.md#eligible-items-exclusions)

Per caricare un file di esclusioni di prodotto, effettua le seguenti operazioni:

1. Prepara un file CSV che associa ogni identificatore di elemento a uno o più gruppi di esclusione. Espandi la sezione seguente per visualizzare un esempio.

   +++Esempio di CSV delle esclusioni

   ![](assets/admin-exclusions-csv.png)

   +++

1. Apri la scheda **[!UICONTROL Esclusioni]**.

1. Fai clic sul pulsante **[!UICONTROL Carica]** e seleziona il file CSV.

   ![](assets/admin-exclusions-upload.png)

1. Esamina il file importato nell’elenco delle esclusioni. L’elenco mostra una riga per elemento. Nella colonna **[!UICONTROL Gruppi inclusi in]** vengono visualizzati tutti i gruppi di esclusione a cui appartiene l&#39;elemento. Ogni gruppo appare come una pillola (diverse pillole se l&#39;articolo è in diversi gruppi).

1. Per visualizzare ogni elemento in un gruppo di esclusione, seleziona la pillola del gruppo nella colonna **[!UICONTROL Gruppi inclusi in]** su qualsiasi riga. Nella visualizzazione Dettagli gruppo sono elencati tutti gli elementi del gruppo, non solo l&#39;elemento nella riga selezionata.

1. Utilizza **[!UICONTROL Cronologia caricamento]** per visualizzare i caricamenti precedenti di file CSV.
