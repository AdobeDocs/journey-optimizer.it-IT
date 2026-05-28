---
solution: Journey Optimizer
product: journey optimizer
title: Schema di esportazione dei messaggi di AJO
description: Scopri i campi disponibili nel set di dati di esportazione dei messaggi di AJO
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: esportazione, messaggi, set di dati, schema, e-mail, SMS
feature_v2: []
subfeature_v2:
  - id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 420
ht-degree: 3%

---

# Schema di esportazione dei messaggi di AJO {#ajo-message-export-schema}

Quando l&#39;esportazione dei messaggi **1&rbrace; è abilitata in una configurazione del canale e-mail o SMS, il contenuto del messaggio inviato viene scritto nel** set di dati esportazione messaggi di AJO **in [!DNL Adobe Experience Platform].**

In questa sezione sono elencati i campi disponibili nel set di dati esportato.

## Campi del set di dati

+++ _experience

**Campo:** `_experience`\
**Tipo:** oggetto

+++

+++ _experience > customerJourneyManagement

**Campo:** `customerJourneyManagement`\
**Tipo:** oggetto

+++

+++ _experience > customerJourneyManagement > messageDeliveryMetadata

**Campo:** `messageDeliveryMetadata`\
**Tipo:** oggetto

+++

+++ _experience > customerJourneyManagement > messageDeliveryMetadata > emailMetadata

**Campo:** `emailMetadata`\
**Tipo:** oggetto

* destinatario

  **Campo:** `recipient`\
  **Tipo:** oggetto

   * ccn

     **Campo:** `bcc`\
     **Tipo:** array di stringhe

   * cc

     **Campo:** `cc`\
     **Tipo:** array di stringhe

   * e-mail

     **Campo:** `email`\
     **Tipo:** stringa

   * name

     **Campo:** `name`\
     **Tipo:** stringa

* mittente

  **Campo:** `sender`\
  **Tipo:** oggetto

   * e-mail

     **Campo:** `email`\
     **Tipo:** stringa

   * errorEmail

     **Campo:** `errorEmail`\
     **Tipo:** stringa

   * name

     **Campo:** `name`\
     **Tipo:** stringa

   * replyToEmail

     **Campo:** `replyToEmail`\
     **Tipo:** stringa

   * replyToName

     **Campo:** `replyToName`\
     **Tipo:** stringa

+++

+++ _experience > customerJourneyManagement > messageDeliveryMetadata > smsMetadata

**Campo:** `smsMetadata`\
**Tipo:** oggetto

* destinatario

  **Campo:** `recipient`\
  **Tipo:** oggetto

   * numero

     **Campo:** `number`\
     **Tipo:** stringa

* mittente

  **Campo:** `sender`\
  **Tipo:** oggetto

   * numeri

     **Campo:** `numbers`\
     **Tipo:** array di stringhe

+++

+++ _experience > customerJourneyManagement > messageExecution

**Campo:** `messageExecution`\
**Tipo:** oggetto

* pubblico

  **Campo:** `audience`\
  **Tipo:** oggetto

   * ID

     **Campo:** `id`\
     **Tipo:** stringa

   * tipo

     **Campo:** `type`\
     **Tipo:** stringa

* fragmentPublicationIDs

  **Campo:** `fragmentPublicationIDs`\
  **Tipo:** array di stringhe

* metadati

  **Campo:** `metadata`\
  **Tipo:** mappa

   * [Chiave mappa]

     **Tipo:** stringa

* parentSourceMeta

  **Campo:** `parentSourceMeta`\
  **Tipo:** oggetto

   * sourceActionID

     **Campo:** `sourceActionID`\
     **Tipo:** stringa

   * sourceID

     **Campo:** `sourceID`\
     **Tipo:** stringa

   * sourceType

     **Campo:** `sourceType`\
     **Tipo:** stringa

   * sourceVersionID

     **Campo:** `sourceVersionID`\
     **Tipo:** stringa

* batchInstanceID

  **Campo:** `batchInstanceID`\
  **Tipo:** stringa

* campaignActionID

  **Campo:** `campaignActionID`\
  **Tipo:** stringa

* campaignID

  **Campo:** `campaignID`\
  **Tipo:** stringa

* campaignVersionID

  **Campo:** `campaignVersionID`\
  **Tipo:** stringa

* journeyActionID

  **Campo:** `journeyActionID`\
  **Tipo:** stringa

* journeyVersionID

  **Campo:** `journeyVersionID`\
  **Tipo:** stringa

* journeyVersionInstanceID

  **Campo:** `journeyVersionInstanceID`\
  **Tipo:** stringa

* journeyVersionNodeID

  **Campo:** `journeyVersionNodeID`\
  **Tipo:** stringa

* messageExecutionID

  **Campo:** `messageExecutionID`\
  **Tipo:** stringa

* messageID

  **Campo:** `messageID`\
  **Tipo:** stringa

* messagePublicationID

  **Campo:** `messagePublicationID`\
  **Tipo:** stringa

* messageType

  **Campo:** `messageType`\
  **Tipo:** stringa

* waveID

  **Campo:** `waveID`\
  **Tipo:** stringa

+++

+++ _experience > customerJourneyManagement > messageProfile

**Campo:** `messageProfile`\
**Tipo:** oggetto

* canale

  **Campo:** `channel`\
  **Tipo:** oggetto

   * contentTypes

     **Campo:** `contentTypes`\
     **Tipo:** array di stringhe

   * locationTypes

     **Campo:** `locationTypes`\
     **Tipo:** array di stringhe

   * metricTypes

     **Campo:** `metricTypes`\
     **Tipo:** array di stringhe

   * _id

     **Campo:** `_id`\
     **Tipo:** stringa

   * _type

     **Campo:** `_type`\
     **Tipo:** stringa

   * mediaAction

     **Campo:** `mediaAction`\
     **Tipo:** stringa

   * mediaType

     **Campo:** `mediaType`\
     **Tipo:** stringa

   * modalità

     **Campo:** `mode`\
     **Tipo:** stringa

   * referenceSource

     **Campo:** `referringSource`\
     **Tipo:** stringa

   * typeAtSource

     **Campo:** `typeAtSource`\
     **Tipo:** stringa

* isSendTimeOptimized

  **Campo:** `isSendTimeOptimized`\
  **Tipo:** booleano

* isTestExecution

  **Campo:** `isTestExecution`\
  **Tipo:** booleano

* messageProfileID

  **Campo:** `messageProfileID`\
  **Tipo:** stringa

* messageProfileTrackingID

  **Campo:** `messageProfileTrackingID`\
  **Tipo:** stringa

* requestID

  **Campo:** `requestID`\
  **Tipo:** stringa

* secondaryDimensionID

  **Campo:** `secondaryDimensionID`\
  **Tipo:** stringa

* secondaryDimensionName

  **Campo:** `secondaryDimensionName`\
  **Tipo:** stringa

* variante

  **Campo:** `variant`\
  **Tipo:** stringa

+++

+++ _experience > customerJourneyManagement > messageRenderedContent

**Campo:** `messageRenderedContent`\
**Tipo:** oggetto

* emailContent

  **Campo:** `emailContent`\
  **Tipo:** oggetto

   * html

     **Campo:** `html`\
     **Tipo:** stringa

   * oggetto

     **Campo:** `subject`\
     **Tipo:** stringa

   * testo

     **Campo:** `text`\
     **Tipo:** stringa

* smsContent

  **Campo:** `smsContent`\
  **Tipo:** oggetto

   * media

     **Campo:** `media`\
     **Tipo:** stringa

   * message

     **Campo:** `message`\
     **Tipo:** stringa

   * titolo

     **Campo:** `title`\
     **Tipo:** stringa

+++

+++ identityMap

**Campo:** `identityMap`\
**Tipo:** mappa

* [Chiave mappa]

  **Tipo:** array di oggetti

   * authenticatedState

     **Campo:** `authenticatedState`\
     **Tipo:** stringa

   * ID

     **Campo:** `id`\
     **Tipo:** stringa

   * primario

     **Campo:** `primary`\
     **Tipo:** booleano

+++

+++ eventType

**Campo:** `eventType`\
**Tipo:** stringa

+++

+++ productby

**Campo:** `producedBy`\
**Tipo:** stringa

+++

+++ timestamp

**Campo:** `timestamp`\
**Tipo:** dateTime

+++

