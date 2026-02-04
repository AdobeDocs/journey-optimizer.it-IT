---
solution: Journey Optimizer
product: journey optimizer
title: Accedere alle sfide di fedeltà
description: Scopri come accedere, cercare e filtrare le sfide relative alla fedeltà in Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta privata" type="Informative"
source-git-commit: dbed4ffeb63ec3c58ff61845bbdb91fd2d51e69b
workflow-type: tm+mt
source-wordcount: '744'
ht-degree: 0%

---


# Accedere alle sfide di fedeltà {#access-loyalty-challenges}

>[!BEGINSHADEBOX]

**Documentazione sulle sfide di fedeltà:**

* [Introduzione alle sfide di fidelizzazione](get-started.md) - Panoramica, flusso di lavoro, prerequisiti
* **Accedi alle sfide di fidelizzazione** ◀︎ **Sei qui** - Inventario e filtro
* [Crea problemi](create-challenges.md) - Genera e configura problemi
* [Crea attività](create-tasks.md) - Definisci le attività di verifica
* [Gestire le sfide](manage-challenges.md) - Modificare, monitorare, ottimizzare

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Questa funzionalità è attualmente in **versione beta privata** e potrebbe non essere disponibile nel tuo ambiente. Per richiedere l’accesso, contatta il rappresentante Adobe. Ulteriori informazioni sulle [etichette di disponibilità](../rn/releases.md#availability-labels).

## Accedere all’inventario delle sfide di fedeltà {#access-inventory}

<!-- SCREENSHOT: Journey Optimizer main menu showing "Loyalty challenges" under "Customer journeys" section -->

Per accedere alle sfide di fedeltà, passa a Journey Optimizer e seleziona **[!UICONTROL Sfide di fedeltà]** nella sezione **[!UICONTROL percorsi di clienti]**.

<!-- SCREENSHOT: Loyalty Challenges landing page showing the two tabs: Challenges and Tasks -->

Viene visualizzata la pagina Sfide di fedeltà con due schede:

* **[!UICONTROL Sfide]**: visualizza e gestisci tutte le sfide relative alla fedeltà

* **[!UICONTROL Attività]**: visualizza e gestisci tutte le attività che possono essere riutilizzate in più sfide

## Inventario delle sfide {#challenges-tab}

<!-- SCREENSHOT: Challenges tab showing the inventory table with columns: Challenge name, Status, Type, Start date, End date, Created by, Last modified, Tags -->

Nella scheda Sfide vengono visualizzate tutte le sfide ordinate in base alla data dell’ultima modifica, con le sfide modificate più di recente visualizzate per prime. Vengono visualizzate le seguenti informazioni:

* **[!UICONTROL Nome sfida]**: il nome assegnato alla sfida
* **[!UICONTROL Stato]**: stato corrente della richiesta di verifica (vedere le descrizioni dello stato di seguito)
* **[!UICONTROL Tipo]**: tipo di verifica (Standard, Streak o Sequenziale)
* **[!UICONTROL Data di inizio]**: quando la sfida diventa attiva
* **[!UICONTROL Data di fine]**: quando scade la sfida
* **[!UICONTROL Creato da]**: utente che ha creato la sfida
* **[!UICONTROL Ultima modifica]**: data e ora dell&#39;ultima modifica
* **[!UICONTROL Tag]**: qualsiasi tag applicato alla richiesta di verifica per l&#39;organizzazione

### Stati di sfida {#challenge-statuses}

<!-- VISUAL: Status badges showing different challenge statuses with color coding: Draft (gray), Scheduled (blue), Live (green), Completed (gray), Stopped (red), Archived (gray) -->

Le sfide vengono visualizzate con diversi stati che indicano il loro stato corrente nel ciclo di vita:

* **Bozza**: è in corso la creazione o la modifica della sfida
* **Pianificato**: la sfida è pubblicata e diventerà attiva alla data di inizio
* **Live**: la sfida è attiva e i clienti possono partecipare
* **Completato**: la data di fine della sfida è passata o gli obiettivi sono stati raggiunti
* **Arrestato**: la verifica è stata arrestata manualmente prima del completamento
* **Archiviato**: la sfida è stata archiviata per scopi organizzativi

Per informazioni dettagliate sulle transizioni di stato e sul ciclo di vita della sfida, vedere [Ciclo di vita della sfida](manage-challenges.md#challenge-lifecycle).

### Problemi di ricerca e filtro {#search-challenges}

<!-- SCREENSHOT: Search bar and filter panel showing available filters (status, type, dates, tags) with an example of active filters applied -->

Puoi individuare rapidamente le sfide utilizzando la ricerca e i filtri:

**Ricerca:**

* Utilizza la barra di ricerca per trovare le sfide immettendo parole chiave dal nome o dalla descrizione della sfida. Gli aggiornamenti della ricerca vengono eseguiti in tempo reale durante la digitazione.

**Filtri:**

* Applica uno o più filtri per limitare i risultati:
   * **Stato**: filtra per stato della richiesta di verifica (bozza, pianificato, live, completato, interrotto, archiviato)
   * **Tipo**: filtra per tipo di richiesta (Standard, Streak, Sequenziale)
   * **Date**: filtra per intervalli di date di inizio o fine
   * **Tag**: filtra per tag applicati alle sfide

È possibile combinare più filtri contemporaneamente. Ad esempio, filtra per le sfide Live Standard con tag &quot;Estate 2024&quot; per trovare rapidamente campagne stagionali attive.

Per cancellare i filtri, selezionare **[!UICONTROL Cancella tutto]** o rimuovere i singoli filtri.

### Intervenire sulle sfide {#inventory-actions}

<!-- SCREENSHOT: More actions menu (three dots) expanded showing options: Edit, Duplicate, Stop, Archive, Delete -->

Dalla scheda Sfide, puoi eseguire azioni rapide sulle sfide:

* **Visualizza dettagli richiesta di verifica**: seleziona il nome della richiesta di verifica per aprirne la pagina dei dettagli
* **Modifica una sfida**: seleziona il menu **[!UICONTROL Altre azioni]** (tre punti) e scegli **[!UICONTROL Modifica]**
* **Duplica una sfida**: seleziona il menu **[!UICONTROL Altre azioni]** e scegli **[!UICONTROL Duplica]**
* **Interrompi una sfida dal vivo**: seleziona il menu **[!UICONTROL Altre azioni]** e scegli **[!UICONTROL Interrompi]**
* **Archivia una sfida**: seleziona il menu **[!UICONTROL Altre azioni]** e scegli **[!UICONTROL Archivia]**
* **Elimina una bozza di richiesta**: seleziona il menu **[!UICONTROL Altre azioni]** e scegli **[!UICONTROL Elimina]** (disponibile solo per le bozze)

Per informazioni dettagliate sulla gestione delle problematiche dopo la creazione, incluse limitazioni di modifica, strategie di duplicazione, monitoraggio delle prestazioni e risoluzione dei problemi, consulta [Gestione delle problematiche](manage-challenges.md).

## Inventario attività {#tasks-tab}

<!-- SCREENSHOT: Tasks tab showing the inventory table with columns: Task name, Task type, Description, Created by, Last modified, Used in challenges -->

Nella scheda Attività vengono visualizzate tutte le attività riutilizzabili che possono essere utilizzate in più sfide. Le attività create qui diventano disponibili per la selezione durante la creazione o la modifica di qualsiasi sfida.

Nell&#39;inventario dei task vengono visualizzate le seguenti informazioni:

* **[!UICONTROL Nome attività]**: nome assegnato all&#39;attività
* **[!UICONTROL Tipo di attività]**: tipo di azione (acquisto, importo spesa, visita, coinvolgimento, evento personalizzato)
* **[!UICONTROL Descrizione]**: breve descrizione di ciò che l&#39;attività richiede
* **[!UICONTROL Creato da]**: utente che ha creato l&#39;attività
* **[!UICONTROL Ultima modifica]**: data e ora dell&#39;ultima modifica
* **[!UICONTROL Utilizzato nelle sfide]**: numero di sfide che attualmente utilizzano questa attività

### Azioni sulle attività {#tasks-actions}

Dalla scheda Attività è possibile eseguire le azioni seguenti sulle attività:

* **Visualizza dettagli attività**: selezionare il nome attività per visualizzare la configurazione completa
* **Modifica attività**: seleziona il menu **[!UICONTROL Altre azioni]** (tre punti) e scegli **[!UICONTROL Modifica]**
* **Duplica attività**: seleziona il menu **[!UICONTROL Altre azioni]** e scegli **[!UICONTROL Duplica]**
* **Elimina un&#39;attività**: seleziona il menu **[!UICONTROL Altre azioni]** e scegli **[!UICONTROL Elimina]** (solo se non viene utilizzato in alcuna sfida attiva)
* **Utilizzo visualizzazione**: individuare le sfide attualmente associate all&#39;attività

## Passaggi successivi {#next-steps}

Ora che sai come accedere e navigare nell’inventario delle sfide di fedeltà:

* [Crea sfide](create-challenges.md) - Scopri come creare la tua prima sfida e configurare le attività
* [Crea attività](create-tasks.md) - Scopri come definire attività riutilizzabili per le sfide
* [Gestire le sfide](manage-challenges.md) - Scopri come modificare, monitorare e ottimizzare le sfide
