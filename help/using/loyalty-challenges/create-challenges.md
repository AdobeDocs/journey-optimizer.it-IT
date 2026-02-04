---
solution: Journey Optimizer
product: journey optimizer
title: Creare problemi di fidelizzazione
description: Scopri come creare e configurare le sfide relative alla fedeltà in Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta privata" type="Informative"
source-git-commit: fd87aeabfae1f07d8f7bea7057f0c6dd0559d024
workflow-type: tm+mt
source-wordcount: '1521'
ht-degree: 0%

---


# Creare le sfide {#create-challenges}

>[!BEGINSHADEBOX]

**Documentazione sulle sfide di fedeltà:**

* [Introduzione alle sfide di fidelizzazione](get-started.md) - Panoramica, flusso di lavoro, prerequisiti
* [Accedere alle sfide di fidelizzazione](access-loyalty-challenges.md) - Inventario e filtro
* **Crea problemi** ◀︎ **Sei qui** - Genera e configura problemi
* [Crea attività](create-tasks.md) - Definisci le attività di verifica
* [Gestire le sfide](manage-challenges.md) - Modificare, monitorare, ottimizzare

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Questa funzionalità è attualmente in **versione beta privata** e potrebbe non essere disponibile nel tuo ambiente. Per richiedere l’accesso, contatta il rappresentante Adobe. Ulteriori informazioni sulle [etichette di disponibilità](../rn/releases.md#availability-labels).

## Come funziona {#how-it-works}

La creazione e il lancio di una sfida di fidelizzazione segue questo flusso di lavoro:

1. **[Crea la sfida](#create-the-challenge)** - Scegli il tipo di sfida (Standard, Streak o Sequenziale) più adatto agli obiettivi del programma fedeltà.

1. **[Configura la struttura della sfida](#structure)**. Definisci le proprietà della sfida, la pianificazione, le attività che i clienti devono completare e i premi che otterranno.

1. **[Configura schede di contenuto](#configure-content-cards)** - Progetta le schede di contenuto per rappresentare visivamente la tua sfida sui dispositivi dei clienti, visualizzando informazioni sulla sfida, l&#39;avanzamento e i premi.

1. **[Configurazione della messaggistica](#configure-messaging)** (facoltativo): configurazione di messaggi multicanale (in-app, e-mail, push) per le fasi chiave: avvio, in corso e completamento.

1. **[Seleziona il pubblico della sfida](#audience)** - Definisci quali clienti sono idonei a partecipare alla sfida.

1. **[Genera e attiva il percorso](#review-and-publish)**. Genera il percorso associato e attivalo per rendere la sfida disponibile al pubblico di destinazione.

## Crea la sfida {#create-the-challenge}

1. Passa a **[!UICONTROL Sfide fedeltà (Beta)]** in Journey Optimizer.

1. Seleziona la scheda **[!UICONTROL Sfide]** e seleziona **[!UICONTROL Crea sfida]**.

   ![](assets/challenge-create.png)

1. Scegli il tipo di sfida:

   * **[!UICONTROL Standard]**: i clienti completano un numero specificato di attività in qualsiasi ordine
   * **[!UICONTROL Streak]**: i clienti completano la stessa attività più volte consecutivamente
   * **[!UICONTROL Sequenziale]**: i clienti completano le attività in un ordine definito

## Configurare la struttura delle sfide {#structure}

Nella scheda Struttura puoi definire l’organizzazione della sfida: le proprietà, la pianificazione, le attività da completare e i premi da assegnare.

### Definire le proprietà della sfida e utilizzare metadati personalizzati {#properties}

1. Nel riquadro delle proprietà della sfida, configura le proprietà della sfida:

   ![](assets/challenge-create-properties.png)

   **Nome**: immetti un nome descrittivo per la richiesta. Questo nome viene visualizzato nell’inventario delle sfide e consente di identificare la sfida.

   **Descrizione**: immetti una descrizione per la richiesta di verifica.

1. Utilizza la sezione **[!UICONTROL Metadati personalizzati]** per aggiungere metadati personalizzati utilizzando coppie chiave/valore. Questi metadati possono essere utilizzati per il tracciamento, la segmentazione o l’integrazione con sistemi esterni.

### Pianificare la sfida {#schedule}

Pianifica la sfida selezionando l&#39;icona ![](assets/do-not-localize/schedule-icon.svg) **[!UICONTROL Apri pianificazione]**.

* **Data e ora di inizio**: imposta quando la sfida diventa disponibile per i clienti (formato: mm/gg/aaaa, —:— AM/PM).

* **Data e ora di fine**: imposta quando scade la sfida e non accetta più nuovi completamenti (formato: mm/gg/aaaa, —:— AM/PM).

* **Fuso orario**: per impostazione predefinita, la sfida utilizza il fuso orario locale del destinatario.

* **Le attività devono essere completate**: scegli quando i clienti possono completare le attività:

   * **[!UICONTROL In qualsiasi momento durante la verifica]**: i clienti possono completare le attività in qualsiasi momento tra le date di inizio e di fine della verifica
   * **[!UICONTROL In ore specifiche del giorno]**: limita il completamento dell&#39;attività a ore giornaliere specifiche impostando **[!UICONTROL Ora inizio]** e **[!UICONTROL Ora fine]**

La pianificazione delle sfide è ora configurata. Ora puoi aggiungere le attività che i clienti devono completare.

### Aggiungi attività {#add-tasks}

Le attività definiscono le azioni o i milestone specifici che i clienti devono completare per ottenere premi. Puoi configurare i tipi di attività (acquisto, spesa, visita, coinvolgimento, eventi personalizzati), le quantità, i filtri dei prodotti e i premi.

A seconda del tipo di sfida, i clienti completano le attività in modo diverso:

* **Sfide standard**: completa un numero specificato di attività in qualsiasi ordine
* **Sfide in streaming**: completa la stessa attività più volte consecutivamente
* **Sfide sequenziali**: attività completate in un ordine definito

Per aggiungere attività alla sfida, effettua le seguenti operazioni:

1. Nella sezione **[!UICONTROL Attività]**, seleziona **[!UICONTROL Aggiungi attività]**.

   ![](assets/challenge-create-add-task.png)

1. Viene aperto l&#39;inventario Attività. Selezionare una o più attività dall&#39;elenco e selezionare **[!UICONTROL Aggiungi]**. Per creare una nuova attività, selezionare **[!UICONTROL Nuova]**.

   Per istruzioni dettagliate sulla creazione e la configurazione delle attività, vedi [Creare le attività](create-tasks.md).

1. Nella sezione **[!UICONTROL Requisito completamento attività]**, specifica quando la richiesta di verifica deve essere considerata completata:

   * **[!UICONTROL Il cliente sceglie 1 attività da completare]**: il cliente può selezionare e completare qualsiasi singola attività dalla sfida per ottenere premi
   * **[!UICONTROL Il cliente completa un numero specifico di attività]**: il cliente deve completare un numero definito di attività. Immettere il numero richiesto di completamenti attività.

1. Per impostazione predefinita, le sfide consentono ai clienti di completare le attività in più transazioni. Per richiedere che tutte le attività vengano completate in una singola transazione, seleziona l&#39;icona ![](assets/do-not-localize/settings-icon.svg) **[!UICONTROL Impostazioni]** e attiva l&#39;opzione **[!UICONTROL Transazione singola]**.

   ![](assets/challenge-create-single-transaction.png)

### Configurare i premi {#rewards}

I premi sono i punti fedeltà o i vantaggi che i clienti ricevono per il completamento delle sfide. Configura come e quando vengono consegnati i premi per motivare la partecipazione dei clienti.

1. Nel menu a discesa **[!UICONTROL Consegna premi]**, scegli quando devono essere consegnati i premi:

   * **[!UICONTROL Distribuisci premi al completamento della sfida]**: assegna tutti i premi quando il cliente completa l&#39;intera sfida
   * **[!UICONTROL Distribuisci i premi alle attività cardine di completamento man mano che vengono completate le sfide]**: premi assegnati in modo incrementale man mano che i clienti completano le singole attività (disponibile solo quando la sfida richiede il completamento di più di un&#39;attività)

1. Seleziona il provider di premi dal menu a discesa. Questa è la soluzione di fidelizzazione che gestisce punti e premi del cliente.

1. Configura gli importi dei premi in base al metodo di consegna selezionato:

   +++Distribuisci premi al termine della sfida

   Nel campo **Numero di [punti fedeltà] al completamento della sfida**, specifica l&#39;importo totale del premio da assegnare quando il cliente completa l&#39;intera sfida.

   Il nome del campo visualizza il nome dei punti fedeltà come definito nel provider selezionato. Ad esempio, se il provider utilizza &quot;Punti Luma&quot;, il campo mostra &quot;Numero di punti Luma al completamento della sfida&quot;.

   ![](assets/challenge-create-reward-total.png)

   **Esempio**: nella schermata precedente, i clienti ricevono 100 punti al completamento della sfida.

   +++

   +++Distribuisci premi alle attività cardine di completamento

   Specificare gli importi dei premi per le attività cardine di completamento. Questa opzione ti consente di creare premi progressivi che aumentano la motivazione del cliente mentre progrediscono attraverso la sfida.

   Per qualsiasi attività per la quale si desidera assegnare un premio, attivare l&#39;opzione relativa al premio e specificare il numero di punti da assegnare quando i clienti completano l&#39;attività specifica. È possibile scegliere di premiare solo alcuni completamenti di attività, ad esempio, se si dispone di 10 attività, è possibile premiare solo le attività 1, 5 e 10.

   ![](assets/challenge-create-reward-milestones.png)

   **Esempio**: nella schermata precedente, i clienti ricevono 10 punti al completamento della prima attività e 50 punti aggiuntivi dopo il completamento della seconda attività, per un totale di 60 punti al completamento della sfida.

   >[!TIP]
   >
   >Valutare la possibilità di aumentare i premi per le attività successive per mantenere il coinvolgimento del cliente durante l&#39;intera sfida.

   +++

La struttura di sfida è ora configurata con attività e premi. Ora puoi progettare le schede di contenuto per presentare la sfida ai clienti.

## Configurare le schede di contenuto {#configure-content-cards}

Le schede di contenuto forniscono una rappresentazione visiva della sfida sui dispositivi dei clienti, visualizzando informazioni sulla sfida, lo stato di avanzamento e i premi. Ulteriori informazioni sulle [schede di contenuto](../content-card/create-content-card.md).

Per configurare le schede di contenuto per la sfida:

1. Nell&#39;editor delle richieste di verifica passare alla scheda **[!UICONTROL Contenuto]**.

1. Immetti un **[!UICONTROL Nome]** per la scheda di contenuto.

1. Seleziona la **[!UICONTROL configurazione canale]** associata. Le configurazioni di canale definiscono come e dove i contenuti vengono consegnati ai clienti. Per ulteriori informazioni, consulta [Configurazioni canale](../configuration/channel-surfaces.md).

1. Seleziona **[!UICONTROL Modifica contenuto]** per progettare la scheda dei contenuti.

   ![](assets/challenge-create-content.png)

Per ulteriori informazioni sulla progettazione e la personalizzazione delle schede di contenuto, vedere [Progettare le schede di contenuto](../content-card/design-content-card.md).

La scheda di contenuto è ora configurata. È ora possibile configurare la messaggistica per coinvolgere i clienti durante l&#39;intero ciclo di vita della sfida.

### Configurare la messaggistica {#configure-messaging}

Configurare messaggi multicanale per coinvolgere i clienti nelle fasi chiave del ciclo di vita della sfida.

1. Passa alla scheda **[!UICONTROL Messaggistica]**.

1. Configurare i messaggi per ogni fase del ciclo di vita:

   ![](assets/challenge-create-messaging.png)

   * **Messaggi di avvio**: avvisa i clienti quando inizia la verifica e fornisci i dettagli iniziali
   * **Messaggi in corso**: mantenere i clienti coinvolti durante la sfida con promemoria, aggiornamenti sull&#39;avanzamento e incoraggiamento a continuare
   * **Messaggi di completamento**: celebra il successo, conferma l&#39;allocazione delle ricompense e suggerisce le sfide o le azioni successive

1. Per ogni fase, selezionare **[!UICONTROL Aggiungi *fase* messaggio]** per creare un messaggio per quella fase.

1. Scegli il tuo canale desiderato: **[!UICONTROL In-app]**, **[!UICONTROL E-mail]** o **[!UICONTROL Notifica push]** e seleziona la configurazione del canale associata.

1. Seleziona l&#39;icona ![](assets/do-not-localize/Smock_More_18_N.svg) e scegli **[!UICONTROL Modifica]** per progettare il contenuto del messaggio.

   Per ulteriori informazioni sulla creazione di messaggi per canali specifici, consulta:

   * [Documentazione dei messaggi in-app](../in-app/get-started-in-app.md)
   * [Documentazione dei messaggi e-mail](../email/get-started-email.md)
   * [Documentazione delle notifiche push](../push/get-started-push.md)

1. Ripetere questi passaggi per ogni fase e canale, in base alle esigenze.

La configurazione della messaggistica è stata completata. Ora puoi definire quali clienti sono idonei a partecipare alla sfida.

## Seleziona il pubblico della sfida {#audience}

Definisci quali clienti sono idonei a partecipare alla sfida di fidelizzazione.

1. Passa alla scheda **[!UICONTROL Pubblico]** e fai clic sul pulsante **[!UICONTROL Seleziona pubblico]**.

   ![](assets/challenge-create-audience.png)

1. Vengono visualizzati tutti i tipi di pubblico di Adobe Experience Platform disponibili. Seleziona il pubblico desiderato dall’elenco.

1. Seleziona **[!UICONTROL Aggiungi pubblico]** per confermare la selezione.

La configurazione della sfida è stata completata. Ora puoi generare il percorso che orchestrerà la consegna della sfida.

## Generare e attivare il percorso {#review-and-publish}

Una volta completata la configurazione della sfida, genera il percorso associato che orchestrerà la consegna della sfida e le interazioni dei clienti. A tale scopo, selezionare **[!UICONTROL Genera Percorso]**.

![](assets/challenge-create-generate-journey.png)

Journey Optimizer crea automaticamente un [percorso](../building-journeys/journey-gs.md) in stato Bozza. Il percorso generato automaticamente viene visualizzato nell&#39;inventario del percorso con il formato del nome &quot;Sfida: [Nome sfida]&quot;.

Rivedi la configurazione del percorso se necessario, quindi [attiva il percorso](../building-journeys/publish-journey.md) per rendere la sfida disponibile ai clienti.

Il percorso inizierà automaticamente alla data di inizio della sfida specificata e distribuirà contenuti e messaggi in base alla configurazione.

>[!NOTE]
>
>Se necessario, il percorso generato automaticamente può essere personalizzato per aggiungere logica o messaggi aggiuntivi. Tuttavia, le modifiche apportate direttamente al percorso non vengono sincronizzate con la configurazione di verifica. Se si modifica la sfida in un secondo momento, tutte le personalizzazioni di percorso andranno perse durante la rigenerazione del percorso.

## Passaggi successivi {#next-steps}

* [Gestire le sfide](manage-challenges.md) - Scopri come modificare, monitorare e ottimizzare le sfide
* [Comprendere le sfide relative alla fedeltà](get-started.md) - Rivedere le funzionalità
