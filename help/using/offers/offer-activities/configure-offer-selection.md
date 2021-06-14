---
title: Configurare la selezione di offerte nelle decisioni
description: Scopri come gestire la selezione delle offerte nelle decisioni.
feature: Offerte
topic: Integrazioni
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 7%

---

# Configurare la selezione di offerte nelle decisioni {#offers-selection-in-activities}

## Informazioni sulla priorità delle offerte {#about-offers-priority}

Per impostazione predefinita, quando più offerte sono idonee per un determinato posizionamento in una decisione (precedentemente nota come attività di offerta), le offerte con la **priorità** più alta verranno consegnate prima ai clienti. I punteggi di priorità delle offerte vengono assegnati durante la creazione di un&#39;offerta (consulta [Creare un&#39;offerta personalizzata](../offer-library/creating-personalized-offers.md)).

![](../../assets/offer-priority.png)

Inoltre, Journey Optimizer consente di creare **formule di classificazione**. Si tratta di formule che determinano quale offerta deve essere presentata prima per un determinato posizionamento, anziché tenere conto dei punteggi di priorità delle offerte. Ad esempio, puoi aumentare la priorità di tutte le offerte in cui la data di fine è inferiore a 24 ore da ora, oppure incrementare le offerte dalla categoria &quot;in esecuzione&quot; se il punto di interesse del profilo è &quot;in esecuzione&quot;.

Per ulteriori informazioni su come creare una formula di classificazione, consulta [questa sezione](../offer-library/create-ranking-formulas.md).

## Assegnare una formula di classificazione a un posizionamento {#assign-ranking-formula}

Una volta creata una formula di classificazione, puoi assegnarla a un posizionamento in una decisione. Per farlo, segui la procedura indicata di seguito:

* Crea una decisione o modifica una decisione esistente, quindi crea i posizionamenti che conterranno le offerte (consulta [Creare decisioni](../offer-activities/create-offer-activities.md)).

* Per ogni posizionamento, seleziona **[!UICONTROL Ranking]** dall’elenco a discesa, quindi fai clic su **[!UICONTROL Add ranking]**.

   ![](../../assets/offer-activity-ranking.png)

* Seleziona la formula di classificazione desiderata, quindi fai clic su **[!UICONTROL Select]**.

   ![](../../assets/ranking-selection.png)

La formula di classificazione è ora associata al posizionamento. Se più offerte possono essere presentate in questo posizionamento, la decisione utilizzerà la formula della classificazione per calcolare quale offerta distribuire per prima.
