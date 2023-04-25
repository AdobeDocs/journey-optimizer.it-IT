---
solution: Journey Optimizer
product: journey optimizer
title: Eventi generali
description: Scopri come utilizzare gli eventi generali
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: personalizzato, generale, eventi, percorso
exl-id: b1813122-7031-452e-9ac5-a4ea7c6dc57c
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 20%

---

# Eventi generali {#general-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_custom"
>title="Eventi generali"
>abstract="Eventi ti consente di attivare i tuoi percorsi in modo unitario per inviare messaggi in tempo reale all’utente che entra nel percorso. Per questo tipo di evento, puoi aggiungere solo un’etichetta e una descrizione. La configurazione dell’evento viene eseguita da un ingegnere dei dati e non può essere modificata."

Eventi ti consente di attivare i tuoi percorsi in modo unitario per inviare messaggi in tempo reale all’utente che entra nel percorso.

Per questo tipo di evento, puoi aggiungere solo un’etichetta e una descrizione. Impossibile modificare il resto della configurazione. È stato eseguito dall’utente tecnico. Consulta [questa pagina](../event/about-events.md).

![](assets/general-events.png)

Quando rilasci un evento aziendale, aggiunge automaticamente una **Leggi segmento** attività. Per ulteriori informazioni sugli eventi aziendali, consulta [questa sezione](../event/about-events.md)

## Ascolto degli eventi durante un periodo di tempo specifico {#events-specific-time}

Un’attività dell’evento posizionata nel percorso ascolta gli eventi a tempo indefinito. Per ascoltare un evento solo durante un certo periodo di tempo, devi configurare un timeout per l’evento.

Il percorso ascolterà quindi l&#39;evento durante il tempo specificato nel timeout. Se un evento viene ricevuto durante quel periodo, la persona scorre nel percorso dell&#39;evento. In caso contrario, il cliente può scorrere in un percorso di timeout o terminare il percorso.

Per configurare un timeout per un evento, effettua le seguenti operazioni:

1. Attiva la **[!UICONTROL Definire il timeout dell’evento]** dalle proprietà dell’evento.

1. Specifica il tempo di attesa dell’evento da parte del percorso.

1. Se desideri inviare i singoli utenti a un percorso di timeout quando non viene ricevuto alcun evento entro il timeout specificato, abilita **[!UICONTROL Imposta un percorso di timeout]** opzione . Se questa opzione non è abilitata, il percorso termina per la persona una volta raggiunto il timeout.

   ![](assets/event-timeout.png)

In questo esempio, il percorso invia un primo messaggio push di benvenuto a un cliente. Invia quindi un push con sconto sul pasto solo se il cliente entra nel ristorante entro il giorno successivo. Abbiamo pertanto configurato l’evento del ristorante con un timeout di 1 giorno:

* Se l’evento del ristorante viene ricevuto meno di 1 giorno dopo il messaggio push di benvenuto, viene inviata l’attività push con sconto sui pasti.
* Se non viene ricevuto alcun evento di ristorante entro il giorno successivo, la persona scorre attraverso il percorso di timeout.

Tieni presente che se desideri configurare un timeout su più eventi posizionati dopo un **[!UICONTROL Wait]** attività , devi configurare il timeout solo per uno di questi eventi.

Il timeout si applica a tutti gli eventi posizionati dopo il **[!UICONTROL Wait]** attività. Se non viene ricevuto alcun evento prima del timeout specificato, i singoli utenti accederanno a un unico percorso di timeout o termineranno il loro percorso.

![](assets/event-timeout-group.png)
