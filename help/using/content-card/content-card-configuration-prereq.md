---
title: Configurazione delle schede di contenuto
description: Prerequisiti per il canale delle schede di contenuto
feature: Channel Configuration
topic: Content Management
role: Admin
level: Experienced
badge: label="Disponibilità limitata" type="Informative"
hide: true
hidefromtoc: true
source-git-commit: 8a902298bbbac5689b4f84266dd9c9027e45fad5
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 7%

---

# Prerequisiti per le schede di contenuto {#content-card-configuration-prereq}

>[!BEGINSHADEBOX]

**Sommario**

* [Introduzione alle schede di contenuto](get-started-content-card.md)
* **Prerequisiti per le schede di contenuto**
* [Configurare il canale delle schede di contenuto in Journey Optimizer](content-card-configuration.md)
* [Creare schede di contenuto](create-content-card.md)
* [Progettare schede di contenuto](design-content-card.md)
* [Rapporto schede di contenuto](content-card-report.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Le schede dei contenuti sono attualmente disponibili solo per un set di organizzazioni (disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.

Affinché Adobe Journey Optimizer visualizzi correttamente le schede di contenuto, devi configurare le seguenti impostazioni Adobe Experience Platform:

* **Raccolta dati di Adobe Experience Platform**

  [Crea uno stream di dati](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure) e [aggiungi il servizio Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure#aep). Abilita le opzioni **[!UICONTROL Segmentazione Edge]** e **[!UICONTROL Adobe Journey Optimizer]**. In questo modo gli eventi Journey Optimizer vengono gestiti dall’Edge Network di Adobe Experience Platform. Per ulteriori informazioni su come configurare uno stream di dati, consulta la [documentazione sugli stream di dati](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure).

* **Adobe Experience Platform**

  Verifica che il criterio di unione predefinito abbia **Criterio di unione attivo su Edge** abilitato nel menu di Experience Platform **[!UICONTROL Cliente]** > **[!UICONTROL Profili]** > **[!UICONTROL Criteri di unione]**. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  >[!NOTE]
  >
  >Quando utilizzi un criterio di unione personalizzato **[!UICONTROL Preferenza set di dati]**, assicurati di aggiungere il set di dati **[!UICONTROL Percorso in entrata]** all&#39;interno del criterio di unione specificato.

* **Adobe Experience Platform Mobile o Platform Web SDK**

  Per le applicazioni per dispositivi mobili e Web, per aggiungere modifiche alle pagine Web o alle app per dispositivi mobili, devi implementare [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/it/docs/platform-learn/implement-web-sdk/overview) sul tuo sito Web o [Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/home/) nelle tue app per dispositivi mobili.

* **Journey Optimizer**

  Crea una [configurazione scheda di contenuto](#content-card-configuration).

* **Risoluzione dei problemi**

  Utilizza la visualizzazione **Edge Delivery** in **Adobe Experience Platform Assurance** per risolvere i problemi relativi alle esperienze mobili. Può esaminare le richieste, verificare le chiamate edge ed esaminare i dati del profilo. [Ulteriori informazioni](https://experienceleague.adobe.com/it/docs/experience-platform/assurance/view/edge-delivery)

* **Esperimenti contenuto**

  Assicurati che il set di dati utilizzato nello [stream di dati](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/overview#_blank) dell&#39;app sia incluso anche nella configurazione di reporting dell&#39;esperimento sui contenuti. I dati dell’app non vengono visualizzati nei rapporti se i set di dati non corrispondono.

  Scopri come aggiungere set di dati per i rapporti sull’esperimento dei contenuti in [questa sezione](../content-management/reporting-configuration.md).
