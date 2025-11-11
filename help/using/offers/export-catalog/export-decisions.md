---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Set di dati sulle decisioni
description: Questa sezione elenca tutti i campi utilizzati nel set di dati esportato per le decisioni
badge: label="Legacy" type="Informative"
feature: Decision Management, Datasets
topic: Integrations
role: User, Developer
level: Intermediate
exl-id: 064762b7-9774-42eb-bcef-1d92bc94a988
version: Journey Orchestration
source-git-commit: d6a9a8a392f0492aa6e4f059198ce77b6b2cd962
workflow-type: tm+mt
source-wordcount: '1530'
ht-degree: 0%

---

# Set di dati sulle decisioni {#decisions-dataset}

Ogni volta che viene modificata un’offerta, il set di dati generato automaticamente per le decisioni viene aggiornato.

![](../assets/dataset-activities.png)

Il batch con esito positivo più recente nel set di dati viene visualizzato a destra. La visualizzazione gerarchica dello schema per il set di dati viene visualizzata nel riquadro a sinistra.

>[!NOTE]
>
>Scopri come accedere ai set di dati esportati per ogni oggetto della Libreria di offerte in [questa sezione](../export-catalog/access-dataset.md).

Elenco di tutti i campi che possono essere utilizzati nel set di dati **[!UICONTROL Archivio oggetti decisionali - Decisioni]** (precedentemente noto come Archivio oggetti decisioni - Attività).

<!--A decision (formerly known as offer decision) is used to control the decisioning process. It specifies the filter applied to the total inventory to narrow down offers by topic/category, the placement to narrow down the inventory to those offers that technically fit into the reserved space for the offer and specifies a fallback option should the combined constraints disqualify all available personalization offers.-->

+++ Identificatore

**Campo:** _id
**Titolo:** Identificatore
**Descrizione:** Identificatore univoco del record.
**Tipo:** stringa

+++

+++ _experience

**Campo:** _esperienza
**Tipo:** oggetto

+++

+++ _experience > decisioning

**Campo:** decisioning
**Tipo:** oggetto

+++

+++ _experience > decisioning > criteri

**Campo:** criteri
**Titolo:** Criteri
**Descrizione:** Definisce un insieme di criteri di decisione in cui ciascun criterio contiene un insieme di vincoli.
**Tipo:** array

+++

+++ _esperienza > decisioni > criteri > descrizione

**Campo:** descrizione
**Titolo:** Descrizione
**Descrizione:** Descrizione criterio. Viene utilizzato per esprimere intenzioni leggibili su come o perché questo criterio è stato costruito e come influisce sulla decisione.
**Tipo:** stringa

+++

+++_experience > decisioning > criteri > optionSelection

**Campo:** optionSelection
**Titolo:** Selezione Opzione
**Descrizione:** La selezione dell&#39;opzione definisce la validità/applicabilità delle opzioni in questo contesto.
**Tipo:** oggetto

* Descrizione

  **Campo:** descrizione
  **Titolo:** Descrizione
  **Descrizione:** descrizione selezione opzione. Viene utilizzato per comunicare le intenzioni leggibili dell’uomo su come o perché la selezione dell’opzione è stata costruita e/o quale opzione corrisponderà.
  **Tipo:** stringa

* Filtro opzioni

  **Campo:** filtro
  **Titolo:** Filtro opzioni
  **Descrizione:** il riferimento a un filtro basato su qualificatore di raccolta (precedentemente noto come &quot;tag&quot;) che corrisponde alle opzioni di un inventario utilizzando i qualificatori di raccolta associati. Il valore è l’URI (@id) della regola di decisione a cui si fa riferimento. Consulta schema https://ns.adobe.com/experience/decisioning/filter.
  **Tipo:** stringa

* Tipo di vincolo profilo

  **Campo:** optionSelectionType
  **Titolo:** Tipo Di Vincolo Profilo
  **Descrizione:** Determina se sono impostati vincoli e la modalità di espressione dei vincoli. Potrebbe essere tramite una query di filtro o una o più appartenenze a un pubblico.
  **Tipo:** stringa
  **Valori possibili:** &quot;none&quot; (impostazione predefinita), &quot;directList&quot;, &quot;filter&quot;

* Elenco opzioni

  **Campo:** opzioni
  **Titolo:** Elenco opzioni
  **Descrizione:** un elenco che specifica direttamente le opzioni senza valutare una query di filtro. È possibile specificare un elenco di opzioni o una regola di filtro delle opzioni.
  **Tipo:** array

<!--Missing title under Option List? Desc = An identifier of an decision option entity. The value value refers to an `@id` property of a decision option. Type: string-->

+++

+++_experience > decisioning > criteri > posizionamenti

**Campo:** posizionamenti
**Titolo:** Limitazioni di posizionamento
**Descrizione:** Il vincolo di posizionamento indica che questo criterio è applicabile solo per i posizionamenti elencati. La selezione dell&#39;opzione è considerata solo quando il posizionamento di destinazione è incluso nell&#39;elenco `xdm:placements`. In caso contrario, vengono ignorati tutti i criteri di decisione. Quando l&#39;elenco &#39;xdm:placements&#39; viene omesso o vuoto, il criterio viene considerato per qualsiasi posizionamento di destinazione. I posizionamenti elencati impongono criteri impliciti per la selezione dell’opzione. Un’opzione da considerare deve avere una rappresentazione per il posizionamento mirato.
**Tipo:** array

* Identificatore di posizionamento

  **Titolo:** Identificatore posizionamento
  **Descrizione:** un riferimento a un&#39;entità di posizionamento. Il valore è l’URI (@id) del posizionamento a cui si fa riferimento. Consulta schema https://ns.adobe.com/experience/decisioning/placement.
  **Tipo:** stringa

+++

+++_experience > decisioning > criteri > profileConstraints

**Campo:** profileConstraints
**Titolo:** Vincolo Profilo
**Descrizione:** Il vincolo di profilo decide se la selezione di un&#39;opzione è idonea per questa identità di profilo in questo momento, in questo contesto. Se non è necessario che il vincolo di profilo consideri i valori di ciascuna opzione, ovvero non è una variante delle opzioni selezionate, il vincolo di profilo che restituisce &quot;false&quot; annulla l’intera selezione dell’opzione. D&#39;altra parte, una regola di vincolo di profilo che accetta un&#39;opzione come parametro viene valutata per ogni opzione qualificata della selezione dell&#39;opzione.
**Tipo:** oggetto

+++

+++_experience > decisioning > criteri > profileConstraints > Descrizione

**Campo:** descrizione
**Titolo:** Descrizione
**Descrizione:** descrizione vincolo profilo. Viene utilizzato per comunicare le intenzioni leggibili dell’uomo su come o perché questo vincolo di profilo è stato costruito e/o quale opzione sarà inclusa o esclusa da esso.
**Tipo:** stringa

+++

+++ _experience > decisioning > criteri > profileConstraints > Regola di idoneità

**Campo:** idoneitàRegola
**Titolo:** Regola di idoneità
**Descrizione:** riferimento a una regola di decisione che restituisce true o false per un profilo specificato e/o altri oggetti XDM contestuali specificati. La regola viene utilizzata per decidere se l’opzione è idonea per un determinato profilo. Il valore è l’URI (@id) della regola di decisione a cui si fa riferimento. Consulta schema https://ns.adobe.com/experience/decisioning/rule.
**Tipo:** stringa

+++

+++ _experience > decisioning > criteri > profileConstraints > Tipo di vincolo profilo

**Campo:** profileConstraintType
**Titolo:** Tipo Di Vincolo Del Profilo
**Descrizione:** Determina se sono attualmente impostati vincoli e il modo in cui questi vengono espressi. Potrebbe essere tramite una regola o tramite una o più appartenenze al pubblico.
**Tipo:** stringa
**Valori possibili:**

* &quot;none&quot; (impostazione predefinita)
* &quot;EliabilityRule&quot;: &quot;Il vincolo di profilo è espresso come una singola regola che deve restituire true prima che l’azione vincolata sia consentita.&quot;
* &quot;anySegments&quot;: &quot;Il vincolo di profilo è espresso come uno o più tipi di pubblico e il profilo deve essere membro di almeno uno di essi prima che l’azione vincolata sia consentita.&quot;
* &quot;allSegments&quot;: &quot;Il vincolo di profilo è espresso come uno o più tipi di pubblico e il profilo deve essere un membro di tutti loro prima che l’azione vincolata sia consentita.&quot;
* &quot;regole&quot;: &quot;Il vincolo di profilo è espresso come una serie di regole diverse, ad esempio idoneità, applicabilità, idoneità, che tutte devono restituire true prima che l’azione vincolata sia consentita.&quot;

+++

+++ _experience > decisioning > criteri > profileConstraints > segmentIdentities

**Campo:** segmentIdentities
**Titolo:** Identificatori Segmento
**Descrizione:** identificatori del pubblico.
**Tipo:** array

* Identificatore

  **Campo:** _id
  **Titolo:** Identificatore
  **Descrizione:** identità del pubblico nel relativo spazio dei nomi.
  **Tipo:** stringa

* namespace

  **Campo:** spazio dei nomi
  **Titolo:** Spazio Dei Nomi
  **Descrizione:** lo spazio dei nomi associato all&#39;attributo `xid`.
  **Tipo:** oggetto
  **Obbligatorio:** &quot;code&quot;

   * Codice

     **Campo:** codice
     **Titolo:** Codice
     **Descrizione:** Il codice è un identificatore leggibile dello spazio dei nomi e può essere utilizzato per richiedere l&#39;ID tecnico dello spazio dei nomi, utilizzato per l&#39;elaborazione del grafico delle identità.
     **Tipo:** stringa

* Identificatore dell’esperienza

  **Campo:** xid
  **Titolo:** Identificatore esperienza
  **Descrizione:** Se presente, questo valore rappresenta un identificatore per più spazi dei nomi che è univoco tra tutti gli identificatori relativi allo spazio dei nomi in tutti gli spazi dei nomi.
  **Tipo:** stringa

+++

+++_experience > decisioning > criteri > classificazione

**Campo:** classificazione
**Titolo:** Dettagli Classificazione
**Descrizione:** Grado (priorità). Definisce il modo in cui viene determinata l’\&quot;opzione migliore\&quot; in base al contesto del criterio di decisione. Tra tutte le opzioni selezionate che soddisfano i vincoli del profilo, la classificazione determinerà le opzioni principali (o le N principali) da proporre.
**Tipo:** oggetto

+++ 

+++_esperienza > decisioni > criteri > classificazione > ordine

**Campo:** ordine
**Titolo:** Valutazione dell&#39;ordine
**Descrizione:** valutazione di un ordine relativo di una o più opzioni di decisione. Le opzioni con valori ordinali più alti vengono selezionate rispetto alle opzioni con valori ordinali più bassi. I valori determinati con questo metodo possono essere ordinati, ma non è possibile misurare le distanze tra di essi né calcolare somme o prodotti. La mediana e la modalità sono le uniche misure della tendenza centrale che possono essere utilizzate per i dati ordinali.
**Tipo:** oggetto

* Funzione punteggio

  **Campo:** funzione
  **Titolo:** Funzione punteggio
  **Descrizione:** Riferimento a una funzione che calcola un punteggio numerico per questa opzione di decisione. Le opzioni di decisione verranno quindi ordinate (classificate) in base a tale punteggio. Il valore di questa proprietà è l&#39;URI (@id) della funzione da richiamare contemporaneamente con l&#39;opzione on. Consulta schema https://ns.adobe.com/experience/decisioning/function.
  **Tipo:** stringa

* Tipo di valutazione ordine**

  **Campo:** orderEvaluationType
  **Titolo:** Tipo di valutazione ordine
  **Descrizione:** Specifica il meccanismo di valutazione dell&#39;ordine utilizzato, la priorità statica delle opzioni di decisione, una funzione di punteggio che calcola un valore numerico per ogni opzione o un modello di IA che riceve un elenco per ordinarlo.
  **Tipo:** stringa
  **Valori possibili:** &quot;static&quot;, &quot;scoringFunction&quot;, &quot;rankingStrategy&quot;

* Strategia di classificazione

  **Campo:** strategia di classificazione
  **Titolo:** Strategia di classificazione
  **Descrizione:** un riferimento a una strategia che classifica un elenco di opzioni di decisione. Le opzioni di decisione verranno restituite in un elenco ordinato. Il valore di questa proprietà è l&#39;URI (@id) della funzione da richiamare contemporaneamente con l&#39;opzione on. Consulta schema https://ns.adobe.com/experience/decisioning/rankingStrategy.
  **Tipo:** stringa

+++

+++ _experience > decisioning > criteri > classificazione > Priorità

**Campo:** priorità
**Titolo:** Priorità
**Descrizione:** la priorità di una singola opzione di decisione rispetto a tutte le altre opzioni. Le opzioni per le quali non viene specificata alcuna funzione di ordinamento hanno priorità utilizzando questa proprietà. Le opzioni con valori di priorità più alti vengono selezionate prima di qualsiasi opzione con priorità inferiore. Se due o più opzioni qualificate condividono il valore di priorità più elevato, una viene scelta in modo casuale e utilizzata per la proposta di decisione.
**Tipo:** numero intero
**Valore minimo:** 0
**Valore predefinito:** 0

+++

+++ _experience > decisioning > Data e ora di fine attività

**Campo:** endTime
**Titolo:** Data e ora di fine attività
**Descrizione:** Data e ora di fine della decisione (precedentemente nota come attività). Per la proprietà è definita la semantica della proprietà &#39;endTime&#39; di schema.org in https://schema.org/Action.
**Tipo:** stringa

+++

+++ _experience > decisioning > Opzione di fallback

**Campo:** fallback
**Titolo:** Opzione di fallback
**Descrizione:** Il riferimento a un&#39;opzione di fallback utilizzata durante le decisioni nel contesto di questa decisione non qualifica alcuna delle opzioni regolari (in genere si verifica quando vengono applicati vincoli rigidi). Il valore è l’URI (@id) dell’opzione di fallback a cui si fa riferimento.
**Tipo:** stringa

+++

+++ _experience > decisioning > Nome attività

**Campo:** nome
**Titolo:** Nome Attività
**Descrizione:** nome della decisione (precedentemente nota come attività) visualizzato in varie interfacce utente.
**Tipo:** stringa

+++

+++_experience > decisioning > Data e ora di inizio attività

**Campo:** startTime
**Titolo:** Data e ora di inizio attività
**Descrizione:** Data di inizio e ora di fine della decisione (precedentemente nota come attività). Per la proprietà è definita la semantica della proprietà &quot;startTime&quot; di schema.org in https://schema.org/Action.
**Tipo:** stringa

+++

+++ _repo

**Campo:** _repo
**Tipo:** oggetto

+++

+++ _repo > Attività ETag

**Campo:** etag
**Titolo:** Attività ETag
**Descrizione:** revisione in cui si trovava l&#39;oggetto decisione (precedentemente noto come attività) quando è stata acquisita l&#39;istantanea.
**Tipo:** stringa

+++
