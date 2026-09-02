---
solution: Journey Optimizer
product: journey optimizer
title: Proprietà del percorso
description: Informazioni sulle proprietà del percorso
feature: Journeys
role: Developer
level: Experienced
keywords: percorso, espressione, editor, proprietà
exl-id: eb1ab0ed-90bd-4613-b63d-b28693947db2
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/f2FVDYuWN9tawdgRdCffwnXNXoI-e-ZAuYAaozoHd3g
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1103
ht-degree: 1%

---

# Attributi proprietà percorso {#journey-properties}

Nell&#39;[editor espressioni semplici](../conditions.md#about_condition) e nell&#39;[editor espressioni avanzate](../expression/expressionadvanced.md), nelle categorie **Evento** e **Origine dati**, è possibile accedere alla categoria **Proprietà Percorso**. Questa categoria contiene campi tecnici relativi al percorso per un determinato profilo. Si tratta delle informazioni recuperate dal sistema dai percorsi attivi, ad esempio l&#39;ID percorso, o gli errori specifici rilevati.

![](../assets/journey-properties.png)

Contiene informazioni, ad esempio, su:

* versione percorso: uid percorso, uid versione percorso, uid istanza, ecc.
* errori: recupero dati, esecuzione azione, ecc.
* passaggio corrente, ultimo passaggio corrente, ecc.
* profili scartati

  L&#39;elenco dei campi è disponibile [in questa sezione](#journey-properties-fields).

Puoi utilizzare questi campi per creare espressioni. Durante l’esecuzione del percorso, i valori vengono recuperati direttamente dal percorso.

Di seguito sono riportati alcuni esempi di casi d’uso:

* **Registra profili scartati**: puoi inviare tutti i profili esclusi da un messaggio da una regola di limitazione a un sistema di terze parti a scopo di registrazione. A questo scopo, imposta un percorso in caso di timeout ed errore e aggiungi una condizione per filtrare in base a un tipo di errore specifico, ad esempio: &quot;elimina le persone applicando una regola di limite&quot;. Puoi quindi inviare i profili eliminati a un sistema di terze parti tramite un’azione personalizzata.

* **Invia avvisi in caso di errori**: è possibile inviare una notifica a un sistema di terze parti ogni volta che si verifica un errore in un messaggio. A questo scopo, puoi impostare un percorso in caso di errore, aggiungere una condizione e un’azione personalizzata. Puoi inviare una notifica su un canale Slack, ad esempio, con la descrizione dell’errore riscontrato.

* **Perfezionare gli errori nella generazione dei rapporti**: invece di disporre di un solo percorso per i messaggi in errore, è possibile definire una condizione per tipo di errore. In questo modo sarà possibile perfezionare la generazione rapporti e visualizzare tutti i dati relativi ai tipi di errore.

## Elenco dei campi {#journey-properties-fields}

| Categoria | Nome campo | Etichetta | Descrizione |
|---|---|---|------------|
| Versione percorso | journeyUID | Identificatore percorso | |
| | journeyVersionUID | Identificatore versione percorso | |
| | journeyVersionName | Nome versione percorso | |
| | journeyVersionDescription | Descrizione versione percorso | |
| | journeyVersion | Versione percorso | |
| Istanza percorso | instanceUID | Identificatore istanza percorso | ID dell’istanza |
| | externalKey | Chiave esterna | Identificatore individuale che attiva il percorso |
| | organizationId | Identificatore organizzazione | Organizzazione del brand |
| | sandboxName | Nome sandbox | Nome della sandbox |
| Identità | profileId | Identificatore dell’identità del profilo | Identificatore del profilo nel percorso |
| | namespace | Spazio dei nomi identità profilo | Spazio dei nomi del profilo nel percorso (ad esempio: ECID) |
| Nodo corrente | currentNodeId | Identificatore nodo corrente | Identificatore dell’attività corrente (nodo) |
| | currentNodeName | Nome nodo corrente | Nome dell’attività corrente (nodo) |
| Nodo precedente | previousNodeId | Identificatore nodo precedente | Identificatore dell’attività precedente (nodo) |
| | previousNodeName | Nome nodo precedente | Nome dell’attività precedente (nodo) |
| Errori | lastNodeUIDInError | Identificatore ultimo nodo in errore | Identificatore dell’attività (nodo) più recente con errore |
| | lastNodeNameInError | Nome ultimo nodo in errore | Nome dell’attività (nodo) più recente con errore |
| | lastNodeTypeInError | Ultimo tipo di nodo in errore | Tipo di errore dell’attività (nodo) più recente nell’errore. Tipi possibili:<ul><li>Eventi: Eventi, Reazioni, SQ (esempio: Qualificazione del pubblico)</li><li>Controllo del flusso: Fine, Condizione, Attesa</li><li>Azioni: azioni ACS, Salta, Azione personalizzata</li></ul> |
| | lastErrorCode | Codice ultimo errore | Codice di errore dell’attività (nodo) più recente che presenta un errore. Possibili errori: <ul><li>Codici di errore HTTP</li><li>con limite</li><li>timeout</li><li>error (esempio: default in caso di errore imprevisto. Non deve/raramente si verifica)</li></ul> |
| | lastExecutedActionErrorCode | Codice errore ultima azione eseguita | Codice di errore dell’ultima azione in errore |
| | lastDataFetchErrorCode | Codice errore ultimo recupero dati | Codice di errore dell’ultimo recupero dati da origini dati |
| Ora | lastActionExecutionElapsedTime | Tempo trascorso dall’esecuzione dell’ultima azione | Tempo impiegato per eseguire l’azione più recente |
| | lastDataFetchElapsedTime | Tempo trascorso dall’ultimo recupero dati | Tempo impiegato per eseguire l’ultimo recupero dati dalle origini dati |

+++ Guida di riferimento della Knowledge Base di AI

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

* **TL;DR:** In questa pagina viene descritta la categoria Proprietà Percorso nell&#39;editor espressioni, ovvero un insieme di campi tecnici relativi all&#39;istanza del percorso attivo (ID, errori, nodi correnti/precedenti, tempi trascorsi) che possono essere utilizzati per creare espressioni per la registrazione, gli avvisi e il reporting specifico degli errori.

**Intenti:**

* Accedi ai campi Proprietà Percorso nell’editor di espressioni semplice o avanzato per fare riferimento ai metadati live del percorso
* Creare una condizione che filtra i profili eliminati per tipo di errore per indirizzarli a un sistema di registrazione di terze parti
* Inviare avvisi di errore a un canale esterno (ad esempio, Slack) facendo riferimento all’ultimo codice di errore e al nome del nodo in un’azione personalizzata
* Ottimizzare la segnalazione degli errori di percorso creando percorsi di condizione separati per tipo di errore utilizzando `lastNodeTypeInError` e `lastErrorCode`
* Fai riferimento a identificatori di versione del percorso, identificatori di istanza e nome sandbox nelle espressioni per il tracciamento e il controllo

**Glossario:**

* **Proprietà Percorso**: categoria nell&#39;editor espressioni contenente campi di metadati tecnici per l&#39;istanza di esecuzione del percorso corrente *(specifica per prodotto)*
* **instanceUID**: identificatore univoco dell&#39;istanza di percorso per l&#39;esecuzione di un profilo specificato *(specifico per prodotto)*
* **lastErrorCode**: il codice di errore dell&#39;attività non riuscita più recente nel percorso; i valori possibili includono i codici HTTP, `capped`, `timedOut` e `error` *(specifico per prodotto)*
* **lastNodeTypeInError**: il tipo dell&#39;ultima attività che ha rilevato un errore; può essere Eventi, Controllo di flusso o Azioni *(specifiche del prodotto)*
* **externalKey**: identificatore individuale (ad esempio, ID profilo) che ha attivato l&#39;istanza di percorso *(specifico per prodotto)*

**Guardrail:**

* I valori dei campi Proprietà percorso vengono recuperati direttamente dal percorso live al momento dell’esecuzione e non sono disponibili per la convalida pre-esecuzione
* Il campo `lastErrorCode` utilizza valori predefiniti: codici di errore HTTP, `capped`, `timedOut` e `error`
* Le proprietà del percorso sono disponibili sia nell’editor di espressioni semplici che in quello avanzato, nella categoria Proprietà Percorso

**Terminologia:**

* Nome canonico: Proprietà Percorso — Acronimo: none — varianti: campi tecnici percorso, campi metadati percorso
* Sinonimi: &quot;Proprietà Percorso&quot; = &quot;campi tecnici percorso&quot;; &quot;instanceUID&quot; = &quot;identificatore istanza percorso&quot;
* Non confondere: journeyUID (identifica la definizione del percorso) ≠ instanceUID (identifica l’esecuzione del percorso da parte di un profilo specifico)

**Domande frequenti:**

* **Q: dove si trovano i campi Proprietà Percorso nell&#39;editor espressioni?** — Vengono visualizzati sia nell&#39;editor di espressioni semplici che in quello avanzato nella categoria Proprietà Percorso, sotto Eventi e Origini dati.
* **D: come posso registrare i profili eliminati da una regola di limite?** — Aggiungere un filtro di condizione del percorso di errore su `lastErrorCode == "capped"` e inviare tali profili a un sistema di terze parti tramite un&#39;azione personalizzata.
* **Q: Qual è la differenza tra `journeyUID` e `instanceUID`?** — `journeyUID` identifica la definizione del percorso; `instanceUID` identifica un&#39;istanza di esecuzione specifica per un determinato profilo.
* **Q: quale codice di errore viene restituito per un errore di sistema imprevisto?** — Il codice `error`, che viene utilizzato come predefinito per gli errori imprevisti e dovrebbe verificarsi raramente.
* **Q: è possibile utilizzare i campi Proprietà Percorso per inviare avvisi di Slack in caso di errori di azione?** — Sì; fare riferimento a `lastNodeNameInError` e `lastErrorCode` in un&#39;azione personalizzata per includere i dettagli dell&#39;errore in una notifica Slack.

+++
