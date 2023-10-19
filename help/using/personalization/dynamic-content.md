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
source-git-commit: 27447578dad6bd2612989d79cd0dc8ddbe78d629
workflow-type: tm+mt
source-wordcount: '545'
ht-degree: 17%

---

# Creare contenuti dinamici {#dynamic-content}

Adobe Journey Optimizer consente di sfruttare le regole condizionali create nella libreria per aggiungere contenuto dinamico ai messaggi.

Il contenuto dinamico può essere creato in qualsiasi campo in cui è possibile aggiungere la personalizzazione utilizzando l’editor di espressioni. Ciò include l’oggetto, i collegamenti, il contenuto delle notifiche push o le rappresentazioni delle offerte di tipo testo. [Ulteriori informazioni sui contesti di personalizzazione](personalization-contexts.md)

Inoltre, è possibile utilizzare le regole condizionali in E-mail Designer per creare più varianti di un componente di contenuto.

## Aggiungere contenuto dinamico alle espressioni {#perso-expressions}

I passaggi per aggiungere contenuto dinamico nelle espressioni sono i seguenti:

1. Passa al campo in cui desideri aggiungere contenuto dinamico, quindi apri l’editor di espressioni.

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
>abstract="Utilizza le regole condizionali per creare più varianti di un componente di contenuto. Se non viene soddisfatta alcuna condizione durante l’invio del messaggio, verrà visualizzato il contenuto della variante predefinita."

>[!CONTEXTUALHELP]
>id="ac_conditional_content_select"
>title="Contenuto condizionale"
>abstract="Utilizza una regola condizionale salvata nella libreria o creane una nuova."

Per creare varianti di un componente di contenuto in E-mail Designer, segui questi passaggi:

1. In E-mail Designer, seleziona un componente di contenuto, quindi fai clic su **[!UICONTROL Abilita contenuto condizionale]**.

   ![](assets/conditions-enable-conditional.png)

1. Il **[!UICONTROL Contenuto condizionale]** a sinistra. In questo riquadro, puoi utilizzare le condizioni per creare più varianti del componente di contenuto selezionato.

   Configura la prima variante selezionando la **[!UICONTROL Applica condizione]** pulsante.

   ![](assets/conditions-apply.png)

1. Viene visualizzata la libreria delle condizioni. Seleziona la regola condizionale da associare alla variante, quindi fai clic su **[!UICONTROL Seleziona]**. In questo esempio, vogliamo adattare il testo del componente in base alla lingua preferita del destinatario.

   ![](assets/conditions-select.png)

   Puoi anche creare una nuova regola facendo clic su **[!UICONTROL Crea nuovo]**. [Scopri come creare le condizioni](create-conditions.md)

1. La regola condizionale è associata alla variante. Per una migliore leggibilità, si consiglia di rinominare la variante facendo clic sul menu dell’ellisse.

   Ora configura come deve essere visualizzato il componente se la regola viene soddisfatta durante l’invio del messaggio. In questo esempio, se la lingua preferita del destinatario è il francese, il testo dovrà essere in francese.

   ![](assets/conditions-design.png)

1. Aggiungi tutte le varianti necessarie per il componente contenuto. Puoi passare in qualsiasi momento da una variante all’altra per verificare come verrà visualizzato il componente contenuto a seconda delle regole condizionali.

   >[!NOTE]
   >Se nessuna delle regole definite nelle varianti è soddisfatta durante l’invio del messaggio, il componente contenuto visualizzerà il contenuto definito nel **[!UICONTROL Variante predefinita]**.
   >
   >Il contenuto condizionale verrà valutato in base alle regole associate nell’ordine in cui vengono visualizzate le varianti. La variante predefinita viene sempre visualizzata se non sono soddisfatte altre condizioni.
