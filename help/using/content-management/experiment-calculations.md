---
solution: Journey Optimizer
product: journey optimizer
title: Calcoli statistici utilizzati dalla sperimentazione Adobe Journey Optimizer
description: Ulteriori informazioni sui calcoli statistici utilizzati durante l’esecuzione di esperimenti
feature: Experimentation
topic: Content Management
role: User
level: Experienced
keywords: contenuto, esperimento, statistica, calcolo
exl-id: 60a1a488-a119-475b-8f80-3c6f43c80ec9
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: tm+mt
source-wordcount: '1067'
ht-degree: 0%

---

# Comprendere i calcoli statistici {#experiment-calculations}

Questo articolo descrive i calcoli statistici utilizzati quando si eseguono Esperimenti in Adobe Journey Optimizer.

La sperimentazione utilizza [metodi statistici avanzati](../content-management/assets/confidence_sequence_technical_details.pdf) per calcolare **sequenze di affidabilità** e **Affidabilità**, che consentono di eseguire gli esperimenti per il tempo necessario e di monitorare continuamente i risultati.

Questo articolo descrive il funzionamento della sperimentazione e fornisce un&#39;introduzione intuitiva alle **sequenze di affidabilità valide in qualsiasi momento** di Adobe.

Per gli utenti esperti, i dettagli tecnici e i riferimenti sono descritti in [questa pagina](../content-management/assets/confidence_sequence_technical_details.pdf).

## Test statistici ed errori di controllo {#statistical-testing}

Quando esegui un esperimento, stai cercando di determinare se c’è una differenza tra due popolazioni e la probabilità che la differenza sia dovuta al caso.

In generale ci sono due ipotesi:

* l&#39;ipotesi **Null** indica che non vi è alcun effetto sul trattamento.
* l&#39;**ipotesi alternativa**, che indica un effetto sul trattamento.

In termini di significatività statistica, l&#39;obiettivo è quello di provare a valutare la forza delle prove per rifiutare l&#39;ipotesi nulla. Un punto importante da notare è che la significatività statistica viene utilizzata per valutare la probabilità che i trattamenti siano diversi, non la probabilità che abbiano successo. Per questo motivo la rilevanza statistica viene utilizzata in combinazione con **Incremento**.

Una sperimentazione efficace richiede di prendere in considerazione diversi tipi di errori che potrebbero causare conclusioni errate.

![](assets/technote_1.png)

La tabella precedente illustra i diversi tipi di errori:

* **Falsi positivi (errori di tipo I)**: sono un rifiuto errato dell&#39;ipotesi nulla, quando in realtà è vera. Nel contesto degli esperimenti online, ciò significa che concludiamo erroneamente che la metrica di risultato è diversa tra ciascun trattamento, anche se era la stessa.
  </br>Prima di eseguire l&#39;esperimento, viene in genere selezionata una soglia `\alpha`. Dopo l&#39;esecuzione dell&#39;esperimento, `p-value` viene calcolato e viene rifiutato `null if p < \alpha`.La scelta di un `/alpha` si basa sulle conseguenze dell&#39;ottenimento della risposta errata, ad esempio in una sperimentazione clinica in cui la vita di un utente potrebbe essere compromessa, è possibile decidere di avere un `\alpha = 0.005`. Una soglia comunemente utilizzata nella sperimentazione online è `\alpha = 0.05`, il che significa che nel lungo periodo ci aspettiamo che 5 esperimenti su 100 siano falsi positivi.

* **Falsi negativi (errori di tipo II)**: indica che non è possibile rifiutare l&#39;ipotesi nulla, anche se è falsa. Per le sperimentazioni, questo significa che non respingiamo l&#39;ipotesi nulla, quando in realtà è diversa. Per controllare questo tipo di errore, in genere è necessario che l’esperimento contenga un numero di utenti sufficiente per garantire una determinata potenza, definita come `1 - \beta` (ovvero uno meno la probabilità di un errore di tipo II).

La maggior parte delle tecniche di deduzione statistica richiede la correzione della dimensione del campione in anticipo, in base alla dimensione dell&#39;effetto che si desidera determinare, nonché la tolleranza di errore (`\alpha` e `\beta`) in anticipo. Tuttavia, la metodologia di Adobe Journey Optimizer è progettata per consentire di esaminare continuamente i risultati, per qualsiasi dimensione di campione.

## Metodologia Statistica Di Adobe: Sequenze Di Affidabilità Valide In Qualsiasi Momento

Una **sequenza di affidabilità** è un analogo sequenziale di un **intervallo di affidabilità**, ad esempio se si ripetono cento esperimenti e si calcola una stima della metrica media e della relativa sequenza con affidabilità al 95% per ogni nuovo utente che entra nell&#39;esperimento. Una sequenza con affidabilità del 95% includerà il valore effettivo della metrica in 95 dei 100 esperimenti eseguiti. Un intervallo di affidabilità del 95% può essere calcolato una sola volta per esperimento al fine di fornire la stessa garanzia di copertura del 95%; non con ogni nuovo utente. Le sequenze di affidabilità consentono quindi di monitorare continuamente gli esperimenti, senza aumentare i tassi di errore di tipo falso positivo.

La differenza tra le sequenze di affidabilità e gli intervalli di affidabilità per un singolo esperimento è mostrata nell’animazione seguente:

![](assets/technote_2.gif)

**Le sequenze di affidabilità** spostano l&#39;attenzione delle sperimentazioni sulla stima piuttosto che sulla verifica delle ipotesi, ovvero sulla stima accurata della differenza nelle medie tra i trattamenti, piuttosto che sul rifiuto o meno di un&#39;ipotesi nulla basata su una soglia di significatività statistica.

Tuttavia, in modo simile alla relazione tra `p-values` o **Affidabilità** e **Intervalli di affidabilità**, esiste anche una relazione tra **Sequenze di affidabilità** e qualsiasi periodo di validità di `p-values` o qualsiasi periodo di validità di Affidabilità. Data la familiarità di quantità come Confidence (Affidabilità), Adobe fornisce sia le **sequenze di affidabilità** che qualsiasi periodo di validità Confidence (Affidabilità valida) nei suoi rapporti.

Le basi teoriche delle **sequenze di affidabilità** derivano dallo studio delle sequenze di variabili casuali note come martingales. Di seguito sono riportati alcuni risultati principali per gli esperti di lettura, ma i suggerimenti dei professionisti sono chiari:

>[!NOTE]
>
>Le sequenze di affidabilità possono essere interpretate come analoghi sequenziali sicuri degli intervalli di affidabilità. Con gli intervalli di affidabilità puoi interpretare l’esperimento solo dopo aver raggiunto la dimensione del campione predeterminata. Tuttavia, con le sequenze di affidabilità è possibile esaminare e interpretare i dati negli esperimenti in qualsiasi momento e interrompere in modo sicuro o continuare gli esperimenti. Anche il valore di Affidabilità valida in qualsiasi momento, o `p-value`, corrispondente, può essere interpretato in modo sicuro in qualsiasi momento.

È importante notare che, poiché le sequenze di affidabilità sono &quot;sempre valide&quot;, saranno più prudenti di una metodologia di orizzonte fissa utilizzata alla stessa dimensione del campione. I limiti della sequenza di affidabilità sono generalmente più ampi di un calcolo dell’intervallo di affidabilità, mentre l’affidabilità valida per qualsiasi periodo di tempo sarà inferiore a un calcolo dell’affidabilità dell’orizzonte fisso. Il vantaggio di questo conservatorismo è che si può tranquillamente interpretare i risultati in ogni momento.

## Dichiarazione di conclusione di un esperimento

![](assets/experimentation_report_2.png)

Ogni volta che visualizzi il rapporto sulla sperimentazione, Adobe analizza i dati accumulati nell’esperimento fino a questo punto e dichiarerà un esperimento &quot;Conclusivo&quot; quando l’affidabilità valida supera una soglia del 95% per almeno uno dei trattamenti.

A questo punto, il trattamento che sta ottenendo il risultato migliore (in base al tasso di conversione o al valore della metrica normalizzata per il profilo) verrà evidenziato nella parte superiore della schermata del rapporto e indicato da una stella nel rapporto tabulare. Solo i trattamenti che hanno un’affidabilità superiore al 95%, insieme al basale, sono considerati in questa determinazione.

Quando sono presenti più di due trattamenti, il collegamento di correzione Bonferroni viene utilizzato per correggere problemi di confronto multipli e controlla il tasso di errore per famiglia. In questo scenario, è anche possibile che ci siano più trattamenti la cui affidabilità è superiore al 95% e i cui intervalli di affidabilità si sovrappongono. In questo caso, Adobe Journey Optimizer dichiarerà che quello con il tasso di conversione più alto (o con il valore della metrica normalizzata per il profilo) ha le prestazioni migliori.
