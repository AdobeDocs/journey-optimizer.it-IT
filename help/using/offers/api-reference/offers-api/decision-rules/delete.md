---
title: Elimina regole decisionali
description: Le regole decisionali sono vincoli aggiunti a un’offerta personalizzata e applicati a un profilo per determinare l’idoneità.
feature: Offerte
topic: Integrazioni
role: Data Engineer
level: Experienced
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 6%

---

# Eliminare una regola di decisione

A volte può essere necessario rimuovere (DELETE) una regola decisionale. È possibile eliminare solo le regole decisionali create nel contenitore tenant. A tal fine, esegui una richiesta DELETE all’ API [!DNL Offer Library] utilizzando l’ID di istanza della regola decisionale che desideri eliminare.

**Formato API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API dell&#39;archivio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Il contenitore in cui si trovano le regole di decisione. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | ID istanza della regola decisionale che si desidera aggiornare. | `eaa5af90-13d9-11eb-9472-194dee6dc381` |

**Richiesta**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/eaa5af90-13d9-11eb-9472-194dee6dc381' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Risposta**

Una risposta corretta restituisce lo stato HTTP 202 (nessun contenuto) e un corpo vuoto.

Puoi confermare l’eliminazione tentando una richiesta di ricerca (GET) alla regola decisionale. Sarà necessario includere un’intestazione Accept nella richiesta, ma dovrebbe ricevere uno stato HTTP 404 (Non trovato) perché la regola decisionale è stata rimossa dal contenitore.
