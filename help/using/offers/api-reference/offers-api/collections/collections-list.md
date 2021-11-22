---
title: Elencare raccolte
description: Le raccolte sono sottoinsiemi di offerte in base a condizioni predefinite definite da un addetto al marketing, ad esempio la categoria dell’offerta.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: f27ffbe0-a61a-428a-bc37-db6b56e38a83
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 5%

---

# Elencare raccolte

Le raccolte sono sottoinsiemi di offerte in base a condizioni predefinite definite da un addetto al marketing, ad esempio la categoria dell’offerta.

Puoi visualizzare un elenco di tutte le raccolte all’interno di un contenitore effettuando una singola richiesta di GET al [!DNL Offer Library] API.

**Formato API**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_FILTER}&{QUERY_PARAMS}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API dell&#39;archivio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Il contenitore in cui si trovano le raccolte. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_FILTER}` | Definisce lo schema associato alle raccolte. | `https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1` |
| `{QUERY_PARAMS}` | Parametri di query opzionali per filtrare i risultati in base a. | `limit=1` |

**Richiesta**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1&limit=2' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

## Utilizzo dei parametri di query

Puoi utilizzare i parametri di query per sfogliare le pagine e filtrare i risultati durante l’elenco delle risorse.

### Paging

I parametri di query più comuni per il paging includono:

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `q` | Una stringa di query facoltativa da cercare nei campi selezionati. La stringa di query deve essere in minuscolo e può essere circondata da virgolette doppie per evitare che venga token ed evitare caratteri speciali. I caratteri `+ - = && || > < ! ( ) { } [ ] ^ \" ~ * ? : \ /` hanno un significato speciale e devono essere preceduti da una barra inversa quando vengono visualizzati nella stringa di interrogazione. | `demo collection` |
| `qop` | Applica l’operatore AND o OR ai valori nel parametro della stringa di query q. | `AND` / `OR` |
| `field` | Elenco facoltativo di campi a cui limitare la ricerca. Questo parametro può essere ripetuto così: field=field1[,field=field2,...] e (le espressioni del percorso sono sotto forma di percorsi separati da punti come _instance.xdm:name) | `_instance.xdm:name` |
| `orderBy` | Ordinare i risultati per una proprietà specifica. Aggiunta di un `-` prima del titolo (`orderby=-title`) ordina gli elementi in base al titolo in ordine decrescente (Z-A). | `-repo:createdDate` |
| `limit` | Limita il numero di raccolte restituite. | `limit=5` |

**Risposta**

Una risposta corretta restituisce un elenco di raccolte presenti all’interno del contenitore a cui hai accesso.

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1",
    "requestTime": "2020-10-21T21:14:19.282175Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "27c92e00-127d-11eb-b9fe-5bcfb5d7ef36",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.3"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 1,
                "repo:createdDate": "2020-10-20T02:37:11.263718Z",
                "repo:lastModifiedDate": "2020-10-20T02:37:11.263718Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:ids": [
                        "xcore:tag:124bd3de7f598dd8"
                    ],
                    "xdm:name": "Mobile Demo",
                    "xdm:filterType": "anyTags",
                    "@id": "xcore:offer-filter:124bd44648f17ec1"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.3#27c92e00-127d-11eb-b9fe-5bcfb5d7ef36",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/27c92e00-127d-11eb-b9fe-5bcfb5d7ef36",
                        "@type": "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.3"
                    }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
            },
            {
                "instanceId": "2c54fc90-f8f3-11ea-ad6e-775ad2c9b1a1",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.3"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 1,
                "repo:createdDate": "2020-09-17T14:36:29.272451Z",
                "repo:lastModifiedDate": "2020-09-17T14:36:29.272451Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:ids": [
                        "xcore:personalized-offer:1221fbedfa4d98b0"
                    ],
                    "xdm:name": "demo collection",
                    "xdm:filterType": "offers",
                    "@id": "xcore:offer-filter:1221fc71c74d98b4"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.3#2c54fc90-f8f3-11ea-ad6e-775ad2c9b1a1",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/2c54fc90-f8f3-11ea-ad6e-775ad2c9b1a1",
                        "@type": "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.3"
                    }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
            }
        ],
        "total": 8,
        "count": 2
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1&limit=2",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        },
        "next": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?start=2c54fc90-f8f3-11ea-ad6e-775ad2c9b1a1&orderby=instanceId&schema=https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1&limit=2",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
