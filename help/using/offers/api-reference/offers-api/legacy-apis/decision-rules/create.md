---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Creare una regola di decisione
description: Le regole di decisione sono vincoli aggiunti a un’offerta personalizzata e applicati a un profilo per determinare l’idoneità.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 12c49f4c-a1b5-4841-ab98-663b4c771fb6
version: Journey Orchestration
source-git-commit: d6a9a8a392f0492aa6e4f059198ce77b6b2cd962
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 13%

---

# Creare una regola di decisione {#create-decision-rule}

Le regole di decisione sono vincoli aggiunti a un’offerta personalizzata e applicati a un profilo per determinare l’idoneità.

## Intestazioni Accept e Content-Type {#accept-and-content-type-headers}

La tabella seguente mostra i valori validi che comprendono i campi *Content-Type* e *Accept* nell&#39;intestazione della richiesta:

| Nome intestazione | Valore |
| ----------- | ----- |
| Accetta | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"` |

**Formato API**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso dell’endpoint per le API dell’archivio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Il contenitore in cui si trovano le regole di decisione. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Richiesta**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
    "xdm:name": "Sales rule",
    "description": "Decisioning rule for sales",
    "xdm:condition": {
        "xdm:type": "PQL",
        "xdm:format": "pql/text",
        "xdm:value": "profile.person.name.firstName.equals(\"Joe\", false)"
    },
    "xdm:definedOn": {
        "profile": {
            "xdm:schema": {
                "$ref": "https://ns.adobe.com/xdm/context/profile_union",
                "version": "1"
            },
            "xdm:referencePaths": [
                "person.name.firstName"
            ]
        }
    }
}'
```

**Risposta**

In caso di esito positivo, la risposta restituisce informazioni sulla regola di decisione appena creata, incluso l’ID istanza univoco e il posizionamento `@id`. Puoi utilizzare l’ID istanza nei passaggi successivi per aggiornare o eliminare la regola di decisione. È possibile utilizzare la regola di decisione univoca `@id` in un&#39;esercitazione successiva per creare offerte personalizzate.

```json
{
    "instanceId": "eaa5af90-13d9-11eb-9472-194dee6dc381",
    "@id": "xcore:eligibility-rule:124e0faf5b8ee89b",
    "repo:etag": 1,
    "repo:createdDate": "2023-10-21T20:13:43.048666Z",
    "repo:lastModifiedDate": "2023-10-21T20:13:43.048666Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
