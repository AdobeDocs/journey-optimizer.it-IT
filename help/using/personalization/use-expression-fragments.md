---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare frammenti di espressione
description: Scopri come utilizzare i frammenti di espressione in [!DNL Journey Optimizer] Editor espressioni.
feature: Personalization, Fragments
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: espressione, editor, libreria, personalizzazione
exl-id: 74b1be18-4829-4c67-ae45-cf13278cda65
source-git-commit: 08f3fc1837a4daa1ecaa7afcd53c80381177efb0
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 1%

---

# Sfrutta i frammenti di espressione {#use-expression-fragments}

Quando si utilizza **Editor espressioni**, puoi sfruttare tutti i frammenti di espressione creati o salvati nella sandbox corrente.

Scopri come creare e gestire i frammenti in [questa sezione](../content-management/fragments.md).

➡️ [Scopri come gestire, creare e utilizzare i frammenti in questo video](../content-management/fragments.md#video-fragments)

## Utilizzare un frammento di espressione {#use-expression-fragment}

Per aggiungere frammenti di espressione al contenuto, segui i passaggi seguenti.

1. Apri [Editor espressioni](personalization-build-expressions.md) e seleziona la **[!UICONTROL Frammenti]** nel riquadro sinistro.

   ![](assets/expression-fragments-pane.png)

   Nell’elenco vengono visualizzati tutti i frammenti di espressione creati o salvati come frammenti nella sandbox corrente. [Ulteriori informazioni](../content-management/fragments.md#create-expression-fragment)

   >[!NOTE]
   >
   >I frammenti sono ordinati per data di creazione: i frammenti di espressione aggiunti di recente vengono visualizzati per primi nell’elenco.

1. Puoi anche aggiornare l’elenco.

   >[!NOTE]
   >
   >Se alcuni frammenti sono stati modificati o aggiunti durante la modifica del contenuto, l’elenco verrà aggiornato con le modifiche più recenti.

1. Fai clic sull’icona + accanto a un frammento di espressione per inserire nell’editor l’ID frammento corrispondente.

   ![](assets/expression-fragment-add.png)

   Una volta aggiunto l’ID frammento, se apri il frammento di espressione corrispondente e [modificarlo](../content-management/fragments.md#edit-fragments) dall’interfaccia di, le modifiche vengono sincronizzate. Vengono propagati automaticamente a tutti **[!UICONTROL Bozza]** percorsi/campagne contenenti tale ID frammento.

   >[!NOTE]
   >
   >Le modifiche non vengono propagate al contenuto utilizzato in **[!UICONTROL Live]** percorsi o campagne.

1. Fai clic su **[!UICONTROL Altre azioni]** accanto a un frammento.

1. Dal menu contestuale visualizzato, seleziona **[!UICONTROL Visualizza frammento]** per ottenere ulteriori informazioni su quel frammento. Il **[!UICONTROL ID frammento]** viene visualizzato anche e può essere copiato da qui.

   ![](assets/expression-fragment-view.png)

1. Puoi aprire il frammento di espressione in un’altra finestra per modificarne il contenuto e le proprietà, utilizzando **[!UICONTROL Apri frammento]** nel menu contestuale o dal menu **[!UICONTROL Informazioni frammento]** riquadro. [Scopri come modificare un frammento](../content-management/fragments.md#edit-fragments)

   ![](assets/expression-fragment-open.png)

1. Puoi quindi personalizzare e convalidare i contenuti come di consueto utilizzando tutte le funzionalità di personalizzazione e authoring del [Editor espressioni](personalization-build-expressions.md).

>[!NOTE]
>
>Se crei un frammento di espressione contenente più interruzioni di riga e lo utilizzi in [SMS](../sms/create-sms.md#sms-content) o [push](../push/design-push.md) contenuti, le interruzioni di riga vengono mantenute. In questo modo, assicurati di testare [SMS](../sms/send-sms.md) o [push](../push/send-push.md) messaggio prima di inviarlo.

## Interrompi ereditarietà {#break-inheritance}

Quando si aggiunge un ID frammento all’editor espressioni, le modifiche apportate al frammento di espressione originale vengono sincronizzate.

Tuttavia, puoi anche incollare il contenuto di un frammento di espressione nell’editor. Dal menu contestuale, seleziona **[!UICONTROL Incolla frammento]** per inserire tale contenuto.

![](assets/expression-fragment-paste.png)

In tal caso, l’ereditarietà dal frammento originale è interrotta. Il contenuto del frammento viene copiato nell’editor e le modifiche non vengono più sincronizzate.

Diventa un elemento autonomo non più collegato al frammento originale; puoi modificarlo come qualsiasi altro elemento nel codice.

