---
product: experience platform
solution: Experience Platform
title: Creare un set di dati per raccogliere gli eventi
description: Scopri come creare un set di dati per raccogliere gli eventi
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 99963ef4-0b19-475e-96f4-2eac3f680c6f
source-git-commit: 17d37da6e6325d36df0f63122fa37f416e3f2c4c
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 13%

---

# Creare un set di dati per raccogliere gli eventi {#create-dataset}

Prima di creare un modello AI, devi creare un set di dati in cui verranno raccolti gli eventi di conversione. Inizia creando lo schema che verrà utilizzato nel set di dati:

1. Da **[!UICONTROL Data Management]** menu, seleziona **[!UICONTROL Schema]**, vai al **[!UICONTROL Browse]** e fai clic su **[!UICONTROL Create schema]**.

   ![](../assets/ai-ranking-create-schema.png)

1. Scegli **[!UICONTROL XDM ExperienceEvent]**.

   ![](../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >    Ulteriori informazioni sugli schemi e sui gruppi di campi XDM nella sezione [Panoramica del sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it).


1. In **[!UICONTROL Search]** digitare &quot;proposition Interposition&quot; e selezionare il campo **[!UICONTROL Experience Event - Proposition Interactions]** gruppo di campi.

   ![](../assets/ai-ranking-proposition-interactions.png)

   >[!CAUTION]
   >
   >    Lo schema che verrà utilizzato nel set di dati deve avere **[!UICONTROL Experience Event - Proposition Interactions]** gruppo di campi associato. In caso contrario, non potrai utilizzarlo nella tua strategia di classificazione.

1. Fai clic su **[!UICONTROL Add field groups]**.

   ![](../assets/ai-ranking-add-field-group.png)

   >[!NOTE]
   >Il gruppo di campi era precedentemente noto come mixin.

1. Digitare un nome e salvare lo schema.<!--How do you edit the fields in this new schema? Examples?-->

>[!NOTE]
>
>    Ulteriori informazioni sulla creazione degli schemi in [Nozioni di base sulla composizione dello schema](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#understanding-schemas).

Ora puoi creare un set di dati utilizzando questo schema. Per farlo, segui la procedura indicata di seguito:

1. Da **[!UICONTROL Data Management]** menu, seleziona **[!UICONTROL Datasets]**, vai al **[!UICONTROL Browse]** e fai clic su **[!UICONTROL Create dataset]**.

   ![](../assets/ai-ranking-create-dataset.png)

1. Seleziona **[!UICONTROL Create dataset from schema]**.

   ![](../assets/ai-ranking-create-dataset-from-schema.png)

1. Seleziona dall’elenco lo schema appena creato.

   ![](../assets/ai-ranking-dataset-select-schema.png)

1. Fai clic su **[!UICONTROL Next]**.

1. Immetti un nome univoco per il set di dati nel **[!UICONTROL Name]** campo e fai clic su **[!UICONTROL Finish]**.

   ![](../assets/ai-ranking-dataset-name.png)

Il set di dati è ora pronto per essere selezionato per raccogliere i dati dell’evento quando [creazione di una strategia di classificazione](#create-ranking-strategy).
