---
title: Prerequisiti per il canale Web
description: Per poter accedere e creare pagine web nell’interfaccia utente di Journey Optimizer, segui i prerequisiti riportati in questa pagina
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: 6cb4f8ab-77ad-44a2-b2bf-a97f87b8f1db
source-git-commit: 65a33d6836c43564ef7c93660a8076677ea5cba8
workflow-type: tm+mt
source-wordcount: '872'
ht-degree: 12%

---

# Prerequisiti e guardrail {#web-prerequisites}

Per poter accedere e creare pagine web in [!DNL Journey Optimizer] nell&#39;interfaccia utente, seguire i prerequisiti seguenti:

* Per aggiungere modifiche al sito web, devi disporre di un’implementazione specifica. [Ulteriori informazioni](#implementation-prerequisites)

* Per accedere al [!DNL Journey Optimizer] web designer, è necessario che sia installata un’estensione specifica per il browser Google Chrome. [Ulteriori informazioni](#visual-authoring-prerequesites)

* Affinché l’esperienza web venga consegnata correttamente, assicurati di definire in dettaglio le impostazioni di Adobe Experience Platform [qui](#delivery-prerequisites).

## Attenzioni

Attualmente in [!DNL Journey Optimizer] puoi creare esperienze web solo utilizzando le **campagne**. [Ulteriori informazioni](../campaigns/create-campaign.md#configure)


[!DNL Journey Optimizer] le campagne web eseguono il targeting di nuovi profili che non sono stati precedentemente coinvolti su altri canali. Questo aumenterà il conteggio totale dei profili coinvolgibili, il che potrebbe avere implicazioni di costo se viene superato il numero contrattuale di profili coinvolgibili acquistati. Le metriche delle licenze per ciascun pacchetto sono elencate nella [Descrizione del prodotto Journey Optimizer](https://helpx.adobe.com/it/legal/product-descriptions/adobe-journey-optimizer.html) pagina.

## Prerequisiti per l’implementazione {#implementation-prerequisites}

Attualmente sono supportati due tipi di implementazioni per abilitare l’authoring e la distribuzione di campagne canale web sulle proprietà web:

* Solo lato client: per aggiungere modifiche al sito web, devi implementare [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=it){target="_blank"} sul tuo sito web.

* Modalità ibrida: è possibile utilizzare [API server di rete Edge AEP](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"} to request for personalization server-side; the response is provided to the Adobe Experience Platform Web SDK to render the modifications client-side. Learn more in the Adobe Experience Platform [Edge Network Server API documentation](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html?lang=it){target="_blank"}. You can find out more about the hybrid mode and check some implementation samples in [this blog post](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}.

>[!NOTE]
>
>L’implementazione solo lato server non è attualmente supportata.

<!--If the Adobe Experience Platform Web SDK is not yet implemented on the website, a message displays in the web designer suggesting that you install the Visual Editing Helper browser extension and implement the [Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target="_blank"}.-->

## Prerequisiti per l’authoring visivo {#visual-authoring-prerequisites}

<!--In order to rapidly author and preview your web experiences, the Adobe Experience Cloud Visual Editing Helper browser extension for Google Chrome lets you load websites reliably within the Adobe [!DNL Journey Optimizer] web designer.-->

Per poter aprire, creare e visualizzare in anteprima le pagine Web in modo affidabile nel [!DNL Journey Optimizer] web designer, è necessario disporre di [Helper per editing video Adobe Experience Cloud](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} estensione del browser installata nel browser web.

>[!CAUTION]
>
>Google Chrome e Microsoft Edge sono attualmente gli unici browser che supportano l’authoring di pagine web in [!DNL Journey Optimizer].

### Installare l’estensione Helper per editing video {#install-visual-editing-helper}

Per scaricare e installare l’estensione del browser Helper per editing video, effettua le seguenti operazioni.

1. Apri una nuova scheda nel browser (Google Chrome o Microsoft Edge).

1. Vai a [Google Chrome Web Store](https://chrome.google.com/webstore/category/extensions){target="_blank"}.

1. Se utilizzi Microsoft Edge, seleziona **[!UICONTROL Consenti estensioni da altri store]** sul banner superiore. Questo ti consente di aggiungere estensioni dal Chrome Web Store a Microsoft Edge.

1. Cerca e accedi al [Helper per editing video Adobe Experience Cloud](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} estensione del browser.

1. Fai clic su **[!UICONTROL Aggiungi a Chrome]** > **[!UICONTROL Aggiungi estensione]**.

   >[!NOTE]
   >
   >Se utilizzi Microsoft Edge, l’estensione verrà aggiunta a Edge anche se il pulsante è etichettato **[!UICONTROL Aggiungi a Chrome]**.

1. Assicurati che l’estensione del browser Helper per editing video sia abilitata correttamente nella barra degli strumenti del browser.

   ![](assets/web-visual-editing-extension-edge.png)

<!--1. Launch [!DNL Journey Optimizer] in a new tab of your browser with the extension installed.

1. Create a web channel campaign in [!DNL Journey Optimizer]. [Learn how](author-web.md#create-web-campaign)

1. Open the [!DNL Journey Optimizer] web designer to start authoring your web experience. [Learn more](author-web.md)-->

L’estensione Helper per editing video di Adobe Experience Cloud ora viene abilitata automaticamente quando un sito web viene aperto in [!DNL Journey Optimizer] web designer per potenziare l’authoring.

L’estensione non dispone di impostazioni condizionali e gestisce automaticamente tutte le impostazioni, incluse le impostazioni dei cookie SameSite.

>[!NOTE]
>
>Alcuni siti web potrebbero non aprirsi in modo affidabile nel [!DNL Journey Optimizer] web designer per uno dei motivi seguenti:
>
> * Il sito web dispone di criteri di sicurezza rigidi.
> * Il sito web si trova in un iframe.
> * Il sito per il controllo qualità o il sito di staging del cliente non è disponibile nel mondo esterno (è un sito interno).


### Risoluzione dei problemi di mancato caricamento del sito Web {#troubleshooting}

Quando si utilizza l’Adobe [!DNL Journey Optimizer] web designer, se si tenta di caricare un sito web che non riesce, viene visualizzato un messaggio per suggerirti di installare [Estensione del browser Helper per editing video](#install-visual-editing-helper).

Se l’estensione del browser Helper per editing video è installata correttamente, ma il sito web non si carica o si comporta in modo imprevisto, è possibile aprire il sito web nel browser e accettare i cookie prima di tentare di caricarlo in [!DNL Journey Optimizer] web designer.

Per le pagine in autenticazione, se la pagina di accesso non viene caricata o se dopo aver tentato di accedere non hai ancora effettuato l’accesso:

* Prova ad accedere prima da una nuova scheda del browser e a passare alla pagina desiderata, quindi copia l’URL e prova ad aprirlo nella [!DNL Journey Optimizer] web designer.

* Se non riesci ancora a caricare il sito web in [!DNL Journey Optimizer] web designer, contatta l’Adobe dell’Assistenza clienti per segnalare il problema, assicurandoti di specificare l’URL errato.

## Prerequisiti per la consegna {#delivery-prerequisites}

Affinché l’esperienza web possa essere consegnata correttamente, è necessario definire le seguenti impostazioni:

* In [Raccolta dati di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=it){target="_blank"}, assicurati di avere un flusso di dati definito, ad esempio sotto **[!UICONTROL Adobe Experience Platform]** servizio che hai sia **[!UICONTROL Segmentazione Edge]** e **[!UICONTROL Adobe Journey Optimizer]** opzioni abilitate.

   In questo modo gli eventi in entrata Journey Optimizer vengono gestiti correttamente da Adobe Experience Platform Edge. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html){target="_blank"}

   ![](assets/web-aep-datastream-ajo.png)

   >[!NOTE]
   >
   >Il **[!UICONTROL Adobe Journey Optimizer]** può essere attivata solo quando **[!UICONTROL Segmentazione Edge]** l&#39;opzione è già abilitata.

* In entrata [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=it){target="_blank"}, make sure you have one merge policy with the **[!UICONTROL Active-On-Edge Merge Policy]** option enabled. To do this, select a policy under the **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** Experience Platform menu. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

   Questo criterio di unione è utilizzato da [!DNL Journey Optimizer] canali in entrata per attivare e pubblicare correttamente le campagne in entrata sul server Edge. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=it){target="_blank"}

   ![](assets/web-aep-merge-policy.png)

## Domini con marchio per le risorse {#branded-domains-for-assets}

Quando crei esperienze web, se aggiungi contenuti provenienti da [Adobe Experience Manager Assets Essentials](../email/assets-essentials.md) devi impostare il sottodominio che verrà utilizzato per pubblicare questo contenuto. [Ulteriori informazioni](web-delegated-subdomains.md)
