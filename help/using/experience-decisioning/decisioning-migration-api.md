---
title: Decisioning Migration API
description: Scopri come utilizzare l’API del servizio di migrazione Decisioning per migrare gli oggetti di gestione delle decisioni tra sandbox con risoluzione automatizzata delle dipendenze e supporto del rollback.
feature: Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 3ec084ca-af9e-4b5e-b66f-ec390328a9d6
source-git-commit: 1ee6f9d74b83ca2b9c2cc0336af0f23a42f4da4f
workflow-type: tm+mt
source-wordcount: '1143'
ht-degree: 4%

---

# Decisioning Migration API {#decisioning-migration-api}

L’API del servizio di migrazione di Decisioning consente di migrare gli oggetti di gestione delle decisioni da una sandbox all’altra. Il processo di migrazione viene eseguito come flussi di lavoro asincroni che includono l’analisi delle dipendenze, l’esecuzione e le funzionalità di rollback facoltative.

Questa API consente di passare facilmente al contenuto decisionale tra gli ambienti <!--(e.g., from development to staging, or staging to production) -->, mantenendo al contempo l&#39;integrità dei dati e le relazioni.

Per informazioni sui vantaggi e le funzionalità di Decisioning rispetto alla gestione delle decisioni, consulta [questa pagina](migrate-to-decisioning.md).

## Funzionalità {#capabilities}

L’API del servizio di migrazione Decisioning fornisce le seguenti funzionalità:

* **Analisi delle dipendenze** - Identifica tutte le dipendenze necessarie tra le sandbox di origine e di destinazione, inclusi attributi, segmenti e requisiti dei set di dati.
* **Ambito di migrazione flessibile**: esegui migrazioni a livello di sandbox, offerta o decisione in base alle tue esigenze.
* **Supporto rollback** - Ripristina una migrazione completata se vengono rilevati problemi durante la convalida.

## Prerequisiti {#prerequisites}

### Autorizzazioni richieste {#permissions}

Per utilizzare l’API di migrazione, è necessario disporre delle autorizzazioni appropriate sia nella sandbox di origine che in quella di destinazione:

**Sandbox Source** - Accesso in lettura agli oggetti di gestione delle decisioni

**Sandbox di destinazione** - Crea e modifica l&#39;accesso agli oggetti Decisioning

Le autorizzazioni tipiche includono:

* Gestisci/Visualizza decisioni
* Gestisci/Visualizza decisioni
* Gestire le offerte
* Gestire le strategie di classificazione
* Gestire le campagne (se si esegue la migrazione degli artefatti relativi alle campagne)
* Gestire/visualizzare gli stream di dati (se si crea uno stream di dati)
* Gestione/Visualizzazione degli schemi

>[!NOTE]
>
>Scopri come assegnare le autorizzazioni Decisioning in [questa sezione](gs-experience-decisioning.md#steps). Per l&#39;elenco completo delle autorizzazioni, fare riferimento alla pagina [Autorizzazioni incorporate](../administration/ootb-permissions.md#ootb-permissions).

### Preparare la sandbox di destinazione {#target-sandbox-preparation}

Prima di eseguire una migrazione, assicurati che la sandbox di destinazione sia configurata correttamente:

* **Attributi** - Verificare che gli attributi di profilo e gli attributi di contesto richiesti siano presenti nella sandbox di destinazione o preparare le relative mappature.
* **Segmenti** - Assicurati che i segmenti richiesti esistano nella sandbox di destinazione o pianifica di mapparli utilizzando lo spazio dei nomi e l&#39;ID.
* **Set di dati** - Identifica un nome di set di dati da utilizzare per la migrazione (`dependency.datasetName`).
* **Stream di dati** - Decidere se la migrazione deve creare uno stream di dati (`createDataStream`).

Per ulteriori informazioni sulla gestione delle sandbox, consulta [Utilizzare e assegnare le sandbox](../administration/sandboxes.md).

## Nozioni di base sulle API {#api-basics}

### URL di base {#base-url}

Utilizza il seguente URL di base:

* **Produzione**: `https://decisioning-migration.adobe.io`
  <!--* **Staging**: `https://decisioning-migration-stage.adobe.io`-->

### Autenticazione {#authentication}

Tutte le richieste API richiedono le seguenti intestazioni:

* `Authorization: Bearer <IMS_ACCESS_TOKEN>`
* `x-gw-ims-org-id: <IMS_ORG_ID>`
* `Content-Type: application/json`

Per istruzioni dettagliate sulla configurazione dell&#39;autenticazione, fare riferimento alla [guida all&#39;autenticazione di Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}.

### Modello flusso di lavoro {#workflow-model}

Ogni chiamata API crea o recupera una risorsa del flusso di lavoro. I flussi di lavoro sono operazioni asincrone che tengono traccia dell’avanzamento e dei risultati delle attività di migrazione.

Un flusso di lavoro ha le seguenti proprietà:

* `id` - Identificatore univoco del flusso di lavoro (UUID)
* `status` - Stato flusso di lavoro corrente: `New`, `Running`, `Completed` o `Failed`
* `result` - Output del flusso di lavoro al completamento (inclusi i risultati della migrazione e gli avvisi)
* `errors` - Dettagli dell&#39;errore strutturato in caso di errore
* `_links.self` - URL del flusso di lavoro per il recupero dello stato
  <!--* `_etag` - Version identifier used for delete operations (service users only)-->

## Flusso di lavoro di migrazione {#migration-workflow}

Il processo di migrazione consiste in due passaggi principali: analisi delle dipendenze ed esecuzione della migrazione. Per eseguire correttamente la migrazione, segui la procedura riportata di seguito.

### Passaggio 1: Analizzare le dipendenze {#analyze-dependencies}

Prima di eseguire la migrazione, utilizza il flusso di lavoro delle dipendenze per identificare gli elementi da mappare da Gestione decisioni a Decisioning nella sandbox di destinazione. Questa analisi consente di comprendere le relazioni tra gli oggetti e di preparare le mappature necessarie.

#### Creare un flusso di lavoro di dipendenza {#create-dependency-workflow}

Utilizza la seguente chiamata API per creare un flusso di lavoro di analisi delle dipendenze.

**Formato API**

```http
POST /workflows/generate-dependencies
```

**Dipendenza a livello di sandbox (prima consigliata)**

Inizia con un’analisi a livello di sandbox per ottenere una visualizzazione completa di tutte le dipendenze:

```shell
curl --request POST \
  --url "https://decisioning-migration.adobe.io/workflows/generate-dependencies" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "Content-Type: application/json" \
  --data '{
    "imsOrgId": "<IMS_ORG_ID>",
    "sourceSandboxDetails": { "sandboxName": "<SOURCE_SANDBOX_NAME>" },
    "targetSandboxDetails": { "sandboxName": "<TARGET_SANDBOX_NAME>" },
    "requestLevel": "sandbox"
  }'
```

**Dipendenza a livello di offerta**

Per analizzare le dipendenze solo per offerte specifiche, impostare `requestLevel: "offer"` e fornire un array `offersList` con gli ID offerta che si desidera analizzare.

**Dipendenza a livello di decisione**

Per analizzare le dipendenze solo per decisioni specifiche, impostare `requestLevel: "decision"` e fornire un array `decisionsList` con gli ID di decisione che si desidera analizzare.

#### Verifica stato del flusso di lavoro delle dipendenze {#poll-dependency-status}

Esegue il polling del flusso di lavoro delle dipendenze per verificare il completamento dell&#39;analisi.

**Formato API**

```http
GET /workflows/generate-dependencies/{id}
```

**Richiesta**

```shell
curl --request GET \
  --url "https://decisioning-migration.adobe.io/workflows/generate-dependencies/<WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>"
```

Quando il campo `status` mostra `Completed`, l&#39;analisi della dipendenza è pronta. Utilizza l’output del flusso di lavoro per creare i mapping delle dipendenze di migrazione:

* **profileAttributes** - Associa gli attributi del profilo di origine agli attributi del profilo di destinazione
* **contextAttributes** - Associa gli attributi del contesto di origine agli attributi del contesto di destinazione
* **segmenti** - Esegue il mapping delle chiavi del segmento di origine con gli identificatori del segmento di destinazione (`{namespace, id}`)
* **datasetName** - Specifica il nome del set di dati di destinazione per la migrazione

### Passaggio 2: eseguire la migrazione {#execute-migration}

Dopo aver analizzato le dipendenze e preparato le mappature, puoi eseguire la migrazione.

#### Creare un flusso di lavoro di migrazione {#create-migration-workflow}

Utilizza i mapping delle dipendenze dal passaggio 1 per configurare ed eseguire la migrazione.

**Formato API**

```http
POST /workflows/migration
```

**Migrazione a livello di sandbox**

Per migrare tutti gli oggetti decisioning da una sandbox all’altra:

```shell
curl --request POST \
  --url "https://decisioning-migration.adobe.io/workflows/migration" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "Content-Type: application/json" \
  --data '{
    "imsOrgId": "<IMS_ORG_ID>",
    "sourceSandboxDetails": { "sandboxName": "<SOURCE_SANDBOX_NAME>" },
    "targetSandboxDetails": { "sandboxName": "<TARGET_SANDBOX_NAME>" },
    "createDataStream": true,
    "dependency": {
      "profileAttributes": {
        "sourceAttr1": "targetAttr1"
      },
      "segments": {
        "sourceSegmentKey1": {
          "namespace": "<TARGET_SEGMENT_NAMESPACE>",
          "id": "<TARGET_SEGMENT_ID>"
        }
      },
      "contextAttributes": {
        "sourceCtx1": "targetCtx1"
      },
      "datasetName": "<TARGET_DATASET_NAME>"
    },
    "requestLevel": "sandbox"
  }'
```

**Migrazione a livello di offerta**

Per migrare solo offerte specifiche, utilizzare `requestLevel: "offer"` e aggiungere un array `offersList`:

```json
"offersList": ["offer-id-1", "offer-id-2"]
```

**Decision-level migration**

To migrate specific decisions only, use `requestLevel: "decision"` and add a `decisionsList` array:

```json
"decisionsList": ["decision-id-1", "decision-id-2"]
```

#### Monitor migration status {#poll-migration-status}

Poll the migration workflow to track its progress.

**Formato API**

```http
GET /workflows/migration/{id}
```

**Richiesta**

```shell
curl --request GET \
  --url "https://decisioning-migration.adobe.io/workflows/migration/<WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>"
```

**Migration results**

When the `status` field shows `Completed`, the migration was successful. The workflow `result` includes:
* Mappings of migrated objects
* Any warnings encountered during migration

When the `status` field shows `Failed`, review the `errors[]` array and `result.error` field for details about what went wrong.

## Validate your migration {#validate-migration}

After the migration completes successfully, verify that all objects were migrated correctly.

### Validation checklist {#validation-checklist}

1. **Segments** - Verify that all referenced segments resolve correctly in the target sandbox according to your mappings.
2. **Attributes** - Confirm that all profile attributes and context attributes exist in the target sandbox and are mapped correctly.
3. **Decisioning objects** - Review migrated objects in the Journey Optimizer user interface:
   * Offers (decision items)
   * Regole di idoneità
   * Formule di ranking
   * Strategie di selezione
   * Decision policies
4. **Datastream testing** - If a datastream was created, test runtime delivery using the Edge Interact API.

### Esempio {#test-runtime-delivery}

If your migration created a datastream, you can test offer delivery using the following example:

```shell
curl --request POST \
  --url "https://edge.adobedc.net/ee/or2/v1/interact?configId=<DATASTREAM_ID>" \
  --header "Content-Type: application/json" \
  --header "x-request-id: <uuid>" \
  --data '{ "events": [ ... ] }'
```

## Rollback a migration {#rollback}

If you discover issues during validation, you can roll back a completed migration to restore the target sandbox to its previous state.

### Create a rollback workflow {#create-rollback-workflow}

Initiate a rollback by creating a rollback workflow that references the migration you want to revert.

**Formato API**

```http
POST /workflows/rollback
```

**Richiesta**

```shell
curl --request POST \
  --url "https://decisioning-migration.adobe.io/workflows/rollback" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "Content-Type: application/json" \
  --data '{ "rollbackWorkflowId": "<MIGRATION_WORKFLOW_ID>" }'
```

Replace `<MIGRATION_WORKFLOW_ID>` with the ID of the migration workflow you want to roll back.

### Monitor rollback status {#poll-rollback-status}

Poll the rollback workflow to track its progress.

**Formato API**

```http
GET /workflows/rollback/{rollbackWorkflowId}
```

**Richiesta**

```shell
curl --request GET \
  --url "https://decisioning-migration.adobe.io/workflows/rollback/<ROLLBACK_WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>"
```

## Handle concurrent workflows {#handle-concurrency}

The Migration API allows only one workflow to run at a time per organization. If you attempt to create a new workflow while another is in progress, you will receive a **409 Conflict** error response (&quot;A workflow is already in progress...&quot;).

In this case, wait for the in-progress workflow to complete, or retrieve the workflow ID and poll its status. Once the current workflow finishes, you can create a new one.

## Entity mapping reference {#entity-mapping}

When migrating from Decision management to Decisioning, entities are mapped as follows:

| Gestione delle decisioni | Funzione Decisioni |
|-------------------|-------------|
| Nome | Decision item |
| Raccolta di offerte | Item collection |
| Eligibility rule | Eligibility rule |
| Ranking formula | Ranking formula |
| Decisione | Selection strategy + Decision policy |
| Campaign | Campaign *(basic content only)* |
| Posizionamento | Surface + Channel configuration |
| Tag | Unified tag |
| Attributi di offerta | `migratedofferattributes` field in the Personalized offer item schema |
| Context attributes | `migratedcontextattributes` field in the schema attached to the dataset provided during migration |

## Workflow cleanup {#cleanup}

<!--
Workflow resources can be deleted by service users only. Delete operations require an `If-Match` header with the workflow's `_etag` value.

**Available delete operations:**

* `DELETE /workflows/generate-dependencies/{id}`
* `DELETE /workflows/migration/{id}`
* `DELETE /workflows/rollback/{id}`
-->

Workflow deletion is not publicly available. If you need to delete a workflow resource, contact your system administrator.

## Argomenti correlati {#related-topics}

* [Migrare da Gestione decisioni a Decisioning](migrate-to-decisioning.md) - Comprendere i vantaggi e le funzionalità della migrazione a Decisioning
* [Introduzione alla funzione Decisioni](gs-experience-decisioning.md)
* [Guardrail e limitazioni decisionali](decisioning-guardrails.md)
* [Introduzione alle API Decisioning](api-reference/getting-started.md)
