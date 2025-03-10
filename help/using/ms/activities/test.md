---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività Test nelle campagne con più passaggi
description: Scopri come utilizzare l’attività Test
hide: true
hidefromtoc: true
source-git-commit: dfa6c6e11db10f3e843035d32e322b212361548c
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 15%

---

# Test {#test}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_test"
>title="Attività di test"
>abstract="L’attività **Test** è un’attività di **Controllo del flusso**. Consente di abilitare le transizioni in base a condizioni specificate."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_test_conditions"
>title="Condizioni"
>abstract="L&#39;attività **Test** può avere più transizioni di output. Durante l’esecuzione di una campagna in più passaggi, ogni condizione viene testata in sequenza fino a quando non ne viene soddisfatta una. Se nessuna delle condizioni è soddisfatta, la campagna con più passaggi continua lungo il percorso della **[!UICONTROL condizione predefinita]**. Se non viene attivata alcuna condizione predefinita, la campagna con più passaggi si interrompe a questo punto."

L’attività **Test** è un’attività di **Controllo del flusso**. Consente di abilitare le transizioni in base a condizioni specificate.

## Configurare l’attività di test {#test-configuration}

Per configurare l&#39;attività **Test**, eseguire la procedura seguente:

1. Aggiungi un&#39;attività **Test** alla campagna in più passaggi.

1. Per impostazione predefinita, l&#39;attività **[!UICONTROL Test]** presenta un semplice test booleano. Se la condizione definita nella transizione &quot;True&quot; è soddisfatta, questa transizione verrà attivata. In caso contrario, verrà attivata una transizione predefinita &quot;False&quot;.

1. Per configurare la condizione associata a una transizione, fai clic sull&#39;icona **[!UICONTROL Apri finestra di personalizzazione]**. Utilizza l’editor di espressioni per definire le regole necessarie per attivare questa transizione. Puoi anche sfruttare le variabili evento, le condizioni e le funzioni data/ora. [Scopri come utilizzare le variabili evento e l&#39;editor di espressioni](../event-variables.md)

   Inoltre, puoi modificare il campo **[!UICONTROL Etichetta]** per personalizzare il nome della transizione nell&#39;area di lavoro della campagna in più passaggi.

   ![](../assets/workflow-test-default.png)

1. È possibile aggiungere più transizioni di output a un&#39;attività **[!UICONTROL Test]**. A tale scopo, fare clic sul pulsante **[!UICONTROL Aggiungi condizione]** e configurare l&#39;etichetta e la condizione associata per ogni transizione.
v
1. Durante l’esecuzione di una campagna in più passaggi, ogni condizione viene testata in sequenza fino a quando non ne viene soddisfatta una. Se nessuna delle condizioni è soddisfatta, le campagne con più passaggi continuano lungo il percorso della **[!UICONTROL condizione predefinita]**. Se non viene attivata alcuna condizione di impostazione predefinita, i flussi di lavoro si interrompono in questo punto.

## Esempio {#example}

In questo esempio vengono attivate diverse transizioni in base al numero di profili interessati da un&#39;attività **[!UICONTROL Genera pubblico]**:

* Se il targeting riguarda più di 10.000 profili, viene inviato un messaggio e-mail.
* Per un numero di profili compreso tra 1.000 e 10.000, viene inviato un SMS.
* Se i profili target scendono al di sotto di 1.000, vengono indirizzati a una transizione &quot;non contattare&quot;.

![](../assets/workflow-test-example.png)

A questo scopo, la variabile dell&#39;evento `vars.recCount` è stata utilizzata nelle condizioni &quot;e-mail&quot; e &quot;sms&quot; per contare il numero di profili target e attivare la transizione appropriata.

![](../assets/workflow-test-example-config.png)
