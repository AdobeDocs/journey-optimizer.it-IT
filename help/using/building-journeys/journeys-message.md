---
solution: Journey Optimizer
product: journey optimizer
title: Aggiungere un messaggio in un percorso
description: Scopri come aggiungere un messaggio in un percorso
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 4db07a9e-c3dd-4873-8bd9-ac34c860694c
source-git-commit: 0b19af568b33d29f4b35deeab6def17919cfe824
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 18%

---

# Messaggi e-mail, SMS e push{#add-a-message-in-a-journey}

[!DNL Journey Optimizer] include funzionalità integrate per messaggi. Puoi semplicemente aggiungere, nel tuo percorso, un’attività push, un SMS o un messaggio e-mail e [definire impostazioni e contenuto](../messages/messages-in-journeys.md). Viene quindi eseguito e inviato nel contesto del percorso.

Puoi anche impostare azioni specifiche per l’invio dei messaggi:

* Se utilizzi un sistema di terze parti per l’invio dei messaggi, puoi creare un’azione personalizzata. Ulteriori informazioni [sezione](../action/action.md).

* Se lavori con Campaign e Journey Optimizer, consulta le sezioni seguenti:

   * [[!DNL Journey Optimizer] e Campaign Classic v7/Campaign v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] e Campaign Standard](../action/acs-action.md)

Per aggiungere un messaggio in un percorso, segui i passaggi seguenti:

1. Inizia il tuo percorso con un [Evento](general-events.md) o un’attività [Leggi segmento](read-segment.md).

1. Dalla sezione **Azioni** della palette, trascina un’attività **E-mail**, **SMS** o **Push** nell’area di lavoro.

   ![](../messages/assets/add-a-message.png)


   Tutti i passaggi per configurare il messaggio e definirne il contenuto sono descritti in [questa sezione](../messages/get-started-content.md).

## Aggiornare il contenuto live{#update-live-content}

Puoi aggiornare il contenuto di un messaggio (e-mail, sms, push) in un percorso live.

A questo scopo, apri il percorso live, seleziona l’attività messaggio e fai clic su **Modifica contenuto**.

![](assets/add-a-message2.png)

Tuttavia, non puoi modificare gli attributi utilizzati nella personalizzazione, siano essi attributi di profilo o dati contestuali (dalle proprietà di evento o percorso).
