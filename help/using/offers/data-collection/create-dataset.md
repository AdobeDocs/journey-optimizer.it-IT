---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Creare un set di dati per raccogliere gli eventi
description: Scopri come creare un set di dati per raccogliere gli eventi
badge: label="Legacy" type="Informative"
feature: Ranking, Decision Management, Datasets
role: Developer
level: Experienced
exl-id: 99963ef4-0b19-475e-96f4-2eac3f680c6f
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/SnbdXcSaDXxO1OapmRL3YYwRmCbBFqcuPlxFt-NEZCc
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: d3cdead0-685a-4489-9250-4bb709942f66id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 289
ht-degree: 15%

---

# Creare un set di dati per raccogliere gli eventi {#create-dataset}

>[!TIP]
>
>La funzione Decisioni, la nuova funzionalità decisionale di [!DNL Adobe Journey Optimizer], è ora disponibile tramite i canali e-mail e di esperienza basati su codice. [Ulteriori informazioni](../../experience-decisioning/gs-experience-decisioning.md)

Per raccogliere eventi di esperienza, devi innanzitutto creare un set di dati in cui verranno inviati questi eventi.

Inizia creando lo schema che verrà utilizzato nel set di dati:

1. Dal menu **[!UICONTROL Gestione dati]**, selezionare **[!UICONTROL Schema]**.

1. Fai clic su **[!UICONTROL Crea schema]**, in alto a destra, seleziona **[!UICONTROL Evento esperienza]** e fai clic su **Avanti**.

   ![](../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >Ulteriori informazioni sugli schemi e sui gruppi di campi XDM nella [documentazione di panoramica del sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target="_blank"}.

1. Immetti un nome e una descrizione per lo schema e fai clic su **Fine**.
   ![](../assets/ai-ranking-xdm-event-2.png)

1. Dalla sezione **[!UICONTROL Gruppi di campi]** a sinistra, seleziona **[!UICONTROL Aggiungi]**.

   ![](../assets/ai-ranking-fields-groups.png)

1. Nel campo **[!UICONTROL Ricerca]** digitare &quot;interazione della proposta&quot;.

1. Seleziona il gruppo di campi **[!UICONTROL Evento esperienza - Interazioni proposte]** e fai clic su **[!UICONTROL Aggiungi gruppi di campi]**.

   ![](../assets/ai-ranking-add-field-group.png)

   >[!CAUTION]
   >
   >Allo schema che verrà utilizzato nel set di dati deve essere associato il gruppo di campi **[!UICONTROL Evento esperienza - Interazioni proposta]**. In caso contrario, non potrai utilizzarlo nel modello di intelligenza artificiale.

1. Salva lo schema.

>[!NOTE]
>
>Ulteriori informazioni sulla creazione di schemi in [Nozioni di base sulla composizione dello schema](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html#understanding-schemas){target="_blank"}.

ora puoi creare un set di dati utilizzando questo schema. Per farlo, segui la procedura indicata di seguito:

1. Dal menu **[!UICONTROL Gestione dati]**, seleziona **[!UICONTROL Set di dati]** e passa alla scheda **[!UICONTROL Sfoglia]**.

1. Fai clic su **[!UICONTROL Crea set di dati]** e seleziona **[!UICONTROL Crea set di dati dallo schema]**.

   ![](../assets/ai-ranking-create-dataset-from-schema.png)

1. Seleziona lo schema appena creato dall&#39;elenco e fai clic su **[!UICONTROL Avanti]**.

1. Fornisci un nome univoco per il set di dati nel campo **[!UICONTROL Name]** e fai clic su **[!UICONTROL Finish]**.

   ![](../assets/ai-ranking-dataset-name.png)

>[!NOTE]
>
>È ora possibile selezionare questo set di dati per raccogliere i dati dell&#39;evento durante la [creazione di un modello di IA](../ranking/create-ranking-strategies.md).
