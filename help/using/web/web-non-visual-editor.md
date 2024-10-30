---
title: Modificare il contenuto utilizzando l’editor non visivo
description: Scopri come creare una pagina web e modificarne il contenuto utilizzando l’editor non visivo di Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Experienced
source-git-commit: 59fae238326186092a29d4a451655efabaabb4b2
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---

# Utilizza l’editor non visivo web {#web-non-visual-editor}

Oltre al [!DNL Journey Optimizer] [Web Designer](web-visual-editor.md) visivo, puoi anche aggiungere modifiche alle pagine Web utilizzando un **editor non visivo**.

Ciò può essere utile se non è possibile installare estensioni del browser, ad esempio [Adobe Experience Cloud Visual Helper](web-prerequisites.md#visual-authoring-prerequisites), necessario per caricare le pagine nella finestra di progettazione Web.

In alcuni casi, potrebbe essere più semplice utilizzare un editor non visivo per applicare modifiche a un particolare selettore CSS, senza il rischio di modificare altri elementi di una pagina web o di modificare la struttura della pagina.

Per creare le tue esperienze web con l’editor non visivo, segui i passaggi indicati di seguito.

1. Dalla schermata **[!UICONTROL Modifica contenuto]** nel percorso o nella campagna, deseleziona l&#39;opzione **[!UICONTROL Editor visivo]**.

1. Fai clic su **[!UICONTROL Aggiungi una modifica]** per iniziare a modificare il contenuto Web.

   ![](assets/web-campaign-add-modification-button.png)

1. Viene visualizzato l’editor non visivo. Puoi aggiungere la prima modifica utilizzando il riquadro a sinistra.

   ![](assets/web-non-visual-editor.png)

1. Selezionare il tipo di modifica:

   * **[!UICONTROL Selettore CSS]** - [Ulteriori informazioni](manage-web-modifications.md#css-selector)
   * **[!UICONTROL Pagina`<Head>`]** - [Ulteriori informazioni](manage-web-modifications.md#page-head)

1. Fai clic sul pulsante **[!UICONTROL Opzioni di modifica avanzate]**. Viene aperto l’editor di personalizzazione.

   Puoi sfruttare l&#39;editor di personalizzazione [!DNL Journey Optimizer] con tutte le sue funzionalità di personalizzazione e authoring. [Ulteriori informazioni](../personalization/personalization-build-expressions.md)

1. Inserisci il contenuto e **[!UICONTROL Salva]** le modifiche.

   ![](assets/web-non-visual-editor-ex-save.png)

1. La prima modifica viene visualizzata sopra il riquadro **[!UICONTROL Modifiche]**.

   Fai clic sul pulsante **[!UICONTROL Altre azioni]** accanto alla modifica e seleziona **[!UICONTROL Informazioni]** per visualizzarne i dettagli. Puoi anche **[!UICONTROL Modificare]** o **[!UICONTROL Eliminare]** la modifica.

   ![](assets/web-non-visual-editor-ex-more.png)

   >[!NOTE]
   >
   >Il riquadro **[!UICONTROL Modifiche]** è identico a quello utilizzato per [Web Designer](web-visual-editor.md). Tutte le azioni che è possibile eseguire sono descritte in [questa sezione](manage-web-modifications.md#use-modifications-pane).

1. Fai clic sul pulsante **[!UICONTROL Altre azioni]** nella parte superiore del riquadro **[!UICONTROL Modifiche]** per **[!UICONTROL Aggiungere una modifica]** e ripeti i passaggi precedenti. [Ulteriori informazioni](manage-web-modifications.md#add-modifications)

   ![](assets/web-non-visual-editor-more.png)

1. Seleziona la freccia in alto a sinistra dello schermo per tornare alla schermata dell’edizione del percorso o della campagna. Puoi visualizzare il numero corrente di modifiche e aggiungere altre modifiche.

   ![](assets/web-campaign-modifications.png)

   Se necessario, puoi anche passare al web designer. Tutte le modifiche verranno mantenute.


1. Puoi selezionare qualsiasi elemento del sito web e tenere traccia dei clic su di esso. Per abilitare il tracciamento dei clic e definire le azioni da tracciare, fai clic sulla seconda icona nella barra a sinistra, come illustrato di seguito:

   ![](assets/web-campaign-click.png)

   Utilizza il pulsante **Aggiungi componente** per selezionare una nuova azione da tracciare. Ulteriori informazioni sull&#39;utilizzo del tracciamento dei clic in [questa sezione](monitor-web-experiences.md#use-click-tracking).
