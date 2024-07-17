---
title: eliminare i posizionamenti
description: I posizionamenti sono contenitori utilizzati per presentare le offerte.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: ca7af3b0-62cd-44ac-8856-b3d1ec15f284
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 9%

---

# Eliminare un posizionamento {#delete-placement}

Occasionalmente può essere necessario rimuovere (DELETE) un posizionamento. Questa operazione viene eseguita eseguendo una richiesta DELETE all&#39;API [!DNL Offer Library] utilizzando l&#39;ID del posizionamento che si desidera eliminare.

**Formato API**

```http
DELETE /{ENDPOINT_PATH}/placements/{ID}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API di persistenza. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | ID istanza del posizionamento da aggiornare. | `offerPlacement1234` |

**Richiesta**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/placements/offerPlacement1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Risposta**

In caso di esito positivo, la risposta restituisce lo stato HTTP 200 e un corpo vuoto.

Puoi confermare l’eliminazione tentando una richiesta di ricerca (GET) al posizionamento e riceverai lo stato HTTP 404 (Non trovato) perché il posizionamento è stato rimosso.
