---
title: Elenco dei qualificatori di raccolta
description: I qualificatori di raccolta ti consentono di organizzare e ordinare meglio le offerte.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 8cee44ed-5569-416c-b463-e75fb20d4c9c
source-git-commit: ba7d065523116c12e22eec300df13c29d92a54fb
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 7%

---


# Elenco dei qualificatori di raccolta {#list-tags}

I qualificatori di raccolta (noti in precedenza come &quot;tag&quot;) consentono di organizzare e ordinare meglio le offerte. Ad esempio, puoi etichettare le offerte del Black Friday con il qualificatore per la raccolta &quot;Black Friday&quot;. Puoi quindi utilizzare la funzionalità di ricerca nella Libreria offerte per individuare facilmente tutte le offerte con quel qualificatore di raccolta.

I qualificatori di raccolta possono essere utilizzati anche per raggruppare le offerte in raccolte.

Per visualizzare un elenco di tutti i qualificatori di raccolta all’interno di un contenitore, esegui una singola richiesta GET all’API Libreria di offerte.

**Formato API**

```http
GET /{ENDPOINT_PATH}/tags?{QUERY_PARAMS}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API di persistenza. | `https://platform.adobe.io/data/core/dps` |
| `{QUERY_PARAMS}` | Parametri di query facoltativi in base ai quali filtrare i risultati. | `limit=2` |

### Paging {#paging}

I parametri di query più comuni per il paging includono:

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `property` | Un filtro proprietà facoltativo: <ul><li>Le proprietà sono raggruppate per operazione AND.</li><li>I parametri possono essere ripetuti come segue: property={PROPERTY_EXPR}[&amp;property={PROPERTY_EXPR2}...] or property={PROPERTY_EXPR1}[,{PROPERTY_EXPR2}...]</li><li>Le espressioni di proprietà sono in formato `[!]field[op]value`, con `op` in `[==,!=,<=,>=,<,>,~]`, con supporto di espressioni regolari.</li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | Ordinare i risultati per una proprietà specifica. Se si aggiunge un segno - prima del nome (orderby=-name), gli elementi verranno ordinati in base al nome in ordine decrescente (Z-A). Le espressioni di percorso sono sotto forma di percorsi separati da punti. Questo parametro può essere ripetuto come segue: `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | Limita il numero di posizionamenti restituiti. | `limit=5` |

**Richiesta**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/tags?limit=2' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Risposta**

In caso di esito positivo, la risposta restituisce un elenco di qualificatori di raccolta presenti all’interno del contenitore a cui hai accesso.

```json
{
    "results": [
        {
            "created": "2022-09-16T19:00:02.070+00:00",
            "modified": "2022-09-16T19:00:02.070+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "tag1234",
            "name": "Sneakers"
        },
        {
            "created": "2022-09-16T19:55:02.168+00:00",
            "modified": "2022-09-16T19:55:02.168+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "tag5678",
            "name": "Black Friday"
        }
    ],
    "count": 2,
    "total": 5,
    "_links": {
        "self": {
            "href": "/tags?href={SELF_HREF}&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/tags?href={NEXT_HREF}&limit=2",
            "type": "application/json"
        }
    }
}
```
