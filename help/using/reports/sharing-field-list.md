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
source-git-commit: c517e7faa027b5c1fe3b130f45fc7bf5020c454a
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 10%

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

Ulteriori informazioni sui tipi di evento [ in questa sezione](#discarded-events).

## stepEvents {#stepevents-field}

Questa categoria contiene i campi dell’evento del passaggio originale. Consulta questa [sezione](../reports/sharing-legacy-fields.md).


## Risolvere i problemi relativi ai tipi di evento scartati in percorsi_step_events  {#discarded-events}

Quando si esegue una query su percorsi_step_events per i record con `eventCode = 'discard'`, è possibile che si verifichino diversi eventTypes.

Di seguito sono riportate le definizioni, le cause comuni e i passaggi di risoluzione dei problemi per i tipi di evento di eliminazione più frequenti:

* EXTERNAL_KEY_COMPUTATION_ERROR: impossibile calcolare un identificatore univoco (chiave esterna) per il cliente dai dati dell&#39;evento.
Cause comuni: identificatori cliente mancanti o non validi (ad esempio e-mail, ID cliente) nel payload dell’evento.
Risoluzione dei problemi: controlla la configurazione dell’evento per gli identificatori richiesti, assicurati che i dati dell’evento siano completi e formattati correttamente.
* NO_INTEREST_PERCORSI_FOR_SEGMENTMEMBERSHIP_EVENT: È stato ricevuto un evento di qualificazione del segmento, ma non sono configurati percorsi per rispondere a questo segmento.
Cause comuni: nessun percorso utilizza il segmento come attivatore, i percorsi sono in stato di bozza/interruzione o gli ID del segmento non corrispondono.
Risoluzione dei problemi: assicurati che almeno un percorso sia attivo e configurato per il segmento e verifica gli ID del segmento.
* PERCORSI_INSTANCE_ID_NOT_CREATE: Impossibile creare un&#39;istanza di percorso per il cliente.
Cause comuni: eventi duplicati, volume di eventi elevato, vincoli delle risorse di sistema.
Risoluzione dei problemi: implementa la deduplicazione, evita picchi di traffico, ottimizza la progettazione del percorso e, se persistente, contatta il supporto.
* EVENT_WITH_NO_PERCORSI: è stato ricevuto un evento ma non è configurato alcun percorso attivo per rispondervi.
Cause comuni: mancata corrispondenza nome evento/ID, percorso non pubblicato, sandbox/org errata, mancata corrispondenza modalità di test/profilo.
Risoluzione dei problemi: verifica la configurazione di eventi e percorsi, controlla lo stato del percorso e utilizza gli strumenti di debug.

Per i rigetti che si verificano nei percorsi in pausa:

* PAUSED_PERCORSI_VERSION: Ignora gli eventi che si sono verificati nel punto di ingresso del percorso

* PERCORSI_IN_PAUSED_STATE: ignora l&#39;evento che si è verificato quando i profili si trovano in un percorso

Per ulteriori informazioni su questi eventi e su come risolverli, consulta la sezione [Sospendere un Percorso](../building-journeys/journey-pause.md#troubleshoot-profile-discards-in-paused-journeys).

## Risorse aggiuntive

* [Esempi di query del set di dati - Evento passaggio Percorso](../data/datasets-query-examples.md#journey-step-event).
* [Esempi di query - Query basate su eventi](query-examples.md#event-based-queries).
* [Dizionario schemi incorporato](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=it)

