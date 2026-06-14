---
title: Modificare il contenuto utilizzando l’editor non visivo
description: Scopri come creare una pagina web e modificarne il contenuto utilizzando l’editor non visivo di Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Experienced
exl-id: 00d2fc73-3ac8-421c-982a-0f3ec7e3dacd
TQID: https://experienceleague.adobe.com/AVN9LN-KzTpcMx-dexxN7i1i2nB4496dzSZ473a3NJE
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: c618a0dc-1818-4c6d-9916-0d92e6796f24id: d056adbe-402d-4f42-9746-f3d424e598b1
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094id: e9001ce2-5245-4a8e-8601-dd958009072f
source-git-commit: a5a700893cc89b29f5fbc214cf3e73f6069144c2
workflow-type: tm+mt
source-wordcount: 462
ht-degree: 0%

---

# Utilizza l’editor non visivo web {#web-non-visual-editor}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come aggiungere alle pagine web modifiche al selettore CSS e all&#39;intestazione senza installare un&#39;estensione del browser o caricare il Web Designer.

>[!ENDSHADEBOX]

Oltre al [!DNL Journey Optimizer] [Web Designer](web-visual-editor.md) visivo, puoi anche aggiungere modifiche alle pagine Web utilizzando un **editor non visivo**.

Questa funzione può essere utile se non è possibile installare estensioni del browser, ad esempio [Adobe Experience Cloud Visual Helper](web-prerequisites.md#visual-authoring-prerequisites), necessario per caricare le pagine nel Web Designer.

In alcuni casi, potrebbe essere più semplice utilizzare un editor non visivo per applicare modifiche a un particolare selettore CSS, senza il rischio di modificare altri elementi di una pagina web o di modificare la struttura della pagina.

Per creare le tue esperienze web con l’editor non visivo, segui i passaggi indicati di seguito.

1. Dalla schermata **[!UICONTROL Modifica contenuto]** nel percorso o nella campagna, deseleziona l&#39;opzione **[!UICONTROL Editor visivo]**.

1. Fai clic su **[!UICONTROL Aggiungi una modifica]** per iniziare a modificare il contenuto Web.

   ![](assets/web-campaign-add-modification-button.png)

1. Viene visualizzato l’editor non visivo. Puoi aggiungere la prima modifica utilizzando il riquadro a sinistra.

   ![](assets/web-non-visual-editor.png)

1. Nell’elenco a discesa, seleziona il tipo di modifica.

   Sono disponibili due tipi. Sono disponibili diverse opzioni. Per ulteriori informazioni, consulta i collegamenti seguenti:

   * **[!UICONTROL Selettore CSS]** - [Ulteriori informazioni](manage-web-modifications.md#css-selector)
   * **[!UICONTROL Pagina`<head>`]** - [Ulteriori informazioni](manage-web-modifications.md#page-head)

1. Fai clic sul pulsante **[!UICONTROL Aggiungi personalizzazione]**. Viene aperto l’editor di personalizzazione.

   Puoi sfruttare l&#39;editor di personalizzazione [!DNL Journey Optimizer] con tutte le sue funzionalità di personalizzazione e authoring. [Ulteriori informazioni](../personalization/personalization-build-expressions.md)

1. Inserisci il contenuto e **[!UICONTROL Salva]** le modifiche.

   ![](assets/web-non-visual-editor-ex-save.png)

1. La prima modifica viene visualizzata sopra il riquadro **[!UICONTROL Modifiche]**.

   Fai clic sul pulsante **[!UICONTROL Altre azioni]** accanto alla modifica e seleziona **[!UICONTROL Informazioni]** per visualizzarne i dettagli. Se necessario, puoi anche **[!UICONTROL Eliminare la modifica]**.

   ![](assets/web-non-visual-editor-ex-more.png){width="50%"}

   >[!NOTE]
   >
   >Il riquadro **[!UICONTROL Modifiche]** è identico a quello utilizzato per [Web Designer](web-visual-editor.md). Tutte le azioni che è possibile eseguire sono descritte in [questa sezione](manage-web-modifications.md#use-modifications-pane).

1. Fai clic sul pulsante **[!UICONTROL Aggiungi]** nella parte superiore del riquadro **[!UICONTROL Modifiche]** per aggiungere un&#39;altra modifica e ripeti i passaggi precedenti.


1. Inoltre, puoi selezionare qualsiasi elemento del sito web e tenere traccia dei clic su di esso. Per abilitare il tracciamento dei clic e definire le azioni da tracciare, fai clic sulla seconda icona nella barra a sinistra, come illustrato di seguito:

   ![](assets/web-campaign-click.png){width="50%"}

   Utilizza il pulsante **Aggiungi componente** per selezionare una nuova azione da tracciare. Ulteriori informazioni sull&#39;utilizzo del tracciamento dei clic in [questa sezione](monitor-web-experiences.md#use-click-tracking).


1. Fai clic sulla freccia in alto a sinistra dello schermo per tornare alla schermata dell’edizione del percorso o della campagna. Puoi visualizzare il numero corrente di modifiche e aggiungere altre modifiche.

   ![](assets/web-campaign-modifications.png)

   Se necessario, puoi anche passare al web designer. Tutte le modifiche verranno mantenute.
