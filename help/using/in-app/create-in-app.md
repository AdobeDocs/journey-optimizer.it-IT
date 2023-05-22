---
title: Creare una notifica in-app
description: Scopri come creare un messaggio in-app in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: in-app, messaggio, creazione, inizio
exl-id: b3b79fe2-7db3-490d-9c3d-87267aa55eea
source-git-commit: 9bebcde9edde40a0fadba34d8b40757036a6436d
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 6%

---

# Creare un messaggio in-app {#create-in-app}

<!--
>[!BEGINTABS]

>[!TAB Add an In-app message to a journey]

>[!AVAILABILITY]
>
>The In-app activity is currently available as a beta to select users only. To join the beta program, contact Adobe Customer Care.

1. Open your journey, then drag and drop an **[!UICONTROL In-app]** activity from the **[!UICONTROL Actions]** section of the palette.

    When a profile reaches the end of their journey, any in-app messages displayed to them will automatically expire. For that reason, a Wait activity is automatically added after your In-app activity to ensure proper timing.

    ![](assets/in_app_journey_1.png)

1. Enter a **[!UICONTROL Label]** and **[!UICONTROL Description]** for your message.

1. Choose the [In-app surface](inapp-configuration.md) to use.

    ![](assets/in_app_journey_2.png)

1. You can now start designing your content with the **[!UICONTROL Edit content]** button. [Learn more](design-in-app.md)

1. Click **[!UICONTROL Edit trigger]** to configure your Trigger. 

    ![](assets/in_app_journey_4.png)

1. Choose the frequency of your trigger when your In-app message is active:

    * **[!UICONTROL Show every time]**: Always show the message when the events selected in the **[!UICONTROL Mobile app trigger]** drop-down occur.
    * **[!UICONTROL Show once]**: Only show this message the first time the events selected in the **[!UICONTROL Mobile app trigger]** drop-down occur.
    * **[!UICONTROL Show until click through]**: Show this message when the events selected in the **[!UICONTROL Mobile app trigger]** drop-down occur until an interact event is sent by the SDK with an action of "clicked".

1. From the **[!UICONTROL Mobile app trigger]** dropdown(s), choose the event(s) and criteria that will trigger your message:

    1. From the left drop-down, select the event required to trigger the message.
    1. From the right drop-down, select the validation required on the selected event.
    1. Click the **[!UICONTROL Add]** button if you want the trigger to consider multiple events or criteria. Then, repeat the steps above.
    1. Select how your events are linked, e.g. choose **[!UICONTROL And]** if you want **both** triggers to be true in order for a message to be shown or choose **[!UICONTROL Or]** if you want the message to be shown if **either** of the triggers are true.
    1. Click **[!UICONTROL Save]** when your Triggers have been configured.

    ![](assets/in_app_journey_3.png)
    
1. If necessary, complete your journey flow by dragging and dropping additional actions or events. [Learn more](../building-journeys/about-journey-activities.md)

1. Once your In-app message is ready, finalize the configuration and publish your journey to activate it.

For more information on how to configure a journey, refer to [this page](../building-journeys/journey-gs.md).

>[!TAB Add an In-app message to a campaign]
-->

1. Accedere a **[!UICONTROL Campagne]** , quindi fai clic su **[!UICONTROL Crea campagna]**.

1. In **[!UICONTROL Proprietà]** , seleziona quando il tipo di esecuzione della campagna è Pianificato o Attivato da API. Ulteriori informazioni sui tipi di campagna in [questa pagina](../campaigns/create-campaign.md#campaigntype).

1. In **[!UICONTROL Azioni]** , scegli il **[!UICONTROL Messaggio in-app]** e **[!UICONTROL Superficie app]** precedentemente configurato per il messaggio in-app. Quindi, fai clic su **[!UICONTROL Crea]**.

   Ulteriori informazioni sulla configurazione in-app in [questa pagina](inapp-configuration.md).

   ![](assets/in_app_create_1.png)

1. Dalla sezione **[!UICONTROL Proprietà]** , immetti il **[!UICONTROL Titolo]** e **[!UICONTROL Descrizione]** descrizione.

1. Per assegnare etichette di utilizzo dei dati personalizzate o di base al messaggio in-app, seleziona **[!UICONTROL Gestisci accesso]**. [Maggiori informazioni](../administration/object-based-access.md).

1. Fai clic su **[!UICONTROL Seleziona pubblico]** per definire il pubblico di destinazione dall’elenco dei segmenti di Adobe Experience Platform disponibili. [Maggiori informazioni](../segment/about-segments.md).

   ![](assets/in_app_create_2.png)

1. In **[!UICONTROL Spazio dei nomi dell’identità]** , scegli lo spazio dei nomi da utilizzare per identificare i singoli utenti dal segmento selezionato. [Maggiori informazioni](../event/about-creating.md#select-the-namespace).

1. Clic **[!UICONTROL Modifica trigger]** per scegliere gli eventi e i criteri che attiveranno il messaggio:

   1. Clic **Aggiungi condizione** se desideri che il trigger consideri più eventi o criteri.
   1. Seleziona la modalità di collegamento degli eventi, ad esempio scegli **[!UICONTROL E]** se vuoi **entrambi** i trigger devono essere true per consentire la visualizzazione di un messaggio o la scelta **[!UICONTROL Oppure]** se desideri che venga visualizzato il messaggio se **o** dei trigger sono true.
   1. Clic **[!UICONTROL Crea gruppo]** per raggruppare i trigger.

   ![](assets/in_app_create_3.png)

1. Scegli la frequenza del trigger quando il messaggio in-app è attivo. Sono disponibili le seguenti opzioni:

   * **[!UICONTROL Ogni volta]**: mostra sempre il messaggio quando gli eventi selezionati nel **[!UICONTROL Attivatore app mobile]** a discesa.
   * **[!UICONTROL Una volta]**: mostra questo messaggio solo la prima volta che gli eventi selezionati nel **[!UICONTROL Attivatore app mobile]** a discesa.
   * **[!UICONTROL Fino al click-through]**: mostra questo messaggio quando gli eventi selezionati nel **[!UICONTROL Attivatore app mobile]** Questo si verifica finché un evento di interazione non viene inviato dall’SDK con l’azione &quot;clicked&quot;.
   * **[!UICONTROL X numero di volte]**: mostra questo messaggio X volta.

1. Se necessario, scegliere quale **[!UICONTROL Giorno della settimana]** o **[!UICONTROL Ora del giorno]** verrà visualizzato il messaggio in-app.

1. Le campagne sono progettate per essere eseguite in una data specifica o con una frequenza ricorrente. Scopri come configurare **[!UICONTROL Pianificazione]** della campagna in [questa sezione](../campaigns/create-campaign.md#schedule).

   ![](assets/in-app-schedule.png)

1. Ora puoi iniziare a progettare il contenuto con **[!UICONTROL Modifica contenuto]** pulsante. [Ulteriori informazioni](design-in-app.md)

   ![](assets/in_app_create_4.png)

<!--
>[!ENDTABS]
-->

## Video introduttivo{#video}

Il video seguente mostra come creare, configurare e pubblicare messaggi in-app nelle campagne.

>[!VIDEO](https://video.tv.adobe.com/v/3410430?quality=12&learn=on)


**Argomenti correlati:**

* [Progettare un messaggio in-app](design-in-app.md)
* [Testare e inviare il messaggio in-app](send-in-app.md)
* [Rapporto in-app](../reports/campaign-global-report.md#inapp-report)
* [Configurazione in-app](inapp-configuration.md)