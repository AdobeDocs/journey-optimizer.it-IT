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
source-git-commit: 8aeb3e3769e28419982c28620e5b141778d2fa67
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 8%

---

# Introduzione all’attività Ottimizza {#journey-path-optimization}

>[!CONTEXTUALHELP]
>id="ajo_journey_optimize"
>title="Attività Ottimizza"
>abstract="L’attività **Ottimizza** consente di definire il modo in cui i singoli utenti avanzano nel percorso creando più percorsi in base a criteri specifici, inclusi sperimentazione, targeting e condizioni specifiche. L&#39;attività **Ottimizza** è il nuovo veicolo per la creazione di percorsi condizionali in percorsi. Sostituisce l&#39;attività **Condition** precedente."

>[!IMPORTANT]
>
>L&#39;attività **Ottimizza** è il nuovo veicolo per la creazione di percorsi condizionali in percorsi. Sostituisce l&#39;attività **Condition** precedente, che è stata rimossa dall&#39;interfaccia utente. Tutta la logica condizionale viene mantenuta e ora viene gestita tramite le **condizioni** dell&#39;attività [Ottimizza](conditions.md).
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
