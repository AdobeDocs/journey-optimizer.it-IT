---
solution: Journey Optimizer
product: journey optimizer
title: Elenco dei campi evento del passaggio
description: Elenco dei campi evento del passaggio
feature: Journeys, Reporting
topic: Content Management
role: Engineer, Admin
level: Experienced
exl-id: e96efa67-ee47-40b9-b680-f5119d8c3481
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '649'
ht-degree: 9%

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

Questo mixin contiene tutti i campi corrispondenti a un processo di esportazione profilo. Questi eventi vengono generati per ogni attività **Read Audience** per tenere traccia del ciclo di vita delle operazioni di esportazione del pubblico (in coda, avviato, completato, errori). A differenza degli eventi dei passaggi regolari, serviceEvents non sono legati a singoli profili ma al nodo Read Audience stesso, il che significa che potrebbero non avere un identificatore di profilo associato.

| Nome campo | Tipo | Descrizione |
|---|---|------------|
| ID | Stringa | Identificatore del processo di esportazione del pubblico attivato |
| stato | Stringa | Stato del processo di esportazione del pubblico: in coda, avviato, completato |
| exportCountTotal | Intero | Il valore massimo possibile del processo di esportazione del pubblico |
| exportCountRealized | Intero | Numero effettivo di tipi di pubblico esportati tramite il processo |
| exportCountFailed | Intero | Numero di tipi di pubblico non riusciti durante l’esportazione tramite il processo |
| exportSegmentID | Stringa | Identificatore del pubblico da esportare |
| eventType | Stringa | Tipo di evento che indica se si tratta di un evento di errore o di un evento di informazioni: Info, Error |
| eventCode | Stringa | Codice di errore che indica il motivo del tipo di evento corrispondente |

Ulteriori informazioni sui tipi di evento [&#x200B; in questa sezione](#discarded-events).

## stepEvents {#stepevents-field}

Questa categoria contiene i campi dell’evento del passaggio originale. Consulta questa [sezione](../reports/sharing-legacy-fields.md).


## Risolvere i problemi relativi ai tipi di evento scartati negli eventi dei passaggi del Percorso  {#discarded-events}

Quando si esegue una query sugli eventi dei passaggi di percorso per i record con `eventCode = 'discard'`, è possibile che si verifichino diversi eventTypes.

Di seguito sono riportate le definizioni, le cause comuni e i passaggi di risoluzione dei problemi per l&#39;eliminazione più frequente `eventTypes`:

* **EXTERNAL_KEY_COMPUTATION_ERROR**: impossibile calcolare un identificatore univoco (chiave esterna) per il cliente dai dati dell&#39;evento.

  **Cause comuni**: identificatori cliente mancanti o non validi (ad esempio e-mail, ID cliente) nel payload dell&#39;evento.

  **Risoluzione dei problemi**: controlla la configurazione dell&#39;evento per gli identificatori richiesti, assicurati che i dati dell&#39;evento siano completi e formattati correttamente.

* **NO_INTEREST_PERCORSI_FOR_SEGMENTMEMBERSHIP_EVENT**: È stato ricevuto un evento di qualificazione del segmento, ma non sono configurati percorsi per rispondere a questo segmento.

  **Cause comuni**: nessun percorso utilizza il segmento come attivatore, i percorsi sono in stato di bozza/interruzione o gli ID del segmento non corrispondono.

  **Risoluzione dei problemi**: assicurati che almeno un percorso sia attivo e configurato per il segmento, verifica gli ID segmento.

* **PERCORSI_INSTANCE_ID_NOT_CREATE**: impossibile creare un&#39;istanza di percorso per il cliente.

  **Cause comuni**: eventi duplicati, volume di eventi elevato, vincoli delle risorse di sistema.

  **Risoluzione dei problemi**: implementa la deduplicazione, evita i picchi di traffico, ottimizza la progettazione del percorso, contatta il supporto se persiste.

* **EVENT_WITH_NO_PERCORSI**: è stato ricevuto un evento ma nessun percorso attivo è configurato per rispondere

  **Cause comuni**: mancata corrispondenza nome evento/ID, percorso non pubblicato, sandbox/organizzazione errata, mancata corrispondenza modalità test/profilo.

  **Risoluzione dei problemi**: verificare la configurazione di eventi e percorsi, controllare lo stato del percorso e utilizzare gli strumenti di debug.

* Per i rigetti che si verificano nei percorsi in pausa:

   * **PAUSED_PERCORSI_VERSION**: ignoramenti verificatisi nel punto di ingresso del percorso
   * **PERCORSO_IN_PAUSED_STATE**: ignora ciò che si è verificato quando i profili si trovano in un percorso

  Per ulteriori informazioni su questi eventi e su come risolverli, consulta la sezione [Sospendere un Percorso](../building-journeys/journey-pause.md#troubleshoot-profile-discards-in-paused-journeys).

## Risorse aggiuntive

* [Esempi di query del set di dati - Evento passaggio Percorso](../data/datasets-query-examples.md#journey-step-event).
* [Esempi di query - Query basate su eventi](query-examples.md#event-based-queries).
* [Dizionario schemi incorporato](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=it)

