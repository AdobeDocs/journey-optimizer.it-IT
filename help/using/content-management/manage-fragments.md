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
source-git-commit: 4f238177485ccc5ab53b48488dd1f2084d34d684
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 2%

---

# Gestire i frammenti {#manage-fragments}

>[!CONTEXTUALHELP]
>id="ajo_fragment_statuses"
>title="Nuovi stati dei frammenti"
>abstract="Da **Bozza** e **Live** Con la versione di giugno di Journey Optimizer sono stati introdotti gli stati; tutti i frammenti creati prima di questa versione hanno lo stato &quot;Bozza&quot;, anche se vengono utilizzati in un percorso o in una campagna. Se apporti modifiche a questi frammenti, devi pubblicarli per renderli &quot;live&quot; e propagare le modifiche alle campagne e ai percorsi associati. Devi anche creare una nuova versione di percorso/campagna e pubblicarla."

Per gestire i frammenti, accedi all’elenco dei frammenti da **[!UICONTROL Gestione dei contenuti]** > **[!UICONTROL Frammenti]** menu a sinistra.

![](assets/fragment-list.png)

Tutti i frammenti creati nella sandbox corrente: [dal **[!UICONTROL Frammenti]** menu](#create-fragments), utilizzando [Salva come frammento](#save-as-fragment) opzione - vengono visualizzati.

Puoi filtrare i frammenti in base ai seguenti elementi:

* Tipo: **[!UICONTROL Visivo]** o **[!UICONTROL Espressione]**
* Tag
* Data di creazione o modifica

Puoi scegliere di visualizzare tutti i frammenti o solo gli elementi creati o modificati dall’utente corrente.

È inoltre possibile visualizzare **[!UICONTROL Archiviato]** frammenti. [Ulteriori informazioni](#archive-fragments)

![](assets/fragment-list-filters.png)

Dalla sezione **[!UICONTROL Altre azioni]** accanto a ciascun frammento, puoi:

* Duplica un frammento.

* Utilizza il **[!UICONTROL Esplora riferimenti]** per visualizzare i percorsi, le campagne o i modelli in cui viene utilizzato. [Ulteriori informazioni](#explore-references)

* Archivia un frammento. [Ulteriori informazioni](#archive-fragments)

* Modificare le proprietà di un frammento [tag](../start/search-filter-categorize.md#tags).

![](assets/fragment-list-more-actions.png)

## Modifica frammenti {#edit-fragments}

Per modificare un frammento, effettua le seguenti operazioni.

1. Fai clic sull’elemento desiderato da **[!UICONTROL Frammenti]** elenco.
1. Dalle proprietà del frammento puoi [esplorare i riferimenti](#explore-references), [gestirne l’accesso](../administration/object-based-access.md), e aggiorna i dettagli del frammento, tra cui [tag](../start/search-filter-categorize.md#tags).

   ![](../email/assets/fragment-edit-content.png)

1. Seleziona il pulsante corrispondente per modificare il contenuto, come faresti per creare un frammento da zero. [Ulteriori informazioni](#create-from-scratch)

>[!NOTE]
>
>Quando modifichi un frammento, le modifiche vengono propagate automaticamente a tutto il contenuto che lo utilizza, ad eccezione del contenuto utilizzato in **[!UICONTROL Live]** percorsi o campagne. Puoi anche interrompere l’ereditarietà dal frammento originale. Per ulteriori informazioni, consulta [Aggiungi frammenti visivi alle e-mail](../email/use-visual-fragments.md#break-inheritance) e [Sfruttare i frammenti di espressione](../personalization/use-expression-fragments.md#break-inheritance) sezioni.

## Esplora riferimenti {#explore-references}

Puoi visualizzare l’elenco dei percorsi, delle campagne e dei modelli di contenuto che attualmente utilizzano un frammento.

A tale scopo, seleziona **[!UICONTROL Esplora riferimenti]** dall&#39; **[!UICONTROL Altre azioni]** nell’elenco dei frammenti o dalla schermata delle proprietà del frammento.

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
