---
product: experience platform
solution: Experience Platform
title: Creare un set di dati per raccogliere gli eventi
description: Scopri come creare un set di dati per raccogliere gli eventi
feature: Ranking, Decision Management, Datasets
role: Developer
level: Experienced
hide: true
hidefromtoc: true
exl-id: 96c1326f-be40-4738-8997-a67dc14872bb
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 7%

---

# Creare un set di dati per raccogliere gli eventi {#create-dataset}

Per raccogliere eventi di esperienza, devi innanzitutto creare un set di dati in cui verranno inviati questi eventi.

Inizia creando lo schema che verrà utilizzato nel set di dati:

1. Dal menu **[!UICONTROL Gestione dati]**, selezionare **[!UICONTROL Schema]**.

1. Fai clic su **[!UICONTROL Crea schema]**, in alto a destra, seleziona **[!UICONTROL Evento esperienza]** e fai clic su **Avanti**.

   ![](../../offers/assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >Ulteriori informazioni sugli schemi e sui gruppi di campi XDM nella [documentazione di panoramica del sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target="_blank"}.

1. Immetti un nome e una descrizione per lo schema e fai clic su **Fine**.
   ![](../../offers/assets/ai-ranking-xdm-event-2.png)

1. Dalla sezione **[!UICONTROL Gruppi di campi]** a sinistra, seleziona **[!UICONTROL Aggiungi]**.

   ![](../../offers/assets/ai-ranking-fields-groups.png)

1. Nel campo **[!UICONTROL Ricerca]** digitare &quot;interazione della proposta&quot;.

1. Seleziona il gruppo di campi **[!UICONTROL Evento esperienza - Interazioni proposte]** e fai clic su **[!UICONTROL Aggiungi gruppi di campi]**.

   ![](../../offers/assets/ai-ranking-add-field-group.png)

   >[!CAUTION]
   >
   >Allo schema che verrà utilizzato nel set di dati deve essere associato il gruppo di campi **[!UICONTROL Evento esperienza - Interazioni proposta]**. In caso contrario, non potrai utilizzarlo nel modello di intelligenza artificiale.

1. Salva lo schema.

>[!NOTE]
>
>Ulteriori informazioni sulla creazione di schemi in [Nozioni di base sulla composizione dello schema](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=it#understanding-schemas){target="_blank"}.

Ora puoi creare un set di dati utilizzando questo schema. Per farlo, segui la procedura indicata di seguito:

1. Dal menu **[!UICONTROL Gestione dati]**, seleziona **[!UICONTROL Set di dati]** e passa alla scheda **[!UICONTROL Sfoglia]**.

1. Fai clic su **[!UICONTROL Crea set di dati]** e seleziona **[!UICONTROL Crea set di dati dallo schema]**.

   ![](../../offers/assets/ai-ranking-create-dataset-from-schema.png)

1. Seleziona lo schema appena creato dall&#39;elenco e fai clic su **[!UICONTROL Avanti]**.

1. Fornisci un nome univoco per il set di dati nel campo **[!UICONTROL Name]** e fai clic su **[!UICONTROL Finish]**.

   ![](../../offers/assets/ai-ranking-dataset-name.png)

>[!NOTE]
>
>È ora possibile selezionare questo set di dati per raccogliere i dati evento durante la creazione di un [modello di IA](../ranking/create-ai-models.md).
