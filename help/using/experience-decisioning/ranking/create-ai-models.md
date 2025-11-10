---
product: experience platform
solution: Experience Platform
title: Creare modelli IA
description: Scopri come creare modelli AI per classificare le offerte
feature: Ranking, Decision Management
role: User
level: Intermediate
exl-id: 532392d6-3637-4381-984d-f5b630f6d32d
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '679'
ht-degree: 15%

---

# Creare modelli AI {#create-ai-models}

[!DNL Journey Optimizer] consente di creare **modelli di IA** per classificare le offerte in base agli obiettivi aziendali.

>[!CAUTION]
>
>Per creare, modificare o eliminare modelli AI, è necessario disporre dell&#39;autorizzazione **Gestisci strategie di classificazione**. [Ulteriori informazioni](../../administration/high-low-permissions.md#manage-ranking-strategies)

## Creare un modello IA {#create-ranking-strategy}

>[!CONTEXTUALHELP]
>id="ajo_exd_ai_model_metric"
>title="Metrica di ottimizzazione"
>abstract="[!DNL Journey Optimizer] classifica le offerte in base al **tasso di conversione** (tasso di conversione = numero totale di eventi di conversione / numero totale di eventi di impression). Il tasso di conversione viene calcolato utilizzando due tipi di metriche: **Eventi di impression** (offerte visualizzate) e **Eventi di conversione** (offerte che generano clic tramite e-mail o Web). Questi eventi vengono acquisiti automaticamente utilizzando il Web SDK o il Mobile SDK fornito."

Per creare un modello di IA, segui i passaggi seguenti:

1. Crea un set di dati in cui verranno raccolti gli eventi di conversione. [Scopri come](../data-collection/create-dataset.md)

1. Passa al menu **[!UICONTROL Decisioning]** > **[!UICONTROL Imposta strategia]** e seleziona **[!UICONTROL Modelli AI]**.

   ![](../assets/ai-model-list.png)

   Vengono elencati tutti i modelli di IA creati finora.

1. Fare clic sul pulsante **[!UICONTROL Crea modello di IA]**.

1. Specifica un nome univoco e, se necessario, una descrizione per il modello di IA.

1. Seleziona il tipo di modello di IA da creare:

   * **[!UICONTROL Ottimizzazione automatica]** ottimizza le offerte in base alle prestazioni delle offerte passate. [Ulteriori informazioni](auto-optimization-model.md)
   * **[!UICONTROL Ottimizzazione personalizzata]** ottimizza e personalizza le offerte in base al pubblico e alle prestazioni delle offerte. [Ulteriori informazioni](personalized-optimization-model.md)

   ![](../assets/ai-model-types.png)

1. La sezione **[!UICONTROL Metrica di ottimizzazione]** fornisce informazioni sull&#39;evento di conversione utilizzato dal modello di intelligenza artificiale per calcolare la classificazione delle offerte.

   [!DNL Journey Optimizer] classifica le offerte in base al **tasso di conversione** (tasso di conversione = numero totale di eventi di conversione / numero totale di eventi di impression). Il tasso di conversione viene calcolato utilizzando due tipi di metriche:
   * **Eventi di impression** (offerte visualizzate)
   * **Eventi di conversione** (offerte che generano clic via e-mail o web).

   Questi eventi vengono acquisiti automaticamente utilizzando il Web SDK o il SDK mobile fornito. Ulteriori informazioni sono disponibili nella panoramica di [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=it).

   +++ Ottimizzazione dei modelli sulle metriche [!DNL Customer Journey Analytics] personalizzate

   >[!NOTE]
   >
   >Questa funzionalità è disponibile solo per [!DNL Customer Journey Analytics] clienti con diritti di amministratore.
   >
   >Prima di iniziare, assicurati di aver integrato Journey Optimizer con Customer Journey Analytics per esportare i set di dati di Journey Optimizer nelle visualizzazioni dati predefinite. [Scopri come sfruttare [!DNL Journey Optmizer] i dati in [!DNL Customer Journey Analytics]](../../reports/cja-ajo.md)

   I modelli di **[!UICONTROL ottimizzazione personalizzata]** sono un tipo di modello di intelligenza artificiale che ti consente di definire obiettivi aziendali e utilizza i dati dei clienti per addestrare modelli orientati al business per distribuire offerte personalizzate e massimizzare i KPI.

   Per impostazione predefinita, i modelli di ottimizzazione personalizzati utilizzano **clic sull&#39;offerta** come metrica di ottimizzazione. Se lavori con [!DNL Customer Journey Analytics], [!DNL Decisioning] ti consente di sfruttare le tue metriche personalizzate per ottimizzare il tuo modello su.

   A questo scopo, seleziona il tipo di modello **[!UICONTROL Ottimizzazione personalizzata]** ed espandi il menu a discesa **[!UICONTROL Evento di conversione]**. Tutte le metriche della [!DNL Customer Journey Analytics] [visualizzazione dati](https://experienceleague.adobe.com/it/docs/analytics-platform/using/cja-dataviews/data-views){target="_blank"} predefinita vengono visualizzate nell&#39;elenco. Seleziona la metrica su cui desideri ottimizzare il modello.

   ![](../assets/ai-model-custom-metrics.png){width=85%}

   >[!NOTE]
   >
   >Per impostazione predefinita, le metriche in [!DNL Customer Journey Analytics] utilizzano un modello di attribuzione &quot;Last Touch&quot; (Ultimo contatto), che assegna il 100% del credito al punto di contatto che si verifica più di recente prima della conversione.
   >
   >Anche se è possibile modificare il modello di attribuzione, non tutti i modelli di attribuzione sono ideali per l’ottimizzazione del modello di IA. È consigliabile selezionare con attenzione un modello di attribuzione in linea con gli obiettivi di ottimizzazione per garantire l’accuratezza e le prestazioni del modello.
   >
   >Per ulteriori dettagli sui modelli di attribuzione disponibili e indicazioni sul loro utilizzo, consulta la [[!DNL Customer Journey Analytics] documentazione](https://experienceleague.adobe.com/it/docs/analytics-platform/using/cja-dataviews/component-settings/attribution){target="_blank"}

   +++

1. Seleziona i set di dati in cui vengono raccolti gli eventi di conversione e di impression. Scopri come creare tali set di dati in [questa sezione](../data-collection/create-dataset.md).

   ![](../assets/ai-model-datasets.png){width=85%}

   >[!CAUTION]
   >
   >Nell&#39;elenco a discesa vengono visualizzati solo i set di dati creati da schemi associati al gruppo di campi **[!UICONTROL Evento esperienza - Interazioni proposta]** (precedentemente noto come mixin).

1. Se stai creando un modello di IA **[!UICONTROL Ottimizzazione personalizzata]**, seleziona i segmenti da utilizzare per addestrare il modello di IA.

   <!--➡️ [Discover this feature in video](#video)-->

   >[!NOTE]
   >
   >Puoi selezionare fino a 5 tipi di pubblico.

1. Salva e attiva il modello di intelligenza artificiale.

<!--At this point, you must have:

* created the AI model,
* defined which type of event you want to capture - offer displayed (impression) and/or offer clicked (conversion),
* and in which dataset you want to collect the event data.-->

Ogni volta che si visualizza e/o si fa clic su un&#39;offerta, si desidera che l&#39;evento corrispondente venga acquisito automaticamente dal gruppo di campi **[!UICONTROL Experience Event - Proposition Interactions]** utilizzando [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html?lang=it#what-is-adobe-experience-platform-web-sdk%3F){target="_blank"} o Mobile SDK.

Per poter inviare in tipi di evento (offerta visualizzata o offerta selezionata), è necessario impostare il valore corretto per ciascun tipo di evento in un evento esperienza inviato in Adobe Experience Platform. [Scopri come](../data-collection/schema-requirement.md)

<!--
## How-to video {#video}

Learn how to create a personalized optimization model and how to apply it to a decision.

>[!VIDEO](https://video.tv.adobe.com/v/3445959?captions=ita&quality=12)-->
