---
title: Aggiornare le raccolte
description: Le raccolte sono sottoinsiemi di offerte in base a condizioni predefinite definite da un addetto al marketing, ad esempio la categoria dell’offerta.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7d766f0a-4fcb-434a-bbfd-e18ade71ae56
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 9%

---

# Aggiornare una raccolta

Puoi modificare o aggiornare una raccolta effettuando una richiesta di PATCH al [!DNL Offer Library] API

Per ulteriori informazioni sulla patch JSON, comprese le operazioni disponibili, consulta il [Documentazione sulle patch JSON](http://jsonpatch.com/).

## Intestazioni Accept e Content-Type

Nella tabella seguente sono riportati i valori validi che comprendono *Content-Type* e *Accetta* campi nell’intestazione della richiesta:

| Nome intestazione | Valore |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1"` |

**Formato API**

```http
PATCH /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API dell&#39;archivio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Il contenitore in cui si trovano le raccolte. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | ID istanza della raccolta che desideri aggiornare. | `0bf31c20-13f1-11eb-a752-e58fd7dc4cb3` |

**Richiesta**

```shell
curl -X PATCH \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/0bf31c20-13f1-11eb-a752-e58fd7dc4cb3' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '[
        {
            "op": "add",
            "path": "/_instance/xdm:filterType",
            "value": "anyTags"
        },
        {
            "op": "add",
            "path": "/_instance/xdm:ids",
            "value": ["xcore:tag:124e147572cd7866"]
        }
    ]'
```

| Parametro | Descrizione |
| --------- | ----------- |
| `op` | Chiamata dell’operazione utilizzata per definire l’azione necessaria per aggiornare la connessione. Le operazioni includono: `add`, `replace`e `remove`. |
| `path` | Percorso del parametro da aggiornare. |
| `value` | Il nuovo valore con cui si desidera aggiornare il parametro. |

**Risposta**

Una risposta corretta restituisce i dettagli aggiornati della raccolta, inclusi l’ID istanza univoco e la raccolta `@id`.

```json
{
    "instanceId": "0bf31c20-13f1-11eb-a752-e58fd7dc4cb3",
    "@id": "xcore:offer-filter:124e3594ce8b4930",
    "repo:etag": 1,
    "repo:createdDate": "2020-10-21T22:59:17.345797Z",
    "repo:lastModifiedDate": "2020-10-21T22:59:17.345797Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
