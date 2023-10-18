---
product: experience platform
solution: Experience Platform
title: Introduzione ai modelli AI
description: Scopri i modelli di intelligenza artificiale che consentono di classificare le offerte
feature: Ranking, Decision Management
role: User
level: Intermediate
exl-id: 4f7f7d1d-a12a-4ff6-b0ff-1a1c3d305a9d
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 4%

---

# Introduzione ai modelli AI {#ai-models}

[!DNL Journey Optimizer] consente di utilizzare un sistema di modelli addestrato che classifica le offerte da visualizzare per un determinato profilo.

Questa funzione consente di creare diversi **Modelli IA** in base agli obiettivi aziendali. Utilizzando queste diverse strategie basate su obiettivi in una decisione, il sistema di modelli addestrato ti aiuterà a capire in che modo i diversi modelli di intelligenza artificiale influiscono sui tuoi obiettivi.

Ad esempio, puoi selezionare un modello di IA per il canale e-mail e un altro per il canale push. Per ogni canale, il sistema di modelli addestrato sfrutta più punti di dati per determinare quale offerta deve essere presentata per prima per un determinato posizionamento, anziché tenere conto dei punteggi di priorità delle offerte o di un [formula di classificazione](create-ranking-formulas.md).

>[!IMPORTANT]
>
>Per il momento, i modelli di classificazione non sono supportati nei canali creati con Journey Optimizer.

## Tipi di modelli IA {#ai-model-types}

In sono disponibili due tipi di modelli di IA [!DNL Journey Optimizer]:

* **Modelli di ottimizzazione automatica** mira a distribuire offerte che massimizzano il ritorno (KPI, Key Performance Indicator) impostato dai clienti aziendali. Questi KPI potrebbero essere sotto forma di tassi di conversione, ricavi, ecc. A questo punto, l’ottimizzazione automatica si concentra sull’ottimizzazione dei clic dell’offerta con la conversione dell’offerta come obiettivo. L’ottimizzazione automatica non è personalizzata e viene ottimizzata in base alle prestazioni &quot;globali&quot; delle offerte. [Ulteriori informazioni](auto-optimization-model.md)

* **Modelli di ottimizzazione personalizzati** consente di definire gli obiettivi aziendali e utilizza i dati dei clienti per addestrare modelli orientati alle aziende a distribuire offerte personalizzate e massimizzare i KPI. [Ulteriori informazioni](personalized-optimization-model.md)

## Creazione di un modello di IA {#create-ai-model}

I passaggi principali per creare e utilizzare modelli di intelligenza artificiale sono i seguenti:

1. Crea un set di dati in cui verranno raccolti gli eventi di conversione e di impression. [Ulteriori informazioni](../data-collection/create-dataset.md)

1. Crea un modello di intelligenza artificiale che sfrutta gli eventi del set di dati per classificare le offerte. [Ulteriori informazioni](create-ranking-strategies.md)

1. Configura lo schema di offerta per acquisire automaticamente gli eventi. [Ulteriori informazioni](../data-collection/schema-requirement.md)

   >[!IMPORTANT]
   >
   >Per poter essere raccolti, i modelli di classificazione richiedono l’invio di eventi di feedback come eventi di esperienza. [Ulteriori informazioni sulla raccolta dati di gestione delle decisioni](../data-collection/data-collection.md)

1. Assegna il modello di IA a un posizionamento in una decisione di classificazione delle offerte idonee. [Ulteriori informazioni](../offer-activities/configure-offer-selection.md)
