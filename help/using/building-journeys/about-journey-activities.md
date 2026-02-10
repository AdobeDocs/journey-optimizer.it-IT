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
version: Journey Orchestration
source-git-commit: 70653bafbbe8f1ece409e3005256d9dff035b518
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 15%

---

# Introduzione alle attività dei percorsi {#about-journey-activities}

Combina attività di evento, orchestrazione e azione per creare scenari tra canali con più passaggi.

## Attività di eventi {#event-activities}

I percorsi personalizzati iniziano con eventi come un acquisto online. Una volta che un profilo entra in un percorso, si sposta attraverso di esso da solo. Ogni profilo può seguire un percorso e un ritmo diversi. Quando inizi con un evento, il percorso si attiva quando l’evento arriva. Ogni profilo segue quindi i passaggi definiti nel percorso.

Gli eventi configurati dall&#39;utente tecnico (vedere [questa pagina](../event/about-events.md)) vengono visualizzati nella prima categoria della palette. Questa categoria si trova sul lato sinistro dello schermo. Sono disponibili le seguenti attività di evento:

* [Eventi generali](../building-journeys/general-events.md)
* [Reazione](../building-journeys/reaction-events.md)
* [Qualificazione del pubblico](../building-journeys/audience-qualification-events.md)

![Tavolozza delle attività degli eventi nella finestra di progettazione del percorso](assets/journey43.png)

Per avviare il percorso, trascina e rilascia un’attività evento. Puoi anche fare doppio clic su di esso.

![Trascina l&#39;attività evento nella finestra di progettazione del percorso](assets/journey44.png)

## Attività di orchestrazione {#orchestration-activities}

Le attività di orchestrazione sono condizioni che consentono di determinare il passaggio successivo nel percorso. Queste condizioni possono includere se la persona ha un caso di supporto aperto o ha completato un acquisto. Possono anche includere le previsioni meteo locali o se la persona ha raggiunto 10.000 punti fedeltà.

Dalla palette, sul lato sinistro dello schermo, sono disponibili le seguenti attività di orchestrazione:

<!--* [Optimize](optimize.md)-->
* [Read Audience](read-audience.md)
* [Attendi](wait-activity.md)
* [Decisione sul contenuto](content-decision.md)
* [Ricerca nei set di dati](dataset-lookup.md)

![Tavolozza delle attività di orchestrazione nella finestra di progettazione del percorso](assets/journey-orchestration-activities.png)

## Attività di azione {#action-activities}

Le azioni sono ciò che si desidera che accada come risultato di un qualche tipo di trigger, ad esempio l’invio di un messaggio. È il pezzo del percorso che il cliente sperimenta.

Dalla palette sul lato sinistro della schermata, sotto **[!UICONTROL Eventi]** e **[!UICONTROL Orchestrazione]**, puoi trovare la categoria **[!UICONTROL Azioni]**. Sono disponibili le seguenti attività di azione:

* [Azioni canale incorporate](../building-journeys/journeys-message.md)
* [Azioni personalizzate](../building-journeys/using-custom-actions.md)
* [Salta](../building-journeys/jump.md)

![Tavolozza delle attività di azione nella finestra di progettazione del percorso](assets/journey58.png)

Queste attività rappresentano i diversi canali di comunicazione disponibili. Puoi combinarle per creare uno scenario cross-channel.

Puoi anche impostare azioni specifiche per l’invio di messaggi:

* Se per l’invio di messaggi utilizzi un sistema di terze parti, puoi creare un’azione personalizzata specifica. [Ulteriori informazioni](../action/action.md)

* Se lavori con [!DNL Adobe Campaign] e [!DNL Adobe Journey Optimizer], consulta le sezioni seguenti:

   * [[!DNL Adobe Journey Optimizer] e [!DNL Adobe Campaign] v7/v8](../action/acc-action.md)
   * [[!DNL Adobe Journey Optimizer] e [!DNL Adobe Campaign] Standard](../action/acs-action.md)
   * [[!DNL Adobe Journey Optimizer] e [!DNL Adobe Marketo Engage]](../action/marketo-engage.md)

## Best practice {#best-practices}

Utilizzare queste raccomandazioni per garantire la leggibilità, la coerenza e la facilità di risoluzione dei problemi dei percorsi.

### Aggiungi un’etichetta

La maggior parte delle attività ti consentono di definire un **[!UICONTROL Etichetta]**. Questo aggiunge un suffisso al nome visualizzato sotto l’attività nell’area di lavoro. Questa funzione è utile se utilizzi la stessa attività più volte nel percorso e desideri identificarla più facilmente. Semplifica inoltre il debug in caso di errori e facilita la lettura dei rapporti. È inoltre possibile aggiungere una **[!UICONTROL Descrizione]** facoltativa.

![Campi Etichetta e Descrizione nelle proprietà delle attività del percorso](assets/journey-action-label.png)

>[!NOTE]
>
>Per alcune attività, il loro ID è visibile anche nel riquadro. Questo ID può essere utilizzato nel reporting come chiave più stabile dell’etichetta, che può cambiare.

### Gestire i parametri avanzati {#advanced-parameters}

La maggior parte delle attività visualizza una serie di parametri avanzati e/o tecnici che non è possibile modificare.

![Campi dei parametri avanzati nelle proprietà dell&#39;attività di percorso](assets/journey-advanced-parameters.png)

Per una migliore leggibilità, nascondi questi parametri utilizzando il pulsante **[!UICONTROL Nascondi campi di sola lettura]** nella parte superiore del riquadro di destra.

![Nascondi l&#39;icona dei campi di sola lettura nelle proprietà dell&#39;attività del percorso](assets/journey-hide-read-only-fields.png)

In alcuni contesti particolari, è possibile ignorare i valori di questi parametri per un uso specifico. Per forzare un valore, fai clic sul pulsante **[!UICONTROL Abilita sovrascrittura del parametro]** a destra del campo. [Ulteriori informazioni](../configuration/primary-email-addresses.md#override-execution-address-journey)

![Abilita l&#39;opzione di sostituzione del parametro nelle proprietà dell&#39;attività E-mail](assets/journey-enable-parameter-override.png)

>[!NOTE]
>
>Se i parametri avanzati sono nascosti, fare clic sul pulsante **[!UICONTROL Mostra campi di sola lettura]**
>
>![Mostra l&#39;icona dei campi di sola lettura nelle proprietà dell&#39;attività del percorso](assets/journey-show-read-only-fields.png){width=60%}

### Aggiungi un percorso alternativo

Quando si verifica un errore in un’azione o in una condizione, il percorso di un singolo utente si interrompe. L&#39;unico modo per far sì che continui è selezionare la casella **[!UICONTROL Aggiungi un percorso alternativo in caso di timeout o errore]**. Vedi [questa sezione](../building-journeys/using-the-journey-designer.md#paths).

![Aggiungi un&#39;opzione di percorso alternativa nelle proprietà dell&#39;attività Condizione](assets/journey42.png)

## Risoluzione dei problemi {#troubleshooting}

Prima di testare e pubblicare il percorso, controlla che tutte le attività siano state configurate correttamente. Non è possibile eseguire test o pubblicazioni se il sistema rileva ancora degli errori.

Scopri come risolvere gli errori nelle attività e nel percorso [in questa pagina](troubleshooting.md).

Vedi anche **[Monitoraggio e risoluzione dei problemi](../../rp_landing_pages/troubleshoot-journey-landing-page.md)**.
