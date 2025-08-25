---
title: Cercare una regola di decisione
description: Le regole di decisione sono vincoli aggiunti a un’offerta personalizzata e applicati a un profilo per determinare l’idoneità.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 54368710-1021-43c0-87b7-5176cc6c72f7
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 7%

---

# Cercare una regola di decisione {#lookup-decision-rule}

È possibile cercare una regola di decisione specifica effettuando una richiesta GET all&#39;API [!DNL Offer Library] che include la regola di decisione `id` nel percorso della richiesta.

**Formato API**

```http
GET /{ENDPOINT_PATH}/offer-rules/{ID}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API di persistenza. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | ID dell’entità da cercare. | `offerRule1234` |

**Richiesta**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offer-rules/offerRule1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Risposta**

In caso di esito positivo, la risposta restituisce i dettagli della regola di decisione specifica cercata, incluse le informazioni sulla regola di decisione univoca `id`.

```json
  {
    "created": "2022-09-16T18:59:53.651+00:00",
    "modified": "2022-09-16T18:59:53.651+00:00",
    "etag": 1,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"
    ],
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "offerRule1234",
    "name": "Californians with one or more purchases greater than $1000",
    "condition": {
        "type": "PQL",
        "format": "pql/text",
        "value": "homeAddress.stateProvince.equals(\"CA\", false) and (select var1 from xEvent where var1.eventType.equals(\"purchase\", true) and (var1.commerce.order.priceTotal = 1000.0 and var1.commerce.order.currencyCode.equals(\"USD\", false)))"
            }
}
```
