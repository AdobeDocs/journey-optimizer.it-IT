---
title: Eliminare una formula di classificazione
description: Le formule di classificazione consentono di definire le funzioni per il punteggio, utilizzate per classificare gli elementi.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: 8fa34ebb7c853f9af5b3f58574374a3acb641dd9
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 5%

---

# Eliminare una formula di classificazione {#delete-selection-strategy}

A volte può essere necessario rimuovere (DELETE) una formula di classificazione. A tal fine, esegui una richiesta DELETE all’API della Libreria di offerte utilizzando l’ID della formula di classificazione che desideri eliminare.

**Formato API**

```http
DELETE /{ENDPOINT_PATH}/ranking-formulas/{ID}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API di persistenza. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | ID dell’entità da eliminare. | `rankingFormula1234` |

**Richiesta**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/ranking-formulas/rankingFormula1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Risposta**

In caso di esito positivo, la risposta restituisce lo stato HTTP 200 e un corpo vuoto.

Puoi confermare l’eliminazione tentando una richiesta di ricerca (GET) nella formula di classificazione. Dovresti ricevere lo stato HTTP 404 (Non trovato) perché la formula di classificazione è stata rimossa.

