---
title: Cercare un posizionamento
description: I posizionamenti sono contenitori utilizzati per presentare le offerte.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 42fb17a2-842e-4e20-9013-7227adba0105
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 4%

---

# Cercare un posizionamento {#look-up-placement}

Per cercare posizionamenti specifici, devi effettuare una richiesta GET al [!DNL Offer Library] API che include il posizionamento `@id` o il nome del posizionamento nel percorso della richiesta.

**Formato API**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_PLACEMENT}&{QUERY_PARAMS}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso dell’endpoint per le API dell’archivio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Il contenitore in cui si trovano i posizionamenti. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `SCHEMA_PLACEMENT}` | Definisce lo schema associato ai posizionamenti. | `https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4` |
| `id` | Stringa utilizzata per la corrispondenza con `@id` delle entità. La stringa corrisponde esattamente. Parametri `id` e `name` non possono essere utilizzati insieme. | `xcore:offer-placement:124541309805b7e8` |
| `name` | Stringa utilizzata per corrispondere alla proprietà xdm:name delle entità. La stringa viene trovata una corrispondenza esatta con maiuscole, ma è possibile utilizzare caratteri jolly. Parametri `id` e `name` non può essere utilizzato insieme | `Sales and Promotions Placement` |

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4&name=Sales%20and%20Promotions%20Placement' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema='\''https://ns.adobe.com/experience/xcore/hal/results'\''' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Risposta**

In caso di esito positivo, la risposta restituisce i dettagli del posizionamento, incluse le informazioni sull’ID contenitore, l’ID istanza e il posizionamento univoco `@id`.

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4",
    "requestTime": "2023-10-21T20:04:53.656503Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "9aa58fd0-13d7-11eb-928b-576735ea4db8",
    "schemas": [
                    "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"
                ],
                "productContexts": [
                    "acp"
    ],
                "repo:etag": 2,
                "repo:createdDate": "2023-10-21T19:57:09.837456Z",
                "repo:lastModifiedDate": "2023-10-21T19:59:10.700149Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_score": 0,
                "_instance": {
                    "xdm:name": "Sales and Promotions Placement",
                    "xdm:componentType": "https://ns.adobe.com/experience/offer-management/content-component-html",
                    "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                    "xdm:description": "A test placement to contain offers of sales and discounts",
                    "@id": "xcore:offer-placement:124e0be5699743d3"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4#9aa58fd0-13d7-11eb-928b-576735ea4db8",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/9aa58fd0-13d7-11eb-928b-576735ea4db8",
                        "@type": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"
                    }
                }
            }
        ],
        "total": 1,
        "count": 1
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4&name=Sales%20and%20Promotions%20Placement",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
