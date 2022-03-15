---
title: Informazioni sugli eventi
description: Scopri gli eventi
feature: Events
topic: Administration
role: Admin
level: Intermediate
exl-id: fb3e51b5-4cbb-4949-8992-1075959da67d
source-git-commit: d9f7c64358be3c3355337ba0db12e5b8c17bba4c
workflow-type: tm+mt
source-wordcount: '820'
ht-degree: 56%

---

# Informazioni sugli eventi{#about-events}

>[!CONTEXTUALHELP]
>id="jo_events"
>title="Informazioni sugli eventi"
>abstract="Un evento è collegato a una persona e si riferisce al suo comportamento: ad esempio, se ha acquistato un prodotto, se ha visitato un negozio, se è uscita da un sito web, e così via. Oppure, indica qualcosa che si verifica in relazione a una persona, che può ad esempio aver raggiunto 10.000 punti fedeltà. Nell’ambito dei percorsi, [!DNL Journey Optimizer] farà da listener a questi dati, in modo da orchestrare le migliori azioni da eseguire successivamente."

La configurazione dell’evento consente di definire le informazioni che [!DNL Journey Optimizer] riceverà sotto forma di eventi. È possibile utilizzare più eventi (in diversi passaggi di un percorso) e diversi percorsi possono utilizzare lo stesso evento.

>[!CAUTION]
>
>La configurazione dell’evento è **obbligatorio** e deve essere eseguito da un **utente tecnico**.

Puoi configurare due tipi di eventi:

* **Unitario** eventi: questi eventi sono collegati a una persona. Si riferiscono al comportamento di una persona (ad esempio, una persona ha acquistato un prodotto, ha visitato un negozio, è uscita da un sito web, ecc.) Oppure, indica qualcosa che si verifica in relazione a una persona, che può ad esempio aver raggiunto 10.000 punti fedeltà. Nell’ambito dei percorsi, [!DNL Journey Optimizer] farà da listener a questi dati, in modo da orchestrare le migliori azioni da eseguire successivamente. Gli eventi unitari possono essere basati su regole o generati dal sistema. Per scoprire come creare un evento unitario, consulta questo [page](../event/about-creating.md).

* **Business** eventi: un evento aziendale è un evento che, a differenza di un evento unitario, non è collegato a un profilo specifico. Ad esempio, può essere un avviso di news, un aggiornamento sportivo, un cambiamento o cancellazione del volo, un aggiornamento dell&#39;inventario, eventi meteo, ecc. Anche se questi eventi non sono specifici per un profilo, possono interessare un qualsiasi numero di profili: persone abbonate a particolari argomenti d&#39;informazione, passeggeri su un volo, acquirenti interessati a un prodotto esaurito, ecc. Gli eventi aziendali sono sempre basati su regole. Quando rilasci un evento aziendale in un percorso, aggiunge automaticamente un **Leggi segmento** attività subito dopo. Per informazioni su come creare un evento aziendale, consulta questo [page](../event/about-creating-business.md).


>[!NOTE]
>
>Se modifichi un evento utilizzato in una bozza di percorso o in un percorso live, puoi cambiare solo il nome e la descrizione oppure aggiungere i campi payload. Al fine di evitare l’interruzione dei percorsi, limitiamo rigorosamente la modifica delle bozze di percorso o dei percorsi live.

➡️ [Scopri questa funzione nel video](#video)

## Tipo ID evento{#event-id-type}

Per gli eventi aziendali, il tipo di ID evento è sempre basato su regole.

Per gli eventi unitari, sono disponibili due tipi di ID evento:

* **Eventi basati sulle regole**: questo tipo di evento non genera un eventID. Utilizzando l’editor di espressioni semplici, puoi semplicemente definire una regola che verrà utilizzata dal sistema per identificare gli eventi rilevanti che attiveranno i percorsi. Questa regola può essere basata su qualsiasi campo disponibile nel payload dell’evento, ad esempio la posizione del profilo o il numero di elementi aggiunti al carrello del profilo.

   >[!CAUTION]
   >
   >Per gli eventi basati su regole viene definita una regola di quota limite. Questa limita a 5000 al secondo il numero di eventi qualificati che un percorso può elaborare per una determinata organizzazione (ORG). Corrisponde agli SLA di Journey Optimizer. Consulta questa [pagina](https://helpx.adobe.com/it/legal/product-descriptions/journey-orchestration.html).

* Eventi **generati dal sistema**: questi eventi richiedono un eventID. Questo campo eventID viene generato automaticamente durante la creazione dell’evento. Il sistema che trasmette l’evento non deve generare un ID, deve trasmettere quello disponibile nell’anteprima del payload.

Journey Optimizer richiede che gli eventi vengano trasmessi in streaming o inseriti in batch in Adobe Experience Platform. Questi dati non devono necessariamente andare al Profilo in tempo reale. Se desideri utilizzare gli eventi per la segmentazione o la ricerca in un percorso diverso, ti consigliamo di abilitare il set di dati per il profilo.

## Ciclo dei dati {#data-cycle}

Gli eventi sono chiamate API POST. Gli eventi vengono inviati a Adobe Experience Platform tramite le API Streaming Ingestion. La destinazione URL degli eventi inviati tramite le API di messaggistica transazionale è denominata “entrata”. Il payload degli eventi segue la formattazione XDM.

Nell’intestazione del payload sono contenute le informazioni richieste per il funzionamento delle API Streaming Ingestion, oltre alle informazioni richieste da [!DNL Journey Optimizer] lavorare e informazioni da utilizzare nei percorsi (nel corpo, ad esempio, la quantità di un carrello abbandonato). Lo streaming ingestion può avvenire in modalità autenticata e non autenticata. Per informazioni dettagliate sulle API Streaming Ingestion, fai riferimento a [questo collegamento](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=it).

Una volta arrivati tramite le API Streaming Ingestion, gli eventi si propagano in un servizio interno denominato Pipeline e infine passano a Adobe Experience Platform. Se nello schema dell’evento è abilitato il flag Profilo del cliente in tempo reale ed è presente un ID set di dati con il medesimo flag, tale schema si propaga nel Profilo del cliente in tempo reale.

Per gli eventi generati dal sistema, la pipeline filtra gli eventi che presentano un payload contenente [!DNL Journey Optimizer] eventIDs (vedi il processo di creazione dell’evento di seguito) fornito da [!DNL Journey Optimizer] e contenuti nel payload dell’evento. Per gli eventi basati su regole, il sistema identifica l&#39;evento utilizzando la condizione eventID . [!DNL Journey Optimizer] fa da listener agli eventi, il che attiva il percorso corrispondente.

## Video sulle procedure {#video}

Scopri come configurare un evento, specificare l’endpoint di streaming e il payload di un evento.

>[!VIDEO](https://video.tv.adobe.com/v/336253?quality=12)

Comprendere i casi d’uso applicabili per gli eventi di business. Scopri come creare un percorso utilizzando un evento di business e quali best practice applicare.

>[!VIDEO](https://video.tv.adobe.com/v/334234?quality=12)
