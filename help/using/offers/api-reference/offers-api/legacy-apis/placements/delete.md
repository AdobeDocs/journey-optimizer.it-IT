---
title: eliminare i posizionamenti
description: I posizionamenti sono contenitori utilizzati per presentare le offerte.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: f5372ee271851ffb5aa1f5ff281282c8c474dc2a
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 6%

---


# Eliminare un posizionamento {#delete-placement}

Occasionalmente può essere necessario rimuovere (DELETE) un posizionamento. È possibile eliminare solo i posizionamenti creati nel contenitore tenant. Questa operazione viene eseguita eseguendo una richiesta DELETE al [!DNL Offer Library] API utilizzando l’ID istanza del posizionamento che desideri eliminare.

**Formato API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso dell’endpoint per le API dell’archivio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Il contenitore in cui si trovano i posizionamenti. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | ID istanza del posizionamento da aggiornare. | `9aa58fd0-13d7-11eb-928b-576735ea4db8` |

**Richiesta**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/9aa58fd0-13d7-11eb-928b-576735ea4db8' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Risposta**

In caso di esito positivo, la risposta restituisce lo stato HTTP 202 (nessun contenuto) e un corpo vuoto.

Puoi confermare l’eliminazione tentando di inviare una richiesta di ricerca (GET) al posizionamento. Dovrai includere un’intestazione Accept nella richiesta, ma dovresti ricevere lo stato HTTP 404 (Non trovato) perché il posizionamento è stato rimosso dal contenitore.
