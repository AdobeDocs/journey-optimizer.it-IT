---
title: Elimina decisioni
description: Una decisione contiene la logica su cui si basa la selezione di un’offerta.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 1eb19ff1-b210-4891-ab41-5488e2635527
source-git-commit: ccc3ad2b186a64b9859a5cc529fe0aefa736fc00
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 7%

---

# Eliminare una decisione {#delete-decision}

Occasionalmente può essere necessario revocare (DELETE) una decisione. È possibile eliminare solo le decisioni create nel contenitore tenant. Questa operazione viene eseguita eseguendo una richiesta DELETE al [!DNL Offer Library] API utilizzando il $id dell’offerta di fallback che desideri eliminare.

**Formato API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso dell’endpoint per le API dell’archivio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Il contenitore in cui si trovano le decisioni. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | ID istanza della decisione. | `f88c9be0-1245-11eb-8622-b77b60702882` |

**Richiesta**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/f88c9be0-1245-11eb-8622-b77b60702882' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Risposta**

In caso di esito positivo, la risposta restituisce lo stato HTTP 202 (nessun contenuto) e un corpo vuoto.

Puoi confermare l’eliminazione tentando una richiesta di ricerca (GET) alla decisione. Dovrai includere un’intestazione Accept nella richiesta, ma dovresti ricevere lo stato HTTP 404 (Non trovato) perché la decisione è stata rimossa dal contenitore.
