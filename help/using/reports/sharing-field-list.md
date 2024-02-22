---
solution: Journey Optimizer
product: journey optimizer
title: Elenco dei campi evento del passaggio
description: Elenco dei campi evento del passaggio
feature: Journeys, Reporting
topic: Content Management
role: Data Engineer, Data Architect, Admin
level: Experienced
exl-id: e96efa67-ee47-40b9-b680-f5119d8c3481
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 17%

---

# Elenco dei campi evento del passaggio {#sharing-field-list}

I campi dell’evento del passaggio sono organizzati per categoria.

* Campi delle informazioni di debug
* Campi del percorso
* Campi profilo
* Campi evento del servizio

Per l’attributo identityMap, l’identità primaria è definita per impostazione predefinita come &quot;primary = true&quot;.

## debugInfo {#debuginfo-field}

| Nome campo | Tipo | Descrizione |
|---|---|------------|
| requestId | Stringa | L’ID richiesta utilizzato da Journey Optimizer per tenere traccia del flusso di una richiesta. |

## percorso {#journey-field}

Questo gruppo di campi viene utilizzato nello schema del percorso (in relazione a journeyStepEvent). Contiene i seguenti campi:

| Nome campo | Tipo | Descrizione |
|---|---|------------|
| ID | Stringa | Identificatore per il Percorso specificato |
| VersionID | Stringa | ID della versione del percorso. Questo ID rappresenta l’identità di un percorso |
| name | Stringa | Nome del percorso |
| descrizione | Stringa | Descrizione del percorso |
| version | Stringa | versione, rappresentata come `major`.`minor` |

## profilo {#profile-field}

Questo gruppo di campi è specifico di journeyStepEvent: questo evento è in relazione con il percorso e non dispone di identityMap che descrive l’eventuale identità del profilo.

Per journeyStepEvent, è inoltre necessario aggiungere campi relativi all’identità:

| Nome campo | Tipo | Descrizione |
|---|---|------------|
| ID | Stringa | L’identificatore del profilo identifica il profilo inviato/utilizzato in un percorso. Esempio: foo@adobe.com. |
| namespace | Stringa | Questo campo descrive lo spazio dei nomi a cui fa riferimento il profilo utilizzato nel Percorso. Ad esempio: E-mail, ECID |

## serviceEvents {#servicevents-field}

Questo mixin contiene tutti i campi corrispondenti a un processo di esportazione profilo.

| Nome campo | Tipo | Descrizione |
|---|---|------------|
| ID | Stringa | Identificatore del processo di esportazione del pubblico attivato |
| stato | Stringa | Stato del processo di esportazione del pubblico: in coda, avviato, completato |
| exportCountTotal | Intero | Il valore massimo possibile del processo di esportazione del pubblico |
| exportCountRealized | Intero | Numero effettivo di tipi di pubblico esportati tramite il processo |
| exportCountFailed | Intero | Numero di tipi di pubblico non riusciti durante l’esportazione tramite il processo |
| exportSegmentID | Stringa | Identificatore del pubblico da esportare |
| eventType | Stringa | Tipo di evento che indica se si tratta di un evento di errore di evento informazioni: Info, Error |
| eventCode | Stringa | Codice di errore che indica il motivo del tipo di evento corrispondente |

## stepEvents {#stepevents-field}

Questa categoria contiene i campi dell’evento del passaggio originale. Consulta questa [sezione](../reports/sharing-legacy-fields.md).
