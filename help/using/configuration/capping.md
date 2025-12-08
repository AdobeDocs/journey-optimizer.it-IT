---
solution: Journey Optimizer
product: journey optimizer
title: API di limitazione di utilizzo
description: Scopri come utilizzare l’API di limitazione di utilizzo
feature: Journeys, API
role: Developer
level: Beginner
keywords: esterno, API, ottimizzatore, limitazione
exl-id: 377b2659-d26a-47c2-8967-28870bddf5c5
source-git-commit: 0b0badfa09a24d451671f5bae9ddc437c6db2911
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 6%

---

# Utilizzare l’API di limitazione di utilizzo {#work}

L’API di limitazione di utilizzo consente di creare, configurare e monitorare le configurazioni di limitazione di utilizzo.

Questa sezione fornisce informazioni globali su come lavorare con l’API. Una descrizione API dettagliata è disponibile nella [documentazione delle API Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}.

## Descrizione API di limitazione e raccolta Postman {#description}

Nella tabella seguente sono elencati i comandi disponibili per l’API di limitazione di utilizzo. Informazioni dettagliate, inclusi esempi di richieste, parametri e formati di risposta, sono disponibili nella [documentazione delle API di Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/journeys-throttling/){target="_blank"}.

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

Inoltre, una raccolta Postman è disponibile [qui](https://github.com/AdobeDocs/JourneyAPI/blob/master/postman-collections/Journeys_Capping-API_postman-collection.json) per aiutarti nella configurazione di test.

Questa raccolta è stata configurata per condividere la raccolta di variabili Postman generata tramite __[Integrazioni della console Adobe I/O](https://console.adobe.io/integrations) > Prova > Scarica per Postman__, che genera un file di ambiente Postman con i valori di integrazione selezionati.

Una volta scaricata e caricata in Postman, è necessario aggiungere tre variabili: `{JO_HOST}`,`{BASE_PATH}` e `{SANDBOX_NAME}`.

* `{JO_HOST}` : [!DNL Journey Optimizer] URL gateway.
* `{BASE_PATH}`: punto di ingresso per l&#39;API.
* `{SANDBOX_NAME}`: l’intestazione **x-sandbox-name** (ad esempio, “prod”) corrispondente al nome della sandbox in cui si svolgeranno le operazioni API. Per ulteriori informazioni, consulta la [panoramica delle sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=it){target="_blank"}.

## Configurazione endpoint

Di seguito è riportata la struttura di base di una configurazione di endpoint:

```json
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
>Il parametro **maxHttpConnections** è facoltativo. Consente di limitare il numero di connessioni aperte da Journey Optimizer al sistema esterno.
>
>Il valore massimo impostabile è 400. Se non viene specificato nulla, il sistema può aprire più di migliaia di connessioni a seconda della scalabilità dinamica del sistema.
>
>Durante la distribuzione della configurazione dei limiti, se non è stato impostato alcun valore `maxHttpConnections`, viene aggiunto un valore predefinito `maxHttpConnections = -1` alla configurazione distribuita e Journey Optimizer utilizza il valore predefinito di sistema.

Esempio:

```json
{
  "url": "https://api.example.org/data/2.5/*",
  "methods": [
    "GET"
  ],
  "services": {
    "dataSource": {
      "rating": {
        "maxCallsCount": 500,
        "periodInMs": 1000
      }
    }
  }
}
```

>[!IMPORTANT]
>
>La configurazione sarà attiva solo dopo aver chiamato l&#39;endpoint **deploy**.

## Avvertenze ed errori

Quando viene chiamato un metodo **canDeploy**, il processo convalida la configurazione e restituisce lo stato di convalida identificato dal relativo ID univoco:

```json
"ok" or "error"
```

I potenziali errori sono:

* **ERR_ENDPOINTCONFIG_100**: configurazione limite: URL mancante o non valido
* **ERR_ENDPOINTCONFIG_101**: configurazione limite: URL non valido
* **ERR_ENDPOINTCONFIG_102**: configurazione limite: URL non valido: wildchar nell&#39;URL non consentito nell&#39;host:port
* **ERR_ENDPOINTCONFIG_103**: configurazione limite: metodi HTTP mancanti
* **ERR_ENDPOINTCONFIG_104**: configurazione limite: nessuna classificazione di chiamata definita
* **ERR_ENDPOINTCONFIG_107**: configurazione limite: numero massimo di chiamate non valido (maxCallsCount)
* **ERR_ENDPOINTCONFIG_108**: configurazione limite: numero massimo di chiamate non valido (periodInMs)
* **ERR_ENDPOINTCONFIG_111**: configurazione limite: impossibile creare la configurazione endpoint: payload non valido
* **ERR_ENDPOINTCONFIG_112**: configurazione limite: impossibile creare la configurazione dell&#39;endpoint: previsto un payload JSON
* **ERR_AUTHORING_ENDPOINTCONFIG_1**: nome di servizio `<!--<given value>-->` non valido: deve essere &#39;dataSource&#39; o &#39;action&#39;

Il potenziale avviso è:

**ERR_ENDPOINTCONFIG_106**: configurazione limite: numero massimo di connessioni HTTP non definite: nessuna limitazione per impostazione predefinita

## Casi d’uso

In questa sezione sono elencati i casi d&#39;uso chiave per la gestione delle configurazioni di limitazione di utilizzo in [!DNL Journey Optimizer] e i comandi API associati necessari per implementare il caso d&#39;uso.

I dettagli su ciascun comando API sono disponibili nella [descrizione API e raccolta Postman](#description).

+++Creare e distribuire una nuova configurazione dei limiti

Chiamate API per l’utilizzo di:

1. **`list`** - Recupera le configurazioni esistenti.
1. **`create`** - Crea una nuova configurazione.
1. **`candeploy`** - Controlla se la configurazione può essere distribuita.
1. **`deploy`** - Distribuisce la configurazione.

+++

+++Aggiornare e distribuire una configurazione dei limiti (non ancora distribuita)

Chiamate API per l’utilizzo di:

1. **`list`** - Recupera le configurazioni esistenti.
1. **`get`** - Recupera i dettagli di una configurazione specifica.
1. **`update`** - Modifica la configurazione.
1. **`candeploy`** - Verifica l&#39;idoneità alla distribuzione.
1. **`deploy`** - Distribuisce la configurazione.

+++

+++Annullare la distribuzione ed eliminare una configurazione di limitazione distribuita

Chiamate API per l’utilizzo di:

1. **`list`** - Recupera le configurazioni esistenti.
1. **`undeploy`** - Annulla la distribuzione della configurazione.
1. **`delete`** - Rimuove la configurazione.

+++

+++Eliminare una configurazione di limitazione distribuita in un unico passaggio

In una sola chiamata API è possibile annullare la distribuzione ed eliminare la configurazione utilizzando il parametro `forceDelete`.

Chiamate API per l’utilizzo di:

1. **`list`** - Recupera le configurazioni esistenti.
1. **`delete`(con il parametro `forceDelete`)** - Forza l&#39;eliminazione di una configurazione distribuita in un singolo passaggio.

+++

+++Aggiornare una configurazione di limite già distribuita

>[!NOTE]
>
>È necessaria una ridistribuzione dopo l’aggiornamento di una configurazione già distribuita.

Chiamate API per l’utilizzo di:

1. **`list`** - Recupera le configurazioni esistenti.
1. **`get`** - Recupera i dettagli di una configurazione specifica.
1. **`update`** - Modifica la configurazione.
1. **`undeploy`** - Annulla la distribuzione della configurazione prima di applicare le modifiche.
1. **`candeploy`** - Verifica l&#39;idoneità alla distribuzione.
1. **`deploy`** - Distribuisce la configurazione aggiornata.

+++
