---
solution: Journey Optimizer
product: journey optimizer
title: Aggiungere un messaggio in un percorso
description: Scopri come aggiungere un messaggio in un percorso
feature: Journeys, Activities, Channels Activity
topic: Content Management
role: User
level: Intermediate
keywords: percorso, messaggio, push, sms, e-mail, in-app
exl-id: 4db07a9e-c3dd-4873-8bd9-ac34c860694c
source-git-commit: 898ad9dadd2d9e71e6881113730ac469a36257bc
workflow-type: tm+mt
source-wordcount: '1167'
ht-degree: 14%

---

# E-mail, in-app, push, SMS/MMS{#add-a-message-in-a-journey}

>[!CONTEXTUALHELP]
>id="ajo_message_activity"
>title="Attività per messaggi"
>abstract="Journey Optimizer viene fornito con funzionalità per messaggi integrate. Puoi semplicemente aggiungere nel percorso un messaggio push, un SMS (SMS/MMS), un’attività in-app o un messaggio e-mail e definire impostazioni e contenuti. Viene quindi eseguito e inviato nel contesto del percorso."

[!DNL Journey Optimizer] viene fornito con funzionalità per i messaggi incorporate. Puoi semplicemente aggiungere nel percorso un’attività push, SMS/MMS, in-app o messaggio e-mail e definire impostazioni e contenuti. Viene quindi eseguito e inviato nel contesto del percorso.

Puoi anche impostare azioni specifiche per l’invio di messaggi:

* Se utilizzi un sistema di terze parti per l’invio dei messaggi, puoi creare un’azione personalizzata. Ulteriori informazioni [sezione](../action/action.md).

* Se utilizzi Campaign e Journey Optimizer, consulta le sezioni seguenti:

   * [[!DNL Journey Optimizer] e Campaign Classic v7/Campaign v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] e CAMPAIGN STANDARD](../action/acs-action.md)

Per aggiungere un messaggio in un percorso, effettua le seguenti operazioni:

1. Iniziare il percorso con un [Evento](general-events.md) o un [Read Audience](read-audience.md) attività.

1. Dalla sezione **Azioni** nella palette, trascina e rilascia una **email**, un **In-app**, un **SMS** o un **Push** attività nell’area di lavoro.

1. Configura l’attività. Scopri i passaggi dettagliati per creare il contenuto del messaggio nelle pagine seguenti:

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
   <a href="../in-app/create-in-app.md">
   <img alt="Lead" src="../assets/do-not-localize/in-app.jpg">
   </a>
   <div><a href="../in-app/create-in-app.md"><strong>Creare messaggi in-app</strong>
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

## Aggiornare contenuti live{#update-live-content}

Puoi aggiornare il contenuto di un messaggio (e-mail, in-app, push, SMS) in un percorso live.

A questo scopo, apri il percorso live, seleziona l’attività del messaggio e fai clic su **Modifica contenuto**.

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

### Informazioni sull’ottimizzazione dell’ora di invio {#about-send-time}

La funzione di ottimizzazione dell’ora di invio di Adobe Journey Optimizer, basata sui servizi di intelligenza artificiale di Adobe, può prevedere il momento migliore per inviare un’e-mail o un messaggio push per massimizzare il coinvolgimento in base alle percentuali storiche di apertura e clic. Utilizza il nostro modello di apprendimento automatico per pianificare un’ora di invio personalizzata in modo da aumentare le percentuali di apertura e clic sui messaggi da parte di ogni utente.

Il modello di ottimizzazione dell’ora di invio acquisisce i dati Adobe Journey Optimizer e osserva le percentuali di apertura (e-mail e push) e clic (per e-mail) a livello di utente, per determinare quando i clienti hanno più probabilità di interagire con i messaggi. L’ottimizzazione dell’ora di invio richiede almeno un mese di dati di tracciamento dei messaggi per generare consigli informati. Per ogni utente, il sistema sceglierà automaticamente il momento migliore utilizzando i punteggi seguenti:

* L&#39;ora migliore di ogni giorno della settimana per massimizzare il coinvolgimento
* Il miglior giorno della settimana per massimizzare il coinvolgimento
* L&#39;ora migliore del giorno migliore della settimana per massimizzare il coinvolgimento

Il modello varia a seconda che si parli di punteggio o di formazione. La formazione viene condotta inizialmente con cadenza settimanale e quindi trimestrale. Il punteggio è inizialmente settimanale e poi mensile.

* Formazione: sviluppo dell’algoritmo utilizzato per assegnare il punteggio
* Punteggio: applicazione di un punteggio ai singoli profili in base al modello addestrato

Queste informazioni vengono memorizzate con il profilo dell’utente e vi si fa riferimento al momento dell’esecuzione del percorso per indicare a Adobe Journey Optimizer quando inviare il messaggio.

>[!CAUTION]
>
>Questa funzione non è compatibile con la modalità burst.

### Domande frequenti {#faq-send-time}

Quali operazioni può eseguire l’ottimizzazione dell’ora di invio? In che modo gestisce i nuovi profili? Distribuisce l’invio nell’arco di un’ora 6/12/24?

Send-Time Optimization cerca di prevedere il momento migliore per interagire con i clienti e ottimizzare le percentuali di apertura e clic sulle e-mail. Il punteggio è in un formato `3*7*24` attributi per ciascun profilo. Il `7*24` gli attributi descrivono la classificazione del momento migliore previsto per inviare e-mail al destinatario e 3 serve per ottimizzare il tasso di apertura delle e-mail, il tasso di clic e il tasso di apertura push.

Dove posso trovare il tempo di invio previsto per ciascun profilo?

Puoi vedere il punteggio complessivo in **Profili** di rete. Per ciascuno dei tre set di 168 punteggi, la classifica va da -83 a 84. Più alto è il rango, migliore è il momento scelto per interagire con il destinatario. Poiché è possibile definire l&#39;inizio e la durata di un percorso, la classificazione migliore (84) potrebbe non rientrare in tale intervallo di tempo. In questo caso, consigliamo di scegliere un’ora con il valore di classificazione più alto.

Quali rapporti sono disponibili?

Accedi al percorso, fai clic su **Visualizza rapporto** in alto a destra e seleziona il pulsante **Percorso** a sinistra. [Ulteriori informazioni](../reports/journey-global-report.md)

In che modo i dati di ottimizzazione dell’ora di invio influiscono sulla ricchezza del profilo?

L’ottimizzazione dell’ora di invio aggiunge il punteggio/attributi a ciascun profilo, ma non ne viene creato uno nuovo.

### Attivare l’ottimizzazione dell’ora di invio{#activate-send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_email"
>title="Attivare l’ottimizzazione dell’ora di invio"
>abstract="Scegli se effettuare l’ottimizzazione per l’apertura delle e-mail o i click-through delle e-mail selezionando l’opzione appropriata. Puoi anche restringere gli orari di invio utilizzati dal sistema immettendo un valore per l’opzione Invia entro."

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_push"
>title="Attivare l’ottimizzazione dell’ora di invio"
>abstract="Per impostazione predefinita, i messaggi push sono impostati sull’opzione Aperture, in quanto i clic non sono applicabili alla messaggistica push. Puoi anche restringere gli orari di invio utilizzati dal sistema immettendo un valore per l’opzione Invia entro."

Abilitare l’ottimizzazione dell’ora di invio in un messaggio e-mail o push selezionando la **Ottimizzazione dell’ora di invio** passa dai parametri dell’attività.

![](../building-journeys/assets/jo-message5.png)

Per i messaggi e-mail, scegli se ottimizzare all’apertura delle e-mail o ai click-through e-mail selezionando il pulsante di opzione appropriato. I messaggi push hanno per impostazione predefinita l’opzione opens, in quanto i clic non sono applicabili ai messaggi push.

È inoltre possibile scegliere di includere tra parentesi i tempi di invio utilizzati dal sistema immettendo un valore per **Invia entro il prossimo** opzione. Se scegli &quot;sei ore&quot; come valore, [!DNL Journey Optimizer] controllerà ciascun profilo utente e sceglierà il tempo di invio ottimale entro sei ore dal tempo di esecuzione del percorso.

**Cosa succede se il tempo ottimale è fuori dalla finestra?**

Prendiamo un esempio con la seguente configurazione:

* Ottimizza sui clic
* L’azione deve iniziare alle 10
* La finestra è di 3 ore

Un profilo può avere un tempo di apertura ottimale che si trova all’esterno della finestra. Ad esempio, l’apertura ottimale di John al clic è alle 17.

A livello di profilo, ci sono punteggi per ogni ora della settimana. In questo esempio, l’e-mail verrà sempre inviata all’interno della finestra. In fase di esecuzione, il sistema controlla l’elenco dei punteggi all’interno di tale finestra (finestra di 3 ore a partire dalle ore 00:00). Il sistema confronta quindi i punteggi per 10, 11 e mezzogiorno e seleziona il punteggio più alto. L’e-mail viene inviata in tale momento.
