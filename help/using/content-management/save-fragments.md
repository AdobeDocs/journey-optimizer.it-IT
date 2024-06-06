---
solution: Journey Optimizer
product: journey optimizer
title: Salva contenuto come frammento
description: Scopri come salvare i contenuti come frammenti per riutilizzarli nelle campagne e nei percorsi Journey Optimizer
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 70e88ea0-f2b0-4c13-8693-619741762429
source-git-commit: f47160f40abd9427cb9b9c793ee0ab402bf9f65b
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 2%

---

# Salva contenuto come frammento {#save-as-fragment}

Durante la modifica del contenuto in [!DNL Journey Optimizer], puoi salvare tutto o parte del contenuto come frammento per riutilizzarlo in futuro.

## Salva contenuto come frammento visivo {#save-as-visual-fragment}

Durante la progettazione di un [modello di contenuto](content-templates.md) o un [email](../email/get-started-email-design.md) in una campagna o in un percorso, puoi salvare una parte del contenuto come frammento visivo. Per farlo, segui la procedura indicata di seguito.

1. In [E-mail Designer](../email/get-started-email-design.md), fai clic sui puntini di sospensione in alto a destra dello schermo.

1. Seleziona **[!UICONTROL Salva come frammento]** dal menu a discesa.

   ![](assets/fragment-save-as.png)

1. Il **[!UICONTROL Salva come frammento]** schermo. Seleziona gli elementi da includere nel frammento, inclusi i campi di personalizzazione e il contenuto dinamico. Gli attributi contestuali non sono supportati nei frammenti.

   >[!CAUTION]
   >
   >Potete selezionare solo le sezioni adiacenti. Non puoi selezionare una struttura vuota o un altro frammento.

   ![](assets/fragment-save-as-screen.png)

1. Clic **[!UICONTROL Crea]**. Inserisci i dettagli del frammento, ovvero nome e descrizione (se necessario).

1. Per assegnare etichette di utilizzo dei dati personalizzate o di base al frammento, seleziona **[!UICONTROL Gestisci accesso]**. [Ulteriori informazioni su OLAC (Object Level Access Control)](../administration/object-based-access.md).

1. Seleziona o crea tag Adobe Experience Platform da **Tag** per categorizzare il modello e migliorare la ricerca. [Ulteriori informazioni](../start/search-filter-categorize.md#tags)

1. Clic **[!UICONTROL Crea]** di nuovo. Il frammento viene salvato in aggiunto al [elenco frammenti](#access-manage-fragments), accessibile dalla [!DNL Journey Optimizer] menu dedicato.

   Diventa un frammento autonomo che può essere [accesso eseguito](#access-manage-fragments), [modificato](#edit-fragments) e [archiviato](#archive-fragments) come qualsiasi altro elemento di tale elenco.

Ora puoi utilizzare questo frammento durante la creazione di qualsiasi [email](../email/get-started-email-design.md) o [modello di contenuto](content-templates.md) entro [!DNL Journey Optimizer]. [Scopri come](../email/use-visual-fragments.md)

>[!NOTE]
>
>Eventuali modifiche apportate al nuovo frammento non vengono propagate all’e-mail o al modello di origine. Allo stesso modo, quando il contenuto originale viene modificato all’interno dell’e-mail o del modello, il nuovo frammento non viene modificato.

## Salva contenuto come frammento di espressione {#save-as-expression-fragment}

>[!CONTEXTUALHELP]
>id="ajo_perso_library"
>title="Salva come frammento di espressione"
>abstract="Il [!DNL Journey Optimizer] l’editor di personalizzazione consente di salvare il contenuto come frammento di espressione. Queste espressioni sono quindi disponibili per creare contenuti personalizzati."

Il [!DNL Journey Optimizer] l’editor di personalizzazione consente di salvare il contenuto come frammento di espressione. Queste espressioni sono quindi disponibili per creare contenuti personalizzati.

Per salvare il contenuto come frammento di espressione, effettua le seguenti operazioni.

1. In [editor di personalizzazione](../personalization/personalization-build-expressions.md) , genera un&#39;espressione, quindi fai clic su **[!UICONTROL Salva come frammento]**.

1. Nel riquadro di destra, immettere un nome e una descrizione per l&#39;espressione in modo che gli utenti possano trovarla più facilmente.

   ![](assets/expression-fragment-save-as.png)

1. Clic **[!UICONTROL Salva frammento]**.

   <!--An expression fragment cannot be nested inside another fragment.-->

1. Il frammento di espressione viene aggiunto al [elenco frammenti](#access-manage-fragments). Ora puoi utilizzarlo per creare contenuti personalizzati.

>[!NOTE]
>
>Le espressioni non possono superare i 200 KB.
