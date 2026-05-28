---
solution: Journey Optimizer
product: journey optimizer
title: Attività Ottimizza
description: Scopri l’attività Ottimizza
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: attività, condizione, area di lavoro, percorso, ottimizzazione
exl-id: f6618de4-7861-488e-90c0-f299ef5897ca
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/hbDoGEHdCBcOe-e9h06kGY2Rvb129cIzto6jJAuGkX4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: d8353d85-5da7-453d-bd68-40ad33fa0ab7id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: bcc5edb5-84c3-4940-9f84-ed88b6c16274id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 470
ht-degree: 17%

---

# Introduzione all’attività Ottimizza {#journey-path-optimization}

>[!CONTEXTUALHELP]
>id="ajo_journey_optimize"
>title="Attività Ottimizza"
>abstract="L’attività **Ottimizza** consente di definire il modo in cui i singoli utenti avanzano nel percorso creando più percorsi in base a criteri specifici, inclusi sperimentazione, targeting e condizioni specifiche. Tieni presente che l’attività **Ottimizza** è il nuovo strumento per la creazione di percorsi condizionali nei percorsi. Sostituisce la precedente attività **Condizione**."

>[!IMPORTANT]
>
>L&#39;attività **Ottimizza** è il nuovo veicolo per la creazione di percorsi condizionali in percorsi. Sostituisce l’attività **Condizione** precedente, che è stata rimossa dall’interfaccia utente. Tutta la logica condizionale viene mantenuta e ora viene gestita tramite le [condizioni](conditions.md) dell&#39;attività **Ottimizza**.
>
>Se esistono percorsi che hanno utilizzato **[!UICONTROL Attività condizionali]**, puoi continuare a utilizzarli come prima. Vengono ora visualizzate con una nuova icona come attività **[!UICONTROL Ottimizza]** utilizzando il metodo **[!UICONTROL Condizione]**, ma il comportamento rimane invariato. Tutte le etichette personalizzate impostate sul nodo vengono mantenute.

L&#39;attività **Ottimizza** consente di definire il modo in cui i singoli utenti avanzano nel percorso creando più **percorsi** in base a criteri specifici, tra cui sperimentazione, targeting e condizioni specifiche, garantendo il massimo coinvolgimento e successo nella creazione di percorsi altamente personalizzati ed efficaci.

![Pulsante Ottimizza nella tavolozza attività percorso](assets/journey-optimize.png)

## Che cos&#39;è un percorso di percorso? {#journey-path}

Un percorso **percorso** può essere costituito da uno dei seguenti elementi: sequenza di comunicazioni, tempo che intercorre tra di esse, numero di comunicazioni o una combinazione di queste tre variabili.

Ad esempio, un percorso potrebbe contenere un messaggio e-mail, un altro potrebbe contenere due messaggi SMS e un terzo potrebbe contenere un messaggio e-mail, un nodo Attendi di due ore e quindi un messaggio SMS.

## Tre modi per ottimizzare i percorsi {#optimization-methods}

Tramite l&#39;attività **Ottimizza** è possibile eseguire le azioni seguenti nei percorsi di percorso:

* [Esegui esperimenti sui percorsi](path-experimentation.md): esegui test di percorsi diversi in base a suddivisioni casuali per determinare quali prestazioni migliori in base alle metriche di successo predefinite (ad esempio, tasso di conversione, ricavi, coinvolgimento).

* [Sfrutta le regole di targeting](path-targeting.md): definisci le regole specifiche che devono essere soddisfatte affinché un cliente possa immettere uno dei percorsi di percorso, in base a segmenti di pubblico, attributi di profilo o dati contestuali. In questo modo il pubblico adatto entra nel percorso specificato.

  >[!AVAILABILITY]
  >
  >Questa funzionalità è attualmente disponibile in modo limitato. Per richiedere l’accesso, contatta il tuo rappresentante Adobe.

* [Applica condizioni](conditions.md) - Crea percorsi condizionali in base a criteri specifici quali origini dati, ora, data, divisioni percentuali o limiti di profilo. Equivale all’attività Condizione precedente.

## Come funziona {#how-it-works}

Una volta che il percorso è attivo, i profili vengono valutati in base ai criteri definiti e, in base ai criteri di corrispondenza, vengono inviati lungo il percorso appropriato dal percorso.

## Passaggi successivi {#next-steps}

Seleziona il metodo di ottimizzazione più adatto al tuo caso d’uso:

* Vuoi testare e scoprire quale percorso funziona meglio? → Vai a [Sperimentazione percorso](path-experimentation.md)
* Vuoi inviare diversi tipi di pubblico in percorsi specifici? → Vai a [Destinazione percorso](path-targeting.md)
* Creare una logica condizionale (scenari if/then)? → Vai a [Condizioni](conditions.md)
