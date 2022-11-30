---
solution: Journey Optimizer
product: journey optimizer
title: Eventi di reazione
description: Scopri gli eventi di reazione
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 235384f3-0dce-4797-8f42-1d4d01fa42d9
source-git-commit: 9b7898d0fe008a0e7ef711b1303230c6f901b712
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 2%

---

# Eventi di reazione {#reaction-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_reaction"
>title="Eventi di reazione"
>abstract="Questa attività ti consente di reagire ai dati di tracciamento relativi a un messaggio inviato nello stesso percorso. Acquisiamo queste informazioni in tempo reale nel momento in cui vengono condivise con Adobe Experience Platform."

Tra le diverse attività dell’evento disponibili nella palette, troverai la **[!UICONTROL Reazioni]** evento. Questa attività ti consente di reagire ai dati di tracciamento relativi a un messaggio inviato nello stesso percorso. Acquisiamo queste informazioni in tempo reale nel momento in cui vengono condivise con Adobe Experience Platform.

Puoi reagire ai messaggi selezionati o aperti.

Puoi inoltre utilizzare questo meccanismo per eseguire un’azione quando non vi sono reazioni ai messaggi. A questo scopo, crea un secondo percorso parallelo all’attività di reazione e aggiungi un’attività di attesa. Se non vi è alcuna reazione durante il periodo definito nell’attività di attesa, verrà scelto il secondo percorso. Puoi scegliere di inviare, ad esempio, un messaggio di follow-up.

Tieni presente che puoi utilizzare un’attività di reazione nell’area di lavoro solo se è presente un’attività di azione del canale prima di (E-mail e push).

Vedi [Informazioni sulle attività azione](../building-journeys/about-journey-activities.md#action-activities).

![](assets/journey45.png)

Di seguito sono riportati i diversi passaggi per configurare gli eventi di reazione:

1. Aggiungi un **[!UICONTROL Etichetta]** alla reazione. Questo passaggio è facoltativo.
1. Dall’elenco a discesa, seleziona l’attività di azione a cui desideri reagire. Puoi selezionare qualsiasi attività di azione posizionata nei passaggi precedenti del percorso.
1. A seconda dell’azione selezionata, scegli a cosa reagire.
1. Puoi definire un timeout evento (tra 40 secondi e 30 giorni) e un percorso di timeout. Questo creerà un secondo percorso per gli individui che non hanno reagito entro la durata definita. Quando si esegue il test di un percorso che utilizza un evento di reazione, la modalità di test **[!UICONTROL Tempo di attesa]** il valore predefinito e minimo è 40 secondi. Vedi [questa sezione](../building-journeys/testing-the-journey.md).

>[!NOTE]
>
>
>Gli eventi di reazione non possono tenere traccia dei messaggi che si verificano in un percorso diverso.
>
>Gli eventi di reazione tengono traccia dei clic sui collegamenti del tipo &quot;tracciati&quot;. I collegamenti di annullamento all’abbonamento e alle pagine mirror non vengono presi in considerazione.

>[!IMPORTANT]
>
>I client e-mail come Gmail consentono il blocco delle immagini. Le aperture delle e-mail vengono tracciate utilizzando un’immagine di 0 pixel inclusa nell’e-mail. Se le immagini sono bloccate, le aperture delle e-mail non verranno prese in considerazione.
