---
solution: Journey Optimizer
product: journey optimizer
title: Creare un frammento
description: Scopri come creare frammenti per riutilizzare i contenuti nelle campagne e nei percorsi Journey Optimizer
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: da3ffe9c-a244-4246-b4b5-a3a1d0508676
source-git-commit: f47160f40abd9427cb9b9c793ee0ab402bf9f65b
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 1%

---

# Creare un frammento da zero {#create-fragments}

>[!CONTEXTUALHELP]
>id="ajo_create_visual_fragment"
>title="Seleziona il tipo di elemento visivo"
>abstract="Crea un frammento visivo indipendente per rendere il contenuto riutilizzabile in un messaggio e-mail all’interno di un percorso, di una campagna o di un modello di contenuto."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/email/design-email/add-content/use-visual-fragments.html" text="Aggiungi frammenti visivi alle e-mail"

>[!CONTEXTUALHELP]
>id="ajo_create_expression_fragment"
>title="Seleziona il tipo di espressione"
>abstract="Crea un frammento di espressione autonomo per rendere il contenuto riutilizzabile in più percorsi e campagne. Quando utilizzi l’editor di personalizzazione, puoi sfruttare tutti i frammenti di espressione creati nella sandbox corrente."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/personalization/expression-editor/use-expression-fragments.html" text="Sfruttare i frammenti di espressione"

I frammenti vengono creati da **[!UICONTROL Frammenti]** menu a sinistra. Inoltre, è possibile anche salvare una parte del contenuto esistente come frammento durante la progettazione. [Scopri come](#save-as-fragment)

Una volta salvato, il frammento è disponibile per l’utilizzo in un percorso, una campagna o un modello. Ora puoi utilizzare questo frammento per creare qualsiasi contenuto in [!DNL Journey Optimizer]. Consulta [Aggiungere frammenti visivi](../email/use-visual-fragments.md) e [Sfruttare i frammenti di espressione](../personalization/use-expression-fragments.md)

Per creare un frammento da zero, segui la procedura riportata di seguito.

1. [Accedere all’elenco dei frammenti](#access-manage-fragments) tramite **[!UICONTROL Gestione dei contenuti]** > **[!UICONTROL Frammenti]** menu a sinistra.

1. Seleziona **[!UICONTROL Crea frammento]**.

1. Inserisci i dettagli del frammento, ovvero nome e descrizione (se necessario).

   ![](assets/fragment-details.png)

1. Seleziona o crea tag Adobe Experience Platform da **[!UICONTROL Tag]** per categorizzare il frammento per una ricerca migliore. [Ulteriori informazioni](../start/search-filter-categorize.md#tags)

1. Seleziona il tipo di frammento: [Frammento visivo](#create-visual-fragment) o [Frammento di espressione](#create-expression-fragment).

   >[!NOTE]
   >
   >Attualmente, per i frammenti visivi solo il **E-mail** canale è supportato.

1. Se stai creando un frammento di espressione, seleziona il tipo di codice che desideri utilizzare: **[!UICONTROL HTML]**, **[!UICONTROL JSON]** o **[!UICONTROL Testo]**.

   ![](assets/fragment-expression-type.png)

1. Per assegnare etichette di utilizzo dei dati personalizzate o di base al frammento, seleziona **[!UICONTROL Gestisci accesso]**. [Ulteriori informazioni su OLAC (Object Level Access Control)](../administration/object-based-access.md).

1. Fai clic su **[!UICONTROL Crea]**.

1. Il [E-mail Designer](../email/get-started-email-design.md) oppure viene aperto l’editor di personalizzazione, a seconda del tipo di frammento che stai creando.

   * Per i frammenti visivi, modifica il contenuto in base alle esigenze, come faresti per qualsiasi e-mail all’interno di un percorso o di una campagna.

     >[!NOTE]
     >
     >Puoi aggiungere campi di personalizzazione e contenuto dinamico, ma gli attributi contestuali non sono supportati nei frammenti.

     ![](assets/fragment-designer.png)

   * Per i frammenti di espressione, sfrutta [!DNL Journey Optimizer] l’editor di personalizzazione con tutte le sue funzionalità di personalizzazione e authoring per creare i contenuti dei frammenti. [Ulteriori informazioni](../personalization/personalization-build-expressions.md)

     ![](assets/fragment-expression-editor.png)

1. Quando il frammento è pronto, fai clic su **[!UICONTROL Salva]**.

Il frammento viene aggiunto al [elenco frammenti](#access-manage-fragments). Ora può essere utilizzato per creare qualsiasi contenuto all’interno di [!DNL Journey Optimizer] E-mail Designer o editor di personalizzazione.

* [Scopri come utilizzare i frammenti visivi](../email/use-visual-fragments.md)
* [Scopri come utilizzare i frammenti di espressione](../personalization/use-expression-fragments.md)
