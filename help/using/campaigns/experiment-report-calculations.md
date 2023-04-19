---
title: Calcoli statistici utilizzati nel rapporto di sperimentazione
description: Ulteriori informazioni sui calcoli statistici utilizzati durante l'esecuzione dei rapporti sugli esperimenti
feature: A/B Testing
topic: Content Management
role: User
level: Experienced
hide: true
hidefromtoc: true
badge: label="Beta" type="Informativo"
exl-id: b3336381-bc73-4c8f-938f-f10fe37305b0
source-git-commit: c823d1a02ca9d24fc13eaeaba2b688249e61f767
workflow-type: tm+mt
source-wordcount: '961'
ht-degree: 3%

---

# Calcoli statistici nel rapporto di sperimentazione {#experiment-report-calculations}

>[!BEGINSHADEBOX]

Cosa troverai in questa documentazione:

* [Introduzione all’esperimento sui contenuti](get-started-experiment.md)
* [Creare un esperimento sui contenuti](content-experiment.md)
* [Comprendere i calcoli statistici](experiment-calculations.md)
* [Configurare i rapporti sulla sperimentazione](reporting-configuration.md)
* **[Calcoli statistici nel rapporto di sperimentazione](experiment-report-calculations.md)**

>[!ENDSHADEBOX]

In questa pagina sono documentati i calcoli statistici dettagliati utilizzati nel rapporto Sperimentazione per le campagne in Adobe Journey Optimizer.

Questa pagina è destinata agli utenti tecnici.

## Tasso di conversione

il tasso di conversione o **meschino**&#x200B;μ<sub>ν</sub> per ogni trattamento `ν` in un esperimento è definito come un rapporto tra la somma della metrica e il numero di profili assegnati a tale metrica, N<sub>ν</sub>:

![](assets/statistical_1.png){width="125" align="center"}

Qui, Y<sub>idroid</sub> è il valore della metrica oggettiva per ciascun profilo `i`, che è stato assegnato a una determinata variante *ν*. Quando la metrica di obiettivo è una metrica &quot;univoca&quot;, ovvero un conteggio del numero di profili che eseguono una particolare azione, viene visualizzata come un tasso di conversione e formattata come percentuale. Quando la metrica è una metrica di &quot;conteggio&quot; o &quot;valore totale&quot; (ad esempio, si apre un’e-mail, rispettivamente un ricavo), la stima media per la metrica viene visualizzata come &quot;Conteggio per profilo&quot; o &quot;Valore per profilo&quot;.

Se necessario, con l’espressione viene utilizzata la deviazione standard del campione:

![](assets/statistical_2.png){width="225" align="center"}

## Lift {#lift}

L’incremento tra una variante  *ν* e la variante di controllo  *ν<sub>0</sub>* è il &quot;delta&quot; relativo nei tassi di conversione, definito come il calcolo sottostante, dove i singoli tassi di conversione sono definiti sopra. Viene visualizzata come percentuale.

![](assets/statistical_3.png){width="125" align="center"}

</br>

## In qualsiasi momento Intervalli di affidabilità validi per trattamenti individuali

Il pannello Sperimentazione Percorso visualizza gli intervalli di affidabilità &quot;in qualsiasi momento validi&quot; (sequenze di affidabilità) per i singoli trattamenti in un esperimento.

Sequenza di affidabilità per una singola variante `ν` è fondamentale per la metodologia statistica utilizzata dall&#39;Adobe. Puoi trovarne la definizione in [questa pagina](https://doi.org/10.48550/arXiv.2103.06476) (riprodotto da [Waudby-Smith et al.]).

Se sei interessato a stimare un parametro target `ψ` come il tasso di conversione di una variante in un esperimento, la dicotomia tra una sequenza di intervalli di affidabilità a tempo fisso (CSI) e una sequenza di affidabilità uniforme in base al tempo (CS) può essere riassunta come segue:

![](assets/statistical_4.png){width="500" align="center"}

Per un intervallo di affidabilità regolare, la garanzia probabilistica che il parametro target si trovi all’interno dell’intervallo di valori Ċ<sub>n</sub> è valido solo a un singolo valore fisso di `n` (4) `n` è il numero di campioni). Al contrario per una sequenza di affidabilità, siamo certi che in ogni momento/ tutti i valori della dimensione del campione `t`, il valore &quot;true&quot; del parametro di interesse si trova entro i limiti.

Questo ha alcune profonde implicazioni che sono molto importanti per i test online:

* Il CS può essere aggiornato facoltativamente ogni volta che nuovi dati diventano disponibili.
* Gli esperimenti possono essere monitorati in modo continuo, arrestati in modo adattivo o continuati.
* L&#39;errore di tipo I viene controllato in tutti i momenti di arresto, compresi i tempi dipendenti dai dati.

L’Adobe utilizza le sequenze di confidenza asintotica, che per una singola variante con stima media `μ` presenta il modulo:

![](assets/statistical_5.png){width="300" align="center"}

Dove:

* `N` è il numero di unità per la variante.
* `σ` è una stima campione della deviazione standard (definita sopra).
* `α` è il livello desiderato di errore di tipo I (o probabilità di copertura errata). È sempre impostato su 0,05.
* true<sup>2</sup> è una costante che regola la dimensione del campione a cui il CS è più stretto. L&#39;Adobe ha scelto un valore universale del valore<sup>2</sup> = 10<sup>-2,8</sup>, appropriato per i tipi di tassi di conversione rilevati negli esperimenti online.

## Confidence {#confidence}

L&#39;affidabilità utilizzata dall&#39;Adobe è un&#39;affidabilità &quot;valida in qualsiasi momento&quot;, ottenuta invertendo la sequenza di confidenza per l&#39;effetto di trattamento medio.

Per essere precisi, in un campione *t* per verificare la differenza di mezzi tra due varianti, esiste una mappatura 1:1 tra i *p*-value per questo test e l&#39;intervallo di affidabilità per la differenza nei mezzi. Per analogia, una qualsiasi volta valida *p*-value può essere ottenuto invertendo la sequenza di confidenza (in qualsiasi momento valida) per il calcolatore medio dell&#39;effetto di trattamento:

![](assets/statistical_6.png){width="200" align="center"}

Qui, *E* è un&#39;aspettativa. Lo stimatore utilizzato è uno stimatore a tendenza inversa (IPW). Considera N = N<sub>0</sub> +N<sub>1</sub> unità, le assegnazioni di variante per ciascuna unità `i` etichettate da A<sub>i</sub>=0,1 se l&#39;unità è assegnata alla variante `ν`=0,1. Se gli utenti sono assegnati con probabilità fissa (propensione) π<sub>0</sub>, (1 π)<sub>0</sub>) e la loro metrica di risultato è Y<sub>i</sub>, quindi lo stimatore IPW per l&#39;effetto medio del trattamento è:

![](assets/statistical_12.png){width="400" align="center"}

Nota che *f* è la funzione di influenza, Waudby-Smith et al. mostra che la sequenza di affidabilità per questo stimatore è:

![](assets/statistical_7.png){width="500" align="center"}

Sostituzione della probabilità di assegnazione con le relative stime empiriche: π<sub>0</sub> = N<sub>0</sub>/N, il termine di varianza può essere espresso in termini di stime medie individuali del campione μ<sub>0,1</sub> e stime di deviazione standard,<sub>0,1</sub> come:

![](assets/statistical_8.png){width="500" align="center"}

Successivamente, ricordare che per una normale prova di ipotesi con la statistica z del test (μ)<sub>A</sub>-μ<sub>0</sub>/Þ<sub>p</sub>) esiste una corrispondenza tra `p`-valori e intervalli di affidabilità:

![](assets/statistical_9.png){width="500" align="center"}

dove `Φ` è la distribuzione cumulativa della norma normale. In qualsiasi momento valido `p`-valori, data la sequenza di affidabilità per l&#39;effetto di trattamento medio sopra definito, possiamo invertire questa relazione:

![](assets/statistical_10.png){width="600" align="center"}

Infine, la **confidenza valida in qualsiasi momento** è:

![](assets/statistical_11.png){width="200" align="center"}

## Dichiarare conclusivo un esperimento

Per un esperimento con due bracci, il pannello Sperimentazione Journey Optimizer visualizza un messaggio che informa che un esperimento è **conclusivo** quando l&#39;affidabilità valida in qualsiasi momento supera il 95% (ovvero, la validità in qualsiasi momento `p`-value è inferiore al 5%).

Quando sono presenti più di due varianti, la correzione Bonferonni viene applicata per controllare il tasso di errore in base alla famiglia. Per un esperimento con `K` trattamenti, e un unico trattamento di base (controllo), ci sono `K-1` test di ipotesi indipendenti. La correzione Bonferonni significa che respingiamo l&#39;ipotesi null secondo cui il controllo e una determinata variante hanno mezzi uguali, se valida in qualsiasi momento `p`-value (definito sopra) è inferiore a una soglia di `α/(K-1)`.

## Braccio dalle prestazioni migliori

Quando un esperimento viene dichiarato conclusivo, viene visualizzato il braccio con le prestazioni migliori. Questa è la leva con le migliori prestazioni (media più alta o tasso di conversione), tra il Set che include il controllo, e tutti i bracci che hanno un `p`-valore inferiore alla soglia Bonferonni.
