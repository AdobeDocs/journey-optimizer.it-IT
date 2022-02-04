---
title: Set di dati di offerte di fallback
description: In questa sezione sono elencati tutti i campi utilizzati nel set di dati esportato per le offerte di fallback
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 73bfdc24-28cf-4cfd-bac9-a4ff1ea543e3
source-git-commit: 0545cda9f91ff18791310a4ee2463b2287ac7557
workflow-type: tm+mt
source-wordcount: '1045'
ht-degree: 0%

---

# Set di dati di offerte di fallback {#fallback-dataset}

Ogni volta che un’offerta viene modificata, viene aggiornato il set di dati generato automaticamente per le offerte di fallback.

![](../../assets/dataset-fallback.png)

Il batch di successo più recente nel set di dati viene visualizzato a destra. La visualizzazione gerarchica dello schema per il set di dati viene visualizzata nel riquadro a sinistra.

>[!NOTE]
>
>Scopri come accedere ai set di dati esportati per ciascun oggetto della Libreria offerte in [questa sezione](../export-catalog/access-dataset.md).

Elenco di tutti i campi che possono essere utilizzati nella **[!UICONTROL Decision Object Repository - Fallback Offers]** set di dati.

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

#### _esperienza > decisione > caratteristiche

**Campo:** caratteristiche
**Titolo:** Caratteristiche dell&#39;opzione di decisione
**Descrizione:** Proprietà o attributi aggiuntivi appartenenti a questa particolare opzione di decisione. istanze diverse possono avere caratteristiche diverse (chiavi nella mappa). Le caratteristiche sono coppie di valori nome utilizzate per distinguere un’opzione di decisione da altre. Le caratteristiche vengono utilizzate come valori nel contenuto che rappresenta questa opzione decisionale e come funzioni per analizzare e ottimizzare le prestazioni di un’opzione. Quando ogni istanza ha lo stesso attributo o proprietà, tale aspetto deve essere modellato come uno schema di estensione che deriva dai dettagli dell’opzione di decisione.
**Tipo:** oggetto

<!--Field under Characteristics without title = additionalProperties? Desc = Value of the property. Type: string-->

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
   **Descrizione:** Set enumerato di URI in cui ogni valore corrisponde a un tipo assegnato al componente contenuto. Alcuni consumatori delle rappresentazioni di contenuto si aspettano che il valore @type sia un riferimento allo schema che descrive proprietà aggiuntive del componente di contenuto.
   **Tipo:** string

* **_esperienza > decisioni > contenuti > componenti > _dc**

   **Campo:** _dc
   **Tipo:** oggetto
   **Obbligatorio:** &quot;format&quot;

   * **Formato**

      **Campo:** format
      **Titolo:** Formato
      **Descrizione:** La manifestazione fisica o digitale della risorsa. In genere, Format deve includere il tipo di supporto della risorsa. Il formato può essere utilizzato per determinare il software, l&#39;hardware o altre apparecchiature necessarie per visualizzare o utilizzare la risorsa. Si consiglia di selezionare un valore da un vocabolario controllato (ad esempio, l&#39;elenco di [Tipi di file multimediali Internet](http://www.iana.org/ assegnazioni/tipi di file multimediali/) definizione dei formati di file multimediali per computer).
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
