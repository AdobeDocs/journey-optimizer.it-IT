---
title: Set di dati di offerte personalizzate
description: In questa sezione sono elencati tutti i campi utilizzati nel set di dati esportato per le offerte.
translation-type: tm+mt
source-git-commit: d96a2b179ce652a119b6008e02b1409666f36402
workflow-type: tm+mt
source-wordcount: '1789'
ht-degree: 0%

---

# Set di dati di offerte personalizzate {#offers-dataset}

Ogni volta che un’offerta viene modificata, viene aggiornato il set di dati generato automaticamente per le offerte di contenuto personalizzato.

![](../assets/dataset-offers.png)

Il batch di successo più recente nel set di dati viene visualizzato a destra. La visualizzazione gerarchica dello schema per il set di dati viene visualizzata nel riquadro a sinistra.

>[!NOTE]
>
>Scopri come accedere ai set di dati esportati per ciascun oggetto della Libreria offerte in [questa sezione](../export-catalog/access-dataset.md).

Le offerte personalizzate costituiscono l’insieme di scelte per una decisione. L&#39;obiettivo per le decisioni è quello di prendere un ampio inventario di articoli e applicare numerose regole di vincolo a tale inventario per restringerlo e poi classificare le opzioni qualificate in base a un criterio. Le proposte risultanti assemblano e personalizzano l’esperienza per singoli utenti specifici.

Elenco di tutti i campi che possono essere utilizzati nel set di dati **[!UICONTROL Decision Object Repository - Personalized Offers]** .

## Identificatore

Identificatore univoco del record.
Tipo: string

## _esperienza

### decisione

#### calendarConstraints

**Dettagli vincolo calendario**. I vincoli del calendario decidono se un&#39;opzione di decisione è valida in base a un intervallo di date. Al di fuori dell’intervallo di date, l’opzione non può essere proposta.
Tipo: oggetto

* **Data e ora di fine**

   Data di fine di validità delle opzioni di decisione. Le opzioni che hanno superato la data di fine non possono più essere proposte nel processo decisionale.

   Tipo: string

* **Data e ora di inizio**

   Data di inizio della validità delle opzioni di decisione. Le opzioni che non hanno raggiunto la data di inizio non possono ancora essere proposte nel processo decisionale.

   Tipo: string

#### caratteristiche

**Caratteristiche** dell&#39;opzione di decisione. Proprietà o attributi aggiuntivi appartenenti a questa particolare opzione di decisione. istanze diverse possono avere caratteristiche diverse (chiavi nella mappa). Le caratteristiche sono coppie di valori nome utilizzate per distinguere un’opzione di decisione da altre. Le caratteristiche vengono utilizzate come valori nel contenuto che rappresenta questa opzione decisionale e come funzioni per analizzare e ottimizzare le prestazioni di un’opzione. Quando ogni istanza ha lo stesso attributo o proprietà, tale aspetto deve essere modellato come uno schema di estensione che deriva dai dettagli dell’opzione di decisione.

Tipo: oggetto

#### sommario

**Dettagli contenuto**. Elementi di contenuto per eseguire il rendering dell’elemento decisione in contesti diversi. Una singola opzione di decisione può avere più varianti di contenuto. Il contenuto è un’informazione rivolta a un pubblico da utilizzare in un’esperienza (digitale). I contenuti vengono consegnati attraverso i canali in un particolare posizionamento.

Tipo: array

* ****
componentiI componenti del contenuto che rappresentano l’opzione di decisione, incluse tutte le varianti di lingua. Componenti specifici sono reperibili da &#39;dx:format&#39;, &#39;dc:subject&#39; e &#39;dc:language&#39; o da una combinazione di essi. Questi metadati vengono utilizzati per individuare o rappresentare il contenuto associato a un’offerta e integrarlo in base al contratto di posizionamento.

   * **Content Component**
TypeUn set enumerato di URI in cui ogni valore viene mappato su un tipo assegnato al componente contenuto. Alcuni consumatori delle rappresentazioni di contenuto si aspettano che il valore @type sia un riferimento allo schema che descrive proprietà aggiuntive del componente di contenuto.
Tipo: string

   * **_dc**

      * ****
FormatoLa manifestazione fisica o digitale della risorsa. In genere, Format deve includere il tipo di supporto della risorsa. Il formato può essere utilizzato per determinare il software, l&#39;hardware o altre apparecchiature necessarie per visualizzare o utilizzare la risorsa. Si consiglia di selezionare un valore da un vocabolario controllato (ad esempio, l&#39;elenco di [Tipi di file multimediali Internet](http://www.iana.org/ assegnazioni/tipi di file multimediali/) che definiscono i formati dei file multimediali per computer).

         Tipo: string

         Esempio: &quot;application/vnd.adobe.photoshop&quot;

      * ****
LinguaLa lingua o le lingue della risorsa.\nLe lingue sono specificate nel codice della lingua come definito in [IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt), che fa parte di BCP 47, utilizzato altrove in XDM.

         Tipo: string

         Esempi: &quot;/n&quot;, &quot;pt-BR&quot;, &quot;es-ES&quot;
   * **_repo**

      * **id**

         Identificatore univoco facoltativo per fare riferimento alla risorsa in un archivio di contenuti. Quando si utilizzano le API di Platform per recuperare la rappresentazione, il client può aspettarsi un&#39;ulteriore proprietà \&quot;repo:resolveUrl\&quot; per recuperare la risorsa.

         Tipo: string

      * **nome**

         Alcuni suggerimenti su dove individuare l&#39;archivio in cui è memorizzata la risorsa esterna tramite il \&quot;repo:id\&quot;.

         Tipo: string

      * **repositoryID**

         Identificatore univoco facoltativo per fare riferimento alla risorsa in un archivio di contenuti. Quando si utilizzano le API di Platform per recuperare la rappresentazione, il client può aspettarsi un&#39;ulteriore proprietà \&quot;repo:resolveUrl\&quot; per recuperare la risorsa.

         Tipo: string

         Esempio: &quot;C87932A55B06F7070A49412D@AdobeOrg&quot;

      * **resolveURL**

         Un localizzatore di risorse univoco facoltativo per leggere la risorsa in un archivio di contenuti. In questo modo sarà più facile ottenere la risorsa senza che il cliente comprenda dove la risorsa viene gestita e quali API chiamare. Questo è simile a un collegamento HAL, ma il semantico è più semplice e più risoluto.

         Tipo: string

         Esempio: &quot;https://plaftform.adobe.io/resolveByPath?path=&quot;/mycorp/content/projectx/fragment/prod/herobanners/banner14.html3&amp;quot&quot;
   * **content**

      Un campo facoltativo per contenere direttamente il contenuto. Invece di fare riferimento al contenuto in un archivio di risorse, il componente può contenere direttamente contenuti semplici. Questo campo non viene utilizzato per le risorse di contenuto composito, complesso e binario.

      Tipo: string

   * **deliveryURL**

      Un localizzatore di risorse univoco facoltativo per ottenere la risorsa da una rete di distribuzione dei contenuti o da un endpoint di servizio. Questo URL viene utilizzato per accedere pubblicamente alla risorsa da un agente utente.

      Tipo: string

      Esempio: &quot;https://cdn.adobe.io/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

   * **linkURL**

      Un localizzatore di risorse univoco facoltativo per le interazioni dell’utente. Questo URL viene utilizzato per fare riferimento all’utente finale in un agente utente e può essere monitorato.

      Tipo: string

      Esempio: &quot;https://cdn.adobe.io/tracker?code=23432&amp;redirect=/content/projectx/fragment/prod/static/1232324wd32.jpeg



* **Posizionamento**

   Posizionamento a cui conformarsi. Il valore è l’URI (@id) del posizionamento dell’offerta a cui si fa riferimento. Vedi schema https://ns.adobe.com/experience/decisioning/placement.

#### Stato del ciclo di vita

Lo stato del ciclo di vita consente di eseguire i flussi di lavoro con un oggetto. Lo stato può influire sul punto in cui un oggetto è visibile o considerato rilevante. Le modifiche allo stato sono guidate dai client o dai servizi che utilizzano gli oggetti.
Tipo: string
Valori possibili: Bozza, Approvato, Live, Completato, Archiviato

#### Nome opzione decisione

Nome opzione. Il nome viene visualizzato in diverse interfacce utente.
Tipo: string

#### Dettagli vincolo profilo

In questo contesto, i vincoli di profilo decidono se un’opzione è idonea per questa identità di profilo. Se il vincolo di profilo non deve considerare i valori di ciascuna opzione, ovvero non è necessariamente una delle opzioni della selezione dell’opzione, il vincolo di profilo che restituisce &quot;false&quot; annulla l’intera selezione dell’opzione. D’altro canto, viene valutata una regola di vincolo di profilo che utilizza un’opzione come parametro per ogni opzione di qualificazione della selezione dell’opzione.
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
Valori possibili:

   * Nessuno

   * &quot;criteri di idoneità&quot;: &quot;Il vincolo di profilo è espresso come una singola regola che deve restituire true prima che l&#39;azione vincolata sia consentita&quot;,

   * &quot;Qualsiasi segmento&quot;: &quot;Il vincolo di profilo è espresso come uno o più segmenti e il profilo deve essere un membro di almeno uno di essi prima che l’azione vincolata sia consentita&quot;,

   * &quot;Tutti i segmenti&quot;: &quot;Il vincolo di profilo è espresso come uno o più segmenti e il profilo deve essere un membro di tutti i segmenti prima che l’azione vincolata sia consentita&quot;,

   * &quot;regole&quot;: &quot;Il vincolo di profilo è espresso come una serie di regole diverse, ad esempio idoneità, applicabilità, idoneità, che tutte devono valutare in true prima che l&#39;azione vincolata sia consentita&quot;

* **Identificatori dei segmenti**

   Identificatori dei segmenti

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


#### Dettagli classificazione

Classificazione (priorità). Definisce ciò che viene considerato la \&quot;azione migliore\&quot; in base al contesto del criterio di decisione. Tra tutte le opzioni selezionate che soddisfano il vincolo di idoneità, l’ordine di classificazione deciderà l’opzione o le opzioni superiori N da proporre.

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

      Valori possibili: &quot;static&quot;, &quot;scoringFunction&quot;, &quot;rankingStrategy&quot; <!--(TBC)-->

   * **Strategia di classificazione**

      Riferimento a una strategia che classifica un elenco di opzioni decisionali. Le opzioni di decisione verranno restituite in un elenco ordinato. Il valore di questa proprietà è l&#39;URI (@id) della funzione da richiamare con l&#39;opzione on alla volta. Vedi schema https://ns.adobe.com/experience/decisioning/rankingStrategy.

      Tipo: string

* **Priorità**

   La priorità di un&#39;unica opzione di decisione rispetto a tutte le altre opzioni. Le opzioni per le quali non è specificata alcuna funzione di ordine hanno priorità utilizzando questa proprietà. Le opzioni con valori di priorità più elevati vengono selezionate prima di qualsiasi opzione di priorità più bassa. Se due o più opzioni qualificate condividono il valore di priorità più elevato, una viene scelta in modo casuale uniforme e utilizzata per la proposta di decisione.

   Tipo: integer

   Valore minimo: 0

   Valore predefinito: 0

#### Tag

Set di tag associati a questa entità. I tag vengono utilizzati nelle espressioni filtro per vincolare l’inventario complessivo a un sottoinsieme (categoria).

* **items**

   Identificatore di un oggetto tag. Il valore è @id del tag a cui si fa riferimento. Vedi schema tag: https://ns.adobe.com/experience/decisioning/tag.

## _repo

### Opzione di decisione ETag

Revisione in cui si trovava l&#39;oggetto opzione di decisione al momento dell&#39;esecuzione dello snapshot.

Tipo: string



