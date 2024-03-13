---
solution: Journey Optimizer
product: journey optimizer
title: Attività Attendi
description: Scopri l’attività Attendi
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: attendi, attività, percorso, successivo, area di lavoro
exl-id: 7268489a-38c1-44da-b043-f57aaa12d7d5
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 17%

---

# Attività Attendi{#wait-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_wait"
>title="Attività Attendi"
>abstract="Se desideri attendere prima di eseguire l’attività successiva nel percorso, puoi utilizzare un’attività Attendi. Consente di stabilire il momento in cui verrà eseguita l’attività successiva. Sono disponibili due opzioni: durata e personalizzato."

Se desideri attendere prima di eseguire l’attività successiva nel percorso, puoi utilizzare un’ **[!UICONTROL Wait]** attività. Consente di stabilire il momento in cui verrà eseguita l’attività successiva. Sono disponibili le seguenti opzioni:

* [Durata](#duration)
* [Personalizzato](#custom)

<!--
* [Email send time optimization](#email_send_time_optimization)
* [Fixed date](#fixed_date) 
-->

## Informazioni sull’attività Attendi{#about_wait}

La durata massima di attesa è di 29 giorni. In modalità di test, il **[!UICONTROL Tempo di attesa nel test]** Questo parametro ti consente di definire la durata di ogni attività Attendi. Il tempo predefinito è di 10 secondi. In questo modo potrai ottenere rapidamente i risultati del test. Consulta [questa pagina](../building-journeys/testing-the-journey.md).

Presta attenzione quando utilizzi più attività di attesa in un percorso, in quanto il timeout percorso globale è di 30 giorni, il che significa che un profilo uscirà sempre dal valore massimo percorso 30 giorni dopo essere entrato. Consulta [questa pagina](../building-journeys/journey-gs.md#global_timeout).

Un singolo utente può accedere a un’attività di attesa solo se nel percorso gli è rimasto abbastanza tempo per completare la durata dell’attesa prima del timeout di 30 percorsi. Ad esempio, se aggiungi due attività di attesa impostate su 20 giorni ciascuna, il sistema rileverà che la seconda attesa terminerà dopo il timeout di 30 giorni. La seconda attesa verrà quindi ignorata e l’individuo uscirà dal percorso prima di avviarlo. In questo esempio, il cliente rimarrà per un totale di 20 giorni nel percorso.

È buona prassi non utilizzare le attese per bloccare il rientro. Invece, utilizza **Consenti rientro** a livello di proprietà del percorso. Consulta [questa pagina](../building-journeys/journey-gs.md#entrance).

## Attesa durata{#duration}

Seleziona la durata dell’attesa prima dell’esecuzione dell’attività successiva. La durata massima è di 29 giorni.

![](assets/journey55.png)

<!--
## Fixed date wait{#fixed_date}

Select the date for the execution of the next activity.

![](assets/journey56.png)

-->

## Attesa personalizzata{#custom}

Questa opzione consente di definire una data personalizzata, ad esempio 12 luglio 2023 alle 17:00, utilizzando un’espressione avanzata basata su un campo proveniente da un evento o un’origine dati. Non consente di definire una durata personalizzata, ad esempio 7 giorni. L’espressione nell’editor espressioni deve fornire un formato dateTimeOnly. Fai riferimento a questo [pagina](expression/expressionadvanced.md). Per ulteriori informazioni sul formato dateTimeOnly, vedere [pagina](expression/data-types.md).

>[!NOTE]
>
>È possibile sfruttare un&#39;espressione dateTimeOnly o utilizzare una funzione per convertire in dateTimeOnly. Ad esempio: toDateTimeOnly(@event{Event.offerOpened.activity.endTime}), il campo nell’evento è nel formato 2023-08-12T09:46:06Z
>
>Il **fuso orario** nelle proprietà del percorso. Di conseguenza, oggi non è possibile dall’interfaccia puntare direttamente a un timestamp completo ISO-8601 che mescola tempo e scostamento fuso orario come 2023-08-12T09:46:06.982-05 Consulta [questa pagina](../building-journeys/timezone-management.md).

![](assets/journey57.png)

Per verificare che l’attività Attendi funzioni come previsto, puoi utilizzare gli eventi dei passaggi. Consulta [questa pagina](../reports/query-examples.md#common-queries).

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
