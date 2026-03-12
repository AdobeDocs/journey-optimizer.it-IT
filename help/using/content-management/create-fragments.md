---
solution: Journey Optimizer
product: journey optimizer
title: Creare un frammento
description: Scopri come creare frammenti per riutilizzare i contenuti nelle campagne e nei percorsi di Journey Optimizer
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: da3ffe9c-a244-4246-b4b5-a3a1d0508676
source-git-commit: 449e8c9c1df7942346bcc94195aee89f2ecbc8f6
workflow-type: tm+mt
source-wordcount: '802'
ht-degree: 21%

---

# Creare un frammento {#create-fragments}

>[!CONTEXTUALHELP]
>id="ajo_create_visual_fragment"
>title="Seleziona il tipo visivo"
>abstract="Crea un frammento visivo autonomo per rendere il contenuto riutilizzabile in un messaggio e-mail all’interno di un percorso, di una campagna o di un modello di contenuto."
>additional-url="https://experienceleague.adobe.com/it/docs/journey-optimizer/using/channels/email/design-email/add-content/use-visual-fragments" text="Aggiungere frammenti visivi alle e-mail"

>[!CONTEXTUALHELP]
>id="ajo_create_expression_fragment"
>title="Seleziona il tipo di espressione"
>abstract="Crea da zero un frammento di espressione autonomo per rendere i contenuti riutilizzabili in più percorsi e campagne. Quando utilizzi l’editor di personalizzazione, puoi sfruttare tutti i frammenti di espressione che sono stati creati nella sandbox corrente."
>additional-url="https://experienceleague.adobe.com/it/docs/journey-optimizer/using/content-management/personalization/personalization-build-expressions" text="Utilizzare l’editor di personalizzazione"

I frammenti possono essere creati da zero dal menu a sinistra **[!UICONTROL Frammenti]**. Inoltre, durante la progettazione di contenuto, è possibile anche salvare una parte del contenuto esistente come frammento. [Scopri come](save-fragments.md#)

Una volta salvato, il frammento è disponibile per l&#39;uso in un viaggio, una campagna o un modello. Puoi utilizzare questo frammento quando crei qualsiasi contenuto all&#39;interno di percorsi e campagne. Vedere [Aggiungere frammenti visivi](../email/use-visual-fragments.md) e [Utilizzare i frammenti di espressione](../personalization/use-expression-fragments.md).

Per creare un frammento, effettuate le seguenti operazioni.

## Definire le proprietà del frammento {#properties}

1. Accedere all&#39;elenco dei frammenti dal menu a sinistra **[!UICONTROL Gestione contenuto]** > **[!UICONTROL Frammenti]**.

1. Selezionare **[!UICONTROL Crea frammento]** e immettere il nome e la descrizione del frammento (se necessario).

   ![](assets/fragment-details.png)

1. Selezionate o create tag Adobe Experience Platform dal campo **[!UICONTROL Tag]** per classificare il frammento per una ricerca migliorata. [Scopri come utilizzare i tag unificati](../start/search-filter-categorize.md#tags)

1. Selezionare il tipo di frammento: **Frammento visivo** o **Frammento espressione**. [Ulteriori informazioni](../content-management/fragments.md#visual-expression)

   >[!NOTE]
   >
   >Attualmente, i frammenti visivi sono disponibili solo per il canale **E-mail**.

1. Se stai creando un frammento di espressione, seleziona il tipo di codice che desideri utilizzare: **[!UICONTROL HTML]**, **[!UICONTROL JSON]** o **[!UICONTROL Text]**.

   ![](assets/fragment-expression-type.png)

1. Per assegnare etichette personalizzate o di base sull&#39;utilizzo dei dati al frammento, fare clic sul pulsante **[!UICONTROL Gestione accesso]** nella sezione superiore dello schermo. [Ulteriori informazioni sul controllo di accesso a livello di oggetto](../administration/object-based-access.md).

1. Fai clic su **[!UICONTROL Crea]** per progettare il contenuto del frammento.

## Progettare il contenuto del frammento {#content}

Dopo aver configurato le proprietà del frammento, si apre il Designer e-mail o l&#39;editor di personalizzazione, a seconda del tipo di frammento che si sta creando.

>[!NOTE]
>
>Gli [attributi contestuali](../personalization/personalization-build-expressions.md) non sono supportati nei frammenti.
>
>Quando il tracciamento è abilitato in un percorso o in una campagna, se aggiungi collegamenti a un frammento e quest’ultimo viene utilizzato in un messaggio, tali collegamenti vengono tracciati come tutti gli altri collegamenti inclusi nel messaggio. [Ulteriori informazioni su collegamenti e tracciamento](../email/message-tracking.md)

* Per i frammenti visivi, modifica i tuoi contenuti in base alle esigenze, come faresti per qualsiasi e-mail all&#39;interno di un viaggio o di una campagna. [Ulteriori informazioni](../email/get-started-email-design.md)

  ![](assets/fragment-designer.png)

  Per applicare rapidamente uno stile specifico che si adatta al vostro marchio e design, potete applicare un [tema](../email/apply-email-themes.md) al vostro frammento.

  ![](assets/fragment-themes.png)

  >[!CAUTION]
  >
  >I frammenti non sono compatibili tra le modalità Usa temi e Stile manuale. Quando usi un frammento di contenuto di posta elettronica, assicurati di applicare un tema definito per questo frammento. [Ulteriori informazioni](../email/apply-email-themes.md#leverage-themes-fragment)

* Per i frammenti di espressione, utilizzare l&#39;editor di personalizzazione [!DNL Journey Optimizer] con tutte le funzionalità di personalizzazione e creazione per creare il contenuto del frammento. [Ulteriori informazioni](../personalization/personalization-build-expressions.md)

  ![](assets/fragment-expression-editor.png)

  >[!NOTE]
  >
  >I frammenti di espressioni di tipo JSON vengono convalidati sintatticamente al salvataggio, con gli eventuali errori visualizzati come avvisi di avvertenza.

Quando il contenuto è pronto, fai clic sul pulsante **[!UICONTROL Salva]**.

>[!NOTE]
>
>I frammenti visivi non possono superare i 100 KB. I frammenti di espressioni non possono superare i 200 KB.

Il frammento viene creato e aggiunto all&#39;elenco di frammenti con stato **[!UICONTROL Bozza]**. Puoi visualizzarlo in anteprima e pubblicarlo per renderlo disponibile in viaggi e campagne.

## Visualizzare in anteprima e pubblicare il frammento {#publish}

>[!NOTE]
>
>Per pubblicare un frammento, è necessario disporre dell&#39;autorizzazione utente [Frammento di Publish](../administration/ootb-product-profiles.md#content-library-manager).

Se il frammento è pronto per essere pubblicato, puoi visualizzarlo in anteprima e pubblicarlo per renderlo disponibile nei tuoi viaggi e nelle tue campagne. A questo scopo, segui i passaggi riportati qui sotto.

1. Tornare alla schermata di creazione dei frammenti dopo averne progettato il contenuto o aprirla dall&#39;elenco dei frammenti.

1. Nel campo **[!UICONTROL Tag]** è disponibile un&#39;anteprima del frammento che consente di verificarne il rendering. Per apportare modifiche, fai clic sul pulsante **[!UICONTROL Modifica]** nella sezione superiore dello schermo per aprire il Designer e-mail o l&#39;editor di personalizzazione, a seconda del tipo di frammento. [Ulteriori informazioni](manage-fragments.md#edit-fragments)

   ![](assets/fragment-preview.png)

1. Fai clic sul pulsante **[!UICONTROL Publish]** in alto a destra per pubblicare il frammento.

1. Se il frammento viene utilizzato in un viaggio o una campagna dal vivo, viene visualizzato un messaggio per informarti. Fai clic sul collegamento **[!UICONTROL Vedi altro]** per accedere all&#39;elenco dei percorsi e/o delle campagne a cui fa riferimento. [Scopri come esplorare i riferimenti di un frammento](../content-management/manage-fragments.md#explore-references)

   ![](assets/fragment-publish.png){width="70%" align="center"}

   Fai clic su **[!UICONTROL Conferma]** per pubblicare il frammento e aggiornarlo nei percorsi/campagne live che lo utilizzano.

Il frammento è ora **[!UICONTROL Live]** e diventa disponibile quando si crea un contenuto nel Designer di posta elettronica o nell&#39;editor di personalizzazione di [!DNL Journey Optimizer].

* [Scoprite come utilizzare i frammenti visivi](../email/use-visual-fragments.md)
* [Scopri come utilizzare i frammenti di espressione](../personalization/use-expression-fragments.md)

>[!CAUTION]
>
>Una volta pubblicata, non è possibile aggiungere nuovi attributi personalizzati a un frammento dinamico. Se si desidera aggiungere attributi di personalizzazione, è necessario duplicare il frammento. [Ulteriori informazioni](manage-fragments.md#adding-new-attributes)