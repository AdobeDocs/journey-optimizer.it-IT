---
title: Raccolte di voci di elenco
description: Le raccolte ti consentono di categorizzare e raggruppare gli elementi decisionali in base alle tue preferenze.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: cc9f0d7a-6166-4736-8cb7-1989816708ad
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 11%

---

# Raccolte di voci di elenco {#list-decision-items}

Le raccolte, note anche come raccolte di elementi, ti consentono di categorizzare e raggruppare gli elementi decisionali in base alle tue preferenze. Queste categorie vengono create creando regole che sfruttano gli attributi degli elementi decisionali.

Per visualizzare un elenco di tutte le raccolte di elementi, esegui una singola richiesta GET all’API Libreria di offerte.

**Formato API**

```http
GET /{ENDPOINT_PATH}/item-collections?{QUERY_PARAMS}
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
| `property` | Un filtro proprietà facoltativo: <ul><li>Le proprietà sono raggruppate per operazione AND.</li><li>I parametri possono essere ripetuti come segue: proprietà={PROPERTY_EXPR}[&amp;proprietà={PROPERTY_EXPR2}...] o proprietà={PROPERTY_EXPR1}[,{PROPERTY_EXPR2}...]</li><li>Le espressioni di proprietà sono in formato `[ !]field[op]value`, con `op` in `[==,!=,<=,>=,<,>,~]`, che supportano espressioni regolari.</li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | Ordinare i risultati per una proprietà specifica. Se si aggiunge un segno - prima del nome (orderby=-name), gli elementi verranno ordinati in base al nome in ordine decrescente (Z-A). Le espressioni di percorso sono sotto forma di percorsi separati da punti. Questo parametro può essere ripetuto come segue: `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | Limita il numero di entità restituite. | `limit=5` |

**Richiesta**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/item-collections?limit=2' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Risposta**

In caso di esito positivo, la risposta restituisce un elenco di raccolte di elementi a cui hai accesso.

```json
{
    "results": [
        {
            "created": "2024-01-31T18:28:52.888Z",
            "modified": "2024-06-28T19:44:13.112Z",
            "etag": 7,
            "schemas": [
                "https://ns.adobe.com/experience/decisioning/item-collection;version=1.2"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "itemCollection1234",
            "name": "Item collection One",
            "description": "Item collection",
            "constraints": [
                {
                    "itemCatalogId": "itemCatalog1234",
                    "uiModel": "{\"operator\":\"equals\",\"value\":{\"left\":\"_experience.decisioning.decisionitem.itemName\",\"right\":\"Some offer item\"}}"
                }
            ],
            "tags": []
        },
        {
            "created": "2024-06-10T16:02:57.878Z",
            "modified": "2024-06-10T16:02:57.878Z",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/decisioning/item-collection;version=1.2"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "itemCollection5678",
            "name": "Item collection One",
            "description": "Item collection",
            "constraints": [
                {
                    "itemCatalogId": "itemCatalog1234",
                    "uiModel": "{\"operator\":\"greater than\",\"value\":{\"left\":\"_<imsOrg>.some_integer\",\"right\":100}}"
                }
            ],
            "tags": []
        }
    ],
    "count": 2,
    "total": 166,
    "_links": {
        "self": {
            "href": "/item-collections?orderby=-modified&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/item-collections?orderby=-modified&limit=2&start=2024-06-04T23:37:33.980Z",
            "type": "application/json"
        }
    }
}
```
