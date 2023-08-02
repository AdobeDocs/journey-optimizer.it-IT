---
solution: Journey Optimizer
product: journey optimizer
title: API di limitazione di utilizzo
description: Scopri come utilizzare l’API di limitazione di utilizzo
role: User
level: Beginner
keywords: esterno, API, ottimizzatore, limitazione
exl-id: 377b2659-d26a-47c2-8967-28870bddf5c5
source-git-commit: cb5f3b042c1902add9b22d28eb24e2b6e8f1a20b
workflow-type: tm+mt
source-wordcount: '607'
ht-degree: 28%

---

# Utilizzare l’API di limitazione di utilizzo {#work}

L’API di limitazione di utilizzo consente di creare, configurare e monitorare le configurazioni di limitazione di utilizzo.

Questa sezione fornisce informazioni globali su come lavorare con l’API. Una descrizione API dettagliata è disponibile in [Documentazione delle API di Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/).

## Descrizione API di limitazione

| Metodo | Percorso | Descrizione |
|---|---|---|
| [!DNL POST] | list/endpointConfigs | Ottieni un elenco delle configurazioni del limite dell’endpoint |
| [!DNL POST] | /endpointConfigs | Creare una configurazione di limitazione di endpoint |
| [!DNL POST] | /endpointConfigs/`{uid}`/deploy | Distribuire una configurazione di limitazione di endpoint |
| [!DNL POST] | /endpointConfigs/`{uid}`/undeploy | Annullare la distribuzione di una configurazione di limitazione di endpoint |
| [!DNL POST] | /endpointConfigs/`{uid}`/canDeploy | Controlla se è possibile distribuire o meno una configurazione di limitazione di endpoint |
| [!DNL PUT] | /endpointConfigs/`{uid}` | Aggiornare la configurazione della limitazione di un endpoint |
| [!DNL GET] | /endpointConfigs/`{uid}` | Recuperare la configurazione della limitazione di un endpoint |
| [!DNL DELETE] | /endpointConfigs/`{uid}` | Eliminare una configurazione di limitazione degli endpoint |

Quando viene creata o aggiornata una configurazione, viene eseguito automaticamente un controllo per garantire la sintassi e l’integrità del payload.
Se si verificano alcuni problemi, l’operazione restituisce un avviso o degli errori per facilitare la correzione della configurazione.

## Configurazione endpoint

Di seguito è riportata la struttura di base di una configurazione di endpoint:

```
{
    "url": "<endpoint URL>",  //wildcards are allowed in the endpoint URL
    "methods": [ "<HTTP method such as GET, POST, >, ...],
    "services": {
        "<service name>": { . //must be "action" or "dataSource" 
            "maxHttpConnections": <max connections count to the endpoint (optional)>
            "rating": {          
                "maxCallsCount": <max calls to be performed in the period defined by period/timeUnit>,
                "periodInMs": <integer value greater than 0>
            }
        },
        ...
    }
}
```

>[!IMPORTANT]
>
>Il **maxHttpConnections** Il parametro è facoltativo. Consente di limitare il numero di connessioni aperte da Journey Optimizer al sistema esterno.
>
>Il valore massimo impostabile è 400. Se non viene specificato nulla, il sistema può aprire più di migliaia di connessioni a seconda della scalabilità dinamica del sistema.

### Esempio:

```
`{
  "url": "https://api.example.org/data/2.5/*",
  "methods": [
    "GET"
  ],
  "services": {
    "dataSource": {
      "maxHttpConnections": 50,
      "rating": {
        "maxCallsCount": 500,
        "periodInMs": 1000
      }
    }
  },
  "orgId": "<IMS Org Id>"
}
```

## Avvertenze ed errori

Quando un **canDeploy** viene chiamato, il processo convalida la configurazione e restituisce lo stato di convalida identificato dal relativo ID univoco:

```
"ok" or "error"
```

I potenziali errori sono:

* **ERR_ENDPOINTCONFIG_100**: configurazione limite: url mancante o non valido
* **ERR_ENDPOINTCONFIG_101**: configurazione limite: url non valido
* **ERR_ENDPOINTCONFIG_102**: configurazione di limitazione: url non valido: wildchar nell’url non consentito in host:port
* **ERR_ENDPOINTCONFIG_103**: configurazione limite: metodi HTTP mancanti
* **ERR_ENDPOINTCONFIG_104**: configurazione limite: nessuna classificazione di chiamata definita
* **ERR_ENDPOINTCONFIG_107**: configurazione limite: numero massimo di chiamate non valido (maxCallsCount)
* **ERR_ENDPOINTCONFIG_108**: configurazione limite: numero massimo di chiamate non valido (periodInMs)
* **ERR_ENDPOINTCONFIG_111**: configurazione limite: impossibile creare la configurazione endpoint: payload non valido
* **ERR_ENDPOINTCONFIG_112**: configurazione limite: impossibile creare la configurazione endpoint: previsto un payload JSON
* **ERR_AUTHORING_ENDPOINTCONFIG_1**: nome di servizio non valido `<!--<given value>-->`: deve essere &quot;dataSource&quot; o &quot;action&quot;

Il potenziale avviso è:

**ERR_ENDPOINTCONFIG_106**: limite configurazione: numero massimo connessioni HTTP non definito: nessuna limitazione per impostazione predefinita

## Casi d’uso

In questa sezione trovi i cinque casi d’uso principali che puoi eseguire per gestire la configurazione dei limiti in [!DNL Journey Optimizer].

Per facilitare i test e la configurazione, [qui](https://raw.githubusercontent.com/AdobeDocs/JourneyAPI/master/postman-collections/Journey-Orchestration_Capping-API_postman-collection.json) è disponibile una raccolta Postman.

Questa raccolta Postman è stata configurata per condividere la raccolta di variabili Postman generata tramite __[Integrazioni della console di Adobe I/O](https://console.adobe.io/integrations) > Prova > Scarica per Postman__, che genera un file di ambiente Postman con i valori delle integrazioni selezionate.

Una volta scaricata e caricata in Postman, è necessario aggiungere tre variabili: `{JO_HOST}`,`{BASE_PATH}` e `{SANDBOX_NAME}`.
* `{JO_HOST}` : [!DNL Journey Optimizer] URL gateway
* `{BASE_PATH}` : punto di ingresso per l’API.
* `{SANDBOX_NAME}`: l’intestazione **x-sandbox-name** (ad esempio, “prod”) corrispondente al nome della sandbox in cui si svolgeranno le operazioni API. Per ulteriori informazioni, consulta la [panoramica delle sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=it).

Nella sezione seguente, è disponibile un elenco ordinato delle chiamate API REST per eseguire il caso d’uso.

Caso d’uso n. 1: **Creazione e distribuzione di una nuova configurazione dei limiti**

1. list
1. create
1. candeploy
1. deploy

Caso d’uso n. 2: **Aggiornare e distribuire una configurazione di limitazione di utilizzo non ancora distribuita**

1. list
1. get
1. update
1. candeploy
1. deploy

Caso d’uso n. 3: **Annullare la distribuzione ed eliminare una configurazione di limitazione distribuita**

1. list
1. undeploy
1. delete

Caso d’uso n. 4: **Elimina una configurazione di limite distribuita.**

È possibile annullare la distribuzione ed eliminare la configurazione in una sola chiamata API utilizzando il parametro forceDelete.
1. list
1. eliminare, con il parametro forceDelete

Caso d’uso n. 5: **Aggiornare una configurazione di limite già distribuita**

1. list
1. get
1. update
1. undeploy
1. candeploy
1. deploy
