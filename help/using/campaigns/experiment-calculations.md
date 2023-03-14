---
solution: Journey Optimizer
product: journey optimizer
title: Calcoli statistici utilizzati dalla sperimentazione Adobe Journey Optimizer
description: Ulteriori informazioni sui calcoli statistici utilizzati durante l’esecuzione di esperimenti
feature: A/B Testing
topic: Content Management
role: User
level: Experienced
keywords: contenuto, esperimento, statistica, calcolo
hide: true
hidefromtoc: true
exl-id: 60a1a488-a119-475b-8f80-3c6f43c80ec9
badge: label="Beta" type="Informativo"
source-git-commit: 160e4ce03d3be975157c30fbe511875a85b00551
workflow-type: tm+mt
source-wordcount: '909'
ht-degree: 5%

---

# Comprendere i calcoli statistici {#experiment-calculations}

>[!BEGINSHADEBOX]

Informazioni disponibili in questa documentazione:

* [Introduzione all’esperimento sui contenuti](get-started-experiment.md)
* [Creare un esperimento sui contenuti](content-experiment.md)
* **[Comprendere i calcoli statistici](experiment-calculations.md)**
* [Configurare i rapporti sulla sperimentazione](reporting-configuration.md)
* [Calcoli statistici nel rapporto di sperimentazione](experiment-report-calculations.md)

>[!ENDSHADEBOX]

Questo articolo descrive i calcoli statistici utilizzati quando si eseguono Esperimenti in Adobe Journey Optimizer.

La sperimentazione utilizza metodi statistici avanzati per calcolare **Sequenze di affidabilità** e **Affidabilità**, che ti consente di eseguire gli esperimenti per il tempo necessario e di monitorare continuamente i risultati.

Adobe Questo articolo descrive come funziona la sperimentazione e fornisce un’introduzione intuitiva alla **Qualsiasi sequenza di affidabilità valida**.

Per gli utenti esperti, i dettagli tecnici e i riferimenti sono descritti in [questa pagina](../campaigns/assets/confidence_sequence_technical_details.pdf).

## Test statistici ed errori di controllo {#statistical-testing}

![](assets/technote_1.png)

Come illustrato nella tabella precedente, molte metodologie di deduzione statistica sono progettate per controllare due tipi di errori:

* **Falsi positivi (errori di tipo I)**: è un rifiuto errato dell’ipotesi nulla, quando in realtà è vera. Nel contesto delle sperimentazioni online, ciò significa che concludiamo erroneamente che la metrica di risultato è diversa tra ciascun trattamento, anche se era la stessa.
   </br>Prima di eseguire l’esperimento, in genere scegliamo una soglia `\alpha`. Dopo l’esecuzione dell’esperimento, `p-value` viene calcolato e rifiutiamo `null if p < \alpha`. Una soglia comunemente utilizzata è `\alpha = 0.05`, il che significa che nel lungo periodo, ci aspettiamo che 5 esperimenti su 100 siano falsi positivi.

* **Falsi negativi (errori di tipo II)**: significa che non possiamo rifiutare l’ipotesi nulla anche se è falsa. Per le sperimentazioni, questo significa che non respingiamo l&#39;ipotesi nulla, quando in realtà è diversa. Per controllare questo tipo di errore, in genere abbiamo bisogno di un numero sufficiente di utenti nel nostro esperimento per garantire una certa Potenza, definita come `1 - \beta`(ovvero uno meno la probabilità di un errore di tipo II).

La maggior parte delle tecniche di deduzione statistica richiede di correggere la dimensione del campione in anticipo, in base alla dimensione dell&#39;effetto che si desidera determinare, nonché alla tolleranza di errore (`\alpha` e `\beta`) in anticipo. Tuttavia, la metodologia di Adobe Journey Optimizer è progettata per consentire di esaminare continuamente i risultati, per qualsiasi dimensione di campione.

## Metodologia Statistica Di Adobe: Sequenze Di Affidabilità Valide In Qualsiasi Momento

A **Sequenza di affidabilità** è un analogo sequenziale di un **Intervallo di affidabilità** Ad esempio, se ripeti i tuoi esperimenti cento volte e calcoli una stima della metrica media e della relativa sequenza con affidabilità al 95% per ogni nuovo utente che entra nell’esperimento. Una sequenza con affidabilità del 95% includerà il valore effettivo della metrica in 95 dei 100 esperimenti eseguiti. Un intervallo di affidabilità del 95% può essere calcolato una sola volta per esperimento al fine di fornire la stessa garanzia di copertura del 95%; non con ogni nuovo utente. Le sequenze di affidabilità consentono quindi di monitorare continuamente gli esperimenti, senza aumentare i tassi di errore di tipo falso positivo.

La differenza tra le sequenze di affidabilità e gli intervalli di affidabilità per un singolo esperimento è mostrata nell’animazione seguente:

![](assets/technote_2.gif)

**Sequenze di affidabilità** spostare l’attenzione delle sperimentazioni sulla stima piuttosto che sulla verifica delle ipotesi, ovvero focalizzandosi su una stima accurata della differenza nelle medie tra i trattamenti, piuttosto che sul rifiuto o meno di un’ipotesi nulla basata su una soglia di significatività statistica.

Tuttavia, in modo analogo al rapporto tra `p-values`, o **Affidabilità**, e **Intervalli di affidabilità**, esiste anche una relazione tra **Sequenze di affidabilità** e in qualsiasi momento valido `p-values`o in qualsiasi momento con affidabilità valida. Data la familiarità di quantità come Confidence (Affidabilità), Adobe fornisce sia **Sequenze di affidabilità** e in qualsiasi momento la fiducia nei suoi rapporti.

I fondamenti teorici di **Sequenze di affidabilità** provengono dallo studio di sequenze di variabili casuali note come martingales. Di seguito sono riportati alcuni risultati principali per gli esperti di lettura, ma i suggerimenti dei professionisti sono chiari:

>[!NOTE]
>
>Le sequenze di affidabilità possono essere interpretate come analoghi sequenziali sicuri degli intervalli di affidabilità.È possibile esaminare e interpretare i dati negli esperimenti in qualsiasi momento e interrompere in modo sicuro o continuare gli esperimenti. Il valore di affidabilità corrispondente per qualsiasi periodo di tempo valido, oppure `p-value`, è anche interpretabile in modo sicuro.

È importante notare che, poiché le sequenze di affidabilità sono &quot;sempre valide&quot;, saranno più prudenti di una metodologia di orizzonte fissa utilizzata alla stessa dimensione del campione. I limiti della sequenza di affidabilità sono generalmente più ampi di un calcolo dell’intervallo di affidabilità, mentre l’affidabilità valida per qualsiasi periodo di tempo sarà inferiore a un calcolo dell’affidabilità dell’orizzonte fisso. Il vantaggio di questo conservatorismo è che si può tranquillamente interpretare i risultati in ogni momento.

## Dichiarazione di conclusione di un esperimento

![](assets/experimentation_report_2.png)

Ogni volta che visualizzi il rapporto sulla sperimentazione, Adobe analizza i dati accumulati nell’esperimento fino a questo punto e dichiarerà un esperimento &quot;Conclusivo&quot; quando l’affidabilità valida supera una soglia del 95% per almeno uno dei trattamenti.

A questo punto, il trattamento che sta ottenendo il risultato migliore (in base al tasso di conversione o al valore della metrica normalizzata per il profilo) verrà evidenziato nella parte superiore della schermata del rapporto e indicato da una stella nel rapporto tabulare. Solo i trattamenti che hanno un’affidabilità superiore al 95%, insieme al basale, sono considerati in questa determinazione.

Quando sono presenti più di due trattamenti, il collegamento di correzione Bonferroni viene utilizzato per correggere problemi di confronto multipli e controlla il tasso di errore per famiglia. In questo scenario, è anche possibile che ci siano più trattamenti la cui affidabilità è superiore al 95% e i cui intervalli di affidabilità si sovrappongono. In questo caso, Adobe Journey Optimizer dichiarerà che quello con il tasso di conversione più alto (o con il valore della metrica normalizzata per il profilo) ha le prestazioni migliori.
