---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare gli eventi del percorso
description: Scopri come utilizzare gli eventi nei tuoi percorsi
feature: Journeys, Events
topic: Administration
role: Engineer, Admin
level: Intermediate, Experienced
keywords: eventi, evento, percorso, definizione, inizio
exl-id: fb3e51b5-4cbb-4949-8992-1075959da67d
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '1537'
ht-degree: 33%

---

# Utilizzare gli eventi del percorso {#about-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_list"
>title="Eventi del percorso"
>abstract="Un evento è collegato a una persona. Riguarda il comportamento di una persona (ad esempio, una persona che ha acquistato un prodotto o visitato un negozio, che è uscita da un sito web, ecc.) o qualcosa che accade in relazione a una persona (ad esempio, una persona che ha raggiunto 10.000 punti fedeltà). Journey Optimizer “ascolta” gli eventi unitari nei percorsi per orchestrare le migliori azioni successive."

Utilizza gli eventi per attivare i singoli percorsi, distribuendo messaggi in tempo reale a ogni utente che entra nel percorso.

Nella configurazione dell’evento, puoi configurare gli eventi previsti nei percorsi. I dati degli eventi in arrivo vengono normalizzati seguendo Adobe Experience Data Model (XDM). Gli eventi provengono dalle API Streaming Ingestion (acquisizione dati in streaming) per gli eventi autenticati e non autenticati, ad esempio gli eventi SDK di Adobe Mobile. Puoi utilizzare più eventi (in passaggi diversi di un percorso) e diversi percorsi possono utilizzare lo stesso evento.

La configurazione dell&#39;evento è **obbligatoria** e deve essere eseguita da un tecnico dati.

È possibile configurare due tipi di eventi: **Eventi unitari** e **Eventi aziendali**.

➡️ [Scopri questa funzione nel video](#video)

## Eventi unitari {#unitary-events}

**Unitario** eventi collegati a una persona. Si riferiscono al comportamento di una persona (ad esempio, una persona ha acquistato un prodotto, ha visitato un negozio, è uscita da un sito web, ecc.) o a qualcosa che si verifica in relazione a una persona (ad esempio, una persona ha raggiunto 10.000 punti fedeltà). [!DNL Journey Optimizer] farà da listener in percorsi per orchestrare le migliori azioni successive. Gli eventi unitari possono essere basati su regole o generati dal sistema. Per informazioni su come creare un evento unitario, consulta questa [pagina](../event/about-creating.md).

I percorsi unitari (a partire da un evento o da una qualificazione del pubblico) includono un guardrail che impedisce ai percorsi di essere attivati erroneamente più volte per lo stesso evento. Per impostazione predefinita, il reingresso del profilo viene bloccato temporaneamente per 5 minuti. Ad esempio, se un evento attiva un percorso alle 12:01 per un profilo specifico e un altro arriva alle 12:03 (che si tratti dello stesso evento o di un altro che attiva lo stesso percorso), il percorso non si riavvierà per questo profilo.

## Eventi di business {#business-events}

Gli eventi **Business** non sono collegati a un profilo specifico. Ad esempio, può essere un avviso di notizie, un aggiornamento sportivo, una modifica o cancellazione di un volo, un aggiornamento di inventario, eventi meteo, ecc. Anche se questi eventi non sono specifici per un profilo, possono essere di interesse per un numero qualsiasi di profili: utenti abbonati a notizie particolari, passeggeri su un volo, acquirenti interessati a un prodotto esaurito, ecc. Gli eventi di business sono sempre basati su regole. Quando rilasci un evento di business in un percorso, aggiunge automaticamente un&#39;attività **Read audience** subito dopo.Scopri come creare un evento di business [in questa pagina](../event/about-creating-business.md).


## Tipo ID evento {#event-id-type}

Per gli eventi **business**, il tipo di ID evento è sempre basato su regole.

Per gli eventi **unitari**, esistono due tipi di ID evento:

* **Eventi basati sulle regole**: questo tipo di evento non genera un eventID. Utilizzando l’editor di espressioni semplici, puoi semplicemente definire una regola che verrà utilizzata dal sistema per identificare gli eventi rilevanti che attiveranno i percorsi. Questa regola può essere basata su qualsiasi campo disponibile nel payload dell’evento, ad esempio la posizione del profilo o il numero di elementi aggiunti al carrello del profilo.

  >[!CAUTION]
  >
  >Per gli eventi basati su regole viene definita una regola di quota limite. Limita il numero di eventi qualificati che un percorso può elaborare a 5.000 al secondo per una determinata organizzazione. Corrisponde agli SLA di Journey Optimizer. Consulta le licenze Journey Optimizer e la [descrizione del prodotto Journey Optimizer](https://helpx.adobe.com/it/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

* Eventi **generati dal sistema**: questi eventi richiedono un eventID. Questo campo eventID viene generato automaticamente durante la creazione dell’evento. Il sistema che trasmette l’evento non deve generare un ID, deve trasmettere quello disponibile nell’anteprima del payload.

>[!NOTE]
>
>Journey Optimizer richiede che gli eventi vengano inviati in streaming al servizio core di raccolta dati (DCCS) per poter attivare un percorso. Eventi acquisiti in batch o eventi da set di dati interni di Journey Optimizer (feedback messaggi, tracciamento e-mail, ecc.) non possono essere utilizzati per attivare un percorso. Per i casi d’uso in cui non è possibile ricevere eventi in streaming, crea un pubblico basato su tali eventi e utilizza l’attiviità **Leggi pubblico**. Tecnicamente è possibile utilizzare la qualificazione del pubblico, ma può causare problemi a valle in base alle azioni utilizzate. Questi dati non devono necessariamente andare al Profilo in tempo reale. Se desideri utilizzare gli eventi per la segmentazione, ti consigliamo di abilitare il set di dati per il profilo.

## Ciclo dei dati {#data-cycle}

Gli eventi sono chiamate API POST. Gli eventi vengono inviati a Adobe Experience Platform tramite le API Streaming Ingestion. La destinazione URL degli eventi inviati tramite API di messaggistica transazionale è denominata &quot;entrata&quot;. Il payload degli eventi segue la formattazione XDM.

Nell&#39;intestazione del payload sono contenute le informazioni richieste per il funzionamento delle API Streaming Ingestion, oltre alle informazioni necessarie per il funzionamento di [!DNL Journey Optimizer] e alle informazioni da utilizzare nei percorsi, ad esempio nel corpo la quantità di un carrello abbandonato. L’acquisizione in streaming può avvenire in modalità autenticata e non autenticata. Per informazioni dettagliate sulle API per l’acquisizione in streaming, fai riferimento a [questo collegamento](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=it){target="_blank"}.

Una volta arrivati attraverso le API Streaming Ingestion, gli eventi si propagano in un servizio interno denominato Pipeline e infine passano a Adobe Experience Platform. Se nello schema dell’evento è abilitato il flag Profilo del cliente in tempo reale ed è presente un ID set di dati con il medesimo flag, tale schema si propaga nel Profilo del cliente in tempo reale.

Per gli eventi generati dal sistema, la pipeline filtra gli eventi che presentano un payload contenente [!DNL Journey Optimizer] eventID (vedi il processo di creazione degli eventi illustrato di seguito) forniti da [!DNL Journey Optimizer] e contenuti nel payload degli eventi. Per gli eventi basati su regole, il sistema identifica l’evento utilizzando la condizione eventID. [!DNL Journey Optimizer] fa da listener agli eventi, il che attiva il percorso corrispondente.


## Informazioni sulla velocità effettiva degli eventi di Percorso {#event-thoughput}

Adobe Journey Optimizer supporta un volume massimo di 5.000 eventi percorsi al secondo a livello di organizzazione, in tutte le sandbox. Questa quota si applica a tutti gli eventi utilizzati nei percorsi attivi, che includono **Live**, **Dry run**, **Closed** e **Paused** percorsi. Al raggiungimento di questa quota, i nuovi eventi vengono messi in coda con una velocità di elaborazione di 5.000 al secondo. Il tempo massimo che un evento può trascorrere nella coda è **24 ore**.

Per la quota di 5.000 TPS vengono conteggiati i seguenti tipi di eventi:

* **Eventi unitari esterni**: include eventi basati su regole e generati dal sistema. Se lo stesso evento non elaborato è idoneo per più definizioni di regola, ogni regola qualificata conta come un evento separato. Maggiori dettagli di seguito.

* **Eventi di qualificazione del pubblico**: se lo stesso pubblico di streaming viene utilizzato in più percorsi, ogni utilizzo conta separatamente. Ad esempio, l’utilizzo dello stesso pubblico in un’attività di qualificazione del pubblico in due percorsi determina due eventi conteggiati.

* **Eventi di reazione**: eventi attivati dalle reazioni del profilo (e-mail aperta, e-mail selezionata, ecc.) all&#39;interno di un percorso.

* **Eventi aziendali**: eventi non associati a un profilo specifico, ma a un evento aziendale.

* **Eventi di Analytics**: se l&#39;integrazione [con Adobe Analytics per attivare i percorsi](about-analytics.md) è stata abilitata, vengono inclusi anche questi eventi.

* **Riprendi eventi**: evento tecnico attivato quando un profilo riprende da un percorso in pausa. Ulteriori informazioni sulla ripresa di [percorsi in pausa](../building-journeys/journey-pause.md#how-to-resume-a-paused-journey).

* **Eventi di completamento nodo di attesa**: quando un profilo esce da un nodo di attesa, viene generato un evento tecnico per riprendere il percorso.

>[!NOTE]
>
>Ad eccezione degli eventi di attesa e ripresa, anche tutti gli altri tipi di evento vengono conteggiati nella quota se utilizzati in percorsi basati su tipi di pubblico di lettura.

### Informazioni sugli eventi non elaborati qualificati per più definizioni di regole

Lo stesso evento non elaborato può essere qualificato per più definizioni di regole nei percorsi. Quando un evento è configurato nella sezione **Amministrazione**, per lo stesso schema eventi è possibile definire più regole evento. Supponiamo ad esempio di avere un evento di acquisto con campi città e purchaseValue. Prendiamo in considerazione i seguenti scenari:

1. Un evento **E1** denominato `newYorkPurchases` è stato creato con una definizione di regola che indica che `city=='New York'`. Questo evento può essere utilizzato tra 10 percorsi, ma verrà comunque conteggiato come 1 evento, quando verrà.

1. Supponiamo ora che venga creato anche un evento **E2** denominato `highValuePurchases` con `purchaseValue > 1000` come definizione di regola, nello stesso schema evento di **E1**. In questo caso, lo stesso evento in ingresso verrà valutato in base a due regole: `newYorkPurchases` e `highValuePurchases`. Ora può capitare che un acquisto di New York sia anche un acquisto di alto valore.

   In questo caso, Journey Optimizer creerà due eventi, **E1** e **E2**, dello stesso evento in ingresso, che farà di questo singolo evento in ingresso un conteggio di due eventi.

   Tieni presente che questi eventi iniziano a essere conteggiati quando vengono utilizzati in un percorso attivo, tra cui **Live**, **Dry run**, **Closed** e **Paused** percorso.

## Aggiornamento ed eliminazione di un evento {#update-event}


Per evitare di interrompere i percorsi esistenti, quando modifichi un evento utilizzato in un percorso **Bozza**, **Live** o **Chiuso**, puoi modificare solo il nome, la descrizione o aggiungere campi payload.

Qualsiasi evento utilizzato in **Live**, **Draft** o **Closed** percorsi non può essere eliminato. Per eliminare un evento utilizzato, è necessario interrompere l&#39;utilizzo dei percorsi e/o rimuoverlo dai percorsi 2D in cui viene utilizzato. Puoi controllare il campo **[!UICONTROL Usato in]**. Viene visualizzato il numero di percorsi che utilizzano quel particolare evento. Per visualizzare l’elenco dei percorsi corrispondenti, puoi fare clic sul pulsante **[!UICONTROL Visualizza percorsi]**.

## Video sulle procedure {#video}

Scopri come configurare un evento, specificare l’endpoint di streaming e il payload di un evento.

>[!VIDEO](https://video.tv.adobe.com/v/336253?quality=12)

Comprendere i casi d’uso applicabili per gli eventi di business. Scopri come creare un percorso utilizzando un evento di business e quali best practice applicare.

>[!VIDEO](https://video.tv.adobe.com/v/334234?quality=12)
