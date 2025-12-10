---
title: Eliminare una strategia di selezione
description: Le strategie di selezione sono costituite da raccolte associate a vincoli e metodi di classificazione per determinare le offerte.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 774f3773-bc39-46c4-b32c-143abbd45696
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 5%

---

# Eliminare una strategia di selezione {#delete-selection-strategy}

A volte può essere necessario rimuovere (DELETE) una strategia di selezione. A tal fine, esegui una richiesta DELETE all’API della Libreria di offerte utilizzando l’ID della strategia di selezione che desideri eliminare.

**Formato API**

```http
DELETE /{ENDPOINT_PATH}/selection-strategies/{ID}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API di persistenza. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | ID dell’entità da eliminare. | `selectionStrategy1234` |

**Richiesta**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/selection-strategies/selectionStrategy1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Risposta**

In caso di esito positivo, la risposta restituisce lo stato HTTP 200 e un corpo vuoto.

Puoi confermare l’eliminazione tentando di inviare una richiesta di ricerca (GET) alla strategia di selezione. Dovresti ricevere lo stato HTTP 404 (Non trovato) perché la strategia di selezione è stata rimossa.
