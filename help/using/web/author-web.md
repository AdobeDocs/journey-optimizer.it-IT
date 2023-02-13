---
title: Creare pagine web
description: Scopri come creare una pagina web e modificarne il contenuto in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 3847ac1d-2c0a-4f80-8df9-e8e304faf261
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '1097'
ht-degree: 5%

---

# Creare pagine web {#author-web}

>[!AVAILABILITY]
>
>La funzione canale web è attualmente disponibile come versione beta solo per gli utenti selezionati.

In [!DNL Journey Optimizer] l&#39;authoring web è basato sull&#39;estensione del browser Adobe Experience Cloud Visual Helper chrome. [Ulteriori informazioni](visual-editing-helper.md)

Per accedere e creare pagine web nel [!DNL Journey Optimizer] interfaccia utente, segui i prerequisiti elencati in [questa sezione](create-web.md#prerequesites).

## Modifica del contenuto della pagina web {#edit-web-content}

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_surface"
>title="Immettere l&#39;URL da modificare"
>abstract="Inserisci l’URL di una pagina web specifica da utilizzare per modificare il contenuto che verrà applicato sulla superficie web definita sopra. La pagina web deve essere implementata utilizzando l’SDK per web di Adobe Experience Platform."
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=it" text="Per saperne di più"

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_rule"
>title="Immettere l&#39;URL da modificare"
>abstract="Inserisci l’URL di una pagina web specifica da utilizzare per modificare il contenuto che verrà applicato a tutte le pagine che corrispondono alla regola. La pagina web deve essere implementata tramite Adobe Experience Platform Web SDK."
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=it" text="Per saperne di più"

<!--Confirm the URL to use for authoring content on the surface. Typically the Authoring URL will be the surface URL itself, but you may include extra parameters if required. The page must include the Adobe Experience Platform Web SDK.-->

Una volta creata un’azione web dalla campagna, è possibile modificarne il contenuto utilizzando il web designer. A questo scopo, segui i passaggi riportati qui sotto.

>[!CAUTION]
>
>Per accedere a [!DNL Journey Optimizer], la pagina web deve essere implementata utilizzando [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=it){target="_blank"}.

1. Da **[!UICONTROL Azione]** scheda della campagna, seleziona **[!UICONTROL Modifica contenuto]** per iniziare a creare la campagna web.

1. Se hai creato una regola di corrispondenza per le pagine, devi immettere qualsiasi URL che corrisponda a questa regola. Le modifiche verranno applicate a tutte le pagine che corrispondono alla regola.

   >[!NOTE]
   >
   >Se hai inserito un singolo URL come superficie web, l’URL da personalizzare è già popolato.

   ![](assets/web-edit-enter-url.png)

1. Viene visualizzato il contenuto della pagina.

   >[!CAUTION]
   >
   >La pagina web deve includere [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=it){target="_blank"}.

1. Fai clic su **[!UICONTROL Apri web designer]** per modificarlo. [Ulteriori informazioni](author-web.md)

   ![](assets/web-open-designer.png)

1. Viene visualizzato il web designer.

   ![](assets/web-designer.png)

1. Seleziona qualsiasi elemento dall’area di lavoro, ad esempio immagine, pulsante, paragrafo, testo, contenitore, intestazione, collegamento e così via. e utilizzare:

   * Il menu contestuale per modificarne il contenuto, il layout, l’inserimento di collegamenti o la personalizzazione, ecc.

      ![](assets/web-designer-contextual-bar.png)

   * Le icone nella parte superiore destra del pannello consentono di modificare, duplicare, eliminare o nascondere ogni elemento.

      ![](assets/web-designer-right-panel-icons.png)

   * Il pannello di destra che cambia dinamicamente in base all’elemento selezionato. Ad esempio, puoi modificare lo sfondo, la composizione tipografica, il bordo, le dimensioni, la posizione, la spaziatura, gli effetti o gli stili in linea di un elemento.

      ![](assets/web-designer-right-panel.png)

## Utilizzare i componenti per contenuti {#content-components}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_components"
>title="Aggiungere componenti di contenuto alla pagina web"
>abstract="Puoi aggiungere diversi componenti alla pagina web e modificarli in base alle tue esigenze."

1. Da **[!UICONTROL Componenti]** a sinistra, puoi aggiungere i seguenti componenti alla pagina web e modificarli in base alle tue esigenze:

   * [Divisore](../email/content-components.md#divider)
   * [HTML](../email/content-components.md#HTML)
   * [Immagine](../email/content-components.md#image)
   * Intestazione : l’utilizzo di questo componente è simile all’utilizzo del comando **[!UICONTROL Testo]** in e-mail designer. [Ulteriori informazioni](../email/content-components.md#text)
   * Paragrafo - L’utilizzo di questo componente è simile a quello dell’utilizzo del **[!UICONTROL Testo]** in e-mail designer. [Ulteriori informazioni](../email/content-components.md#text)
   * Collegamento : scopri come definire lo stile dei collegamenti in [questa sezione](../email/styling-links.md)
   * [Decisione di offerta](../email/add-offers-email.md)

   ![](assets/web-designer-components.png)

1. Passa il puntatore del mouse sulla pagina e fai clic sul pulsante **[!UICONTROL Inserisci prima]** o **[!UICONTROL Inserisci dopo]** per aggiungere il componente a un elemento esistente nella pagina.

   ![](assets/web-designer-insert-components.png)

1. Dal contenitore visualizzato per questo componente, modifica il contenuto del componente in base alle esigenze.

   ![](assets/web-designer-edit-html.png)

1. Regolare gli stili visualizzati dalla **[!UICONTROL Contenitore]** a destra, ad esempio sfondo, colore del testo, bordo, dimensione, posizione, ecc. a seconda del componente selezionato.

   ![](assets/web-designer-html-style.png)

## Navigare nel web designer

### Utilizzare le breadcrumb

1. Seleziona qualsiasi elemento dall’area di lavoro.

1. Fai clic sul pulsante **[!UICONTROL Espandi/comprimi breadcrumb]** pulsante in basso a sinistra dello schermo per visualizzare rapidamente le informazioni sull’elemento selezionato.

   ![](assets/web-designer-breadcrumbs.png)

1. Quando passi il cursore del mouse sulle breadcrumb, l’elemento corrispondente viene evidenziato nell’editor.

1. Puoi facilmente passare a qualsiasi elemento principale, di pari livello o secondario all’interno dell’editor visivo.

### Scambio in modalità Sfoglia {#browse-mode}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_browse"
>title="Utilizzare la modalità Sfoglia"
>abstract="Da questa modalità è possibile passare alla pagina esatta dalla superficie selezionata che si desidera personalizzare."

È possibile eseguire lo scambio dal valore predefinito **[!UICONTROL Progettazione]** alla modalità **[!UICONTROL Sfoglia]** utilizzando il pulsante dedicato.

![](assets/web-designer-browse-mode.png)

Da **[!UICONTROL Sfoglia]** In questa modalità, puoi passare alla pagina esatta dalla superficie selezionata che desideri personalizzare.

È particolarmente utile quando si tratta di pagine che si trovano dietro l’autenticazione o che non sono disponibili dall’inizio in un determinato URL. Ad esempio, potrai eseguire l’autenticazione, passare alla pagina dell’account o alla pagina del carrello e quindi tornare a **[!UICONTROL Progettazione]** per eseguire le modifiche desiderate nella pagina desiderata.

### Modificare le dimensioni del dispositivo

È possibile modificare le dimensioni del dispositivo in una dimensione predefinita, ad esempio **[!UICONTROL Tablet]** o **[!UICONTROL Panorama mobile]** o definire una dimensione personalizzata. Immetti il numero desiderato di pixel per definire una dimensione personalizzata.

È inoltre possibile modificare la messa a fuoco dello zoom dal 25% al 400%.

![](assets/web-designer-device.png)

## Gestione delle modifiche {#manage-modifications}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_modifications"
>title="Gestione semplice di tutte le modifiche"
>abstract="Utilizzando questo riquadro, puoi navigare tra e gestire tutte le regolazioni e gli stili aggiunti alla pagina web."

Puoi gestire facilmente tutti i componenti, le regolazioni e gli stili aggiunti alla pagina web.

1. Seleziona la **[!UICONTROL Modifiche]** per visualizzare il riquadro corrispondente a sinistra.

   ![](assets/web-designer-modifications-pane.png)

1. Puoi rivedere ciascuna delle modifiche apportate alla pagina.

1. Seleziona una modifica indesiderata e fai clic sull’icona Elimina per rimuoverla.

   ![](assets/web-designer-modifications-delete.png)

   >[!CAUTION]
   >
   >Procedi con cautela durante l’eliminazione di un’azione in quanto potrebbe influenzare le azioni successive.

1. È inoltre possibile annullare e ripristinare le azioni utilizzando **[!UICONTROL Annulla/Ripristina]** in alto a destra dello schermo.

   ![](assets/web-designer-undo-redo.png)

   Fai clic e tieni premuto il pulsante per passare dalla **[!UICONTROL Annulla]** e **[!UICONTROL Ripeti]** opzioni. Quindi fai clic sul pulsante stesso per applicare l’azione desiderata.

## Aggiungere personalizzazione e offerte

Per aggiungere la personalizzazione, seleziona un contenitore e fai clic sull’icona di personalizzazione nella barra dei menu contestuale visualizzata. Aggiungi le modifiche utilizzando l’editor espressioni. [Ulteriori informazioni](../personalization/personalization-build-expressions.md)

![](assets/web-designer-personalization.png)

Utilizza la **[!UICONTROL Decisione di offerta]** componente da inserire [offerte](../offers/get-started/starting-offer-decisioning.md) nelle pagine web. Il processo è lo stesso di quando [aggiunta di un’offerta a un messaggio e-mail](../email/add-offers-email.md). Utilizza la Gestione delle decisioni per scegliere l&#39;offerta migliore da consegnare ai tuoi clienti.

![](assets/web-designer-offer.png)

## Test della campagna web {#test-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_preview"
>title="Visualizzare in anteprima l&#39;esperienza web"
>abstract="Ottieni una simulazione dell’aspetto della tua esperienza web."

Per visualizzare un’anteprima dell’esperienza web modificata, segui i passaggi riportati di seguito.

>[!CAUTION]
>
>Devi disporre di profili di test per simulare quali offerte verranno consegnate loro. Scopri come [creare profili di test](../segment/creating-test-profiles.md).

1. Da **[!UICONTROL Modifica contenuto]** schermata o web designer, seleziona **[!UICONTROL Simulazione del contenuto]**.

   ![](assets/web-designer-simulate.png)

1. Fai clic su **[!UICONTROL Gestire i profili di test]** per selezionare uno o più profili di test.
1. Viene visualizzata un’anteprima della pagina web modificata.

   ![](assets/web-designer-preview.png)

1. Puoi anche copiare l’URL di test per incollarlo in qualsiasi browser, oppure aprirlo nel browser predefinito.
