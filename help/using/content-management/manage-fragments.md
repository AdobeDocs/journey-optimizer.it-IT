---
solution: Journey Optimizer
product: journey optimizer
title: Gestire i frammenti
description: Scopri come gestire i frammenti del contenuto
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 1fc708e1-a993-4a2a-809c-c5dc08a4bae1
source-git-commit: c42fc1069e11b8e34b7477fc26ed8a6b4ef95ac7
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 18%

---

# Gestire i frammenti {#manage-fragments}

Per gestire i frammenti, accesso l&#39;elenco dei frammenti dal **[!UICONTROL menu a sinistra Gestione contenuto]** > **[!UICONTROL Frammenti]** .

Vengono visualizzati tutti i frammenti creati nella sandbox corrente, sia dal menu Frammenti ]**, sia utilizzando l&#39;opzione [Salva come frammento](#save-as-fragment).](#create-fragments)**[!UICONTROL [

![](assets/fragment-list-filters.png)

È possibile filtrare i frammenti in base a:

* Stato (bozza o live)
* Tipo (visivo o espressivo)
* Data di creazione o modifica
* Stato (archiviato o meno)
* Tag

È inoltre possibile scegliere di visualizzare tutti i frammenti o solo gli elementi che il utente corrente creato o modificato.

Dall&#39;pulsante **[!UICONTROL Altre azioni]** accanto a ciascun frammento è possibile:

* Duplicare un frammento.
* Utilizza l&#39;opzione **[!UICONTROL Esplora riferimenti]** per visualizzare i percorsi, le campagne o i modelli in cui viene utilizzata. [Ulteriori informazioni](#explore-references)
* Archiviare un frammento. [Ulteriori informazioni](#archive-fragments)
* Modifica i tag di un frammento Scopri come utilizzare i [tag unificati](../start/search-filter-categorize.md#tags).

![](assets/fragment-list-more-actions.png)

## Stati dei frammenti

>[!CONTEXTUALHELP]
>id="ajo_fragment_statuses"
>title="Nuovi stati dei frammenti"
>abstract="Da quando sono stati introdotti gli stati **Bozza** e **Live** con la versione di giugno di Journey Optimizer, tutti i frammenti creati prima di questa versione hanno lo stato “Bozza”, anche se vengono utilizzati in un percorso o in una campagna. Se apporti modifiche a questi frammenti, devi pubblicarli per renderli “live” e propagare le modifiche alle campagne e ai percorsi associati. È necessario creare anche una nuova versione di percorso/campagna e pubblicarla. <br/>pubblicazione richiede la <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/access-control/privacy/ootb-product-profiles#content-library-manage">utente autorizzazione frammento</a> Publish."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/access-control/privacy/ootb-product-profiles#content-library-manager" text="Scopri maggiori informazioni sulle autorizzazioni per contenuto frammenti"

I frammenti possono avere più stati:

* **[!UICONTROL Bozza]**: il frammento è in fase di modifica e non è stato approvato.

* **[!UICONTROL Live]**: il frammento è stato approvato ed è attivo. [Scopri come pubblicare un frammento](../content-management/create-fragments.md#publish)

  Durante la modifica di un frammento attivo, accanto al relativo stato viene visualizzata un&#39;icona specifica. Fare clic su questa icona per aprire la versione bozza del frammento.

* **[!UICONTROL pubblicazione]**: il frammento è stato approvato ed è in corso di pubblicazione.
* **[!UICONTROL Archiviato]**: il frammento è stato archiviato. [Scopri come archiviare i frammenti](#archive-fragments)

>[!CAUTION]
>
>Da quando sono stati introdotti gli stati **Bozza** e **Live** con la versione di giugno di Journey Optimizer, tutti i frammenti creati prima di questa versione hanno lo stato “Bozza”, anche se vengono utilizzati in un percorso o in una campagna. Se apporti modifiche a questi frammenti, devi pubblicarli per renderli “live” e propagare le modifiche alle campagne e ai percorsi associati. È necessario creare anche una nuova versione di percorso/campagna e pubblicarla. pubblicazione richiede la [utente autorizzazione frammento](../administration/ootb-product-profiles.md#content-library-manager) Publish.

## Modifica frammenti {#edit-fragments}

>[!CONTEXTUALHELP]
>id="ajo_fragments_update_campaigns"
>title="Aggiornamento dei frammenti nelle campagne"
>abstract="Questa campagna non verrà aggiornata se pubblicare modifiche al frammento. Richiede la pubblicazione di una nuova versione per supportare la funzionalità di aggiornamento dei frammenti."

>[!CONTEXTUALHELP]
>id="ajo_fragments_update_journeys"
>title="Aggiornamento dei frammenti nei percorsi"
>abstract="Questo percorso non verrà aggiornato se pubblicare modifiche al frammento. Richiede la pubblicazione di una nuova versione per supportare la funzionalità di aggiornamento dei frammenti."

Per modificare un frammento, seguire i passaggi riportati di seguito.

1. Selezionare il frammento desiderato nell&#39;elenco **[!UICONTROL Frammenti]** .

1. Le proprietà del frammento vengono visualizzate con un&#39;anteprima del relativo contenuto.

1. Se il frammento in fase di modifica ha lo **stato Live** , fare clic sull&#39;pulsante **Modifica** per creare una bozza del frammento. La versione corrente del frammento continuerà a essere attiva finché non avrai pubblicare la versione bozza.

1. Apportare le modifiche desiderate al frammento. Per modificarne il contenuto, fare clic sul **Modifica** pulsante quindi modificare il contenuto come si farebbe quando si crea un frammento da zero. [Scopri Creazione di un frammento](#create-from-scratch)

   >[!NOTE]
   >
   >Quando si modifica un frammento di espressione, è possibile rimuovere qualsiasi campo personalizzazione, ma non è possibile aggiungerne di nuovi al frammento contenuto. Per aggiungere campi personalizzazione, duplicare il frammento per crearne uno nuovo.

   È inoltre possibile controllare l&#39;elenco dei percorsi, delle campagne e dei modelli contenuto in cui il frammento è attualmente utilizzato selezionando l&#39;opzione **Riferimenti** esploratore. [Ulteriori informazioni](#explore-references)

   ![](assets/fragment-edit.png)

1. Una volta pronte le modifiche, fai clic sull&#39;pulsante Publish **per rendere attive le** modifiche.

Quando si modifica un frammento, le modifiche vengono propagate automaticamente a tutti i contenuti che utilizzano tale frammento, inclusi i percorsi live e le campagne, ad eccezione dei contenuti in cui è stata interrotta l&#39;ereditarietà dal frammento originale. Scopri come interrompere l&#39;ereditarietà [nelle sezioni Aggiungi frammenti visivi ai messaggi di posta elettronica](../email/use-visual-fragments.md#break-inheritance) e [Sfrutta i frammenti di](../personalization/use-expression-fragments.md#break-inheritance) espressione.

## Esplora riferimenti {#explore-references}

È possibile visualizzare l&#39;elenco dei percorsi, delle campagne e dei modelli di contenuto che attualmente utilizzano un frammento. A tale scopo, selezionare **[!UICONTROL Esplora riferimenti]** dal **[!UICONTROL menu Altre azioni]** nell&#39;elenco dei frammenti o dalla schermata Proprietà frammento.

![](assets/fragment-explore-references.png)

Seleziona un scheda per alternare tra percorsi, campagne, modelli e frammenti. Puoi visualizzarne lo stato e fare clic su un nome per essere reindirizzato all&#39;elemento corrispondente a cui si fa riferimento al frammento.

![](assets/fragment-usage-screen.png)

>[!NOTE]
>
>Se il frammento viene utilizzato in un viaggio, una campagna o un modello la cui etichetta impedisce l&#39;accesso, verrà visualizzato un messaggio di avviso sopra il scheda selezionato. [Scopri ulteriori informazioni sul controllo di accesso a livello di oggetto (OLAC, Object Level Access Control)](../administration/object-based-access.md)

## Archiviare frammenti {#archive-fragments}

È possibile pulire l&#39;elenco di frammenti dagli elementi non più pertinenti al marchio.

A tale scopo, fare clic sulla **[!UICONTROL pulsante Altre azioni]** accanto al frammento desiderato e selezionare **[!UICONTROL Archivia]**. Scomparirà dall&#39;elenco dei frammenti, impedendo agli utenti di utilizzarlo in e-mail o modelli futuri.

![](assets/fragment-list-archive.png)

>[!NOTE]
>
>Se archivi un frammento utilizzato in un contenuto, <!--it will remain in the email or template, but you won't be able to select it from the fragment list to edit it-->tale contenuto non subirà effetti negativi.

Per annullare l&#39;archiviazione di un frammento, filtrare gli **[!UICONTROL elementi archiviati]** e selezionare **[!UICONTROL Annulla archiviazione]** dal **[!UICONTROL menu Altre azioni]** . Ora è di nuovo accessibile dall&#39;elenco dei frammenti e può essere utilizzato in qualsiasi e-mail o modello.

![](assets/fragment-list-unarchive.png)
