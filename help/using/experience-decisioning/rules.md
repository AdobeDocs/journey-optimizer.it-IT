---
title: Regole di decisione
description: Scopri come utilizzare le regole di decisione
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 033a11b8-c848-4e4a-b6f0-62fa0a2152bf
source-git-commit: c13cd73229b2fab80722663afae9fe24b660c0f9
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 31%

---

# Regole di decisione {#rules}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_rules"
>title="Creare regole di decisione"
>abstract="Le regole di decisione consentono di definire il pubblico per gli elementi decisionali applicando vincoli, direttamente a livello dell’elemento decisionale o all’interno di una strategia di selezione specifica. Ciò consente di controllare con precisione quali elementi devono essere presentati a chi."

>[!BEGINSHADEBOX &quot;Cosa troverai in questa guida alla documentazione&quot;]

* [Introduzione a Offer Decisioning](gs-experience-decisioning.md)
* Gestire gli elementi decisionali: [Configurare il catalogo articoli](catalogs.md) - [Creare elementi decisionali](items.md) - [Gestire le raccolte elementi](collections.md)
* Configura la selezione degli elementi: **[Creare regole di decisione](rules.md)** - [Creare metodi di classificazione](ranking.md)
* [Creare strategie di selezione](selection-strategies.md)
* [Creare criteri di decisione](create-decision.md)

>[!ENDSHADEBOX]

Le regole di decisione consentono di definire il pubblico per gli elementi decisionali applicando vincoli, direttamente a livello dell’elemento decisionale o all’interno di una strategia di selezione specifica. Ciò consente di controllare con precisione quali elementi devono essere presentati a chi.

Ad esempio, consideriamo uno scenario in cui si hanno elementi decisionali con prodotti relativi allo yoga progettati per le donne. Con le regole di decisione, puoi specificare che questi elementi devono essere visualizzati solo ai profili il cui genere è &quot;Femmina&quot; e che hanno indicato un &quot;Punto di interesse&quot; in &quot;Yoga&quot;.

>[!NOTE]
>
>Oltre alle regole di decisione a livello di articolo e di strategia di selezione, puoi anche definire il pubblico a cui rivolgerti a livello di campagna. [Ulteriori informazioni](../campaigns/create-campaign.md#audience)


L’elenco delle regole di decisione è accessibile nella sezione **[!UICONTROL Configurazione]** / **[!UICONTROL Regole delle decisioni]** menu.

<!--![](assets/decision-rules-list.png)-->

>[!IMPORTANT]
>
>Per il momento, le regole di decisione vengono gestite utilizzando Journey Optimizer **Gestione delle decisioni** menu. Di conseguenza, il **[!UICONTROL Regole di decisione]** L’elenco in Experience Decisioning include regole create da Journey Optimizer **[!UICONTROL Gestione delle decisioni]** o **[!UICONTROL Experience Decisioning]** menu.

Per creare una regola, effettua le seguenti operazioni:

1. Accedi a **[!UICONTROL Configurazione]** / **[!UICONTROL Regole di decisione]**.
1. L’interfaccia utente di Journey Optimizer per la gestione delle decisioni viene visualizzata nell’area centrale. Segui i passaggi descritti in [Documentazione sulla gestione delle decisioni](../offers/offer-library/creating-decision-rules.md) per creare la regola in base alle tue esigenze.

1. Una volta creata, la regola viene visualizzata nell’elenco ed è disponibile per l’utilizzo in elementi di decisione e strategie di selezione per gestire la presentazione degli elementi di decisione ai profili.
