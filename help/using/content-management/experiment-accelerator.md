---
solution: Journey Optimizer
product: journey optimizer
title: Experimentation Accelerator
description: Migliora la tua capacità di condurre esperimenti in modo efficace e generare informazioni
feature: Experimentation
topic: Content Management
role: User
level: Beginner
keywords: contenuto, esperimento, multiplo, pubblico, trattamento
hide: true
hidefromtoc: true
source-git-commit: e4d5631701c5c270af7aec931f6b98a567b4ed29
workflow-type: tm+mt
source-wordcount: '960'
ht-degree: 1%

---

# Introduzione a Experimentation Accelerator {#content-experiment}

>[!BEGINSHADEBOX]

* **[Introduzione ad Experimentation Accelerator](experiment-accelerator.md)**
* [Scheda Esperimenti](experiment-accelerator-monitor.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
> Experimentation Accelerator è attualmente in versione beta, con l’introduzione progressiva delle funzioni.

**Experimentation Accelerator** è uno strumento potente progettato per semplificare e migliorare il processo di sperimentazione. Integrandosi con Adobe Target e Adobe Journey Optimizer, fornisce una piattaforma centralizzata per la gestione, l’analisi e l’ottimizzazione degli esperimenti. Sfruttando le informazioni basate sull’intelligenza artificiale e i test adattivi, Experimentation Accelerator ti consente di prendere decisioni basate sui dati, migliorare le strategie di marketing e promuovere risultati misurabili.

I vantaggi principali includono:

* **Sperimentazione più veloce**: esegui test adattivi e sempre attivi con modelli che si modificano nel tempo.

* **Piattaforma unificata**: gestisci tutti gli esperimenti da Adobe Target e Journey Optimizer in un&#39;unica posizione.

* **Informazioni basate sull&#39;intelligenza artificiale**: vengono visualizzati automaticamente i risultati chiave, i driver delle prestazioni e le nuove opportunità.

* **Targeting più intelligente**: utilizza i dati comportamentali e di contenuto per dare priorità agli esperimenti ad alto impatto.

* **Monitoraggio KPI**: tieni traccia di metriche quali incremento, ricavi e affidabilità negli esperimenti.

* **Collaboration** senza problemi: condividi facilmente i risultati e gestisci i ruoli del team con avvisi in tempo reale.

Dopo [aver creato e configurato l&#39;esperimento](content-experiment.md) e aver inviato le campagne o i percorsi ai profili, puoi accedere a **[!UICONTROL Experimentation Accelerator]** per approfondire le prestazioni dell&#39;esperimento.

Per accedere a **[!UICONTROL Experimentation Accelerator]**:

* Dal menu a sinistra, seleziona **[!UICONTROL Experimentation Accelerator]** nel menu a discesa **[!UICONTROL Sperimentazione]**.

* In alternativa, selezionare **[!UICONTROL Experimentation Accelerator]** dal commutatore App.

Gli utenti con una sola licenza di Target possono accedervi solo tramite il selettore App.

<!--
<table style="table-layout:fixed"><tr style="border: 0;">
<td><img alt="Overview" href="experiment-accelerator-overview.md" src="assets/do-not-localize/experiments-2.jpeg">
<div align="center"><p><strong><a href="experiment-accelerator-overview.md">Overview</a></strong></p></div></td>
<td><img alt="Experiments" href="experiment-accelerator-monitor.md" src="assets/do-not-localize/experiment-overview.jpeg">
<div align="center"><p><strong><a href="experiment-accelerator-monitor.md">Experiments</a></strong></p></div></td>
<td><img alt="Metrics" href="experiment-accelerator-metrics.md" src="assets/do-not-localize/experiment-metrics.png">
<div align="center"><p><strong><a href="experiment-accelerator-metrics.md">Metrics</a></strong></p></div></td>
</tr></table>
-->

## Cos’è il test A/B?

Il test A/B è il processo di confronto di due o più versioni di un elemento per determinare quali prestazioni sono migliori rispetto a un obiettivo definito.

I partecipanti vengono assegnati in modo casuale a una versione, nota come variante, e il loro comportamento viene tracciato. I risultati mostrano se una versione ha prestazioni statisticamente superiori alle altre.

## Terminologia chiave

| Termine | Definizione |
|-|-|
| Controllo | Versione originale utilizzata come base di confronto. |
| Variante o trattamento | Nuova versione creata per il test rispetto al controllo. |
| Ipotesi | Una previsione su quali cambiamenti produrranno un risultato migliore, e perché. |
| Dimensione campione | Il numero di individui o sessioni inclusi nel test. |
| Significatività statistica | Misura di affidabilità che i risultati non sono dovuti a casualità. |
| Incremento | Miglioramento o declino percentuale di una variante rispetto al controllo. |
| Metrica primaria | La misura principale utilizzata per determinare il successo del test. |
| Metriche secondarie | Metriche di supporto che offrono insight aggiuntivo o monitoraggio per rilevare effetti indesiderati. |
| Intervallo di affidabilità | L’intervallo stimato entro il quale è probabile che il vero effetto diminuisca. |
| Segmento | Un sottoinsieme specifico del pubblico analizzato in modo indipendente (ad esempio, nuovi utenti, visitatori mobili). |

## Best practice per l’esecuzione di esperimenti

* **Inizia con un&#39;ipotesi chiara**

  Un&#39;ipotesi forte include cosa stai cambiando, cosa ti aspetti che accada e perché.
Esempio: _Si ritiene che la modifica di X determinerà un aumento di Y a causa di Z._

* **Definire una metrica di successo significativa**

  Scegli una metrica che sia allineata ai tuoi obiettivi più ampi. Evita metriche &quot;vanity&quot; dall’aspetto positivo ma che non riflettono l’impatto reale.

* **Verifica una modifica alla volta (quando possibile)**

  L’isolamento delle variabili semplifica l’interpretazione accurata dei risultati. Se esegui il test di più modifiche contemporaneamente, potresti non sapere cosa ha causato l’effetto.

* **Eseguire il test abbastanza a lungo**

  Conclusioni premature possono essere fuorvianti. Prima di agire, attendi una dimensione del campione statisticamente significativa.

* **Presta attenzione ai fattori esterni**

  La stagionalità, le festività e altri cambiamenti nell’ambiente possono distorcere i risultati. Documenta tutto ciò che potrebbe influenzare il comportamento durante il test.

* **Utilizza la segmentazione con attenzione**

  La suddivisione dei risultati per segmento di pubblico può rivelare pattern nascosti, ma evitare di interpretare in modo eccessivo piccole dimensioni del campione.

* **Documenta e condividi gli insegnamenti**

  Conserva un registro chiaro di ciò che è stato testato, perché e ciò che hai imparato. Questo costruisce la conoscenza istituzionale e previene gli errori ripetuti.

## Metriche comuni

| Metrica | Cosa Misura | Quando utilizzare |
|-|-|-|
| Tasso di conversione | Percentuale di utenti che completano l&#39;azione desiderata | Utile per monitorare il successo di un’esperienza basata su obiettivi |
| Percentuale di click-through (CTR) | Percentuale di utenti che fanno clic su un elemento specifico | Indica quanto è coinvolgente l&#39;esperienza |
| Tasso di coinvolgimento | Livello di interazione degli utenti con l’esperienza | Ideale per misurare l’interesse o l’attenzione |
| Percentuale non recapitate | Percentuale di utenti che escono rapidamente senza intervenire | Può indicare un’esperienza di scarsa vestibilità o confusione |
| Tempo sulla pagina | La quantità di tempo che gli utenti trascorrono su una parte specifica dell’esperienza | Può riflettere profondità di interesse o complessità |
| Ricavo per visitatore (RPV) | Ricavi medi ottenuti per utente | Spesso utilizzato in esperimenti incentrati sul commercio |
| Tasso di conservazione | Percentuale di utenti che restituiscono o rimangono coinvolti nel tempo | Utile per valutazioni a lungo termine |

## Cosa rende un buon esperimento?

Un buon esperimento non produce solo una vittoria, produce un apprendimento chiaro e actionable.
Ecco cosa cercare:

&amp;check; **Affidabilità statistica**: è improbabile che la differenza tra le varianti sia dovuta al caso.
&amp;check; **Allineamento con obiettivi**: la metrica principale riflette i progressi significativi verso un obiettivo aziendale.
&amp;check; **Impatto secondario**: nessun effetto collaterale negativo significativo sulle metriche correlate.
&amp;check; **Scalabilità**: il risultato può informare decisioni future o essere generalizzato in altre aree.
&amp;check; **Chiarezza**: la causa del risultato è ragionevolmente isolata e compresa.

La sperimentazione non consiste solo nel trovare la versione &quot;migliore&quot;, ma nel costruire la conoscenza attraverso test e iterazioni. Se eseguiti correttamente, gli esperimenti rivelano informazioni che guidano decisioni più intelligenti, esperienze utente migliori e risultati migliorati.

>[!BEGINSHADEBOX]

**Esempio:**

* **Società**: catena alberghiera
* **Ipotesi**: se si utilizza un linguaggio più urgente nella home page, verranno effettuate più prenotazioni.
   * **Controllo**: versione originale
   * **Variante**: aggiunta nuova versione con urgenza
   * **Metrica principale**: tariffa di prenotazione
   * **Metriche secondarie**: percentuale di mancato recapito, tempo sul sito
* **Risultato**: la variante ha prodotto un incremento del 14% nella tariffa di prenotazione, senza variazioni negative in altre metriche.
* **Azione**: valuta l&#39;implementazione della variante e l&#39;esecuzione di esperimenti di follow-up per testare approcci simili in altre aree.

>[!ENDSHADEBOX]
