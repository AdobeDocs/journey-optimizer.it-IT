---
product: experience platform
solution: Experience Platform
title: Modelli di ottimizzazione automatica
description: Ulteriori informazioni sui modelli di ottimizzazione automatica
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: a85de6a9-ece2-43da-8789-e4f8b0e4a0e7
source-git-commit: c530905eacbdf6161f6449d7a0b39c8afaf3a321
workflow-type: tm+mt
source-wordcount: '1377'
ht-degree: 0%

---

# Modelli di ottimizzazione automatica {#auto-optimization-model}

Un modello di ottimizzazione automatica mira a fornire offerte che massimizzano il rendimento (KPI) impostato dai clienti aziendali. Questi KPI possono essere sotto forma di tassi di conversione, ricavi, ecc. A questo punto, l’ottimizzazione automatica si concentra sull’ottimizzazione dei clic delle offerte con la conversione delle offerte come target. L’ottimizzazione automatica non è personalizzata e si ottimizza in base alle prestazioni &quot;globali&quot; delle offerte.

## Limitazioni {#limitations}

L’utilizzo dei modelli di ottimizzazione automatica per la gestione delle decisioni è soggetto alle limitazioni seguenti:

* I modelli di ottimizzazione automatica non funzionano con l’API di Decisioning in batch.
* Il feedback necessario per creare il modello deve essere inviato come evento di esperienza. Non deve essere inviato automaticamente in [!DNL Journey Optimizer] canali.

## Terminologia {#terminology}

I seguenti termini sono utili quando si parla di ottimizzazione automatica:

* **Bandit multi-armata**: A [slot machine](https://en.wikipedia.org/wiki/Multi-armed_bandit)L&#39;approccio all&#39;ottimizzazione {target=&quot;_blank&quot;} compensa l&#39;apprendimento esplorativo e lo sfruttamento di tale apprendimento.

* **campionamento di Thomson**: il campionamento di Thompson è un algoritmo per i problemi decisionali online in cui le azioni vengono intraprese in sequenza in modo da bilanciare lo sfruttamento di ciò che è noto per massimizzare le prestazioni immediate e l’investimento per accumulare nuove informazioni che possono migliorare le prestazioni future. [Ulteriori informazioni](#thompson-sampling)

* [**Distribuzione beta**](https://en.wikipedia.org/wiki/Beta_distribution){target=&quot;_blank&quot;}: Serie continua [distribuzioni delle probabilità](https://en.wikipedia.org/wiki/Probability_distribution){target=&quot;_blank&quot;} definito nell&#39;intervallo [0, 1] [parametrizzato](https://en.wikipedia.org/wiki/Statistical_parameter){target=&quot;_blank&quot;} da due positivo [parametri della forma](https://en.wikipedia.org/wiki/Shape_parameter){target=&quot;_blank&quot;}.

## Campionamento di Thompson {#thompson-sampling}

L’algoritmo alla base dell’ottimizzazione automatica è **Campionamento di Thompson**. In questa sezione viene illustrato l’intuizione alla base del campionamento di Thompson.

[Campionamento di Thompson](https://en.wikipedia.org/wiki/Thompson_sampling){target=&quot;_blank&quot;}, o banditi bayesiani, è un approccio bayesiano al problema della slot machine.  L&#39;idea di base è trattare la ricompensa media? da ogni offerta come **variabile casuale** e utilizzare i dati raccolti finora, per aggiornare la nostra &quot;convinzione&quot; sulla ricompensa media. Questa &quot;credenza&quot; è rappresentata matematicamente da un **distribuzione della probabilità posteriore** - essenzialmente una gamma di valori per la ricompensa media, insieme alla plausibilità (o probabilità) che la ricompensa ha quel valore per ogni offerta. Allora, per ogni decisione, **campionare un punto da ciascuna di queste distribuzioni di ricompensa posteriori** e seleziona l’offerta il cui premio campione aveva il valore più alto.

Questo processo è illustrato nella figura seguente, dove abbiamo 3 diverse offerte. Inizialmente non abbiamo alcuna prova dai dati e supponiamo che tutte le offerte abbiano una distribuzione uniforme di ricompensa posteriore. Disegniamo un campione dalla distribuzione della ricompensa posteriore di ogni offerta. Il campione selezionato nella distribuzione dell&#39;offerta 2 ha il valore più alto. Questo è un esempio di **esplorazione**. Dopo aver mostrato l&#39;Offerta 2, raccogliamo ogni potenziale premio (per esempio conversione/no-conversione) e aggiorniamo la distribuzione posteriore dell&#39;Offerta 2 utilizzando il Teorema Bayes come spiegato di seguito.  Continuiamo questo processo e aggiorniamo le distribuzioni posteriori ogni volta che viene mostrata un&#39;offerta e viene raccolto il premio. Nella seconda figura, l&#39;offerta 3 è selezionata - nonostante l&#39;offerta 1 abbia il premio medio più alto (la sua distribuzione di ricompensa posteriore è più a destra), il processo di campionamento da ogni distribuzione ci ha portato a scegliere un&#39;offerta apparentemente non ottimale 3. In questo modo ci offriamo l’opportunità di saperne di più sulla distribuzione della ricompensa effettiva dell’offerta 3.

Man mano che vengono raccolti più campioni, l&#39;affidabilità aumenta e si ottiene una stima più accurata del possibile premio (corrispondente a distribuzioni di ricompense più ristrette). Questo processo di aggiornamento delle nostre convinzioni man mano che più prove diventano disponibili è noto come **Inferenza bayesiana**.

Alla fine, se un&#39;offerta (ad es. offerta 1) è un chiaro vincitore, la sua distribuzione di ricompensa posteriore sarà separata dagli altri. A questo punto, per ogni decisione, la ricompensa campionata dall&#39;offerta 1 è probabilmente la più alta, e la sceglieremo con una probabilità più alta. Questo è **sfruttamento** - abbiamo una forte convinzione che l&#39;offerta 1 sia la migliore, e quindi viene scelta per massimizzare i premi.

![](../assets/ai-ranking-thompson-sampling.png)

**Figura 1**: *Per ogni decisione, campioniamo un punto dalla distribuzione della ricompensa posteriore. Verrà selezionata l’offerta con il valore di campione più alto (tasso di conversione). Nella fase iniziale, tutte le offerte hanno una distribuzione uniforme in quanto non abbiamo alcuna prova dei tassi di conversione delle offerte dai dati. Man mano che raccogliamo più campioni, le distribuzioni posteriori diventano più strette e accurate. Infine, l&#39;offerta con il più alto tasso di conversione sarà scelta ogni volta.*

<!--
![](../assets/ai-ranking-thompson-sampling-initial.png)
![](../assets/ai-ranking-thompson-sampling-intermediate.png)
![](../assets/ai-ranking-thompson-sampling-ultimate.png)
-->

+++**Dettagli tecnici**

Per calcolare/aggiornare le distribuzioni, utilizziamo **Teorema di Bayes**. Per ogni offerta ***i***, vogliamo calcolare il loro ***P(??i | dati)***, vale a dire per ogni offerta ***i***, la probabilità che un valore di premio **?** , dati i dati raccolti finora per tale offerta.

Da Bayes Theorem:

***Posteriore = Probabilità * Precedente***

La **probabilità precedente** è la stima iniziale della probabilità di produrre un output. La probabilità, dopo la raccolta di alcune prove, è nota come **probabilità posteriore**. 

L&#39;ottimizzazione automatica è progettata per considerare premi binari (clic/senza clic). In questo caso, la probabilità rappresenta il numero di successi ottenuti da N prove ed è modellata da un **Distribuzione binomica**. Per alcune funzioni di probabilità, se si sceglie un certo precedente, il posteriore finisce per essere nella stessa distribuzione del precedente. Tale precedente allora è chiamato un **coniugare prima**. Questo tipo di precedente rende il calcolo della distribuzione posteriore molto semplice. La **Distribuzione beta** è un coniugato prima della probabilità binomiale (premi binari), e così è una scelta conveniente e ragionevole per le distribuzioni di probabilità precedenti e posteriori.La distribuzione Beta prende due parametri, ***α*** e ***β***. Questi parametri possono essere pensati come il conteggio dei successi e degli errori e il valore medio dato da:

![](../assets/ai-ranking-beta-distribution.png)

La funzione di probabilità, come spiegato sopra, è modellata da una distribuzione Binomiale, con i suoi successi (conversioni) e i suoi fallimenti (no-conversioni) e q è un [variabile casuale](https://en.wikipedia.org/wiki/Random_variable){target=&quot;_blank&quot;} con un [distribuzione beta](https://en.wikipedia.org/wiki/Beta_distribution){target=&quot;_blank&quot;}.

Il precedente è modellato dalla distribuzione Beta e la distribuzione posteriore assume la seguente forma:

![](../assets/ai-ranking-posterior-distribution.svg)

Il posteriore viene calcolato semplicemente aggiungendo il numero di successi e guasti ai parametri esistenti ***α***, ***β***.

Per l’ottimizzazione automatica, come mostrato nell’esempio precedente, viene avviata una distribuzione precedente ***Beta(1, 1)*** (distribuzione uniforme) per tutte le offerte e dopo aver ottenuto i suoi successi e i suoi fallimenti per una determinata offerta, il posteriore diventa una distribuzione beta con parametri ***(s+α, f+β)*** per quell&#39;offerta.
+++

**Argomenti correlati**:

Per un&#39;immersione più approfondita sul campionamento di Thompson, leggi i seguenti documenti di ricerca:
* [Valutazione empirica del campionamento di Thompson](https://proceedings.neurips.cc/paper/2011/file/e53a0a2978c28872a4505bdb51db06dc-Paper.pdf){target=&quot;_blank&quot;}
* [Analisi del campionamento di Thompson per il problema del slot machine](http://proceedings.mlr.press/v23/agrawal12/agrawal12.pdf){target=&quot;_blank&quot;}

## Problema di avviamento a freddo {#cold-start}

Il problema &quot;Avvio a freddo&quot; si verifica quando una nuova offerta viene aggiunta a una campagna e non sono disponibili dati sul tasso di conversione della nuova offerta. Durante questo periodo, dobbiamo elaborare una strategia per quanto spesso viene scelta questa nuova offerta in modo da ridurre al minimo il calo delle prestazioni, mentre raccogliamo informazioni sul tasso di conversione di questa nuova offerta. Ci sono diverse soluzioni disponibili per affrontare questo problema. La chiave è trovare un equilibrio tra l&#39;esplorazione di questa nuova offerta mentre non sacrifichiamo molto lo sfruttamento. Attualmente utilizziamo la &quot;distribuzione uniforme&quot; come stima iniziale del tasso di conversione della nuova offerta (distribuzione precedente). In sostanza, diamo a tutti i valori del tasso di conversione uguale probabilità di occorrenza.


![](../assets/ai-ranking-cold-start-strategies.png)

**Figura 2**: *Considera una campagna con 3 offerte. Mentre la campagna è attiva, l’offerta 4 viene aggiunta alla campagna. Inizialmente non disponiamo di dati sul tasso di conversione dell&#39;offerta 4 e dobbiamo affrontare il problema dell&#39;avviamento a freddo. Utilizziamo la distribuzione uniforme come stima iniziale del tasso di conversione dell&#39;offerta 4, mentre raccogliamo i dati per questa nuova offerta. Come spiegato nel [Campionamento di Thompson](#thompson-sampling) sezione, per scegliere quale offerta verrà mostrata a un utente, campioniamo i punti dalle distribuzioni dei premi posteriori delle offerte e selezioniamo l&#39;offerta con il valore di campione più alto. Nell&#39;esempio precedente, l&#39;offerta 4 viene scelta e successivamente basata sulla ricompensa raccolta, la distribuzione posteriore di questa offerta viene aggiornata come spiegato nel [Campionamento di Thompson](#thompson-sampling) sezione .*

## Misurazione dell’incremento {#lift}

&quot;Incremento&quot; è la metrica utilizzata per misurare le prestazioni di qualsiasi strategia implementata in un servizio di classificazione, rispetto alla strategia di base (servizio offerte in modo casuale).

Ad esempio, se siamo interessati a misurare le prestazioni di una strategia di campionamento di Thompson (TS) utilizzata nel servizio di classificazione e il KPI è il tasso di conversione (CVR), l’&quot;incremento&quot; della strategia TS rispetto alla strategia di base è definito come:

![](../assets/ai-ranking-lift.png)
