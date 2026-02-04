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
source-git-commit: e683461c6adbf45cacb30692e23927175685f9fb
workflow-type: tm+mt
source-wordcount: '1445'
ht-degree: 0%

---


# Creare le sfide {#create-challenges}

>[!BEGINSHADEBOX]

**Documentazione sulle sfide di fedeltà:**

* [Introduzione alle sfide di fidelizzazione](get-started.md) - Panoramica, flusso di lavoro, prerequisiti
* [Accesso e gestione delle sfide di fidelizzazione](access-loyalty-challenges.md) - Gestione di inventario, sfide e attività
* **Crea problemi** ◀︎ **Sei qui** - Genera e configura problemi
* [Crea attività](create-tasks.md) - Definisci le attività di verifica

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Questa funzionalità è attualmente in **versione beta privata** e potrebbe non essere disponibile nel tuo ambiente. Per richiedere l’accesso, contatta il rappresentante Adobe. Ulteriori informazioni sulle [etichette di disponibilità](../rn/releases.md#availability-labels).

## Crea la sfida {#create-the-challenge}

1. Passa a **[!UICONTROL Sfide fedeltà (Beta)]** in Journey Optimizer.

1. Seleziona la scheda **[!UICONTROL Sfide]** e seleziona **[!UICONTROL Crea sfida]**.

   ![](assets/challenge-create.png)

1. Scegli il tipo di sfida:

   * **[!UICONTROL Standard]**: i clienti completano un numero specificato di attività in qualsiasi ordine\
     *Esempio: completamento di 3 attività su 5 disponibili*

   * **[!UICONTROL Streak]**: i clienti completano la stessa attività più volte consecutivamente\
     *Esempio: effettuare un acquisto in 7 giorni consecutivi*

   * **[!UICONTROL Sequenziale]**: i clienti completano le attività in un ordine definito\
     *Esempio: acquistare → rivedere → condividere (deve essere completato in questa sequenza)*

## Configurare la struttura delle sfide {#structure}

Nella scheda **[!UICONTROL Struttura]**, definisci come è organizzata la sfida: proprietà, pianificazione, attività da completare e premi da consegnare.

### Definire le proprietà della sfida e utilizzare metadati personalizzati {#properties}

1. Nel riquadro **[!UICONTROL Proprietà verifica]**, definire le impostazioni globali per la verifica:

   * **[!UICONTROL Nome]**: immetti un nome descrittivo per la richiesta. Questo nome viene visualizzato nell&#39;inventario delle sfide.
   * **[!UICONTROL Descrizione]**: immetti una descrizione che spieghi lo scopo e gli obiettivi della sfida.

   ![](assets/challenge-create-properties.png)

1. Utilizza la sezione **[!UICONTROL Metadati personalizzati]** per aggiungere metadati personalizzati utilizzando coppie chiave/valore. Questi metadati possono essere utilizzati per il tracciamento o l’integrazione con sistemi esterni.

### Pianificare la sfida {#schedule}

Configura quando viene eseguita la richiesta di verifica selezionando l&#39;icona **[!UICONTROL Apri pianificazione]**:

![](assets/challenge-create-schedule.png)

* **[!UICONTROL Data e ora di inizio]**: imposta il momento in cui la sfida diventa disponibile per i clienti.
* **[!UICONTROL Data e ora di fine]**: imposta la scadenza della richiesta e non accetta più nuovi completamenti.
* **[!UICONTROL Fuso orario]**: per impostazione predefinita, la sfida utilizza il fuso orario locale del destinatario.
* **[!UICONTROL Le attività devono essere completate]**: scegli quando i clienti possono completare le attività:

   * **[!UICONTROL In qualsiasi momento durante la verifica]**: i clienti possono completare le attività in qualsiasi momento tra le date di inizio e di fine della verifica.
   * **[!UICONTROL In ore specifiche del giorno]**: limita il completamento dell&#39;attività a ore giornaliere specifiche impostando **[!UICONTROL Ora inizio]** e **[!UICONTROL Ora fine]**.

La pianificazione delle sfide è ora configurata. Quindi, aggiungi le attività che i clienti devono completare.

### Aggiungi attività {#add-tasks}

Le attività definiscono le azioni specifiche che i clienti devono completare per ottenere dei premi. Puoi configurare tipi di task (acquisto, spesa), quantità, filtri prodotto e altri attributi.

Per aggiungere attività alla sfida, effettua le seguenti operazioni:

1. Nella sezione **[!UICONTROL Attività]**, seleziona **[!UICONTROL Aggiungi attività]**.

   ![](assets/challenge-create-add-task.png)

1. Viene aperto **[!UICONTROL Inventario attività]**. Selezionare una o più attività dall&#39;elenco e selezionare **[!UICONTROL Aggiungi]**. Per creare una nuova attività, selezionare **[!UICONTROL Nuova]**. [Scopri come creare e configurare le attività](create-tasks.md).

1. Specifica quando la richiesta di verifica è considerata completata. Le impostazioni disponibili dipendono dal tipo di sfida:

   +++Sfide standard

   **[!UICONTROL Requisito completamento attività]** - Scegliere tra:

   * **[!UICONTROL Il cliente sceglie 1 attività da completare]**: i clienti possono selezionare e completare qualsiasi singola attività per ottenere premi
   * **[!UICONTROL Il cliente completa un numero specifico di attività]**: i clienti devono completare un numero definito di attività. Specifica il numero richiesto - *Esempio: completamento di 3 attività su 5*

   +++

   +++Sfide in streaming

   * **[!UICONTROL Tipo di flusso]**:

      * **Consecutivo**: i clienti devono completare l&#39;attività in giorni consecutivi senza pause - *Esempio: acquisto effettuato il lunedì, martedì, mercoledì - un giorno mancante interrompe la striscia*

      * **Non consecutivo**: i clienti possono completare l&#39;attività con intervalli tra i completamenti - *Esempio: completare 7 acquisti in 30 giorni, con pause consentite*

   * **[!UICONTROL Lunghezza flusso]**: specifica quante volte l&#39;attività deve essere completata - *Esempio: imposta su 7 per un &quot;flusso di acquisto di 7 giorni&quot;*

   +++

   +++Sfide sequenziali

   **[!UICONTROL Requisito completamento attività]** - Scegliere tra:

   * **[!UICONTROL Il cliente sceglie 1 attività da completare]**: i clienti possono selezionare e completare qualsiasi singola attività per ottenere premi
   * **[!UICONTROL Il cliente completa un numero specifico di attività]**: i clienti devono completare un numero definito di attività nell&#39;ordine esatto definito dall&#39;utente. Un&#39;attività mancante o ignorata interrompe la sequenza. Specifica il numero richiesto (ad esempio, completa 3 attività su 5)

   *Esempio: l&#39;attività 1 (acquisto) → l&#39;attività 2 (revisione) → l&#39;attività 3 (condivisione) - deve essere completata in questo ordine*

   +++

1. Per impostazione predefinita, le sfide standard e sequenziali consentono ai clienti di completare attività in più transazioni. Per richiedere che tutte le attività vengano completate in una singola transazione, seleziona l&#39;icona ![](assets/do-not-localize/settings-icon.svg) **[!UICONTROL Impostazioni]** e attiva l&#39;opzione seguente.

   ![](assets/challenge-create-single-transaction.png)

Dopo aver aggiunto le attività alla sfida, configura i premi che i clienti guadagneranno per completarle.

### Configurare i premi {#rewards}

I premi sono i punti fedeltà o i vantaggi che i clienti ricevono per il completamento delle sfide. Configura quando e come vengono consegnati i premi.

1. Nel menu a discesa **[!UICONTROL Consegna premi]**, scegli quando distribuire i premi:

   * **[!UICONTROL Distribuisci premi al completamento della sfida]**: Riconosci premi quando i clienti completano l&#39;intera sfida\
     *Esempio: assegna 100 punti dopo aver completato tutte e 5 le attività*

   * **[!UICONTROL Distribuisci premi alle fasi cardine di completamento dell&#39;attività man mano che l&#39;avanzamento della sfida viene completato]**: Riconosci premi in modo incrementale man mano che i clienti completano le singole attività (disponibile solo per le sfide che richiedono più di un&#39;attività)\
     *Esempio: assegna 10 punti dopo l&#39;attività 1, 20 punti dopo l&#39;attività 2 e 50 punti dopo l&#39;attività 3*

1. Selezionare il provider di premi. Questa è la soluzione di fidelizzazione che gestisce punti e premi del cliente.

1. Configura gli importi dei premi in base al metodo di consegna selezionato:

   +++Distribuisci premi al termine della sfida

   Specifica l&#39;importo totale del premio da assegnare quando i clienti completano l&#39;intera sfida.

   ![](assets/challenge-create-reward-total.png)

   **Esempio**: i clienti ricevono 100 punti al completamento della sfida.

   +++

   +++Distribuisci premi alle attività cardine di completamento

   Specificare gli importi dei premi per le attività cardine di completamento. Questa opzione ti consente di creare premi progressivi che aumentano la motivazione del cliente mentre progrediscono attraverso la sfida.

   Per qualsiasi attività per la quale si desidera assegnare un premio, attivare l&#39;opzione relativa al premio e specificare il numero di punti da assegnare quando i clienti completano l&#39;attività specifica. È possibile scegliere di premiare solo alcuni completamenti di attività, ad esempio, se si dispone di 10 attività, è possibile premiare solo le attività 1, 5 e 10.

   ![](assets/challenge-create-reward-milestones.png)

   **Esempio**: i clienti ricevono 10 punti al completamento della prima attività e 50 punti in più al completamento della seconda attività, per un totale di 60 punti al completamento della sfida.

   >[!TIP]
   >
   >Valutare la possibilità di aumentare i premi per le attività successive per mantenere il coinvolgimento del cliente durante l&#39;intera sfida.

   +++

Dopo aver configurato la struttura di sfida con attività e premi, progetta le schede di contenuto per mostrare la sfida ai clienti.

## Configurare le schede di contenuto {#configure-content-cards}

Le schede dei contenuti rappresentano visivamente la sfida sui dispositivi dei clienti, visualizzando informazioni sulla sfida, lo stato di avanzamento e i premi. [Ulteriori informazioni sulle schede dei contenuti](../content-card/create-content-card.md).

Per configurare le schede di contenuto per la sfida:

1. Passa alla scheda **[!UICONTROL Contenuto]** e immetti un **[!UICONTROL Nome]** per la scheda di contenuto.

1. Selezionare la **[!UICONTROL configurazione canale]**. Le configurazioni del canale contengono tutti i parametri tecnici per l’invio di messaggi, ad esempio parametri di intestazione, sottodominio, app mobili e così via. [Ulteriori informazioni sulle configurazioni dei canali](../configuration/channel-surfaces.md).

1. Seleziona **[!UICONTROL Modifica contenuto]** per progettare la scheda dei contenuti. [Scopri come progettare e personalizzare schede di contenuto](../content-card/design-content-card.md).

   ![](assets/challenge-create-content.png)

Dopo aver configurato la scheda di contenuti, imposta la messaggistica per coinvolgere i clienti durante l’intero ciclo di vita della sfida.

### Configurare la messaggistica {#configure-messaging}

Configurare messaggi multicanale per coinvolgere i clienti nelle fasi chiave del ciclo di vita della sfida. La messaggistica è facoltativa ma consigliata per massimizzare il coinvolgimento dei clienti.

1. Passa alla scheda **[!UICONTROL Messaggistica]** e configura i messaggi per ogni fase del ciclo di vita:

   * **Messaggio di avvio**: avvisa i clienti quando inizia la richiesta di verifica
   * **Messaggio in corso**: mantenere i clienti coinvolti con promemoria e aggiornamenti sull&#39;avanzamento
   * **Completamento** messaggio: celebra il successo e conferma l&#39;allocazione dei premi

1. Per ogni fase, selezionare **[!UICONTROL Aggiungi [fase] messaggio]** (dove [fase] rappresenta lancio, in corso o completamento) per creare un messaggio per quella fase.

1. Scegli il tuo canale desiderato: **[!UICONTROL In-app]**, **[!UICONTROL E-mail]** o **[!UICONTROL Notifica push]** e seleziona la configurazione del canale associata.

1. Seleziona l&#39;icona ![](assets/do-not-localize/Smock_More_18_N.svg) e scegli **[!UICONTROL Modifica]** per progettare il contenuto del messaggio.

   ![](assets/challenge-create-messaging.png)

Scopri come creare messaggi per canali specifici:

* [Messaggi in-app](../in-app/get-started-in-app.md)
* [Messaggi e-mail](../email/get-started-email.md)
* [Notifiche push](../push/get-started-push.md)

Dopo aver completato la configurazione di messaggistica, definisci quali clienti sono idonei a partecipare alla sfida.

## Seleziona il pubblico della sfida {#audience}

Definisci quali clienti possono partecipare alla sfida di fidelizzazione.

1. Passa alla scheda **[!UICONTROL Pubblico]** e seleziona il pulsante **[!UICONTROL Seleziona pubblico]**.

   ![](assets/challenge-create-audience.png)

1. Seleziona il pubblico di destinazione dall’elenco dei tipi di pubblico di Adobe Experience Platform disponibili. [Scopri come utilizzare i tipi di pubblico](../audience/about-audiences.md).

1. Seleziona **[!UICONTROL Aggiungi pubblico]**.

La sfida è ora completamente configurata con la sua struttura, il contenuto, la messaggistica e il pubblico di destinazione. Il passaggio finale consiste nel generare e pubblicare il percorso.

## Generare e pubblicare il percorso {#review-and-publish}

Genera il percorso che orchestrerà la consegna delle sfide e le interazioni dei clienti. A tale scopo, selezionare **[!UICONTROL Genera Percorso]**.

![](assets/challenge-create-generate-journey.png)

Journey Optimizer crea automaticamente un [percorso](../building-journeys/journey-gs.md) in stato Bozza. Il percorso generato automaticamente viene visualizzato nell&#39;inventario del percorso con il formato del nome &quot;Sfida: [Nome sfida]&quot;.

![](assets/challenge-create-journey.png)

Se necessario, rivedi la configurazione del percorso, quindi pubblica il percorso per rendere la sfida disponibile ai clienti. [Scopri come pubblicare un percorso](../building-journeys/publish-journey.md).

Il percorso inizierà automaticamente alla data di inizio della sfida specificata e distribuirà contenuti e messaggi in base alla configurazione.

>[!NOTE]
>
>Il percorso generato automaticamente può essere personalizzato per aggiungere logica o messaggi aggiuntivi. Tuttavia, le modifiche apportate direttamente al percorso non vengono sincronizzate con la configurazione di verifica. Se si modifica la sfida in un secondo momento, tutte le personalizzazioni di percorso andranno perse durante la rigenerazione del percorso.
