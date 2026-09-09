---
title: API della migrazione a Decisioning
description: Scopri come utilizzare l’API del servizio di migrazione Decisioning per migrare gli oggetti di gestione delle decisioni tra sandbox con risoluzione automatizzata delle dipendenze e supporto del rollback.
feature: Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 3ec084ca-af9e-4b5e-b66f-ec390328a9d6
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
  - id: a984631b-2bae-4860-9b15-69c41a799dcb
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: bf147566ac63bce11f4413a2450b55d436f01d7a
workflow-type: tm+mt
source-wordcount: 3211
ht-degree: 3%

---

# API della migrazione a Decisioning {#decisioning-migration-api}

>[!BEGINSHADEBOX]

**In questa pagina:** utilizza l&#39;API del servizio di migrazione Decisioning per spostare gli oggetti di gestione delle decisioni tra sandbox con l&#39;analisi automatizzata delle dipendenze e il supporto del rollback, in modo da poter trasferire il contenuto decisionale tra gli ambienti mantenendo l&#39;integrità dei dati.

>[!ENDSHADEBOX]

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

>[!NOTE]
>
>La sandbox di destinazione può essere la stessa della sandbox di origine. Il processo di migrazione gestisce questo scenario e garantisce l’integrità dei dati, indipendentemente dal fatto che gli oggetti vengano migrati all’interno della stessa sandbox o a una diversa.

### Prerequisiti per la migrazione tra sandbox {#cross-sandbox-prerequisites}

Quando la sandbox di origine ≠ la sandbox di destinazione, sono necessari i seguenti elementi:

* **Attributi profilo** - Devono esistere nella sandbox di destinazione o avere mappature predefinite
* **ID segmento** - Deve essere precreato nella sandbox di destinazione con le vecchie→nuove mappature ID
* **Mapping identità** - Deve essere configurato per la risoluzione identità coerente

## Nozioni di base sulle API {#api-basics}

### URL di base {#base-url}

Utilizza il seguente URL di base:

* **Produzione**: `https://decisioning-migration.adobe.io`

### Autenticazione {#authentication}

Tutte le richieste API richiedono le seguenti intestazioni:

* `Authorization: Bearer <IMS_ACCESS_TOKEN>`
* `x-gw-ims-org-id: <IMS_ORG_ID>`
* `Content-Type: application/json`

Per istruzioni dettagliate sulla configurazione dell&#39;autenticazione, fare riferimento alla [guida all&#39;autenticazione di Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}.

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
  --url "https://decisioning-migration.adobe.io/workflows/generate-dependencies?request-level=sandbox" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "Content-Type: application/json" \
  --data '{
    "imsOrgId": "<IMS_ORG_ID>",
    "sourceSandboxDetails": { "sandboxName": "<SOURCE_SANDBOX_NAME>" },
    "targetSandboxDetails": { "sandboxName": "<TARGET_SANDBOX_NAME>" }
  }'
```

**Dipendenza a livello di offerta**

Per analizzare le dipendenze solo per offerte specifiche, chiama lo stesso endpoint con `request-level=offer` nella stringa di query e fornisci un array `offersList` nel corpo con gli ID offerta da analizzare.

**Dipendenza a livello di decisione**

Per analizzare le dipendenze solo per decisioni specifiche, utilizzare `request-level=decision` nella stringa di query e fornire un array `decisionsList` nel corpo con gli ID di decisione che si desidera analizzare.

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
* **segmenti** - Mappa ogni chiave del segmento di origine su un identificatore del segmento di destinazione (`{namespace, id}`)
* **datasetName** - Set di dati Experience Event di destinazione utilizzato per la migrazione. Deve essere associato a un flusso di dati abilitato per le chiamate di Journey Optimizer Edge (Web SDK); il relativo schema viene utilizzato per aggiungere gli attributi di contesto migrati.

Fornisci queste mappature nell&#39;oggetto `dependency` della richiesta di migrazione nel passaggio 2.

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
  --url 'https://decisioning-migration.adobe.io/workflows/migration?request-level=sandbox' \
  --header 'Authorization: Bearer <IMS_ACCESS_TOKEN>' \
  --header 'Content-Type: application/json' \
  --header 'x-gw-ims-org-id: <IMS_ORG_ID>' \
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
    }
  }'
```

**Migrazione a livello di offerta**

Per migrare solo offerte specifiche, utilizza `request-level=offer` nella stringa di query e aggiungi un array `offersList` al corpo:

```json
"offersList": ["offer-id-1", "offer-id-2"]
```

**Migrazione a livello di decisione**

Per migrare solo decisioni specifiche, utilizza `request-level=decision` nella stringa di query e aggiungi un array `decisionsList` al corpo:

```json
"decisionsList": ["decision-id-1", "decision-id-2"]
```

**Campi richiesta**

* **livello-richiesta** (query) - Ambito di migrazione: `sandbox`, `offer` o `decision`.
* **imsOrgId** (obbligatorio) - ID organizzazione IMS.
* **sourceSandboxDetails.sandboxName** (obbligatorio) - Sandbox Source che contiene le entità di gestione delle decisioni.
* **targetSandboxDetails.sandboxName** (obbligatorio) - Sandbox di destinazione in cui vengono create le entità decisioning.
* **dependency.datasetName** (obbligatorio) - Set di dati di Target Experience Event. Deve essere associato a un flusso di dati abilitato per le chiamate di Journey Optimizer Edge (Web SDK); il suo schema viene utilizzato per aggiungere gli attributi di contesto migrati.
* **createDataStream** - `true` crea un nuovo flusso di dati abilitato per Journey Optimizer; `false` riutilizza quello già associato al set di dati in `dependency.datasetName`.
* **dependency.profileAttributes** - Mappa degli attributi del profilo di origine → di destinazione.
* **dependency.contextAttributes** - Mappa degli attributi di contesto di origine → di destinazione.
* **dependency.segments** - Mappa della chiave del segmento di origine → del segmento di destinazione (`{namespace, id}`).
* **offersList[]** / **decisionList[]** - ID offerta o decisione da migrare; obbligatorio quando `request-level` è rispettivamente `offer` o `decision`.

#### Monitorare lo stato della migrazione {#poll-migration-status}

Esegui il polling del flusso di lavoro di migrazione per tracciarne l’avanzamento.

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

**Risultati migrazione**

Quando il campo `status` mostra `Completed`, la migrazione è riuscita. Il flusso di lavoro `result` include:
* Mappature di oggetti migrati
* Eventuali avvisi rilevati durante la migrazione

Quando il campo `status` mostra `Failed`, controlla l&#39;array `errors[]` e il campo `result.error` per i dettagli sul problema.

Ogni flusso di lavoro (dipendenza, migrazione e rollback) restituisce gli stessi campi di risorse:

* **id** - Identificatore del flusso di lavoro (UUID); esegui il polling del relativo stato con `GET /{id}` corrispondente.
* **stato** - Stato del ciclo di vita: `New`, `Running`, `Completed` o `Failed`.
* **risultato** - Presente in `Completed`; l&#39;output del flusso di lavoro (ad esempio, le mappature degli oggetti migrati ed eventuali avvisi).
* **errori[]** - Presente il `Failed`; dettagli errore strutturato (vedere anche `result.error`).
* **_links.self** - URL della risorsa del flusso di lavoro.

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

Sostituire `<MIGRATION_WORKFLOW_ID>` con l&#39;ID del flusso di lavoro di migrazione di cui si desidera eseguire il rollback.

### Monitora stato rollback {#poll-rollback-status}

Esamina il flusso di lavoro di rollback per tenerne traccia dell’avanzamento.

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

## Gestire flussi di lavoro simultanei {#handle-concurrency}

L’API di migrazione consente di eseguire un solo flusso di lavoro alla volta per organizzazione. Se tenti di creare un nuovo flusso di lavoro mentre ne è in corso un altro, riceverai una risposta di errore **409** (&quot;Un flusso di lavoro è già in corso...&quot;).

In questo caso, attendi il completamento del flusso di lavoro in corso oppure recupera l’ID del flusso di lavoro ed esegui il polling del relativo stato. Al termine del flusso di lavoro corrente, puoi crearne uno nuovo.

## Ambito e copertura della migrazione {#migration-scope}

Comprendere l’ambito della migrazione consente di pianificare e convalidare la transizione da Gestione delle decisioni a Decisioning. Questa sezione descrive cosa è coperto dal processo di migrazione e cosa richiede un’azione manuale.

### In-Scope: cosa è coperto {#in-scope}

L’API di migrazione gestisce i seguenti elementi e funzionalità:

* **Casi di utilizzo** - Solo i casi di utilizzo delle decisioni in entrata/Edge sono inclusi nell&#39;ambito. In uscita o OD nella migrazione del canale e-mail di Journey Optimizer sono supportati, ma richiedono aggiornamenti manuali.
* **Campagne basate su codice**: create automaticamente durante la migrazione, una campagna per ogni ambito decisionale migrato nella sandbox di destinazione.
* **Configurazione canale/Superficie** - Configurazioni canale/Superfici create in base al posizionamento di Gestione delle decisioni, garantendo il corretto routing delle risposte alle decisioni.
* **Tipi di contenuto dell&#39;offerta** - Le offerte vengono migrate solo se il loro tipo di contenuto è JSON o Text. Altri tipi di contenuto richiedono la ricreazione manuale.
* **Caratteristiche dell&#39;offerta** - Mantenute nel gruppo di campi `offer_item_custom_attributes` nello schema &quot;Elementi offerta personalizzati - Experience Decisioning&quot;, mantenendo i metadati personalizzati.
* **Attributi di contesto** - Aggiunti allo schema Experience Event nel gruppo di campi `custom_context_attributes` per il tracciamento e la personalizzazione.
* **Ambiti decisionali** - Un ambito decisionale di gestione delle decisioni viene mappato su una strategia di selezione + un criterio di decisione + una campagna in Decisioning, garantendo una gerarchia di entità corretta.
* **Regole di idoneità solo API** - Le regole di idoneità create solo tramite API (non nell&#39;interfaccia utente di gestione delle decisioni) vengono migrate e rimangono solo API in Decisioning. Viene effettuata anche la migrazione delle regole create dall’interfaccia utente.

### Fuori ambito: cosa non è coperto o richiede un’azione manuale {#out-of-scope}

Gli elementi seguenti richiedono un&#39;azione manuale o non sono supportati dagli strumenti di migrazione:

* **Posizionamenti decisionali** - Nessun posizionamento creato dagli strumenti di migrazione. Devi crearli manualmente in Decisioning prima o dopo la migrazione in base alla tua architettura.
* **Limitazione a livello di posizionamento** - La migrazione dei limiti di frequenza a livello di posizionamento non è stata eseguita.
* **Contenuto offerta non JSON/Text** - Le offerte con tipi di contenuto diversi da JSON o Text (ad esempio, HTML, immagini) NON vengono migrate e richiedono la ricreazione manuale in Decisioning.
* **Attributi e segmenti di profilo** - Gli attributi di profilo e le appartenenze ai segmenti NON vengono MAI creati o modificati dagli strumenti di migrazione. Devono esistere già nella sandbox di destinazione prima di eseguire la migrazione.
* **Mappatura ID segmento** - Gli ID segmento devono essere precreati nella sandbox di destinazione. Nella richiesta API di migrazione per la risoluzione dei segmenti devi fornire una mappatura ID precedente → nuova.
* **Modifiche al codice di raccolta dati** - Le modifiche al codice di tracciamento degli eventi lato client e lato server NON sono automatizzate. Il team di implementazione deve aggiornare la raccolta di eventi per utilizzare i formati di richiesta/risposta Decisioning e gli schemi di eventi Decisioning.

## Riferimento mapping entità {#entity-mapping}

Durante la migrazione da Gestione decisioni a Decisioning, le entità vengono mappate in base alla tabella seguente. I mapping includono le entità decisioning primarie e altre entità associate create o utilizzate durante la migrazione.

### Mappatura entità da gestione delle decisioni a decisioning

| Entità di gestione delle decisioni | Entità decisionale | Entità aggiuntive |
|-----------|--------------|-------------------|
| Decisione | Strategia di selezione | Raccolta articoli, Regola di idoneità, Formula di classificazione |
| | Criterio decisionale | Conteggio articoli, strategie di selezione, articolo offerta di fallback |
| | Campagna di esperienza basata su codice | Criterio decisionale, Contenuto, Configurazione canale, Frammenti Journey Optimizer |
| Posizionamento | Configurazione dei canali | — |
| Raccolta | Raccolta elementi | Tag unificati, elementi offerta |
| Qualificatore raccolta | Tag unificati | — |
| Regola | Regola di decisione | — |
| Formula di classificazione | Formula di classificazione delle decisioni | — |
| Nome | Elemento offerta | Regola di idoneità, Frammenti di Journey Optimizer, Tag unificati, Limite di frequenza |
| | Schema Elemento Offerta | — |
| | Frammenti Journey Optimizer | — |

### Convenzioni di denominazione

Il processo di migrazione applica le convenzioni di denominazione utilizzando il prefisso `ExD_` per garantire la coerenza ed evitare conflitti di denominazione.

| Oggetto Source | Pattern per nome gestione decisioni | Pattern nome decisione |
|---------------|-----------------|-------------------|
| Nome | `<offerName>` | `ExD_<offerName>` |
| Regola di idoneità | `<ruleName>` | `ExD_<ruleName>` |
| Formula di classificazione | `<formulaName>` | `ExD_<formulaName>` |
| Raccolta | `<collectionName>` | `ExD_<collectionName>_<placementName>` |
| Decisione → strategia di selezione | `<decisionName>` | `ExD_<decisionName>_selection_strategy_<index>` |
| Decisione → politica decisionale | `<decisionName>` | `ExD_<decisionName>_<placementName>` |
| Frammento Journey Optimizer | `<offerName>` | `ExD_<offerName>_<placementName>_<index>` |
| Posizionamento → superficie | `<placementName>` | `ExD_<placementName>` *(spazi/punti convertiti in trattini bassi)* |
| Tag unificato | `<sourceName>, <targetName>` | `ExDMigration_<sourceName>_<targetName>` |
| Campagna CBE | `<decisionName>, <placementName>` | `Campaign for <decisionName> : <placementName>` |

### Attributi aggiuntivi

| Attributo Source | Posizione di destinazione |
|-----------------|-----------------|
| Attributi di offerta | Campo &quot;migratedofferattributes&quot; nello schema di elementi di offerta personalizzati |
| Attributi di contesto | campo &quot;migratedcontextattributes&quot; nello schema associato al set di dati fornito durante la migrazione |

## Modello di richiesta e risposta {#request-response-model}

Durante la migrazione da Gestione decisioni a Decisioning, il codice dell’applicazione deve essere aggiornato per utilizzare i nuovi formati di richiesta e risposta. Entrambi i sistemi utilizzano l’endpoint Edge Network, ma con strutture di payload e nomi di campo diversi.

### Richiesta Edge di gestione delle decisioni (corrente) {#dm-request}

L’attuale richiesta Edge di gestione delle decisioni segue questa struttura:

**Endpoint:**

```
POST https://edge.adobedc.net/ee/v2/interact
```

**Intestazioni:**
&#x200B;- `Authorization: Bearer <IMS_ACCESS_TOKEN>`
&#x200B;- `x-api-key: <API_KEY>` (da Developer Console)
&#x200B;- `x-gw-ims-org-id: <IMS_ORG_ID>` (formato: `{ORG_ID}@AdobeOrg`)
&#x200B;- `x-request-id: <UNIQUE_REQUEST_ID>` (per traccia e deduplicazione)
&#x200B;- `Content-Type: application/vnd.adobe.xdm+json; schema="…/decision-request;version=1.0"`
&#x200B;- `Accept: application/vnd.adobe.xdm+json; schema="…/decision-response;version=1.0"`
&#x200B;- `x-sandbox-name: <SANDBOX_NAME>` (ad esempio, prod, dev)

**Parametri corpo richiesta:**
&#x200B;- `xdm:dryRun` (true/false) - Verifica le richieste senza rapporti inquinanti
&#x200B;- `xdm:propositionRequests[]` - Array di richieste di decisione:
  &#x200B;- `activityId` - Identificatore attività decisione
  &#x200B;- `placementId` - Identificatore di posizionamento
  &#x200B;- `itemCount` - Numero massimo di offerte da restituire
&#x200B;- `xdm:profiles[].xdm:identityMap` - Mappatura identità (e-mail, ECID, ecc.)
&#x200B;- `xdm:validateContextData` - Flag di convalida dei dati di contesto rigoroso
&#x200B;- `xdm:responseFormat.xdm:includeContent` - Includi solo contenuto effettivo e ID

**Esempio di corpo della richiesta:**

```json
{
  "xdm": {
    "dryRun": false,
    "propositionRequests": [
      { "activityId": "<ACTIVITY_ID>", "placementId": "<PLACEMENT_ID>", "itemCount": 3 }
    ],
    "profiles": [
      { "identityMap": { "ECID": [ { "id": "<ECID>", "primary": true } ] } }
    ],
    "validateContextData": true,
    "responseFormat": { "includeContent": true }
  }
}
```

>[!NOTE]
>Per il riferimento completo alla richiesta/risposta di Gestione decisioni (OD), vedere [API Edge Decisioning](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/decisioning/offer-decisioning/api-reference/offer-delivery-api/edge-decisioning-api) (la variante Web SDK/Edge, che utilizza `decisionScopes` con codifica base64 che contiene `activityId` e `placementId`).

### Decisioning della richiesta di Edge (dopo la migrazione) {#decisioning-request}

Dopo la migrazione, utilizza il formato di richiesta Decisioning tramite lo stesso endpoint Edge Network.

**Endpoint:**

```
POST https://edge.adobedc.net/ee/v2/interact
```

**Campi richiesta chiave:**
&#x200B;- `query.identity.fetch` - Array di tipi di identità da risolvere (esempio: `["ECID"]`)
&#x200B;- `event.xdm.environment.type` - Tipo di ambiente: `"browser"`, `"app"` o `"server"`
&#x200B;- `event.xdm.environment.browserDetails` - Metadati browser (`viewportWidth`, `viewportHeight`, `userAgent`)
&#x200B;- `event.xdm.identityMap` - Stessa mappatura identità come gestione delle decisioni
&#x200B;- `event.xdm.timestamp` - Timestamp ISO 8601
&#x200B;- `query.personalization.surfaces` - Array di superfici di destinazione (ad esempio, `["web://site.com/homepage"]`) — sostituisce `decisionScope`
&#x200B;- `query.personalization.schemas` - Schemi di contenuto da restituire (esempio: `["json-content-item", "html-content-item"]`)
&#x200B;- `data.__adobe.ajo.allowDuplicateDecisionItems` - Controllo di deduplicazione (impostazione predefinita: `true`; impostazione di `false` in modo che un elemento idoneo per più superfici venga restituito una sola volta, mentre le altre superfici ricevono un elemento vuoto o di fallback). Sostituisce la gestione delle decisioni `allowDuplicatePropositions`.
&#x200B;- `data.__adobe.ajo.dryRun` - Flag di test; sopprime gli eventi di feedback sia per i contatori di reporting che per i contatori di limitazione. Sostituisce la gestione delle decisioni `xdm:dryRun`. Rimuovi prima della produzione.

**Esempio di corpo della richiesta (lato server):**

```json
{
  "events": [
    {
      "query": {
        "identity": { "fetch": ["ECID"] },
        "personalization": {
          "surfaces": ["web://my-web/IP_NLI_HP_GET_LOAN_WIDGET"],
          "schemas": [
            "https://ns.adobe.com/personalization/json-content-item",
            "https://ns.adobe.com/personalization/html-content-item"
          ]
        }
      },
      "xdm": {
        "eventType": "decisioning.propositionFetch",
        "environment": {
          "type": "browser",
          "browserDetails": { "viewportWidth": 1280, "viewportHeight": 900, "userAgent": "<USER_AGENT>" }
        },
        "identityMap": {
          "ECID": [ { "id": "<ECID>", "authenticatedState": "ambiguous", "primary": true } ]
        },
        "timestamp": "2025-09-08T12:00:00.000Z"
      },
      "data": {
        "__adobe": { "ajo": { "allowDuplicateDecisionItems": false } }
      }
    }
  ],
  "meta": {
    "state": {
      "domain": "my-web",
      "cookiesEnabled": true,
      "entries": [
        { "key": "kndctr_<ORG>_AdobeOrg_identity", "value": "<identity-cookie>" },
        { "key": "kndctr_<ORG>_AdobeOrg_cluster", "value": "<cluster-cookie>" }
      ]
    }
  }
}
```

>[!NOTE]
>Per informazioni di riferimento complete su Journey Optimizer Decisioning Web SDK/Edge, consulta [Esperienza basata su codice: implementazioni di Decisioning](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/channels/code-based-experience/configure-code-based-channel/code-based-decisioning-implementations).

### Decisioning della risposta di Edge {#decisioning-response}

La risposta di Decisioning contiene più handle organizzati per tipo di problema: `personalization:decisions` (le offerte), `locationHint:result` e `state:store` (i cookie da mantenere).

**Struttura risposta:**

```json
{
  "requestId": "<REQUEST_ID>",
  "handle": [
    {
      "type": "personalization:decisions",
      "eventIndex": 0,
      "payload": [
        {
          "id": "103ae599-e6d8-4631-baf3-51dd8c6ed4c1",
          "scope": "web://my-web/IP_NLI_HP_GET_LOAN_WIDGET",
          "scopeDetails": {
            "decisionProvider": "AJO",
            "correlationID": "<CORRELATION_ID>",
            "characteristics": {
              "eventToken": "<base64 message-level event token>",
              "subPropositions": "<base64-encoded array of decision items>"
            },
            "rank": 1,
            "activity": {
              "id": "<campaignId>#<actionId>",
              "priority": 0,
              "matchedSurfaces": ["web://my-web/IP_NLI_HP_GET_LOAN_WIDGET"]
            }
          },
          "items": [
            {
              "id": "36646bab-af1b-44c6-b632-bbfb9c357919",
              "schema": "https://ns.adobe.com/personalization/json-content-item",
              "data": { "content": "{ ...offer JSON... }" }
            }
          ]
        }
      ]
    },
    {
      "type": "locationHint:result",
      "payload": [
        { "scope": "EdgeNetwork", "hint": "ind1", "ttlSeconds": 1800 }
      ]
    },
    {
      "type": "state:store",
      "payload": [
        { "key": "kndctr_<ORG>_AdobeOrg_cluster", "value": "<cluster-cookie>", "maxAge": 1800 },
        { "key": "kndctr_<ORG>_AdobeOrg_identity", "value": "<identity-cookie>", "maxAge": 34128000 }
      ]
    }
  ]
}
```

**Campi risposta chiave:**
&#x200B;- `handle[].type` - Tipo di handle (`personalization:decisions`, `locationHint:result`, `state:store`)
&#x200B;- `payload[].id` - ID istanza proposta univoco — esegui l’eco sugli eventi di visualizzazione/interazione
&#x200B;- `payload[].scope` - URI di superficie per cui è stata risolta la proposta
&#x200B;- `payload[].scopeDetails.decisionProvider` - Conferma motore: `AJO`
&#x200B;- `payload[].scopeDetails.correlationID` - Collega l&#39;istanza di decisione all&#39;evento di servizio
&#x200B;- `payload[].scopeDetails.rank` / `payload[].scopeDetails.activity` - Classificazione e metadati campagna/azione per la proposta
&#x200B;- `payload[].scopeDetails.characteristics.eventToken` - Token di tracciamento a livello di messaggio
&#x200B;- `payload[].scopeDetails.characteristics.subPropositions` - Array **con codifica Base64 degli elementi decisionali**; ogni elemento ha il proprio `token` per elemento. Questi token per elemento sono ciò che trasmetti in `propositionAction.tokens` sugli eventi di visualizzazione/interazione
&#x200B;- `payload[].items[].schema` / `payload[].items[].data.content` - Schema del contenuto e contenuto dell&#39;offerta effettiva (JSON/HTML) da riprodurre
&#x200B;- Payload `state:store`: cookie di identità e cluster da mantenere e inoltrare nelle richieste successive (lato server)

La stringa `characteristics.subPropositions` base64-decodifica nell&#39;array di elementi serviti, ciascuno con il relativo `token` per elemento:

```json
[
  {
    "id": "1ae75277-8832-4c23-bbbc-09f01cfe6c8b",
    "scope": "web://my-web/IP_NLI_HP_GET_LOAN_WIDGET",
    "scopeDetails": { "decisionProvider": "EXD", "correlationID": "<CORRELATION_ID>-0", "rank": 1 },
    "items": [
      { "id": "dps:<schema>:1be64ff83a612488", "name": "ExD_Personal Loan Offer", "score": 997.0, "token": "CLaefQnVLcLbCtzEXV3Jeg" },
      { "id": "dps:<schema>:1be6516838e1248c", "name": "ExD_Home Loan Offer",     "score": 995.0, "token": "ALlB5KV1B0e+CpHoahi7Ew" },
      { "id": "dps:<schema>:1be650da3cd06e98", "name": "ExD_Auto Loan Offer",     "score": 994.0, "token": "koJTRQcwFkR92AqbZ88ytQ" },
      { "id": "dps:<schema>:1be65612d5a1248d", "name": "ExD_Fallback Offer",      "itemSelection": { "selectionDetail": { "selectionType": "fallback" } }, "token": "GHo4ow7h6iCzBOhYR1+6jg" }
    ]
  }
]
```

## Modelli di implementazione {#implementation-patterns}

Decisioning supporta tre approcci di implementazione:

### Implementazione lato client (Web SDK / Mobile SDK) {#client-side}

Il SDK web o il SDK mobile gestisce automaticamente tutte le richieste e la gestione dei cookie. Con ogni richiesta, SDK archivia e inoltra cookie di identità e cookie cluster.

**Gestione cookie:** Automatica. Web SDK gestisce `kndctr_<OrgId>_identity` e `kndctr_<OrgId>_cluster` cookie.

### Implementazione lato server (API Edge Network) {#server-side}

Il server applicazioni POST viene inviato direttamente ad Edge Network e deve gestire manualmente l’inoltro dei cookie. Il server estrae i cookie del browser dalle richieste in arrivo e li inoltra ad Edge Network tramite `meta.state.entries[]`, quindi restituisce i cookie nella risposta.

**Gestione cookie:** manuale. Il server app deve estrarre i cookie dalla richiesta del browser, inoltrarli ad Edge Network nel corpo della richiesta e impostarli nella risposta. I cookie devono essere inoltrati esplicitamente in `meta.state.entries` per coerenza identità.

### Implementazione ibrida {#hybrid}

Combina il rendering lato server (caricamento pagina iniziale) con SDK lato client (interazioni successive). Il server esegue il rendering del contenuto iniziale tramite Edge Network, quindi Web SDK subentra nelle successive richieste di personalizzazione.

**Gestione cookie:** misti: il lato server richiede l&#39;inoltro manuale dei cookie ad Edge Network; il lato client viene gestito automaticamente da Web SDK. Assicurati che i token di identità dal rendering lato server siano disponibili per SDK lato client per una risoluzione coerente delle identità.

## Tracciamento degli eventi e raccolta dati {#event-tracking}

Per attribuire correttamente i risultati del decisioning, abilitare il limite di frequenza e l’ottimizzazione del ranking basato sull’intelligenza artificiale, devi implementare il tracciamento degli eventi utilizzando lo schema evento Decisioning.

### Campi evento obbligatori {#event-fields}

Sono necessari sia `eventType` che `_experience.decisioning.propositionEventType`. Se manca una delle due, il display/contatore di interazione corrispondente non incrementa.

* **`eventType`** - Specifica la categoria dell&#39;evento:
  &#x200B;- `decisioning.propositionDisplay` — Evento di impression (offerta mostrata all&#39;utente)
  &#x200B;- `decisioning.propositionInteract` — Evento di interazione (clic dell&#39;utente o coinvolgimento con l&#39;offerta)

* **`_experience.decisioning.propositionEventType`** - Contrassegna il sottotipo dell&#39;evento. Includere **esattamente una chiave** del tipo di evento impostata su `1` (ogni valore è `1` o `0`; non impostare più tipi di evento su `1` nello stesso oggetto):
  &#x200B;- `{ "display": 1 }` — Evento di impression
  &#x200B;- `{ "interact": 1 }` — Evento di interazione
  &#x200B;- Se tutte le `display`/`interact`/`dismiss` sono `0` o `eventType` è un valore diverso da `decisioning.proposition<Display|Interact|Dismiss>`, l&#39;evento viene considerato come **evento personalizzato**.

* **`_experience.decisioning.propositionAction.tokens[]`** - Token per elemento che identifica gli elementi serviti da incrementare contatori per:
  &#x200B;- Copiare il `token` di ogni elemento dall&#39;array `subPropositions` decodificato — **not** `scopeDetails.characteristics.eventToken`, che è un token diverso a livello di messaggio.
  &#x200B;- Passa il token esattamente come ricevuto, senza modifiche.
  &#x200B;- **Eventi di interazione:** forniscono **esattamente un token** (l&#39;elemento su cui è stato fatto clic).
  &#x200B;- **Visualizza eventi:** facoltativo — fornire i token per incrementare elementi specifici oppure **omettere** `tokens` per incrementare il contatore per **tutti** elementi in `subPropositions`.

* **`_experience.decisioning.propositions[]`** - Echo ripristina le proposte servite, inclusi `id`, `scope` e il `scopeDetails` completo dalla risposta (che trasporta `characteristics.subPropositions` e richiede `decisionProvider`). Non è necessario creare un array `items[]` esplicito.

### Requisiti dello schema {#schema-requirements}

Associa il gruppo di campi Decisioning allo schema del set di dati dell’evento prima della migrazione:

1. In Experience Platform, apri lo schema del set di dati evento
2. Aggiungi il gruppo di campi `Experience Event - Proposition Details`
3. Assicurati che siano mappati i seguenti campi:
   &#x200B;- `_experience.decisioning.*` campi
   &#x200B;- `_experience.decisioning.propositionAction.tokens`
   &#x200B;- `_experience.decisioning.propositionEventType`

### Gestione dei token di tracciamento {#tracking-token}

Il token di tracciamento deve essere gestito in base ai seguenti requisiti:

* **Il token per elemento guida i contatori**. I valori in `propositionAction.tokens` sono i `token` di ogni elemento servito da `subPropositions`, non i `characteristics.eventToken` a livello di messaggio.
* **Eventi di interazione**: fornire esattamente un token (l&#39;elemento su cui è stato fatto clic).
* **Visualizza eventi** — i token sono facoltativi. Omettere di incrementare tutti gli elementi in `subPropositions` o fornire token specifici per incrementare solo tali elementi.
* **Non modificare il token**. Passare il valore esattamente come ricevuto. Non codificarlo, analizzarlo o modificarlo.

## Esempi di eventi decisionali {#event-examples}

Ogni esempio fa eco alla proposta trasmessa (incluso `scopeDetails`, che contiene `characteristics.subPropositions`) e imposta sia `eventType` che `propositionEventType`. I contatori aumentano rispetto agli elementi in `subPropositions`; `propositionAction.tokens` seleziona gli elementi desiderati.

### Visualizza eventi

Gli eventi di visualizzazione avvisano Decisioning quando un’offerta viene mostrata a un utente. Fornisci i token degli elementi visualizzati oppure ometti `tokens` per incrementare il contatore di visualizzazione per tutti gli elementi in `subPropositions`:

```json
{
  "header": {
    "imsOrgId": "YOUR_ORG_ID",
    "sandboxId": "sandbox-id",
    "sandboxName": "sandbox-name",
    "source": { "name": "ajo-inbound" }
  },
  "body": {
    "xdmEntity": {
      "identityMap": {
        "ECID": [ { "id": "ecid-123", "primary": true } ]
      },
      "eventType": "decisioning.propositionDisplay",
      "_experience": {
        "decisioning": {
          "propositionEventType": { "display": 1 },
          "propositionAction": {
            "id": "b96f842b-5dd9-4c55-9dae-647d96250028",
            "tokens": ["CLaefQnVLcLbCtzEXV3Jeg", "ALlB5KV1B0e+CpHoahi7Ew"]
          },
          "propositions": [
            {
              "id": "103ae599-e6d8-4631-baf3-51dd8c6ed4c1",
              "scope": "web://my-web/IP_NLI_HP_GET_LOAN_WIDGET",
              "scopeDetails": {
                "decisionProvider": "AJO",
                "characteristics": {
                  "eventToken": "<base64 eventToken from response>",
                  "subPropositions": "<base64 subPropositions from response>"
                }
              }
            }
          ]
        }
      }
    }
  }
}
```

### Eventi di interazione (clic)

Gli eventi di interazione tengono traccia di quando un utente fa clic su un’offerta visualizzata o la interagisce con essa. **devi** fornire **esattamente un token** che identifica l&#39;elemento su cui è stato fatto clic:

```json
{
  "header": {
    "imsOrgId": "YOUR_ORG_ID",
    "sandboxId": "sandbox-id",
    "sandboxName": "sandbox-name",
    "source": { "name": "ajo-inbound" }
  },
  "body": {
    "xdmEntity": {
      "identityMap": {
        "ECID": [ { "id": "ecid-123", "primary": true } ]
      },
      "eventType": "decisioning.propositionInteract",
      "_experience": {
        "decisioning": {
          "propositionEventType": { "interact": 1 },
          "propositionAction": {
            "id": "b96f842b-5dd9-4c55-9dae-647d96250028",
            "tokens": ["CLaefQnVLcLbCtzEXV3Jeg"]
          },
          "propositions": [
            {
              "id": "103ae599-e6d8-4631-baf3-51dd8c6ed4c1",
              "scope": "web://my-web/IP_NLI_HP_GET_LOAN_WIDGET",
              "scopeDetails": {
                "decisionProvider": "AJO",
                "characteristics": {
                  "eventToken": "<base64 eventToken from response>",
                  "subPropositions": "<base64 subPropositions from response>"
                }
              }
            }
          ]
        }
      }
    }
  }
}
```

### Eventi personalizzati

Un evento personalizzato utilizza un `eventType` definito dal cliente (qualsiasi valore diverso da `decisioning.proposition<Display|Interact|Dismiss>`) e imposta tutti i valori di `display`/`interact`/`dismiss` su `0` in `propositionEventType` (classificato come `OTHER`). Gli eventi personalizzati vengono decodificati come eventi di visualizzazione (filtro multi-token) rispetto a `subPropositions` e vengono valutati tramite il PQL configurato:

```json
{
  "header": {
    "imsOrgId": "YOUR_ORG_ID",
    "sandboxId": "sandbox-id",
    "sandboxName": "sandbox-name",
    "originalTimestamp": 1700000
  },
  "body": {
    "xdmEntity": {
      "identityMap": {
        "ECID": [ { "id": "ecid-123", "primary": true } ]
      },
      "eventType": "add-to-cart",
      "_experience": {
        "decisioning": {
          "propositionEventType": { "display": 0, "interact": 0, "dismiss": 0 },
          "propositionAction": {
            "id": "b96f842b-5dd9-4c55-9dae-647d96250028",
            "tokens": ["CLaefQnVLcLbCtzEXV3Jeg"]
          },
          "propositions": [
            {
              "id": "103ae599-e6d8-4631-baf3-51dd8c6ed4c1",
              "scope": "web://my-web/IP_NLI_HP_GET_LOAN_WIDGET",
              "scopeDetails": {
                "decisionProvider": "AJO",
                "characteristics": {
                  "eventToken": "<base64 eventToken from response>",
                  "subPropositions": "<base64 subPropositions from response>"
                }
              }
            }
          ]
        }
      }
    }
  }
}
```

Questi eventi abilitano il limite di frequenza, il reporting preconfigurato e l’ottimizzazione del ranking basata sull’intelligenza artificiale in Decisioning. Per l&#39;invio di eventi di proposta con Web SDK, consulta [Esperienza basata su codice: implementazioni di decisioning](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/channels/code-based-experience/configure-code-based-channel/code-based-decisioning-implementations).

## Processo di migrazione completo {#migration-process}

1. Convalidare i prerequisiti: prima di avviare la migrazione, assicurati che la sandbox di destinazione sia preparata e che tutte le dipendenze dei prerequisiti siano identificate e pronte (attributi di profilo, ID segmento, mappatura ID).

1. Chiama l’API di migrazione: esegui l’API di migrazione per migrare gli oggetti di gestione delle decisioni in Decisioning utilizzando i prerequisiti e le mappature preparati.

1. Generazione di entità Draft Decisioning - Lo strumento crea campagne, criteri di decisione, strategie di selezione, elementi di offerta e così via in stato Bozza per il mapping di entità. Esamina tutti gli oggetti Decisioning generati nella sandbox di destinazione. Convalida della correttezza di nomi, tipi di entità e riferimenti. Ancora nulla è rivolto al cliente, la funzione di gestione delle decisioni mantiene il traffico in tempo reale.

1. Aggiorna codice client e server: implementa le modifiche al codice necessarie per utilizzare i nuovi formati di richiesta/risposta Decisioning e implementa il tracciamento degli eventi con i campi obbligatori.

1. Attiva e personalizza: attiva gli oggetti Decisioning (strategie, criteri, campagne, superfici) e sposta il traffico dalla gestione delle decisioni sulla tua timeline.

## Argomenti correlati {#related-topics}

* [Migrare da Gestione decisioni a Decisioning](migrate-to-decisioning.md) - Comprendere i vantaggi e le funzionalità della migrazione a Decisioning
* [Introduzione alla funzione Decisioni](gs-experience-decisioning.md)
* [Guardrail e limitazioni decisionali](decisioning-guardrails.md)
* [Introduzione alle API Decisioning](api-reference/getting-started.md)