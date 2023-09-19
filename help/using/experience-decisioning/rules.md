---
title: Regole di decisione
description: Scopri come utilizzare le regole di decisione
feature: Offers
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
source-git-commit: 69a2ef17b6f5ccd40c08858f7b434029964d544d
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 5%

---

# Regole di decisione {#rules}

>[!BEGINSHADEBOX]

Cosa troverai in questa documentazione di guida:

* [Introduzione a Experience Decisioning](gs-experience-decisioning.md)
* Gestire gli elementi decisionali
   * [Configurare il catalogo articoli](catalogs.md)
   * [Creare elementi decisionali](items.md)
   * [Gestire le raccolte elementi](collections.md)
* Configurare la selezione degli elementi
   * **[Creare regole di decisione](rules.md)**
   * [Creare metodi di classificazione](ranking.md)
* [Creare strategie di selezione](selection-strategies.md)
* [Creare criteri di decisione](create-decision.md)

>[!ENDSHADEBOX]

Le regole di decisione ti consentono di definire il pubblico per gli elementi di decisione applicando vincoli, direttamente a livello di elemento di decisione o all’interno di una strategia di selezione specifica. Ciò consente di controllare con precisione quali elementi devono essere presentati a chi.

Ad esempio, consideriamo uno scenario in cui si hanno elementi decisionali con prodotti relativi allo yoga progettati per le donne. Con le regole di decisione, puoi specificare che questi elementi devono essere visualizzati solo ai profili il cui genere è &quot;Femmina&quot; e che hanno indicato un &quot;Punto di interesse&quot; in &quot;Yoga&quot;.

L’elenco delle regole di decisione è accessibile nella sezione **[!UICONTROL Configurazione]** / **[!UICONTROL Regole delle decisioni]** menu.

<!--![](assets/decision-rules-list.png)-->

>[!IMPORTANT]
>
>Per il momento, le regole di decisione vengono gestite utilizzando Journey Optimizer **Gestione delle decisioni** menu. Di conseguenza, il **[!UICONTROL Regole di decisione]** L’elenco in Experience Decisioning include regole create da Journey Optimizer **[!UICONTROL Gestione delle decisioni]** o **[!UICONTROL Experience Decisioning]** menu.

Per creare una raccolta, effettua le seguenti operazioni:

1. Accedi a **[!UICONTROL Configurazione]** / **[!UICONTROL Regole di decisione]**.
1. L’interfaccia utente di Journey Optimizer per la gestione delle decisioni viene visualizzata nell’area centrale. Segui i passaggi descritti in [Documentazione sulla gestione delle decisioni](../offers/offer-library/creating-decision-rules.md) per creare la regola in base alle tue esigenze.

1. Una volta creata, la regola viene visualizzata nell’elenco ed è disponibile per l’utilizzo in elementi di decisione e strategie di selezione per gestire la presentazione degli elementi di decisione ai profili.
