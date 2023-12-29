---
title: Eliminare le regole di decisione
description: Le regole di decisione sono vincoli aggiunti a un’offerta personalizzata e applicati a un profilo per determinare l’idoneità.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 52f4803b-9e9a-4ad0-ae24-de652006763d
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 9%

---

# Eliminare una regola di decisione {#delete-decision-rule}

Occasionalmente può essere necessario rimuovere (DELETE) una regola di decisione. Questa operazione viene eseguita eseguendo una richiesta DELETE al [!DNL Offer Library] API tramite `id` della regola di decisione che desideri eliminare.

**Formato API**

```http
DELETE /{ENDPOINT_PATH}/offer-rules/{ID}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API di persistenza. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | ID dell’entità da eliminare. | `offerRule1234` |

**Richiesta**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-rules/offerRule1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Risposta**

In caso di esito positivo, la risposta restituisce lo stato HTTP 200 e un corpo vuoto.

Puoi confermare l’eliminazione tentando una richiesta di ricerca (GET) alla regola di decisione e dovresti ricevere lo stato HTTP 404 (Non trovato) perché la regola di decisione è stata rimossa.
