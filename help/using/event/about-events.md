---
solution: Journey Optimizer
product: journey optimizer
title: Informazioni sugli eventi
description: Informazioni sugli eventi
feature: Events
topic: Administration
role: Admin
level: Intermediate
exl-id: fb3e51b5-4cbb-4949-8992-1075959da67d
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '904'
ht-degree: 0%

---

# Informazioni sugli eventi{#about-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_list"
>title="Informazioni sugli eventi"
>abstract="Un evento è collegato a una persona. Si riferisce al comportamento di una persona (ad esempio, una persona ha acquistato un prodotto, ha visitato un negozio, è uscita da un sito web, ecc.) o qualcosa che si verifica in relazione a una persona (ad esempio, una persona ha raggiunto 10 000 punti fedeltà). Nell’ambito dei percorsi, Journey Optimizer farà da listener a questi dati per orchestrare le migliori azioni successive."

La configurazione dell’evento ti consente di definire le informazioni [!DNL Journey Optimizer] riceverà come eventi. Puoi utilizzare più eventi (in diversi passaggi di un percorso) e più percorsi possono utilizzare lo stesso evento.

>[!CAUTION]
>
>La configurazione dell’evento è **obbligatorio** e deve essere eseguito da un **ingegnere informatico**.

Puoi configurare due tipi di eventi:

* **Unitario** eventi: questi eventi sono collegati a una persona. Si riferiscono al comportamento di una persona (ad esempio, una persona ha acquistato un prodotto, ha visitato un negozio, è uscita da un sito web, ecc.) o qualcosa che si verifica in relazione a una persona (ad esempio, una persona ha raggiunto 10 000 punti fedeltà). Questo è ciò che [!DNL Journey Optimizer] farà da listener ai percorsi, in modo da orchestrare le migliori azioni successive. Gli eventi unitari possono essere basati su regole o generati dal sistema. Per scoprire come creare un evento unitario, consulta questo [page](../event/about-creating.md).

* **Business** eventi: un evento aziendale è un evento che, a differenza di un evento unitario, non è collegato a un profilo specifico. Ad esempio, può essere un avviso di news, un aggiornamento sportivo, un cambiamento o cancellazione del volo, un aggiornamento dell&#39;inventario, eventi meteo, ecc. Anche se questi eventi non sono specifici per un profilo, possono interessare un qualsiasi numero di profili: persone abbonate a particolari argomenti d&#39;informazione, passeggeri su un volo, acquirenti interessati a un prodotto esaurito, ecc. Gli eventi aziendali sono sempre basati su regole. Quando rilasci un evento aziendale in un percorso, questo aggiunge automaticamente un **Leggi segmento** attività subito dopo. Per informazioni su come creare un evento aziendale, consulta questo [page](../event/about-creating-business.md).


>[!NOTE]
>
>Se modifichi un evento utilizzato in una bozza di percorso o in un percorso live, puoi solo modificare il nome, la descrizione o aggiungere campi payload. Limitiamo rigorosamente la modifica delle bozze di percorso o dei percorsi live per evitare di interrompere i percorsi.

I percorsi unitari (a partire da un evento o da una qualifica di segmento) includono una guardrail che impedisce l’attivazione errata dei percorsi più volte per lo stesso evento. Per impostazione predefinita, il rientro del profilo viene bloccato temporaneamente per 5 minuti. Ad esempio, se un evento attiva un percorso alle 12:01 per un profilo specifico e un altro arriva alle 12:03 (che si tratti dello stesso evento o di un altro che attiva lo stesso percorso), il percorso non verrà più avviato per questo profilo.

➡️ [Scopri questa funzione nel video](#video)

## Tipo ID evento{#event-id-type}

Per gli eventi aziendali, il tipo di ID evento è sempre basato su regole.

Per gli eventi unitari, sono disponibili due tipi di ID evento:

* **Basato su regole** eventi: questo tipo di evento non genera un eventID. Utilizzando l’editor di espressioni semplici, puoi semplicemente definire una regola che verrà utilizzata dal sistema per identificare gli eventi rilevanti che attiveranno i tuoi percorsi. Questa regola può essere basata su qualsiasi campo disponibile nel payload dell’evento, ad esempio la posizione del profilo o il numero di elementi aggiunti al carrello del profilo.

   >[!CAUTION]
   >
   >Per gli eventi basati su regole viene definita una regola di limitazione. Limita il numero di eventi qualificati che un percorso può elaborare a 5000 al secondo per una determinata organizzazione. Corrisponde agli SLA di Journey Optimizer. Fai riferimento alle licenze e agli [Descrizione del prodotto di Journey Optimizer](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html).

* **Generato dal sistema** eventi: questi eventi richiedono un eventID. Questo campo eventID viene generato automaticamente durante la creazione dell’evento. Il sistema che preme l’evento non deve generare un ID, deve passare quello disponibile nell’anteprima del payload.

Journey Optimizer richiede che gli eventi vengano inviati in streaming o batch in Adobe Experience Platform. Questi dati non devono necessariamente andare al Profilo in tempo reale. Se desideri utilizzare gli eventi per la segmentazione o la ricerca in un percorso separato, ti consigliamo di abilitare il set di dati per il profilo.

## Ciclo dei dati {#data-cycle}

Gli eventi sono chiamate API POST. Gli eventi vengono inviati ad Adobe Experience Platform tramite le API Streaming Ingestion. La destinazione URL degli eventi inviati tramite le API di messaggistica transazionale è denominata &quot;entrata&quot;. Il payload degli eventi segue la formattazione XDM.

Nell’intestazione del payload sono contenute le informazioni richieste per il funzionamento delle API Streaming Ingestion, oltre alle informazioni richieste da [!DNL Journey Optimizer] al lavoro e alle informazioni da utilizzare nei percorsi (nel corpo, ad esempio, la quantità di un carrello abbandonato). Lo streaming ingestion può avvenire in due modalità: autenticato e non autenticato. Per informazioni dettagliate sulle API Streaming Ingestion, consulta [questo link](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html).

Una volta arrivati tramite le API Streaming Ingestion, gli eventi si propagano in un servizio interno denominato Pipeline e infine passano ad Adobe Experience Platform. Se lo schema dell’evento dispone del flag Real-time Customer Profile Service abilitato e di un ID set di dati che dispone anche del flag Real-time Customer Profile Service, questo si propaga nel Real-time Customer Profile Service.

Per gli eventi generati dal sistema, la pipeline filtra gli eventi che presentano un payload contenente [!DNL Journey Optimizer] eventIDs (vedi il processo di creazione dell’evento di seguito) fornito da [!DNL Journey Optimizer] e contenuti nel payload dell’evento. Per gli eventi basati su regole, il sistema identifica l&#39;evento utilizzando la condizione eventID . Questi eventi sono ascoltati [!DNL Journey Optimizer] e viene attivato il percorso corrispondente.

## Video dimostrativi {#video}

Scopri come configurare un evento, specificare l’endpoint di streaming e il payload di un evento.

>[!VIDEO](https://video.tv.adobe.com/v/336253?quality=12)

Comprendere i casi d’uso applicabili per gli eventi aziendali. Scopri come creare un percorso utilizzando un evento aziendale e quali best practice applicare.

>[!VIDEO](https://video.tv.adobe.com/v/334234?quality=12)
