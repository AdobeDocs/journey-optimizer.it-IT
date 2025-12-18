---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Elenco dei qualificatori di raccolta
description: I qualificatori di raccolta ti consentono di organizzare e ordinare meglio le offerte.
feature: Decision Management, API
badge: label="Legacy" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: cc577989-198c-4e21-80e7-32ebb7a60606
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 11%

---

# Elenco dei qualificatori di raccolta {#list-tags}

>[!TIP]
>
>La funzione Decisioni, la nuova funzionalità decisionale di [!DNL Adobe Journey Optimizer], è ora disponibile tramite i canali e-mail e di esperienza basati su codice. [Ulteriori informazioni](../../experience-decisioning/gs-experience-decisioning.md)


I qualificatori di raccolta (noti in precedenza come &quot;tag&quot;) consentono di organizzare e ordinare meglio le offerte. Ad esempio, puoi etichettare le offerte del Black Friday con il qualificatore per la raccolta &quot;Black Friday&quot;. Puoi quindi utilizzare la funzionalità di ricerca nella Libreria offerte per individuare facilmente tutte le offerte con quel qualificatore di raccolta.

I qualificatori di raccolta possono essere utilizzati anche per raggruppare le offerte in raccolte. Per ulteriori informazioni, consulta l&#39;esercitazione su [creazione di raccolte](../../../../offer-library/creating-collections.md).

È possibile visualizzare un elenco di tutti i qualificatori di raccolta eseguendo una singola richiesta GET all&#39;API [!DNL Offer Library].

**Formato API**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_TAG}&{QUERY_PARAMS}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso dell’endpoint per le API dell’archivio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Contenitore in cui si trovano i qualificatori di raccolta. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_TAG}` | Definisce lo schema associato ai qualificatori di raccolta. | `https://ns.adobe.com/experience/offer-management/tag;version=0.1` |
| `{QUERY_PARAMS}` | Parametri di query facoltativi in base ai quali filtrare i risultati. | `limit=2` |

**Richiesta**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/tag;version=0.1&limit=2' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

## Utilizzo dei parametri di query {#using-query-parameters}

Puoi utilizzare i parametri di query per visualizzare e filtrare i risultati quando elenchi le risorse.

### Paging {#paging}

I parametri di query più comuni per il paging includono:

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `property` | Un filtro proprietà facoltativo: <ul><li>Le proprietà sono raggruppate per operazione AND.</li><li>I parametri possono essere ripetuti come segue: proprietà={PROPERTY_EXPR}[&amp;proprietà={PROPERTY_EXPR2}...] o proprietà={PROPERTY_EXPR1}[,{PROPERTY_EXPR2}...]</li><li>Le espressioni di proprietà sono in formato `[!]field[op]value`, con `op` in `[==,!=,<=,>=,<,>,~]`, che supportano espressioni regolari.</li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | Ordinare i risultati per una proprietà specifica. Se si aggiunge un segno - prima del nome (orderby=-name), gli elementi verranno ordinati in base al nome in ordine decrescente (Z-A). Le espressioni di percorso sono sotto forma di percorsi separati da punti. Questo parametro può essere ripetuto come segue: `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | Limita il numero di entità restituite. | `limit=5` |

**Risposta**

In caso di esito positivo, la risposta restituisce un elenco di qualificatori di raccolta presenti all’interno del contenitore a cui hai accesso.

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/tag;version=0.1",
    "requestTime": "2023-10-21T20:28:21.521267Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "0adf2ef0-0f6e-11eb-b3be-9b775f952952",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 2,
                "repo:createdDate": "2023-10-16T05:11:26.815213Z",
                "repo:lastModifiedDate": "2023-10-16T22:20:20.190006Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:name": "Sneakers",
                    "@id": "xcore:tag:1246d138ec8cca1f"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/tag;version=0.1#0adf2ef0-0f6e-11eb-b3be-9b775f952952",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/0adf2ef0-0f6e-11eb-b3be-9b775f952952",
                        "@type": "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
                    }
                }
            },
            {
                "instanceId": "149e0de0-ff5f-11ea-b017-f98866426d43",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 1,
                "repo:createdDate": "2023-09-25T18:44:02.109748Z",
                "repo:lastModifiedDate": "2023-09-25T18:44:02.109748Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:name": "retirement",
                    "@id": "xcore:tag:122c81d2804e69e3"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/tag;version=0.1#149e0de0-ff5f-11ea-b017-f98866426d43",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/149e0de0-ff5f-11ea-b017-f98866426d43",
                        "@type": "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
                    }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
            }
        ],
        "total": 11,
        "count": 2
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/tag;version=0.1&limit=2",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        },
        "next": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?start=149e0de0-ff5f-11ea-b017-f98866426d43&orderby=instanceId&schema=https://ns.adobe.com/experience/offer-management/tag;version=0.1&limit=2",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
