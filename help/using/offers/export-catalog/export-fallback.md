---
title: Set di dati delle offerte di fallback
description: Questa sezione elenca tutti i campi utilizzati nel set di dati esportato per le offerte di fallback
feature: Decision Management, Datasets
topic: Integrations
role: User, Data Engineer
level: Intermediate
exl-id: 73bfdc24-28cf-4cfd-bac9-a4ff1ea543e3
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '1056'
ht-degree: 3%

---

# Set di dati delle offerte di fallback {#fallback-dataset}

Ogni volta che viene modificata un’offerta, viene aggiornato il set di dati generato automaticamente per le offerte di fallback.

![](../assets/dataset-fallback.png)

Il batch con esito positivo più recente nel set di dati viene visualizzato a destra. La visualizzazione gerarchica dello schema per il set di dati viene visualizzata nel riquadro a sinistra.

>[!NOTE]
>
>Scopri come accedere ai set di dati esportati per ogni oggetto della Libreria di offerte in [questa sezione](../export-catalog/access-dataset.md).

Elenco di tutti i campi che possono essere utilizzati nel **[!UICONTROL Archivio oggetti decisione - Offerte di fallback]** set di dati.

+++ Identificatore

**Campo:** _id
**Titolo:** Identificatore
**Descrizione:** Identificatore univoco del record.
**Tipo:** stringa

+++

+++ _esperienza

**Campo:** _experience
**Tipo:** oggetto

+++

+++ _experience > decisioning

**Campo:** decisioning
**Tipo:** oggetto

+++

+++ _experience > decisioning > caratteristiche

**Campo:** caratteristiche
**Titolo:** Caratteristiche dell’opzione di decisione
**Descrizione:** Proprietà o attributi aggiuntivi appartenenti a questa particolare opzione di decisione. Diverse istanze possono avere caratteristiche diverse (chiavi nella mappa). Le caratteristiche sono coppie di nome e valore utilizzate per distinguere un’opzione di decisione dalle altre. Le caratteristiche vengono utilizzate come valori nel contenuto che rappresenta questa opzione di decisione e come funzioni per analizzare e ottimizzare le prestazioni di un’opzione. Quando ogni istanza ha lo stesso attributo o proprietà, tale aspetto deve essere modellato come schema di estensione che deriva dai dettagli dell’opzione di decisione.
**Tipo:** oggetto

+++

<!--Field under Characteristics without title = additionalProperties? Desc = Value of the property. Type: string-->

+++ _experience > decisioning > content

**Campo:** sommario
**Titolo:** Dettagli contenuto
**Descrizione:** Elementi di contenuto per il rendering dell’elemento decisione in contesti diversi. Una singola opzione di decisione può avere più varianti di contenuto. Il contenuto è un’informazione destinata a un pubblico e destinata a essere utilizzata in un’esperienza (digitale). I contenuti vengono distribuiti attraverso i canali in un particolare posizionamento.
**Tipo:** array

+++

+++_esperienza > decisioni > contenuti > componenti

**Campo:** componenti
**Descrizione:** I componenti del contenuto che rappresentano l’opzione di decisione, incluse tutte le varianti linguistiche. Componenti specifici disponibili sono &#39;dx:format&#39;, &#39;dc:subject&#39; e &#39;dc:language&#39; o una loro combinazione. Questi metadati vengono utilizzati per individuare o rappresentare il contenuto associato a un’offerta e integrarlo in base al contratto di posizionamento.
**Tipo:** array
**Obbligatorio:** &quot;_type&quot;, &quot;_dc&quot; <!--TBC?-->

* **_experience > decisioning > contenuti > componenti > Tipo di componente Contenuto**

  **Campo:** _type
  **Titolo:** Tipo di componente contenuto
  **Descrizione:** Set enumerato di URI in cui ogni valore corrisponde a un tipo assegnato al componente contenuto. Alcuni consumatori delle rappresentazioni di contenuto si aspettano che il valore @type sia un riferimento a uno schema che descrive proprietà aggiuntive del componente contenuto.
  **Tipo:** stringa

* **_esperienza > decisioni > contenuti > componenti > _dc**

  **Campo:** _dc
  **Tipo:** oggetto
  **Obbligatorio:** &quot;format&quot;

   * **Formato**

     **Campo:** formato
     **Titolo:** Formato
     **Descrizione:** La manifestazione fisica o digitale della risorsa. In genere, il formato deve includere il tipo di file multimediale della risorsa. Il formato può essere utilizzato per determinare il software, l&#39;hardware o altre apparecchiature necessarie per visualizzare o utilizzare la risorsa. Si consiglia di selezionare un valore da un vocabolario controllato (ad esempio, l’elenco di [Tipi di file multimediali Internet](https://www.iana.org/ assegnazioni/tipi di file multimediali/) definizione dei formati di file multimediali per computer).
     **Tipo:** stringa
     **Esempio:** &quot;application/vnd.adobe.photoshop&quot;

   * **Lingua**

     **Campo:** lingua
     **Titolo:** Lingua
     **Descrizione:** Lingua o lingue della risorsa. \nLe lingue sono specificate nel codice della lingua definito in [IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt), che fa parte di BCP 47, utilizzato altrove in XDM.
     **Tipo:** array
     **Esempi:** &quot;\n&quot;, &quot;pt-BR&quot;, &quot;es-ES&quot;

* **_experience > decisioning > sommario > componenti > _repo**

  **Campo:** _repo
  **Tipo:** oggetto

   * **id**

     **Campo:** id
     **Descrizione:** Identificatore univoco facoltativo per fare riferimento alla risorsa in un archivio di contenuti. Quando si utilizzano le API di Platform per recuperare la rappresentazione, il client può aspettarsi una proprietà aggiuntiva \&quot;repo:resolveUrl\&quot; per recuperare la risorsa.
     **Tipo:** stringa
     **Esempio:** &quot;urn:aaid:sc:US:6dc33479-13ca-4b19-b25d-c805eff8a69e&quot;

   * **nome**

     **Campo:** nome
     **Descrizione:** Alcuni suggerimenti su dove individuare l’archivio in cui è memorizzata la risorsa esterna dal \&quot;repo:id\&quot;.
     **Tipo:** stringa

   * **repositoryID**

     **Campo:** repositoryID
     **Descrizione:** Identificatore univoco facoltativo per fare riferimento alla risorsa in un archivio di contenuti. Quando si utilizzano le API di Platform per recuperare la rappresentazione, il client può aspettarsi una proprietà aggiuntiva \&quot;repo:resolveUrl\&quot; per recuperare la risorsa.
     **Tipo:** stringa
     **Esempio:** C87932A55B06F7070A49412D@AdobeOrg

   * **resolveURL**

     **Campo:** resolveURL
     **Descrizione:** Un localizzatore di risorse univoco facoltativo per leggere la risorsa in un archivio di contenuti. In questo modo sarà più facile ottenere la risorsa senza che il cliente capisca dove viene gestita e quali API chiamare. Questo è simile a un collegamento HAL, ma la semantica è più semplice e più mirata.
     **Tipo:** stringa
     **Esempio:** &quot;https://plaftform.adobe.io/resolveByPath?path=&quot;/mycorp/content/projectx/fragment/prod/herobanners/banner14.html3&quot;&quot;

* **_esperienza > decisioning > contenuti > componenti > contenuto**

  **Campo:** contenuto
  **Descrizione:** Un campo facoltativo che contiene direttamente il contenuto. Invece di fare riferimento al contenuto in un archivio di risorse, il componente può contenere direttamente il contenuto semplice. Questo campo non viene utilizzato per risorse di contenuto composito, complesso e binario.
  **Tipo:** stringa

* **_experience > decisioning > contenuti > componenti > deliveryURL**

  **Campo:** deliveryURL
  **Descrizione:** Un localizzatore di risorse univoco facoltativo per ottenere la risorsa da una rete di distribuzione di contenuti o da un endpoint di servizio. Questo URL viene utilizzato per accedere alla risorsa pubblicamente da un agente utente.
  **Tipo:** stringa
  **Esempio:** https://cdn.adobe.io/content/projectx/fragment/prod/static/1232324wd32.jpeg

* **_experience > decisioning > contenuti > componenti > linkURL**

  **Campo:** linkURL
  **Descrizione:** Un localizzatore di risorse univoco facoltativo per le interazioni dell’utente. Questo URL viene utilizzato per fare riferimento all’utente finale in un agente utente e può essere tracciato.
  **Tipo:** stringa
  **Esempio:** https://cdn.adobe.io/tracker?code=23432&amp;redirect=/content/projectx/fragment/prod/static/1232324wd32.jpeg

+++

+++ _experience > decisioning > content > Placement (Esperienza > decisioni > contenuti > Posizionamento)

**Campo:** posizionamento
**Titolo:** Posizione
**Descrizione:** Posizionamento per conformarsi a. Il valore è l’URI (@id) del posizionamento dell’offerta a cui si fa riferimento. Consulta schema https://ns.adobe.com/experience/decisioning/placement.
**Tipo:** stringa

+++

+++ _experience > decisioning > Stato del ciclo di vita

**Campo:** lifecycleStatus
**Titolo:** Stato del ciclo di vita
**Descrizione:** Lo stato del ciclo di vita consente di eseguire flussi di lavoro con un oggetto. Lo stato può influenzare il punto in cui un oggetto è visibile o considerato rilevante. Le modifiche di stato sono guidate dai client o dai servizi che utilizzano gli oggetti.
**Tipo:** stringa
**Valori possibili:** &quot;Bozza&quot; (predefinito), &quot;Approvato&quot;, &quot;Live&quot;, &quot;Completato&quot;, &quot;Archiviato&quot;

+++

+++ _experience > decisioning > Nome opzione decisione

**Campo:** nome
**Titolo:** Nome opzione di decisione
**Descrizione:** Nome dell&#39;opzione visualizzato in varie interfacce utente.
**Tipo:** stringa

+++

+++ _experience > decisioning > tag

**Campo:** tag
**Titolo:** Tag
**Descrizione:** Il set di qualificatori di raccolta (precedentemente noti come &quot;tag&quot;) associati a questa entità. I qualificatori di raccolta vengono utilizzati nelle espressioni di filtro per vincolare l’inventario complessivo a un sottoinsieme (categoria).
**Tipo:** array

+++

<!--Field without name under collection qualifiers: Description: An identifier of a collection qualifier object. The value is the @id of the collection qualifier that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

+++ _repo

**Campo:** _repo
**Tipo:** oggetto

+++

+++ _repo > Opzione di decisione ETag

**Campo:** etag
**Titolo:** Opzione di decisione ETag
**Descrizione:** Revisione in cui si trovava l’oggetto opzione di decisione quando è stata acquisita l’istantanea.
**Tipo:** stringa

+++
