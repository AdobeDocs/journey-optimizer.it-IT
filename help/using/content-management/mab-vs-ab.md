---
title: Calcoli statistici utilizzati nel rapporto sulla sperimentazione
description: Ulteriori informazioni sui test A/B e sui slot machine
feature: A/B Testing, Experimentation
role: User
level: Experienced
exl-id: 1f7b74d2-77c3-4113-8e6a-1e2a95117748
TQID: https://experienceleague.adobe.com/47tFiWTUUsGUMeWhuJVQnakAIrgz1Ax1mO-u8pf27uc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: []
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
subfeature_v2:
  - id: f29a52db-c90c-4345-902e-b586d1406d8d
source-git-commit: dc3ac795cd3cbfbd3dd3adfe6f220641d331081f
workflow-type: tm+mt
source-wordcount: 658
ht-degree: 18%

---

# Esperimenti A/B e Multi-armed bandit {#mab-vs-ab}

>[!BEGINSHADEBOX]

**In questa pagina:** Confronta gli esperimenti A/B e slot machine in Adobe Journey Optimizer, inclusi i relativi punti di forza, limitazioni e scenari in cui ogni metodo di allocazione del traffico funziona al meglio.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_ab_test_mab"
>title="Tipo di esperimento"
>abstract="Il tipo di esperimento determina il modo in cui il traffico viene allocato tra i vari trattamenti durante il test. Scegli il metodo che meglio si allinea agli obiettivi:</br><b>Esperimento A/B</b>: divide il traffico mentre definisci tra trattamenti e misurazioni delle prestazioni, fino a ottenere risultati statisticamente significativi. Ideale per capire quale trattamento offre prestazioni migliori in un confronto controllato.</br><b>Multi-armed bandit</b>: sposta il traffico verso i trattamenti con prestazioni migliori man mano che vengono raccolti i dati, in modo da bilanciare velocità e ottimizzazione. Utile quando desideri ottimizzare le conversioni durante l’esperimento.</br><b>Multi-armed bandit proprio</b>: utilizza un tuo algoritmo per decidere l’allocazione del traffico, per intervenire con flessibilità se disponi di una strategia o di un modello personalizzato."

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
