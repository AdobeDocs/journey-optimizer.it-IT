---
title: Eliminare una raccolta di elementi
description: Scopri come categorizzare le decisioni di gruppo in raccolte.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: eb89bc5205d98a67cd0bb42bebbd9429786e33e7
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 6%

---


# Eliminare una raccolta di elementi {#delete-decision-item}

A volte può essere necessario rimuovere (DELETE) una raccolta di elementi. A tale scopo, devi eseguire una richiesta DELETE all’API della Libreria di offerte utilizzando l’ID della raccolta di elementi che desideri eliminare.

**Formato API**

```http
DELETE /{ENDPOINT_PATH}/item-collections/{ID}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API di persistenza. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | ID dell’entità da eliminare. | `itemCollections1234` |

**Richiesta**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/item-collections/itemCollections1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Risposta**

In caso di esito positivo, la risposta restituisce lo stato HTTP 200 e un corpo vuoto.

È possibile confermare l&#39;eliminazione tentando una richiesta di ricerca (GET) alla raccolta di elementi. Dovresti ricevere lo stato HTTP 404 (Non trovato) perché la raccolta di elementi è stata rimossa.
