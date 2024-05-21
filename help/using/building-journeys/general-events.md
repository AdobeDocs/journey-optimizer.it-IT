---
solution: Journey Optimizer
product: journey optimizer
title: Eventi generali
description: Scopri come utilizzare gli eventi generali
feature: Journeys, Events
topic: Content Management
role: User
level: Intermediate
keywords: personalizzato, generale, eventi, percorso
exl-id: b1813122-7031-452e-9ac5-a4ea7c6dc57c
source-git-commit: cc4ea97f858a212b82ac3b77328e61f59e3bfc27
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 14%

---

# Eventi generali {#general-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_custom"
>title="Eventi unitari"
>abstract="Gli eventi consentono di attivare i percorsi in modo unitario per inviare messaggi in tempo reale all’utente che entra nel percorso. Per questo tipo di evento, puoi aggiungere solo un’etichetta e una descrizione. La configurazione dell’evento viene eseguita da un ingegnere dei dati e non può essere modificata."

>[!CONTEXTUALHELP]
>id="ajo_journey_event_business_canvas"
>title="Eventi di business"
>abstract="Questi eventi ti consentono di avviare un percorso utilizzando un evento non correlato al profilo. Quando tale evento viene attivato, potrai inviare messaggi a un pubblico di profili. Per questo tipo di evento, puoi aggiungere solo un’etichetta e una descrizione. La configurazione dell’evento viene eseguita da un utente tecnico e non può essere modificata."

Eventi consente di attivare i percorsi in modo unitario per inviare messaggi in tempo reale all’utente che entra nel percorso.

Per questo tipo di evento, puoi aggiungere solo un’etichetta e una descrizione. Impossibile modificare il resto della configurazione. È stata eseguita dall’utente tecnico. Consulta [questa pagina](../event/about-events.md).

![](assets/general-events.png)

Quando si rilascia un evento di business, questo aggiunge automaticamente un **Read Audience** attività. Per ulteriori informazioni sugli eventi di business, consulta [questa sezione](../event/about-events.md)

## Ascolto degli eventi durante un periodo di tempo specifico {#events-specific-time}

Un’attività evento posizionata nel percorso ascolta gli eventi a tempo indefinito. Per ascoltare un evento solo durante un determinato periodo di tempo, è necessario configurare un timeout per l’evento.

Il percorso ascolterà quindi l’evento durante il tempo specificato nel timeout. Se un evento viene ricevuto durante tale periodo, la persona scorrerà nel percorso dell’evento. In caso contrario, il cliente passa al percorso di timeout, se definito, oppure continua quel percorso.

Se non è definito alcun percorso di timeout, l’impostazione di timeout fungerà da attività di attesa, facendo aspettare il profilo per un periodo di tempo che potrebbe essere interrotto se un evento si verifica prima della fine di tale attesa. Se desideri escludere i profili da tale percorso dopo il timeout, devi impostare un percorso di timeout.

Per configurare un timeout per un evento, effettua le seguenti operazioni:

1. Attiva il **[!UICONTROL Definire il timeout dell’evento]** dalle proprietà dell’evento.

1. Specifica il tempo di attesa dell&#39;evento da parte del percorso. La durata massima è di 29 giorni.

1. Se desideri inviare i singoli utenti a un percorso di timeout quando non viene ricevuto alcun evento entro il timeout specificato, abilita **[!UICONTROL Impostare un percorso di timeout]** opzione. Se questa opzione non è abilitata, il percorso continuerà per la singola persona una volta raggiunto il timeout. È consigliabile abilitare sempre **Impostare un percorso di timeout** opzione.

   ![](assets/event-timeout.png)

In questo esempio, il percorso invia un’e-mail di benvenuto a un cliente dopo che è entrato nell’atrio. Invia un’e-mail con uno sconto sui pasti solo se il cliente entra nel ristorante entro il giorno successivo. Abbiamo quindi configurato l’evento del ristorante con un timeout di 1 giorno:

* Se l’evento del ristorante viene ricevuto meno di 1 giorno dopo l’e-mail di benvenuto, viene inviata l’e-mail con lo sconto sui pasti.
* Se non viene ricevuto alcun evento del ristorante nel giorno successivo, la persona scorre attraverso il percorso di timeout.

Se desideri configurare un timeout per più eventi posizionati dopo un’ **[!UICONTROL Wait]** attività, è necessario configurare il timeout solo per uno di questi eventi.

Il timeout definito si applica a tutti gli eventi posizionati dopo il **[!UICONTROL Wait]** attività:

* Se un evento viene ricevuto entro la durata di timeout, il singolo passa nel percorso dell’evento ricevuto.
* Se non viene ricevuto alcun evento entro la durata di timeout, il singolo fluisce nel ramo di timeout dell’evento in cui è stato definito il timeout.

![](assets/event-timeout-group.png)
