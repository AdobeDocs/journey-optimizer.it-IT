---
title: Raccolte
description: Scopri come utilizzare le raccolte
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 099d1439-34f7-47fe-9181-0e9ce2032a01
source-git-commit: 2b9261ff0f225a429b9be04db214452736163766
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 50%

---

# Raccolte {#collections}

>[!CONTEXTUALHELP]
>id="ajo_exd_item_collections"
>title="Creare le raccolte"
>abstract="Le raccolte consentono di categorizzare e raggruppare gli elementi decisionali in base alle preferenze. Queste categorie vengono create creando regole che sfruttano gli attributi degli elementi decisionali."

>[!CONTEXTUALHELP]
>id="ajo_exd_item_collection_rules"
>title="Definire le regole per la raccolta"
>abstract="Aggiungi una o più regole per determinare gli elementi da includere nella raccolta. Scegliere un attributo dell’elemento da utilizzare come criterio. Selezionare l’operatore desiderato e inserisci il valore su cui filtrare. Aggiungere il maggior numero di regole necessario."

>[!CONTEXTUALHELP]
>id="ajo_exd_strategy_collection"
>title="Scegli una raccolta"
>abstract="Selezionare la raccolta contenente le offerte da considerare. Questo passaggio è obbligatorio durante la creazione di una strategia di selezione. Le raccolte consentono di categorizzare e raggruppare gli elementi decisionali in base alle preferenze. Ad esempio, puoi creare una raccolta che includa tutti gli elementi decisionali con il valore “Yoga” nell’attributo personalizzato “Categoria”."

>[!BEGINSHADEBOX &quot;Cosa troverai in questa guida alla documentazione&quot;]

* [Introduzione a Experience Decisioning](gs-experience-decisioning.md)
* Gestire gli elementi decisionali: [Configurare il catalogo articoli](catalogs.md) - [Creare elementi decisionali](items.md) - **[Gestire le raccolte elementi](collections.md)**
* Configura la selezione degli elementi: [Creare regole di decisione](rules.md) - [Creare metodi di classificazione](ranking.md)
* [Creare strategie di selezione](selection-strategies.md)
* [Creare criteri di decisione](create-decision.md)

>[!ENDSHADEBOX]

Le raccolte consentono di categorizzare e raggruppare gli elementi decisionali in base alle preferenze. Queste categorie vengono create creando regole che sfruttano gli attributi degli elementi decisionali.

Ad esempio, supponiamo che tu abbia aggiunto un attributo personalizzato &quot;Categoria&quot; allo schema del catalogo degli elementi decisionali. Questo consente di creare una raccolta che include tutti gli elementi decisionali con il valore &quot;Yoga&quot; nell’attributo &quot;Category&quot;.

L’elenco delle raccolte è accessibile dalla sezione **[!UICONTROL Cataloghi]** menu.

Per creare una raccolta, effettua le seguenti operazioni:

1. Accedi a **[!UICONTROL Cataloghi]** > **[!UICONTROL Raccolte]** e fai clic su **[!UICONTROL Crea raccolta]**.
1. Fornisci un nome e una descrizione per la raccolta.
1. Aggiungi una o più regole per determinare gli elementi da includere nella raccolta. Per eseguire questa operazione:

   1. Scegliere un attributo dell’elemento da utilizzare come criterio. L’elenco degli attributi include tutti gli attributi standard e personalizzati definiti nello schema del catalogo. [Ulteriori informazioni sul catalogo degli articoli](catalogs.md)
   1. Seleziona l’operatore desiderato e inserisci il valore su cui filtrare.
   1. Ripeti questi passaggi per aggiungere tutte le regole necessarie. Quando vengono aggiunte più regole, puoi scegliere tra **E** e **Oppure** per combinarli. A questo scopo, fai clic sul badge dell’operatore per passare da una scelta all’altra.

   ![](assets/collection-create.png)

1. Una volta definite le regole di raccolta, fai clic su **[!UICONTROL Crea]**. La raccolta viene ora visualizzata nell’elenco.
