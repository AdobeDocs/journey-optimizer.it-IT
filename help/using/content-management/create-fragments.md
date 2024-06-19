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
source-git-commit: c843ca5bda10aa5f3ee8a676630d78c5ec092b14
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 13%

---

# Creare un frammento {#create-fragments}

>[!CONTEXTUALHELP]
>id="ajo_create_visual_fragment"
>title="Seleziona il tipo visivo"
>abstract="Crea un frammento visivo autonomo per rendere il contenuto riutilizzabile in un messaggio e-mail all’interno di un percorso, di una campagna o di un modello di contenuto."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/email/design-email/add-content/use-visual-fragments.html?lang=it" text="Aggiungi frammenti visivi alle e-mail"

>[!CONTEXTUALHELP]
>id="ajo_create_expression_fragment"
>title="Seleziona il tipo di espressione"
>abstract="Crea da zero un frammento di espressione autonomo per rendere i contenuti riutilizzabili in più percorsi e campagne. Quando utilizzi l’editor di personalizzazione, puoi sfruttare tutti i frammenti di espressione che sono stati creati nella sandbox corrente."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/personalization/expression-editor/use-expression-fragments.html?lang=it" text="Sfruttare i frammenti di espressione"

I frammenti possono essere creati da zero dalla **[!UICONTROL Frammenti]** menu a sinistra. Inoltre, è possibile anche salvare una parte del contenuto esistente come frammento durante la progettazione. [Scopri come](#save-as-fragment)

Una volta salvato, il frammento è disponibile per l’utilizzo in un percorso, una campagna o un modello. Puoi utilizzare questo frammento quando crei qualsiasi contenuto all’interno di percorsi e campagne. Consulta [Aggiungere frammenti visivi](../email/use-visual-fragments.md) e [Sfruttare i frammenti di espressione](../personalization/use-expression-fragments.md)

Per creare un frammento, segui la procedura riportata di seguito.

## Definire le proprietà del frammento {#properties}

1. Accedere all’elenco dei frammenti tramite **[!UICONTROL Gestione dei contenuti]** > **[!UICONTROL Frammenti]** menu a sinistra.

1. Seleziona **[!UICONTROL Crea frammento]** e compila il nome e la descrizione del frammento (se necessario).

   ![](assets/fragment-details.png)

1. Seleziona o crea tag Adobe Experience Platform da **[!UICONTROL Tag]** per categorizzare il frammento per una ricerca migliore. [Scopri come utilizzare i tag unificati](../start/search-filter-categorize.md#tags)

1. Seleziona il tipo di frammento: **Frammento visivo** o **Frammento di espressione**. [Ulteriori informazioni sui frammenti visivi e di espressione](../content-management/fragments.md#visual-expression)

   >[!NOTE]
   >
   >Per il momento, sono disponibili frammenti visivi per **E-mail** solo canale.

1. Se stai creando un frammento di espressione, seleziona il tipo di codice che desideri utilizzare: **[!UICONTROL HTML]**, **[!UICONTROL JSON]** o **[!UICONTROL Testo]**.

   ![](assets/fragment-expression-type.png)

1. Per assegnare etichette di utilizzo dei dati personalizzate o di base al frammento, fai clic su **[!UICONTROL Gestisci accesso]** nella sezione superiore dello schermo. [Ulteriori informazioni su OLAC (Object Level Access Control)](../administration/object-based-access.md).

1. Clic **[!UICONTROL Crea]** per progettare il contenuto del frammento.

## Progettare il contenuto del frammento {#content}

Dopo aver configurato le proprietà del frammento, viene aperto E-mail Designer o l’editor di personalizzazione, a seconda del tipo di frammento che stai creando.

* Per i frammenti visivi, modifica il contenuto in base alle esigenze, come faresti per qualsiasi e-mail all’interno di un percorso o di una campagna. [Ulteriori informazioni](../email/get-started-email-design.md)

  ![](assets/fragment-designer.png)

* Per i frammenti di espressione, sfrutta [!DNL Journey Optimizer] l’editor di personalizzazione con tutte le sue funzionalità di personalizzazione e authoring per creare i contenuti dei frammenti. [Ulteriori informazioni](../personalization/personalization-build-expressions.md)

  ![](assets/fragment-expression-editor.png)

Quando il contenuto è pronto, fai clic su **Salva** pulsante. Il frammento viene creato e aggiunto all’elenco di frammenti con il comando **Bozza** stato. Puoi visualizzarlo in anteprima e pubblicarlo per renderlo disponibile in percorsi e campagne.

>[!NOTE]
>
>La pubblicazione dei frammenti viene implementata gradualmente nel corso di diversi giorni a partire dalla versione di giugno di Journey Optimizer. Alcuni utenti avranno accesso immediato, altri potrebbero notare un ritardo prima che questo diventi disponibile nei loro ambienti. Se questo miglioramento non è ancora disponibile nell’ambiente, tieni presente che la pubblicazione dei frammenti non è necessaria per utilizzare i frammenti nei percorsi e nelle campagne.

## Anteprima e pubblicazione del frammento {#publish}

>[!NOTE]
>
>Per pubblicare un frammento, è necessario disporre di **Pubblica frammento** autorizzazioni correlate. [Ulteriori informazioni sulle autorizzazioni](../administration/ootb-permissions.md)

Se il frammento è pronto per essere pubblicato, puoi visualizzarlo in anteprima e pubblicarlo per renderlo disponibile nei tuoi percorsi e campagne. Per farlo, segui questi passaggi:

1. Torna alla schermata di creazione del frammento dopo averne progettato il contenuto oppure aprilo dall’elenco dei frammenti.

1. Un’anteprima del frammento è disponibile nella sezione **Tag** , che consente di verificarne il rendering. Se è necessario apportare modifiche, fare clic su **Modifica** nella sezione superiore della schermata per aprire E-mail Designer o l’editor di personalizzazione a seconda del tipo di frammento.

   ![](assets/fragment-preview.png)

1. Fai clic su **Pubblica** nell’angolo in alto a destra per pubblicare il frammento.

   Se il frammento viene utilizzato in un percorso o in una campagna live, si apre un messaggio per informarti. Fai clic su **Vedi altro** per accedere all’elenco dei percorsi e/o delle campagne in cui è fatto riferimento a esso. [Scopri come esplorare i riferimenti di un frammento](../content-management/manage-fragments.md#explore-references)

   Clic **Conferma** per pubblicare il frammento e aggiornarlo nei percorsi/campagne live che lo utilizzano.

   ![](assets/fragment-publish.png){width="70%" align="center"}

Il frammento ora è **Live**, e diventa disponibile quando crei qualsiasi contenuto all’interno del [!DNL Journey Optimizer] E-mail Designer o editor di personalizzazione:

* [Scopri come utilizzare i frammenti visivi](../email/use-visual-fragments.md)
* [Scopri come utilizzare i frammenti di espressione](../personalization/use-expression-fragments.md)
