---
title: aggiornare un posizionamento
description: I posizionamenti sono contenitori utilizzati per mostrare le offerte.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 6990918c-e736-4f28-9ac6-9ac3101b069f
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 9%

---

# Aggiornare un posizionamento

Puoi modificare o aggiornare un posizionamento nel contenitore effettuando una richiesta di PATCH al [!DNL Offer Library] API.

Per ulteriori informazioni sulla patch JSON, comprese le operazioni disponibili, consulta il [Documentazione sulle patch JSON](http://jsonpatch.com/).

## Intestazioni Accept e Content-Type

Nella tabella seguente sono riportati i valori validi che comprendono *Content-Type* e *Accetta* campi nell’intestazione della richiesta:

| Nome intestazione | Valore |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"` |

**Formato API**

```http
PATCH /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API dell&#39;archivio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Il contenitore in cui si trovano i posizionamenti. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | ID istanza del posizionamento da aggiornare. | `9aa58fd0-13d7-11eb-928b-576735ea4db8` |

**Richiesta**

```shell
curl -X PATCH \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/9aa58fd0-13d7-11eb-928b-576735ea4db8' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'\
  -d '[
        {
            "op": "replace",
            "path": "/_instance/xdm:name",
            "value": "Sales and Promotions Placement"
        },
        {
            "op": "replace",
            "path": "/_instance/xdm:description",
            "value": "A test placement to contain offers of sales and discounts"
        }
    ]'
```

| Parametro | Descrizione |
| --------- | ----------- |
| `op` | Chiamata dell’operazione utilizzata per definire l’azione necessaria per aggiornare la connessione. Le operazioni includono: `add`, `replace`e `remove`. |
| `path` | Percorso del parametro da aggiornare. |
| `value` | Il nuovo valore con cui si desidera aggiornare il parametro. |

**Risposta**

Una risposta corretta restituisce i dettagli aggiornati del posizionamento, inclusi l’ID istanza univoco e il posizionamento `@id`.

```json
{
    "instanceId": "9aa58fd0-13d7-11eb-928b-576735ea4db8",
    "@id": "xcore:offer-placement:124e0be5699743d3",
    "repo:etag": 2,
    "repo:createdDate": "2020-10-21T19:57:09.837456Z",
    "repo:lastModifiedDate": "2020-10-21T19:59:10.700149Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
