---
title: Creare pagine web
description: Scopri come creare una pagina web e modificarne il contenuto in Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 3847ac1d-2c0a-4f80-8df9-e8e304faf261
badge: label="Beta" type="Informativo"
source-git-commit: 160e4ce03d3be975157c30fbe511875a85b00551
workflow-type: tm+mt
source-wordcount: '1110'
ht-degree: 6%

---

# Creare pagine web {#author-web}

>[!BEGINSHADEBOX]

Informazioni disponibili in questa documentazione:

* [Introduzione al canale Web](get-started-web.md)
* [Creare esperienze web](create-web.md)
* **[Creare pagine web](author-web.md)**
* [Estensione Helper per editing video](visual-editing-helper.md)
* [Generazione rapporti Web](web-report.md)

>[!ENDSHADEBOX]

In entrata [!DNL Journey Optimizer] l’authoring web è basato sull’estensione del browser chrome Adobe Experience Cloud Visual Helper. [Ulteriori informazioni](visual-editing-helper.md)

Per poter accedere e creare pagine web in [!DNL Journey Optimizer] , seguire i prerequisiti elencati in [questa sezione](create-web.md#prerequesites).

## Modificare il contenuto di una pagina web {#edit-web-content}

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_surface"
>title="Conferma l’URL da modificare"
>abstract="Conferma l’URL della pagina web specifica da utilizzare per la modifica del contenuto che verrà applicato alla superficie web definita sopra. La pagina web deve essere implementata utilizzando Adobe Experience Platform Web SDK."
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=it" text="Ulteriori informazioni"

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_rule"
>title="Inserisci l’URL da modificare"
>abstract="Inserisci l’URL di una pagina web specifica da utilizzare per modificare il contenuto che verrà applicato a tutte le pagine che corrispondono alla regola. La pagina web deve essere implementata utilizzando Adobe Experience Platform Web SDK."
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=it" text="Ulteriori informazioni"

<!--Confirm the URL to use for authoring content on the surface. Typically the Authoring URL will be the surface URL itself, but you may include extra parameters if required. The page must include the Adobe Experience Platform Web SDK.-->

Dopo aver creato un’azione web dalla campagna, puoi modificare il contenuto utilizzando il web designer. A questo scopo, segui i passaggi riportati qui sotto.

>[!CAUTION]
>
>Da accedere in [!DNL Journey Optimizer], la pagina web deve essere implementata utilizzando [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=it){target="_blank"}.

1. Dalla sezione **[!UICONTROL Azione]** scheda della campagna, seleziona **[!UICONTROL Modifica contenuto]** per iniziare a creare la tua campagna web.

1. Se hai creato una regola di corrispondenza pagine, devi immettere qualsiasi URL che corrisponda a questa regola. Le modifiche verranno applicate a tutte le pagine che corrispondono alla regola.

   >[!NOTE]
   >
   >Se hai inserito un singolo URL come superficie web, l’URL da personalizzare è già popolato.

   ![](assets/web-edit-enter-url.png)

1. Viene visualizzato il contenuto della pagina.

   >[!CAUTION]
   >
   >La pagina web deve includere [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=it){target="_blank"}.

1. Clic **[!UICONTROL Apri Web Designer]** per modificarlo. [Ulteriori informazioni](author-web.md)

   ![](assets/web-open-designer.png)

1. Viene visualizzato il web designer.

   ![](assets/web-designer.png)

1. Seleziona qualsiasi elemento dall’area di lavoro, ad esempio immagine, pulsante, paragrafo, testo, contenitore, intestazione, collegamento e così via. e utilizza:

   * Il menu contestuale per modificarne il contenuto, il layout, l’inserimento di collegamenti o la personalizzazione, ecc.

      ![](assets/web-designer-contextual-bar.png)

   * Le icone sopra il pannello di destra per modificare, duplicare, eliminare o nascondere ogni elemento.

      ![](assets/web-designer-right-panel-icons.png)

   * Pannello a destra che cambia dinamicamente in base all’elemento selezionato. Ad esempio, puoi modificare lo sfondo, la composizione tipografica, il bordo, le dimensioni, la posizione, la spaziatura, gli effetti o gli stili in linea di un elemento.

      ![](assets/web-designer-right-panel.png)

## Utilizzare i componenti per contenuti {#content-components}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_components"
>title="Aggiungere componenti di contenuto alla pagina web"
>abstract="Puoi aggiungere diversi componenti alla pagina web e modificarli in base alle tue esigenze."

1. Dalla sezione **[!UICONTROL Componenti]** sulla sinistra, puoi aggiungere i seguenti componenti alla pagina web e modificarli in base alle tue esigenze:

   * [Divisore](../email/content-components.md#divider)
   * [HTML](../email/content-components.md#HTML)
   * [Immagine](../email/content-components.md#image)
   * Intestazione: l’utilizzo di questo componente è simile all’utilizzo di **[!UICONTROL Testo]** componente in e-mail designer. [Ulteriori informazioni](../email/content-components.md#text)
   * Paragrafo: l’utilizzo di questo componente è simile all’utilizzo del **[!UICONTROL Testo]** componente in e-mail designer. [Ulteriori informazioni](../email/content-components.md#text)
   * Collegamento: scopri come definire lo stile dei collegamenti in [questa sezione](../email/styling-links.md)
   * [Decisione sull’offerta](../email/add-offers-email.md)

   ![](assets/web-designer-components.png)

1. Passa il puntatore del mouse sulla pagina e fai clic su **[!UICONTROL Inserisci prima]** o **[!UICONTROL Inserisci dopo]** per aggiungere il componente a un elemento esistente nella pagina.

   ![](assets/web-designer-insert-components.png)

1. Dal contenitore visualizzato per questo componente, modifica il contenuto del componente in base alle esigenze.

   ![](assets/web-designer-edit-html.png)

1. Regola gli stili visualizzati dalla **[!UICONTROL Contenitore]** riquadro a destra, ad esempio sfondo, colore del testo, bordo, dimensioni, posizione e così via. a seconda del componente selezionato.

   ![](assets/web-designer-html-style.png)

## Navigazione all&#39;interno del Web Designer

### Utilizzare le breadcrumb

1. Seleziona un elemento dall’area di lavoro.

1. Fai clic su **[!UICONTROL Espandi/comprimi breadcrumb]** in basso a sinistra per visualizzare rapidamente le informazioni sull’elemento selezionato.

   ![](assets/web-designer-breadcrumbs.png)

1. Quando passi il cursore del mouse sulle breadcrumb, l’elemento corrispondente viene evidenziato nell’editor.

1. Utilizzando questo elemento è possibile passare facilmente a qualsiasi elemento padre, di pari livello o figlio all’interno dell’editor visivo.

### Passa alla modalità Sfoglia {#browse-mode}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_browse"
>title="Utilizzare la modalità Sfoglia"
>abstract="Da questa modalità, puoi passare alla pagina esatta dalla superficie selezionata che desideri personalizzare."

È possibile sostituire il valore predefinito **[!UICONTROL Progettazione]** alla modalità **[!UICONTROL Sfoglia]** mediante il pulsante dedicato.

![](assets/web-designer-browse-mode.png)

Dalla sezione **[!UICONTROL Sfoglia]** in modalità, puoi passare alla pagina esatta dalla superficie selezionata che desideri personalizzare.

È particolarmente utile quando si tratta di pagine che sono dietro l’autenticazione o che non sono disponibili dall’inizio a un determinato URL. Ad esempio, potrai eseguire l’autenticazione, passare alla pagina dell’account o del carrello e quindi tornare a **[!UICONTROL Progettazione]** per eseguire le modifiche sulla pagina desiderata.

### Cambia dimensione dispositivo

È possibile impostare le dimensioni predefinite del dispositivo, ad esempio **[!UICONTROL Tablet]** o **[!UICONTROL Orizzontale mobile]** o definisci una dimensione personalizzata. Immetti il numero di pixel desiderato per definire una dimensione personalizzata.

È anche possibile cambiare la messa a fuoco dello zoom: da 25% a 400%.

![](assets/web-designer-device.png)

## Gestione modifiche {#manage-modifications}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_modifications"
>title="Gestione semplificata di tutte le modifiche"
>abstract="Utilizzando questo riquadro, puoi navigare e gestire tutte le regolazioni e gli stili aggiunti alla pagina web."

Puoi gestire facilmente tutti i componenti, le regolazioni e gli stili aggiunti alla pagina web.

1. Seleziona la **[!UICONTROL Modifiche]** per visualizzare il riquadro corrispondente a sinistra.

   ![](assets/web-designer-modifications-pane.png)

1. Puoi rivedere tutte le modifiche apportate alla pagina.

1. Seleziona una modifica indesiderata e fai clic sull’icona Elimina per rimuoverla.

   ![](assets/web-designer-modifications-delete.png)

   >[!CAUTION]
   >
   >Procedi con cautela durante l’eliminazione di un’azione, in quanto può influire sulle azioni successive.

1. Puoi anche annullare e ripristinare le azioni utilizzando **[!UICONTROL Annulla/Ripristina]** in alto a destra.

   ![](assets/web-designer-undo-redo.png)

   Fai clic e tieni premuto il pulsante per passare da un’icona all’altra **[!UICONTROL Annulla]** e **[!UICONTROL Ripeti]** opzioni. Quindi fai clic sul pulsante stesso per applicare l’azione desiderata.

## Aggiungere personalizzazione e offerte

Per aggiungere la personalizzazione, seleziona un contenitore e fai clic sull’icona di personalizzazione dalla barra dei menu contestuale visualizzata. Aggiungi le modifiche utilizzando l’editor espressioni. [Ulteriori informazioni](../personalization/personalization-build-expressions.md)

![](assets/web-designer-personalization.png)

Utilizza il **[!UICONTROL Decisione sull’offerta]** componente da inserire [offerte](../offers/get-started/starting-offer-decisioning.md) nelle pagine web. Il processo è lo stesso di quando [aggiunta di un’offerta a un’e-mail](../email/add-offers-email.md). Sfrutterà la funzione di gestione delle decisioni per scegliere l’offerta migliore da offrire ai clienti.

![](assets/web-designer-offer.png)

## Testare la campagna web {#test-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_preview"
>title="Visualizzare l’anteprima della tua esperienza web"
>abstract="Ottieni una simulazione dell’aspetto della tua esperienza web."

Per visualizzare un’anteprima della tua esperienza web modificata, segui i passaggi indicati di seguito.

>[!CAUTION]
>
>Devi disporre di profili di test per simulare quali offerte verranno consegnate. Scopri come [creare profili di test](../segment/creating-test-profiles.md).

1. Da una delle due opzioni **[!UICONTROL Modifica contenuto]** o il web designer, seleziona **[!UICONTROL Simula contenuto]**.

   ![](assets/web-designer-simulate.png)

1. Clic **[!UICONTROL Gestire i profili di test]** per selezionare uno o più profili di test.
1. Viene visualizzata un’anteprima della pagina web modificata.

   ![](assets/web-designer-preview.png)

1. Puoi anche copiare l’URL di prova per incollarlo in qualsiasi browser, oppure aprirlo nel browser predefinito.
