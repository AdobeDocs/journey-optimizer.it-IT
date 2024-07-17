---
product: experience platform
solution: Experience Platform
title: Modelli di ottimizzazione automatica
description: Ulteriori informazioni sui modelli di ottimizzazione automatica
feature: Ranking, Decision Management
role: User
level: Experienced
exl-id: a85de6a9-ece2-43da-8789-e4f8b0e4a0e7
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '1357'
ht-degree: 0%

---

# Modelli di ottimizzazione automatica {#auto-optimization-model}

Un modello di ottimizzazione automatica mira a fornire offerte che massimizzano il rendimento (KPI) impostato dai clienti aziendali. Questi KPI potrebbero essere sotto forma di tassi di conversione, ricavi, ecc. A questo punto, l’ottimizzazione automatica si concentra sull’ottimizzazione dei clic dell’offerta con la conversione dell’offerta come obiettivo. L’ottimizzazione automatica non è personalizzata e viene ottimizzata in base alle prestazioni &quot;globali&quot; delle offerte.

## Limitazioni {#limitations}

L’utilizzo di modelli di ottimizzazione automatica per la gestione delle decisioni è soggetto alle limitazioni seguenti:

* I modelli di ottimizzazione automatica non funzionano con l’API Batch Decisioning.
* Il feedback necessario per creare il modello deve essere inviato come evento esperienza. Non deve essere inviato automaticamente in [!DNL Journey Optimizer] canali.

## Terminologia {#terminology}

I seguenti termini sono utili quando si parla di ottimizzazione automatica:

* **Slot machine**: un approccio all&#39;ottimizzazione [Slot machine](https://en.wikipedia.org/wiki/Multi-armed_bandit){target="_blank"} compensa l&#39;apprendimento esplorativo e il suo sfruttamento.

* **Campionamento di Thompson**: il campionamento di Thompson è un algoritmo per i problemi decisionali online in cui le azioni vengono eseguite in sequenza in modo da bilanciare lo sfruttamento di ciò che è noto per massimizzare le prestazioni immediate e l&#39;investimento di nuove informazioni che possono migliorare le prestazioni future. [Ulteriori informazioni](#thompson-sampling)

* [**Distribuzione Beta**](https://en.wikipedia.org/wiki/Beta_distribution){target="_blank"}: set di [distribuzioni di probabilità](https://en.wikipedia.org/wiki/Probability_distribution){target="_blank"} continue definite nell&#39;intervallo [0, 1] [con parametri](https://en.wikipedia.org/wiki/Statistical_parameter){target="_blank"} da due [parametri forma positivi](https://en.wikipedia.org/wiki/Shape_parameter){target="_blank"}.

## Campionamento di Thompson {#thompson-sampling}

L&#39;algoritmo alla base dell&#39;ottimizzazione automatica è **campionamento di Thompson**. In questa sezione viene descritta l’intuizione alla base del campionamento di Thompson.

Il [campionamento di Thompson](https://en.wikipedia.org/wiki/Thompson_sampling){target="_blank"}, o banditi bayesiani, è un approccio bayesiano al problema della slot machine.  L&#39;idea di base è quella di trattare il ?? di ricompensa medio di ogni offerta come una **variabile casuale** e utilizzare i dati raccolti finora, per aggiornare la nostra &quot;convinzione&quot; sul premio medio. Questa &quot;convinzione&quot; è rappresentata matematicamente da una **distribuzione di probabilità posteriore** - essenzialmente un intervallo di valori per la ricompensa media, insieme alla plausibilità (o probabilità) che la ricompensa abbia quel valore per ogni offerta. Quindi, per ogni decisione, **preleveremo un punto da ciascuna di queste distribuzioni di premi posteriori** e selezioneremo l&#39;offerta con la ricompensa campionata con il valore più alto.

Questo processo è illustrato nella figura seguente, dove sono disponibili 3 diverse offerte. Inizialmente non abbiamo alcuna prova dai dati e supponiamo che tutte le offerte abbiano una distribuzione di ricompensa a posteriori uniforme. Prendiamo un campione dalla distribuzione di ogni offerta di premi a posteriori. Il campione selezionato dalla distribuzione di Offerta 2 ha il valore più alto. Questo è un esempio di **esplorazione**. Dopo aver mostrato l&#39;Offerta 2, raccogliamo qualsiasi potenziale ricompensa (ad esempio conversione/non conversione) e aggiorniamo la distribuzione posteriore dell&#39;Offerta 2 utilizzando il Teorema di Bayes come spiegato di seguito.  Continuiamo questo processo e aggiorniamo le distribuzioni posteriori ogni volta che viene mostrata un’offerta e viene raccolto il premio. Nella seconda figura, viene selezionata l&#39;Offerta 3 - nonostante l&#39;Offerta 1 abbia la più alta ricompensa media (la sua distribuzione di ricompensa posteriore è più a destra), il processo di campionamento da ogni distribuzione ci ha portato a scegliere un&#39;Offerta 3 apparentemente non ottimale. In questo modo, offriamo a noi stessi l&#39;opportunità di conoscere meglio la vera distribuzione delle ricompense offerta 3.

Man mano che vengono raccolti più campioni, l’affidabilità aumenta e si ottiene una stima più accurata del possibile premio (corrispondente a distribuzioni più ridotte). Questo processo di aggiornamento delle nostre convinzioni man mano che diventano disponibili ulteriori prove è noto come **Inferenza bayesiana**.

Alla fine, se un&#39;offerta (ad es. Offerta 1) è un chiaro vincitore, la sua distribuzione successiva della ricompensa sarà separata dagli altri. A questo punto, per ogni decisione, la ricompensa campionata dall’Offerta 1 è probabilmente la più alta e la sceglieremo con una probabilità più elevata. Si tratta di **sfruttamento**. Siamo convinti che l&#39;offerta 1 sia la migliore e quindi viene scelta per massimizzare i premi.

![](../assets/ai-ranking-thompson-sampling.png)

**Figura 1**: *Per ogni decisione, campioniamo un punto dalle distribuzioni di premi posteriori. Verrà scelta l’offerta con il valore di esempio più alto (tasso di conversione). Nella fase iniziale, tutte le offerte hanno una distribuzione uniforme, in quanto non disponiamo di alcuna evidenza sui tassi di conversione delle offerte dai dati. Mentre raccogliamo più campioni, le distribuzioni posteriori diventano più strette e più precise. In ultima analisi, l&#39;offerta con il tasso di conversione più alto verrà scelta ogni volta.*

<!--
![](../assets/ai-ranking-thompson-sampling-initial.png)
![](../assets/ai-ranking-thompson-sampling-intermediate.png)
![](../assets/ai-ranking-thompson-sampling-ultimate.png)
-->

+++**Dettagli tecnici**

Per calcolare/aggiornare le distribuzioni, si utilizza **Teorema di Bayes**. Per ogni offerta ***i***, vogliamo calcolare la loro ***P(??i | dati)***, ovvero per ogni offerta ***i***, quanto è probabile un valore di ricompensa **??i**, dati i dati raccolti finora per tale offerta.

Dal Teorema Di Bayes:

***Posteriore = Probabilità * Precedente***

La **probabilità precedente** è la stima iniziale della probabilità di produzione di un output. La probabilità, dopo aver raccolto alcune prove, è nota come **probabilità posteriore**. 

L’ottimizzazione automatica è progettata per prendere in considerazione i premi binari (clic/nessun clic). In questo caso, la probabilità rappresenta il numero di successi da N prove ed è modellata da una **distribuzione binomiale**. Per alcune funzioni di verosimiglianza, se si sceglie una certa distribuzione a priori, la distribuzione a posteriori finisce per essere nella stessa distribuzione della distribuzione a priori. Tale priore è chiamato **priore coniugato**. Questo tipo di distribuzione a priori rende il calcolo della distribuzione a posteriori molto semplice. La **distribuzione Beta** è coniugata prima della probabilità binomiale (premi binari), quindi è una scelta comoda e ragionevole per le distribuzioni di probabilità precedenti e posteriori. La distribuzione Beta prende due parametri, ***α*** e ***β***. Questi parametri possono essere considerati come il conteggio dei successi e degli errori e il valore medio dato da:

![](../assets/ai-ranking-beta-distribution.png)

La funzione Likelihood, come spiegato in precedenza, è modellata da una distribuzione binomiale, con s successi (conversioni) e f errori (nessuna conversione) e q è una [variabile casuale](https://en.wikipedia.org/wiki/Random_variable){target="_blank"} con una [distribuzione beta](https://en.wikipedia.org/wiki/Beta_distribution){target="_blank"}.

La distribuzione a priori è modellata dalla distribuzione Beta e la distribuzione a posteriori assume la seguente forma:

![](../assets/ai-ranking-posterior-distribution.svg)

La parte posteriore viene calcolata semplicemente aggiungendo il numero di successi ed errori ai parametri esistenti ***α***, ***β***.

Per l&#39;ottimizzazione automatica, come mostrato nell&#39;esempio precedente, si inizia con una distribuzione precedente ***Beta(1, 1)*** (distribuzione uniforme) per tutte le offerte e dopo aver ottenuto s successi e f errori per una determinata offerta, la distribuzione posteriore diventa una distribuzione Beta con parametri ***(s+α, f+β)*** per tale offerta.
+++

**Argomenti correlati**:

Per un approfondimento sul campionamento di Thompson, leggi i seguenti articoli di ricerca:
* [Valutazione empirica del campionamento di Thompson](https://proceedings.neurips.cc/paper/2011/file/e53a0a2978c28872a4505bdb51db06dc-Paper.pdf){target="_blank"}
* [Analisi del campionamento di Thompson per il problema di slot machine](https://proceedings.mlr.press/v23/agrawal12/agrawal12.pdf){target="_blank"}

## Problema di avviamento a freddo {#cold-start}

Il problema di &quot;avviamento a freddo&quot; si verifica quando una nuova offerta viene aggiunta a una campagna e non sono disponibili dati sul tasso di conversione della nuova offerta. Durante questo periodo, dovremo elaborare una strategia che indichi la frequenza con cui questa nuova offerta viene scelta in modo da ridurre al minimo il calo delle prestazioni, mentre raccoglieremo informazioni sul tasso di conversione di questa nuova offerta. Sono disponibili diverse soluzioni per affrontare questo problema. La chiave è trovare un equilibrio tra l&#39;esplorazione di questa nuova offerta, mentre non sacrifichiamo molto lo sfruttamento. Attualmente utilizziamo la &quot;distribuzione uniforme&quot; come stima iniziale del tasso di conversione della nuova offerta (distribuzione precedente). In sostanza, tutti i valori del tasso di conversione hanno la stessa probabilità di verificarsi.


![](../assets/ai-ranking-cold-start-strategies.png)

**Figura 2**: *Considera una campagna con 3 offerte. Durante la pubblicazione della campagna, alla campagna viene aggiunta l’Offerta 4. Inizialmente non disponiamo di dati sul tasso di conversione dell’Offerta 4 e dobbiamo affrontare il problema dell’avviamento a freddo. Utilizziamo la distribuzione uniforme come ipotesi iniziale sul tasso di conversione dell’offerta 4, mentre raccogliamo i dati per questa nuova offerta. Come spiegato nella sezione [Campionamento di Thompson](#thompson-sampling), per scegliere quale offerta verrà mostrata a un utente, campioniamo punti dalle distribuzioni di premi posteriori delle offerte e selezioniamo l&#39;offerta con il valore di esempio più alto. Nell&#39;esempio precedente, l&#39;Offerta 4 viene scelta e successivamente in base alla ricompensa raccolta, la distribuzione posteriore di questa offerta viene aggiornata come spiegato nella sezione [Campionamento di Thompson](#thompson-sampling).*

## Misurazione dell’incremento {#lift}

&quot;Incremento&quot; è la metrica utilizzata per misurare le prestazioni di qualsiasi strategia implementata nel servizio di classificazione, rispetto alla strategia di base (serving delle offerte solo in modo casuale).

Ad esempio, se siamo interessati a misurare le prestazioni di una strategia di campionamento di Thompson (TS) utilizzata nel servizio di classificazione e il KPI è il tasso di conversione (CVR), l’&quot;incremento&quot; della strategia TS rispetto alla strategia di base è definito come segue:

![](../assets/ai-ranking-lift.png)
