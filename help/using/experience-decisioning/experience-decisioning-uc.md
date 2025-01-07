---
title: Caso d’uso della funzione Decisioni
description: Scopri come creare decisioni utilizzando esperimenti con il canale basato su codice
feature: Decisioning
topic: Integrations
role: User
level: Intermediate, Experienced
hide: true
hidefromtoc: true
exl-id: 09770df2-c514-4217-a71b-e31c248df543
source-git-commit: 83ad828a4d342bba10284cdd20d22eb325e3e1f7
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 8%

---

# Caso d’uso della funzione Decisioni {#experience-decisioning-uc}

Questo caso d&#39;uso presenta tutti i passaggi necessari per utilizzare Decisioning con il canale basato su codice [!DNL Journey Optimizer].

<!--In this use case, you create a campaign where you define two delivery treatments - each containing a different decision policy in order to measure which one performs best for your target audience.-->

In questo caso d’uso, non sei sicuro se una formula di classificazione specifica funzionerà meglio delle priorità di offerta preassegnate.

Per misurare quale funziona meglio per il pubblico di destinazione, crea una campagna in cui definisci due trattamenti di consegna:

<!--Set up the experiment such that:-->

* Il primo trattamento contiene una strategia di selezione con priorità come metodo di classificazione.
* Il secondo trattamento contiene una diversa strategia di selezione per la quale una formula è il metodo di classificazione.

## Creare strategie di selezione

Innanzitutto, devi creare due strategie di selezione: una con priorità come metodo di classificazione e un’altra con una formula come metodo di classificazione.

### Creare la prima strategia di selezione

Nella prima strategia di selezione, seleziona priorità come metodo di classificazione. Segui i passaggi seguenti.

1. Crea un elemento di decisione. [Scopri come](items.md)

1. Imposta la **[!UICONTROL Priorità]** dell&#39;elemento di decisione rispetto ad altri. Se un profilo è idoneo per più elementi, una priorità più alta concede la precedenza degli elementi rispetto agli altri.

   ![](assets/exd-uc-item-priority.png)

   >[!NOTE]
   >
   >La priorità è un tipo di dati intero. Tutti gli attributi che sono tipi di dati integer devono contenere valori interi (senza decimali).

1. Definisci tipi di pubblico o regole per limitare l’elemento solo a profili specifici. [Scopri come impostare l&#39;idoneità dell&#39;elemento di decisione](items.md#eligibility)

1. Imposta le regole di limite per definire il numero massimo di volte in cui un’offerta può essere presentata. [Scopri come](items.md#capping)

<!--1. If needed, repeat the steps above to create one or more additional decision items.-->

1. Crea una **raccolta** in cui verranno inclusi gli elementi decisionali. [Ulteriori informazioni](collections.md)

1. Crea una **strategia di selezione**. [Scopri come](selection-strategies.md#create-selection-strategy)

1. Seleziona la [raccolta](collections.md) che contiene le offerte da considerare.

1. [Scegli il metodo di classificazione](#select-ranking-method) da utilizzare per selezionare l&#39;offerta migliore per ciascun profilo. In questo caso, selezionare **[!UICONTROL Priorità offerta]**. [Ulteriori informazioni](selection-strategies.md#offer-priority)

   ![](assets/exd-uc-strategy-priority.png)

   <!--If multiple offers are eligible for this strategy, the [Offer priority](#offer-priority) method uses the value defined in the offers.-->

### Creare la seconda strategia di selezione

Nella seconda strategia di selezione, selezionare una formula come metodo di classificazione. Segui i passaggi seguenti.

1. Crea un elemento di decisione. [Scopri come](items.md)

<!--1. Set the same **[!UICONTROL Priority]** as for the first decision item. TBC?-->

1. Definisci tipi di pubblico o regole per limitare l’elemento solo a profili specifici. [Scopri come impostare l&#39;idoneità dell&#39;elemento di decisione](items.md#eligibility)

1. Imposta le regole di limite per definire il numero massimo di volte in cui un’offerta può essere presentata. [Scopri come](items.md#capping)

<!--1. If needed, repeat the steps above to create one or more additional decision items.-->

1. Crea una **raccolta** in cui verranno inclusi gli elementi decisionali. [Ulteriori informazioni](collections.md)

1. Crea una **strategia di selezione**. [Scopri come](selection-strategies.md#create-selection-strategy)

1. Seleziona la [raccolta](collections.md) che contiene le offerte da considerare.

1. [Selezionare il metodo di classificazione](#select-ranking-method) da utilizzare per selezionare l&#39;offerta migliore per ogni profilo. In questo caso, selezionare **[!UICONTROL Formula]** per utilizzare un punteggio calcolato specifico per scegliere l&#39;offerta idonea da consegnare. [Ulteriori informazioni](selection-strategies.md#ranking-formula)

   ![](assets/exd-uc-strategy-formula.png)

<!--
## Create decision items and selection strategies

You first need to create items, group them together in collections, set up rules and ranking methods. These elements will allow you to build selection strategies.

1. Navigate to **[!UICONTROL Decisioning]** > **[!UICONTROL Catalogs]** and create several decision items. Set constraints using audiences or rules to restrict each item to specific profiles only. [Learn more](items.md)

1. From the items list, click the **[!UICONTROL Edit schema]** button  and edit the custom attributes if needed. [Learn how to work with catalogs](catalogs.md)

1. Create **collections** to categorize and group your decision items according to your preferences. [Learn more](collections.md)

1. Create **decision rules** to determine to whom a decision item can be shown. [Learn more](rules.md)

1. Create **ranking methods** and apply them within decision strategies to determine the priority order for selecting decision items. [Learn more](ranking.md)

1. Build **selection strategies** that leverage collections, decision rules, and ranking methods to identify the decision items suitable for displaying to profiles. [Learn more](selection-strategies.md)
-->

## Creare criteri di decisione

<!--To present the best dynamic offer and experience to your visitors on your website or mobile app, add a decision policy to a code-based campaign.

Define two delivery treatments each containing a different decision policy.-->

1. Crea una campagna e seleziona l&#39;azione **[!UICONTROL Esperienza basata su codice]**. [Ulteriori informazioni](../code-based/create-code-based.md)

1. Dalla finestra **[!UICONTROL Modifica contenuto]**, inizia a personalizzare il trattamento A.

1. Seleziona l&#39;icona **[!UICONTROL Decisioni]**, fai clic su **[!UICONTROL Crea una decisione]** e compila i dettagli della decisione. [Ulteriori informazioni](create-decision.md)

   ![](assets/decision-code-based-create.png)

1. Selezionare la prima strategia creata. Fare clic su **[!UICONTROL Aggiungi strategia]**.

1. Fai clic su **[!UICONTROL Crea]**. La nuova decisione viene aggiunta in **[!UICONTROL Decisioni]**.

   ![](assets/decision-code-based-decision-added.png)

1. Fai clic sull&#39;icona altre azioni (tre punti) e seleziona **[!UICONTROL Aggiungi]**. Ora puoi aggiungere tutti gli attributi di decisione desiderati all’interno di questo.

   ![](assets/decision-code-based-add-decision.png)

1. Puoi anche aggiungere qualsiasi altro attributo disponibile nell’editor di personalizzazione, ad esempio gli attributi del profilo.

   ![](assets/decision-code-based-decision-profile-attribute.png)

1. Dalla pagina di riepilogo della campagna, fai clic su **[!UICONTROL Crea esperimento]** per iniziare a configurare l&#39;esperimento sui contenuti. [Ulteriori informazioni](../content-management/content-experiment.md)

1. Dalla finestra **[!UICONTROL Modifica contenuto]**, seleziona il trattamento B e ripeti i passaggi precedenti per creare un&#39;altra decisione.

1. Selezionare la seconda strategia creata. Fare clic su **[!UICONTROL Aggiungi strategia]**.

1. Salva il contenuto.
