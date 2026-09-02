---
solution: Journey Optimizer
product: Journey Optimizer
title: Introduzione ai modelli AI
description: Scopri i modelli di intelligenza artificiale che consentono di classificare le offerte
feature: Ranking, Decisioning
topic: Artificial Intelligence
role: User
level: Intermediate
exl-id: 07679823-2288-4528-b09a-12fd76a69482
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/sWJEr5Pm1wl83Q-2HVb-7mqy7hasQ1ffqRDmJsOFomw
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8cid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: d3cdead0-685a-4489-9250-4bb709942f66
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
source-git-commit: ee394c77b226dd35a9c27f4a02e3b8d7a997ccbd
workflow-type: tm+mt
source-wordcount: 367
ht-degree: 20%

---

# Introduzione ai modelli AI {#ai-models}

>[!BEGINSHADEBOX]

**In questa pagina:** Comprendi i tipi di modelli di IA per l&#39;ottimizzazione automatica e l&#39;ottimizzazione personalizzata e i passaggi per generarli in modo da poter classificare le offerte in base ai tuoi obiettivi aziendali.

>[!ENDSHADEBOX]

[!DNL Journey Optimizer] consente di utilizzare un sistema di modelli addestrati che classifica le offerte da visualizzare per un determinato profilo.

Questa funzione ti consente di creare **modelli di IA** diversi in base agli obiettivi aziendali. Utilizzando queste diverse strategie basate su obiettivi in una decisione, il sistema di modelli addestrato ti aiuterà a capire in che modo i diversi modelli di intelligenza artificiale influiscono sui tuoi obiettivi.

<!--
For example, you can select an AI model for the email channel and another one for the push channel. For each channel, the trained model system will leverage multiple data points to determine which offer should be presented first for a given decision policy?, rather than taking into account the offers' priority scores or a [ranking formula](create-ranking-formulas.md).

>[!IMPORTANT]
>
>For now, ranking models are not supported in Journey Optimizer authored channels.
-->

## Tipi di modelli IA {#ai-model-types}

>[!CONTEXTUALHELP]
>id="ajo_exd_ai_model_type"
>title="Scegli il tipo di modello"
>abstract="Seleziona il tipo di modello di IA da creare: **Ottimizzazione automatica** ottimizza le offerte in base alle prestazioni delle offerte passate, mentre **Ottimizzazione personalizzata** ottimizza e personalizza le offerte in base al pubblico e alle prestazioni delle offerte."
>additional-url="https://experienceleague.adobe.com/it/docs/journey-optimizer/using/decisioning/offer-decisioning/rankings/ai-models/create-ranking-strategies#create-ranking-strategy" text="Creare un modello IA"

In [!DNL Journey Optimizer] sono disponibili due tipi di modelli di IA:

* I **modelli di ottimizzazione automatica** hanno lo scopo di distribuire le offerte che massimizzano il ritorno (KPI) impostato dai client aziendali. Questi KPI potrebbero essere sotto forma di tassi di conversione, ricavi, ecc. A questo punto, l’ottimizzazione automatica si concentra sull’ottimizzazione dei clic dell’offerta con la conversione dell’offerta come obiettivo. L’ottimizzazione automatica non è personalizzata e viene ottimizzata in base alle prestazioni &quot;globali&quot; delle offerte. [Ulteriori informazioni](auto-optimization-model.md)

* I **modelli di ottimizzazione personalizzati** ti consentono di definire gli obiettivi aziendali e di utilizzare i dati dei clienti per addestrare modelli orientati al business in modo da distribuire offerte personalizzate e massimizzare i KPI. [Ulteriori informazioni](personalized-optimization-model.md)

## Creare un modello di IA {#create-ai-model}

I passaggi principali per poter creare e utilizzare modelli di intelligenza artificiale sono i seguenti:

1. Crea un set di dati in cui verranno raccolti gli eventi di conversione e di impression. [Ulteriori informazioni](../data-collection/create-dataset.md)

1. Crea un modello di intelligenza artificiale che sfrutta gli eventi del set di dati per classificare le offerte. [Ulteriori informazioni](create-ai-models.md)

1. Configura lo schema di offerta per acquisire automaticamente gli eventi. [Ulteriori informazioni](../data-collection/schema-requirement.md)

   >[!IMPORTANT]
   >
   >Per poter essere raccolti, i modelli di classificazione richiedono l’invio di eventi di feedback come eventi di esperienza. [Ulteriori informazioni sulla raccolta dati Decisioning](../data-collection/data-collection.md)

1. Assegna il modello di IA a una strategia di selezione per classificare le offerte idonee. [Ulteriori informazioni](../selection-strategies.md#select-ranking-method)

1. Monitora lo stato di apprendimento e le prestazioni del modello di intelligenza artificiale. [Ulteriori informazioni](ai-model-observability.md)
