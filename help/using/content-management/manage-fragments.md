---
solution: Journey Optimizer
product: journey optimizer
title: Gestire i frammenti
description: Scopri come gestire i frammenti di contenuto
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

Per gestire i frammenti, accedi all’elenco dei frammenti da **[!UICONTROL Gestione dei contenuti]** > **[!UICONTROL Frammenti]** menu a sinistra.

Tutti i frammenti creati nella sandbox corrente: [dal **[!UICONTROL Frammenti]** menu](#create-fragments), utilizzando [Salva come frammento](#save-as-fragment) opzione - vengono visualizzati.

![](assets/fragment-list-filters.png)

Puoi filtrare i frammenti in base ai seguenti elementi:

* Stato (bozza o in tempo reale)
* Tipo (visivo o espressione)
* Data di creazione o modifica
* Stato (archiviato o meno)
* Tag

Puoi anche scegliere di visualizzare tutti i frammenti o solo gli elementi creati o modificati dall’utente corrente.

Dalla sezione **[!UICONTROL Altre azioni]** accanto a ciascun frammento, puoi:

* Duplica un frammento.
* Utilizza il **[!UICONTROL Esplora riferimenti]** per visualizzare i percorsi, le campagne o i modelli in cui viene utilizzato. [Ulteriori informazioni](#explore-references)
* Archivia un frammento. [Ulteriori informazioni](#archive-fragments)
* Modificare i tag di un frammento [Scopri come utilizzare i tag unificati](../start/search-filter-categorize.md#tags).

![](assets/fragment-list-more-actions.png)

## Stati dei frammenti

>[!CONTEXTUALHELP]
>id="ajo_fragment_statuses"
>title="Nuovi stati dei frammenti"
>abstract="Da quando sono stati introdotti gli stati **Bozza** e **Live** con la versione di giugno di Journey Optimizer, tutti i frammenti creati prima di questa versione hanno lo stato “Bozza”, anche se vengono utilizzati in un percorso o in una campagna. Se apporti modifiche a questi frammenti, devi pubblicarli per renderli “live” e propagare le modifiche alle campagne e ai percorsi associati. È necessario creare anche una nuova versione di percorso/campagna e pubblicarla. <br/>La pubblicazione richiede <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/access-control/privacy/ootb-product-profiles#content-library-manage">Frammento Publish</a> autorizzazione utente."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/access-control/privacy/ootb-product-profiles#content-library-manager" text="Ulteriori informazioni sulle autorizzazioni per i frammenti di contenuto"

I frammenti possono avere più stati:

* **[!UICONTROL Bozza]**: frammento in fase di modifica che non è stato approvato.

* **[!UICONTROL Live]**: il frammento è stato approvato ed è live. [Scopri come pubblicare un frammento](../content-management/create-fragments.md#publish)

  Quando si modifica un frammento live, viene visualizzata un’icona specifica accanto al relativo stato. Fai clic su questa icona per aprire la versione bozza del frammento.

* **[!UICONTROL Pubblicazione]**: il frammento è stato approvato e viene pubblicato.
* **[!UICONTROL Archiviato]**: frammento archiviato. [Scopri come archiviare i frammenti](#archive-fragments)

>[!CAUTION]
>
>Da quando sono stati introdotti gli stati **Bozza** e **Live** con la versione di giugno di Journey Optimizer, tutti i frammenti creati prima di questa versione hanno lo stato “Bozza”, anche se vengono utilizzati in un percorso o in una campagna. Se apporti modifiche a questi frammenti, devi pubblicarli per renderli “live” e propagare le modifiche alle campagne e ai percorsi associati. È necessario creare anche una nuova versione di percorso/campagna e pubblicarla. La pubblicazione richiede [Frammento Publish](../administration/ootb-product-profiles.md#content-library-manager) autorizzazione utente.

## Modifica frammenti {#edit-fragments}

>[!CONTEXTUALHELP]
>id="ajo_fragments_update_campaigns"
>title="Aggiornamento di frammenti nelle campagne"
>abstract="Se pubblichi modifiche al frammento, questa campagna non verrà aggiornata. Richiede la pubblicazione di una nuova versione, in modo da poter supportare la funzionalità di aggiornamento dei frammenti."

>[!CONTEXTUALHELP]
>id="ajo_fragments_update_journeys"
>title="Aggiornamento frammenti in percorsi"
>abstract="Questo percorso non verrà aggiornato se pubblichi modifiche al frammento. Richiede la pubblicazione di una nuova versione, in modo da poter supportare la funzionalità di aggiornamento dei frammenti."

Per modificare un frammento, effettua le seguenti operazioni.

1. Fai clic sul frammento desiderato da **[!UICONTROL Frammenti]** elenco.

1. Le proprietà del frammento vengono aperte con un’anteprima del relativo contenuto.

1. Se il frammento in fase di modifica presenta **Live** stato, fai clic su **Modifica** per creare una versione bozza del frammento. La versione corrente del frammento continuerà a essere attiva, fino a quando non pubblicherai la versione bozza.

1. Apporta al frammento le modifiche desiderate. Per modificarne il contenuto, fai clic su **Modifica** quindi modifica il contenuto come faresti per creare un frammento da zero. [Scopri come creare un frammento](#create-from-scratch)

   >[!NOTE]
   >
   >Quando modifichi un frammento di espressione, puoi rimuovere qualsiasi campo di personalizzazione ma non aggiungerne di nuovi al contenuto del frammento. Se desideri aggiungere campi di personalizzazione, duplica il frammento per crearne uno nuovo.

   Puoi anche controllare l’elenco dei percorsi, delle campagne e dei modelli di contenuto in cui il frammento è attualmente utilizzato selezionando la **Riferimenti a Explorer** opzione. [Ulteriori informazioni](#explore-references)

   ![](assets/fragment-edit.png)

1. Quando le modifiche sono pronte, fai clic su **Publish** per rendere attive le modifiche.

Quando modifichi un frammento, le modifiche vengono propagate automaticamente a tutti i contenuti che lo utilizzano, inclusi i percorsi live e le campagne, ad eccezione dei contenuti per i quali è stata interrotta l’ereditarietà dal frammento originale. Scopri come interrompere l’ereditarietà in [Aggiungi frammenti visivi alle e-mail](../email/use-visual-fragments.md#break-inheritance) e [Sfruttare i frammenti di espressione](../personalization/use-expression-fragments.md#break-inheritance) sezioni.

## Esplora riferimenti {#explore-references}

Puoi visualizzare l’elenco dei percorsi, delle campagne e dei modelli di contenuto che attualmente utilizzano un frammento. A tale scopo, seleziona **[!UICONTROL Esplora riferimenti]** dall&#39; **[!UICONTROL Altre azioni]** nell’elenco dei frammenti o dalla schermata delle proprietà del frammento.

![](assets/fragment-explore-references.png)

Seleziona una scheda per scegliere tra percorsi, campagne, modelli e frammenti. Puoi visualizzarne lo stato e fare clic su un nome da reindirizzare all’elemento corrispondente in cui si fa riferimento al frammento.

![](assets/fragment-usage-screen.png)

>[!NOTE]
>
>Se il frammento viene utilizzato in un percorso, una campagna o un modello con un’etichetta che impedisce l’accesso, viene visualizzato un messaggio di avviso sopra la scheda selezionata. [Ulteriori informazioni su OLAC (Object Level Access Control)](../administration/object-based-access.md)

## Archivia frammenti {#archive-fragments}

Puoi eliminare dall’elenco i frammenti gli elementi che non sono più rilevanti per il tuo marchio.

A tale scopo, fare clic sul pulsante **[!UICONTROL Altre azioni]** accanto al frammento desiderato e seleziona **[!UICONTROL Archivia]**. Scomparirà dall’elenco dei frammenti, impedendo agli utenti di utilizzarlo in e-mail o modelli futuri.

![](assets/fragment-list-archive.png)

>[!NOTE]
>
>Se archivi un frammento utilizzato in un contenuto, <!--it will remain in the email or template, but you won't be able to select it from the fragment list to edit it-->tale contenuto non sarà interessato.

Per annullare l’archiviazione di un frammento, applica il filtro **[!UICONTROL Archiviato]** elementi e seleziona **[!UICONTROL Annulla archiviazione]** dal **[!UICONTROL Altre azioni]** menu. Ora è nuovamente accessibile dall’elenco dei frammenti e può essere utilizzato in qualsiasi e-mail o modello.

![](assets/fragment-list-unarchive.png)
