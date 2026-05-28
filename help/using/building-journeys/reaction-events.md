---
solution: Journey Optimizer
product: journey optimizer
title: Eventi di reazione
description: Scopri come utilizzare gli eventi di reazione per rispondere ai dati di tracciamento dei messaggi, come aperture e clic all’interno dei percorsi, e configurare percorsi di timeout per i non-responder.
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: percorso, eventi, reazione, tracciamento, piattaforma
exl-id: 235384f3-0dce-4797-8f42-1d4d01fa42d9
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/6myO49j2-TgkX0-diC8JDePxvMBPjZGnMYdxO466cP4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: d08afb72-92f6-4856-88e3-11ec34313c2f
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
  - id: e57d1da4-32c2-4cc6-945c-9feb219156ff
  - id: ebd64fe4-362a-4a1c-9476-b2573ed12a95
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 506
ht-degree: 15%

---

# Eventi di reazione {#reaction-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_reaction"
>title="Eventi di reazione"
>abstract="Questa attività consente di reagire ai dati di tracciamento relativi a un messaggio inviato nello stesso percorso. Queste informazioni vengono acquisite in tempo reale nel momento in cui sono condivise con [!DNL Adobe Experience Platform]."

## Panoramica {#overview}

Tra le diverse attività degli eventi disponibili nella palette, troverai l&#39;evento integrato **[!UICONTROL Reactions]**. Questa attività consente di reagire ai dati di tracciamento relativi a un messaggio inviato nello stesso percorso. Queste informazioni vengono acquisite in tempo reale nel momento in cui sono condivise con [!DNL Adobe Experience Platform].

Puoi reagire ai messaggi selezionati o aperti. Ad esempio, puoi inviare un altro messaggio se una persona ha aperto l’e-mail precedente o ha fatto clic al suo interno, oppure puoi inviare un messaggio di follow-up diverso se non ha interagito con la tua comunicazione.

Consulta [Attività azione](../building-journeys/about-journey-activities.md#action-activities).

Puoi utilizzare l&#39;attività **[!UICONTROL Reazione]** per eseguire un&#39;azione quando non vi è alcuna reazione ai messaggi. A questo scopo, crea un secondo percorso parallelo all&#39;attività **[!UICONTROL Reaction]** e aggiungi un&#39;attività **[!UICONTROL Wait]**. Se non si verifica alcuna reazione durante il periodo definito nell&#39;attività **[!UICONTROL Wait]**, verrà scelto il secondo percorso. Puoi scegliere di inviare, ad esempio, un messaggio di follow-up.

## Come configurare gli eventi di reazione {#configure}

![Configurazione evento di reazione con selezione canale e opzioni tipo evento](assets/journey45.png)

Per configurare gli eventi di reazione, segui la procedura riportata di seguito:

1. Posiziona un&#39;attività **[!UICONTROL Reazione]** **immediatamente** dopo un&#39;attività [azione canale](journey-action.md) nell&#39;area di lavoro del percorso.
1. Aggiungi un&#39;etichetta **[!UICONTROL Label]** alla reazione. Questo passaggio è facoltativo.
1. Dall’elenco a discesa, seleziona l’attività di azione a cui desideri reagire. Puoi selezionare qualsiasi attività di azione posizionata nei passaggi precedenti del percorso.
1. A seconda dell’azione selezionata, scegli a cosa desideri reagire.
1. Puoi definire un timeout dell’evento (tra 40 secondi e 90 giorni) e un percorso di timeout. Questo crea un secondo percorso per i singoli utenti che non hanno reagito entro la durata definita. Durante il test di un percorso che utilizza un evento di reazione, il valore predefinito e minimo della modalità di test **[!UICONTROL Tempo di attesa]** è di 40 secondi. Vedi [questa sezione](../building-journeys/testing-the-journey.md).

## Guardrail e limitazioni {#guardrails-limitations}

* Un&#39;attività **[!UICONTROL Reaction]** deve essere inserita **immediatamente** dopo un&#39;attività [channel action](journey-action.md) nell&#39;area di lavoro del percorso.
* Non è possibile utilizzare un&#39;attività **[!UICONTROL Reazione]** se prima non è presente alcuna attività di azione del canale.
* Il posizionamento di un&#39;attività **[!UICONTROL Wait]** o di qualsiasi altra attività tra l&#39;azione del canale e l&#39;attività **[!UICONTROL Reaction]** non è supportato e potrebbe impedire il funzionamento previsto dell&#39;attività Reaction.
* Gli eventi di reazione possono tracciare solo i messaggi inviati all’interno dello stesso percorso. Non possono tenere traccia dei messaggi che si verificano in un percorso diverso.
* Gli eventi di reazione tengono traccia dei clic su collegamenti del tipo &quot;tracciato&quot;. L’annullamento dell’abbonamento e i collegamenti alle pagine mirror non vengono presi in considerazione.
* Le aperture delle e-mail vengono tracciate utilizzando un’immagine a 0 pixel inclusa nell’e-mail. Se i client e-mail (come Gmail) bloccano le immagini, le aperture e-mail non verranno prese in considerazione.
