---
title: Prerequisiti per l’esperienza basata su codice
description: Per poter modificare app e pagine web utilizzando la funzione basata su codice di Journey Optimizer, segui i prerequisiti riportati in questa pagina
feature: Offers
topic: Content Management
role: User
level: Experienced
hide: true
hidefromtoc: true
badge: label="Beta"
source-git-commit: 69a2ef17b6f5ccd40c08858f7b434029964d544d
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 13%

---

# Prerequisiti e guardrail {#web-prerequisites}

>[!BEGINSHADEBOX]

Cosa troverai in questa documentazione di guida:

* [Introduzione al canale basato su codice](get-started-code-based.md)
* **[Prerequisiti basati su codice](code-based-prerequisites.md)**
* [Esempi di implementazione basati su codice](code-based-implementation-samples.md)
* [Creare esperienze basate su codice](create-code-based.md)

>[!ENDSHADEBOX]

Per poter utilizzare le azioni basate su codice nelle [!DNL Journey Optimizer] e consegnare il payload del contenuto del codice che può essere utilizzato dalle applicazioni, segui i prerequisiti seguenti:

* Per aggiungere modifiche alle applicazioni, è necessario disporre di un’implementazione specifica. [Ulteriori informazioni](#implementation-prerequisites)

* Affinché le esperienze basate sul codice possano essere consegnate correttamente, assicurati di definire in dettaglio le impostazioni di Adobe Experience Platform [qui](#delivery-prerequisites).

## Note di attenzione {#caution-notes-web}

* Il canale di esperienza basato su codice è attualmente disponibile come versione beta solo per alcuni utenti. Per partecipare al programma beta, contatta l’Assistenza clienti Adobe.

* Attualmente in [!DNL Journey Optimizer] puoi creare esperienze basate su codice solo in **campagne**. [Ulteriori informazioni](../campaigns/create-campaign.md#configure)

## Prerequisiti per l’implementazione {#implementation-prerequisites}

L’esperienza basata su codice supporta qualsiasi tipo di implementazione del cliente, come illustrato nelle opzioni seguenti. Puoi utilizzare un metodo di implementazione lato client, lato server o ibrido per le proprietà:

* Solo lato client: per aggiungere modifiche alle pagine web o alle app mobili, devi implementare [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=it){target="_blank"} on your website or [Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation/){target="_blank"} sulle app mobili.

* Modalità ibrida: è possibile utilizzare [API server di rete Edge AEP](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"} to request for personalization server-side; the response is provided to the Adobe Experience Platform Web SDK to render the modifications client-side. Learn more in the Adobe Experience Platform [Edge Network Server API documentation](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html?lang=it){target="_blank"}. You can find out more about the hybrid mode and check some implementation samples in [this blog post](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}.

* Lato server: è possibile utilizzare [API server di rete Edge AEP](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"} per richiedere personalizzazione lato server. Il team di sviluppo deve gestire la risposta ed eseguire il rendering delle modifiche lato client nell’implementazione dell’app.

Puoi trovare campioni per ciascuno dei metodi di implementazione indicati sopra in [questa sezione](code-based-implementation-samples.md).

## Prerequisiti per la consegna {#delivery-prerequisites}

Per consegnare correttamente le esperienze basate su codice, è necessario definire le seguenti impostazioni:

* In [Raccolta dati di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=it){target="_blank"}, assicurati di avere un flusso di dati definito, ad esempio sotto **[!UICONTROL Adobe Experience Platform]** servizio di cui si dispone **[!UICONTROL Adobe Journey Optimizer]** opzione abilitata.

  In questo modo gli eventi in entrata Journey Optimizer vengono gestiti correttamente da Adobe Experience Platform Edge. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html){target="_blank"}

  ![](../web/assets/web-aep-datastream-ajo.png)

* In entrata [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=it){target="_blank"}, make sure you have one merge policy with the **[!UICONTROL Active-On-Edge Merge Policy]** option enabled. To do this, select a policy under the **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** Experience Platform menu. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  Questo criterio di unione è utilizzato da [!DNL Journey Optimizer] canali in entrata per attivare e pubblicare correttamente le campagne in entrata sul server Edge. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=it){target="_blank"}

  ![](../web/assets/web-aep-merge-policy.png)

## Prerequisiti per l’esperimento sui contenuti {#experiment-prerequisites}

Per abilitare gli esperimenti di contenuto per il canale basato su codice, è necessario assicurarsi che il [set di dati](../data/get-started-datasets.md) utilizzato nell&#39;implementazione dell&#39;app [flusso di dati](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html?lang=it){target="_blank"} è incluso anche nella configurazione di reporting.

In altre parole, quando configuri la generazione di rapporti sull’esperimento, se aggiungi un set di dati non presente nello stream di dati dell’app, i dati dell’app non verranno visualizzati nei rapporti sull’esperimento del contenuto.

Scopri come aggiungere set di dati per il reporting degli esperimenti sui contenuti in [questa sezione](../campaigns/reporting-configuration.md#add-datasets).

>[!NOTE]
>
>Il set di dati viene utilizzato in sola lettura da [!DNL Journey Optimizer] e non influisce sulla raccolta o l’acquisizione dei dati.


