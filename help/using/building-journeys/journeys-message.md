---
solution: Journey Optimizer
product: journey optimizer
title: Aggiungere un'azione di canale incorporata a un percorso
description: Scopri come aggiungere un’azione di canale incorporata a un percorso
feature: Journeys, Activities, Channels Activity
topic: Content Management
role: User
level: Intermediate
keywords: percorso, messaggio, push, sms, e-mail, in-app, web, scheda di contenuti, esperienza basata su codice
exl-id: 4db07a9e-c3dd-4873-8bd9-ac34c860694c
version: Journey Orchestration
source-git-commit: afac93abcd2bacc4371748b94c0e66942a4c5076
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 17%

---

# Utilizzare le azioni canale incorporate {#add-a-message-in-a-journey}

>[!CONTEXTUALHELP]
>id="ajo_message_activity"
>title="Azioni canale incorporate"
>abstract="Journey Optimizer viene fornito con funzionalità di azioni canale incorporate. Puoi semplicemente aggiungere al tuo percorso un messaggio (e-mail, messaggio di testo (SMS/MMS), push) o un’attività di un’esperienza in entrata (in-app, web, esperienza basata su codice, scheda contenuto) e definire impostazioni e contenuti. Viene quindi eseguito e inviato nel contesto del percorso."

[!DNL Journey Optimizer] viene fornito con funzionalità di azione del canale incorporate utilizzate per inviare messaggi: quando un profilo accede a questa attività, viene inviato un messaggio.

Per aggiungere al percorso un’azione di canale incorporata, trascina e rilascia un’attività di canale e definisci le relative impostazioni e il contenuto. Viene quindi eseguito e inviato nel contesto del percorso.

>[!NOTE]
>
>Puoi anche impostare azioni personalizzate per inviare i messaggi in [!DNL Journey Optimizer]. [Ulteriori informazioni](#recommendation)

## Aggiungere un messaggio in un percorso  {#add-msg-in-journey}

Con le azioni del canale incorporate, puoi configurare i messaggi in uscita o in entrata. Per ulteriori informazioni sui canali disponibili nei percorsi, consulta la tabella in questa sezione: [Canali nei percorsi e nelle campagne](../channels/gs-channels.md#channels).

Per aggiungere un’azione di canale incorporata a un percorso, segui la procedura riportata di seguito.

1. Avvia il percorso con un&#39;attività [Event](general-events.md) o [Read Audience](read-audience.md).

1. Dalla sezione **Azioni** della palette, trascina e rilascia un&#39;attività di canale nell&#39;area di lavoro.

   ![](assets/journey-web-activity.png)

1. È inoltre possibile selezionare l&#39;attività **[!UICONTROL Azione]**, che consente di selezionare più azioni in entrata. [Ulteriori informazioni](journey-action.md)

1. Configura l’attività. Linee guida dettagliate sulla configurazione sono disponibili nei collegamenti riportati di seguito.

   * Scopri i passaggi dettagliati per creare l’azione in uscita come segue:

     <table style="table-layout:fixed">
      <tr style="border: 0;">
      <td>
      <a href="../email/create-email.md">
      <img alt="Lead" src="../assets/do-not-localize/email.jpg">
      </a>
      <div><a href="../email/create-email.md"><strong>Creare e-mail</strong>
      </div>
      <p>
      </td>
      <td>
      <a href="../push/create-push.md">
      <img alt="Non frequente" src="../assets/do-not-localize/push.jpg">
      </a>
      <div>
      <a href="../push/create-push.md"><strong>Creare notifiche push<strong></a>
      </div>
      <p>
      </td>
      <td>
      <a href="../sms/create-sms.md">
      <img alt="Convalida" src="../assets/do-not-localize/sms.jpg">
      </a>
      <div>
      <a href="../sms/create-sms.md"><strong>Creare messaggi di testo (SMS/MMS)</strong></a>
      </div>
      <p>
      </td>
      </tr>
      </table>

   * Scopri i passaggi dettagliati per creare l’azione in entrata come segue:

     <table style="table-layout:fixed">
      <tr style="border: 0;">
      <td>
      <a href="../in-app/create-in-app.md">
      <img alt="Lead" src="../assets/do-not-localize/in-app.jpg">
      </a>
      <div><a href="../in-app/create-in-app.md"><strong>Creare messaggi in-app</strong>
      </div>
      <p>
      </td>
      <td>
      <a href="../web/create-web.md">
      <img alt="Lead" src="../assets/do-not-localize/web-create.jpg">
      </a>
      <div><a href="../web/create-web.md"><strong>Crea esperienze Web</strong>
      </div>
      <p>
      </td>
      <td>
      <a href="../content-card/create-content-card.md">
      <img alt="Lead" src="../assets/do-not-localize/sms-config.jpg">
      </a>
      <div><a href="../content-card/create-content-card.md"><strong>Creare schede di contenuti</strong>
      </div>
      <p>
      </td>
      <td>
      <a href="../code-based/create-code-based.md">
      <img alt="Non frequente" src="../assets/do-not-localize/web-design.jpg">
      </a>
      <div>
      <a href="../code-based/create-code-based.md"><strong>Creare esperienze basate su codice<strong></a>
      </div>
      <p>
      </td>
      </tr>
      </table>

   >[!NOTE]
   >
   >* Ogni attività esperienza in entrata viene fornita con un&#39;attività **Wait** di 3 giorni. [Ulteriori informazioni](wait-activity.md#auto-wait-node)
   >
   >* Per le e-mail e le notifiche push, puoi abilitare Ottimizzazione del tempo di invio. [Ulteriori informazioni](send-time-optimization.md)

1. A seconda dell’attività, puoi visualizzare parametri avanzati specifici per il canale selezionato e ignorare alcuni valori predefiniti, come l’indirizzo di esecuzione. [Ulteriori informazioni](about-journey-activities.md#advanced-parameters)

   >[!NOTE]
   >
   >Se i parametri avanzati sono nascosti, fare clic sul pulsante **[!UICONTROL Mostra campi di sola lettura]** nella parte superiore del riquadro di destra.

## Aggiornare un contenuto live {#update-live-content}

Puoi aggiornare il contenuto di un’azione del canale incorporata in un percorso live.

A questo scopo, apri il percorso live, seleziona l&#39;attività del canale e fai clic su **Modifica contenuto**.

![](assets/add-a-message2.png)

Tuttavia, non puoi modificare gli attributi utilizzati nella personalizzazione, siano essi attributi di profilo o dati contestuali (dalle proprietà di evento o di percorso).

Se i dati contestuali sono stati modificati, verrà visualizzato il seguente messaggio di errore: `ERR_AUTHORING_JOURNEYVERSION_201`

Se sono stati modificati gli attributi del profilo, verrà visualizzato il seguente messaggio di errore: `ERR_AUTHORING_JOURNEYVERSION_202`

Tieni presente che per l’attività in-app è possibile apportare qualsiasi modifica al contenuto mentre il percorso è in esecuzione, ma non è possibile modificare i trigger in-app.

## Inviare con azioni personalizzate {#recommendation}

Invece di utilizzare le funzionalità per messaggi incorporate, puoi utilizzare azioni personalizzate per configurare la connessione di un sistema di terze parti per l’invio di messaggi o chiamate API.

* Se utilizzi un sistema di terze parti per l’invio dei messaggi, puoi creare un’azione personalizzata. [Ulteriori informazioni](../action/action.md)

* Se utilizzi Adobe Campaign, consulta le sezioni seguenti:

   * [[!DNL Journey Optimizer] e Campaign v7/v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] e Campaign Standard](../action/acs-action.md)