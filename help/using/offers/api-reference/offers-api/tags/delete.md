---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Elimina qualificatori raccolta
description: I qualificatori di raccolta ti consentono di organizzare e ordinare meglio le offerte.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 335c1b80-f1f0-4fd0-add8-84b8cc5e2e00
version: Journey Orchestration
source-git-commit: d6a9a8a392f0492aa6e4f059198ce77b6b2cd962
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 9%

---


# Eliminare un qualificatore di raccolta {#delete-tag}

A volte può essere necessario rimuovere (DELETE) un qualificatore di raccolta (precedentemente noto come &quot;tag&quot;). A tal fine, esegui una richiesta DELETE all’API della Libreria di offerte utilizzando l’ID del qualificatore di raccolta che desideri eliminare.

**Formato API**

```http
DELETE /{ENDPOINT_PATH}/tags/{ID}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API di persistenza. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | ID dell’entità da eliminare. | `tag1234` |

**Richiesta**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/tags/tag1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Risposta**

In caso di esito positivo, la risposta restituisce lo stato HTTP 200 e un corpo vuoto.

Puoi confermare l’eliminazione tentando una richiesta di ricerca (GET) nel qualificatore della raccolta. Dovresti ricevere lo stato HTTP 404 (Non trovato) perché il qualificatore della raccolta è stato rimosso.