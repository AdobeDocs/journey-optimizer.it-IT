---
title: Elimina qualificatori raccolta
description: I qualificatori di raccolta consentono di organizzare e ordinare meglio le offerte.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 335c1b80-f1f0-4fd0-add8-84b8cc5e2e00
source-git-commit: 835e4bf227ce330b1426a9a4331fdf533fc757e3
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 7%

---

# Eliminare un qualificatore di raccolta {#delete-tag}

A volte può essere necessario rimuovere (DELETE) un qualificatore di raccolta (noto in precedenza come &quot;tag&quot;). È possibile eliminare solo i qualificatori di raccolta creati nel contenitore tenant. A questo scopo, esegui una richiesta DELETE al [!DNL Offer Library] API utilizzando l’ID $del qualificatore di raccolta che desideri eliminare.

**Formato API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API dell&#39;archivio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Il contenitore in cui si trovano i qualificatori della raccolta. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | ID istanza del qualificatore della raccolta che si desidera aggiornare. | `d48fd160-13dc-11eb-bc55-c11be7252432` |

**Richiesta**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/d48fd160-13dc-11eb-bc55-c11be7252432' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Risposta**

Una risposta corretta restituisce lo stato HTTP 202 (nessun contenuto) e un corpo vuoto.

Puoi confermare l’eliminazione tentando una richiesta di ricerca (GET) al qualificatore della raccolta. Sarà necessario includere un’intestazione Accept nella richiesta, ma dovrebbe ricevere uno stato HTTP 404 (Non trovato) perché il qualificatore della raccolta è stato rimosso dal contenitore.
