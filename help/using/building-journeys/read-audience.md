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
version: Journey Orchestration
source-git-commit: 5eddbb1f9ab53f1666ccd8518785677018e10f6f
workflow-type: tm+mt
source-wordcount: '2461'
ht-degree: 13%

---

# Utilizzare un pubblico in un percorso {#segment-trigger-activity}

## Informazioni sull’attività Leggi pubblico {#about-segment-trigger-actvitiy}

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment"
>title="Attività Leggi pubblico"
>abstract="L’attività Leggi pubblico consente di fare in modo che tutti i singoli utenti appartenenti a un pubblico di Adobe Experience Platform entrino in un percorso. L’ingresso in un percorso può essere eseguito una volta o su base regolare."

Utilizza l&#39;attività **Read Audience** per fare in modo che tutti i singoli utenti di un pubblico entrino nel percorso. L’ingresso in un percorso può essere eseguito una volta o su base regolare.

Prendiamo ad esempio il pubblico &quot;Apertura e pagamento dell’app Luma&quot; creato nel caso d’uso [Genera tipi di pubblico](../audience/about-audiences.md). Con l’attività Read Audience, puoi fare in modo che tutti gli individui appartenenti a questo pubblico entrino in un percorso e li facciano confluire in percorsi personalizzati che sfrutteranno tutte le funzionalità del percorso: condizioni, timer, eventi, azioni.

➡️ [Scopri questa funzione nel video](#video)

>[!NOTE]
>
>Quando viene eseguita un&#39;attività Read Audience, il sistema genera eventi interni (denominati `segmentExportJob` eventi) per tenere traccia del ciclo di vita dell&#39;operazione di esportazione del pubblico. Questi eventi vengono registrati a livello di attività, non per singolo profilo, e possono essere interrogati a scopo di monitoraggio e risoluzione dei problemi. Ulteriori informazioni su [query sugli eventi Read Audience](../reports/query-examples.md#read-segment-queries).

>[!CAUTION]
>
>* Prima di iniziare a utilizzare l&#39;attività Read audience, [leggi i guardrail e le limitazioni](#must-read).

## Configurare l’attività {#configuring-segment-trigger-activity}

Di seguito sono riportati i passaggi per configurare l’attività Read Audience.

### Aggiungere un’attività Read audience e selezionare il pubblico

1. Espandi la categoria **[!UICONTROL Orchestrazione]** e rilascia un&#39;attività **[!UICONTROL Read Audience]** nell&#39;area di lavoro.

   L’attività deve essere posizionata come primo passaggio di un percorso.

1. Aggiungi un&#39;etichetta **[!UICONTROL Label]** all&#39;attività (facoltativo).

1. Nel campo **[!UICONTROL Pubblico]**, scegli il pubblico di Adobe Experience Platform che entrerà nel percorso, quindi fai clic su **[!UICONTROL Salva]**. Puoi selezionare qualsiasi pubblico Adobe Experience Platform generato utilizzando [definizioni di segmenti](../audience/creating-a-segment-definition.md).

   >[!NOTE]
   >
   >Inoltre, puoi anche eseguire il targeting dei tipi di pubblico di Adobe Experience Platform creati utilizzando [composizioni di pubblico](../audience/get-started-audience-orchestration.md) o [caricati da un file CSV](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=it#import-audience){target="_blank"}.

   Si noti che è possibile personalizzare le colonne visualizzate nell&#39;elenco e ordinarle.

   ![](assets/read-segment-selection.png)

   Una volta aggiunto il pubblico, il pulsante **[!UICONTROL Copia]** ti consente di copiarne il nome e l&#39;ID:

   `{"name":"Luma app opening and checkout","id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](assets/read-segment-copy.png)

   >[!NOTE]
   >
   >Solo i singoli utenti con lo stato di partecipazione al pubblico **Realizzato** entreranno nel percorso. Per ulteriori informazioni su come valutare un pubblico, consulta la [documentazione del servizio di segmentazione](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=it#interpret-segment-results){target="_blank"}.

1. Nel campo **[!UICONTROL Spazio dei nomi]**, scegli lo spazio dei nomi da utilizzare per identificare i singoli utenti. Per impostazione predefinita, il campo è precompilato con l’ultimo spazio dei nomi utilizzato. [Ulteriori informazioni sugli spazi dei nomi](../event/about-creating.md#select-the-namespace).

   >[!NOTE]
   >
   >Le persone appartenenti a un pubblico che non ha l’identità (spazio dei nomi) selezionata tra le loro diverse identità non possono entrare nel percorso. È possibile selezionare solo uno spazio dei nomi delle identità basato su persone. Se è stato definito uno spazio dei nomi per una tabella di ricerca (ad esempio, Spazio dei nomi ProductID per una ricerca di prodotti), questo non sarà disponibile nell&#39;elenco a discesa **Spazio dei nomi**.

### Guardrail e consigli {#must-read}

* Solo un&#39;attività **[!UICONTROL Read Audience]** può essere utilizzata in un percorso e deve essere la prima attività nell&#39;area di lavoro.

* L&#39;attività **[!UICONTROL Read audience]** può essere indirizzata a un solo pubblico. Se sono necessari più tipi di pubblico, è consigliabile unirli in un unico pubblico prima dell’uso. [Scopri come combinare i tipi di pubblico utilizzando i flussi di lavoro di composizione](../audience/get-started-audience-orchestration.md)

* Per i percorsi che utilizzano un’attività **Leggi pubblico** esiste un numero massimo di percorsi che è possibile avviare contemporaneamente. I tentativi verranno eseguiti dal sistema, ma evita di avere più di cinque percorsi (con **Read Audience**, pianificato o che inizia &quot;non appena possibile&quot;) a partire nello stesso momento. Si consiglia di distribuirli nel tempo, ad esempio a 5-10 minuti di distanza.

* I gruppi di campo di evento esperienza non possono essere utilizzati in percorsi che iniziano con un&#39;attività **Read audience**, **[Audience qualification](audience-qualification-events.md)** o un&#39;attività di evento business.

* Come best practice, consigliamo di utilizzare solo tipi di pubblico in batch in un&#39;attività **Read audience**. Questo fornirà un conteggio affidabile e coerente per i tipi di pubblico utilizzati in un percorso. Read audience è progettato per i casi di utilizzo in batch. Se il tuo caso d&#39;uso richiede dati in tempo reale, utilizza l&#39;attività **[Qualificazione del pubblico](audience-qualification-events.md)**.

* I tipi di pubblico [importati da un file CSV](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=it#import-audience) o risultanti da [flussi di lavoro di composizione](../audience/get-started-audience-orchestration.md) possono essere selezionati nell&#39;attività **Read Audience**. Questi tipi di pubblico non sono disponibili nell&#39;attività **Qualificazione del pubblico**.

* Limite simultaneo pubblico di lettura per organizzazione: ogni organizzazione può eseguire fino a cinque istanze Read Audience simultaneamente. Sono incluse sia le esecuzioni pianificate che quelle attivate da eventi aziendali, su tutte le sandbox e i percorsi. Questo limite viene applicato per garantire un’allocazione equa ed equilibrata delle risorse in tutte le organizzazioni.

* Gestione della velocità effettiva delle sandbox: il sistema gestisce in modo dinamico la velocità effettiva di elaborazione per sandbox con un limite massimo di 20.000 profili al secondo condivisi tra tutte le attività Read Audience. È possibile configurare singole attività Read Audience con una frequenza minima di 500 profili al secondo. I processi possono essere messi in coda se vengono raggiunti i limiti di velocità effettiva a livello di sandbox per garantire un’allocazione equa delle risorse.

* Timeout di elaborazione del processo: i processi di lettura del pubblico che non possono essere elaborati entro 12 ore a causa dei limiti di guardrail verranno automaticamente puliti e non verranno mai eseguiti. Ciò impedisce l&#39;accumulo di posti di lavoro e garantisce la stabilità del sistema.

* Quando utilizzi i segmenti batch, assicurati che l’acquisizione e gli aggiornamenti giornalieri delle istantanee vengano completati ben prima dell’inizio del percorso. Considera un periodo di attesa aggiuntivo se i segmenti devono riflettere i dati acquisiti nello stesso giorno. Se l’aggiornamento immediato del profilo è fondamentale, è consigliabile utilizzare un caso di utilizzo basato su eventi o in streaming invece di un approccio batch giornaliero, oppure inserire un meccanismo di attesa aggiuntivo per consentire la propagazione dei dati aggiornati prima della valutazione del percorso.



I guardrail relativi all&#39;attività **Read Audience** sono elencati in [questa pagina](../start/guardrails.md#read-segment-g).


>[!CAUTION]
>
>[I guardrail per i dati e la segmentazione del profilo cliente in tempo reale](https://experienceleague.adobe.com/docs/experience-platform/profile/guardrails.html?lang=it){target="_blank"} vengono applicati anche a Adobe Journey Optimizer.


### Gestire la voce dei profili nel percorso

Imposta la **[!UICONTROL velocità di lettura]**. Questo è il numero massimo di profili che possono entrare nel percorso al secondo. Questo tasso si applica solo a questa attività e non ad altre nel percorso. Per definire un tasso di limitazione sulle azioni personalizzate, ad esempio, devi utilizzare l’API di limitazione. Consulta [questa pagina](../configuration/throttling.md).

Questo valore viene memorizzato nel payload della versione del percorso. Il valore predefinito è 5.000 profili al secondo. Puoi modificare questo valore da 500 a 20.000 profili al secondo.

>[!NOTE]
>
>La velocità di lettura complessiva per sandbox è impostata su 20.000 profili al secondo. Pertanto, la velocità di lettura di tutti i tipi di pubblico di lettura eseguiti contemporaneamente nella stessa sandbox non supera i 20.000 profili al secondo. Non puoi modificare questo limite. Ulteriori informazioni sulle velocità di elaborazione e la velocità effettiva del percorso in [questa sezione](entry-management.md#journey-processing-rate).

### Pianifica il percorso {#schedule}

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_scheduler_start_date"
>title="Data/ora di inizio"
>abstract="Definisci la data e l’ora in cui desideri attivare questo percorso."

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_scheduler_repeat_until"
>title="Ripeti fino a"
>abstract="Definisci la data di fine della ricorrenza."

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_scheduler_repeat_every"
>title="Ripeti ogni"
>abstract="Definisci la frequenza per il modulo di pianificazione ricorrente."

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_scheduler_incremental_read"
>title="Lettura incrementale"
>abstract="Consenti l’ingresso nel percorso solo ai nuovi profili rispetto all’ultima lettura."

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_scheduler_force_reentrance"
>title="Forza reingresso"
>abstract="Rilascia tutti i partecipanti al percorso prima della lettura di ciascun pubblico."

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_scheduler_synchronize_audience"
>title="Attiva dopo la valutazione del pubblico in batch"
>abstract="Utilizza questa opzione per attivare l’esecuzione del percorso dopo una nuova valutazione del pubblico in batch."

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_scheduler_synchronize_audience_wait_time"
>title="Tempo di attesa per una nuova valutazione del pubblico"
>abstract="Specifica la durata di attesa del percorso per la nuova valutazione del pubblico in batch. Il periodo di attesa è limitato a valori interi, può essere specificato in minuti o ore e deve essere compreso tra 1 e 6 ore."

Per impostazione predefinita, il percorso è configurato per essere eseguito una sola volta. Per definire una data, un&#39;ora e una frequenza specifiche per l&#39;esecuzione del percorso, effettuare le seguenti operazioni.

>[!NOTE]
>
>I percorsi Read audience univoci passano allo stato **Finished** 91 percorsi ([timeout globale del percorso](journey-properties.md#global_timeout)) dopo l&#39;esecuzione. Per i tipi di pubblico di tipo Read pianificati, devono essere trascorsi 91 giorni dall’esecuzione dell’ultima occorrenza.

1. Nelle proprietà dell&#39;attività **[!UICONTROL Read audience]**, pa,e seleziona **[!UICONTROL Modifica pianificazione percorso]**.

   ![](assets/read-segment-schedule.png)

1. Vengono visualizzate le proprietà del percorso. Nell&#39;elenco a discesa **[!UICONTROL Tipo modulo di pianificazione]** selezionare la frequenza di esecuzione del percorso.

   ![](assets/read-segment-schedule-list.png)

Per i percorsi ricorrenti, sono disponibili opzioni specifiche per aiutarti a gestire l’immissione di profili nel percorso. Per ulteriori informazioni su ciascuna opzione, espandi le sezioni seguenti.

![](assets/read-audience-options.png)

+++**[!UICONTROL Lettura incrementale]**

Quando viene eseguito per la prima volta un percorso con un pubblico ricorrente di tipo **Lettura**, tutti i profili del pubblico entrano nel percorso.

Questa opzione consente di eseguire il targeting, dopo la prima occorrenza, solo delle persone che sono entrate nel pubblico dall’ultima esecuzione del percorso.

>[!NOTE]
>
>Se nel tuo percorso esegui il targeting di un pubblico di [caricamento personalizzato](../audience/about-audiences.md#segments-in-journey-optimizer), i profili vengono recuperati solo alla prima ricorrenza se questa opzione è abilitata in un percorso ricorrente, in quanto questi tipi di pubblico sono fissi.

+++

+++**[!UICONTROL Forza il rientro in caso di ricorrenza]**

Questa opzione ti consente di far sì che tutti i profili ancora presenti nel percorso lo abbandonino automaticamente all’esecuzione successiva.

Ad esempio, se attendi 2 percorsi in un giorno ricorrente giornaliero, attivando questa opzione i profili verranno sempre spostati all’esecuzione del percorso successivo (quindi il giorno successivo), indipendentemente dal fatto che si trovino o meno nel pubblico dell’esecuzione successiva.

Se la durata dei profili in questo percorso può essere più lunga della frequenza di ricorrenza, non attivare questa opzione per assicurarsi che i profili possano terminare il percorso.

+++

+++**[!UICONTROL Attiva dopo la valutazione del pubblico in batch]**

Per i percorsi pianificati giornalmente e per il targeting dei tipi di pubblico in blocco, puoi definire un intervallo di tempo fino a 6 ore affinché il percorso attenda nuovi dati sul pubblico dai processi di segmentazione in blocco. Se il processo di segmentazione viene completato entro l’intervallo di tempo, il percorso si attiva. In caso contrario, ignora il percorso fino alla sua occorrenza successiva. Questa opzione assicura che i percorsi vengano eseguiti con dati accurati e aggiornati sul pubblico.

Se, ad esempio, un percorso è pianificato per le 18.00, è possibile specificare un numero di minuti o di ore di attesa prima dell&#39;esecuzione del percorso. Quando il percorso si sveglia alle 18, verifica la presenza di un nuovo pubblico, ovvero un pubblico più recente di quello utilizzato nell’esecuzione del percorso precedente. Durante l’intervallo di tempo specificato, il percorso viene eseguito immediatamente dopo aver rilevato il nuovo pubblico. Tuttavia, se non viene rilevato alcun nuovo pubblico, l’esecuzione del percorso viene ignorata.

**Periodo di look-back per percorsi di lettura incrementali**

Quando **[!UICONTROL Trigger dopo la valutazione del pubblico in batch]** è selezionato, [!DNL Journey Optimizer] cerca una nuova valutazione del pubblico. Per il punto iniziale del periodo di look-back, viene utilizzata l’ora dell’ultima esecuzione riuscita del percorso, anche se si è verificata più di 24 ore fa. Ciò è significativo per i percorsi di lettura incrementali che in genere hanno un periodo di look-back di 24 ore.

Esempi di percorsi di lettura incrementali giornalieri:

* Con &quot;Trigger dopo valutazione del pubblico in batch&quot; attivo: se sono trascorsi tre giorni dall’ingresso dei profili incrementali nel percorso, il periodo di look-back si estenderebbe di tre giorni alla ricerca dei profili incrementali.
* Con &quot;Trigger dopo valutazione del pubblico in batch&quot; non attivo: se sono trascorsi tre giorni da quando i profili incrementali sono entrati nel percorso, il periodo di look-back torna indietro solo di 24 ore quando si cercano profili incrementali.

+++

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

## Test e pubblicazione del percorso {#testing-publishing}

L&#39;attività **[!UICONTROL Read Audience]** ti consente di testare il percorso su un profilo unitario.

A questo scopo, attiva la modalità di test.

![](assets/read-segment-test-mode.png)

Configura ed esegui la modalità di test normalmente. [Scopri come verificare un percorso](testing-the-journey.md).

Quando il test è in esecuzione, il pulsante **[!UICONTROL Mostra registri]** consente di visualizzare i risultati del test. Per ulteriori informazioni, consulta [questa sezione](testing-the-journey.md#viewing_logs)

![](assets/read-segment-log.png)

Una volta completati i test, puoi pubblicare il percorso (vedi [Pubblicazione del percorso](publishing-the-journey.md)). Gli utenti appartenenti al pubblico entreranno nel percorso alla data/ora specificata nella sezione **[!UICONTROL Scheduler]** delle proprietà del percorso.

>[!NOTE]
>
>Per i percorsi ricorrenti basati su pubblico, il percorso si chiude automaticamente una volta eseguita la sua ultima occorrenza. Se non è stata specificata alcuna data/ora di fine, sarà necessario chiudere manualmente il percorso ai nuovi ingressi per terminarlo.

## Targeting del pubblico in percorsi basati sul pubblico

I percorsi basati sul pubblico iniziano sempre con un&#39;attività **Read Audience** per recuperare gli individui appartenenti a un pubblico Adobe Experience Platform.

Il pubblico appartenente al pubblico viene recuperato una volta o su base regolare.

Dopo l’accesso al percorso, puoi creare casi di utilizzo di orchestrazione del pubblico, consentendo ai singoli utenti del pubblico iniziale di passare a settori diversi del percorso.

**Segmentazione**

È possibile utilizzare le condizioni per eseguire la segmentazione utilizzando l&#39;attività **Condition**. Ad esempio, puoi fare in modo che le persone VIP seguano un particolare percorso e un flusso non VIP in un altro percorso.

La segmentazione può essere basata su:

* dati origine dati
* il contesto degli eventi fa parte dei dati del percorso, ad esempio: una persona ha fatto clic sul messaggio ricevuto un’ora fa?
* una data, ad esempio: siamo a giugno quando una persona passa attraverso il percorso?
* un’ora, ad esempio: è mattina nel fuso orario della persona?
* un algoritmo che divide il pubblico che scorre nel percorso in base a una percentuale, ad esempio: 90% - 10% per escludere un gruppo di controllo

![](assets/read-segment-audience1.png)

>[!NOTE]
>
>Quando utilizzi il tipo di pianificazione &quot;Giornaliero&quot; con un&#39;attività **[!UICONTROL Read Audience]**, puoi definire un intervallo di tempo per il percorso in modo che attenda nuovi dati sul pubblico. In questo modo è possibile garantire un targeting accurato e prevenire i problemi causati da ritardi nei processi di segmentazione batch. [Scopri come pianificare un percorso](#schedule)
>
>L&#39;opzione **[!UICONTROL Trigger dopo valutazione del pubblico in batch]** è disponibile solo per un set di organizzazioni (disponibilità limitata). Per ottenere l’accesso, contatta il tuo rappresentante Adobe.

**Exclusion**

La stessa attività **Condition** utilizzata per la segmentazione (vedi sopra) ti consente anche di escludere parte della popolazione. Ad esempio, puoi escludere le persone VIP facendole fluire in un ramo con un passaggio finale subito dopo.

Questa esclusione può verificarsi subito dopo il recupero del pubblico, per scopi di conteggio della popolazione o lungo un percorso a più passaggi.

![](assets/read-segment-audience2.png)

**Unione**

I percorsi consentono di creare N rami e unirli dopo una segmentazione. Di conseguenza, puoi fare in modo che due tipi di pubblico tornino a un’esperienza comune.

Ad esempio, dopo aver seguito un’esperienza diversa per dieci giorni di un percorso, i clienti VIP e non VIP possono tornare allo stesso percorso. Dopo un’unione, puoi dividere nuovamente il pubblico eseguendo una segmentazione o un’esclusione.

![](assets/read-segment-audience3.png)

## Nuovi tentativi {#read-audience-retry}

I nuovi tentativi vengono ora applicati per impostazione predefinita ai percorsi attivati dal pubblico (a partire da **Leggi pubblico** o **Evento di business**) durante il recupero del processo di esportazione. Se si verifica un errore durante la creazione del processo di esportazione, verranno eseguiti nuovi tentativi ogni 10 minuti, per un massimo di 1 ora. Dopo i tentativi, verrà considerato come un errore. Questi tipi di percorsi possono quindi essere eseguiti fino a 1 ora dopo l’orario pianificato.

I trigger **Read Audience** non riusciti vengono acquisiti e visualizzati in **Alerts**. L&#39;avviso **Read Audience** ti avvisa se un&#39;attività **Read Audience** non ha elaborato alcun profilo 10 minuti dopo l&#39;ora di esecuzione pianificata. Questo errore può essere causato da problemi tecnici o perché il pubblico è vuoto. Se l’errore è causato da problemi tecnici, tieni presente che possono comunque verificarsi nuovi tentativi, a seconda del tipo di problema (ad esempio, se la creazione del processo di esportazione non è riuscita, verrà eseguito un nuovo tentativo ogni 10mn per un massimo di 1h). [Ulteriori informazioni](../reports/alerts.md#alert-read-audiences)

## Video introduttivo {#video}

Comprendi i casi d’uso applicabili a un percorso attivato dall’attività Leggi pubblico. Scopri come creare percorsi basati su batch e quali best practice applicare.

>[!VIDEO](https://video.tv.adobe.com/v/3430364?captions=ita&quality=12)
