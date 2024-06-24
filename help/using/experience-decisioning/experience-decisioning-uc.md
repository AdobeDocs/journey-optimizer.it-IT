---
title: Caso di utilizzo di Experience Decisioning
description: Scopri come creare decisioni utilizzando esperimenti con il canale basato su codice
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate, Experienced
badge: label="Disponibilità limitata"
source-git-commit: 59ecb9a5376e697061ddac4cc68f09dee68570c0
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 6%

---

# Caso di utilizzo di Experience Decisioning {#experience-decisioning-uc}

In questo caso d’uso, definisci due trattamenti di consegna ciascuno contenente un criterio di decisione diverso al fine di misurare quale offre le prestazioni migliori per il pubblico di destinazione.

## Creare elementi e strategie

Devi innanzitutto creare gli elementi, raggrupparli in raccolte, impostare regole e metodi di classificazione. Questi elementi ti consentiranno di creare strategie di selezione.

1. Accedi a **[!UICONTROL Experience Decisioning]** > **[!UICONTROL Cataloghi]** e creare diversi elementi dell’offerta. Imposta i vincoli utilizzando tipi di pubblico o regole per limitare ogni elemento solo a profili specifici. [Ulteriori informazioni](items.md)

   <!--
   1. From the items list, click the **[!UICONTROL Edit schema]** button  and edit the custom attributes if needed. [Learn how to work with catalogs](catalogs.md)-->

1. Crea **raccolte** per categorizzare e raggruppare gli elementi decisionali in base alle proprie preferenze. [Ulteriori informazioni](collections.md)

1. Crea **regole di decisione** per determinare a chi può essere visualizzato un elemento di decisione. [Ulteriori informazioni](rules.md)

1. Crea **metodi di classificazione** e applicarli nelle strategie di decisione per determinare l’ordine prioritario per la selezione degli elementi decisionali. [Ulteriori informazioni](ranking.md)

1. Genera **strategie di selezione** che sfruttano raccolte, regole di decisione e metodi di classificazione per identificare gli elementi di decisione adatti per la visualizzazione nei profili. [Ulteriori informazioni](selection-strategies.md)

## Creare criteri di decisione

Per presentare l’offerta e l’esperienza migliore e dinamica ai visitatori sul sito web o sull’app mobile, aggiungi un criterio decisionale a una campagna basata su codice.

Definisci due trattamenti di consegna ciascuno contenente un criterio di decisione diverso.

1. Crea una campagna e seleziona la **[!UICONTROL Esperienza basata su codice]** azione. [Ulteriori informazioni](../code-based/create-code-based.md)

1. Dalla pagina di riepilogo della campagna, fai clic su **[!UICONTROL Crea esperimento]** per iniziare a configurare l’esperimento sui contenuti. [Ulteriori informazioni](../content-management/content-experiment.md)

1. Seleziona la **[!UICONTROL Decisioni]** , fai clic su **[!UICONTROL Creare una decisione]** e compila i dettagli della decisione. [Ulteriori informazioni](create-decision.md)

   ![](assets/decision-code-based-create.png)

1. Definisci le strategie di selezione per la decisione. Clic **[!UICONTROL Aggiungi strategia]**.

1. Fai clic su **[!UICONTROL Crea]**. La nuova decisione è aggiunta alla voce **[!UICONTROL Decisioni]**.

   ![](assets/decision-code-based-decision-added.png)

1. Fai clic sull’icona altre azioni (tre punti) e seleziona **[!UICONTROL Aggiungi]**. Ora puoi aggiungere tutti gli attributi di decisione desiderati all’interno di questo.

   ![](assets/decision-code-based-add-decision.png)

1. Puoi anche aggiungere qualsiasi altro attributo disponibile nell’editor di personalizzazione, ad esempio gli attributi del profilo.

   ![](assets/decision-code-based-decision-profile-attribute.png)

1. Genera il trattamento B e ripeti i passaggi precedenti per creare un’altra decisione.

1. Salva il contenuto.


