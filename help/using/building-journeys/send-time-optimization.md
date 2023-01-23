---
solution: Journey Optimizer
product: journey optimizer
title: Ottimizzazione dell’ora di invio
description: Scopri come impostare i parametri per l’ottimizzazione del tempo di invio nei messaggi
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: tempo di invio, invio, messaggio, ottimizzazione, percorso, AI, Intelligente
exl-id: ec604e91-4c7f-459c-b6ff-d825919e7181
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 1%

---

# Ottimizzazione dei tempi di invio{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="Informazioni sull’ottimizzazione del tempo inviato"
>abstract="La funzione di ottimizzazione del momento di invio di Adobe Journey Optimizer, basata sui servizi AI di Adobe, può prevedere il momento migliore per inviare un messaggio e-mail o push al fine di massimizzare il coinvolgimento in base alle percentuali di apertura e clic storiche."

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

## Attivare l’ottimizzazione del tempo di invio{#activate-send-time-optimization}

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
