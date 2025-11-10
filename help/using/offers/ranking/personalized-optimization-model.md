---
product: experience platform
solution: Experience Platform
title: Modello di ottimizzazione personalizzata
description: Ulteriori informazioni sui modelli di ottimizzazione personalizzati
badge: label="Legacy" type="Informative"
feature: Ranking, Decision Management
role: User
level: Experienced
exl-id: c73b3092-e96d-4957-88e6-500e99542782
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '944'
ht-degree: 5%

---

# Modello di ottimizzazione personalizzata {#personalized-optimization-model}

## Panoramica {#overview}

Sfruttando le tecnologie all’avanguardia di machine learning supervisionato e di deep learning, l’ottimizzazione personalizzata consente a un utente aziendale (marketer) di definire gli obiettivi aziendali e utilizza i dati della clientela per addestrare modelli orientati al business per offerte personalizzate e ottimizzazione dei KPI.

![](../../rn/assets/do-not-localize/ai-ranking.gif)

## Requisiti del set di dati

Per addestrare un modello di ottimizzazione personalizzato, il set di dati deve soddisfare i seguenti requisiti minimi:

* Almeno 2 offerte nel set di dati devono avere almeno 250 eventi di visualizzazione e 25 eventi di successo (ad esempio, clic o conversioni) negli ultimi 30 giorni.
* Le offerte con meno di 250 visualizzazioni e/o 25 eventi di successo negli ultimi 30 giorni possono essere incluse nel traffico personalizzato, ma vengono considerate dal modello di personalizzazione come eseguite al livello dell’offerta con il punteggio peggiore * fino al superamento di questa soglia.
* Le offerte con meno di 250 visualizzazioni e/o 25 eventi di successo negli ultimi 30 giorni rimarranno idonee per l’inclusione nel traffico di esplorazione.

Fino alla prima volta che viene addestrato un modello di ottimizzazione personalizzato, le offerte all’interno di una strategia di selezione che utilizza un modello di ottimizzazione personalizzato verranno servite a caso.

## Principali ipotesi e limitazioni del modello {#key}

Per massimizzare il vantaggio dell’utilizzo dell’ottimizzazione personalizzata, è necessario conoscere alcuni presupposti e limitazioni chiave.

* **Le offerte sono sufficientemente diverse, cosicché gli utenti avranno preferenze diverse tra le offerte considerate**. Se le offerte sono troppo simili, un modello risultante avrà un impatto minore in quanto le risposte sono apparentemente casuali.
Ad esempio, se una banca dispone di due offerte di carte di credito con l’unica differenza rappresentata dal colore, potrebbe non avere importanza quale carta sia consigliata, ma se ogni carta dispone di termini diversi, ciò fornisce una motivazione per spiegare perché alcuni clienti ne sceglierebbero una e fornisce una differenza sufficiente tra le offerte per costruire un modello più incisivo.
* **La composizione del traffico utente è stabile**. Se la composizione del traffico dell’utente cambia drasticamente durante l’apprendimento e la previsione del modello, le prestazioni del modello potrebbero peggiorare. Ad esempio, supponiamo che nella fase di apprendimento del modello siano disponibili solo i dati per gli utenti nel pubblico A, ma che il modello addestrato venga utilizzato per generare previsioni per gli utenti nel pubblico B, e che le prestazioni del modello possano esserne influenzate.
* **Le prestazioni delle offerte non cambiano drasticamente in un breve periodo di tempo** poiché questo modello viene aggiornato ogni settimana e le modifiche alle prestazioni vengono trasmesse man mano che il modello viene aggiornato. Ad esempio, un prodotto era molto popolare in precedenza, ma un rapporto pubblico identifica il prodotto come dannoso per la nostra salute, e questo prodotto diventa impopolare estremamente veloce. In questo scenario, il modello potrebbe continuare a prevedere questo prodotto fino a quando il modello non si aggiorna con le modifiche nel comportamento dell’utente.

## Come funziona {#how}

Il modello apprende interazioni complesse tra le funzioni di offerte, informazioni sugli utenti e informazioni contestuali per consigliare offerte personalizzate agli utenti finali. Le feature sono input nel modello.

Esistono 3 tipi di funzionalità:

| Tipi di funzionalità | Come aggiungere feature ai modelli |
|--------------|----------------------------|
| Oggetti decisioning (placementID, activityID, decisionScopeID) | Parte del feedback di gestione delle decisioni Eventi di esperienza inviati ad AEP |
| Tipi di pubblico | È possibile aggiungere 0-50 tipi di pubblico come funzioni durante la creazione del modello di IA per la classificazione |
| Dati contestuali | Parte del feedback decisionale Eventi di esperienza inviati ad AEP. Dati contestuali disponibili da aggiungere allo schema: Dettagli Commerce, Dettagli canale, Dettagli applicazione, Dettagli web, Dettagli ambiente, Dettagli dispositivo, placeContext |

Il modello prevede due fasi:

* Nella fase **apprendimento del modello offline**, un modello viene addestrato apprendendo e memorizzando le interazioni delle funzionalità nei dati storici.
* Nella fase di **inferenza online**, le offerte candidate vengono classificate in base ai punteggi in tempo reale generati dal modello. A differenza delle tecniche di filtro collaborativo tradizionali, che è difficile includere funzioni per utenti e offerte, l’ottimizzazione personalizzata è un metodo di raccomandazione basato sull’apprendimento profondo ed è in grado di includere e imparare pattern di interazione di funzioni complessi e non lineari.

Di seguito è riportato un esempio semplificato per illustrare l’idea di base dietro l’ottimizzazione personalizzata. Supponiamo di avere un set di dati in cui sono memorizzate le interazioni storiche tra utenti e offerte, come illustrato nella Figura 1. Sono disponibili:

* Due offerte, offer_1 e offer_2,
* Due feature, feature_1 e feature_2,
* Una colonna di risposta.

Il valore di feature_1, feature_2 e risposta è 0 o 1. Osservando le caselle blu e arancione della Figura 1, si può notare che per offer_1, le risposte sono più probabili quando feature_1 e feature_2 hanno gli stessi valori, mentre per offer_2, le etichette hanno più probabilità di essere 1 quando feature_1 è 0 e feature_2 è 1. Nella casella rossa, viene inoltre visualizzato offer_1 quando feature_1 è 0 e feature_2 è 1 e la risposta è 0. In base alla serie visualizzata nelle caselle arancioni, quando feature_1 è 0 e feature_2 è 1, offer_2 è probabilmente un consiglio migliore.

Fondamentalmente, questa è l&#39;idea di imparare e memorizzare interazioni storiche delle funzioni e di applicarle per generare previsioni personalizzate.

![](../assets/perso-ranking-schema.png)

## Problema di avviamento a freddo {#cold-start}

Il problema di avvio a freddo si verifica quando non ci sono abbastanza dati per creare un consiglio. Per l’ottimizzazione personalizzata, esistono due tipi di problemi con avviamento a freddo.

* **Dopo aver creato un nuovo modello di IA senza dati storici**, le offerte verranno distribuite in modo casuale per un periodo di tempo per la raccolta dei dati e i dati verranno utilizzati per addestrare il primo modello.
* **Dopo il rilascio del primo modello**, il 10% del traffico totale verrà allocato per la distribuzione casuale, mentre il 90% del traffico verrà utilizzato per le raccomandazioni sui modelli. Pertanto, se al modello di IA fossero aggiunte nuove offerte, queste verrebbero consegnate come parte del 10% del traffico. I dati raccolti su tali offerte determinano il numero di volte in cui viene selezionato tra il 90% del traffico mentre il modello continua a essere aggiornato.

## Riaddestramento {#re-training}

I modelli verranno riaddestrati per scoprire le ultime interazioni delle funzioni e attenuare il deterioramento settimanale delle prestazioni del modello.
