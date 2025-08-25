---
title: Calcoli statistici utilizzati nel rapporto sulla sperimentazione
description: Ulteriori informazioni sui calcoli statistici utilizzati durante l’esecuzione dei rapporti sugli esperimenti
feature: A/B Testing, Experimentation
role: User
level: Experienced
exl-id: 67ba8861-be6f-42ae-b9b8-96168d0dd15c
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: tm+mt
source-wordcount: '950'
ht-degree: 1%

---

# Comprendere i calcoli statistici nel rapporto sulla sperimentazione {#experiment-report-calculations}

In questa pagina sono documentati i calcoli statistici dettagliati utilizzati nel rapporto Sperimentazione per le campagne in Adobe Journey Optimizer.

Questa pagina è destinata agli utenti tecnici.

## Tasso di conversione

Il tasso di conversione o **media**, μ<sub></sub> per ogni trattamento `ν` in un esperimento è definito come un rapporto tra la somma della metrica e il numero di profili assegnati a tale metrica, N<sub></sub>:

![](assets/statistical_1.png){width="125" align="center"}

In questo caso, Y<sub>i</sub> è il valore della metrica di obiettivo per ogni profilo `i`, che è stato assegnato a una determinata variante **. Quando la metrica obiettiva è una metrica &quot;univoca&quot;, ovvero è un conteggio del numero di profili che eseguono una particolare azione, viene visualizzata come tasso di conversione e formattata come percentuale. Quando la metrica è una metrica di &quot;conteggio&quot; o &quot;valore totale&quot; (ad esempio apertura di e-mail, ricavi rispettivamente), la stima media per la metrica viene visualizzata come &quot;Conteggio per profilo&quot; o &quot;Valore per profilo&quot;.

Se necessario, la deviazione standard del campione è usata con l&#39;espressione:

![](assets/statistical_2.png){width="225" align="center"}

## Incremento {#lift}

L&#39;incremento tra una variante ** e la variante di controllo *<sub>0</sub>* è il &quot;delta&quot; relativo nei tassi di conversione, definito come il calcolo seguente, in cui i singoli tassi di conversione sono definiti come sopra. Viene visualizzata come percentuale.

![](assets/statistical_3.png){width="125" align="center"}

</br>

## Intervalli di confidenza validi per i singoli trattamenti

Nel pannello Sperimentazione di Percorso vengono visualizzati intervalli di affidabilità (sequenze di affidabilità) &quot;sempre validi&quot; per i singoli trattamenti di un esperimento.

La sequenza di affidabilità per una singola variante `ν` è fondamentale per la metodologia statistica utilizzata da Adobe. Puoi trovarne la definizione in [questa pagina](https://doi.org/10.48550/arXiv.2103.06476) (riprodotta da [Waudby-Smith et al.]).

Se si è interessati a stimare un parametro di destinazione `ψ`, ad esempio il tasso di conversione di una variante in un esperimento, la dicotomia tra una sequenza di intervalli di affidabilità (CI) a tempo fisso e una sequenza di affidabilità (CS) uniforme nel tempo può essere riassunta come segue:

![](assets/statistical_4.png){width="500" align="center"}

Per un intervallo di affidabilità regolare, la garanzia probabilistica che il parametro di destinazione si trovi all&#39;interno dell&#39;intervallo di valori<sub>n</sub> è valida solo per un singolo valore fisso di `n` (dove `n` è il numero di campioni). Al contrario, per una sequenza di affidabilità, siamo certi che in ogni momento/ tutti i valori della dimensione del campione `t`, il valore &quot;true&quot; del parametro di interesse si trova entro i limiti.

Questo ha alcune implicazioni profonde che sono molto importanti per i test online:

* Facoltativamente, il CS può essere aggiornato ogni volta che diventano disponibili nuovi dati.
* Gli esperimenti possono essere monitorati in modo continuo, interrotti in modo adattivo o continuati.
* L’errore di tipo I viene controllato in tutti i momenti di arresto, compresi quelli dipendenti dai dati.

Adobe utilizza le sequenze di affidabilità asintotiche, che per una singola variante con stima media `μ` hanno il formato:

![](assets/statistical_5.png){width="300" align="center"}

Dove:

* `N` è il numero di unità per quella variante.
* `σ` è una stima campione della deviazione standard (definita sopra).
* `α` è il livello desiderato di errore di tipo I (o la probabilità di mancata copertura). Questo valore è sempre impostato su 0,05.
* L&#39;elemento che caratterizza il CS è la costante che consente di regolare le dimensioni del campione in base alle quali il CS è più stretto. <sup></sup> Adobe ha scelto un valore universale di<sup>2</sup> = 10<sup>-2.8</sup>, appropriato per i tipi di tassi di conversione visualizzati negli esperimenti online.

## Affidabilità {#confidence}

L’affidabilità utilizzata da Adobe è un’affidabilità &quot;valida in qualsiasi momento&quot;, ottenuta invertendo la sequenza di affidabilità per l’effetto medio del trattamento.

Per essere precisi, in un test di due campioni *t* per la differenza di medie tra due varianti, esiste una mappatura 1:1 tra il valore di *p* per questo test e l&#39;intervallo di affidabilità per la differenza di medie. Per analogia, è possibile ottenere un valore di *p* valido in qualsiasi momento invertendo la sequenza di affidabilità (valida in qualsiasi momento) per il stimatore dell&#39;effetto medio del trattamento:

![](assets/statistical_6.png){width="200" align="center"}

*E* è un&#39;aspettativa. Lo stimatore utilizzato è uno stimatore con ponderazione della propensione inversa (IPW). Considerare N = N<sub>0</sub> +N<sub>1</sub> unità, le assegnazioni di variante per ogni unità `i` etichettata da A<sub>i</sub>=0,1 se l&#39;unità è assegnata alla variante `ν`=0,1. Se gli utenti vengono assegnati con una probabilità fissa (propensione)<sub>0</sub>, (1-<sub>0</sub>) e la metrica di risultato è Y<sub>i</sub>, allora lo stimatore IPW per l&#39;effetto del trattamento medio è:

![](assets/statistical_12.png){width="400" align="center"}

Notando che *f* è la funzione di influenza, Waudby-Smith et al. ha mostrato che la sequenza di affidabilità per questo stimatore è:

![](assets/statistical_7.png){width="500" align="center"}

Sostituendo la probabilità di assegnazione con le stime empiriche:<sub>0</sub> = N<sub>0</sub>/N, il termine di varianza può essere espresso in termini di stime medie di campione individuali μ<sub>0,1</sub> e stime di deviazione standard, con:<sub></sub>

![](assets/statistical_8.png){width="500" align="center"}

Successivamente, ricorda che per un test di ipotesi regolare con statistica del test z = (μ<sub>A</sub>-μ<sub>0</sub>/μ<sub>p</sub>) esiste una corrispondenza tra i valori `p` e gli intervalli di affidabilità:

![](assets/statistical_9.png){width="500" align="center"}

dove `Φ` è la distribuzione cumulativa della normale standard. Per ogni periodo di tempo valido `p` valori, data la sequenza di affidabilità per l’effetto medio del trattamento definito sopra, è possibile invertire questa relazione:

![](assets/statistical_10.png){width="600" align="center"}

Infine, **attendibilità valida in qualsiasi momento** è:

![](assets/statistical_11.png){width="200" align="center"}

## Dichiarazione di conclusione di un esperimento

Per un esperimento con due bracci, nel pannello Sperimentazione di Journey Optimizer viene visualizzato un messaggio che indica che un esperimento è **conclusivo** quando l&#39;affidabilità valida supera il 95% (ovvero, il valore valido `p` è inferiore al 5%).

Se sono presenti più di due varianti, la correzione Bonferroni viene applicata per controllare il tasso di errore per famiglia. Per un esperimento con `K` trattamenti e un singolo trattamento di base (di controllo), sono disponibili `K-1` test di ipotesi indipendenti. La correzione Bonferroni significa che rifiutiamo l&#39;ipotesi nulla che il controllo e una determinata variante abbiano mezzi uguali, se il valore valido `p` (definito sopra) è al di sotto di una soglia di `α/(K-1)`.

## Braccio dalle prestazioni migliori

Quando un esperimento è dichiarato conclusivo, viene visualizzato il braccio con le prestazioni migliori. Questo è il braccio con le migliori prestazioni (media più alta o tasso di conversione), tra il Set che include il controllo, e tutti i bracci con un valore di `p` che è al di sotto della soglia Bonferroni.
