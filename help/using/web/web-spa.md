---
title: Creare applicazioni a pagina singola
description: Scopri come creare SPA e applicare modifiche a diverse visualizzazioni in Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Intermediate
exl-id: b33e4bca-d2e9-4610-9f04-008d47f686d0
source-git-commit: 45f19563c79d298eeec6cb757636a9ce47e54adf
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 26%

---

# Creare applicazioni a pagina singola {#web-author-spas}

## Informazioni sulle viste {#about-views}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_modifications_views"
>title="Applicare le modifiche alle viste selezionate"
>abstract="Le modifiche verranno applicate solo alle viste selezionate. Le viste possono essere rilevate utilizzando la modalità **Sfoglia** e accedendo ad esse. Non trovi la vista che stai cercando?"
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=it" text="Ulteriori informazioni"

**Applicazioni a pagina singola** (SPA) ora può essere creato nell’editor visivo del designer web. Questo consente di selezionare quali **visualizzazioni** desideri applicare le modifiche apportate alla pagina web a.

[Scopri come creare applicazioni a pagina singola in questo video](#video)

Una vista può essere definita come un intero sito o un gruppo di elementi visivi su un sito, ad esempio la pagina Home, l’intero sito dei prodotti o il frame delle preferenze di consegna su tutte le pagine di pagamento.

È necessaria la configurazione per sviluppatori una tantum per definire le visualizzazioni nell’implementazione di Adobe Experience Platform Web SDK. Questo consente di creare ed eseguire campagne web Adobe Journey Optimizer sull’SPA.

## Definire le viste nell’implementazione dell’SDK web {#define-views}

È possibile sfruttare le viste XDM in Adobe [!DNL Journey Optimizer] per consentire agli addetti al marketing di eseguire campagne di personalizzazione web e sperimentazione sull’SPA tramite l’editor visivo web. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/ajo/web-spa-implementation.html){target="_blank"}

Per poter accedere e creare visualizzazioni in [!DNL Journey Optimizer] nell&#39;interfaccia utente, assicurati di seguire i passaggi elencati in [questa sezione](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/ajo/web-spa-implementation.html#implement-xdm-views){target="_blank"}.

## Scopri le visualizzazioni nel web designer {#discover-views}

Una volta completata la configurazione dell’SPA nell’implementazione di Adobe Experience Platform Web SDK, è necessario navigare tra tutte le visualizzazioni del sito web a cui desideri applicare le modifiche. Effettua le seguenti operazioni.

1. [Creare una campagna web](create-web.md) e accedere al [web designer](edit-web-content.md).

   La vista in cui sei attualmente è visualizzata in alto a sinistra.

   ![](assets/web-designer-view-home.png)

1. Scambia in **[!UICONTROL Sfoglia]** modalità. [Ulteriori informazioni](../web/edit-web-content.md#browse-mode)

   ![](assets/web-designer-view-browse.png)

1. Passa tra le diverse pagine del sito web per scoprirle tutte. Il nome visualizzato nella parte superiore cambia quando si passa da un&#39;altra pagina all&#39;altra.

   ![](assets/web-designer-other-view.png)

## Applica modifiche ad altre viste {#apply-modifications-views}

Dopo aver aggiunto una modifica mentre ti trovi in una vista specifica, puoi applicarla ad altre viste selezionate. Effettua le seguenti operazioni.

>[!CAUTION]
>
>Se non sono state individuate visualizzazioni utilizzando **[!UICONTROL Sfoglia]** non sarà possibile selezionarli per applicare le modifiche. [Ulteriori informazioni](#discover-views)

1. Seleziona la **[!UICONTROL Modifiche]** per visualizzare il riquadro corrispondente a sinistra.

   ![](assets/web-designer-view-modifications-pane.png)

1. Seleziona una modifica e fai clic su **[!UICONTROL Altre azioni]** accanto. Seleziona **[!UICONTROL Applica a più visualizzazioni]**.

   ![](assets/web-designer-modifications-more-actions.png)

1. Selezionare le visualizzazioni a cui applicare le modifiche.

   ![](assets/web-designer-modifications-apply-to.png)

1. Fai clic su **[!UICONTROL Applica]**.

1. Scambia in **[!UICONTROL Sfoglia]** per verificare che le modifiche vengano applicate alle pagine desiderate.

   ![](assets/web-designer-modifications-applied-view.png)

## Video introduttivo{#video}

Questo video spiega come:

* Scopri le visualizzazioni SPA tramite **[!UICONTROL Sfoglia]** modalità
* Eseguire l’authoring sulla vista corrente
* Applicare le modifiche al sito web per più viste o tutte le viste individuate
* Eseguire azioni in blocco sulle modifiche

>[!VIDEO](https://video.tv.adobe.com/v/3424536/?quality=12&learn=on)
