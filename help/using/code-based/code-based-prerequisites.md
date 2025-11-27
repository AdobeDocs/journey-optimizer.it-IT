---
title: Prerequisiti per l’esperienza basata su codice
description: Per poter modificare app e pagine web utilizzando la funzione basata su codice di Journey Optimizer, segui i prerequisiti riportati in questa pagina
feature: Code-based Experiences
topic: Content Management
role: Admin
level: Experienced
exl-id: ac901f88-5fde-4220-88c6-fe05433866cc
source-git-commit: 1b6158132e5df1912d9658805fa8b1344c6f938f
workflow-type: tm+mt
source-wordcount: '668'
ht-degree: 2%

---

# Prerequisiti per l’esperienza basata su codice {#code-based-prerequisites}

Per poter utilizzare in [!DNL Journey Optimizer] le azioni di esperienza basate su codice e distribuire il payload del contenuto di codice che può essere utilizzato dalle applicazioni, attenersi ai prerequisiti seguenti:

* Per aggiungere modifiche alle applicazioni, è necessario disporre di un’implementazione specifica. [Ulteriori informazioni](#implementation-prerequisites)

* Affinché le esperienze basate sul codice vengano consegnate correttamente, assicurati di definire le impostazioni Adobe Experience Platform dettagliate [qui](#delivery-prerequisites).

* Per abilitare la visualizzazione dei dati nei report esperienza basati su codice, assicurati di seguire questi [prerequisiti per la generazione di rapporti](#reporting-prerequisites).

* Quando crei una configurazione del canale esperienza basata su [codice](code-based-configuration.md), accertati di immettere una stringa o un percorso o un URI di superficie che corrisponda a quello dichiarato nella tua implementazione. In questo modo il contenuto viene consegnato nella posizione desiderata all’interno dell’app o della pagina specificata. In caso contrario, non sarà possibile consegnare le modifiche. [Ulteriori informazioni](code-based-surface.md)

>[!CAUTION]
>
>Quando esegui il targeting di profili pseudonimi (visitatori non autenticati) con esperienze basate su codice, puoi impostare un valore TTL (Time-To-Live) per l’eliminazione automatica del profilo, in modo da gestire il conteggio dei profili coinvolgibili e i costi associati. [Ulteriori informazioni](../start/guardrails.md#profile-management-inbound)

## Prerequisiti per l’implementazione {#implementation-prerequisites}

L’esperienza basata su codice supporta qualsiasi tipo di implementazione del cliente, come illustrato nelle opzioni seguenti. Puoi utilizzare un metodo di implementazione lato client, lato server o ibrido per le proprietà:

* Solo lato client: per aggiungere modifiche alle pagine Web o alle app mobili, devi implementare [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=it){target="_blank"} sul tuo sito Web o [Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/code-based/tutorial/){target="_blank"} nelle tue app mobili.

* Modalità ibrida: è possibile utilizzare l&#39;[API server AEP Edge Network](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=it){target="_blank"} per richiedere la personalizzazione lato server; la risposta viene fornita a Adobe Experience Platform Web SDK per eseguire il rendering delle modifiche lato client. Per ulteriori informazioni, consulta la [documentazione sulle API server di Adobe Experience Platform per Edge Network](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html){target="_blank"}. Per ulteriori informazioni sulla modalità ibrida, consulta alcuni esempi di implementazione in [questo post di blog](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}.

* Lato server: è possibile utilizzare l&#39;[API server di AEP Edge Network](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=it){target="_blank"} per richiedere la personalizzazione lato server. Il team di sviluppo deve gestire la risposta ed eseguire il rendering delle modifiche lato client nell’implementazione dell’app.

Puoi trovare campioni per ciascuno dei metodi di implementazione indicati sopra in [questa sezione](code-based-implementation-samples.md).

## Prerequisiti per la consegna {#delivery-prerequisites}

Per consegnare correttamente le esperienze basate su codice, è necessario definire le seguenti impostazioni:

* Nella [raccolta dati di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=it){target="_blank"}, assicurati di avere uno stream di dati definito, ad esempio nel servizio **[!UICONTROL Adobe Experience Platform]** hai l&#39;opzione **[!UICONTROL Adobe Journey Optimizer]** abilitata.

  In questo modo gli eventi in entrata Journey Optimizer vengono gestiti correttamente da Adobe Experience Platform Edge. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html){target="_blank"}

  ![](../web/assets/web-aep-datastream-ajo.png)

* In [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=it){target="_blank"}, assicurati di avere abilitato un criterio di unione con l&#39;opzione **[!UICONTROL Criterio di unione attivo su Edge]**. A questo scopo, seleziona un criterio dal menu Experience Platform **[!UICONTROL Cliente]** > **[!UICONTROL Profili]** > **[!UICONTROL Criteri di unione]**. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  Questo criterio di unione viene utilizzato da [!DNL Journey Optimizer] canali in entrata per attivare e pubblicare correttamente le campagne in entrata sul server Edge. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=it){target="_blank"}

  ![](../web/assets/web-aep-merge-policy.png)

* Per risolvere i problemi relativi alla distribuzione delle esperienze Web di Journey Optimizer, puoi utilizzare la visualizzazione **Edge Delivery** in **Adobe Experience Platform Assurance**. Questo plug-in consente di esaminare in dettaglio le chiamate di richiesta, verificare se si verificano le chiamate edge previste come previsto ed esaminare i dati del profilo, tra cui le mappe di identità, le appartenenze ai segmenti e le impostazioni di consenso. Inoltre, puoi rivedere le attività per le quali la richiesta si è qualificata e identificare quelle per le quali non si è qualificata.

  L&#39;utilizzo del plug-in **Edge Delivery** consente di ottenere le informazioni necessarie per comprendere e risolvere in modo efficace le implementazioni in entrata.

  [Ulteriori informazioni sulla visualizzazione Edge Delivery](https://experienceleague.adobe.com/it/docs/experience-platform/assurance/view/edge-delivery){target="_blank"}

## Prerequisiti per la generazione di rapporti {#reporting-prerequisites}

Per abilitare il reporting per il canale basato su codice, è necessario assicurarsi che il [set di dati](../data/get-started-datasets.md) utilizzato nell&#39;implementazione dell&#39;app [flusso di dati](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html){target="_blank"} sia incluso anche nella configurazione del reporting.

In altre parole, quando configuri il reporting, se aggiungi un set di dati non presente nello stream di dati dell’app, i dati dell’app non verranno visualizzati nei rapporti.

Scopri come aggiungere set di dati per il reporting in [questa sezione](../reports/reporting-configuration.md#add-datasets).

>[!NOTE]
>
>Il set di dati viene utilizzato in sola lettura dal sistema di reporting [!DNL Journey Optimizer] e non influisce sulla raccolta o sull&#39;acquisizione dei dati.

