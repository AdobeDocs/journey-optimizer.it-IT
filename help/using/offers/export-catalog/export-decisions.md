---
title: Introduzione all’esportazione del catalogo delle offerte
description: In questa sezione sono elencati tutti i campi utilizzati nel set di dati esportato per le decisioni.
translation-type: tm+mt
source-git-commit: d96a2b179ce652a119b6008e02b1409666f36402
workflow-type: tm+mt
source-wordcount: '1242'
ht-degree: 1%

---

# Set di dati delle decisioni {#decisions-dataset}

Ogni volta che un’offerta viene modificata, viene aggiornato il set di dati generato automaticamente per le decisioni.

![](../assets/dataset-activities.png)

Il batch di successo più recente nel set di dati viene visualizzato a destra. La visualizzazione gerarchica dello schema per il set di dati viene visualizzata nel riquadro a sinistra.

>[!NOTE]
>
>Scopri come accedere ai set di dati esportati per ciascun oggetto della Libreria offerte in [questa sezione](../export-catalog/access-dataset.md).

Una decisione (precedentemente nota come decisione di offerta) viene utilizzata per controllare il processo decisionale. Specifica il filtro applicato all’inventario totale per limitare le offerte in base all’argomento/categoria, il posizionamento per limitare l’inventario alle offerte che tecnicamente rientrano nello spazio riservato per l’offerta e specifica un’opzione di fallback se i vincoli combinati non qualificano tutte le offerte di personalizzazione disponibili.

Elenco di tutti i campi che possono essere utilizzati nel set di dati **[!UICONTROL Decision Object Repository - Decisions]** (precedentemente noto come Archivio oggetti decisionali - Attività).

## Identificatore

Identificatore univoco del record.

Tipo: string

## _esperienza

### decisione

#### criteri

Definisce un insieme di criteri decisionali in cui ciascuno contiene un insieme di vincoli.

Tipo: array

* **Descrizione**

   Descrizione del criterio. Viene utilizzato per comunicare le intenzioni comprensibili all&#39;uomo su come o perché questo criterio è stato elaborato e come influisce sulla decisione.

   Tipo: string

* **Selezione dell&#39;opzione**

   La selezione delle opzioni definisce la validità/applicabilità delle opzioni in questo contesto.

   Tipo: oggetto

   * **Descrizione**

      Descrizione selezione opzione. Viene utilizzato per comunicare le intenzioni di lettura umana su come o perché è stata costruita questa selezione di opzioni e/o quale opzione corrisponderà.

      Tipo: string

   * **Filtro opzione**

      Il riferimento a un filtro basato su tag che corrisponde alle opzioni di un inventario utilizzando i relativi tag allegati. Il valore è l&#39;URI (@id) della regola decisionale a cui si fa riferimento. Vedi schema https://ns.adobe.com/experience/decisioning/filter.

      Tipo: string

   * **Tipo di vincolo del profilo**

      Determina se sono attualmente impostati vincoli e come vengono espressi i contrasti. Potrebbe essere tramite una query di filtro o attraverso una o più appartenenze al segmento.

      Tipo: string

   * **Elenco opzioni**

      Elenco che specifica direttamente le opzioni senza valutare una query di filtro. È possibile specificare un elenco di opzioni o una regola di filtro opzioni.

      Tipo: array

      <!--Missing title under Option List? Desc = An identifier of an decision option entity. The value value refers to an `@id` property of a decision option.-->

* **posizionamenti**

   Il vincolo di posizionamento indica che questo criterio è applicabile solo per i posizionamenti elencati. Solo quando il posizionamento di destinazione è nell’elenco `xdm:placements` è considerata la selezione di opzioni. In caso contrario, vengono ignorati tutti i criteri decisionali. Quando l’elenco &quot;xdm:placements&quot; viene omesso o lasciato vuoto, il criterio viene considerato per qualsiasi posizionamento mirato. I posizionamenti qui elencati impongono criteri impliciti per la selezione dell’opzione. Un’opzione da considerare deve avere una rappresentazione per il posizionamento mirato.

   Tipo: array

   * **Identificatore di posizionamento**

   Un riferimento a un’entità di posizionamento. Il valore è l’URI (@id) del posizionamento a cui si fa riferimento. Vedi schema https://ns.adobe.com/experience/decisioning/placement.

   Tipo: string

* **Vincolo profilo**

   Il vincolo di profilo decide se una selezione di opzioni è attualmente idonea per questa identità di profilo, in questo contesto. Se il vincolo di profilo non deve considerare i valori di ciascuna opzione, ovvero non è necessariamente una delle opzioni della selezione dell’opzione, il vincolo di profilo che restituisce &quot;false&quot; annulla l’intera selezione dell’opzione. D’altro canto, viene valutata una regola di vincolo di profilo che utilizza un’opzione come parametro per ogni opzione di qualificazione della selezione dell’opzione.

   Tipo: oggetto

   * **Descrizione**

      Descrizione del vincolo di profilo. Viene utilizzato per comunicare le intenzioni leggibili dell’uomo su come o perché è stato costruito questo vincolo di profilo e/o quale opzione sarà inclusa o esclusa da esso.

      Tipo: string

   * **Regola di idoneità**

      Un riferimento a una regola decisionale che restituisce true o false per un determinato profilo e/o altri oggetti XDM contestuali specificati. La regola viene utilizzata per decidere se l’opzione è idonea per un determinato profilo. Il valore è l&#39;URI (@id) della regola decisionale a cui si fa riferimento. Vedi schema https://ns.adobe.com/experience/decisioning/rule.

      Tipo: string

   * **Tipo di vincolo del profilo**

      Determina se sono attualmente impostati vincoli e come vengono espressi i contrasti. Potrebbe essere attraverso una regola o attraverso una o più appartenenze al segmento.

      Tipo: string

      Valori possibili: &quot;none&quot;, &quot;allowrule&quot;, &quot;anySegments&quot;, &quot;allSegments&quot;, &quot;rules&quot;

      Valore predefinito: &quot;none&quot;

   * **Identificatori dei segmenti**

      Identificatori dei segmenti

      Stringa: array

      * **Identificatore**

         Identità del segmento nello spazio dei nomi correlato.

         Tipo: string

      * **Namespace**

         Spazio dei nomi associato all&#39;attributo `xid` .

         Tipo: oggetto

         * **Codice**

            Il codice è un identificatore leggibile dall’utente per lo spazio dei nomi e può essere utilizzato per richiedere l’ID tecnico dello spazio dei nomi utilizzato per l’elaborazione del grafico delle identità.

            Tipo: string
      * **Identificatore esperienza**

         Se presente, questo valore rappresenta un identificatore dello spazio dei nomi incrociato univoco per tutti gli identificatori con ambito dello spazio dei nomi in tutti i namespace.

         Tipo: string


* **Dettagli classificazione**

   Classificazione (priorità). Definisce come viene determinata la \&quot;opzione migliore\&quot; in base al contesto del criterio di decisione. Tra tutte le opzioni selezionate che soddisfano i vincoli del profilo, la classificazione deciderà l’opzione o le opzioni superiori N da proporre.

   Tipo: oggetto

   * **Valutazione ordine**

      Valutazione di un ordine relativo di una o più opzioni decisionali. Le opzioni con valori ordinali più alti vengono selezionate su qualsiasi opzione con valori ordinali più bassi. I valori determinati con questo metodo possono essere ordinati, ma le distanze tra di essi non possono essere misurate né le somme né i prodotti possono essere calcolati. La mediana e la modalità sono le uniche misure di tendenza centrale che possono essere utilizzate per i dati ordinali.

      Tipo: oggetto

      * **Funzione di punteggio**

         Riferimento a una funzione che calcola un punteggio numerico per questa opzione di decisione. Le opzioni di decisione saranno quindi ordinate (classificate) in base a quel punteggio. Il valore di questa proprietà è l&#39;URI (@id) della funzione da richiamare con l&#39;opzione on alla volta. Vedi schema https://ns.adobe.com/experience/decisioning/function.

         Tipo: string

      * **Tipo di valutazione ordine**

         Specifica quale meccanismo di valutazione dell&#39;ordine viene utilizzato, priorità statica delle opzioni di decisione, una funzione di punteggio che calcola un valore numerico per ogni opzione o una strategia di classificazione che riceve un elenco per ordinarlo.

         Tipo: string

      * **Strategia di classificazione**

         Riferimento a una strategia che classifica un elenco di opzioni decisionali. Le opzioni di decisione verranno restituite in un elenco ordinato. Il valore di questa proprietà è l&#39;URI (@id) della funzione da richiamare con l&#39;opzione on alla volta. Vedi schema https://ns.adobe.com/experience/decisioning/rankingStrategy.

         Tipo: string
   * **Priorità**

      La priorità di un&#39;unica opzione di decisione rispetto a tutte le altre opzioni. Le opzioni per le quali non è specificata alcuna funzione di ordine hanno priorità utilizzando questa proprietà. Le opzioni con valori di priorità più elevati vengono selezionate prima di qualsiasi opzione di priorità più bassa. Se due o più opzioni qualificate condividono il valore di priorità più elevato, una viene scelta in modo casuale uniforme e utilizzata per la proposta di decisione.

      Tipo: integer

      Valore minimo: 0

      Valore predefinito: 0


#### Data e ora di fine attività

Data e ora di fine della decisione. La proprietà ha la semantica della proprietà &#39;endTime&#39; di schema.org definita su http://schema.org/Action.

Tipo: string

#### Opzione di fallback

Il riferimento a un&#39;opzione di fallback utilizzata quando si prende una decisione nel contesto di questa decisione non qualifica nessuna delle opzioni regolari (questo accade in genere quando si applicano vincoli rigidi). Il valore è l’URI (@id) dell’opzione di fallback a cui si fa riferimento.

Tipo: string

#### Nome attività

Nome della decisione visualizzato in diverse interfacce utente.

Tipo: string

#### Data e ora di inizio attività

Data e ora di inizio della decisione. La proprietà ha la semantica della proprietà &#39;startTime&#39; di schema.org definita su http://schema.org/Action.

Tipo: string

## _repo

### Attività ETag

Revisione in cui si trovava l&#39;oggetto decisione al momento dell&#39;istantanea.

Tipo: string
