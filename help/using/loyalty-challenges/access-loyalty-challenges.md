---
solution: Journey Optimizer
product: journey optimizer
title: Accesso e gestione delle sfide di fidelizzazione
description: Scopri come accedere, gestire e organizzare le sfide e le attività relative alla fedeltà in Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta privata" type="Informative"
source-git-commit: f41c1ed8a2d9e74b9d8fe97e0bf9e565d326aec6
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 0%

---


# Accesso e gestione delle sfide di fidelizzazione {#access-loyalty-challenges}

>[!BEGINSHADEBOX]

**Documentazione sulle sfide di fedeltà:**

* [Introduzione alle sfide di fidelizzazione](get-started.md) - Panoramica, flusso di lavoro, prerequisiti
* **Accedi alle sfide di fidelizzazione** ◀︎ **Sei qui** - Gestione di inventario, sfide e attività
* [Crea problemi](create-challenges.md) - Genera e configura problemi
* [Crea attività](create-tasks.md) - Definisci le attività di verifica

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>Questa funzionalità è attualmente in **versione beta privata** e potrebbe non essere disponibile nel tuo ambiente. Per richiedere l’accesso, contatta il rappresentante Adobe. Ulteriori informazioni sulle [etichette di disponibilità](../rn/releases.md#availability-labels).

## Accedere alle sfide leali

Per accedere alle sfide di fidelizzazione, passa a Journey Optimizer e seleziona **[!UICONTROL Sfida di fidelizzazione (Beta)]** nella sezione **[!UICONTROL Gestione Percorso]**.

L’interfaccia Sfide di fedeltà fornisce una posizione centralizzata per visualizzare, gestire e organizzare tutte le sfide e le attività. È possibile accedere a due inventari principali:

* **Inventario delle sfide**: visualizza e gestisci tutte le sfide di fidelizzazione, monitora il loro stato ed esegui azioni rapide
* **Inventario attività**: visualizza le attività riutilizzabili che possono essere utilizzate in più sfide

## Inventario delle sfide {#challenges-tab}

Nella scheda **[!UICONTROL Problemi]** sono visualizzate tutte le sfide ordinate in base alla data dell&#39;ultima modifica, con le sfide modificate più di recente visualizzate per prime.

![](assets/challenges-inventory.png)

Informazioni chiave visualizzate:

* **[!UICONTROL Sfida]**: nome della sfida
* **[!UICONTROL Stato]**: stato corrente della sfida (bozza o pubblicato)
* **[!UICONTROL Attività]**: numero di attività configurate nella richiesta di verifica
* **[!UICONTROL Percorso]**: collegamento al percorso generato automaticamente associato alla richiesta di verifica
* **[!UICONTROL Stato]**: stato corrente del percorso associato (Bozza, Live, Arrestato, ecc.)
* **[!UICONTROL Data di inizio/fine (UTC)]**: quando la richiesta di verifica diventa attiva e scade

Dalla scheda Sfide è possibile eseguire le azioni seguenti per le sfide:

* **Visualizza la sfida**: seleziona il nome della sfida per aprirne la pagina dei dettagli
* **Duplica una sfida**: seleziona l&#39;icona ![](assets/do-not-localize/Smock_More_18_N.svg) e scegli **[!UICONTROL Duplica]**. Viene creata una copia con tutte le attività, il contenuto e i messaggi intatti.
* **Elimina una sfida**: seleziona l&#39;icona ![](assets/do-not-localize/Smock_More_18_N.svg) e scegli **[!UICONTROL Elimina]**
* **Modifica una richiesta di verifica**: seleziona il nome della richiesta di verifica per aprirne la pagina dei dettagli e modificarla.

  Quando apri una sfida pubblicata per la modifica, devi innanzitutto ripristinarla allo stato Bozza:

   * Tutte le personalizzazioni apportate direttamente al percorso generato automaticamente andranno perse
   * La sfida torna allo stato Bozza
   * Dopo aver apportato le modifiche, è necessario salvare e pubblicare nuovamente la sfida
   * Devi ripubblicare il percorso associato per rendere la sfida aggiornata disponibile ai clienti

  >[!IMPORTANT]
  >
  >Il ripristino di una richiesta di verifica pubblicata in bozza non può essere annullato. Prima di procedere, considera l’impatto sul percorso attivo.

## Inventario attività {#tasks-tab}

Nella scheda **[!UICONTROL Attività]** sono visualizzate tutte le attività riutilizzabili che possono essere utilizzate in più sfide. Le attività create qui diventano disponibili per la selezione durante la creazione o la modifica di qualsiasi sfida.

![](assets/tasks-inventory.png)

Informazioni chiave visualizzate:

* **[!UICONTROL Nome attività]**: nome assegnato all&#39;attività
* **[!UICONTROL Descrizione]**: breve descrizione di ciò che l&#39;attività richiede
* **[!UICONTROL Attività attività]**: tipo di attività (acquisto, spesa)
* **[!UICONTROL SKU]**: elementi idonei e/o esclusi
* **[!UICONTROL Utilizzato nelle sfide]**: numero di sfide che attualmente utilizzano questa attività

Dalla scheda Attività è possibile eseguire le azioni seguenti sulle attività:

* **Visualizza/Modifica attività**: selezionare il nome dell&#39;attività per visualizzare la configurazione completa e modificare l&#39;attività
* **Duplica attività**: seleziona l&#39;icona ![](assets/do-not-localize/Smock_More_18_N.svg) e scegli **[!UICONTROL Duplica]**
* **Elimina attività**: seleziona l&#39;icona ![](assets/do-not-localize/Smock_More_18_N.svg) e scegli **[!UICONTROL Elimina]**
