---
solution: Journey Optimizer
product: journey optimizer
title: Eventi di reazione
description: Scopri gli eventi di reazione
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: percorso, eventi, reazione, tracciamento, piattaforma
exl-id: 235384f3-0dce-4797-8f42-1d4d01fa42d9
version: Journey Orchestration
source-git-commit: 7822e9662d03e6c6b2d5bc5ecb9ca85dc32f0942
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 20%

---

# Eventi di reazione {#reaction-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_reaction"
>title="Eventi di reazione"
>abstract="Questa attività consente di reagire ai dati di tracciamento relativi a un messaggio inviato nello stesso percorso. Acquisiamo queste informazioni in tempo reale nel momento in cui vengono condivise con Adobe Experience Platform."

Tra le diverse attività degli eventi disponibili nella palette, troverai l&#39;evento integrato **[!UICONTROL Reactions]**. Questa attività consente di reagire ai dati di tracciamento relativi a un messaggio inviato nello stesso percorso. Acquisiamo queste informazioni in tempo reale nel momento in cui vengono condivise con Adobe Experience Platform.

Puoi reagire ai messaggi selezionati o aperti.

Puoi anche utilizzare questo meccanismo per eseguire un’azione quando non vi è alcuna reazione ai messaggi. A questo scopo, crea un secondo percorso parallelo all’attività di reazione e aggiungi un’attività Attendi. Se non si verifica alcuna reazione durante il periodo definito nell’attività Attendi, verrà scelto il secondo percorso. Puoi scegliere di inviare, ad esempio, un messaggio di follow-up.

Tieni presente che puoi utilizzare un’attività di reazione nell’area di lavoro solo se è presente un’attività di azione del canale prima di (e-mail e push).

Consulta [Informazioni sulle attività di azione](../building-journeys/about-journey-activities.md#action-activities).

![Configurazione evento di reazione con selezione canale e opzioni tipo evento](assets/journey45.png)

Di seguito sono riportati i diversi passaggi per configurare gli eventi di reazione:

1. Aggiungi un&#39;etichetta **[!UICONTROL Label]** alla reazione. Questo passaggio è facoltativo.
1. Dall’elenco a discesa, seleziona l’attività di azione a cui desideri reagire. Puoi selezionare qualsiasi attività di azione posizionata nei passaggi precedenti del percorso.
1. A seconda dell’azione selezionata, scegli a cosa desideri reagire.
1. Puoi definire un timeout dell’evento (tra 40 secondi e 90 giorni) e un percorso di timeout. Questo crea un secondo percorso per i singoli utenti che non hanno reagito entro la durata definita. Durante il test di un percorso che utilizza un evento di reazione, il valore predefinito e minimo della modalità di test **[!UICONTROL Tempo di attesa]** è di 40 secondi. Consulta [questa sezione](../building-journeys/testing-the-journey.md).

>[!NOTE]
>
>
>Gli eventi di reazione non possono tenere traccia dei messaggi che si verificano in un percorso diverso.
>
>Gli eventi di reazione tengono traccia dei clic su collegamenti del tipo &quot;tracciato&quot;. L’annullamento dell’abbonamento e i collegamenti alle pagine mirror non vengono presi in considerazione.

>[!IMPORTANT]
>
>I client di posta elettronica come Gmail consentono il blocco delle immagini. Le aperture delle e-mail vengono tracciate utilizzando un’immagine a 0 pixel inclusa nell’e-mail. Se le immagini sono bloccate, le aperture delle e-mail non verranno prese in considerazione.
