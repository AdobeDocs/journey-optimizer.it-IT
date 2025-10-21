---
solution: Journey Optimizer
product: journey optimizer
title: campi comuni degli eventi journeyStep
description: campi comuni degli eventi journeyStep
feature: Journeys, Reporting
topic: Content Management
role: Engineer, Admin
level: Experienced
exl-id: 42aec986-2352-456a-a725-7f1585ae01f8
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 0%

---

# campi comuni degli eventi journeyStep {#sharing-common-fields}

Questo gruppo di campi verrà condiviso dai seguenti eventi: **journeyStepEvent** e **journeyStepProfileEvent**.

Questi sono i campi XDM comuni che [!DNL Journey Optimizer] invia a Adobe Experience Platform. Campi comuni vengono inviati per ogni passaggio elaborato in un percorso. Campi più specifici vengono utilizzati per azioni personalizzate e arricchimenti.

Alcuni di questi campi sono disponibili solo in pattern di elaborazione specifici (esecuzione di azioni, recupero di dati, ecc.) per limitare la dimensione degli eventi.


>[!NOTE]
>
>Ulteriori informazioni sugli attributi delle proprietà del percorso [in questa sezione](../building-journeys/expression/journey-properties.md#journey-propertoes-fields).


## entrata {#entrance-field}

Indica se l&#39;utente è entrato nel percorso. Se non presente, supponiamo che il valore sia falso.

Tipo: booleano

Valori: true/false

## rientro {#reentrance-field}

Indica se l&#39;utente è rientrato nel percorso con la stessa istanza. Se non presente, supponiamo che il valore sia falso.

Tipo: booleano

Valori: true/false

## instanceEnded {#instance-ended-field}

Indica se l’istanza è terminata (con successo o meno).

Tipo: booleano

## eventID {#eventid-field}

ID evento in elaborazione, per il passaggio di elaborazione. Se l&#39;evento è esterno, il valore è il relativo eventId. Se l’evento è interno, il valore è l’eventId interno (ad esempio scheduledNotificationReceived, executeAction, ecc.).

Tipo: stringa

## nodeID {#nodeid-field}

ID del nodo client (dall’area di lavoro).

Tipo: stringa

## stepID {#stepdid-field}

ID univoco del passaggio attualmente in fase di elaborazione.

Tipo: stringa

## stepName {#stepname-field}

Nome del passaggio attualmente in fase di elaborazione.

Tipo: stringa

## stepType {#steptype-field}

Tipo del passaggio.

Tipo: stringa

Valori possibili:

* Condizione
* Azione
* Modulo di pianificazione
* Timer

## stepStatus {#stepstatus-field}

Stato del passaggio, che rappresenta lo stato del passaggio, al termine dell&#39;elaborazione (e quando l&#39;evento del passaggio viene generato).

Tipo: stringa

Lo stato può essere:

* terminato: il passaggio non presenta alcuna transizione e l’elaborazione è terminata correttamente.
* errore: l’elaborazione del passaggio ha generato un errore.
* transizioni: il passaggio è in attesa che un evento passi a un altro passaggio.
* limitato: il passaggio non è riuscito a causa di un errore di limite, generato durante un’azione o un arricchimento.
* timeout: il passaggio non è riuscito a causa di un errore di timeout, generato durante un&#39;azione o un arricchimento.
* instanceTimedout: l&#39;elaborazione del passaggio è stata interrotta perché è stato raggiunto il timeout dell&#39;istanza.

## journeyID {#journeyid-field}

ID del percorso.

Tipo: stringa

## journeyVersionID {#journeyversionid-field}

ID della versione del percorso. Questo ID rappresenta il riferimento di identità al percorso, nel caso di journeyStepEvent.

Tipo: stringa

>[!NOTE]
>
>Per la risoluzione dei problemi, si consiglia di utilizzare journeyVersionID invece di journeyVersionName durante la query sui percorsi.

## journeyVersionName {#journeyversionname-field}

Nome della versione del percorso.

Tipo: stringa

>[!NOTE]
>
>Per la risoluzione dei problemi, si consiglia di utilizzare journeyVersionID invece di journeyVersionName durante la query sui percorsi.

## journeyVersion {#journeyversion-field}

Versione del percorso.

Tipo: stringa

## instanceID {#instanceid-field}

ID interno dell’istanza di percorso.

Tipo: stringa

## externalKey {#externalkey-field}

Chiave esterna estratta dall’evento per elaborarlo.

Tipo: stringa

## parentStepID {#parenstepid-field}

ID del passaggio padre del passaggio elaborato corrente nell’istanza.

Tipo: stringa

## parentStepName {#parentstepname-field}

Nome del passaggio padre del passaggio corrente.

Tipo: stringa

## parentTransitionID {#parenttransitionid-field}

ID della transizione che ha portato l’istanza al passaggio elaborato.

Tipo: stringa

## parentTransitionName {#parenttransitionname-field}

Nome della transizione che ha portato l’istanza al passaggio elaborato.

Tipo: stringa

## inTest {#intest-field}

Indica se il percorso è in modalità di test o meno.

Tipo: booleano

## processingTime {#processingtime-field}

Tempo totale in millisecondi dall’ingresso del passaggio dell’istanza alla fine dell’elaborazione.

Tipo: long

## instanceType {#instancetype-field}

Indica il tipo di istanza, se è batch o unitaria.

Tipo: stringa

Valori: batch/unitario

## recurrenceIndex {#recurrenceindex-field}

Indice della ricorrenza se il percorso è batch e ricorrente (la prima esecuzione ha recurrenceIndex = 1).

Tipo: long

## isBatchToUninary {#isbatchtounitary-field}

Indica se questa istanza unitaria è stata attivata da un&#39;istanza batch.

Tipo: booleano

## batchExternalKey {#batchexternalkey-field}

Chiave esterna per evento batch.

Tipo: stringa

## batchInstanceID {#batchinstanceid-field}

questo è l’ID dell’istanza batch.

Tipo: stringa

## batchUninaryBranchID {#batchunitarybranchid-field}

se l’istanza è stata attivata da un’istanza batch, ID del ramo unitario.

Tipo: stringa

## exitCriteriaID

ID dei criteri di uscita

Tipo: stringa

## exitCriteriaName

Nome dei criteri di uscita

Tipo: stringa