---
title: Calcoli statistici utilizzati nel rapporto sulla sperimentazione
description: Ulteriori informazioni sui test A/B e sui slot machine
feature: A/B Testing, Experimentation
role: User
level: Experienced
source-git-commit: 397fad9c95e0c11c0496ab5c9adfb6f8169de4f6
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 2%

---

# Esperimenti A/B vs slot machine {#mab-vs-ab}

<!--
>[!CONTEXTUALHELP]
>id="ajo_ab_test_mab"
>title="Experiment type"
>abstract="Experiment type determines how traffic is allocated between treatments during your test. Choose the method that best aligns with your goals:</br>
>
>* **A/B Experiment**: Splits traffic as you define between treatments and measures performance until results are statistically significant. Best for learning which treatment performs better in a controlled comparison.
>
>* **Multi-armed Bandit**: Shifts traffic toward higher-performing treatments as data is collected, balancing speed and optimization. Useful when you want to maximize conversions during the experiment.
>
>* **Bring your own Multi-armed Bandit**: Use your own algorithm to decide traffic allocation, giving you flexibility if you have a custom model or strategy."
-->

Questa pagina fornisce un confronto dettagliato degli esperimenti **A/B** e **Multi-Armed Bandit**, illustrandone i rispettivi punti di forza, limitazioni e scenari in cui ogni approccio è più efficace.

## A/B {#ab-test}

Il tradizionale esperimento A/B prevede la suddivisione del traffico equamente tra i trattamenti e il mantenimento di questa allocazione fino alla conclusione dell’esperimento. Una volta raggiunta la significatività statistica, il trattamento vincente viene identificato e successivamente scalato.

### Vantaggi

I punti di forza del tradizionale esperimento A/B sono:

* **Rigore Statistico**

  La struttura fissa fornisce tassi di errore e intervalli di affidabilità ben definiti.

  I framework di test delle ipotesi, ad esempio un livello di affidabilità del 95%, sono più facili da applicare e interpretare.

  Esperimenti con potenza adeguata riducono la probabilità di falsi positivi.

* **Semplicità**

  La metodologia è semplice da progettare ed eseguire.

  I risultati possono essere comunicati chiaramente alle parti interessate non tecniche.

* **Raccolta dati completa**

  Ogni trattamento riceve un’esposizione adeguata, che consente l’analisi non solo della variante vincente, ma anche delle alternative poco performanti.

  Queste informazioni aggiuntive possono orientare le decisioni strategiche a lungo termine.

* **Controllo Bias**

  L&#39;allocazione fissa riduce la suscettibilità a distorsioni come la &quot;maledizione del vincitore&quot; o la regressione alla media.

### Limitazioni

I principali limiti dell’esperimento A/B tradizionale sono:

* **Costo opportunità**

  Una parte sostanziale del traffico è diretta verso trattamenti inferiori, riducendo potenzialmente le conversioni o i ricavi durante il test.

  Il trattamento vincente non può essere implementato fino alla conclusione dell’esperimento.

* **Requisito durata fissa**

  I test devono in genere essere eseguiti per il loro orizzonte predefinito, anche se le condizioni esterne, ad esempio la stagionalità, i cambiamenti di mercato, cambiano a metà percorso.

  L’adattamento durante l’esperimento è limitato.

## Slot machine {#mab-experiment}

Gli algoritmi slot machine utilizzano l’allocazione adattiva: con l’accumularsi delle prove, viene indirizzato più traffico verso trattamenti con prestazioni migliori. L’obiettivo è massimizzare il premio cumulativo durante l’esperimento anziché concentrarsi esclusivamente sul risultato finale.

### Vantaggi

I punti di forza principali dei metodi di slot machine sono:

* **Ottimizzazione più rapida**

  I trattamenti promettenti hanno priorità prima, migliorando le prestazioni complessive durante il test.

* **Adattabilità**

  Le allocazioni vengono aggiornate continuamente durante la raccolta dei dati, rendendo la slot machine adatta per ambienti dinamici.

* **Costo opportunità ridotto**

  I trattamenti scadenti vengono eliminati rapidamente, riducendo al minimo lo spreco di traffico.

* **Idoneità al testing continuo**

  Efficace per la sperimentazione in corso o in contesti in cui il traffico è costoso.

### Limitazioni

Le principali limitazioni dei metodi di slot machine sono:

* **Garanzie statistiche più deboli**

  Il tradizionale test delle ipotesi è più difficile da applicare e le regole di interruzione sono meno chiare.

* **Trasparenza ridotta**

  L’allocazione adattiva può essere difficile da spiegare alle parti interessate.

* **Informazioni limitate sui trattamenti insoddisfacenti**

  I trattamenti deboli ricevono una bassa esposizione, limitando l&#39;insight diagnostico.

* **Complessità dell&#39;implementazione**

  Richiede algoritmi e infrastrutture avanzati, con un maggiore rischio di errori di configurazione.

## Quando utilizzare A/B rispetto a slot machine

| Scenario | Metodo consigliato |
|-|-|
| Stai eseguendo test esplorativi o di ricerca | A/B |
| Stai eseguendo campagne sempre attive, ad esempio annunci e consigli | slot machine |
| Desideri massimizzare le conversioni durante il test | slot machine |
| Desideri informazioni chiare e sicure | A/B |
| È necessario adattarsi rapidamente, ad esempio per i turni stagionali | slot machine |
| Hai traffico limitato e desideri ottimizzare rapidamente il ritorno sull’investimento | slot machine |
| Hai traffico elevato e puoi permetterti un apprendimento più lento | A/B |
| Le parti interessate hanno bisogno di punti decisionali chiari | A/B |

