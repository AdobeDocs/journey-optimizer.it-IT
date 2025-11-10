---
title: API Batch Decisioning
description: Scopri come utilizzare l’API Batch Decisioning per selezionare le offerte migliori per i profili di pubblico all’interno di un ambito decisionale predefinito.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 1ed01a6b-5e42-47c8-a436-bdb388f50b4e
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 4%

---


# Consegnare offerte tramite l&#39;API [!DNL Batch Decisioning] {#deliver-offers-batch}

L&#39;API [!DNL Batch Decisioning] consente alle organizzazioni di utilizzare la funzionalità di decisioning per tutti i profili in un determinato pubblico in una chiamata. Il contenuto dell’offerta per ogni profilo del pubblico viene inserito in un set di dati Adobe Experience Platform dove è disponibile per flussi di lavoro batch personalizzati.

Con l&#39;API [!DNL Batch Decisioning], puoi popolare un set di dati con le offerte migliori per tutti i profili in un pubblico Adobe Experience Platform per ambiti decisionali. Ad esempio, un&#39;organizzazione potrebbe voler eseguire [!DNL Batch Decisioning] in modo da poter inviare offerte a un fornitore di recapito messaggi. Tali offerte vengono quindi utilizzate come contenuto inviato per la consegna di messaggi in batch allo stesso pubblico di utenti.

A tal fine, l’organizzazione:

* Eseguire l&#39;API [!DNL Batch Decisioning], che contiene due richieste:

   1. **Richiesta POST batch** per avviare un carico di lavoro per elaborare in batch le selezioni delle offerte.

   2. **Richiesta batch di GET** per ottenere lo stato del carico di lavoro batch.

* Esporta il set di dati nell’API del fornitore per la consegna dei messaggi.

<!-- (Refer to the [export jobs endpoint documentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/export-jobs.html) to learn more about exporting audiences.) -->

>[!NOTE]
>
>Le decisioni in batch possono essere eseguite anche utilizzando l’interfaccia di Journey Optimizer. Per ulteriori informazioni, consulta [questa sezione](../../batch-delivery.md), che fornisce informazioni sui prerequisiti e le limitazioni globali da tenere in considerazione durante l&#39;utilizzo delle decisioni batch.

* **Numero di processi batch in esecuzione per set di dati**: è possibile eseguire fino a cinque processi batch alla volta per set di dati. Eventuali altre richieste batch con lo stesso set di dati di output vengono aggiunte alla coda. Un processo in coda viene selezionato per l&#39;elaborazione al termine dell&#39;esecuzione del processo precedente.
* **Limitazione della frequenza**: viene eseguito un batch dello snapshot del profilo che si verifica una volta al giorno. L&#39;API [!DNL Batch Decisioning] limita la frequenza e carica sempre i profili dallo snapshot più recente.

## Introduzione {#getting-started}

Prima di utilizzare questa API, assicurati di completare i seguenti passaggi preliminari richiesti.

### Preparare la decisione {#prepare-decision}

Per preparare una o più decisioni, assicurati di aver creato un set di dati, un pubblico e una decisione. Tali prerequisiti sono descritti in [questa sezione](../../batch-delivery.md).

### Requisiti API {#api-requirements}

Tutte le [!DNL Batch Decisioning] richieste richiedono le intestazioni seguenti oltre a quelle indicate nella [Guida per gli sviluppatori API per la gestione delle decisioni](../getting-started.md):

* `Content-Type`: `application/json`
* `x-request-id`: stringa univoca che identifica la richiesta.
* `x-sandbox-name`: nome della sandbox.

## Avviare un processo batch {#start-a-batch-process}

Per avviare un carico di lavoro per elaborare in batch le decisioni, effettuare una richiesta POST all&#39;endpoint `/workloads/decisions`.

>[!NOTE]
>
>Informazioni dettagliate sui tempi di elaborazione dei processi batch sono disponibili in [questa sezione](../../batch-delivery.md).

**Formato API**

```https
POST {ENDPOINT_PATH}/workloads/decisions
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso dell’endpoint per le API dell’archivio. | `https://platform.adobe.io/data/core/dwm` |

**Richiesta**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dwm/workloads/decisions' \
-H 'x-request-id: f671a589-eb7b-432f-b6b9-23d5b796b4dc' \
-H 'Content-Type: application/json' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-sandbox-id: {SANDBOX_ID}' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-d '{
  "xdm:segmentIds": [
    "609028e4-e66c-4776-b0d9-c782887e2273"
  ],
  "xdm:dataSetId": "6196b4a1a63bd118dafe093c",
  "xdm:propositionRequests": [
        {
            "xdm:activityId": "xcore:offer-activity:1410cdcda196707b",
            "xdm:placementId": "xcore:offer-placement:1410c4117306488a",
            "xdm:itemCount": 1
        }
  ],
  "xdm:includeContent": false
}'
```

| Proprietà | Descrizione | Esempio |
| -------- | ----------- | ------- |
| `xdm:activityId` | L’identificatore univoco della decisione. |  |
| `xdm:dataSetId` | Il set di dati di output in cui è possibile scrivere gli eventi di decisione. | `6196b4a1a63bd118dafe093c` |
| `xdm:includeContent` | Questo è un campo facoltativo ed è `false` per impostazione predefinita. Se `true`, il contenuto dell&#39;offerta viene incluso negli eventi di decisione del set di dati. | `false` |
| `xdm:itemCount` | Questo è un campo facoltativo che mostra il numero di elementi, ad esempio le opzioni richieste per l’ambito decisionale. Per impostazione predefinita, l’API restituisce un’opzione per ambito, ma è possibile richiedere esplicitamente più opzioni specificando questo campo. È possibile richiedere un minimo di 1 e un massimo di 30 opzioni per ambito. | `xcore:offer-activity:1410cdcda196707b` |
| `xdm:placementId` | L’identificatore di posizionamento univoco. | `xcore:offer-placement:1410c4117306488a` |
| `xdm:propositionRequests` | Un wrapper contenente `placementId` e `activityId` |  |
| `xdm:segmentIds` | Il valore è un array che contiene l’identificatore univoco del pubblico. Può contenere un solo valore. | `609028e4-e66c-4776-b0d9-c782887e2273` |

Per una panoramica dei concetti e delle proprietà principali, consulta la [documentazione sulla gestione delle decisioni](../../get-started/starting-offer-decisioning.md).

**Risposta**

```json
{
    "@id": "47efef25-4bcf-404f-96e2-67c4f784a1f5",
    "xdm:imsOrgId": "9GTO98D5F@AdobeOrg",
    "ode:createDate": 1648078924834,
    "ode:status": "QUEUED"
}
```

| Proprietà | Descrizione | Esempio |
| -------- | ----------- | ------- |
| `@id` | L’UUID generato dalla gestione delle decisioni che identifica un singolo carico di lavoro. | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | L’ID organizzazione. | `9GTO98D5F@AdobeOrg` |
| `ode:createDate` | L’ora in cui è stata creata la richiesta del carico di lavoro di decisione. | `1648078924834` |
| `ode:status` | Stato del carico di lavoro. | `ode:status: "QUEUED"` |

## Recuperare informazioni su una decisione batch {#retrieve-information-on-a-batch-decision}

Per recuperare informazioni su una decisione specifica, effettua una richiesta GET all&#39;endpoint `/workloads/decisions` fornendo il valore ID del carico di lavoro corrispondente per la decisione.

**Formato API**

```https
GET {ENDPOINT_PATH}/workloads/decisions/{WORKLOAD_ID}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso dell’endpoint per le API dell’archivio. | `https://platform.adobe.io/data/core/dwm` |
| `{WORKLOAD_ID}` | L’UUID generato dalla gestione delle decisioni che identifica un singolo carico di lavoro. | `47efef25-4bcf-404f-96e2-67c4f784a1f5` |

**Richiesta**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dwm/workloads/decisions/f395ab1f-dfaf-48d4-84c9-199ad6354591' \
-H 'x-request-id: 7832a42a-d4e5-413b-98e8-e49bef056436' \
-H 'Content-Type: application/json' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H'x-sandbox-id: {SANDBOX_ID}' \
-H 'Authorization: Bearer {ACCESS_TOKEN}'
```

**Risposta**

```json
{
   "@id": "f395ab1f-dfaf-48d4-84c9-199ad6354591",
    "xdm:imsOrgId": "{IMS_ORG}",
    "ode:createDate": 1648076994405,
    "ode:status": "COMPLETED"
}
```

| Proprietà | Descrizione | Esempio |
| -------- | ----------- | ------- |
| `@id` | L’UUID generato dalla gestione delle decisioni che identifica un singolo carico di lavoro. | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | ID organizzazione | `9GTO98D5F@AdobeOrg` |
| `ode:createDate` | Ora di creazione della richiesta del carico di lavoro delle decisioni. | `1648076994405` |
| `ode:status` | Lo stato del carico di lavoro inizia con &quot;QUEUED&quot; (IN CODA) e cambia in &quot;PROCESSING&quot; (ELABORAZIONE), &quot;INGESTING&quot; (ACQUISIZIONE), &quot;COMPLETED&quot; (COMPLETATO) o &quot;ERROR&quot; (ERRORE). | `ode:status: "COMPLETED"` |
| `ode:statusDetail` | Mostra altri dettagli come sparkJobId e batchID se lo stato è &quot;PROCESSING&quot; o &quot;INGESTING&quot;. Mostra i dettagli dell’errore se lo stato è &quot;ERROR&quot;. |  |

## Passaggi successivi {#next-steps}

Seguendo questa guida API, hai controllato lo stato del carico di lavoro e hai consegnato le offerte utilizzando l’API [!DNL [!DNL Batch Decisioning]]. Per ulteriori informazioni, consulta la [panoramica sulla gestione delle decisioni](../../get-started/starting-offer-decisioning.md).
