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
source-git-commit: a6b2c1585867719a48f9abc4bf0eb81558855d85
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 15%

---

# Eventi generali {#general-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_custom"
>title="Eventi unitari"
>abstract="Gli eventi consentono di attivare i percorsi in modo unitario per inviare messaggi in tempo reale all’utente che entra nel percorso. Per questo tipo di evento, puoi aggiungere solo un’etichetta e una descrizione. La configurazione dell’evento viene eseguita da un ingegnere dei dati e non può essere modificata."

Eventi consente di attivare i percorsi in modo unitario per inviare messaggi in tempo reale all’utente che entra nel percorso.

Per questo tipo di evento, puoi aggiungere solo un’etichetta e una descrizione. Impossibile modificare il resto della configurazione. È stata eseguita dall’utente tecnico. Consulta [questa pagina](../event/about-events.md).

![](assets/general-events.png)

Quando si rilascia un evento di business, questo aggiunge automaticamente un **Read Audience** attività. Per ulteriori informazioni sugli eventi di business, consulta [questa sezione](../event/about-events.md)

## Ascolto degli eventi durante un periodo di tempo specifico {#events-specific-time}

Un’attività evento posizionata nel percorso ascolta gli eventi a tempo indefinito. Per ascoltare un evento solo durante un determinato periodo di tempo, è necessario configurare un timeout per l’evento.

Il percorso ascolterà quindi l’evento durante il tempo specificato nel timeout. Se un evento viene ricevuto durante tale periodo, la persona scorrerà nel percorso dell’evento. In caso contrario, il cliente percorrerà un percorso di timeout o terminerà il percorso.

Per configurare un timeout per un evento, effettua le seguenti operazioni:

1. Attiva il **[!UICONTROL Definire il timeout dell’evento]** dalle proprietà dell’evento.

1. Specifica il tempo di attesa dell&#39;evento da parte del percorso. La durata massima è di 29 giorni.

1. Se desideri inviare i singoli utenti a un percorso di timeout quando non viene ricevuto alcun evento entro il timeout specificato, abilita **[!UICONTROL Impostare un percorso di timeout]** opzione. Se questa opzione non è abilitata, il percorso termina per l’utente una volta raggiunto il timeout.

   ![](assets/event-timeout.png)

In questo esempio, il percorso invia un messaggio push di benvenuto a un cliente. Invia quindi un messaggio push con uno sconto sui pasti solo se il cliente entra nel ristorante entro il giorno successivo. Abbiamo quindi configurato l’evento del ristorante con un timeout di 1 giorno:

* Se l’evento del ristorante viene ricevuto meno di 1 giorno dopo il messaggio push di benvenuto, l’attività push per lo sconto sui pasti viene inviata.
* Se non viene ricevuto alcun evento del ristorante nel giorno successivo, la persona scorre attraverso il percorso di timeout.

Se desideri configurare un timeout per più eventi posizionati dopo un’ **[!UICONTROL Wait]** attività, è necessario configurare il timeout solo per uno di questi eventi.

Il timeout verrà applicato a tutti gli eventi posizionati dopo il **[!UICONTROL Wait]** attività. Se non viene ricevuto alcun evento prima del timeout specificato, i singoli utenti scorrono in un unico percorso di timeout o terminano il percorso.

![](assets/event-timeout-group.png)
