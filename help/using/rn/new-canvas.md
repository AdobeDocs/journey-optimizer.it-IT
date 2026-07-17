---
solution: Journey Optimizer
product: journey optimizer
title: Nuova interfaccia del percorso
feature: Release Notes
topic: Content Management
description: Scopri il nuovo modello di percorso semplificato, la nuova interfaccia utente dell’area di lavoro di percorso e il reporting live introdotto per i percorsi Journey Optimizer.
keywords: area di lavoro percorso, nuovo modello percorso, reportistica live, progettista percorso
role: User
level: Beginner, Intermediate
hide: true
exl-id: 03828fca-dde7-4b3b-b890-2c007d1245cc
TQID: https://experienceleague.adobe.com/-QKSnBRN9yPYEq5ay9wD-uf4lLduJqmtlFWDnLYt1gk
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2: id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 1f2a71d3323b6a64b346a83aa58b23aed035eb29
workflow-type: tm+mt
source-wordcount: 727
ht-degree: 1%

---

# Ti diamo il benvenuto nel Journey Designer migliorato {#new-canvas}

[!DNL Journey Optimizer] offre ora un **modello di percorso semplificato** che mira a migliorare l&#39;esperienza utente e i processi interni. A partire dalla versione di aprile, potrai beneficiare delle seguenti funzionalità:

* **area di lavoro di percorso riprogettata** per un&#39;esperienza dell&#39;interfaccia utente modernizzata
* Un&#39;interfaccia utente di **reportistica in tempo reale** direttamente disponibile nell&#39;area di lavoro del percorso

>[!NOTE]
>
>Tieni presente che il rollout di questa funzione sarà progressivo. Potresti non vedere le modifiche immediatamente.

Per ulteriori informazioni sulla creazione di percorsi nella nuova area di lavoro, vedere [utilizzo della finestra di progettazione dei percorsi](../building-journeys/using-the-journey-designer.md#canvas-capabilities).

## Aggiornamenti sul modello di percorso {#updates-journey-model}

Il nuovo modello di percorso coesisterà con quello esistente, il che significa che ci saranno percorsi che utilizzano **due modelli diversi**:

* Il modello legacy
* Il nuovo modello

Tutti i percorsi del modello legacy rimarranno al suo interno. Potrai comunque modificarli, testarli o pubblicarli. Vi rimarrà anche qualsiasi nuova versione creata da un percorso sul modello legacy. **nessuna modifica funzionale** in questi percorsi.

Come vedi nella schermata seguente, i nodi sono a forma di arrotondamento, che è la vecchia interfaccia utente per i percorsi del modello legacy.

![Area di lavoro di percorso legacy con nodi di attività a forma rotonda per AirportBeacon e Email, connessa in un semplice flusso orizzontale](assets/new-canvas.png)

Tuttavia, quando **crei un nuovo percorso** o **ne duplichi uno esistente**, questo si troverà nel nuovo modello. I percorsi del modello precedente continueranno a essere supportati fino a quando la maggior parte dei clienti non sarà trasferita a quello nuovo.

Esiste un limite al nuovo modello di percorso; **non sarà possibile copiare e incollare le attività dal modello legacy a quello nuovo e viceversa**. Se desideri eseguire questa operazione, ti consigliamo di duplicare il percorso legacy per passare al nuovo modello e quindi copiare le attività.

Nella schermata seguente puoi visualizzare l’interfaccia utente riprogettata per l’area di lavoro del percorso (disponibile solo con il nuovo modello):

![Area di lavoro percorso riprogettata che mostra le caselle di attività quadrate (membri fedeltà leggono il pubblico, condizione) che si diramano nelle attività e-mail di benvenuto e messaggi di Slack](assets/new-canvas2.png)

**A partire da questo momento tutte le nuove funzionalità aggiunte alla finestra di progettazione del percorso (incluso il reporting in tempo reale) saranno disponibili solo per i percorsi del nuovo modello.**

## Progettazione dell’area di lavoro del percorso migliorata {#improved-canvas-design}

Con il nuovo modello di percorso, verrà introdotta una nuova e migliorata interfaccia utente **dell&#39;area di lavoro di percorso**, che si inserisce perfettamente nelle soluzioni [!DNL Adobe CX Enterprise] e nell&#39;ecosistema dell&#39;app, offrendo un&#39;esperienza utente intuitiva ed efficiente. Tutti i percorsi del nuovo modello saranno su quel nuovo design.

![Dimostrazione animata della nuova struttura dell&#39;area di lavoro del percorso, con un percorso con Start, un&#39;attività Read-Audience membri fedeltà e nodi End](assets/new-canvas3.gif)

Le attività saranno ora rappresentate da caselle quadrate con le seguenti funzionalità:

* La prima riga rappresenta il tipo di attività che spesso viene sovrascritto da informazioni più contestuali (in Read Audiences, contiene il nome del pubblico selezionato) o da un’etichetta personalizzata, se ne definisci una.
* La seconda riga rappresenta sempre il tipo di attività.

![Casella attività che mostra l&#39;etichetta dell&#39;attività &quot;Membri fedeltà&quot; sulla prima riga e il tipo di attività &quot;Read audience&quot; sulla seconda riga](assets/new-canvas4.png)

Questa nuova interfaccia utente migliora la leggibilità dell&#39;area di lavoro del percorso fornendo **etichette e tipi di attività più chiari**.

Consente inoltre al team di prodotto di aggiungere più informazioni sull’area di lavoro con un numero inferiore di clic. Un esempio di &quot;ulteriori informazioni&quot; potrebbe essere l’inclusione di rapporti live nell’area di lavoro del percorso, in cui puoi visualizzare i profili che entrano ed escono dalle attività a causa di errori.

![Riquadro attività con metriche di reporting live che mostrano 56 profili immessi e 0 errori per l&#39;attività Membri fedeltà](assets/new-canvas5.png)

## Generazione di rapporti live nell’area di lavoro del percorso {#live-reporting-canvas}

Oltre al layout migliorato dell&#39;area di lavoro di percorso, è stata introdotta una nuova funzionalità per consentire agli utenti di visualizzare le metriche di reporting in tempo reale a partire dalle **ultime 24 ore**, denominata reporting live, direttamente nell&#39;area di lavoro di percorso. Completa il rapporto live di [ percorso esistente](../reports/journey-live-report.md).

Per ogni attività all’interno di ogni percorso live che utilizza il nuovo modello, puoi accedere a:


* Il numero di profili che entrano in questa attività.
* Numero di profili che escono da questa attività a causa di un errore.

![L&#39;area di lavoro del percorso live mostra i conteggi di errori e immessi per ogni attività, inclusi i profili di test, la condizione e più azioni personalizzate di Slack in percorsi diversi](assets/new-canvas6bis.png)

<!--
`
With every live journey on the new model, you will be able to see two types of "last 24 hours" reporting information:

* On a **new insert**, you will see:
    * The number of profiles that have been exported for audience-triggered journeys. You will see the number of profiles available in the last export job alongside the time when that export has been made.
    * The number of profiles who exited the journey
    * The percentage of errors
    ![](assets/new-canvas7.png)
* **On each activity**, you will see the number of profiles who entered that activity and the number who exited because of an error:
    ![](assets/new-canvas8.png)
-->
<!--
Please note that you may see differences between the number of exported profiles and the number of profiles flowing through the journey. The exported profiles count only provides information about the last export job being made while the number of profiles entering an activity only contains profiles who did it in the last 24 hours. This can especially be visible on recurring daily journeys as there could be a data overlap between two days.
-->
