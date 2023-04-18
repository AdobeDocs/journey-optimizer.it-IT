---
solution: Journey Optimizer
product: journey optimizer
title: Aggiungere un messaggio in un percorso
description: Scopri come aggiungere un messaggio in un percorso
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: percorso, messaggio, push, sms, e-mail, in-app
exl-id: 4db07a9e-c3dd-4873-8bd9-ac34c860694c
source-git-commit: 0c32248d13c08a98e9298ddc932aa2e547ab2acd
workflow-type: tm+mt
source-wordcount: '864'
ht-degree: 2%

---

# E-mail, In-app, Push, SMS{#add-a-message-in-a-journey}

[!DNL Journey Optimizer] include funzionalità integrate per messaggi. Puoi semplicemente aggiungere, nel tuo percorso, un push, un SMS, un’attività in-app o un messaggio e-mail e definire impostazioni e contenuti. Viene quindi eseguito e inviato nel contesto del percorso.

Puoi anche impostare azioni specifiche per l’invio dei messaggi:

* Se utilizzi un sistema di terze parti per l’invio dei messaggi, puoi creare un’azione personalizzata. Ulteriori informazioni [sezione](../action/action.md).

* Se lavori con Campaign e Journey Optimizer, consulta le sezioni seguenti:

   * [[!DNL Journey Optimizer] e Campaign Classic v7/Campaign v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] e Campaign Standard](../action/acs-action.md)

Per aggiungere un messaggio in un percorso, segui i passaggi seguenti:

1. Inizia il tuo percorso con un [Evento](general-events.md) o un’attività [Leggi segmento](read-segment.md).

1. Da **Azioni** sezione della palette, trascinare e rilasciare un **email**, un **In-app**, un **SMS** o **Push** nell’area di lavoro.

1. Configura l’attività. Scopri i passaggi dettagliati per la creazione del contenuto del messaggio nelle pagine seguenti:

   <table style="table-layout:fixed">
   <tr style="border: 0;">
   <td>
   <a href="../email/create-email.md">
   <img alt="Lead" src="../assets/do-not-localize/email.jpg">
   </a>
   <div><a href="../email/create-email.md"><strong>Creare le e-mail</strong>
   </div>
   <p>
   </td>
   <td>
   <a href="../in-app/create-in-app.md">
   <img alt="Lead" src="../assets/do-not-localize/in-app.jpg">
   </a>
   <div><a href="../in-app/create-in-app.md"><strong>Creare messaggi in-app</strong>
   </div>
   <p>
   </td>
   <td>
   <a href="../push/create-push.md">
   <img alt="Non fequente" src="../assets/do-not-localize/push.jpg">
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
   <a href="../sms/create-sms.md"><strong>Creare messaggi SMS</strong></a>
   </div>
   <p>
   </td>
   </tr>
   </table>

## Aggiornare il contenuto live{#update-live-content}

Puoi aggiornare il contenuto di un messaggio (e-mail, in-app, push, SMS) in un percorso live.

A questo scopo, apri il percorso live, seleziona l’attività messaggio e fai clic su **Modifica contenuto**.

![](assets/add-a-message2.png)

Tuttavia, non puoi modificare gli attributi utilizzati nella personalizzazione, siano essi attributi di profilo o dati contestuali (dalle proprietà di evento o percorso).

Per l’attività in-app, è possibile apportare eventuali modifiche al contenuto mentre il percorso è attivo, ma gli attivatori in-app non possono essere modificati.

## Ottimizzazione dei tempi di invio{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="Informazioni sull’ottimizzazione del tempo inviato"
>abstract="La funzione di ottimizzazione del momento di invio di Adobe Journey Optimizer, basata sui servizi AI di Adobe, può prevedere il momento migliore per inviare un messaggio e-mail o push al fine di massimizzare il coinvolgimento in base alle percentuali di apertura e clic storiche."

### Informazioni sull’ottimizzazione del tempo di invio {#about-send-time}

La funzione di ottimizzazione del momento di invio di Adobe Journey Optimizer, basata sui servizi AI di Adobe, può prevedere il momento migliore per inviare un messaggio e-mail o push al fine di massimizzare il coinvolgimento in base alle percentuali di apertura e clic storiche. Utilizza il nostro modello di apprendimento automatico per pianificare tempi di invio personalizzati per ogni utente in modo che aumentino le percentuali di apertura e clic dei messaggi.

Il modello di ottimizzazione del momento di invio acquisisce i dati di Adobe Journey Optimizer ed esamina le percentuali di apertura a livello di utente (per e-mail e push) e di clic (per e-mail) per determinare quando è più probabile che i clienti interagiscano con i tuoi messaggi. Per formulare raccomandazioni informate, l’ottimizzazione in fase di invio richiede almeno un mese di dati di tracciamento dei messaggi. Per ogni utente, il sistema sceglierà automaticamente il momento migliore utilizzando i seguenti punteggi:

* L&#39;ora migliore di ogni giorno della settimana per massimizzare il coinvolgimento
* Il giorno migliore della settimana per massimizzare il coinvolgimento
* L&#39;ora migliore del giorno migliore della settimana per massimizzare il coinvolgimento

Il modello varia a seconda che si tratti di punteggio o formazione. L&#39;addestramento viene effettuato inizialmente settimanalmente e poi trimestralmente. Il punteggio è inizialmente settimanale e poi mensile.

* Formazione: lo sviluppo dell’algoritmo utilizzato per ottenere il punteggio
* Punteggio: applicazione di un punteggio a singoli profili in base al modello addestrato

Queste informazioni vengono memorizzate con il profilo dell’utente e a cui si fa riferimento durante l’esecuzione del percorso per indicare a Adobe Journey Optimizer quando inviare il messaggio.

>[!CAUTION]
>
>Questa funzione non è compatibile con la modalità burst.

### Attivare l’ottimizzazione del tempo di invio{#activate-send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_email"
>title="Attivare l’ottimizzazione del tempo di invio"
>abstract="Scegli se ottimizzare l’apertura delle e-mail o i click-through delle e-mail selezionando il pulsante di opzione appropriato. Puoi anche scegliere di mettere tra parentesi i tempi di invio utilizzati dal sistema immettendo un valore per l’opzione Invia all’interno dell’opzione successiva."

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_push"
>title="Attivare l’ottimizzazione del tempo di invio"
>abstract="I messaggi push vengono impostati per impostazione predefinita sull’opzione di apertura, in quanto i clic non sono applicabili ai messaggi push. Puoi anche scegliere di mettere tra parentesi i tempi di invio utilizzati dal sistema immettendo un valore per l’opzione Invia all’interno dell’opzione successiva."

Abilita l’ottimizzazione in fase di invio su un messaggio e-mail o push selezionando la **Ottimizzazione dei tempi di invio** passa dai parametri dell’attività.

![](../building-journeys/assets/jo-message5.png)

Per i messaggi e-mail, scegli se ottimizzare le aperture dei messaggi e-mail o i click-through di e-mail selezionando il pulsante di scelta appropriato. I messaggi push vengono impostati per impostazione predefinita sull’opzione di apertura, in quanto i clic non sono applicabili ai messaggi push.

Puoi anche scegliere di applicare una parentesi ai tempi di invio utilizzati dal sistema immettendo un valore per la **Invia all&#39;interno del successivo** opzione . Se si sceglie &quot;sei ore&quot; come valore, [!DNL Journey Optimizer] controllerà ogni profilo utente e sceglierà il tempo di invio ottimale entro sei ore dal tempo di esecuzione del percorso.

**Cosa succede se il tempo ottimale è fuori dalla finestra?**

Prendiamo un esempio con la seguente configurazione:

* Ottimizzare i clic
* L&#39;azione deve iniziare alle 10 di mattina
* Finestra 3 ore

Un profilo può avere un tempo di apertura ottimale che si trova al di fuori della finestra. Ad esempio, l&#39;apertura ottimale di John al clic è alle 5 del pomeriggio.

A livello di profilo, ci sono punteggi per ogni ora della settimana. In questo esempio, l’e-mail verrà sempre inviata all’interno della finestra . In fase di esecuzione, il sistema controlla l’elenco dei punteggi all’interno di tale finestra (finestra di 3 ore a partire dalle 10 di mattina). Il sistema confronta quindi i punteggi per 10, 11 e mezzogiorno e seleziona il più alto. L’e-mail viene inviata in quel momento.
