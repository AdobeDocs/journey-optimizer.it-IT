---
title: Raccolte
description: Scopri come utilizzare le raccolte
feature: Offers
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
source-git-commit: 69a2ef17b6f5ccd40c08858f7b434029964d544d
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 6%

---

# Raccolte {#collections}

>[!BEGINSHADEBOX]

Cosa troverai in questa documentazione di guida:

* [Introduzione a Experience Decisioning](gs-experience-decisioning.md)
* Gestire gli elementi decisionali
   * [Configurare il catalogo articoli](catalogs.md)
   * [Creare elementi decisionali](items.md)
   * **[Gestire le raccolte elementi](collections.md)**
* Configurare la selezione degli elementi
   * [Creare regole di decisione](rules.md)
   * [Creare metodi di classificazione](ranking.md)
* [Creare strategie di selezione](selection-strategies.md)
* [Creare criteri di decisione](create-decision.md)

>[!ENDSHADEBOX]

Le raccolte ti consentono di categorizzare e raggruppare gli elementi decisionali in base alle tue preferenze. Queste categorie vengono create creando regole che sfruttano gli attributi degli elementi decisionali.

Ad esempio, supponiamo che tu abbia aggiunto un attributo personalizzato &quot;Categoria&quot; allo schema del catalogo degli elementi decisionali. Questo consente di creare una raccolta che include tutti gli elementi decisionali con il valore &quot;Yoga&quot; nell’attributo &quot;Category&quot;.

L’elenco delle raccolte è accessibile dalla sezione **[!UICONTROL Elementi]** menu.

Per creare una raccolta, effettua le seguenti operazioni:

1. Accedi a **[!UICONTROL Elementi]** > **[!UICONTROL Raccolte]** e fai clic su **[!UICONTROL Crea raccolta]**.
1. Fornisci un nome e una descrizione per la raccolta.
1. Aggiungi una o più regole per determinare gli elementi da includere nella raccolta. Per eseguire questa operazione:

   1. Scegliere un attributo articolo da utilizzare come criterio. L’elenco degli attributi include tutti gli attributi standard e personalizzati definiti nello schema del catalogo. [Ulteriori informazioni sul catalogo degli articoli](catalogs.md)
   1. Seleziona l’operatore desiderato e inserisci il valore su cui filtrare.
   1. Ripeti questi passaggi per aggiungere tutte le regole necessarie. Quando vengono aggiunte più regole, puoi scegliere tra **E** e **Oppure** per combinarli. A questo scopo, fai clic sul badge dell’operatore per passare da una scelta all’altra.

   ![](assets/collection-create.png)

1. Una volta definite le regole di raccolta, fai clic su **[!UICONTROL Crea]**. La raccolta viene ora visualizzata nell’elenco.
