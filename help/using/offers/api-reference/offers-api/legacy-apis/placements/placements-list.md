---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Elencare posizionamenti
description: I posizionamenti sono contenitori utilizzati per presentare le offerte.
feature: Decision Management, API
badge: label="Legacy" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 52fbf683-d86f-43c6-be1a-c06141b64b16
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 17%

---

# Elencare posizionamenti {#list-placements}

>[!TIP]
>
>La funzione Decisioni, la nuova funzionalità decisionale di [!DNL Adobe Journey Optimizer], è ora disponibile tramite i canali e-mail e di esperienza basati su codice. [Ulteriori informazioni](../../experience-decisioning/gs-experience-decisioning.md)


I posizionamenti sono contenitori utilizzati per presentare le offerte. Il posizionamento garantisce che il contenuto dell’offerta corretta venga visualizzato nella posizione corretta all’interno del messaggio. Quando aggiungi contenuto a un’offerta, ti verrà chiesto di selezionare un posizionamento in cui visualizzare il contenuto.

È possibile visualizzare un elenco di tutti i posizionamenti all&#39;interno di un contenitore eseguendo una singola richiesta GET all&#39;API [!DNL Offer Library].

**Formato API**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_PLACEMENT}&{QUERY_PARAMS}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso dell’endpoint per le API dell’archivio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Il contenitore in cui si trovano i posizionamenti. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `SCHEMA_PLACEMENT}` | Definisce lo schema associato ai posizionamenti. | `https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4` |
| `{QUERY_PARAMS}` | Parametri di query facoltativi in base ai quali filtrare i risultati. | `limit=2` |

## Utilizzo dei parametri di query {#using-query-parameters}

Puoi utilizzare i parametri di query per visualizzare e filtrare i risultati quando elenchi le risorse.

### Paging {#paging}

I parametri di query più comuni per il paging includono:

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `q` | Stringa di query facoltativa da cercare nei campi selezionati. La stringa di query deve essere in minuscolo e può essere racchiusa tra virgolette doppie per impedire che venga tokenizzata e per evitare caratteri speciali. I caratteri `+ - = && \|\| > < ! ( ) { } [ ] ^ \" ~ * ? : \ /` hanno un significato speciale e devono essere preceduti da una barra rovesciata quando vengono visualizzati nella stringa query. | JSON per sito web |
| `qop` | Applica l’operatore AND o OR ai valori nel parametro della stringa di query q. | `AND` / `OR` |
| `field` | Elenco facoltativo di campi a cui limitare la ricerca. Questo parametro può essere ripetuto come segue: field=field1[,field=field2,...] e (le espressioni di percorso sono sotto forma di percorsi separati da punti come _instance.xdm:name) | `_instance.xdm:name` |
| `orderBy` | Ordinare i risultati per una proprietà specifica. L&#39;aggiunta di un `-` prima del titolo (`orderby=-title`) ordinerà gli elementi in base al titolo in ordine decrescente (Z-A). | `-repo:createdDate` |
| `limit` | Limita il numero di posizionamenti restituiti. | `limit=5` |

**Richiesta**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4&limit=2' \
  -H 'Accept: *,application/json' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Risposta**

In caso di esito positivo, la risposta restituisce un elenco di posizionamenti presenti all’interno del contenitore a cui hai accesso.

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4",
    "requestTime": "2023-10-21T19:48:51.843067Z",
    "_embedded": {
    "results": [
        {
                "instanceId": "0feb6a80-0f32-11eb-8110-e17787c335b5",
            "schemas": [
                    "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"
            ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 2,
                "repo:createdDate": "2023-10-15T22:02:05.480449Z",
                "repo:lastModifiedDate": "2023-10-15T22:13:00.278175Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:name": "New placement name",
                    "xdm:componentType": "https://ns.adobe.com/experience/offer-management/content-component-html",
                    "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                    "xdm:description": "Updated placement description",
                    "@id": "xcore:offer-placement:12466ef35fc5baa0"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4#0feb6a80-0f32-11eb-8110-e17787c335b5",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/0feb6a80-0f32-11eb-8110-e17787c335b5",
                        "@type": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"
                    }
            }
        },
        {
                "instanceId": "269192b0-f8f2-11ea-8723-916b9fbadc53",
            "schemas": [
                    "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"
                ],
                "productContexts": [
                    "acp"
            ],
                "repo:etag": 1,
                "repo:createdDate": "2023-09-17T14:29:10.107121Z",
                "repo:lastModifiedDate": "2023-09-17T14:29:10.107121Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:componentType": "https://ns.adobe.com/experience/offer-management/content-component-html",
                    "xdm:name": "demo placement",
                    "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                    "@id": "xcore:offer-placement:1221fac4e7340521"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4#269192b0-f8f2-11ea-8723-916b9fbadc53",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/269192b0-f8f2-11ea-8723-916b9fbadc53",
                        "@type": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"
            }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
        }
    ],
        "total": 17,
        "count": 2
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4&limit=2",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        },
        "next": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?start=269192b0-f8f2-11ea-8723-916b9fbadc53&orderby=instanceId&schema=https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4&limit=2",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
