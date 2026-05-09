---
solution: Journey Optimizer
product: journey optimizer
title: Frammenti percorso
description: Scopri come creare e utilizzare frammenti di percorso per salvare e riutilizzare set di nodi di percorso in più percorsi in Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
keywords: frammenti, percorso, riutilizzo, nodi, area di lavoro, inventario, riutilizzabile
badge: label="Disponibilità limitata" type="Informative"
version: Journey Orchestration
source-git-commit: 384f4e4b4c3acd9f1f1d73d4b140845870b31289
workflow-type: tm+mt
source-wordcount: '1482'
ht-degree: 1%

---


# Frammenti percorso {#journey-fragments}

>[!AVAILABILITY]
>Questa funzionalità è attualmente disponibile in modo limitato. Per richiedere l’accesso, contatta il tuo rappresentante Adobe.

I frammenti di percorso sono set riutilizzabili di nodi di percorso che è possibile compilare una volta e rilasciare in qualsiasi percorso della sandbox. Che si tratti di un controllo di idoneità, di una logica di indirizzamento dei canali preferita o di una sequenza di benvenuto, i frammenti consentono ai team di spostarsi più rapidamente e rimanere coerenti, senza dover ogni volta ricostruire la stessa logica da zero. [Vedi esempi di casi d&#39;uso.](#examples)

Una volta creati, i frammenti vengono memorizzati in un **[!UICONTROL Inventario frammenti]** dedicato e possono essere inseriti in qualsiasi percorso utilizzando l&#39;attività **[!UICONTROL Frammenti Percorso]**.

>[!NOTE]
>I frammenti di percorso utilizzano un **comportamento di copia**: inserendo un frammento in un percorso viene creata una copia statica dei nodi originali. Eventuali aggiornamenti apportati al frammento originale non vengono riflessi nei percorsi che l’hanno già utilizzato.

## Autorizzazioni {#journey-fragments-permissions}

Per utilizzare i frammenti di percorso, sono necessarie le [autorizzazioni](../administration/permissions.md) seguenti:

* **Gestisci Percorsi**: necessario per creare, modificare ed eliminare frammenti.
* **Pubblica Percorsi**: necessario per attivare un frammento.

## Accedere all’inventario dei frammenti {#journey-fragments-inventory}

I frammenti di percorso sono accessibili dalla sezione **[!UICONTROL Percorsi]**. Apri la scheda **[!UICONTROL Frammenti]** per sfogliare tutti i frammenti disponibili nella sandbox.

Puoi filtrare l’elenco per nome del frammento, stato, data di creazione, autore, data dell’ultima modifica o tag.

## Creare un frammento di percorso {#create-journey-fragment}

>[!CONTEXTUALHELP]
>id="ajo_journey_fragment_create_canvas"
>title="Salva come frammento di percorso"
>abstract="Immetti un nome univoco per il frammento e fai clic su Salva. I nodi selezionati verranno salvati come frammento riutilizzabile disponibile nell’inventario dei frammenti."

Puoi creare un frammento di percorso in due modi: direttamente dall’area di lavoro del percorso (scelta consigliata) o dall’inventario dei frammenti.

>[!BEGINTABS]

>[!TAB Dall&#39;area di lavoro del percorso]

Per salvare i nodi del percorso come frammento direttamente dall’area di lavoro del percorso:

1. Apri un percorso e seleziona uno o più nodi connessi nell’area di lavoro.
1. Fai clic sull&#39;icona **[!UICONTROL Salva come frammento]** nella barra degli strumenti.

   ![Icona per inserire un frammento di percorso](assets/journey-fragment-icon.png)

1. Immetti un nome univoco per il frammento all’interno della sandbox.

   ![Salva i nodi come frammento dall&#39;area di lavoro del percorso](assets/journey_fragment_create_canvas.png)

1. Fai clic su **[!UICONTROL Salva]**. Il frammento viene salvato come bozza.

>[!TIP]
>
>Se crei un frammento da un percorso, [verifica o simula il percorso](testing-the-journey.md) **prima** di salvare il frammento per garantire che i nodi selezionati si comportino come previsto.

>[!TAB Dall&#39;inventario dei frammenti]

Per creare un frammento direttamente dall’inventario:

1. Passa a **[!UICONTROL Percorsi]** > scheda **[!UICONTROL Frammenti]**.
1. Fare clic su **[!UICONTROL Crea frammento]**.
1. Nell’area di lavoro per la creazione dei frammenti, aggiungi e configura le attività di percorso.
1. Al termine, fai clic su **[!UICONTROL Salva]** per salvare il frammento come bozza.

>[!CAUTION]
>
>La modalità di test e la simulazione non sono disponibili nell’editor di frammenti. Ciò significa che non puoi convalidare il comportamento delle attività configurate prima che il frammento venga attivato e inserito in un percorso. Per i frammenti in cui l&#39;accuratezza della logica è fondamentale, è consigliabile [creare e testare o simulare prima i nodi in un percorso completo](testing-the-journey.md), quindi salvarli come frammento dalla scheda area di lavoro precedente.

>[!ENDTABS]

## Modificare un frammento {#edit-journey-fragment}

>[!CONTEXTUALHELP]
>id="ajo_journey_fragment_properties"
>title="Proprietà dei frammenti di percorso"
>abstract="Apri un frammento dall’inventario per modificarne nodi, proprietà, tag o etichette. I frammenti attivi devono essere disattivati prima di poter essere modificati."

Per modificare un frammento, aprirlo dall&#39;**[!UICONTROL Inventario frammenti]** facendo clic sul nome. Nell’interfaccia utente per l’authoring dei frammenti puoi effettuare le seguenti operazioni:

* Aggiungere, rimuovere o modificare le attività.
* Imposta o aggiorna le proprietà del frammento: nome, tag ed etichette.

>[!NOTE]
>
>* È possibile modificare solo **[!UICONTROL frammenti bozza]**. Per modificare un frammento **[!UICONTROL Attivo]**, disattivarlo.
>
>* La modalità di test e la simulazione non sono disponibili nell’editor di frammenti. Prima di salvare i nodi come frammento, verifica o simula qualsiasi logica a livello di percorso nell’intero percorso.
>
>* [Le attività Salta](jump.md) non sono consentite all&#39;interno di un frammento.

## Gestire i frammenti {#manage-journey-fragments}

### Stati dei frammenti {#fragment-statuses}

I frammenti di percorso seguono un ciclo di vita con i seguenti stati:

| Stato | Descrizione |
|---|---|
| **[!UICONTROL Bozza]** | Il frammento è in fase di creazione e non è ancora disponibile per l’utilizzo in percorsi. |
| **[!UICONTROL Attivo]** | Il frammento è pronto per essere utilizzato in percorsi. |
| **[!UICONTROL Archiviato]** | Il frammento è stato archiviato e non è più disponibile per l’utilizzo in percorsi. |

Le seguenti regole si applicano alle transizioni di stato dei frammenti:

* È possibile attivare solo **[!UICONTROL frammenti bozza]**. Apri una bozza di frammento e utilizza l&#39;icona **[!UICONTROL Attiva]**.
* Solo i **[!UICONTROL frammenti attivi]** possono essere disattivati o archiviati.
* È possibile annullare l&#39;archiviazione solo di **[!UICONTROL frammenti archiviati]**. L&#39;annullamento dell&#39;archiviazione di un frammento ne riporta lo stato **[!UICONTROL Bozza]**.
* È possibile eliminare solo **[!UICONTROL frammenti bozza]**.

>[!NOTE]
>Quando si attiva un frammento, vengono applicati la maggior parte dei controlli di convalida eseguiti durante la pubblicazione del percorso. Tuttavia, **gli attributi contestuali non sono convalidati** e **i criteri di governance non sono applicati** al momento dell&#39;attivazione; entrambi vengono valutati quando il frammento viene inserito e utilizzato in un percorso.

### Azioni frammento {#fragment-actions}

Dall’inventario dei frammenti, puoi eseguire le seguenti azioni su un frammento:

* **[!UICONTROL Apri]**: modifica il frammento facendo clic sul nome.
* **[!UICONTROL Duplicato]**: crea una copia del frammento, da **[!UICONTROL Altre azioni]** (...) icona.
* **[!UICONTROL Archivio]**: archiviare un frammento (disponibile solo per **[!UICONTROL frammenti attivi]**), dalle **[!UICONTROL Altre azioni]** (...) icona. I frammenti archiviati non sono più disponibili nel selettore di frammenti.
* **[!UICONTROL Annulla archiviazione]**: ripristina un frammento archiviato (disponibile solo per **[!UICONTROL Frammenti archiviati]**), dalle **[!UICONTROL Altre azioni]** (...) icona. Il frammento torna allo stato **[!UICONTROL Bozza]**.
* **[!UICONTROL Elimina]**: elimina definitivamente un frammento (disponibile solo per **[!UICONTROL Bozza]** frammenti) dalle **[!UICONTROL Altre azioni]** (...) icona.
* **[!UICONTROL Modifica tag]**: aggiungi o rimuovi tag di un frammento dalle **[!UICONTROL Altre azioni]** (...) icona.

## Utilizzare un frammento in un percorso {#use-journey-fragment}

>[!CONTEXTUALHELP]
>id="ajo_journey_fragment_add"
>title="Aggiungi un frammento di percorso"
>abstract="Nel selettore sono disponibili solo **[!UICONTROL frammenti attivi]**. L&#39;inserimento di un frammento crea una **copia statica** dei relativi nodi; gli aggiornamenti al frammento originale non vengono riflessi nel percorso."

Per inserire un frammento in un percorso:

1. Apri il percorso e trascina l&#39;attività **[!UICONTROL Frammenti di Percorso]** dalla barra a sinistra.
1. Rilascialo in un ramo esistente o su un’area di lavoro vuota. Viene visualizzato un selettore frammenti.
1. Individua o cerca il frammento da utilizzare. Puoi visualizzare in anteprima un frammento o aprirlo in un’altra scheda prima di inserirlo.
1. Seleziona il frammento. I relativi nodi vengono copiati nell’area di lavoro nel punto di rilascio.

>[!NOTE]
>Nel selettore sono disponibili solo **[!UICONTROL frammenti attivi]**. L&#39;inserimento di un frammento crea una **copia statica** dei relativi nodi. Tutti gli aggiornamenti successivi al frammento originale non verranno inclusi nel percorso.
>
>Quando si rilascia un frammento in un&#39;area di lavoro vuota, il frammento deve iniziare con un nodo **[!UICONTROL Read Audience]**, **[!UICONTROL Audience Qualification]** o **[!UICONTROL Event]** (stessa regola applicata all&#39;avvio di qualsiasi percorso).

## Guardrail e limitazioni {#guardrails}

I seguenti guardrail si applicano ai frammenti di percorso:

**Creazione frammento**

* I nomi dei frammenti devono essere **univoci per sandbox**.
* Un frammento può avere solo **un percorso di ingresso**. Le selezioni con più punti di ingresso non possono essere salvate come frammento.
* Solo **nodi connessi** possono essere salvati insieme come frammento.
* Un frammento **non può contenere un&#39;attività [Salta](jump.md)**.
* Un frammento può contenere un massimo di **20 nodi**.
* Una sandbox può avere un massimo di **200 frammenti attivi**.

**Utilizzo frammento**

* Solo i **[!UICONTROL frammenti attivi]** possono essere inseriti in un percorso.
* L&#39;inserimento di un frammento crea una **copia statica** dei relativi nodi. Gli aggiornamenti al frammento originale non vengono propagati ai percorsi in cui è stato utilizzato.
* Un frammento può essere rilasciato in un ramo esistente o su un’area di lavoro vuota. Quando viene rilasciato in un&#39;area di lavoro vuota, il frammento deve iniziare con un nodo **[!UICONTROL Read Audience]**, **[!UICONTROL Audience Qualification]** o **[!UICONTROL Event]**.

**Generale**

* I frammenti possono essere trovati utilizzando la barra di ricerca unificata [1} nella categoria **[!UICONTROL Frammenti di Percorso]**.](../start/search-filter-categorize.md)
* [Tag](tags.md) e **Etichette** sono supportati nei frammenti.
* [I registri di controllo](../privacy/audit-logs.md) sono supportati.
* I percorsi in esecuzione nel vecchio stack (utilizzando le campagne in linea) non supportano i frammenti di percorso. Duplica tale percorso per spostarlo nella nuova pila prima di utilizzare questa funzione.

## Esempi di casi d’uso {#examples}

Gli esempi seguenti illustrano i pattern di percorso comuni che possono essere salvati e riutilizzati come frammenti di percorso.

**Controlli di idoneità**

Un pattern di ingresso standard, ad esempio un nodo [Read Audience](read-audience.md) seguito da filtri di idoneità, può essere incapsulato in un frammento. Questo consente ai team di mantenere la coerenza nel modo in cui i profili entrano nei percorsi, riducendo al contempo i tempi di configurazione. Il frammento può essere solo l&#39;attività [Ottimizza](optimize.md) o l&#39;attività Leggi pubblico e Ottimizza insieme.

![Esempio di frammento di verifica idoneità](assets/journey-fragments-uc-eligibility-check.png)

**Canale preferito**

Un frammento può valutare il canale di comunicazione preferito di un profilo, e-mail, push o SMS, e instradare il profilo di conseguenza. Questa logica può essere riutilizzata in qualsiasi percorso che coinvolga la messaggistica in uscita, garantendo una gestione coerente delle preferenze di canale. Il frammento può includere l&#39;attività [Ottimizza](optimize.md) e tutti e tre i rami di canale.

![Esempio di frammento di canale preferito](assets/journey-fragments-uc-preferred-channel.png)

**Sequenza di benvenuto per l&#39;onboarding**

Una sequenza di benvenuto temporizzata, ad esempio una serie di tre messaggi che introducono un prodotto o un servizio, può essere salvata come frammento. Questo è utile per l’onboarding di nuovi utenti tra diversi segmenti di pubblico o linee di prodotti. Il frammento può includere le attività [Wait](wait-activity.md) e i nodi dei messaggi.

![Esempio di frammento di sequenza di benvenuto per l&#39;onboarding](assets/journey-fragments-uc-welcome-sequence.png)

**Promemoria e attesa basati sulla reazione**

Un frammento può incapsulare un&#39;attività E-mail seguita da una [Reazione](reaction-events.md), in attesa che il profilo apra l&#39;e-mail entro un determinato numero di giorni e inviando un promemoria in caso contrario. Questa logica viene comunemente riutilizzata nei percorsi di nutrizione e nei flussi di conversione di prova. Il frammento può includere le attività E-mail e Reazione.

![Esempio di frammento di promemoria basato su reazioni](assets/journey-fragments-uc-reminder.png)
