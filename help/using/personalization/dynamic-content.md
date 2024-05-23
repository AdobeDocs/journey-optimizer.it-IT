---
solution: Journey Optimizer
product: journey optimizer
title: Creare contenuti dinamici
description: Scopri come aggiungere dinamico ai messaggi.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: espressione, editor, dynamic, content
exl-id: 639ad7df-0d0f-4c9b-95d1-f3101267aae2
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '564'
ht-degree: 1%

---

# Creare contenuti dinamici {#dynamic-content}

Adobe Journey Optimizer consente di sfruttare le regole condizionali create nella libreria per aggiungere contenuto dinamico ai messaggi.

Il contenuto dinamico può essere creato in qualsiasi campo in cui puoi aggiungere la personalizzazione utilizzando l’editor di personalizzazione. Ciò include l’oggetto, i collegamenti, il contenuto delle notifiche push o le rappresentazioni delle offerte di tipo testo. [Ulteriori informazioni sui contesti di personalizzazione](personalization-contexts.md)

Inoltre, è possibile utilizzare le regole condizionali in E-mail Designer per creare più varianti di un componente di contenuto.

## Aggiungere contenuto dinamico alle espressioni {#perso-expressions}

I passaggi per aggiungere contenuto dinamico nelle espressioni sono i seguenti:

1. Passa al campo in cui desideri aggiungere contenuto dinamico, quindi apri l’editor di personalizzazione.

1. Seleziona la **[!UICONTROL Condizioni]** per visualizzare l’elenco delle regole condizionali disponibili. Fai clic sul pulsante + accanto a una regola per aggiungerla all’espressione corrente.

   Puoi anche creare una nuova regola selezionando **[!UICONTROL Crea nuovo]**. [Scopri come creare le condizioni](create-conditions.md)

   ![](assets/conditions-expression.png)

1. Aggiungi tra `{%if}` e `{%/if}` assegna i tag al contenuto da visualizzare se la regola condizionale è soddisfatta. Puoi aggiungere tutte le regole necessarie per creare diverse varianti di un’espressione.

   Nell’esempio seguente, sono state create due varianti per un contenuto SMS, a seconda della lingua preferita del destinatario.

   ![](assets/conditions-language-sample.png)

1. Quando il contenuto è pronto, puoi visualizzare in anteprima le diverse varianti utilizzando **[!UICONTROL Simula contenuto]** pulsante. [Scopri come testare e visualizzare in anteprima i messaggi](../content-management/preview-test.md)

   ![](assets/conditions-preview.png)

## Aggiungere contenuto dinamico alle e-mail {#emails}

>[!CONTEXTUALHELP]
>id="ac_conditional_content"
>title="Contenuto condizionale"
>abstract="Utilizza le regole condizionali per creare più varianti di un componente contenuto. Se nessuna delle condizioni è soddisfatta durante l’invio del messaggio, verrà visualizzato il contenuto della variante predefinita."

>[!CONTEXTUALHELP]
>id="ac_conditional_content_select"
>title="Contenuto condizionale"
>abstract="Utilizza una regola condizionale salvata nella libreria o creane una nuova."

Per creare varianti di un componente di contenuto in E-mail Designer, segui questi passaggi:

1. In [E-mail Designer](../email/content-from-scratch.md), seleziona un componente di contenuto, quindi fai clic su **[!UICONTROL Abilita contenuto condizionale]**.

   ![](assets/conditions-enable-conditional.png)

1. Il **[!UICONTROL Contenuto condizionale]** a sinistra. In questo riquadro, puoi creare più varianti del componente di contenuto selezionato utilizzando le condizioni.

   Configura la prima variante selezionando la **[!UICONTROL Seleziona condizione]** pulsante.

   ![](assets/conditions-apply.png)

1. Viene visualizzata la libreria delle condizioni. Seleziona la regola condizionale da associare alla variante, quindi fai clic su **[!UICONTROL Seleziona]**. In questo esempio, vogliamo adattare il testo del componente in base alla lingua preferita del destinatario.

   ![](assets/conditions-select.png)

   Puoi anche creare una nuova regola facendo clic su **[!UICONTROL Crea nuovo]**. [Scopri come creare le condizioni](create-conditions.md)

1. La regola condizionale è associata alla variante. Per una migliore leggibilità, rinomina la variante selezionando la **[!UICONTROL Rinomina]** dall&#39;icona Altre azioni.

   ![](assets/conditions-rename.png)

1. Configura la modalità di visualizzazione del componente se la regola viene soddisfatta durante l’invio del messaggio. In questo esempio, vogliamo visualizzare il testo in francese se è la lingua preferita del destinatario.

   ![](assets/conditions-design.png)

1. Aggiungi tutte le varianti necessarie per il componente contenuto. Puoi passare in qualsiasi momento da una variante all’altra per verificare come verrà visualizzato il componente contenuto a seconda delle regole condizionali.

   >[!NOTE]
   >Se nessuna delle regole definite nelle varianti è soddisfatta durante l’invio del messaggio, il componente contenuto visualizzerà il contenuto definito nel **[!UICONTROL Variante predefinita]**.
   >
   >Il contenuto condizionale verrà valutato in base alle regole associate nell’ordine in cui vengono visualizzate le varianti. La variante predefinita viene sempre visualizzata se non sono soddisfatte altre condizioni.

1. Per eliminare una variante, fai clic sull’icona Altre azioni accanto alla variante desiderata e seleziona **[!UICONTROL Elimina]**.

   ![](assets/conditions-delete.png)
