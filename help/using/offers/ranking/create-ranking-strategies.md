---
product: experience platform
solution: Experience Platform
title: Creare modelli IA
description: Scopri come creare modelli AI per classificare le offerte
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 81d07ec8-e808-4bc6-97b1-b9f7db2aec22
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 6%

---

# Creare modelli IA {#ai-rankings}

[!DNL Journey Optimizer] consente di creare **Modelli IA** per classificare le offerte in base agli obiettivi aziendali.

>[!CAUTION]
>
>Per creare, modificare o eliminare modelli AI, è necessario disporre del **Gestire le strategie di classificazione** autorizzazione. [Ulteriori informazioni](../../administration/high-low-permissions.md#manage-ranking-strategies)

## Creare un modello IA {#create-ranking-strategy}

Per creare un modello di IA, segui i passaggi seguenti:

1. Crea un set di dati in cui verranno raccolti gli eventi di conversione. [Scopri come](../data-collection/create-dataset.md)

1. In **[!UICONTROL Componenti]** , accedere al menu **[!UICONTROL Classificazione]** , quindi seleziona **[!UICONTROL Modelli IA]**.

   ![](../assets/ai-ranking-list.png)

   Vengono elencati tutti i modelli di IA creati finora.

1. Fai clic su **[!UICONTROL Crea modello di IA]** pulsante.

1. Specifica un nome univoco e una descrizione per il modello di IA, quindi seleziona il tipo di modello di IA da creare:

   * **[!UICONTROL Ottimizzazione automatica]** ottimizza le offerte in base alle prestazioni delle offerte passate. [Ulteriori informazioni](auto-optimization-model.md)
   * **[!UICONTROL Personalizzato]** ottimizza e personalizza le offerte in base al pubblico e alle prestazioni delle offerte. [Ulteriori informazioni](personalized-optimization-model.md)

   ![](../assets/ai-ranking-fields.png)

   >[!NOTE]
   >
   >Il **[!UICONTROL Metrica di ottimizzazione]** Questa sezione fornisce informazioni sull’evento di conversione utilizzato dal modello AI per calcolare la classificazione delle offerte.
   >
   >[!DNL Journey Optimizer] classifica le offerte in base al **tasso di conversione** (Tasso di conversione = Numero totale di eventi di conversione / Numero totale di eventi di impression). Il tasso di conversione viene calcolato utilizzando due tipi di metriche:
   >* **Eventi di impression** (offerte visualizzate)
   >* **Eventi di conversione** (offerte che si traducono in clic via e-mail o web).
   >
   >Questi eventi vengono acquisiti automaticamente tramite l’SDK web o l’SDK mobile fornito. Ulteriori informazioni in [Panoramica di Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=it).

1. Seleziona i set di dati in cui vengono raccolti gli eventi di conversione e di impression. Scopri come creare questo set di dati in [questa sezione](../data-collection/create-dataset.md). <!--This dataset needs to be associated with a schema that must have the **[!UICONTROL Proposition Interactions]** field group (previously known as mixin) associated with it.-->

   ![](../assets/ai-ranking-dataset-id.png)

   >[!CAUTION]
   >
   >Solo i set di dati creati da schemi associati al **[!UICONTROL Evento esperienza - Interazioni proposte]** nell’elenco a discesa viene visualizzato il gruppo di campi (precedentemente noto come mixin).

1. Se stai creando un **[!UICONTROL Ottimizzazione personalizzata]** Modello di IA, seleziona i tipi di pubblico da utilizzare per addestrare il modello di IA.

   ![](../assets/ai-ranking-segments.png)

   >[!NOTE]
   >
   >Puoi selezionare fino a 5 tipi di pubblico.

1. Salva e attiva il modello di intelligenza artificiale.

   ![](../assets/ai-ranking-save-activate.png)

<!--At this point, you must have:

* created the AI model,
* defined which type of event you want to capture - offer displayed (impression) and/or offer clicked (conversion),
* and in which dataset you want to collect the event data.-->

Ora, ogni volta che si visualizza e/o si fa clic su un’offerta, si desidera che l’evento corrispondente venga acquisito automaticamente da **[!UICONTROL Evento esperienza - Interazioni proposte]** gruppo di campi che utilizza [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html#what-is-adobe-experience-platform-web-sdk%3F){target="_blank"} o Mobile SDK.

Per poter inviare in tipi di evento (offerta visualizzata o offerta selezionata), è necessario impostare il valore corretto per ciascun tipo di evento in un evento esperienza inviato in Adobe Experience Platform. [Scopri come](../data-collection/schema-requirement.md)

## Video introduttivo {#video}

Scopri come creare un modello di ottimizzazione personalizzato e come applicarlo a una decisione.

>[!VIDEO](https://video.tv.adobe.com/v/3419954?quality=12)
