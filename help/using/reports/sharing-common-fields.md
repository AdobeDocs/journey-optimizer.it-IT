---
title: Campi comuni degli eventi di journeyStep
description: Campi comuni degli eventi di journeyStep
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 42aec986-2352-456a-a725-7f1585ae01f8
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 9%

---

# Campi comuni degli eventi di journeyStep {#sharing-common-fields}

Questo gruppo di campi verrà condiviso da journeyStepEvent e journeyStepProfileEvent.

Si tratta dei campi XDM comuni che [!DNL Journey Optimizer] invia a Adobe Experience Platform. Verranno inviati campi comuni per ogni passaggio elaborato in un percorso. Campi più specifici vengono utilizzati per azioni personalizzate e arricchimenti.

Alcuni di questi campi sono disponibili solo in pattern di elaborazione specifici (esecuzione azione, recupero dati, ecc.) per limitare le dimensioni degli eventi.

## ingresso {#entrance-field}

Indica se l’utente è entrato nel percorso. Se non è presente, si presuppone che il valore sia falso.

Tipo: booleano

Valori: true/false

## rientro {#reentrance-field}

Indica se l’utente è rientrato nel percorso con la stessa istanza. Se non è presente, si presuppone che il valore sia falso.

Tipo: booleano

Valori: true/false

## instanceEnded {#instance-ended-field}

Indica se l&#39;istanza è terminata (con successo o meno).

Tipo: booleano

## eventID {#eventid-field}

ID evento in elaborazione, per l’elaborazione dei passaggi. Se l’evento è esterno, il valore è il relativo eventId. Se l’evento è interno, il valore è l’ID evento interno (ad esempio, scheduledNotificationReceived, executeAction, ecc.).

Tipo: stringa

## nodeID {#nodeid-field}

ID nodo client (dall’area di lavoro).

Tipo: stringa

## stepID {#stepdid-field}

ID univoco del passaggio in fase di elaborazione.

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
* Attività Scheduler
* Timer

## stepStatus {#stepstatus-field}

Stato del passaggio, che rappresenta lo stato del passaggio, al termine dell’elaborazione (e all’avvio dell’evento step).

Tipo: stringa

Lo stato può essere:

* end: il passaggio non ha alcuna transizione e l’elaborazione è terminata correttamente.
* errore: errore generato dall&#39;elaborazione dei passaggi.
* transizioni: il passaggio è in attesa della transizione di un evento a un altro passaggio.
* con limiti massimi: il passaggio non è riuscito per un errore di limitazione, generato durante un&#39;azione o un arricchimento.
* timeout: il passaggio non è riuscito per un errore di timeout, generato durante un&#39;azione o un arricchimento.
* instanceTimedout: il passaggio ha interrotto l’elaborazione perché l’istanza ha raggiunto il timeout.

## journeyID {#journeyid-field}

ID del percorso.

Tipo: stringa

## journeyVersionID {#journeyversionid-field}

ID della versione del percorso. Questo id rappresenta il riferimento di identità al percorso, nel caso di journeyStepEvent.

Tipo: stringa

## journeyVersionName {#journeyversionname-field}

Nome della versione del percorso.

Tipo: stringa

## journeyVersion {#journeyversion-field}

Versione del percorso.

Tipo: stringa

## instanceID {#instanceid-field}

ID interno dell&#39;istanza del percorso.

Tipo: stringa

## externalKey {#externalkey-field}

Chiave esterna estratta dall’evento per elaborarla.

Tipo: stringa

## parentStepID {#parenstepid-field}

ID del passo padre del passaggio elaborato corrente nell&#39;istanza.

Tipo: stringa

## parentStepName {#parentstepname-field}

Nome del passo dell&#39;elemento padre del passaggio corrente.

Tipo: stringa

## parentTransitionID {#parenttransitionid-field}

ID della transizione che ha portato l’istanza al passaggio elaborato.

Tipo: stringa

## parentTransitionName {#parenttransitionname-field}

Nome della transizione che ha portato l&#39;istanza al passaggio elaborato.

Tipo: stringa

## inTest {#intest-field}

Indica se il percorso è in modalità di prova o meno.

Tipo: booleano

## processingTime {#processingtime-field}

Quantità totale di tempo in millisecondi dall’entrata del passaggio dell’istanza alla fine dell’elaborazione.

Tipo: long

## instanceType {#instancetype-field}

Indica il tipo di istanza, se è batch o unitario.

Tipo: stringa

Valori: batch/unitario

## recidivaIndex {#recurrenceindex-field}

Indice della ricorrenza se il percorso è in batch e ricorrente (la prima esecuzione ha ricorrenzaIndex = 1).

Tipo: long

## isBatchToUnitaria {#isbatchtounitary-field}

Indica se questa istanza unitaria è stata attivata da un&#39;istanza batch.

Tipo: booleano

## batchExternalKey {#batchexternalkey-field}

Chiave esterna per evento batch.

Tipo: stringa

## batchInstanceID {#batchinstanceid-field}

questo è l&#39;ID dell&#39;istanza batch.

Tipo: stringa

## batchUnitarioBranchID {#batchunitarybranchid-field}

se l&#39;istanza è stata attivata da un&#39;istanza batch, ID ramo unitario.

Tipo: stringa
