---
title: Aggiungere un messaggio in un percorso
description: Aggiungere un messaggio in un percorso
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 4db07a9e-c3dd-4873-8bd9-ac34c860694c
source-git-commit: 51254efaab08a572def118d475dc18f74c9d29b7
workflow-type: tm+mt
source-wordcount: '793'
ht-degree: 6%

---

# Aggiungere un messaggio in un percorso{#add-a-message-in-a-journey}

[!DNL Journey Optimizer] le funzionalità per i messaggi sono integrate e ti basta progettare il contenuto e pubblicare il messaggio. Vedi [questa sezione](../messages/get-started-content.md). Quindi devi semplicemente aggiungere, nel tuo percorso, un messaggio push o e-mail progettato utilizzando Journey Optimizer.

Se utilizzi un sistema di terze parti per l’invio dei messaggi, puoi creare un’azione personalizzata. Ulteriori informazioni [sezione](../action/action.md).

## Aggiungere un’attività Messaggio

1. Come sempre, inizia il tuo percorso con un evento o un **Leggi segmento** attività.

   ![](../assets/jo-message0.png)

1. Da **Azioni** sezione della palette, trascinare un **Messaggio** nell’area di lavoro.

   ![](../assets/jo-message1.png)

1. Aggiungi un’etichetta e una descrizione.

   ![](../assets/jo-message2.png)

1. Fai clic all’interno del **Messaggio** campo . Viene visualizzato l’elenco dei messaggi disponibili progettati in Journey Optimizer. È possibile filtrare l’elenco in base allo stato.

   ![](../assets/jo-message3.png)

1. Scegli un messaggio e fai clic su **Seleziona**. Puoi anche creare un nuovo messaggio direttamente da questa schermata facendo clic su **Creare un messaggio**.

   ![](../assets/jo-message4-ter.png)

   Per controllare il messaggio, puoi fare clic sul pulsante **Apri il messaggio** nella **Messaggio** campo . Il messaggio verrà aperto in una nuova scheda.

   ![](../assets/jo-message4-bis.png)

1. Aggiungi i passaggi successivi al percorso.

## Parametri e-mail e parametri push

La **[!UICONTROL Email parameters]** e **[!UICONTROL Push parameters]** le sezioni mostrano campi di sola lettura. Questa configurazione viene in genere eseguita al momento della creazione del messaggio. Vedi [questa sezione](../messages/get-started-content.md).

![](../assets/jo-message4.png)

Per forzare un valore specifico, puoi utilizzare la funzione **Abilita sostituzione parametro** a destra del campo. Questa opzione può essere utile per vari scopi:

* Ad esempio, per testare un’e-mail, puoi aggiungere il tuo indirizzo e-mail. Dopo aver pubblicato il percorso, l’e-mail ti viene inviata.
* Puoi fare riferimento all’indirizzo e-mail degli abbonati a un elenco. Vedi questo [caso d&#39;uso](message-to-subscribers-uc.md).

## Ottimizzazione dei tempi di invio{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="Informazioni sull’ottimizzazione del tempo inviato"
>abstract="La funzione di ottimizzazione del momento di invio di Adobe Journey Optimizer, basata sui servizi AI di Adobe, può prevedere il momento migliore per inviare un messaggio e-mail o push al fine di massimizzare il coinvolgimento in base alle percentuali di apertura e clic storiche."

La funzione di ottimizzazione del momento di invio di Adobe Journey Optimizer, basata sui servizi AI di Adobe, può prevedere il momento migliore per inviare un messaggio e-mail o push al fine di massimizzare il coinvolgimento in base alle percentuali di apertura e clic storiche. Utilizza il nostro modello di apprendimento automatico per pianificare tempi di invio personalizzati per ogni utente in modo che aumentino le percentuali di apertura e clic dei messaggi.

>[!NOTE]
>
>Al momento questa funzione è disponibile nella versione beta e solo per i clienti beta. Per partecipare al programma beta, contatta l’Assistenza clienti Adobe.

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
>* Questa funzione è disponibile solo per i messaggi mono-canale su e-mail e push con il tracciamento abilitato.
>* Il messaggio deve essere pubblicato.
>* Questa funzione non è compatibile con la modalità burst.


### Attivare l’ottimizzazione del tempo di invio{#activate-send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_email"
>title="Attivare l’ottimizzazione del tempo di invio"
>abstract="Scegli se ottimizzare l’apertura delle e-mail o i click-through delle e-mail selezionando il pulsante di opzione appropriato. Puoi anche scegliere di mettere tra parentesi i tempi di invio utilizzati dal sistema immettendo un valore per l’opzione Invia all’interno dell’opzione successiva."

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_push"
>title="Attivare l’ottimizzazione del tempo di invio"
>abstract="I messaggi push vengono impostati per impostazione predefinita sull’opzione di apertura, in quanto i clic non sono applicabili ai messaggi push. Puoi anche scegliere di mettere tra parentesi i tempi di invio utilizzati dal sistema immettendo un valore per l’opzione Invia all’interno dell’opzione successiva."

Abilita l’ottimizzazione in fase di invio su un messaggio e-mail o push selezionando la **Ottimizzazione dei tempi di invio** dai parametri dell’attività Messaggio .

![](../assets/jo-message5.png)

Per i messaggi e-mail, scegli se ottimizzare le aperture dei messaggi e-mail o i click-through di e-mail selezionando il pulsante di scelta appropriato. I messaggi push vengono impostati per impostazione predefinita sull’opzione di apertura, in quanto i clic non sono applicabili ai messaggi push.

Puoi anche scegliere di applicare una parentesi ai tempi di invio utilizzati dal sistema immettendo un valore per la **Invia all&#39;interno del successivo** opzione . Se si sceglie &quot;sei ore&quot; come valore, [!DNL Journey Optimizer] controllerà ogni profilo utente e sceglierà il tempo di invio ottimale entro sei ore dal tempo di esecuzione del percorso.
