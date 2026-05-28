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
feature_v2: []
subfeature_v2: []
source-git-commit: 2e01cd1880b8527911376d94188d0204f7649541
workflow-type: tm+mt
source-wordcount: 1973
ht-degree: 16%

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

Questa pagina descrive l’intero processo di creazione di una sfida di fidelizzazione, dalla selezione del tipo di sfida e la configurazione delle relative proprietà alla generazione e pubblicazione del percorso che fornirà la sfida ai clienti.

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

   * **[!UICONTROL Acquisisci i tuoi dati]**: seleziona **[!UICONTROL Acquisisci i tuoi dati]** quando desideri che il framework delle sfide, come attività e premi, venga assemblato dall&#39;integrazione dei dati delle sfide di fedeltà. Quando questo tipo è selezionato, non è necessario configurare la struttura di verifica, è sufficiente configurare **[!UICONTROL Contenuto]**, **[!UICONTROL Messaggistica]** e **[!UICONTROL Pubblico]** nello stesso modo delle altre verifiche.

     >[!AVAILABILITY]
     >
     >Il tipo di richiesta **[!UICONTROL Porta i tuoi dati]** è attualmente disponibile per un gruppo limitato di organizzazioni e sarà reso disponibile in modo più ampio in una versione futura.

   Dopo aver selezionato un tipo di sfida, viene visualizzata l’interfaccia per la creazione della sfida con più schede di configurazione. Per tutti i tipi ad eccezione di **[!UICONTROL Porta i tuoi dati]**, inizia configurando la struttura delle sfide.

## Configurare la struttura delle sfide {#structure}

Nella scheda **[!UICONTROL Struttura]**, definisci come è organizzata la sfida: proprietà, pianificazione, attività da completare e premi da consegnare.

### Definire le proprietà della sfida e utilizzare metadati personalizzati {#properties}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenge_properties"
>title="Proprietà della sfida"
>abstract="Nel riquadro Proprietà della sfida, imposta il nome e la descrizione della sfida e aggiungi metadati personalizzati chiave-valore per il tracciamento o le integrazioni esterne."

1. Nel riquadro **[!UICONTROL Proprietà verifica]**, definire le impostazioni globali per la verifica:

   * **[!UICONTROL Nome]**: immetti un nome descrittivo per la richiesta. Questo nome viene visualizzato nell&#39;inventario delle sfide.
   * **[!UICONTROL Descrizione]**: immetti una descrizione che spieghi lo scopo e gli obiettivi della sfida.

1. Utilizza la sezione **[!UICONTROL Metadati personalizzati]** per aggiungere metadati personalizzati utilizzando coppie chiave/valore. Questi metadati possono essere utilizzati per il tracciamento o l’integrazione con sistemi esterni.

   ![](assets/challenge-create-properties.png)

### Pianificare la sfida {#schedule}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenge_schedule"
>title="Pianificazione della sfida"
>abstract="Utilizza la pianificazione per stabilire quando attivare la sfida: imposta la data e l’ora di inizio in cui diventa disponibile per i clienti e la data e l’ora di fine per interrompere l’accettazione dei completamenti. Scegli un fuso orario e seleziona quando i clienti possono completare le attività nella **[!UICONTROL sezione Intervallo di completamento attività]**."

Configura quando viene eseguita la richiesta di verifica:

1. Seleziona l&#39;icona **[!UICONTROL Apri pianificazione]**:

   ![](assets/challenge-create-schedule.png)

1. Configura le seguenti opzioni di pianificazione:

   * **[!UICONTROL Data e ora di inizio]**: imposta il momento in cui la sfida diventa disponibile per i clienti.
   * **[!UICONTROL Data e ora di fine]**: imposta la scadenza della richiesta e non accetta più nuovi completamenti.
   * **[!UICONTROL Fuso orario]**: per impostazione predefinita, la sfida utilizza il fuso orario locale del destinatario.
   * **[!UICONTROL Le attività devono essere completate]**: scegli quando i clienti possono completare le attività:

      * **[!UICONTROL In qualsiasi momento durante la verifica]**: i clienti possono completare le attività in qualsiasi momento tra le date di inizio e di fine della verifica.
      * **[!UICONTROL In ore specifiche del giorno]**: limita il completamento dell&#39;attività a ore giornaliere specifiche impostando **[!UICONTROL Ora inizio]** e **[!UICONTROL Ora fine]**.

La pianificazione delle sfide è ora configurata. Quindi, aggiungi le attività che i clienti devono completare.

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

1. Per impostazione predefinita, le sfide standard e sequenziali consentono ai clienti di completare attività in più transazioni. Per richiedere che tutte le attività vengano completate in una singola transazione, seleziona l&#39;icona **[!UICONTROL Impostazioni]** e attiva l&#39;opzione seguente.

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

Dopo aver configurato la struttura di sfida con attività e premi, progetta le schede di contenuto per mostrare la sfida ai clienti.

## Configurare le schede di contenuto {#configure-content-cards}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenge_content"
>title="Contenuto"
>abstract="Configura la scheda dei contenuti che rappresenta la tua sfida sui dispositivi dei clienti e mostra le informazioni sulla sfida, l’avanzamento e i premi. Inserisci un nome per la scheda, seleziona una configurazione dei canali in modo che la consegna utilizzi le impostazioni tecniche corrette (ad esempio intestazioni, sottodominio o app mobili), quindi seleziona Modifica contenuto per progettare e personalizzare l’esperienza della scheda."

Le schede dei contenuti rappresentano visivamente la sfida sui dispositivi dei clienti, visualizzando informazioni sulla sfida, lo stato di avanzamento e i premi. [Ulteriori informazioni sulle schede dei contenuti](../content-card/create-content-card.md).

Per configurare le schede di contenuto per la sfida:

1. Passa alla scheda **[!UICONTROL Contenuto]** e immetti un **[!UICONTROL Nome]** per la scheda di contenuto.

1. Selezionare la **[!UICONTROL configurazione canale]**. Le configurazioni del canale contengono tutti i parametri tecnici per l&#39;invio di messaggi, ad esempio parametri di intestazione, sottodominio, app mobili e così via. [Ulteriori informazioni sulle configurazioni del canale](../configuration/channel-surfaces.md).

1. Seleziona **[!UICONTROL Modifica contenuto]** per progettare la scheda dei contenuti. [Scopri come progettare e personalizzare schede di contenuto](../content-card/design-content-card.md).

   ![](assets/challenge-create-content.png)

Dopo aver configurato la scheda di contenuti, imposta la messaggistica per coinvolgere i clienti durante l’intero ciclo di vita della sfida.

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

Dopo aver completato la configurazione di messaggistica, definisci quali clienti sono idonei a partecipare alla sfida.

## Selezionare il pubblico della sfida {#audience}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenge_audience"
>title="Pubblico"
>abstract="Nella scheda Pubblico, scegli chi può partecipare alla sfida selezionando i tipi di pubblico disponibili in Adobe Experience Platform."

Definisci quali clienti possono partecipare alla sfida di fidelizzazione.

1. Passa alla scheda **[!UICONTROL Pubblico]** e fai clic sul pulsante **[!UICONTROL Seleziona pubblico]**.

   ![](assets/challenge-create-audience.png)

1. Nella finestra di dialogo di selezione del pubblico, seleziona il pubblico di destinazione dall&#39;elenco dei tipi di pubblico di Adobe Experience Platform disponibili e seleziona **[!UICONTROL Aggiungi pubblico]**. [Scopri come utilizzare i tipi di pubblico](../audience/about-audiences.md).

La sfida è ora completamente configurata con la sua struttura, il contenuto, la messaggistica e il pubblico di destinazione. Per avviarlo, devi pubblicare la sfida e il percorso associato.

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
