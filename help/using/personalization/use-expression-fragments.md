---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare frammenti di espressione
description: Scopri come utilizzare i frammenti di espressione in [!DNL Journey Optimizer] editor di personalizzazione.
feature: Personalization, Fragments
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: espressione, editor, libreria, personalizzazione
exl-id: 74b1be18-4829-4c67-ae45-cf13278cda65
source-git-commit: ca743774017e8f6cf5f385119d9c71de6020bb19
workflow-type: tm+mt
source-wordcount: '750'
ht-degree: 0%

---

# Sfruttare i frammenti di espressione {#use-expression-fragments}

Quando si utilizza **editor di personalizzazione**, puoi sfruttare tutti i frammenti di espressione creati o salvati nella sandbox corrente.

Un frammento è un componente riutilizzabile a cui è possibile fare riferimento in [!DNL Journey Optimizer] campagne e percorsi. Questa funzionalità consente di precreare più blocchi di contenuto personalizzati che possono essere utilizzati dagli utenti di marketing per assemblare rapidamente i contenuti in un processo di progettazione migliorato. [Scopri come creare e gestire i frammenti](../content-management/fragments.md).

➡️ [Scopri come gestire, creare e utilizzare i frammenti in questo video](../content-management/fragments.md#video-fragments)

## Utilizzare un frammento di espressione {#use-expression-fragment}

Per aggiungere frammenti di espressione al contenuto, segui i passaggi seguenti.

>[!NOTE]
>
>Puoi aggiungere fino a 30 frammenti in una determinata consegna. I frammenti possono essere nidificati solo fino a un livello.

1. Apri [editor di personalizzazione](personalization-build-expressions.md) e seleziona la **[!UICONTROL Frammenti]** nel riquadro sinistro.

   Nell’elenco vengono visualizzati tutti i frammenti di espressione creati o salvati come frammenti nella sandbox corrente. Sono ordinati per data di creazione: i frammenti di espressione aggiunti di recente vengono visualizzati per primi nell’elenco. [Ulteriori informazioni](../content-management/fragments.md#create-expression-fragment)

   ![](assets/expression-fragments-pane.png)

   Puoi anche aggiornare questo elenco.

   >[!NOTE]
   >
   >Se alcuni frammenti sono stati modificati o aggiunti durante la modifica del contenuto, l’elenco verrà aggiornato con le modifiche più recenti.

1. Fai clic sull’icona + accanto a un frammento di espressione per inserire nell’editor l’ID frammento corrispondente.

   ![](assets/expression-fragment-add.png)

   >[!CAUTION]
   >
   >Puoi aggiungere qualsiasi **Bozza** o **Live** frammento nel contenuto. Tuttavia, non potrai attivare il percorso o la campagna se al suo interno viene utilizzato un frammento con lo stato Bozza. Durante la pubblicazione di un percorso o di una campagna, i frammenti bozza mostreranno un errore e dovrai approvarli per poterli pubblicare.
   >
   > Si prega di notare che gli stati dei frammenti vengono gradualmente implementati nel corso di diversi giorni dopo la versione di giugno di Journey Optimizer. Alcuni utenti avranno accesso immediato, altri potrebbero notare un ritardo prima che questo diventi disponibile nei loro ambienti. Se questo miglioramento non è ancora disponibile nel tuo ambiente, tieni presente che il frammento non deve essere **Live** da utilizzare nei percorsi e nelle campagne.

1. Una volta aggiunto l’ID frammento, se apri il frammento di espressione corrispondente e [modificarlo](../content-management/fragments.md#edit-fragments) dall’interfaccia di, le modifiche vengono sincronizzate. Vengono propagati automaticamente a tutte le bozze o ai percorsi/campagne live che contengono tale ID frammento.

1. Fai clic su **[!UICONTROL Altre azioni]** accanto a un frammento. Dal menu contestuale visualizzato, seleziona **[!UICONTROL Visualizza frammento]** per ottenere ulteriori informazioni su quel frammento. Il **[!UICONTROL ID frammento]** viene visualizzato anche e può essere copiato da qui.

   ![](assets/expression-fragment-view.png)

1. Puoi aprire il frammento di espressione in un’altra finestra per modificarne il contenuto e le proprietà, utilizzando **[!UICONTROL Apri frammento]** nel menu contestuale o dal menu **[!UICONTROL Informazioni frammento]** riquadro. [Scopri come modificare un frammento](../content-management/fragments.md#edit-fragments)

   ![](assets/expression-fragment-open.png)

1. Puoi quindi personalizzare e convalidare i contenuti come di consueto utilizzando tutte le funzionalità di personalizzazione e authoring del [editor di personalizzazione](personalization-build-expressions.md).

>[!NOTE]
>
>Se crei un frammento di espressione contenente più interruzioni di riga e lo utilizzi in [SMS](../sms/create-sms.md#sms-content) o [push](../push/design-push.md) contenuti, le interruzioni di riga vengono mantenute. In questo modo, assicurati di testare [SMS](../sms/send-sms.md) o [push](../push/send-push.md) messaggio prima di inviarlo.

## Personalizza campi modificabili {#customize-fields}

Se alcune parti di un frammento di espressione sono state rese modificabili utilizzando le variabili, è possibile sovrascrivere i relativi valori predefiniti utilizzando una sintassi specifica. [Scopri come rendere personalizzabili i frammenti](../content-management/customizable-fragments.md)

Per personalizzare i campi, effettua le seguenti operazioni:

1. Inserisci il frammento nel codice da **Frammenti** menu.

1. Utilizza il `<fieldId>="<value>"` codice alla fine della sintassi per sostituire il valore predefinito della variabile.

   Nell’esempio seguente, sostituiamo il valore di una variabile il cui ID è &quot;sports&quot; con il valore &quot;yoga&quot;. Questo visualizzerà lo &quot;yoga&quot; nel contenuto del frammento in tutti i casi in cui si fa riferimento alla variabile &quot;sport&quot;.

   ![](../content-management/assets/fragment-expression-use.png)

Un esempio che mostra come aggiungere campi modificabili in un frammento di espressione e sostituirne i valori durante la creazione di un messaggio e-mail è disponibile in [questa sezione](../content-management/customizable-fragments.md#example).

## Interrompi ereditarietà {#break-inheritance}

Quando si aggiunge un ID frammento all’editor di personalizzazione, le modifiche apportate al frammento di espressione originale vengono sincronizzate.

Tuttavia, puoi anche incollare il contenuto di un frammento di espressione nell’editor. Dal menu contestuale, seleziona **[!UICONTROL Incolla frammento]** per inserire tale contenuto.

![](assets/expression-fragment-paste.png)

In tal caso, l’ereditarietà dal frammento originale è interrotta. Il contenuto del frammento viene copiato nell’editor e le modifiche non vengono più sincronizzate.

Diventa un elemento autonomo non più collegato al frammento originale; puoi modificarlo come qualsiasi altro elemento nel codice.

