---
solution: Journey Optimizer
product: journey optimizer
title: Attività attendi
description: Scopri come configurare l’attività Attendi
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: attendi, attività, percorso, successivo, area di lavoro
exl-id: 7268489a-38c1-44da-b043-f57aaa12d7d5
source-git-commit: ab6292e93bf848671d39037bdfe0de8bdd7191b6
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 5%

---

# Attività attendi {#wait-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_wait"
>title="Attività attendi"
>abstract="Se desideri attendere prima di eseguire l’attività successiva nel percorso, puoi utilizzare un’attività Attendi. Ti consente di definire il momento in cui verrà eseguita l’attività successiva. Sono disponibili due opzioni: durata e personalizzata."

È possibile utilizzare una **[!UICONTROL Wait]** per definire una durata prima di eseguire l’attività successiva.  La durata massima di attesa è **29 giorni**.

È possibile impostare due tipi di **Wait** attività:

* Un’attesa basata su una durata di correzione. [Ulteriori informazioni](#duration)
* Un’attesa personalizzata, utilizzando le funzioni per calcolarla. [Ulteriori informazioni](#custom)

<!--
* [Email send time optimization](#email_send_time_optimization)
* [Fixed date](#fixed_date) 
-->

## Consigli {#wait-recommendations}

### Attività di attesa multiple {#multiple-wait-activities}

Quando si utilizzano più **Wait** attività di un percorso, tieni presente che il timeout percorso globale è di 30 giorni, il che significa che i profili vengono sempre eliminati dal massimo percorso di 30 giorni dopo il loro ingresso. Per ulteriori informazioni, consulta [questa pagina](../building-journeys/journey-gs.md#global_timeout).

Un individuo può immettere un **Wait** attività solo se dispone di tempo sufficiente nel percorso per completare la durata dell’attesa prima del timeout di 30 percorsi. Ad esempio, se ne aggiungi due **Wait** attività impostate su 20 giorni ciascuna, il sistema rileva che il secondo **Wait** l’attività termina dopo il timeout di 30 giorni. Il secondo **Wait** L’attività verrà quindi ignorata e l’utente uscirà dal percorso prima di avviarlo. In questo esempio, il cliente rimarrà per un totale di 20 giorni nel percorso.

### Attendere e rientrare {#wait-re-entrance}

Best practice per non utilizzare **Wait** attività per bloccare il rientro. Invece, utilizza **Consenti rientro** a livello di proprietà del percorso. Per ulteriori informazioni, consulta [questa pagina](../building-journeys/journey-gs.md#entrance).

### Modalità di attesa e test {#wait-test-modd}

In modalità di test, il **[!UICONTROL Tempo di attesa nel test]** parametro consente di definire il tempo che ogni **Wait** l’attività durerà. Il tempo predefinito è di 10 secondi. In questo modo potrai ottenere rapidamente i risultati del test. Per ulteriori informazioni, consulta [questa pagina](../building-journeys/testing-the-journey.md).

## Configurazione {#wait-configuration}

### Attesa durata {#duration}

Seleziona la **Durata** digita per impostare la durata dell’attesa prima dell’esecuzione dell’attività successiva. La durata massima è **29 giorni**.

![Definire la durata dell’attesa](assets/journey55.png)

<!--
## Fixed date wait{#fixed_date}

Select the date for the execution of the next activity.

![](assets/journey56.png)

-->

### Attesa personalizzata {#custom}

Seleziona la **Personalizzato** digita per definire una durata personalizzata, utilizzando un’espressione avanzata basata su un campo proveniente da un evento o da una risposta a un’azione personalizzata. Non è possibile definire direttamente una durata relativa, ad esempio 7 giorni, ma è possibile utilizzare le funzioni per calcolarla se necessario (ad esempio, 2 giorni dopo l’acquisto).

![Definire un’attesa personalizzata con un’espressione](assets/journey57.png)

L’espressione nell’editor deve fornire `dateTimeOnly` formato. Consulta [questa pagina](expression/expressionadvanced.md). Per ulteriori informazioni sul formato dateTimeOnly, fare riferimento a [questa pagina](expression/data-types.md).

Si consiglia di utilizzare date personalizzate specifiche per i profili ed evitare di utilizzare la stessa data per tutti. Ad esempio, non definire `toDateTimeOnly('2024-01-01T01:11:00Z')` ma piuttosto `toDateTimeOnly(@event{Event.productDeliveryDate})` che è specifico per ciascun profilo. Tieni presente che l’utilizzo di date fisse può causare problemi nell’esecuzione del percorso.


>[!NOTE]
>
>Puoi sfruttare una `dateTimeOnly` espressione o utilizzare una funzione per convertire in una `dateTimeOnly`. Ad esempio: `toDateTimeOnly(@event{Event.offerOpened.activity.endTime})`, se il campo è del modulo 2023-08-12T09:46:06Z
>
>Il **fuso orario** nelle proprietà del percorso. Di conseguenza, dall’interfaccia utente di, non è possibile puntare direttamente a una marca temporale ISO-8601 completa per la combinazione di tempo e scostamento fuso orario, come 2023-08-12T09:46:06.982-05 [Ulteriori informazioni](../building-journeys/timezone-management.md).


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
