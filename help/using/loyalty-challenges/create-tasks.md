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
badge: label="Beta privata" type="Informative"
mini-toc-levels: 1
exl-id: c1e49173-69cc-4729-9f9a-afea2ccff3fa
source-git-commit: 384f4e4b4c3acd9f1f1d73d4b140845870b31289
workflow-type: tm+mt
source-wordcount: '993'
ht-degree: 18%

---

# Creare le attività {#create-tasks}

>[!BEGINSHADEBOX]

**Documentazione sulle sfide di fedeltà:**

* [Introduzione alle sfide di fedeltà](get-started.md)
* [Accesso e gestione di sfide e attività](access-loyalty-challenges.md)
* [Creare le sfide](create-challenges.md)
* **Crea attività** ◀︎ **Sei qui**
* [Monitorare le prestazioni della sfida fedeltà](loyalty-reporting.md)
* [Riferimento API per le sfide di fedeltà](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Questa funzionalità è attualmente in **versione beta privata**. Per informazioni dettagliate sul ciclo di rilascio e sulle fasi di disponibilità, consulta [Ciclo di rilascio di Journey Optimizer](../rn/releases.md).

Le attività definiscono le azioni o i milestone specifici che i clienti devono completare per ottenere premi in una sfida di fedeltà. Puoi configurare tipi di attività, quantità e requisiti di prodotto per creare esperienze di fidelizzazione coinvolgenti e personalizzate.

Ogni attività rappresenta un’azione misurabile che contribuisce al completamento della sfida. Le attività sono componenti riutilizzabili che possono essere creati in modo indipendente e quindi aggiunti a una o più sfide, oppure creati direttamente all’interno di una sfida.

## Creare un’attività {#create-task}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_task_create"
>title="Creare un’attività"
>abstract="Seleziona un’attività dei clienti (Acquisto o Spesa), quindi configura gli attributi specifici dell’attività: quantità o importi, articoli idonei ed esclusioni e limiti facoltativi, tra cui la spesa minima o il numero massimo di transazioni. Nel riquadro Proprietà imposta il nome e la descrizione dell’attività."

È possibile creare attività da due punti di ingresso. Il processo di configurazione è lo stesso indipendentemente da dove si inizia.

>[!BEGINTABS]

>[!TAB Dall&#39;inventario delle attività]

Seleziona la scheda **[!UICONTROL Attività]** e seleziona **[!UICONTROL Crea attività]**. Le attività create dall’inventario vengono salvate e sono disponibili per il riutilizzo in più sfide.

![](assets/task-create-inventory.png)

>[!TAB Dall&#39;interno di una sfida]

Apri una sfida esistente o creane una nuova. Seleziona **[!UICONTROL Aggiungi attività]** e fai clic sul pulsante **[!UICONTROL Nuovo]**. Le attività create in questo modo vengono automaticamente aggiunte alla sfida e salvate nell’inventario Attività per essere riutilizzate in altre sfide.

![](assets/task-create-challenge.png)

>[!ENDTABS]

## Scegli l’attività del cliente {#choose-activity}

Selezionare il tipo di attività che i clienti devono eseguire per completare questa attività:

* **[!UICONTROL Acquisto]**: i clienti devono acquistare uno o più elementi per completare questa attività
* **[!UICONTROL Spesa]**: i clienti devono spendere una somma specificata per completare l&#39;attività

Per selezionare un&#39;attività, fare clic sull&#39;icona **+** e selezionare l&#39;attività cliente che meglio si allinea agli obiettivi dei risultati. Ogni tipo di attività dispone di attributi configurabili specifici per definire e modellare ulteriormente i requisiti delle attività.
![](assets/task-create-activity.png)

## Definire gli attributi del task {#define-attributes}

Configura gli attributi del task in base al tipo di attività selezionato. Sfoglia le schede seguenti per visualizzare gli attributi disponibili per ciascun tipo di attività:

>[!BEGINTABS]

>[!TAB Attività di acquisto]

Attributi disponibili per **Attività di acquisto**:

* **[!UICONTROL Quantità]**: immettere il numero di articoli da acquistare per completare l&#39;attività.
* **[!UICONTROL Elementi ed esclusioni idonei]**: definisci gli elementi o i gruppi di elementi che contano per il completamento dell&#39;attività e quelli che non lo fanno, oppure scegli **[!UICONTROL Porta i tuoi dati]** per determinare l&#39;idoneità dai tuoi dati esterni. [Ulteriori informazioni](#eligible-items-exclusions)
* **[!UICONTROL Importo valore spesa minimo]**: impostare un requisito importo acquisto minimo.
* **[!UICONTROL Numero massimo di transazioni]**: limitare il numero di transazioni che è possibile utilizzare per completare l&#39;attività.

![](assets/task-create-purchase.png)

>[!TAB Attività di spesa]

Attributi disponibili per le attività **Spend**:

* **[!UICONTROL Importo]**: immettere l&#39;importo totale di spesa necessario per completare l&#39;attività.
* **[!UICONTROL Elementi ed esclusioni idonei]**: definisci gli elementi o i gruppi di elementi che contano per il completamento dell&#39;attività e quelli che non lo fanno. [Ulteriori informazioni su elementi ed esclusioni idonei](#eligible-items-exclusions)
* **[!UICONTROL Numero massimo di transazioni]**: specificare il numero di transazioni consentite per soddisfare il requisito di spesa. Puoi attivare questo attributo dall’icona dei parametri.

![](assets/task-create-spend.png)

>[!ENDTABS]

## Definire gli articoli idonei e le esclusioni {#eligible-items-exclusions}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_task_eligible_items_exclusion"
>title="Articoli idonei ed esclusioni"
>abstract="Per entrambe le attività **Acquisto** e **Spesa**, puoi utilizzare l’attributo **[!UICONTROL Articoli idonei ed esclusioni]** per definire quali articoli e gruppi sono idonei e quali sono esclusi. Questo consente di eseguire il targeting di prodotti, categorie o punti vendita specifici per allinearli agli obiettivi della sfida. Ad esempio, puoi limitare un’attività di spesa a specifiche categorie di prodotti oppure escludere le carte regalo o gli articoli in promozione dal conteggio per il completamento dell’attività."

<!-- SCREENSHOT: Eligible items & exclusions popup showing the two sections: "Eligible task purchases are limited to the following" and "The following are excluded from this task" with text input fields -->

Per entrambe le attività **Acquisto** e **Spesa**, puoi utilizzare l’attributo **[!UICONTROL Articoli idonei ed esclusioni]** per definire quali articoli e gruppi sono idonei e quali sono esclusi. Questo consente di eseguire il targeting di prodotti, categorie o punti vendita specifici per allinearli agli obiettivi della sfida.

Ad esempio, è possibile limitare un&#39;attività a specifiche categorie di prodotti oppure escludere le gift card o gli articoli promozionali dal conteggio per il completamento dell&#39;attività.

![](assets/tasks-create-eligible.png)

### Imposta gli elementi idonei per l&#39;attività

Per definire gli elementi idonei, immettere ID di elementi, categorie o ID di destinazione specifici, separati da virgole nel campo **[!UICONTROL Gli acquisti di attività idonee sono limitati al seguente]**. Se lasci vuoto questo campo, tutti gli acquisti sono idonei per impostazione predefinita. È inoltre possibile immettere `*` per rendere idonei in modo esplicito tutti gli acquisti.

Esempio: `SKU001, SKU002, CategoryA`

### Escludi elementi dall&#39;attività

Per escludere elementi dall&#39;attività, immettere ID di elementi, categorie o ID di destinazione specifici nel campo **[!UICONTROL I seguenti elementi sono esclusi da questa attività]**.

Esempio: `CLEARANCE01, GIFTCARD, SALE_CATEGORY`

### Acquisisci i tuoi dati per idoneità ed esclusioni {#byod-personalization}

>[!AVAILABILITY]
>
>L&#39;opzione **[!UICONTROL Porta i tuoi dati]** è attualmente disponibile per un gruppo limitato di organizzazioni e sarà resa disponibile in modo più ampio in una versione futura.

Oltre a immettere gli ID degli elementi per renderli idonei o escluderli, è anche possibile determinare l&#39;idoneità dai dati delle sfide di fedeltà esterne in fase di esecuzione utilizzando l&#39;opzione **[!UICONTROL Porta i tuoi dati]**.

Quando **[!UICONTROL Porta i tuoi dati]** è selezionato, l&#39;idoneità per partecipante viene risolta in fase di runtime dai dati sincronizzati con l&#39;ambiente delle sfide di fedeltà anziché da un elenco di ID elemento.

Per utilizzare questa opzione, seleziona l&#39;icona di personalizzazione in **[!UICONTROL Elementi ed esclusioni idonei]**, quindi scegli **[!UICONTROL Porta i tuoi dati]**.

![](assets/tasks-create-eligible-bring.png)

>[!IMPORTANT]
>
>Quando si assegna questa attività a una sfida, selezionare **[!UICONTROL Standard]** come tipo di sfida. Non selezionare **[!UICONTROL Porta i tuoi dati]** a livello di sfida, poiché tale opzione è riservata alle sfide completamente basate sui dati in cui l&#39;intera struttura, incluse attività e premi, viene fornita esternamente.

## Definire le proprietà dell’attività {#define-task-properties}

Nel riquadro **[!UICONTROL Proprietà]** dell&#39;attività configurare le informazioni di base sull&#39;attività:

* **[!UICONTROL Nome attività]**: immettere un nome descrittivo per l&#39;attività.
* **[!UICONTROL Descrizione attività]**: la descrizione viene generata automaticamente in base all&#39;attività e agli attributi configurati. Per immettere una descrizione personalizzata, disattiva l’opzione di generazione automatica e immetti la descrizione nel campo di testo.

![](assets/tasks-create-properties.png)

Dopo aver configurato tutti gli attributi e le proprietà, selezionare **[!UICONTROL Crea]** per salvare l&#39;attività. L’attività viene salvata nell’inventario Attività e, se creata dall’interno di una sfida, viene aggiunta automaticamente a tale sfida.
