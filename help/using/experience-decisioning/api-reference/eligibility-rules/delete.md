---
title: Eliminare una regola di idoneità
description: Le regole di idoneità consentono di definire i candidati idonei in base a ciò di cui desideri eseguire il targeting, ad esempio gli attributi di profilo e i tipi di pubblico.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: 8fa34ebb7c853f9af5b3f58574374a3acb641dd9
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 5%

---

# Eliminare una regola di idoneità {#delete-eligibility-rule}

A volte può essere necessario rimuovere (DELETE) una regola di idoneità. A tal fine, esegui una richiesta DELETE all’API della Libreria di offerte utilizzando l’ID della regola di idoneità che desideri eliminare.

**Formato API**

```http
DELETE /{ENDPOINT_PATH}/eligibility-rules/{ID}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API di persistenza. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | ID dell’entità da eliminare. | `rule1234` |

**Richiesta**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-rules/rule1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Risposta**

In caso di esito positivo, la risposta restituisce lo stato HTTP 200 e un corpo vuoto.

Puoi confermare l’eliminazione tentando una richiesta di ricerca (GET) alla regola. Dovresti ricevere lo stato HTTP 404 (Non trovato) perché la regola è stata rimossa.
