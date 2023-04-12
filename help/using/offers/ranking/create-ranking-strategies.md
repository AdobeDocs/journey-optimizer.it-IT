---
product: experience platform
solution: Experience Platform
title: Crea modelli AI
description: Scopri come creare modelli AI per classificare le offerte
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 81d07ec8-e808-4bc6-97b1-b9f7db2aec22
source-git-commit: b06b545d377fcd1ffe6ed218badeb94c1bb85ef2
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 6%

---

# Crea modelli AI {#ai-rankings}

[!DNL Journey Optimizer] consente di creare **Modelli AI** per classificare le offerte in base ai tuoi obiettivi aziendali.

>[!CAUTION]
>
>Per creare, modificare o eliminare modelli AI, è necessario disporre della **Gestire le strategie di classificazione** autorizzazione. [Ulteriori informazioni](../../administration/high-low-permissions.md#manage-ranking-strategies)

## Creare un modello IA {#create-ranking-strategy}

Per creare un modello AI, segui i passaggi seguenti:

1. Crea un set di dati in cui verranno raccolti gli eventi di conversione. [Scopri come](../data-collection/create-dataset.md)

1. In **[!UICONTROL Componenti]** accedere al menu **[!UICONTROL Classifica]** , quindi seleziona **[!UICONTROL Modelli AI]**.

   ![](../assets/ai-ranking-list.png)

   Vengono elencati tutti i modelli di intelligenza artificiale creati finora.

1. Fai clic sul pulsante **[!UICONTROL Creare un modello AI]** pulsante .

1. Specifica un nome univoco e una descrizione per il modello AI, quindi seleziona il tipo di modello AI che desideri creare:

   * **[!UICONTROL Ottimizzazione automatica]** ottimizza le offerte in base alle prestazioni delle offerte passate. [Ulteriori informazioni](auto-optimization-model.md)
   * **[!UICONTROL Personalizzato]** ottimizza e personalizza le offerte in base ai segmenti e alle prestazioni delle offerte. [Ulteriori informazioni](personalized-optimization-model.md)

   ![](../assets/ai-ranking-fields.png)

   >[!NOTE]
   >
   >La **[!UICONTROL Metrica di ottimizzazione]** fornisce informazioni sull’evento di conversione utilizzato dal modello AI per calcolare la classificazione delle offerte.
   >
   >[!DNL Journey Optimizer] offerte di classificazione basate su **tasso di conversione** (Tasso di conversione = Numero totale di eventi di conversione / Numero totale di eventi di impression). Il tasso di conversione viene calcolato utilizzando due tipi di metriche:
   >* **Eventi di impression** (offerte visualizzate)
   >* **Eventi di conversione** (offerte che generano clic tramite e-mail o web).

   >
   >Questi eventi vengono acquisiti automaticamente utilizzando l’SDK per web o l’SDK per dispositivi mobili fornito. Ulteriori informazioni su questo in [Panoramica di Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=it).

1. Seleziona i set di dati in cui vengono raccolti gli eventi di conversione e impression. Scopri come creare tale set di dati in [questa sezione](../data-collection/create-dataset.md). <!--This dataset needs to be associated with a schema that must have the **[!UICONTROL Proposition Interactions]** field group (previously known as mixin) associated with it.-->

   ![](../assets/ai-ranking-dataset-id.png)

   >[!CAUTION]
   >
   >Solo i set di dati creati dagli schemi associati alla **[!UICONTROL Evento esperienza - Interazioni proposte]** i gruppi di campi (precedentemente noti come mixin) vengono visualizzati nell’elenco a discesa.

1. Se stai creando un **[!UICONTROL Personalizzazione]** Modello AI, seleziona i segmenti da utilizzare per addestrare il modello AI.

   ![](../assets/ai-ranking-segments.png)

   >[!NOTE]
   >
   >Puoi selezionare fino a 5 segmenti.

1. Salva e attiva il modello AI.

   ![](../assets/ai-ranking-save-activate.png)

<!--At this point, you must have:

* created the AI model,
* defined which type of event you want to capture - offer displayed (impression) and/or offer clicked (conversion),
* and in which dataset you want to collect the event data.-->

Ora ogni volta che un’offerta viene visualizzata e/o fai clic su di essa, desideri che l’evento corrispondente venga catturato automaticamente da **[!UICONTROL Evento esperienza - Interazioni proposte]** gruppo di campi utilizzando [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html#what-is-adobe-experience-platform-web-sdk%3F){target="_blank"} o Mobile SDK.

Per poter inviare tipi di evento (offerta visualizzata o offerta su cui è stato fatto clic), devi impostare il valore corretto per ciascun tipo di evento in un evento di esperienza inviato in Adobe Experience Platform. [Scopri come](../data-collection/schema-requirement.md)