---
title: Creare una regola di decisione
description: Le regole decisionali sono vincoli aggiunti a un’offerta personalizzata e applicati a un profilo per determinare l’idoneità.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 6a05efca-31bd-46d5-998d-ff3038d9013f
source-git-commit: 353aaf2bc4f32b1b0d7bfc2f7f4f48537cc79df4
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 12%

---

# Creare una regola di decisione {#create-decision-rule}

Le regole decisionali sono vincoli aggiunti a un’offerta personalizzata e applicati a un profilo per determinare l’idoneità.

## Intestazioni Accept e Content-Type {#accept-and-content-type-headers}

Nella tabella seguente sono riportati i valori validi che comprendono *Content-Type* e *Accetta* campi nell’intestazione della richiesta:

| Nome intestazione | Valore |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"` |

**Formato API**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API dell&#39;archivio. | `https://platform.adobe.io/data/core/xcore/` |
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
        "condition": {
            "type": "PQL",
            "format": "pql/text",
            "value": "profile.person.name.firstName.equals(\"Joe\", false)"
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

Una risposta corretta restituisce informazioni sulla regola decisionale appena creata, incluso l’ID istanza univoco e il posizionamento `@id`. Puoi utilizzare l’ID istanza nei passaggi successivi per aggiornare o eliminare la regola decisionale. Puoi utilizzare la tua regola decisionale univoca `@id` in un’esercitazione successiva per creare offerte personalizzate.

```json
{
    "instanceId": "eaa5af90-13d9-11eb-9472-194dee6dc381",
    "@id": "xcore:eligibility-rule:124e0faf5b8ee89b",
    "repo:etag": 1,
    "repo:createdDate": "2020-10-21T20:13:43.048666Z",
    "repo:lastModifiedDate": "2020-10-21T20:13:43.048666Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
