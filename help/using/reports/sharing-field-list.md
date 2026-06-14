---
solution: Journey Optimizer
product: journey optimizer
title: Elenco dei campi evento del passaggio
description: Elenco dei campi evento del passaggio
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: e96efa67-ee47-40b9-b680-f5119d8c3481
TQID: https://experienceleague.adobe.com/7sYxw--oKKa6SnRgoXnwFxme5n-6L4pe9SR-AKZOmHA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a9f73820-6899-47c2-a597-3fec28ab756a
  - id: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
subfeature_v2:
  - id: d145add9-d5b9-481b-aa8a-e15e6bb7f813
  - id: a7289281-9ae4-47b1-b8cf-4028b98af776
  - id: b5afe8bf-bda6-41b5-ba06-922638872d63
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: 7f28f19b11ead867b0851943fdd997dcc3af170b
workflow-type: tm+mt
source-wordcount: 806
ht-degree: 8%

---

# Elenco dei campi evento del passaggio {#sharing-field-list}

>[!BEGINSHADEBOX]

**In questa pagina:** Fai riferimento ai campi dell&#39;evento del passaggio di percorso organizzati per categoria, inclusi i campi dell&#39;evento di debug, di percorso, di profilo e di servizio, nonché alla risoluzione dei problemi relativi ai tipi di evento scartati.

>[!ENDSHADEBOX]

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

* **PERCORSI_INSTANCE_ID_NOT_CREATED**: impossibile creare un&#39;istanza di percorso per il cliente.

  **Cause comuni**: eventi duplicati, volume di eventi elevato, vincoli delle risorse di sistema.

  **Risoluzione dei problemi**: implementa la deduplicazione, evita i picchi di traffico, ottimizza la progettazione del percorso, [contatta l&#39;assistenza](../start/user-interface.md#support-ticket-guidelines) se persiste.

* **maxInstanceStackEventsReached**: il runtime del percorso ha raggiunto il limite interno di 10 eventi per stack di eventi per profilo per una determinata versione del percorso.

  **Cause comuni**: l&#39;istanza di percorso del profilo è bloccata in un passaggio di lunga durata (ad esempio, lunghe attese, arricchimenti lenti o nuovi tentativi di azione personalizzati) e gli eventi per lo stesso profilo, utilizzati anche in tale percorso, si accumulano oltre il limite di 10 eventi.

  **Risoluzione dei problemi**: riduci i passaggi a lungo termine sui percorsi che possono riattivarsi frequentemente, annullare o deduplicare eventi a monte e suddividere scenari lunghi in più percorsi. Questo è un guardrail di sicurezza e il limite non è configurabile; gli eventi aggiuntivi vengono scartati fino allo scarico dello stack. Per ulteriori informazioni, vedere [Eventi eliminati a causa di un&#39;istanza di percorso bloccata](../building-journeys/troubleshooting-execution.md#max-instance-stack-events-reached).

* **EVENT_WITH_NO_PERCORSI**: è stato ricevuto un evento ma nessun percorso attivo è configurato per rispondere

  **Cause comuni**: mancata corrispondenza nome evento/ID, percorso non pubblicato, sandbox/organizzazione errata, mancata corrispondenza modalità test/profilo.

  **Risoluzione dei problemi**: verificare la configurazione di eventi e percorsi, controllare lo stato del percorso e utilizzare gli strumenti di debug.

* Per i rigetti che si verificano nei percorsi in pausa:

   * **PAUSED_PERCORSI_VERSION**: ignoramenti verificatisi nel punto di ingresso del percorso
   * **PERCORSO_IN_PAUSED_STATE**: ignora ciò che si è verificato quando i profili si trovano in un percorso

  Per ulteriori informazioni su questi eventi e su come risolverli, consulta la sezione [Sospendere un Percorso](../building-journeys/journey-pause.md#discards-troubleshoot).

## Risorse aggiuntive

* [Esempi di query del set di dati - Evento passaggio Percorso](../data/datasets-query-examples.md#journey-step-event).
* [Esempi di query - Query basate su eventi](query-examples.md#event-based-queries).
* [Esempi di query - Query di regole business](query-examples.md#business-rules-queries).
* [Dizionario schemi incorporato](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=it)

