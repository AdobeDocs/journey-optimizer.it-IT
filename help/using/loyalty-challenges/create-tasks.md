---
solution: Journey Optimizer
product: journey optimizer
title: Creare attività per le sfide di fidelizzazione
description: Scopri come creare e configurare attività per le sfide di fidelizzazione in Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta privata" type="Informative"
source-git-commit: dbed4ffeb63ec3c58ff61845bbdb91fd2d51e69b
workflow-type: tm+mt
source-wordcount: '844'
ht-degree: 0%

---


# Creare le attività {#create-tasks}

>[!BEGINSHADEBOX]

**Documentazione sulle sfide di fedeltà:**

* [Introduzione alle sfide di fidelizzazione](get-started.md) - Panoramica, flusso di lavoro, prerequisiti
* [Accedere alle sfide di fidelizzazione](access-loyalty-challenges.md) - Inventario e filtro
* [Crea problemi](create-challenges.md) - Genera e configura problemi
* **Crea attività** ◀︎ **Sei qui** - Definisci le attività di verifica
* [Gestire le sfide](manage-challenges.md) - Modificare, monitorare, ottimizzare

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Questa funzionalità è attualmente in **versione beta privata** e potrebbe non essere disponibile nel tuo ambiente. Per richiedere l’accesso, contatta il rappresentante Adobe. Ulteriori informazioni sulle [etichette di disponibilità](../rn/releases.md#availability-labels).

## Panoramica {#overview}

Le attività definiscono le azioni o i milestone specifici che i clienti devono completare per ottenere premi in una sfida di fedeltà. Puoi configurare tipi di task, quantità, requisiti di prodotto e valori di ricompensa per creare esperienze di fidelizzazione coinvolgenti e personalizzate.

Ogni attività rappresenta un’azione misurabile che contribuisce al completamento della sfida. Le attività sono componenti riutilizzabili che possono essere creati in modo indipendente e quindi aggiunti a una o più sfide, oppure creati direttamente all’interno di una sfida.

### Funzionamento delle attività in diversi tipi di sfide {#task-overview}

<!-- VISUAL: Diagram showing how task completion works differently for Standard, Streak, and Sequential challenges with examples -->

A seconda del tipo di sfida (Standard, Streak o Sequenziale), i clienti completano le attività in modo diverso:

* **Sfide standard**: i clienti completano un numero specificato di attività in qualsiasi ordine
* **Sfide**: i clienti completano la stessa attività più volte di seguito
* **Sfide sequenziali**: i clienti completano le attività in un ordine definito

## Creare un’attività {#create-task}

<!-- SCREENSHOT: Two screenshots side by side showing the two entry points: Tasks tab with "Create task" button, and challenge editor with "Add task" button -->

È possibile creare attività da due punti di ingresso. Il processo di configurazione è lo stesso indipendentemente da dove si inizia.

+++Dall&#39;inventario Attività

1. Passa a **[!UICONTROL Sfide fedeltà]** in Journey Optimizer.

1. Selezionare la scheda **[!UICONTROL Attività]**.

1. Seleziona **[!UICONTROL Crea attività]**.

Le attività create dall’inventario vengono salvate e sono disponibili per il riutilizzo in più sfide.

+++

+++Dall’interno di una sfida

1. Apri una sfida esistente o creane una nuova.

1. Passa alla sezione **[!UICONTROL Attività]**.

1. Seleziona **[!UICONTROL Aggiungi attività]**, quindi scegli **[!UICONTROL Crea nuova attività]**.

Le attività create in questo modo vengono automaticamente aggiunte alla sfida e salvate nell’inventario Attività per essere riutilizzate in altre sfide.

+++

### Definire le proprietà dell’attività {#define-task-properties}

<!-- SCREENSHOT: Task properties form showing Task name and Task description fields -->

Configurare le informazioni sulle attività di base:

* **Nome attività**: immettere un nome descrittivo per l&#39;attività. Questo nome è visibile a te e al tuo team, ma potrebbe non essere mostrato ai clienti a seconda della progettazione della scheda di contenuto.
* **Descrizione attività**: (facoltativo) aggiungi dettagli sullo scopo o sui requisiti dell&#39;attività.

### Scegli l’attività del cliente {#choose-activity}

<!-- SCREENSHOT: Activity type selection showing Purchase and Spend options with radio buttons -->

Selezionare il tipo di attività cliente che i clienti devono eseguire per completare l&#39;attività:

* **[!UICONTROL Acquisto]**: i clienti devono acquistare uno o più elementi per completare questa attività
* **[!UICONTROL Spesa]**: i clienti devono spendere una somma specificata per completare l&#39;attività

Seleziona l’attività del cliente che si allinea al meglio agli obiettivi dei risultati. Ogni tipo di attività dispone di attributi configurabili specifici per definire e modellare ulteriormente i requisiti delle attività.

### Definire gli attributi {#define-attributes}

<!-- SCREENSHOT: Attributes form for Purchase activity showing Quantity field, Eligible items & exclusions field, and parameters icon for optional attributes -->

Configura gli attributi del task in base al tipo di attività selezionato:

+++Per l’attività di acquisto

Configura i seguenti attributi:

* **Quantità**: immettere il numero di articoli da acquistare per completare l&#39;attività
* **Elementi ed esclusioni idonei**: definisci gli elementi o i gruppi di elementi che contano per il completamento dell&#39;attività e quelli che non lo fanno. Ulteriori informazioni su [definizione di elementi ed esclusioni idonei](#eligible-items-exclusions)

**Attributi opzionali** (da configurare tramite l&#39;icona dei parametri):

* **Importo valore di spesa minimo**: imposta un requisito importo di acquisto minimo
* **Numero massimo di transazioni**: limita il numero di transazioni utilizzabili per completare l&#39;attività

+++

+++Per l’attività Spesa

Configura i seguenti attributi:

* **Importo**: immettere l&#39;importo totale di spesa necessario per completare l&#39;attività
* **Numero massimo di transazioni**: specificare il numero di transazioni consentite per soddisfare il requisito di spesa. È possibile disattivare questo attributo dall&#39;icona dei parametri se non si desidera limitare il numero di transazioni
* **Elementi ed esclusioni idonei**: (facoltativo) definisci gli elementi o i gruppi di elementi che contano per il completamento dell&#39;attività e quelli che non lo fanno. Ulteriori informazioni su [definizione di elementi ed esclusioni idonei](#eligible-items-exclusions)

+++

Dopo aver configurato tutti gli attributi, seleziona **[!UICONTROL Crea]** per salvare l&#39;attività. L’attività viene salvata nell’inventario Attività e, se creata dall’interno di una sfida, viene aggiunta automaticamente a tale sfida.

## Definire gli articoli e le esclusioni idonei {#eligible-items-exclusions}

<!-- SCREENSHOT: Eligible items & exclusions popup showing the two sections: "Eligible task purchases are limited to the following" and "The following are excluded from this task" with text input fields -->

Sia per le attività Acquisto che per quelle Spesa è possibile definire gruppi e articoli idonei ed escludere articoli e gruppi. Questo consente di eseguire il targeting di prodotti, categorie o posizioni specifici per allinearli agli obiettivi della sfida.

**Casi d&#39;uso:**

* Crea un&#39;attività che premia i clienti per l&#39;acquisto di articoli da caffè ma esclude i prodotti di sdoganamento
* Limitare un&#39;attività di spesa a categorie di prodotti specifiche
* Escludi le gift card o gli articoli promozionali dal conteggio per il completamento dell&#39;attività

### Configurare gli elementi idonei {#configure-eligible-items}

Per definire gli elementi idonei, utilizzare **[!UICONTROL Gli acquisti di attività idonee sono limitati alla seguente]** sezione:

* Immetti ID articolo, categorie o ID destinazione specifici, separati da virgole
* Esempio: `SKU001, SKU002, CategoryA, StoreLocation123`
* **Suggerimento**: immetti `*` per rendere idonei tutti gli acquisti (comportamento predefinito se lasciato vuoto)

### Configurare le esclusioni {#configure-exclusions}

Per escludere elementi dall&#39;attività, utilizzare **[!UICONTROL I seguenti elementi sono esclusi da questa sezione dell&#39;attività]**:

* Immetti ID articolo, categorie o ID destinazione specifici che non devono essere conteggiati per il completamento dell&#39;attività
* Esempio: `CLEARANCE01, GIFTCARD, SALE_CATEGORY`
* Esclusioni comuni: articoli di vendita o sdoganamento, carte regalo, articoli promozionali

>[!NOTE]
>
>Le esclusioni hanno la precedenza sugli elementi idonei. Se un elemento corrisponde sia a un elemento idoneo che a un’esclusione, verrà escluso dall’attività.

## Passaggi successivi {#next-steps}

Ora che sai come creare e configurare le attività:

* [Sfide create](create-challenges.md) - Scopri come creare sfide complete e configurare premi
* [Gestire le sfide](manage-challenges.md) - Scopri come modificare, monitorare e ottimizzare le sfide
