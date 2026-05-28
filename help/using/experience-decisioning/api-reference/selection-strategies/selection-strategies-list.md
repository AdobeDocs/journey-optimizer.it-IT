---
title: Elencare strategie di selezione
description: Le strategie di selezione sono costituite da raccolte associate a vincoli e metodi di classificazione per determinare le offerte.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: be0f683d-1d39-47f6-b565-1cc7ee06ee71
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/u90FzwxAaE8VS3wt0ArcZq0ibha1-1Rn0btxbRfniyA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 219
ht-degree: 10%

---

# Elencare strategie di selezione {#list-selection-strategies}

Una strategia di selezione è costituita da una raccolta associata a un vincolo di idoneità e a un metodo di classificazione per determinare le offerte da mostrare quando vengono selezionate in un [criterio di decisione](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/decisioning/experience-decisioning/create-decision).

Per visualizzare un elenco di tutte le strategie di selezione, esegui una singola richiesta GET all’API della Libreria di offerte.

**Formato API**

```http
GET /{ENDPOINT_PATH}/selection-strategies?{QUERY_PARAMS}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API di persistenza. | `https://platform.adobe.io/data/core/dps` |
| `{QUERY_PARAMS}` | Parametri di query facoltativi in base ai quali filtrare i risultati. | `limit=2` |

## Utilizzo dei parametri di query {#using-query-parameters}

Puoi utilizzare i parametri di query per visualizzare e filtrare i risultati quando elenchi le risorse.

### Paging {#paging}

I parametri di query più comuni per il paging includono:

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `property` | Un filtro proprietà facoltativo: <ul><li>Le proprietà sono raggruppate per operazione AND.</li><li>I parametri possono essere ripetuti come segue: proprietà={PROPERTY_EXPR}[&amp;proprietà={PROPERTY_EXPR2}...] o proprietà={PROPERTY_EXPR1}[,{PROPERTY_EXPR2}...]</li><li>Le espressioni di proprietà sono in formato `[!]field[op]value`, con `op` in `[==,!=,<=,>=,<,>,~]`, che supportano espressioni regolari.</li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | Ordinare i risultati per una proprietà specifica. Se si aggiunge un segno - prima del nome (orderby=-name), gli elementi verranno ordinati in base al nome in ordine decrescente (Z-A). Le espressioni di percorso sono sotto forma di percorsi separati da punti. Questo parametro può essere ripetuto come segue: `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | Limita il numero di entità restituite. | `limit=5` |

**Richiesta**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/selection-strategies?limit=2' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Risposta**

In caso di esito positivo, la risposta restituisce un elenco di strategie di selezione a cui hai accesso.

```json
{
    "results": [
        {
            "created": "2024-02-08T03:01:50.924Z",
            "modified": "2024-02-16T23:03:03.019Z",
            "etag": 4,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/selection-strategy;version=0.2"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "selectionStrategy1234",
            "name": "Selection Strategy One",
            "description": "Selection Strategy",
            "rank": {
                "priority": 1,
                "order": {
                    "orderEvaluationType": "static"
                }
            },
            "profileConstraint": {
                "profileConstraintType": "eligibilityRule",
                "eligibilityRule": "offerRule1234"
            },
            "optionSelection": {
                "filter": "itemCollection1234",
            }
        },
        {
            "created": "2024-01-11T11:12:06.775Z",
            "modified": "2024-01-15T14:36:02.994Z",
            "etag": 2,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/selection-strategy;version=0.1"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "selectionStrategy5678",
            "name": "Selection Strategy Two",
            "rank": {
                "priority": 1,
                "order": {
                    "orderEvaluationType": "scoringFunction",
                    "function": "rankingFormula5678"
                }
            },
            "profileConstraint": {
                "profileConstraintType": "none"
            "optionSelection": {
                "filter": "itemCollection5678"
            }
        }
    ],
    "count": 2,
    "total": 166,
    "_links": {
        "self": {
            "href": "/selection-strategies?orderby=-modified&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/selection-strategies?orderby=-modified&limit=2&start=2024-06-04T23:37:33.980Z",
            "type": "application/json"
        }
    }
}
```
