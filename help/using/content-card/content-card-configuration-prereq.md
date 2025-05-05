---
title: Configurazione delle schede di contenuto
description: Prerequisiti per il canale delle schede di contenuto
feature: Channel Configuration, Content Cards
topic: Content Management
role: Admin
level: Experienced
exl-id: df92e319-1e42-486f-b688-595964a762c9
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 5%

---

# Prerequisiti per le schede contenuto {#content-card-configuration-prereq}

Affinché Adobe Journey Optimizer visualizzi correttamente le schede di contenuto, devi configurare le seguenti impostazioni Adobe Experience Platform:

* **Raccolta dati di Adobe Experience Platform**

  [Crea uno stream di dati](https://experienceleague.adobe.com/it/docs/experience-platform/datastreams/configure) e [aggiungi il servizio Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/datastreams/configure#aep). Abilita le opzioni **[!UICONTROL Segmentazione Edge]** e **[!UICONTROL Adobe Journey Optimizer]**. In questo modo gli eventi Journey Optimizer vengono gestiti da Adobe Experience Platform Edge Network.
Aggiungi il gruppo di campi **Evento esperienza - Interazione proposta** al set di dati per includere i dati nei rapporti. [Ulteriori informazioni sugli stream di dati](https://experienceleague.adobe.com/it/docs/experience-platform/datastreams/configure)

* **Adobe Experience Platform**

  Verifica che il criterio di unione predefinito abbia **Criterio di unione attivo su Edge** abilitato nel menu Experience Platform **[!UICONTROL Cliente]** > **[!UICONTROL Profili]** > **[!UICONTROL Criteri di unione]**. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=it#configure){target="_blank"}

  >[!NOTE]
  >
  >Quando utilizzi un criterio di unione personalizzato **[!UICONTROL Preferenza set di dati]**, assicurati di aggiungere il set di dati **[!UICONTROL Percorso in entrata]** all&#39;interno del criterio di unione specificato.

* **Adobe Experience Platform Mobile o Platform Web SDK**

  Per le applicazioni per dispositivi mobili e Web, per aggiungere modifiche alle pagine Web o alle app per dispositivi mobili, devi implementare [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/it/docs/platform-learn/implement-web-sdk/overview) sul tuo sito Web o [Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/home/) nelle tue app per dispositivi mobili.

* **Journey Optimizer**

  Crea una [configurazione scheda di contenuto](#content-card-configuration).

* **Risoluzione dei problemi**

  Utilizza la visualizzazione **Edge Delivery** in **Adobe Experience Platform Assurance** per risolvere i problemi delle esperienze mobili. Può esaminare le richieste, verificare le chiamate edge ed esaminare i dati del profilo. [Ulteriori informazioni](https://experienceleague.adobe.com/it/docs/experience-platform/assurance/view/edge-delivery)

* **Esperimenti contenuto**

  Assicurati che il set di dati utilizzato nello [stream di dati](https://experienceleague.adobe.com/it/docs/experience-platform/datastreams/overview#_blank) dell&#39;app sia incluso anche nella configurazione di reporting dell&#39;esperimento sui contenuti. I dati dell’app non vengono visualizzati nei rapporti se i set di dati non corrispondono.

  Scopri come aggiungere set di dati per i rapporti sull’esperimento dei contenuti in [questa sezione](../reports/reporting-configuration.md).
