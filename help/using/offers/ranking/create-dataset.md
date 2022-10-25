---
product: experience platform
solution: Experience Platform
title: Creare un set di dati per raccogliere gli eventi
description: Scopri come creare un set di dati per raccogliere gli eventi
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 99963ef4-0b19-475e-96f4-2eac3f680c6f
source-git-commit: 5abcef4ff057bb351abaafbf4dcb99e1ab61c6a9
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 16%

---

# Creare un set di dati per raccogliere gli eventi {#create-dataset}

Prima di creare un modello AI, devi creare un set di dati in cui verranno raccolti gli eventi di conversione. Inizia creando lo schema che verrà utilizzato nel set di dati:

1. Da **[!UICONTROL Gestione dati]** menu, seleziona **[!UICONTROL Schema]**, vai al **[!UICONTROL Sfoglia]** e fai clic su **[!UICONTROL Creare uno schema]**.

   ![](../assets/ai-ranking-create-schema.png)

1. Scegli **[!UICONTROL ExperienceEvent XDM]**.

   ![](../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >Ulteriori informazioni sugli schemi e sui gruppi di campi XDM nella [Documentazione di panoramica del sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target=&quot;_blank&quot;}.

1. Da **[!UICONTROL Gruppi di campi]** a sinistra, seleziona **[!UICONTROL Aggiungi]**.

   ![](../assets/ai-ranking-fields-groups.png)

1. In **[!UICONTROL Ricerca]** digitare &quot;proposition Interposition&quot; e selezionare il campo **[!UICONTROL Evento esperienza - Interazioni proposte]** gruppo di campi.

   ![](../assets/ai-ranking-proposition-interactions.png)

   >[!CAUTION]
   >
   >Lo schema che verrà utilizzato nel set di dati deve avere **[!UICONTROL Evento esperienza - Interazioni proposte]** gruppo di campi associato. In caso contrario, non potrai utilizzarlo nella tua strategia di classificazione.

1. Fai clic su **[!UICONTROL Aggiungi gruppi di campi]**.

   ![](../assets/ai-ranking-add-field-group.png)

   >[!NOTE]
   >Il gruppo di campi era precedentemente noto come mixin.

1. Digitare un nome e salvare lo schema.

>[!NOTE]
>
>Ulteriori informazioni sulla creazione degli schemi in [Nozioni di base sulla composizione dello schema](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#understanding-schemas){target=&quot;_blank&quot;}.

Ora puoi creare un set di dati utilizzando questo schema. Per farlo, segui la procedura indicata di seguito:

1. Da **[!UICONTROL Gestione dati]** menu, seleziona **[!UICONTROL Set di dati]**, vai al **[!UICONTROL Sfoglia]** e fai clic su **[!UICONTROL Creare un set di dati]**.

   ![](../assets/ai-ranking-create-dataset.png)

1. Seleziona **[!UICONTROL Creare un set di dati dallo schema]**.

   ![](../assets/ai-ranking-create-dataset-from-schema.png)

1. Seleziona dall’elenco lo schema appena creato.

   ![](../assets/ai-ranking-dataset-select-schema.png)

1. Fai clic su **[!UICONTROL Avanti]**.

1. Immetti un nome univoco per il set di dati nel **[!UICONTROL Nome]** campo e fai clic su **[!UICONTROL Fine]**.

   ![](../assets/ai-ranking-dataset-name.png)

Il set di dati è ora pronto per essere selezionato per raccogliere i dati dell’evento quando [creazione di una strategia di classificazione](#create-ranking-strategy).
