---
solution: Journey Optimizer
product: journey optimizer
title: Proprietà del percorso
description: Informazioni sulle proprietà del percorso
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: percorso, espressione, editor, proprietà
exl-id: eb1ab0ed-90bd-4613-b63d-b28693947db2
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '589'
ht-degree: 2%

---

# Attributi proprietà percorso {#journey-properties}

Nell&#39;[editor espressioni semplici](../condition-activity.md#about_condition) e nell&#39;[editor espressioni avanzate](../expression/expressionadvanced.md), nelle categorie **Evento** e **Origine dati**, è possibile accedere alla categoria **Proprietà Percorso**. Questa categoria contiene campi tecnici relativi al percorso per un determinato profilo. Si tratta delle informazioni recuperate dal sistema dai percorsi attivi, ad esempio l&#39;ID percorso, o gli errori specifici rilevati.

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
| | organizationId | Identificatore dell’organizzazione | Organizzazione del brand |
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
