---
title: Configurare la selezione di offerte nelle decisioni
description: Scopri come gestire la selezione delle offerte nelle decisioni
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 8c7135d7-bf5a-4671-afdf-afec60907a56
source-git-commit: 06a7abc2ada930356cbaf45ce01eed5e3156f2e3
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 9%

---

# Configurare la selezione di offerte nelle decisioni {#offers-selection-in-decisions}

Se più offerte sono idonee per un determinato posizionamento, puoi scegliere il metodo che sceglierà l’offerta migliore per ciascun profilo al momento della configurazione di una decisione (precedentemente nota come attività di offerta). Puoi classificare le offerte in base a:
* Priorità offerta
* Formula di classificazione
* [Classificazione dell’intelligenza artificiale](#use-ranking-strategy) (solo per utenti selezionati)

![](../../assets/offer-rank-by.png)

## Priorità offerta {#offer-priority}

Per impostazione predefinita, quando più offerte sono idonee per un determinato posizionamento in una decisione (precedentemente nota come attività di offerta), le offerte con il valore più alto **priorità** verranno consegnati prima ai clienti.

![](../../assets/offer-priority.png)

I punteggi di priorità delle offerte vengono assegnati durante la creazione di un’offerta. Scopri come creare un’offerta personalizzata in [questa sezione](../offer-library/creating-personalized-offers.md).

## Formula di classificazione {#assign-ranking-formula}

Oltre alla priorità delle offerte, Journey Optimizer consente di creare **classificazione delle formule**. Si tratta di formule che determinano quale offerta deve essere presentata prima per un determinato posizionamento, anziché tenere conto dei punteggi di priorità delle offerte.

Ad esempio, puoi aumentare la priorità di tutte le offerte in cui la data di fine è inferiore a 24 ore da ora, oppure incrementare le offerte dalla categoria &quot;in esecuzione&quot; se il punto di interesse del profilo è &quot;in esecuzione&quot;.

Scopri come creare una formula di classificazione in [questa sezione](../offer-library/create-ranking-formulas.md).

Una volta creata una formula di classificazione, puoi assegnarla a un posizionamento in una decisione (precedentemente nota come attività di offerta). Per farlo, segui la procedura indicata di seguito:

1. Crea una decisione o modifica una decisione esistente. Consulta [Creare decisioni](../offer-activities/create-offer-activities.md).

1. Aggiungi i posizionamenti che conterranno le offerte. Vedi [Creare posizionamenti](../offer-library/creating-placements.md).

1. Per ogni posizionamento, aggiungi una raccolta. Vedi [Creare raccolte](../offer-library/creating-collections.md).

1. Seleziona **[!UICONTROL Ranking formula]** come metodo di classificazione, quindi fare clic su **[!UICONTROL Add ranking]**.

   ![](../../assets/offer-activity-ranking.png)

1. Seleziona la formula di classificazione desiderata, quindi fai clic su **[!UICONTROL Select]**.

   ![](../../assets/ranking-selection.png)

La formula di classificazione è ora associata al posizionamento.

Se più offerte sono idonee per essere presentate in questo posizionamento, la decisione utilizzerà la formula della classificazione per calcolare quale offerta distribuire per prima.

## Classificazione basata su IA {#use-ranking-strategy}

<!--If you are an [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target="_blank"} user leveraging the **Offer Decisioning** application service,-->You can also use an trained model system that automatically ranks offers to display for a given profile by selecting a ranking strategy. Learn how to create a ranking strategy in [this section](../offer-library/create-ranking-strategies.md).

>[!CAUTION]
>
>L’utilizzo della classificazione basata su IA è attualmente disponibile in accesso anticipato solo per determinati utenti.

Una volta creata una strategia di classificazione, puoi assegnarla a un posizionamento in una decisione (precedentemente nota come attività di offerta). A questo scopo, segui i passaggi seguenti:

1. Crea una decisione o modifica una decisione esistente. Consulta [Creare decisioni](../offer-activities/create-offer-activities.md).

1. Aggiungi i posizionamenti che conterranno le offerte. Vedi [Creare posizionamenti](../offer-library/creating-placements.md).

1. Per ogni posizionamento, aggiungi una raccolta. Vedi [Creare raccolte](../offer-library/creating-collections.md).

1. Scegli di classificare le offerte per **[!UICONTROL AI ranking]** dall’elenco a discesa e fai clic su **[!UICONTROL Add ranking]**.

   ![](../../assets/ranking-selection-ai-ranking.png)

1. Seleziona la strategia di classificazione creata. Vengono visualizzati tutti i dettagli della strategia di classificazione.

   ![](../../assets/ranking-selection-ai-ranking-selected.png)

1. Fai clic su **[!UICONTROL Select]**. La strategia di classificazione è ora associata al posizionamento.

Se sono ammissibili più offerte, il sistema di modelli addestrati determinerà quale offerta presentare prima per un determinato posizionamento.

