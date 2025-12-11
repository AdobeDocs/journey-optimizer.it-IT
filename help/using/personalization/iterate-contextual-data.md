---
solution: Journey Optimizer
product: journey optimizer
title: Eseguire iterazioni sui dati contestuali
description: Scopri come eseguire iterazioni su array provenienti da varie origini di contesto utilizzando la sintassi Handlebars
feature: Personalization
topic: Personalization
role: Developer
level: Intermediate
hide: true
hidefromtoc: true
keywords: espressione, editor, manubrio, iterazione, array, contesto, personalizzazione
source-git-commit: a67707e50960e4848197fa1bd39ce95af3ef14ab
workflow-type: tm+mt
source-wordcount: '2484'
ht-degree: 3%

---

# Eseguire iterazioni sui dati contestuali {#personalization-contexts}

Scopri come utilizzare la sintassi di iterazione Handlebars per visualizzare elenchi dinamici di dati provenienti da varie origini nei messaggi, inclusi eventi, risposte di azioni personalizzate e altri dati contestuali.

## Panoramica {#overview}

Journey Optimizer fornisce l&#39;accesso ai dati contestuali provenienti da più origini durante la [personalizzazione dei messaggi](personalize.md). Puoi eseguire iterazioni su array da queste origini utilizzando la sintassi Handlebars nei canali nativi ([email](../email/get-started-email-design.md), [push](../push/create-push.md), [SMS](../sms/create-sms.md)) per visualizzare contenuti dinamici come elenchi di prodotti, consigli o altri elementi ripetuti.

**Origini di contesto disponibili:**

* **[Eventi](#event-data)**: dati da eventi di percorso (eventi di business, eventi unitari)
* **[Risposte alle azioni personalizzate](#custom-action-responses)**: dati restituiti da chiamate API esterne tramite azioni personalizzate
* **[Ricerca set di dati](#dataset-lookup)**: dati arricchiti recuperati dai set di dati di Adobe Experience Platform
* **[Proprietà tecniche](#technical-properties)**: metadati di Percorso come ID percorso e identificatori supplementari
* **[Contesto Percorso](#other-contexts)**: altri dati relativi al percorso accessibili durante l&#39;esecuzione

Questa guida illustra come eseguire iterazioni su array da ciascuna di queste origini nei messaggi e come utilizzare gli array durante la configurazione delle attività di percorso. Inizia con [Sintassi di iterazione Handlebars](#syntax) per comprendere le nozioni di base sulla personalizzazione dei messaggi, oppure passa a [Utilizza gli array nelle espressioni di Percorso](#arrays-in-journeys) per scoprire come passare i dati degli array alle azioni personalizzate e alle ricerche di set di dati.

## Sintassi di iterazione Handlebars {#syntax}

Handlebars fornisce a `{{#each}}` [helper](functions/helpers.md) l&#39;iterazione su array. La sintassi di base è:

```handlebars
{{#each arrayPath as |item|}}
  <!-- Access item properties here -->
  {{item.property}}
{{/each}}
```

**Punti chiave:**

* Sostituisci `arrayPath` con il percorso dei tuoi dati array
* Sostituisci `item` con il nome di variabile desiderato (ad esempio `product`, `response`, `element`)
* Accedere alle proprietà di ogni elemento utilizzando `{{item.propertyName}}`
* È possibile nidificare più blocchi `{{#each}}` per array multilivello

## Iterazione dei dati evento {#event-data}

I dati evento sono disponibili quando il percorso viene attivato da un [evento](../event/about-events.md). Ciò è utile per visualizzare i dati acquisiti al momento dell’avvio del percorso, ad esempio il contenuto del carrello, gli elementi dell’ordine o gli invii di moduli.

>[!TIP]
>
>Puoi combinare i dati dell’evento con altre origini. Per esempi, vedere [Combinare più origini di contesto](#combine-sources).

### Percorso contesto per gli eventi

```handlebars
context.journey.events.<event_ID>.<fieldPath>
```

* `<event_ID>`: ID univoco dell&#39;evento configurato nel percorso
* `<fieldPath>`: percorso del campo o dell&#39;array nello schema eventi

### Esempio: Cart items from an event (Carrelli da un evento)

Se lo schema [evento](../event/experience-event-schema.md) include un array `productListItems` (formato [XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/product-list-item.html?lang=it){target="_blank"} standard), puoi visualizzare il contenuto del carrello come segue:

```handlebars
{{#each context.journey.events.event_ID.productListItems as |product|}}
  <div class="product">
    <h3>{{product.name}}</h3>
    <p>Quantity: {{product.quantity}}</p>
    <p>Price: ${{product.priceTotal}}</p>
  </div>
{{/each}}
```

### Esempio: array nidificati negli eventi

Per le strutture nidificate, utilizzare blocchi `{{#each}}` nidificati. Ulteriori informazioni sulla nidificazione in [Best practice](#best-practices).

```handlebars
{{#each context.journey.events.event_ID.categories as |category|}}
  <h2>{{category.name}}</h2>
  <ul>
    {{#each category.items as |item|}}
      <li>{{item.title}}</li>
    {{/each}}
  </ul>
{{/each}}
```

## Alterna le risposte di azione personalizzate {#custom-action-responses}

[Le risposte all&#39;azione personalizzata](../action/about-custom-action-configuration.md) contengono dati restituiti da chiamate API esterne. È utile per visualizzare informazioni in tempo reale dai sistemi, ad esempio punti fedeltà, consigli di prodotto, stato dell’inventario o offerte personalizzate.

>[!NOTE]
>
>Per utilizzare questa funzione, le azioni personalizzate devono essere configurate con un payload di risposta. Ulteriori informazioni in [questa sezione](../action/action-response.md#config-response). Puoi anche combinare le risposte alle azioni personalizzate con i dati evento o le ricerche di set di dati. Per esempi, consulta [Combinare più origini di contesto](#combine-sources).

### Percorso contestuale per azioni personalizzate

```handlebars
context.journey.actions.<actionName>.<fieldPath>
```

* `<actionName>`: nome dell&#39;[azione personalizzata](../action/about-custom-action-configuration.md) configurata nel percorso
* `<fieldPath>`: percorso del campo o dell&#39;array all&#39;interno del payload di risposta

### Esempio: consigli di prodotto da un’API

Se l’azione personalizzata restituisce consigli di prodotto:

**Risposta API:**

```json
{
  "recommendations": [
    {
      "productId": "12345",
      "productName": "Summer Jacket",
      "price": 89.99,
      "imageUrl": "https://example.com/jacket.jpg"
    },
    {
      "productId": "67890",
      "productName": "Running Shoes",
      "price": 129.99,
      "imageUrl": "https://example.com/shoes.jpg"
    }
  ]
}
```

**Personalizzazione dei messaggi:**

```handlebars
<h2>Recommended for You</h2>
<div class="recommendations">
  {{#each context.journey.actions.GetRecommendations.recommendations as |item|}}
    <div class="product-card">
      <img src="{{item.imageUrl}}" alt="{{item.productName}}" />
      <h3>{{item.productName}}</h3>
      <p class="price">${{item.price}}</p>
    </div>
  {{/each}}
</div>
```

### Esempio: array nidificati da azioni personalizzate

Se l’azione personalizzata restituisce array nidificati (ad esempio, categorie con prodotti). Per schemi di nidificazione più complessi, consulta [Best practice](#best-practices).

**Risposta API:**

```json
{    
  "id": "84632848268632",    
  "responses": [
    { "productIDs": [1111, 2222, 3333] },
    { "productIDs": [4444, 5555, 6666] },
    { "productIDs": [7777, 8888, 9999] }
  ]
}
```

**Personalizzazione dei messaggi:**

```handlebars
<h2>Product Groups</h2>
{{#each context.journey.actions.GetProducts.responses as |response|}}
  <div class="product-group">
    <ul>
      {{#each response.productIDs as |productID|}}
        <li>Product ID: {{productID}}</li>
      {{/each}}
    </ul>
  </div>
{{/each}}
```

### Esempio: vantaggi del livello fedeltà

Visualizzare i vantaggi dinamici in base allo stato di fedeltà:

**Risposta API:**

```json
{
  "loyaltyTier": "gold",
  "benefits": [
    { "name": "Free shipping", "icon": "truck" },
    { "name": "20% discount", "icon": "percent" },
    { "name": "Priority support", "icon": "headset" }
  ]
}
```

**Personalizzazione dei messaggi:**

```handlebars
<h2>Your {{context.journey.actions.GetLoyaltyInfo.loyaltyTier}} Member Benefits</h2>
<ul class="benefits">
  {{#each context.journey.actions.GetLoyaltyInfo.benefits as |benefit|}}
    <li>
      <span class="icon-{{benefit.icon}}"></span>
      {{benefit.name}}
    </li>
  {{/each}}
</ul>
```

## Alterna i risultati della ricerca del set di dati {#dataset-lookup}

L&#39;[attività di ricerca set di dati](../building-journeys/dataset-lookup.md) ti consente di recuperare dati dai [set di dati Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=it){target="_blank"} durante il runtime di percorso. I dati arricchiti vengono memorizzati come array e possono essere iterati nei messaggi.

>[!AVAILABILITY]
>
>L’attività di ricerca del set di dati è disponibile solo per un set limitato di organizzazioni. Per ottenere l’accesso, contatta il tuo rappresentante Adobe.

Ulteriori informazioni sulla configurazione dell&#39;attività di ricerca del set di dati in [questa sezione](../building-journeys/dataset-lookup.md). La ricerca del set di dati è particolarmente efficace quando viene combinata con i dati dell&#39;evento. Vedere [Esempio: dati dell&#39;evento arricchiti con la ricerca del set di dati](#combine-sources) per un caso d&#39;uso pratico.

### Percorso contesto per le ricerche dei set di dati

```handlebars
context.journey.datasetLookup.<activityID>.entities
```

* `<activityID>`: ID univoco dell&#39;attività di ricerca del set di dati
* `entities`: array di dati arricchiti recuperati dal set di dati

### Esempio: dettagli del prodotto da un set di dati

Se utilizzi un’attività di ricerca del set di dati per recuperare informazioni di prodotto in base agli SKU:

**Configurazione ricerca set di dati:**

* Chiavi di ricerca: `list(@event{purchase_event.products.sku})`
* Campi da restituire: `["SKU", "category", "price", "name"]`

**Personalizzazione dei messaggi:**

```handlebars
<h2>Product Details</h2>
<table>
  <thead>
    <tr>
      <th>Product Name</th>
      <th>Category</th>
      <th>Price</th>
    </tr>
  </thead>
  <tbody>
    {{#each context.journey.datasetLookup.3709000.entities as |product|}}
      <tr>
        <td>{{product.name}}</td>
        <td>{{product.category}}</td>
        <td>${{product.price}}</td>
      </tr>
    {{/each}}
  </tbody>
</table>
```

### Esempio: iterazione filtrata con dati del set di dati

Visualizza solo i prodotti di una categoria specifica. Ulteriori informazioni sul filtro condizionale in [Best practice](#best-practices).

```handlebars
<h2>Household Products</h2>
{{#each context.journey.datasetLookup.3709000.entities as |product|}}
  {{#if product.category = "household"}}
    <div class="product">
      <h3>{{product.name}}</h3>
      <p>Price: ${{product.price}}</p>
    </div>
  {{/if}}
{{/each}}
```

### Esempio: calcolare i totali dalla ricerca del set di dati

```handlebars
{% let householdTotal = 0 %}
{{#each context.journey.datasetLookup.3709000.entities as |product|}}
  {%#if product.category = "household"%}
    {% let householdTotal = householdTotal + product.price %}
  {%/if%}
{{/each}}

<p>Your household products total: ${{householdTotal}}</p>
```

## Usa proprietà tecniche del percorso {#technical-properties}

Le proprietà tecniche del percorso consentono di accedere ai metadati sull&#39;esecuzione del percorso, ad esempio l&#39;ID percorso e gli identificatori supplementari. Questi possono essere utili se combinati con pattern di iterazione, in particolare per filtrare gli array in base a specifiche istanze di percorso.

### Proprietà tecniche disponibili

```handlebars
context.journey.technicalProperties.journeyUID
context.journey.technicalProperties.supplementalId
```

### Esempio: filtrare gli elementi array utilizzando l’identificatore supplementare

Quando si utilizzano identificatori supplementari in percorsi attivati da eventi con array, è possibile filtrare per visualizzare solo l&#39;elemento rilevante per l&#39;istanza di percorso corrente. Ulteriori informazioni sugli identificatori supplementari in [questa guida](../building-journeys/supplemental-identifier.md).

**Scenario**: un percorso viene attivato con più prenotazioni, ma desideri visualizzare solo le informazioni per la prenotazione specifica (identificata dall&#39;ID supplementare) che ha attivato questa istanza di percorso.

```handlebars
{{#each context.journey.events.event_ID.bookingList as |booking|}}
  {%#if booking.bookingInfo.bookingNum = context.journey.technicalProperties.supplementalId%}
    <div class="booking-details">
      <h3>Your Booking: {{booking.bookingInfo.bookingNum}}</h3>
      <p>Destination: {{booking.bookingInfo.bookingCountry}}</p>
      <p>Date: {{booking.bookingInfo.bookingDate}}</p>
    </div>
  {%/if%}
{{/each}}
```

### Esempio: Includi ID percorso per il tracciamento

```handlebars
<footer>
  <p>Journey Reference: {{context.journey.technicalProperties.journeyUID}}</p>
</footer>
```

## Combinare più origini di contesto {#combine-sources}

Puoi combinare dati provenienti da origini diverse nello stesso messaggio per creare esperienze avanzate e personalizzate. In questa sezione vengono illustrati esempi pratici di utilizzo congiunto di più origini di contesto.

**Origini di contesto che è possibile combinare:**

* [Dati evento](#event-data) + [Risposte azione personalizzate](#custom-action-responses)
* [Dati evento](#event-data) + [Ricerca set di dati](#dataset-lookup)
* [Più origini](#combine-sources) + [Proprietà tecniche](#technical-properties)

### Esempio: articoli del carrello con inventario in tempo reale

Combina i dati evento (contenuti del carrello) con i dati azione personalizzati (stato inventario):

```handlebars
<h2>Your Cart</h2>
{{#each context.journey.events.cartEvent.productListItems as |product|}}
  <div class="cart-item">
    <h3>{{product.name}}</h3>
    <p>Quantity: {{product.quantity}}</p>
    <p>Price: ${{product.priceTotal}}</p>
  </div>
{{/each}}

<h2>We Also Recommend</h2>
{{#each context.journey.actions.GetRecommendations.items as |recommendation|}}
  <div class="recommendation">
    <h4>{{recommendation.name}}</h4>
    <p>${{recommendation.price}}</p>
    {{#if recommendation.inStock}}
      <span class="badge">In Stock</span>
    {{else}}
      <span class="badge out-of-stock">Out of Stock</span>
    {{/if}}
  </div>
{{/each}}
```

### Esempio: dati evento arricchiti con la ricerca del set di dati

Combina [SKU evento](#event-data) con informazioni dettagliate sul prodotto da una [ricerca set di dati](#dataset-lookup):

```handlebars
<h2>Your Order Details</h2>
{{#each context.journey.events.orderEvent.productListItems as |item|}}
  <div class="order-item">
    <p><strong>SKU:</strong> {{item.SKU}}</p>
    <p><strong>Quantity:</strong> {{item.quantity}}</p>
    
    <!-- Enrich with dataset lookup data -->
    {{#each context.journey.datasetLookup.1234567.entities as |enrichedProduct|}}
      {{#if enrichedProduct.SKU = item.SKU}}
        <p><strong>Product Name:</strong> {{enrichedProduct.name}}</p>
        <p><strong>Category:</strong> {{enrichedProduct.category}}</p>
        <img src="{{enrichedProduct.imageUrl}}" alt="{{enrichedProduct.name}}" />
      {{/if}}
    {{/each}}
  </div>
{{/each}}
```

### Esempio: combinare più origini con proprietà tecniche

```handlebars
<div class="personalized-content">
  <!-- Profile data -->
  <h1>Hello {{profile.person.name.firstName}},</h1>
  
  <!-- Event data iteration -->
  <h2>Your Recent Purchases</h2>
  {{#each context.journey.events.purchaseEvent.items as |purchase|}}
    <div class="purchase">
      <p>{{purchase.productName}} - ${{purchase.price}}</p>
    </div>
  {{/each}}
  
  <!-- Custom action response iteration -->
  <h2>Recommended for You</h2>
  {{#each context.journey.actions.GetPersonalizedRecs.recommendations as |rec|}}
    <div class="recommendation">
      <h3>{{rec.title}}</h3>
      <p>{{rec.description}}</p>
    </div>
  {{/each}}
  
  <!-- Technical properties -->
  <footer>
    <p class="fine-print">Journey ID: {{context.journey.technicalProperties.journeyUID}}</p>
  </footer>
</div>
```

## Altri tipi di contesto {#other-contexts}

Mentre questa guida si concentra sull’iterazione rispetto agli array, per la personalizzazione sono disponibili altri tipi di contesto che in genere non richiedono l’iterazione. L’accesso a questi elementi è diretto anziché ripetuto ciclicamente:

* **[Attributi profilo](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=it){target="_blank"}** (`profile.*`): singoli campi profilo da Adobe Experience Platform
* **[Tipi di pubblico](../audience/about-audiences.md)** (`inAudience()`): verifiche appartenenza pubblico
* **[Decisioni di offerta](../offers/get-started/starting-offer-decisioning.md)**: offerte di gestione delle decisioni
* **[Attributi di destinazione](../orchestrated/activities/channels.md#add-personalization)** (solo campagne orchestrate): attributi calcolati nell&#39;area di lavoro della campagna
* **Token** (`context.token`): token di sessione o autenticazione

Per informazioni sulla sintassi di personalizzazione completa e sugli esempi che utilizzano queste origini, consulta:

* [Aggiungere personalizzazione](personalization-build-expressions.md)
* [Sintassi di personalizzazione](personalization-syntax.md)

## Utilizzare gli array nelle espressioni di Percorso {#arrays-in-journeys}

Mentre le sezioni precedenti si concentrano sull’iterazione degli array nella personalizzazione dei messaggi utilizzando Handlebars, puoi anche lavorare con gli array durante la configurazione delle attività del percorso. Questa sezione spiega come utilizzare i dati array dagli eventi nelle espressioni di Percorso, in particolare quando si trasmettono dati ad azioni personalizzate o si utilizzano array con ricerche di set di dati.

>[!IMPORTANT]
>
>Le espressioni di percorso utilizzano una sintassi diversa rispetto alla personalizzazione Handlebars. Nella configurazione del percorso (ad esempio parametri o condizioni di azioni personalizzate), si utilizza l&#39;[editor espressioni di Percorso](../building-journeys/expression/expressionadvanced.md) con funzioni quali `first`, `all` e `serializeList`. Nel contenuto del messaggio viene utilizzata la sintassi Handlebars con `{{#each}}` loop.

### Trasmettere i valori dell’array ai parametri delle azioni personalizzati {#arrays-to-custom-actions}

Durante la configurazione di [azioni personalizzate](../action/about-custom-action-configuration.md), spesso è necessario estrarre i valori dagli array di eventi e trasmetterli come parametri. Questa sezione descrive i pattern comuni.

Ulteriori informazioni sul passaggio delle raccolte in [Trasmettere le raccolte nei parametri delle azioni personalizzate](../building-journeys/collections.md#passing-collection).

#### Estrarre un singolo valore da un array

**Caso d&#39;uso**: ottieni un campo specifico da un array di eventi da passare come parametro di query in una richiesta GET.

**Scenario di esempio**: estrarre il primo SKU con un prezzo maggiore di 0 da un elenco di prodotti.

**Esempio di schema evento**:

```json
{
  "commerce": {
    "productListItems": [
      { "SKU": "SKU-1", "priceTotal": 10.0 },
      { "SKU": "SKU-2", "priceTotal": 0.0 },
      { "SKU": "SKU-3", "priceTotal": 20.0 }
    ]
  }
}
```

**Configurazione azione personalizzata**:

1. Nell&#39;azione personalizzata configurare un parametro di query (ad esempio, `sku`) con tipo `string`
2. Contrassegnalo come `Variable` per consentire valori dinamici

**Espressione Percorso nel parametro azione**:

```javascript
@event{YourEventName.commerce.productListItems.first(currentEventField.priceTotal > 0).SKU}
```

**Spiegazione**:

* `@event{YourEventName}`: fa riferimento all&#39;evento di percorso
* `.first(currentEventField.condition)`: restituisce il primo elemento di matrice che corrisponde alla condizione
* `currentEventField`: rappresenta ogni elemento nell&#39;array di eventi mentre lo si scorre
* `.SKU`: estrae il campo SKU dall&#39;elemento corrispondente
* Risultato: `"SKU-1"` (stringa adatta al parametro azione)

Ulteriori informazioni sulla funzione `first` in [Funzioni di gestione della raccolta](../building-journeys/expression/collection-management-functions.md).

#### Creare un elenco di valori da un array

**Caso d&#39;uso**: crea un elenco separato da virgole di ID da passare come parametro di query (ad esempio, `/products?ids=sku1,sku2,sku3`).

**Configurazione azione personalizzata**:

1. Configurare un parametro di query (ad esempio, `ids`) con il tipo `string`
2. Contrassegna come `Variable`

**Espressione Percorso**:

```javascript
serializeList(
  @event{YourEventName.commerce.productListItems.all(currentEventField.priceTotal > 0).SKU},
  ",",
  true
)
```

**Spiegazione**:

* `.all(currentEventField.condition)`: restituisce tutti gli elementi matrice che corrispondono alla condizione (restituisce un elenco)
* `currentEventField`: rappresenta ogni elemento nell&#39;array di eventi mentre lo si scorre
* `.SKU`: progetta l&#39;elenco in modo da includere solo valori SKU
* `serializeList(list, delimiter, addQuotes)`: unisce l&#39;elenco in una stringa
   * `","`: Usa la virgola come delimitatore
   * `true`: Aggiungi virgolette intorno a ogni elemento stringa
* Risultato: `"SKU-1,SKU-3"` (adatto a un parametro di query)

Ulteriori informazioni su:

* [&#39;all&#39;](../building-journeys/expression/collection-management-functions.md)
* [`serializeList`](../building-journeys/functions/list-functions.md#serializeList)

La gestione delle raccolte per le azioni personalizzate è descritta in [Trasmettere le raccolte nei parametri delle azioni personalizzate](../building-journeys/collections.md#passing-collection).

#### Trasmettere un array di oggetti a un’azione personalizzata

**Caso d&#39;uso**: invia una matrice completa di oggetti nel corpo di una richiesta (per POST o GET con corpo).

**Esempio di corpo della richiesta**:

```json
{
  "ctxt": {
    "products": [
      {
        "id": "productA",
        "name": "Product A",
        "price": 20.1,
        "color": "blue"
      }
    ]
  }
}
```

**Configurazione azione personalizzata**:

1. Nel corpo della richiesta, definisci `products` come tipo `listObject`
2. Contrassegna come `Variable`
3. Definisci i campi oggetto: `id`, `name`, `price`, `color` (ciascuno diventa mappabile)

**Configurazione area di lavoro Percorsi**:

1. In modalità avanzata, imposta l’espressione della raccolta:

   ```javascript
   @event{YourEventName.commerce.productListItems.all(currentEventField.priceTotal > 0)}
   ```

1. Nell’interfaccia utente per la mappatura della raccolta:
   * Mappa `id` → `productListItems.SKU`
   * Mappa `name` → `productListItems.name`
   * Mappa `price` → `productListItems.priceTotal`
   * Mappa `color` → `productListItems.color`

Journey Optimizer crea l’array di oggetti che corrispondono alla struttura del payload dell’azione.

>[!NOTE]
>
>Quando si lavora con array di eventi, utilizzare `currentEventField` per fare riferimento a ogni elemento. Per le raccolte di origini dati (Adobe Experience Platform), utilizzare `currentDataPackField`. Per le raccolte di risposte di azioni personalizzate, utilizzare `currentActionField`.

Ulteriori informazioni in [Trasmettere le raccolte nei parametri delle azioni personalizzate](../building-journeys/collections.md#passing-collection).

### Utilizzare gli array con le ricerche dei set di dati {#arrays-with-dataset-lookup}

Quando si utilizza l&#39;[attività di ricerca set di dati](../building-journeys/dataset-lookup.md), è possibile passare una matrice di valori come chiavi di ricerca per recuperare dati arricchiti.

**Esempio**: cerca i dettagli del prodotto per tutti gli SKU in un array di eventi.

**Configurazione ricerca set di dati**:

Nel campo delle chiavi di ricerca, utilizzare `list()` per convertire un percorso di matrice in un elenco:

```javascript
list(@event{purchaseEvent.productListItems.SKU})
```

Viene creato un elenco di tutti i valori SKU da cercare nel set di dati. I risultati sono disponibili come array in `context.journey.datasetLookup.<activityID>.entities` e possono essere ripetuti nel messaggio (vedi [Iterare nei risultati della ricerca del set di dati](#dataset-lookup)).

### Limitazioni e pattern {#array-limitations}

Tenere presenti queste limitazioni quando si lavora con array in percorsi:

#### Nessun loop dinamico su array nel flusso di percorso

I percorsi non possono creare loop dinamici in cui un nodo di azione viene eseguito più volte per ogni elemento di un array. Questo è intenzionale per evitare problemi di prestazioni inutili.

**Operazione non consentita**:

* Eseguire un&#39;azione personalizzata una volta per ogni elemento dell&#39;array in modo dinamico
* Creazione di più rami di percorso in base alla lunghezza dell’array

**Modelli consigliati**:

1. **Invia tutti gli elementi contemporaneamente**: passa l&#39;intero array o un elenco serializzato a una singola azione personalizzata che elabora tutti gli elementi. Vedere [Creare un elenco di valori da un array](#arrays-to-custom-actions).

2. **Utilizza aggregazione esterna**: chiedi all&#39;API esterna di accettare più ID e restituire risultati combinati in una singola chiamata.

3. **Pre-calcolo in AEP**: utilizzare [attributi calcolati](../audience/computed-attributes.md) per precalcolare i valori dalle matrici a livello di profilo.

4. **Estrazione valore singolo**: se è necessario un solo valore, estrarlo utilizzando `first` o `head`. Vedi [Estrarre un singolo valore da un array](#arrays-to-custom-actions).

Ulteriori informazioni in [Guardrail e limitazioni](../start/guardrails.md).

#### Considerazioni sulle dimensioni della matrice

Gli array di grandi dimensioni possono influire sulle prestazioni del percorso:

* **Array di eventi**: mantieni i payload degli eventi al di sotto di 50 KB in totale
* **Risposte alle azioni personalizzate**: i payload di risposta devono essere inferiori a 100 KB
* **Risultati ricerca set di dati**: limita il numero di chiavi di ricerca ed entità restituite

### Esempio completo: array di eventi per azione personalizzata {#complete-example}

Questo è un flusso di lavoro completo che mostra come utilizzare un array di eventi con un’azione personalizzata.

**Scenario**: quando un utente abbandona il carrello, invia i dati del carrello a un&#39;API di consigli esterna per ottenere suggerimenti personalizzati, quindi visualizzali in un messaggio e-mail.

**Passaggio 1: configurare l&#39;azione personalizzata**

Crea un’azione personalizzata &quot;GetCartRecommendations&quot;:

* **Metodo**: POST
* **URL**: `https://api.example.com/recommendations`
* **Corpo richiesta**:

```json
{
  "cartItems": [
    {
      "sku": "string",
      "price": 0,
      "quantity": 0
    }
  ]
}
```

* Contrassegna `cartItems` come tipo `listObject` e `Variable`
* Definisci i campi: `sku` (stringa), `price` (numero), `quantity` (numero intero)

Ulteriori informazioni in [Configurare un&#39;azione personalizzata](../action/about-custom-action-configuration.md).

**Passaggio 2: configurare il payload di risposta**

Nell’azione personalizzata, configura la risposta:

```json
{
  "recommendations": [
    {
      "productId": "string",
      "productName": "string",
      "price": 0,
      "imageUrl": "string"
    }
  ]
}
```

Ulteriori informazioni in [Utilizzare le risposte alle chiamate API](../action/action-response.md).

**Passaggio 3: esegui l&#39;azione nel percorso**

1. Aggiungi l’azione personalizzata dopo l’evento di abbandono del carrello
1. In modalità avanzata per la raccolta `cartItems`:

   ```javascript
   @event{cartAbandonment.commerce.productListItems.all(currentEventField.quantity > 0)}
   ```

1. Mappa i campi della raccolta:
   * `sku` → `productListItems.SKU`
   * `price` → `productListItems.priceTotal`
   * `quantity` → `productListItems.quantity`

**Passaggio 4: utilizza la risposta nell&#39;e-mail**

Nel contenuto dell’e-mail, scorri i consigli:

```handlebars
<h2>We noticed you left these items in your cart</h2>
{{#each context.journey.events.cartAbandonment.productListItems as |item|}}
  <div class="cart-item">
    <p>{{item.name}} - Quantity: {{item.quantity}}</p>
  </div>
{{/each}}

<h2>You might also like</h2>
{{#each context.journey.actions.GetCartRecommendations.recommendations as |rec|}}
  <div class="recommendation">
    <img src="{{rec.imageUrl}}" alt="{{rec.productName}}" />
    <h3>{{rec.productName}}</h3>
    <p>${{rec.price}}</p>
  </div>
{{/each}}
```

**Passaggio 5: verifica la configurazione**

Prima di eseguire un percorso live, verifica l’azione personalizzata utilizzando la funzione &quot;Send test request&quot; (Invia richiesta di test) nella configurazione dell’azione per verificare la richiesta e i valori generati.

1. Usa [modalità test percorso](../building-journeys/testing-the-journey.md)
2. Attiva con dati evento di esempio che includono un array `productListItems`
3. Verificare che l&#39;azione personalizzata riceva la struttura di array corretta
4. Controlla i [registri del test delle azioni](../action/action-response.md#test-mode-logs)
5. Visualizzare l’anteprima del messaggio e-mail per verificare che entrambi gli array siano visualizzati correttamente

Ulteriori informazioni in [Risoluzione dei problemi relativi alle azioni personalizzate](../action/troubleshoot-custom-action.md).

## Best practice {#best-practices}

Segui queste best practice durante l’iterazione di dati contestuali per creare una personalizzazione manutenibile ed performante.

### Usa nomi di variabili descrittive

Scegli nomi di variabili che indichino chiaramente ciò su cui stai eseguendo l’iterazione. Questo rende il codice più leggibile e di facile gestione. Ulteriori informazioni sulla [sintassi di personalizzazione](personalization-syntax.md):

```handlebars
<!-- Good -->
{{#each products as |product|}}
{{#each users as |user|}}
{{#each recommendations as |recommendation|}}

<!-- Less clear -->
{{#each items as |item|}}
{{#each array as |element|}}
```

### Gestire gli array vuoti

Utilizzare la clausola `{{else}}` per fornire contenuto di fallback quando un array è vuoto. Ulteriori informazioni sulle [funzioni helper](functions/helpers.md):

```handlebars
{{#each context.journey.actions.GetRecommendations.items as |item|}}
  <div>{{item.name}}</div>
{{else}}
  <p>No recommendations available at this time.</p>
{{/each}}
```

### Combina con helper condizionali

Utilizza `{{#if}}` nei cicli per il contenuto condizionale. Ulteriori informazioni sulle [regole condizionali](create-conditions.md) e esempi nelle [risposte alle azioni personalizzate](#custom-action-responses) e nelle [sezioni di ricerca set di dati](#dataset-lookup).

```handlebars
{{#each context.journey.actions.GetProducts.items as |product|}}
  <div class="product">
    <h3>{{product.name}}</h3>
    {{#if product.onSale}}
      <span class="badge">On Sale!</span>
    {{/if}}
    {{#if product.newArrival}}
      <span class="badge">New</span>
    {{/if}}
  </div>
{{/each}}
```

### Limita iterazione per prestazioni

Per array di grandi dimensioni, è consigliabile limitare il numero di iterazioni:

```handlebars
<!-- Display only first 5 items -->
{{#each context.journey.actions.GetProducts.items as |product|}}
  {{#if @index < 5}}
    <div>{{product.name}}</div>
  {{/if}}
{{/each}}
```

### Accedere ai metadati dell’array

Handlebars fornisce variabili speciali all&#39;interno di loop utili per i pattern di iterazione avanzati:

* `@index`: indice di iterazione corrente (basato su 0)
* `@first`: True per la prima iterazione
* `@last`: True per l&#39;ultima iterazione

```handlebars
{{#each products as |product|}}
  <div class="product {{#if @first}}featured{{/if}}">
    {{@index}}. {{product.name}}
  </div>
{{/each}}
```

>[!NOTE]
>
>Queste variabili Handlebars (`@index`, `@first`, `@last`) sono disponibili solo all&#39;interno di `{{#each}}` cicli nella personalizzazione dei messaggi. Per utilizzare gli array nelle espressioni di Percorso, ad esempio per ottenere il primo elemento da un array prima di passare a un&#39;azione personalizzata, utilizzare funzioni di array come [`head`](../personalization/functions/arrays-list.md#head), [`first`](../building-journeys/expression/collection-management-functions.md) o [`all`](../building-journeys/expression/collection-management-functions.md). Per ulteriori dettagli, vedi [Utilizzare gli array nelle espressioni di Percorso](#arrays-in-journeys).

## Risoluzione dei problemi {#troubleshooting}

Problemi di iterazione? In questa sezione vengono descritti problemi e soluzioni comuni.

### Array non visualizzato

**Problema**: l&#39;iterazione dell&#39;array non mostra alcun contenuto.

**Possibili cause e soluzioni**:

1. **Percorso non corretto**: verificare il percorso esatto dell&#39;array in base all&#39;origine del contesto:
   * Per [eventi](#event-data): `context.journey.events.<event_ID>.<fieldPath>`
   * Per [azioni personalizzate](#custom-action-responses): `context.journey.actions.<actionName>.<fieldPath>`
   * Per [ricerche set di dati](#dataset-lookup): `context.journey.datasetLookup.<activityID>.entities`

2. **La matrice è vuota**: aggiungere una clausola `{{else}}` per verificare se la matrice non contiene dati. Consulta [Best practice](#best-practices) per alcuni esempi.

3. **Dati non ancora disponibili**: assicurati che l&#39;azione personalizzata, l&#39;evento o l&#39;attività di ricerca del set di dati sia stata eseguita prima dell&#39;attività messaggio nel flusso di percorso.

### Errori di sintassi

**Problema**: la convalida dell&#39;espressione non riesce o il messaggio non viene visualizzato.

**Errori comuni**:

* Tag di chiusura mancanti: ogni `{{#each}}` deve avere un `{{/each}}`. Verificare la struttura corretta della sintassi di iterazione [Handlebars](#syntax).
* Nome variabile non corretto: assicurati che il nome della variabile sia utilizzato in modo coerente in tutto il blocco. Consulta [Best practice](#best-practices) per le convenzioni di denominazione.
* Separatori di percorso non corretti: utilizzare punti (`.`) non barre o altri caratteri

### Verifica delle iterazioni

Utilizza [modalità test percorso](../building-journeys/testing-the-journey.md) per verificare le iterazioni. Ciò è particolarmente importante quando si utilizzano [azioni personalizzate](#custom-action-responses) o [ricerche set di dati](#dataset-lookup):

1. Avvia il percorso in [modalità di test](../building-journeys/testing-the-journey.md)
2. Attiva l&#39;evento o l&#39;azione personalizzata con i dati di esempio
3. Controlla l&#39;[anteprima del messaggio](../content-management/preview.md) per verificare che l&#39;iterazione venga visualizzata correttamente
4. Esaminare i registri della modalità di test per individuare eventuali errori (vedere [Registri della modalità di test delle azioni personalizzati](../action/action-response.md#test-mode-logs))

## Argomenti correlati {#related-topics}

**Nozioni di base di Personalization:**

* [Introduzione alla personalizzazione](personalize.md)
* [Aggiungere personalizzazione](personalization-build-expressions.md)
* [Sintassi di personalizzazione](personalization-syntax.md)
* [Funzioni Helper](functions/helpers.md)
* [Creare regole condizionali](create-conditions.md)

**Configurazione Percorso:**

* [Informazioni sugli eventi](../event/about-events.md)
* [Utilizzare le azioni personalizzate](../action/about-custom-action-configuration.md)
* [Trasmettere le raccolte nei parametri delle azioni personalizzate](../building-journeys/collections.md#passing-collection)
* [Utilizzare le risposte alle chiamate API nelle azioni personalizzate](../action/action-response.md)
* [Risolvere i problemi relativi alle azioni personalizzate](../action/troubleshoot-custom-action.md)
* [Utilizzare i dati di Adobe Experience Platform nei percorsi](../building-journeys/dataset-lookup.md)
* [Utilizzare identificatori supplementari nei percorsi](../building-journeys/supplemental-identifier.md)
* [Guardrail e limitazioni](../start/guardrails.md)
* [Testare il percorso](../building-journeys/testing-the-journey.md)

**Funzioni espressione Percorso:**

* [Editor di espressioni avanzate](../building-journeys/expression/expressionadvanced.md)
* [Funzioni di gestione della raccolta](../building-journeys/expression/collection-management-functions.md) (prima, tutte, ultima)
* [Funzioni elenco](../building-journeys/functions/list-functions.md) (serializeList, filter, sort)
* [Funzioni array](../personalization/functions/arrays-list.md) (head, tail)

**Casi di utilizzo di Personalization:**

* [E-mail di abbandono carrello](personalization-use-case-helper-functions.md)
* [Notifica dello stato dell’ordine](personalization-use-case.md)

**Progettazione messaggi:**

* [Introduzione alla progettazione delle e-mail](../email/get-started-email-design.md)
* [Creare notifiche push](../push/create-push.md)
* [Creare messaggi SMS](../sms/create-sms.md)
* [Anteprima e test del contenuto](../content-management/preview-test.md)

