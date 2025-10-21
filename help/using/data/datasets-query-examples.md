---
solution: Journey Optimizer
product: journey optimizer
title: Esempi di query per set di dati
description: Esempi di query per set di dati
feature: Journeys, Reporting, Use Cases, Datasets, Data Management
topic: Content Management
role: Engineer, Admin
level: Experienced
keywords: set di dati, ottimizzatore, casi d’uso
exl-id: 26ba8093-8b6d-4ba7-becf-b41c9a06e1e8
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '1066'
ht-degree: 2%

---

# Esempi di query {#query-examples}

In questa pagina è disponibile l’elenco dei set di dati di Adobe Journey Optimizer e dei casi d’uso correlati:

* [Set di dati dell’evento di tracciamento e-mail](#email-tracking-experience-event-dataset)
* [Set di dati evento feedback messaggio](#message-feedback-event-dataset)
* [Set di dati evento di tracciamento push](#push-tracking-experience-event-dataset)
* [Evento passaggio percorso](#journey-step-event)
* [Set di dati dell’evento Decisioning](#ode-decisionevents)
* [Set di dati evento feedback Ccn](#bcc-feedback-event-dataset)
* [Set di dati di entità](#entity-dataset)

Per visualizzare l’elenco completo dei campi e degli attributi di ogni schema, consulta il [dizionario dello schema di Journey Optimizer](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=it){target="_blank"}.

Vedi anche alcuni [esempi comunemente utilizzati per eseguire query sugli eventi dei passaggi del Percorso](../reports/query-examples.md).


## Set di dati dell’evento di tracciamento e-mail{#email-tracking-experience-event-dataset}

_Nome nell&#39;interfaccia: Set di dati evento di tracciamento e-mail AJO_

Set di dati di sistema per l’acquisizione di eventi di esperienza di tracciamento e-mail da Journey Optimizer.

Lo schema correlato è lo schema AJO Email Tracking Experience Event.

Questa query mostra il numero di diverse interazioni e-mail (aperture, clic) per un determinato messaggio:

```sql
select
    _experience.customerJourneyManagement.messageInteraction.interactionType AS interactionType,
    count(1) eventCount
from ajo_email_tracking_experience_event_dataset
where
     _experience.customerJourneyManagement.messageExecution.messageExecutionID IN ('UMA-30647505')
group by
    _experience.customerJourneyManagement.messageInteraction.interactionType
```

Questa query mostra il raggruppamento dei conteggi di diverse interazioni e-mail (aperture, clic) per messaggio per un determinato percorso:

```sql
select
    _experience.customerJourneyManagement.messageExecution.messageExecutionID AS messageExecutionID,
    _experience.customerJourneyManagement.messageInteraction.interactionType AS interactionType,
    count(1) eventCount
from ajo_email_tracking_experience_event_dataset
where
     _experience.customerJourneyManagement.messageExecution.journeyVersionID IN ('0e86ac62-c315-48cc-ab4f-3f8b741ae667')
group by
    _experience.customerJourneyManagement.messageExecution.messageExecutionID,
    _experience.customerJourneyManagement.messageInteraction.interactionType
order by
    _experience.customerJourneyManagement.messageExecution.messageExecutionID,
    _experience.customerJourneyManagement.messageInteraction.interactionType
limit 100;
```

## Set di dati evento feedback messaggio{#message-feedback-event-dataset}

_Nome nell&#39;interfaccia: Set di dati evento feedback messaggi di AJO_

Set di dati per l’acquisizione di eventi di feedback di applicazioni e-mail e push da Journey Optimizer.

Lo schema correlato è Schema evento feedback messaggio di AJO.

Questa query mostra i conteggi di diversi stati di feedback e-mail (inviato, non recapitato, ecc.) per un determinato messaggio:

```sql
select
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus AS feedbackStatus,
    count(1) eventCount
from ajo_message_feedback_event_dataset
where
     _experience.customerJourneyManagement.messageExecution.messageExecutionID IN ('UMA-30647505')
group by
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus;
```

Questa query mostra il raggruppamento dei conteggi dei diversi stati di feedback delle e-mail (inviato, non recapitato, ecc.) per messaggio per un determinato percorso:

```sql
select
    _experience.customerJourneyManagement.messageExecution.messageExecutionID AS messageExecutionID,
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus AS feedbackStatus,
    count(1) eventCount
from ajo_message_feedback_event_dataset
where
     _experience.customerJourneyManagement.messageExecution.journeyVersionID IN ('0e86ac62-c315-48cc-ab4f-3f8b741ae667')
group by
    _experience.customerJourneyManagement.messageExecution.messageExecutionID,
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus
order by
    _experience.customerJourneyManagement.messageExecution.messageExecutionID,
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus
limit 100;
```

A livello aggregato, rapporto a livello di dominio (ordinato per domini principali): Nome di dominio, Messaggio inviato, Mancato recapito

```sql
SELECT split_part(_experience.customerJourneyManagement.emailChannelContext.address, '@', 2) AS recipientDomain, SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' THEN 1 ELSE 0 END)AS sentCount , SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'bounce' THEN 1 ELSE 0 END )AS bounceCount FROM ajo_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY recipientDomain ORDER BY sentCount DESC;
```

L’e-mail viene inviata su base giornaliera:

```sql
SELECT date_trunc('day', TIMESTAMP) AS rolluptimestamp, SUM( CASE WHEN _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'sent' THEN 1 ELSE 0 END) AS deliveredcount FROM ajo_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY date_trunc('day', TIMESTAMP) ORDER BY rolluptimestamp ASC;
```

Scopri se un particolare ID e-mail ha ricevuto o meno un’e-mail e, in caso contrario, qual era l’errore, la categoria di mancato recapito e il codice:

```sql
SELECT _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus AS status, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type AS bouncetype FROM ajo_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' AND _experience.customerjourneymanagement.emailchannelcontext.address = 'user@domain.com' AND TIMESTAMP >= now() - INTERVAL '7' DAY ORDER BY status ASC
```

Trova l’elenco di tutti i singoli ID e-mail che hanno presentato un errore, una categoria di mancato recapito o un codice particolare nelle ultime x ore/giorni o associati a una consegna di messaggio particolare:

```sql
SELECT _experience.customerjourneymanagement.emailchannelcontext.address AS emailid, _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus AS status, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type AS bouncetype FROM ajo_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' AND _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus != 'sent' AND TIMESTAMP >= now() - INTERVAL '10' HOUR AND _experience.customerjourneymanagement.messageexecution.messageexecutionid = 'BMA-45237824' ORDER BY emailid
```

Percentuale mancati recapiti permanenti a livello aggregato:

```sql
select hardBounceCount, case when sentCount > 0 then(hardBounceCount/sentCount)*100.0 else 0 end as hardBounceRate from ( select SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'bounce' AND _experience.customerJourneyManagement.messageDeliveryfeedback.messageFailure.type = 'Hard' THEN 1 ELSE 0 END)AS hardBounceCount , SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' THEN 1 ELSE 0 END )AS sentCount from ajo_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' )
```

Errori permanenti raggruppati per codice di mancato recapito:

```sql
SELECT _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, COUNT(*) AS hardbouncecount FROM ajo_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'bounce' AND _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type = 'Hard' AND _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY failurereason
```

>[!NOTE]
>
>In alcuni percorsi, `messageID` potrebbe non essere univoco per ogni singola consegna. Se un percorso invia nuovamente la stessa azione allo stesso profilo, è possibile riutilizzare `messageID`. Pertanto, per tenere traccia o attribuire con precisione gli eventi al livello di invio individuale, combinare i campi `journeyVersionID`, `journeyActionID` e `batchInstanceID` (per percorsi batch) o `identityMap` per ottenere un&#39;univocità più precisa.


### Identificare gli indirizzi messi in quarantena dopo un’interruzione del servizio ISP{#isp-outage-query}

In caso di interruzione del servizio di un provider di servizi Internet (ISP), è necessario identificare gli indirizzi e-mail erroneamente contrassegnati come mancati recapiti (messi in quarantena) per domini specifici, durante un determinato arco temporale. Per ottenere tali indirizzi, utilizza la seguente query:

```sql
SELECT
    _experience.customerJourneyManagement.emailChannelContext.address AS RecipientAddress,
    timestamp AS EventTime,
    _experience.customerJourneyManagement.messageDeliveryfeedback.messageFailure.reason AS "Invalid Recipient"
FROM ajo_message_feedback_event_dataset
WHERE
    eventtype = 'message.feedback' AND
    DATE(timestamp) BETWEEN '<start-date-time>' AND '<end-date-time>' AND
    _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'bounce' AND
    _experience.customerJourneyManagement.emailChannelContext.address ILIKE '%domain.com%'
ORDER BY timestamp DESC;
```

dove il formato delle date è: `YYYY-MM-DD HH:MM:SS`.

Una volta identificati, rimuovi tali indirizzi dall’elenco di soppressione di Journey Optimizer. [Ulteriori informazioni](../configuration/manage-suppression-list.md#remove-from-suppression-list).

>[!NOTE]
>
>Quando si fa riferimento a identityMap nel set di dati dell’evento di feedback del messaggio, si prega di notare che questo riflette solo l’identità utilizzata in fase di esecuzione. Per le notifiche push, un evento &quot;inviato&quot; si baserebbe solo sull’ECID collegato al token push utilizzato per inviare questa notifica, mentre un evento &quot;esclusione&quot; potrebbe basarsi su un’identità personalizzata. Ad esempio, se un profilo è stato escluso perché non è stato trovato alcun token push, per registrare questo evento verrà selezionata l’identità utilizzata a livello di percorso o di campagna di azione. Se hai bisogno di spazi dei nomi aggiuntivi (ad esempio, ID personalizzati), unisci questi record di feedback con un set di dati relativi al profilo (ad esempio, quelli profile_snapshot) per recuperare l’elenco delle identità completo.




## Set di dati evento di tracciamento push {#push-tracking-experience-event-dataset}

_Nome nell&#39;interfaccia: Set di dati evento di tracciamento push di AJO_

Set di dati per l’acquisizione degli eventi di esperienza di tracciamento mobile per il push da Journey Optimizer.

Lo schema correlato è Schema AJO Push Tracking Experience Event.

Esempio di query:

```sql
select _experience.customerJourneyManagement.pushChannelContext.platform, sum(pushNotificationTracking.customAction.value)  from ajo_push_tracking_experience_event_dataset
group by _experience.customerJourneyManagement.pushChannelContext.platform

select  _experience.customerJourneyManagement.pushChannelContext.platform, SUM (_experience.customerJourneyManagement.messageInteraction.offers.offerCount) from ajo_email_tracking_experience_event_dataset
  group by _experience.customerJourneyManagement.pushChannelContext.platform
```

## Evento passaggio percorso{#journey-step-event}

_Nome interno: eventi passaggio Percorso (set di dati di sistema)_

Set di dati per l’acquisizione degli eventi dei passaggi nel percorso.

Lo schema correlato è lo schema evento passaggio di Percorso per Journey Orchestration.

Questa query mostra la suddivisione dei conteggi di successo delle azioni per etichetta azione per un determinato percorso:

```sql
select
    _experience.journeyOrchestration.stepEvents.actionName AS actionLabel,
    count(1) actionSuccessCount
from journey_step_events
where
     _experience.journeyOrchestration.stepEvents.journeyVersionID IN ('0e86ac62-c315-48cc-ab4f-3f8b741ae667')
     AND _experience.journeyOrchestration.stepEvents.actionID IS NOT NULL
     AND _experience.journeyOrchestration.stepEvents.actionType IS NOT NULL
     AND _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode IS NULL
group by
    _experience.journeyOrchestration.stepEvents.actionName;   
```

Questa query mostra la suddivisione dei conteggi dei passaggi immessi per nodeId e nodeLabel per un determinato percorso. nodeId è incluso qui poiché nodeLabel può essere lo stesso per nodi di percorso diversi.

```sql
select
    _experience.journeyOrchestration.stepEvents.nodeID AS nodeID,
    _experience.journeyOrchestration.stepEvents.nodeName AS nodeLabel,
    count(1) stepEnteredCount
from journey_step_events
where
     _experience.journeyOrchestration.stepEvents.journeyVersionID IN ('0e86ac62-c315-48cc-ab4f-3f8b741ae667')
     AND _experience.journeyOrchestration.stepEvents.journeyNodeProcessed = TRUE
     AND _experience.journeyOrchestration.stepEvents.eventID IS DISTINCT FROM 'createInstance'
group by
    _experience.journeyOrchestration.stepEvents.nodeID,
    _experience.journeyOrchestration.stepEvents.nodeName; 
```




Questa query recupera i nodi (per nodeID e nodeName) del percorso associati alla consegna di un messaggio a un profilo, utilizzando il relativo ID profilo e il set di dati Evento di feedback del messaggio:

```sql
select
    _experience.journeyorchestration.stepevents.nodeID, JSE._experience.journeyorchestration.stepevents.nodeName
from journey_step_events JSE
where 
    _experience.journeyOrchestration.stepEvents.actionID 
    in

    (
    select
        _experience.customerJourneyManagement.messageExecution.journeyActionID
    from  ajo_message_feedback_event_dataset
    where 
        _experience.customerJourneyManagement.messageProfile.messageProfileID = '<PROFILE ID>'
    group by
        _experience.customerJourneyManagement.messageExecution.journeyActionID
    )

group by
    _experience.journeyorchestration.stepevents.nodeID, JSE._experience.journeyorchestration.stepevents.nodeName  
```


Vedi anche alcuni [esempi comunemente utilizzati per eseguire query sugli eventi dei passaggi del Percorso](../reports/query-examples.md).

Scopri come [risolvere i problemi relativi ai tipi di evento eliminati in percorsi_step_events](../reports/sharing-field-list.md#discarded-events).

## Set di dati dell’evento Decisioning{#ode-decisionevents}

_Nome nell&#39;interfaccia: ODE DecisionEvents (set di dati di sistema)_

Set di dati per l’acquisizione delle proposte di offerte agli utenti.

Lo schema correlato è ODE DecisionEvents.

Questa query mostra tutte le offerte restituite il giorno precedente:

```sql
SELECT date_format(Decision.Timestamp, 'MM/dd/yyyy') as Date
,HOUR(Decision.timestamp) as Hour
,COUNT(*)  as Count
FROM ode_decisionevents_b699fa78_efec_41b1_99fa_78efecc1b1ef_decision AS Decision
WHERE date_format(Decision.timestamp, 'MM/dd/yyyy') = date_format(CURRENT_DATE, 'MM/dd/yyyy') and Decision._experience.decisioning.propositionDetails.activity[0].id = 'xcore:offer-activity:13ab41890a335ad6'
GROUP BY date_format(Decision.Timestamp, 'MM/dd/yyyy')
,HOUR(Decision.timestamp)
ORDER BY 1, 2 DESC;
```

Questa query mostra il numero di offerte proposte negli ultimi 30 giorni di una particolare attività/decisione e la relativa priorità di offerta.

```sql
select proposedOffers.id,proposedOffers.name, po._experience.decisioning.ranking.priority, count(proposedOffers.id) as ProposedCount from (
select explode(propositionexplode.selections) AS proposedOffers from
(select explode(_experience.decisioning.propositionDetails) AS propositionexplode,timestamp FROM ode_decisionevents_itca_decisioning_20230925_235340_379  where date_format(timestamp, 'MM/dd/yyyy') >= date_format(DATE_ADD(CURRENT_DATE, -30), 'MM/dd/yyyy') and _experience.decisioning.propositionDetails.activity[0].id = 'xcore:offer-activity:12ae6f35a055c6f0')) a, decision_object_repository_personalized_offers po where proposedOffers.id LIKE 'xcore:personalized-offer%' and po._id=proposedOffers.id
group by proposedOffers.id, proposedOffers.name, po._experience.decisioning.ranking.priority;
```

<!--
## Consent Service Dataset{#consent-service-dataset}

_Name in the interface: CJM Consent Service Dataset (system dataset)_

Dataset for Journey Optimizer Consent service.

The related schema is CJM Consent Service Schema.

Query to list email IDs that have consented to receive email:

```sql
select key as email FROM (
  select explode(value) FROM (
  select explode(consents.idSpecific)
  from cjm_consent_service_dataset
 )
)
where value.marketing.email.val == 'y'
```

Query to return consent value for an email ID where email ID would be the input:

```sql
select value.marketing.email.val FROM (
  select explode(value) FROM (
  select explode(consents.idSpecific)
  from cjm_consent_service_dataset
 )
```
-->

## Set di dati evento feedback Ccn{#bcc-feedback-event-dataset}

_Nome nell&#39;interfaccia: Set di dati evento feedback Ccn AJO (set di dati di sistema)_

Set di dati per memorizzare informazioni per messaggi Ccn.

Eseguire una query per tutti i messaggi Ccn entro 2 giorni (per una determinata campagna):

```sql
SELECT bcc.*
FROM ajo_bcc_feedback_event_dataset AS bcc
WHERE 
    bcc._experience.customerJourneyManagement.messageExecution.messageExecutionID = '<message-execution-id>' AND 
    bcc.timestamp >= now() - INTERVAL '2' day; 
```

Esegui una query con set di dati di feedback per mostrare gli utenti che non hanno ricevuto (tutti i mancati recapiti e le eliminazioni) e che dispongono di voci Ccn per un particolare messaggio:

```sql
SELECT 
    distinct bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress AS OriginalRecipientAddress 
FROM ajo_bcc_feedback_event_dataset  AS bcc 
WHERE 
    bcc.timestamp > now() - INTERVAL '2' DAY AND     bcc._experience.customerJourneyManagement.messageExecution.messageExecutionID  = '<message-execution-id>' AND      bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress != '' AND
    ( 
            bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress NOT IN ( 
        SELECT distinct mfe._experience.customerJourneyManagement.emailChannelContext.address
        FROM ajo_message_feedback_event_dataset AS mfe 
        WHERE 
            mfe.timestamp > now() - INTERVAL '2' DAY AND 
            mfe._experience.customerJourneyManagement.messageExecution.messageExecutionID  = '<message-execution-id>' AND
            mfe._experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'sent'
        )  
    OR     bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress IN ( 
        SELECT distinct mfe._experience.customerJourneyManagement.emailChannelContext.address
        FROM ajo_message_feedback_event_dataset AS mfe 
        WHERE 
        mfe.timestamp > now() - INTERVAL '2' DAY AND 
            mfe._experience.customerJourneyManagement.messageExecution.messageExecutionID  = '<message-execution-id>' AND 
            mfe._experience.customerJourneyManagement.messageDeliveryfeedback.messageFailure.category = 'async' AND 
            mfe._experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus
```

## Set di dati di entità{#entity-dataset}

_Nome nell&#39;interfaccia: ajo_entity_dataset (set di dati di sistema)_

Set di dati per memorizzare i metadati di entità per i messaggi inviati all’utente finale.

Lo schema correlato è AJO Entity Schema.

Questo set di dati consente di accedere a metadati definiti dall’addetto al marketing, che consentono di ottenere informazioni migliori sui rapporti quando i set di dati di Journey Optimizer vengono esportati per la visualizzazione di reporting in strumenti esterni. Questo viene ottenuto utilizzando l’attributo messageID che consente di unire vari set di dati, come il set di dati di feedback sui messaggi e di tracciamento degli eventi sull’esperienza, per ottenere i dettagli di una consegna di messaggi dall’invio al tracciamento a livello di profilo.

**Note importanti**

* Una voce per un messaggio viene creata solo dopo la pubblicazione del percorso o della campagna.

* La voce potrebbe essere visualizzata 30 minuti dopo la pubblicazione della campagna/del percorso.

>[!NOTE]
>
>Per il momento, esistono due voci per ogni pubblicazione di messaggi nel set di dati di entità per motivi di compatibilità futuri. Questo non influisce sulla possibilità di utilizzare le query di unione in base alle esigenze tra set di dati per recuperare le informazioni desiderate.

Se desideri ordinare, nei rapporti, le e-mail inviate da un percorso specifico in base all’azione che le ha inviate. puoi unire il set di dati Feedback messaggio con il set di dati Entità. I campi da utilizzare sono: `_experience.decisioning.propositions.scopeDetails.correlationID` e `_id field in entity dataset`.

La query seguente ti aiuta a ottenere il modello di messaggio associato per una determinata campagna:

```sql
SELECT
  AE._experience.customerJourneyManagement.entities.channelDetails.template
from
  ajo_entity_dataset AE
    WHERE AE._experience.customerJourneyManagement.entities.campaign.campaignVersionID = 'd7a01136-b113-4ef2-8f59-b6001f7eef6e'
```

La query seguente consente di ottenere i dettagli del Percorso e l’oggetto e-mail associati a tutti gli eventi di feedback:

```sql
SELECT 
  AE._experience.customerJourneyManagement.entities.journey.journeyActionName, 
  AE._experience.customerJourneyManagement.entities.journey.journeyActionID, 
  AE._experience.customerJourneyManagement.entities.journey.journeyVersionID, 
  AE._experience.customerJourneyManagement.entities.channelDetails.email.subject 
from 
  ajo_entity_dataset AE 
  INNER JOIN ajo_message_feedback_event_dataset MF ON AE._experience.customerJourneyManagement.entities.channelDetails.messageID = MF._experience.customerJourneyManagement.messageExecution.messageID 
WHERE 
  AE._experience.customerJourneyManagement.entities.channelDetails.channel._id = 'https://ns.adobe.com/xdm/channels/email' 
  AND MF._experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' 
  AND AE._experience.customerJourneyManagement.entities.journey.journeyVersionID IS NOT NULL
```

Puoi unire gli eventi dei passaggi del percorso, il feedback dei messaggi e i set di dati di tracciamento per ottenere le statistiche per un particolare profilo:

```sql
SELECT 
  AE._experience.customerJourneyManagement.entities.journey.journeyActionName, 
  AE._experience.customerJourneyManagement.entities.journey.journeyActionID, 
  AE._experience.customerJourneyManagement.entities.journey.journeyVersionID, 
  AE._experience.customerJourneyManagement.entities.channelDetails.email.subject,
    JE._EXPERIENCE.JOURNEYORCHESTRATION.STEPEVENTS.PROFILEID,
    JE._EXPERIENCE.JOURNEYORCHESTRATION.STEPEVENTS.NODENAME
from 
  ajo_entity_dataset AE 
  INNER JOIN ajo_message_feedback_event_dataset MF 
    ON AE._experience.customerJourneyManagement.entities.channelDetails.messageID = MF._experience.customerJourneyManagement.messageExecution.messageID 
    INNER JOIN journey_step_events JE
    ON AE._experience.customerJourneyManagement.entities.journey.journeyActionID = JE._experience.journeyOrchestration.stepEvents.actionID
WHERE 
  AE._experience.customerJourneyManagement.entities.channelDetails.channel._id = 'https://ns.adobe.com/xdm/channels/email' 
  AND MF._experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' 
  AND AE._experience.customerJourneyManagement.entities.journey.journeyVersionID IS NOT NULL
```
