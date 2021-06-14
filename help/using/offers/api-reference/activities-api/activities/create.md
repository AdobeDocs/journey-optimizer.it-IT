---
title: Creare decisioni
description: Una decisione contiene la logica che informa la selezione di un’offerta.
feature: Offerte
topic: Integrazioni
role: Data Engineer
level: Experienced
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 12%

---

# Creare una decisione

Puoi creare una decisione (precedentemente nota come attività di offerta) effettuando una richiesta di POST all’ API [!DNL Offer Library] , fornendo al contempo il tuo ID contenitore.

## Intestazioni Accept e Content-Type

La tabella seguente mostra i valori validi che comprendono i campi *Content-Type* e *Accept* nell&#39;intestazione della richiesta:

| Nome intestazione | Valore |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"` |

**Formato API**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API dell&#39;archivio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Il contenitore in cui si trovano le decisioni. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Richiesta**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '{
        "xdm:name": "Activity 1",
        "xdm:startDate": "2020-10-01T16:00:00Z",
        "xdm:endDate": "2021-12-13T16:00:00Z",
        "xdm:status": "live",
        "xdm:criteria": [
            {
                "xdm:placements": [
                    "xcore:offer-placement:122204529514a2c0"
                ],
                "xdm:optionSelection": {
                    "xdm:filter": "xcore:offer-filter:122a120f234dac7f"
                }
            }
        ],
        "xdm:fallback": "xcore:fallback-offer:1233160780eaa2ef"
    }'
```

**Risposta**

Una risposta corretta restituisce informazioni sulla nuova decisione creata, incluso l’ID istanza univoco e il posizionamento `@id`. Puoi utilizzare l’ID istanza nei passaggi successivi per aggiornare o eliminare la tua decisione.

```json
{
    "instanceId": "f88c9be0-1245-11eb-8622-b77b60702882",
    "@id": "xcore:offer-activity:124b79dc3ce2d720",
    "repo:etag": 1,
    "repo:createdDate": "2020-10-19T20:02:09.694067Z",
    "repo:lastModifiedDate": "2020-10-19T20:02:09.694067Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
