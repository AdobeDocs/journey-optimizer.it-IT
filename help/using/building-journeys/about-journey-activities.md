---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione alle attività dei percorsi
description: Introduzione alle attività dei percorsi
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 239b3d72-3be0-4a82-84e6-f219e33ddca4
source-git-commit: ca423c25d39162838368b2242c1aff99388df768
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 17%

---

# Introduzione alle attività dei percorsi {#about-journey-activities}

Combina le diverse attività relative a un evento, un percorso e un’azione in modo da creare scenari tra canali con più passaggi.

## Attività eventi {#event-activities}

Gli eventi attivano un percorso personalizzato, ad esempio un acquisto online. Una volta che qualcuno entra in un percorso, si muove come un individuo, e non due individui si muovono allo stesso ritmo o lungo lo stesso percorso. Quando avvii il percorso con un evento, il percorso viene attivato quando l’evento viene ricevuto. Ogni persona nel percorso segue, singolarmente, i passaggi successivi definiti nel percorso.

Eventi configurati dall’utente tecnico (consulta [questa pagina](../event/about-events.md)) sono visualizzate nella prima categoria della palette, sul lato sinistro dello schermo. Sono disponibili le seguenti attività eventi:

* [Eventi generali](../building-journeys/general-events.md)
* [Reazione](../building-journeys/reaction-events.md)
* [Qualificazione del segmento](../building-journeys/segment-qualification-events.md)

![](assets/journey43.png)

Avvia il percorso trascinando e rilasciando un’attività evento. Puoi anche fare doppio clic su di esso.

![](assets/journey44.png)

## Attività di orchestrazione {#orchestration-activities}

Le attività di orchestrazione sono condizioni diverse che consentono di determinare il passaggio successivo nel percorso. Può essere se la persona ha o meno un caso di supporto aperto, le previsioni del tempo nella sua posizione attuale, se ha completato o meno un acquisto, o ha raggiunto 10 000 punti fedeltà.

Nella palette a sinistra dello schermo sono disponibili le seguenti attività di orchestrazione:

* [Condizione](../building-journeys/condition-activity.md)
* [Attendi](../building-journeys/wait-activity.md)
* [Leggi segmento](../building-journeys/read-segment.md)

![](assets/journey49.png)

## Attività di azione {#action-activities}

Le azioni sono ciò che desideri che accada in seguito a un certo tipo di trigger, ad esempio l’invio di un messaggio. È il pezzo di percorso che il cliente sperimenta.

Dalla palette, sul lato sinistro dello schermo, sotto **[!UICONTROL Eventi]** e **[!UICONTROL Orchestrazione]**, puoi trovare la **[!UICONTROL Azioni]** categoria. Sono disponibili le seguenti attività di azione:

* [Messaggi e-mail, SMS e push](../building-journeys/journeys-message.md)
* [Azioni personalizzate](../building-journeys/using-custom-actions.md)
* [Salta](../building-journeys/jump.md)

![](assets/journey58.png)

Queste attività rappresentano i diversi canali di comunicazione disponibili. Puoi combinarle per creare uno scenario cross-channel.

Se hai configurato azioni personalizzate, queste vengono visualizzate anche qui. [Ulteriori informazioni](../building-journeys/using-custom-actions.md)).

## Best practice {#best-practices}

La maggior parte delle attività ti consente di definire un **[!UICONTROL Etichetta]**. Questo aggiunge un suffisso al nome che verrà visualizzato sotto l&#39;attività nell&#39;area di lavoro. Questa funzione è utile se utilizzi più volte la stessa attività nel percorso e desideri identificarla più facilmente. Semplifica inoltre il debug in caso di errori e faciliterà la lettura dei rapporti. È inoltre possibile aggiungere un **[!UICONTROL Descrizione]**.

![](assets/journey59bis.png)

Quando si verifica un errore in un’azione o in una condizione, il percorso di un singolo utente si arresta. L’unico modo per far sì che continui è selezionare la casella . **[!UICONTROL Aggiungi un percorso alternativo in caso di timeout o di errore]**. Vedi [questa sezione](../building-journeys/using-the-journey-designer.md#paths).

![](assets/journey42.png)
