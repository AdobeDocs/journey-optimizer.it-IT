---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Creare una decisione
description: Una decisione contiene la logica su cui si basa la selezione di un’offerta.
feature: Decision Management, API
badge: label="Legacy" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 7cb906b9-8925-4482-9915-448a41e11d9d
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/ZSGnM6ab3lRA3tFax09mDx7Aaw32b01Mxduq-MrMDrQ
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: ed0d8d0e-04b9-4326-be72-a0fbca265377
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 129
ht-degree: 0%

---

# Creare una decisione {#create-decision}

>[!TIP]
>
>Decisioning, la nuova funzionalità decisionale di [!DNL Adobe Journey Optimizer], è ora disponibile tramite l&#39;esperienza basata sul codice e i canali e-mail. [Ulteriori informazioni](../../../../../experience-decisioning/gs-experience-decisioning.md)


È possibile creare una decisione effettuando una richiesta POST all&#39;API [!DNL Offer Library] e fornendo al tempo stesso l&#39;ID contenitore.

## Intestazioni Accept e Content-Type {#accept-and-content-type-headers}

La tabella seguente mostra i valori validi che comprendono i campi *Content-Type* e *Accept* nell&#39;intestazione della richiesta:

| Nome intestazione | Valore |
| ----------- | ----- |
| Content-Type | `application/json` |

**Formato API**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso dell’endpoint per le API dell’archivio. | `https://platform.adobe.io/data/core/xcore/` |
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
      "_instance": {
          "xdm:name": "Test API",
          "xdm:startDate": "2022-01-20T16:00:00Z",
          "xdm:endDate": "2022-01-27T16:00:00Z",
          "xdm:status": "live",
          "xdm:criteria": [
        {
                  "xdm:placements": [
                      "xcore:offer-placement:1457f9322f005194"
            ],
                  "xdm:optionSelection": {
                      "xdm:filter": "xcore:offer-filter:1457f93227d0b6f0"
                }
              }
          ],
          "xdm:fallback": "xcore:fallback-offer:13c259399d8bf013"
            },
      "_links": {}
}'
```

**Risposta**

In caso di esito positivo, la risposta restituisce informazioni sulla decisione appena creata, incluso il relativo `id` univoco. È possibile utilizzare `id` nei passaggi successivi per aggiornare o eliminare la decisione.

```json
{
    "instanceId": "f88c9be0-1245-11eb-8622-b77b60702882",
    "@id": "xcore:offer-activity:124b79dc3ce2d720",
    "repo:etag": 1,
    "repo:createdDate": "2023-10-19T20:02:09.694067Z",
    "repo:lastModifiedDate": "2023-10-19T20:02:09.694067Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
