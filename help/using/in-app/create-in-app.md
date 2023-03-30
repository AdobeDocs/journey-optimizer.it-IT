---
title: Creare una notifica in-app
description: Scopri come creare un messaggio in-app in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: in-app, messaggio, creazione, avvio
exl-id: b3b79fe2-7db3-490d-9c3d-87267aa55eea
source-git-commit: c70b782b077b57485e7a40ec9f159832604f76e5
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 3%

---

# Creare un messaggio in-app {#create-in-app}

Per creare un messaggio in-app, segui i passaggi seguenti:

1. Accedere al **[!UICONTROL Campagne]** menu, quindi fai clic su **[!UICONTROL Creare una campagna]**.

1. In **[!UICONTROL Proprietà]** Specifica quando eseguire la campagna.

1. In **[!UICONTROL Azioni]** scegli la sezione **[!UICONTROL Messaggio in-app]** e **[!UICONTROL Superficie dell&#39;app]** configurato in precedenza per il messaggio in-app. Quindi, fai clic su **[!UICONTROL Crea]**.

   [Ulteriori informazioni sulla configurazione in-app](inapp-configuration.md).

   ![](assets/in_app_create_1.png)

1. Da **[!UICONTROL Proprietà]** , modifica la **[!UICONTROL Titolo]** e **[!UICONTROL Descrizione]**.

1. Per assegnare etichette di utilizzo dati personalizzate o di base al messaggio in-app, seleziona **[!UICONTROL Gestisci accesso]**. [Maggiori informazioni](../administration/object-based-access.md).

1. Fai clic sul pulsante **[!UICONTROL Selezionare il pubblico]** per definire il pubblico di cui eseguire il targeting dall’elenco dei segmenti Adobe Experience Platform disponibili. [Maggiori informazioni](../segment/about-segments.md).

   ![](assets/in_app_create_2.png)

1. In **[!UICONTROL Spazio dei nomi identità]** scegli lo spazio dei nomi da utilizzare per identificare gli individui del segmento selezionato. [Maggiori informazioni](../event/about-creating.md#select-the-namespace).

1. Fai clic su **[!UICONTROL Modifica trigger]** per scegliere gli eventi e i criteri che attiveranno il messaggio:

   1. Fai clic su **[!UICONTROL Aggiungi] condizione** se desideri che il trigger prenda in considerazione più eventi o criteri.
   1. Seleziona il collegamento degli eventi, ad esempio scegli **[!UICONTROL E]** se vuoi **entrambi** trigger impostati su true per mostrare o scegliere un messaggio **[!UICONTROL Oppure]** se desideri che il messaggio venga visualizzato se **o** dei trigger sono true.
   1. Fai clic su **[!UICONTROL Crea gruppo]** per raggruppare gli attivatori.

   ![](assets/in_app_create_3.png)

1. Scegli la frequenza del trigger quando il messaggio in-app è attivo:

   * **[!UICONTROL Ogni]**: Mostra sempre il messaggio quando gli eventi selezionati nella **[!UICONTROL Attivazione app mobile]** si verificano a discesa.
   * **[!UICONTROL Una volta]**: Mostra questo messaggio solo la prima volta che gli eventi selezionati nel **[!UICONTROL Attivazione app mobile]** si verificano a discesa.
   * **[!UICONTROL Fino al click-through]**: Mostra questo messaggio quando gli eventi selezionati nella **[!UICONTROL Attivazione app mobile]** si verifica fino a quando un evento interattivo non viene inviato dall&#39;SDK con un&#39;azione di &quot;clic&quot;.
   * **[!UICONTROL X numero di volte]**: Mostra questo messaggio X ora.

1. Se necessario, scegli quale **[!UICONTROL Giorno della settimana]** o **[!UICONTROL Ora del giorno]** verrà visualizzato il messaggio in-app.

1. Le campagne sono progettate per essere eseguite in una data specifica o su una frequenza ricorrente. Scopri come configurare il **[!UICONTROL Pianificazione]** della campagna in [questa sezione](../campaigns/create-campaign.md#schedule).

   ![](assets/in-app-schedule.png)

1. Ora puoi iniziare a progettare i contenuti con **[!UICONTROL Modifica contenuto]** pulsante . [Ulteriori informazioni](design-in-app.md)

   ![](assets/in_app_create_4.png)


## Video introduttivo{#video}

Il video seguente mostra come creare, configurare e pubblicare messaggi in-app nelle campagne.

>[!VIDEO](https://video.tv.adobe.com/v/3410430?quality=12&learn=on)


**Argomenti correlati:**

* [Progettare un messaggio in-app](design-in-app.md)
* [Test e invio del messaggio in-app](send-in-app.md)
* [Rapporto in-app](../reports/campaign-global-report.md#inapp-report)
* [Configurazione in-app](inapp-configuration.md)