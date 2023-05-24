---
title: Eliminare le offerte personalizzate
description: Un’offerta personalizzata è un messaggio di marketing personalizzabile basato su regole e vincoli di idoneità.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 52a5053d-3b94-47fd-a064-a20f9a595150
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 7%

---

# Eliminare un’offerta personalizzata {#delete-personalized-offer}

Occasionalmente può essere necessario rimuovere (DELETE) un’offerta personalizzata. È possibile eliminare solo le offerte personalizzate create nel contenitore tenant. Questa operazione viene eseguita eseguendo una richiesta DELETE al [!DNL Offer Library] API utilizzando il $id dell’offerta personalizzata che desideri eliminare.

**Formato API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso dell’endpoint per le API dell’archivio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Il contenitore in cui si trovano le offerte personalizzate. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Richiesta**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/0f4bc230-13df-11eb-bc55-c11be7252432' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Risposta**

In caso di esito positivo, la risposta restituisce lo stato HTTP 202 (nessun contenuto) e un corpo vuoto.

Puoi confermare l’eliminazione tentando una richiesta di ricerca (GET) nell’offerta personalizzata. Dovrai includere un’intestazione Accept nella richiesta, ma dovresti ricevere lo stato HTTP 404 (Non trovato) perché l’offerta personalizzata è stata rimossa dal contenitore.
