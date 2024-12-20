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
source-git-commit: 47482adb84e05fe41eb1c50479a8b50e00469ec4
workflow-type: tm+mt
source-wordcount: '1268'
ht-degree: 19%

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
      <div><a href="../content-card/create-content-card.md"><strong>Crea schede contenuto</strong>
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
     >Ogni attività di messaggio in entrata viene fornita con un&#39;attività **Wait** di 3 giorni. [Ulteriori informazioni](../building-journeys/wait-activity.md#auto-wait-node)

## Consiglio {#recommendation}

[!DNL Journey Optimizer] viene fornito con funzionalità per messaggi incorporate. Tuttavia, le azioni personalizzate ti consentono di configurare la connessione di un sistema di terze parti per l’invio di messaggi o chiamate API.

* Se utilizzi un sistema di terze parti per l’invio dei messaggi, puoi creare un’azione personalizzata. [Ulteriori informazioni](../action/action.md)

* Se utilizzi Campaign e Journey Optimizer, consulta le sezioni seguenti:

   * [[!DNL Journey Optimizer] e Campaign v7/v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] e Campaign Standard](../action/acs-action.md)

## Aggiornare contenuti live{#update-live-content}

Puoi aggiornare il contenuto di un’azione del canale incorporata in un percorso live.

A questo scopo, apri il percorso live, seleziona l&#39;attività del canale e fai clic su **Modifica contenuto**.

![](assets/add-a-message2.png)

Tuttavia, non puoi modificare gli attributi utilizzati nella personalizzazione, siano essi attributi di profilo o dati contestuali (dalle proprietà di evento o di percorso).

Se sono stati modificati i dati contestuali, verrà visualizzato il seguente messaggio di errore: ERR_AUTHORING_JOURNEYVERSION_201

Se sono stati modificati gli attributi del profilo, verrà visualizzato il seguente messaggio di errore: ERR_AUTHORING_JOURNEYVERSION_202

Tieni presente che per l’attività in-app è possibile apportare qualsiasi modifica al contenuto mentre il percorso è in esecuzione, ma non è possibile modificare i trigger in-app.

## Ottimizzazione dei tempi di invio{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="Ottimizzazione dell’ora di invio"
>abstract="La funzione di ottimizzazione dell’ora di invio di Adobe Journey Optimizer, basata sui servizi Adobe basati su intelligenza artificiale, può prevedere il momento migliore per inviare un messaggio e-mail o push al fine di massimizzare il coinvolgimento in base alle percentuali di apertura e di clic storici."

>[!NOTE]
>
>Questa funzione non è abilitata per impostazione predefinita. Puoi rivolgerti al tuo rappresentante Adobe per attivarlo.
>
>La funzione di ottimizzazione dell’ora di invio si applica solo ai canali e-mail e push.

### Informazioni sull’ottimizzazione dell’ora di invio {#about-send-time}

La funzione di ottimizzazione dell&#39;ora di invio di Adobe Journey Optimizer, basata sui servizi di intelligenza artificiale di Adobe, può prevedere il momento migliore per inviare un **messaggio e-mail** o **messaggio push** per massimizzare il coinvolgimento in base alle percentuali storiche di apertura e clic. Utilizza il nostro modello di apprendimento automatico per pianificare un’ora di invio personalizzata in modo da aumentare le percentuali di apertura e clic sui messaggi da parte di ogni utente.

Il modello di ottimizzazione dell’ora di invio acquisisce i dati Adobe Journey Optimizer e osserva le percentuali di apertura (e-mail e push) e clic (per e-mail) a livello di utente, per determinare quando i clienti hanno più probabilità di interagire con i messaggi. L’ottimizzazione dell’ora di invio richiede almeno un mese di dati di tracciamento dei messaggi per generare consigli informati. Per ogni utente, il sistema sceglierà automaticamente il momento migliore utilizzando i punteggi seguenti:

* L&#39;ora migliore di ogni giorno della settimana per massimizzare il coinvolgimento
* Il miglior giorno della settimana per massimizzare il coinvolgimento
* L&#39;ora migliore del giorno migliore della settimana per massimizzare il coinvolgimento

Il modello varia a seconda che si parli di punteggio o di formazione. La formazione viene condotta inizialmente con cadenza settimanale e quindi trimestrale. Il punteggio è inizialmente settimanale e poi mensile.

* Formazione: sviluppo dell’algoritmo utilizzato per assegnare il punteggio
* Punteggio: applicazione di un punteggio ai singoli profili in base al modello addestrato

Queste informazioni vengono memorizzate con il profilo dell’utente e vi si fa riferimento al momento dell’esecuzione del percorso per indicare a Adobe Journey Optimizer quando inviare il messaggio.

### Domande frequenti {#faq-send-time}

+++ Quali operazioni può eseguire l’ottimizzazione dell’ora di invio? In che modo gestisce i nuovi profili? Distribuisce l’invio nell’arco di un’ora 6/12/24?

Send-Time Optimization cerca di prevedere il momento migliore per interagire con i clienti e ottimizzare le percentuali di apertura e clic sulle e-mail. Il punteggio è in un formato di `3*7*24` attributi per ciascun profilo. Gli attributi `7*24` descrivono la classificazione del momento migliore previsto per l’invio di e-mail al destinatario e 3 serve per ottimizzare il tasso di apertura delle e-mail, il tasso di clic e il tasso di apertura push.

+++

+++Dove posso trovare il tempo di invio previsto per ciascun profilo?

Puoi visualizzare il punteggio complessivo nell&#39;interfaccia **Profili**. Per ciascuno dei tre set di 168 punteggi, la classifica va da -83 a 84. Più alto è il rango, migliore è il momento scelto per interagire con il destinatario. Poiché è possibile definire l&#39;inizio e la durata di un percorso, la classificazione migliore (84) potrebbe non rientrare in tale intervallo di tempo. In questo caso, consigliamo di scegliere un’ora con il valore di classificazione più alto.

+++


+++Quali rapporti sono disponibili?

Accedi al tuo percorso, fai clic sul pulsante **Visualizza rapporto** in alto a destra e seleziona la scheda **Percorso** a sinistra. [Ulteriori informazioni](../reports/journey-global-report-cja.md)

+++

+++In che modo i dati di ottimizzazione dell’ora di invio influiscono sulla ricchezza dei profili?

L’ottimizzazione dell’ora di invio aggiunge il punteggio/attributi a ciascun profilo, ma non ne viene creato uno nuovo.

+++

### Attivare l’ottimizzazione dell’ora di invio{#activate-send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_email"
>title="Attivare l’ottimizzazione dell’ora di invio"
>abstract="Scegli se effettuare l’ottimizzazione per l’apertura delle e-mail o i click-through delle e-mail selezionando l’opzione appropriata. Puoi anche restringere gli orari di invio utilizzati dal sistema immettendo un valore per l’opzione Invia entro."

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_push"
>title="Attivare l’ottimizzazione dell’ora di invio"
>abstract="Per impostazione predefinita, i messaggi push sono impostati sull’opzione Aperture, in quanto i clic non sono applicabili alla messaggistica push. Puoi anche restringere gli orari di invio utilizzati dal sistema immettendo un valore per l’opzione Invia entro."

Abilita Ottimizzazione dell&#39;ora di invio in un messaggio e-mail o push selezionando lo switch **Ottimizzazione dell&#39;ora di invio** dai parametri dell&#39;attività.

![](../building-journeys/assets/jo-message5.png)

Per i messaggi e-mail, scegli se ottimizzare all’apertura delle e-mail o ai click-through e-mail selezionando il pulsante di opzione appropriato. I messaggi push hanno per impostazione predefinita l’opzione opens, in quanto i clic non sono applicabili ai messaggi push.

È inoltre possibile scegliere di includere tra parentesi i tempi di invio utilizzati dal sistema immettendo un valore per l&#39;opzione **Invia entro il successivo**. Se si sceglie &quot;sei ore&quot; come valore, [!DNL Journey Optimizer] controllerà ogni profilo utente e sceglierà il tempo di invio ottimale entro sei ore dal tempo di esecuzione del percorso.

**Cosa succede se il tempo ottimale si trova all&#39;esterno della finestra?**

Prendiamo un esempio con la seguente configurazione:

* Ottimizza sui clic
* L’azione deve iniziare alle 10
* La finestra è di 3 ore

Un profilo può avere un tempo di apertura ottimale che si trova all’esterno della finestra. Ad esempio, l’apertura ottimale di John al clic è alle 17.

A livello di profilo, ci sono punteggi per ogni ora della settimana. In questo esempio, l’e-mail verrà sempre inviata all’interno della finestra. In fase di esecuzione, il sistema controlla l’elenco dei punteggi all’interno di tale finestra (finestra di 3 ore a partire dalle ore 00:00). Il sistema confronta quindi i punteggi per 10, 11 e mezzogiorno e seleziona il punteggio più alto. L’e-mail viene inviata in tale momento.
