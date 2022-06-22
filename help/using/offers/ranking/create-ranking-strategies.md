---
product: experience platform
solution: Experience Platform
title: Crea modelli AI
description: Scopri come creare modelli AI per classificare le offerte
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 81d07ec8-e808-4bc6-97b1-b9f7db2aec22
source-git-commit: 12b01cb9de84399e5ede987866609acc10b64c5f
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 9%

---

# Crea modelli AI {#ai-rankings}

[!DNL Journey Optimizer] consente di creare **Modelli AI** per classificare le offerte in base ai tuoi obiettivi aziendali.

>[!CAUTION]
>
>Per creare, modificare o eliminare modelli AI, è necessario disporre della **Gestire le strategie di classificazione** autorizzazione. [Ulteriori informazioni](../../administration/high-low-permissions.md#manage-ranking-strategies)

## Creare un modello IA {#create-ranking-strategy}

Per creare un modello AI, segui i passaggi seguenti:

1. In **[!UICONTROL Components]** accedere al menu **[!UICONTROL Ranking]** , quindi seleziona **[!UICONTROL AI models]**.

   ![](../assets/ai-ranking-list.png)

   Vengono elencati tutti i modelli di intelligenza artificiale creati finora.

1. Fai clic sul pulsante **[!UICONTROL Create AI model]**.

1. Specifica un nome univoco e una descrizione per il modello AI.

   <!--* **[!UICONTROL Auto-optimization]** optimizes offers based on past offer performance. [Learn more](auto-optimization-model.md)
    * **[!UICONTROL Personalized]** optimizes and personalizes offers based on segments and offer performance. [Learn more](personalized-optimization-model.md)-->

   ![](../assets/ai-ranking-fields.png)

   >[!NOTE]
   >
   >La **[!UICONTROL Optimization metric]** fornisce informazioni sull’evento di conversione utilizzato dal modello AI per calcolare la classificazione delle offerte.
   >
   >[!DNL Journey Optimizer] offerte di classificazione basate su **tasso di conversione** (Tasso di conversione = Numero totale di eventi di conversione / Numero totale di eventi di impression). Il tasso di conversione viene calcolato utilizzando due tipi di metriche:
   >* **Eventi di impression** (offerte visualizzate)
   >* **Eventi di conversione** (offerte che generano clic tramite e-mail o web).

   >
   >Questi eventi vengono acquisiti automaticamente utilizzando l’SDK per web o l’SDK per dispositivi mobili fornito. Ulteriori informazioni su questo in [Panoramica di Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=it).

1. Seleziona i set di dati in cui vengono raccolti gli eventi di conversione e impression. Scopri come creare tale set di dati in [questa sezione](#create-dataset). <!--This dataset needs to be associated with a schema that must have the **[!UICONTROL Proposition Interactions]** field group (previously known as mixin) associated with it.-->

   ![](../assets/ai-ranking-dataset-id.png)

   >[!CAUTION]
   >
   >Solo i set di dati creati dagli schemi associati alla **[!UICONTROL Experience Event - Proposition Interactions]** i gruppi di campi (precedentemente noti come mixin) vengono visualizzati nell’elenco a discesa.

<!--1. If you are creating a **[!UICONTROL Personalization]** AI model, select the segment(s) to use to train the AI model.

    ![](../assets/ai-ranking-segments.png)

    >[!NOTE]
    >
    >You can select up to 5 segments.-->

1. Salva e attiva il modello AI.

   ![](../assets/ai-ranking-save-activate.png)
