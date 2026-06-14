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
TQID: https://experienceleague.adobe.com/wX-aqOHlSWGU0gTqyv0nEuSVFL8sstvCMxgiqeFDWIo
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a9f73820-6899-47c2-a597-3fec28ab756aid: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
subfeature_v2: id: d145add9-d5b9-481b-aa8a-e15e6bb7f813id: a7289281-9ae4-47b1-b8cf-4028b98af776id: b5afe8bf-bda6-41b5-ba06-922638872d63
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 7f28f19b11ead867b0851943fdd997dcc3af170b
workflow-type: tm+mt
source-wordcount: 685
ht-degree: 2%

---

# Campi di esecuzione dell’azione eventi journeyStep {#sharing-execution-fields}

>[!BEGINSHADEBOX]

**In questa pagina:** Fai riferimento ai campi di esecuzione dell&#39;azione aggiunti agli eventi dei passaggi del percorso quando un passaggio elabora un&#39;azione personalizzata.

>[!ENDSHADEBOX]

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
* error

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

## actionOriginEndpoint {#actionoriginendpoint}

URI dell&#39;endpoint dell&#39;azione personalizzata utilizzato nell&#39;azione.

Tipo: stringa

## actionOriginMethod {#actionoriginmethod}

Descrive il metodo utilizzato nella richiesta HTTP (GET o POST).

Tipo: stringa

## actionOriginIsMTLS {#actionoriginismtls}

Descrive se MTLS è abilitato per l’endpoint.

Tipo: booleano

## actionIsProxy {#actionisproxy}

Descrive se per la chiamata viene utilizzato un proxy HTTP con intervallo di indirizzi IP definito.

Tipo: booleano

## actionExecutionOriginStartTime {#actionexecutionoriginstarttime}

Descrive la marca temporale in cui viene avviata la richiesta HTTP. In caso di un nuovo tentativo, questo è il timestamp in cui viene avviato il tentativo finale di nuovo tentativo. La marca temporale utilizza il formato ISO8601 nel fuso orario UTC.

Tieni presente che questa marca temporale sarà in genere leggermente successiva all’ingresso del profilo nel nodo dell’azione personalizzata, o significativamente successiva all’ingresso nel nodo in caso di limitazione.

Tipo: timestamp

## actionExecutionOriginTime {#actionexecutionorigintime}

Descrive il tempo di risposta della chiamata HTTP. In caso di nuovo tentativo, questo è il tempo impiegato dal tentativo finale di nuovo tentativo. Misura il tempo che intercorre tra l’avvio della richiesta HTTP e la restituzione della risposta completa dal server. Tieni presente che, in caso di limitazione, questo esclude il tempo di attesa in coda.

Tipo: long

## actionIsThrottled {#actionisthrottled}

Descrive se la limitazione è abilitata per l’endpoint.

Tipo: booleano

## actionWaitTime {#actionwaittime}

Descrive quando viene raggiunto il limite di frequenza configurato per un endpoint con limitazione, le chiamate vengono messe in coda ed elaborate alla velocità configurata. Questo campo indica il tempo di attesa della chiamata nella coda prima dell’esecuzione. Specificato solo se actionIsThrottled == true.

Tipo: long

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
