---
solution: Journey Optimizer
product: journey optimizer
title: Esempi di query del set di dati
description: Esempi di query del set di dati
feature: Reporting
topic: Content Management
role: User
level: Intermediate
keywords: set di dati, ottimizzatore, casi d’uso
exl-id: 26ba8093-8b6d-4ba7-becf-b41c9a06e1e8
source-git-commit: 4c0508d415630ca4a74ec30e5b43a3bfe7fd8a4f
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 0%

---

# Casi d’uso del set di dati {#tracking-datasets}

In questa pagina trovi l’elenco dei set di dati Adobe Journey Optimizer e dei relativi casi di utilizzo:

[Set di dati evento esperienza tracciamento e-mail](#email-tracking-experience-event-dataset)
[Set di dati evento del feedback del messaggio](#message-feedback-event-dataset)
[Set di dati evento esperienza tracciamento push](#push-tracking-experience-event-dataset)
[Evento passaggio percorso](#journey-step-event)
[Decisioning del set di dati evento](#ode-decisionevents)
[Set di dati del servizio di consenso](#consent-service-dataset)
[Set di dati evento feedback CCN](#bcc-feedback-event-dataset)
[Set di dati di entità](#entity-dataset)

Per visualizzare l’elenco completo dei campi e degli attributi di ogni schema, consulta la [Dizionario dello schema Journey Optimizer](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html){target="_blank"}.

## Set di dati evento esperienza tracciamento e-mail{#email-tracking-experience-event-dataset}

_Nome nell’interfaccia : Set di dati evento esperienza di tracciamento e-mail CJM_

Set di dati di sistema per l’acquisizione di eventi di esperienza di tracciamento e-mail da Journey Optimizer.

Lo schema correlato è lo schema evento esperienza di tracciamento e-mail di CJM.

Questa query mostra il numero di diverse interazioni e-mail (aperture, clic) per un messaggio specifico:

```sql
select
    _experience.customerJourneyManagement.messageInteraction.interactionType AS interactionType,
    count(1) eventCount
from cjm_email_tracking_experience_event_dataset
where
     _experience.customerJourneyManagement.messageExecution.messageExecutionID IN ('UMA-30647505')
group by
    _experience.customerJourneyManagement.messageInteraction.interactionType
```

Questa query mostra il raggruppamento del numero di interazioni e-mail diverse (aperture, clic) per messaggio per un dato percorso:

```sql
select
    _experience.customerJourneyManagement.messageExecution.messageExecutionID AS messageExecutionID,
    _experience.customerJourneyManagement.messageInteraction.interactionType AS interactionType,
    count(1) eventCount
from cjm_email_tracking_experience_event_dataset
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

## Set di dati evento del feedback del messaggio{#message-feedback-event-dataset}

_Nome nell’interfaccia: Set di dati evento feedback del messaggio CJM_

Set di dati per l’acquisizione di eventi di feedback delle applicazioni e-mail e push da Journey Optimizer.

Lo schema correlato è lo schema Evento di feedback del messaggio CJM.

Questa query mostra il numero di diversi stati di feedback e-mail (inviati, non recapitati, ecc.) per un dato messaggio:

```sql
select
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus AS feedbackStatus,
    count(1) eventCount
from cjm_message_feedback_event_dataset
where
     _experience.customerJourneyManagement.messageExecution.messageExecutionID IN ('UMA-30647505')
group by
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus;
```

Questa query mostra il raggruppamento dei conteggi dei diversi stati di feedback via e-mail (inviati, non recapitati, ecc.) per messaggio per un dato percorso:

```sql
select
    _experience.customerJourneyManagement.messageExecution.messageExecutionID AS messageExecutionID,
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus AS feedbackStatus,
    count(1) eventCount
from cjm_message_feedback_event_dataset
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

A livello aggregato, rapporto a livello di dominio (ordinato per domini principali): Nome di dominio, messaggio inviato, rimbalzi

```sql
SELECT split_part(_experience.customerJourneyManagement.emailChannelContext.address, '@', 2) AS recipientDomain, SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' THEN 1 ELSE 0 END)AS sentCount , SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'bounce' THEN 1 ELSE 0 END )AS bounceCount FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY recipientDomain ORDER BY sentCount DESC;
```

L’e-mail invia su base giornaliera:

```sql
SELECT date_trunc('day', TIMESTAMP) AS rolluptimestamp, SUM( CASE WHEN _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'sent' THEN 1 ELSE 0 END) AS deliveredcount FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY date_trunc('day', TIMESTAMP) ORDER BY rolluptimestamp ASC;
```

Trova se un particolare ID e-mail ha ricevuto o meno un’e-mail e, in caso contrario, qual è stato l’errore, la categoria di rimbalzo, il codice:

```sql
SELECT _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus AS status, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type AS bouncetype FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' AND _experience.customerjourneymanagement.emailchannelcontext.address = 'user@domain.com' AND TIMESTAMP >= now() - INTERVAL '7' DAY ORDER BY status ASC
```

Trova l’elenco di tutti i singoli ID e-mail che hanno generato un errore, una categoria di messaggi non recapitati o un codice negli ultimi x ore/giorni o associati a una particolare consegna del messaggio:

```sql
SELECT _experience.customerjourneymanagement.emailchannelcontext.address AS emailid, _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus AS status, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type AS bouncetype FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' AND _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus != 'sent' AND TIMESTAMP >= now() - INTERVAL '10' HOUR AND _experience.customerjourneymanagement.messageexecution.messageexecutionid = 'BMA-45237824' ORDER BY emailid
```

Frequenza di rimbalzo duro a livello aggregato:

```sql
select hardBounceCount, case when sentCount > 0 then(hardBounceCount/sentCount)*100.0 else 0 end as hardBounceRate from ( select SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'bounce' AND _experience.customerJourneyManagement.messageDeliveryfeedback.messageFailure.type = 'Hard' THEN 1 ELSE 0 END)AS hardBounceCount , SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' THEN 1 ELSE 0 END )AS sentCount from cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' )
```

Errori permanenti raggruppati per codice non recapitato:

```sql
SELECT _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, COUNT(*) AS hardbouncecount FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'bounce' AND _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type = 'Hard' AND _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY failurereason
```

### Identificare gli indirizzi messi in quarantena dopo un’interruzione dell’ISP{#isp-outage-query}

In caso di interruzione di un provider di servizi Internet (ISP), è necessario identificare gli indirizzi e-mail erroneamente contrassegnati come non recapitati (messi in quarantena) per domini specifici, durante un intervallo di tempo. Per ottenere questi indirizzi, utilizza la seguente query:

```sql
SELECT
    _experience.customerJourneyManagement.emailChannelContext.address AS RecipientAddress,
    timestamp AS EventTime,
    _experience.customerJourneyManagement.messageDeliveryfeedback.messageFailure.reason AS "Invalid Recipient"
FROM cjm_message_feedback_event_dataset
WHERE
    eventtype = 'message.feedback' AND
    DATE(timestamp) BETWEEN '<start-date-time>' AND '<end-date-time>' AND
    _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'bounce' AND
    _experience.customerJourneyManagement.emailChannelContext.address ILIKE '%domain.com%'
ORDER BY timestamp DESC;
```

se il formato delle date è: AAAA-MM-GG HH:MM:SS.

Una volta identificati, rimuovi tali indirizzi dall’elenco di soppressione di Journey Optimizer. [Maggiori informazioni](../configuration/manage-suppression-list.md#remove-from-suppression-list).

## Set di dati evento esperienza tracciamento push {#push-tracking-experience-event-dataset}

_Nome nell’interfaccia: Dataset dell’evento esperienza di tracciamento push CJM_

Set di dati per l’acquisizione di eventi di esperienza di tracciamento mobile per il push da Journey Optimizer.

Lo schema correlato è lo schema evento esperienza di tracciamento push di CJM.

Esempio di query:

```sql
select _experience.customerJourneyManagement.pushChannelContext.platform, sum(pushNotificationTracking.customAction.value)  from cjm_push_tracking_experience_event_dataset
group by _experience.customerJourneyManagement.pushChannelContext.platform

select  _experience.customerJourneyManagement.pushChannelContext.platform, SUM (_experience.customerJourneyManagement.messageInteraction.offers.offerCount) from cjm_email_tracking_experience_event_dataset
  group by _experience.customerJourneyManagement.pushChannelContext.platform
```

## Evento passaggio percorso{#journey-step-event}

_Nome interno: Eventi dei passaggi del percorso (set di dati di sistema)_

Set di dati per l’acquisizione di eventi passaggio nel percorso.

Lo schema correlato è lo schema Evento passaggio Percorso per Journey Orchestration.

Questa query mostra la suddivisione dei conteggi di successo delle azioni per etichetta di azione per un dato percorso:

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

Questa query mostra la suddivisione dei conteggi immessi per nodeId e nodeLabel per un determinato percorso. nodeId è incluso qui come nodeLabel può essere lo stesso per nodi di percorso diversi.

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

## Decisioning del set di dati evento{#ode-decisionevents}

_Nome nell’interfaccia: ODE DecisionEvents (set di dati di sistema)_

Set di dati per l’acquisizione delle proposte di offerta per gli utenti.

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

Questa query mostra il numero di volte in cui sono state proposte offerte negli ultimi 30 giorni di una particolare attività/decisione e la relativa priorità di offerta.

```sql
select proposedOffers.id,proposedOffers.name, po._experience.decisioning.ranking.priority, count(proposedOffers.id) as ProposedCount from (
select explode(propositionexplode.selections) AS proposedOffers from
(select explode(_experience.decisioning.propositionDetails) AS propositionexplode,timestamp FROM ode_decisionevents_itca_decisioning_20200925_235340_379  where date_format(timestamp, 'MM/dd/yyyy') >= date_format(DATE_ADD(CURRENT_DATE, -30), 'MM/dd/yyyy') and _experience.decisioning.propositionDetails.activity[0].id = 'xcore:offer-activity:12ae6f35a055c6f0')) a, decision_object_repository_personalized_offers po where proposedOffers.id LIKE 'xcore:personalized-offer%' and po._id=proposedOffers.id
group by proposedOffers.id, proposedOffers.name, po._experience.decisioning.ranking.priority;
```

## Set di dati del servizio di consenso{#consent-service-dataset}

_Nome nell’interfaccia: Set di dati del servizio Consent CJM (set di dati di sistema)_

Set di dati per il servizio Journey Optimizer Consent.

Lo schema correlato è lo schema del servizio di consenso CJM.

Invia una query per elencare gli ID e-mail che hanno acconsentito alla ricezione di un’e-mail:

```sql
select key as email FROM (
  select explode(value) FROM (
  select explode(consents.idSpecific)
  from cjm_consent_service_dataset
 )
)
where value.marketing.email.val == 'y'
```

Query per restituire il valore di consenso per un ID e-mail in cui l’ID e-mail sarebbe l’input:

```sql
select value.marketing.email.val FROM (
  select explode(value) FROM (
  select explode(consents.idSpecific)
  from cjm_consent_service_dataset
 )
```

## Set di dati evento feedback CCN{#bcc-feedback-event-dataset}

_Nome nell’interfaccia: Set di dati dell’evento del feedback CCN AJO (set di dati di sistema)_

Set di dati per memorizzare le informazioni per i messaggi CCN.

Esegui una query per tutti i messaggi CCN entro 2 giorni (per una particolare campagna):

```sql
SELECT bcc.*
FROM ajo_bcc_feedback_event_dataset AS bcc
WHERE 
    bcc._experience.customerJourneyManagement.messageExecution.messageExecutionID = '<message-execution-id>' AND 
    bcc.timestamp >= now() - INTERVAL '2' day; 
```

Effettua una query con set di dati di feedback per mostrare agli utenti che non hanno ricevuto (tutti i messaggi non recapitati e cancellati) e che hanno una voce CCN per un particolare messaggio:

```sql
SELECT 
    distinct bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress AS OriginalRecipientAddress 
FROM ajo_bcc_feedback_event_dataset  AS bcc 
WHERE 
    bcc.timestamp > now() - INTERVAL '2' DAY AND     bcc._experience.customerJourneyManagement.messageExecution.messageExecutionID  = '<message-execution-id>' AND      bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress != '' AND
    ( 
            bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress NOT IN ( 
        SELECT distinct mfe._experience.customerJourneyManagement.emailChannelContext.address
        FROM cjm_message_feedback_event_dataset AS mfe 
        WHERE 
            mfe.timestamp > now() - INTERVAL '2' DAY AND 
            mfe._experience.customerJourneyManagement.messageExecution.messageExecutionID  = '<message-execution-id>' AND
            mfe._experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'sent'
        )  
    OR     bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress IN ( 
        SELECT distinct mfe._experience.customerJourneyManagement.emailChannelContext.address
        FROM cjm_message_feedback_event_dataset AS mfe 
        WHERE 
        mfe.timestamp > now() - INTERVAL '2' DAY AND 
            mfe._experience.customerJourneyManagement.messageExecution.messageExecutionID  = '<message-execution-id>' AND 
            mfe._experience.customerJourneyManagement.messageDeliveryfeedback.messageFailure.category = 'async' AND 
            mfe._experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus
```

## Set di dati di entità{#entity-dataset}

_Nome nell’interfaccia: ajo_entity_dataset (set di dati di sistema)_

Set di dati per memorizzare i metadati delle entità per i messaggi inviati all’utente finale.

Lo schema correlato è lo schema di entità AJO.

Questo set di dati consente di accedere ai metadati definiti dall’addetto al marketing, che consentono di ottenere migliori informazioni sui rapporti quando i set di dati Journey Optimizer vengono esportati per la visualizzazione dei rapporti in strumenti esterni. Questo si ottiene utilizzando l’attributo messageID che consente di unire vari set di dati come set di dati di feedback dei messaggi e set di dati di tracciamento degli eventi di esperienza per ottenere i dettagli di una consegna dei messaggi dall’invio al tracciamento a livello di profilo.

**Note importanti**

* Una voce per un messaggio viene creata solo dopo la pubblicazione del percorso o della campagna.

* È possibile visualizzare la voce 30 minuti dopo la pubblicazione della campagna/percorso.

>[!NOTE]
>
>Al momento, per motivi di compatibilità futuri, nel set di dati di entità sono presenti due voci per ogni pubblicazione di messaggi. Questo non influisce sulla capacità di utilizzare le query di join in base alle esigenze tra i set di dati per recuperare le informazioni desiderate.

Se desideri ordinare nei rapporti le e-mail inviate da un percorso specifico in base all’azione che le ha inviate. puoi unire il set di dati Feedback per i messaggi con il set di dati di entità. I campi da utilizzare sono: `_experience.decisioning.propositions.scopeDetails.correlationID` e `_id field in entity dataset`.

La seguente query ti aiuta a ottenere il modello di messaggio associato per una determinata campagna:

```sql
SELECT
  AE._experience.customerJourneyManagement.entities.channelDetails.template
from
  ajo_entity_dataset AE
    WHERE AE._experience.customerJourneyManagement.entities.campaign.campaignVersionID = 'd7a01136-b113-4ef2-8f59-b6001f7eef6e'
```

La seguente query aiuta a ottenere i dettagli del Percorso e l’oggetto e-mail associati a tutti gli eventi di feedback:

```sql
SELECT 
  AE._experience.customerJourneyManagement.entities.journey.journeyActionName, 
  AE._experience.customerJourneyManagement.entities.journey.journeyActionID, 
  AE._experience.customerJourneyManagement.entities.journey.journeyVersionID, 
  AE._experience.customerJourneyManagement.entities.channelDetails.email.subject 
from 
  ajo_entity_dataset AE 
  INNER JOIN cjm_message_feedback_event_dataset MF ON AE._experience.customerJourneyManagement.entities.channelDetails.messageID = MF._experience.customerJourneyManagement.messageExecution.messageID 
WHERE 
  AE._experience.customerJourneyManagement.entities.channelDetails.channel._id = 'https://ns.adobe.com/xdm/channels/email' 
  AND MF._experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' 
  AND AE._experience.customerJourneyManagement.entities.journey.journeyVersionID IS NOT NULL
```

Puoi unire gli eventi dei passaggi di percorso, il feedback dei messaggi e i set di dati di tracciamento per ottenere gli stati di un particolare profilo:

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
  INNER JOIN cjm_message_feedback_event_dataset MF 
    ON AE._experience.customerJourneyManagement.entities.channelDetails.messageID = MF._experience.customerJourneyManagement.messageExecution.messageID 
    INNER JOIN journey_step_events JE
    ON AE._experience.customerJourneyManagement.entities.journey.journeyActionID = JE._experience.journeyOrchestration.stepEvents.actionID
WHERE 
  AE._experience.customerJourneyManagement.entities.channelDetails.channel._id = 'https://ns.adobe.com/xdm/channels/email' 
  AND MF._experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' 
  AND AE._experience.customerJourneyManagement.entities.journey.journeyVersionID IS NOT NULL
```
