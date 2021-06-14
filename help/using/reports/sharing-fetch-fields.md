---
title: Campi di recupero dati di journeyStep
description: Campi di recupero dati di journeyStep
feature: Reporting
topic: Gestione dei contenuti
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 4%

---

# Campi di recupero dati di journeyStep {#sharing-fetch-fields}

![](../assets/do-not-localize/badge.png)

Questo mixin sarà condiviso da journeyStepEvent e journeyStepProfileEvent.

Durante un&#39;elaborazione a gradini, è possibile ottenere N dati sui gruppi di campi.

## fetchTotalTime

Quantità totale di tempo impiegato nel recupero dei dati in millisecondi durante l&#39;elaborazione delle fasi.

Tipo: long

## fetchTypeInError

Definisce se il recupero in errore si trova su Adobe Experience Platform o su un’origine dati personalizzata.

Tipo: string

Valori:
* aep
* personalizzato

## fetchError

Tipo di errore che si verifica quando il recupero dei dati viene elaborato.

Tipo: string

Valori:
* http
* tappatura
* timeout
* errore

## fetchErrorCode

Errore di recupero del codice. Presente se l&#39;errore ha un codice, ad esempio uno HTTP. Ad esempio, se actionExecError è http, il codice 404 rappresenta l&#39;errore HTTP 404.

Tipo: string

## fetchOriginError

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

Tipo: string

## fetchOriginErrorCode

Il codice di errore fornito dal sistema [!DNL Journey Orchestration] sta eseguendo una query. Ad esempio può essere un 404, 500, ecc.

Tipo: string

## fetchCount

Quante volte i dati vengono recuperati, indipendentemente dal tipo di origine.

Tipo: long

## fetchPlatformTotalTime

Il tempo totale impiegato per recuperare i dati da Adobe Experience Platform in millisecondi. Nota: tale quantità di tempo viene calcolata dal momento in cui il motore invia l’evento di arricchimento al servizio di arricchimento e riceve la risposta.

Tipo: long

## fetchPlatformCount

Quante volte i dati vengono recuperati da Adobe Experience Platform.

Tipo: long

## fetchCustomTotalTime

Quantità di tempo per recuperare i dati personalizzati in millisecondi. Nota: tale quantità di tempo è calcolata dal momento in cui il motore invia l’evento di arricchimento al servizio di arricchimento e riceve la risposta

Tipo: long

## fetchCustomCount

Quante volte i dati personalizzati vengono recuperati da sistemi esterni.

Tipo: long
