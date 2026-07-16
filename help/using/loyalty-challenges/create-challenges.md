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
badge: label="Beta privata" type="Informative"
mini-toc-levels: 1
exl-id: c950bee8-4ea9-4b64-810d-91371e8b3e4c
source-git-commit: 43b78122a37fc6e8bcbcc3da12200bc2c0bcd7d4
workflow-type: tm+mt
source-wordcount: '2272'
ht-degree: 11%

---

# Creare le sfide {#create-challenges}

>[!BEGINSHADEBOX]

**Sommario**

[Introduzione alle sfide di fedeltà](get-started.md)

<table style="table-layout:fixed">
<tr style="border: 0;">
<td style="vertical-align:top;">

**Crea e gestisci le sfide**

* [Accesso e gestione di sfide e attività](access-loyalty-challenges.md)
* **Crea sfide** ◀︎ **Sei qui**
* [Creare le attività](create-tasks.md)
* [Monitorare le prestazioni della sfida fedeltà](loyalty-reporting.md)

</td>
<td style="vertical-align:top;">

**Configura e integra**

* [Configurare le sfide relative alla fedeltà](loyalty-admin.md)
* [Dati e set di dati sulla fedeltà](loyalty-data-and-datasets.md)
* [Riferimento API per le sfide di fedeltà](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

</td>
</tr>
</table>

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Questa funzionalità è attualmente in **versione beta privata**. Per informazioni dettagliate sul ciclo di rilascio e sulle fasi di disponibilità, consulta [Ciclo di rilascio di Journey Optimizer](../rn/releases.md).

Questa pagina descrive l’intero processo di creazione di una sfida di fidelizzazione, dalla selezione del tipo di sfida e la configurazione di impostazioni, struttura, contenuti e messaggi alla generazione e pubblicazione del percorso che offre la sfida ai clienti.

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

   * **[!UICONTROL Acquisisci i tuoi dati]**: seleziona **[!UICONTROL Acquisisci i tuoi dati]** quando desideri che il framework delle sfide, come attività e premi, venga assemblato dall&#39;integrazione dei dati delle sfide di fedeltà. Quando questo tipo è selezionato, la scheda **[!UICONTROL Struttura]** è di sola lettura. Configura **[!UICONTROL Impostazioni]**, **[!UICONTROL Contenuto]** e **[!UICONTROL Messaggistica]** allo stesso modo di altri tipi di verifica.

     >[!AVAILABILITY]
     >
     >Il tipo di richiesta **[!UICONTROL Porta i tuoi dati]** è attualmente disponibile per un gruppo limitato di organizzazioni e sarà reso disponibile in modo più ampio in una versione futura.

   Dopo aver selezionato un tipo di richiesta di verifica, l&#39;editor delle richieste di verifica si apre con le seguenti schede: **[!UICONTROL Impostazioni]**, **[!UICONTROL Struttura]**, **[!UICONTROL Contenuto]** e **[!UICONTROL Messaggistica]**. Inizia con **[!UICONTROL Impostazioni]** per definire dettagli, pubblico, pianificazione e regole della sfida. Quindi configura **[!UICONTROL Struttura]** (attività e premi) per tutti i tipi eccetto **[!UICONTROL Porta i tuoi dati]**.

## Configurare le impostazioni di verifica {#settings}

Nella scheda **[!UICONTROL Impostazioni]**, configura le proprietà a livello di sfida: chi può partecipare, quando viene eseguita la sfida, in che modo i membri acconsentono e ottengono l&#39;avanzamento e metadati facoltativi.

### Dettagli della sfida {#challenge-details}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenge_properties"
>title="Dettagli della sfida"
>abstract="Imposta il nome e la descrizione della sfida. L’ID della sfida viene assegnato automaticamente al momento della creazione della sfida e può essere copiato per l’utilizzo nell’API o nell’integrazione."

1. Nella sezione **[!UICONTROL Dettagli richiesta di verifica]**, definisci quanto segue:

   * **[!UICONTROL Nome]**: immetti un nome descrittivo per la richiesta. Questo nome viene visualizzato nell&#39;inventario delle sfide.
   * **[!UICONTROL ID sfida]**: un identificatore univoco assegnato al momento della creazione della sfida. Utilizza il controllo Copy per fare riferimento a questo ID nelle API o nei sistemi esterni.
   * **[!UICONTROL Descrizione]**: immetti una descrizione che spieghi lo scopo e gli obiettivi della sfida.

   ![](assets/challenge-create-details.png)

### Pubblico {#audience}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenge_audience"
>title="Pubblico"
>abstract="Scegli chi può partecipare alla sfida. Aggiungi un pubblico Adobe Experience Platform o lascia il pubblico vuoto in modo da considerare idonei tutti i membri del programma fedeltà. Facoltativamente, puoi richiedere che vengano completate altre sfide."

Definisci chi può partecipare alla tua sfida di fedeltà.

1. Nella sezione **[!UICONTROL Pubblico]**, seleziona **[!UICONTROL Aggiungi pubblico]** per limitare la sfida a un pubblico Adobe Experience Platform specifico. [Scopri come utilizzare i tipi di pubblico](../audience/about-audiences.md).

   ![](assets/challenge-create-audience.png)

1. In **[!UICONTROL Prerequisiti per la verifica]**, selezionare **[!UICONTROL Richiedi completamento della verifica]** per limitare l&#39;idoneità ai membri che hanno già completato una o più verifiche selezionate.

### Pianificazione {#schedule}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenge_schedule"
>title="Pianificazione della sfida"
>abstract="Specifica quando la sfida è attiva utilizzando la data e l’ora di inizio e di fine e un fuso orario. Nella finestra di completamento delle attività, scegli quando i clienti possono completare le attività durante il periodo della sfida."

Configura quando viene eseguita la richiesta di verifica:

1. Nella sezione **[!UICONTROL Pianifica]**, imposta:

   * **[!UICONTROL Data e ora di inizio]**: quando la sfida diventa disponibile per i clienti.
   * **[!UICONTROL Data e ora di fine]**: quando la richiesta scade e non accetta più nuovi completamenti.
   * **[!UICONTROL Fuso orario]**: il fuso orario utilizzato per la pianificazione della richiesta di verifica.

   ![](assets/challenge-create-schedule.png)

1. In **[!UICONTROL Finestra di completamento attività]**, scegli quando i clienti possono completare le attività:

   * **[!UICONTROL In qualsiasi momento durante la verifica]**: i clienti possono completare le attività in qualsiasi momento tra le date di inizio e di fine della verifica.
   * **[!UICONTROL In ore specifiche del giorno]**: limita il completamento dell&#39;attività a ore giornaliere specifiche impostando **[!UICONTROL Ora inizio]** e **[!UICONTROL Ora fine]**.

### Regole {#rules}

Configurare il consenso dei membri, il momento in cui l&#39;avanzamento dell&#39;attività viene conteggiato per la sfida e quante volte è possibile completare la sfida.

![](assets/challenge-create-rules.png)

* **[!UICONTROL Trigger consenso]**:

   * **[!UICONTROL Metodo Opt-in]**: scegli se i clienti si uniscono alla sfida manualmente o tramite un trigger di evento.
   * **[!UICONTROL Evento]**: per il consenso basato su eventi, selezionare l&#39;evento che attiva il consenso. Gli amministratori possono fare clic sul pulsante ![ingranaggio](assets/do-not-localize/settings-icon.svg) per creare una definizione di evento. [Scopri come configurare le definizioni degli eventi](loyalty-admin.md#event-definitions)

* **[!UICONTROL Avvia il tracciamento dell&#39;avanzamento]**:

   * **[!UICONTROL Avvio del tracciamento dell&#39;avanzamento dell&#39;attività]**: scegli quando i completamenti dell&#39;attività vengono conteggiati per l&#39;avanzamento della sfida. Ad esempio, selezionare **[!UICONTROL Quando inizia la verifica (dopo il consenso)]**, quindi l&#39;avanzamento inizia dopo il consenso del membro e la verifica è attiva.

     È possibile separare quando una sfida è visibile ai membri da quando viene tracciato l’avanzamento. Ad esempio, una scheda di sfida può apparire e accettare i consensi prima che i completamenti delle attività inizino a contare l&#39;avanzamento in una data successiva.

   * **[!UICONTROL Inizio]**: quando scegli un&#39;opzione di inizio personalizzata, imposta la data e l&#39;ora in cui inizia il tracciamento dell&#39;avanzamento.

* **[!UICONTROL Limiti di ripetizione]**:

   * **[!UICONTROL La sfida può essere completata]**: scegli se la sfida può essere completata una o più volte. Ad esempio, **[!UICONTROL Una volta]** o un numero definito di completamenti.

   * **[!UICONTROL Numero di operazioni completabili]**: quando la ripetizione è abilitata, specificare quante volte un membro può completare la richiesta di verifica.

* **[!UICONTROL Requisiti di completamento]** *(solo sfide standard)*:

   * **[!UICONTROL Completa in un&#39;unica transazione]**: se abilitata, i clienti devono completare tutte le attività all&#39;interno di una singola transazione. Se l&#39;opzione è disabilitata, le attività possono essere completate in transazioni separate.

### Metadati personalizzati {#custom-metadata}

Nella sezione **[!UICONTROL Metadati personalizzati]**, seleziona **[!UICONTROL Aggiungi coppia chiave/valore]** per aggiungere metadati personalizzati. Utilizza i metadati per il tracciamento o l’integrazione con sistemi esterni.

![](assets/challenge-create-metadata.png)

## Configurare la struttura delle sfide {#structure}

Nella scheda **[!UICONTROL Struttura]**, definisci le attività che i clienti devono completare e i premi che guadagnano. Questa scheda non viene utilizzata per **[!UICONTROL Inserire i dati]**.

### Aggiungi attività {#add-tasks}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenge_tasks"
>title="Attività"
>abstract="Seleziona le attività da eseguire per completare la sfida. Successivamente, configura le modalità di completamento della sfida: le opzioni disponibili dipendono dal tipo di sfida scelto (Standard, Serie o Sequenziale)."

Le attività definiscono le azioni specifiche che i clienti devono completare per ottenere dei premi. Puoi configurare tipi di task (acquisto, spesa o evento personalizzato), quantità, filtri prodotto e altri attributi.

Per aggiungere attività alla sfida, effettua le seguenti operazioni:

1. Nella sezione **[!UICONTROL Attività]**, seleziona **[!UICONTROL Aggiungi attività]**.

   ![](assets/challenge-create-add-task.png)

1. Viene aperto **[!UICONTROL Inventario attività]**. Selezionare una o più attività dall&#39;elenco e selezionare **[!UICONTROL Aggiungi]**. Per creare una nuova attività, selezionare **[!UICONTROL Nuova]**. [Scopri come creare e configurare le attività](create-tasks.md).

1. Specifica quando la richiesta di verifica è considerata completata. Le impostazioni disponibili dipendono dal tipo di sfida:

   +++Sfide standard

   Nel menu a discesa **[!UICONTROL Requisito completamento attività]**, scegli tra:

   * **[!UICONTROL Il cliente sceglie 1 attività da completare]** - *I clienti possono selezionare e completare qualsiasi attività per guadagnare premi*
   * **[!UICONTROL Il cliente completa un numero specifico di attività]** - *I clienti devono completare un numero definito di attività. Specificare il numero richiesto di attività da completare.*

   +++

   +++Sfide in streaming

   Nel menu a discesa **[!UICONTROL Tipo di flusso]**, scegli tra:

   * **Consecutivo**: i clienti devono completare l&#39;attività in giorni consecutivi senza interruzioni. *Esempio: l&#39;acquisto viene effettuato lunedì, martedì e mercoledì. Un giorno mancante interrompe la sequenza.*

   * **Non consecutivi**: i clienti possono completare l&#39;attività con intervalli tra i completamenti. *Esempio: completare 7 acquisti nell&#39;arco di 30 giorni, con pause consentite.*

   Nel campo **[!UICONTROL Lunghezza flusso]**, specifica quante volte l&#39;attività deve essere completata. *Esempio: impostare su 7 per una &quot;sequenza di acquisti di 7 giorni&quot;*.

   +++

   +++Sfide sequenziali

   Nel menu a discesa **[!UICONTROL Requisito completamento attività]**, scegli tra:

   * **[!UICONTROL Il cliente sceglie 1 attività da completare]** - *I clienti possono selezionare e completare qualsiasi attività per guadagnare premi*
   * **[!UICONTROL Il cliente completa un numero specifico di attività]** - *I clienti devono completare un numero definito di attività nell&#39;ordine esatto definito dall&#39;utente. Un&#39;attività mancante o ignorata interrompe la sequenza. Specifica il numero di attività richieste da completare*

   +++

1. Per impostazione predefinita, le sfide standard e sequenziali consentono ai clienti di completare attività in più transazioni. Per richiedere che tutti i task vengano completati in una singola transazione, aprire il menu delle opzioni dei task e attivare l&#39;opzione di transazione singola.

   ![](assets/challenge-create-single-transaction.png)

Dopo aver aggiunto le attività alla sfida, configura i premi che i clienti guadagneranno per completarle.

### Configurare i premi {#rewards}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenge_rewards"
>title="Premi"
>abstract="Scegli quando i clienti ottengono punti: al completamento dell’intera sfida oppure al raggiungimento di determinate milestone durante il progresso nelle attività. Seleziona il provider dei premi (la soluzione di fidelizzazione che gestisce punti e premi), quindi imposta gli importi: un totale unico per il completamento della sfida intera o valori per singola attività per le milestone, attivando i premi solo per le attività che prevedono un pagamento."

I premi sono i punti fedeltà o i vantaggi che i clienti ricevono per il completamento delle sfide.

Per configurare quando e come vengono distribuiti i premi:

1. Nel menu a discesa **[!UICONTROL Consegna premi]**, scegli quando distribuire i premi:

   * **[!UICONTROL Distribuisci premi al completamento della sfida]**: Riconosci premi quando i clienti completano l&#39;intera sfida\
     *Esempio: assegna 100 punti dopo aver completato tutte e 5 le attività*

   * **[!UICONTROL Distribuisci premi alle fasi cardine di completamento dell&#39;attività man mano che l&#39;avanzamento della sfida viene completato]**: Riconosci premi in modo incrementale man mano che i clienti completano le singole attività (disponibile solo per le sfide che richiedono più di un&#39;attività)\
     *Esempio: assegna 10 punti dopo l&#39;attività 1, 20 punti dopo l&#39;attività 2 e 50 punti dopo l&#39;attività 3*

1. Selezionare il provider di premi. Questa è la soluzione di fidelizzazione che gestisce punti e premi del cliente. I provider di premi vengono creati nel menu **[!UICONTROL Amministratore fedeltà]** prima che tu crei le sfide. [Scopri come configurare i provider di premi](loyalty-admin.md#reward-providers)

   ![](assets/challenge-create-reward-type.png)

1. Configura gli importi dei premi in base al metodo di consegna selezionato:

   +++Distribuisci premi al termine della sfida

   Specifica l&#39;importo totale del premio da assegnare quando i clienti completano l&#39;intera sfida.

   *Nell&#39;esempio seguente, i clienti ricevono 100 punti al completamento della sfida.*

   ![](assets/challenge-create-reward-total.png)

   +++

   +++Distribuisci premi alle attività cardine di completamento

   Specificare gli importi dei premi per le attività cardine di completamento. Questa opzione ti consente di creare premi progressivi che aumentano la motivazione del cliente mentre progrediscono attraverso la sfida.

   Per qualsiasi attività per la quale si desidera assegnare un premio, attivare l&#39;opzione relativa al premio e specificare il numero di punti da assegnare quando i clienti completano l&#39;attività specifica. È possibile scegliere di premiare solo alcuni completamenti di attività, ad esempio, se si dispone di 10 attività, è possibile premiare solo le attività 1, 5 e 10.

   *Nell&#39;esempio seguente, i clienti ricevono 10 punti quando completano la prima attività e 50 punti aggiuntivi dopo aver completato la seconda attività.*

   ![](assets/challenge-create-reward-milestones.png)

   +++

Dopo aver configurato la struttura della sfida con attività e premi, puoi facoltativamente configurare il modo in cui la sfida viene rappresentata ai clienti. Se non hai bisogno di contenuto di sfida, salta questo passaggio e procedi direttamente a [Configura messaggi](#configure-messaging).

## Configurare il contenuto della sfida (facoltativo) {#configure-content-cards}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenge_content"
>title="Contenuto"
>abstract="Configura in che modo la sfida viene rappresentata nelle posizioni in cui i membri fedeltà accedono alle sfide e ne tengono traccia dell’avanzamento. Utilizza l’azione Aggiungi per scegliere la scheda Contenuto per visualizzare un’esperienza in stile scheda o un’esperienza basata su codice per distribuire contenuti tramite un’implementazione personalizzata."

La scheda **[!UICONTROL Contenuto]** controlla come viene rappresentata la sfida nelle posizioni in cui i membri fedeltà accedono alle sfide e ne tengono traccia dell&#39;avanzamento.

Per configurare il contenuto della sfida:

1. Passa alla scheda **[!UICONTROL Contenuto]** e fai clic su **[!UICONTROL Aggiungi azione]**.

1. Scegli il tipo di azione:

   * **[!UICONTROL Scheda contenuto]**: visualizza la sfida come esperienza in stile scheda sui dispositivi del cliente. Seleziona una **[!UICONTROL configurazione canale]** e fai clic su **[!UICONTROL Modifica contenuto]** per progettare e personalizzare la scheda. [Ulteriori informazioni sulle schede dei contenuti](../content-card/create-content-card.md).
   * **[!UICONTROL Esperienza basata su codice]**: fornisce contenuti problematici tramite l&#39;implementazione personalizzata utilizzando il canale basato su codice di Journey Optimizer. Seleziona una **[!UICONTROL configurazione canale]** e fai clic su **[!UICONTROL Modifica contenuto]** per definire il contenuto. [Ulteriori informazioni sulle esperienze basate su codice](../code-based/create-code-based.md).

   ![](assets/challenge-create-content.png)

   Potete aggiungere più azioni per rappresentare la sfida su superfici diverse.

Dopo aver configurato il contenuto, imposta la messaggistica per coinvolgere i clienti durante l’intero ciclo di vita della sfida.

### Configurare la messaggistica {#configure-messaging}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenge_messaging"
>title="Messaggi"
>abstract="La messaggistica facilita il coinvolgimento durante l’intero ciclo di vita della sfida. Nella scheda Messaggistica, aggiungi i messaggi per ciascuna fase: Avvio (quando inizia la sfida), In corso (promemoria e aggiornamenti sull’avanzamento) e Completamento (per festeggiare il successo e confermare i premi). Per ciascuna fase, aggiungi un messaggio, scegli il canale, seleziona una configurazione dei canali, quindi seleziona Modifica per progettarne il contenuto."

Configurare messaggi multicanale per coinvolgere i clienti nelle fasi chiave del ciclo di vita della sfida. La messaggistica è facoltativa ma consigliata per massimizzare il coinvolgimento dei clienti.

1. Passa alla scheda **[!UICONTROL Messaggistica]** e configura i messaggi per ogni fase del ciclo di vita:

   * **Messaggio di avvio**: avvisa i clienti quando inizia la richiesta di verifica
   * **Messaggio in corso**: mantenere i clienti coinvolti con promemoria e aggiornamenti sull&#39;avanzamento
   * **Completamento** messaggio: celebra il successo e conferma l&#39;allocazione dei premi

1. Per ogni fase, fai clic sul pulsante Aggiungi messaggio per creare un messaggio per quella fase.

1. Scegli il tuo canale desiderato: **[!UICONTROL In-app]**, **[!UICONTROL E-mail]** o **[!UICONTROL Notifica push]** e seleziona la configurazione del canale associata.

1. Seleziona l&#39;icona ![](assets/do-not-localize/Smock_More_18_N.svg) e scegli **[!UICONTROL Modifica]** per progettare il contenuto del messaggio.

   ![](assets/challenge-create-messaging.png)

Scopri come creare messaggi per canali specifici nelle seguenti sezioni: [Messaggi in-app](../in-app/get-started-in-app.md) - [Messaggi e-mail](../email/get-started-email.md) - [Notifiche push](../push/get-started-push.md)

La sfida è ora completamente configurata con le relative impostazioni, struttura, contenuti e messaggi. Per avviarlo, devi pubblicare la sfida e il percorso associato.

## Lancio della sfida {#launch}

L&#39;avvio di una sfida richiede **tre passaggi**: (1) pubblicare la sfida, (2) generare il percorso, (3) pubblicare il percorso. Tutti e tre devono essere completati per consegnare la sfida ai clienti.

1. Esamina la configurazione della sfida per assicurarti che tutti i campi obbligatori siano completati.

1. Fai clic sull&#39;icona ![](assets/do-not-localize/Smock_More_18_N.svg) e seleziona **[!UICONTROL Pubblica]**.

   ![](assets/challenge-create-publish.png)

1. Seleziona **[!UICONTROL Genera Percorso]** per creare il percorso che orchestrerà la consegna delle richieste.

   ![](assets/challenge-create-generate-journey.png)

1. Journey Optimizer crea automaticamente un percorso in stato &quot;Bozza&quot;. Il percorso viene visualizzato nell&#39;inventario dei percorsi con il formato nome *&quot;Percorso: [Nome richiesta di verifica]&quot;*. [Ulteriori informazioni sull&#39;inventario dei percorsi](../building-journeys/journey-ui.md).

   ![](assets/challenge-create-journey.png)

1. Apri il percorso e pubblicalo. Il percorso inizierà automaticamente alla data di inizio della sfida specificata e distribuirà contenuti e messaggi in base alla configurazione. [Scopri come pubblicare un percorso](../building-journeys/publish-journey.md).

1. Una volta che la sfida è attiva, monitora i KPI del programma, i risultati della sfida e le metriche a livello di attività nei [rapporti sulle sfide di fedeltà](loyalty-reporting.md). Puoi anche monitorare la consegna dei messaggi nel [rapporto percorso](../reports/journey-global-report-cja.md).

>[!NOTE]
>
>Il percorso generato automaticamente può essere personalizzato per aggiungere logica o messaggi aggiuntivi. Tuttavia, le modifiche apportate direttamente al percorso non vengono sincronizzate con la configurazione di verifica. Se si modifica la sfida in un secondo momento, tutte le personalizzazioni di percorso andranno perse durante la rigenerazione del percorso.
