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
source-git-commit: 56a1ef1ba256d1aac3593d8a61e67bdc42c17d32
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 27%

---

# Utilizzare le azioni canale integrate {#add-a-message-in-a-journey}

>[!CONTEXTUALHELP]
>id="ajo_message_activity"
>title="Azione canale integrate"
>abstract="Journey Optimizer viene fornito con funzionalità di azione canale integrate. Puoi semplicemente aggiungere al tuo percorso un’attività in uscita (e-mail, messaggio di testo (SMS/MMS), push) o in entrata (in-app, web, esperienza basata su codice, scheda di contenuti) e definire impostazioni e contenuti. Viene quindi eseguito e inviato nel contesto del percorso."

[!DNL Journey Optimizer] viene fornito con funzionalità di azione del canale integrate. Puoi semplicemente aggiungere al tuo percorso un’attività in uscita (e-mail, messaggio di testo (SMS/MMS), push) o in entrata (in-app, web, esperienza basata su codice, scheda di contenuti) e definire impostazioni e contenuti. Viene quindi eseguito e inviato nel contesto del percorso.

>[!NOTE]
>
>Puoi anche impostare azioni specifiche per l’invio dei messaggi. [Ulteriori informazioni](#recommendation)

Per aggiungere un’azione di canale incorporata a un percorso, segui la procedura riportata di seguito.

1. Avvia il percorso con un&#39;attività [Event](general-events.md) o [Read Audience](read-audience.md).

1. Dalla sezione **Azioni** della palette, trascina un&#39;attività in uscita (**e-mail**, **push**, **SMS**) o in entrata (**In-app**, **web**, **esperienza basata su codice**, **scheda contenuto**) nell&#39;area di lavoro.

   ![](assets/journey-web-activity.png)

1. Configura l’attività.

   * Scopri i passaggi dettagliati per creare il contenuto del messaggio come segue:

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

     >[!NOTE]
     >
     >Per le e-mail e le notifiche push, puoi abilitare Ottimizzazione del tempo di invio. [Ulteriori informazioni](send-time-optimization.md)

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
     >Ogni attività di messaggio in entrata viene fornita con un&#39;attività **Wait** di 3 giorni. [Ulteriori informazioni](wait-activity.md#auto-wait-node)


## Aggiornare contenuti live {#update-live-content}

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