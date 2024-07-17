---
solution: Journey Optimizer
product: journey optimizer
title: Campi di esecuzione dell’azione eventi journeyStep
description: Campi di esecuzione dell’azione eventi journeyStep
feature: Journeys, Reporting
topic: Content Management
role: Data Engineer, Data Architect, Admin
level: Experienced
exl-id: 273cda84-0261-4c5b-b5f4-0202e8874d05
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 5%

---

# Campi di esecuzione dell’azione eventi journeyStep {#sharing-execution-fields}

Questo gruppo di campi verrà condiviso da journeyStepEvent e journeyStepProfileEvent.

Se il passaggio ha un’azione da elaborare, questi campi verranno aggiunti al payload dell’evento.

## actionID {#actionid-field}

ID dell’azione in esecuzione.

Tipo: stringa

## actionName {#actionname-field}

Nome dell’azione. Se non è stato impostato alcun nome, verrà utilizzato stepName.

Tipo: stringa

## actionType {#actionType-field}

Tipo di azione.

Tipo: stringa

## actionParameterized {#actionparameterized-field}

Indica se l&#39;azione è parametrizzata o meno.

Tipo: booleano

## actionExecutionTime {#actionexecutiontime-field}

Tempo (in millisecondi) impiegato per eseguire un&#39;azione corrente.

Tipo: long

## actionExecutionError {#actionexecutionerror-field}

Tipo di errore che si verifica quando viene chiamata l’azione.

Tipo: stringa

Valori:
* http
* limiti
* timeout
* errore

## actionExecutionErrorCode {#actionexecutionerrorcode-field}

Codice per l’errore di esecuzione dell’azione. Presente se l’errore ha un codice, ad esempio HTTP.

Tipo: stringa

## actionExecutionOriginError {#actionexecutionoriginerror-field}

Può verificarsi un timeout in due casi:

* al primo tentativo viene eseguita un’azione. In questo caso, l’esecuzione non è terminata, quindi non si verifica alcun errore sottostante
* in caso di nuovo tentativo: in questo caso, actionExecOrigError/actionExecOrigErrorCode descrive l’errore riscontrato nel tentativo prima del nuovo tentativo.

Ad esempio, viene inviato un messaggio e-mail e al primo tentativo viene restituito un errore HTTP 500. Il recupero viene ritentato, ma la durata dei 2 tentativi supera il timeout. Quindi l’esecuzione dell’azione viene taggata come timeout. La parte azione sarà simile alla seguente:

```
    ...
    "actionId": "myActionId",
    "actionName": "My mail sending",
    "actionType": "acsRestAction",
    "actionParameterized": true,
    "actionExecError": "timedout",
    "actionExecOrigError": "http",
    "actionExecOrigErrorCode": "500"
```

Tipo: stringa

## actionExecutionOriginCode {#actionexecutionorigincode-field}

Codice di errore di actionExecOrigError.

Tipo: stringa

## actionBusinessType {#actionbusinesstype-field}

Indica il tipo di azione.

Valori:

* builtin
* E-mail ACS
* SMS ACS
* Push ACS
* cliente
* Epsilon
* ...

Tipo: stringa

## deliveryJobID {#deliveryjobid-field}

Descrive l’ID del processo di consegna per il Percorso batch.

Tipo: stringa

## batchDeliveryID {#batchdeliveryid-field}

Descrive l’ID di consegna per il Percorso batch.

Tipo: stringa

## fromSegmentTrigger {#fromsegmenttrigger-field}

Descrive se il Percorso batch viene attivato dal segmento di pubblico.

Tipo: booleano

## actionSchedulerCount {#actionschedulercount-field}

Numero di richieste di notifica del modulo di pianificazione inviate al servizio di pianificazione durante l&#39;elaborazione del passaggio.

Tipo: long
