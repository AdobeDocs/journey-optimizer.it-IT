---
solution: Journey Optimizer
product: journey optimizer
title: Passaggi aggiuntivi per inviare eventi a un percorso
description: Scopri ulteriori passaggi per inviare eventi a un percorso
feature: Journeys, Events
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: passaggi, configurazione, percorso, eventi, flusso, API
exl-id: e0144151-6c54-4656-9650-b544d8e7be16
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 5%

---

# Passaggi aggiuntivi per l’invio di eventi {#additional-steps-to-send-events}

Per configurare gli eventi da inviare a **[!UICONTROL API Streaming Ingestion]** e da utilizzare in [!DNL Journey Optimizer], è necessario seguire questi passaggi:

1. Ottieni l’URL di ingresso dalle API di Adobe Experience Platform. Ulteriori informazioni in [Panoramica delle API Streaming Ingestion](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=it){target="_blank"}.
1. Copiare il payload dall’anteprima del payload in **[!UICONTROL Evento]** menu. Per ulteriori informazioni, consulta [questa pagina](../event/about-creating.md#define-the-payload-fields).

Quindi devi configurare il sistema di dati che invia gli eventi alle API Streaming Ingestion utilizzando il payload copiato:

1. Imposta una chiamata API POST all’URL delle API Streaming Ingestion (chiamata entrata).
1. Utilizza il payload copiato da [!DNL Journey Optimizer] nel corpo (&quot;sezione dati&quot;) della chiamata API alle API Streaming Ingestion. Vedi di seguito per un esempio
1. Determina dove ottenere tutte le variabili presenti nel payload. Esempio: se l’evento deve trasmettere l’indirizzo, il payload incollato mostrerà &quot;address&quot;: &quot;string&quot;. &quot;string&quot; deve essere sostituito dalla variabile che compilerà automaticamente il valore corretto, l’e-mail della persona a cui inviare un messaggio. Nell’anteprima del payload, nella sezione **[!UICONTROL Intestazione]** , vengono compilati automaticamente molti valori che dovrebbero facilitare il tuo lavoro.
1. Seleziona &quot;application/json&quot; come tipo di corpo.
1. Passa l’ID organizzazione nell’intestazione utilizzando la chiave &quot;x-gw-ims-org-id&quot;. Per il valore, utilizza l’ID organizzazione (&quot;XXX@AdobeOrg&quot;).

Ecco un esempio di evento Streaming Ingestion APIs:

```
{
    "header": {
        "msgType": "xdmEntityCreate",
        "msgId": "c25585b9-252e-431d-b562-e73da70c04e7",
        "msgVersion": "1.0",
        "xactionId": "f5995abe-c49d-4848-9577-a7a4fc2996fb",
        "datasetId": "string - required if you want the data to land in a specific dataset - not mandatory",
        "imsOrgId": "XXX@AdobeOrg",
        "schemaRef": {
            "id": "XXX",
            "contentType": "application/vnd.adobe.xed-full+json;version=1"
        },
        "source": {
            "name": "Journeys"
        }
    },
    "body": {
        "xdmMeta": {
            "schemaRef": {
                "id": "XXX",
                "contentType": "application/vnd.adobe.xed-full+json;version=1"
            }
        },
        "xdmEntity": {
            "_instance_name": {
                "person": {
                    "firstName": "string",
                    "lastName": "string",
                    "gender": "string",
                    "birthYear": 10,
                    "emailAddress": "string"
                }
            },
            "identityMap": {
                "Email": [
                {
                    "id": "string"
                    }
                ]
            },
            "_id": "string",
            "timestamp": "2018-05-29T00:00:00.000Z",
            "_experience": {
                "campaign": {
                    "orchestration": {
                    "eventID": "XXX"
                    }
                }
            }
        }
    }
}
```

Per facilitare l’identificazione del punto in cui incollare la parte &quot;dati&quot;, puoi utilizzare uno strumento di visualizzazione JSON come [Formattatore JSON](https://jsonformatter.curiousconcept.com){target="_blank"}.

Per risolvere i problemi relativi alle API Streaming Ingestion, consulta [Documentazione di Experienci Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html){target="_blank"}.
