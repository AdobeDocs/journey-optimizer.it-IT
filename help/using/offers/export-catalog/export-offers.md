---
title: Set di dati di offerte personalizzate
description: In questa sezione sono elencati tutti i campi utilizzati nel set di dati esportato per le offerte
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: c7f691aa-8f89-4f23-b897-53211863eb6d
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '2003'
ht-degree: 0%

---

# Set di dati di offerte personalizzate {#offers-dataset}

Ogni volta che un’offerta viene modificata, viene aggiornato il set di dati generato automaticamente per le offerte di contenuto personalizzato.

![](../assets/dataset-offers.png)

Il batch di successo più recente nel set di dati viene visualizzato a destra. La visualizzazione gerarchica dello schema per il set di dati viene visualizzata nel riquadro a sinistra.

>[!NOTE]
>
>Scopri come accedere ai set di dati esportati per ciascun oggetto della Libreria offerte in [questa sezione](../export-catalog/access-dataset.md).

Elenco di tutti i campi che possono essere utilizzati nella **[!UICONTROL Decision Object Repository - Personalized Offers]** set di dati.

<!--Personalized offers form the set of choices for a decision. The objective for decisioning is to take a large inventory of items and apply numerous constraint rules to that inventory to narrow it down and then to rank the qualifying options according to a criteria. The resulting propositions assemble and personalize the experience for specific individuals.-->

## Identificatore {#identifier}

**Campo:** _id
**Titolo:** Identificatore
**Descrizione:** Identificatore univoco del record.
**Tipo:** string

## _esperienza {#experience}

**Campo:** _esperienza
**Tipo:** oggetto

### _esperienza > decisionale

**Campo:** decisione
**Tipo:** oggetto

#### _esperienza > decisionale > calendarConstraints

**Campo:** calendarConstraints
**Titolo:** Dettagli vincolo calendario
**Descrizione:** I vincoli del calendario decidono se un&#39;opzione di decisione è valida in base a un intervallo di date. Al di fuori dell’intervallo di date, l’opzione non può essere proposta.
**Tipo:** oggetto

* **Data e ora di fine**

   **Campo:** endDate
   **Titolo:** Data e ora di fine
   **Descrizione:** Data di fine di validità delle opzioni di decisione. Le opzioni che hanno superato la data di fine non possono più essere proposte nel processo decisionale.
   **Tipo:** string

* **Data e ora di inizio**

   **Campo:** startDate
   **Titolo:** Data e ora di inizio
   **Descrizione:** Data di inizio della validità delle opzioni di decisione. Le opzioni che non hanno raggiunto la data di inizio non possono ancora essere proposte nel processo decisionale.
   **Tipo:** string

#### _esperienza > decisione > caratteristiche

**Campo:** caratteristiche
**Titolo:** Caratteristiche dell&#39;opzione di decisione
**Descrizione:** Proprietà o attributi aggiuntivi appartenenti a questa particolare opzione di decisione. istanze diverse possono avere caratteristiche diverse (chiavi nella mappa). Le caratteristiche sono coppie di valori nome utilizzate per distinguere un’opzione di decisione da altre. Le caratteristiche vengono utilizzate come valori nel contenuto che rappresenta questa opzione decisionale e come funzioni per analizzare e ottimizzare le prestazioni di un’opzione. Quando ogni istanza ha lo stesso attributo o proprietà, tale aspetto deve essere modellato come uno schema di estensione che deriva dai dettagli dell’opzione di decisione.
**Tipo:** oggetto

#### _esperienza > decisioni > contenuti

**Campo:** sommario
**Titolo:** Dettagli contenuto
**Descrizione:** Elementi di contenuto per eseguire il rendering dell’elemento decisione in contesti diversi. Una singola opzione di decisione può avere più varianti di contenuto. Il contenuto è un’informazione rivolta a un pubblico da utilizzare in un’esperienza (digitale). I contenuti vengono consegnati attraverso i canali in un particolare posizionamento.
**Tipo:** array

**_esperienza > decisioni > contenuti > componenti**

**Campo:** componenti
**Descrizione:** I componenti del contenuto che rappresentano l’opzione di decisione, incluse tutte le varianti di lingua. Componenti specifici sono reperibili da &#39;dx:format&#39;, &#39;dc:subject&#39; e &#39;dc:language&#39; o da una combinazione di essi. Questi metadati vengono utilizzati per individuare o rappresentare il contenuto associato a un’offerta e integrarlo in base al contratto di posizionamento.
**Tipo:** array
**Obbligatorio:** &quot;_type&quot;, &quot;_dc&quot; <!--TBC?-->

* **_esperienza > decisioni > contenuti > componenti > tipo di componente contenuto**

   **Campo:** _type
   **Titolo:** Tipo componente contenuto
   **Descrizione:** Set enumerato di URI in cui ogni valore corrisponde a un tipo assegnato al componente contenuto. Alcuni utenti delle rappresentazioni di contenuto si aspettano che il valore @type sia un riferimento allo schema che descrive proprietà aggiuntive del componente di contenuto.
   **Tipo:** string

* **_esperienza > decisioni > contenuti > componenti > _dc**

   **Campo:** _dc
   **Tipo:** oggetto
   **Obbligatorio:** &quot;format&quot;

   * **Formato**

      **Campo:** format
      **Titolo:** Formato
      **Descrizione:** La manifestazione fisica o digitale della risorsa. In genere, Format deve includere il tipo di supporto della risorsa. Il formato può essere utilizzato per determinare il software, l&#39;hardware o altre apparecchiature necessarie per visualizzare o utilizzare la risorsa. Si consiglia di selezionare un valore da un vocabolario controllato (ad esempio, l&#39;elenco di [Tipi di file multimediali Internet](http://www.iana.org/assignments/media-types/) definizione dei formati dei supporti del computer).
      **Tipo:** string
      **Esempio:** &quot;application/vnd.adobe.photoshop&quot;

   * **Lingua**
      **Campo:** language
      **Titolo:** Lingua
      **Descrizione:** Lingua o lingue della risorsa. \nLe lingue sono specificate nel codice della lingua come definito in [RFC 3066 di IETF](https://www.ietf.org/rfc/rfc3066.txt), che fa parte del BCP 47, utilizzato altrove in XDM.
      **Tipo:** array
      **Esempi:** &quot;\n&quot;, &quot;pt-BR&quot;, &quot;es-ES&quot;

* **_esperienza > decisioni > contenuti > componenti > _repo**

   **Campo:** _repo
   **Tipo:** oggetto

   * **id**

      **Campo:** id
      **Descrizione:** Identificatore univoco facoltativo per fare riferimento alla risorsa in un archivio di contenuti. Quando le API di Platform vengono utilizzate per recuperare la rappresentazione, il client può aspettarsi una proprietà aggiuntiva \&quot;repo:resolveUrl\&quot; per recuperare la risorsa.
      **Tipo:** string
      **Esempio:** &quot;urn:aaid:sc:US:6dc33479-13ca-4b19-b25d-c805eff8a69e&quot;

   * **nome**

      **Campo:** name
      **Descrizione:** Alcuni suggerimenti su dove individuare l&#39;archivio in cui è memorizzata la risorsa esterna tramite il \&quot;repo:id\&quot;.
      **Tipo:** string

   * **repositoryID**

      **Campo:** repositoryID
      **Descrizione:** Identificatore univoco facoltativo per fare riferimento alla risorsa in un archivio di contenuti. Quando le API di Platform vengono utilizzate per recuperare la rappresentazione, il client può aspettarsi una proprietà aggiuntiva \&quot;repo:resolveUrl\&quot; per recuperare la risorsa.
      **Tipo:** string
      **Esempio:** &quot;C87932A55B06F7070A49412D@AdobeOrg&quot;

   * **resolveURL**

      **Campo:** resolveURL
      **Descrizione:** Un localizzatore di risorse univoco facoltativo per leggere la risorsa in un archivio di contenuti. In questo modo sarà più facile ottenere la risorsa senza che il cliente comprenda dove la risorsa viene gestita e quali API chiamare. Questo è simile a un collegamento HAL, ma il semantico è più semplice e mirato.
      **Tipo:** string
      **Esempio:** &quot;https://plaftform.adobe.io/resolveByPath?path=&quot;/mycorp/content/projectx/fragment/prod/herobanners/banner14.html3&quot;&quot;

* **_esperienza > decisioni > contenuti > componenti > contenuto**

   **Campo:** content
   **Descrizione:** Un campo facoltativo per contenere direttamente il contenuto. Invece di fare riferimento al contenuto in un archivio di risorse, il componente può contenere direttamente contenuti semplici. Questo campo non viene utilizzato per le risorse di contenuto composito, complesso e binario.
   **Tipo:** string

* **_esperienza > decisioni > contenuti > componenti > deliveryURL**

   **Campo:** deliveryURL
   **Descrizione:** Un localizzatore di risorse univoco facoltativo per ottenere la risorsa da una rete di distribuzione dei contenuti o da un endpoint di servizio. Questo URL viene utilizzato per accedere pubblicamente alla risorsa da un agente utente.
   **Tipo:** string
   **Esempio:** &quot;https://cdn.adobe.io/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

* **_esperienza > decisioni > contenuti > componenti > linkURL**

   **Campo:** linkURL
   **Descrizione:** Un localizzatore di risorse univoco facoltativo per le interazioni dell’utente. Questo URL viene utilizzato per fare riferimento all’utente finale in un agente utente e può essere monitorato.
   **Tipo:** string
   **Esempio:** &quot;https://cdn.adobe.io/tracker?code=23432&amp;redirect=/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

**_esperienza > decisionale > contenuto > Posizionamento**

**Campo:** placement
**Titolo:** Posizionamento
**Descrizione:** Posizionamento a cui conformarsi. Il valore è l’URI (@id) del posizionamento dell’offerta a cui si fa riferimento. Vedi schema https://ns.adobe.com/experience/decisioning/placement.
**Tipo:** string

#### _esperienza > decisioni > Stato del ciclo di vita

**Campo:** lifecycleStatus
**Titolo:** Stato del ciclo di vita
**Descrizione:** Lo stato del ciclo di vita consente di eseguire i flussi di lavoro con un oggetto. Lo stato può influire sul punto in cui un oggetto è visibile o considerato rilevante. Le modifiche allo stato sono guidate dai client o dai servizi che utilizzano gli oggetti.
**Tipo:** string
**Valori possibili:** &quot;Bozza&quot; (predefinito), &quot;Approvato&quot;, &quot;Live&quot;, &quot;Completato&quot;, &quot;Archiviato&quot;

#### _esperienza > decisionale > Nome opzione decisione

**Campo:** name
**Titolo:** Nome opzione decisione
**Descrizione:** Nome dell&#39;opzione visualizzato in diverse interfacce utente.
**Tipo:** string

#### _esperienza > decisionale > profileConstraints

**Campo:** profileConstraints
**Titolo:** Dettagli vincolo profilo
**Descrizione:** In questo contesto, i vincoli di profilo decidono se un’opzione è idonea per questa identità di profilo. Se il vincolo di profilo non deve considerare i valori di ciascuna opzione, ovvero non è necessariamente una delle opzioni della selezione dell’opzione, il vincolo di profilo che restituisce &quot;false&quot; annulla l’intera selezione dell’opzione. D&#39;altra parte, viene valutata una regola di vincolo di profilo che utilizza un&#39;opzione come parametro per ogni opzione di qualificazione della selezione di opzione.
**Tipo:** oggetto

**_esperienza > decisionale > profileConstraints > Descrizione**

**Campo:** descrizione
**Titolo:** Descrizione
**Descrizione:** Descrizione del vincolo di profilo. Viene utilizzato per comunicare le intenzioni leggibili dell’uomo su come o perché è stato costruito questo vincolo di profilo e/o quale opzione sarà inclusa o esclusa da esso.
**Tipo:** string

**_esperienza > decisionale > profileConstraints > Regola di idoneità**

**Campo:** adaptRule
**Titolo:** Regola di idoneità
**Descrizione:** Un riferimento a una regola decisionale che restituisce true o false per un determinato profilo e/o altri oggetti XDM contestuali specificati. La regola viene utilizzata per decidere se l’opzione è idonea per un determinato profilo. Il valore è l&#39;URI (@id) della regola decisionale a cui si fa riferimento. Vedi schema https://ns.adobe.com/experience/decisioning/rule.
**Tipo:** string

**_esperienza > decisione > profileConstraints > Tipo di vincolo del profilo**

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

**_esperienza > decisionale > profileConstraints > Identificatori di segmento**

**Campo:** segmentIdentities
**Titolo:** Identificatori dei segmenti
**Descrizione:** Identificatori dei segmenti
**Tipo:** array

* **Identificatore**

   **Campo:** _id
   **Titolo:** Identificatore
   **Descrizione:** Identità del segmento nello spazio dei nomi correlato.
   **Tipo:** string

* **Namespace**

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

#### _esperienza > decisionale > classificazione

**Campo:** classificazione
**Titolo:** Dettagli classificazione
**Descrizione:** Classificazione (priorità). Definisce ciò che viene considerato la \&quot;azione migliore\&quot; in base al contesto del criterio di decisione. Tra tutte le opzioni selezionate che soddisfano il vincolo di idoneità, l’ordine di classificazione deciderà l’opzione o le opzioni superiori N da proporre.
**Tipo:** oggetto

**_esperienza > decisionale > classificazione > Valutazione ordine**

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

**_esperienza > decisionale > classificazione > Priorità**

**Campo:** priorità
**Titolo:** Priorità
**Descrizione:** La priorità di un&#39;unica opzione di decisione rispetto a tutte le altre opzioni. Le opzioni per le quali non viene specificata alcuna funzione di ordine vengono definite come priorità utilizzando questa proprietà. Le opzioni con valori di priorità più elevati vengono selezionate prima di qualsiasi opzione di priorità più bassa. Se due o più opzioni qualificate condividono il valore di priorità più elevato, una viene scelta in modo casuale uniforme e utilizzata per la proposta di decisione.
**Tipo:** integer
**Valore minimo:** 0
**Valore predefinito:** 0

#### _esperienza > decisionale > tag

**Campo:** tag
**Titolo:** Tag
**Descrizione:** Set di tag associati a questa entità. I tag vengono utilizzati nelle espressioni filtro per vincolare l’inventario complessivo a un sottoinsieme (categoria).
**Tipo:** array

<!--Field without name under tags: Description: An identifier of a tag object. The value is the @id of the tag that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

## _repo {#repo}

**Campo:** _repo
**Tipo:** oggetto

### _repo > Opzione decisione ETag

**Campo:** etag
**Titolo:** Opzione di decisione ETag
**Descrizione:** Revisione in cui si trovava l&#39;oggetto opzione di decisione al momento dell&#39;esecuzione dello snapshot.
**Tipo:** string
