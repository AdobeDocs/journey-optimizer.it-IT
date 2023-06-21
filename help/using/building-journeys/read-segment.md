---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare un segmento in un percorso
description: Scopri come utilizzare un segmento in un percorso
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: attività, percorso, lettura, segmento, piattaforma
exl-id: 7b27d42e-3bfe-45ab-8a37-c55b231052ee
source-git-commit: a278b217882f2646e106600e110226941e7e4f10
workflow-type: tm+mt
source-wordcount: '1337'
ht-degree: 12%

---

# Utilizzare un segmento in un percorso {#segment-trigger-activity}

## Aggiungere un’attività Leggi segmento {#about-segment-trigger-actvitiy}

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment"
>title="Attività Leggi segmento"
>abstract="L’attività Leggi segmento consente di fare in modo che tutti i singoli utenti appartenenti a un segmento Adobe Experience Platform entrino in un percorso. L’entrata in un percorso può essere eseguita una volta o su base regolare."

Utilizza il **Leggi segmento** attività per fare in modo che tutti i singoli utenti di un segmento entrino nel percorso. L’entrata in un percorso può essere eseguita una volta o su base regolare.

Prendiamo ad esempio il segmento &quot;Apertura e pagamento dell’app Luma&quot; creato in [Creare segmenti](../segment/about-segments.md) caso d’uso. Con l’attività Leggi segmento, puoi fare in modo che tutti gli individui appartenenti a questo segmento entrino in un percorso e li facciano confluire in percorsi personalizzati che sfrutteranno tutte le funzionalità del percorso: condizioni, timer, eventi, azioni.

>[!NOTE]
>
>Per i percorsi che utilizzano un’attività di lettura del segmento, esiste un numero massimo di percorsi che possono avviare contemporaneamente. I tentativi verranno eseguiti dal sistema, ma evita di disporre di più di cinque percorsi (con Leggi segmento, programmato o che inizia “non appena possibile”) che si avviano nello stesso momento distribuendoli nel tempo, ad esempio a 5-10 minuti di distanza.
>
>I gruppi di campo di evento esperienza non possono più essere utilizzati nei percorsi che iniziano con un’attività Leggi segmento, Qualificazione del segmento o Evento di business.

### Configurare l’attività {#configuring-segment-trigger-activity}

I passaggi per configurare l’attività Leggi segmento sono i seguenti:

1. Espandi la **[!UICONTROL Orchestrazione]** categoria e rilascia una **[!UICONTROL Leggi segmento]** attività nell’area di lavoro.

   L’attività deve essere posizionata come primo passaggio di un percorso.

1. Aggiungi un **[!UICONTROL Etichetta]** all’attività (facoltativo).

1. In **[!UICONTROL Segmento]** , scegli il segmento di Adobe Experience Platform che entrerà nel percorso, quindi fai clic su **[!UICONTROL Salva]**.

   Si noti che è possibile personalizzare le colonne visualizzate nell&#39;elenco e ordinarle.

   >[!NOTE]
   >
   >Solo i singoli utenti con **Realizzato** e **Esistente** gli stati di partecipazione al segmento entreranno nel percorso. Per ulteriori informazioni su come valutare un segmento, consulta [Documentazione del servizio di segmentazione](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target="_blank"}.

   ![](assets/read-segment-selection.png)

   Una volta aggiunto il segmento, il **[!UICONTROL Copia]** consente di copiarne nome e ID:

   `{"name":"Luma app opening and checkout",”id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](assets/read-segment-copy.png)

1. In **[!UICONTROL Namespace]** , scegli lo spazio dei nomi da utilizzare per identificare i singoli utenti. Per impostazione predefinita, il campo è precompilato con l’ultimo spazio dei nomi utilizzato. [Ulteriori informazioni sugli spazi dei nomi](../event/about-creating.md#select-the-namespace).

   >[!NOTE]
   >
   >Le persone appartenenti a un segmento che non ha l’identità (spazio dei nomi) selezionata tra le loro diverse identità non possono entrare nel percorso. È possibile selezionare solo uno spazio dei nomi delle identità basato su persone. Se hai definito uno spazio dei nomi per una tabella di ricerca (ad esempio: Spazio dei nomi ProductID per una ricerca di prodotto), questo non sarà disponibile nella **Namespace** elenco a discesa.

1. Imposta il **[!UICONTROL Tasso di limitazione]** al limite di velocità effettiva dell’attività Leggi segmento.

   Questo valore viene memorizzato nel payload della versione del percorso. Il valore predefinito è 5.000 messaggi al secondo. Puoi modificare questo valore da 500 a 20.000 messaggi al secondo.

   >[!NOTE]
   >
   >Il tasso di limitazione complessivo per sandbox è impostato su 20.000 messaggi al secondo. Di conseguenza, il tasso di limitazione di tutti i segmenti letti eseguiti contemporaneamente nella stessa sandbox non supera i 20.000 messaggi al secondo. Non puoi modificare questo limite.

1. Il **[!UICONTROL Leggi segmento]** attività ti consente di specificare l’ora in cui il segmento entrerà nel percorso. A questo scopo, fai clic su **[!UICONTROL Modifica pianificazione percorso]** per accedere alle proprietà del percorso.Quindi, configura il **[!UICONTROL Tipo di modulo di pianificazione]** campo.

   ![](assets/read-segment-schedule.png)

   Per impostazione predefinita, i segmenti entrano nel percorso **[!UICONTROL Appena possibile]**. Se desideri che il segmento entri nel percorso in una data/ora specifica o su base periodica, seleziona il valore desiderato dall’elenco.

   >[!NOTE]
   >
   >Tieni presente che **[!UICONTROL Pianificazione]** è disponibile solo quando un **[!UICONTROL Leggi segmento]** l&#39;attività è stata rilasciata nell&#39;area di lavoro.

   ![](assets/read-segment-schedule-list.png)

   Quando un percorso con una **Leggi segmento** viene eseguito per la prima volta, tutti i profili nel segmento entrano nel percorso. Utilizza il **Lettura incrementale** opzione per eseguire il targeting, dopo la prima occorrenza, solo delle persone che sono entrate nel segmento dall’ultima esecuzione del percorso.

   Abilitazione di **Forza rientro in caso di ricorrenza** consente di rimuovere automaticamente tutti i profili attualmente presenti nel percorso durante l’esecuzione successiva. Ad esempio, se si verifica un’attesa di 2 giorni in un percorso ricorrente giornaliero, l’attivazione di questa opzione sposterà in modo coerente i profili all’esecuzione successiva del percorso (il giorno successivo), indipendentemente dal fatto che facciano parte del pubblico dell’esecuzione successiva. Tuttavia, se la durata dei profili in questo percorso può superare la frequenza di ricorrenza, è consigliabile non abilitare questa opzione per garantire che i profili possano completare il percorso.

<!--

### Segment filters {#segment-filters}

[!CONTEXTUALHELP]
>id="jo_segment_filters"
>title="About segment filters"
>abstract="You can choose to target only the individuals who entered or exited a specific segment during a specific time window. For example, you can decide to only retrieve all the customers who entered the VIP segment since last week."

You can choose to target only the individuals who entered or exited a specific segment during a specific time window. For example, you can decide to only retrieve all the customers who entered the VIP segment since last week. Only the new VIP customers will be targeted. All the customers who were already part of the VIP segment before will be excluded.

To activate this mode, click the **Segment Filters** toggle. Two fields are displayed:

**Segment membership**: choose whether you want to listen to segment entrances or exits. 

**Lookback window**: define when you want to start to listen to entrances or exits. This lookback window is expressed in hours, starting from the moment the journey is triggered.  If you set this duration to 0, the journey will target all members of the segment. For recurring journeys, it will take into account all entrances/exits since the last time the journey was triggered.

-->

>[!NOTE]
>
>Una sola ripresa **Leggi segmento** I percorsi passano al **Completato** stato 30 giorni dopo l’esecuzione del percorso. Per programmato **Leggi segmenti**, sono trascorsi 30 giorni dall’esecuzione dell’ultima occorrenza.

### Test e pubblicazione del percorso {#testing-publishing}

Il **[!UICONTROL Leggi segmento]** L’attività ti consente di testare il percorso su un profilo unitario o su 100 profili di test casuali selezionati tra i profili qualificati per il segmento.

A questo scopo, attiva il **modalità di test**. Quindi, seleziona l’opzione desiderata dal riquadro a sinistra.

![](assets/read-segment-test-mode.png)

È quindi possibile configurare ed eseguire la **modalità di test** come al solito. [Scopri come testare un percorso](testing-the-journey.md).

Una volta eseguito il test, il **[!UICONTROL Mostra registri]** consente di visualizzare i risultati del test in base all’opzione di test selezionata:

* **[!UICONTROL Profilo singolo alla volta]**: i registri di test visualizzano le stesse informazioni visualizzate quando si utilizza la modalità di test unitaria. Per ulteriori informazioni al riguardo, consulta [questa sezione](testing-the-journey.md#viewing_logs)

* **[!UICONTROL Fino a 100 profili alla volta]**: i registri di test ti consentono di monitorare la progressione dell’esportazione del segmento da Adobe Experience Platform, nonché l’avanzamento individuale di tutte le persone che sono entrate nel percorso.

  Il test del percorso con un massimo di 100 profili alla volta non consente di monitorare l’avanzamento dei singoli utenti nel percorso utilizzando il flusso visivo.

  ![](assets/read-segment-log.png)

Una volta completati i test, puoi pubblicare il percorso (vedi [Pubblicazione del percorso](publishing-the-journey.md)). Le persone appartenenti al segmento entreranno nel percorso alla data/ora specificata nelle proprietà del percorso **[!UICONTROL Scheduler]** sezione.

>[!NOTE]
>
>Per i percorsi ricorrenti basati su segmenti, il percorso si chiude automaticamente una volta eseguita la sua ultima occorrenza. Se non è stata specificata alcuna data/ora di fine, sarà necessario chiudere manualmente il percorso ai nuovi ingressi per terminarlo.

## Targeting del pubblico in percorsi basati su segmenti

I percorsi basati su segmenti iniziano sempre con **Leggi segmento** per recuperare singoli utenti appartenenti a un segmento Adobe Experience Platform.

Il pubblico appartenente al segmento viene recuperato una volta o su base regolare.

Dopo aver inserito il percorso, puoi creare casi di utilizzo di orchestrazione del pubblico, consentendo ai singoli utenti del segmento iniziale di passare in rami diversi del percorso.

**Segmentazione**

È possibile utilizzare le condizioni per eseguire la segmentazione utilizzando **Condizione** attività. Ad esempio, è possibile fare in modo che le persone affette da VIP seguano un percorso particolare e che il flusso non-VIP segua un altro percorso.

La segmentazione può essere basata su:

* dati origine dati
* il contesto degli eventi fa parte dei dati del percorso, ad esempio: una persona ha fatto clic sul messaggio ricevuto un’ora fa?
* una data, ad esempio: siamo a giugno quando una persona passa attraverso il percorso?
* un’ora, ad esempio: è mattina nel fuso orario della persona?
* un algoritmo che divide il pubblico che scorre nel percorso in base a una percentuale, ad esempio: 90% - 10% per escludere un gruppo di controllo

![](assets/read-segment-audience1.png)

**Exclusion**

Uguale **Condizione** l’attività utilizzata per la segmentazione (vedi sopra) ti consente anche di escludere parte della popolazione. Ad esempio, puoi escludere le persone VIP facendole fluire in una filiale con una fase finale subito dopo.

Questa esclusione può verificarsi subito dopo il recupero del segmento, per scopi di conteggio delle popolazioni o lungo un percorso a più passaggi.

![](assets/read-segment-audience2.png)

**Unione**

I percorsi consentono di creare N rami e unirli dopo una segmentazione.

Di conseguenza, puoi fare in modo che due tipi di pubblico tornino a un’esperienza comune.

Ad esempio, dopo aver seguito un’esperienza diversa per dieci giorni di un percorso, i clienti VIP e non VIP possono tornare allo stesso percorso.

Dopo un’unione, puoi dividere nuovamente il pubblico eseguendo una segmentazione o un’esclusione.

![](assets/read-segment-audience3.png)
