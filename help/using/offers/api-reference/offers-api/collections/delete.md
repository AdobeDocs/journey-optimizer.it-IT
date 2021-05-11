---
title: Eliminare una raccolta
description: Le raccolte sono sottoinsiemi di offerte in base a condizioni predefinite definite da un addetto al marketing, ad esempio la categoria dell’offerta.
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 7%

---

# Eliminare una raccolta

A volte può essere necessario rimuovere (DELETE) una raccolta. È possibile eliminare solo le raccolte create nel contenitore tenant. A tal fine, esegui una richiesta DELETE all’ API [!DNL Offer Library] utilizzando il valore $id della raccolta che desideri eliminare.

**Formato API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API dell&#39;archivio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Il contenitore in cui si trovano le raccolte. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | ID istanza della raccolta che desideri aggiornare. | `0bf31c20-13f1-11eb-a752-e58fd7dc4cb3` |

**Richiesta**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/0bf31c20-13f1-11eb-a752-e58fd7dc4cb3' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Risposta**

Una risposta corretta restituisce lo stato HTTP 202 (nessun contenuto) e un corpo vuoto.

Puoi confermare l&#39;eliminazione tentando una richiesta di ricerca (GET) alla raccolta. Sarà necessario includere un’intestazione Accept nella richiesta, ma dovrebbe ricevere lo stato HTTP 404 (Non trovato) perché la raccolta è stata rimossa dal contenitore.
