---
solution: Journey Optimizer
product: journey optimizer
title: Campi di recupero dati di eventi journeyStep
description: Campi di recupero dati di eventi journeyStep
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: 948fe843-47cf-4b20-976a-48069eb9cf5c
TQID: https://experienceleague.adobe.com/obaiLWD6yq0dZ5ZhE69q-iLHzI99ll7XJnMNlOpJp1A
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
source-git-commit: 7f28f19b11ead867b0851943fdd997dcc3af170b
workflow-type: tm+mt
source-wordcount: 405
ht-degree: 4%

---

# Campi di recupero dati di eventi journeyStep {#sharing-fetch-fields}

>[!BEGINSHADEBOX]

**In questa pagina:** Fai riferimento ai campi di recupero dati aggiunti agli eventi dei passaggi del percorso quando i dati vengono arricchiti da Adobe Experience Platform o da un&#39;origine personalizzata durante l&#39;elaborazione dei passaggi.

>[!ENDSHADEBOX]

Questo gruppo di campi verrà condiviso da journeyStepEvent e journeyStepProfileEvent.

Durante un passaggio di elaborazione, possiamo avere N recupero dati sui gruppi di campi.

## fetchTotalTime {#fetchtotaltime-field}

Tempo totale impiegato per il recupero dei dati in millisecondi durante l’elaborazione del passaggio.

Tipo: long

## fetchTypeInError {#fetchtypeinerror-field}

Definisce se il recupero in errore si trova su Adobe Experience Platform o su un’origine dati personalizzata.

Tipo: stringa

Valori:

* aep
* personalizzato

## fetchError {#fetcherror-field}

Tipo di errore che si verifica quando viene elaborato il recupero dei dati.

Tipo: stringa

Valori:

* http
* limiti
* timeout
* error

## fetchErrorCode {#fetcherrorcode-field}

Codice per l’errore di recupero. Presente se l’errore ha un codice, ad esempio HTTP. Ad esempio, se actionExecError è http, il codice 404 rappresenta l&#39;errore HTTP 404.

Tipo: stringa

## fetchOriginError {#fetchoriginerror-field}

Può verificarsi un timeout in due casi:

* al primo tentativo l’azione viene eseguita. In questo caso, l’esecuzione non è terminata, quindi non si verifica alcun errore sottostante
* in caso di nuovo tentativo: in questo caso, actionExecOrigError/actionExecOrigErrorCode descrive l’errore riscontrato nel tentativo prima del nuovo tentativo.

Ad esempio, i dati vengono recuperati da Unified Profile Service e al primo tentativo viene restituito un errore HTTP 500. Il recupero viene ritentato, ma la durata dei 2 tentativi supera il timeout. Quindi l’esecuzione dell’azione viene taggata come timeout. La parte azione sarà simile alla seguente:

```
    ...
    "fetchTypeInError": "aep",
    "fieldgroupIdInError": "MyProfileFieldgroup",
    "fetchError": "timedout",
    "fetchOrigError": "http",
    "fetchOrigErrorCode": "500"
```

Tipo: stringa

## fetchOriginErrorCode {#fetchoriginerrorcode-field}

È in corso la query del codice di errore fornito dal sistema [!DNL Journey Optimizer]. Ad esempio, può essere un 404, 500, ecc.

Tipo: stringa

## fetchCount {#fetchcount-field}

Quante volte vengono recuperati i dati, indipendentemente dal tipo di origine.

Tipo: long

## fetchPlatformTotalTime {#fetchplatformtotaltime-field}

Il tempo totale impiegato per recuperare i dati da Adobe Experience Platform in millisecondi. Nota: questo periodo di tempo viene calcolato dal momento in cui il motore invia l’evento di arricchimento al servizio di arricchimento e riceve la risposta.

Tipo: long

## fetchPlatformCount {#fetchplatformcount-field}

Quante volte i dati vengono recuperati da Adobe Experience Platform.

Tipo: long

## fetchCustomTotalTime {#fetchcustomtotaltime-field}

Tempo di recupero dei dati personalizzati in millisecondi. Nota: questo periodo di tempo viene calcolato dal momento in cui il motore invia l’evento di arricchimento al servizio di arricchimento e riceve la risposta

Tipo: long

## fetchCustomCount {#fetchcustomcount-field}

Quante volte i dati personalizzati vengono recuperati da sistemi esterni.

Tipo: long
