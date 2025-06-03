---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione alle attività dei percorsi
description: Introduzione alle attività dei percorsi
feature: Journeys, Activities, Overview
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: percorso, attività, guida introduttiva, eventi, azione
exl-id: 239b3d72-3be0-4a82-84e6-f219e33ddca4
source-git-commit: 84beb9ba9646cb1b40bcfd8a180fc98963a8ff0b
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 12%

---

# Introduzione alle attività dei percorsi {#about-journey-activities}

Combina le diverse attività relative a eventi, orchestrazioni e azioni per creare scenari cross-channel con più passaggi.

## Attività eventi {#event-activities}

I percorsi personalizzati vengono attivati da eventi, ad esempio un acquisto online. Una volta che un profilo entra in un percorso, si sposta come un individuo, e non ci sono due individui che si muovono lungo la stessa velocità o lungo lo stesso percorso. Quando si avvia il percorso con un evento, il percorso si attiva quando l’evento viene ricevuto. Ogni persona nel percorso segue quindi singolarmente i passaggi successivi definiti nel percorso.

Gli eventi configurati dall&#39;utente tecnico (vedere [questa pagina](../event/about-events.md)) sono tutti visualizzati nella prima categoria della palette, sul lato sinistro dello schermo. Sono disponibili le seguenti attività di evento:

* [Eventi generali](../building-journeys/general-events.md)
* [Reazione](../building-journeys/reaction-events.md)
* [Qualificazione del pubblico](../building-journeys/audience-qualification-events.md)

![Tavolozza delle attività degli eventi nella finestra di progettazione del percorso](assets/journey43.png)

Per avviare il percorso, trascina e rilascia un’attività evento. Puoi anche fare doppio clic su di esso.

![Trascina l&#39;attività evento nella finestra di progettazione del percorso](assets/journey44.png)

## Attività di orchestrazione {#orchestration-activities}

Le attività di orchestrazione sono condizioni diverse che consentono di determinare il passaggio successivo nel percorso. Queste condizioni possono includere se la persona ha un caso di supporto aperto, le previsioni del tempo nella posizione corrente, se ha completato un acquisto o se ha raggiunto 10.000 punti fedeltà.

Dalla palette, sul lato sinistro dello schermo, sono disponibili le seguenti attività di orchestrazione:

* [Condizione](../building-journeys/condition-activity.md)
* [Attendi](../building-journeys/wait-activity.md)
* [Read Audience](../building-journeys/read-audience.md)

![Tavolozza delle attività di orchestrazione nella finestra di progettazione del percorso](assets/journey49.png)

## Attività azione {#action-activities}

Le azioni sono ciò che si desidera che accada come risultato di un qualche tipo di trigger, ad esempio l’invio di un messaggio. È il pezzo del percorso che il cliente sperimenta.

Dalla palette, sul lato sinistro della schermata, sotto **[!UICONTROL Eventi]** e **[!UICONTROL Orchestrazione]**, puoi trovare la categoria **[!UICONTROL Azioni]**. Sono disponibili le seguenti attività di azione:

* [Azioni del canale incorporate](../building-journeys/journeys-message.md)
* [Azioni personalizzate](../building-journeys/using-custom-actions.md)
* [Salta](../building-journeys/jump.md)

![Tavolozza delle attività di azione nella finestra di progettazione del percorso](assets/journey58.png)

Queste attività rappresentano i diversi canali di comunicazione disponibili. Puoi combinarle per creare uno scenario cross-channel.

<!--If you have configured custom actions, they also appear here. [Learn more](../building-journeys/using-custom-actions.md)-->

Puoi anche impostare azioni specifiche per l’invio di messaggi:

* Se per l’invio di messaggi utilizzi un sistema di terze parti, puoi creare un’azione personalizzata specifica. [Ulteriori informazioni](../action/action.md)

* Se utilizzi Campaign e Journey Optimizer, consulta le sezioni seguenti:

   * [[!DNL Journey Optimizer] e Campaign v7/v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] e Campaign Standard](../action/acs-action.md)

## Best practice {#best-practices}

### Aggiungi un’etichetta

La maggior parte delle attività ti consentono di definire un **[!UICONTROL Etichetta]**. Questo aggiunge un suffisso al nome visualizzato sotto l’attività nell’area di lavoro. Questa funzione è utile se utilizzi la stessa attività più volte nel percorso e desideri identificarla più facilmente. Semplifica inoltre il debug in caso di errori e facilita la lettura dei rapporti. È inoltre possibile aggiungere una **[!UICONTROL Descrizione]** facoltativa.

![](assets/journey-action-label.png)

>[!NOTE]
>
>Per alcune attività, il loro ID è visibile anche nel riquadro. Questo ID può essere utilizzato nel reporting come chiave più stabile dell’etichetta, che può cambiare.

### Gestire i parametri avanzati {#advanced-parameters}

La maggior parte delle attività visualizza una serie di parametri avanzati e/o tecnici che non è possibile modificare.

![](assets/journey-advanced-parameters.png)

Per una migliore leggibilità, nascondi questi parametri utilizzando il pulsante **[!UICONTROL Nascondi campi di sola lettura]**.

![](assets/journey-hide-read-only-fields.png)

In alcuni contesti particolari, è possibile ignorare i valori di questi parametri per un uso specifico. Per forzare un valore, fai clic sul pulsante **[!UICONTROL Abilita sovrascrittura del parametro]** a destra del campo. [Ulteriori informazioni](../configuration/primary-email-addresses.md#journey-parameters)

![](assets/journey-enable-parameter-override.png)

### Aggiungi un percorso alternativo

Quando si verifica un errore in un’azione o in una condizione, il percorso di un singolo utente si arresta. L&#39;unico modo per far sì che continui è selezionare la casella **[!UICONTROL Aggiungi un percorso alternativo in caso di timeout o errore]**. Consulta [questa sezione](../building-journeys/using-the-journey-designer.md#paths).

![](assets/journey42.png)
