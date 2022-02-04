---
title: Elimina decisioni
description: Una decisione contiene la logica che informa la selezione di un’offerta.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 1eb19ff1-b210-4891-ab41-5488e2635527
source-git-commit: 9873af4caf7cd8bc4e9672748414bf78f28ed30b
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 6%

---

# Eliminare una decisione {#delete-decision}

A volte può essere necessario rimuovere (DELETE) una decisione (precedentemente nota come attività di offerta). È possibile eliminare solo le decisioni create nel contenitore tenant. A questo scopo, esegui una richiesta DELETE al [!DNL Offer Library] API utilizzando l’ID $dell’offerta di fallback che desideri eliminare.

**Formato API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API dell&#39;archivio. | `https://platform.adobe.io/data/core/xcore/` |
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

Una risposta corretta restituisce lo stato HTTP 202 (nessun contenuto) e un corpo vuoto.

Puoi confermare l’eliminazione tentando una richiesta di ricerca (GET) alla decisione. Sarà necessario includere un’intestazione Accept nella richiesta, ma dovrebbe ricevere uno stato HTTP 404 (Non trovato) perché la decisione è stata rimossa dal contenitore.
