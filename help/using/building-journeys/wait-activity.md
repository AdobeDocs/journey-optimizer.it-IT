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
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 16%

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

Quando utilizzi più attività **Wait** in un percorso, tieni presente che il [timeout globale](journey-properties.md#global_timeout) per i percorsi è di 91 giorni, il che significa che i profili vengono sempre eliminati dal massimo percorso 91 giorni dopo l&#39;immissione. Ulteriori informazioni su [questa pagina](journey-properties.md#global_timeout).

Una persona può accedere a un&#39;attività **Wait** solo se nel percorso è rimasto abbastanza tempo per completare la durata dell&#39;attesa prima del timeout di 91 percorsi.

### Attendere e rientrare {#wait-reentrance}

È consigliabile non utilizzare le attività **Wait** per bloccare il rientro. Utilizza invece l&#39;opzione **Consenti rientro** a livello di proprietà del percorso. Ulteriori informazioni su [questa pagina](../building-journeys/journey-properties.md#entrance).

### Modalità di attesa e test {#wait-test-modd}

In modalità di test, il parametro **[!UICONTROL Wait time in test]** (Tempo di attesa nel test) consente di definire la durata di ogni attività **Wait**. Il tempo predefinito è di 10 secondi. In questo modo potrai ottenere rapidamente i risultati del test. Ulteriori informazioni su [questa pagina](../building-journeys/testing-the-journey.md).

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

## Nodo di attesa automatico  {#auto-wait-node}


>[!CONTEXTUALHELP]
>id="ajo_journey_auto_wait_node "
>title="Informazioni sul nodo di attesa automatico"
>abstract="Un’attività **Attesa** viene aggiunta automaticamente dopo questa attività. È impostato per 3 giorni. Puoi rimuoverlo o configurarlo in base alle esigenze."

Ogni attività messaggio in entrata (messaggio in-app, esperienza basata su codice o scheda) viene fornita con un&#39;attività **Wait** di 3 giorni. Poiché i messaggi in entrata terminano automaticamente quando un profilo raggiunge la fine del percorso, si presume che gli utenti debbano visualizzarlo almeno per 3 giorni. Puoi rimuovere questa attività **Attendi** o modificarne la configurazione, se necessario.