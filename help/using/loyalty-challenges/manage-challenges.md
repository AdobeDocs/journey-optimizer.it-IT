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
source-git-commit: f41c1ed8a2d9e74b9d8fe97e0bf9e565d326aec6
workflow-type: tm+mt
source-wordcount: '807'
ht-degree: 0%

---


# Gestire sfide e attività {#manage-challenges}

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

### Stati della sfida {#challenge-lifecycle}

Le sfide passano attraverso stati diversi durante il loro ciclo di vita:

* **Bozza**: è in corso la creazione o la modifica della richiesta di verifica e non è ancora disponibile per i clienti.
* **Pubblicato**: la sfida è attiva e il percorso associato è stato creato.

### Modifica le sfide {#edit-challenges}

Puoi modificare le sfide aprendole nell’inventario Sfide. Il comportamento di modifica varia a seconda dello stato della sfida:

**Sfide bozza**: è disponibile la funzionalità di modifica completa. Tutte le proprietà, le attività, il contenuto e la messaggistica possono essere modificati senza limitazioni.

**Sfide pubblicate**: quando apri una sfida pubblicata per la modifica, devi prima ripristinarla allo stato Bozza.

* Tutte le personalizzazioni apportate direttamente al percorso generato automaticamente andranno perse.
* La sfida torna allo stato Bozza.
* Dopo aver apportato le modifiche, è necessario salvare e pubblicare nuovamente la sfida.
* Devi ripubblicare il percorso associato per rendere la sfida aggiornata disponibile ai clienti.

>[!IMPORTANT]
>
>Il ripristino di una richiesta di verifica pubblicata in bozza non può essere annullato. Prima di procedere, considera l’impatto sul percorso attivo.

### Sfide duplicate {#duplicate-challenges}

La duplicazione di una sfida crea una copia esatta con tutte le attività, il contenuto e i messaggi intatti, consentendo di creare rapidamente nuove versioni senza iniziare da zero.

Per duplicare una richiesta di verifica:

1. Passa alla scheda **[!UICONTROL Sfide]** e individua la sfida da duplicare.

1. Seleziona l&#39;icona ![](assets/do-not-localize/Smock_More_18_N.svg) accanto a quella sfida e scegli **[!UICONTROL Duplica]**.

1. Viene creata una copia della sfida. Apri la richiesta duplicata e modifica le proprietà necessarie.

1. Salva la richiesta duplicata e genera il percorso associato.

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

* **Attività non utilizzate in sfide attive**: possono essere modificate liberamente. Tutte le proprietà possono essere modificate senza alcun impatto.
* **Attività utilizzate nelle sfide live**: presta attenzione, poiché le modifiche influiscono su tutte le sfide che utilizzano l&#39;attività. Le modifiche si applicano immediatamente a tutte le sfide di riferimento.

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

* Controlla il conteggio **[!UICONTROL Usato nelle sfide]** nell&#39;inventario Attività.
* Assicurati che nessuna sfida in bozza, pianificata o live faccia riferimento all’attività.

Per eliminare un&#39;attività:

1. Passa alla scheda **[!UICONTROL Attività]** nell&#39;inventario Sfide fedeltà.

1. Individuare l&#39;attività da eliminare.

1. Verifica che il conteggio **[!UICONTROL Usato nelle sfide]** indichi 0. Se il conteggio è maggiore di 0, è necessario rimuovere l&#39;attività da tutte le sfide prima di eliminarla.

1. Seleziona l&#39;icona ![](assets/do-not-localize/Smock_More_18_N.svg) accanto all&#39;attività.

1. Scegliere **[!UICONTROL Elimina]**.

1. Confermate l&#39;eliminazione nella finestra di dialogo.

>[!NOTE]
>
>Se un’attività viene utilizzata in una sfida (bozza, pianificata o live), devi prima rimuoverla da tutte le sfide prima di poterla eliminare. È consigliabile archiviare o duplicare le attività anziché eliminarle, se necessario in futuro.
