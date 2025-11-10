---
title: Eliminare un elemento di decisione
description: Gli elementi decisionali sono offerte di marketing che puoi creare e organizzare in raccolte e cataloghi.
feature: Decision Management, API, Collections
topic: Integrations
role: Developer
level: Experienced
exl-id: 0fd608e0-df71-4e2d-8304-d7d5561c7c7a
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 6%

---

# Eliminare un elemento di decisione {#delete-decision-item}

Per rimuovere un elemento di decisione, esegui una richiesta DELETE all’API Libreria di offerte con l’ID dell’elemento di decisione che desideri eliminare.

**Formato API**

```http
DELETE /{ENDPOINT_PATH}/offer-items/{ID}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API di persistenza. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | ID dell’entità da eliminare. | `offerItem1234` |

**Richiesta**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-items/offerItem1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-schema-id: {SCHEMA_ID}'
```

**Risposta**

In caso di esito positivo, la risposta restituisce lo stato HTTP 200 e un corpo vuoto.

Puoi confermare l’eliminazione tentando una richiesta di ricerca (GET) all’elemento decisionale. Dovresti ricevere lo stato HTTP 404 (Non trovato) perché l’elemento decisione è stato rimosso.
