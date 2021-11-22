---
title: Introduzione all’esportazione del catalogo delle offerte
description: In questa sezione sono elencati tutti i campi utilizzati nel set di dati esportato per le decisioni.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 064762b7-9774-42eb-bcef-1d92bc94a988
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '1550'
ht-degree: 0%

---

# Set di dati sulle decisioni {#decisions-dataset}

Ogni volta che un’offerta viene modificata, viene aggiornato il set di dati generato automaticamente per le decisioni (precedentemente noto come attività).

![](../../assets/dataset-activities.png)

Il batch di successo più recente nel set di dati viene visualizzato a destra. La visualizzazione gerarchica dello schema per il set di dati viene visualizzata nel riquadro a sinistra.

>[!NOTE]
>
>Scopri come accedere ai set di dati esportati per ciascun oggetto della Libreria offerte in [questa sezione](../export-catalog/access-dataset.md).

Elenco di tutti i campi che possono essere utilizzati nella **[!UICONTROL Decision Object Repository - Decisions]** set di dati (precedentemente noto come archivio oggetti decisionali - Attività).

<!--A decision (formerly known as offer decision) is used to control the decisioning process. It specifies the filter applied to the total inventory to narrow down offers by topic/category, the placement to narrow down the inventory to those offers that technically fit into the reserved space for the offer and specifies a fallback option should the combined constraints disqualify all available personalization offers.-->

## Identificatore

**Campo:** _id
**Titolo:** Identificatore
**Descrizione:** Identificatore univoco del record.
**Tipo:** string

## _esperienza

**Campo:** _esperienza
**Tipo:** oggetto

### _esperienza > decisionale

**Campo:** decisione
**Tipo:** oggetto

#### _esperienza > decisioni > criteri

**Campo:** criteri
**Titolo:** Criteri
**Descrizione:** Definisce un insieme di criteri decisionali in cui ciascuno contiene un insieme di vincoli.
**Tipo:** array

**_esperienza > decisioni > criteri > descrizione**

**Campo:** descrizione
**Titolo:** Descrizione
**Descrizione:** Descrizione del criterio. Viene utilizzato per comunicare le intenzioni comprensibili all&#39;uomo su come o perché questo criterio è stato elaborato e come influisce sulla decisione.
**Tipo:** string

**_esperienza > decisione > criteri > opzioneSelezione**

**Campo:** optionSelection
**Titolo:** Selezione dell&#39;opzione
**Descrizione:** La selezione delle opzioni definisce la validità/applicabilità delle opzioni in questo contesto.
**Tipo:** oggetto

* **Descrizione**

   **Campo:** descrizione
   **Titolo:** Descrizione
   **Descrizione:** Descrizione selezione opzione. Viene utilizzato per comunicare le intenzioni di lettura umana su come o perché è stata costruita questa selezione di opzioni e/o quale opzione corrisponderà.
   **Tipo:** string

* **Filtro opzione**

   **Campo:** filter
   **Titolo:** Filtro opzione
   **Descrizione:** Il riferimento a un filtro basato su tag che corrisponde alle opzioni di un inventario utilizzando i relativi tag allegati. Il valore è l&#39;URI (@id) della regola decisionale a cui si fa riferimento. Vedi schema https://ns.adobe.com/experience/decisioning/filter.
   **Tipo:** string

* **Tipo di vincolo del profilo**

   **Campo:** optionSelectionType
   **Titolo:** Tipo di vincolo del profilo
   **Descrizione:** Determina se sono attualmente impostati vincoli e come vengono espressi i vincoli. Potrebbe essere attraverso una query di filtro o attraverso una o più appartenenze al segmento.
   **Tipo:** string
   **Valori possibili:** &quot;none&quot; (predefinito), &quot;directList&quot;, &quot;filter&quot;

* **Elenco opzioni**

   **Campo:** options
   **Titolo:** Elenco opzioni
   **Descrizione:** Elenco che specifica direttamente le opzioni senza valutare una query di filtro. È possibile specificare un elenco di opzioni o una regola di filtro opzioni.
   **Tipo:** array

   <!--Missing title under Option List? Desc = An identifier of an decision option entity. The value value refers to an `@id` property of a decision option. Type: string-->

**_esperienza > decisioni > criteri > posizionamenti**

**Campo:** posizionamenti
**Titolo:** Restrizioni di posizionamento
**Descrizione:** Il vincolo di posizionamento indica che questo criterio è applicabile solo per i posizionamenti elencati. Solo quando il posizionamento di destinazione è nel `xdm:placements` elenco è la selezione di opzioni considerata. In caso contrario, vengono ignorati tutti i criteri decisionali. Quando l’elenco &quot;xdm:placements&quot; viene omesso o lasciato vuoto, il criterio viene considerato per qualsiasi posizionamento mirato. I posizionamenti qui elencati impongono criteri impliciti per la selezione dell’opzione. Un’opzione da considerare deve avere una rappresentazione per il posizionamento mirato.
**Tipo:** array

* **Identificatore di posizionamento**

   **Titolo:** Identificatore di posizionamento
   **Descrizione:** Un riferimento a un’entità di posizionamento. Il valore è l’URI (@id) del posizionamento a cui si fa riferimento. Vedi schema https://ns.adobe.com/experience/decisioning/placement.
   **Tipo:** string

**_esperienza > decisioni > criteri > profileConstraints**

**Campo:** profileConstraints
**Titolo:** Vincolo profilo
**Descrizione:** Il vincolo di profilo decide se una selezione di opzioni è attualmente idonea per questa identità di profilo, in questo contesto. Se il vincolo di profilo non deve considerare i valori di ciascuna opzione, ovvero non è necessariamente una delle opzioni della selezione dell’opzione, il vincolo di profilo che restituisce &quot;false&quot; annulla l’intera selezione dell’opzione. D&#39;altra parte, viene valutata una regola di vincolo di profilo che utilizza un&#39;opzione come parametro per ogni opzione di qualificazione della selezione di opzione.
**Tipo:** oggetto

* **_esperienza > decisioni > criteri > profileConstraints > Descrizione**

   **Campo:** descrizione
   **Titolo:** Descrizione
   **Descrizione:** Descrizione del vincolo di profilo. Viene utilizzato per comunicare le intenzioni leggibili dell’uomo su come o perché è stato costruito questo vincolo di profilo e/o quale opzione sarà inclusa o esclusa da esso.
   **Tipo:** string

* **_esperienza > decisione > criteri > profileConstraints > Regola di idoneità**

   **Campo:** adaptRule
   **Titolo:** Regola di idoneità
   **Descrizione:** Un riferimento a una regola decisionale che restituisce true o false per un determinato profilo e/o altri oggetti XDM contestuali specificati. La regola viene utilizzata per decidere se l’opzione è idonea per un determinato profilo. Il valore è l&#39;URI (@id) della regola decisionale a cui si fa riferimento. Vedi schema https://ns.adobe.com/experience/decisioning/rule.
   **Tipo:** string

* **_esperienza > decisione > criteri > profileConstraints > Tipo di vincolo del profilo**

   **Campo:** profileConstraintType
   **Titolo:** Tipo di vincolo del profilo
   **Descrizione:** Determina se sono attualmente impostati vincoli e come vengono espressi i vincoli. Potrebbe essere attraverso una regola o attraverso una o più appartenenze al segmento.
   **Tipo:** string
   **Valori possibili:**
   * &quot;none&quot; (predefinito)
   * &quot;criteri di idoneità&quot;: &quot;Il vincolo di profilo è espresso come una singola regola che deve essere valutata come true prima che l&#39;azione vincolata sia consentita.&quot;
   * &quot;anySegments&quot;: &quot;Il vincolo di profilo è espresso come uno o più segmenti e il profilo deve essere un membro di almeno uno di essi prima che l’azione vincolata sia consentita.&quot;
   * &quot;allSegments&quot;: &quot;Il vincolo di profilo è espresso come uno o più segmenti e il profilo deve essere un membro di tutti i segmenti prima che l’azione vincolata sia consentita.&quot;
   * &quot;regole&quot;: &quot;Il vincolo di profilo è espresso come una serie di regole diverse, ad esempio idoneità, applicabilità, idoneità, che tutte devono valutare in true prima che l&#39;azione vincolata sia consentita.&quot;

* **_esperienza > decisioni > criteri > profileConstraints > segmentIdentities**

   **Campo:** segmentIdentities
   **Titolo:** Identificatori dei segmenti
   **Descrizione:** Identificatori dei segmenti.
   **Tipo:** array

   * **Identificatore**

      **Campo:** _id
      **Titolo:** Identificatore
      **Descrizione:** Identità del segmento nello spazio dei nomi correlato.
      **Tipo:** string

   * **namespace**

      **Campo:** namespace
      **Titolo:** Namespace
      **Descrizione:** Lo spazio dei nomi associato al `xid` attributo.
      **Tipo:** oggetto
      **Obbligatorio:** &quot;code&quot;

      * **Codice**

         **Campo:** codice
         **Titolo:** Codice
         **Descrizione:** Il codice è un identificatore leggibile dall’utente per lo spazio dei nomi e può essere utilizzato per richiedere l’ID tecnico dello spazio dei nomi utilizzato per l’elaborazione del grafico delle identità.
         **Tipo:** string
   * **Identificatore esperienza**

      **Campo:** xid
      **Titolo:** Identificatore esperienza
      **Descrizione:** Se presente, questo valore rappresenta un identificatore dello spazio dei nomi incrociato univoco per tutti gli identificatori con ambito dello spazio dei nomi in tutti i namespace.
      **Tipo:** string


**_esperienza > decisionale > criteri > classificazione**

**Campo:** classificazione
**Titolo:** Dettagli classificazione
**Descrizione:** Classificazione (priorità). Definisce come viene determinata la \&quot;opzione migliore\&quot; in base al contesto del criterio di decisione. Tra tutte le opzioni selezionate che soddisfano i vincoli del profilo, la classificazione deciderà l’opzione o le opzioni superiori N da proporre.
**Tipo:** oggetto

* **_esperienza > decisionale > criteri > classificazione > ordine**

   **Campo:** ordine
   **Titolo:** Valutazione ordine
   **Descrizione:** Valutazione di un ordine relativo di una o più opzioni decisionali. Le opzioni con valori ordinali più alti vengono selezionate su qualsiasi opzione con valori ordinali più bassi. I valori determinati con questo metodo possono essere ordinati, ma le distanze tra di essi non possono essere misurate né le somme né i prodotti possono essere calcolati. La mediana e la modalità sono le uniche misure di tendenza centrale che possono essere utilizzate per i dati ordinali.
   **Tipo:** oggetto

   * **Funzione di punteggio**

      **Campo:** Funzione
      **Titolo:** Funzione di punteggio
      **Descrizione:** Riferimento a una funzione che calcola un punteggio numerico per questa opzione di decisione. Le opzioni di decisione saranno quindi ordinate (classificate) in base a quel punteggio. Il valore di questa proprietà è l&#39;URI (@id) della funzione da richiamare con l&#39;opzione on alla volta. Vedi schema https://ns.adobe.com/experience/decisioning/function.
      **Tipo:** string

   * **Tipo di valutazione ordine**

      **Campo:** orderEvaluationType
      **Titolo:** Tipo di valutazione ordine
      **Descrizione:** Specifica quale meccanismo di valutazione dell&#39;ordine viene utilizzato, priorità statica delle opzioni di decisione, una funzione di punteggio che calcola un valore numerico per ogni opzione o una strategia di classificazione che riceve un elenco per ordinarlo.
      **Tipo:** string
      **Valori possibili:** &quot;static&quot;, &quot;scoringFunction&quot;, &quot;rankingStrategy&quot;

   * **Strategia di classificazione**

      **Campo:** rankingStrategy
      **Titolo:** Strategia di classificazione
      **Descrizione:** Riferimento a una strategia che classifica un elenco di opzioni decisionali. Le opzioni di decisione verranno restituite in un elenco ordinato. Il valore di questa proprietà è l&#39;URI (@id) della funzione da richiamare con l&#39;opzione on alla volta. Vedi schema https://ns.adobe.com/experience/decisioning/rankingStrategy.
      **Tipo:** string

* **_esperienza > decisionale > criteri > classificazione > Priorità**

   **Campo:** priorità
   **Titolo:** Priorità
   **Descrizione:** La priorità di un&#39;unica opzione di decisione rispetto a tutte le altre opzioni. Le opzioni per le quali non viene specificata alcuna funzione di ordine vengono definite come priorità utilizzando questa proprietà. Le opzioni con valori di priorità più elevati vengono selezionate prima di qualsiasi opzione di priorità più bassa. Se due o più opzioni qualificate condividono il valore di priorità più elevato, una viene scelta in modo casuale uniforme e utilizzata per la proposta di decisione.
   **Tipo:** integer
   **Valore minimo:** 0
   **Valore predefinito:** 0

#### _esperienza > decisionale > Data e ora di fine attività

**Campo:** endTime
**Titolo:** Data e ora di fine attività
**Descrizione:** Data e ora di fine della decisione (precedentemente nota come attività). La proprietà ha la semantica della proprietà &#39;endTime&#39; di schema.org definita su http://schema.org/Action.
**Tipo:** string

#### _esperienza > decisionale > Opzione di fallback

**Campo:** fallback
**Titolo:** Opzione di fallback
**Descrizione:** Il riferimento a un&#39;opzione di fallback utilizzata quando si prende una decisione nel contesto di questa decisione non qualifica nessuna delle opzioni regolari (questo accade in genere quando si applicano vincoli rigidi). Il valore è l’URI (@id) dell’opzione di fallback a cui si fa riferimento.
**Tipo:** string

#### _esperienza > decisionale > Nome attività

**Campo:** name
**Titolo:** Nome attività
**Descrizione:** Nome della decisione (precedentemente noto come attività) visualizzato in diverse interfacce utente.
**Tipo:** string

#### _esperienza > decisionale > Data e ora di inizio attività

**Campo:** startTime
**Titolo:** Data e ora di inizio attività
**Descrizione:** Data e ora di inizio e di fine della decisione (precedentemente nota come attività). La proprietà ha la semantica della proprietà &#39;startTime&#39; di schema.org definita su http://schema.org/Action.
**Tipo:** string

## _repo

**Campo:** _repo
**Tipo:** oggetto

### _repo > Attività ETag

**Campo:** etag
**Titolo:** Attività ETag
**Descrizione:** Revisione in cui si trovava l&#39;oggetto decisione (precedentemente noto come attività) al momento dell&#39;esecuzione dello snapshot.
**Tipo:** string
