---
title: Modificare il contenuto web
description: Scopri come creare una pagina web e modificarne il contenuto in Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: 3847ac1d-2c0a-4f80-8df9-e8e304faf261
source-git-commit: ec071392cec9933bb73ae9ab20618292b6089061
workflow-type: tm+mt
source-wordcount: '1093'
ht-degree: 17%

---

# Modificare il contenuto web {#edit-web-content}

Una volta [ha aggiunto un’azione web](create-web.md#create-web-campaign) nella campagna, puoi modificare il contenuto del sito utilizzando web designer.

[Scopri come creare una campagna web in questo video](#video)

In entrata [!DNL Journey Optimizer], l’authoring web è basato su **Helper visivo Adobe Experience Cloud** estensione del browser chrome. [Ulteriori informazioni](web-prerequisites.md#visual-authoring-prerequisites)

>[!CAUTION]
>
>Per poter accedere e creare pagine web in [!DNL Journey Optimizer] nell&#39;interfaccia utente, assicurarsi di seguire i prerequisiti elencati in [questa sezione](web-prerequisites.md).

Per ulteriori informazioni su ciascun argomento, consulta le sezioni seguenti:

* [Gestione modifiche](manage-web-modifications.md)

* [Monitorare le campagne web](monitor-web-campaigns.md)

## Utilizzare il web designer {#work-with-web-designer}

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_surface"
>title="Confermare l’URL per la modifica"
>abstract="Conferma l’URL della pagina web specifica da utilizzare per modificare il contenuto che verrà applicato sulla superficie web definita sopra. La pagina web deve essere implementata utilizzando Adobe Experience Platform Web SDK."
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=it" text="Ulteriori informazioni"

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_rule"
>title="Immettere l’URL per la modifica"
>abstract="Immetti l’URL di una pagina web specifica da utilizzare per modificare il contenuto che verrà applicato a tutte le pagine che corrispondono alla regola. La pagina web deve essere implementata utilizzando l’SDK per web di Adobe Experience Platform."
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=it" text="Ulteriori informazioni"

Per iniziare a creare la tua campagna web, segui i passaggi indicati di seguito.

1. Dalla sezione **[!UICONTROL Azione]** scheda di [campagna](create-web.md#create-web-campaign), seleziona **[!UICONTROL Modifica contenuto]**.<!--change screen with rule-->

   ![](assets/web-campaign-edit-content.png)

1. Se hai creato una regola di corrispondenza pagine, devi immettere un URL che corrisponda a questa regola: le modifiche verranno applicate a tutte le pagine che corrispondono alla regola. Viene visualizzato il contenuto della pagina.

   >[!NOTE]
   >
   >Se hai inserito un singolo URL come superficie web, l’URL da personalizzare è già popolato.

   ![](assets/web-edit-enter-url.png)

   >[!CAUTION]
   >
   >La pagina web deve includere [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=it){target="_blank"}. [Ulteriori informazioni](web-prerequisites.md#implementation-prerequisites)

1. Clic **[!UICONTROL Modifica pagina web]** per iniziare a crearlo. Viene visualizzato il web designer.

   ![](assets/web-designer.png)

   >[!NOTE]
   >
   >Se il caricamento di un sito web non riesce, viene visualizzato un messaggio per suggerirti di installare il [Estensione del browser Helper per editing video](#install-visual-editing-helper). Consulta alcuni suggerimenti per la risoluzione dei problemi in [questa sezione](web-prerequisites.md#troubleshooting).

1. Seleziona qualsiasi elemento dall’area di lavoro, ad esempio immagine, pulsante, paragrafo, testo, contenitore, intestazione, collegamento e così via. [Ulteriori informazioni](#content-components)

1. Seleziona:

   * Il menu contestuale per modificarne il contenuto, il layout, l’inserimento di collegamenti o la personalizzazione, ecc.

     ![](assets/web-designer-contextual-bar.png)

   * Le icone sopra il pannello di destra per modificare, duplicare, eliminare o nascondere ogni elemento.

     ![](assets/web-designer-right-panel-icons.png)

   * Pannello a destra che cambia dinamicamente in base all’elemento selezionato. Ad esempio, puoi modificare lo sfondo, la composizione tipografica, il bordo, le dimensioni, la posizione, la spaziatura, gli effetti o gli stili in linea di un elemento.

     ![](assets/web-designer-right-panel.png)

>[!NOTE]
>
>Il designer del contenuto web è per lo più simile al designer e-mail. Ulteriori informazioni su [progettazione di contenuti con [!DNL Journey Optimizer]](../email/get-started-email-design.md).

## Utilizzare i componenti {#content-components}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_components"
>title="Aggiungere componenti alla pagina web"
>abstract="Puoi aggiungere diversi componenti alla pagina web e modificarli in base alle tue esigenze."

1. Dalla sezione **[!UICONTROL Componenti]** a sinistra, selezionare un elemento. Puoi aggiungere i seguenti componenti alla pagina web e modificarli in base alle tue esigenze:

   * [Divisore](../email/content-components.md#divider)
   * [HTML](../email/content-components.md#HTML)
   * [Immagine](../email/content-components.md#image)
   * Intestazione: l’utilizzo di questo componente è simile all’utilizzo di **[!UICONTROL Testo]** componente in e-mail designer. [Ulteriori informazioni](../email/content-components.md#text)
   * Paragrafo: l’utilizzo di questo componente è simile all’utilizzo del **[!UICONTROL Testo]** componente in e-mail designer. [Ulteriori informazioni](../email/content-components.md#text)
   * Collegamento
   * [Decisione sull’offerta](../email/add-offers-email.md)

   ![](assets/web-designer-components.png)

1. Passa il puntatore del mouse sulla pagina e fai clic su **[!UICONTROL Inserisci prima]** o **[!UICONTROL Inserisci dopo]** per aggiungere il componente a un elemento esistente nella pagina.

   ![](assets/web-designer-insert-components.png)

   >[!NOTE]
   >
   >Per deselezionare un componente, fai clic su **[!UICONTROL ESC]** nel banner contestuale blu visualizzato nella parte superiore dell’area di lavoro.

1. Modifica il componente in base alle esigenze direttamente nel contenuto della pagina.

   ![](assets/web-designer-edit-header.png)

1. Regola gli stili visualizzati dal riquadro contestuale a destra, ad esempio sfondo, colore del testo, bordo, dimensione, posizione e così via. - a seconda del componente selezionato.

   ![](assets/web-designer-header-style.png)

## Aggiungere personalizzazione e offerte

Per aggiungere la personalizzazione, seleziona un contenitore e fai clic sull’icona di personalizzazione dalla barra dei menu contestuale visualizzata. Aggiungi le modifiche utilizzando l’editor espressioni. [Ulteriori informazioni](../personalization/personalization-build-expressions.md)

![](assets/web-designer-personalization.png)

Utilizza il **[!UICONTROL Decisione sull’offerta]** componente da inserire [offerte](../offers/get-started/starting-offer-decisioning.md) nelle pagine web. Il processo è lo stesso di quando [aggiunta di un’offerta a un’e-mail](../email/add-offers-email.md). Sfrutterà la funzione di gestione delle decisioni per scegliere l’offerta migliore da offrire ai clienti.

![](assets/web-designer-offer.png)

## Navigazione all&#39;interno del Web Designer {#navigate-web-designer}

In questa sezione vengono descritti i diversi modi in cui è possibile spostarsi all&#39;interno del designer Web. Per visualizzare e gestire le modifiche aggiunte all’esperienza web, consulta [questa sezione](manage-web-modifications.md).

### Utilizzare le breadcrumb {#breadcrumbs}

1. Seleziona un elemento dall’area di lavoro.

1. Fai clic su **[!UICONTROL Espandi/comprimi breadcrumb]** in basso a sinistra per visualizzare rapidamente le informazioni sull’elemento selezionato.

   ![](assets/web-designer-breadcrumbs.png)

1. Quando passi il cursore del mouse sulle breadcrumb, l’elemento corrispondente viene evidenziato nell’editor.

1. Utilizzando questo elemento è possibile passare facilmente a qualsiasi elemento padre, di pari livello o figlio all’interno dell’editor visivo.

### Passa alla modalità Sfoglia {#browse-mode}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_browse"
>title="Utilizzare la modalità Sfoglia"
>abstract="Da questa modalità puoi passare alla pagina esatta dalla superficie selezionata che desideri personalizzare."

È possibile sostituire il valore predefinito **[!UICONTROL Progettazione]** alla modalità **[!UICONTROL Sfoglia]** mediante il pulsante dedicato.

![](assets/web-designer-browse-mode.png)

Dalla sezione **[!UICONTROL Sfoglia]** in modalità, puoi passare alla pagina esatta dalla superficie selezionata che desideri personalizzare.

È particolarmente utile quando si tratta di pagine che sono dietro l’autenticazione o che non sono disponibili dall’inizio a un determinato URL. Ad esempio, potrai eseguire l’autenticazione, passare alla pagina dell’account o del carrello e quindi tornare a **[!UICONTROL Progettazione]** per eseguire le modifiche sulla pagina desiderata.

### Cambia dimensione dispositivo {#change-device-size}

È possibile impostare le dimensioni del dispositivo della visualizzazione del Web Designer su una dimensione predefinita, ad esempio **[!UICONTROL Tablet]** o **[!UICONTROL Orizzontale mobile]**, o definisci una dimensione personalizzata immettendo il numero di pixel desiderato.

È anche possibile cambiare la messa a fuoco dello zoom: da 25% a 400%.

![](assets/web-designer-device.png)

La possibilità di modificare le dimensioni del dispositivo è progettata per i siti reattivi con un rendering ottimale su vari dispositivi, finestre e dimensioni di schermo. I siti reattivi si adattano automaticamente a qualsiasi dimensione di schermo, compresi desktop, laptop, tablet o telefoni cellulari.

>[!CAUTION]
>
>Puoi modificare un’esperienza web con una dimensione dispositivo specifica. Tuttavia, se i selettori sono gli stessi, queste modifiche si applicano a tutte le dimensioni e ai dispositivi, non solo alle dimensioni del dispositivo in cui stai lavorando. Analogamente, la modifica di un’esperienza nella normale visualizzazione desktop applica le modifiche a tutte le dimensioni di schermo, non solo alla visualizzazione desktop.
>
>Attualmente, [!DNL Journey Optimizer] non supporta le modifiche di pagina specifiche per le dimensioni del dispositivo. Ciò significa che, ad esempio, se disponi di un sito web mobile separato con una struttura del sito separata, dovrai apportare le modifiche specifiche al sito mobile in un’altra campagna.

## Video introduttivo{#video}

Il video seguente mostra come creare un’esperienza web utilizzando il designer web in [!DNL Journey Optimizer] campagne.

>[!VIDEO](https://video.tv.adobe.com/v/3418803/?quality=12&learn=on)