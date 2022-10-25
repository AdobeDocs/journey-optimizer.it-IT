---
solution: Journey Optimizer
product: journey optimizer
title: Creare contenuti dinamici
description: Scopri come aggiungere elementi dinamici ai messaggi.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 1%

---


# Creare contenuti dinamici {#dynamic-content}

Adobe Journey Optimizer consente di sfruttare le regole condizionali create nella libreria per aggiungere contenuto dinamico ai messaggi.

Il contenuto dinamico può essere creato in qualsiasi campo in cui puoi aggiungere la personalizzazione utilizzando l’editor espressioni. Ciò include riga dell’oggetto, collegamenti, contenuto di notifiche push o rappresentazioni di offerte di tipo testo. [Ulteriori informazioni sui contesti di personalizzazione](personalization-contexts.md)

Inoltre, è possibile utilizzare le regole condizionali in E-mail Designer per creare più varianti di un componente contenuto.

## Aggiungere contenuto dinamico alle espressioni {#perso-expressions}

I passaggi per aggiungere contenuto dinamico nelle espressioni sono i seguenti:

1. Passa al campo in cui desideri aggiungere contenuto dinamico, quindi apri l’editor espressioni.

1. Seleziona la **[!UICONTROL Condizioni]** per visualizzare l’elenco delle regole condizionali disponibili. Fai clic sul pulsante + accanto a una regola per aggiungerla all’espressione corrente.

   Puoi anche creare una nuova regola selezionando **[!UICONTROL Crea nuovo]**. [Scopri come creare condizioni](create-conditions.md)

   ![](assets/conditions-expression.png)

1. Aggiungi tra `{%if}` e `{%/if}` assegna i tag al contenuto da visualizzare se la regola condizionale è soddisfatta. Puoi aggiungere tutte le regole necessarie per creare diverse varianti di un’espressione.

   Nell’esempio seguente, sono state create due varianti per un contenuto SMS, a seconda della lingua preferita del destinatario.

   ![](assets/conditions-language-sample.png)

1. Quando il contenuto è pronto, puoi visualizzare in anteprima le diverse varianti utilizzando la **[!UICONTROL Simulazione del contenuto]** pulsante . [Scopri come verificare e visualizzare in anteprima i messaggi](../design/preview.md)

   ![](assets/conditions-preview.png)

## Aggiungere contenuto dinamico alle e-mail {#emails}

>[!CONTEXTUALHELP]
>id="ac_conditional_content"
>title="Contenuto condizionale"
>abstract="Utilizza le regole condizionali per creare più varianti di un componente di contenuto. Se non viene soddisfatta alcuna condizione durante l’invio del messaggio, viene visualizzato il contenuto della variante Predefinito ."

>[!CONTEXTUALHELP]
>id="ac_conditional_content_select"
>title="Contenuto condizionale"
>abstract="Utilizza una regola condizionale salvata nella libreria o creane una nuova."

I passaggi per creare varianti di un componente contenuto in E-mail Designer sono i seguenti:

1. In E-mail Designer, seleziona un componente di contenuto, quindi fai clic su **[!UICONTROL Abilitare il contenuto condizionale]**.

   ![](assets/conditions-enable-conditional.png)

1. La **[!UICONTROL Contenuto condizionale]** a sinistra viene visualizzato il riquadro . In questo riquadro è possibile creare più varianti del componente di contenuto selezionato utilizzando le condizioni.

   Configura la prima variante selezionando la **[!UICONTROL Applica condizione]** pulsante .

   ![](assets/conditions-apply.png)

1. Viene visualizzata la libreria delle condizioni. Seleziona la regola condizionale da associare alla variante, quindi fai clic su **[!UICONTROL Seleziona]**. In questo esempio, vogliamo adattare il testo del componente in base alla lingua preferita del destinatario.

   ![](assets/conditions-select.png)

   Puoi anche creare una nuova regola facendo clic su **[!UICONTROL Crea nuovo]**. [Scopri come creare condizioni](create-conditions.md)

1. La regola condizionale è associata alla variante. Per una migliore leggibilità, è consigliabile rinominare la variante facendo clic sul menu ellisse.

   Ora configura la modalità di visualizzazione del componente se la regola è soddisfatta durante l’invio del messaggio. In questo esempio, si desidera visualizzare il testo in francese se si tratta della lingua preferita del destinatario.

   ![](assets/conditions-design.png)

1. Aggiungi tutte le varianti necessarie per il componente contenuto. Puoi passare in qualsiasi momento tra le diverse varianti per controllare la modalità di visualizzazione del componente contenuto in base alle regole condizionali.

   >[!NOTE]
   >Se durante l’invio del messaggio non viene soddisfatta nessuna delle regole definite nelle varianti, il componente di contenuto visualizza il contenuto definito nella **[!UICONTROL Variante predefinita]**.
   >
   >Il contenuto condizionale viene valutato in base alle regole associate nell’ordine in cui vengono visualizzate le varianti. La variante predefinita viene sempre visualizzata se non sono soddisfatte altre condizioni.
