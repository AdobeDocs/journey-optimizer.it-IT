---
solution: Journey Optimizer
product: journey optimizer
title: Ciclo di rilascio di Adobe Journey Optimizer
feature: Release Notes
description: Informazioni sul ciclo di rilascio di Adobe Journey Optimizer
hide: true
hidefromtoc: true
source-git-commit: 625dfbb66effb30172f6faf56db6fe512aef909a
workflow-type: tm+mt
source-wordcount: '851'
ht-degree: 0%

---

# Ciclo di rilascio di Journey Optimizer {#releases}

[!DNL Adobe Journey Optimizer] viene aggiornato regolarmente per fornire nuove funzionalità, miglioramenti e correzioni. Questa pagina spiega come funziona il ciclo di rilascio e cosa significa ogni fase di rilascio, in modo da poter capire facilmente quando le funzioni diventano disponibili per la tua organizzazione.

## Modello di consegna continua {#continuous-delivery-model}

[!DNL Adobe Journey Optimizer] opera su un modello di distribuzione continua, consentendo un approccio scalabile e graduale alla distribuzione delle funzionalità. Questo modello consente ad Adobe di fornire innovazione più rapidamente e garantire stabilità e prestazioni costanti durante il rollout.

>[!NOTE]
>
> Poiché [!DNL Adobe Journey Optimizer] utilizza la distribuzione continua, è possibile che le nuove funzionalità vengano visualizzate progressivamente in più organizzazioni o aree geografiche.

Come parte di questo modello:

* Nuove funzionalità e miglioramenti vengono implementati in produzione non appena sono pronti.

* Le [**Note sulla versione**](release-notes.md) vengono aggiornate tra le versioni mensili con una sezione _Ultimi aggiornamenti_, che annuncia nuove funzionalità e miglioramenti durante il rollout, in modo da rimanere informati in tempo reale.

## Tempistiche e cadenza di rilascio {#release-timing}

[!DNL Adobe Journey Optimizer] segue in genere una cadenza di rilascio mensile, con le distribuzioni che in genere si verificano durante l&#39;ultima settimana di ogni mese. Le note sulla versione mensili e la relativa documentazione vengono pubblicate il martedì della settimana di rilascio. Le note pre-release vengono pubblicate il venerdì precedente la settimana di rilascio.

>[!TIP]
>
> Alla fine di ogni trimestre, è possibile prevedere i rilasci e implementarli fino a due settimane prima della fine del mese per allinearli ai programmi trimestrali o ai rilasci di prodotti dipendenti.

Mentre il rilascio mensile introduce il set principale di nuove funzionalità e correzioni, l’approccio di distribuzione continua consente di distribuire aggiornamenti aggiuntivi tra i cicli quando sono pronti. Le note sulla versione vengono quindi aggiornate di conseguenza nella sezione _Ultimi aggiornamenti_ e viene menzionata la data di disponibilità. Tutte le modifiche rilasciate durante il mese sono consolidate nelle note sulla versione mensili alla data di rilascio.


## Percorsi di rilascio {#release-paths}

Le funzioni di Journey Optimizer seguono percorsi di rilascio diversi a seconda della complessità, delle dipendenze e dell’ambito. La piattaforma utilizza diverse etichette di disponibilità (Beta, Disponibilità limitata, Disponibilità generale), ma non tutte le funzioni passano attraverso tutte.

I percorsi di rilascio comuni includono:

* **Diretto a GA**: alcune nuove funzionalità e miglioramenti sono direttamente disponibili in General Availability (GA).
* **LA → GA** — Alcune funzionalità sono disponibili per un pubblico limitato (disponibilità limitata) prima del rollout generale.
* **Beta → LA → GA**: le funzionalità più grandi o sperimentali avanzano in tutte le fasi di test e convalida.
* **Beta → GA**: alcune funzionalità stabili di Beta possono essere spostate direttamente in GA, senza una fase di LA intermedia.

>[!TIP]
>
> Se ti interessa accedere in anteprima alle funzioni di Beta o a disponibilità limitata, contatta il tuo rappresentante Adobe per discutere le opzioni di partecipazione.


## Etichette di disponibilità {#availability-labels}

| **Etichetta** | **Finalità** | **Disponibilità** | **Note chiave** |
|------------|-------------|------------------|----------------|
| **Beta** | Test preliminari e raccolta di feedback. | Limitato a clienti o organizzazioni selezionati che partecipano al programma Beta di Adobe. | - non destinati alla produzione.<br>- La funzionalità o la progettazione potrebbero cambiare prima del GA.<br>- Il feedback consente di perfezionare l&#39;implementazione finale. |
| **Disponibilità limitata (LA)** | Rollout controllato per la convalida e il monitoraggio. | Abilitato solo per i clienti o gli ambienti selezionati (ad esempio, sandbox di sviluppo). | - La funzione è quasi finale e monitorata attivamente.<br>- Utilizzato per convalidare le prestazioni e la scalabilità prima della versione generale.<br>- L&#39;accesso richiede l&#39;approvazione di Adobe. |
| **Disponibilità generale (GA)** | Ampia versione di funzionalità completamente supportate. | Abilitata per impostazione predefinita per tutte le organizzazioni idonee. | - Predisposizione alla produzione e supporto completo.<br> - È possibile che vengano applicate licenze o autorizzazioni.<br> - Possibilità di distribuzione progressiva tra aree geografiche. |


## Rollout e disponibilità {#rollout}

Anche dopo un annuncio GA, il rollout può avvenire gradualmente tra organizzazioni o aree geografiche. Se una nuova funzionalità non viene visualizzata immediatamente nell’ambiente, in genere sarà disponibile entro pochi giorni dal rilascio.

Questo rollout graduale consente ad Adobe di monitorare la stabilità, le prestazioni e l’esperienza utente prima di completare l’implementazione.


## Rimanere informati {#staying-informed}

Per rimanere aggiornati:

* Consulta le [**note sulla versione più recente**](release-notes.md) per informazioni sulle funzionalità nuove e aggiornate.
* Controlla la sezione **_Ultimi aggiornamenti_** tra i rilasci mensili per le distribuzioni in tempo reale.
* Monitora **Note pre-release** (se disponibili) per un&#39;anteprima delle prossime funzionalità.
* Contatta il tuo rappresentante Adobe per informazioni su Beta, disponibilità limitata o adesione.


## Domande frequenti {#faq}

+++ Quando vengono pianificate le versioni di Adobe Journey Optimizer?

[!DNL Adobe Journey Optimizer] in genere rilascia gli aggiornamenti durante l&#39;ultima settimana di ogni mese. Alla fine di ogni trimestre, il rilascio può essere anticipato di un massimo di due settimane per allinearsi ad aggiornamenti a livello di più soluzioni o piattaforma.

+++

+++ Perché non visualizzo una nuova funzione subito dopo il suo annuncio?

Alcune funzioni GA vengono implementate progressivamente per garantire la stabilità e le prestazioni della piattaforma. Se non visualizzi subito una funzione, questa verrà visualizzata una volta completata l’implementazione per la tua area geografica o organizzazione.

+++

+++ Qual è la differenza tra Beta, disponibilità limitata e disponibilità generale (GA)?

* **Beta**: fase iniziale di test, accesso limitato, basato su feedback.
* **Disponibilità limitata (LA)**: rollout controllato per la convalida finale.
* **Disponibilità generale (GA)**: versione completa per tutti i clienti autorizzati.

+++

+++ Tutte le funzioni sono gestite tramite Beta e la disponibilità limitata?

No. Alcune funzioni vengono rilasciate direttamente in GA o solo in LA, a seconda della loro natura e disponibilità. Il percorso di rilascio è personalizzato per ogni funzionalità per bilanciare agilità, qualità e stabilità.

+++

+++ Come posso partecipare ai programmi Beta o Disponibilità limitata?

L’accesso avviene su invito o richiesta tramite il rappresentante Adobe. La partecipazione contribuisce a modellare la struttura delle funzioni e garantisce che i casi d’uso vengano considerati nella versione finale.

+++

+++ Con quale frequenza vengono aggiornate le note sulla versione?

Le note sulla versione vengono continuamente aggiornate. Oltre ai rilasci mensili, la sezione _Ultimi aggiornamenti_ viene aggiornata ogni volta che nuove funzioni o miglioramenti vengono inviati alla produzione.

+++
