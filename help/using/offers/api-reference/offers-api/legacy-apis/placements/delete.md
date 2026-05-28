---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: eliminare i posizionamenti
description: I posizionamenti sono contenitori utilizzati per presentare le offerte.
feature: Decision Management, API
badge: label="Legacy" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 944efb12-6745-4bb2-be52-293e23925350
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/gPJcSwy-Z-hondA5knYpiR9OUlHXmSahDHTufmNC7gw
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 164
ht-degree: 17%

---

# Eliminare un posizionamento {#delete-placement}

>[!TIP]
>
>La funzione Decisioni, la nuova funzionalità decisionale di [!DNL Adobe Journey Optimizer], è ora disponibile tramite i canali e-mail e di esperienza basati su codice. [Ulteriori informazioni](../../../../../experience-decisioning/gs-experience-decisioning.md)


A volte può essere necessario rimuovere (DELETE) un posizionamento. È possibile eliminare solo i posizionamenti creati nel contenitore tenant. Questa operazione viene eseguita eseguendo una richiesta DELETE all&#39;API [!DNL Offer Library] utilizzando l&#39;ID istanza del posizionamento che si desidera eliminare.

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
