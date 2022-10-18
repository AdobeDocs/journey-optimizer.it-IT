---
solution: Journey Optimizer
product: journey optimizer
title: Calcoli statistici utilizzati dalla sperimentazione Adobe Journey Optimizer
description: Ulteriori informazioni sui calcoli statistici utilizzati durante l'esecuzione di esperimenti
feature: A/B Testing
topic: Content Management
role: User
level: Experienced
hide: true
hidefromtoc: true
exl-id: 60a1a488-a119-475b-8f80-3c6f43c80ec9
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '897'
ht-degree: 3%

---

# Comprendere i calcoli statistici {#experiment-calculations}

>[!AVAILABILITY]
>
>La **Esperimento dei contenuti** al momento è disponibile solo per un set di organizzazioni (disponibilità limitata). Per ulteriori informazioni, contatta il tuo rappresentante Adobe.

Questo articolo descrive i calcoli statistici utilizzati durante l’esecuzione di esperimenti in Adobe Journey Optimizer.

La sperimentazione utilizza metodi statistici avanzati per calcolare **Sequenze di affidabilità** e **Affidabilità**, che consente di eseguire gli esperimenti per il tempo necessario e di monitorare continuamente i risultati.

Questo articolo descrive come funziona la Sperimentazione e fornisce un’introduzione intuitiva al Adobe **Qualsiasi Sequenza Di Affidabilità Valida**.

Per gli utenti esperti, i dettagli tecnici e i riferimenti sono descritti in [questa pagina](../campaigns/assets/confidence_sequence_technical_details.pdf).

## Test statistici e controllo degli errori {#statistical-testing}

![](assets/technote_1.png)

Come illustrato nella tabella precedente, molte metodologie di deduzione statistica sono progettate per controllare due tipi di errori:

* **Falso positivo (errori di tipo I)**: è un rifiuto scorretto dell&#39;ipotesi null, quando in realtà è vera. Nel contesto delle Sperimentazioni online, ciò significa che falsa conclusione che la metrica dei risultati è diversa tra ogni trattamento, anche se era la stessa.
   </br>Prima di eseguire l&#39;esperimento, tipicamente scegliamo una soglia `\alpha`. Dopo l&#39;esecuzione dell&#39;esperimento, la `p-value` viene calcolato e rifiutiamo il `null if p < \alpha`. Una soglia comunemente utilizzata è `\alpha = 0.05`Il che significa che a lungo termine, ci aspettiamo 5 esperimenti su 100 siano falsi positivi.

* **Falso negativo (errori di tipo II)**: significa che non respingiamo l&#39;ipotesi null anche se è falsa. Per le sperimentazioni, ciò significa che non respingiamo l&#39;ipotesi null, quando in realtà è diversa. Per controllare questo tipo di errore, generalmente abbiamo bisogno di abbastanza utenti nel nostro esperimento per garantire una certa potenza, definita come `1 - \beta`(cioè uno meno la probabilità di un errore di tipo II).

La maggior parte delle tecniche di deduzione statistica richiederà di correggere anticipatamente la dimensione del campione in base alla dimensione dell’effetto che si desidera determinare, nonché alla tolleranza di errore (`\alpha` e `\beta`) in anticipo. Tuttavia, la metodologia Adobe Journey Optimizer è progettata per consentire di esaminare continuamente i risultati, per qualsiasi dimensione del campione.

## Metodologia statistica del Adobe: Qualsiasi Sequenza Di Affidabilità Valida

A **Sequenza di affidabilità** è un analogico sequenziale di un **Intervallo di affidabilità**, ad esempio se ripeti i tuoi esperimenti cento volte e calcola una stima della metrica media e della sequenza di affidabilità al 95% associata per ogni nuovo utente che accede all’esperimento. Una sequenza di affidabilità del 95% includerà il valore vero della metrica in 95 dei 100 esperimenti eseguiti. Un intervallo di affidabilità del 95% può essere calcolato una sola volta per esperimento al fine di fornire la stessa garanzia di copertura del 95%; non con ogni nuovo utente. Le sequenze di affidabilità consentono quindi di monitorare continuamente gli esperimenti, senza aumentare i tassi di errore falsi positivi.

La differenza tra le sequenze di affidabilità e gli intervalli di affidabilità per un singolo esperimento è mostrata nell&#39;animazione seguente:

![](assets/technote_2.gif)

**Sequenze di affidabilità** spostare l&#39;attenzione delle Sperimentazioni verso la stima piuttosto che il test di ipotesi, cioè concentrandosi su una stima accurata della differenza di mezzi tra i trattamenti, piuttosto che sul rifiuto o meno di un&#39;ipotesi nulla basata su una soglia di significatività statistica.

Tuttavia, in modo analogo al rapporto tra `p-values`oppure **Affidabilità** e **Intervalli di affidabilità**, esiste anche una relazione tra **Sequenze di affidabilità** e in qualsiasi momento valido `p-values`o in qualsiasi momento Confidence valida. Data la familiarità delle quantità come la Confidenza, l&#39;Adobe fornisce sia **Sequenze di affidabilità** e ogni volta che la Confidence nei suoi rapporti è valida.

Le basi teoriche **Sequenze di affidabilità** provengono dallo studio di sequenze di variabili casuali note come martingales. Alcuni risultati principali sono inclusi per i lettori esperti qui sotto, ma le prese di posizione dei professionisti sono chiare:

>[!NOTE]
>
>Le sequenze di affidabilità possono essere interpretate come analoghi sequenziali sicuri degli intervalli di affidabilità.È possibile esaminare e interpretare i dati negli esperimenti in qualsiasi momento e interrompere o continuare gli esperimenti in modo sicuro. La Confidenza Valida In Qualsiasi Momento, `p-value`, è anche sicuro da interpretare.

È importante notare che, poiché le sequenze di affidabilità sono &quot;valide in qualsiasi momento&quot;, saranno più conservative rispetto a una metodologia a orizzonte fisso utilizzata con le stesse dimensioni del campione. I limiti della sequenza di affidabilità sono generalmente più ampi di un calcolo dell’intervallo di affidabilità, mentre l’eventuale affidabilità valida sarà inferiore a un calcolo dell’affidabilità dell’orizzonte fisso. Il vantaggio di questo conservatorismo è che si può tranquillamente interpretare i risultati in ogni momento.

## Dichiarare conclusivo un esperimento

![](assets/experimentation_report_2.png)

Ogni volta che visualizzi il rapporto sulla sperimentazione, l&#39;Adobe analizza i dati accumulati nell&#39;esperimento fino a questo punto e dichiarerà un esperimento &quot;conclusivo&quot; quando la fiducia valida supera una soglia del 95% per almeno uno dei trattamenti.

A questo punto, il trattamento che offre le prestazioni migliori (in base al tasso di conversione o al valore di metrica normalizzata in base al profilo) verrà evidenziato nella parte superiore della schermata del rapporto e indicato con una stella nel rapporto tabulare. In questa determinazione sono considerati solo i trattamenti con una confidenza superiore al 95%, insieme alla linea di base.

Quando ci sono più di due trattamenti, il link di correzione Bonferroni viene utilizzato per correggere problemi di confronto multipli e controlla il tasso di errore familiare. In questo scenario, è anche possibile che ci siano più trattamenti la cui fiducia è superiore al 95% e i cui intervalli di affidabilità si sovrappongono. In questo caso, Adobe Journey Optimizer dichiarerà quello con il più alto tasso di conversione (o valore di metrica normalizzata del profilo) come il più performante.
