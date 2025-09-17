---
solution: Journey Optimizer
product: journey optimizer
title: Best practice per Journey Optimizer Experimentation Accelerator
description: Migliora la tua capacità di condurre esperimenti in modo efficace e generare informazioni
feature: Experimentation
topic: Content Management
role: User
level: Beginner
keywords: contenuto, esperimento, multiplo, pubblico, trattamento
hide: true
hidefromtoc: true
source-git-commit: ddeb3512fbe1d1de86456fe2c3ccd2b3805b5684
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 2%

---

# Best practice per Journey Optimizer Experimentation Accelerator {#content-experiment-best-practices}

>[!BEGINSHADEBOX]

* [Introduzione a Journey Optimizer Experimentation Accelerator](experiment-accelerator.md)
* **[Best practice per Journey Optimizer Experimentation Accelerator](experiment-accelerator-best-practices.md)**
* [Privacy, sicurezza e governance in Journey Optimizer Experimentation Accelerator](experiment-accelerator-security.md)
* [Monitorare gli esperimenti](experiment-accelerator-monitor.md)
* [Metriche della sperimentazione](experiment-accelerator-metrics.md)

>[!ENDSHADEBOX]

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
