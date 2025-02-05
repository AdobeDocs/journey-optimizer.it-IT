---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare gli eventi del percorso
description: Scopri come utilizzare gli eventi nei tuoi percorsi
feature: Journeys, Events
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: eventi, evento, percorso, definizione, inizio
exl-id: fb3e51b5-4cbb-4949-8992-1075959da67d
source-git-commit: aec3d79ad07ec6904e55afd6fc61ba9b4f403fc8
workflow-type: tm+mt
source-wordcount: '989'
ht-degree: 52%

---

# Utilizzare gli eventi del percorso {#about-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_list"
>title="Eventi del percorso"
>abstract="Un evento è collegato a una persona. Riguarda il comportamento di una persona (ad esempio una persona che ha acquistato un prodotto, visitato un negozio, che è uscita da un sito web, ecc.) o qualcosa che accade in relazione a una persona (ad esempio, una persona che ha raggiunto 10.000 punti fedeltà). Nell’ambito dei percorsi, Journey Optimizer farà da listener per questi dati, in modo da orchestrare le migliori azioni da eseguire in futuro."

La configurazione dell’evento consente di definire le informazioni che [!DNL Journey Optimizer] riceverà sotto forma di eventi. Puoi utilizzare più eventi (in passaggi diversi di un percorso) e diversi percorsi possono utilizzare lo stesso evento.

>[!CAUTION]
>
>La configurazione dell&#39;evento è **obbligatoria** e deve essere eseguita da un **ingegnere dati**.

Puoi configurare due tipi di eventi:

* **Eventi unitari**: questi eventi sono collegati a una persona. Si riferiscono al comportamento di una persona (ad esempio, una persona ha acquistato un prodotto, ha visitato un negozio, è uscita da un sito web, ecc.) o a qualcosa che si verifica in relazione a una persona (ad esempio, una persona ha raggiunto 10.000 punti fedeltà). [!DNL Journey Optimizer] farà da listener in percorsi per orchestrare le migliori azioni successive. Gli eventi unitari possono essere basati su regole o generati dal sistema. Per informazioni su come creare un evento unitario, consulta questa [pagina](../event/about-creating.md).

* **Eventi di business**: un evento di business è un evento che, a differenza di un evento unitario, non è collegato a un profilo specifico. Ad esempio, può essere un avviso di notizie, un aggiornamento sportivo, una modifica o cancellazione di un volo, un aggiornamento di inventario, eventi meteo, ecc. Anche se questi eventi non sono specifici per un profilo, possono essere di interesse per un numero qualsiasi di profili: utenti abbonati a notizie particolari, passeggeri su un volo, acquirenti interessati a un prodotto esaurito, ecc. Gli eventi di business sono sempre basati su regole. Quando rilasci un evento di business in un percorso, aggiunge automaticamente un&#39;attività **Read audience** subito dopo. Per informazioni su come creare un evento di business, consulta questa [pagina](../event/about-creating-business.md).


>[!NOTE]
>
>Se modifichi un evento utilizzato in una bozza di percorso o in un percorso live, puoi cambiare solo il nome e la descrizione oppure aggiungere i campi payload. Al fine di evitare l’interruzione dei percorsi, limitiamo rigorosamente la modifica delle bozze di percorso o dei percorsi live.

I percorsi unitari (a partire da un evento o da una qualificazione del pubblico) includono un guardrail che impedisce ai percorsi di essere attivati erroneamente più volte per lo stesso evento. Per impostazione predefinita, il rientro del profilo viene bloccato temporaneamente per 5 minuti. Ad esempio, se un evento attiva un percorso alle 12:01 per un profilo specifico e un altro arriva alle 12:03 (che si tratti dello stesso evento o di un altro che attiva lo stesso percorso), il percorso non si riavvierà per questo profilo.

➡️ [Scopri questa funzione nel video](#video)

## Tipo ID evento{#event-id-type}

Per gli eventi di business, il tipo di ID evento è sempre basato su regole.

Per gli eventi unitari, esistono due tipi di ID evento:

* **Eventi basati sulle regole**: questo tipo di evento non genera un eventID. Utilizzando l’editor di espressioni semplici, puoi semplicemente definire una regola che verrà utilizzata dal sistema per identificare gli eventi rilevanti che attiveranno i percorsi. Questa regola può essere basata su qualsiasi campo disponibile nel payload dell’evento, ad esempio la posizione del profilo o il numero di elementi aggiunti al carrello del profilo.

  >[!CAUTION]
  >
  >Per gli eventi basati su regole viene definita una regola di quota limite. Limita il numero di eventi qualificati che un percorso può elaborare a 5.000 al secondo per una determinata organizzazione. Corrisponde agli SLA di Journey Optimizer. Consulta le licenze Journey Optimizer e la [descrizione del prodotto Journey Optimizer](https://helpx.adobe.com/it/legal/product-descriptions/adobe-journey-optimizer.html).

* Eventi **generati dal sistema**: questi eventi richiedono un eventID. Questo campo eventID viene generato automaticamente durante la creazione dell’evento. Il sistema che trasmette l’evento non deve generare un ID, deve trasmettere quello disponibile nell’anteprima del payload.

>[!NOTE]
>
>Journey Optimizer richiede che gli eventi vengano inviati in streaming al servizio core di raccolta dati (DCCS) per poter attivare un percorso. Gli eventi acquisiti in batch o gli eventi dai set di dati interni di Journey Optimizer (feedback messaggi, tracciamento e-mail, ecc.) non possono essere utilizzati per attivare un percorso. Per i casi d’uso in cui non è possibile ricevere eventi in streaming, crea un pubblico basato su tali eventi e utilizza l’attiviità **Leggi pubblico**. Tecnicamente è possibile utilizzare la qualificazione del pubblico, ma può causare problemi a valle in base alle azioni utilizzate. Questi dati non devono necessariamente andare al Profilo in tempo reale. Se desideri utilizzare gli eventi per la segmentazione o la ricerca in un percorso diverso, ti consigliamo di abilitare il set di dati per il profilo.

## Ciclo dei dati {#data-cycle}

Gli eventi sono chiamate API POST. Gli eventi vengono inviati a Adobe Experience Platform tramite le API Streaming Ingestion. La destinazione URL degli eventi inviati tramite API di messaggistica transazionale è denominata &quot;entrata&quot;. Il payload degli eventi segue la formattazione XDM.

Nell&#39;intestazione del payload sono contenute le informazioni richieste per il funzionamento delle API Streaming Ingestion, oltre alle informazioni necessarie per il funzionamento di [!DNL Journey Optimizer] e alle informazioni da utilizzare nei percorsi, ad esempio nel corpo la quantità di un carrello abbandonato. Lo streaming ingestion può avvenire in modalità autenticata e non autenticata. Per informazioni dettagliate sulle API Streaming Ingestion, fai riferimento a [questo collegamento](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=it).

Una volta arrivati attraverso le API Streaming Ingestion, gli eventi si propagano in un servizio interno denominato Pipeline e infine passano a Adobe Experience Platform. Se nello schema dell’evento è abilitato il flag Profilo del cliente in tempo reale ed è presente un ID set di dati con il medesimo flag, tale schema si propaga nel Profilo del cliente in tempo reale.

Per gli eventi generati dal sistema, la pipeline filtra gli eventi che presentano un payload contenente [!DNL Journey Optimizer] eventID (vedi il processo di creazione degli eventi illustrato di seguito) forniti da [!DNL Journey Optimizer] e contenuti nel payload degli eventi. Per gli eventi basati su regole, il sistema identifica l’evento utilizzando la condizione eventID. [!DNL Journey Optimizer] fa da listener agli eventi, il che attiva il percorso corrispondente.

## Video sulle procedure {#video}

Scopri come configurare un evento, specificare l’endpoint di streaming e il payload di un evento.

>[!VIDEO](https://video.tv.adobe.com/v/336253?quality=12)

Comprendere i casi d’uso applicabili per gli eventi di business. Scopri come creare un percorso utilizzando un evento di business e quali best practice applicare.

>[!VIDEO](https://video.tv.adobe.com/v/334234?quality=12)
