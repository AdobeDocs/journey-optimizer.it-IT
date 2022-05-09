---
title: API Batch Decisioning
description: Scopri come utilizzare l’API Batch Decisioning per selezionare le migliori offerte per i profili segmentati all’interno di un ambito decisionale predefinito.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 1ed01a6b-5e42-47c8-a436-bdb388f50b4e
source-git-commit: 79d3bd42c208d38aaebce742e70b247106c21587
workflow-type: tm+mt
source-wordcount: '856'
ht-degree: 3%

---


# Consegnare offerte utilizzando [!DNL Batch Decisioning] API {#deliver-offers-batch}

La [!DNL Batch Decisioning] L’API consente alle organizzazioni di utilizzare la funzionalità di offer decisioning per tutti i profili in un dato segmento in una chiamata. Il contenuto dell’offerta per ogni profilo del segmento viene inserito in un set di dati Adobe Experience Platform, dove è disponibile per flussi di lavoro batch personalizzati.

Con la [!DNL Batch Decisioning] API, puoi compilare un set di dati con le migliori offerte per tutti i profili in un segmento Adobe Experience Platform per gli ambiti decisionali. Ad esempio, un&#39;organizzazione può voler eseguire [!DNL Batch Decisioning] in modo da poter inviare offerte a un fornitore di consegna messaggi. Tali offerte vengono quindi utilizzate come contenuto inviato per la consegna di messaggi batch allo stesso segmento di utenti.

A tal fine, l&#39;organizzazione:

* Esegui il [!DNL Batch Decisioning] API, che contiene due richieste:

   1. A **Richiesta Batch POST** per avviare un carico di lavoro per elaborare in batch le selezioni delle offerte.

   2. A **Richiesta di GET batch** per ottenere lo stato del carico di lavoro batch.

* Esporta il set di dati nell’API del fornitore della consegna dei messaggi.

<!-- (Refer to the [export jobs endpoint documentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/export-jobs.html?lang=en) to learn more about exporting segments.) -->

## Introduzione {#getting-started}

Prima di utilizzare questa API, assicurati di completare i seguenti passaggi prerequisiti.

### Preparare la decisione {#prepare-decision}

Segui i passaggi seguenti per preparare una o più decisioni:

* Per esportare il risultato della decisione, crea un set di dati utilizzando lo schema &quot;ODE DecisionEvents&quot;.

* Crea un segmento di Platform da valutare e quindi aggiornare. Fai riferimento a [documentazione sulla segmentazione](http://www.adobe.com/go/segmentation-overview-en) per ulteriori informazioni su come aggiornare la valutazione dell’appartenenza al segmento.

* Crea una decisione (che ha un ambito decisionale costituito da un ID decisione e un ID posizionamento) in Adobe Journey Optimizer. Fai riferimento a [sezione sulla definizione degli ambiti decisionali](../../offer-activities/create-offer-activities.md) della guida sulla creazione di decisioni per saperne di più.

### Requisiti API {#api-requirements}

Tutto [!DNL Batch Decisioning] le richieste richiedono le seguenti intestazioni oltre a quelle di cui al [Guida per gli sviluppatori API per la gestione delle decisioni](../getting-started.md):

* `Content-Type`: `application/json`
* `x-request-id`: Una stringa univoca che identifica la richiesta.
* `x-sandbox-name`: Nome della sandbox.
* `x-sandbox-id`: ID sandbox.

## Avviare un processo batch {#start-a-batch-process}

Per avviare un carico di lavoro per l&#39;elaborazione in batch delle decisioni, inviare una richiesta POST `/workloads/decisions` punto finale.

**Formato API**

```https
POST {ENDPOINT_PATH}/{CONTAINER_ID}/workloads/decisions
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API dell&#39;archivio. | `https://platform.adobe.io/data/core/ode` |
| `{CONTAINER_ID}` | Il contenitore in cui si trovano le decisioni. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Richiesta**

```shell
curl -X POST 'https://platform.adobe.io/data/core/ode/0948b1c5-fff8-3b76-ba17-909c6b93b5a2/workloads/decisions' \
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
| `xdm:segmentIds` | Il valore è una matrice che contiene l’identificatore univoco del segmento. Può contenere un solo valore. | `609028e4-e66c-4776-b0d9-c782887e2273` |
| `xdm:dataSetId` | Il dataSet di output in cui è possibile scrivere gli eventi decisionali. | `6196b4a1a63bd118dafe093c` |
| `xdm:propositionRequests` | Un wrapper contenente il `placementId` e `activityId` |  |
| `xdm:activityId` | Identificatore univoco della decisione. | `xcore:offer-activity:1410cdcda196707b` |
| `xdm:placementId` | Identificatore di posizionamento univoco. | `xcore:offer-placement:1410c4117306488a` |
| `xdm:itemCount` | Si tratta di un campo facoltativo che mostra il numero di elementi, ad esempio le opzioni richieste per l&#39;ambito decisionale. Per impostazione predefinita, l’API restituisce un’opzione per ambito, ma puoi chiedere esplicitamente più opzioni specificando questo campo. È possibile richiedere un minimo di 1 e un massimo di 30 opzioni per ambito. | `1` |
| `xdm:includeContent` | Questo è un campo facoltativo ed è `false` per impostazione predefinita. Se `true`, il contenuto dell’offerta è incluso negli eventi decisionali del set di dati. | `false` |

Fai riferimento a [Documentazione di Gestione delle decisioni](../../get-started/starting-offer-decisioning.md) per una panoramica dei concetti e delle proprietà principali.

**Risposta**

```json
{
    "@id": "47efef25-4bcf-404f-96e2-67c4f784a1f5",
    "xdm:imsOrgId": "9GTO98D5F@AdobeOrg",
    "xdm:containerId": "0948b1c5-fff8-3b76-ba17-909c6b93b5a2",
    "ode:createDate": 1648078924834,
    "ode:status": "QUEUED"
}
```

| Proprietà | Descrizione | Esempio |
| -------- | ----------- | ------- |
| `@id` | UUID generato dall&#39;Offer decisioning che identifica un singolo carico di lavoro. | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | ID organizzazione. | `9GTO98D5F@AdobeOrg` |
| `xdm:containerId` | ID del contenitore. | `0948b1c5-fff8-3b76-ba17-909c6b93b5a2` |
| `ode:createDate` | Data di creazione della richiesta del carico di lavoro della decisione. | `1648078924834` |
| `ode:status` | Stato del carico di lavoro. | `ode:status: "QUEUED"` |

## Recupera informazioni su una decisione batch {#retrieve-information-on-a-batch-decision}

Per recuperare informazioni su una decisione specifica, invia una richiesta GET al `/workloads/decisions` endpoint fornendo il valore ID del carico di lavoro corrispondente per la decisione.

**Formato API**

```https
GET  {ENDPOINT_PATH}/{CONTAINER_ID}/workloads/decisions/{WORKLOAD_ID}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API dell&#39;archivio. | `https://platform.adobe.io/data/core/ode` |
| `{CONTAINER_ID}` | Il contenitore in cui si trovano le decisioni. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{WORKLOAD_ID}` | UUID generato dall&#39;Offer decisioning che identifica un singolo carico di lavoro. | `47efef25-4bcf-404f-96e2-67c4f784a1f5` |

**Richiesta**

```shell
curl -X GET 'https://platform.adobe.io/data/core/ode/0948b1c5-fff8-3b76-ba17-909c6b93b5a2/workloads/decisions/f395ab1f-dfaf-48d4-84c9-199ad6354591' \
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
    "xdm:containerId": "0948b1c5-fff8-3b76-ba17-909c6b93b5a2",
    "ode:createDate": 1648076994405,
    "ode:status": "COMPLETED"
}
```

| Proprietà | Descrizione | Esempio |
| -------- | ----------- | ------- |
| `@id` | UUID generato dall&#39;Offer decisioning che identifica un singolo carico di lavoro. | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | ID organizzazione | `9GTO98D5F@AdobeOrg` |
| `xdm:containerId` | ID contenitore | `0948b1c5-fff8-3b76-ba17-909c6b93b5a2` |
| `ode:createDate` | Data e ora di creazione della richiesta di carico di lavoro della decisione. | `1648076994405` |
| `ode:status` | Lo stato del carico di lavoro inizia con &quot;QUEUED&quot; e cambia in &quot;PROCESSING&quot;, &quot;INGESTING&quot;, &quot;COMPLETED&quot; o &quot;ERROR&quot;. | `ode:status: "COMPLETED"` |
| `ode:statusDetail` | Questo mostra ulteriori dettagli come sparkJobId e batchID se lo stato è &quot;PROCESSING&quot; o &quot;INGESTING&quot;. Mostra i dettagli dell&#39;errore se lo stato è &quot;ERROR&quot;. |  |

## Livelli di servizio {#service-levels}

Il tempo end-to-end per ogni decisione batch è la durata dal momento in cui il carico di lavoro viene creato al momento in cui il risultato della decisione è disponibile nel set di dati di output. La dimensione del segmento nel payload della richiesta POST è il fattore principale che influisce sul tempo di decisione del batch end-to-end.  Di seguito sono riportate alcune osservazioni per diverse dimensioni di segmento:

| Dimensione del segmento | Tempo di elaborazione end-to-end |
|--------------|----------------------------|
| 10 mila profili o meno | 6 minuti |
| 1 milione di profili o meno | 10 minuti |
| 15 milioni di profili o meno | 75 minuti |

## Limitazioni  {#limitations}

Quando utilizzi [!DNL Batch Decisioning] Tieni presente le seguenti limitazioni:

* **Processo batch singolo per set di dati**: Attualmente, è possibile eseguire un solo processo batch alla volta per ogni set di dati. Qualsiasi altra richiesta con lo stesso set di dati di output risponderebbe con HTTP 429 (Troppe richieste) prima del termine della richiesta precedente.
* **Limite di frequenza**: Un batch esegue lo snapshot del profilo che si verifica una volta al giorno. La [!DNL Batch Decisioning] L’API limita la frequenza e carica sempre i profili dallo snapshot più recente.

## Passaggi successivi {#next-steps}

Seguendo questa guida API, hai controllato lo stato del carico di lavoro e hai consegnato le offerte utilizzando [!DNL [!DNL Batch Decisioning]] API. Per ulteriori informazioni, consulta la sezione [Panoramica sulla gestione delle decisioni](../../get-started/starting-offer-decisioning.md).
