---
title: Campi di esecuzione dell’azione eventi journeyStep
description: Campi di esecuzione dell’azione eventi journeyStep
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 273cda84-0261-4c5b-b5f4-0202e8874d05
source-git-commit: 6d744c0289e81ab2229f02c44ead43943b945b89
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 5%

---

# Campi di esecuzione dell’azione eventi journeyStep {#sharing-execution-fields}

Questo gruppo di campi verrà condiviso da journeyStepEvent e journeyStepProfileEvent.

Se il passaggio dispone di un’azione da elaborare, tali campi verranno aggiunti al payload dell’evento.

## actionID {#actionid-field}

ID dell&#39;azione in corso di esecuzione.

Tipo: string

## actionName {#actionname-field}

Nome dell’azione. Se non è stato impostato alcun nome, viene eseguito stepName.

Tipo: string

## actionType {#actionType-field}

Tipo di azione.

Tipo: string

## actionParameter {#actionparameterized-field}

Indica se l’azione è parametrizzata o meno.

Tipo: booleano

## actionExecutionTime {#actionexecutiontime-field}

Il tempo (in millisecondi) impiegato per eseguire un&#39;azione corrente.

Tipo: long

## actionExecutionError {#actionexecutionerror-field}

Tipo di errore che si verifica quando viene chiamata l&#39;azione.

Tipo: string

Valori:
* http
* tappatura
* timeout
* error

## actionExecutionErrorCode {#actionexecutionerrorcode-field}

Errore di esecuzione del codice per l&#39;azione. Presente se l&#39;errore ha un codice, ad esempio uno HTTP.

Tipo: string

## actionExecutionOriginError {#actionexecutionoriginerror-field}

Può verificarsi un timeout, in due casi:

* al primo tentativo viene eseguita un&#39;azione. In questo caso, l&#39;esecuzione non è completata, quindi non vi è alcun errore sottostante
* in un nuovo tentativo: in questo caso, actionExecOrigError/actionExecOrigErrorCode descrive l&#39;errore rilevato nel tentativo prima del nuovo tentativo.

Ad esempio, viene inviata un’e-mail e al primo tentativo viene restituito un errore HTTP 500. Il recupero viene ritentato, ma la durata dei 2 tentativi supera il timeout. Quindi l’esecuzione dell’azione viene taggata come timeout. La parte azione avrà un aspetto simile al seguente:

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

Tipo: string

## actionExecutionOriginCode {#actionexecutionorigincode-field}

Codice di errore dell&#39;actionExecOrigError.

Tipo: string

## actionBusinessType {#actionbusinesstype-field}

Indica il tipo di azione.

Valori:

* costruzione
* E-mail ACS
* SMS ACS
* Push ACS
* cliente
* Epsilon
* ...

Tipo: string

## deliveryJobID {#deliveryjobid-field}

Questo descrive l’ID del processo di consegna per il Percorso batch.

Tipo: string

## batchDeliveryID {#batchdeliveryid-field}

Questo descrive l’ID di consegna per il Percorso batch.

Tipo: string

## fromSegmentTrigger {#fromsegmenttrigger-field}

Questo descrive se il Percorso batch viene attivato dal segmento di pubblico.

Tipo: booleano

## actionSchedulerCount {#actionschedulercount-field}

Numero di richieste di notifica del programmatore inviate al servizio di pianificazione durante l&#39;elaborazione dei passaggi.

Tipo: long
