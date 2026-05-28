---
solution: Journey Optimizer
product: Journey Optimizer
title: Modelli di ottimizzazione automatica
description: Ulteriori informazioni sui modelli di ottimizzazione automatica
feature: Ranking, Decisioning
role: User
level: Experienced
exl-id: 8a8b66cb-dd96-4373-bbe0-a67e0dc0b2c0
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/HC3N8cjiZQQTfyt2Z0hKU3M-OUTw4y9REDnBIBXsJ9Q
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 1763
ht-degree: 0%

---

# Modelli di ottimizzazione automatica {#auto-optimization-model}

Il modello di ottimizzazione automatica di [!DNL Adobe Journey Optimizer] è un modello di apprendimento di rinforzo che massimizza il tasso di click-through delle offerte esplorando tutte le offerte (o i contenuti), quindi classificando gli elementi in base al CTR previsto, dopo l&#39;applicazione delle regole di idoneità e dei limiti di frequenza.

## Casi d’uso e vantaggi {#use-cases-benefits}

L’ottimizzazione automatica può essere utilizzata in qualsiasi momento desideri una configurazione rapida e semplice, trovare offerte vincenti complessive e massimizzare i clic sulle offerte all’interno di un singolo canale. Ad esempio:

* Scegli le offerte migliori da inserire in una pagina web per massimizzare i clic sulle offerte.
* Scegli le offerte migliori da inserire in un’e-mail per massimizzare i clic sulle offerte.
* Scegli le offerte migliori da inserire nella schermata di un’app mobile per massimizzare i clic sulle offerte.

L’ottimizzazione automatica è una buona scelta quando:

* Le offerte cambiano nel tempo o di frequente: il modello di ottimizzazione automatica viene riqualificato ogni sei ore.

## Requisiti e limitazioni {#requirements-limitations}

L’ottimizzazione automatica presenta i seguenti requisiti e limiti:

* L’ottimizzazione automatica richiede un set di dati di formazione contenente eventi di visualizzazione dell’offerta, eventi di clic dell’offerta e il gruppo di campi Evento esperienza - Interazioni proposta.
* I modelli di ottimizzazione automatica non possono essere utilizzati nelle richieste all’API Batch Decisioning.
* L’ottimizzazione automatica ottimizza sempre in base ai clic dell’offerta. Per massimizzare per un obiettivo diverso dai clic sulle offerte, utilizza il modello [Ottimizzazione personalizzata](personalized-optimization-model.md).
* L’ottimizzazione automatica cerca di trovare offerte complessivamente vincenti e non trova una classificazione personalizzata per ciascun cliente. Per trovare classificazioni personalizzate per ogni cliente, utilizza il modello [Ottimizzazione personalizzata](personalized-optimization-model.md).

Per addestrare un modello di ottimizzazione automatica, il set di dati deve soddisfare i seguenti requisiti minimi:

* Almeno 2 offerte nel set di dati devono avere almeno 100 eventi di visualizzazione e 5 eventi di clic negli ultimi 14 giorni.
* Le offerte con meno di 100 visualizzazioni e/o 5 eventi di clic negli ultimi 14 giorni verranno trattate dal modello come nuove offerte e saranno idonee solo per essere servite dal team di esplorazione.
* Le offerte con più di 100 display e 5 eventi di clic negli ultimi 14 giorni verranno trattate dal modello come offerte esistenti e potranno essere servite da banditi sia di esplorazione che di sfruttamento.

Fino alla prima volta che viene addestrato un modello di ottimizzazione automatica, le offerte all’interno di una strategia di selezione che utilizza un modello di ottimizzazione automatica verranno servite a caso.

## Bilanciamento dell’ottimizzazione con l’apprendimento {#balancing-optimization-learning}

L&#39;ottimizzazione automatica è un modello di [apprendimento per rinforzi](https://en.wikipedia.org/wiki/Reinforcement_learning){target="_blank"} che apprende le prestazioni di click-through delle offerte in base al comportamento reale dei clienti. I modelli di apprendimento per il rafforzamento cercano di massimizzare un obiettivo scegliendo azioni con risultati migliori. Tuttavia, un modello che presentasse sempre a ogni cliente gli elementi con il miglior risultato previsto non apprenderebbe mai le prestazioni dei nuovi elementi introdotti nel tempo (il cosiddetto &quot;problema dell’avviamento a freddo&quot;), né le variazioni delle prestazioni di altri elementi esistenti derivanti da cambiamenti nel comportamento dei clienti nel tempo. I modelli di apprendimento per rinforzo devono quindi gestire quello che viene comunemente definito [compromesso tra esplorazione e sfruttamento](https://en.wikipedia.org/wiki/Exploration%E2%80%93exploitation_dilemma){target="_blank"}, ovvero l&#39;ottimizzazione del bilanciamento con l&#39;apprendimento.

L&#39;ottimizzazione automatica utilizza un approccio comune denominato [slot machine](https://en.wikipedia.org/wiki/Multi-armed_bandit){target="_blank"} per gestire il compromesso. La banca multiarmata prende decisioni di classificazione sulla base di:

* il tasso di click-through previsto per ciascun elemento
* le differenze nel tasso di click-through previsto per ogni elemento
* il grado di incertezza del modello sulle previsioni per ciascun elemento.

I banditi multiarmati utilizzano queste informazioni, insieme alla variabilità casuale, per scegliere le azioni da intraprendere. L&#39;ottimizzazione automatica è un [algoritmo di insieme](https://en.wikipedia.org/wiki/Ensemble_learning){target="_blank"} che contiene più banditi multiarmati per garantire che tutte le offerte siano adeguatamente esplorate e massimizzare le prestazioni complessive.

Quando risponde a una richiesta di classificazione, un bandit multi-armato &quot;supervisore&quot; fa prima una scelta se questa richiesta dovrebbe essere tendenziosa verso l&#39;esplorazione o tendente allo sfruttamento. Questa decisione viene presa usando un approccio &quot;epsilon-greedy&quot;.

Il secondo livello di classificazione viene eseguito da uno dei due [banditi di campionamento Thompson](https://en.wikipedia.org/wiki/Thompson_sampling){target="_blank"}:

* Il 10% del traffico viene allocato a una slot machine incentrata sull’esplorazione che ha maggiori probabilità di consigliare nuove offerte o quelle con dati limitati, partendo dal presupposto che il modello trarrebbe vantaggio dall’apprendere di più sul comportamento del cliente in risposta a tali offerte.
* Il 90% del traffico è allocato a una banca incentrata sullo sfruttamento che ha maggiori probabilità di consigliare costantemente offerte ad alte prestazioni nel tempo, partendo dal presupposto che le offerte nuove o a basso contenuto di dati abbiano maggiori probabilità di ottenere prestazioni inferiori, fino a prova contraria.

In senso tecnico, queste ipotesi sono parametri della distribuzione di probabilità precedente, anche denominati [precedenti](https://en.wikipedia.org/wiki/Prior_probability){target="_blank"}. Man mano che le offerte raccolgono più dati di visualizzazione e di clic, l&#39;influenza dei priori scelti diventa più bassa e le previsioni fatte dai due banditi tendono a convergere nel tempo.

Il nostro approccio che prevede la combinazione di più banditi e l’allocazione di parte del traffico dedicato per l’esplorazione offre diversi vantaggi:

* il modello viene a conoscenza più rapidamente delle offerte più recenti con il minor numero di dati
* il modello continua a conoscere tutte le offerte e risponde ai cambiamenti nel comportamento dei clienti nel tempo
* il modello non si adatta eccessivamente favorendo aggressivamente le offerte con CTR apparente più elevato ma poche osservazioni, o sfavorendo aggressivamente le offerte con CTR apparente più basso ma poche osservazioni
* il modello è affidabile per gestire le decisioni di allocazione del traffico tra centinaia di offerte con dati di clic sparsi e con quantità molto diverse di dati storici

## Campionamento di Thompson {#thompson-sampling}

[Il campionamento di Thompson](https://en.wikipedia.org/wiki/Thompson_sampling){target="_blank"}, o banditi bayesiani, è un approccio bayesiano al problema della slot machine. Il modello considera il premio medio 𝛍 di ogni offerta come una variabile casuale e utilizza i dati raccolti finora per aggiornare le nostre &quot;convinzioni&quot; sul premio medio. Questa &quot;convinzione&quot; è rappresentata matematicamente da una distribuzione di probabilità posteriore - essenzialmente un intervallo di valori per la ricompensa media, insieme alla plausibilità (o probabilità) che la ricompensa abbia quel valore per ogni offerta. Quindi, per ogni decisione, campioneremo un punto da ciascuna di queste distribuzioni di premi posteriori e selezioneremo l&#39;offerta la cui ricompensa campionata aveva il valore più alto.

Questo processo è illustrato nella figura seguente, dove sono disponibili 3 diverse offerte. Inizialmente non abbiamo alcuna prova dai dati, e supponiamo che tutte le offerte abbiano una distribuzione di ricompensa a posteriori uniforme. Prendiamo un campione dalla distribuzione di ogni offerta di premi a posteriori. Il campione selezionato dalla distribuzione di Offerta 2 ha il valore più alto. Questo è un esempio di esplorazione. Dopo aver mostrato l&#39;Offerta 2, raccogliamo qualsiasi potenziale ricompensa (ad esempio conversione/non conversione) e aggiorniamo la distribuzione posteriore dell&#39;Offerta 2 utilizzando il Teorema di Bayes come spiegato di seguito. Continuiamo questo processo e aggiorniamo le distribuzioni posteriori ogni volta che viene mostrata un’offerta e viene raccolto il premio. Nella seconda figura, viene selezionata l&#39;Offerta 3 - nonostante l&#39;Offerta 1 abbia la più alta ricompensa media (la sua distribuzione di ricompensa posteriore è più a destra), il processo di campionamento da ogni distribuzione ci ha portato a scegliere un&#39;Offerta 3 apparentemente non ottimale. In questo modo, ci offriamo l&#39;opportunità di conoscere meglio la vera distribuzione delle ricompense dell&#39;Offerta 3.

Man mano che vengono raccolti più campioni, l’affidabilità aumenta e si ottiene una stima più accurata del possibile premio (corrispondente a distribuzioni più ridotte). Questo processo di aggiornamento delle nostre convinzioni man mano che diventano disponibili ulteriori prove è noto come **Inferenza bayesiana**.

Alla fine, se un&#39;offerta (ad es. Offerta 1) è un chiaro vincitore, la sua distribuzione successiva della ricompensa sarà separata dagli altri. A questo punto, per ogni decisione, la ricompensa campionata dall’Offerta 1 è probabilmente la più alta e la sceglieremo con una probabilità più elevata. Siamo convinti che l&#39;Offerta 1 sia la migliore, e quindi viene scelta per massimizzare i premi.

![](../assets/ai-ranking-thompson-sampling.png)

**Figura 1**: *Per ogni decisione, campioniamo un punto dalle distribuzioni di premi posteriori. Verrà scelta l’offerta con il valore di esempio più alto (tasso di conversione). Nella fase iniziale, tutte le offerte hanno una distribuzione uniforme, in quanto non disponiamo di alcuna evidenza sui tassi di conversione delle offerte dai dati. Mentre raccogliamo più campioni, le distribuzioni posteriori diventano più strette e più precise. In ultima analisi, l&#39;offerta con il tasso di conversione più alto verrà scelta ogni volta.*

+++ Dettagli di calcolo

Per calcolare/aggiornare le distribuzioni, si utilizza il Teorema di **Bayes**. Per ogni offerta ***i***, vogliamo calcolare la loro ***P(𝛍i | data)***, ovvero per ogni offerta ***i***, quanto è probabile un valore di ricompensa&#x200B;**𝛍 i**, dati i dati raccolti finora per tale offerta.

Dal Teorema Di Bayes:

***Posteriore = Probabilità * Precedente***

La **probabilità precedente** è la stima iniziale della probabilità di produzione di un output. La probabilità, dopo aver raccolto alcune prove, è nota come **probabilità posteriore**.

L’ottimizzazione automatica è progettata per prendere in considerazione i premi binari (clic/nessun clic). In questo caso, la probabilità rappresenta il numero di successi da N studi ed è modellata da una distribuzione binomiale. Per alcune funzioni di verosimiglianza, se si sceglie una certa distribuzione a priori, la distribuzione a posteriori finisce per essere nella stessa distribuzione della distribuzione a priori. Tale priore è chiamato **priore coniugato**. Questo tipo di distribuzione a priori rende il calcolo della distribuzione a posteriori molto semplice. La [distribuzione Beta](https://en.wikipedia.org/wiki/Beta_distribution){target="_blank"} è coniugata prima della probabilità binomiale (premi binari) e quindi è una scelta conveniente e ragionevole per le distribuzioni di probabilità precedenti e posteriori. La distribuzione Beta accetta due parametri, ***α*** e ***β***. Questi parametri possono essere considerati come il conteggio dei successi e degli errori e il valore medio dato da:

![](../assets/ai-ranking-beta-distribution.png)

La funzione Likelihood come spiegato in precedenza è modellata da una distribuzione binomiale, con s successi (conversioni) e f fallimenti (nessuna conversione) e q è una variabile casuale con una distribuzione Beta.

La distribuzione a priori è modellata dalla distribuzione Beta e la distribuzione a posteriori assume la seguente forma:

![](../assets/ai-ranking-posterior-distribution.svg)

+++

### Pregiudizio per l&#39;esplorazione e pregiudizio per lo sfruttamento {#exploration-exploitation-bias}

È necessario scegliere un valore iniziale per i parametri ***α***, ***β***. L&#39;ottimizzazione automatica include sia un modulo di campionamento Thompson basato sull&#39;esplorazione che un modulo di campionamento Thompson basato sull&#39;utilizzo che utilizzano diversi moduli iniziali ***α***, ***β*** nelle loro distribuzioni beta.

In un approccio di campionamento generale di Thompson, la parte posteriore viene calcolata semplicemente aggiungendo il numero di successi ed errori ai parametri esistenti ***α***, ***β***. L’ottimizzazione automatica utilizza diversi fattori di ponderazione per i nuovi successi e gli errori nel modificare l’impatto dei nuovi dati rispetto ai dati precedenti sia nei bit orientati all’esplorazione che in quelli orientati allo sfruttamento.

## Riferimenti {#references}

Per informazioni più approfondite sui banditi di campionamento di Thompson, consulta i seguenti articoli di ricerca:

* [Valutazione empirica del campionamento di Thompson](https://proceedings.neurips.cc/paper/2011/file/e53a0a2978c28872a4505bdb51db06dc-Paper.pdf){target="_blank"}
* [Analisi del campionamento di Thompson per il problema della slot machine](https://proceedings.mlr.press/v23/agrawal12/agrawal12.pdf){target="_blank"}
