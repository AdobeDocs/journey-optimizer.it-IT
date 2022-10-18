---
solution: Journey Optimizer
product: journey optimizer
title: Campi di recupero dati di eventi journeyStep
description: Campi di recupero dati di eventi journeyStep
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 948fe843-47cf-4b20-976a-48069eb9cf5c
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 7%

---

# Campi di recupero dati di eventi journeyStep {#sharing-fetch-fields}

Questo gruppo di campi verrà condiviso da journeyStepEvent e journeyStepProfileEvent.

Durante un&#39;elaborazione a gradini, è possibile ottenere N dati sui gruppi di campi.

## fetchTotalTime {#fetchtotaltime-field}

Quantità totale di tempo impiegato nel recupero dei dati in millisecondi durante l&#39;elaborazione delle fasi.

Tipo: long

## fetchTypeInError {#fetchtypeinerror-field}

Definisce se il recupero in errore si trova su Adobe Experience Platform o su un’origine dati personalizzata.

Tipo: stringa

Valori:
* aep
* personalizzato

## fetchError {#fetcherror-field}

Tipo di errore che si verifica quando il recupero dei dati viene elaborato.

Tipo: stringa

Valori:
* http
* tappatura
* timeout
* error

## fetchErrorCode {#fetcherrorcode-field}

Errore di recupero del codice. Presente se l&#39;errore ha un codice, ad esempio uno HTTP. Ad esempio, se actionExecError è http, il codice 404 rappresenta l&#39;errore HTTP 404.

Tipo: stringa

## fetchOriginError {#fetchoriginerror-field}

Può verificarsi un timeout, in due casi:

* al primo tentativo l’azione viene eseguita. In questo caso, l&#39;esecuzione non è completata, quindi non vi è alcun errore sottostante
* in un nuovo tentativo: in questo caso, actionExecOrigError/actionExecOrigErrorCode descrive l&#39;errore rilevato nel tentativo prima del nuovo tentativo.

Ad esempio, i dati vengono recuperati da Unified Profile Service e viene restituito un errore HTTP 500 al primo tentativo. Il recupero viene ritentato, ma la durata dei 2 tentativi supera il timeout. Quindi l’esecuzione dell’azione viene taggata come timeout. La parte azione avrà un aspetto simile al seguente:

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

Codice di errore fornito dal sistema [!DNL Journey Optimizer] sta eseguendo una query. Ad esempio può essere un 404, 500, ecc.

Tipo: stringa

## fetchCount {#fetchcount-field}

Quante volte i dati vengono recuperati, indipendentemente dal tipo di origine.

Tipo: long

## fetchPlatformTotalTime {#fetchplatformtotaltime-field}

Il tempo totale impiegato per recuperare i dati da Adobe Experience Platform in millisecondi. Nota: tale quantità di tempo viene calcolata dal momento in cui il motore invia l’evento di arricchimento al servizio di arricchimento e riceve la risposta.

Tipo: long

## fetchPlatformCount {#fetchplatformcount-field}

Quante volte i dati vengono recuperati da Adobe Experience Platform.

Tipo: long

## fetchCustomTotalTime {#fetchcustomtotaltime-field}

Quantità di tempo per recuperare i dati personalizzati in millisecondi. Nota: tale quantità di tempo è calcolata dal momento in cui il motore invia l’evento di arricchimento al servizio di arricchimento e riceve la risposta

Tipo: long

## fetchCustomCount {#fetchcustomcount-field}

Quante volte i dati personalizzati vengono recuperati da sistemi esterni.

Tipo: long
