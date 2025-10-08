---
solution: Journey Optimizer
product: journey optimizer
title: Metriche di Journey Optimizer Experimentation Accelerator
description: Migliora la tua capacità di condurre esperimenti in modo efficace e generare informazioni
feature: Experimentation
topic: Content Management
role: User
level: Beginner
keywords: contenuto, esperimento, multiplo, pubblico, trattamento
exl-id: 74868625-f4ea-44f9-ae2a-8e5fdd22a081
source-git-commit: 664f6bafd4cfb4d86b7a449c279484ca49933247
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 2%

---

# Metriche {#experiment-accelerator-metrics}

Nella pagina **[!UICONTROL Metriche]** le metriche di successo degli esperimenti di Journey Optimizer e Target vengono visualizzate in un&#39;unica posizione, consentendo il monitoraggio delle prestazioni, il confronto e informazioni più approfondite.

## Dashboard di {#dashboard}

Quando si accede alla scheda **[!UICONTROL Metriche]**, tutte le metriche di successo disponibili in Journey Optimizer e Adobe Target sono elencate in una visualizzazione consolidata per consentire di tenere traccia delle prestazioni tra le iniziative, confrontare i risultati e identificare rapidamente le aree che richiedono attenzione.

Accedere ai filtri facendo clic su ![](assets/do-not-localize/Smock_Filter_18_N.svg), che offre opzioni specifiche del contesto, ad esempio il filtro per **[!UICONTROL Source]** o **[!UICONTROL Utilizzato in esperimenti attivi]**.

In alternativa, puoi trovare rapidamente una metrica digitandone il nome nella barra di ricerca.

![](assets/experiment-monitor-metrics.png)

## Dettagli metrica {#metric-details}

### Incrementale nel tempo

![](assets/experiment-monitor-metrics-2.png)

Il grafico **[!UICONTROL Incrementale nel tempo]** fornisce un&#39;analisi visiva della tendenza della metrica selezionata in un intervallo di tempo scelto. Utilizza il menu a discesa per passare dalla visualizzazione giornaliera a quella settimanale e viceversa, in modo da regolare il livello di granularità.

Per riferimento rapido sono disponibili i seguenti valori di riepilogo:

* **[!UICONTROL Totale]**: il valore cumulativo della metrica selezionata nel periodo di reporting.

* **[!UICONTROL Media]**: valore tipico della metrica calcolato nell&#39;intervallo di tempo selezionato. Il bilanciamento delle fluttuazioni giornaliere o settimanali consente di ottenere un quadro più chiaro delle prestazioni normali e può essere utilizzato come base di confronto.

* **[!UICONTROL Tasso di conversione]**: percentuale di profili che hanno completato l&#39;azione desiderata (ad esempio, acquisto, iscrizione) dopo aver visto il trattamento.

Ciascun valore include una variazione percentuale rispetto al periodo precedente, per verificare facilmente se le prestazioni stanno migliorando, diminuendo o rimanendo stabili.

### Effetto esperimento

![](assets/experiment-monitor-metrics-3.png)

Questa sezione mostra tutti gli esperimenti attivi entro l’intervallo di tempo selezionato (Ultimi 90 giorni, Ultimi 30 giorni o Ultimi 7 giorni) ed evidenzia il loro contributo alla metrica.

Sono disponibili le metriche seguenti:

* **[!UICONTROL Incremento]**: misura del miglioramento percentuale del tasso di conversione di un determinato trattamento rispetto al basale.

* **[!UICONTROL Affidabilità]**: prova che un determinato trattamento è uguale al trattamento basale. [Ulteriori informazioni](../content-management/experiment-calculations.md#understand-confidence)

* **[!UICONTROL Contributo]**: proporzione della modifica complessiva della metrica che può essere attribuita a un esperimento o a un trattamento specifico, consentendo l&#39;identificazione delle iniziative che esercitano il maggiore impatto relativo.
