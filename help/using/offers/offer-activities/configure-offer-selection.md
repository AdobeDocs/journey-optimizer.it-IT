---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Configurare la selezione di offerte nelle decisioni
description: Scopri come gestire la selezione delle offerte in decisioni
badge: label="Legacy" type="Informative"
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: 8c7135d7-bf5a-4671-afdf-afec60907a56
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 10%

---

# Configurare la selezione di offerte nelle decisioni {#offers-selection-in-decisions}

>[!TIP]
>
>La funzione Decisioni, la nuova funzionalità decisionale di [!DNL Adobe Journey Optimizer], è ora disponibile tramite i canali e-mail e di esperienza basati su codice. [Ulteriori informazioni](../../experience-decisioning/gs-experience-decisioning.md)

Se diverse offerte sono idonee per un determinato posizionamento, puoi scegliere il metodo che selezionerà l’offerta migliore per ciascun profilo al momento di configurare una decisione. Puoi classificare le offerte in base a:

* Priorità offerte
* Formula di classificazione
* [Classificazione basata su IA](#use-ranking-strategy)

![](../assets/offer-rank-by.png)

## Priorità offerte {#offer-priority}

Per impostazione predefinita, quando diverse offerte sono idonee per un determinato posizionamento in una decisione, le offerte con la **priorità** più elevata verranno consegnate prima ai clienti.

![](../assets/offer-priority.png)

I punteggi di priorità delle offerte vengono assegnati al momento della creazione di un’offerta. Scopri come creare un&#39;offerta personalizzata in [questa sezione](../offer-library/creating-personalized-offers.md).

## Formula di classificazione {#assign-ranking-formula}

Oltre alla priorità dell&#39;offerta, Journey Optimizer consente di creare **formule di classificazione**. Si tratta di formule che determinano quale offerta deve essere presentata per prima per un determinato posizionamento, anziché tenere conto dei punteggi di priorità delle offerte.

Ad esempio, puoi aumentare la priorità di tutte le offerte la cui data di fine è inferiore a 24 ore da ora, oppure puoi aumentare le offerte dalla categoria &quot;in esecuzione&quot; se il punto di interesse del profilo è &quot;in esecuzione&quot;.

Scopri come creare una formula di classificazione in [questa sezione](../ranking/create-ranking-formulas.md).

Una volta creata una formula, puoi assegnarla a un posizionamento in una decisione. Per farlo, segui la procedura indicata di seguito:

1. Crea una decisione o modificane una esistente. Consulta [Creare decisioni](../offer-activities/create-offer-activities.md).

1. Aggiungi i posizionamenti che conterranno le offerte. Consulta [Creare posizionamenti](../offer-library/creating-placements.md).

1. Per ogni posizionamento, aggiungi una raccolta. Consulta [Creare raccolte](../offer-library/creating-collections.md).

1. Seleziona **[!UICONTROL Formula]** come metodo di classificazione, quindi fai clic su **[!UICONTROL Aggiungi classificazione]**.

   ![](../assets/offer-activity-ranking.png)

1. Seleziona la formula desiderata, quindi fai clic su **[!UICONTROL Seleziona]**.

   ![](../assets/ranking-selection.png)

La formula di classificazione è ora associata al posizionamento.

Se più offerte sono idonee per essere presentate in questo posizionamento, la decisione utilizzerà la formula selezionata per calcolare quale offerta consegnare per prima.

## Classificazione basata su IA {#use-ranking-strategy}

<!--If you are an [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target="_blank"} user leveraging the **Offer Decisioning** application service,-->

Puoi anche utilizzare un sistema di modelli addestrato che classifica automaticamente le offerte da visualizzare per un determinato profilo selezionando un modello di intelligenza artificiale. Scopri come creare un modello di IA in [questa sezione](../ranking/create-ranking-strategies.md).

Una volta creato un modello di IA, puoi assegnarlo a un posizionamento in una decisione. A questo scopo, segui la procedura indicata di seguito:

1. Crea una decisione o modificane una esistente. Consulta [Creare decisioni](../offer-activities/create-offer-activities.md).

1. Aggiungi i posizionamenti che conterranno le offerte. Consulta [Creare posizionamenti](../offer-library/creating-placements.md).

1. Per ogni posizionamento, aggiungi una raccolta. Consulta [Creare raccolte](../offer-library/creating-collections.md).

1. Scegli di classificare le offerte in base alla **[!UICONTROL classificazione IA]** dall&#39;elenco a discesa, quindi fai clic su **[!UICONTROL Aggiungi classificazione]**.

   ![](../assets/ranking-selection-ai-ranking.png)

1. Seleziona il modello di IA creato. Vengono visualizzati tutti i dettagli del modello.

   ![](../assets/ranking-selection-ai-ranking-selected.png)

1. Fai clic su **[!UICONTROL Seleziona]**. Il modello di intelligenza artificiale è ora associato al posizionamento.

Se sono idonee più offerte, il sistema di modelli addestrato determinerà quale offerta deve essere presentata per prima per un determinato posizionamento.

