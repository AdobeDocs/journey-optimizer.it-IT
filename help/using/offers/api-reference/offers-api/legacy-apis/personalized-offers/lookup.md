---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Cercare un’offerta personalizzata
description: Un’offerta personalizzata è un messaggio di marketing personalizzabile basato su regole e vincoli di idoneità.
feature: Decision Management, API
badge: label="Legacy" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 679f2229-19c6-47f9-b293-e1c3c8dcb61e
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 12%

---

# Cercare un’offerta personalizzata {#look-up-personalized-offer}

>[!TIP]
>
>La funzione Decisioni, la nuova funzionalità decisionale di [!DNL Adobe Journey Optimizer], è ora disponibile tramite i canali e-mail e di esperienza basati su codice. [Ulteriori informazioni](../../experience-decisioning/gs-experience-decisioning.md)


Un’offerta personalizzata è un messaggio di marketing personalizzabile basato su regole e vincoli di idoneità.

Per cercare offerte personalizzate specifiche, invia una richiesta GET all&#39;API **Libreria offerte** che include l&#39;offerta personalizzata `@id` o il nome dell&#39;offerta personalizzata nel percorso della richiesta.

**Formato API**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_PERSONALIZED_OFFER}&{QUERY_PARAMS}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso dell’endpoint per le API dell’archivio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Il contenitore in cui si trovano le offerte personalizzate. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_PERSONALIZED_OFFER}` | Definisce lo schema associato alle offerte personalizzate. | `https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5` |
| `id` | Stringa utilizzata per corrispondere alla proprietà `@id` delle entità. La stringa corrisponde esattamente. I parametri &quot;id&quot; e &quot;name&quot; non possono essere utilizzati insieme. | `xcore:personalized-offer:124cc332095cfa74` |
| `name` | Stringa utilizzata per corrispondere alla proprietà xdm:name delle entità. La stringa viene trovata una corrispondenza esatta con maiuscole, ma è possibile utilizzare caratteri jolly. I parametri `id` e `name` non possono essere utilizzati insieme | `Discount offer` |

**Richiesta**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5&name=Discount%20offer' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Risposta**

In caso di esito positivo, la risposta restituisce i dettagli del posizionamento, incluse informazioni sull&#39;ID contenitore, sull&#39;ID istanza e sull&#39;offerta personalizzata univoca `@id`.

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5",
    "requestTime": "2023-10-21T20:59:16.238585Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "fb2aad00-130e-11eb-aa26-21e7b1fa6da6",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 1,
                "repo:createdDate": "2023-10-20T20:01:02.927874Z",
                "repo:lastModifiedDate": "2023-10-20T20:01:02.927874Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_score": 0,
                "_instance": {
                    "xdm:name": "Discount offer",
                    "xdm:representations": [
                        {
                            "xdm:components": [
                                {
                                    "dc:language": [
                                        "en"
                                    ],
                                    "@type": "https://ns.adobe.com/experience/offer-management/content-component-json",
                                    "dc:format": "application/json"
                                }
                            ],
                            "xdm:placement": "xcore:offer-placement:12428d436d87dc84"
                        }
                    ],
                    "xdm:rank": {
                        "xdm:priority": 1
                    },
                    "xdm:selectionConstraint": {
                        "xdm:startDate": "2023-10-01T16:00:00Z",
                        "xdm:endDate": "2021-12-13T16:00:00Z",
                        "xdm:eligibilityRule": "xcore:eligibility-rule:124cb4511da781fc"
                    },
                    "xdm:status": "draft",
                    "xdm:cappingConstraint": {
                        "xdm:globalCap": 150
                    },
                    "xdm:tags": [
                        "xcore:tag:1246d138ec8cca1f"
                    ],
                    "@id": "xcore:personalized-offer:124cc332095cfa74"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5#fb2aad00-130e-11eb-aa26-21e7b1fa6da6",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/fb2aad00-130e-11eb-aa26-21e7b1fa6da6",
                        "@type": "https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"
                    }
                }
            }
        ],
        "total": 1,
        "count": 1
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5&name=Discount%20offer",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
