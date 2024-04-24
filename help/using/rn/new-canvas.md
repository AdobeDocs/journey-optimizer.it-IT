---
solution: Journey Optimizer
product: journey optimizer
title: Nuova interfaccia del percorso
feature: Release Notes
topic: Content Management
description: Nuova interfaccia del percorso
hide: true
hidefromtoc: true
exl-id: 03828fca-dde7-4b3b-b890-2c007d1245cc
source-git-commit: f6b9060ed512d6abff37102fa1316b43736bebd5
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 1%

---

# Progettazione Percorsi migliorata {#new-canvas}

>[!CONTEXTUALHELP]
>id="ajo_new_canvas"
>title="Novità"
>abstract="Nuova area di lavoro"

Benvenuti nel designer del percorso migliorato.

Abbiamo sviluppato un **modello di percorso semplificato** che mira a migliorare i processi interni. Anche se questo nuovo modello rappresenta un miglioramento di back-end, il nostro team ha colto l’opportunità per aggiungere funzionalità visibili e vantaggiose per gli utenti di Journey Optimizer:

A **area di lavoro percorso riprogettata** progettato per un’esperienza di interfaccia utente A modernizzata **reportistica live** Interfaccia utente direttamente disponibile nell’area di lavoro del percorso

## Aggiornamenti sul modello di percorso

Il nuovo modello di percorso coesisterà con quello esistente, il che significa che ci saranno percorsi che utilizzano **due modelli diversi**:

* La vecchia, chiamata &quot;v1&quot;
* E la nuova, chiamata &quot;v2&quot;

Tutti i percorsi nella versione 1 rimarranno nella versione 1. Potrai comunque modificarli, testarli o pubblicarli. Tutte le nuove versioni create a partire da una v1 rimarranno anche nella v1. Ci sono **nessuna modifica funzionale** intorno ai percorsi v1.

Come vedi nella schermata seguente, i nodi sono a forma di arrotondamento, che è la vecchia interfaccia utente per i percorsi sul modello v1.

![](assets/new-canvas.png)

Tuttavia, quando **Crea un nuovo percorso** o **duplicare un elemento esistente**, sarà un percorso v2.  Prevediamo di continuare a supportare i percorsi v1 fino a quando la maggior parte dei clienti non sarà trasferita ai percorsi v2.

Esiste un limite al nuovo modello di percorso che **impossibile copiare e incollare attività da un percorso v1 a una v2 e viceversa**. Se desideri eseguire questa operazione, ti consigliamo di duplicare il percorso v1 per renderlo v2 e quindi di copiare le attività.

Nella schermata seguente puoi vedere l’interfaccia utente riprogettata per l’area di lavoro del percorso (disponibile solo con il modello v2):

![](assets/new-canvas2.png)

**A partire da questo momento, qualsiasi nuova funzione aggiunta al designer del percorso (incluso il reporting live) sarà disponibile solo per i percorsi v2.**

## Progettazione dell’area di lavoro del percorso migliorata

Con il nuovo modello di percorso introduciamo un nuovo **Interfaccia utente area di lavoro percorso**, che si inserisce perfettamente nell’ecosistema delle soluzioni e delle app Adobe Experience Cloud, offrendo un’esperienza utente intuitiva ed efficiente. Qualsiasi percorso nello stack v2 si troverà in quella nuova progettazione.

![](assets/new-canvas3.gif)

Le attività saranno ora rappresentate da caselle quadrate con le seguenti funzionalità:

* La prima riga che rappresenta il tipo di attività e che spesso viene sovrascritta da informazioni più contestuali (ad esempio, in Read Audiences, conterrà il nome del pubblico selezionato), o da un’etichetta personalizzata se ne definisci una.
* La seconda riga rappresenta sempre il tipo di attività.

![](assets/new-canvas4.png)

Questa nuova interfaccia utente migliora la leggibilità dell’area di lavoro del percorso fornendo **etichette e tipi di attività più chiari**.

Consente inoltre al team di prodotto di aggiungere più informazioni sull’area di lavoro con un numero inferiore di clic. Un esempio di &quot;ulteriori informazioni&quot; potrebbe essere l’inclusione di rapporti live nell’area di lavoro del percorso, in cui puoi visualizzare i profili che entrano ed escono dalle attività a causa di errori.

![](assets/new-canvas5.png)


## Generazione di rapporti live nell’area di lavoro del percorso

Oltre al design migliorato dell’area di lavoro del percorso, stiamo introducendo la possibilità di vedere **metriche di reporting delle ultime 24 ore** (chiamato &quot;reporting live&quot;) direttamente nell’area di lavoro del percorso.

![](assets/new-canvas6.png)

Con ogni percorso live sul nuovo modello, potrai vedere due tipi di informazioni di reporting &quot;ultime 24 ore&quot;:

* Su un **nuovo inserto**, visualizzerai:
   * Il numero di profili esportati per percorsi attivati dal pubblico. Visualizzerai il numero di profili disponibili nell’ultimo processo di esportazione insieme all’ora in cui è stata effettuata l’esportazione.
   * Il numero di profili che sono usciti dal percorso
   * Percentuale di errori
     ![](assets/new-canvas7.png)
* **Per ogni attività**, visualizzerai il numero di profili che sono entrati in tale attività e il numero di persone che sono uscite a causa di un errore:
  ![](assets/new-canvas8.png)

L’interfaccia utente viene aggiornata automaticamente ogni minuto.

Tieni presente che potrebbero essere presenti differenze tra il numero di profili esportati e il numero di profili che attraversano il percorso. Il conteggio dei profili esportati fornisce solo informazioni sull’ultimo processo di esportazione in corso, mentre il numero di profili che entrano in un’attività contiene solo profili che l’hanno fatto nelle ultime 24 ore. Questo può essere visibile in particolare nei percorsi giornalieri ricorrenti, in quanto potrebbe esserci una sovrapposizione di dati tra due giorni.
