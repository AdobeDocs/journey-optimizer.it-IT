---
solution: Journey Optimizer
product: journey optimizer
title: Guida alla definizione del premio
description: Scopri come configurare le definizioni dei premi per i provider di premi per le sfide di fedeltà in Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="Beta privata" type="Informative"
mini-toc-levels: 1
exl-id: 9b0fd9d8-18d1-4a51-8b6f-b2e2a4c6f1d7
feature_v2: []
subfeature_v2: []
source-git-commit: 00c24e9b97b4f6597048731858f3bfbcb39a0030
workflow-type: tm+mt
source-wordcount: 1206
ht-degree: 3%

---

# Guida alla definizione del premio {#reward-definition-guide}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_reward_definition"
>title="Guida alla definizione del premio"
>abstract="Utilizzare questa guida per configurare le definizioni dei premi per i provider di premi fedeltà, inclusi i campi payload di tipo Comportamento definizione predefinito e Evasione."

>[!BEGINSHADEBOX]

**Sommario**

[Introduzione alle sfide di fedeltà](get-started.md)

<table style="table-layout:fixed">
<tr style="border: 0;">
<td style="vertical-align:top;">

**Crea e gestisci le sfide**

* [Accesso e gestione di sfide e attività](access-loyalty-challenges.md)
* [Creare le sfide](create-challenges.md)
* [Creare le attività](create-tasks.md)
* [Monitorare le prestazioni della sfida fedeltà](loyalty-reporting.md)

</td>
<td style="vertical-align:top;">

**Configura e integra**

* [Configurare le sfide relative alla fedeltà](loyalty-admin.md)
* **Guida alla definizione del premio** ◀︎ **Sei qui**
* [Guida di Event Transformer](event-transformer-guide.md)
* [Dati e set di dati sulla fedeltà](loyalty-data-and-datasets.md)
* [Riferimento API per le sfide di fedeltà](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

</td>
</tr>
</table>

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Questa funzionalità è attualmente in **versione beta privata**. Per informazioni dettagliate sul ciclo di rilascio e sulle fasi di disponibilità in [!DNL Journey Optimizer], vedere [ciclo di rilascio](../rn/releases.md).

Quando un&#39;attività di verifica, un&#39;attività cardine o una sfida completa **e ha un valore di ricompensa configurato**, la piattaforma emette una ricompensa chiamando l&#39;endpoint HTTP del provider di ricompensa con un payload JSON. Una **definizione premio** descrive il premio da emettere e fornisce un&#39;espressione [JSONata](https://docs.jsonata.org/overview), `rewardJsonata`, che definisce il payload esatto previsto dal provider.

Questa guida illustra come configurare un provider di premi, creare definizioni di premi, scrivere l&#39;espressione `rewardJsonata` e capire il contesto disponibile al momento della valutazione.

## Modello a due livelli

I premi sono organizzati in due livelli:

```
Reward Provider  (endpoint, auth, headers)
└── Reward Definition  (denomination, rewardJsonata)
└── Reward Definition
└── ...
```

Un **Provider di premi** rappresenta un singolo sistema di premi esterno. Contiene l&#39;URL dell&#39;endpoint di consegna, l&#39;autenticazione ed eventuali intestazioni HTTP personalizzate. Un provider può contenere più **Definizioni di ricompensa**, ognuna delle quali descrive un tipo di ricompensa o una denominazione distinta offerta dal provider (ad esempio &quot;50 Stelle&quot;, &quot;Stelle doppie&quot;, &quot;Elemento libero&quot;).

Una richiesta di verifica fa riferimento al provider e alla definizione per GUID. Quando viene assegnato un premio, la piattaforma valuta l&#39;espressione `rewardJsonata` della definizione e PUBBLICA il risultato sull&#39;endpoint del provider.

## Campi di definizione e provider di premi

+++Campi del provider di premi

<table>
<colgroup>
<col style="width:160px">
<col style="width:80px">
<col style="width:160px">
<col>
</colgroup>
<tr><th>Campo</th><th>Tipo</th><th>Obbligatorio</th><th>Descrizione</th></tr>
<tr><td><code>guid</code></td><td><code>String</code></td><td>No (assegnato dal sistema)</td><td>Identificatore univoco. Sola lettura.</td></tr>
<tr><td><code>name</code></td><td><code>String</code></td><td><strong>Sì</strong></td><td>Nome visualizzato, univoco all’interno dell’organizzazione.</td></tr>
<tr><td><code>desc</code></td><td><code>String</code></td><td>No</td><td>Descrizione leggibile del provider.</td></tr>
<tr><td><code>enabled</code></td><td><code>Boolean</code></td><td>No</td><td>Quando <code>false</code>, la consegna dei premi è <br> sospesa per tutte le definizioni in questo provider.</td></tr>
<tr><td><code>url</code></td><td><code>String</code></td><td><strong>Sì</strong></td><td>Endpoint HTTP che riceve il payload di ricompensa.<br>La piattaforma invia l'output <br><code>rewardJsonata</code> valutato a questo URL.</td></tr>
<tr><td><code>additionalHeaders</code></td><td><code>Object</code></td><td>No</td><td>Intestazioni HTTP personalizzate da includere in ogni <br>richiesta di consegna (ad esempio chiavi API,<br>sostituzioni di tipo contenuto).</td></tr>
<tr><td><code>maxRatePerSecond</code></td><td><code>Integer</code></td><td>No</td><td>Limite di tariffa per provider facoltativo (1-5000).<br>Null significa illimitato.</td></tr>
<tr><td><code>enableMTLS</code></td><td><code>Boolean</code></td><td>No</td><td>Se l’endpoint richiede TLS reciproco.</td></tr>
</table>

+++

+++Campi di definizione del premio

<table>
<colgroup>
<col style="width:160px">
<col style="width:80px">
<col style="width:160px">
<col>
</colgroup>
<tr><th>Campo</th><th>Tipo</th><th>Obbligatorio</th><th>Descrizione</th></tr>
<tr><td><code>guid</code></td><td><code>String</code></td><td>No (assegnato dal sistema)</td><td>Identificatore univoco. Sola lettura.</td></tr>
<tr><td><code>name</code></td><td><code>String</code></td><td><strong>Sì</strong></td><td>Nome visualizzato, univoco all’interno del provider.</td></tr>
<tr><td><code>denomination</code></td><td><code>String</code></td><td>No</td><td>Unità del premio, utilizzata in visualizzazione<br>e disponibile nelle espressioni come<br><code>reward.denomination</code><br>(ad esempio <code>"Stars"</code>, <code>"Points"</code>, <code>"Miles"</code>).</td></tr>
<tr><td><code>desc</code></td><td><code>String</code></td><td>No</td><td>Descrizione del premio, disponibile<br>nelle espressioni come <code>reward.desc</code>.</td></tr>
<tr><td><code>enabled</code></td><td><code>Boolean</code></td><td>No</td><td>Quando <code>false</code>, questa definizione è inattiva<br>e non emetterà premi.</td></tr>
<tr><td><code>isDefault</code></td><td><code>Boolean</code></td><td>No</td><td>Contrassegna questo come definizione di ricompensa predefinita<br>a livello di sandbox. È possibile impostare una sola definizione<br>per tutti i provider alla volta;<br>l'impostazione di un nuovo valore predefinito cancella quello precedente.<br>Utilizzato per popolare automaticamente i dettagli dei premi sulle<br>sfide personalizzate al momento della pubblicazione.</td></tr>
<tr><td><code>rewardJsonata</code></td><td><code>String</code></td><td><strong>Sì</strong></td><td>Espressione JSONata valutata <br>al momento del problema del premio. Riceve il contesto completo<br>di ricompensa e deve restituire il payload JSON<br>a POST al provider.</td></tr>
</table>

+++

## Contesto del premio

Quando `rewardJsonata` viene valutato, riceve un singolo oggetto principale contenente tutto ciò che è noto sull&#39;evento di ricompensa. Tutti i percorsi nell’espressione sono relativi a questa radice.

```json
{
  "rewardContext": {
    "rewardValue": "50",
    "source":      "challenge"
  },
  "reward": {
    "name":         "500 Stars",
    "desc":         "Issue 500 Stars to the member",
    "denomination": "Stars",
    "enabled":      true
  },
  "task": { ... },
  "milestone": { ... },
  "challenge": { ... },
  "timestamp": "2026-02-10T00:29:22.538+00:00"
}
```

+++ Campi contestuali

| Campo | Descrizione |
|----------------------------------------|-------------|
| `rewardContext.rewardValue` | Stringa di valore del premio configurata per la sfida, l&#39;attività o l&#39;attività cardine che ha attivato l&#39;emissione. |
| `rewardContext.source` | Che cosa ha attivato il premio: `"task"`, `"challenge"` o `"milestone"`. |
| `reward` | La stessa RewardDefinition: `name`, `desc`, `denomination`. |
| `task` | L&#39;attività di completamento, inclusi `accumulators`, `schedule` e `reward`. |
| `task.accumulators.spend` | Spesa totale qualificata accumulata dall&#39;attività. |
| `task.accumulators.qty` | Numero totale di articoli qualificati accumulato dall&#39;attività. |
| `task.accumulators.item_list` | Tutti gli elementi idonei applicati all&#39;attività. Ogni voce ha `item`, `transactionId`, `timestamp`, `utcOffset`, `locationId`. |
| `task.accumulators.item_list[-1]` | L’elemento più recente applicato (indice JSONata negativo). Utile per determinare l’origine dell’ID o della marca temporale dell’ultima transazione. |
| `task.schedule.currentStreak` | Conteggio attuale delle sequenze di visite consecutive (per le sfide di serie). |
| `task.schedule.currentVisits` | Conteggio totale delle visite (per le sfide relative alle visite). |
| `milestone` | La milestone che ha attivato questo premio, o `null` se non è un premio milestone. Include `count` e `reward.rewardValue`. |
| `challenge.profileId` | ID fedeltà del membro. |
| `challenge.kvpCustom` | Coppie chiave-valore personalizzate configurate per la sfida. Un modello comune per il passaggio di ID campagna, nomi di prodotto o metadati specifici del provider. |
| `challenge.name` | Nome della sfida. |
| `challenge._id` | ID sfida. |
| `timestamp` | Timestamp ISO 8601 dell’emissione del premio. |

+++

## Scrittura dell&#39;espressione rewardJsonata

L’espressione riceve il contesto di ricompensa come input e deve restituire un oggetto JSON, il payload POSTed all’endpoint del provider. La forma di tale oggetto dipende interamente dall&#39;API del provider. I campi contestuali vengono mappati in base alla struttura prevista dal provider.

+++Payload fisso semplice

Il caso più semplice: il provider richiede un conteggio dei punti e un ID membro, entrambi noti dal contesto.

```jsonata
{
  "memberId":   challenge.profileId,
  "points":     $number(rewardContext.rewardValue),
  "currency":   reward.denomination
}
```

**Output:**

```json
{
  "memberId": "ADB-0000030",
  "points":   50,
  "currency": "Stars"
}
```

> `rewardContext.rewardValue` è sempre una stringa. Utilizza `$number()` per convertirlo se il provider prevede un valore numerico.

+++

+++Utilizzo di `kvpCustom` per metadati specifici del provider

I provider spesso richiedono campi come ID campagna o codici del sistema sorgente specifici per ogni sfida eseguita. Memorizza questi elementi in `challenge.kvpCustom` durante l’authoring della sfida, quindi fai riferimento ad essi nell’espressione, mantenendo l’espressione riutilizzabile nelle campagne.

```jsonata
{
  "memberId":         challenge.profileId,
  "points":           $number(rewardContext.rewardValue),
  "campaignId":       challenge.kvpCustom.campaignId,
  "transactionSource": "AJO"
}
```

È inoltre possibile utilizzare `reward.kvpCustom` per le costanti fisse per un determinato tipo di premio anziché per sfida.

+++

+++Utilizzo dei dati accumulatori delle attività

Gli accumulatori di task tengono traccia di ogni evento qualificato. Utilizza `item_list[-1]` per accedere all&#39;elemento applicato più di recente. I relativi `transactionId` e `timestamp` sono utili per gli audit trail e la deduplicazione sul lato provider.

```jsonata
{
  "memberId":       challenge.profileId,
  "points":         $number(rewardContext.rewardValue),
  "transactionId":  task.accumulators.item_list[-1].transactionId,
  "transactionDate": task.accumulators.item_list[-1].timestamp
}
```

+++

+++Creazione di un messaggio di testo

Per i provider basati su notifiche (Slack, SMS, e-mail), puoi creare una stringa di messaggio direttamente utilizzando l’operatore di concatenazione `&` di JSONata:

```jsonata
{
  "text": "You just earned " & rewardContext.rewardValue & " " & reward.denomination & "!"
}
```

**Output:**

```json
{
  "text": "You just earned 50 Stars!"
}
```

+++

## Esempi

+++Esempio 1 — Fornitore di punti semplice

**Scenario:** un&#39;API di base per i punti fedeltà prevede un ID membro e una quantità di punti.

**Definizione premio:**

```json
{
  "name":         "Standard Points",
  "denomination": "Points",
  "desc":         "Award loyalty points",
  "enabled":      true,
  "rewardJsonata": "{\"memberId\": challenge.profileId, \"pointQuantity\": $number(rewardContext.rewardValue), \"denomination\": reward.denomination}"
}
```

**Espressione formattata:**

```jsonata
{
  "memberId":      challenge.profileId,
  "pointQuantity": $number(rewardContext.rewardValue),
  "denomination":  reward.denomination
}
```

**Payload inviato al provider:**

```json
{
  "memberId":      "ADB-0000030",
  "pointQuantity": 50,
  "denomination":  "Points"
}
```

+++

+++Esempio 2 — Payload del provider con metadati della campagna

**Scenario:** Il provider richiede un record di riconoscimento strutturato che includa campi di controllo, riferimenti alla campagna e descrizione del membro. I valori specifici della campagna sono archiviati in `challenge.kvpCustom`, pertanto la stessa definizione del premio funziona nelle campagne senza modificare l&#39;espressione.

**Sfida`kvpCustom`** (impostata durante l&#39;authoring della sfida):

```json
{
  "parentCampaignId": "CAMP-2026-Q1",
  "productName":      "Loyalty Program"
}
```

**Definizione premio:**

```json
{
  "name":         "Stars — Campaign Award",
  "denomination": "Stars",
  "desc":         "Issue Stars for completing a qualifying purchase",
  "enabled":      true,
  "rewardJsonata": "{\"awardPoints\":[{\"idType\":\"externalId\",\"id\":challenge.profileId,\"transactionId\":task.accumulators.item_list[-1].transactionId,\"transactionDate\":task.accumulators.item_list[-1].timestamp,\"originalTransactionId\":task.accumulators.item_list[-1].transactionId,\"transactionSource\":\"AJO\",\"channelSource\":\"Web\",\"parentCampaignId\":challenge.kvpCustom.parentCampaignId,\"productName\":challenge.kvpCustom.productName,\"memberAwardDescription\":reward.desc,\"pointQuantity\":$number(rewardContext.rewardValue)}]}"
}
```

**Espressione formattata:**

```jsonata
{
  "awardPoints": [
    {
      "idType":                "externalId",
      "id":                    challenge.profileId,
      "transactionId":         task.accumulators.item_list[-1].transactionId,
      "transactionDate":       task.accumulators.item_list[-1].timestamp,
      "originalTransactionId": task.accumulators.item_list[-1].transactionId,
      "transactionSource":     "AJO",
      "channelSource":         "Web",
      "parentCampaignId":      challenge.kvpCustom.parentCampaignId,
      "productName":           challenge.kvpCustom.productName,
      "memberAwardDescription": reward.desc,
      "pointQuantity":         $number(rewardContext.rewardValue)
    }
  ]
}
```

**Payload inviato al provider:**

```json
{
  "awardPoints": [
    {
      "idType":                "externalId",
      "id":                    "ADB-0000030",
      "transactionId":         "b4fa0e89-f4bb-41ce-b370-fb97f9c52f1a",
      "transactionDate":       "2026-02-08T00:12:00.000+00:00",
      "originalTransactionId": "b4fa0e89-f4bb-41ce-b370-fb97f9c52f1a",
      "transactionSource":     "AJO",
      "channelSource":         "Web",
      "parentCampaignId":      "CAMP-2026-Q1",
      "productName":           "Loyalty Program",
      "memberAwardDescription": "Issue Stars for completing a qualifying purchase",
      "pointQuantity":         50
    }
  ]
}
```

+++

+++Esempio 3 — Premio Milestone

**Scenario:** una sfida di tipo streak genera un premio milestone ogni N visite. L’espressione include il conteggio delle milestone e la sequenza corrente per il contesto lato provider.

**Espressione formattata:**

```jsonata
{
  "memberId":       challenge.profileId,
  "points":         $number(rewardContext.rewardValue),
  "milestoneCount": milestone.count,
  "currentStreak":  task.schedule.currentStreak,
  "denomination":   reward.denomination,
  "source":         rewardContext.source
}
```

**Payload POST inviato al provider** (alla seconda visita):

```json
{
  "memberId":       "ADB-0000030",
  "points":         20,
  "milestoneCount": 2,
  "currentStreak":  2,
  "denomination":   "Stars",
  "source":         "milestone"
}
```

> Quando `rewardContext.source` è `"milestone"`, l&#39;oggetto `milestone` viene popolato con `count` e `reward.rewardValue`. Quando l&#39;origine è `"task"` o `"challenge"`, `milestone` è `null`.

+++

## Documentazione delle API

+++Provider di premi

```http
POST   /loyalty/metadata/config/rewards/providers
GET    /loyalty/metadata/config/rewards/providers
GET    /loyalty/metadata/config/rewards/providers/{providerId}
PUT    /loyalty/metadata/config/rewards/providers/{providerId}
DELETE /loyalty/metadata/config/rewards/providers/{providerId}
```

Tutte le richieste richiedono `x-gw-ims-org-id` e `x-sandbox-name` intestazioni.

**Crea un provider:**

```http
POST /loyalty/metadata/config/rewards/providers
x-gw-ims-org-id: {ORG_ID}
x-sandbox-name: {SANDBOX}
Content-Type: application/json

{
  "name":    "My Points Provider",
  "desc":    "Issues loyalty points via REST",
  "enabled": true,
  "url":     "https://rewards.example.com/award",
  "additionalHeaders": {
    "x-api-key": "YOUR_API_KEY"
  }
}
```

+++

+++Definizioni dei premi

```http
POST   /loyalty/metadata/config/rewards/definitions/{providerId}
GET    /loyalty/metadata/config/rewards/definitions/{providerId}
GET    /loyalty/metadata/config/rewards/definitions/{providerId}/{rewardId}
PUT    /loyalty/metadata/config/rewards/definitions/{providerId}/{rewardId}
DELETE /loyalty/metadata/config/rewards/definitions/{providerId}/{rewardId}
```

**Creare una definizione di premio:**

```http
POST /loyalty/metadata/config/rewards/definitions/{providerId}
x-gw-ims-org-id: {ORG_ID}
x-sandbox-name: {SANDBOX}
Content-Type: application/json

{
  "name":         "50 Stars",
  "denomination": "Stars",
  "desc":         "Award 50 Stars on task completion",
  "enabled":      true,
  "rewardJsonata": "{ \"memberId\": challenge.profileId, \"points\": $number(rewardContext.rewardValue) }"
}
```

+++

## Convalida espressione

`rewardJsonata` espressioni sono convalidate per la sintassi al momento della pubblicazione. Se l&#39;espressione non è valida, l&#39;API restituisce un errore `422` con una descrizione dell&#39;errore di analisi.

Per sviluppare e testare un&#39;espressione prima della pubblicazione, utilizzare l&#39;[JSONata Exerciser](https://try.jsonata.org/). Incolla il JSON del contesto di ricompensa come documento di input e l’espressione per verificare che l’output corrisponda a quello previsto dal provider. Negli esempi precedenti viene mostrato un contesto di ricompensa rappresentativo per ogni tipo di trigger (`task`, `milestone`, `challenge`).

## Errori comuni

| Errore | Effetto | Correggi |
|---------|--------|-----|
| `rewardContext.rewardValue` utilizzato come numero senza conversione | Tipo non corrispondente se il provider convalida il campo come numerico | A capo con `$number(rewardContext.rewardValue)` |
| `challenge.kvpCustom.someKey` restituisce null | Chiave non impostata sulla sfida al momento dell’authoring | Assicurarsi che la chiave sia presente in `kvpCustom` per ogni sfida che utilizza questa definizione |
| `task.accumulators.item_list[-1]` è nullo | Nessun elemento applicato prima del premio emesso (evento non di acquisto) | Controlla con un condizionale o utilizza `timestamp` dal contesto |
| Accesso a `milestone` eseguito quando l&#39;origine è `"task"` o `"challenge"` | `milestone` è null; l&#39;espressione genera o produce campi null | Controlla `rewardContext.source` prima di accedere a `milestone` oppure utilizza solo `milestone` nelle definizioni allegate ai premi milestone |
| L’espressione restituisce un array invece di un oggetto | Il provider riceve una struttura di payload imprevista | Racchiudi espressioni che restituiscono array in un oggetto esterno: `{ "items": [...] }` |
