---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: eliminare i posizionamenti
description: I posizionamenti sono contenitori utilizzati per presentare le offerte.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: ca7af3b0-62cd-44ac-8856-b3d1ec15f284
version: Journey Orchestration
source-git-commit: d6a9a8a392f0492aa6e4f059198ce77b6b2cd962
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 9%

---

# Eliminare un posizionamento {#delete-placement}

A volte può essere necessario rimuovere (DELETE) un posizionamento. Questa operazione viene eseguita eseguendo una richiesta DELETE all&#39;API [!DNL Offer Library] utilizzando l&#39;ID del posizionamento che si desidera eliminare.

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

Puoi confermare l’eliminazione tentando di inviare una richiesta di ricerca (GET) al posizionamento; in caso contrario, riceverai lo stato HTTP 404 (Non trovato) perché il posizionamento è stato rimosso.
