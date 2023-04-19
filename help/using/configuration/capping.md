---
solution: Journey Optimizer
product: journey optimizer
title: API di limitazione di utilizzo
description: Scopri come lavorare con l’API di limitazione delle funzioni
role: User
level: Beginner
keywords: esterno, API, ottimizzatore, limiti
exl-id: 377b2659-d26a-47c2-8967-28870bddf5c5
source-git-commit: c823d1a02ca9d24fc13eaeaba2b688249e61f767
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 30%

---

# Utilizzare l’API di limitazione di utilizzo {#work}

L’API di limitazione di utilizzo consente di creare, configurare e monitorare le configurazioni di limitazione di utilizzo.

Questa sezione fornisce informazioni globali su come utilizzare l’API. Una descrizione dettagliata dell’API è disponibile in [Documentazione API di Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/).

## Limitazione della descrizione API

| Metodo | Percorso | Descrizione |
|---|---|---|
| [!DNL POST] | list/endpointConfigs | Ottieni un elenco delle configurazioni di limiti endpoint |
| [!DNL POST] | /endpointConfigs | Creare una configurazione di limite endpoint |
| [!DNL POST] | /endpointConfigs/`{uid}`/deploy | Distribuzione di una configurazione di limite endpoint |
| [!DNL POST] | /endpointConfigs/`{uid}`/undeploy | Disdistribuire una configurazione di limite endpoint |
| [!DNL POST] | /endpointConfigs/`{uid}`/canDeploy | Controlla se è possibile distribuire o meno una configurazione di limite endpoint |
| [!DNL PUT] | /endpointConfigs/`{uid}` | Aggiornare una configurazione di limite endpoint |
| [!DNL GET] | /endpointConfigs/`{uid}` | Recuperare una configurazione di limite endpoint |
| [!DNL DELETE] | /endpointConfigs/`{uid}` | Eliminare una configurazione di limite di livello |

Quando una configurazione viene creata o aggiornata, viene eseguito automaticamente un controllo per garantire la sintassi e l’integrità del payload.
Se si verificano alcuni problemi, l&#39;operazione restituisce un avviso o degli errori per facilitare la correzione della configurazione.

## Configurazione endpoint

La struttura di base di una configurazione dell’endpoint è la seguente:

```
{
    "url": "<endpoint URL>",  //wildcards are allowed in the endpoint URL
    "methods": [ "<HTTP method such as GET, POST, >, ...],
    "services": {
        "<service name>": { . //must be "action" or "dataSource" 
            "maxHttpConnections": <max connections count to the endpoint>
            "rating": {          
                "maxCallsCount": <max calls to be performed in the period defined by period/timeUnit>,
                "periodInMs": <integer value greater than 0>
            }
        },
        ...
    }
}
```

### Esempio:

```
`{
  "url": "https://api.example.org/data/2.5/*",
  "methods": [
    "GET"
  ],
  "services": {
    "dataSource": {
      "maxHttpConnections": 30000,
      "rating": {
        "maxCallsCount": 5000,
        "periodInMs": 1000
      }
    }
  },
  "orgId": "<IMS Org Id>"
}
```

## Avvisi ed errori

Quando un **canDeploy** viene chiamato , il processo convalida la configurazione e restituisce lo stato di convalida identificato dal relativo ID univoco:

```
"ok" or "error"
```

Gli errori potenziali sono:

* **ERR_ENDPOINTCONFIG_100**: configurazione di tappping: url mancante o non valido
* **ERR_ENDPOINTCONFIG_101**: configurazione di tappping: url malformato
* **ERR_ENDPOINTCONFIG_102**: configurazione di tappping: url non valido: carattere jolly nell&#39;url non consentito in host:port
* **ERR_ENDPOINTCONFIG_103**: configurazione di tappping: metodi HTTP mancanti
* **ERR_ENDPOINTCONFIG_104**: configurazione di tappping: nessuna classificazione di chiamata definita
* **ERR_ENDPOINTCONFIG_107**: configurazione di tappping: conteggio massimo chiamate non valido (maxCallsCount)
* **ERR_ENDPOINTCONFIG_108**: configurazione di tappping: conteggio massimo chiamate non valido (periodInMs)
* **ERR_ENDPOINTCONFIG_111**: configurazione di tappping: impossibile creare la configurazione dell&#39;endpoint: payload non valido
* **ERR_ENDPOINTCONFIG_112**: configurazione di tappping: impossibile creare la configurazione dell&#39;endpoint: attesa di un payload JSON
* **ERR_AUTHORING_ENDPOINTCONFIG_1**: nome di servizio non valido `<!--<given value>-->`: deve essere &#39;dataSource&#39; o &#39;action&#39;

L&#39;avviso potenziale è:

**ERR_ENDPOINTCONFIG_106**: configurazione di tappping: connessioni HTTP massime non definite: nessuna limitazione per impostazione predefinita

## Casi d’uso

In questa sezione sono disponibili i cinque casi d’uso principali che è possibile eseguire per gestire la configurazione dei limiti in [!DNL Journey Optimizer].

Per facilitare i test e la configurazione, [qui](https://raw.githubusercontent.com/AdobeDocs/JourneyAPI/master/postman-collections/Journey-Orchestration_Capping-API_postman-collection.json) è disponibile una raccolta Postman.

Questa raccolta Postman è stata configurata per condividere la raccolta di variabili Postman generata tramite __[Integrazioni della console di Adobe I/O](https://console.adobe.io/integrations) > Prova > Scarica per Postman__, che genera un file di ambiente Postman con i valori delle integrazioni selezionate.

Una volta scaricata e caricata in Postman, è necessario aggiungere tre variabili: `{JO_HOST}`,`{BASE_PATH}` e `{SANDBOX_NAME}`.
* `{JO_HOST}` : [!DNL Journey Optimizer] URL gateway
* `{BASE_PATH}` : punto di ingresso per l’API.
* `{SANDBOX_NAME}`: l’intestazione **x-sandbox-name** (ad esempio, “prod”) corrispondente al nome della sandbox in cui si svolgeranno le operazioni API. Per ulteriori informazioni, consulta la [panoramica delle sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=it).

Nella sezione seguente, è disponibile un elenco ordinato delle chiamate API REST per eseguire il caso d’uso.

Caso d’uso n° 1: **Creazione e distribuzione di una nuova configurazione di tappatura**

1. list
1. create
1. candeploy
1. deploy

Caso d’uso n° 2: **Aggiornare e distribuire una configurazione di limite non ancora distribuita**

1. list
1. get
1. update
1. candeploy
1. deploy

Caso d’uso n° 3: **Disdistribuire ed eliminare una configurazione di limitazione distribuita**

1. list
1. undeploy
1. delete

Caso d’uso n° 4: **Elimina una configurazione di limitazione distribuita.**

È possibile annullare la distribuzione ed eliminare la configurazione in una sola chiamata API utilizzando il parametro forceDelete.
1. list
1. eliminare, con il parametro forceDelete

Caso d’uso n° 5: **Aggiornare una configurazione di limite già distribuita**

1. list
1. get
1. update
1. undeploy
1. candeploy
1. deploy
