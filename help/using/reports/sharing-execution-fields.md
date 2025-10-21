---
solution: Journey Optimizer
product: journey optimizer
title: Campi di esecuzione dell’azione eventi journeyStep
description: Campi di esecuzione dell’azione eventi journeyStep
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: 273cda84-0261-4c5b-b5f4-0202e8874d05
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 3%

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

Il campo `actionExecutionTime` rappresenta il tempo totale (in millisecondi) impiegato per eseguire l&#39;azione, incluso il tempo di attesa della richiesta nella coda (se la limitazione è configurata e il limite di velocità è raggiunto) e il tempo di esecuzione effettivo (inclusa la latenza di rete per l&#39;endpoint esterno).

Il campo `Timestamp` indica l&#39;ora di fine dell&#39;esecuzione dell&#39;azione. Per determinare quando il profilo è entrato nel nodo dell&#39;azione personalizzata, sottrarre `actionExecutionTime` da `Timestamp`.

Ad esempio, se `Timestamp` è &quot;2025-02-04 09:39:03 UTC&quot; e `actionExecutionTime` è 1.813.227 ms (~31 minuti), il profilo è entrato nel nodo approssimativamente &quot;2025-02-04 09:08:32 UTC&quot;.




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
