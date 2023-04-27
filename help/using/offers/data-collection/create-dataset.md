---
product: experience platform
solution: Experience Platform
title: Creare un set di dati per raccogliere gli eventi
description: Scopri come creare un set di dati per raccogliere gli eventi
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 99963ef4-0b19-475e-96f4-2eac3f680c6f
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 15%

---

# Creare un set di dati per raccogliere gli eventi {#create-dataset}

Per raccogliere gli eventi di esperienza, devi innanzitutto creare un set di dati in cui tali eventi verranno inviati.

Inizia creando lo schema che verrà utilizzato nel set di dati:

1. Da **[!UICONTROL Gestione dati]** menu, seleziona **[!UICONTROL Schema]** e vai al **[!UICONTROL Sfoglia]** scheda .

1. Fai clic su **[!UICONTROL Creare uno schema]** e scegli **[!UICONTROL ExperienceEvent XDM]**.

   ![](../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >Ulteriori informazioni sugli schemi e sui gruppi di campi XDM nella [Documentazione di panoramica del sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target="_blank"}.

1. Da **[!UICONTROL Gruppi di campi]** a sinistra, seleziona **[!UICONTROL Aggiungi]**.

   ![](../assets/ai-ranking-fields-groups.png)

1. In **[!UICONTROL Ricerca]** campo, digitare &quot;proposition interposition&quot;.

1. Seleziona la **[!UICONTROL Evento esperienza - Interazioni proposte]** gruppo di campi e fai clic su **[!UICONTROL Aggiungi gruppi di campi]**.

   ![](../assets/ai-ranking-add-field-group.png)

   >[!CAUTION]
   >
   >Lo schema che verrà utilizzato nel set di dati deve avere **[!UICONTROL Evento esperienza - Interazioni proposte]** gruppo di campi associato. In caso contrario, non potrai utilizzarlo nella tua strategia di classificazione.

1. Digitare un nome e salvare lo schema.

>[!NOTE]
>
>Ulteriori informazioni sulla creazione degli schemi in [Nozioni di base sulla composizione dello schema](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#understanding-schemas){target="_blank"}.

Ora puoi creare un set di dati utilizzando questo schema. Per farlo, segui la procedura indicata di seguito:

1. Da **[!UICONTROL Gestione dati]** menu, seleziona **[!UICONTROL Set di dati]** e vai al **[!UICONTROL Sfoglia]** scheda .

1. Fai clic su **[!UICONTROL Creare un set di dati]** e seleziona **[!UICONTROL Creare un set di dati dallo schema]**.

   ![](../assets/ai-ranking-create-dataset-from-schema.png)

1. Seleziona lo schema appena creato dall’elenco e fai clic su **[!UICONTROL Successivo]**.

1. Immetti un nome univoco per il set di dati nel **[!UICONTROL Nome]** campo e fai clic su **[!UICONTROL Fine]**.

   ![](../assets/ai-ranking-dataset-name.png)

>[!NOTE]
>
>Questo set di dati può ora essere selezionato per raccogliere i dati dell’evento quando [creazione di una strategia di classificazione](#create-ranking-strategy).
