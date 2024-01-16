---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare un pubblico in un percorso
description: Scopri come utilizzare un pubblico in un percorso
feature: Journeys, Activities, Audiences
topic: Content Management
role: User
level: Intermediate
keywords: attività, percorso, lettura, pubblico, piattaforma
exl-id: 7b27d42e-3bfe-45ab-8a37-c55b231052ee
source-git-commit: d735f8c92466cb17a7364833950312e338c630cc
workflow-type: tm+mt
source-wordcount: '1398'
ht-degree: 10%

---

# Utilizzare un pubblico in un percorso {#segment-trigger-activity}

## Aggiungere un’attività Leggi pubblico {#about-segment-trigger-actvitiy}

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment"
>title="Attività Leggi pubblico"
>abstract="L’attività Leggi pubblico consente di fare in modo che tutti i singoli utenti appartenenti a un pubblico di Adobe Experience Platform entrino in un percorso. L’ingresso in un percorso può essere eseguito una volta o su base regolare."

Utilizza il **Read Audience** attività per fare in modo che tutti i singoli utenti di un pubblico entrino nel percorso. L’ingresso in un percorso può essere eseguito una volta o su base regolare.

Prendiamo ad esempio il pubblico &quot;Apertura e pagamento dell’app Luma&quot; creato in [Creare tipi di pubblico](../audience/about-audiences.md) caso d’uso. Con l’attività Read Audience, puoi fare in modo che tutti gli individui appartenenti a questo pubblico entrino in un percorso e li facciano confluire in percorsi personalizzati che sfrutteranno tutte le funzionalità del percorso: condizioni, timer, eventi, azioni.

## Da leggere {#must-read}

* Per i percorsi che utilizzano un’attività di Leggii pubblico esiste un numero massimo di percorsi che è possibile avviare contemporaneamente. I tentativi verranno eseguiti dal sistema, ma evita di disporre di più di cinque percorsi (con Leggi pubblico, programmato o che inizia “non appena possibile”) che si avviano nello stesso momento distribuendoli nel tempo, ad esempio a 5-10 minuti di distanza.

* I gruppi di campo di evento esperienza non possono essere utilizzati in percorsi che iniziano con un’attività Read audience, Audience Qualification o Business Event.

* Come best practice, consigliamo di utilizzare solo i tipi di pubblico in batch in una **Read audience** attività. Questo fornirà un conteggio affidabile e coerente per i tipi di pubblico utilizzati in un percorso. Read audience è progettato per i casi di utilizzo in batch. Se il tuo caso d’uso richiede dati in tempo reale, utilizza **[Qualificazione del pubblico](audience-qualification-events.md)** attività.

* Per il momento, l’utilizzo dei tipi di pubblico [importato da un file CSV](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html#import-audience) o derivanti da [flussi di lavoro di composizione](../audience/get-started-audience-orchestration.md) in percorsi è disponibile come versione beta privata. Per ulteriori informazioni, contatta il tuo rappresentante Adobe.

## Configurare l’attività {#configuring-segment-trigger-activity}

I passaggi per configurare l’attività Read Audience sono i seguenti:

1. Espandi la **[!UICONTROL Orchestrazione]** categoria e rilascia una **[!UICONTROL Read Audience]** attività nell’area di lavoro.

   L’attività deve essere posizionata come primo passaggio di un percorso.

1. Aggiungi un **[!UICONTROL Etichetta]** all’attività (facoltativo).

1. In **[!UICONTROL Pubblico]** , scegli il pubblico di Adobe Experience Platform che entrerà nel percorso, quindi fai clic su **[!UICONTROL Salva]**. Puoi selezionare qualsiasi pubblico Adobe Experience Platform generato utilizzando [definizioni dei segmenti](../audience/creating-a-segment-definition.md).

   >[!NOTE]
   >
   >Inoltre, puoi anche eseguire il targeting dei tipi di pubblico di Adobe Experience Platform creati utilizzando [composizioni di pubblico](../audience/get-started-audience-orchestration.md) o [caricato da un file CSV](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html#import-audience){target="_blank"}. Queste funzionalità sono attualmente disponibili come versione beta privata.

   Si noti che è possibile personalizzare le colonne visualizzate nell&#39;elenco e ordinarle.

   ![](assets/read-segment-selection.png)

   Una volta aggiunto il pubblico, il **[!UICONTROL Copia]** consente di copiarne nome e ID:

   `{"name":"Luma app opening and checkout","id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](assets/read-segment-copy.png)

   >[!NOTE]
   >
   >Solo i singoli utenti con **Realizzato** e **Esistente** gli stati di partecipazione del pubblico entreranno nel percorso. Per ulteriori informazioni su come valutare un pubblico, consulta [Documentazione del servizio di segmentazione](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target="_blank"}.

1. In **[!UICONTROL Namespace]** , scegli lo spazio dei nomi da utilizzare per identificare i singoli utenti. Per impostazione predefinita, il campo è precompilato con l’ultimo spazio dei nomi utilizzato. [Ulteriori informazioni sugli spazi dei nomi](../event/about-creating.md#select-the-namespace).

   >[!NOTE]
   >
   >Le persone appartenenti a un pubblico che non ha l’identità (spazio dei nomi) selezionata tra le loro diverse identità non possono entrare nel percorso. È possibile selezionare solo uno spazio dei nomi delle identità basato su persone. Se hai definito uno spazio dei nomi per una tabella di ricerca (ad esempio: Spazio dei nomi ProductID per una ricerca di prodotto), questo non sarà disponibile nella **Namespace** elenco a discesa.

1. Imposta il **[!UICONTROL Percentuale di lettura]**. Questo è il numero massimo di profili che possono entrare nel percorso al secondo. Questo tasso si applica solo a questa attività e non ad altre nel percorso. Per definire un tasso di limitazione sulle azioni personalizzate, ad esempio, devi utilizzare l’API di limitazione. Fai riferimento a questo [pagina](../configuration/throttling.md).

   Questo valore viene memorizzato nel payload della versione del percorso. Il valore predefinito è 5.000 profili al secondo. Puoi modificare questo valore da 500 a 20.000 profili al secondo.

   >[!NOTE]
   >
   >La velocità di lettura complessiva per sandbox è impostata su 20.000 profili al secondo. Pertanto, la velocità di lettura di tutti i tipi di pubblico di lettura eseguiti contemporaneamente nella stessa sandbox non supera i 20.000 profili al secondo. Non puoi modificare questo limite.

1. Il **[!UICONTROL Read Audience]** attività ti consente di specificare l’ora in cui il pubblico entrerà nel percorso. A questo scopo, fai clic su **[!UICONTROL Modifica pianificazione percorso]** per accedere alle proprietà del percorso, quindi configura il **[!UICONTROL Tipo di modulo di pianificazione]** campo.

   ![](assets/read-segment-schedule.png)

   Per impostazione predefinita, il pubblico entra nel percorso **[!UICONTROL Appena possibile]**. Se desideri che il pubblico entri nel percorso in una data/ora specifica o su base ricorrente, seleziona il valore desiderato dall’elenco.

   >[!NOTE]
   >
   >Tieni presente che **[!UICONTROL Pianificazione]** è disponibile solo quando un **[!UICONTROL Read Audience]** l&#39;attività è stata rilasciata nell&#39;area di lavoro.

   ![](assets/read-segment-schedule-list.png)

   **Lettura incrementale** opzione: quando un percorso con un **Read audience** viene eseguito per la prima volta, tutti i profili nel pubblico entrano nel percorso. Questa opzione consente di eseguire il targeting, dopo la prima occorrenza, solo delle persone che sono entrate nel pubblico dall’ultima esecuzione del percorso.

   **Forza rientro in caso di ricorrenza**: questa opzione ti consente di far uscire automaticamente tutti i profili ancora presenti nel percorso all’esecuzione successiva. Ad esempio, se attendi 2 percorsi in un giorno ricorrente giornaliero, attivando questa opzione i profili verranno sempre spostati all’esecuzione del percorso successivo (quindi il giorno successivo), indipendentemente dal fatto che si trovino o meno nel pubblico dell’esecuzione successiva. Se la durata dei profili in questo percorso può essere più lunga della frequenza di ricorrenza, non attivare questa opzione per assicurarsi che i profili possano terminare il percorso.

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
>I percorsi Read audience una tantum passano allo stato Finito 30 giorni dopo l’esecuzione del percorso. Per i tipi di pubblico di tipo Read pianificati, devono essere trascorsi 30 giorni dall’esecuzione dell’ultima occorrenza.

## Test e pubblicazione del percorso {#testing-publishing}

Il **[!UICONTROL Read Audience]** attività ti consente di testare il percorso su un profilo unitario.

A questo scopo, attiva la modalità di test.

![](assets/read-segment-test-mode.png)

Configura ed esegui la modalità di test normalmente. [Scopri come testare un percorso](testing-the-journey.md).

Una volta eseguito il test, il **[!UICONTROL Mostra registri]** consente di visualizzare i risultati del test. Per ulteriori informazioni, consulta [questa sezione](testing-the-journey.md#viewing_logs)

![](assets/read-segment-log.png)

Una volta completati i test, puoi pubblicare il percorso (vedi [Pubblicazione del percorso](publishing-the-journey.md)). Gli individui appartenenti al pubblico entreranno nel percorso alla data/ora specificata nelle proprietà del percorso **[!UICONTROL Scheduler]** sezione.

>[!NOTE]
>
>Per i percorsi ricorrenti basati su pubblico, il percorso si chiude automaticamente una volta eseguita la sua ultima occorrenza. Se non è stata specificata alcuna data/ora di fine, sarà necessario chiudere manualmente il percorso ai nuovi ingressi per terminarlo.

## Targeting del pubblico in percorsi basati sul pubblico

I percorsi basati sul pubblico iniziano sempre con **Read Audience** per recuperare singoli utenti appartenenti a un pubblico Adobe Experience Platform.

Il pubblico appartenente al pubblico viene recuperato una volta o su base regolare.

Dopo l’accesso al percorso, puoi creare casi di utilizzo di orchestrazione del pubblico, consentendo ai singoli utenti del pubblico iniziale di passare a settori diversi del percorso.

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

Questa esclusione può verificarsi subito dopo il recupero del pubblico, per scopi di conteggio della popolazione o lungo un percorso a più passaggi.

![](assets/read-segment-audience2.png)

**Unione**

I percorsi consentono di creare N rami e unirli dopo una segmentazione.

Di conseguenza, puoi fare in modo che due tipi di pubblico tornino a un’esperienza comune.

Ad esempio, dopo aver seguito un’esperienza diversa per dieci giorni di un percorso, i clienti VIP e non VIP possono tornare allo stesso percorso.

Dopo un’unione, puoi dividere nuovamente il pubblico eseguendo una segmentazione o un’esclusione.

![](assets/read-segment-audience3.png)
