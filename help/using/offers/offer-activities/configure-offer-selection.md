---
title: Configurare la selezione di offerte nelle decisioni
description: Scopri come gestire la selezione delle offerte nelle decisioni.
feature: Offerte
topic: Integrazioni
role: User
level: Intermediate
source-git-commit: 807157d4d6fc1dba018bbe796c8bd213504589dc
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 7%

---

# Configurare la selezione di offerte nelle decisioni {#offers-selection-in-activities}

Se più offerte sono idonee per un determinato posizionamento, puoi scegliere il metodo che sceglierà l’offerta migliore per ciascun profilo al momento della configurazione di una decisione (precedentemente nota come attività di offerta). Puoi classificare le offerte in base a:
* Priorità offerta
* Formula di classificazione

## Priorità offerta {#about-offers-priority}

Per impostazione predefinita, quando più offerte sono idonee per un determinato posizionamento in una decisione (precedentemente nota come attività di offerta), le offerte con la **priorità** più alta verranno consegnate prima ai clienti.

![](../../assets/offer-priority.png)

I punteggi di priorità delle offerte vengono assegnati durante la creazione di un’offerta. Scopri come creare un’offerta personalizzata in [questa sezione](../offer-library/creating-personalized-offers.md)).

## Formula di classificazione {#assign-ranking-formula}

Oltre alla priorità delle offerte, Journey Optimizer consente di creare **formule di classificazione**. Si tratta di formule che determinano quale offerta deve essere presentata prima per un determinato posizionamento, anziché tenere conto dei punteggi di priorità delle offerte.

Ad esempio, puoi aumentare la priorità di tutte le offerte in cui la data di fine è inferiore a 24 ore da ora, oppure incrementare le offerte dalla categoria &quot;in esecuzione&quot; se il punto di interesse del profilo è &quot;in esecuzione&quot;.

Scopri come creare una formula di classificazione in [questa sezione](../offer-library/create-ranking-formulas.md).

Una volta creata una formula di classificazione, puoi assegnarla a un posizionamento in una decisione (precedentemente nota come attività di offerta). Per farlo, segui la procedura indicata di seguito:

1. Crea una decisione o modifica una decisione esistente. Consulta [Creare decisioni](../offer-activities/create-offer-activities.md).

1. Aggiungi i posizionamenti che conterranno le offerte. Consulta [Creare posizionamenti](../offer-library/creating-placements.md).

1. Per ogni posizionamento, aggiungi una raccolta. Consulta [Creare raccolte](../offer-library/creating-collections.md).

1. Scegli di classificare le offerte per **[!UICONTROL Ranking]** dall’elenco a discesa, quindi fai clic su **[!UICONTROL Add ranking]**.

   ![](../../assets/offer-activity-ranking.png)

1. Seleziona la formula di classificazione desiderata, quindi fai clic su **[!UICONTROL Select]**.

   ![](../../assets/ranking-selection.png)

La formula di classificazione è ora associata al posizionamento.

Se più offerte sono idonee per essere presentate in questo posizionamento, la decisione utilizzerà la formula della classificazione per calcolare quale offerta distribuire per prima.
