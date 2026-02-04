---
solution: Journey Optimizer
product: journey optimizer
title: Gestire le sfide di fidelizzazione
description: Scopri come gestire, monitorare e ottimizzare le sfide legate alla fedeltà in Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta privata" type="Informative"
source-git-commit: dbed4ffeb63ec3c58ff61845bbdb91fd2d51e69b
workflow-type: tm+mt
source-wordcount: '955'
ht-degree: 0%

---


# Gestire le sfide {#manage-challenges}

>[!BEGINSHADEBOX]

**Documentazione sulle sfide di fedeltà:**

* [Introduzione alle sfide di fidelizzazione](get-started.md) - Panoramica, flusso di lavoro, prerequisiti
* [Accedere alle sfide di fidelizzazione](access-loyalty-challenges.md) - Inventario e filtro
* [Crea problemi](create-challenges.md) - Genera e configura problemi
* [Crea attività](create-tasks.md) - Definisci le attività di verifica
* **Gestisci le sfide** ◀︎ **Sei qui** - Modifica, monitora, ottimizza

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Questa funzionalità è attualmente in **versione beta privata** e potrebbe non essere disponibile nel tuo ambiente. Per richiedere l’accesso, contatta il rappresentante Adobe. Ulteriori informazioni sulle [etichette di disponibilità](../rn/releases.md#availability-labels).

## Gestire le sfide {#manage-challenges-section}

### Ciclo di vita della sfida {#challenge-lifecycle}

<!-- VISUAL: Flowchart diagram showing challenge lifecycle with status transitions: Draft → Scheduled → Live → Completed/Stopped/Archived -->

Le sfide passano attraverso stati diversi durante il loro ciclo di vita:

* **Bozza**: è in corso la creazione o la modifica della richiesta di verifica e non è ancora disponibile per i clienti
* **Pianificato**: la sfida è stata pubblicata e diventerà automaticamente attiva alla data di inizio specificata
* **Live**: la sfida è attualmente attiva e i clienti possono partecipare
* **Completato**: la sfida è terminata - la data di fine è passata o tutti gli obiettivi sono stati raggiunti
* **Interrotto**: la sfida è stata interrotta manualmente prima del completamento naturale
* **Archiviato**: la sfida è stata archiviata per scopi organizzativi e non è più visibile nell&#39;inventario principale

### Modifica le sfide {#edit-challenges}

Puoi modificare le sfide in base al loro stato corrente:

* **Sfide bozza**: funzionalità di modifica completa - tutte le proprietà possono essere modificate
* **Sfide pianificate/live**: modifiche limitate. È possibile aggiornare il contenuto, i messaggi e le date di estensione, ma non modificare la struttura delle sfide principali (definizioni di tipo, pubblico o attività)

Per modificare una richiesta di verifica:

1. Passa alla scheda **[!UICONTROL Sfide]** nell&#39;inventario Sfide fedeltà.

1. Individua la sfida da modificare.

1. Seleziona il nome della richiesta di verifica per aprirla in modalità di modifica.

1. Apporta le modifiche in base allo stato della sfida:
   * **Sfide bozza**: modifica proprietà, attività, contenuto o messaggi
   * **Sfide pianificate/live**: aggiorna le schede di contenuto, i messaggi o estendi le date di fine in base alle esigenze

1. Salva le modifiche. Per le sfide pianificate o live, le modifiche diventano effettive immediatamente o in base alla pianificazione degli aggiornamenti.

>[!NOTE]
>
>Per le modifiche che richiedono modifiche principali (come la modifica del tipo di sfida, del pubblico o della struttura delle attività), duplica la sfida e crea una nuova versione invece di modificare quella esistente.

### Sfide duplicate {#duplicate-challenges}

Sfide duplicate per:

* Riesecuzione delle sfide riuscite per nuovi periodi di tempo
* Creare varianti per tipi di pubblico diversi
* Aggiorna i requisiti o i premi delle attività
* Riattivare le sfide interrotte o completate

La duplicazione di una sfida crea una copia esatta con tutte le attività, il contenuto e i messaggi intatti, consentendo di creare rapidamente nuove versioni senza iniziare da zero.

Per duplicare una richiesta di verifica:

1. Passa alla scheda **[!UICONTROL Sfide]** nell&#39;inventario Sfide fedeltà.

1. Individua la sfida da duplicare.

1. Seleziona il menu altre azioni (tre punti) accanto a quella sfida.

1. Scegli **[!UICONTROL Duplica]**.

1. Viene creata una copia della sfida con &quot;[Copia]&quot; aggiunto al nome.

1. Apri la richiesta duplicata e modifica le proprietà necessarie:
   * Aggiorna il nome della richiesta di verifica
   * Regolare le date di inizio e fine
   * Se necessario, modifica il pubblico di destinazione
   * Modifica attività, premi, contenuto o messaggi in base alle esigenze

1. Rivedi e pubblica la sfida duplicata.

### Monitorare le prestazioni {#monitor-performance}

<!-- SCREENSHOT: Challenge Performance tab showing key metrics dashboard with participation, completion, reward, and engagement metrics -->

Monitora le prestazioni della sfida tramite metriche chiave:

* **Metriche di partecipazione**:
   * Iscrizione: numero di clienti che hanno partecipato alla sfida
   * Partecipanti attivi: clienti attualmente coinvolti nella sfida
* **Metriche di completamento**:
   * Percentuali di completamento: percentuale di clienti iscritti che hanno completato la sfida
   * Tempo medio di completamento: tempo medio impiegato per completare tutte le attività
* **Metriche premio**:
   * Premi totali distribuiti: valore aggregato di tutti i premi forniti
   * Premi per tipo: suddivisione dei premi per categoria di premio
* **Metriche di coinvolgimento**:
   * Impression della scheda di contenuto: numero di volte in cui sono state visualizzate le schede di contenuto di sfida
   * Consegna dei messaggi: numero di messaggi inviati correttamente su tutti i canali

Per accedere ai dati sulle prestazioni:

1. Passa alla scheda **[!UICONTROL Sfide]** nell&#39;inventario Sfide fedeltà.

1. Seleziona la sfida da monitorare.

1. Apri la scheda **[!UICONTROL Prestazioni]** per visualizzare metriche e analisi in tempo reale.

<!-- SCREENSHOT: Journey report showing challenge performance data with graphs and tables -->

Puoi anche accedere ai dati dettagliati sulle prestazioni nei [rapporti di percorso generati automaticamente](../reports/journey-global-report-cja.md), che forniscono ulteriori informazioni e tendenze storiche.

## Gestire le attività {#manage-tasks}

Le attività sono componenti riutilizzabili che possono essere utilizzati in più sfide. La gestione efficace delle attività garantisce la coerenza tra i diversi programmi fedeltà e semplifica l&#39;aggiornamento centralizzato delle definizioni delle attività. Le attività create in una sfida possono essere riutilizzate in altre sfide, riducendo la duplicazione e mantenendo la standardizzazione.

### Modifica attività {#edit-tasks}

È possibile modificare le attività esistenti dall&#39;inventario Attività. Considera i seguenti aspetti:

* **Attività non utilizzate in sfide attive**: possono essere modificate liberamente - tutte le proprietà possono essere modificate senza alcun impatto
* **Attività utilizzate nelle sfide live**: fai attenzione, poiché le modifiche influiscono su tutte le sfide utilizzando l&#39;attività: le modifiche vengono applicate immediatamente a tutte le sfide di riferimento

Per modificare un&#39;attività:

1. Passa alla scheda **[!UICONTROL Attività]** nell&#39;inventario Sfide fedeltà.

1. Individuare l&#39;attività da modificare.

1. Selezionare il nome dell&#39;attività per aprirla in modalità di modifica.

1. Modifica le proprietà dell’attività come necessario:
   * Aggiorna il nome o la descrizione dell&#39;attività
   * Modifica il tipo di attività o gli attributi
   * Regolare elementi ed esclusioni idonei
   * Modifica fabbisogni quantità o importo

1. Salva le modifiche.

>[!WARNING]
>
>Quando modifichi un’attività utilizzata attivamente nelle sfide live, prendi in considerazione la creazione di un duplicato con una nuova versione anziché modificare l’originale. In questo modo si evitano modifiche non desiderate alle sfide attive e si può testare le modifiche prima di applicarle.

### Elimina attività {#delete-tasks}

Le attività possono essere eliminate solo se non sono attualmente utilizzate in alcuna sfida. Prima di eliminare un’attività:

* Controlla il conteggio **[!UICONTROL Usato nelle sfide]** nell&#39;inventario Attività
* Assicurati che nessuna sfida in bozza, pianificata o live faccia riferimento all’attività

Per eliminare un&#39;attività:

1. Passa alla scheda **[!UICONTROL Attività]** nell&#39;inventario Sfide fedeltà.

1. Individuare l&#39;attività da eliminare.

1. Verifica che il conteggio **[!UICONTROL Usato nelle sfide]** indichi 0. Se il conteggio è maggiore di 0, è necessario rimuovere l&#39;attività da tutte le sfide prima di eliminarla.

1. Selezionare il menu Altre azioni (tre punti) accanto all&#39;attività.

1. Scegliere **[!UICONTROL Elimina]**.

1. Confermate l&#39;eliminazione nella finestra di dialogo.

>[!NOTE]
>
>Se un’attività viene utilizzata in una sfida (bozza, pianificata o live), devi prima rimuoverla da tutte le sfide prima di poterla eliminare. È consigliabile archiviare o duplicare le attività anziché eliminarle, se necessario in futuro.
