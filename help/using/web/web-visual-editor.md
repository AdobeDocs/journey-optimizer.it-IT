---
title: Modificare il contenuto mediante il Web Designer
description: Scopri come creare una pagina web e modificarne il contenuto utilizzando l’editor web di Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: 98e99978-8538-40b4-92ac-7184864017eb
source-git-commit: 25b1e6050e0cec3ae166532f47626d99ed68fe80
workflow-type: tm+mt
source-wordcount: '934'
ht-degree: 8%

---

# Utilizzare il Designer web {#work-with-web-designer}

<!--
>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_surface"
>title="Confirm the URL to edit"
>abstract="Confirm the URL of the specific web page to use for editing the content that will be applied on the web configuration defined above. The web page must be implemented using the Adobe Experience Platform Web SDK."
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=it" text="Learn more"

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_rule"
>title="Enter the URL to edit"
>abstract="Enter the URL of a specific web page to use for editing the content that will be applied to all pages matching the rule. The web page must be implemented using Adobe Experience Platform Web SDK."
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=it" text="Learn more"
-->

In [!DNL Journey Optimizer], l&#39;authoring Web visivo è basato sull&#39;estensione del browser Chrome **Adobe Experience Cloud Visual Helper**. [Ulteriori informazioni](web-prerequisites.md#visual-authoring-prerequisites)

>[!CAUTION]
>
>Per poter accedere alle pagine Web e crearle nell&#39;interfaccia utente [!DNL Journey Optimizer], assicurarsi di seguire i prerequisiti elencati in [questa sezione](web-prerequisites.md).

## Inizia a creare la tua esperienza web

Per iniziare a creare la tua esperienza web utilizzando il designer Web visivo, segui i passaggi indicati di seguito.

>[!CAUTION]
>
>Il [SDK Web Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=it){target="_blank"} deve essere incluso nella pagina Web. [Ulteriori informazioni](web-prerequisites.md#implementation-prerequisites)

1. Dalla schermata **[!UICONTROL Modifica contenuto]**, fare clic su **[!UICONTROL Modifica pagina Web]** per aprire la finestra di progettazione Web.

   ![](assets/web-campaign-edit-web-page.png)

   <!--![](assets/web-designer.png)-->

   >[!NOTE]
   >
   >Se il caricamento di un sito Web non riesce, viene visualizzato un messaggio per suggerirti di installare l&#39;[estensione del browser Helper per editing video](#install-visual-editing-helper). Consulta alcuni suggerimenti per la risoluzione dei problemi in [questa sezione](web-prerequisites.md#troubleshooting).
   >
   >Puoi anche modificare il contenuto web senza caricare l’editor visivo. Per eseguire questa operazione, deselezionare l&#39;opzione **[!UICONTROL Editor visivo]** per utilizzare la modalità di modifica non visiva. [Ulteriori informazioni](web-non-visual-editor.md)

1. Una volta nella finestra di progettazione web, seleziona qualsiasi elemento dall’area di lavoro, ad esempio immagine, pulsante, paragrafo, testo, contenitore, intestazione, collegamento e così via. [Ulteriori informazioni](#content-components)

1. Per modificare un elemento, puoi utilizzare:

   * Il menu contestuale per modificarne il contenuto, il layout, l’inserimento di collegamenti o la personalizzazione, ecc.

     ![](assets/web-designer-contextual-bar.png)

   * Le icone sopra il pannello di destra per modificare, duplicare, eliminare o nascondere ogni elemento.

     ![](assets/web-designer-right-panel-icons.png)

   * Pannello a destra che cambia dinamicamente in base all’elemento selezionato. Ad esempio, puoi modificare lo sfondo, la composizione tipografica, il bordo, le dimensioni, la posizione, la spaziatura, gli effetti o gli stili in linea di un elemento.

     ![](assets/web-designer-right-panel.png)

>[!NOTE]
>
>Il designer di contenuti web è per lo più simile a E-mail Designer. Ulteriori informazioni sulla [progettazione di contenuti con [!DNL Journey Optimizer]](../email/get-started-email-design.md).

Dopo aver modificato il contenuto web, puoi gestire le modifiche. [Ulteriori informazioni](manage-web-modifications.md)

## Utilizzare i componenti {#content-components}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_components"
>title="Aggiungere componenti alla pagina web"
>abstract="Puoi aggiungere diversi componenti alla pagina web e modificarli in base alle tue esigenze."

1. Selezionare un elemento dal riquadro **[!UICONTROL Componenti]** a sinistra. Puoi aggiungere i seguenti componenti alla pagina web e modificarli in base alle tue esigenze:

   * [Divisore](../email/content-components.md#divider)
   * [HTML](../email/content-components.md#HTML)
   * [Immagine](../email/content-components.md#image)
   * Intestazione - L&#39;utilizzo di questo componente è simile all&#39;utilizzo del componente **[!UICONTROL Testo]** nel Designer e-mail. [Ulteriori informazioni](../email/content-components.md#text)
   * Paragrafo - L&#39;utilizzo di questo componente è simile all&#39;utilizzo del componente **[!UICONTROL Testo]** nel Designer e-mail. [Ulteriori informazioni](../email/content-components.md#text)
   * Collegamento

   ![](assets/web-designer-components.png)

1. Passa il mouse sulla pagina e fai clic sul pulsante **[!UICONTROL Inserisci prima]** o **[!UICONTROL Inserisci dopo]** per aggiungere il componente a un elemento esistente nella pagina.

   ![](assets/web-designer-insert-components.png)

   >[!NOTE]
   >
   >Per deselezionare un componente, fare clic sul pulsante **[!UICONTROL ESC]** nel banner contestuale blu visualizzato sopra l&#39;area di lavoro.

1. Modifica il componente in base alle esigenze direttamente nel contenuto della pagina.

   ![](assets/web-designer-edit-header.png)

1. Regola gli stili visualizzati dal riquadro contestuale a destra, ad esempio sfondo, colore del testo, bordo, dimensione, posizione e così via. - a seconda del componente selezionato.

   ![](assets/web-designer-header-style.png)

## Aggiungere personalizzazione

Per aggiungere la personalizzazione, seleziona un contenitore e fai clic sull’icona di personalizzazione dalla barra dei menu contestuale visualizzata. Aggiungi le modifiche utilizzando l’editor di personalizzazione. [Ulteriori informazioni](../personalization/personalization-build-expressions.md)

![](assets/web-designer-personalization.png)

## Navigazione all&#39;interno del Web Designer {#navigate-web-designer}

In questa sezione vengono descritti i diversi modi in cui è possibile spostarsi all&#39;interno del designer Web. Per visualizzare e gestire le modifiche aggiunte alla tua esperienza Web, consulta [questa sezione](manage-web-modifications.md).

### Utilizzare le breadcrumb {#breadcrumbs}

1. Seleziona un elemento dall’area di lavoro.

1. Fai clic sul pulsante **[!UICONTROL Espandi/comprimi breadcrumb]** in basso a sinistra dello schermo per visualizzare rapidamente le informazioni sull&#39;elemento selezionato.

   ![](assets/web-designer-breadcrumbs.png)

1. Quando passi il cursore del mouse sulle breadcrumb, l’elemento corrispondente viene evidenziato nell’editor.

1. Utilizzando questo elemento è possibile passare facilmente a qualsiasi elemento padre, di pari livello o figlio all’interno dell’editor visivo.

### Passare alla modalità sfoglia {#browse-mode}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_browse"
>title="Utilizzare la modalità Sfoglia"
>abstract="Da questa modalità puoi passare alla pagina esatta dalla configurazione selezionata che desideri personalizzare."

È possibile passare dalla modalità predefinita **[!UICONTROL Progettazione]** alla modalità **[!UICONTROL Sfoglia]** utilizzando il pulsante dedicato.

![](assets/web-designer-browse-mode.png)

Dalla modalità **[!UICONTROL Sfoglia]**, puoi passare alla pagina esatta dalla configurazione selezionata che desideri personalizzare.

È particolarmente utile quando si tratta di pagine che sono dietro l’autenticazione o che non sono disponibili dall’inizio a un determinato URL. Ad esempio, potrai eseguire l&#39;autenticazione, passare alla pagina dell&#39;account o alla pagina del carrello e quindi tornare alla modalità **[!UICONTROL Progettazione]** per eseguire le modifiche nella pagina desiderata.

L&#39;utilizzo della modalità **[!UICONTROL Sfoglia]** consente inoltre di spostarsi tra tutte le visualizzazioni del sito Web durante la creazione di applicazioni a pagina singola. [Ulteriori informazioni](web-spa.md)

### Cambia dimensione dispositivo {#change-device-size}

È possibile modificare le dimensioni del dispositivo della visualizzazione del Web designer impostando una dimensione predefinita, ad esempio **[!UICONTROL Tablet]** o **[!UICONTROL Orizzontale mobile]**, oppure definire una dimensione personalizzata immettendo il numero di pixel desiderato.

È anche possibile cambiare la messa a fuoco dello zoom: da 25% a 400%.

![](assets/web-designer-device.png)

La possibilità di modificare le dimensioni del dispositivo è progettata per i siti reattivi con un rendering ottimale su vari dispositivi, finestre e dimensioni di schermo. I siti reattivi si adattano automaticamente a qualsiasi dimensione di schermo, inclusi desktop, laptop, tablet o telefoni cellulari.

>[!CAUTION]
>
>Puoi modificare un’esperienza web con una dimensione dispositivo specifica. Tuttavia, se i selettori sono gli stessi, queste modifiche si applicano a tutte le dimensioni e ai dispositivi, non solo alle dimensioni del dispositivo in cui stai lavorando. Analogamente, la modifica di un’esperienza nella normale visualizzazione desktop applica le modifiche a tutte le dimensioni di schermo, non solo alla visualizzazione desktop.
>
>Attualmente, [!DNL Journey Optimizer] non supporta le modifiche di pagina specifiche per le dimensioni del dispositivo. Ciò significa che, ad esempio, se disponi di un sito web mobile separato con una struttura del sito separata, dovrai apportare le modifiche specifiche al sito mobile in un’altra campagna.

## Video dimostrativo{#video}

Il video seguente mostra come creare un&#39;esperienza Web utilizzando il designer Web nelle campagne [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3418803/?quality=12&learn=on)
