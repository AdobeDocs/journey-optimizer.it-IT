---
title: Attività attendi
description: Scopri l’attività attendi
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 7268489a-38c1-44da-b043-f57aaa12d7d5
source-git-commit: b31eb2bcf52bb57aec8e145ad8e94790a1fb44bf
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 5%

---

# Attività attendi{#wait-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_wait"
>title="Attività attendi"
>abstract="Se desideri attendere prima di eseguire l’attività successiva nel percorso, puoi utilizzare un’attività Attendi . Ti consente di definire il momento in cui verrà eseguita l’attività successiva. Sono disponibili due opzioni: durata e personalizzazione."

Se desideri attendere prima di eseguire l&#39;attività successiva nel percorso, puoi utilizzare un **[!UICONTROL Wait]** attività. Ti consente di definire il momento in cui verrà eseguita l’attività successiva. Sono disponibili tre opzioni:

* [Durata](#duration)
* [Personalizzato](#custom)

<!--
* [Email send time optimization](#email_send_time_optimization)
* [Fixed date](#fixed_date) 
-->

## Informazioni sull’attività Attendi{#about_wait}

La durata massima di attesa è di 30 giorni. In modalità di prova, il **[!UICONTROL Wait time in test]** ti consente di definire la durata di ogni attività di attesa. Il tempo predefinito è di 10 secondi. In questo modo sarà possibile ottenere rapidamente i risultati del test. Consulta [questa pagina](../building-journeys/testing-the-journey.md)

Presta attenzione quando utilizzi più attività Attendi in un percorso, in quanto il timeout del percorso globale è di 30 giorni, il che significa che un profilo abbandonerà sempre il percorso al massimo 30 giorni dopo l’inserimento.

## Durata attesa{#duration}

Seleziona la durata dell’attesa prima dell’esecuzione dell’attività successiva.

![](assets/journey55.png)

<!--
## Fixed date wait{#fixed_date}

Select the date for the execution of the next activity.

![](assets/journey56.png)

-->

## Attesa personalizzata{#custom}

Questa opzione ti consente di definire una data personalizzata, ad esempio 12 luglio 2020 alle 17:00, utilizzando un’espressione avanzata basata su un campo proveniente da un evento o da un’origine dati. Non ti consente di definire una durata personalizzata, ad esempio 7 giorni. L&#39;espressione nell&#39;editor di espressioni deve fornire un formato dateTimeOnly. Fai riferimento a questo [page](expression/expressionadvanced.md). Per ulteriori informazioni sul formato dateTimeOnly, consulta questo [page](expression/data-types.md).

>[!NOTE]
>
>È possibile sfruttare un&#39;espressione dateTimeOnly o utilizzare una funzione per convertire in dateTimeOnly. Ad esempio: toDateTimeOnly(@{Event.offerOpened.activity.endTime}), il campo nell&#39;evento è del modulo 2016-08-12T09:46:06Z
>
>La **fuso orario** è previsto nelle proprietà del percorso. Di conseguenza, oggi non è possibile dall&#39;interfaccia puntare direttamente a un tempo pieno di mixaggio e fuso orario ISO-8601 come 2016-08-12T09:46:06,982-05. Consulta [questa pagina](../building-journeys/timezone-management.md).

![](assets/journey57.png)

<!--## Email send time optimization{#email_send_time_optimization}

This type of wait uses a score calculated in Adobe Experience Platform. The score calculates the propensity to click or open an email in the future based on past behavior. Note that the algorithm calculating the score needs a certain amount of data to work. As a result, when it does not have enough data, the default wait time will apply. At publication time, you’ll be notified that the default time applies.

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
