---
product: experience platform
solution: Experience Platform
title: Modello di ottimizzazione personalizzata
description: Ulteriori informazioni sui modelli di ottimizzazione personalizzati
feature: Ranking Formulas
role: User
level: Intermediate
source-git-commit: 3188bc97b8103d2a01101a23d8c242a3e2924f76
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 0%

---

# Modello di ottimizzazione personalizzata {#personalized-optimization-model}

>[!CAUTION]
>
>L’utilizzo di modelli di ottimizzazione personalizzata è attualmente disponibile in fase di accesso anticipato solo per determinati utenti.

## Panoramica {#overview}

Sfruttando le tecnologie all’avanguardia nell’apprendimento automatico controllato e nell’apprendimento profondo, la personalizzazione automatica consente a un utente aziendale (addetto al marketing) di definire gli obiettivi aziendali e di utilizzare i dati dei clienti per addestrare modelli orientati al business al fine di offrire offerte personalizzate e massimizzare i KPI.

## Ipotesi e limitazioni del modello chiave {#key}

Al fine di massimizzare il vantaggio dell’utilizzo della personalizzazione automatica, è necessario tenere presenti alcuni presupposti e limitazioni chiave.

* **Le offerte sono abbastanza diverse in modo che gli utenti avranno preferenze diverse tra le offerte in considerazione**. Se le offerte sono troppo simili, un modello risultante avrà meno impatto in quanto le risposte sono apparentemente casuali.
Ad esempio, se una banca ha due offerte di carte di credito con l&#39;unica differenza di colore, allora potrebbe non avere importanza quale carta è consigliata, ma se ogni carta ha termini diversi, questo fornisce una motivazione per il motivo per cui alcuni clienti ne sceglierebbero una e fornire sufficiente differenza tra le offerte per costruire un modello più incisivo.
* **La composizione del traffico dell&#39;utente è stabile**. Se la composizione del traffico utente cambia drasticamente durante l&#39;addestramento dei modelli e la previsione, le prestazioni del modello potrebbero peggiorare. Ad esempio, supponiamo che nella fase di formazione del modello siano disponibili solo i dati per gli utenti del segmento A, ma il modello addestrato viene utilizzato per generare previsioni per gli utenti del segmento B, quindi le prestazioni del modello potrebbero essere influenzate.
* **Le prestazioni delle offerte non cambiano drasticamente in un breve periodo di tempo** poiché questo modello viene aggiornato settimanalmente, le modifiche alle prestazioni vengono trasmesse man mano che il modello viene aggiornato. Per esempio, un prodotto era molto popolare prima, ma un rapporto pubblico identifica il prodotto come dannoso per la nostra salute, e questo prodotto diventa impopolare molto velocemente. In questo scenario, il modello potrebbe continuare a prevedere questo prodotto fino a quando il modello non si aggiorna con i cambiamenti nel comportamento dell&#39;utente.

## Come funziona {#how}

La personalizzazione automatica apprende interazioni di funzioni complesse tra offerte, informazioni degli utenti e informazioni contestuali per consigliare offerte personalizzate agli utenti finali. Le feature sono input nel modello.

Sono disponibili 3 tipi di funzioni:

| Tipi di funzioni | Come aggiungere funzionalità ai modelli |
|--------------|----------------------------|
| Oggetti di Offer decisioning (placementID, activityID, DecisionScopeID) | Parte dell’Offer decisioning feedback Eventi di esperienza inviati ad AEP |
| Segmenti | Da 0 a 50 segmenti possono essere aggiunti come feature durante la creazione del modello Ranking AI |
| Dati contestuali | Parte dell’Offer decisioning feedback Eventi esperienza inviati ad AEP. Dati contestuali disponibili da aggiungere allo schema: Dettagli commerciali, dettagli canale, dettagli applicazione, dettagli web, dettagli ambiente, dettagli dispositivo, placeContext |

Il modello prevede due fasi:

* In **formazione su modelli offline** un modello viene formato mediante l’apprendimento e la memorizzazione delle interazioni delle funzioni nei dati storici.
* In **deduzione online** Le offerte candidate vengono classificate in base ai punteggi in tempo reale generati dal modello. A differenza delle tradizionali tecniche di filtro collaborativo, che è difficile includere funzionalità per utenti e offerte, la personalizzazione automatica è un metodo di raccomandazione basato sull&#39;apprendimento profondo, ed è in grado di includere e apprendere pattern di interazione con funzioni complesse e non lineari.

Ecco un esempio semplificato per illustrare l’idea di base della personalizzazione automatica. Supponiamo di avere un set di dati che memorizza le interazioni storiche tra utenti e offerte, come mostrato nella Figura 1. Sono disponibili:
* Due offerte, offer_1 e offer_2,
* Due funzioni, feature_1 e feature_2,
* Una colonna di risposta.

Il valore di feature_1, feature_2 e risposta è 0 o 1. Se guardiamo le caselle blu e le caselle arancioni della Figura 1, scopriamo che per offer_1, le risposte sono più probabili 1 quando feature_1 e feature_2 hanno gli stessi valori, mentre per offer_2, le etichette hanno più probabilità di essere 1 quando feature_1 è 0 e feature_2 è 1. Possiamo anche vedere che nella casella rossa, offer_1 viene servito quando feature_1 è 0 e feature_2 è 1 e la risposta è 0. In base al pattern visualizzato nelle caselle arancioni, quando feature_1 è 0 e feature_2 è 1, offer_2 è probabilmente una raccomandazione migliore.

In sostanza, questa è l&#39;idea di imparare e memorizzare le interazioni delle funzioni storiche e di applicarle per generare previsioni personalizzate.

![](../assets/perso-ranking-schema.png)

## Problema di avviamento a freddo {#cold-start}

Il problema dell&#39;avvio a freddo si verifica quando non ci sono abbastanza dati per creare consigli. Per la personalizzazione automatica, esistono due tipi di problemi con avvio a freddo.

* **Dopo aver creato una nuova strategia di classificazione senza dati storici**, le offerte verranno servite in modo casuale per un periodo di tempo per raccogliere i dati e i dati verranno utilizzati per addestrare il primo modello.
* A **Dopo il rilascio del primo modello**, il 10% del traffico totale sarà assegnato per il servizio casuale, mentre il 90% del traffico verrà utilizzato per le raccomandazioni dei modelli. Pertanto, se alla strategia di classificazione venissero aggiunte nuove offerte, queste verrebbero consegnate come parte del 10% del traffico. I dati raccolti su tali offerte determinano il numero di volte in cui vengono selezionati tra il 90% del traffico man mano che il modello continua ad essere aggiornato.

## Riqualificazione {#re-training}

I modelli verranno riformati per apprendere le interazioni più recenti tra le funzioni e attenuare il degrado delle prestazioni del modello settimanalmente.
