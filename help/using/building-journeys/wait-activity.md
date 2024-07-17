---
solution: Journey Optimizer
product: journey optimizer
title: Attività Attendi
description: Scopri come configurare l’attività Attendi
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: attendi, attività, percorso, successivo, area di lavoro
exl-id: 7268489a-38c1-44da-b043-f57aaa12d7d5
source-git-commit: cae6d394ad1c2356e55bd5f1cb4ad7494c9623dd
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 15%

---

# Attività Attendi {#wait-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_wait"
>title="Attività Attendi"
>abstract="Se desideri attendere prima di eseguire l’attività successiva nel percorso, puoi utilizzare un’attività Attendi. Consente di stabilire il momento in cui verrà eseguita l’attività successiva. Sono disponibili due opzioni: durata e personalizzato."

Puoi utilizzare un&#39;attività **[!UICONTROL Wait]** per definire una durata prima di eseguire l&#39;attività successiva.  La durata massima di attesa è di **90 giorni**.

È possibile impostare due tipi di attività **Attendi**:

* Un’attesa basata su una durata relativa. [Ulteriori informazioni](#duration)
* Una data personalizzata, utilizzando le funzioni per calcolarla. [Ulteriori informazioni](#custom)

<!--
* [Email send time optimization](#email_send_time_optimization)
* [Fixed date](#fixed_date) 
-->

## Raccomandazioni {#wait-recommendations}

### Attività di attesa multiple {#multiple-wait-activities}

Quando utilizzi più attività **Wait** in un percorso, tieni presente che il [timeout globale](journey-properties.md#global_timeout) per i percorsi è di 91 giorni, il che significa che i profili vengono sempre eliminati dal massimo percorso 91 giorni dopo l&#39;immissione. Per ulteriori informazioni, consulta [questa pagina](journey-properties.md#global_timeout).

Una persona può accedere a un&#39;attività **Wait** solo se nel percorso è rimasto abbastanza tempo per completare la durata dell&#39;attesa prima del timeout di 91 percorsi.

### Attendere e rientrare {#wait-re-entrance}

È consigliabile non utilizzare le attività **Wait** per bloccare il rientro. Utilizza invece l&#39;opzione **Consenti rientro** a livello di proprietà del percorso. Per ulteriori informazioni, consulta [questa pagina](../building-journeys/journey-properties.md#entrance).

### Modalità di attesa e test {#wait-test-modd}

In modalità di test, il parametro **[!UICONTROL Wait time in test]** (Tempo di attesa nel test) consente di definire la durata di ogni attività **Wait**. Il tempo predefinito è di 10 secondi. In questo modo potrai ottenere rapidamente i risultati del test. Per ulteriori informazioni, consulta [questa pagina](../building-journeys/testing-the-journey.md).

## Configurazione {#wait-configuration}

### Attesa durata {#duration}

Selezionare il tipo **Durata** per impostare la durata relativa dell&#39;attesa prima dell&#39;esecuzione dell&#39;attività successiva. La durata massima è di **90 giorni**.

![Definisci la durata dell&#39;attesa](assets/journey55.png)

<!--
## Fixed date wait{#fixed_date}

Select the date for the execution of the next activity.

![](assets/journey56.png)

-->

### Attesa personalizzata {#custom}

Seleziona il tipo **Personalizzato** per definire una data personalizzata, utilizzando un&#39;espressione avanzata basata su un campo proveniente da un evento o una risposta a un&#39;azione personalizzata. Non è possibile definire direttamente una durata relativa, ad esempio 7 giorni, ma è possibile utilizzare le funzioni per calcolarla se necessario (ad esempio, 2 giorni dopo l’acquisto).

![Definisci un&#39;attesa personalizzata con un&#39;espressione](assets/journey57.png)

L&#39;espressione nell&#39;editor deve fornire un formato `dateTimeOnly`. Consulta [questa pagina](expression/expressionadvanced.md). Per ulteriori informazioni sul formato dateTimeOnly, vedere [questa pagina](expression/data-types.md).

Si consiglia di utilizzare date personalizzate specifiche per i profili ed evitare di utilizzare la stessa data per tutti. Ad esempio, non definire `toDateTimeOnly('2024-01-01T01:11:00Z')`, ma `toDateTimeOnly(@event{Event.productDeliveryDate})` specifico per ciascun profilo. Tieni presente che l’utilizzo di date fisse può causare problemi nell’esecuzione del percorso.


>[!NOTE]
>
>È possibile sfruttare un&#39;espressione `dateTimeOnly` o utilizzare una funzione per convertire in `dateTimeOnly`. Ad esempio: `toDateTimeOnly(@event{Event.offerOpened.activity.endTime})`, il campo nell&#39;evento è del modulo 2023-08-12T09:46:06Z.
>
>Il **fuso orario** è previsto nelle proprietà del percorso. Di conseguenza, dall’interfaccia utente non è possibile puntare direttamente a una marca temporale ISO-8601 completa per la combinazione di tempo e scostamento fuso orario, ad esempio 2023-08-12T09:46:06.982-05. [Ulteriori informazioni](../building-journeys/timezone-management.md).


Per verificare che l’attività Attendi funzioni come previsto, puoi utilizzare gli eventi dei passaggi. [Ulteriori informazioni](../reports/query-examples.md#common-queries).

<!--## Email send time optimization{#email_send_time_optimization}

This type of wait uses a score calculated in Adobe Experience Platform. The score calculates the propensity to click or open an email in the future based on past behavior. Note that the algorithm calculating the score needs a certain amount of data to work. As a result, when it does not have enough data, the default wait time will apply. At publication time, you'll be notified that the default time applies.

>[!NOTE]
>
>The first event of your journey must have a namespace.
>
>This capability is only available after an **[!UICONTROL Email]** activity. You need to have Adobe Campaign Standard.

1. In the **[!UICONTROL Amount of time]** field, define the number of hours to consider to optimize email sending.
1. In the **[!UICONTROL Optimization type]** field, choose if the optimization should increase clicks or opens.
1. In the **[!UICONTROL Default time]** field, define the default time to wait if the predictive send time score is not available.

    >[!NOTE]
    >
    >Note that the send time score can be unavailable because there is not enough data to perform the calculation. In this case, you will be informed, at publication time, that the default time applies.

![](assets/journey57bis.png)-->
