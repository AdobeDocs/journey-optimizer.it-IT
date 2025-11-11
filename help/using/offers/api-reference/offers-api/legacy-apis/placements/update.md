---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: aggiornare un posizionamento
description: I posizionamenti sono contenitori utilizzati per presentare le offerte.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 759c58e7-af1e-409c-8400-996b9a647ba7
version: Journey Orchestration
source-git-commit: d6a9a8a392f0492aa6e4f059198ce77b6b2cd962
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 10%

---

# Aggiornare un posizionamento {#update-placement}

È possibile modificare o aggiornare un posizionamento nel contenitore effettuando una richiesta PATCH all&#39;API [!DNL Offer Library].

Per ulteriori informazioni sulla patch JSON, incluse le operazioni disponibili, consulta la [documentazione ufficiale sulla patch JSON](https://jsonpatch.com/).

## Intestazioni Accept e Content-Type {#accept-and-content-type-headers}

La tabella seguente mostra i valori validi che comprendono i campi *Content-Type* e *Accept* nell&#39;intestazione della richiesta:

| Nome intestazione | Valore |
| ----------- | ----- |
| Accetta | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"` |

**Formato API**

```http
PATCH /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso dell’endpoint per le API dell’archivio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Il contenitore in cui si trovano i posizionamenti. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | ID istanza del posizionamento da aggiornare. | `9aa58fd0-13d7-11eb-928b-576735ea4db8` |

**Richiesta**

```shell
curl -X PATCH \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/9aa58fd0-13d7-11eb-928b-576735ea4db8' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
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
| `op` | Chiamata di operazione utilizzata per definire l&#39;azione necessaria per aggiornare la connessione. Le operazioni includono: `add`, `replace` e `remove`. |
| `path` | Percorso del parametro da aggiornare. |
| `value` | Il nuovo valore con cui desideri aggiornare il parametro. |

**Risposta**

In caso di esito positivo, la risposta restituisce i dettagli aggiornati del posizionamento, inclusi l’ID istanza univoco e il posizionamento `@id`.

```json
{
    "instanceId": "9aa58fd0-13d7-11eb-928b-576735ea4db8",
    "@id": "xcore:offer-placement:124e0be5699743d3",
    "repo:etag": 2,
    "repo:createdDate": "2023-10-21T19:57:09.837456Z",
    "repo:lastModifiedDate": "2023-10-21T19:59:10.700149Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
