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
version: Journey Orchestration
source-git-commit: cec807afe35bc95be9fa8d455cd72c2600e51fa7
workflow-type: tm+mt
source-wordcount: '732'
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

## Consigli {#wait-recommendations}

### Attività di attesa multiple {#multiple-wait-activities}

Quando utilizzi più attività **Wait** in un percorso, tieni presente che il [timeout globale](journey-properties.md#global_timeout) per i percorsi è di 91 giorni, il che significa che i profili vengono sempre eliminati dal massimo percorso 91 giorni dopo l&#39;immissione. Ulteriori informazioni sono disponibili in [questa pagina](journey-properties.md#global_timeout).

Una persona può accedere a un&#39;attività **Wait** solo se nel percorso è rimasto abbastanza tempo per completare la durata dell&#39;attesa prima del timeout di 91 percorsi.

### Attendere e rientrare {#wait-reentrance}

È consigliabile non utilizzare le attività **Wait** per bloccare il rientro. Utilizza invece l&#39;opzione **Consenti rientro** a livello di proprietà del percorso. Ulteriori informazioni sono disponibili in [questa pagina](../building-journeys/journey-properties.md#entrance).

### Modalità di attesa e test {#wait-test-mode}

In modalità di test, il parametro **[!UICONTROL Wait time in test]** (Tempo di attesa nel test) consente di definire la durata di ogni attività **Wait**. Il tempo predefinito è di 10 secondi. In questo modo potrai ottenere rapidamente i risultati del test. Ulteriori informazioni sono disponibili in [questa pagina](../building-journeys/testing-the-journey.md).

### Canali attendi e mobili {#wait-mobile-channels}

Se desideri visualizzare un [messaggio in-app](../in-app/create-in-app.md) poco dopo aver inviato una [notifica push](../../rp_landing_pages/push-landing-page.md), utilizza un&#39;attività **Attendi** per consentire la propagazione del tempo di payload del messaggio in-app. In genere si consiglia un’attesa di 5-15 minuti, ma i tempi esatti possono variare a seconda della complessità del payload e delle esigenze di personalizzazione.

## Configurazione {#wait-configuration}

### Attesa durata {#duration}

Selezionare il tipo **Durata** per impostare la durata relativa dell&#39;attesa prima dell&#39;esecuzione dell&#39;attività successiva. La durata massima è di **90 giorni**.

![Definisci la durata dell&#39;attesa](assets/journey55.png)

<!--
## Fixed date wait{#fixed_date}

Select the date for the execution of the next activity.

![Wait activity configuration panel with duration and fixed date options](assets/journey56.png)

-->

### Attesa personalizzata {#custom}

Seleziona il tipo **Personalizzato** per definire una data personalizzata, utilizzando un&#39;espressione avanzata basata su un campo proveniente da un evento o una risposta a un&#39;azione personalizzata. Non è possibile definire direttamente una durata relativa, ad esempio 7 giorni, ma è possibile utilizzare le funzioni per calcolarla se necessario (ad esempio, 2 giorni dopo l’acquisto).

![Definisci un&#39;attesa personalizzata con un&#39;espressione](assets/journey57.png)

L&#39;espressione nell&#39;editor deve fornire un formato `dateTimeOnly`. Consulta [questa pagina](expression/expressionadvanced.md). Per ulteriori informazioni sul formato dateTimeOnly, vedere [questa pagina](expression/data-types.md).

Si consiglia di utilizzare date personalizzate specifiche per i profili ed evitare di utilizzare la stessa data per tutti. Ad esempio, non definire `toDateTimeOnly('2024-01-01T01:11:00Z')`, ma `toDateTimeOnly(@event{Event.productDeliveryDate})` specifico per ciascun profilo. Tieni presente che l’utilizzo di date fisse può causare problemi nell’esecuzione del percorso. Ulteriori informazioni sull&#39;impatto delle attività Attendi sulla velocità di elaborazione del percorso in [questa sezione](entry-management.md#wait-activities-impact).


>[!NOTE]
>
>È possibile sfruttare un&#39;espressione `dateTimeOnly` o utilizzare una funzione per convertire in `dateTimeOnly`. Ad esempio: `toDateTimeOnly(@event{Event.offerOpened.activity.endTime})`, il campo nell&#39;evento è del modulo 2023-08-12T09:46:06Z.
>
>Il **fuso orario** è previsto nelle proprietà del percorso. Di conseguenza, dall’interfaccia utente non è possibile puntare direttamente a una marca temporale ISO-8601 completa per la combinazione di tempo e scostamento fuso orario, ad esempio 2023-08-12T09:46:06.982-05. [Ulteriori informazioni](../building-journeys/timezone-management.md).

>[!CAUTION]
>
>Durante la creazione di un&#39;espressione di attesa personalizzata con `toDateTimeOnly()`, evitare di aggiungere &#39;Z&#39; o qualsiasi scostamento di fuso orario (ad esempio, &#39;-05:00&#39;) nel risultato dell&#39;espressione. L’espressione deve utilizzare una sintassi data/ora ISO valida che faccia riferimento al fuso orario configurato dal percorso senza indicatori di fuso orario espliciti.
>
>**Esempio corretto:** `toDateTimeOnly(concat(toString(toDateOnly(nowWithDelta(2, "days"))),"T10:00:00"))`
>
>**Esempio non corretto:** `toDateTimeOnly(concat(toString(toDateOnly(nowWithDelta(2, "days"))),"T10:00:00Z"))` ❌ (contiene &#39;Z&#39;)
>
>L’utilizzo di indicatori di fuso orario non supportati può causare il blocco dei profili nell’attività di attesa, anziché procedere come previsto.

Per verificare che l’attività Attendi funzioni come previsto, puoi utilizzare gli eventi dei passaggi. [Ulteriori informazioni](../reports/query-examples.md#common-queries).

## Nodo di attesa automatico  {#auto-wait-node}


>[!CONTEXTUALHELP]
>id="ajo_journey_auto_wait_node "
>title="Informazioni sul nodo di attesa automatico"
>abstract="Un’attività **Attesa** viene aggiunta automaticamente dopo questa attività. È impostato per 3 giorni. Puoi rimuoverlo o configurarlo in base alle esigenze."

Ogni attività esperienza in entrata (messaggio in-app, esperienza basata su codice o scheda) viene fornita con un&#39;attività **Wait** di 3 giorni. Poiché i messaggi in entrata terminano automaticamente quando un profilo raggiunge la fine del percorso, si presume che gli utenti debbano visualizzarlo almeno per 3 giorni. Puoi rimuovere questa attività **Attendi** o modificarne la configurazione, se necessario.
