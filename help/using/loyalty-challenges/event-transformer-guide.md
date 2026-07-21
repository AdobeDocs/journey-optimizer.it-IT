---
solution: Journey Optimizer
product: journey optimizer
title: Guida di Event Transformer
description: Scopri come configurare le impostazioni dello schema e del trasformatore per le definizioni degli eventi Sfide di fedeltà in Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="Beta privata" type="Informative"
mini-toc-levels: 1
exl-id: d3ad85f0-7f7e-40ab-b8c4-fc0c1234be87
feature_v2: []
subfeature_v2: []
source-git-commit: 80abca7068e021e52e9c34d9a2fb629ebad70302
workflow-type: tm+mt
source-wordcount: 1731
ht-degree: 1%

---

# Guida di Event Transformer {#event-transformer-guide}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_event_transformer"
>title="Guida di Event Transformer"
>abstract="Utilizza questa guida per configurare le espressioni di convalida dello schema e di trasformazione per le definizioni degli eventi Sfide di fedeltà."

>[!BEGINSHADEBOX]

**Sommario**

[Introduzione alle sfide di fedeltà](get-started.md)

<table style="table-layout:fixed">
<tr style="border: 0;">
<td style="vertical-align:top;">

**Crea e gestisci le sfide**

* [Accesso e gestione di sfide e attività](access-loyalty-challenges.md)
* [Creare le sfide](create-challenges.md)
* [Creare le attività](create-tasks.md)
* [Monitorare le prestazioni della sfida fedeltà](loyalty-reporting.md)

</td>
<td style="vertical-align:top;">

**Configura e integra**

* [Configurare le sfide relative alla fedeltà](loyalty-admin.md)
* [Guida alla definizione del premio](reward-definition-guide.md)
* **Guida di Event Transformer** ◀︎ **Sei qui**
* [Dati e set di dati sulla fedeltà](loyalty-data-and-datasets.md)
* [Riferimento API per le sfide di fedeltà](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

</td>
</tr>
</table>

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Questa funzionalità è attualmente in **versione beta privata**. Per informazioni dettagliate sul ciclo di rilascio e sulle fasi di disponibilità in [!DNL Journey Optimizer], vedere [ciclo di rilascio](../rn/releases.md).

Prima di poter applicare una transazione cliente a una sfida fedeltà, è necessario che il formato **Adobe Loyalty Event** comprenda il servizio di verifica. Gli eventi dei clienti, provenienti da un sistema POS, un’app mobile, una piattaforma di e-commerce o qualsiasi altra origine, in genere utilizzano lo schema dati del cliente. **I trasformatori di eventi** colmano questo gap senza richiedere alcuna modifica al sistema a monte.

## Panoramica

Una **Definizione evento** indica alla piattaforma due cose:

* **Quali eventi rivendicare** — come riconoscere che un evento in ingresso appartiene a questa definizione (corrispondenza)
* **Come modificarne la forma** — un&#39;espressione [JSONata](https://docs.jsonata.org/overview) che mappa i campi del cliente nel formato dell&#39;evento fedeltà (trasformazione)

È possibile configurare più definizioni di evento per organizzazione. La piattaforma li valuta in ordine e applica il primo corrispondente. Gli eventi che non corrispondono ad alcuna definizione passano all&#39;acquisizione nativa (vedi [Fallback — Native Loyalty Events](#fallback--native-loyalty-events)).

## Formato dell’evento fedeltà di Adobe

Ogni definizione di evento deve produrre un oggetto JSON nel formato seguente. Questo è l’input elaborato dal servizio di verifica.

```json
{
  "_id":              "string — optional; used for duplicate detection if enabled",
  "event_name":       "string — used for internal metrics and reporting only (e.g. 'purchase', 'visit')",
  "timestamp":        "ISO 8601 date-time string — when the event occurred",
  "utc_offset":       "string — UTC offset of the store or device (e.g. '-07:00'); required for daypart matching",
  "location_id":      "string — optional; store or location identifier",
  "transaction_id":   "string — optional; dedup key for the transaction",
  "loyalty_identity": {
    "id": "string — the member's loyalty ID"
  },
  "item_list": [
    {
      "item_set":   ["string", "..."],  // one or more identifiers — SKU, category, event code, etc.
      "item_name":  "string — optional human-readable label",
      "quantity":   1,                  // integer; how many units
      "unit_price": 4.99,               // float; price per unit
      "sub_total":  4.99                // float; line total (quantity × unit_price)
    }
  ]
}
```

### Note campo

| Campo | Obbligatorio | Note |
|--------------------------------|--------------------|-------|
| `loyalty_identity` | **Sì** | Deve contenere `id`, l&#39;ID fedeltà del membro. |
| `item_list` | **Sì** | Deve contenere ≥1 elemento; l&#39;elenco_elementi vuoto viene rifiutato. |
| `item_set` | **Sì** (per elemento) | Gli elenchi di inclusione/esclusione delle attività degli identificatori corrispondono a. |
| `timestamp` | **Sì** | Utilizzato per la valutazione dell’intervallo di date. Deve essere ISO 8601. |
| `utc_offset` | Consigliato | Necessario per la corrispondenza delle parti diurne e il conteggio delle giornate di striscia. |
| `_id` | No | Utilizzato per la deduplicazione se per l’organizzazione è abilitato il rilevamento dei duplicati. |
| `sub_total` | No | Le attività con soglia di spesa utilizzano questo valore; omettere significa zero spesa. |

## Campi definizione evento

| Campo | Tipo | Obbligatorio | Descrizione |
|--------------------------------|------------------|----------------------|-------------|
| `guid` | Stringa | No (assegnato dal sistema) | ID univoco assegnato dal sistema; sola lettura. |
| `name` | Stringa | **Sì** | Etichetta leggibile, ad esempio `"Starbucks POS Purchase"`. |
| `xdmSchemaId` | Stringa | **Sì** | Corrisponde agli eventi in base all’ID dello schema XDM (consulta Funzionamento della corrispondenza). |
| `schema` | Stringa | No | [Schema JSON](https://json-schema.org/) (come stringa) per convalidare gli eventi in arrivo. |
| `transformer` | Stringa | **Sì** | Espressione JSONata che mappa l’evento nel formato Fedeltà. |

## Come funziona la corrispondenza

Gli eventi in arrivo tramite il servizio core di raccolta dati (DCCS, Data Collection Core Service) contengono un riferimento allo schema XDM nella busta. La piattaforma legge l&#39;ID schema da `/body/xdmMeta/schemaRef/id` e lo confronta con il `xdmSchemaId` di ogni definizione.

La piattaforma esamina le definizioni degli eventi dell&#39;organizzazione **in ordine** e applica la prima corrispondenza. Una volta trovata una corrispondenza, il corpo `xdmEntity` viene passato al trasformatore.

## Scrittura del trasformatore

Il campo `transformer` è un&#39;espressione [JSONata](https://docs.jsonata.org/overview). Riceve l’evento in ingresso JSON come input e deve restituire un oggetto Adobe Loyalty Event valido.

+++Pattern di mappatura di base

Mappa ogni campo di primo livello del formato di destinazione al percorso corrispondente nell’evento sorgente:

```jsonata
{
  "_id":            sourceEvent._id,
  "event_name":     sourceEvent.eventType,
  "timestamp":      sourceEvent.timestamp,
  "utc_offset":     sourceEvent.storeInfo.utcOffset,
  "location_id":    sourceEvent.storeInfo.storeId,
  "transaction_id": sourceEvent.transaction.id,
  "loyalty_identity": {
    "id": sourceEvent.member.loyaltyId
  },
  "item_list": sourceEvent.transaction.items.{
    "item_set":   [itemSku, itemCategory],
    "item_name":  itemDescription,
    "quantity":   quantity,
    "unit_price": unitPrice,
    "sub_total":  lineTotal
  }
}
```

+++

+++Codifica fissa del nome dell’evento

Se tutti gli eventi che corrispondono a questa definizione rappresentano la stessa attività logica, utilizzare il codice hardware `event_name`:

```jsonata
{
  "event_name": "in-store-purchase",
  ...
}
```

`event_name` viene utilizzato per le metriche interne e il reporting. Non viene utilizzato come filtro attività. La qualifica dell&#39;attività è determinata dal contenuto `item_set`, non dal nome dell&#39;evento.

+++

+++Mappatura dell’identità per eventi DCCS/XDM

Per gli eventi in arrivo tramite la route DCCS, l&#39;identità del membro viene in genere inclusa nel campo XDM `identityMap` standard anziché in una proprietà tenant personalizzata. `identityMap` è una mappa basata sullo spazio dei nomi. La chiave stessa è il nome dello spazio dei nomi e il valore è una matrice di oggetti identità.

```jsonata
"loyalty_identity": {
  "id": identityMap.Email[0].id
}
```

* **Sostituzione dello spazio dei nomi:** Sostituisci `Email` con qualsiasi spazio dei nomi utilizzato dall&#39;organizzazione per i membri fedeltà: `Loyalty`, `ECID`, `CRMID`, ecc. Leggi sempre dallo spazio dei nomi che contiene l’identità del profilo fedeltà principale.

* **Usa sempre `[0]`:** `identityMap.Email` è un array. Senza l&#39;indice, JSONata restituisce una sequenza anziché un singolo valore se sono presenti più identità e `loyalty_identity.id` diventa un elenco. Aggiungerlo al primo elemento con `[0]`.

* **Evitare i campi tenant personalizzati per l&#39;identità:** I gruppi di campi personalizzati a volte espongono un campo di aspetto e-mail (ad esempio `_yourtenant.identification.core.email`). Nei dati di esempio questo restituisce un valore e sembra corretto, ma negli eventi di produzione è spesso vuoto. L&#39;origine affidabile dell&#39;identità è sempre `identityMap`.

+++

+++Generazione di `item_set`

`item_set` è una matrice di identificatori di stringa. Includi tutti i campi in base ai quali le attività di verifica potrebbero filtrare:

```jsonata
"item_set": [itemSku, productCategory, departmentCode]
```

Per gli eventi non transazionali (check-in, completamento di un sondaggio, trigger personalizzato) è sufficiente un singolo identificatore:

```jsonata
"item_set": [eventName]
```

+++

+++Mappatura di `unit_price`

`unit_price` deve essere un prezzo unitario. Alcuni schemi di origine memorizzano invece un totale riga (prezzo × quantità). Se il campo di origine è un totale riga, dividere per quantità per ottenere il prezzo unitario:

```jsonata
"unit_price": priceTotal / quantity
```

> Dividi solo se il campo di origine è un totale riga. Se memorizza già un prezzo per unità, eseguirne la mappatura diretta. Se si divide un prezzo per unità per quantità, si otterrà automaticamente un valore errato.

+++

+++Derivazione di `transaction_id`

Se l’evento di origine non include un identificatore di transazione, puoi derivarne uno stabile dalla marca temporale:

```jsonata
"transaction_id": "txn_" & $string($toMillis(timestamp))
```

Questo converte la marca temporale ISO in millisecondi epoca e produce un valore deterministico per un dato evento. Utilizza la funzione di generazione ID della tua piattaforma, se disponibile.

+++

+++Utilizzo delle funzioni JSONata

È disponibile la libreria completa delle funzioni JSONata. Esempi utili:

```jsonata
/* String concatenation */
"item_set": [skuId & ':' & categoryId]

/* Number formatting */
"item_set": ["spend:" & $formatNumber(totalAmount, '0.00')]

/* Conditional field */
"event_name": eventType ? eventType : "unknown"

/* Array transformation */
"item_list": items.{ "item_set": [sku], "quantity": qty, "sub_total": price * qty }
```

+++

## Esempi

+++Esempio 1 — Evento personalizzato semplice (non transazionale)

**Scenario:** un&#39;app mobile invia un evento di archiviazione. Non ci sono elementi di riga — l&#39;evento stesso è l&#39;attività qualificata.

**Evento in ingresso:**

```json
{
  "_id":       "evt-001",
  "eventName": "store-checkin",
  "timestamp": "2025-10-15T14:22:00Z",
  "storeId":   "STORE-042",
  "member": {
    "loyaltyId": "LM-8827361"
  }
}
```

**Definizione evento:**

```json
{
  "name":        "Mobile Store Check-In",
  "xdmSchemaId": "https://ns.adobe.com/yourtenant/schemas/store-checkin-v1",
  "transformer": "{\"_id\": _id, \"event_name\": eventName, \"timestamp\": timestamp, \"location_id\": storeId, \"loyalty_identity\": {\"id\": member.loyaltyId}, \"item_list\": [{\"item_set\": [eventName], \"quantity\": 1}]}"
}
```

**Trasformatore formattato (per la leggibilità):**

```jsonata
{
  "_id":        _id,
  "event_name": eventName,
  "timestamp":  timestamp,
  "location_id": storeId,
  "loyalty_identity": {
    "id": member.loyaltyId
  },
  "item_list": [
    {
      "item_set": [eventName],
      "quantity": 1
    }
  ]
}
```

**Evento Adobe Loyalty Di Output:**

```json
{
  "_id":        "evt-001",
  "event_name": "store-checkin",
  "timestamp":  "2025-10-15T14:22:00Z",
  "location_id": "STORE-042",
  "loyalty_identity": { "id": "LM-8827361" },
  "item_list": [{ "item_set": ["store-checkin"], "quantity": 1 }]
}
```

Un&#39;attività di verifica senza restrizioni di inclusione/esclusione conterà questo evento come visita qualificata. La singola `item_set` voce `["store-checkin"]` corrisponde a qualsiasi attività che consente tutti gli elementi.

+++

+++Esempio 2 — Acquisto POS con elementi riga

**Scenario:** un sistema POS invia un payload di transazione. Ogni voce ha uno SKU e appartiene a una categoria. Le attività di verifica utilizzano SKU e categoria per determinare ciò che è idoneo.

**Evento in ingresso:**

```json
{
  "_id":       "txn-20251015-4492",
  "timestamp": "2025-10-15T14:35:00Z",
  "storeInfo": {
    "storeId":   "STORE-042",
    "utcOffset": "-07:00"
  },
  "transaction": {
    "transactionId": "4492",
    "items": [
      { "sku": "COFFEE-001", "category": "BEVERAGE", "qty": 2, "unitPrice": 4.50, "lineTotal": 9.00 },
      { "sku": "MUFFIN-007", "category": "FOOD",     "qty": 1, "unitPrice": 3.25, "lineTotal": 3.25 }
    ]
  },
  "member": {
    "loyaltyId": "LM-8827361"
  }
}
```

**Definizione evento:**

```json
{
  "name":        "Retail POS Purchase",
  "xdmSchemaId": "https://ns.adobe.com/yourtenant/schemas/retail-pos-purchase-v1",
  "transformer": "{\"_id\": _id, \"event_name\": \"purchase\", \"timestamp\": timestamp, \"utc_offset\": storeInfo.utcOffset, \"location_id\": storeInfo.storeId, \"transaction_id\": transaction.transactionId, \"loyalty_identity\": {\"id\": member.loyaltyId}, \"item_list\": transaction.items.{\"item_set\": [sku, category], \"quantity\": qty, \"unit_price\": unitPrice, \"sub_total\": lineTotal}}"
}
```

**Trasformatore formattato:**

```jsonata
{
  "_id":            _id,
  "event_name":     "purchase",
  "timestamp":      timestamp,
  "utc_offset":     storeInfo.utcOffset,
  "location_id":    storeInfo.storeId,
  "transaction_id": transaction.transactionId,
  "loyalty_identity": {
    "id": member.loyaltyId
  },
  "item_list": transaction.items.{
    "item_set":   [sku, category],
    "quantity":   qty,
    "unit_price": unitPrice,
    "sub_total":  lineTotal
  }
}
```

**Evento Adobe Loyalty Di Output:**

```json
{
  "_id":            "txn-20251015-4492",
  "event_name":     "purchase",
  "timestamp":      "2025-10-15T14:35:00Z",
  "utc_offset":     "-07:00",
  "location_id":    "STORE-042",
  "transaction_id": "4492",
  "loyalty_identity": { "id": "LM-8827361" },
  "item_list": [
    { "item_set": ["COFFEE-001", "BEVERAGE"], "quantity": 2, "unit_price": 4.50, "sub_total": 9.00 },
    { "item_set": ["MUFFIN-007", "FOOD"],     "quantity": 1, "unit_price": 3.25, "sub_total": 3.25 }
  ]
}
```

Un&#39;attività di verifica con `include: ["BEVERAGE"]` potrebbe rendere idoneo l&#39;elemento della riga di caffè (il relativo `item_set` contiene `"BEVERAGE"`) e accumulare 9,00 $ di spesa per tale attività. La riga muffin verrebbe esclusa.

+++

+++Esempio 3 — AEP Experience Event (corrispondenza schema XDM)

**Scenario:** gli eventi passano attraverso Adobe Journey Optimizer. L’evento in arrivo è un Experience Event XDM con un ID schema noto. La piattaforma utilizza l’ID dello schema per la corrispondenza anziché un controllo percorso/valore.

**Corpo entità XDM in ingresso** (il `xdmEntity` estratto dall&#39;evento AJO):

```json
{
  "_brandname": {
    "identities": {
      "loyaltyId": "LM-8827361"
    },
    "transactions": {
      "transactionId": "TXN-9901",
      "storeNumber":   "042",
      "utcOffset":     "-07:00",
      "lineItems": [
        { "skuNumber": "11143053", "priceAmount": 345, "qty": 1, "category": "BEVERAGE" },
        { "skuNumber": "11161387", "priceAmount": 495, "qty": 1, "category": "FOOD" }
      ],
      "totalAmount": 840
    }
  },
  "_id":       "87c0cccf-5809-38e0-a703-3994e80173ab",
  "timestamp": "2025-07-04T16:03:32.000Z"
}
```

**Definizione evento:**

```json
{
  "name":        "AJO Brand Purchase",
  "xdmSchemaId": "https://ns.adobe.com/brandname/schemas/purchase-event-v1",
  "transformer":  "{\"_id\": _id, \"event_name\": \"purchase\", \"timestamp\": timestamp, \"utc_offset\": _brandname.transactions.utcOffset, \"location_id\": _brandname.transactions.storeNumber, \"transaction_id\": _brandname.transactions.transactionId, \"loyalty_identity\": {\"id\": _brandname.identities.loyaltyId}, \"item_list\": _brandname.transactions.lineItems.{\"item_set\": [skuNumber, category], \"quantity\": qty, \"unit_price\": priceAmount, \"sub_total\": priceAmount * qty}}"
}
```

**Trasformatore formattato:**

```jsonata
{
  "_id":            _id,
  "event_name":     "purchase",
  "timestamp":      timestamp,
  "utc_offset":     _brandname.transactions.utcOffset,
  "location_id":    _brandname.transactions.storeNumber,
  "transaction_id": _brandname.transactions.transactionId,
  "loyalty_identity": {
    "id": _brandname.identities.loyaltyId
  },
  "item_list": _brandname.transactions.lineItems.{
    "item_set":   [skuNumber, category],
    "quantity":   qty,
    "unit_price": priceAmount,
    "sub_total":  priceAmount * qty
  }
}
```

> **Nota:** quando un evento corrisponde per ID schema XDM, il trasformatore riceve solo la porzione `xdmEntity` dell&#39;evento, non la busta esterna di AJO. Tutti i percorsi nell’espressione del trasformatore sono relativi al corpo dell’entità XDM.

+++

## Aggiunta della convalida dello schema JSON (facoltativo)

Se si desidera che la piattaforma convalidi la struttura degli eventi in arrivo prima di tentare la trasformazione, impostare il campo `schema` su un documento [Schema JSON](https://json-schema.org/draft-04) codificato come stringa JSON.

Gli eventi che non superano la convalida dello schema vengono rifiutati prima dell’esecuzione della trasformazione. La risposta all’errore include un errore di convalida specifico che semplifica la diagnosi di eventi a monte con formato non corretto.

+++Schema di esempio (per esempio 2 sopra)

```json
{
  "$schema": "http://json-schema.org/draft-04/schema#",
  "type": "object",
  "required": ["_id", "timestamp", "transaction", "member"],
  "properties": {
    "_id":       { "type": "string" },
    "timestamp": { "type": "string", "format": "date-time" },
    "member": {
      "type": "object",
      "required": ["loyaltyId"],
      "properties": {
        "loyaltyId": { "type": "string" }
      }
    },
    "transaction": {
      "type": "object",
      "required": ["items"],
      "properties": {
        "transactionId": { "type": "string" },
        "items": {
          "type": "array",
          "items": {
            "type": "object",
            "required": ["sku", "qty", "lineTotal"],
            "properties": {
              "sku":       { "type": "string" },
              "category":  { "type": "string" },
              "qty":       { "type": "number" },
              "unitPrice": { "type": "number" },
              "lineTotal": { "type": "number" }
            }
          }
        }
      }
    }
  }
}
```

+++

Passa questo schema come stringa JSON minimizzata nel campo `schema` della definizione dell&#39;evento.

## Fallback: eventi fedeltà nativi

Se nessuna definizione di evento corrisponde a un evento in arrivo, la piattaforma tenta di acquisirlo direttamente come evento fedeltà nativo di Adobe. Se il payload è già conforme al formato dell’evento fedeltà descritto in precedenza, non è necessario alcun trasformatore e l’evento viene applicato così com’è. Questo consente ai clienti che hanno preformattato i loro eventi di ignorare completamente la trasformazione.

## Riferimento API

Tutte le operazioni di definizione degli eventi utilizzano il percorso di base `/loyalty/metadata/config/events`.

+++Creare una definizione di evento

```http
POST /loyalty/metadata/config/events
x-gw-ims-org-id: {ORG_ID}
x-sandbox-name: {SANDBOX}
Content-Type: application/json

{
  "name":        "Retail POS Purchase",
  "xdmSchemaId": "https://ns.adobe.com/yourtenant/schemas/retail-pos-purchase-v1",
  "transformer": "{ ... }"
}
```

+++

+++Elenca definizioni eventi

```http
GET /loyalty/metadata/config/events
x-gw-ims-org-id: {ORG_ID}
x-sandbox-name: {SANDBOX}
```

+++

+++Aggiornare una definizione di evento

```http
PUT /loyalty/metadata/config/events/{eventId}
x-gw-ims-org-id: {ORG_ID}
x-sandbox-name: {SANDBOX}
Content-Type: application/json

{
  "name":        "Retail POS Purchase (v2)",
  "transformer": "{ ... updated expression ... }"
}
```

+++

+++Eliminare una definizione di evento

```http
DELETE /loyalty/metadata/config/events/{eventId}
x-gw-ims-org-id: {ORG_ID}
x-sandbox-name: {SANDBOX}
```

+++

## Convalida del trasformatore

Le espressioni JSONata vengono convalidate per la sintassi al momento del salvataggio della definizione dell’evento. Se l&#39;espressione non è valida, l&#39;API restituisce un errore `422` con una descrizione dell&#39;errore di analisi.

Per eseguire il test di un trasformatore prima della distribuzione, utilizzare l&#39;[JSONata Exerciser](https://try.jsonata.org/) — incollare l&#39;evento di origine come input e l&#39;espressione del trasformatore per verificare che l&#39;output corrisponda al formato dell&#39;evento fedeltà previsto.

## Insidie comuni

Questi errori vengono tutti eseguiti senza errori su un semplice payload di test a elemento singolo, che è esattamente il motivo per cui non vengono rilevati. Prima dell’implementazione, verifica sempre il trasformatore rispetto a un payload con due o più prodotti.

+++Creazione di un oggetto invece della mappatura sull’array

L&#39;errore più frequente. Se si utilizza un valore letterale di oggetto singolo con `productListItems.SKU`, ogni SKU e ogni quantità viene estratta in sequenze di dati raggruppati anziché produrre un elemento riga per prodotto.

**✗comprime tutti gli elementi in uno:**

```jsonata
"item_list": [
  {
    "item_set": [ productListItems.SKU ],
    "quantity": productListItems.quantity
  }
]
```

Con due prodotti, `item_set` contiene entrambi gli SKU e `quantity` diventa un array come `[1, 4]`.

**✓Un elemento riga per prodotto:**

```jsonata
"item_list": [
  productListItems.{
    "item_set": [SKU],
    "quantity": quantity
  }
]
```

La mappa `.{ }` viene eseguita una volta per prodotto, in modo che ogni voce diventi la propria.

+++

+++Dimenticanza dell’indice dell’array sull’identità

`identityMap.Email` è un array. Senza `[0]`, se un profilo contiene più di un&#39;identità nello spazio dei nomi, `id` diventa un elenco di valori invece di una singola stringa.

**✗** `identityMap.Email.id`

**✓** `identityMap.Email[0].id`

+++

+++Identità di origine da un campo tenant personalizzato

I gruppi di campi personalizzati a volte espongono un campo di aspetto e-mail come `_yourtenant.identification.core.email`. Nei dati di esempio restituisce un valore e sembra corretto, ma negli eventi di produzione è spesso vuoto, causando la visualizzazione di `loyalty_identity.id` null. Utilizza sempre `identityMap` come origine dell&#39;identità.

+++

+++Un array nidificato perde in `item_set`

L&#39;aggiunta di un campo categoria a `item_set` è semplice, ma se `productCategories` è di per sé un array, il risultato si espande in modo imprevedibile.

**✗Può produrre più voci del previsto:**

```jsonata
"item_set": [SKU, productCategories.categoryID]
```

Un prodotto con tre categorie produce un `item_set` con quattro valori.

**✓Indicizzare la matrice nidificata per ottenere esattamente un valore:**

```jsonata
"item_set": [SKU, productCategories[0].categoryID]
```

+++

+++`item_list` è vuoto o mancante

Un evento con `item_list` vuoto o assente è stato rifiutato in quanto non valido. Per gli eventi non transazionali (check-in, trigger personalizzati) non ci sono elementi di riga naturali, quindi creane uno sintetico:

```jsonata
"item_list": [{ "item_set": [eventName], "quantity": 1 }]
```

+++

+++`timestamp` come numero intero dell&#39;epoca Unix invece di ISO 8601

La piattaforma richiede una stringa ISO 8601. Se l’evento sorgente è rimasto in millisecondi dall’epoca, convertiscilo:

```jsonata
"timestamp": $fromMillis(timestamp)
```

+++

+++`utc_offset` omesso

Senza `utc_offset`, verranno ignorati sia la corrispondenza della finestra di Fasce orarie che il conteggio delle sequenze di giorni consecutivi. Mappa l’offset UTC dello store o del dispositivo dall’evento di origine ovunque sia disponibile.

+++

+++Percorsi del trasformatore relativi all’envelope di AJO in un evento DCCS

Per gli eventi DCCS, il trasformatore riceve solo il corpo `xdmEntity`, non l&#39;envelope esterno di AJO. Tutti i percorsi devono essere relativi alla radice dell’entità XDM. Se l&#39;espressione fa riferimento a campi che si trovano nella busta esterna (ad esempio `/body/xdmMeta/...`), non verranno trovati e produrranno automaticamente null.

+++
