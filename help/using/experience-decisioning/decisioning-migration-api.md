---
title: Decisioning Migration API
description: Scopri come utilizzare l’API del servizio di migrazione Decisioning per migrare gli oggetti di gestione delle decisioni tra sandbox con risoluzione automatizzata delle dipendenze e supporto del rollback.
feature: Decisioning
topic: Integrations
role: Developer
level: Experienced
source-git-commit: 9ac3eaba0b4c6536c1c447df825eb5f5c0afc900
workflow-type: tm+mt
source-wordcount: '1157'
ht-degree: 4%

---


# Decisioning Migration API {#decisioning-migration-api}

L’API del servizio di migrazione di Decisioning consente di migrare gli oggetti di gestione delle decisioni da una sandbox all’altra. Il processo di migrazione viene eseguito come flussi di lavoro asincroni che includono l’analisi delle dipendenze, l’esecuzione e le funzionalità di rollback facoltative.

Questa API consente di passare facilmente al contenuto decisionale tra ambienti diversi (ad esempio, da sviluppo a staging o da staging a produzione), mantenendo al contempo l’integrità e le relazioni tra i dati.

Per informazioni sui vantaggi e le funzionalità di Decisioning rispetto alla gestione delle decisioni, consulta [Vantaggi della migrazione a Decisioning](migrate-to-decisioning.md).

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

### URL di base {#base-urls}

Utilizza i seguenti URL di base a seconda dell’ambiente:

* **Produzione**: `https://platform.adobe.io`
* **Gestione temporanea**: `https://platform-stage.adobe.io`

### Autenticazione {#authentication}

Tutte le richieste API richiedono le seguenti intestazioni:

* `Authorization: Bearer <IMS_ACCESS_TOKEN>`
* `x-gw-ims-org-id: <IMS_ORG_ID>`
* `x-api-key: <CLIENT_API_KEY>`
* `Content-Type: application/json`

Per istruzioni dettagliate sulla configurazione dell&#39;autenticazione, fare riferimento alla [guida all&#39;autenticazione di Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}.

### Modello flusso di lavoro {#workflow-model}

Ogni chiamata API crea o recupera una risorsa del flusso di lavoro. I flussi di lavoro sono operazioni asincrone che tengono traccia dell’avanzamento e dei risultati delle attività di migrazione.

Un flusso di lavoro ha le seguenti proprietà:

* `id` - Identificatore univoco del flusso di lavoro (UUID)
* `status` - Stato flusso di lavoro corrente: `New`, `Running`, `Completed`, `Failed` o `Cancelled`
* `result` - Output del flusso di lavoro al completamento (inclusi i risultati della migrazione e gli avvisi)
* `errors` - Dettagli dell&#39;errore strutturato in caso di errore
* `_etag` - Identificatore di versione utilizzato per le operazioni di eliminazione (solo per gli utenti del servizio)
* `_links.self` - URL del flusso di lavoro per il recupero dello stato

## Flusso di lavoro di migrazione {#migration-workflow}

Il processo di migrazione consiste in due passaggi principali: analisi delle dipendenze ed esecuzione della migrazione. Per eseguire correttamente la migrazione, segui la procedura riportata di seguito.

### Passaggio 1: Analizzare le dipendenze {#analyze-dependencies}

Prima di eseguire la migrazione, utilizza il flusso di lavoro delle dipendenze per identificare gli elementi da mappare da Gestione decisioni a Decisioning nella sandbox di destinazione. Questa analisi consente di comprendere le relazioni tra gli oggetti e di preparare le mappature necessarie.

#### Creare un flusso di lavoro di dipendenza {#create-dependency-workflow}

Utilizza la seguente chiamata API per creare un flusso di lavoro di analisi delle dipendenze.

**Formato API**

```http
POST /migration/service/dependency
```

**Dipendenza a livello di sandbox (prima consigliata)**

Inizia con un’analisi a livello di sandbox per ottenere una visualizzazione completa di tutte le dipendenze:

```shell
curl --request POST \
  --url "https://platform.adobe.io/migration/service/dependency" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>" \
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
GET /migration/service/dependency/{id}
```

**Richiesta**

```shell
curl --request GET \
  --url "https://platform.adobe.io/migration/service/dependency/<WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>"
```

Quando il campo `status` mostra `Completed`, l&#39;analisi della dipendenza è pronta. Utilizza l’output del flusso di lavoro per creare i mapping delle dipendenze di migrazione:

* **profileAttributeDependency** - Associa gli attributi del profilo di origine agli attributi del profilo di destinazione
* **contextAttributeDependency** - Associa gli attributi del contesto di origine agli attributi del contesto di destinazione
* **segmentsDependency** - Associa le chiavi del segmento di origine agli identificatori del segmento di destinazione (`{segmentNamespace, segmentId}`)
* **datasetName** - Specifica il nome del set di dati di destinazione per la migrazione

### Passaggio 2: eseguire la migrazione {#execute-migration}

Dopo aver analizzato le dipendenze e preparato le mappature, puoi eseguire la migrazione.

#### Creare un flusso di lavoro di migrazione {#create-migration-workflow}

Utilizza i mapping delle dipendenze dal passaggio 1 per configurare ed eseguire la migrazione.

**Formato API**

```http
POST /migration/service/migrations
```

**Migrazione a livello di sandbox**

Per migrare tutti gli oggetti decisioning da una sandbox all’altra:

```shell
curl --request POST \
  --url "https://platform.adobe.io/migration/service/migrations" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>" \
  --header "Content-Type: application/json" \
  --data '{
    "imsOrgId": "<IMS_ORG_ID>",
    "sourceSandboxDetails": { "sandboxName": "<SOURCE_SANDBOX_NAME>" },
    "targetSandboxDetails": { "sandboxName": "<TARGET_SANDBOX_NAME>" },
    "createDataStream": true,
    "dependency": {
      "profileAttributeDependency": {
        "sourceAttr1": "targetAttr1"
      },
      "segmentsDependency": {
        "sourceSegmentKey1": {
          "segmentNamespace": "<TARGET_SEGMENT_NAMESPACE>",
          "segmentId": "<TARGET_SEGMENT_ID>"
        }
      },
      "contextAttributeDependency": {
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

**Migrazione a livello di decisione**

Per migrare solo decisioni specifiche, utilizzare `requestLevel: "decision"` e aggiungere un array `decisionsList`:

```json
"decisionsList": ["decision-id-1", "decision-id-2"]
```

#### Monitorare lo stato della migrazione {#poll-migration-status}

Esegui il polling del flusso di lavoro di migrazione per tracciarne l’avanzamento.

**Formato API**

```http
GET /migration/service/migrations/{id}
```

**Richiesta**

```shell
curl --request GET \
  --url "https://platform.adobe.io/migration/service/migrations/<WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>"
```

**Risultati migrazione**

Quando il campo `status` mostra `Completed`, la migrazione è riuscita. Il flusso di lavoro `result` include:
* Mappature di oggetti migrati
* Eventuali avvisi rilevati durante la migrazione

Quando il campo `status` mostra `Failed`, controlla l&#39;array `errors[]` e il campo `result.error` per i dettagli sul problema.

## Convalidare la migrazione {#validate-migration}

Al termine della migrazione, verificare che tutti gli oggetti siano stati migrati correttamente.

### Elenco di controllo per la convalida {#validation-checklist}

1. **Segmenti** - Verifica che tutti i segmenti a cui si fa riferimento vengano risolti correttamente nella sandbox di destinazione in base ai tuoi mapping.
2. **Attributi** - Verificare che tutti gli attributi di profilo e gli attributi di contesto siano presenti nella sandbox di destinazione e mappati correttamente.
3. **Oggetti decisioning** - Esaminare gli oggetti migrati nell&#39;interfaccia utente di Journey Optimizer:
   * Offerte (elementi di decisione)
   * Regole di idoneità
   * Formule di ranking
   * Strategie di selezione
   * Criteri di decisione
4. **Test dello stream di dati** - Se è stato creato uno stream di dati, verifica la consegna in fase di esecuzione utilizzando l&#39;API di interazione di Edge.

### Esempio {#test-runtime-delivery}

Se la migrazione ha creato un flusso di dati, puoi testare la consegna delle offerte utilizzando il seguente esempio:

```shell
curl --request POST \
  --url "https://edge.adobedc.net/ee/or2/v1/interact?configId=<DATASTREAM_ID>" \
  --header "Content-Type: application/json" \
  --header "x-request-id: <uuid>" \
  --data '{ "events": [ ... ] }'
```

## Ripristino dello stato precedente di una migrazione {#rollback}

Se riscontri dei problemi durante la convalida, puoi eseguire il rollback di una migrazione completata per ripristinare lo stato precedente della sandbox di destinazione.

### Creare un flusso di lavoro di rollback {#create-rollback-workflow}

Avvia un rollback creando un flusso di lavoro di rollback che faccia riferimento alla migrazione da ripristinare.

**Formato API**

```http
POST /migration/service/rollbacks/{migrationWorkflowId}
```

Sostituire `{migrationWorkflowId}` con l&#39;ID del flusso di lavoro di migrazione di cui si desidera eseguire il rollback.

**Richiesta**

```shell
curl --request POST \
  --url "https://platform.adobe.io/migration/service/rollbacks/<MIGRATION_WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>"
```

### Monitora stato rollback {#poll-rollback-status}

Esamina il flusso di lavoro di rollback per tenerne traccia dell’avanzamento.

**Formato API**

```http
GET /migration/service/rollbacks/{rollbackWorkflowId}
```

**Richiesta**

```shell
curl --request GET \
  --url "https://platform.adobe.io/migration/service/rollbacks/<ROLLBACK_WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>"
```

## Gestire flussi di lavoro simultanei {#handle-concurrency}

L’API di migrazione consente di eseguire un solo flusso di lavoro alla volta per organizzazione. Se tenti di creare un nuovo flusso di lavoro mentre ne è in corso un altro, riceverai una risposta di errore **409** (&quot;Un flusso di lavoro è già in corso...&quot;).

In questo caso, attendi il completamento del flusso di lavoro in corso oppure recupera l’ID del flusso di lavoro ed esegui il polling del relativo stato. Al termine del flusso di lavoro corrente, puoi crearne uno nuovo.

## Riferimento mapping entità {#entity-mapping}

Durante la migrazione da Gestione decisioni a Decisioning, le entità vengono mappate come segue:

| Gestione delle decisioni | Funzione Decisioni |
|-------------------|-------------|
| Nome | Elemento decisionale |
| Raccolta di offerte | Raccolta elementi |
| Regola di idoneità | Regola di idoneità |
| Formula di classificazione | Formula di classificazione |
| Decisione | Strategia di selezione e politica decisionale |
| Campaign | Campagna *(solo contenuto di base)* |
| Posizionamento | Configurazione di superficie e canale |
| Tag | Tag unificato |

## Pulizia del flusso di lavoro {#cleanup}

Le risorse del flusso di lavoro possono essere eliminate solo dagli utenti del servizio. Le operazioni di eliminazione richiedono un&#39;intestazione `If-Match` con il valore `_etag` del flusso di lavoro.

**Operazioni di eliminazione disponibili:**

* `DELETE /migration/service/dependency/{id}`
* `DELETE /migration/service/migrations/{id}`
* `DELETE /migration/service/rollbacks/{id}`

>[!NOTE]
>
>L’eliminazione del flusso di lavoro è disponibile solo per gli account di servizio con le autorizzazioni appropriate. Se devi eliminare una risorsa del flusso di lavoro, contatta l’amministratore di sistema.

## Argomenti correlati {#related-topics}

* [Migrare da Gestione decisioni a Decisioning](migrate-to-decisioning.md) - Comprendere i vantaggi e le funzionalità della migrazione a Decisioning
* [Introduzione alla funzione Decisioni](gs-experience-decisioning.md)
* [Guardrail e limitazioni decisionali](decisioning-guardrails.md)
* [Introduzione alle API Decisioning](api-reference/getting-started.md)
