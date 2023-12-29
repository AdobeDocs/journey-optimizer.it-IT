---
title: Elimina qualificatori raccolta
description: I qualificatori di raccolta ti consentono di organizzare e ordinare meglio le offerte.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 335c1b80-f1f0-4fd0-add8-84b8cc5e2e00
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 6%

---


# Eliminare un qualificatore di raccolta {#delete-tag}

A volte può essere necessario rimuovere (DELETE) un qualificatore di raccolta (precedentemente noto come &quot;tag&quot;). È possibile eliminare solo i qualificatori di raccolta creati nel contenitore tenant. Questa operazione viene eseguita eseguendo una richiesta DELETE al [!DNL Offer Library] tramite l&#39;API $id del qualificatore di raccolta che desideri eliminare.

**Formato API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso dell’endpoint per le API dell’archivio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Contenitore in cui si trovano i qualificatori di raccolta. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | ID istanza del qualificatore di raccolta da aggiornare. | `d48fd160-13dc-11eb-bc55-c11be7252432` |

**Richiesta**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/d48fd160-13dc-11eb-bc55-c11be7252432' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Risposta**

In caso di esito positivo, la risposta restituisce lo stato HTTP 202 (nessun contenuto) e un corpo vuoto.

Puoi confermare l’eliminazione tentando una richiesta di ricerca (GET) nel qualificatore della raccolta. Dovrai includere un’intestazione Accept nella richiesta, ma dovresti ricevere lo stato HTTP 404 (Non trovato) perché il qualificatore di raccolta è stato rimosso dal contenitore.