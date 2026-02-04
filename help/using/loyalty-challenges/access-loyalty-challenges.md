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
source-git-commit: e98fe328b5a72a7091d48b5e2939a24e4ad6954c
workflow-type: tm+mt
source-wordcount: '807'
ht-degree: 0%

---


# Accedere alle sfide di fedeltà {#access-loyalty-challenges}

>[!BEGINSHADEBOX]

**Documentazione sulle sfide di fedeltà:**

* [Introduzione alle sfide di fidelizzazione](get-started.md) - Panoramica, flusso di lavoro, prerequisiti
* **Accedi alle sfide di fidelizzazione** ◀︎ **Sei qui** - Inventario e filtro
* [Crea problemi](create-challenges.md) - Genera e configura problemi
* [Gestire le sfide](manage-challenges.md) - Modificare, monitorare, ottimizzare

>[!ENDSHADEBOX]

## Accedere all’inventario delle sfide di fedeltà {#access-inventory}

Per accedere alle sfide di fedeltà:

1. In Adobe Journey Optimizer, seleziona **[!UICONTROL Sfide fedeltà]** nel menu di navigazione a sinistra nella sezione **[!UICONTROL percorsi di clienti]**.

2. Viene visualizzata la pagina Sfide di fedeltà con due schede:
   * **[!UICONTROL Sfide]**: visualizza e gestisci tutte le sfide relative alla fedeltà
   * **[!UICONTROL Attività]**: visualizza e gestisci tutte le attività che possono essere riutilizzate in più sfide

Per impostazione predefinita, la scheda **[!UICONTROL Sfide]** è selezionata e mostra tutte le sfide esistenti nell&#39;organizzazione.

## Scheda Problemi {#challenges-tab}

Nella scheda Sfide vengono visualizzate tutte le sfide ordinate in base alla data dell’ultima modifica, con le sfide modificate più di recente visualizzate per prime.

### Informazioni sull’inventario delle sfide {#inventory-overview}

Nell&#39;inventario Sfide vengono visualizzate tutte le sfide con le seguenti informazioni:

* **[!UICONTROL Nome sfida]**: il nome assegnato alla sfida
* **[!UICONTROL Stato]**: stato corrente della richiesta di verifica (vedere le descrizioni dello stato di seguito)
* **[!UICONTROL Tipo]**: tipo di verifica (Standard, Streak o Sequenziale)
* **[!UICONTROL Data di inizio]**: quando la sfida diventa attiva
* **[!UICONTROL Data di fine]**: quando scade la sfida
* **[!UICONTROL Creato da]**: utente che ha creato la sfida
* **[!UICONTROL Ultima modifica]**: data e ora dell&#39;ultima modifica
* **[!UICONTROL Tag]**: qualsiasi tag applicato alla richiesta di verifica per l&#39;organizzazione

### Stati di sfida {#challenge-statuses}

Le sfide possono avere i seguenti stati:

* **[!UICONTROL Bozza]**: è in corso la creazione o la modifica della richiesta di verifica, ma non è ancora stata pubblicata
* **[!UICONTROL Pianificato]**: la sfida è pubblicata e pianificata per iniziare in una data futura
* **[!UICONTROL Live]**: la sfida è attualmente attiva e disponibile per il pubblico di destinazione
* **[!UICONTROL Completato]**: la sfida ha superato la data di fine oppure tutti gli obiettivi sono stati raggiunti
* **[!UICONTROL Arrestato]**: la verifica è stata arrestata manualmente prima del completamento
* **[!UICONTROL Archiviato]**: la sfida è stata archiviata per scopi organizzativi

### Problemi di ricerca e filtro {#search-challenges}

Utilizza la funzionalità di ricerca per trovare rapidamente problemi specifici per nome o descrizione.

Puoi anche applicare i filtri per restringere l’elenco delle sfide in base a criteri specifici. Puoi combinare più filtri per perfezionare la ricerca.

Puoi filtrare le sfide in base al loro stato corrente, al tipo di sfida, alle date di inizio o fine o ai tag applicati per l’organizzazione.

### Intervenire sulle sfide {#inventory-actions}

Dalla scheda Sfide, puoi eseguire azioni rapide sulle sfide:

* **Visualizza dettagli richiesta di verifica**: seleziona un nome di richiesta di verifica per aprire la pagina dei dettagli
* **Modifica una sfida**: seleziona il menu altre azioni (tre punti) e scegli **[!UICONTROL Modifica]**
* **Duplica una sfida**: seleziona il menu Altre azioni e scegli **[!UICONTROL Duplica]**
* **Interrompi una sfida dal vivo**: seleziona il menu Altre azioni e scegli **[!UICONTROL Interrompi]**
* **Archivia una sfida**: seleziona il menu Altre azioni e scegli **[!UICONTROL Archivia]**
* **Elimina una bozza di richiesta di verifica**: seleziona il menu Altre azioni e scegli **[!UICONTROL Elimina]** (disponibile solo per le bozze)

### Crea una nuova sfida {#create-from-inventory}

Per creare una nuova sfida dalla scheda Sfide:

1. Seleziona **[!UICONTROL Crea sfida]** nell&#39;angolo in alto a destra.

2. Viene avviato il flusso di lavoro per la creazione della sfida.

Per istruzioni dettagliate, consulta [Creare le sfide](create-challenges.md).

## Scheda Attività {#tasks-tab}

Nella scheda Attività vengono visualizzate tutte le attività riutilizzabili che possono essere utilizzate in più sfide. Le attività create qui diventano disponibili per la selezione durante la creazione o la modifica di qualsiasi sfida.

### Informazioni sull&#39;inventario dei task {#tasks-inventory-overview}

Nell&#39;inventario dei task vengono visualizzati tutti i task con le seguenti informazioni:

* **[!UICONTROL Nome attività]**: nome assegnato all&#39;attività
* **[!UICONTROL Tipo di attività]**: tipo di azione (acquisto, importo spesa, visita, coinvolgimento, evento personalizzato)
* **[!UICONTROL Descrizione]**: breve descrizione di ciò che l&#39;attività richiede
* **[!UICONTROL Creato da]**: utente che ha creato l&#39;attività
* **[!UICONTROL Ultima modifica]**: data e ora dell&#39;ultima modifica
* **[!UICONTROL Utilizzato nelle sfide]**: numero di sfide che attualmente utilizzano questa attività

### Creare attività dalla scheda Attività {#create-tasks-from-tab}

È possibile creare le attività in due modi:

1. **Dalla scheda Attività** (consigliato per le attività riutilizzabili):
   * Passa alla scheda **[!UICONTROL Attività]**
   * Seleziona **[!UICONTROL Crea attività]**
   * Configurare le proprietà del task (nome, tipo, quantità, filtri prodotti, premi)
   * Salva l’attività per renderla disponibile per l’utilizzo in qualsiasi sfida

2. **Durante la creazione di una sfida** (per attività specifiche della sfida):
   * Durante la creazione della sfida, seleziona **[!UICONTROL Aggiungi attività]** nella sezione Attività
   * Scegli **[!UICONTROL Crea nuova attività]** o seleziona un&#39;attività esistente
   * Le attività create in questo modo vengono salvate anche nell&#39;inventario Attività e possono essere riutilizzate

>[!TIP]
>
>La creazione di attività dalla scheda Attività è consigliata quando si prevede di utilizzare la stessa attività in più sfide. Ciò garantisce la coerenza e semplifica l&#39;aggiornamento centralizzato delle definizioni delle attività.

### Azioni sulle attività {#tasks-actions}

Dalla scheda Attività è possibile eseguire le azioni seguenti sulle attività:

* **Visualizza dettagli attività**: selezionare un nome attività per visualizzare la configurazione completa
* **Modifica un&#39;attività**: seleziona il menu altre azioni (tre punti) e scegli **[!UICONTROL Modifica]**
* **Duplica un&#39;attività**: seleziona il menu Altre azioni e scegli **[!UICONTROL Duplica]**
* **Elimina un&#39;attività**: seleziona il menu Altre azioni e scegli **[!UICONTROL Elimina]** (solo se non utilizzato in alcuna sfida attiva)
* **Utilizzo visualizzazione**: individuare le sfide attualmente associate all&#39;attività

## Passaggi successivi {#next-steps}

Ora che sai come accedere e navigare nell’inventario delle sfide di fedeltà:

* [Crea sfide](create-challenges.md) - Scopri come creare la tua prima sfida
* [Gestire le sfide](manage-challenges.md) - Scopri come modificare e monitorare le sfide
