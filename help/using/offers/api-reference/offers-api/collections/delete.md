---
title: Eliminare una raccolta
description: Le raccolte sono sottoinsiemi di offerte in base a condizioni predefinite definite da un addetto al marketing, ad esempio la categoria dell’offerta.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 2eaa0092-2436-4679-83f1-7530ab4a858f
source-git-commit: 9873af4caf7cd8bc4e9672748414bf78f28ed30b
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 8%

---

# Eliminare una raccolta {#delete-collection}

A volte può essere necessario rimuovere (DELETE) una raccolta. È possibile eliminare solo le raccolte create nel contenitore tenant. A questo scopo, esegui una richiesta DELETE al [!DNL Offer Library] API utilizzando il $id della raccolta che desideri eliminare.

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
