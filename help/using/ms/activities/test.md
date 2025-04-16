---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l'attività Test nelle campagne orchestrate
description: Scopri come utilizzare l'attività Test
hide: true
hidefromtoc: true
exl-id: edd70849-0a21-45f2-91f3-4774a0cad9dd
source-git-commit: 3d380d2d02eb7043aebcffd00bb2092e7341b0d5
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
>abstract="L&#39;attività **Test** può avere più transizioni di output. Durante l&#39;esecuzione della campagna orchestrata, ogni condizione viene testata in sequenza fino a quando non viene soddisfatta una di esse. Se nessuna delle condizioni viene soddisfatta, la campagna orchestrata continua lungo il percorso della **[!UICONTROL condizione]** predefinita. Se non viene attivata alcuna condizione predefinita, la campagna orchestrata si interrompe a questo punto."

L’attività **Test** è un’attività di **Controllo del flusso**. Consente di abilitare le transizioni in base a condizioni specificate.

## Configurare l&#39;attività di test {#test-configuration}

Per configurare l&#39;attività **di test** , effettuate le seguenti operazioni:

1. Aggiungi un&#39;attività **di test** alla campagna orchestrata.

1. Per impostazione predefinita, l&#39;attività **[!UICONTROL Test]** presenta un test booleano semplice. Se viene soddisfatta la condizione definita nel transizione &quot;True&quot;, questa transizione verrà attivata. In caso contrario, verrà attivata una transizione predefinita &quot;False&quot;.

1. Per configurare la condizione associata a un transizione, fare clic sull&#39;icona **[!UICONTROL della finestra di dialogo]** Apri personalizzazione. Utilizzare l&#39;espressione editor per definire le regole necessarie per attivare questo transizione. È inoltre possibile sfruttare variabili di evento, condizioni e funzioni di data/ora. [Scopri come utilizzare le variabili di evento e l&#39;espressione editor](../event-variables.md)

   Inoltre, puoi modificare il **[!UICONTROL campo Etichetta]** per personalizzare il nome del transizione nell&#39;area di lavoro della campagna orchestrata.

   ![](../assets/workflow-test-default.png)

1. È possibile aggiungere più transizioni di output a un&#39;attività **[!UICONTROL di test]** . A tale scopo, fare clic sulla **[!UICONTROL pulsante Aggiungi condizione]** e configurare l&#39;etichetta e la condizione associata per ogni transizione.
v
1. Durante l&#39;esecuzione della campagna orchestrata, ogni condizione viene testata in sequenza fino a quando non viene soddisfatta una di esse. Se nessuna delle condizioni viene soddisfatta, le campagne orchestrate continuano lungo il percorso della **[!UICONTROL condizione]** predefinita. Se non viene attivata alcuna condizione di impostazione predefinita, i flussi di lavoro si interrompono in questo punto.

## Esempio {#example}

In questo esempio, vengono attivate transizioni diverse in base al numero di profili di destinazione di un&#39;attività **[!UICONTROL di creazione di pubblico]** :

* Se viene scelto come target più di 10.000 profili, viene inviato un messaggio e-mail.
* Per 1.000-10.000 profili, viene inviato un SMS.
* Se i profili con targeting scendono al di sotto di 1.000, vengono indirizzati a un transizione &quot;non contattare&quot;.

![](../assets/workflow-test-example.png)

Per fare ciò, la `vars.recCount` variabile di evento è stata sfruttata nelle condizioni &quot;email&quot; e &quot;sms&quot; per contare il numero di profili mirati e attivare il transizione appropriato.

![](../assets/workflow-test-example-config.png)
