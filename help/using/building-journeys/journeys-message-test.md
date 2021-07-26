---
title: Aggiungere un messaggio in un percorso
description: Aggiungere un messaggio in un percorso
feature: Percorsi
topic: Gestione dei contenuti
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 3530a600a4c842ff99bc23354b2d158c6d41f902
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 3%

---


# Aggiungere un messaggio in un percorso

[!DNL Journey Optimizer] le funzionalità per i messaggi sono integrate e ti basta progettare il contenuto e pubblicare il messaggio. Vedi [questa sezione](../get-started-content.md). Quindi devi semplicemente aggiungere, nel tuo percorso, un messaggio push o e-mail progettato utilizzando Journey Optimizer.

Se utilizzi un sistema di terze parti per l’invio dei messaggi, puoi creare un’azione personalizzata. Ulteriori informazioni in questa sezione [sezione](../action/action.md).

## Aggiunta di un’attività Messaggio

1. Come sempre, inizia il percorso con un evento o un&#39;attività **Leggi segmento** .

   ![](../assets/jo-message0.png)

1. Dalla sezione **Azioni** della palette, trascina e rilascia un’attività **Messaggio** nell’area di lavoro.

   ![](../assets/jo-message1.png)

1. Aggiungi un’etichetta e una descrizione.

   ![](../assets/jo-message2.png)

1. Fare clic all&#39;interno del campo **Messaggio**. Viene visualizzato l’elenco dei messaggi disponibili progettati in Journey Optimizer. È possibile filtrare l’elenco in base allo stato.

   ![](../assets/jo-message3.png)

1. Scegli un messaggio e fai clic su **Seleziona**. Puoi anche creare un nuovo messaggio direttamente da questa schermata facendo clic su **Crea messaggio**.

   ![](../assets/jo-message4-ter.png)

   Per controllare il messaggio, fai clic sull&#39;icona **Apri il messaggio** nel campo **Messaggio** . Il messaggio verrà aperto in una nuova scheda.

   ![](../assets/jo-message4-bis.png)

1. Aggiungi i passaggi successivi al percorso.

## Parametri e-mail e parametri push

Le sezioni **[!UICONTROL Email parameters]** e **[!UICONTROL Push parameters]** mostrano campi di sola lettura. Questa configurazione viene in genere eseguita al momento della creazione del messaggio. Vedi [questa sezione](../get-started-content.md).

![](../assets/jo-message4.png)

Per forzare un valore specifico, puoi utilizzare l&#39;icona **Abilita sostituzione parametro** a destra del campo. Questa opzione può essere utile a scopo di test. Ad esempio, per un’e-mail, puoi aggiungere il tuo indirizzo e-mail. Dopo aver pubblicato il percorso, l’e-mail ti viene inviata.

## Ottimizzazione del tempo di invio{#send-time-optimization}

### Informazioni sull’ottimizzazione del tempo inviato{#about-send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="Informazioni sull’ottimizzazione del tempo inviato"
>abstract="La funzione di ottimizzazione del momento di invio di Adobe Journey Optimizer, basata sui servizi AI di Adobe, può prevedere il momento migliore per inviare un messaggio e-mail o push al fine di massimizzare il coinvolgimento in base alle percentuali di apertura e clic storiche."

La funzione di ottimizzazione del momento di invio di Adobe Journey Optimizer, basata sui servizi AI di Adobe, può prevedere il momento migliore per inviare un messaggio e-mail o push al fine di massimizzare il coinvolgimento in base alle percentuali di apertura e clic storiche. Utilizza il nostro modello di apprendimento automatico per pianificare tempi di invio personalizzati per ogni utente in modo che aumentino le percentuali di apertura e clic dei messaggi.

Il modello di ottimizzazione del momento di invio acquisisce i dati di Adobe Journey Optimizer ed esamina le percentuali di apertura a livello di utente (per e-mail e push) e di clic (per e-mail) per determinare quando è più probabile che i clienti interagiscano con i tuoi messaggi. Per formulare raccomandazioni informate, l’ottimizzazione in fase di invio richiede almeno un mese di dati di tracciamento dei messaggi. Per ogni utente, il modello genera i seguenti dati predittivi:

* L&#39;ora migliore di ogni giorno della settimana per massimizzare il coinvolgimento
* Il giorno migliore della settimana per massimizzare il coinvolgimento
* L&#39;ora migliore del giorno migliore della settimana per massimizzare il coinvolgimento

Il modello varia a seconda che si tratti di punteggio o formazione. L&#39;addestramento viene effettuato inizialmente settimanalmente e poi trimestralmente. Il punteggio è inizialmente settimanale e poi mensile.

* Formazione: lo sviluppo dell’algoritmo utilizzato per ottenere il punteggio
* Punteggio: applicazione di un punteggio a singoli profili in base al modello addestrato

Queste informazioni vengono memorizzate con il profilo dell’utente e a cui si fa riferimento durante l’esecuzione del percorso per indicare a Adobe Journey Optimizer quando inviare il messaggio.

## Note importanti{#send-time-optimization-notes}

* Questa funzione è disponibile solo per i messaggi mono-canale su e-mail e push con il tracciamento abilitato.
* Il messaggio deve essere pubblicato.
* Questa funzione non è compatibile con la modalità burst.

## Attiva ottimizzazione del tempo inviato{#activate-send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_email"
>title="Attiva ottimizzazione del tempo inviato"
>abstract="Scegli se ottimizzare l’apertura delle e-mail o i click-through delle e-mail selezionando il pulsante di opzione appropriato. Puoi anche scegliere di mettere tra parentesi i tempi di invio utilizzati dal sistema immettendo un valore per l’opzione Invia all’interno dell’opzione successiva."

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_push"
>title="Attiva ottimizzazione del tempo inviato"
>abstract="I messaggi push vengono impostati per impostazione predefinita sull’opzione di apertura, in quanto i clic non sono applicabili ai messaggi push. Puoi anche scegliere di mettere tra parentesi i tempi di invio utilizzati dal sistema immettendo un valore per l’opzione Invia all’interno dell’opzione successiva."

Abilita l’ottimizzazione del tempo di invio su un messaggio e-mail o push selezionando l’opzione **Ottimizzazione del tempo di invio** dai parametri dell’attività Messaggio .

![](../assets/jo-message5.png)

Per i messaggi e-mail, scegli se ottimizzare le aperture dei messaggi e-mail o i click-through di e-mail selezionando il pulsante di scelta appropriato. I messaggi push vengono impostati per impostazione predefinita sull’opzione di apertura, in quanto i clic non sono applicabili ai messaggi push.

Puoi anche scegliere di mettere tra parentesi i tempi di invio utilizzati dal sistema immettendo un valore per l’ **Invia all’interno dell’opzione successiva**. Se selezioni &quot;sei ore&quot; come valore, Adobe Journey Optimizer controllerà ogni profilo utente per vedere se il tempo di invio ottimale si verifica entro sei ore dal tempo di esecuzione del percorso e seleziona il tempo determinato per l’ottimizzazione del tempo di invio. Se l’orario non è compreso nelle sei ore successive, per impostazione predefinita Adobe Journey Optimizer invierà il messaggio al momento dell’esecuzione del percorso.
