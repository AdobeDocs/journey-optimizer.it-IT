---
product: experience platform
solution: Experience Platform
title: Introduzione ai modelli AI
description: Scopri i modelli di intelligenza artificiale che consentono di classificare le offerte
badge: label="Legacy" type="Informative"
feature: Ranking, Decision Management
role: User
level: Intermediate
exl-id: 4f7f7d1d-a12a-4ff6-b0ff-1a1c3d305a9d
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 15%

---

# Introduzione ai modelli AI {#ai-models}

[!DNL Journey Optimizer] consente di utilizzare un sistema di modelli addestrati che classifica le offerte da visualizzare per un determinato profilo.

Questa funzione ti consente di creare **modelli di IA** diversi in base agli obiettivi aziendali. Utilizzando queste diverse strategie basate su obiettivi in una decisione, il sistema di modelli addestrato ti aiuterà a capire in che modo i diversi modelli di intelligenza artificiale influiscono sui tuoi obiettivi.

Ad esempio, puoi selezionare un modello di IA per il canale e-mail e un altro per il canale push. Per ogni canale, il sistema di modelli addestrato sfrutterà più punti dati per determinare quale offerta deve essere presentata per prima per un determinato posizionamento, invece di tenere conto dei punteggi di priorità delle offerte o di una formula di classificazione [](create-ranking-formulas.md).

>[!IMPORTANT]
>
>Attualmente i modelli AI non sono supportati nei canali creati con Journey Optimizer.

➡️ [Scopri questa funzione nel video](#video)

## Tipi di modelli IA {#ai-model-types}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_ai_model_type"
>title="Scegli il tipo di modello"
>abstract="Seleziona il tipo di modello di IA da creare: **Ottimizzazione automatica** ottimizza le offerte in base alle prestazioni delle offerte passate, mentre **Ottimizzazione personalizzata** ottimizza e personalizza le offerte in base al pubblico e alle prestazioni delle offerte."
>additional-url="https://experienceleague.adobe.com/it/docs/journey-optimizer/using/decisioning/offer-decisioning/rankings/ai-models/create-ranking-strategies#create-ranking-strategy" text="Creare un modello IA"

In [!DNL Journey Optimizer] sono disponibili due tipi di modelli di IA:

* I **modelli di ottimizzazione automatica** hanno lo scopo di distribuire le offerte che massimizzano il ritorno (KPI) impostato dai client aziendali. Questi KPI potrebbero essere sotto forma di tassi di conversione, ricavi, ecc. A questo punto, l’ottimizzazione automatica si concentra sull’ottimizzazione dei clic dell’offerta con la conversione dell’offerta come obiettivo. L’ottimizzazione automatica non è personalizzata e viene ottimizzata in base alle prestazioni &quot;globali&quot; delle offerte. [Ulteriori informazioni](auto-optimization-model.md)

* I **modelli di ottimizzazione personalizzati** ti consentono di definire gli obiettivi aziendali e di utilizzare i dati dei clienti per addestrare modelli orientati al business in modo da distribuire offerte personalizzate e massimizzare i KPI. [Ulteriori informazioni](personalized-optimization-model.md)

## Creazione di un modello di IA {#create-ai-model}

I passaggi principali per creare e utilizzare modelli di intelligenza artificiale sono i seguenti:

1. Crea un set di dati in cui verranno raccolti gli eventi di conversione e di impression. [Ulteriori informazioni](../data-collection/create-dataset.md)

1. Crea un modello di intelligenza artificiale che sfrutta gli eventi del set di dati per classificare le offerte. [Ulteriori informazioni](create-ranking-strategies.md)

1. Configura lo schema di offerta per acquisire automaticamente gli eventi. [Ulteriori informazioni](../data-collection/schema-requirement.md)

   >[!IMPORTANT]
   >
   >Per poter essere raccolti, i modelli di IA richiedono l’invio di eventi di feedback come eventi di esperienza. [Ulteriori informazioni sulla raccolta dati di gestione delle decisioni](../data-collection/data-collection.md)

1. Assegna il modello di IA a un posizionamento in una decisione di classificazione delle offerte idonee. [Ulteriori informazioni](../offer-activities/configure-offer-selection.md)

## Video introduttivo {#video}

Scopri come creare un modello di intelligenza artificiale per Offer Decisioning e come applicarlo a una decisione.

>[!VIDEO](https://video.tv.adobe.com/v/3419959?quality=12)
