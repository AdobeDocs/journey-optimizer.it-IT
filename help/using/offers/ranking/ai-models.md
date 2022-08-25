---
product: experience platform
solution: Experience Platform
title: Guida introduttiva ai modelli AI
description: Scopri i modelli AI che consentono di classificare le offerte
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 4f7f7d1d-a12a-4ff6-b0ff-1a1c3d305a9d
source-git-commit: 12bc2373ac5c391764df3880c5c87666a19e99b2
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Guida introduttiva ai modelli AI {#ai-models}

[!DNL Journey Optimizer] consente di utilizzare un sistema di modelli addestrati che classifica le offerte da visualizzare per un determinato profilo.

Questa funzione consente di creare **Modelli AI** in base agli obiettivi aziendali. Utilizzando queste diverse strategie basate su obiettivi in una decisione, il sistema di modelli addestrati ti aiuterà a comprendere in che modo i diversi modelli AI influenzano i tuoi obiettivi.

Ad esempio, puoi selezionare un modello AI per il canale e-mail e un altro per il canale push. Per ogni canale, il sistema di modelli addestrati sfrutterà più punti di dati per determinare quale offerta deve essere presentata prima per un determinato posizionamento, invece di tenere conto dei punteggi di priorità delle offerte o di un [formula di classificazione](create-ranking-formulas.md).

## Tipi di modelli basati su IA {#ai-model-types}

Sono disponibili due tipi di modelli AI in [!DNL Journey Optimizer]:

* **Modelli di ottimizzazione automatica** cerca di offrire che massimizzino i rendimenti (KPI) impostati dai clienti aziendali. Questi KPI possono essere sotto forma di tassi di conversione, ricavi, ecc. A questo punto, l’ottimizzazione automatica si concentra sull’ottimizzazione dei clic delle offerte con la conversione delle offerte come target. L’ottimizzazione automatica non è personalizzata e si ottimizza in base alle prestazioni &quot;globali&quot; delle offerte. [Ulteriori informazioni](auto-optimization-model.md)

* **Modelli di personalizzazione** consente di definire obiettivi aziendali e utilizza i dati dei clienti per addestrare modelli orientati alle aziende in modo da offrire offerte personalizzate e massimizzare i KPI. [Ulteriori informazioni](personalized-optimization-model.md)

   >[!CAUTION]
   >
   >L’utilizzo di modelli di ottimizzazione personalizzata è attualmente disponibile in fase di accesso anticipato solo per determinati utenti.

## Creazione di un modello AI {#create-ai-model}

I passaggi principali per creare e utilizzare i modelli AI sono i seguenti:

1. Crea un set di dati in cui verranno raccolti gli eventi di conversione e impression. [Ulteriori informazioni](create-dataset.md)
1. Crea un modello AI che sfrutti gli eventi dal set di dati per classificare le offerte. [Ulteriori informazioni](create-ranking-strategies.md)
1. Configura lo schema dell’offerta per acquisire automaticamente gli eventi. [Ulteriori informazioni](schema-requirement.md)
1. Assegna il modello AI a un posizionamento in una decisione per classificare le offerte idonee. [Ulteriori informazioni](../offer-activities/configure-offer-selection.md)
