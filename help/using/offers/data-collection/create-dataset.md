---
product: experience platform
solution: Experience Platform
title: Creare un set di dati per raccogliere gli eventi
description: Scopri come creare un set di dati per raccogliere gli eventi
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 99963ef4-0b19-475e-96f4-2eac3f680c6f
source-git-commit: 7f5085e1f615917181dc618ec1006b4526346afe
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 17%

---

# Creare un set di dati per raccogliere gli eventi {#create-dataset}

Per raccogliere eventi di esperienza, devi innanzitutto creare un set di dati in cui verranno inviati questi eventi.

Inizia creando lo schema che verrà utilizzato nel set di dati:

1. Dalla sezione **[!UICONTROL Gestione dati]** menu, seleziona **[!UICONTROL Schema]**.

1. Clic **[!UICONTROL Crea schema]**, in alto a destra, seleziona **[!UICONTROL Evento esperienza]** e fai clic su **Successivo**.

   ![](../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >Ulteriori informazioni sugli schemi e sui gruppi di campi XDM nella [Documentazione di panoramica del sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target="_blank"}.

1. Immetti un nome e una descrizione per lo schema e fai clic su **Fine**.
   ![](../assets/ai-ranking-xdm-event-2.png)

1. Dalla sezione **[!UICONTROL Gruppi di campi]** a sinistra, seleziona **[!UICONTROL Aggiungi]**.

   ![](../assets/ai-ranking-fields-groups.png)

1. In **[!UICONTROL Ricerca]** , digita &quot;interazione della proposta&quot;.

1. Seleziona la **[!UICONTROL Evento esperienza - Interazioni proposte]** gruppo di campi e fare clic su **[!UICONTROL Aggiungi gruppi di campi]**.

   ![](../assets/ai-ranking-add-field-group.png)

   >[!CAUTION]
   >
   >Lo schema che verrà utilizzato nel set di dati deve avere **[!UICONTROL Evento esperienza - Interazioni proposte]** gruppo di campi ad esso associato. In caso contrario, non potrai utilizzarlo nel modello di intelligenza artificiale.

1. Salva lo schema.

>[!NOTE]
>
>Ulteriori informazioni sulla creazione di schemi in [Nozioni di base sulla composizione dello schema](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=it#understanding-schemas){target="_blank"}.

Ora puoi creare un set di dati utilizzando questo schema. Per farlo, segui la procedura indicata di seguito:

1. Dalla sezione **[!UICONTROL Gestione dati]** menu, seleziona **[!UICONTROL Set di dati]** e vai al **[!UICONTROL Sfoglia]** scheda.

1. Clic **[!UICONTROL Crea set di dati]** e seleziona **[!UICONTROL Crea set di dati dallo schema]**.

   ![](../assets/ai-ranking-create-dataset-from-schema.png)

1. Seleziona lo schema appena creato dall’elenco e fai clic su **[!UICONTROL Successivo]**.

1. Fornisci un nome univoco per il set di dati nel **[!UICONTROL Nome]** e fai clic su **[!UICONTROL Fine]**.

   ![](../assets/ai-ranking-dataset-name.png)

>[!NOTE]
>
>Ora è possibile selezionare questo set di dati per raccogliere i dati dell’evento quando [creazione di un modello di IA](../ranking/create-ranking-strategies.md).
