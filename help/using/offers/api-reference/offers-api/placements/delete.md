---
title: eliminare i posizionamenti
description: I posizionamenti sono contenitori utilizzati per mostrare le offerte.
feature: Offerte
topic: Integrazioni
role: Data Engineer
level: Experienced
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 6%

---

# Eliminare un posizionamento

A volte può essere necessario rimuovere (DELETE) un posizionamento. È possibile eliminare solo i posizionamenti creati nel contenitore tenant. A tal fine, esegui una richiesta DELETE all’ API [!DNL Offer Library] utilizzando l’ID istanza del posizionamento da eliminare.

**Formato API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API dell&#39;archivio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Il contenitore in cui si trovano i posizionamenti. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | ID istanza del posizionamento da aggiornare. | `9aa58fd0-13d7-11eb-928b-576735ea4db8` |

**Richiesta**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/9aa58fd0-13d7-11eb-928b-576735ea4db8' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Risposta**

Una risposta corretta restituisce lo stato HTTP 202 (nessun contenuto) e un corpo vuoto.

Puoi confermare l’eliminazione tentando una richiesta di ricerca (GET) al posizionamento. Sarà necessario includere un’intestazione Accept nella richiesta, ma dovrebbe ricevere uno stato HTTP 404 (Non trovato) perché il posizionamento è stato rimosso dal contenitore.
