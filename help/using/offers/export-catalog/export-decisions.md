---
title: Introduzione all’esportazione del catalogo delle offerte
description: In questa sezione sono elencati tutti i campi utilizzati nel set di dati esportato per le decisioni.
feature: Offerte
topic: Integrazioni
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '1552'
ht-degree: 1%

---

# Set di dati sulle decisioni {#decisions-dataset}

Ogni volta che un’offerta viene modificata, viene aggiornato il set di dati generato automaticamente per le decisioni (precedentemente noto come attività).

![](../../assets/dataset-activities.png)

Il batch di successo più recente nel set di dati viene visualizzato a destra. La visualizzazione gerarchica dello schema per il set di dati viene visualizzata nel riquadro a sinistra.

>[!NOTE]
>
>Scopri come accedere ai set di dati esportati per ciascun oggetto della Libreria offerte in [questa sezione](../export-catalog/access-dataset.md).

Elenco di tutti i campi che possono essere utilizzati nel set di dati **[!UICONTROL Decision Object Repository - Decisions]** (precedentemente noto come Archivio oggetti decisionali - Attività).

<!--A decision (formerly known as offer decision) is used to control the decisioning process. It specifies the filter applied to the total inventory to narrow down offers by topic/category, the placement to narrow down the inventory to those offers that technically fit into the reserved space for the offer and specifies a fallback option should the combined constraints disqualify all available personalization offers.-->

## Identificatore

**Campo:** _id 
**Titolo:** Identificatore 
**Descrizione:** un identificatore univoco per il record.
**Tipo:** stringa

## _esperienza

**Campo:** _experience 
**Type:** object

### _esperienza > decisionale

**Campo:** 
**tipo di decisione:** oggetto

#### _esperienza > decisioni > criteri

**Campo:** criteri 
**Titolo:** Criteri 
**Descrizione:** definisce un set di criteri decisionali in cui ciascuno contiene un set di vincoli.
**Tipo:** array

**_esperienza > decisioni > criteri > descrizione**

**Campo:** descrizione 
**Titolo:** Descrizione 
**Descrizione:** descrizione criterio. Viene utilizzato per comunicare le intenzioni comprensibili all&#39;uomo su come o perché questo criterio è stato elaborato e come influisce sulla decisione.
**Tipo:** stringa

**_esperienza > decisione > criteri > opzioneSelezione**

**Campo:** opzione
**Titolo selezione:** Selezione opzione 
**Descrizione:** la selezione dell’opzione definisce la validità/applicabilità delle opzioni in questo contesto.
**Tipo:** oggetto

* **Descrizione**

   **Campo:** descrizione
   **Titolo:** Descrizione
   **Descrizione:** descrizione della selezione dell’opzione. Viene utilizzato per comunicare le intenzioni di lettura umana su come o perché è stata costruita questa selezione di opzioni e/o quale opzione corrisponderà.
   **Tipo:** stringa

* **Filtro opzione**

   **Campo:** filtro
   **Titolo:** Filtro opzione
   **Descrizione:** il riferimento a un filtro basato su tag che corrisponde alle opzioni di un inventario utilizzando i relativi tag allegati. Il valore è l&#39;URI (@id) della regola decisionale a cui si fa riferimento. Vedi schema https://ns.adobe.com/experience/decisioning/filter.
   **Tipo:** stringa

* **Tipo di vincolo del profilo**

   **Campo:** optionSelectionType
   **Titolo:** Tipo di vincolo del profilo
   **Descrizione:** determina se sono attualmente impostati dei vincoli e come vengono espressi i vincoli. Potrebbe essere attraverso una query di filtro o attraverso una o più appartenenze al segmento.
   **Tipo:** stringa
   **Valori possibili:** &quot;none&quot; (predefinito), &quot;directList&quot;, &quot;filter&quot;

* **Elenco opzioni**

   **Campo:** opzioni
   **Titolo:** Elenco opzioni
   **Descrizione:** elenco che specifica direttamente le opzioni senza valutare una query di filtro. È possibile specificare un elenco di opzioni o una regola di filtro opzioni.
   **Tipo:** array

   <!--Missing title under Option List? Desc = An identifier of an decision option entity. The value value refers to an `@id` property of a decision option. Type: string-->

**_esperienza > decisioni > criteri > posizionamenti**

**Campo:** posizionamenti 
**Titolo:** Restrizioni di posizionamento 
**Descrizione:** il vincolo di posizionamento indica che questo criterio è applicabile solo ai posizionamenti elencati. Solo quando il posizionamento di destinazione è nell’elenco `xdm:placements` è considerata la selezione di opzioni. In caso contrario, vengono ignorati tutti i criteri decisionali. Quando l’elenco &quot;xdm:placements&quot; viene omesso o lasciato vuoto, il criterio viene considerato per qualsiasi posizionamento mirato. I posizionamenti qui elencati impongono criteri impliciti per la selezione dell’opzione. Un’opzione da considerare deve avere una rappresentazione per il posizionamento mirato.
**Tipo:** array

* **Identificatore di posizionamento**

   **Titolo:** Identificatore di posizionamento
   **Descrizione:** un riferimento a un’entità di posizionamento. Il valore è l’URI (@id) del posizionamento a cui si fa riferimento. Vedi schema https://ns.adobe.com/experience/decisioning/placement.
   **Tipo:** stringa

**_esperienza > decisioni > criteri > profileConstraints**

**Campo:** profileConstraints 
**Titolo:** 
**Descrizione vincolo profilo:** il vincolo di profilo decide se una selezione di opzione è idonea per questa identità di profilo in questo momento, in questo contesto. Se il vincolo di profilo non deve considerare i valori di ciascuna opzione, ovvero non è necessariamente una delle opzioni della selezione dell’opzione, il vincolo di profilo che restituisce &quot;false&quot; annulla l’intera selezione dell’opzione. D’altro canto, viene valutata una regola di vincolo di profilo che utilizza un’opzione come parametro per ogni opzione di qualificazione della selezione dell’opzione.
**Tipo:** oggetto

* **_esperienza > decisioni > criteri > profileConstraints > Descrizione**

   **Campo:** descrizione
   **Titolo:** Descrizione
   **Descrizione:** descrizione del vincolo di profilo. Viene utilizzato per comunicare le intenzioni leggibili dell’uomo su come o perché è stato costruito questo vincolo di profilo e/o quale opzione sarà inclusa o esclusa da esso.
   **Tipo:** stringa

* **_esperienza > decisione > criteri > profileConstraints > Regola di idoneità**

   **Campo:** idoneitàRule
   **Titolo:** Regola di idoneità
   **Descrizione:** un riferimento a una regola decisionale che restituisce true o false per un determinato profilo e/o altri oggetti contestuali XDM. La regola viene utilizzata per decidere se l’opzione è idonea per un determinato profilo. Il valore è l&#39;URI (@id) della regola decisionale a cui si fa riferimento. Vedi schema https://ns.adobe.com/experience/decisioning/rule.
   **Tipo:** stringa

* **_esperienza > decisione > criteri > profileConstraints > Tipo di vincolo del profilo**

   **Campo:** profileConstraintType
   **Titolo:** Tipo di vincolo del profilo
   **Descrizione:** determina se sono attualmente impostati dei vincoli e come vengono espressi i vincoli. Potrebbe essere attraverso una regola o attraverso una o più appartenenze al segmento.
   **Tipo:** stringa
   **Valori possibili:**
   * &quot;none&quot; (predefinito)
   * &quot;criteri di idoneità&quot;: &quot;Il vincolo di profilo è espresso come una singola regola che deve essere valutata come true prima che l&#39;azione vincolata sia consentita.&quot;
   * &quot;anySegments&quot;: &quot;Il vincolo di profilo è espresso come uno o più segmenti e il profilo deve essere un membro di almeno uno di essi prima che l’azione vincolata sia consentita.&quot;
   * &quot;allSegments&quot;: &quot;Il vincolo di profilo è espresso come uno o più segmenti e il profilo deve essere un membro di tutti i segmenti prima che l’azione vincolata sia consentita.&quot;
   * &quot;regole&quot;: &quot;Il vincolo di profilo è espresso come una serie di regole diverse, ad esempio idoneità, applicabilità, idoneità, che tutte devono valutare in true prima che l&#39;azione vincolata sia consentita.&quot;

* **_esperienza > decisioni > criteri > profileConstraints > segmentIdentities**

   **Campo:** segmentIdentities
   **Titolo:** Identificatori di segmento
   **Descrizione:** identificatori dei segmenti.
   **Tipo:** array

   * **Identificatore**

      **Campo:** _id
      **Titolo:** Identificatore
      **Descrizione:** identità del segmento nello spazio dei nomi correlato.
      **Tipo:** stringa

   * **namespace**

      **Campo:** namespace
      **Titolo:** Namespace
      **Descrizione:** lo spazio dei nomi associato all’ `xid` attributo.
      **Tipo:** oggetto
      **Obbligatorio:** &quot;code&quot;

      * **Codice**

         **Campo:** codice
         **Titolo:** Codice
         **Descrizione:** il codice è un identificatore leggibile dall’utente per lo spazio dei nomi e può essere utilizzato per richiedere l’ID tecnico dello spazio dei nomi utilizzato per l’elaborazione del grafico delle identità.
         **Tipo:** stringa
   * **Identificatore esperienza**

      **Campo:** xid
      **Titolo:** identificatore esperienza
      **Descrizione:** se presente, questo valore rappresenta un identificatore cross-namespace univoco per tutti gli identificatori con ambito namespace in tutti i namespace.
      **Tipo:** stringa


**_esperienza > decisionale > criteri > classificazione**

**Campo:** 
**Titolo classificazione:** Dettagli classificazione 
**Descrizione:** Classifica (priorità). Definisce come viene determinata la \&quot;opzione migliore\&quot; in base al contesto del criterio di decisione. Tra tutte le opzioni selezionate che soddisfano i vincoli del profilo, la classificazione deciderà l’opzione o le opzioni superiori N da proporre.
**Tipo:** oggetto

* **_esperienza > decisionale > criteri > classificazione > ordine**

   **Campo:** ordine
   **Titolo:** Valutazione ordine
   **Descrizione:** Valutazione di un ordine relativo di una o più opzioni decisionali. Le opzioni con valori ordinali più alti vengono selezionate su qualsiasi opzione con valori ordinali più bassi. I valori determinati con questo metodo possono essere ordinati, ma le distanze tra di essi non possono essere misurate né le somme né i prodotti possono essere calcolati. La mediana e la modalità sono le uniche misure di tendenza centrale che possono essere utilizzate per i dati ordinali.
   **Tipo:** oggetto

   * **Funzione di punteggio**

      **Campo:** funzione
      **Titolo:** Funzione di punteggio
      **Descrizione:** un riferimento a una funzione che calcola un punteggio numerico per questa opzione di decisione. Le opzioni di decisione saranno quindi ordinate (classificate) in base a quel punteggio. Il valore di questa proprietà è l&#39;URI (@id) della funzione da richiamare con l&#39;opzione on alla volta. Vedi schema https://ns.adobe.com/experience/decisioning/function.
      **Tipo:** stringa

   * **Tipo di valutazione ordine**

      **Campo:** orderEvaluationType
      **Titolo:** Tipo di valutazione ordine
      **Descrizione:** specifica quale meccanismo di valutazione dell’ordine viene utilizzato, priorità statica delle opzioni di decisione, una funzione di punteggio che calcola un valore numerico per ogni opzione o una strategia di classificazione che riceve un elenco per ordinarlo.
      **Tipo:** stringa
      **Valori possibili:** &quot;static&quot;, &quot;scoringFunction&quot;, &quot;rankingStrategy&quot;

   * **Strategia di classificazione**

      **Campo:** rankingStrategy
      **Titolo:** Strategia di classificazione
      **Descrizione:** un riferimento a una strategia che classifica un elenco di opzioni decisionali. Le opzioni di decisione verranno restituite in un elenco ordinato. Il valore di questa proprietà è l&#39;URI (@id) della funzione da richiamare con l&#39;opzione on alla volta. Vedi schema https://ns.adobe.com/experience/decisioning/rankingStrategy.
      **Tipo:** stringa

* **_esperienza > decisionale > criteri > classificazione > Priorità**

   **Campo:** priorità
   **Titolo:** Priorità
   **Descrizione:** la priorità di una singola opzione di decisione rispetto a tutte le altre opzioni. Le opzioni per le quali non è specificata alcuna funzione di ordine hanno priorità utilizzando questa proprietà. Le opzioni con valori di priorità più elevati vengono selezionate prima di qualsiasi opzione di priorità più bassa. Se due o più opzioni qualificate condividono il valore di priorità più elevato, una viene scelta in modo casuale uniforme e utilizzata per la proposta di decisione.
   **Tipo:** integer
   **Valore minimo:** 0
   **Valore predefinito:** 0

#### _esperienza > decisionale > Data e ora di fine attività

**Campo:** endTime 
**Title:** Activity End Date and Time 
**Description:** Decision (in precedenza noto come activity) end date and end time (Data e ora di fine attività). La proprietà ha la semantica della proprietà &#39;endTime&#39; di schema.org definita su http://schema.org/Action.
**Tipo:** stringa

#### _esperienza > decisionale > Opzione di fallback

**Campo:** 
**Titolo di fallback:** Opzione di fallback 
**Descrizione:** il riferimento a un&#39;opzione di fallback utilizzata quando si prendono decisioni nel contesto di questa decisione non qualifica nessuna delle opzioni regolari (questo accade in genere quando si applicano vincoli rigidi). Il valore è l’URI (@id) dell’opzione di fallback a cui si fa riferimento.
**Tipo:** stringa

#### _esperienza > decisionale > Nome attività

**Campo:** nome 
**Titolo:** Nome attività 
**Descrizione:** nome della decisione (precedentemente noto come attività) visualizzato in varie interfacce utente.
**Tipo:** stringa

#### _esperienza > decisionale > Data e ora di inizio attività

**Campo:** startTime 
**Title:** Activity Start Date and Time 
**Description:** Decision (in precedenza noto come activity) start date and end time. La proprietà ha la semantica della proprietà &#39;startTime&#39; di schema.org definita su http://schema.org/Action.
**Tipo:** stringa

## _repo

**Campo:** _repo 
**Type:** object

### _repo > Attività ETag

**Campo:** 
**Titolo tag:** Attività ETag 
**Descrizione:** La revisione in cui si trovava l&#39;oggetto decisione (precedentemente noto come attività) al momento dell&#39;istantanea.
**Tipo:** stringa
