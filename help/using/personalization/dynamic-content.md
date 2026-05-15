---
solution: Journey Optimizer
product: journey optimizer
title: Creare contenuti dinamici
description: Scopri come aggiungere contenuto dinamico ai messaggi.
feature: Personalization
topic: Personalization
role: Developer
level: Intermediate
keywords: espressione, editor, dynamic, content
exl-id: 639ad7df-0d0f-4c9b-95d1-f3101267aae2
TQID: https://experienceleague.adobe.com/j9jmVxc9Pn53hghR-2sUGXjcczfQibs5XTGuD7gwiI4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: ee5bb250-0884-4d71-86eb-d8489e8bcadd
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 655
ht-degree: 0%

---

# Creare contenuti dinamici {#dynamic-content}

Adobe Journey Optimizer consente di sfruttare le regole condizionali create nella libreria per aggiungere contenuto dinamico ai messaggi.

Il contenuto dinamico può essere creato in qualsiasi campo in cui puoi aggiungere la personalizzazione utilizzando l’editor di personalizzazione. Ciò include l’oggetto, i collegamenti, il contenuto delle notifiche push o le rappresentazioni delle offerte di tipo testo. [Ulteriori informazioni sulla personalizzazione](personalize.md)

Inoltre, puoi utilizzare le regole condizionali nel Designer e-mail per creare più varianti di un componente di contenuto.

## Aggiungere contenuto dinamico alle espressioni {#perso-expressions}

I passaggi per aggiungere contenuto dinamico nelle espressioni sono i seguenti:

1. Passa al campo in cui desideri aggiungere contenuto dinamico, quindi apri l’editor di personalizzazione.

1. Selezionare il menu **[!UICONTROL Condizioni]** per visualizzare l&#39;elenco delle regole condizionali disponibili. Fai clic sul pulsante + accanto a una regola per aggiungerla all’espressione corrente.

   Puoi anche creare una nuova regola selezionando **[!UICONTROL Crea nuovo]**. [Scopri come creare le condizioni](create-conditions.md)

   ![](assets/conditions-expression.png)

1. Aggiungere tra i tag `{%if}` e `{%/if}` il contenuto da visualizzare se la regola condizionale è soddisfatta. Puoi aggiungere tutte le regole necessarie per creare diverse varianti di un’espressione.

   Nell’esempio seguente, sono state create due varianti per un contenuto SMS, a seconda della lingua preferita del destinatario.

   ![](assets/conditions-language-sample.png)

1. Quando il contenuto è pronto, puoi visualizzare in anteprima le diverse varianti utilizzando il pulsante **[!UICONTROL Simula contenuto]**. [Scopri come verificare e visualizzare in anteprima i messaggi](../content-management/preview-test.md)

   ![](assets/conditions-preview.png)

>[!CAUTION]
>
>Se il rendering di E-mail Designer non riesce dopo l’aggiunta di blocchi condizionali, verifica che la sintassi di ogni nuova condizione sia corretta e che non esistano istruzioni duplicate o in conflitto. Se i problemi persistono, è consigliabile ricostruire le sezioni problematiche in un nuovo modello e testare ogni blocco condizionale in modo incrementale.


## Aggiungere contenuto dinamico alle e-mail {#emails}

>[!CONTEXTUALHELP]
>id="ac_conditional_content"
>title="Contenuto condizionale"
>abstract="Utilizza le regole condizionali per creare più varianti di un componente contenuto. Se nessuna delle condizioni è soddisfatta durante l’invio del messaggio, verrà visualizzato il contenuto della variante predefinita."

>[!CONTEXTUALHELP]
>id="ac_conditional_content_select"
>title="Contenuto condizionale"
>abstract="Utilizza una regola condizionale salvata nella libreria o creane una nuova."

I passaggi per creare varianti di un componente di contenuto nel Designer e-mail sono i seguenti:

1. In [E-mail Designer](../email/content-from-scratch.md), seleziona un componente di contenuto, quindi fai clic su **[!UICONTROL Abilita contenuto condizionale]**.

   ![](assets/conditions-enable-conditional.png)

1. Il riquadro **[!UICONTROL Contenuto condizionale]** viene visualizzato a sinistra. In questo riquadro, puoi creare più varianti del componente di contenuto selezionato utilizzando le condizioni.

   Configura la prima variante selezionando il pulsante **[!UICONTROL Seleziona condizione]**.

   ![](assets/conditions-apply.png)

1. Viene visualizzata la libreria delle condizioni. Seleziona la regola condizionale da associare alla variante, quindi fai clic su **[!UICONTROL Seleziona]**. In questo esempio, vogliamo adattare il testo del componente in base alla lingua preferita del destinatario.

   ![](assets/conditions-select.png)

   Puoi anche creare una nuova regola facendo clic su **[!UICONTROL Crea nuovo]**. [Scopri come creare le condizioni](create-conditions.md)

1. La regola condizionale è associata alla variante. Per una migliore leggibilità, rinomina la variante selezionando l&#39;azione **[!UICONTROL Rinomina]** dall&#39;icona Altre azioni.

   ![](assets/conditions-rename.png)

1. Configura la modalità di visualizzazione del componente se la regola viene soddisfatta durante l’invio del messaggio. In questo esempio, vogliamo visualizzare il testo in francese se è la lingua preferita del destinatario.

   ![](assets/conditions-design.png)

1. Aggiungi tutte le varianti necessarie per il componente contenuto. Puoi passare in qualsiasi momento da una variante all’altra per verificare come verrà visualizzato il componente contenuto a seconda delle regole condizionali.

   >[!NOTE]
   >
   >* Se nessuna delle regole definite nelle varianti viene soddisfatta durante l&#39;invio del messaggio, il componente contenuto visualizzerà il contenuto definito nella **[!UICONTROL variante predefinita]**.
   >
   >* Il contenuto condizionale verrà valutato in base alle regole associate nell’ordine in cui vengono visualizzate le varianti. La variante predefinita viene sempre visualizzata se non sono soddisfatte altre condizioni.
   >
   >* Durante la simulazione o il rendering delle bozze per e-mail contenenti più varianti condizionali, Journey Optimizer potrebbe richiedere più tempo di elaborazione. In caso di timeout o messaggi di errore, puoi ridurre il numero totale di varianti o semplificare le regole condizionali. Ulteriori informazioni sulla verifica del contenuto in [questa pagina](../content-management/preview-test.md).


1. Per eliminare una variante, fai clic sull&#39;icona Altre azioni accanto alla variante desiderata e seleziona **[!UICONTROL Elimina]**.

   ![](assets/conditions-delete.png)
