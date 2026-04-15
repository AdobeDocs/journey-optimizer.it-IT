---
solution: Journey Optimizer
product: Journey Optimizer
title: Monitoraggio del modello di IA
description: Monitorare l’integrità, lo stato e le prestazioni del modello di classificazione AI per i modelli di ottimizzazione personalizzati
feature: Ranking, Decisioning
topic: Artificial Intelligence
role: User
level: Intermediate
version: Journey Orchestration
exl-id: 90e71c42-94f3-4cc5-bd6e-1df29def4d39
source-git-commit: 110c4c9b12b085f3febb83f799f5fd0ba8a8b1fb
workflow-type: tm+mt
source-wordcount: '1432'
ht-degree: 2%

---

# Monitorare i modelli AI {#ai-model-observability}

Che tu sia un addetto al marketing, un data scientist o un amministratore delle decisioni, comprendere le prestazioni e il comportamento dei modelli di ottimizzazione personalizzati ti aiuta a selezionare le offerte migliori per ogni cliente che utilizza l’intelligenza artificiale.

A questo scopo, puoi monitorare lo stato, lo stato di formazione e l&#39;evoluzione dei tuoi modelli di intelligenza artificiale direttamente in [!DNL Journey Optimizer].

In questo modo puoi vedere chiaramente se il modello funziona, quando è stato addestrato per l&#39;ultima volta, cosa è successo durante la formazione, come sta determinando il tuo risultato di business (ad esempio, conversioni o ricavi) e come risolvere i problemi quando non funziona<!-- (for example, unexpected decision item count, training data date range, or insufficient events)-->.

>[!AVAILABILITY]
>
>Attualmente questa funzionalità è supportata solo per i modelli [personalized optimization](personalized-optimization-model.md).

➡️ [Scopri questa funzione nel video](#video)

## Visualizza lo stato del corso di formazione {#from-ai-model-list}

Una volta impostato il modello come live, questo entra in un ciclo di vita continuo: i dati vengono raccolti e il modello viene riaddestrato periodicamente per ottimizzare la classificazione delle offerte. Puoi controllare lo stato di apprendimento dei modelli di ottimizzazione personalizzati nell’elenco dei modelli di intelligenza artificiale.

1. Vai a **[!UICONTROL Decisioning]** > **[!UICONTROL Configurazione strategia]** > **[!UICONTROL Modelli AI]** per aprire l&#39;inventario dei modelli AI.

1. Puoi visualizzare tutti i modelli AI disponibili e il loro stato.

1. Per ogni modello di IA **[!UICONTROL Live]** del tipo di ottimizzazione personalizzato, due colonne ti consentono di visualizzare:
   * quando è stato eseguito l&#39;ultimo processo di apprendimento (**[!UICONTROL Ultimo apprendimento]**) e
   * se ciascun modello è stato addestrato correttamente o meno (**[!UICONTROL Risultato del training]**).

   ![](../assets/ai-model-list-training.png)

   Questo consente di identificare rapidamente i modelli che necessitano di ulteriori indagini o risoluzione dei problemi.

## Accedere a un rapporto sullo stato del modello {#access-ai-model-details}

Dall’elenco, fai clic su un modello di IA per l’ottimizzazione personalizzata. Da qui puoi visualizzare gli elementi elencati di seguito:

* **[!UICONTROL Modello attualmente distribuito]** - Questa sezione mostra il modello attualmente distribuito, la data di distribuzione, l&#39;intervallo di dati utilizzato, il numero di elementi decisionali (offerte) inclusi e personalizzati e l&#39;allocazione del traffico corrente tra i sottomodelli<!-- (random exploration, new offer booster?, contextual bandit, neural network)-->.

  ![](../assets/ai-model-deployed-model.png)

  In questo esempio, il modello è stato addestrato su cinque elementi decisionali e il relativo traffico è sufficiente per sviluppare previsioni personalizzate per tre elementi decisionali. I due elementi di decisione rimanenti vengono serviti a caso.

  Puoi anche vedere che il modello sta attualmente allocando il 40% del traffico alla rete neurale personalizzata, il 40% del traffico alla banda contestuale e il 20% del traffico all’esplorazione casuale.

* **[!UICONTROL Ultimo processo di formazione]** - In questa sezione viene visualizzato lo stato dell&#39;ultimo processo di formazione, la data di esecuzione e gli eventuali messaggi di errore. [Ulteriori informazioni sugli stati di errore](#check-for-error-states)

  ![](../assets/ai-model-last-training-job.png)

  In questo esempio, puoi osservare che il modello distribuito corrisponde al processo di formazione previsto.

* **[!UICONTROL Proprietà]** - Questa sezione mostra le proprietà del modello, ad esempio il set di dati utilizzato, la metrica di ottimizzazione e i tipi di pubblico utilizzati per addestrare il modello di ottimizzazione personalizzato.

  ![](../assets/ai-model-properties.png)

  Fai clic su **[!UICONTROL Modifica proprietà]** per modificare questi elementi. Verrai reindirizzato alla schermata Crea modello di intelligenza artificiale. [Ulteriori informazioni](create-ai-models.md)

* **[!DNL Model performance]** - Questa sezione mostra le prestazioni di ogni braccio del modello nel tempo, ad esempio l&#39;allocazione del traffico e il tasso di conversione per ogni sottomodello. Puoi passare da **ultimi 7 giorni** agli **ultimi 30 giorni**. L’incremento e la rilevanza statistica sono gli indicatori chiave per stabilire se il modello stia effettivamente migliorando i risultati di marketing.

  ![](../assets/ai-model-performance.png)

  In questo esempio, puoi notare che negli ultimi 30 giorni i modelli secondari personalizzati hanno generato un aumento del tasso di conversione di oltre il 60%, un incremento statisticamente significativo, il che significa che questo modello di intelligenza artificiale sta generando un impatto sulla tua azienda.

* **[!UICONTROL Allocazione del traffico del modello nel tempo]** - In questa sezione viene illustrata l&#39;evoluzione del modello nel tempo. Quando un modello viene distribuito per la prima volta, il 100% del traffico è casuale, perché non sono ancora stati raccolti dati di offerta. Dopo la prima riqualificazione, il traffico di solito si sposta verso le braccia personalizzate.

  ![](../assets/ai-model-trafic-allocation.png)

  In questo esempio, puoi vedere che l’allocazione del traffico è passata dall’esplorazione casuale al 100% alla rete neurale e al traffico di slot contestuale, in quanto il modello è stato riqualificato nel tempo.

## Comprendere gli errori di apprendimento {#check-for-error-states}

Per visualizzare i dettagli dell’errore relativo a un modello di IA per l’ottimizzazione personalizzata il cui ultimo processo di apprendimento non è riuscito, effettua le seguenti operazioni.

1. Fate clic sul modello nell&#39;elenco. Vengono visualizzati i dettagli dello stato del modello.

   ![](../assets/ai-model-no-model-deployed.png){width="95%"}

   In questo esempio, puoi vedere che non viene distribuito alcun modello perché l’ultimo processo di apprendimento non è riuscito.

   >[!NOTE]
   >
   >Quando non viene distribuito alcun modello, le richieste di decisione vengono distribuite utilizzando l’allocazione casuale uniforme del traffico.

1. Scopri i dettagli dell’errore nella sezione **[!UICONTROL Ultimo processo di apprendimento]**.

   ![](../assets/ai-model-training-job-failed.png){width="70%"}

   Un processo di formazione in genere ha esito negativo se non sono presenti eventi di feedback nel set di dati selezionato per questo modello. Ciò significa che devi compilare il set di dati o selezionare un nuovo set di dati con gli eventi di conversione appropriati.

1. Puoi controllare quale set di dati è selezionato nelle **[!UICONTROL Proprietà]** del modello. Fai clic su **[!UICONTROL Modifica proprietà]** per selezionare un altro set di dati. [Ulteriori informazioni](create-ai-models.md)

   ![](../assets/ai-model-properties-edit-dataset.png){align="center" width="45%"}

## Domande frequenti {#faq}

+++ Quali modelli AI è possibile monitorare?

Il monitoraggio del modello di IA è attualmente supportato solo per [modelli di ottimizzazione personalizzati](personalized-optimization-model.md). Altri tipi di modello di classificazione non espongono ancora il rapporto sullo stato del modello.
+++

+++ Perché il processo di formazione del mio modello non è riuscito?

I processi di formazione spesso non vanno a buon fine quando il set di dati selezionato per il modello non ha eventi di feedback o ne ha solo pochi (conversione). Controlla la sezione **[!UICONTROL Ultimo processo di apprendimento]** per i dettagli dell&#39;errore, quindi controlla le **[!UICONTROL proprietà]** del modello per confermare il set di dati e la metrica di ottimizzazione. Popola il set di dati con gli eventi giusti o [seleziona un set di dati diverso](create-ai-models.md) con i dati di conversione appropriati.
+++

+++ In che modo il monitoraggio del modello di intelligenza artificiale si relaziona ai rapporti di campagna e percorso?

Il monitoraggio del modello di IA è diverso dal reporting di campagne o percorsi. Un singolo modello di IA può essere utilizzato in più campagne o più percorsi e i rapporti delle campagne o dei percorsi non mostrano quale modello è stato utilizzato per una determinata consegna. Utilizza il monitoraggio dello stato del modello di intelligenza artificiale per comprendere e monitorare il modello stesso; utilizza [rapporti sulle campagne](../../reports/campaign-global-report-cja.md) e [rapporti sui percorsi](../../reports/journey-global-report-cja.md) per le metriche a livello di consegna.
+++

+++ La mia metrica di ottimizzazione è una metrica continua come ricavi o valore dell’ordine, non una metrica binaria come clic o conversioni. Come si interpretano i valori delle conversioni e del tasso di conversione riportati?

Quando si utilizza una metrica continua come ricavi o valore dell’ordine, il modello tenta di prevedere il valore stimato associato alla presentazione di una determinata offerta (non la probabilità di conversione). Il valore &quot;Conversioni&quot; riportato è il ricavo totale (o valore dell’ordine) associato alle visualizzazioni dell’offerta registrata per ciascun braccio del modello. Il &quot;Tasso di conversione&quot; riportato è il valore di Conversioni diviso per il valore Visualizzazioni e può superare il 100% in caso di metrica continua.
+++

+++ Cos’è il significato di incremento?

La significatività dell’incremento è la significatività statistica dell’incremento riportato rispetto all’esplorazione casuale. La significatività è calcolata utilizzando un test del chi quadrato delle differenze di proporzione, che fornisce un risultato identico al calcolo della significatività di un test Z per due proporzioni di popolazione.
+++

+++ Qual è il modello indice Gini? Cos’è un valore &quot;buono&quot; dell’indice Gini?

L&#39;indice di Gini del modello (noto anche come coefficiente di Gini) è una misura offline della potenza predittiva di un modello. L’indice Gini del modello va da 0 (nessuna potenza predittiva) a 1 (prevede perfettamente il valore di conversione o metrica per ogni offerta per ogni cliente). Non esiste un valore universale di indice Gini &quot;buono&quot;, in quanto diversi casi di utilizzo del processo decisionale determinano un comportamento dell’utente diverso e quindi risultati di modello diversi. Nello stesso caso d’uso, valori più alti dell’indice Gini indicano un modello di qualità superiore.
+++

+++ Come viene calcolato l’indice Gini?

L’indice Gini per ciascun braccio del modello viene calcolato in modo diverso a seconda che la metrica di ottimizzazione sia binaria o continua:

**Metrica di ottimizzazione binaria** (ad es. clic, ordini): l&#39;indice Gini viene calcolato in base all&#39;area sotto la curva (AUC) della curva delle caratteristiche di funzionamento del ricevitore (ROC), normalmente indicata come AUC del ROC o semplicemente AUC in breve. L’AUC del ROC varia da 0,5 (modello casuale con potenza predittiva pari a zero) a 1,0 (potenza predittiva perfetta). L’AUC della ROC viene convertita in un indice Gini utilizzando la formula Gini = 2 x (AUC della ROC) - 1.

**Metrica di ottimizzazione continua** (ad es. ricavi, valore ordine): l&#39;indice Gini viene calcolato in base all&#39;area sotto la curva di Lorenz associata ai positivi previsti cumulativi del modello rispetto ai veri positivi cumulativi nella popolazione. L&#39;area sotto la curva di Lorenz varia da 0,0 (potenza predittiva perfetta) a 0,5 (modello casuale con potenza predittiva pari a zero). L&#39;AUC di Lorenz viene convertita in un indice di Gini usando la formula Gini = 1 - 2 x (AUC di Lorenz).
+++

+++ Qual è una misura migliore della qualità del modello: indice di Gini o significatività di incremento/incremento?

In genere, le misure online della qualità del modello, come l&#39;incremento e la rilevanza dell&#39;incremento, sono considerate il metodo &quot;gold standard&quot; per misurare la qualità del modello. Gli indici Gini forniscono un punto dati aggiuntivo per i team di customer data science che valutano modelli decisionali.
+++

<!--
## Understanding statuses and errors {#statuses-errors}

* **Success** – The latest training job completed successfully. The model is trained and deployed for ranking.
* **Failed** – The latest training job failed (for example, no events in the datasets). The UI shows an error message and a request ID; use these when troubleshooting or contacting support.
* **In progress** – A training job is running. Some metrics may be temporarily unavailable until it finishes.
* **Pending** – No result yet (for example, model recently activated or settings recently changed).

If no model has been successfully deployed yet, the "currently deployed model" section and some performance fields will be empty or show the initial-state messaging.
-->

## Video introduttivo {#video}

Scopri come monitorare i modelli di classificazione AI e interpretare lo stato e le prestazioni del training in [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3479849?quality=12)

## Documentazione correlata {#related}

* [Informazioni sui modelli di IA](ai-models.md)
* [Modello di ottimizzazione personalizzata](personalized-optimization-model.md)
* [Creare modelli AI](create-ai-models.md)
* [Creare un set di dati per raccogliere gli eventi](../data-collection/create-dataset.md)
